<template>
    <div id="Section3">
        <div class="Header">
            <h2>چرا رژیم برناجت</h2>
        </div>
        <div class="text">
            <div class="part1">
              <div class="picture">
                <img src="../assets/images/icone/why-bornafit-icon1.png">
              </div>
              <h1>با سریع‌ترین راه، شکم‌تو تخت کن</h1>
              <p>با برناجت علاوه بر رژیم غذایی، برنامه تمرینی هم دریافت می‌کنی. این 2 در کنار هم باعث می‌شن چربی‌سوزی بدنت به بالاترین سطح برسه</p>
            </div>
            <div class="part2">
              <div class="picture">
                <img src="../assets/images/icone/why-bornafit-icon2.png">
              </div>
              <h1>با رژیم اصولی چربی‌هاتو بسوزون</h1>
              <p>به رژیم فعلی ای که از برنافیت دریافت کردی یک سهمیه پروتئینی اضافه میشه تا به کمکش چربی هارو به عضله تبدیل کنی</p>
            </div>
            <div class="part3">
              <div class="picture">
                <img src="../assets/images/icone/why-bornafit-icon3.png">
              </div>
              <h1>تو خونه‌ زیر نظر مربی‌ تمرین کن</h1>
              <p>برنامه تمرینی، یه برنامه تخصصی حرکات اصلاحی در منزله. می‌تونی به راحتی ویدئوی تمرینات رو توی گوشی یا تلویزیون ببینی و با هر آمادگی جسمانی همراه مربی‌ت تمرین کنی</p>
            </div>
          </div>
    </div>
</template>
<style scoped>
#Section3 {
    text-align: center;
    margin-bottom: 30px;
}
.Header {
  position: relative;
}
.Header h2 {
    text-align: center;
    font-size: 18px;
    padding: 10px 0;
}
.Header ::before {
    content: "";
    position: absolute;
    top: 25px;
    right: 7px;
    background-color: hsl(219.3, 82.9%, 93.1%);
    width: 30%;
    height: 2px;
}
.Header ::after {
    content: "";
    position: absolute;
    top: 25px;
    left: 7px;
    background-color: hsl(219.3, 82.9%, 93.1%);
    width: 30%;
    height: 2px;
}
.text {
  text-align: right;
}
.part1,.part2,.part3 {
  border: 1px solid hsl(215.3, 58.6%, 94.3%);
  margin-bottom: 10px;
  border-radius: 17px;
  padding: 20px;
}
.text h1 {
  font-size: 18px;
  word-spacing: -5px;
}
.text {
  font-size: 15px;
}
.part1 {
  background-color: #f6f1fe;
}
.part2 {
  background-color: #faf0f5;
}
.part3 {
  background-color: #eef9fc;
}
.picture img {
  width: 50px;
}
.picture {
  width: 17%;
  float: right;
  height: 100px;
}
</style>