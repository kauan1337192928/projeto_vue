<template>
 <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
 <p v-else>Estou em busca de novas oportunidades</p>
   <p>Utilizo as seguintes tecnologias para back-end:</p>
   <ul >
     <li v-for="(tecnology, index) in backedn_technologies" v-bind:key="index">{{ tecnology }}</li>
   </ul>
<p>Utilizo as seguintes tecnologias para front-end:</p>
<ul>
  <li v-for="technology in frontend_technologies" :key="technology.id">{{ technology.language }}</li>


</ul>


   <button @click="showEmail"> {{textoBotao}}</button>
   <p v-show="mostrar_email">Mande uma mensagem para {{ email }}</p>
   <p class= "teste">Para acessar meu portifólio <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a></p>
   <Picture/>
</template>

<script>
import Picture from './Picture.vue';

export default{
    name:'Info',
    components:{
      Picture
    },
    data(){
      return{
        esta_trabalhando: true,
        mostrar_email: true,
        email: 'kauagacontreras@gmail.com',
        meu_link: 'https://www.youtube.com/watch?v=dQw4w9WgXcQ&list=RDdQw4w9WgXcQ&start_radio=1',
        textoBotao: 'Mostrar e-mail',
        backedn_technologies: ['JavaScript', 'PHP', 'Python'],
        frontend_technologies:[
          {id:1, language: 'HTML'},
          {id:2, language: 'CSS'},
          {id:3, language: 'Vue'}
        ]
      }
    },
    methods:{
      showEmail(){
        this.mostrar_email = !this.mostrar_email
        if(!this.mostrar_email){
          this.textoBotao = 'Mostrar e-mail'
        } else {
          this.textoBotao = 'Esconder e-mail'

        }
        }
      }
    }
</script>