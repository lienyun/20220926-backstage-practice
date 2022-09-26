<template>
  <button type="button" class="btn btn-light btn-sm" @click="goBack">上一頁</button>
  <h4>用戶詳情 --- {{id}}</h4>
</template>

<script>
  export default {
    name: 'MyUserDetail',
    props: ['id'],
    methods: {
      goBack() {
        this.$router.go(-1)
      }
    }
  }
</script>