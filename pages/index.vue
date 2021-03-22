<template>
<div>
  <h1>Welcome to My first Nuxt App</h1>
  <Contenido/>
  
  
 </div>
</template>

<script>

import Contenido from "@/components/Content.vue";
//import Posts "../../components/Posts";
export default {
  head() {
    return {
      title: "Posts App | Home",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Website abut tutorials"
        }
      ],
      htmlAttrs: {
        lang: "en"
      }
    };
  },
   components: {
    Contenido
  }
};
</script>


<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
