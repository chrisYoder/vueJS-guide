<template>
  <div>
    <h4>Using Javascript Expressions</h4>
    <ul>
      <li>We can use full Javascript Expressions inside all data bindings.</li>
      <li>flow control (if-else) statements won't work but ternary expressions will</li>
      <li>Examples</li>
      <ul>
        <li>Mathematical operations ({{ number }}): {{ number + 1}}, {{ number * 3 }}, etc</li>
        <li>Ternary Operations: Is the answer to a random questions {{ ok ? 'YES' : 'NO' }}</li>
        <li>String manipulations:
          <ul>
            <li>Original message: {{ message }}</li>
            <li>Reversed message: {{ message.split('').reverse().join('') }}</li>
          </ul>
        </li>
      </ul>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number: 5,
      ok: "yes",
      message: "This a vue new world"
    };
  }
};
</script>

<style>
</style>


