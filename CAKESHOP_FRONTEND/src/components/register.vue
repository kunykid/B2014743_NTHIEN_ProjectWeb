<template>
    <div class="login-form">
        <div class="iconbutton" @click="goToIndex($event)">
            <i class="fa-solid fa-xmark"></i>
        </div>
        <form @submit.prevent="register()">
            <div class="text-center">
                <h1>Sign Up</h1>
            </div>
            
            <div class="content">
                <ul class="ul_form">
                    <li>
                        <div class="input-field">
                            <input type="email" v-model="user.email" placeholder="Email" autocomplete="nope"
                                @blur="validate()" :class="{ 'is-invalid': errors.email }">
                            <div class="invalid-feedback" v-if="errors.email">
                                {{ errors.email }}
                            </div>
                        </div>
                    </li>
                    <li>
                        <div class="input-field">
                            <input type="text" v-model="user.name" placeholder="Họ và tên" autocomplete="nope"
                                @blur="validate()" :class="{ 'is-invalid': errors.name }">
                            <div class="invalid-feedback" v-if="errors.name">
                                {{ errors.name }}
                            </div>
                        </div>
                    </li>
                    <li>
                        <div class="input-field">
                            <input type="password" v-model="user.password" placeholder="Password"
                                autocomplete="new-password" @blur="validate()" :class="{ 'is-invalid': errors.password }">
                            <div class="invalid-feedback" v-if="errors.password">
                                {{ errors.password }}
                            </div>
                        </div>
                    </li>
                    <li>
                        <div class="input-field">
                            <input type="password" v-model="user.confirmPassword" placeholder="Confirm password"
                                @blur="validate()" :class="{ 'is-invalid': errors.confirmPassword }"
                                >
                            <div class="invalid-feedback" v-if="errors.confirmPassword">
                                {{ errors.confirmPassword }}
                            </div>
                        </div>
                    </li>
                    <li>
                        <div class="input-field">
                            <input type="text" v-model="user.address" placeholder="Địa chỉ"
                                @blur="validate()" :class="{ 'is-invalid': errors.address }"
                            >
                            <div class="invalid-feedback" v-if="errors.address">
                                {{ errors.address }}
                            </div>
                        </div>
                    </li>
                    <li>
                        <div class="input-field">
                            <input type="text" v-model="user.phoneNumber" placeholder="Số điện thoại"
                                @blur="validate()" :class="{ 'is-invalid': errors.phoneNumber }"
                            >
                            <div class="invalid-feedback" v-if="errors.phoneNumber">
                                {{ errors.phoneNumber }}
                            </div>
                        </div>
                    </li>
                    <li><a href="#" class="link">Forgot Your Password?</a></li>
                </ul>
            </div>
            <div class="action">
                <button type="submit">Đăng ký</button>
            </div>
        </form>
        <div class="action2">
            <button @click="goToLogin($event)">Đăng nhập</button>
        </div>
    </div>
</template>
  
<script>
import UserService from "../services/user.service";
export default {
    data() {
        return {
            errors: {
                email: "",
                name: "",
                password: "",
                confirmPassword: "",
                address: "",
                phoneNumber: "",
            },
            user: {
                email: "",
                name: "",
                password: "",
                confirmPassword: "",
                address: "",
                phoneNumber: "",
            },
        }
    },
    methods: {
        validate() {
            let isValid = true;

            this.errors = {
                email: "",
                password: "",
                confirmPassword: "",
            };
            if (!this.user.email) {
                this.errors.email = "Email là bắt buộc";
                isValid = false;
            }
            if (!this.user.name) {
                this.errors.name = "Họ và tên là bắt buộc";
                isValid = false;
            }
            if (!this.user.password) {
                this.errors.password = "Mật khẩu là bắt buộc";
                isValid = false;
            }
            if (this.user.confirmPassword != this.user.password) {
                this.errors.confirmPassword = "Mật khẩu chưa đúng";
                isValid = false;
            }
            if(!this.user.address){
                this.errors.address = "Địa chỉ là bắt buộc";
                isValid = false;
            }
            if( !this.user.phoneNumber){
                this.errors.phoneNumber = "Số điện thoại là bắt buộc";
                isValid = false;
            }
            return isValid;
        },
        // goToRegister() {
        //     this.$router.push('/register');
        // },
        goToLogin(event) {
            event.preventDefault();
            this.$router.push('/login');
        },
        goToIndex(event) {
            event.preventDefault();
            this.$router.push('/');
        },
        async register() {
            if (this.validate()) {
                try {
                    await UserService.create(this.user);
                    alert(
                        `Chúc mừng ${this.user.name} !!! Bạn đã đăng ký tài khoản thành công!`
                    );
                    this.$router.push({ name: "login" });
                } catch (error) {
                    console.log(error);
                }
            }
        },
    }
};
</script>
  

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    -webkit-font-smoothing: antialiased;
}

