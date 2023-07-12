<template>
        <header>
        <div class="header">
            <div class="back"><i class="fa-solid fa-arrow-left"></i></div>
            <div class="title">¿Cómo querés pagar?</div>
            <div class="hidden"><i class="fa-solid fa-arrow-left"></i></div>
        </div>
    </header>
</template>

<style scoped>
    header{
    width: 100%;
    background-color: yellow;
    height: 50px;
}

.header{
    display: flex;
    width: 100%;
    justify-content: space-between;
    align-items: center;
    background-color: yellow;
    height: 50px;
}

.header i{
    margin-left: 10px;
    font-size: 1em;
}

.hidden{
    opacity: 0;
}
</style>