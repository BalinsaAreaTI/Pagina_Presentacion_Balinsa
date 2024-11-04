<script setup>
import { onMounted } from 'vue'
import { initFlowbite } from 'flowbite'
import Glide from '@glidejs/glide'
import BalanzasGrameras from './BalanzasGrameras.vue'
import DeterminadorasHumeda from './DeterminadorasHumeda.vue'
import BalanzasPrecision from './BalanzasPrecision.vue'
import BalanzasPlataforma from './BalanzasPlataforma.vue'
import BalanzasRecepcion from './BalanzasRecepcion.vue'
import Indicadores from './Indicadores.vue'

// initialize components based on data attribute selectors
onMounted(() => {
    initFlowbite();
})
</script>

<script>
document.addEventListener("DOMContentLoaded", function() {
    let productos2 = false;
    let productos3 = false;
    let productos4 = false;
    let productos5 = false;
    let productos6 = false;

    let glide = new Glide('.glide', {
        type: 'carousel',
        perView: 2,
        autoplay: 3000,
        breakpoints: {
            1000: {
                perView: 1
            }
        }
    })

    glide.mount();

    document.getElementById('determinadorasHumeda-tab').addEventListener('click', function() {
        if (productos2 === false){
            var glide2 = new Glide('.glide2', {
                type: 'carousel',
                perView: 2,
                autoplay: 3000,
                breakpoints: {
                    1000: {
                        perView: 1
                    }
                }
            })
            glide2.mount();
            productos2 = true
        }
    });

    document.getElementById('balanzasPrecision-tab').addEventListener('click', function() {
        if (productos3 === false){
            var glide3 = new Glide('.glide3', {
                type: 'carousel',
                perView: 2,
                autoplay: 3000,
                breakpoints: {
                    1000: {
                        perView: 1
                    }
                }
            })
            glide3.mount();
            productos3 = true
        }
    });

    document.getElementById('balanzasPlataforma-tab').addEventListener('click', function() {
        if (productos4 === false){
            var glide4 = new Glide('.glide4', {
                type: 'carousel',
                perView: 2,
                autoplay: 3000,
                breakpoints: {
                    1000: {
                        perView: 1
                    }
                }
            })
            glide4.mount();
            productos4 = true
        }
    });

    document.getElementById('balanzasRecepcion-tab').addEventListener('click', function() {
        if (productos5 === false){
            var glide5 = new Glide('.glide5', {
                type: 'carousel',
                perView: 2,
                autoplay: 3000,
                breakpoints: {
                    1000: {
                        perView: 1
                    }
                }
            })
            glide5.mount();
            productos5 = true
        }
    });

    document.getElementById('indicadores-tab').addEventListener('click', function() {
        if (productos6 === false){
            var glide6 = new Glide('.glide6', {
                type: 'carousel',
                perView: 2,
                autoplay: 3000,
                breakpoints: {
                    1000: {
                        perView: 1
                    }
                }
            })
            glide6.mount();
            productos6 = true
        }
    });

});
</script>

