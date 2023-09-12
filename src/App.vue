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
        "I am a passionate web developer with a strong background in vue 3. With
        1 years of experience, I have honed my skills in web development, and I'm constantly seeking opportunities to
        innovate and grow.

        My work is driven by a commitment to excellence, attention to detail, and a deep desire to solve problems. I
        thrive in collaborative environments, and my ability to communicate complex ideas clearly makes me a valuable team
        member.

        I've had the privilege to work on projects in deans, and I'm eager
        to take on new challenges that allow me to push my boundaries and contribute to meaningful work.

        I'm excited to connect with like-minded individuals and organizations to embark on new adventures and create
        lasting impacts. Let's collaborate and bring ideas to life."
      </p>
    </div>
  </section>

  <section class="work" id="work">
    <h2>My Resumé</h2>
    <div class="main">
      <!-- <div class="education">
        <h2>Education</h2>
      </div> -->
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

  <footer>
    <ul>
      <li>
        <span>
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <path
              d="M6.94048 4.99993C6.94011 5.81424 6.44608 6.54702 5.69134 6.85273C4.9366 7.15845 4.07187 6.97605 3.5049 6.39155C2.93793 5.80704 2.78195 4.93715 3.1105 4.19207C3.43906 3.44699 4.18654 2.9755 5.00048 2.99993C6.08155 3.03238 6.94097 3.91837 6.94048 4.99993ZM7.00048 8.47993H3.00048V20.9999H7.00048V8.47993ZM13.3205 8.47993H9.34048V20.9999H13.2805V14.4299C13.2805 10.7699 18.0505 10.4299 18.0505 14.4299V20.9999H22.0005V13.0699C22.0005 6.89993 14.9405 7.12993 13.2805 10.1599L13.3205 8.47993Z">
            </path>
          </svg>
        </span> linkedin.com
      </li>
      <li>
        <span>
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <path
              d="M14 13.5H16.5L17.5 9.5H14V7.5C14 6.47062 14 5.5 16 5.5H17.5V2.1401C17.1743 2.09685 15.943 2 14.6429 2C11.9284 2 10 3.65686 10 6.69971V9.5H7V13.5H10V22H14V13.5Z">
            </path>
          </svg>
        </span> facebook.com
      </li>
      <li>
        <span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <path
              d="M12.001 2C6.47598 2 2.00098 6.475 2.00098 12C2.00098 16.425 4.86348 20.1625 8.83848 21.4875C9.33848 21.575 9.52598 21.275 9.52598 21.0125C9.52598 20.775 9.51348 19.9875 9.51348 19.15C7.00098 19.6125 6.35098 18.5375 6.15098 17.975C6.03848 17.6875 5.55098 16.8 5.12598 16.5625C4.77598 16.375 4.27598 15.9125 5.11348 15.9C5.90098 15.8875 6.46348 16.625 6.65098 16.925C7.55098 18.4375 8.98848 18.0125 9.56348 17.75C9.65098 17.1 9.91348 16.6625 10.201 16.4125C7.97598 16.1625 5.65098 15.3 5.65098 11.475C5.65098 10.3875 6.03848 9.4875 6.67598 8.7875C6.57598 8.5375 6.22598 7.5125 6.77598 6.1375C6.77598 6.1375 7.61348 5.875 9.52598 7.1625C10.326 6.9375 11.176 6.825 12.026 6.825C12.876 6.825 13.726 6.9375 14.526 7.1625C16.4385 5.8625 17.276 6.1375 17.276 6.1375C17.826 7.5125 17.476 8.5375 17.376 8.7875C18.0135 9.4875 18.401 10.375 18.401 11.475C18.401 15.3125 16.0635 16.1625 13.8385 16.4125C14.201 16.725 14.5135 17.325 14.5135 18.2625C14.5135 19.6 14.501 20.675 14.501 21.0125C14.501 21.275 14.6885 21.5875 15.1885 21.4875C19.259 20.1133 21.9999 16.2963 22.001 12C22.001 6.475 17.526 2 12.001 2Z">
            </path>
          </svg></span> github.com
      </li>
      <li>
        <span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <path
              d="M18.2048 2.25H21.5128L14.2858 10.51L22.7878 21.75H16.1308L10.9168 14.933L4.95084 21.75H1.64084L9.37084 12.915L1.21484 2.25H8.04084L12.7538 8.481L18.2048 2.25ZM17.0438 19.77H18.8768L7.04484 4.126H5.07784L17.0438 19.77Z">
            </path>
          </svg></span> twitter.com
      </li>
    </ul>
    &copy; bestdev.com
  </footer>
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
  align-iztems: center;
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

.contact {
  display: grid;
  place-items: center;
  width: 100%;
  padding: 0 30px;
  align-items: center;
  height: 400px;
  margin-top: 30px;
}

.contact section {
  display: flex;
  justify-content: space-between;
  width: 95%;
}

.contact .header {
  width: 40%;
  display: grid;
  place-items: center;
  margin-bottom: 30px;
}

.contact .form {
  width: 60%;
  display: grid;
  place-items: center;
  margin-right: -20px;
}

.contact .form form {
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

.contact .form form input {
  width: 80%;
  height: 40px;
  padding-left: 10px;
  margin-bottom: 15px;
  border-radius: 5px;
  border: 1px solid#000;
}

.contact .form form textarea {
  width: 80%;
  height: 100px;
  padding-left: 10px;
  margin-bottom: 15px;
  border-radius: 5px;
  border: 1px solid#000;
  padding-top: 10px;
  font-size: 18px;
}

.contact .form form button {
  border: none;
  width: 40%;
  height: 40px;
  background: #6969ee;
  border-radius: 50px;
  color: #000;
  margin-bottom: -20px;
}

footer {
  width: 100%;
  height: 150px;
  display: grid;
  place-items: center;
  background: #6969ee;
  color: #fff;
  margin-top: 120px;
}
footer ul{
  display: flex;
  margin-left: 10px;
  align-items: center;
  justify-content: center;
}
footer ul li{
  list-style: none;
  margin-right: 10px;
}
footer ul li span svg{
  height: 30px;
  margin-bottom: -8px;
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

  .about .description {
    width: 100%;

  }

  .work {
    display: grid;
    place-items: center;
    width: 100%;
  }

  .work .main {
    display: grid;
    place-items: center;
    width: 100%;
  }

  .work .main .skill,
  .work .main .education {
    width: 350px;
  }

  .contact {
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
  .contact section {
    display: grid;
    width: 100%;
    place-items: center;
  }

  .contact .header {
    width: 400px;
    display: grid;
    place-items: center;
    margin-top: 30px;
  }

  .contact .form {
    display: grid;
    place-items: center;
    width: 100%;
  }

  .contact .form form {
    width: 100%;
    height: 300px;
    margin-top: 20px;
  }
  footer{
    height: 170px;
  }

}

@media screen and (max-width: 800px) {
  .contact {
    width: 100%;
    display: grid;
    place-items: center;
  }

  .contact section {
    display: grid;
    width: 100%;
    place-items: center;
  }
}</style>
