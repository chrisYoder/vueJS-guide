<template>
  <div>
    <h4>Other Notes</h4>
    <ul>
      <li>
        <code>v-if</code> v
        <code>v-show</code>
        <ul>
          <li>
            <code>v-if</code> is "real" rendering because it ensures that event listeners and child components inside the condition block are properly destroyed and recreated during toggles
          </li>
          <li>
            <code>v-if</code> is "lazy" because if the condition is false on the initial render then it won't do anything until the condition becomes true for the first time.
          </li>
          <li>
            <code>v-show</code> is simpler because the element is always rendered regardless of initial condition and the CSS property is toggled
          </li>
          <li>
            <code>v-if</code> has a higher toggle costs while
            <code>v-show</code> has a higher initial render cost. Use the latter if something is toggled often and the former when the condition is unlikley to change at runtime
          </li>
        </ul>
      </li>
      <li>
        <code>v-if</code> with
        <code>v-for</code>
        <ul>
          <li>Using
            <code>v-if</code> and
            <code>v-for</code> is not recommended.
          </li>
          <li>However, if you do then
            <code>v-for</code> has a higher priority than
            <code>v-if</code>
          </li>
        </ul>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'OtherNotes'
};
</script>

