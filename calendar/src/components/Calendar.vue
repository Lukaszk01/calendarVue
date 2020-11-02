

<template>

  <div class="container">
    <div class="calendar">
      <div @click="append('1')" class="btn">{{ current || '1'}}</div >
      <div @click='display' id="btn2" class="btn">2</div>
      <div @click='onClick' id="btn" :class="{ red : deleteClicked }">3</div>
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
    <div @click='display' class="btn">
      <b-list-group>
      <b-list-group-item>
        <div>
          <b-form-textarea
            id="textarea"
            v-model="text"
            placeholder="Enter something..."
            rows="3"
            max-rows="6"></b-form-textarea>
          <pre class="mt-3 mb-0">{{ text }}</pre>
        </div>
      </b-list-group-item>
        <b-list-group-item>2.</b-list-group-item>
        <b-list-group-item>3.</b-list-group-item>
        <b-list-group-item>4.</b-list-group-item>
        <b-list-group-item>5.</b-list-group-item>
    </b-list-group>29</div>


    <div @click='display' class="btn">
    30</div>

    <div @click='display' class="btn">
        31</div>
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
      text: '',
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
  width: 100px;
  height: 10px;
  background-color: #F2F2F2;
  border: none;
  font-size: 5px;
}

.list-group-item {
  width: 130px;
  height: 35px;
}










</style>
