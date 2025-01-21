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
        description: 'Projeto simula um dashboard de vendas, desenvolvido com Vue.js, HTML, CSS, Bootstrap e Chart.js. A aplicação exibe gráficos interativos e responsivos, utilizando dados estáticos para apresentar informações de vendas de forma visual e dinâmica.',
        image: '/img/projeto1.png',
        viewLink: 'https://dashboardvenda.netlify.app/',
        repoLink: 'https://github.com/Angellica06/Dashboard',
    },
    {
        id: 2,
        title: 'SaborChef',
        description: 'Projeto de landing page de restaurante, desenvolvida com Angular, Html, Css e Boostrap. O objetivo principal da página é oferecer uma interface atraente e funcional, com informações sobre o restaurante, o menu e uma área de contato.',
        image: '/img/projeto2.png',
        viewLink: 'https://saborchef.netlify.app/',
        repoLink: 'https://github.com/Angellica06/SaborChef',
    },
    {
        id: 3,
        title: 'Lista de Compras',
        description: 'Projeto de lista de compras, desenvolvido com Angular, Html, Css e Bootstrap, com as funcionalidades de logar a partir de uma conta do Google, adicionar item a lista, podendo marcar como comprado ou não comprado, além de poder editar e remover o item.',
        image: '/img/projeto3.png',
        viewLink: 'https://lista-de-compras1.netlify.app',
        repoLink: 'https://github.com/Angellica06/Lista-de-compras',
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