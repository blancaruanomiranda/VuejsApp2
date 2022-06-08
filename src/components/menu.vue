<template>
    <div class="menu">
        <p>MENUUUUU</p>
    </div>
</template>

<script>
    export default {
        name: 'menu',
        props: {
            counter: Number,
            chapter_counter: Number
        },

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
        margin-top: 100px;
        margin-bottom: 30px;
        margin-left: 250px;
        margin-right: 250px;
        padding: 20px;
        color: white;
    }

</style>