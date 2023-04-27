<script>
  import {menus} from '../assets/data/DB'
  export default {
    name: 'Header',
    data(){
      return{
        menus
      }
    }
  }
</script>

<template>
  <header>
    <div class="container">
      <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="DC-logo">
      </div>
      <nav>
        <ul>
          <li 
            v-for="(link, i) in menus.headerMenu" 
            :key="i"
            >
            <a 
            :href="link.href"
            :class="{'active': link.isActive}">{{ link.label }}</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style lang="scss" scoped>
  @import '../scss/partials/header';
</style>