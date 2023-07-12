
<template>
  <div class="app-container">
    <Navbar/>
    
    <div class="tittle">
        <div class="icon"><h3>Pagá con Mercado pago</h3></div>
    </div>
    
    <CardBase>
      <PagarMP/>
    </CardBase>

    <div class="tittle">
        <h3>Pagá con tarjeta</h3>
    </div>

    <CardBase>
      <Tarjetas/>
    </CardBase>

    <div class="tittle">
        <h3>Aplicá descuentos</h3>
    </div>

    <CardBase>
      <Link_referido @open-modal="onOpenModal"/>
    </CardBase>

    <Total :producto="producto" :descuento="descuento"/>

    <Modal v-if="openModal" @close-modal="onCloseModal" @apply-desc="onApplyDesc" :links="links"/>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import PagarMP from './components/Pagar-MP.vue';
import CardBase from './components/Card_Base.vue';
import Tarjetas from './components/Tarjetas.vue';
import Link_referido from './components/Link_referido.vue';
import Total from './components/Total.vue';
import Modal from './components/Modal.vue';
  export default {
    components:{Navbar,PagarMP,CardBase,Tarjetas,Link_referido,Total,Modal},
    data() {
      return {
        openModal:false,
        producto:{
          precio:5000,
          precioDescuento:0,
        },
        descuento:false,
        links:['01234','56789']
      }
    },

    methods: {
      onOpenModal(){
        this.openModal = true;
      },
      onCloseModal(){
        this.openModal = false;
      },
      onApplyDesc(){
        this.producto.precioDescuento = this.producto.precio*0.95 ;
        this.descuento = true
      }

    },

    computed: {
      

    },
  };
</script>

<style>
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Geologica';
 }

 body{
    background-color: rgb(242, 242, 242);
    height: 100vh;
  }

  .app-container{
    height: 100%;
  }

  .tittle{
    width: 90%;
    margin: auto;
    margin-top: 20px;
}

@media (min-width:768px){
  .tittle{
    max-width: fit-content;
  }
}

.icon{
    display: flex;
    align-items: center;
    
}


.next i{
    background: white;
    padding: none;
    font-size: 1em;
  
}



</style>