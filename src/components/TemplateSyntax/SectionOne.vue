<template>
  <div class="section">
    <h2>Section 1: Template Syntax</h2>
    <h3>Interpolations</h3>
    <text-interpolation/>
    <raw-html/>
    <attributes/>
    <javascript-expressions/>
    <h3>Directives</h3>
    <directives/>
    <arguments/>
    <dynamic-arguments/>
    <modifiers/>
  </div>
</template>

<script>
import TextInterpolation from "./Interpolations/TextInterpolation";
import RawHtml from "./Interpolations/RawHtml";
import Attributes from "./Interpolations/Attributes";
import JavascriptExpressions from "./Interpolations/JavascriptExpressions";
import Directives from "./directives/Directives";
import Arguments from "./directives/Arguments";
import DynamicArguments from "./directives/DynamicArguments";
import Modifiers from "./directives/Modifiers";

export default {
  name: "SectionOne",
  components: {
    TextInterpolation,
    RawHtml,
    Attributes,
    JavascriptExpressions,
    Directives,
    Arguments,
    DynamicArguments,
    Modifiers
  }
};
</script>

<style>
</style>


