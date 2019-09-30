<template>
  <div class="section">
    <h2>Section 2: Computed Properties and Watchers</h2>
    <h3>Computed Properties</h3>
    <basic-example/>
    <caching-v-methods/>
    <computed-v-watched/>
    <computed-setters/>
    <h3>Watchers</h3>
    <watchers/>
  </div>
</template>

<script>
import BasicExample from "./ComputedProperties/BasicExample";
import CachingVMethods from "./ComputedProperties/CachingVMethods";
import ComputedVWatched from "./ComputedProperties/ComputedVWatched";
import ComputedSetters from "./ComputedProperties/ComputedSetter";
import Watchers from "./Watchers/Watchers";
export default {
  name: "SectionTwo",
  components: {
    BasicExample,
    CachingVMethods,
    ComputedVWatched,
    ComputedSetters,
    Watchers
  }
};
</script>

