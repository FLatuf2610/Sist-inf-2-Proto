<template>
    <div class="modal">
        <div class="inner-modal">
            <h2>Ingresá acá el link de referido</h2>
            <ul>
                <h4>Recordá que:</h4>
                <li>
                    <i class="fa-solid fa-check"></i>
                    <p>Solo puede aplicarse un link por producto</p>
                </li>
                <li>
                    <i class="fa-solid fa-check"></i>
                    <p>Los descuentos pueden variar según el influencer</p>
                </li>
                
            </ul>
            <input v-model="enteredLink" type="text" placeholder="Link de referido">
            <div v-if="error" class="error">Ingresa un link válido</div>
            <div class="btns-modal">
                <button @click="applyDesc" class="btn-modal" id="descuento">Aplicar</button>
                <button @click="$emit('close-modal')" class="btn-modal">Cerrar</button>
            </div>
        </div>
    </div>
</template>

<script>
    export default{
        emits:['close-modal','apply-desc'],
        props:['links'],
        data() {
            return {
                enteredLink:'',
                error:false
            }
        },
        methods: {
            applyDesc(){
                if (this.enteredLink == '' || this.links.indexOf(this.enteredLink) == -1){
                    this.error = true;
                }

                else{
                    this.error = false;
                    this.$emit('close-modal')
                    this.$emit('apply-desc')
                }
            }
        },
    };
</script>

<style>
    ul{
        list-style: none;
        display: flex;
        flex-direction: column;
        gap: 5px;
        margin-top: 20px;
        margin-bottom: 20px;
    }

    li{        display: flex;
        gap: 10px;
        align-items: center;
    }

    li i{
        font-size: 1.5em;
        color: rgb(35, 101, 200);
    }
    

    .error{
        font-size: 0.8em;
        margin-bottom:5px;
        color: red;
    }
    
    .modal{
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: 100000;
    background-color: rgba(0, 0, 0, 0.5);
    display: flex;
    align-items: center;
    justify-content: center;
}

.inner-modal{
    background-color: white;
    width: 85%;
    border-radius: 10px;
    padding: 20px;
}

@media (min-width:768px){
    .inner-modal{
        width:50%;
    }
}

@media (min-width:1024px){
    .inner-modal{
        width:30%;
    }
}

.inner-modal input{
    border-radius: 5px;
    outline: none;
    padding: 5px;
    width: 100%;
    border: 1px gray solid;

}

.btns-modal{
    display: flex;
    gap: 10px;
    width: 100%;
    margin-top: 10px;
    justify-content: center;
}

.btn-modal{
    color: white;
    background-color: rgb(35, 101, 200);
    outline: none;
    border: none;
    padding: 5px 10px;
    font-weight: 200;
    border-radius: 5px;
    width: 50%;
    cursor: pointer;
}
</style>