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
  @use '../scss/partials/vars' as *;
  @import '../scss/partials/general';

  header{
    .container{
      background-color: white;
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 5rem;
      padding: .5rem;

      .logo{
        height: 100%;

        img{
          height: 100%;
          width: 100%;
          object-fit: cover;
        }
      }

      nav{
        height: 100%;
        
        ul{
          list-style: none;
          height: 100%;

          li{
            display: inline-block;
            height: 100%;
            line-height: 4rem;
            margin: 0 .5rem;

            a{
              display: inline-block;
              height: 100%;
              font-size: .7rem;
              color: $primary-dark;
              text-decoration: none;
              text-transform: uppercase;
              &:hover{
                color: $primary-blue;
                box-shadow: 0 .3rem 0 $primary-blue;
              }
              &.active{
                color: $primary-blue;
                box-shadow: 0 .3rem 0 $primary-blue;
              }
            }
          }
        }
      }
    }
  }
</style>