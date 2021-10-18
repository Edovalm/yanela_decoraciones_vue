<template>
    <div>
        <form class="item-card__form grid-column-2" action="">
            <label for="idProducto">Id del Producto</label>
            <input class="item-card__form-input" type="text" name="idProducto" id="idProducto" v-model="producto.idProducto">

            <label for="nombreProducto">Nombre</label>
            <input class="item-card__form-input" type="text" name="nombreProducto" id="nombre_producto" v-model="producto.nombreProducto">

            <label for="precioProducto">Precio</label>
            <input class="item-card__form-input" type="text" name="precioProducto" id="precio_producto" v-model="producto.precioProducto">

            <label for="imgProducto">Imagen</label>
            <input class="item-card__form-input" type="text" name="imgProducto" id="img_producto" v-model="producto.imgProducto">

            <label for="descripcionProducto">Descripcion</label>
            <input class="item-card__form-input" type="text" name="descripcionProducto" id="descripcion_producto" v-model="producto.descripcionProducto">

            <label for="categoriaProducto">Id de la Categoría del Producto (Debe estar registrado)</label>
            <input class="item-card__form-input" type="text" name="categoriaProducto" id="categoria_producto" v-model="producto.categoriaProducto.idCategoria">

            <label for="proveedorProducto">Id del Proveedor del Producto (Debe estar registrado)</label>
            <input class="item-card__form-input" type="text" name="proveedorProducto" id="proveedor_producto" v-model="producto.proveedorProducto.idProveedor">

            <!-- <label for="texturaProducto">Id de una Textura del Producto (Debe estar registrado)</label>
            <input class="item-card__form-input" type="text" name="texturaProducto" id="textura_producto" v-model="producto.productos_texturas.idTextura"> -->

            <div>
                <button class="link-button" type="submit" v-on:click="guardar()">Guardar</button>
                <button class="link-button" type="submit" v-on:click="eliminar(producto.idProducto)">Eliminar</button>
            </div>
        </form>
    </div>
</template>

<script>
import axios from 'axios'
export default {
  name:'formularioProductos',
data:function (){
return{
producto: {
idProducto:"",
nombreProducto:"",
precioProducto:"",
imgProducto: "",
descripcionProducto: "",
categoriaProducto:{idCtegoria:""},
proveedorProducto:{idProveedor:""}
// texturas: [
//       { idTextura: "" }
//     ]
}
}
},
methods:{
guardar(){
axios.post('http://localhost:8080/api/productos',this.producto)
.then(data=>{
console.log(data);
})
},eliminar(id){  
    axios.delete('http://localhost:8080/api/productos/'+id)
    .then(data=>{
console.log(data);
})
//location.reload()  
}
}
}
</script>

