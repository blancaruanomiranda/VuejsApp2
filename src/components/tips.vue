<template>
    <div class="tips">
        <p>
            Ahora que ya conoces un poquito más lo que es la huella digital, te dejo por aquí unos consejos para que la cuides y le saques partido:
        </p>     
        <ul class="a">
            <li v-for="item in items" :key="item.message">
                {{ item.message }}
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'tips',
        props: {
            counter: Number,
            chapter_counter: Number
        },
        data() {
            return {
                items: [
                    { message: 'Prueba a buscar tu nombre en Internet. A veces los resultados te pueden sorprender. ' },
                    { message: 'Siempre es mejor borrar aquellas cuentas que ya no utilices' },
                    { message: 'Cuida la huella digital de los demás: pregunta antes de colgar una foto con alguien, de etiquetar,...' },
                    { message: 'Piensa antes de postear algo. ¿Es ofensivo o irrespetuoso el comentario que quieres publicar? ¿Estás revelando información personal?' },
                    { message: 'Controla quién ve lo que publicas controlando las opciones de privacidad. ' },
                    { message: 'Aunque tengas el perfil privado, una vez publicas algo cualquiera que lo vea puede compartirlo, hacer captura… Tenlo en cuenta. ' }
                ]
            }
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

    p {
        font-size: 15px;
        text-align: center;
        margin-top: 15vh;
        margin-bottom: 3vh;
        margin-left: 15vw;
        margin-right: 15vw;
        color: white;
    }

    li {
        font-size: 15px;
        margin-left: 15vw;
        margin-right: 15vw;
        padding: 20px;
        color: white;
        padding-bottom: 1px;     
    }

    ul.a{
        list-style-type: "\1F44D";
        list-style-position: inside;
        color: red;
        margin-bottom: 5vh;        
    }
   
</style>