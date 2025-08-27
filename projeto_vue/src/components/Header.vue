<template>
<ul>
    <li><a href="#">Home</a> </li>
    <li><a href="#">Projetos</a> </li>
    <li><a href="#">Contato</a> </li>
</ul>
</template>


<script>
export default{
    name: 'Header'
}
</script>

<style scoped>
ul{
    list-style: none;
    display: flex;
    background-color: cadetblue;
}
li{
    margin-right: 15px;
}
a{
    color: white;
    text-decoration: none;
    transition: .5s;
}

a:hover{
    color: deeppink;
}
</style>