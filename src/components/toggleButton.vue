<template>
    <div class="icon-toggle">
        <input id="check-toggle" type="checkbox">
        <label class="toggle-bg" for="check-toggle"></label>
    </div>
</template>

<style scoped>
    #check-toggle{
    display: none;
}

.toggle-bg{
    display: block;
    width: 40px;
    height: 23px;
    background-color: rgb(221, 221, 221);
    border-radius: 20px;
    position: relative;
    cursor: pointer;
    transition: 0.1s;
}

.toggle-bg::after{
    position: absolute;
    content: '';
    width: 17px;
    height: 17px;
    border-radius: 50%;
    background-color: rgb(255, 255, 255);
    top: 3px;
    left: 3px;
    transition: 0.1s;
}

#check-toggle:checked~.toggle-bg{
    background-color: rgb(35, 101, 200);
}

#check-toggle:checked~.toggle-bg::after{
    left: 19px;
}
</style>