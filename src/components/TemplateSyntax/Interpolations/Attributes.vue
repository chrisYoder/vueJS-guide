<template>
  <div>
    <h4>Attributes</h4>
    <ul>
      <li>Mustaches cannot be used inside HTML attributes. Instead use v-bind.</li>
      <li>V-bind:
        <ul>
          <li>dynamically bind one or more attributes or a component prop to an expression.</li>
          <li>
            When used with
            <code>class</code> or
            <code>style</code> attributes Array and Object data types are supported.
          </li>
          <li>When used with a boolean attribute the mere existence implies true.</li>
        </ul>
      </li>
    </ul>
    <div>
      <p>Example 0</p>
      <div v-bind:id="dynamicID">The id is {{ dynamicID }}</div>
      <p>Example 1</p>
      <div>
        <button v-bind:disabled="isButtonDisabled">Button is Disabled</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      dynamicID: "thisIsADynamicID",
      isButtonDisabled: true
    };
  }
};
</script>

<style>
</style>


