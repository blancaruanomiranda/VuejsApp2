<template>
    <div class="questionnaire">

        <p>Antes de empezar a jugar, necesito que contestes unas preguntitas. Por favor, clica en el siguiente link y rellena el formulario. </p>
        <a href="https://docs.google.com/forms/d/e/1FAIpQLScjf_W24OII6NEdVNroXMsE6DaUUE2F_b-MrcJ4PIZvge1nLQ/viewform?usp=sf_link" target="_blank">Link al test</a>

    </div>
</template>

<script>
    export default {
        name: 'questionnaire',
        props: {
            counter: Number,
            chapter_counter: Number
        }
    };
</script>

<style scoped>
    * {
        padding: 0;
        margin: 0;
        background-color: black;
        background-size: 100% 100%;
    }

    h1 {
        color: white;
        text-align: center;
        font-size: 50px;
        padding: 20px;
        margin-top: 200px;
    }

    p {
        font-size: 15px;
        text-align: center;
        margin-top: 30vh;
        padding: 20px;
        color: white;
    }

    a {
        justify-content: center;
        display: flex;
        margin-bottom: 6vh;
    }
</style>