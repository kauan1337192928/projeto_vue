<template>
  <img v-bind:src="avatar" :alt="descrição">
  <MudarImagem/>
</template>

<script>
import MudarImagem from './MudarImagem.vue';


export default{
    name:'Picture',
    components:{
    MudarImagem
},
    data(){
        return{
            avatar:'/img/avatar.png',
            descrição: 'Kauan Gabriel'
        }
    }
}
</script>