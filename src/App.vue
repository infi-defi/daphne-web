<template>
  <Home/>
</template>

<script>
import Home from './components/home/Home.vue'

export default {
  name: 'App',
  components: {
    Home
  }
}
</script>

<style>
:root {
  --dark: #19171e;
  --text: #b8c0c9;
  --brand: #c91f58;
  --par: #b6bec6;
}

body {
  background-color: var(--dark);
  height: 100%;
  font-family: "Poppins", Helvetica, Arial, sans-serif;
}

::selection {
  background: var(--brand); /* WebKit/Blink Browsers */
  color: white;
}

::-moz-selection {
  background: var(--brand); /* Gecko Browsers */
  color: white;
}

.subtitle:hover {
  cursor: text;
  color: var(--text-color);
}

.title {
  color: white !important;
}
</style>
