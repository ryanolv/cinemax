<template>
    <div id="Connect">
        <p>Quer assistir? Informe seu email para criar sua conta</p>
        <form :on-click="{newUser}">
            <input type="text" name="email" id="email"  placeholder="Email">
            <button type="submit">Vamos lá</button>
        </form>
        <p>Já tenho cadastro</p>
    </div>
</template>

<script>
    export default {
        name: 'Connect',
        data() {
            return {
                email: null
            }
        },
        methods: {

            newUser(e) {

                e.preventDefault()


            }
        }
    }
</script>

<style scoped>
    #Connect {
        text-align: center;
        /* padding: 20px; */
    }

    #Connect p {
        color: #FFF;
    }

    #Connect form {
        display: flex;
        justify-content: center;
        padding-inline: 0;
    }

    #Connect form input {
        width: 800px;
        height: 30px;
        padding-left: 30px;
        border: none;
        
    }

    #Connect form button {
        width: 100px;
        height: 100%px;
        background-color: #6F0A0A;
        border: none;
        color: #FFF;
        cursor: pointer;
    }


</style>