body {
    /* background: #e35869; */
    font-family: 'Rubik', sans-serif;
}

.invalid-feedback {
    text-align: left;
    color: red;
    margin-top: 5px;
}

.login-form {
    position: relative;
    background: #fff;
    top: 0;
    right: 0;
    width: 500px;
    margin: 65px auto;
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-direction: column;
    border-radius: 4px;
    box-shadow: 0 2px 25px rgba(0, 0, 0, 0.2);
}

.login-form .iconbutton {
    font-size: 25px;
    position: absolute;
    top: 0;
    right: 0;
    margin: 10px;
}

.login-form h1 {
    padding: 35px 35px 0 35px;
    font-weight: 300;
}

.login-form .content {
    padding: 35px;
    text-align: center;
}

.login-form .input-field {
    padding: 12px 5px;
}

.login-form .input-field input {
    font-size: 16px;
    display: block;
    font-family: 'Rubik', sans-serif;
    width: 420px;
    padding: 10px 1px;
    border: 0;
    border-bottom: 1px solid #747474;
    outline: none;
    -webkit-transition: all .2s;
    transition: all .2s;
}

.login-form .input-field input::-webkit-input-placeholder {
    text-transform: uppercase;
}

.login-form .input-field input::-moz-placeholder {
    text-transform: uppercase;
}

.login-form .input-field input:-ms-input-placeholder {
    text-transform: uppercase;
}

.login-form .input-field input::-ms-input-placeholder {
    text-transform: uppercase;
}

.login-form .input-field input::placeholder {
    text-transform: uppercase;
}

.login-form .input-field input:focus {
    border-color: #222;
}

.login-form a.link {
    text-decoration: none;
    color: #747474;
    letter-spacing: 0.2px;
    text-transform: uppercase;
    display: inline-block;
    margin-top: 20px;
}

.login-form .action {
    display: -webkit-box;
    display: flex;
    text-align: center;
    -webkit-box-orient: horizontal;
    -webkit-box-direction: normal;
    flex-direction: column;
}

.login-form .action button {
    width: 100%;
    border: none;
    padding: 18px;
    font-family: 'Rubik', sans-serif;
    cursor: pointer;
    text-transform: uppercase;
    background: #e8e9ec;
    color: #777;
    border-bottom-left-radius: 4px;
    border-bottom-right-radius: 0;
    letter-spacing: 0.2px;
    outline: 0;
    -webkit-transition: all .3s;
    transition: all .3s;
}

.login-form .action button:hover {
    background: #d8d8d8;
}

.login-form .action2 button {
    margin-top: 10px;
    width: 100%;
    border: none;
    padding: 18px;
    font-family: 'Rubik', sans-serif;
    cursor: pointer;
    text-transform: uppercase;
    background: #fff;
    color: #1976d2;
    letter-spacing: 0.2px;
    outline: 0;
}

.login-form .action2 button:hover {
    background-color: #d8d8d8;
}


.ul_form {
    list-style-type: none;
    /* Loại bỏ dấu chấm đầu */
    padding-left: 0;
    /* Loại bỏ khoảng cách trái của danh sách */
}
</style>