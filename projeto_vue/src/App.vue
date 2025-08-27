<template>
<Header/>
<h1>Olá Mundo!</h1>
<PrimeiroComponente/>
<LifeCycle/>
<Pessoa/>
</template>



  <script>
  import PrimeiroComponente from './components/PrimeiroComponente.vue';
  import LifeCycle from './components/LifeCycle.vue';
  import Pessoa from './components/Pessoa.vue';  
  import Header from './components/Header.vue';


  export default{
    name: 'App',
    components: {
      PrimeiroComponente,
      LifeCycle,
      Pessoa,
      Header
    }
  }

  </script>

<style>
body{
  background-color: black;
  color: white;
}
a{
  color: aquamarine;
}
</style>