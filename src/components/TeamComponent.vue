<template>
  <div>
    <table>
      <thead>
        <tr>
          <th>Name</th>
          <th>Last Name</th>
          <th>Age</th>
          <th>Position</th>
          <th>Country</th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="(player, index) in team"
          :key="index">
          <td>{{ player.name }}</td>
          <td>{{ player.lastName }}</td>
          <td>{{ player.age }}</td>
          <td>{{ player.position }}</td>
          <td>{{ player.country }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
  export default {
    name: "teamComponent",
    data() {
      return {
        team: [
          {
            name: 'Mike',
            lastName: 'Mainan',
            position: 'POR',
            age: 27,
            country: 'France'
          },
          {
            name: 'Theo',
            lastName: 'Hernandez',
            position: 'LTI',
            age: 25,
            country: 'France'
          },
          {
            name: 'Sandro',
            lastName: 'Tonali',
            position: 'MCD',
            age: 22,
            country: 'Italy'
          },
          {
            name: 'Rafael',
            lastName: 'Leao',
            position: 'DC',
            age: 23,
            country: 'Portugal'
          },
          {
            name: 'Olivier',
            lastName: 'Giroud',
            position: 'DC',
            age: 36,
            country: 'France'
          }
        ]
      }
    }
  }
</script>

<style lang="scss" scoped>
  table {
    display: block;
    width: 100%;
    thead,
    tbody {
      display: block;
      width: 100%;
      tr {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        text-align: center;
        padding: 0.5rem 0;
        &:nth-child(even) {
          background: rgba(0, 0, 0, 0.1);
        }
        th,
        td {
          width: 100%;
          color: #fff;
        }
      }
    }
    thead {
      tr {
        background: rgba(0, 0, 0, 0.1);
      }
    }
  }
</style>