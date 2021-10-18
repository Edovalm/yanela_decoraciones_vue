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
              <article class="item-card" v-for="categoria in categorias" :key="categoria.idCategorias">
                <a class="item-card__link" href="#">
                    <h2 class="item-card__title">{{categoria.nombreCategoria}}</h2>
                    <img class="item-card__image" src="../assets/img-categoria-cortinas.jpg" alt="Productos Cortinas">
                    <div class="item-card__details">
                        <span class="icon-search"></span>
                    </div>
                    <p class="item-card__info">{{categoria.imgCategoria}}{{categoria.descripcionCategoria}}<span class="item-card__button">Ver Mas...</span></p>
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
     categorias:[]
  }
},
mounted(){
  let vue=this;
  axios.get('http://localhost:8080/api/categorias/listar')
  .then( response =>{

    vue.categorias=response.data;
  })
},methods:{

}
}

</script>
