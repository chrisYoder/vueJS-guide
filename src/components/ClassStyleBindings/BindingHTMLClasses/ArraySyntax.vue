<template>
  <div>
    <h4>Array Syntax</h4>
    <ul>
      <li>We can pass an array to
        <code>v-bind:class</code> to apply a list of classes.
      </li>
      <li>Example:</li>
      <ul>
        <li>
          <span :class="[activeClass, errorClass]">Basic Example</span>
        </li>
        <li>
          <span
            :class="[hasError ? errorClass : '', activeClass]"
            @click="changeClasses"
          >Conditionally rendered with ternary (clickable)</span>
        </li>
        <!-- ^^ should always render activeClass but will only apply errorClass when hasError is truthy -->
        <li>
          <span
            id="test"
            :class="[{active: isActive}, errorClassMixed]"
            @click="changeActive"
          >Object Syntax inside Array Syntax</span>
        </li>
        <!-- ^^ should always render errorClass unless isActive is truthy -->
      </ul>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeClass: "active",
      errorClass: "text-danger",
      errorClassMixed: 'text-danger',
      isActive: true,
      hasError: false,
      
    };
  },

  methods: {
    changeClasses: function() {
      this.hasError = !this.hasError;
    },

    changeActive: function() {
      if(this.isActive === false) {
        this.errorClassMixed = '';
        this.isActive = true;
      } else {
        this.errorClassMixed = 'text-danger';
        this.isActive = false;
      }
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
</style>

