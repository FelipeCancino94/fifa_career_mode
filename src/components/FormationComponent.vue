<template>
  <div>
    <div id="field">
      <div class="corner-left-area"></div>
      <div class="corner-right-area"></div>
      <div class="goalkeeper-primary-area"></div>
      <div class="penalty-area"></div>
      <div class="goalkeeper-secondary-area"></div>
      <div class="goalkeeper-terciary-area"></div>
      <div class="attak-area"></div>
      <div class="grass">
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
      </div>
      <div class="formation">
        <div class="por">Maignan</div>
        <div class="dfc1">Kalulu</div>
        <div class="dfc2">Tomori</div>
        <div class="lti">Hernandez</div>
        <div class="ltd">Calabria</div>
        <div class="mcd1">Tonali</div>
        <div class="mcd2">Bennacer</div>
        <div class="mi">Leao</div>
        <div class="md">Messias</div>
        <div class="mco">Diaz</div>
        <div class="dc">Giroud</div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "formationComponent",
    data() {
      return {
        prueba: true,
      }
    }
  }
</script>

<style lang="scss" scoped>
#field {
  border: 2px solid #fff;
  max-width: 1024px;
  width: 100%;
  height: 700px;
  position: relative;
  overflow: hidden;
  background: #b91c1c;

  .grass {
    position: absolute;
    width: 100%;
    height: 100%;
    border: 0;
    .line {
      position: relative;
      width: 100%;
      height: calc(100% / 7);
      background: rgba(0, 0, 0, .3);
      border: 0;
      &:nth-child(odd) {
        background: rgba(0, 0, 0, .4);
      }
    }
  }

  div {
    position: absolute;
    border: 2px solid #fff;
  }
  .corner-left-area {
    width: 100px;
    height: 100px;
    bottom: -50px;
    left: -50px;
    border-radius: 50%;
    z-index: 1;
  }
  .corner-right-area {
    width: 100px;
    height: 100px;
    bottom: -50px;
    right: -50px;
    border-radius: 50%;
    z-index: 1;
  }
  .goalkeeper-primary-area{
    width: 300px;
    height: 100px;
    bottom: -25px;
    left: 50%;
    margin-left: -150px;
    z-index: 1;
  }
  .penalty-area {
    width: 6px;
    height: 6px;
    background: #fff;
    bottom: 130PX;
    left: 50%;
    margin-left: -3px;
    border-radius: 50%;
    z-index: 1;
  }
  .goalkeeper-secondary-area {
    width: 600px;
    height: 200px;
    bottom: -2px;
    left: 50%;
    margin-left: -300px;
    z-index: 1;
  }
  .goalkeeper-terciary-area {
    width: 300px;
    height: 300px;
    bottom: 0;
    left: 50%;
    margin-left: -150px;
    border-radius: 50%;
    &:after {
      content: "";
      width: 320px;
      height: 199px;
      background: #b91c1c;
      position: absolute;
      bottom: -5px;
      left: -10px;
    }
  }
  .attak-area {
    width: 300px;
    height: 300px;
    top: -150px;
    left: 50%;
    margin-left: -150px;
    border-radius: 50%;
    z-index: 1;
  }

  .formation {
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    border: 0;
    > div {
      border: 0;
      color: #fff;
      position: absolute;
      background: rgba(0, 0, 0, 0.5);
      padding: 0.5rem 1rem;
      font-size: 1.5rem;
      &.por {
        bottom: 0;
        left: 50%;
        margin-left: -47px;
      }
      &.dfc1 {
        bottom: 16%;
        left: 35%;
      }
      &.dfc2 {
        bottom: 16%;
        left: 57%;
      }

      &.lti {
        bottom: 16%;
        left: 10%;
      }

      &.ltd {
        bottom: 16%;
        left: 85%;
      }

      &.mcd1 {
        bottom: 45%;
        left: 35%;
      }

      &.mcd2 {
        bottom: 45%;
        left: 57%;
      }

      &.mco {
        bottom: 70%;
        left: 47%;
      }

      &.mi {
        bottom: 70%;
        left: 10%;
      }

      &.md {
        bottom: 70%;
        left: 85%;
      }

      &.dc {
        bottom: 90%;
        left: 46%;
      }
    }
  }
}
</style>