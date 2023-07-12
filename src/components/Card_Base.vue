<template>
    <div class="card">
        <slot></slot>
    </div>
</template>

<style scoped>
    .card{
    background-color: white;
    box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
    display: flex;
    flex-direction: column;
    width: 95%;
    margin: 20px auto;
    padding: 10px;
}

@media (min-width:768px){
    .card{
        width: 60%;
    }
}

@media (min-width:1024px){
    .card{width: 40%;}
}
</style>