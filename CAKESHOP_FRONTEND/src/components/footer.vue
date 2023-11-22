<template>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css">
    <div class="container-fluid bg-dark text-white">
        <div class="row">
            <div class="col-lg-3 col-md-6 col-sm-6">
            <h3>Fresh Garden</h3>
               <ul class="listItem">
                <router-link :to="{ name: 'about' }"><li><a>Giới thiệu</a></li></router-link>
                <router-link :to="{ name: 'products' }"><li><a>Cửa hàng</a></li></router-link>
                <router-link :to="{ name: 'contact' }"><li><a>Liên Hệ</a></li></router-link>
                <li @click="scrollToTop()"><a>Về đầu trang</a></li>
               </ul>
            </div>
            <div class="col-lg-3 col-md-6 col-sm-6">
            <h3>Kết nối với chúng tôi</h3>
            <div class="socials">
                    <a href="#"><i class="fa fa-facebook"></i></a>
                    <a href="#"><i class="fa fa-twitter"></i></a>
                    <a href="#"><i class="fa fa-google-plus"></i></a>
                    <a href="#"><i class="fa fa-youtube"></i></a>
                    <a href="#"><i class="fa fa-linkedin-square"></i></a>
                </div>
            </div>
            <div class="col-lg-3 col-md-6 col-sm-6">
                <h3>Chính sách</h3>
                <ul class="listItem">
                    <li><a href="#">Hướng dẫn mua hàng</a></li>
                    <li><a href="#">Chính sách vận chuyển</a></li>
                    <li><a href="#">Chính sách đổi trả</a></li>
                    <li><a href="#">Chính sách an toàn thực phẩm</a></li>
                    <li><a href="#">Điều khoản sử dụng</a></li>
                </ul>
            </div>
            <div class="col-lg-3 col-md-6 col-sm-6">
                <h3>Thông tin cửa hàng</h3>
                <ul class="listItem">
                    <li><a href="#"><i class="fa-solid fa-location-dot"></i>Khu 2, Đ.3/2</a></li>
                    <li><a href="#"><i class="fa-solid fa-address-card"></i> P.Xuân Khánh, Q.Ninh Kiều, TP.CT</a></li>
                    <li><a href="#"><i class="fa-solid fa-square-phone-flip"></i> Hotline: 098***142**</a></li>
                    <li><a href="#"><i class="fa-solid fa-envelope"></i>hienb2014743@student.ctu.edu.vn</a> </li>
                </ul>
            </div>
        </div>
    </div>
    <div class="container-fluid bg-dark text-white footer-content">
         <p>Copyright &copy;2023 Freshgarden.vn</p>
    </div>

</template>
<script>
    export default{
        methods: {
            scrollToTop() {
                 window.scrollTo({
                top: 0,
                behavior: "smooth" // Để có hiệu ứng cuộn mượt
            });
            }
        }
    }
</script>
<style media="screen">

.footer-content {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    text-align: center;
}

/* .footer-content h3 {
    font-size: 2.1rem;
    font-weight: 500;
    text-transform: capitalize;
    line-height: 3rem;
} */

.footer-content p {
    max-width: 500px;
    margin: 10px auto;
    line-height: 28px;
    font-size: 14px;
    color: #cacdd2;
}

.socials {
    list-style: none;
    display: flex;
    padding: 10px;
}


.socials a {
    text-decoration: none;
    color: #fff;
    border: 1.1px solid white;
    padding: 5px;
    border-radius: 50%;
    margin: 0 5px;
}

.socials a i {
    font-size: 1.1rem;
    width: 20px;
    transition: color .4s ease;
}

.socials a:hover i {
    color: aqua;
}
.listItem li:hover a {
    color: aqua;
}

.footer-bottom {
    background: #000;
    width: 100vw;
    padding: 20px;
    padding-bottom: 40px;
    text-align: center;
}

.footer-bottom p {
    float: left;
    font-size: 14px;
    word-spacing: 2px;
    text-transform: capitalize;
}

.footer-bottom p a {
    color: #44bae8;
    font-size: 16px;
    text-decoration: none;
}

.footer-bottom span {
    text-transform: uppercase;
    opacity: .4;
    font-weight: 200;
}

.footer-menu {
    float: right;

}

.footer-menu ul {
    display: flex;
}

.footer-menu ul li {
    padding-right: 10px;
    display: block;
}

.footer-menu ul li a {
    color: #cfd2d6;
    text-decoration: none;
}

.footer-menu ul li a:hover {
    color: #27bcda;
}

@media (max-width:500px) {
    .footer-menu ul {
        display: flex;
        margin-top: 10px;
        margin-bottom: 20px;
    }
}
</style>
