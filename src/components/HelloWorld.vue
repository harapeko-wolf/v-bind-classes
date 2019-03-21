<template>
  <div class="hello">
    <p>
      Hello,
      <span v-bind:class="{ large:isSize, 'text-danger': hasError }">Vue.js</span>
      <!-- クラスにハイフンがつく場合、シングルコーテーションで囲む必要がある！！ -->
    </p>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data: () => ({
    isSize: true,
    hasError: true
  })
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.large {
  font-size: 32px;
}

.text-danger {
  color: red;
}
</style>
