<template>
  <div id="app">
    <h1>
      <a href="https://vuejs.org/v2/guide/">Vue.js Official Guide</a>
    </h1>
    <section-one/>
    <section-two/>
  </div>
</template>

<script>
import SectionOne from "./components/TemplateSyntax/SectionOne";
import SectionTwo from './components/ComputedPropertiesAndWatchers/SectionTwo';

export default {
  name: "App",
  components: {
    SectionOne, 
    SectionTwo
  }
};
</script>

<style>
:root {
  --philosopher: "Philosopher", sans-serif;
  --blue: #0e1a40;
  --bronze: #946b2d;
}
#app {
  font-family: var(--philosopher);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: var(--blue);
}

h1,
h2,
h3 {
  text-align: center;
}

h4 {
  color: var(--bronze);
}

.section {
  border: 1px solid black;
  border-radius: 5px;
  padding: 5px;
  box-shadow: 3px 3px 7px black;
  margin-top: 2em;
}

a {
  color: var(--blue);
  text-decoration: none;
}
</style>
