<template>
    <div id="Section1">
        <div class="Header-text">
            <div class="Header">
                <h2>میان‌‌بر قطعی تخت‌شدن شکم</h2>
            </div>
            <p>برای این که تا عید با چربی‌های شکمت خداحافظی کنی و تو مهمونی‌ها قشنگ‌ترین لباس‌هاتو بپوشی، بـرناجت بهترین و سریع‌ترین راهه! اما چجوری؟ حتما این ویدئو رو ببین!</p>
            <p>برنافیت برای شمایی که عضو رژیم هستین یه تخفیف ویژه در نظر گرفته تا بتونین در کنار رژیم غذایی، برنامه تمرینی برناجت رو هم دریافت کنید</p>
        </div>
        <video class="video" controls  poster="../assets/images/video/cover1.jpg">
            <source src="../assets/images/video/bornajet-intro.mp4" type="video/mp4">
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
#Section1 {
    text-align: center;
    margin-bottom: 30px;
}
.Header-text p {
    text-align: right;
    font-size: 15px;
}
.Header h2 {
    font-size: 1.2rem;
    position: relative;
}
.Header ::before { 
    content: "";
    position: absolute;
    top: 15px;
    right: 0;
    background-color: hsl(219.3, 82.9%, 93.1%);
    width: 17%;
    height: 2px;
}
.Header ::after {
    content: "";
    position: absolute;
    top: 15px;
    left: 0;
    background-color: hsl(219.3, 82.9%, 93.1%);
    width: 17%;
    height: 2px;
}
.video {
    width: 100%;
    border-radius: 20px;
    margin-bottom: 10px;
    border: none;
}
.text {
    background-color: white;
    padding: 20px 25px 15px;
    border-radius: 20px;
    position: relative;
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