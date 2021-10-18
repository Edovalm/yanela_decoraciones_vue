<template>
    <div>
        <RegularHero/>
        <main>
            <div class="wrapper card space-usher">
                <h1 class="card__title">Mapa del Sitio</h1>
                <div class="grid-wrapper grid-column-3">
                    <ul class="card__sitemap">
                        <li>
                            <a class="card__link-sitemap1" href="/" target="_blank" >
                                <span class="icon-home"></span>Inicio
                            </a>
                        </li>
                        <li>
                            <a class="card__link-sitemap1" href="/Registros" target="_blank" >
                                <span class="icon-folder"></span>Registros
                            </a>
                            <ul>
                                <li>
                                    <a class="card__link-sitemap2" href="/Usuarios" target="_blank" >
                                        <span class="icon-file"></span>Usuarios
                                    </a>
                                </li>
                                <li>
                                    <a class="card__link-sitemap2" href="/Proveedores" target="_blank" >
                                        <span class="icon-file"></span>Proveedores
                                    </a>
                                </li>
                                <li>
                                    <a class="card__link-sitemap2" href="/Categorias" target="_blank" >
                                        <span class="icon-file"></span>Categorias
                                    </a>
                                </li>
                                <li>
                                    <a class="card__link-sitemap2" href="/Texturas" target="_blank" >
                                        <span class="icon-file"></span>Texturas
                                    </a>
                                </li>
                                <li>
                                    <a class="card__link-sitemap2" href="/Productos" target="_blank" >
                                        <span class="icon-file"></span>Productos
                                    </a>
                                </li>
                            
                            </ul>
                        </li>
                        <li>
                            <a class="card__link-sitemap1" href="/About" target="_blank" >
                                <span class="icon-file"></span>¿Quienes Somos?
                            </a>
                        </li>
                        <li>
                            <a class="card__link-sitemap1" href="/Terminos_uso" target="_blank" >
                                <span class="icon-file"></span>Terminos de uso
                            </a>
                        </li>
                        <li>
                            <a class="card__link-sitemap1" href="/Mapa_sitio" target="_blank" >
                                <span class="icon-file"></span>Mapa del Sitio
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </main>
    </div>
</template>

<script>
// @ is an alias to /src
import RegularHero from '@/components/RegularHero.vue'

export default {
  name: 'Mapa_sitio',
  components: {
    RegularHero
  }
}
</script>