<template>
    <div class="answer">
        <meta charset="UTF-8" />
        <h1>CAPÍTULO {{chapter_counter}}</h1>

        <p id="text"> {{items[chapter_counter-1].message}}</p>
        <div class="answer_box">
            <p id="answer_text">{{items[chapter_counter-1].answer1}}</p>
            <p v-if="items[chapter_counter-1].point==1" id="answer_text"><ion-icon name="checkmark-outline"></ion-icon></p>
            <p v-if="items[chapter_counter-1].point==0" id="answer_text"><ion-icon name="close-outline"></ion-icon></p>
        </div>
        
        <script type="module" src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.esm.js"></script>
    </div>
</template>

<script>
    
    export default {
        
        name: 'answer',

        props: {
            counter: Number,
            chapter_counter: Number,
            value: Number,
            
            
         
        },
        data() {
            return {
                icon_name: "",
                items: [
                    {
                        message: 'Son las 11 de la mañana de un viernes. Es la hora del patio. Jimmy y sus amigos se sientan en las gradas, como siempre, mientras se comen sus bocatas. Hoy es un día especial: los padres de Jimmy por fin le dejan hacerse un perfil en las redes sociales. Los amigos de Jimmy le explican que lo primero que tienes que hacer al crearte un perfil es escoger el nombre de usuario, la foto de perfil y añadir una pequeña biografía para que la gente te pueda conocer un poco más. ',
                        answer1: '¡Cuidado! Compartir información tan personal en las redes puede ser peligroso. Quizás debería haber escogido la otra opción.',
                        point: 0
                    },
                    {
                        message: 'Después de todo el día en el insti, por fin es la hora de volver a casa. Jimmy tiene muchas ganas de llegar y estirarse en el sofá para ver el debate de la Isla de las Tentaciones de la noche anterior mientras se toma un ColaCao. Jimmy tiene tantas ganas de llegar a su casa que cuando por fin está delante de la puerta decide compartirlo en su perfil.',
                        answer1: '¡Genial! El acosador sabe que Jimmy está en su casa, pero no logra extraer ningún dato relevante de esta historia, así que decide dejar tranquilo a Jimmy toda la tarde.',
                        point: 1
                    },
                    {
                        message: 'Tras una tarde chill en el sofá, Jimmy se pone su mejor outfit para ir a cenar con sus amigos. Van a celebrar el cumpleaños de Marc, el pequeño del grupo. En ese grupo es tradición que el cumpleañero escoja dónde quiere cenar, así que como Marc es muy fan de las hamburguesas con patatas, van a la mejor hamburguesería de la ciudad.',
                        answer1: ' ¡Genial! El acosador ve la foto y no reconoce el sitio. De hecho, la hamburguesa de la foto tiene tan buena pinta que le da envidia y decide hacerse una para él en su casa. Jimmy puede estar tranquilo toda la noche.',
                        point: 1
                    },
                    {
                        message: 'Al día siguiente, los panas comentan por WhatsApp la noche anterior. Aunque se lo pasaron genial, porque lo importante es la compañía, tuvieron algún problemilla con los camareros. Jimmy decide buscar el perfil de la hamburguesería y dejarles un comentario en su última publicación para quejarse.',
                        answer1: '¡Vaya! Al acosador le da igual el comentario de Jimmy, pero a los dueños del restaurante no. Resulta que conocen a los padres de Jimmy, y deciden enseñarles la review de su hijo. Jimmy recibe una bronca monumental y dos semanas de castigo. Desde luego, Jimmy no debería haber dejado un comentario tan despectivo.',
                        point: 0
                    },
                    {
                        message: 'Se acercan los exámenes finales. Jimmy decide aprovechar todo el finde para estudiar. Las primeras tres horas son bastante productivas y Jimmy está a tope estudiando mates, pero al final acaba con la cabeza como un bombo. Jimmy coge el móvil y le hace una foto a sus apuntes, para compartir el sufrimiento con sus seguidores.',
                        answer1: '¡Genial! Un poco de postureo nunca viene mal.',
                        point: 1
                    },
                    {
                        message: 'Justo cuando Jimmy acaba de colgar la foto de sus apuntes, le llega una notificación de un mensaje. La persona que le manda el mensaje no tiene foto de perfil y se llama rodasoca_al_reves. El mensaje dice lo siguiente: “Hola Jimmy!! ¡Cuánto tiempo hermano!  Te acuerdas de mí ? Soy David, jugábamos juntos a basket jaja me das tu email y tu número de teléfono para que hablemos y quedemos un día ?”',
                        answer1: '¡¡FATAL!! Jimmy ni siquiera sabe quién es este tal David. ¿No crees que no debería haberle dado su email y su número a un completo desconocido?',
                        point: 0
                    }
                 
                ]
            }
        },
        methods: {
            answerFunction: function () {
                alert('this is A.foo');
            }
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
        margin-top: 8vh;
        margin-left: 6vw;
        font-size: 30px;
        color: #9f00eb;
        padding: 20px;
        font-family: 'Press Start 2P', cursive;
    }
    p {
        font-size: 15px;
        margin-left: 7vw;
        margin-bottom: 5vh;
        margin-right: 8vw;
        color: white;
    }

    #answer_text {
        text-align: center;
        margin-bottom: 2vh;
        color: #00fff0;
    }
    .answer_box {
        color: #00fff0;
        padding: 30px;
        text-align: center;
        margin-block-start: 5vh;
        border: 3px #e300ff double;
        width: 50%;
        margin: 5vh auto;
    }
    i {
        color: #00fff0;
        background: transparent;
    }
   
</style>