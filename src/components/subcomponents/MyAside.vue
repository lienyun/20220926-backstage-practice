<template>
  <div class="layout-aside-container">
    <ul class="user-select-none menu">
      <li class="menu-item">
        <router-link to="/home/users">使用者管理</router-link>
      </li>
      <li class="menu-item">
        <router-link to="/home/rights">權限管理</router-link>
      </li>
      <li class="menu-item">
        <router-link to="/home/goods">商品管理</router-link>
      </li>
      <li class="menu-item">
        <router-link to="/home/orders">訂單管理</router-link>
      </li>
      <li class="menu-item">
        <router-link to="/home/settings">系統設定</router-link>
      </li>

    </ul>
  </div>

</template>

<style scoped>
  .menu-item {
    text-decoration: none;
  }
</style>