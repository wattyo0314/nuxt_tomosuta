<template>
  <div>
    <p>{{ IP }}</p>
    <button type="button" @click="fetchSomething">I Pアドレスを取得</button>
  </div>
</template>


<script>
export default {
  data() {
    return {
      IP: "",
    };
  },
  methods: {
    async fetchSomething() {
      this.IP = await this.$axios.$get("http://icanhazip.com");
    },
  },
};
</script>