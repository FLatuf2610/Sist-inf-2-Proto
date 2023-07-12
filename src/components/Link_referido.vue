<template>
        <div class="link-referido">
            <div class="icon-referido"><i class="fa-solid fa-user-tag"></i></div>
            <div class="desc-referido">Usá el link de tu influencer favorito, ganá un descuento y dale una mano!</div>
            <div class="next" @click="$emit('open-modal')"><i class="fa-solid fa-angle-right"></i></div>
    </div>
</template>


<script>
    export default{
        emits:['open-modal']
    };
</script>

<style scoped>
    .link-referido{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    gap: 7px;
    }

    .icon-referido i{
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

.next i{
    font-size: 1.5em;
    color: rgb(35, 101, 200);
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
}

.desc-referido{
    font-size: 0.8em;
}
</style>