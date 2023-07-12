<template>
    <div class="pagar-mp">
        <div class="icon-mp"><i class="fa-solid fa-dollar-sign"></i></div>
        <div class="desc-container">
            <div class="desc-mp">Pagá con tu dinero disponible</div>
            <div class="desc-mp">Dinero disponible: $0</div>
        </div>
        <toggleButton/>
    </div>
</template>

<script>
    import toggleButton from './toggleButton.vue';
    export default{
        components:{toggleButton}
    };
</script>

<style scoped>
    .pagar-mp{
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    .pagar-mp .desc-container :first-child{
    font-size: 0.8em;
}

.pagar-mp .desc-container :nth-child(2){
    font-size: 0.7em;
}

@media (max-width:320px){
    .pagar-mp .desc-container :first-child{
    font-size: 0.7em;
}

.pagar-mp .desc-container :nth-child(2){
    font-size: 0.6em;
}
}

.pagar-mp .icon{
    display: flex;
    align-items: center;
    justify-content: center;
    width: 2em;
}

.pagar-mp i{
    font-size: 1.5em;
    color: rgb(35, 101, 200);
    background-color: rgb(237, 237, 237);
    border-radius: 50%;
    width: 45px;
    height: 45px;
    display: flex;
    align-items: center;
    justify-content: center;
}


</style>