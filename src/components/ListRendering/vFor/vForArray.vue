<template>
  <div>
    <h4>
      Mapping an Array to Elements with
      <code>v-for</code>
    </h4>

    <ul>
      <li>
        Use
        <code>v-for</code> to render a list of items based on an array.
      </li>
      <li>
        The syntax is
        <code>item in items</code> where
        <code>items</code> is the source array and
        <code>item</code> is an alias for the array element being iterated on
      </li>
      <li>Example:
        <ul>
          <li v-for="item in items" :key="item.id">{{item.message}}</li>
        </ul>
      </li>
      <li>
        <code>v-for</code> also supports an optional second argument for the index of the current item
      </li>
      <li>Example
        <ul>
          <li
            v-for="(item, index) in items"
            :key="item.id"
          >{{ index + 1}} - {{item.message}}</li>
        </ul>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "vForArray",
  data() {
    return {
      parentMessage: "Parent",
      items: [
        { message: "Fu", id: 1 },
        { message: "Bar", id: 2 },
        { message: "Is German for...", id: 3 },
        { message: "Frakked Up Beyond All Repair", id: 4 }
      ]
    };
  }
};
</script>


