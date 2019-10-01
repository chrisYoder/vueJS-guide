<template>
  <div>
    <h4>vIf</h4>
    <ul>
      <li>
        The directive
        <code>v-if</code> is used to conditionally render a block
      </li>
      <li>The block will only be rendered if the directives expression returns a truthy value</li>
      <li>Examples:
        <ul>
          <li>
            <span v-if="awesome">Vue is Awesome</span>
          </li>
        </ul>
      </li>
      <li>
        You can also had an "else block" with
        <code>v-else</code> which must come immediately after a
        <code>v-if</code> or
        <code>v-else-if</code> to be recognized
      </li>
      <li>Example:</li>
      <ul>
        <li>
          <span v-if="awesome">Vue Is Awesome</span>
          <span v-else>You need to get your head checked</span>
        </li>
      </ul>
      <li>
        The
        <code>v-if</code> directive can only be attached to a single element we can nest other elements within the directive element
      </li>
      <li>Example:
        <ul>
          <li>
            <div v-if="ok">
              <p>Paragraph 1</p>
              <p>Paragraph 2</p>
            </div>
          </li>
        </ul>
      </li>
      <li>
        <code>v-else-if</code> is a conditional operative that can be chained multiple times.
      </li>
      <li>Examples:
        <ul>
          <li>
            <p v-if="type === 'A'">A</p>
            <p v-else-if="type === 'B'">B</p>
            <p v-else-if="type === 'C'">C</p>
            <p v-else>Not A/B/C</p>
          </li>
        </ul>
      </li>
      <li>Vue tries to render elements as efficiently as possible--often reusing them instead of rendering from scratch.</li>
      <li>Example:
        <div v-if="loginType === 'username'">
          <label>Username</label>
          <input type="text" placeholder="Enter your username">
        </div>
        <div v-else>
          <label>Email</label>
          <input type="text" placeholder="Enter your email">
        </div>
        <button @click="toggleLoginType">Toggle Login Type</button>

        <p>The way this code is written--without a unique key--will not erase what the user has already entered.</p>

        <div v-if="loginType === 'username'">
          <label>Username:</label>
          <input type="text" placeholder="Enter your username" key="username-input">
        </div>
        <div v-else>
          <label>Email</label>
          <input type="text" placeholder="Enter your email" key="email-input">
        </div>
        <button @click="toggleLoginType">Toggle Login Type</button>

        <p>The second set of code utilizes a key attribute on the input tag to let Vue know that they are seperate and not to reuse them.</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "vIf",
  data() {
    return {
      awesome: true,
      ok: true,
      type: "A",
      loginType: "username"
    };
  },

  methods: {
    toggleLoginType: function() {
      if (this.loginType === "username") {
        this.loginType = "";
      } else {
        this.loginType = "username";
      }
    }
  }
};
</script>

