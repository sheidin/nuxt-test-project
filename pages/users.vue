<template>
  <div>
    <button @click="onLoadUser">Load user</button>
    <input type="text" v-model="userId">
    <nuxt-child />
  </div>
</template>


<script>
export default {
  data() {
    return {
      userId: ''
    }
  },
  methods: {
    onLoadUser() {
      this.$router.push('/users/' + this.userId);
    }
  }
}
</script>
