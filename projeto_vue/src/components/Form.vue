<template>
    <h2>Meu formulário</h2>
<form action="" @submit="enviarFormulario($event)">
    <div>
        <input type="text" v-model="name">
    </div>
    <div>
<input type="text" v-model="email">
    </div>
    <div>
<Submit/>
    </div>
</form>
<p>Conteudo</p>
<p>Conteudo</p>
<p>Conteudo</p>
</template>

<script>
import InputText from './form/InputText.vue';
import Submit from './form/Submit.vue';

export default{
    name: 'Form',
    components:{
        InputText,
        Submit,
    },
    data(){
        return{
           name:"",
           email:""
        }
    },
    methods:{
        enviarFormulario(e){

            e.preventDefault();  

            const name = this.name;
            const email = this.email;

            console.log("Formulario Enviado");
            console.log("o nome é:" + name);
            console.log("o email é:" + email); 

        }
    }
}
</script>

<style scoped>
p{
    margin: 50px;
}
</style>