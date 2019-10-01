<template>
  <div>
    <h4>vShow</h4>
    <ul>
      <li>
        <code>v-show</code> works largely the same as
        <code>v-if</code> except the element remains in the DOM
      </li>
      <li>
        <code>v-show</code> toggles the
        <code>display</code> CSS property of the element
      </li>
      <li>
        <code>v-show</code> cannot be used on the template element like
        <code>v-if</code> and does not support
        <code>v-else</code>
      </li>
      <li>Examples:
        <ul>
          <li>
            <span v-show="ok">Hello!</span>
          </li>
        </ul>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "vShow",
  data() {
    return {
      ok: true
    };
  }
};
</script>

