<template>
    <div>
        <form class="item-card__form grid-column-2" action="">
            <label for="idProveedor">Id del Proveedor</label>
            <input class="item-card__form-input" type="text" name="idProveedor" id="idProveedor" v-model="proveedor.idProveedor">

            <label for="nombreProveedor">Nombre</label>
            <input class="item-card__form-input" type="text" name="nombreProveedor" id="nombre_proveedor" v-model="proveedor.nombreProveedor">

            <label for="imgProveedor">Imagen</label>
            <input class="item-card__form-input" type="text" name="imgProveedor" id="img_proveedor" v-model="proveedor.imgProveedor">

            <div>
                <button class="link-button" type="submit" v-on:click="guardar()">Guardar</button>
                <button class="link-button" type="submit" v-on:click="eliminar(proveedor.idProveedor)">Eliminar</button>
            </div>
        </form>
    </div>
</template>

<script>
import axios from 'axios'

export default {
  name:'formularioProveedores',
data:function (){
return{
proveedor: {
idProveedor:"",
nombreProveedor:"",
imgProveedor: ""
}
}
},
methods:{
guardar(){

axios.post('http://localhost:8080/api/proveedores',this.proveedor)
.then(data=>{

console.log(data);

})

},eliminar(id){

    
    axios.delete('http://localhost:8080/api/proveedores/'+id)
    .then(data=>{

console.log(data);

})
//location.reload()  
}
}
}

</script>
