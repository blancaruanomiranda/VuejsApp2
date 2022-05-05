<template>
    <div class="evaluation">

        <p>Entra en este link para contestar el test</p>
        <a href="https://docs.google.com/forms/d/e/1FAIpQLSeZHZV_2BNeOzCIPn6C6TEgY_sSGiQjv3mHRwn3qB7iZjS4EA/viewform?usp=sf_link">Link al test</a>

    </div>
</template>

<script>
    export default {
        name: 'evaluation',
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