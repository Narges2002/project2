<template>
    <div id="Section5">
        <video class="video" controls>
            <source src="../assets/images/video/recorders.mp4" type="video/mp4">
        </video>
        <div class="text">
            <p><b>چطور با برناجت سرعت کاهش وزنم رو 2 برابر کنم؟</b></p>
        </div>
        <call/>
    </div>
</template>

<script>
import call from './call'
export default {
    name : 'section5',
    components:{
        call
    }
}
</script>

<style scoped>
#Section5 {
    text-align: center;
    margin-bottom: 30px;
}
.video {
    width: 100%;
    border-radius: 20px;
    margin-bottom: 7px;
    border: none;
}
.text {
    position: relative;
    margin-bottom: 30px;
}
.text p {
    background-color: white;
    padding: 20px;
    border-radius: 10px;
}
.text ::before {
    content: "";
    position: absolute;
    left: 5%;
    background-color: hsl(228, 9.3%, 57.6%);
    width: 2px;
    height: 39%;
    bottom: 85%;
    z-index: 2;
}
.text p ::before {
    content: "";
    position: absolute;
    left: 4%;
    background-color: rgb(77, 78, 83);
    width: 9px;
    height: 9px;
    border-radius: 50%;
    top: 9%;
    z-index: 1;
}
.text ::after {
    content: "";
    position: absolute;
    right: 5%;
    background-color: hsl(228, 9.3%, 57.6%);
    width: 2px;
    height: 39%;
    bottom: 85%;
    z-index: 2;
}
.text p ::after {
    content: "";
    position: absolute;
    right: 4%;
    background-color: rgb(77, 78, 83);
    width: 9px;
    height: 9px;
    border-radius: 50%;
    top: 9%;
}
</style>