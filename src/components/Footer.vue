<template>
    <div id="Section5">
        <div class="footer">
            <img src="../assets/images/footer/logo.png">
            <p><b>برنافیت دکتر کرمانی</b></p>
            <p>تهران، خیابان شریعتی، کوچه داد</p>
            <p><a href="tel:02191016633" style="margin-bottom: 5px; font-size: 18px;">۹۱۰۱۶۶۳۳ - ۰۲۱</a></p>
            <p>www.bornafit.ir</p>
        </div>
    </div>
</template>
<style scoped>
#Section5 {
    text-align: center;
    margin-bottom: 30px;
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
.footer img {
    width: 110px;
    margin: 20px 0 10px;
}
.footer {
    background-color: white;
    padding: 10px 30px;
    border-radius: 30% 30% 0 0;
}
.invalid-feedback {
    color: white;
    font-size: 12px;
}
</style>