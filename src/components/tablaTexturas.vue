<template>
    <div>
      <h3 class="card__title">Tabla de Texturas</h3>
      <table  class="tablaTexturas tablaRegistros">
        <tr>
          <th>Id</th>
          <th>Nombre</th>
          <th>Imagen</th>
        </tr>
        <tr v-for="textura in texturas" :key="textura.idTexturas">
          <td>{{textura.idTextura}}</td>
          <td>{{textura.nombreTextura}}</td>
          <td>{{textura.imgTextura}}</td>
        </tr>
      </table>
      <router-view/>
    </div>
</template>

<script>
import axios from 'axios'
export default{
name:'tablaTexturas',
data(){
  return{
     texturas:[]
  }
},
mounted(){
  let vue=this;
  axios.get('http://localhost:8080/api/texturas/listar')
  .then( response =>{

    vue.texturas=response.data;
  })
},methods:{
}
}
</script>
