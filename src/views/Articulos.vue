<template>
  <div>
    <RegularHero/>
    <main>
        <div class="wrapper card space-usher">
            <h1 class="card__title">Productos Para Ti en Yanela Decoraciones</h1>
            <p class="card__text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Eos repellat atque officia, quis molestias vel dolore deleniti unde expedita sit cupiditate odit illum saepe libero esse, cum ipsa eum rerum?</p>
            <h2 class="card__subtitle">Un Subtítulo</h2>
            <p class="card__text">Este es un ejemplo de guia para saber que clases usar en las páginas que hay textos con subtítulos en lo referente al contenedor de calse .card.</p>
            <section class="grid-wrapper grid-column-2" >
              <article class="item-card" v-for="producto in productos" :key="producto.idProductos">
                <a class="item-card__link" href="#">
                    <h2 class="item-card__title">{{producto.nombreProducto}}</h2>
                    <img class="item-card__image" src="../assets/img-categoria-persianas.jpg" alt="Productos Persianas">
                    <div class="item-card__details">
                        <span class="icon-search"></span>
                    </div>
                    <p class="item-card__info">{{producto.imgProducto}} <span> </span>{{producto.descripcionProducto}}<span> </span><span class="item-card__button"> Ver Mas...</span></p>
                </a>
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
  name: 'Cortinas',
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
