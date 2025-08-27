<template>
    <div>
    <h1>Olá Vue</h1>
    <p>Meu Nome é: {{ nome }} e trabalho como {{ trabalho }}</p>
    <MultiplosEventos/>
</div>
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue';

export default{
    name: 'PrimeiroComponente',
    components:{
        MultiplosEventos
    },
    data(){
        return{
           nome:"Kauan Gabriel",
           trabalho:"Garoto de programa"
        }
    }
}
</script>
