<template lang="html">
  <div class="dashboard">
    <div class="chart">
      <div class="extra">
        <div class="columns is-multiline">
          <div class="column head-column">
            <div class="columns">
              <div class="column part-left">
                <div class="figure">
                  <i class="fas fa-list-alt fa-5x"></i>
                </div>
              </div>
              <div class="column part-right box">
                <div class="title">
                  100
                </div>
                <div class="subtitle">
                  Total Invoices
                </div>
              </div>
            </div>
          </div>
          <div class="column head-column">
            <div class="columns">
              <div class="column part-left">
                <div class="figure">
                  <i class="far fa-address-card fa-5x"></i>
                </div>
              </div>
              <div class="column part-right box">
                <div class="title">
                  25
                </div>
                <div class="subtitle">
                  Total Users
                </div>
              </div>
            </div>
          </div>
          <div class="column head-column">
            <div class="columns">
              <div class="column part-left">
                <div class="figure">
                  <i class="fa fa-suitcase fa-5x"></i>
                </div>
              </div>
              <div class="column part-right box">
                <div class="title">
                  20
                </div>
                <div class="subtitle">
                  Total Products
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="tile is-ancestor">
        <div class="tile is-parent">
          <article class="tile is-child box">
            <h4 class="title">Daily</h4>
            <div class="block">
              <chartist class="lines-bars" :type="'Bar'" :data="linesData" :options="linesOptions"></chartist>
            </div>
          </article>
        </div>
        <div class="tile is-parent">
          <article class="tile is-child box" style="height: 240px;">
            <h4 class="title">Monthly</h4>
            <div class="block">
              <chartist class="lines-bars" :type="'Line'" :data="lineAreaData" :options="lineAreaOptions"></chartist>
            </div>
          </article>
        </div>
        <div class="tile is-parent">
          <article class="tile is-child box">
            <h4 class="title">Yearly</h4>
            <div class="content">
              <chartist class="lines-bars" :type="'Pie'" :data="pieData" :options="pieOptions"></chartist>
            </div>
          </article>
        </div>
      </div>
      <!-- Table -->
      <div>
        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <h4 class="title">Table</h4>
              <table class="table">
                <thead>
                  <tr>
                    <th>Name</th>
                    <th>Instrument</th>
                    <th></th>
                    <th></th>
                  </tr>
                </thead>
                <tfoot>
                  <tr>
                    <th>Name</th>
                    <th>Instrument</th>
                    <th></th>
                    <th></th>
                  </tr>
                </tfoot>
                <tbody>
                  <tr>
                    <td>Misty Abbott</td>
                    <td>Bass Guitar</td>
                    <td class="is-icon">
                      <a href="#">
                        <i class="fa fa-twitter"></i>
                      </a>
                    </td>
                    <td class="is-icon">
                      <a href="#">
                        <i class="fa fa-instagram"></i>
                      </a>
                    </td>
                  </tr>
                  <tr>
                    <td>John Smith</td>
                    <td>Rhythm Guitar</td>
                    <td class="is-icon">
                      <a href="#">
                        <i class="fa fa-twitter"></i>
                      </a>
                    </td>
                    <td class="is-icon">
                      <a href="#">
                        <i class="fa fa-instagram"></i>
                      </a>
                    </td>
                  </tr>
                  <tr>
                    <td>Robert Mikels</td>
                    <td>Lead Guitar</td>
                    <td class="is-icon">
                      <a href="#">
                        <i class="fa fa-twitter"></i>
                      </a>
                    </td>
                    <td class="is-icon">
                      <a href="#">
                        <i class="fa fa-instagram"></i>
                      </a>
                    </td>
                  </tr>
                  <tr>
                    <td>Karyn Holmberg</td>
                    <td>Drums</td>
                    <td class="is-icon">
                      <a href="#">
                        <i class="fa fa-twitter"></i>
                      </a>
                    </td>
                    <td class="is-icon">
                      <a href="#">
                        <i class="fa fa-instagram"></i>
                      </a>
                    </td>
                  </tr>
                </tbody>
              </table>
            </article>
          </div>
        </div>
        <div class="tile is-ancestor">
          <div class="tile is-parent is-4">
            <article class="tile is-child box">
              <h4 class="title">Table is-bordered</h4>
              <table class="table is-bordered">
                <thead>
                  <tr>
                    <th>One</th>
                    <th>Two</th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td>Three</td>
                    <td>Four</td>
                  </tr>
                </tbody>
              </table>
            </article>
          </div>
          <div class="tile is-parent is-4">
            <article class="tile is-child box">
              <h4 class="title">Table is-striped</h4>
              <table class="table is-striped">
                <thead>
                  <tr>
                    <th>One</th>
                    <th>Two</th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td>Three</td>
                    <td>Four</td>
                  </tr>
                  <tr>
                    <td>Five</td>
                    <td>Six</td>
                  </tr>
                  <tr>
                    <td>Seven</td>
                    <td>Eight</td>
                  </tr>
                </tbody>
              </table>
            </article>
          </div>
          <div class="tile is-parent is-4">
            <article class="tile is-child box">
              <h4 class="title">Table is-narrow</h4>
              <table class="table is-narrow">
                <thead>
                  <tr>
                    <th>One</th>
                    <th>Two</th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td>Three</td>
                    <td>Four</td>
                  </tr>
                  <tr>
                    <td>Five</td>
                    <td>Six</td>
                  </tr>
                  <tr>
                    <td>Seven</td>
                    <td>Eight</td>
                  </tr>
                </tbody>
              </table>
            </article>
          </div>
        </div>
      </div>
      <div class=" foot box">
        <nav class="level">
          <div class="level-item has-text-centered">
            <div>
              <p class="heading">Tweets</p>
              <p class="title">3,456</p>
            </div>
          </div>
          <div class="level-item has-text-centered">
            <div>
              <p class="heading">Following</p>
              <p class="title">123</p>
            </div>
          </div>
          <div class="level-item has-text-centered">
            <div>
              <p class="heading">Followers</p>
              <p class="title">456K</p>
            </div>
          </div>
          <div class="level-item has-text-centered">
            <div>
              <p class="heading">Likes</p>
              <p class="title">789</p>
            </div>
          </div>
        </nav>
      </div>
    </div>
  </div>
