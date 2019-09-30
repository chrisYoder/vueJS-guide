
<template>
  <div>
    <h4>Text</h4>
    <ul>
      <li>
        Message:
        <b>{{ msg }}</b>
      </li>
      <li>The mustache tag ({{ mustache }}) will replace the value of a variable with the property in the corresponding data object</li>
      <li>
        You can also do one-time interpolations by using the v-once directive. For example,
        <b>
          <span v-once>{{ msg2 }}</span>
        </b> will not be updated on any data change
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      msg: "Hello World!",
      msg2: "This Message",
      mustache: "{{ variable }}"
    };
  }
};
</script>

<style scoped>
</style>


