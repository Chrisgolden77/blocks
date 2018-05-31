<template>
  <div id="app">
    <!-- <h3 v-if="amount != 1">Count: {{amount}} clicks </h3>
    <h3 v-else> Count: {{amount}} click </h3> -->
    <div id="button-area">
      <h1>BLOXY</h1>
      <button class="incriment" @click="incriment">+</button>
      <button class="decriment" @click="decriment">-</button>
    </div>
    <div id="box-area">
      <div class="block" :key="n" v-for="n in amount"></div>
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      amount: 0
    };
  },


  methods: {
    incriment() {
      this.amount ++;
    },
    decriment() {
      this.amount --;
    }
  }
}
</script>

<style>
body {
  display: flex;
  flex-flow: column;
  align-items: center;
  background-color: salmon;

}
#button-area {
  text-align: center;
}
button {
  font-size: 35px;
  padding: 0px;
  margin: 10px;
  height: 50px;
  width: 50px;
  color: white;
  background-color: lightskyblue;
  border-style: none;
  border-radius: 10px;
}
button:hover {
  background: lightcyan;
  cursor: pointer;
}
.block {
  border-radius: 15px;
  background: slateblue;
  height: 80px;
  width: 80px;
  margin: 3px;
}
.block:hover {
  transition: .35s;
  background: paleturquoise;
  border-radius: 20px;
  width: 70px;
  height: 70px;
}

#box-area {
  max-width: 800px;
  float: left;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

</style>
