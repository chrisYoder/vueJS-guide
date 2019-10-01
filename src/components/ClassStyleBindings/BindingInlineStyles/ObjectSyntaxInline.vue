<template>
  <div>
    <h4>Object Syntax Inline Styles</h4>
    <ul>
      <li>The object syntax for
        <code>v-bind:style</code> is pretty much like CSS except that it is a JS object.
      </li>
      <li>You can use either camelCase or kebab-case (with quotes)</li>
      <li>Example</li>
      <ul>
        <li>
          <span :style="{color: activeColor, fontSize: fontSize + 'px'}">This is an example</span>
        </li>
      </ul>
      <li>We can also bind an object</li>
      <ul>
        <li>
          <span :style="styleObject">This is an example of binding an object in the data field</span>
        </li>
      </ul>
    </ul>
  </div>
</template>

<script scoped>
export default {
  data() {
    return {
      activeColor: "#50c878",
      fontSize: 30,
      styleObject: {
        color: "#ae0001",
        fontSize: "20px"
      }
    };
  }
};
</script>

<style>
</style>

