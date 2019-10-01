<template>
  <div class="section">
    <h2>Section 5: List Rendering</h2>
    <vFor-array/>
    <vFor-object/>
    <other-notes/>
  </div>
</template>

<script>
import vForArray from "./vFor/vForArray";
import vForObject from './vFor/vForObject';
import OtherNotes from "./OtherNotes/OtherNotes";

export default {
  name: "SectionFive",
  components: {
    vForArray,
    vForObject,
    OtherNotes
  }
};
</script>

