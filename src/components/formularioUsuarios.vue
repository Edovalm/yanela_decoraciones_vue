<template>
    <div>
        <form class="item-card__form grid-column-2" action="">
            <label for="idUsuario">Id del Usuario</label>
            <input class="item-card__form-input"  type="text" name="idUsuario" id="idUsuario" v-model="usuario.idUsuario">

            <label for="nombreUsuario">Nombre</label>
            <input class="item-card__form-input"  type="text" name="nombreUsuario" id="nombre_usuario" v-model="usuario.nombreUsuario">

            <label for="imgUsuario">Imagen</label>
            <input class="item-card__form-input"  type="text" name="imgUsuario" id="img_usuario" v-model="usuario.imgUsuario">

            <label for="contraseñaUsuario">Contraseña</label>
            <input class="item-card__form-input"  type="text" name="contraseñaUsuario" id="contraseña_usuario" v-model="usuario.contraseñaUsuario">

            <label for="emailUsuario">Email</label>
            <input class="item-card__form-input"  type="text" name="emailUsuario" id="email_usuario" v-model="usuario.emailUsuario">
            
            <div>
                <button class="link-button" type="submit" v-on:click="guardar()">Guardar</button>
                <button class="link-button" type="submit" v-on:click="eliminar(usuario.idUsuario)">Eliminar</button>
            </div>
        </form>
    </div>
</template>

<script>
import axios from 'axios'

export default {
  name:'formularioUsuarios',
data:function (){
return{
usuario: {
idUsuario:"",
nombreUsuario:"",
imgUsuario: "",
contraseñaUsuario: "",
emailUsuario: ""
}
}
},
methods:{
guardar(){

axios.post('http://localhost:8080/api/usuarios',this.usuario)
.then(data=>{

console.log(data);

})

},eliminar(id){

    
    axios.delete('http://localhost:8080/api/usuarios/'+id)
    .then(data=>{

console.log(data);

})
//location.reload()  
}
}
}

</script>



<style scoped>

.formUsuarios{

text-align: center;
padding: 5%;
font-family : inherit;

}



</style>