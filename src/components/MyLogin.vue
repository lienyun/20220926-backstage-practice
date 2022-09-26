<template>
  <form class="m-5">
  <div class="mb-3">
    <label for="exampleInputEmail1" class="form-label">帳號</label>
    <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" v-model.trim="username">
    
  </div>
  <div class="mb-3">
    <label for="exampleInputPassword1" class="form-label">密碼</label>
    <input type="password" class="form-control" id="exampleInputPassword1" v-model.trim="password">
  </div>
  <div class="mb-3 form-check">
    <input type="checkbox" class="form-check-input" id="exampleCheck1">
    <label class="form-check-label" for="exampleCheck1">Check me out</label>
  </div>
  <button type="button" class="btn btn-primary" @click="onLoginClick">登入</button>
</form>
</template>

<script scoped>
  export default {
    data() {
      return {
        username: '',
        password: ''
      }
    },
    methods: {
      onLoginClick() {
        if(this.username === 'admin' && this.password === '123456'){
          this.$router.push('/home')
          localStorage.setItem('token', 'Bearer xxx')
        }else {
          localStorage.removeItem('token')
        }
      }
    }
  }
</script>

<style>
  body {
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>