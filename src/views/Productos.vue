<template>
    <div>
      <RegularHero2/>
      <main>
        <div class="wrapper card space-usher">
            <h1 class="card__title">Registro de Productos</h1>
            <p class="card__text">Bienvenido a la página de registros de productos.</p>
            <h2 class="card__subtitle">Instrucciones:</h2>
            <p class="card__text">Tenga en cuenta que tanto para realizar como para modificar un registro, debe llenar todos los campos; para eliminar un registro, solo debe llenar el campo del Id.</p>
            <section class="item-card">
              <formularioProductos/> 
              <tablaProductos/>
            </section>
        </div>
    </main>
    </div>
</template>

<script>
import RegularHero2 from '@/components/RegularHero2.vue'
import formularioProductos from '@/components/formularioProductos.vue'
import tablaProductos from '@/components/tablaProductos.vue'

export default {
  name: 'Productos',
  components: {
    RegularHero2,formularioProductos,tablaProductos
  }
}
</script>
