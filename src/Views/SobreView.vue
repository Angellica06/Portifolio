<template>
    <section id="sobre" class="content">
        <h2>Sobre Mim</h2>
        <div class="text-sobre d-flex justify-content-center my-4 align-items-center">
            <img src="/img/dev-avatar.jpg" class="img efeito-img-sobre">
            <p class="efeito-txt-sobre px-4">
                Concluí recentemente o curso de <span>Análise e
                    Desenvolvimento de Sistemas</span> pela Ucsal, sou desenvolvedora front-end apaixonada por
                criar interfaces intuitivas e focadas na experiência do usuário. Atualmente, estou em uma residência em
                front-end, com foco em UI/UX e Angular 13+. Tenho experiência com <span>Html,
                    Css,
                    Javascript, Vue.js e Bootstrap</span>, onde, durante meu estágio, utilizei essas tecnologias no
                desenvolvimento de soluções práticas e eficientes em projetos reais. Busco oportunidades para aplicar
                meu aprendizado, colaborar em
                equipe e crescer profissionalmente.
            </p>
        </div>
    </section>
</template>

<style>
.text-sobre {
    gap: 4rem;
    flex-wrap: wrap;
    color: var(--cor-11);
}

.text-sobre p {
    max-width: 600px;
    flex-wrap: wrap;
    line-height: 24px;
    text-align: justify;
    font-size: 1.1rem;
    font-family: "Roboto", sans-serif;
    font-weight: 600;
}

.img {
    width: 280px;
    min-width: 210px;
    border-radius: 1rem 2rem;
    padding: .8rem;
}
</style>