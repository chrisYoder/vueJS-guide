<template>
  <div>
    <h4>Computed vs Watched Property</h4>
    <ul>
      <li>Vue provides a more generic way to observe and react to data changes on a Vue instance via watch properties</li>
      
      <li>However, this code is imperative and repetitive unlike its computed property cousin {{ fullNameC }}</li>
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
    fullNameC: function() {
      return this.firstName + " " + this.lastName;
    }
  }
};
</script>

<style>
</style>

