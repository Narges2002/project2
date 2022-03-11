<template>
    <div id="Section4">
        <div class="img">
            <img src="../assets/images/bmi/bmi-header-icon.png">
        </div>
        <div class="text">
            <p><b>می‌خوای بدونی چه قدر اضافه وزن داری؟ و چقدر طول میکشه شکمت تخت بشه؟</b></p>
            <p><b>مشخصاتت رو وارد کن!</b></p>
        </div>
        <div class="circle">
            <span class="">2</span>
            <span id="active">1</span>
        </div>
        <div class="input-form">
            <div class="input-group">
                <div id="container-toggle">
                    <div class="inner-container-toggle">
                        <div class="toggle">
                            <input type="radio" id="inp1" name="gender" value="female">
                            <label for="inp1">خانم هستم</label>
                        </div>
                        <div class="toggle">
                            <input type="radio" id="inp2" name="gender" value="male">
                            <label for="inp2">آقا هستم</label>
                        </div>
                    </div>
                </div>
            </div>
            <form>
                <div class="mb-3">
                    <label for="exampleInputWeight" class="form-label"></label>
                    <input
                    
                    maxlength="8"
                    @input="standardWeight"
                    type="tel" class="form-control" placeholder="وزن(کیلوگرم)"
                    v-model="weight"
                    :class="{
                        'is-invalid':weightE===true,
                        'is-valid':weightE===false
                        }"
                    >
                    <div class="invalid-feedback" v-if="weightE">{{weightEM}}</div>
                </div>
                <div class="mb-3">
                    <label for="exampleInputHeight" class="form-label"></label>
                    <input 
                    maxlength="8"
                    @input="standardHieght"
                    type="tel" class="form-control" placeholder="قد(سانتی متر)"
                    v-model="height"
                    :class="{
                        'is-invalid':heightE===true,
                        'is-valid':heightE===false
                        }"
                    >
                     <div class="invalid-feedback" v-if="heightE">{{heightEM}}</div>
                </div>
                <div class="mb-3">
                    <label for="exampleInputAge" class="form-label"></label>
                    <input
                    required="required"
                    maxlength="8"
                    @input="standardAge"
                     type="tel" class="form-control" placeholder="سن(سال)"
                    v-model="age"
                    :class="{
                        'is-invalid':ageE===true,
                        'is-valid':ageE===false
                        }"
                    >
                     <div class="invalid-feedback" v-if="ageE">{{ageEM}}</div>
                </div>
            </form>
             <button type="submit" @click="goHighlevel" class="btn">تایید و مرحله بعدی</button>
        </div>
    </div>
</template>
<script>
export default {
    data() {
    return {
        weight: '',
        age: '',
        height: '',
        weightE: null,
        ageE: null,
        heightE: null,
        weightEM: null,
        ageEM: null,
        heightEM: null
    }
},
methods: {
    standardWeight() {
        if (this.weight < 200 && this.weight > 20) {
            this.weightE = false
            this.weightEM = ''
        } else {
            this.weightE = true
            this.weightEM = "وزن باید عددی بین 20 تا 200 کیلوگرم باشد"
        }
    },
    standardAge() {
        if (this.age < 72 && this.age > 12) {
            this.ageE = false
            this.ageEM = ''
        } else {
            this.ageE = true
            this.ageEM = "سن باید عددی بین 12 تا 72 سال باشد"
        }
    },
    standardHieght() {
        if (this.height < 230 && this.height > 100) {
            this.heightE = false
            this.heightEM = ''
        } else {
            this.heightE = true
            this.heightEM = "قد باید عددی بین 100 تا 230 سانتی متر باشد"
        }
    },
    goHighlevel() {
        if (this.weight < 200 && this.weight > 20) {
            this.weightE = false
            this.weightEM = ''
        } else {
            this.weightE = true
            this.weightEM = "وزن باید عددی بین 20 تا 200 کیلوگرم باشد"
        }

        if (this.age < 72 && this.age > 12) {
            this.ageE = false
            this.ageEM = ''
        } else {
            this.ageE = true
            this.ageEM = "سن باید عددی بین 12 تا 72 سال باشد"
        }

        if (this.height < 230 && this.height > 100) {
            this.heightE = false
            this.heightEM = ''
        } else {
            this.heightE = true
            this.heightEM = "قد باید عددی بین 100 تا 230 سانتی متر باشد"
        }
    },
}
}
</script>

