<template>
  <div>
    <h4>Dyanmic Arguments</h4>
    <ul>
      <li>It is possible to use a JS expression in a directive argument by wrapping it in square brackets</li>
      <li>Example:</li>
      <ul>
        <li>
          <code>a :[attrName]='url'</code>
        </li>
        <li>
          <a :[attrName]="url">{{ url }}</a>
        </li>
      </ul>
      <li>Constraints</li>
      <ul>
        <li>Dynamic Argument Values are expected to evaluate to a string with the exception of null</li>
        <li>Dynamic Argument Expressions have some syntax constraints because certain characters, such as spaces and quotes, are invalid inside HTML attribute names</li>
        <li>Avoid naming keys with uppercase characters.</li>
      </ul>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      url: "https://vuejs.org",
      attrName: "href"
    };
  }
};
</script>

