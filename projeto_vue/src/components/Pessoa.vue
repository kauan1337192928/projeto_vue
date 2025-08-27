<template>
   <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
   <info/>
   <Form/>
</template>


<script>
import Info from './Info.vue';
import Form from './Form.vue';

export default{
    name: 'Pessoa',
    components:{
        Info,
        Form
    },
    data(){
        return{
            nome:'LINDO'
        }
    }
}

</script>