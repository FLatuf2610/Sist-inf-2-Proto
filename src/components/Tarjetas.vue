<template>
          <div class="tarjeta" id="tarjeta-1">
            <div class="icon-tarjeta"><i class="fa-solid fa-credit-card"></i></div>
            <div class="desc-tarjeta">Agrega una nueva tarjeta de crédito</div>
            <div class="next"><i class="fa-solid fa-angle-right"></i></div>
        </div>
        <div class="tarjeta">
            <div class="icon-tarjeta"><i class="fa-solid fa-credit-card"></i></div>
            <div class="desc-tarjeta">Agrega una nueva tarjeta de débito</div>
            <div class="next"><i class="fa-solid fa-angle-right"></i></div>
        </div>
</template>

<style scoped>
    .tarjeta{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding:10px;
    gap: 15px;
    }


    #tarjeta-1{
    border-bottom: 2px solid rgb(152, 152, 152);
}


.tarjeta .icon-tarjeta i{
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
.tarjeta .next i{
    font-size: 1.5em;
    color: rgb(35, 101, 200);
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
}


</style>