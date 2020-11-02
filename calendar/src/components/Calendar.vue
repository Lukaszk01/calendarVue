

<template>
  <div class="container">
    <div class="calendar">
      <movable @click="append('1')" class="btn">{{ current || '1'}}</movable >
      <movable @click='display' id="btn2" class="btn">2</movable>
      <movable @click='onClick' id="btn" :class="{ red : deleteClicked }">3</movable>
      <movable @click='display' class="btn">4</movable>

    <movable @click='display' class="btn">5</movable>
    <movable @click='display' class="btn">6</movable>
    <movable @click='display' class="btn">7</movable>
    <movable @click='display' class="btn">8</movable>
    <movable @click='display' class="btn">9</movable>
    <movable @click='display' class="btn">10</movable>
    <movable @click='display' class="btn">11</movable>
    <movable @click='display' class="btn">12</movable>
    <movable @click='display' class="btn">12</movable>
    <movable @click='display' class="btn">13</movable>
    <movable @click='display' class="btn">14</movable>
    <movable @click='display' class="btn">15</movable>
    <movable @click='display' class="btn">16</movable>
    <movable @click='display' class="btn">17</movable>
    <movable @click='display' class="btn">18</movable>
    <movable @click='display' class="btn">19</movable>
    <movable @click='display' class="btn">20</movable>
    <movable @click='display' class="btn">21</movable>
    <movable @click='display' class="btn">23</movable>
    <movable @click='display' class="btn">24</movable>
    <movable @click='display' class="btn">25</movable>
    <movable @click='display' class="btn">26</movable>
    <movable @click='display' class="btn">27</movable>
    <movable @click='display' class="btn">28</movable>
    <movable @click='display' class="btn">29</movable>
    <movable @click='display' class="btn">30</movable>
    <movable @click='display' class="btn">
      <span>Your task:</span>
        <p style="white-space: pre-line;">{{ message }}</p>
        <br>
        <textarea v-model="message" placeholder="Type"></textarea>
        31</movable>
  </div>
  </div>
<!--   <div style="position:relative; margin:50px;">
    <movable class="btn" target="parentEl">modal behavior</movable>`
      <movable class="testmove" posTop="444" posLeft="444" :bounds="{y:[0,0]}"><span>bounds:only x</span></movable>
     </div>
 -->
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
  border: 1px solid #999;
  width: 150px;
  height: 200px;
  margin: 8px;
  box-shadow: 1px 0.5px 3px gray;
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
.testmove {
        display:block;
        position: absolute;
        top: 0;
        height: 150px;
        width: 150px;
        margin: 200px;
        background: #333;
        color: white;
      }
      .modaltitle {
        background: blue;
        display:block;
        width:100%;
        color: white;
      }
textarea {
  width: 120px;
  background-color: #F2F2F2;
  border: none;
}


</style>
