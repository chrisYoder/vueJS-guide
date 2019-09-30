<template>
  <div>
    <h4>Computed Setter</h4>
    <ul>
      <li>computed properties are by default getter-only but you can provide a setter when you need it.</li>
      <li>getter: binds an{} bject property to a function that will be called when that property is looked up.</li>
      <li>setter: binds an object property to a function to be called when there is an attempt to set that property.</li>
      <li>Example:</li>
      <ul>
        <li>Full name: {{ fullName }}</li>
      </ul>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      firstName: "Arya",
      lastName: "Yoder"
    };
  },

  computed: {
    fullName: {
      get: function() {
        return `${this.firstName} ${this.lastName}`;
      },

      set: function(newValue) {
        let names = newValue.split("");
        this.firstName = names[0];
        this.lastName = names[names.length - 1];
      }
    }
  }
};
</script>

<style>
</style>

