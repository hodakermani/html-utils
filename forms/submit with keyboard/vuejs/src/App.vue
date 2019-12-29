<template>
  <div id="app">
    <h1>Submit a form using enter with Vue.js</h1>
    <h3 class="tip">Use <i>tab</i> to navigate between fields and <i>enter</i> to submit the form.</h3>
    <form>
      Email: <input
        type="email"
        name="email"
        id="#email" />
      <br/>
      Comment: <input
        type="textarea"
        name="comment"
        v-on:keyup="submitForm" />
    </form>
  </div>
</template>

<script>
export default {
  name: 'app',
  methods: {
    submitForm: (e) => {
      if (e.keyCode === 13) alert("yeey! Thank you for your feedback.");
    }
  }
}
</script>

<style>
.tip {
  background-color: orange;
  padding: 1vw;
}
</style>
