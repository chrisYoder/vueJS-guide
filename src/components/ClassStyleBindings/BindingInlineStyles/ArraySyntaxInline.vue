<template>
  <div>
    <h4>Array Syntax Inline Styles</h4>
    <ul>
      <li>The array syntax allows you to apply multiple style objects to the same element</li>
      <ul>
        <li>
          <span
            :style="[fontColor, fontSize]"
          >This was styled using the fontColor and fontSize object</span>
        </li>
      </ul>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fontColor: {
        color: "#ae0001"
      },
      fontSize: {
        fontSize: "30px"
      }
    };
  }
};
</script>

<style>
</style>