<style scoped>
#Section4 {
    margin-top: 130px;
    text-align: center;
    margin-bottom: 30px;
    background-color: white;
    padding: 30px;
    position: relative;
    border-radius: 20% 20% 25px 25px;
}
.img img {
    width: 130px;
    position: absolute;
    top: -80px;
    right: 35%;
}
.text {
    margin-top: 25px;
}
.img img {
    width: 130px;
}
.circle {
    display: flex;
    justify-content:space-between;
    position: relative;
    padding: 0 60px;
    margin-bottom: 30px;
}
.circle span {
    padding: 5px 12px;
    background-color: #edf1fa;
    color: gray;
    border-radius: 50%;
}
#active {
    z-index: 4;
    background-color:hsl(262.4, 44.4%, 56.3%);
    color: white;
}
.circle ::after {
    content: '';
    position: absolute;
    left: 37%;
    top: 50%;
    width: 25%;
    height: 0;
    border-top: 4px dotted rgba(157, 170, 198, 0.5);
    z-index: -1;
}
.form-check-input:checked {
    background-color: hsl(262.4, 44.4%, 56.3%);
    background-image: none !important;
    border: none;
}
.input {
    margin-top: 30px;
    width: 100%;
    display: flex;
    justify-content: center;
}
.inp1 {
    margin-left: 20px;
}
label {
    margin-right: 5px;
}
form {
    margin-bottom: 90px;
}
.btn {
    padding: 10px 70px;
    background-color: hsl(120, 45.8%, 47.1%);
    border: none;
    border-radius: 10px;
    color: white;
    font-size: 17px;
}
input {
    border: 1px solid hsl(262.4, 44.4%, 56.3%);
    outline: none;
}
.input-group {
    display: -webkit-box;
    /* display: flex; */
    -webkit-box-align: center;
    align-items: center;
    margin-bottom: 20px;
}
.input-group {
    position: relative;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -ms-flex-wrap: wrap;
    flex-wrap: wrap;
    -webkit-box-align: stretch;
    -ms-flex-align: stretch;
    align-items: stretch;
    width: 100%;
}

div {
    display: block;
}
.register-wrapper .inner form {
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-flow: column;
    height: 100%;
    -webkit-box-flex: 1;
    flex: auto;
}
.register-wrapper .inner {
    padding-top: 10px;
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-flow: column;
    min-height: 410px;
}
.register-wrapper {
    max-width: 450px;
    position: relative;
    border-radius: 100px 100px 15px 15px;
    text-align: center;
    padding: 50px 15px 1px 15px;
}
.panel {
    background: white;
    border: 1px solid #E5EBF8;
    box-sizing: border-box;
    border-radius: 15px;
    text-align: right;
}
#container-toggle {
    width: 100%;
    height: 40px;
    /* margin: auto; */
    position: relative;
    border-radius: 6px;
    overflow: hidden;
    user-select: none;
    cursor: pointer;
}
.register-wrapper .inner form {
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-flow: column;
    height: 100%;
    -webkit-box-flex: 1;
    flex: auto;
}
.register-wrapper .inner {
    padding-top: 10px;
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-flow: column;
    min-height: 410px;
}
.register-wrapper {
    max-width: 450px;
    position: relative;
    border-radius: 100px 100px 15px 15px;
    text-align: center;
    padding: 50px 15px 1px 15px;
}
.panel {
    background: white;
    border: 1px solid #E5EBF8;
    box-sizing: border-box;
    border-radius: 15px;
    text-align: right;
}
.inner-container-toggle {
    position: absolute;
    left: 0;
    top: 0;
    width: inherit;
    height: inherit;
    text-transform: uppercase;
    font-size: 13px;
}
#container-toggle {
    width: 100%;
    height: 40px;
    /* margin: auto; */
    position: relative;
    border-radius: 6px;
    overflow: hidden;
    user-select: none;
    cursor: pointer;
}
.register-wrapper .inner form {
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-flow: column;
    height: 100%;
    -webkit-box-flex: 1;
    flex: auto;
}
.register-wrapper .inner {
    padding-top: 10px;
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-flow: column;
    min-height: 410px;
}
.register-wrapper {
    max-width: 450px;
    position: relative;
    border-radius: 100px 100px 15px 15px;
    text-align: center;
    padding: 50px 15px 1px 15px;
}
.panel {
    background: white;
    border: 1px solid #E5EBF8;
    box-sizing: border-box;
    border-radius: 15px;
    text-align: right;
}