<template>
    <section class="bg-gray-100 dark:bg-gray-900 max-w-4xl m-auto mb-20" id="productos">
        <div class="w-full mb-10">
            <h1 class="text-center text-4xl md:text-5xl font-bold text-[#251F17] dark:text-white">Productos Destacados</h1>
            <div class="h-4 w-full">
                <div class="bg-[url('/img/onda.svg')] bg-[length:22px_15px] w-40 md:w-96 h-4 m-auto"></div>
            </div>
        </div>
        <div class="w-full mt-10 px-4">
            <ul class="text-sm font-medium text-center text-gray-500 grid grid-cols-2 md:grid-cols-3 gap-2 dark:text-gray-400 rtl:divide-x-reverse" id="fullWidthTab" data-tabs-toggle="#fullWidthTabContent" role="tablist">
                <li class="w-full">
                    <button id="balanzasGrameras-tab" data-tabs-target="#balanzasGrameras" type="button" role="tab" aria-controls="balanzasGrameras" aria-selected="true" class="inline-block w-full p-4 bg-gray-50 hover:bg-gray-100 focus:outline-none dark:bg-gray-700 dark:hover:bg-gray-600 rounded-lg h-full">Balanzas Grameras</button>
                </li>
                <li class="w-full">
                    <button id="determinadorasHumeda-tab" data-tabs-target="#determinadorasHumeda" type="button" role="tab" aria-controls="determinadorasHumeda" aria-selected="false" class="inline-block w-full p-4 bg-gray-50 hover:bg-gray-100 focus:outline-none dark:bg-gray-700 dark:hover:bg-gray-600 rounded-lg h-full">Determinadoras de Humedad</button>
                </li>
                <li class="w-full">
                    <button id="balanzasPrecision-tab" data-tabs-target="#balanzasPrecision" type="button" role="tab" aria-controls="balanzasPrecision" aria-selected="false" class="inline-block w-full p-4 bg-gray-50 hover:bg-gray-100 focus:outline-none dark:bg-gray-700 dark:hover:bg-gray-600 rounded-lg h-full">Balanzas de Precisión</button>
                </li>
                <li class="w-full">
                    <button id="balanzasPlataforma-tab" data-tabs-target="#balanzasPlataforma" type="button" role="tab" aria-controls="balanzasPlataforma" aria-selected="false" class="inline-block w-full p-4 bg-gray-50 hover:bg-gray-100 focus:outline-none dark:bg-gray-700 dark:hover:bg-gray-600 rounded-lg h-full">Balanzas de Plataforma</button>
                </li>
                <li class="w-full">
                    <button id="balanzasRecepcion-tab" data-tabs-target="#balanzasRecepcion" type="button" role="tab" aria-controls="balanzasRecepcion" aria-selected="false" class="inline-block w-full p-4 bg-gray-50 hover:bg-gray-100 focus:outline-none dark:bg-gray-700 dark:hover:bg-gray-600 rounded-lg h-full">Balanzas de Recepción</button>
                </li>
                <li class="w-full">
                    <button id="indicadores-tab" data-tabs-target="#indicadores" type="button" role="tab" aria-controls="indicadores" aria-selected="false" class="inline-block w-full p-4 rounded-se-lg bg-gray-50 hover:bg-gray-100 focus:outline-none dark:bg-gray-700 dark:hover:bg-gray-600 rounded-lg h-full">Indicadores</button>
                </li>
            </ul>
            <div id="fullWidthTabContent" class="py-6">
                <div class="hidden rounded-lg" id="balanzasGrameras" role="tabpanel" aria-labelledby="balanzasGrameras-tab">
                    <BalanzasGrameras/>
                </div>
                <div class="hidden rounded-lg" id="determinadorasHumeda" role="tabpanel" aria-labelledby="determinadorasHumeda-tab">
                    <DeterminadorasHumeda/>
                </div>
                <div class="hidden rounded-lg" id="balanzasPrecision" role="tabpanel" aria-labelledby="balanzasPrecision-tab">
                    <BalanzasPrecision/>
                </div>
                <div class="hidden rounded-lg" id="balanzasPlataforma" role="tabpanel" aria-labelledby="balanzasPlataforma-tab">
                    <BalanzasPlataforma/>
                </div>
                <div class="hidden rounded-lg" id="balanzasRecepcion" role="tabpanel" aria-labelledby="balanzasRecepcion-tab">
                    <BalanzasRecepcion/>
                </div>
                <div class="hidden rounded-lg" id="indicadores" role="tabpanel" aria-labelledby="indicadores-tab">
                    <Indicadores/>
                </div>
            </div>
        </div>
        <div class="max-w-4xl w-full px-4">
            <div class="max-w-4xl w-full flex justify-center items-center bg-[#FEAA1A] p-4 rounded-lg gap-2">
                <h1 class="text-white text-lg font-semibold">Visualiza nuestro catalogo completo</h1>
                <a href="https://balinsa.com/CATALOGO_PRODUCTOS.pdf" id="btnFinal">
                    <svg viewBox="0 0 24 24" width="20" height="20" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round" class="css-i6dzq1"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"></polygon></svg> Aqui
                </a>
            </div>
        </div>
    </section>
</template>

<style scoped>

#btnFinal {
 display: flex;
 align-items: center;
 justify-content: center;
 gap: 5px;
 font-family: inherit;
 font-size: 12px;
 font-weight: 500;
 text-transform: uppercase;
 letter-spacing: 0.4px;
 color: #7e97b8;
 background-color: #e0e8ef;
 border-style: solid;
 border-width: 2px 2px 2px 2px;
 border-color: rgba(255, 255, 255, 0.333);
 border-radius: 40px 40px 40px 40px;
 padding: 10px 20px;
 transform: translate(0px, 0px) rotate(0deg);
 transition: 0.2s;
}

#btnFinal:hover {
 color: #516d91;
 background-color: #E5EDF5;
}

#btnFinal:active {
 box-shadow: none;
}

</style>