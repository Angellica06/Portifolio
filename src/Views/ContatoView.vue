<script setup>
import axios from 'axios';
import Swal from 'sweetalert2';

const handleSubmit = async (event) => {
    event.preventDefault();

    const form = event.target;
    const formData = new FormData(form);

    try {
        const response = await axios.post('https://api.staticforms.xyz/submit', formData, {
            headers: { 'Content-Type': 'application/json' },
        });

        if (response.status === 200) {
            Swal.fire({
                title: 'Sucesso!',
                text: 'Seu formulário foi enviado com sucesso. Obrigada pelo contato!',
                icon: 'success',
                confirmButtonText: 'OK',
            });
            form.reset();
        } else {
            Swal.fire({
                title: 'Erro!',
                text: 'Ocorreu um erro ao enviar o formulário.',
                icon: 'error',
                confirmButtonText: 'OK',
            });
        }
    } catch (error) {
        Swal.fire({
            title: 'Erro!',
            text: 'Erro ao enviar o formulário. Verifique sua conexão e tente novamente.',
            icon: 'error',
            confirmButtonText: 'OK',
        });
        console.error(error);
    }
};

</script>

<template>
    <section class="content d-flex justify-content-center align-items-center pb-5" id="contato">
        <div class="contato">
            <h2 class="mb-0">Contato</h2>
            <p class="text-center mb-5 fw-bold">Tem alguma dúvida, sugestão ou ideia? Entre em contato!</p>
            <form class="d-flex flex-column w-100" id="meuFormulario" @submit="handleSubmit">
                <label class="text-start">Nome</label>
                <input type="text" name="name" placeholder="Digite seu nome" autocomplete="off" required />
                <label class="text-start">E-mail</label>
                <input type="email" name="email" placeholder="Digite seu e-mail" autocomplete="off" required />
                <label class="text-start">Mensagem</label>
                <textarea name="message" cols="30" rows="10" placeholder="Digite sua mensagem" required></textarea>
                <button type="submit" id="enviarBtn">Enviar</button>

                <input type="hidden" name="accessKey" value="e4b81bb3-a590-482e-a3fd-197b34bed221" />
            </form>
        </div>
    </section>
</template>

<style scoped>
.contato {
    display: flex;
    align-items: center;
    flex-direction: column;
    width: 86%;
    max-width: 500px;
}

.contato p {
    font-size: 1.1rem;
    color: var(--cor-10);
}

form label {
    color: var(--cor-10);
    font-size: 1rem;
    margin-bottom: .4rem;
    font-weight: 600;
}

form input {
    padding: .8rem;
    outline: none;
    border: 0;
    margin-bottom: 1.4rem;
    font-size: 1rem;
    transition: all 0.5s;
    border: 2px solid var(--cor-10);
    color: var(--cor-9);
}

form input:focus {
    border-radius: 1rem;
}

form textarea {
    padding: .8rem;
    outline: none;
    border: 0;
    font-size: 1rem;
    margin-bottom: 30px;
    transition: all 0.5s;
    border: 2px solid var(--cor-10);
    color: var(--cor-9);
}

form textarea:focus {
    border-radius: 1rem;
}

form button {
    padding: 1rem;
    cursor: pointer;
    color: var(--cor-9);
    font-size: 1rem;
    background: transparent;
    border: 2px solid var(--cor-9);
    margin-bottom: 2rem;
    transition: all 1s;
    font-weight: 600;
}

form button:hover {
    background: var(--cor-9);
    color: var(--cor-11);
    border-radius: 2rem;
}
</style>