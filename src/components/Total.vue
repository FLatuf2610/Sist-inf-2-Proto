<template>
   <div class="total-container">
        <div class="container">
            <div class='mobile-container'>
            <div v-if="descuento" class="pagar">
                <del class='tachado'>Pagás ${{ producto.precio }}</del>
                <span class='desc'>5%OFF</span>
                Pagás $ {{ producto.precioDescuento }}
            </div>
            <div v-else class="pagar">
                Pagás ${{ producto.precio }}
            </div>
            <div>
                <button class='btn-comprar'>Comprar</button>
            </div>
        </div>
    </div>
    
   </div> 
</template>

<script>
    export default{
        props:['producto','descuento','precioDescuento'],
        data() {
            return {
            
            }
        },

        methods: {
            
        },
    };
</script>

<style scoped>
    
    .total-container{
    position: absolute;
    bottom: 0;
    width: 100%;
    background-color: white;
    box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
    padding: 10px;
    }

    .mobile-container{
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    @media (min-width:1024px){
        .mobile-container{
            justify-content: center;
            gap: 30px;
        }
    }

    .btn-comprar{
    cursor: pointer;
        color: white;
    background-color: rgb(35, 101, 200);
    outline: none;
    border: none;
    padding: 5px 10px;
    font-weight: 200;
    border-radius: 5px;
    }

    .pagar{
        display: flex;
        flex-direction: column;
    }

    .desc{
    color: green;
    font-size: 0.7em;
}

.tachado{
    font-size: 0.6em;
}

</style>