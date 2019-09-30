<template>
  <div>
    <h4>Raw HTML</h4>
    <ul>
      <li>Text interpolation interperts data as plain text, not HTML. To render HTML you need to use the v-html directive</li>
      <li>Using text interpolation: {{ RawHTML }}</li>
      <li>
        Using v-html directive:
        <span v-html="RawHTML"></span>
      </li>
      <li>Dynamically rending arbitrary HTML on a website can be dangerous because it can easily lead to Cross Site Scripting (XSS) vulnerabilities.</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      RawHTML:
        "<span style='color: var(--bronze)'>This should be Ravenclaw Bronze"
    };
  }
};
</script>

<style>
</style>

