<template>
  <div class="container">
    <div class="calendar">
      <section class="parent">
 <div>
    <b-form-input v-model="text" placeholder="Enter your name"></b-form-input>
    <div class="mt-2">Value: {{ text }}</div>
  </div>

      <div @click="append('1')" class="btn">{{ current || '1'}}</div >
      <div @click='display' id="btn2" class="btn">2</div>
      <div @click='display' id="btn2" class="btn">3</div>
      <!-- <div @click='onClick' id="btn" :class="{ red : deleteClicked }">3</div> -->
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
      <div @click='display' class="btn">23
      <b-form-group id="input-group-4">
        <b-form-checkbox-group v-model="form.checked" id="checkboxes-4">
          <b-form-checkbox value="me">First task</b-form-checkbox>
          <b-form-checkbox value="that">Second task</b-form-checkbox>
        </b-form-checkbox-group>
      </b-form-group>
      </div>
      <div @click='display' class="btn">24</div>
      <div @click='display' class="btn">25</div>
      <div @click='display' class="btn">26
      </div>
      <div @click='display' class="btn">27</div>
      <div @click='display' class="btn">28
    <info-card :frontType="'graph'"
      :frontTitle="front.text"
      :frontData="front.graphData"
      :backTitle="back.title"
      :backData="back.message" />
 <!--  </div> -->
      </div>
 </section>
    <div @click='display' class="btn">
      <b-list-group>
      <b-list-group-item>
          <div>
  </div>
      </b-list-group-item>
        <b-list-group-item>2.</b-list-group-item>
        <b-list-group-item>3.</b-list-group-item>
        <b-list-group-item>4.</b-list-group-item>
        <b-list-group-item>5.</b-list-group-item>
    </b-list-group>29</div>

    <div @click='display' class="btn">

    <br>30</div>

    <div @click='display' class="btn">
        31</div>
    </div>
  </div>

</template>

<script>
import InfoCard from 'vue-info-card';
  // import CardAnimationsPage from '/src/components/card';
  export default {
    components: {
      InfoCard
  },
  data() {
    return {
      text: '',
      form: {
          checked: []
        },
      front: {
        title: '30th October',
        graphData: "Hover to see",
      },
      back: {
        title: 'Your tasks for 30th of October:',
        message: '1. Do this <br> 2. Do that <br>3. And another thing <br> 1. Do this <br> 2. Do that <br>3. And another thing <br> 1. Do this <br> 2. Do that <br>3. And another thing',
      },
      newText: '',
      current: ''
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
.container {

}
.calculator {
  margin: 0 auto;
  width: 400px;
  font-size: 40px;

}
.btn {
  background-color: #F2F2F2;
  border: 1px solid #999;
  width: 190px;
  height: 240px;
  margin: 8px;
  box-shadow: 1px 0.5px 3px gray;
  opacity: 1.0;
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
        width: 100%;
        color: white;
      }

.list-group-item {
  width: 130px;
  height: 35px;
}
.btn:hover {
  box-shadow: 2px 0.5px 8px gray;
  opacity: 0.3;
  transition: 0.8s;
  height: 500px;
  width: 400px;
}
.parent:hover > .btn {
  opacity: 0.3;
  transition: 0.8s;
}
.parent:hover > .btn:hover {
  opacity: 1.0;
}
*, *::before, *::after {
  font-size: 10px;
}
.mt-3, .mb-0 {
  color: red;
  font-size: 50px;
}

</style>
