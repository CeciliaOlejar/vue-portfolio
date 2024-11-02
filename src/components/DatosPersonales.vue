<script setup>

</script>

<template>
    <section class="datos-personales">
        <div class="card">
            <h1>Cecilia Olejar</h1>
            <ul class="container-lista">
                <li><a href=""><img class="icon-redsocial" src="" width="35rem" alt="">lindkin</a></li>
                <li><a href=""><img class="icon-redsocial" src="" width="35rem" alt="">insta</a></li>
                <li><a href=""><img class="icon-redsocial" src="" width="35rem" alt="">git</a></li>
                <li><a href=""><img class="icon-redsocial" src="" width="35rem" alt="">cv</a></li>
            </ul>
        </div>
    </section>
</template>



<style>
h1 {
    font-size: 2.5rem;
}

.card {
    background-color: rgb(28, 41, 52);
    border-radius: 10px;
    padding: 10px;
    margin: 10px;
    text-align: center;
}

.container-lista {
    display: flex;
    justify-content: center;
    list-style: none;
    padding: 0;
    margin: 0;
    text-align: center;
}

.icon-redsocial {
    align-items: center;
    background-color: aliceblue;
    border-radius: 50%;
    padding: 2px;
    margin: 5px;
    box-shadow: 0 0 5px rgba(95, 124, 205, 0.934);
}

.icon-redsocial:hover {
    background-color: rgb(28, 41, 52);
    box-shadow: 0 0 5px rgba(251, 249, 249, 0.934);
}
</style>