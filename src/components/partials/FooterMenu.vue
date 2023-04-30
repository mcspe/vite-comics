<script>
  import {menus} from '../../assets/data/DB.js'
  export default {
    name: 'FooterMenu',
    data(){
      return{
        menus
      }
    }
  }
</script>

<template>
  <section>
    <div class="container">
      <nav>
        <ul
          v-for="(menus, i) in menus.footerMenus"
          :key="i">
          <h3>{{menus.title}}</h3>
          <li
            v-for="(link, index) in menus.links"
            :key="index">
            <a :href="link.href">
              {{ link.label }}
            </a>
          </li>
        </ul>
      </nav>
      <div class="logo">
        <!-- <img src="../../assets/img/dc-logo-bg.png" alt=""> -->
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  @use '../../scss/partials/vars' as *;
  section{
    background: url('../../assets/img/footer-bg.jpg');

    .container{
      padding: 1.5rem 0;
      display: flex;
      justify-content: space-between;
      align-items: center;

      nav{
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
        align-content: flex-start;
        max-height: 350px;
        
        ul{
          margin: .5rem 1rem;

          h3{
          text-transform: uppercase;
          color: white;
          font-size: 1.1rem;
          margin: .5rem 0;
          }

          li{
            list-style: none;
  
            a{
              font-size: .7rem;
              text-transform: capitalize;
              text-decoration: none;
              color: $primary-light;
  
              &:hover{
                color: white;
              }
            }
          }
        }
      }

      .logo{
        background: url('../../assets/img/dc-logo-bg.png');
        height: 100%;
        width: 75%;
      }
    }
  }
</style>