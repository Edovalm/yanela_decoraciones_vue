<template>
    <div>
        <form class="item-card__form grid-column-2" action="">
            <label for="idCategoria">Id de Categoria</label>
            <input class="item-card__form-input" type="text" name="idCategoria" id="idCategoria" v-model="categoria.idCategoria">

            <label for="nombreCategoria">Nombre</label>
            <input class="item-card__form-input" type="text" name="nombreCategoria" id="nombre_categoria" v-model="categoria.nombreCategoria">

            <label for="imgCategoria">Imagen</label>
            <input class="item-card__form-input" type="text" name="imgCategoria" id="img_categoria" v-model="categoria.imgCategoria">

            <label for="descripcionCategoria">Descripcion</label>
            <input class="item-card__form-input" type="text" name="descripcionCategoria" id="descripcion_categoria" v-model="categoria.descripcionCategoria">

            <div>
                <button class="link-button"  type="submit" v-on:click="guardar()">Guardar</button>
                <button class="link-button"  type="submit" v-on:click="eliminar(categoria.idCategoria)">Eliminar</button>
            </div>
        </form>
    </div>
</template>

<script>
import axios from 'axios'

export default {
  name:'formularioCategorias',
data:function (){
return{
categoria: {
idCategoria:"",
nombreCategoria:"",
imgCategoria: "",
descripcionCategoria: ""
}
}
},
methods:{
guardar(){

axios.post('http://localhost:8080/api/categorias',this.categoria)
.then(data=>{
console.log(data);
})

},eliminar(id){
    axios.delete('http://localhost:8080/api/categorias/'+id)
    .then(data=>{
console.log(data);
})
//location.reload()  
}
}
}
</script>

