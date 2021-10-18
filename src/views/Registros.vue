<template>
 <div>
  <RegularHero/>
  <main>
    <div class="wrapper card space-usher">
      <h1 class="card__title">Registros</h1>
      <p class="card__text">Bienvenido a la página de registros en la báse de datos. abajo encontrará los accesos a las paginas donde podrá gestionar cada tipo de registro.</p>
      <section class="item-card ">
        <ul class="botnera-registros">  
            <li><router-link to="/usuarios" class="main-nav__menu-link" exact-active-class="main-nav__menu-link--active">Usuarios</router-link></li>
            <li><router-link to="/proveedores" class="main-nav__menu-link" exact-active-class="main-nav__menu-link--active">Proveedores</router-link></li>
            <li><router-link to="/categorias" class="main-nav__menu-link" exact-active-class="main-nav__menu-link--active">Categorías</router-link></li>
            <li><router-link to="/texturas" class="main-nav__menu-link" exact-active-class="main-nav__menu-link--active">Texturas</router-link></li>
            <li><router-link to="/productos" class="main-nav__menu-link" exact-active-class="main-nav__menu-link--active">Productos</router-link></li>
        </ul>
      </section>
    </div>
  </main>
 </div>
</template>

<script>
// @ is an alias to /src
import RegularHero from '@/components/RegularHero.vue'

export default {
  name: 'Home',
  components: {
    RegularHero
  }
}
</script>