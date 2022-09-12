<template>
  <div class="home">
    <nav class="principal-navigation">
      <router-link to="/manager"><span>Career Manager</span></router-link>
      <router-link to="/player"><span>Career Player</span></router-link>
    </nav>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    // HelloWorld
  }
}
</script>

<style lang="scss">
  .principal-navigation {
    height: 100vh;
    display: block;
    position: relative;
    a {
      width: 100%;
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      background: #cacaca;
      font-size: 3rem;
      color: #fff;
      text-decoration: none;
      transition: .2s linear;
      overflow: hidden;
      position: absolute;
      top: 0;
      left: 0;
      span {
        position: relative;
        &:before {
          content: "";
          position: absolute;
          top: 0;
          left: 0;
          width: 100%;
          height: 100%;
          border-top: 5px solid #fff;
          border-bottom: 5px solid #fff;
          transform: scale(1.5);
          transition: .1s linear;
          opacity: 0;
        }
      }
      &:first-child {
        background-image: url(../assets/career-mode-manager-background.jpeg);
        background-size: cover;
        background-position: center;
        clip-path: polygon(0 0%, 75% 0%, 0% 154%, 0% 100%);
        justify-content: flex-start;
        z-index: 1;
        span {
          margin-left: 1.5rem;
        }
      }
      &:last-child {
        background-image: url(../assets/career-mode-background-2.jpeg);
        background-size: cover;
        background-position: -27% 0;
        z-index: 0;
        background-repeat: no-repeat;
        justify-content: flex-end;
        span {
          margin-right: 1.5rem;
        }
      }
      &:hover {
        span {
          &:before {
            transform: scale(1);
            opacity: 1;
          }
        }
      }
    }
  }
</style>
