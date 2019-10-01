<template>
  <div class="section">
    <h2>Section 4: Conditional Rendering</h2>
    <h3>vIf</h3>
    <vIf/>
    <h3>vShow</h3>
    <vShow/>
    <h3>Other Notes</h3>
    <otherNotes/>
  </div>
</template>

<script>
import vIf from "./vIf/vIf";
import vShow from "./vShow/vShow";
import OtherNotes from "./otherNotes/OtherNotes";

export default {
  name: "SectionFour",
  components: {
    vIf,
    vShow,
    OtherNotes
  }
};
</script>


