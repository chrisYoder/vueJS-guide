<template>
  <div>
    <h4>Object Syntax</h4>
    <ul>
      <li>
        We can pass an object to
        <code>v-bind:class</code> tod dynamically toggle classes
      </li>
      <li>You cna have multiple classes toggled by having more fields in the object</li>
      <li>
        <code>v-bind:class</code> can co-exist with the plain
        <code>class</code> attribute
      </li>
      <li>Examples:</li>
      <ul>
        <li>
          <span
            @click="changeValues"
            :class="{active: isActive, 'text-danger': hasError}"
          >This is an example</span>
        </li>
        <li>
          <span
            :class="classObject"
            @click="changeFonts"
          >This is an example with classObject and a Computed value</span>
        </li>
      </ul>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isActive: true,
      hasError: false,
      isNormalFont: true,
      isDangerFont: false
    };
  },

  methods: {
    changeValues: function() {
      this.isActive = !this.isActive;
      this.hasError = !this.hasError;
    },

    changeFonts: function() {
      this.isNormalFont = !this.isNormalFont;
      this.isDangerFont = !this.isDangerFont;
    }
  },

  computed: {
    classObject: function() {
      return {
        normal: this.isNormalFont && !this.isDangerFont,
        "danger-font": this.isDangerFont && !this.isNormalFont
      };
    }
  }
};
</script>

<style scoped>
.active {
  color: #50c878;
}

.text-danger {
  color: #ae0001;
}

.normal {
  font-size: 14px;
  font-family: Western;
}

.danger-font {
  font-size: 20px;
  color: red;
  font-family: Helvetica;
}
</style>



