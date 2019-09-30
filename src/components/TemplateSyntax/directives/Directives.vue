<template>
  <div>
    <h4>Directives</h4>
    <ul>
      <li>
        Directives are special attributes with the
        <code>v-</code> prefix.
      </li>
      <li>
        Expected to be a single JavaScript expression (except
        <code>v-for</code>)
      </li>
      <li>A directives job is to reactively apply side effects to the DOM when the value of its express changes</li>
      <li>Example:</li>
      <ul>
        <li>
          <span v-if="seen">Now you see me</span>
        </li>
        <li>In the above example you will see a span if the value of see is true</li>
        <li>
          <button @click="changeSeen">Click here to change the value of seen</button>
        </li>
      </ul>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      seen: true
    };
  },

  methods: {
    changeSeen: function() {
      if (this.seen === true) {
        this.seen = false;
      } else {
        this.seen = true;
      }
    }
  }
};
</script>

