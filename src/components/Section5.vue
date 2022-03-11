<template>
    <div id="Section5">
        <video class="video" controls>
            <source src="../assets/images/video/recorders.mp4" type="video/mp4">
        </video>
        <div class="text">
            <p><b>چطور با برناجت سرعت کاهش وزنم رو 2 برابر کنم؟</b></p>
        </div>
        <div class="cal">
            <div class="possition">
                <h3>دریافت مشاوره‌ی رایگان</h3>
                <p>برای ثبت‌نام یا دریافت مشاوره رایگان، شماره‌ واتساپ تو ثبت کن تا کارشناس‌های برنافیت بهت پیام بدن</p>
                <span @click="postNumber(phone_number)">ثبت</span>
                <label>09</label>
            </div>
            <div class="CallNumber">
                <input
                v-model="phone_number"
                @input="click"
                :class="{
                    'is-valid':numberE===false,
                    'is-invalid':numberE===true
                    }"
                maxlength="11"
                pattern="[0-9()#&amp;+*-=.]+" title="فقط اعداد و کاراکترهای تلفن (#، -، *، و غیره) پذیرفته می شوند
."
                type="tel" placeholder="شماره واتساپ">
                <div class="invalid-feedback" v-if="numberE">{{numberEM}}</div>
            </div>
        </div>
    </div>
</template>
<script>
import axios from 'axios'
    export default {
        data() {
            return {
                number:'',
                numberE: null,
                numberEM: null,
                phone_number: null,
            }
        },
        methods: { 
            click() {
                this.addNumber()
                this.enforcePhoneFormat()
            },
            addNumber() {
                if (this.phone_number.length < 11) {
                this.numberE = true
                this.numberEM = "شماره همراه خود را بدرستی وارد کنید."
                } else {
                this.numberE = false
                this.numberEM = ''
                }
            },
            enforcePhoneFormat() {
                let x = this.phone_number
                .match(/(\d{0,3})(\d{0,3})(\d{0,4})/);

                this.phone_number = !x[2]
                ? x[1]
                : + x[1]  + x[2] + (x[3] ? + x[3] : "");
            },
            postNumber(phone_number) {
                console.log('click')
                axios.post("https://crm.bornafit.ir/api/getnumber", {
                headers: {
                    'Content-Type': 'application/json',
                    'Authorization': 'nz9XS54cGjV7nfPfASDF@#$ASDfEHuQP3kGm2rymF'
                },
	                "repositoty": 1,
                    "topic": 31,
                    "mobile": `09${phone_number}`
                })      
                .then((response) => {
    
                })
                .catch((error) => {
    
                })
            },
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
.cal {
    background-color: hsl(340, 76.3%, 46.3%);
    padding: 15px;
    color: white;
    border-radius: 20px;
    font-size: 20px;
    margin-bottom: 30px;
    margin-top: 30px;
    font-size: 15px;
}
.cal input {
    padding: 9px 35px;
    border-radius: 7px;
    border: none;
    font-family: IRANSansWeb;
    font-size: 18px;
    text-align: center;
}
.possition {
    position: relative;
}
.cal span {
   position: absolute;
    right: 15%;
    bottom: -65%;
    background-color: hsl(120, 45.8%, 47.1%);
    font-size: 17px;
    padding: 4px 8px;
    border-radius: 7px;
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
.invalid-feedback {
    color: white;
    font-size: 12px;
}
span:hover {
    background-color: rgb(192, 188, 188);
}
label {
    font-size: 19px;
    position: absolute;
    bottom: -62%;
    left: 27%;
    color: black;
}
</style>