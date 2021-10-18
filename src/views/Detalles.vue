<template>
  <div>
    <RegularHero/>
    <main>
        <div class="wrapper card space-usher">
            <h1 class="card__title">Detalles de los Productos</h1> 
            <section class="grid-wrapper" >
              <article class="item-card" v-for="producto in productos" :key="producto.idProductos">
                
                    <h2 class="item-card__title">{{producto.nombreProducto}}</h2>
                    <img class="item-card__image" src="../assets/img-categoria-persianas.jpg" alt="Productos Persianas">

                    <p> <span class="card__subtitle" > Imagen: </span> {{producto.imgProducto}} </p>
                    <p> <span class="card__subtitle" > Categoria: </span> {{producto.categoriaProducto.idCategoria}}</p>
                    <p> <span class="card__subtitle" > Descripción </span> {{producto.descripcionProducto}}</p>
                    <p> <span class="card__subtitle" > Proveedor </span> {{producto.proveedorProducto.idProveedor}}</p>
                    <p> <span class="card__subtitle" > Id: </span> {{producto.idProducto}}</p>
                    <p> <span class="card__subtitle" > Precio: $ </span> {{producto.precioProducto}}</p>
                
              </article>
            </section>
        </div>
      </main>
  </div>
</template>

<script>
import RegularHero from '@/components/RegularHero.vue'

import axios from 'axios'
export default {
  name: 'Articulos',
  components: {
    RegularHero
  },
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