</template>

<script>
import Chartist from 'vue-bulma-chartist';
import Auth from '@/packages/auth/Auth.js';
import api from '@/api/main';

export default {
  name: 'dashboard',
  components: {
    Chartist
  },
  created() {
  },
  data() {
    return {
      json: {},
      //daily
      series: [
        [12, 9, 7, 8, 5],
      ],
      labels: ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday'],
      linesOptions: {
        chartPadding: {
          right: 0
        }
      },
      //monthly
      lineAreaData: {
        labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'June', 'July', 'Aug'],
        series: [
          [5, 9, 7, 8, 5, 3, 5, 4]
        ]
      },
      lineAreaOptions: {
        low: 0,
        showArea: true
      },
      //yearly
      pieData: {
        series: [2015, 2016, 2017]
      },
      pieOptions: {
        //  chartPadding: 30,
        //  labelOffset: 40,
        labelDirection: 'explode',
        labelInterpolationFnc(value) {
          return value
        }
      },
    }
  },
  computed: {
    linesData() {
      return {
        labels: this.labels,
        series: this.series
      }
    }
  },
}
</script>

<style lang="scss">
.dashboard {
  height: 100%;
  .head-column {
    // padding: 0;
    margin: 1rem;
    .box {
      padding: 0;
    }
  }
  .part-left {
    padding: 0;
    .figure {
      min-height: 100%;
      svg {
        margin-left: 25%;
        margin-top: 15%;
      }
    }
  }
  .part-right.box {
    padding: 0;
    height: 8.2rem;
    border-radius: inherit;
  }
  margin-bottom: 1rem;
  margin-right: 1rem;
  .title {
    margin-bottom: 1rem;
  }
  .ct-label {
    font-weight: bold;
  }
  .table-responsive {
    display: block;
    width: 100%;
    min-height: 0.01%;
    overflow-x: auto;
  }
  .figure {
    background: turquoise;
    i {
      font-size: 5rem;
      height: 8.2rem;
      display: flex;
      align-items: center;
      justify-content: center;
    }
  }
  .column {
    .title {
      height: 50%;
      display: flex;
      align-items: flex-end;
      justify-content: center;
    }
    .subtitle {
      height: 30%;
      display: flex;
      align-items: flex-end;
      justify-content: center;
    }
  }
  .foot.box {
    margin-top: 1rem;
  }
}
</style>