.inner-container-toggle .toggle {
    width: 50%;
    position: absolute;
    height: inherit;
    display: flex;
    box-sizing: border-box;
    cursor: pointer;
}
.inner-container-toggle:first-child {
    background: #EDF1FA;
    color: #8f8f8f;
}
.inner-container-toggle {
    position: absolute;
    left: 0;
    top: 0;
    width: inherit;
    height: inherit;
    text-transform: uppercase;
    font-size: 13px;
}
#container-toggle {
    width: 100%;
    height: 40px;
    /* margin: auto; */
    position: relative;
    border-radius: 6px;
    overflow: hidden;
    user-select: none;
    cursor: pointer;
}
.register-wrapper .inner form {
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-flow: column;
    height: 100%;
    -webkit-box-flex: 1;
    flex: auto;
}
.register-wrapper .inner {
    padding-top: 10px;
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-flow: column;
    min-height: 410px;
}
.register-wrapper {
    max-width: 450px;
    position: relative;
    border-radius: 100px 100px 15px 15px;
    text-align: center;
    padding: 50px 15px 1px 15px;
}
.panel {
    background: white;
    border: 1px solid #E5EBF8;
    box-sizing: border-box;
    border-radius: 15px;
    text-align: right;
}
body {
    direction: rtl;
    text-align: right;
    cursor: default;
    font-size: 16px;
    font-family: YekanBakh, sans-serif;
    background-color: #f5f8fc;
    color: #53576B;
}
body {
    margin: 0;
    font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol";
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.5;
    color: #212529;
    text-align: left;
    background-color: #fff;
}
.inner-container-toggle input {
    display: none;
}
input[type=checkbox], input[type=radio] {
    box-sizing: border-box;
    padding: 0;
}
button, input {
    overflow: visible;
}
button, input, optgroup, select, textarea {
    margin: 0;
    font-family: inherit;
    font-size: inherit;
    line-height: inherit;
}
*, ::after, ::before {
    box-sizing: border-box;
}
user agent stylesheet
input[type="radio" i] {
    background-color: initial;
    cursor: default;
    appearance: auto;
    box-sizing: border-box;
    margin: 3px 3px 0px 5px;
    padding: initial;
    border: initial;
}
user agent stylesheet
input {
    writing-mode: horizontal-tb !important;
    text-rendering: auto;
    color: -internal-light-dark(black, white);
    letter-spacing: normal;
    word-spacing: normal;
    line-height: normal;
    text-transform: none;
    text-indent: 0px;
    text-shadow: none;
    display: inline-block;
    text-align: start;
    appearance: auto;
    -webkit-rtl-ordering: logical;
    cursor: text;
    background-color: -internal-light-dark(rgb(255, 255, 255), rgb(59, 59, 59));
    margin: 0em;
    padding: 1px 2px;
    border-width: 2px;
    border-style: inset;
    border-color: -internal-light-dark(rgb(118, 118, 118), rgb(133, 133, 133));
    border-image: initial;
}
.inner-container-toggle .toggle {
    width: 50%;
    position: absolute;
    height: inherit;
    display: flex;
    box-sizing: border-box;
    cursor: pointer;
}
.inner-container-toggle:first-child {
    background: #EDF1FA;
    color: #8f8f8f;
}
.inner-container-toggle {
    position: absolute;
    left: 0;
    top: 0;
    width: inherit;
    height: inherit;
    text-transform: uppercase;
    font-size: 13px;
}
#container-toggle {
    width: 100%;
    height: 40px;
    /* margin: auto; */
    position: relative;
    border-radius: 6px;
    overflow: hidden;
    user-select: none;
    cursor: pointer;
}
.register-wrapper .inner form {
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-flow: column;
    height: 100%;
    -webkit-box-flex: 1;
    flex: auto;
}
.register-wrapper .inner {
    padding-top: 10px;
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-flow: column;
    min-height: 410px;
}
.register-wrapper {
    max-width: 450px;
    position: relative;
    border-radius: 100px 100px 15px 15px;
    text-align: center;
    padding: 50px 15px 1px 15px;
}
.panel {
    background: white;
    border: 1px solid #E5EBF8;
    box-sizing: border-box;
    border-radius: 15px;
    text-align: right;
}
.inner-container-toggle input[type="radio"]:checked+label {
    background: #835ec1;
    color: #fff;
    transition: .3s cubic-bezier(0,0,0,1);
}
.input-group label {
    margin: 0;
    cursor: pointer;
}
.inner-container-toggle label {
    flex-grow: 1;
    text-align: center;
    display: block;
    line-height: 40px;
    cursor: pointer;
    font-size: 14px;
    font-weight: 500;
}
label {
    display: inline-block;
    margin-bottom: 0.5rem;
}
*, ::after, ::before {
    box-sizing: border-box;
}
user agent stylesheet
label {
    cursor: default;
}
.inner-container-toggle .toggle {
    width: 50%;
    position: absolute;
    height: inherit;
    display: flex;
    box-sizing: border-box;
    cursor: pointer;
}
.inner-container-toggle:first-child {
    background: #EDF1FA;
    color: #8f8f8f;
}
.inner-container-toggle {
    position: absolute;
    left: 0;
    top: 0;
    width: inherit;
    height: inherit;
    text-transform: uppercase;
    font-size: 13px;
}
#container-toggle {
    width: 100%;
    height: 40px;
    /* margin: auto; */
    position: relative;
    border-radius: 6px;
    overflow: hidden;
    user-select: none;
    cursor: pointer;
}
.register-wrapper .inner form {
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-flow: column;
    height: 100%;
    -webkit-box-flex: 1;
    flex: auto;
}
.register-wrapper .inner {
    padding-top: 10px;
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-flow: column;
    min-height: 410px;
}
.register-wrapper {
    max-width: 450px;
    position: relative;
    border-radius: 100px 100px 15px 15px;
    text-align: center;
    padding: 50px 15px 1px 15px;
}
.panel {
    background: white;
    border: 1px solid #E5EBF8;
    box-sizing: border-box;
    border-radius: 15px;
    text-align: right;
}
.inner-container-toggle .toggle:nth-child(2) {
    left: 0;
}
.inner-container-toggle .toggle {
    width: 50%;
    position: absolute;
    height: inherit;
    display: flex;
    box-sizing: border-box;
    cursor: pointer;
}
*, ::after, ::before {
    box-sizing: border-box;
}
user agent stylesheet
div {
    display: block;
}
.inner-container-toggle:first-child {
    background: #EDF1FA;
    color: #8f8f8f;
}
.inner-container-toggle {
    position: absolute;
    left: 0;
    top: 0;
    width: inherit;
    height: inherit;
    text-transform: uppercase;
    font-size: 13px;
}
#container-toggle {
    width: 100%;
    height: 40px;
    /* margin: auto; */
    position: relative;
    border-radius: 6px;
    overflow: hidden;
    user-select: none;
    cursor: pointer;
}
.register-wrapper .inner form {
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-flow: column;
    height: 100%;
    -webkit-box-flex: 1;
    flex: auto;
}
.register-wrapper .inner {
    padding-top: 10px;
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-flow: column;
    min-height: 410px;
}
.register-wrapper {
    max-width: 450px;
    position: relative;
    border-radius: 100px 100px 15px 15px;
    text-align: center;
    padding: 50px 15px 1px 15px;
}
.panel {
    background: white;
    border: 1px solid #E5EBF8;
    box-sizing: border-box;
    border-radius: 15px;
    text-align: right;
}
body {
    direction: rtl;
    text-align: right;
    cursor: default;
    font-size: 16px;
    font-family: YekanBakh, sans-serif;
    background-color: #f5f8fc;
    color: #53576B;
}
body {
    margin: 0;
    font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol";
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.5;
    color: #212529;
    text-align: left;
    background-color: #fff;
}
.inner-container-toggle input {
    display: none;
}
input[type=checkbox], input[type=radio] {
    box-sizing: border-box;
    padding: 0;
}
button, input {
    overflow: visible;
}
button, input, optgroup, select, textarea {
    margin: 0;
    font-family: inherit;
    font-size: inherit;
    line-height: inherit;
}
*, ::after, ::before {
    box-sizing: border-box;
}
user agent stylesheet
input[type="radio" i] {
    background-color: initial;
    cursor: default;
    appearance: auto;
    box-sizing: border-box;
    margin: 3px 3px 0px 5px;
    padding: initial;
    border: initial;
}
user agent stylesheet
input {
    writing-mode: horizontal-tb !important;
    text-rendering: auto;
    color: -internal-light-dark(black, white);
    letter-spacing: normal;
    word-spacing: normal;
    line-height: normal;
    text-transform: none;
    text-indent: 0px;
    text-shadow: none;
    display: inline-block;
    text-align: start;
    appearance: auto;
    -webkit-rtl-ordering: logical;
    cursor: text;
    background-color: -internal-light-dark(rgb(255, 255, 255), rgb(59, 59, 59));
    margin: 0em;
    padding: 1px 2px;
    border-width: 2px;
    border-style: inset;
    border-color: -internal-light-dark(rgb(118, 118, 118), rgb(133, 133, 133));
    border-image: initial;
}
.inner-container-toggle .toggle {
    width: 50%;
    position: absolute;
    height: inherit;
    display: flex;
    box-sizing: border-box;
    cursor: pointer;
}
.inner-container-toggle:first-child {
    background: #EDF1FA;
    color: #8f8f8f;
}
.inner-container-toggle {
    position: absolute;
    left: 0;
    top: 0;
    width: inherit;
    height: inherit;
    text-transform: uppercase;
    font-size: 13px;
}
#container-toggle {
    width: 100%;
    height: 40px;
    /* margin: auto; */
    position: relative;
    border-radius: 6px;
    overflow: hidden;
    user-select: none;
    cursor: pointer;
}
.register-wrapper .inner form {
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-flow: column;
    height: 100%;
    -webkit-box-flex: 1;
    flex: auto;
}
.register-wrapper .inner {
    padding-top: 10px;
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-flow: column;
    min-height: 410px;
}
.register-wrapper {
    max-width: 450px;
    position: relative;
    border-radius: 100px 100px 15px 15px;
    text-align: center;
    padding: 50px 15px 1px 15px;
}
.panel {
    background: white;
    border: 1px solid #E5EBF8;
    box-sizing: border-box;
    border-radius: 15px;
    text-align: right;
}
body {
    direction: rtl;
    text-align: right;
    cursor: default;
    font-size: 16px;
    font-family: YekanBakh, sans-serif;
    background-color: #f5f8fc;
    color: #53576B;
}
body {
    margin: 0;
    font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol";
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.5;
    color: #212529;
    text-align: left;
    background-color: #fff;
}
.input-group label {
    margin: 0;
    cursor: pointer;
}
.inner-container-toggle label {
    flex-grow: 1;
    text-align: center;
    display: block;
    line-height: 40px;
    cursor: pointer;
    font-size: 14px;
    font-weight: 500;
}
label {
    display: inline-block;
    margin-bottom: 0.5rem;
}
*, ::after, ::before {
    box-sizing: border-box;
}
user agent stylesheet
label {
    cursor: default;
}
.inner-container-toggle .toggle {
    width: 50%;
    position: absolute;
    height: inherit;
    display: flex;
    box-sizing: border-box;
    cursor: pointer;
}
.inner-container-toggle:first-child {
    background: #EDF1FA;
    color: #8f8f8f;
}
.inner-container-toggle {
    position: absolute;
    left: 0;
    top: 0;
    width: inherit;
    height: inherit;
    text-transform: uppercase;
    font-size: 13px;
}
#container-toggle {
    width: 100%;
    height: 40px;
    /* margin: auto; */
    position: relative;
    border-radius: 6px;
    overflow: hidden;
    user-select: none;
    cursor: pointer;
}
.register-wrapper .inner form {
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-flow: column;
    height: 100%;
    -webkit-box-flex: 1;
    flex: auto;
}
.register-wrapper .inner {
    padding-top: 10px;
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-flow: column;
    min-height: 410px;
}
.register-wrapper {
    max-width: 450px;
    position: relative;
    border-radius: 100px 100px 15px 15px;
    text-align: center;
    padding: 50px 15px 1px 15px;
}
.panel {
    background: white;
    border: 1px solid #E5EBF8;
    box-sizing: border-box;
    border-radius: 15px;
    text-align: right;
}
body {
    direction: rtl;
    text-align: right;
    cursor: default;
    font-size: 16px;
    font-family: YekanBakh, sans-serif;
    background-color: #f5f8fc;
    color: #53576B;
}
body {
    margin: 0;
    font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol";
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.5;
    color: #212529;
    text-align: left;
    background-color: #fff;
}
 </style>