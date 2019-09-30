<template>
  <div>
    <h4>Computed Caching vs Methods</h4>
    <ul>
      <li>We can acheive the same result by invoking a method in the expression ( {{ text }} )</li>
      <li>Example:</li>
      <ul>
        <li>Message: {{ message }}</li>
        <li>Reversed Message: {{ reverseMessageMethod() }}</li>
      </ul>
      <li>The difference between Computed Properties and Methods are:</li>
      <ul>
        <li>Computed Properties:</li>

        <ul>
          <li>Cached based on their reactive dependencies</li>
          <li>This means that if we call reversedMessageComputed multiple times it won't change until message is change</li>
          <li>{{ reverseMessageComputed }}, {{ reverseMessageComputed }}</li>
          <li>Another example is creating a date using
            <code>Date.now()</code> as a computed Method because it is not a reactive dependency
          </li>
          <li>Re-render at {{ nowComputed }}</li>
        </ul>
        <li>Method Invocation</li>
        <ul>
          <li>Whenever we have a method invocation will always run the function whenever a re-render happens</li>
          <li>Re-render at {{ nowMethod() }}</li>
          <li>{{ reverseMessageMethod() }} {{ reverseMessageMethod() }}</li>
        </ul>
        <li>We would want to use a computed property when the situation requires us to loop through a large array and doing a lot of computations, or other similar situations, where running the function at each re-render would be inefficient</li>
      </ul>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: "{{ reverseMessage() }}",
      message: "Sanderson is the greatest living fantasy author (GLFA)"
    };
  },

  computed: {
    reverseMessageComputed: function() {
      return this.message
        .split("")
        .reverse("")
        .join("");
    },

    nowComputed: function() {
      return Date.now().toLocaleString();
    }
  },

  methods: {
    reverseMessageMethod: function() {
      return this.message
        .split("")
        .reverse()
        .join("");
    },

    nowMethod: function() {
      return Date.now().toLocaleString();
    }
  }
};
</script>

<style>
</style>

