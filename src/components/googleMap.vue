<template>
    <div class="map-wrap">
      <a href="https://www.maptiler.com" class="watermark"><img
          src="https://api.maptiler.com/resources/logo.svg" alt="MapTiler logo"/></a>
      <div class="map" ref="mapContainer"></div>
    </div>
  </template>
  
  <script>
  import { Map } from 'maplibre-gl';
  import { shallowRef, onMounted, onUnmounted, markRaw } from 'vue';
  
  export default {
    name: "googleMap",
    setup () {
      const mapContainer = shallowRef(null);
      const map = shallowRef(null);
  
      onMounted(() => {
        const apiKey = "qA6ZFFNaF9aKr7T0TEoy";
  
        const initialState = { lng: 139.753, lat: 35.6844, zoom: 14 };
  
        map.value = markRaw(new Map({
          container: mapContainer.value,
          style: `https://api.maptiler.com/maps/streets-v2/style.json?key=${apiKey}`,
          center: [initialState.lng, initialState.lat],
          zoom: initialState.zoom
        }));
  
      }),
      onUnmounted(() => {
        map.value?.remove();
      })
  
      return {
        map, mapContainer
      };
    }
  };
  </script>
  
  
  <style>
  @import '~maplibre-gl/dist/maplibre-gl.css';
  
  .map-wrap {
    position: relative;
    width: 500px;
    height: 500px;
    border:  1px solid #000;
  }
  
  .map {
    position: absolute;
    width: 100%;
    height: 100%;
  }
  
  .watermark {
    position: absolute;
    left: 10px;
    bottom: 10px;
    z-index: 999;
  }
  </style>