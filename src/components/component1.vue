<template>
    <div class="c1">
        <h1>CAPÍTULO {{chapter_counter}}</h1>
    </div>
</template>

<script>
    export default {
        name: 'component1',
        props: {
            counter: Number,
            chapter_counter: Number
        }
    };
</script>

<style scoped>

    @import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');

    * {
        padding: 0;
        margin: 0;
        background-color: black;
        background-size: 100% 100%;   
    }

    h1 {
        color: #e300ff;
        text-align: center;
        font-size: 50px;
        padding: 20px;
        margin-top: 35vh;
        font-family: 'Press Start 2P', cursive;
    }

</style>