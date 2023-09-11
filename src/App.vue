<template>
  <div class="navbar">
    <div class="logo">My Portfolio</div>

    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#work">Resumé</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </div>

  <section class="body" id="home">
    <h2>Welcome To My Portfolio</h2>
  </section>

  <section class="about" id="about">
    <div class="image">input an image</div>
    <div class="description">
      <h2>About Me</h2>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi odio
        porro optio similique? Sint iure a ccusantium dolorem pariatur
        voluptatem consequatur r epellendus quasi? Officia fugit ducimus culpa,
        nulla deleniti, placeat quis temporibus, accusantium cum a ut minus
        dignissimos soluta veritatis numquam illo? Deleniti hic, voluptatibus
        necessitatibus nulla ex r atione commodi suscipit accusantium. Lorem
        ipsum, dolor sit amet consectetur adipisicing elit. Necessitatibus quo
        corporis explicabo facere a rerum, quibusdam veniam impedit! Magni
        impedit vel repudiandae ex dolorem animi assumenda odio placeat
        voluptatibus! Odit, quibusdam consequuntur dolore tenetur, veritatis
        nisi at reiciendis nemo natus molestiae officia perspiciatis delectus
        suscipit iste, ex voluptate tempora ea.
      </p>
    </div>
  </section>

  <section class="work" id="work">
    <h2>My Resumé</h2>
    <div class="main">
      <div class="education">
        <h2>Education</h2>
      </div>
      <div class="skill">
        <h2>Skills</h2>

        <div>
          HTML - 100%
          <div class="rating">
            <div class="html"></div>
          </div>
        </div>
        <div>
          CSS - 90%
          <div class="rating">
            <div class="css"></div>
          </div>
        </div>
        <div>
          Vue 3 - 80%
          <div class="rating">
            <div class="vue"></div>
          </div>
        </div>
      </div>
    </div>
  </section>

  
  <section class="contact" id="contact">
    <div class="header">
    <h2>Contact Me</h2>
  </div>
    <section>
        <googleMap />
      <div class="form">
        <form action="" method="post">
          <input v-model="text" placeholder="Fullname" required>
          <input v-model="email" placeholder="Email Address" required>
          <textarea v-model="message" placeholder="message"></textarea>
          
          <button type="submit">Submit</button>
        </form>
      </div>
    </section>
  </section>
</template>

<script>
import googleMap from './components/googleMap.vue'

export default {
  components: {
    googleMap
  }
}

</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #6969ee;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 60px;
  box-shadow: 0 0 5px 0 #000;
  padding: 0 10px;
  z-index: 999;
}

.logo {
  font-size: 24px;
  font-weight: 600;
}

.navbar ul {
  display: flex;
  margin-right: 20px;
}
.navbar ul li {
  list-style: none;
  margin-right: 20px;
}
.navbar ul li a {
  text-decoration: none;
  color: black;
  transition: 0.3s ease;
}
.navbar ul li a:hover {
  color: #fff;
}

.body {
  margin-top: 60px;
  width: 100%;
  height: 500px;
  background: #8585f3;
  display: grid;
  place-items: center;
  margin-bottom: 20px;
}
.body h2 {
  font-size: 28px;
}
.about {
  display: flex;
  justify-content: space-between;
  padding: 0 20px;
  width: 100%;
  margin-bottom: 30px;
}
.about .image {
  width: 25%;
  display: grid;
  place-items: center;
  border: 1px solid #000;
  height: 300px;
  margin-top: 50px;
  margin-left: 30px;
}
.about .description {
  width: 60%;
  display: grid;
  place-items: center;
  height: 400px;
}
.about .description p {
  margin-top: -20px;
}
.about .description h2,
.work h2,
.contact .header h2 {
  font-size: 28px;
  color: #6969ee;
}
.work {
  width: 100%;
  height: 500px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin-bottom: 30px;
}
.work .main {
  height: 480px;
  /* border: 1px solid#000; */
  width: 80%;
  margin-top: 20px;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}
.work .main .skill,
.work .main .education {
  height: 90%;
  width: 40%;
  border-radius: 20px;
  box-shadow: 0 0 4px 0 #000;
  padding: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.work .main .skill {
  flex-direction: column;
  justify-content: space-evenly;
}
.work .main .skill .rating {
  width: 200px;
  height: 15px;
  border: 1px solid#000;
  border-radius: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: px 0;
}
.work .main .skill .rating .html {
  width: 100%;
  height: 14px;
  border-radius: inherit;
  background-color: #6969ee;
}
.work .main .skill .rating .css {
  width: 90%;
  height: 14px;
  margin-left: -10%;
  border-radius: inherit;
  background-color: #6969ee;
}
.work .main .skill .rating .vue {
  width: 85%;
  height: 14px;
  margin-left: -15%;
  border-radius: inherit;
  background-color: #6969ee;
}
.contact{
  display: grid;
  place-items: center;
  width: 100%;
  padding: 0 30px;
  align-items: center;
  height: 400px;
  margin-top: 30px;
}
.contact section{
  display: flex;
  justify-content: space-between;
  width: 95%;
}
.contact .header{
  width: 40%;
  display: grid;
  place-items: center;
  margin-bottom: 30px;
}
.contact .form{
  width: 60%;
  display: grid;
  place-items: center;
  margin-right: -20px;
}
.contact .form form{
  width: 70%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 20px;
  box-shadow: 0 0 4px 0#000;
  height: 400px;
  padding: 20px;
}
.contact .form form input{
  width: 80%;
  height: 40px;
  padding-left: 10px;
  margin-bottom: 15px;
  border-radius: 5px;
  border: 1px solid#000;
}
.contact .form form textarea{
  width: 80%;
  height: 100px;
  padding-left: 10px;
  margin-bottom: 15px;
  border-radius: 5px;
  border: 1px solid#000;
  padding-top: 10px;
  font-size: 18px;
}
.contact .form form button{
  border: none;
  width: 40%;
  height: 40px;
  background: #6969ee;
  border-radius: 50px;
  color: #000;
  margin-bottom: -20px;
}

@media screen and (max-width: 900px) {
  .about {
  display: grid;
  place-items: center;
  width: 100%;
}
.about .image {
  width: 70%;
}
.about .description{
  width: 100%;

}
.work{
  display: grid;
  place-items: center;
  width: 100%;
}
.work .main{
  display: grid;
  place-items: center;
  width: 100%;
}
.work .main .skill,
.work .main .education {
  width: 350px;
}
.contact{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 800px;
}
/* .contact{
    width: 100%;
    display: grid;
    place-items: center;
  } */
  .contact section{
  display: grid;
  width: 100%;
  place-items: center;
}

.contact .header{
  width: 400px;
  display: grid;
  place-items: center;
  margin-top: 30px;
}
.contact .form{
  display: grid;
  place-items: center;
  width: 100%;
}
.contact .form form{
  width: 100%;
  height: 300px;
  margin-top: 20px;
}

}
@media screen and (max-width: 800px) {
  .contact{
    width: 100%;
    display: grid;
    place-items: center;
  }
  .contact section{
  display: grid;
  width: 100%;
  place-items: center;
}
}
</style>
