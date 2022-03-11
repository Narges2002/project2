<template>
    <div id="Header">
        <div id="Header">
            <img src="../assets/images/Header/1.png" alt="img">
            <img class="image" src="../assets/images/Header/loader-stars.jpg">
            <img class="img" src="../assets/images/Header/small-rocket.png">
            <button @click="scrollToTop" class="btn">
             ثبت نام در رژیم
            </button>
        </div>
    </div>
</template>
<script>
export default {
    methods: {
        scrollToTop() {
            window.scrollTo(0,2370);
        },
    }
}
</script>
<style scoped>
#Header {
    text-align: center;
    margin-bottom: 30px;
    position: relative;
}
.img {
    animation-timing-function: ease-out;
}
@keyframes mymove {
from {bottom: 200px;}
to {bottom: 800px;}
}
.img {
    width: 55px;
    position: absolute;
    bottom: 25%;
    left: 45%;
    animation: mymove 5s infinite;
}
.image {
    border-radius: 50%;
    width: 110px;
    position: absolute;
    bottom: 25%;
    left: 38%;
}
img {
    width: 100%;
    height: auto;
    display: block;
    margin: 0 auto;
    margin-bottom: 30px;
}
.btn {
    padding: 10px 110px;
    background-color: hsl(120, 45.8%, 47.1%);
    border: none;
    border-radius: 10px;
    color: white;
    font-size: 17px;
}
</style>