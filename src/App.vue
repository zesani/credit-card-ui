<template>
  <div id="app">
    <div class="card">
      <h1 :style="{ color: 'white'}">Payment details</h1>
      <div class="number-card">
        <h3 :style="{color: 'white'}">Card Number</h3>
        <input type="text" class="number-card-input" maxlength="4" v-model="number1" placeholder="XXXX">
        <input type="text" class="number-card-input" maxlength="4" v-model="number2" placeholder="XXXX">
        <input type="text" class="number-card-input" maxlength="4" v-model="number3" placeholder="XXXX">
        <input type="text" class="number-card-input" maxlength="4" v-model="number4" placeholder="XXXX">
      </div>
      <div class="date-card">
        <h3 class="head-expiration" :style="{color: 'white'}">Expiration</h3>
        <h3 class="head-cvc" :style="{color: 'white'}">CVC Code</h3>
        <select class="select-mouth" name="">
          <option value="">Month</option>
          <option value="1">January</option>
          <option value="2">February</option>
          <option value="3">March</option>
          <option value="4">April</option>
          <option value="5">May</option>
          <option value="6">June</option>
          <option value="7">July</option>
          <option value="8">August</option>
          <option value="9">September</option>
          <option value="10">October</option>
          <option value="11">November</option>
          <option value="12">December</option>
        </select>
        <select class="select-year" name="">
          <option value="">Year</option>
          <option value="2016">2016</option>
          <option value="2017">2017</option>
          <option value="2018">2018</option>
          <option value="2019">2019</option>
          <option value="2020">2020</option>
          <option value="2021">2021</option>
          <option value="2022">2022</option>
          <option value="2023">2023</option>
          <option value="2024">2024</option>
          <option value="2025">2025</option>
        </select>

        <input type="text" class="input-cvc" v-model="cvc"  maxlength="3" placeholder="XXX">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  components: {
  },
  data () {
    return {
      mouth: '',
      year: '',
      numberCard: '',
      number1: '',
      number2: '',
      number3: '',
      number4: '',
      cvc: ''
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Lato');
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
  font-family: 'Lato', sans-serif;
}
.card {
  border: 0px solid black;
  margin-left: 10%;
  width: 500px;
  height: 300px;
  background-color: #28d8b2;
  border-radius: 20px;
  padding-top: 40px;
  padding-left: 3%;
  padding-right: 3%;

}
.select-mouth {
  border-radius: 5px;
  background-color: white;
  height: 40px;
  width: 38%;
  padding-left: 5%;
  border: 0px solid white;
  display: inline-block;
  margin-right: 3%;
}
.select-year {
  border-radius: 5px;
  background-color: white;
  height: 40px;
  width: 26%;
  padding-left: 4%;
  border: 0px solid white;
  display: inline-block;
  margin-right: 5%;
}
.input-cvc {
  border-radius: 5px;
  background-color: white;
  text-align: center;
  height: 40px;
  width: 22%;
  border: 0px solid white;
  display: inline-block;
}
.date-card {
  display: inline-block;
  font-size: 1.4em;
  margin-bottom: 0px;
}
.head-expiration {
  width: 76%;
  margin-left: 0px;
  display: inline-block;
}
.head-cvc {
  display: inline-block;
}
.number-card-input {
  display: inline-block;
  height: 40px;
  border-radius: 5px;
  font-size: 1.4em;
  width: 24%;
  text-align: center;
  border: 0px solid white;
}
</style>
