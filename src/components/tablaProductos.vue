<template>
    <div>
      <h3 class="card__title">Tabla de Productos</h3>
      <table class="tablaProveedores tablaRegistros">
        <tr>
          <th>Id</th>
          <th>Nombre</th>
          <th>Precio</th>
          <th>Imagen</th>
          <th>Descripción</th>
          <th>Categoría</th>
          <th>Proveedor</th>
          <!-- <th>Textura(s)</th> -->
        </tr>
        <tr v-for="producto in productos" :key="producto.idProductos">
          <td>{{producto.idProducto}}</td>
          <td>{{producto.nombreProducto}}</td>
          <td>{{producto.precioProducto}}</td>
          <td>{{producto.imgProducto}}</td>
          <td>{{producto.descripcionProducto}}</td>
          <td>{{producto.categoriaProducto.idCategoria}}</td>
          <td>{{producto.proveedorProducto.idProveedor}}</td>
          <!-- <td>{{producto.texturas}}</td> -->
        </tr>
      </table>
      <router-view/>
    </div>
</template>

<script>
import axios from 'axios'
export default{
name:'tablaProductos',
data(){
  return{
     productos:[]
  }
},
mounted(){
  let vue=this;
  axios.get('http://localhost:8080/api/productos/listar')
  .then( response =>{

    vue.productos=response.data;
  })
},methods:{
}
}
</script>

