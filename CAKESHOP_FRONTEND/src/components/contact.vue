<template>
    <body>
        <div class="container">
            <div class="text-center">
                <h1>Liên hệ</h1>
            </div>
            <div class="row mt-5">
                <div class="col-md-6">
                    <h3 class="title">Thông tin liên hệ</h3>
                    <form @submit.prevent="saveTT" ref="myForm">
                        <div class="form-group">
                            <label for="name">Họ và tên:</label>
                            <input type="text" class="form-control bgColor" v-model="name" id="name" required>
                        </div>
                        <div class="form-group my-3">
                            <label for="email">Email:</label>
                            <input type="email" class="form-control bgColor" v-model="email" id="email" required>
                        </div>
                        <div class="form-group">
                                <label for="phone">Số điện thoại:</label>
                                <input type="phone" class="form-control bgColor " v-model="phone" id="phone" required>
                            </div>
                        <div class="form-group my-3">
                            <label for="message">Nội dung:</label>
                            <textarea class="form-control bgColor" id="message" v-model="content" rows="5" required></textarea>
                        </div>
                        <div class="text-center">
                            <button type="submit"
                                class="btn btn-outline-primary mt-5 mb-5 justify-content-center">Gửi</button>
                        </div>

                    </form>
                </div>
                <div class="col-md-6 ">
                    <h1 class="title">Công ty TNHH NTH</h1>
                    <div>
                        <p>Đ.3/2, P.Xuân Khánh, Q.Ninh Kiều, TP Cần Thơ</p>
                        <p><span class="collig">Phone :</span> +84 12345678</p>
                        <p><span class="collig">Email :</span> cskh@freshgarden.vn</p>
                        <p><span class="collig">Hotline CSKH :</span> 19002075</p>
                    </div>
                    <div>
                        <iframe
                            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3928.8415184420483!2d105.76804037592433!3d10.029933690077037!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x31a0895a51d60719%3A0x9d76b0035f6d53d0!2zVHLGsOG7nW5nIMSQ4bqhaSBo4buNYyBD4bqnbiBUaMah!5e0!3m2!1svi!2s!4v1699971700132!5m2!1svi!2s"
                            width="100%" height="400" style="border:0;" loading="lazy"
                            referrerpolicy="no-referrer-when-downgrade"></iframe>
                    </div>
                </div>
            </div>
        </div>
    </body>
</template>
<style>
* {
    margin: 0px;
    padding: 0px;
}
</style>

<script>
    export default {
        data() {
        return {
            name: '',
            email: '',
            phone: '',
            content: ''
        };
    },
        methods: {
        saveTT() {
            if(this.$store.isLogged) {
                alert('Thông tin liên hệ đã được lưu lại');
            this.$router.push('/');
            }
            this.$refs.myForm.reset();
            alert('Hãy đăng nhập để liên hệ với chúng tôi');
            this.$router.push('/login');
        }
    }
    }
</script>