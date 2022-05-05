<template>
    <div class="answer2">

        <h1>CAPÍTULO {{chapter_counter}}</h1>

        <p id="text"> {{items[chapter_counter-1].message}}</p>
        <div class="answer_box">
            <p id="answer_text">{{items[chapter_counter-1].answer2}}</p>
            <p v-if="items[chapter_counter-1].point==1" id="answer_text"><ion-icon name="checkmark-outline"></ion-icon></p>
            <p v-if="items[chapter_counter-1].point==0" id="answer_text"><ion-icon name="close-outline"></ion-icon></p>
        </div>
        <div class="barra_container">
            <div class="stalker-icon">
                <img src="@/components/static/img/stalker_icon.png" />
            </div>
            <div class="barra">
                <div :style="barWidthCalculated"></div>
            </div>
            <div class="jimmy-icon">
                <img src="@/components/static/img/timmy_icon.png" />
            </div>
        </div>

        <script type="module" src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.esm.js"></script>

    </div>
</template>

<script>

    export default {
        name: 'answer2',
        computed: {
            barWidthCalculated: function () {
                return {
                    width: (this.progreso) + '%'
                };
            }
        },
        props: {
            counter: Number,
            chapter_counter: Number,
            progreso: Number
        },
        data() {
            return {

                items: [
                    {
                        message: 'Son las 11 de la mañana de un viernes. Es la hora del patio. Jimmy y sus amigos se sientan en las gradas, como siempre, mientras se comen sus bocatas. Hoy es un día especial: los padres de Jimmy por fin le dejan hacerse un perfil en las redes sociales. Los amigos de Jimmy le explican que lo primero que tienes que hacer al crearte un perfil es escoger el nombre de usuario, la foto de perfil y añadir una pequeña biografía para que la gente te pueda conocer un poco más. ',
                        answer2: 'Muy buena elección. La gente que vea el perfil de Jimmy podrá saber cuáles son sus aficiones, no hay nada malo en eso.',
                        point: 1
                    },
                    {
                        message: 'Después de todo el día en el insti, por fin es la hora de volver a casa. Jimmy tiene muchas ganas de llegar y estirarse en el sofá para ver el debate de la Isla de las Tentaciones de la noche anterior mientras se toma un ColaCao. Jimmy tiene tantas ganas de llegar a su casa que cuando por fin está delante de la puerta decide compartirlo en su perfil.',
                        answer2: '¡Qué pena! Sin saberlo, Jimmy le acaba de dar una información muy valiosa a su acosador al compartir esta historia. Resulta que el acosador conoce perfectamente el barrio de Jimmy y ha reconocido al instante su portal. Ahora sabe dónde vive exactamente.',
                        point: 0
                    },
                    {
                        message: 'Tras una tarde chill en el sofá, Jimmy se pone su mejor outfit para ir a cenar con sus amigos. Van a celebrar el cumpleaños de Marc, el pequeño del grupo. En ese grupo es tradición que el cumpleañero escoja dónde quiere cenar, así que como Marc es muy fan de las hamburguesas con patatas, van a la mejor hamburguesería de la ciudad.',
                        answer2: '¡Qué pena! Al compartir la ubicación del restaurante en el que se encuentran en ese mismo momento, Jimmy le ha dado una oportunidad a su acosador para acercarse a él. Durante toda la cena, notan que alguien les vigila desde la calle. Además, una cuenta un tanto extraña ha empezado a seguir a todos los amigos de Jimmy...',
                        point: 0
                    },
                    {
                        message: 'Al día siguiente, los panas comentan por WhatsApp la noche anterior. Aunque se lo pasaron genial, porque lo importante es la compañía, tuvieron algún problemilla con los camareros. Jimmy decide buscar el perfil de la hamburguesería y dejarles un comentario en su última publicación para quejarse.',
                        answer2: '¡Bien! El restaurante ve la crítica que ha escrito Jimmy y toma nota. Se esfuerzan mucho en mejorar y tienen muy en cuenta las opiniones de sus clientes, así que para compensar el error del otro día deciden invitar a Jimmy y sus amigos a tomar una hamburguesa gratis.',
                        point: 1
                    },
                    {
                        message: 'Se acercan los exámenes finales. Jimmy decide aprovechar todo el finde para estudiar. Las primeras tres horas son bastante productivas y Jimmy está a tope estudiando mates, pero al final acaba con la cabeza como un bombo. Jimmy coge el móvil y le hace una foto a sus apuntes, para compartir el sufrimiento con sus seguidores.',
                        answer2: '¡Cuidado! Si te fijas bien, se puede ver el DNI de Jimmy en una esquina de la foto. Jimmy debería vigilar todo lo que cuelga, incluso los pequeños detalles y sobretodo debería evitar compartir información personal. ',
                        point: 0
                    },
                    {
                        message: 'Justo cuando Jimmy acaba de colgar la foto de sus apuntes, le llega una notificación de un mensaje. La persona que le manda el mensaje no tiene foto de perfil y se llama rodasoca_al_reves. El mensaje dice lo siguiente: “Hola Jimmy!! ¡Cuánto tiempo hermano!  Te acuerdas de mí ? Soy David, jugábamos juntos a basket jaja me das tu email y tu número de teléfono para que hablemos y quedemos un día ?”',
                        answer2: '¡Lo estás haciendo genial! ¿Cómo iba Jimmy a darle esos datos a un desconocido? Encima da muy mal rollito',
                        point: 1
                    }

                ]
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
        margin-top: 5vh;
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
    .barra_container {
        display: flex;
        width: fit-content;
        justify-content: center;
        align-items: center;
        margin: auto;
        height: 8vh;
        overflow: hidden;
    }

    .jimmy-icon {
        transform: scale(0.4);
        background: transparent;
    }

    .stalker-icon {
        transform: scale(0.4);
        background: transparent;
    }

    .barra_container img {
        background: transparent;
    }
    .barra {
        width: 250px;
        height: 16px;
        margin: auto;
        border-radius: 10px;
        border: 1px solid #9f00eb;
        background-color: red;
        color: red;
    }

        .barra div {
            
            border-radius: 10px;
            border: 8px solid #9f00eb;
        }
</style>