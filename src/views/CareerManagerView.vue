<template>
  <div class="content bg-gradient-to-r from-red-700 to-stone-900">
    <img src="../assets/logo_acmilan.svg" alt="" class="logo-team">
    <div class="principal-stats">
      <div class="row">
        <div class="stat">
          <h3>Seasons</h3>
          <h4>0</h4>
        </div>
        <div class="stat">
          <h3>Trophies</h3>
          <h4>0</h4>
        </div>
      </div>
      <div class="row">
        <div class="stat">
          <h3>total invested</h3>
          <h4>€ 0</h4>
        </div>
        <div class="stat">
          <h3>UEFA Champions league</h3>
          <h4>7</h4>
        </div>
      </div>
    </div>
    <div class="container-stats">
      <ul class="navigation-career-mode">
        <li><a @click="activeTab = 'team'">Team</a></li>
        <li><a @click="activeTab = 'formation'">Formation</a></li>
        <li><a @click="activeTab = 'transfers'">Transfers</a></li>
        <li><a @click="activeTab = 'trophies'">Trophies</a></li>
      </ul>
    </div>
    <div class="container-components">
      <team-component v-if="activeTab === 'team'"></team-component>
      <formation-component v-if="activeTab === 'formation'"></formation-component>
      <transfers-component v-if="activeTab === 'transfers'"></transfers-component>
      <trophies-component v-if="activeTab === 'trophies'"></trophies-component>
    </div>
  </div>
</template>

<script>
  import TeamComponent from '../components/TeamComponent.vue';
  import FormationComponent from '../components/FormationComponent.vue';
  import TransfersComponent from '../components/TransfersComponent.vue';
  import TrophiesComponent from '../components/TrophiesComponent.vue';

  export default {
    name: "CareerManagerView",
    components: {
      TeamComponent,
      FormationComponent,
      TransfersComponent,
      TrophiesComponent
    },
    data() {
      return {
        clubName: 'AC Milan',
        actualSeason: '2022-2023',
        activeTab: 'team',
      }
    }
  }
</script>

<style lang="scss" scoped>

  .content {
    height: 100vh;
  }
  .logo-team {
    max-width: 150px;
    padding: 1rem;
    box-sizing: border-box;
  }

  .principal-stats {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    max-width: 500px;
    float: right;
    margin-top: -14rem;
    padding: 1rem;
    box-sizing: border-box;
    .row {
      &:first-child {
        margin-right: 3rem;
      }
      .stat {
        line-height: 2rem;
        margin-bottom: 2rem;
        h3 {
          color: #fff;
          font-size: 1.5rem;
        }
        h4 {
          color: #fff;
          font-size: 3rem;
        }
      }
    }
  }

  .container-stats {
    padding: 1rem;
    .navigation-career-mode {
      display: flex;
      justify-content: space-between;
      align-items: center;
      li {
        text-align: center;
        display: block;
        width: 100%;
        a {
          color: #fff;
          display: block;
          cursor: pointer;
          &:hover {
            color: #aaa;
          }
        }
      }
    }
  }
</style>