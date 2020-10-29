
  Vue.config.devtools = false;
  Vue.config.productionTip = false;
  <template>
  <div class="container">
    <div class="calendar">
    <div @click="append('1')" class="btn">{{ current || '1'}}</div>
    <div @click='display' id="btn2" class="btn">2</div>
    <div @click='onClick' :class="{ red : deleteClicked }" class="btn">3</div>
    <div @click='display' class="btn">4</div>
    <div @click='display' class="btn">5</div>
    <div @click='display' class="btn">6</div>
    <div @click='display' class="btn">7</div>
    <div @click='display' class="btn">8</div>
    <div @click='display' class="btn">9</div>
    <div @click='display' class="btn">10</div>
    <div @click='display' class="btn">11</div>
    <div @click='display' class="btn">12</div>
    <div @click='display' class="btn">12</div>
    <div @click='display' class="btn">13</div>
    <div @click='display' class="btn">14</div>
    <div @click='display' class="btn">15</div>
    <div @click='display' class="btn">16</div>
    <div @click='display' class="btn">17</div>
    <div @click='display' class="btn">18</div>
    <div @click='display' class="btn">19</div>
    <div @click='display' class="btn">20</div>
    <div @click='display' class="btn">21</div>
    <div @click='display' class="btn">23</div>
    <div @click='display' class="btn">24</div>
    <div @click='display' class="btn">25</div>
    <div @click='display' class="btn">26</div>
    <div @click='display' class="btn">27</div>
    <div @click='display' class="btn">28</div>
    <div @click='display' class="btn">29</div>
    <div @click='display' class="btn">30</div>
    <div @click='display' class="btn">31</div>

  </div>
  </div>

</template>

<script>
  export default {
  data() {
    return {
      previous: null,
      current: '',
      operator: null,
      operatorClicked: false,
      show: false,
      deleteClicked: false
    }
  },
  methods: {
    display: function (event) {
      // `this` inside methods point to the Vue instance
      alert('This date is not aval. ' + this.name + '!')
      // `event` is the native DOM event
      alert(event.target.tagName)
    },
    onClick() {
      this.deleteClicked = true;
    }
  }
}

</script>


<style scoped>
.red {
  background-color: red;
}
.calculator {
  margin: 0 auto;
  width: 400px;
  font-size: 40px;
  grid-auto-rows: minmax(50px, auto);
}
.btn {
  background-color: #F2F2F2;
  border: 1px solid #999;
  width: 150px;
  height: 200px;
  margin: 8px;
  box-shadow: 1px 0.5px 3px gray;
}
/*.btn:hover {
  height: 500px;
  width: 400px;
  transition: 3s;

}
*/
</style>
