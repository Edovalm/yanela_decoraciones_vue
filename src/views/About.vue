<template>
  <div>
    <RegularHero/>
    <main>
      <article class="wrapper card space-usher">
          <h1 class="card__title">¿Quiénes Somos?</h1>
          <div class="grid-wrapper grid-column-2">
              <div>
                  <h2 class="card__subtitle">Cortinas & Persianas, Yanela Decoraciones</h2>
                  <p class="card__text">Somos una empresa orgullosamente colombiana fundada en Bogotá, donde te brindamos el servicio de distribución, instalación de cortinas y persianas a la medida.</p>
                  <p class="card__text">Nuestros servicios están diseñados para proporcionar la mejor opción  en cuanto al cubrimiento de ventanas, pisos, entre otros servicios decorativos, con la más alta calidad. Estamos siempre a la vanguardia, ya que distribuimos productos de grandes marcas del mercado y por ello contamos con garantías y respaldo.</p>
                  
              </div>         
              <div>
                  <img class="card__image"  src="../assets/Persiana1.jpg" alt="Persiana">
              </div>
              <div>
                  <img  class="card__image" src="../assets/Persiana2.jpg" alt="decoración"> 
              </div>
              <div>
                  <p class="card__text">
                    Gracias a nuestra amplia experiencia y conocimientos en el área de la decoración, podemos orientarle de forma profesional  y brindarle la más completa asesoría, al momento de elegir el producto adecuado a sus necesidades, sin exceder su presupuesto.
                  </p>
                  <p class="card__text" >
                    Nuestros tiempos de entrega son garantizados. Ofrecemos un amplio portafolio de productos para interiores y exteriores.
                  </p>
                  <p class="card__text">
                    Para nosotros "Tu nuevo hogar es un lienso en blanco en donde puedes escribir tu historia"
                  </p>                                                       
              </div>
          </div>
      </article>
    </main>
  </div>
</template>

<script>
import RegularHero from '@/components/RegularHero.vue'


export default {
  name: 'About',
  components: {
    RegularHero
  }
}
</script>
