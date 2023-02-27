<script setup>
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
          <input class="form-control" type="number" placeholder="Número A" required>
        </div>
        <div class="col-md-3">
          <input class="form-control" type="number" placeholder="Número B" required>
        </div>
        <div class="col-md-5">
          <select class="form-control" id="selection">
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
          <span id="result"></span>
        </div>
      </div>
      
    </div>
  </main>
  
  
</template>

<style scoped>

</style>
