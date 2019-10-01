<template>
  <div>
    <h4>Multiple Values</h4>
    <p>
      You can provide an array of multiple prefixed values to a style property. Vue will only render the last value value in the array which the browser support.
      For example,
      <code>:style="{display: ['-webkit-box', '-ms-flexbox', 'flex']}"</code> will render
      <code>display: flex</code>
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  }
};
</script>

<style>
</style>

