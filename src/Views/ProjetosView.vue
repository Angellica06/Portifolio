<template>
    <section id="projetos" class="content px-3">
        <h2>Projetos</h2>
        <div class="row mx-0 justify-content-center">
            <Card class="col-12 col-md-6 col-lg-4 mb-3" v-for="project in projects" :key="project.id"
                :title="project.title" :description="project.description" :image="project.image"
                :viewLink="project.viewLink" :repoLink="project.repoLink" />
        </div>
        <div class="link-repo d-flex flex-column flex-wrap align-items-center">
            <a class="text-decoration-none" href="https://github.com/Angellica06?tab=repositories" target="_blank"
                rel="noopener noopener">Repositórios no GitHub</a>
        </div>
    </section>
</template>

<script setup>
import Card from '@/components/Card.vue';

const projects = [
    {
        id: 1,
        title: 'Dashboard',
        description: 'Projeto que simula um dashboard de vendas, desenvolvido com Vue.js, HTML, CSS, Bootstrap e Chart.js. A aplicação exibe gráficos interativos e responsivos, utilizando dados estáticos para apresentar informações de vendas de forma visual e dinâmica.',
        image: '/img/projeto1.png',
        viewLink: 'https://dashboardvenda.netlify.app/',
        repoLink: 'https://github.com/Angellica06/Dashboard',
    },
    {
        id: 2,
        title: 'SaborChef',
        description: 'Projeto de landing page de restaurante, desenvolvida com Angular, HTML, CSS e Bootstrap. O objetivo principal da página é oferecer uma interface atraente e funcional, com informações sobre o restaurante, o menu e uma área de contato.',
        image: '/img/projeto2.png',
        viewLink: 'https://saborchef.netlify.app/',
        repoLink: 'https://github.com/Angellica06/SaborChef',
    },
    {
        id: 3,
        title: 'Calculadora IMC',
        description: 'Uma calculadora de IMC (Índice de Massa Corporal) criada com HTML, CSS e JavaScript. A aplicação permite inserir o peso e altura do usuário e exibe sua classificação, ajudando a acompanhar a saúde de forma prática. O design é simples e funcional.',
        image: '/img/projeto3.png',
        viewLink: 'https://calculadora-imc13.netlify.app/',
        repoLink: 'https://github.com/Angellica06/Calculadora_IMC?tab=readme-ov-file',
    }
];
</script>

<style scoped>
.link-repo {
    margin: 0 auto;
    padding-top: 2.2rem;
    font-size: 1.1rem;
    font-weight: 600;
}

.link-repo a {
    color: var(--cor-9);
}

.link-repo a:hover {
    color: var(--cor-3);
}
</style>