<template>
    <div>
        <form  class="item-card__form grid-column-2" action="">
            <label for="idTextura">Id de Textura</label>
            <input class="item-card__form-input" type="text" name="idTextura" id="idTextura" v-model="textura.idTextura">

            <label for="nombreTextura">Nombre</label>
            <input class="item-card__form-input" type="text" name="nombreTextura" id="nombre_textura" v-model="textura.nombreTextura">

            <label for="imgTextura">Imagen</label>
            <input class="item-card__form-input" type="text" name="imgTextura" id="img_textura" v-model="textura.imgTextura">

            <div>
                <button class="link-button" type="submit" v-on:click="guardar()">Guardar</button>
                <button class="link-button" type="submit" v-on:click="eliminar(textura.idTextura)">Eliminar</button>
            </div>
        </form>
    </div>
</template>

<script>
import axios from 'axios'
export default {
  name:'formularioTexturas',
data:function (){
return{
textura: {
idTextura:"",
nombreTextura:"",
imgTextura: ""
}
}
},
methods:{
guardar(){
axios.post('http://localhost:8080/api/texturas',this.textura)
.then(data=>{
console.log(data);
})
},eliminar(id){   
    axios.delete('http://localhost:8080/api/texturas/'+id)
    .then(data=>{
console.log(data);
})
//location.reload()  
}
}
}
</script>


