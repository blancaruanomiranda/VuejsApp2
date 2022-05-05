<template>
    
    <div class="instructions">
        <component :is="component" v-bind="{ counter: this.counter, chapter_counter: this.chapter_counter }"></component>
        <div v-if="chapter_counter==7">
            <h1>CAPÍTULO {{chapter_counter}}</h1>
            <p id="last_chapter_text">
                La conversación con el desconocido ha dejado a Jimmy un poco rayado. Le da mal rollo que alguien extraño pueda ver lo que publica, o incluso hablarle… ¿Qué podría hacer para evitar todo eso? ¿Cómo podría controlar quién puede ver su perfil?
                Si Jimmy pudiera hacer todo eso con un solo click estaría super contento. No tendría que preocuparse por el acosador nunca más.
            </p>
        </div>
        <div v-if="chapter_counter==1">
            <p>En este juego vas a participar en una historia. A medida que vayas avanzando, deberás tomar varias decisiones que afectarán al protagonista de la historia. En cada capítulo, se te mostrarán dos opciones y deberás hacer click en la que creas que es mejor, así de simple. </p>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'instructions',
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

    h1 {
        margin-top: 8vh;
        margin-left: 6vw;
        font-size: 30px;
        color: #9f00eb;
        padding: 20px;
        font-family: 'Press Start 2P', cursive;
    }

    p {
        font-size: 15px;
        text-align: center;
        margin-top: 35vh;
        margin-bottom: 5vh;
        margin-left: 15vw;
        margin-right: 15vw;
        padding: 20px;
        color: white;
    }

    #last_chapter_text {
        margin-top: 15vh;
    }
</style>