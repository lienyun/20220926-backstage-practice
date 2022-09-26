<template>
  <div class="m-5">
    <h1>後台管理系統</h1>
    <button type="button" class="btn btn-light" @click="onLogout">登出</button>
  </div>

</template>

<script>
  export default {
    name: 'MyHeader',
    methods: {
      onLogout() {
        localStorage.removeItem('token')
        this.$router.push('/login')
      }
    }
  }
</script>