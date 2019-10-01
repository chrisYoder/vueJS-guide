<template>
  <div class="section">
    <h2>Section 3: Class and Style Bindings</h2>
    <h3>Binding HTML Class</h3>
    <object-syntax/>
    <array-syntax/>
    <with-components/>
    <h3>Binding Inline Styles</h3>
    <object-syntax-inline/>
    <array-syntax-inline/>
    <auto-prefix/>
    <multiple-values/>
  </div>
</template>

<script>
import ObjectSyntax from "./BindingHTMLClasses/ObjectSyntax";
import ArraySyntax from "./BindingHTMLClasses/ArraySyntax";
import WithComponents from "./BindingHTMLClasses/WithComponents";
import ObjectSyntaxInline from "./BindingInlineStyles/ObjectSyntaxInline";
import ArraySyntaxInline from "./BindingInlineStyles/ArraySyntaxInline";
import AutoPrefix from "./BindingInlineStyles/AutoPrefix";
import MultipleValues from "./BindingInlineStyles/MultipleValue";

export default {
  name: "SectionThree",
  components: {
    ObjectSyntax,
    ArraySyntax,
    WithComponents,
    ObjectSyntaxInline,
    ArraySyntaxInline,
    AutoPrefix,
    MultipleValues
  }
};
</script>



