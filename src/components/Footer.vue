<template>
    <footer class="main-footer">
        <div class="wrapper grid-wrapper grid-column-3">
            <section class="main-footer__card space-usher">
                <h2 class="main-footer__card-title">Síguenos</h2>
                <ul class="main-footer__card-social-wrapper">
                    <li class="main-footer__card-item"><a href="#"><span class="main-footer__card-social icon-facebook"></span></a></li>
                    <li class="main-footer__card-item"><a href="#"><span class="main-footer__card-social icon-instagram"></span></a></li>
                    <li class="main-footer__card-item"><a href="#"><span class="main-footer__card-social icon-pinterest"></span></a></li>
                    <li class="main-footer__card-item"><a href="#"><span class="main-footer__card-social icon-youtube"></span></a></li>
                    <li class="main-footer__card-item"><a href="#"><span class="main-footer__card-social icon-linkedin"></span></a></li>
                </ul>
                <img src="../assets/logo-footer.png" alt="Logo Yanela Decoraciones">
            </section>
            <section class="main-footer__card space-usher">
                <h2 class="main-footer__card-title">Información</h2>
                <p class="main-footer__card-item"><span class="main-footer__icon icon-mobile"></span> 316 999 9999</p>  
                <p class="main-footer__card-item"><span class="main-footer__icon icon-email"></span> hola@yaneladecoraciones.com</p>  
                <p class="main-footer__card-item"><span class="main-footer__icon icon-clock"></span> Infomación de Horario</p>  
                <p class="main-footer__card-item"><span class="main-footer__icon icon-marker"></span> Carrera ## Nº ## - ## Bogotá - Colombia</p> 
            </section>
            <section class="main-footer__card space-usher">
                <h2  class="main-footer__card-title">Legalidad</h2>
                <ul>
                    <li class="main-footer__card-item"><router-link to="/terminos_uso" class="main-footer__link" exact-active-class="main-footer__link--active">Términos de Uso</router-link></li>  

                    <li class="main-footer__card-item"><router-link to="/politica_privacidad" class="main-footer__link" exact-active-class="main-footer__link--active">Política de Privacidad</router-link></li> 

                    <li class="main-footer__card-item"><router-link to="/mapa_sitio" class="main-footer__link" exact-active-class="main-footer__link--active">Mapa del Sitio</router-link></li> 
                </ul>
            </section>
        </div>
        <div class="wrapper main-footer__copyright">
            <p><span class="icon-copyright main-footer__copyright-icon"></span>Copyright - 2021</p>
        </div>
    </footer> 
</template>