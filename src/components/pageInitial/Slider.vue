<template>
    <div id="slider">
        <div id="slides">
            <!-- Raio Buttons -->
            <input type="radio" name="radio-btn" id="radio1">
            <input type="radio" name="radio-btn" id="radio2">
            <input type="radio" name="radio-btn" id="radio3">
            <input type="radio" name="radio-btn" id="radio4">

            <!-- Slides Images -->
            <div class="slide first">
                <img src="/img/slider1.jpg" alt="Imagem 1">
            </div>
            <div class="slide">
                <img src="/img/slide2.jpg" alt="Imagem 2">
            </div>
            <div class="slide">
                <img src="/img/slide3.jpg" alt="Imagem 3">
            </div>
            <div class="slide">
                <img src="/img/slide4.jpg" alt="Imagem 4">
            </div>

            <!-- Navigation auto -->
            <div id="navigation-auto">
                <div class="auto-btn1"></div>
                <div class="auto-btn2"></div>
                <div class="auto-btn3"></div>
                <div class="auto-btn4"></div>
            </div>
        </div>

        <div id="manual-navigation">
            <label for="radio1" class="manual-btn"></label>
            <label for="radio2" class="manual-btn"></label>
            <label for="radio3" class="manual-btn"></label>
            <label for="radio4" class="manual-btn"></label>
        </div>

    </div>
</template>

<script>
    export default {
        name: 'Slider',
        methods: {
            // nextImage() {
            //     const count = 1
            //     document.getElementById("radio1").checked = true

            //     setInterval(function() {
            //         count++
            //         if(count>4) {
            //             count = 1
            //         }

            //         document.getElementById("radio" + count).checked = true
            //     }, 2000)
            // }
        },
        mounted() {
            // this.nextImage()
        }
    }

</script>

<style scoped>

    #slider {
        /* background-position: 0 -250px; */
        margin: 100px 0;
        width: auto;
        height: 400px;
        overflow: hidden;
        
    }

    #slides {
        width: 400%;
        height: 400px;
        display: flex;
    }
    
    #slides input {
        display: none;
    }

    .slide {
        width: 25%;
        position: relative;
    }

    .slide img {
        width: 100%;
        height: 110%;

    }

    #manual-navigation {
        position: absolute;
        width: 100%;
        margin: -20px;
        display: flex;
        justify-content: center;
    }

    .manual-btn {
        margin-inline: 10px;
        border: 2px solid #fff;
        padding: 5px;
        border-radius: 10px;
        cursor: pointer; 
        transition: 1s;
    }

    .manual-btn:not(:last-child) {
        margin-right: 20px;
    }

    .manual-btn:hover {
        background-color: #fff;
    }

    #radio1:checked ~ .first {
        margin-left: 0;

    }
    #radio2:checked ~ .first {
        margin-left: -25%;
    }
    #radio3:checked ~ .first {
        margin-left: -50%;
    }
    #radio4:checked ~ .first {
        margin-left: -75%;
    }

    /* #navigation-auto div {
        border: 2px solid #20a6ff;
        padding: 5px;
        border-radius: 10px;
        cursor: pointer;
        transition: 1s;
    }

    #navigation-auto {
        position: absolute;
        width: 800px;
        margin-top: 360px;
        display: flex;
        justify-content: center;
    }

    #navigation-auto div:not(:last-child) {
        margin-right: 15px;
    } */

    #radio1:checked ~ #navigation-auto .auto-btn1 {
        background-color: #FFF;
    }

</style>