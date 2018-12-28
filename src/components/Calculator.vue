<template>
  <div class="calculator">
    <div class="display"> {{ current || 0}} </div>
    <div @click="fraction" class="btn"> a / b </div>
    <div @click="pow" class="btn"> ^ </div>
    <div @click="root" class="btn"> √ </div>
    <div @click="logarithm" class="btn"> log </div>
    <div @click="logNatural" class="btn"> ln </div>
    <div @click="sin" class="btn"> sin </div>
    <div @click="cos" class="btn"> cos </div>
    <div @click="tan" class="btn"> tan </div>
    <div @click="del" class="btn"> DEL </div>
    <div @click="clear" class="btn"> C </div>
    <div @click="append('7')" class="btn number"> 7 </div>
    <div @click="append('8')" class="btn number"> 8 </div>
    <div @click="append('9')" class="btn number"> 9 </div>
    <div @click="multiply" class="btn"> x </div>
    <div @click="divide" class="btn"> ÷ </div>
    <div @click="append('4')" class="btn number"> 4 </div>
    <div @click="append('5')" class="btn number"> 5 </div>
    <div @click="append('6')" class="btn number"> 6 </div>
    <div @click="sum" class="btn"> + </div>
    <div @click="sub" class="btn"> - </div>
    <div @click="append('1')" class="btn number"> 1 </div>
    <div @click="append('2')" class="btn number"> 2 </div>
    <div @click="append('3')" class="btn number"> 3 </div>
    <div @click="equals" class="btn"> = </div>
    <div @click="dot" class="btn"> . </div>
    <div @click="append('0')" class="btn zero number"> 0 </div>
    <div @click="sign" class="btn"> + / - </div>
    <div @click="percent" class="btn"> % </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      current: '',
    }
  },
  methods: {
    clear() {
      this.current = '';
    },
    percent() {
      this.current = `${parseFloat(this.current) / 100}`
    },
    sign() {
      this.current = this.current.charAt(0) === '-' ? 
        this.current.slice(1) : `-${this.current}`;
    },
    append(number) {
      this.current = `${this.current}${number}`;
    },
    dot() {
      if (this.current.indexOf('.') === -1) {
        this.append('.');
      }
    },
    fraction() {

    },
    pow() {

    },
    root() {

    },
    logarithm() {

    },
    logNatural() {

    },
    sin() {

    },
    cos() {

    },
    tan() {

    },
    del() {

    },
    multiply() {

    },
    divide() {

    },
    sum() {

    },
    sub() {

    },
    equals() {

    },
  }
}
</script>

<style scoped>
.calculator {
  margin: 0 auto;
  width: 600px;
  font-size: 40px;
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-auto-rows: minmax(50px, auto);
}

.display {
  height: 60px;
  padding-top: 20px;
  padding-right: 20px;
  margin-bottom: 5px;
  text-align: right;
  grid-column: 1 / 6;
  background-color: #5A5050;
  color: #E5EEC1;
  border: 1px solid black;
  border-radius: 25px;
}

.zero {
  grid-column: 1 / 4;
}

.btn {
  padding: 10px;
  margin: 5px;
  background-color: #547A82;
  border: 1px solid black;
  color: black;
  border-radius: 15px;
  cursor: pointer;
}

.number {
  background-color: #3EACA8;
}
</style>
