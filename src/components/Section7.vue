<template>
    <div class="section7 mt-5 pt-5">
        <div class="container pb-5">
            <div class="row">
                <div class="col-12 col-md-6 text-center mb-5 mb-md-0">
                    <div class="input-text mt-md-0">
                        <h4>
                            ثبت نام در رژیم
                        </h4>
                        <p class="mb-2">برای دریافت مشاوره با کارشناسان دکتر کرمانی
                            <br>
                           شماره همراه خود را ثبت کنید،ما با شما تماس میگیریم
                        </p>
                    </div>
                    <div class="btn-success-box">
                        <button class="btn btn-success scroll-to-reg btn-lg" id="submit-2">
                            <a href="">همین الان میخوام خوش اندام بشم</a>
                        </button>
                    </div>
                </div>
                <div class="col-12 col-md-6 text-center mb-5 mb-md-0">
                    <div class="input-text mt-md-0">
                        <h4>
                            دریافت مشاور تلفنی 
                        </h4>
                        <p class="mb-2">برای دریافت رژیم و شروع یه برنامه منظم
                            <br>
                                میتونی همین الان ثبت نام کنی
                        </p>
                    </div>
                    <div class="form-holder text-center">
                        <input type="tel" name="tel" placeholder="xx xxx xxxx" class="form-control tel">
                        <label>09</label>
                        <button type="submit" class="btn landing-btn">
                            <span>ثبت</span>
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import axios from 'axios'
    export default {
        setup() {
           function getNumber() {
            axios.post('https://crm.bornafit.ir/api/getnumber', {
            phoneNumber:'09121111111'
        })
            .then(function (response) {
             console.log(response);
        })
            .catch(function (error) {
            console.log(error);
        });
        }
        getNumber()
    }
}
</script>

<style scoped>
.container {
    max-width: 1140px;
}
.section7 {
    width: 100%;
    background-repeat: no-repeat;
}
.btn {
    border-radius: 20px;
    font-size: 14px;
    padding: 10px 50px;
}
.input-text h4 {
    font-size: 20px;
    color: #b53471;
}
.input-text p {
    font-size: 13px;
}
.btn a {
    text-decoration: none;
    color: white;
}
.form-holder {
    width: 350px;
    position: relative;
    margin: auto;
}
.form-control {
    border-radius: 22px;
    display: block;
    margin: o auto;
    direction: ltr !important;
    padding: 7px 89px 7px 63px;
}
label {
    position: absolute;
    top: 9px;
    left: 40px;
}
.landing-btn {
    position: absolute;
    top: 0;
    bottom: 0;
    right: 1px;
    font-size: 17px;
    background-color: #82888d;
    padding: 7px 25px;
    border-radius: 0 22px 22px 0;
    color: white;
}
</style>