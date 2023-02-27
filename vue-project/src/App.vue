<script>
  export default {
    data() {
      return { numberA: '', numberB: '', selected: ''}
    },
    computed: {
    arit() {
      if (this.selected && this.numberA && this.numberB){
        if (this.selected === "Adição"){
          return this.numberA + this.numberB
        } else if (this.selected === "Subtração"){
          return this.numberA - this.numberB
        } else if (this.selected === "Multiplicação"){
          return this.numberA * this.numberB
        } else{
          if (this.numberB === 0){
            return "Erro matemático!"
          } else{
            return this.numberA / this.numberB
          }
        }
      }
      return "......."
    },
  },
  }
</script>

<template>
  <header>
    <div class="container-fluid" id="first">
      <h1 class="title">Calculadora Aritmética</h1>
    </div>
    <div class="side">
      <img alt="site logo" class="logo" src="./assets/images/calculator-4151004_960_720.png"  />
    </div>
  </header>

  <main>
    <div class="container cont-main">
      <form action="">
        <div class="row">
        <div class="col-md-3">
          <input class="form-control" type="number" placeholder="Número A" required v-model.number="numberA">
        </div>
        <div class="col-md-3">
          <input class="form-control" type="number" placeholder="Número B" required v-model.number="numberB">
        </div>
        <div class="col-md-5">
          <select class="form-control" id="selection" v-model="selected">
            <option value='total' selected disabled>Selecionar operação aritmética</option>
            <option>Adição</option>
            <option>Subtração</option>
            <option>Multiplicação</option>
            <option>Divisão</option>
          </select>
        </div>
      </div>
      </form>
    </div>
    <div class="container">

      <div class="row">
        <h4 style="margin-bottom: 16px;">Resultado da operação: </h4>
      </div>

      <div class="row">
        <div class="col-xs-1 center-block text-center">
          <span id="result">{{ arit }}</span>
        </div>
      </div>

    </div>
  </main>
</template>


