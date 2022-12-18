<template>
  <div class="content bg-gradient-to-r from-red-700 to-stone-900">
    <div class="header-view">
      <div class="total-goals">
        <p>Goals</p>
        <p>0</p>
      </div>
      <img src="../assets/logo_acmilan.svg" alt="" class="logo-team">
      <div class="trophies">
        <p>Trophies</p>
        <p>0</p>
      </div>
    </div>
    <div class="body-view">
      <div class="accordion-data">
        <div
          class="item"
          @click="hideItems()">
          <div class="item-header">
            <p>
              Temporada 2022 - 2023
            </p>
          </div>
          <div class="item-body">
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur, deserunt dolores adipisci sed, quasi enim iure magni natus odio exercitationem cumque nostrum aspernatur, tenetur voluptatem assumenda distinctio quam. Doloribus, aliquid.
            </p>
          </div>
        </div>
        <div class="item" @click="hideItems()">
          <div class="item-header">
            <p>
              Temporada 2023 - 2024
            </p>
          </div>
          <div class="item-body">
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur, deserunt dolores adipisci sed, quasi enim iure magni natus odio exercitationem cumque nostrum aspernatur, tenetur voluptatem assumenda distinctio quam. Doloribus, aliquid.
            </p>
          </div>
        </div>
        <div class="item" @click="hideItems()">
          <div class="item-header">
            <p>
              Temporada 2024 - 2025
            </p>
          </div>
          <div class="item-body">
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur, deserunt dolores adipisci sed, quasi enim iure magni natus odio exercitationem cumque nostrum aspernatur, tenetur voluptatem assumenda distinctio quam. Doloribus, aliquid.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "CareerPlayerView",
    data() {
      return {
        statistics: {
          clubs: [
            {
              season: '2022 - 2023',
              goals: 0,
              assists: 0,
              games: 0,
              yellowCards: 0,
              redCards: 0,
              trophies: 0,
              wins: 0,
              draws: 0,
              losses: 0,
              playerOfTheMonth: 0,
              playerOfTheYear: false,
              competences: [
                {
                  status: 'Champion',
                  name: 'Serie A',
                  position: 1,
                  goals: 0,
                  assists: 0,
                  games: 0,
                  wins: 0,
                  draws: 0,
                  losses: 0,
                  yellowCards: 0,
                  redCards: 0,
                  topScorer: false,
                  topAssists: false,
                  mostValuePlayer: false,
                },
                {
                  status: 'Final',
                  name: 'Copa Italia',
                  position: 1,
                  goals: 0,
                  assists: 0,
                  games: 0,
                  wins: 0,
                  draws: 0,
                  losses: 0,
                  yellowCards: 0,
                  redCards: 0,
                  topScorer: false,
                  topAssists: false,
                  mostValuePlayer: false,
                },
                {
                  status: 'Final',
                  name: 'Uefa Champions League',
                  position: 1,
                  goals: 0,
                  assists: 0,
                  games: 0,
                  wins: 0,
                  draws: 0,
                  losses: 0,
                  yellowCards: 0,
                  redCards: 0,
                  topScorer: false,
                  topAssists: false,
                  mostValuePlayer: false,
                },
              ]
            }
          ],
          nationalSelection: [
            {
              season: '2022 - 2023',
              goals: 0,
              assists: 0,
              games: 0,
              yellowCards: 0,
              redCards: 0,
              trophies: 0,
              wins: 0,
              draws: 0,
              losses: 0,
            }
          ],
        },
      }
    },
    methods: {
      hideItems() {
        const allItems = document.querySelector('.accordion-data').querySelectorAll('.item');
        allItems.forEach((element) => {
          element.classList.remove('open');
        });
      }
    },
  }
</script>

<style lang="scss" scoped>
  .content {
    min-height: 100vh;
    padding: 0 2rem;
  }
  .header-view {
    display: flex;
    justify-content: space-between;
    align-items: center;

    div {
      p {
        color: #fff;
        font-size: 3rem;
        line-height: 3rem;
      }
    }
    .logo-team {
      max-width: 150px;
      padding: 1rem;
      box-sizing: border-box;
    }
  }
  .body-view {
    .accordion-data {
      .item {
        position: relative;
        display: block;
        .item-header {
          background: rgba(0, 0, 0, .3);
          padding: 1rem 2rem;
          cursor: pointer;
          p {
            text-align: left;
            color: #fff;
          }
        }
        .item-body {
          background: rgba(0, 0, 0, .1);
          height: 0;
          max-height: 500px;
          overflow: hidden;
        }
      }
    }
  }
</style>