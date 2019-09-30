<template>
  <div>
    <h4>Basic Example</h4>
    <ul>
      <li>While in-template expressions are nice they are meant for simple operations. Too much logic in the templates makes them bloated and hard to maintain</li>
      <li>Template should be simple and declarative</li>
      <li>Complex logic should be located in a computed property</li>
      <li>Example:</li>
      <ul>
        <li>Message: {{ message }}</li>
        <li>Reversed Message: {{ reversedMessage }}</li>
        <li>
          <button @click="changeMessage">Click here</button>
        </li>
      </ul>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: "Go Cowboys Go",
      count: 1
    };
  },

  computed: {
    // a computed getter
    reversedMessage: function() {
      return this.message
        .split("")
        .reverse()
        .join("");
    }
  },

  methods: {
    changeMessage: function() {
      this.count++;
      if (this.count % 2 === 0) {
        this.message = "Go Spurs Go";
      } else {
        this.message = "Go Cowboys Go";
      }
    }
  }
};
</script>

<style>
</style>

