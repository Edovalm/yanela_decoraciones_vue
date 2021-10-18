<template>
    <div>
      <h3 class="card__title">Tabla de Categorías</h3>
      <table class="tablaCatedorias tablaRegistros">
        <tr>
          <th>Id</th>
          <th>Nombre</th>
          <th>Imagen</th>
          <th>Descripción</th>
        </tr>
        <tr v-for="categoria in categorias" :key="categoria.idCategorias">
          <td>{{categoria.idCategoria}}</td>
          <td>{{categoria.nombreCategoria}}</td>
          <td>{{categoria.imgCategoria}}</td>
          <td>{{categoria.descripcionCategoria}}</td>
        </tr>
      </table>
      <router-view/>
    </div>
</template>

<script>
import axios from 'axios'
export default{
name:'tablaCategorias',
data(){
  return{
     categorias:[]
  }
},
mounted(){
  let vue=this;
  axios.get('http://localhost:8080/api/categorias/listar')
  .then( response =>{

    vue.categorias=response.data;
  })
},methods:{

}
}
</script>

