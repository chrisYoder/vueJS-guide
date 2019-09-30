<template>
  <div>
    <h4>Arguments</h4>
    <ul>
      <li>Some directives can take an 'argument' which is denoted by a colon after the directive name.</li>
      <li>Examples:</li>
      <ul>
        <li>
          We can use
          <code>v-bond:href="url"</code> to reactively update an HTML update
        </li>
        <li>
          short hand method for bind is
          <code>:href</code>
        </li>
        <li>Examples: </li>
        <ul>
          <li>
            <a :href="url">{{url}}</a>
          </li>
        </ul>
        <li>
          We can also use
          <code>v-on:click="doSomething"</code> to listen to DOM events
        </li>
        <li>
          Short hand method for
          <code>v-on</code> is @event
        </li>
        <li>Examples:</li>
        <ul>
          <li>
            <span id="changeColorText">Change the color of this text</span>&nbsp;
            <button @click="changeColor">Click to change color</button>
          </li>
        </ul>
      </ul>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      url: "https://vuejs.org/"
    };
  },

  methods: {
    changeColor: function() {
      let el = document.getElementById("changeColorText");

      if (el.style.color === "rgb(14, 26, 64)") {
        el.style.color = "rgb(148, 107, 45)";
      } else {
        el.style.color = "rgb(14, 26, 64)";
      }
    }
  }
};
</script>

<style>
</style>

