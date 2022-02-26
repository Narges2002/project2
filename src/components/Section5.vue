<template>
    <div class="slider container">
        <div class="section2-header m-md-0">
            <h2>برخی از افراد موفق</h2>
        </div>
    </div>
    <div class="Section5">
        <video class="video" controls  poster="../assets/image/video/recorders.jpg">
            <source src="../assets/image/video/recorders.mp4" type="video/mp4">
        </video>
    </div>
</template>

<style scoped>
.container {
    max-width: 1140px;
}
    .video {
        width: 68%;
        margin: 0 auto;
        display: block;
    }
.section2-header {
    color: #b1346e;
    position: relative;
    padding: 40px 0 20px;
}
.section2-header h2 {
    padding-right: 40px;
    font-size: 20px;
    font-weight: 600;
}
.section2-header h2::before {
    content: "";
    position: absolute;
    top: 58%;
    right: 0;
    background-color: #b1346e;
    width: 30px;
    height: 2px;
}
</style>