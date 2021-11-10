<template>
  <Home />
</template>

<script>
import Home from "./components/home/Home.vue";

export default {
  name: "App",
  components: {
    Home,
  },
};
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

.card {
  border-radius: 5px;
  background: var(--dark);
  color: white;
  padding: 20px 30px;
  box-shadow: rgba(0, 0, 0, 0.06) 0px 2px 4px;
  transition: all 0.3s ease-in-out;
}

.card:hover {
  box-shadow: rgba(0, 0, 0, 0.22) 0px 19px 43px;
  transform: translate3d(0px, -5px, 0px);
}

.col-ml {
  margin-left: 0.75rem !important;
}

.col-mr {
  margin-right: 0.75rem !important;
}

@media screen and (max-width: 1080px) {
  .col-ml {
    margin-left: 0 !important;
  }

  .col-mr {
    margin-right: 0 !important;
  }
}

.button {
  background-color: var(--brand);
  border-color: var(--brand);
  color: white;
}

.button:hover,
.button:focus {
  background-color: var(--brand);
  border-color: var(--brand);
  color: white;
}
</style>
