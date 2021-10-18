<template>
    <div>
      <h3 class="card__title">Tabla de Proveedores</h3>
      <table class="tablaProveedores tablaRegistros">
        <tr>
          <th>Id</th>
          <th>Nombre</th>
          <th>Imagen</th>
        </tr>
        <tr v-for="proveedor in proveedores" :key="proveedor.idProveedores">
          <td>{{proveedor.idProveedor}}</td>
          <td>{{proveedor.nombreProveedor}}</td>
          <td>{{proveedor.imgProveedor}}</td>
        </tr>
      </table>
      <router-view/>
    </div>
</template>

<script>
import axios from 'axios'
export default{
name:'tablaProveedores',
data(){
  return{
     proveedores:[]
  }
},
mounted(){
  let vue=this;
  axios.get('http://localhost:8080/api/proveedores/listar')
  .then( response =>{

    vue.proveedores=response.data;
  })
},methods:{

}
}

</script>

