<template>
    <section id="habilidades" class="skills content">
        <h2 class="titulo-skills">Habilidades Técnicas</h2>
        <div class="language d-flex justify-content-center flex-wrap">
            <p><img class="img-skills mx-1" src="/img/html-5.png" alt="html">HTML</p>
            <p><img class="img-skills mx-1" src="/img/css.png" alt="css">CSS</p>
            <p><img class="img-skills mx-1" src="/img/js.png" alt="javascript">JavaScript</p>
            <p><img class="img-skills mx-1" src="/img/vue-js.png" alt="vue">Vue</p>
            <p><img class="img-skills mx-1" src="/img/bootstrap.png" alt="bootstrap">Bootstrap</p>
            <p><img class="img-skills mx-1" src="/img/figma.png" alt="figma">Figma</p>
        </div>
    </section>
</template>

<style scoped>
.skills {
    background-color: var(--cor-6);
}

.language {
    gap: 4rem;
    font-size: 1.2rem;
}

.img-skills {
    width: 1.5rem;
}

.language p {
    font-weight: bold;
    color: var(--cor-11);
    background-color: var(--cor-4);
    padding: .6rem;
    border-radius: 1rem;
}
</style>