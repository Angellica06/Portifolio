<template>
    <div class="container d-flex justify-content-center">
        <div class="card pb-2">
            <div class="card-body">
                <img :src="image" class="card-img">
                <h5 class="text-light text-center m-2">{{ title }}</h5>
                <p class="card-text text-light text-center px-2">{{ description }}</p>
                <div class="btn-group d-flex justify-content-center">
                    <a :href="viewLink" target="_blank" rel="noopener noopener" class="btn-card text-light text-decoration-none">
                        Visualizar
                    </a>
                    <a :href="repoLink" target="_blank" rel="noopener noopener" class="btn-card text-light text-decoration-none">
                        Repositório
                    </a>
                </div>
            </div>
        </div>
    </div>

</template>

<script setup>
const props = defineProps({
    title: String,
    description: String,
    image: String,
    viewLink: String,
    repoLink: String,
})
</script>

<style>
.card {
    max-width: 25rem;
    border-radius: 0.8rem;
    border: 0;
    background-color: var(--cor-7) !important;
    box-shadow: 5px 5px 10px var(--cor-1);
    box-sizing: border-box;
}

.card-body h5 {
    font-weight: 600;
}

.btn-card {
    background: linear-gradient(90deg, #1e488b, #a23fb5);
    border-radius: 1rem;
    padding: .5rem 1rem;
    font-size: .9rem;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s;
    margin: 0 .3rem;
}

.card a:hover {
    box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.2);
}
</style>