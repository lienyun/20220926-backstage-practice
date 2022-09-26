<template>
  <h1 class="text-center">MyUsers</h1>
  <table class="table table-bordered table-striped table-hover">
    <thead>
      <tr>
        <th>#</th>
        <th>姓名</th>
        <th>年齡</th>
        <th>頭銜</th>
        <th>操作</th>
      </tr>
    </thead>
  
  <tbody>
    <tr v-for="(item, i) in userlist" :key="item.id">
    <td>{{i+1}}</td>
    <td>{{item.name}}</td>
    <td>{{item.age}}</td>
    <td>{{item.position}}</td>
    <td>
      <router-link :to="'/home/users/' + item.id">詳情</router-link>
    </td>
  </tr>
  </tbody>
</table>
</template>

<script>
  export default {
    name: 'MyUser',
    data() {
      return {
        userlist: [
          {id: 1, name: '1', age: 18, position: '1'},
          {id: 2, name: '1', age: 56, position: '12'},

          {id: 3, name: '1', age: 78, position: '13'},
          {id: 4, name: '1', age: 9, position: '14'},

        ]
      }
    }
  }
</script>