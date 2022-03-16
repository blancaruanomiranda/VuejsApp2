<template>

    <div class="final_menu">
        
        <p>¿Y ahora qué?</p>
    </div>
</template>

<script>
    export default {
        name: 'final_menu',
        props: {
            counter: Number,
            chapter_counter: Number
        },

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

   

    p {
        font-size: 20px;
        margin-bottom: 5vh;
        text-align: center;
        margin-top: 30vh;   
        
        color: #e300ff;
        font-family: 'Press Start 2P', cursive;
    }
</style>