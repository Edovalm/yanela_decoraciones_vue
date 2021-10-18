<template>
    <div>
        <h3 class="card__title">Tabla de Usuarios</h3>
        <table class="tablaUsuarios tablaRegistros">
            <tr>
                <th>Id</th>
                <th>Nombre</th>
                <th>Imagen</th>
                <th>Contraseña</th>
                <th>Email</th>
            </tr>
            <tr v-for="usuario in usuarios" :key="usuario.idUsuarios">
                <td>{{usuario.idUsuario}}</td>
                <td>{{usuario.nombreUsuario}}</td>
                <td>{{usuario.imgUsuario}}</td>
                <td>{{usuario.contraseñaUsuario}}</td>
                <td>{{usuario.emailUsuario}}</td>
            </tr>
        </table>
        <router-view/>
    </div>
</template>

<script>
    import axios from 'axios'
    export default{
    name:'tablaUsuarios',
    data(){
    return{
        usuarios:[]
    }
    },
    mounted(){
    let vue=this;
    axios.get('http://localhost:8080/api/usuarios/listar')
    .then( response =>{

        vue.usuarios=response.data;
    })
    },methods:{
    }
    }
</script>

