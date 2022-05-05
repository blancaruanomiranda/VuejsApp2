    <template>
    
        <div class="instructions2">
            <meta charset="UTF-8" />
            <p id="p1">
                Jimmy es un chico de 15 años que vive en Stalk Hollow. En Stalk Hollow hay un acosador que investiga las redes sociales de los adolescentes para extraer información sobre ellos y perseguirlos. Jimmy nunca ha tenido redes sociales porque a sus padres les da miedo el acosador, pero a Jimmy le gustaría poder tenerlas y compartir parte de su día a día, como hacen todos sus amigos.
                Tu misión consiste en ayudar a Jimmy a gestionar sus redes sociales y evitar que el acosador de la ciudad pueda seguirle el rastro.
            </p>
            <p id="p2">Cada vez que tomes una decisión, verás una respuesta y una barra de progreso. La barra se acercará más a Jimmy cada vez que tomes una buena decisión y se acercará más al acosador cuando tomes una mala.</p>
            <img src="@/components/static/img/stalker.png" />
        </div>
    </template>

    <script>
    export default {
        name: 'instructions2',
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

            margin-left: 15vw;
            margin-right: 15vw;
            padding: 20px;
            color: white;
        }
        #p1 {
            margin-top: 10vh;
        }
        #p2{
            
            margin-bottom: 5vh;
        }
        img {
            position: fixed;
            right: 5vw;
            bottom: 5vh;
            height: 45%;
            width: 30%;
        }
        
    </style>            