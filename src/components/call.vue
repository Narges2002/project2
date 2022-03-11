<template>
  <div class="cal">
    <h3>دریافت مشاوره‌ی رایگان</h3>
    <p>برای ثبت‌نام یا دریافت مشاوره رایگان، شماره‌ واتساپ تو ثبت کن تا کارشناس‌های برنافیت بهت پیام بدن</p>
    <div v-if="!response">
      <div class="possition">
        <button v-if="!loading" :disabled="!valid" :class="!valid ? 'disabled' : ''" @click="postNumber">
          ثبت
        </button>
        <button v-else>
          <svg version="1.1" id="L9" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
               x="0px"
               y="0px"
               viewBox="0 0 100 100" enable-background="new 0 0 0 0" xml:space="preserve">
          <path fill="#fff"
                d="M73,50c0-12.7-10.3-23-23-23S27,37.3,27,50 M30.9,50c0-10.5,8.5-19.1,19.1-19.1S69.1,39.5,69.1,50">
              <animateTransform
                  attributeName="transform"
                  attributeType="XML"
                  type="rotate"
                  dur="1s"
                  from="0 50 50"
                  to="360 50 50"
                  repeatCount="indefinite"/>
          </path>
        </svg>
        </button>
        <input :class="{'is-valid':!valid,'is-invalid':valid}" ref="input1" maxlength="11"
              @input="phoneNumberChecker($event.target.value)">
      </div>
      <div class="mt-2" v-if="numberEM">{{ numberEM }}</div>
    </div>
    <div v-else>
      <p class="response-message">ثبت نام شما با موفقیت انجام شد!</p>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  data() {
    return {
      number: '',
      valid: false,
      numberEM: '',
      loading: false,
      response: false
    }
  },
  methods: {
    phoneNumberChecker(phoneNumber) {
      if (/^(\+98|0098|98|0)?9\d{9}$/.test(phoneNumber)) {
        this.number = phoneNumber
        this.numberEM = ""
        this.valid = true
      } else {
        this.valid = false
        this.numberEM = "شماره همراه خود را بدرستی وارد کنید."
      }
    },
    postNumber() {
      this.loading = true
      axios.post("https://crm.bornafit.ir/api/getnumber", {
        headers: {
          'Content-Type': 'application/json',
          'Authorization': 'nz9XS54cGjV7nfPfASDF@#$ASDfEHuQP3kGm2rymF'
        },
        "repositoty": 1,
        "topic": 31,
        "mobile": this.number
      })
          .then((response) => {
            this.response = true
            this.loading = false
          })
          .catch((error) => {
            console.log(error)
            this.response = true
            this.loading = false
          })
    },
  }
}
</script>

<style scoped>
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
  padding: 9px 65px;
  border-radius: 7px;
  border: none;
  font-family: IRANSansWeb;
  font-size: 18px;
  text-align: center;
  width: 100%;
}

svg {
  width: 25px;
  height: 25px;
  display: inline-block;
}

.possition {
  position: relative;
  width: 100%;
  max-width: 317px;
  margin: 0 auto;
}

.cal button {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  right: 10px;
  background-color: hsl(120, 45.8%, 47.1%);
  font-size: 17px;
  border: 0;
  color: white;
  padding: 4px 8px;
  border-radius: 7px;
  z-index: 5;
}
.response-message{
  color: #76e44c
}

.cal .disabled {
  background: gray;
}

.invalid-feedback {
  color: white;
  font-size: 12px;
}

button:hover {
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
