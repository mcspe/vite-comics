<script>
  export default {
    name: 'FooterCTA'
  }
</script>

<template>
  <section>
    <div class="container">
      <button>
        <img src="../../assets/img/buy-comics-digital-comics.png" alt="Digital Comics">
        <span>Digital Comics</span>
      </button>
      <button>
        <img src="../../assets/img/buy-comics-merchandise.png" alt="DC Merchandise">
        <span>DC Merchandise</span>
      </button>
      <button>
        <img src="../../assets/img/buy-comics-subscriptions.png" alt="Subscription">
        <span>Subscription</span>
      </button>
      <button>
        <img src="../../assets/img/buy-comics-shop-locator.png" alt="Comic Shop Locator">
        <span>Comic Shop Locator</span>
      </button>
      <button>
        <img src="../../assets/img/buy-dc-power-visa.svg" alt="DC Power Visa">
        <span>DC Power Visa</span>
      </button>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  @use '../../scss/partials/vars' as *;
  section{
    background: $primary-blue;

    .container{
      padding: 2rem 3rem;
      display: flex;
      justify-content: space-between;

      button{
        cursor: pointer;
        background: none;
        border: none;
        height: 3rem;
        display: flex;
        justify-content: center;
        align-items: center;

        img {
          height: 100%;
          width: 100%;
          object-fit: contain;
        }

        span{
          text-transform: uppercase;
          color: white;
          font-size: .7rem;
          flex-shrink: 0;
          margin: 0 .5rem;
        }

        &:hover{
          opacity: .8;
        }

        &:last-child img{
          height: 60%;
        }
      }
    }
  }
</style>