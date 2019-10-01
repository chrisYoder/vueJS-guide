<template>
  <div>
    <h4><code>v-for</code> with an Object</h4>
    <ul>
      <li>We can also use <code>v-for</code> to iterate throught the properties of an object.</li>
      <li>Can take up to two arguments: 
        <ol>
          <li>value (property value)</li>
          <li>Name (property name)</li>
          <li>Index</li>
        </ol>
      <li>Example:
        <ul>
          <li v-for="(value, name, index) in object" :key='value.index'> {{index+1}}. {{ name }}:  {{ value }}</li>
        </ul>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'vForObject', 
    data() {
      return {
        object: {
          title: 'The Way of Kings',
          author: 'Brandon Sanderson',
          publishedAt: 'August 31, 2010'
        }
      };      
    }
  }
</script>