<script setup>
let wholeNum
let topFracNum
let bottomFracNum
let calculate = (wholeNum) => {
  let fullCut
  let halfCut
  let finalHalf
  fullCut = 97 - wholeNum
  halfCut = fullCut / 2
  finalHalf = 97 - halfCut
  return finalHalf
}
let calculatedResult
</script>
<template>
  <h1>Measurement</h1>
  <div class="container">
    <input type="number" name="Whole Number" id="whole-num" v-model="wholeNum">
    <input type="number" name="Top Fraction Number" id="top-frac-num" v-model="topFracNum">
    <input type="number" name="Bottom Fraction Number" id="btm-frac-num" v-model="bottomFracNum">
    <div id="fraction-line">______________________________</div>
  </div>
  <input type="button" value="Calculate" id="calc-btn" v-on:click="calculate">
  <h1 v-bind=""></h1>
</template>

<style scoped>
.container {
  display: grid;
  grid-template-columns: 2fr;
  grid-template-rows: 3fr;
  justify-items: center;
}
#whole-num {
  grid-column: 1;
  grid-row: 2;
}
#top-frac-num {
  grid-column: 2;
  grid-row: 1;
}
#btm-frac-num {
  grid-column: 2;
  grid-row: 3;
}
#fraction-line {
  grid-column: 2;
  grid-row: 2;
  padding-top: 7px;

}
input {
  padding: .7rem;
  margin: .3rem;
}
#calc-btn {
  float: right;
}
</style>
