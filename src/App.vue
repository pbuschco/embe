<template>
  <div id="app">
    <div class="iframe-container">
      <iframe
        :src="iframeSrc"
        frameborder="0"
        scrolling="no"
        seamless>
      </iframe>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      iframeSrc: "https://embeds.beehiiv.com/070131cf-be7b-481f-8e65-71fcc936e0f2", // Initial source
    };
  },
};
</script>

<style>
/* Ensure the app container fills the entire viewport */
#app {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image:none;
}

/* Make the iframe responsive and full-screen */
.iframe-container {
  width: 100%; /* Full width */
  height: 100%; /* Full height */
  overflow: hidden; /* Prevent scrollbars inside the iframe container */
}

.iframe-container iframe {
  width: 100%; /* Match container's width */
  height: 100%; /* Match container's height */
  border: 0; /* Remove border */
  background-color: transparent;
  overflow: hidden; /* Prevent scrollbars */
}
</style>
