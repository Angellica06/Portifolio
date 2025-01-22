<template>
    <section id="home" class="content d-flex justify-content-center align-items-center">
        <div class="col-12 col-md-6">
            <div class="home-content px-3">
                <h4>Olá!</h4>
                <h1>Eu sou <span>Angélica Anjos</span></h1>
                <h3><span>Desenvolvedora Front-End</span></h3>
                <p class="text-ligh mb-1">Amo a arte de unir criatividade e lógica para transformar ideias em interfaces
                    funcionais.</p>
            </div>
            <div class="redes-sociais">
                <a href="https://www.linkedin.com/in/angélica-anjos6" target="_blank" rel="noopener noopener">
                    <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" fill="#fff" class="bi bi-linkedin"
                        viewBox="0 0 16 16">
                        <path
                            d="M0 1.146C0 .513.526 0 1.175 0h13.65C15.474 0 16 .513 16 1.146v13.708c0 .633-.526 1.146-1.175 1.146H1.175C.526 16 0 15.487 0 14.854V1.146zm4.943 12.248V6.169H2.542v7.225h2.401zm-1.2-8.212c.837 0 1.358-.554 1.358-1.248-.015-.709-.52-1.248-1.342-1.248-.822 0-1.359.54-1.359 1.248 0 .694.521 1.248 1.327 1.248h.016zm4.908 8.212V9.359c0-.216.016-.432.08-.586.173-.431.568-.878 1.232-.878.869 0 1.216.662 1.216 1.634v3.865h2.401V9.25c0-2.22-1.184-3.252-2.764-3.252-1.274 0-1.845.7-2.165 1.193v.025h-.016a5.54 5.54 0 0 1 .016-.025V6.169h-2.4c.03.678 0 7.225 0 7.225h2.4z" />
                    </svg>
                </a>
                <a href="https://github.com/Angellica06/" target="_blank" rel="noopener noopener">
                    <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" fill="#fff" class="bi bi-github"
                        viewBox="0 0 16 16">
                        <path
                            d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z" />
                    </svg>
                </a>
            </div>
        </div>
        <div class="imagem img-fluid col-12 col-md-6 text-center">
            <img src="/img/Dev-Front.png" class="img-fluid">
        </div>
    </section>
</template>

<style scoped>
.home-content {
    margin-left: 7rem;
}

.home-content h3,
.home-content h4 {
    color: var(--cor-11);
    font-family: "Roboto", sans-serif;
    font-size: 1.7rem;
    font-weight: 800;
}

.home-content h1 {
    color: var(--cor-11);
    font-size: 2.2rem;
    font-family: "Roboto", sans-serif;
    font-weight: 800;
}

#home .redes-sociais {
    margin-left: 7.8rem;
}

#home .redes-sociais svg {
    width: 2.2rem;
    margin: 1rem .3rem;
}

.redes-sociais svg:hover {
    transform: scale(1.1);
    filter: drop-shadow(10px 10px 7px rgba(0, 0, 0, 0.5));
}

.home-content p {
    font-size: 1.2rem;
    font-weight: 700;
    color: var(--cor-9);
    margin-top: .8rem;
}

@keyframes float {

    0%,
    100% {
        transform: translateY(0);
    }

    50% {
        transform: translateY(-10px);
    }
}

.imagem img {
    height: 76vh;
    animation: float 5s ease-in-out infinite;
}

@media (max-width: 980px) {
    #home {
        flex-direction: column;
        padding-top: 7rem;
    }

    .home-content, #home .redes-sociais {
        text-align: center;
        margin: 0;
    }

    .imagem img {
        height: 22rem;
    }
}

@media (max-width: 576px) {

    .home-content h3,
    .home-content h4 {
        font-size: 1.4rem;
    }

    .home-content h1 {
        font-size: 1.8rem;
    }

    .home-content p {
        font-size: 1rem;
    }
}
</style>
