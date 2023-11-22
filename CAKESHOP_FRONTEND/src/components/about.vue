<template>
    <!-- <p class="text-blk headingText">
        About Us
    </p> -->
    <h1 class="text-dark text-center">Giới thiệu</h1>
    <div class="responsive-container-block bigContainer">
        <div class="responsive-container-block Container bottomContainer">
            <div class="ultimateImg">
                    <p class="text-blk subHeadingText">
                        Những giá trị tạo nên Fresh Garden
                    </p>
                    <p class="text-blk description">
                        Từng sản phẩm Fresh Garden được đầu tư rất kỹ ngay từ khâu chọn nguyên liệu, đó là những thành phần tươi mới nhất và chủ yếu đang sử dụng đều đến từ những nhãn hiệu có uy tín như Anchor, Vivo, Meiji, Komplet… Một số dòng sốt của Ý như sốt pizza, sốt mayonaise cũng được nhập trực tiếp từ Ý.
                    </p>
                    <img class="mainImg" src="https://theme.hstatic.net/200000411281/1000949882/14/home_slider_image_2.jpg?v=260">

                    <p class="text-blk subHeadingText">
                        Dấu ấn hành trình
                        </p>
                        <p class="text-blk description">Với hơn 100 cửa hàng và đại lý phân phối phủ khắp các tỉnh phía Bắc, Fresh Garden tự hào là thương hiệu bánh tươi uy tín bậc nhất với dây chuyền sản xuất tiên tiến hiện đại cùng gần 1000 nhân sự làm việc chăm chỉ không ngừng sáng tạo. Với tín đồ của bánh ngọt, mặn, bánh kem thì thật sự Fresh Garden chính là một "thế giới thu nhỏ" của bánh trái, chiều lòng bất kì vị khách nào ghé ngang. Trải qua một thập kỷ với những cung bậc sáng tạo, Fresh Garden không chỉ ghi dấu bởi chất lượng mà còn vì sự tinh tế trong từng nấc hương vị, đa dạng bánh Âu, Á và dần trở thành thói quen trong văn hóa tiêu dùng của những tín đồ yêu bánh.
                        </p>
                        <p class="text-blk description">
                        Thế mạnh của Fresh Garden nằm ở những dòng bánh kem tươi mềm mịn ngọt dịu tươi mới, bánh mì nướng đặc biệt giòn thơm, bánh cuộn chuẩn Nhật với lớp kem sữa Hokkaido… rất được ưa chuộng. Trong mỗi dịp lễ hay sinh nhật, bánh kem của Fresh Garden luôn là một lựa chọn hàng đầu, bởi độ ngọt vừa phải, mẫu bánh đẹp, giá thành hợp lý. Bên cạnh đó, đồng hành với khách hàng mỗi ngày là các sản phẩm bánh mì tươi – bánh mỳ kẹp tiện lợi, dinh dưỡng.</p>
                            <img src="https://file.hstatic.net/200000411281/file/banh-gato-fresh-garden-min_24ddfc8a20c84fc48d6413b8b2e0b370_grande.jpg" alt="m2">

                        <p class="text-blk subHeadingText">Sứ mệnh và tầm nhìn</p>
                        <p class="text-blk description">
                            Đằng sau Fresh Garden là đội ngũ nhân viên, chuyên gia đầu bếp luôn nỗ lực sáng tạo, không ngừng đam mê để có thể đưa ra những sản phẩm ngon, chất lượng, đẹp mắt và an toàn cho sức khỏe khách hàng. Đi cùng quy trình làm bánh nghiêm ngặt, khép kín, đòi hỏi nhân viên phải cẩn thận, tỉ mỉ và chăm chút trong từng công đoạn nhỏ nhất. Fresh Garden cam kết mang đến những sản phẩm đạt chất lượng cao nhất như một lời tri ân đối với sự yêu mến và tin dùng.
                        </p>
                        <img src="https://file.hstatic.net/200000411281/file/banh-my-tuoi-fresh-garden-min_aa5a4a7dbb9246f2a277f13ee2213858_grande.jpg" alt="m3">
            </div>
            <!-- <div class="allText bottomText">
                <p class="text-blk subHeadingText">
                    Những giá trị tạo nên Fresh Garden
                </p>
                <p class="text-blk description">
                    Từng sản phẩm Fresh Garden được đầu tư rất kỹ ngay từ khâu chọn nguyên liệu, đó là những thành phần tươi mới nhất và chủ yếu đang sử dụng đều đến từ những nhãn hiệu có uy tín như Anchor, Vivo, Meiji, Komplet… Một số dòng sốt của Ý như sốt pizza, sốt mayonaise cũng được nhập trực tiếp từ Ý.
                </p>
                <router-link :to="{ name: 'products' }"><a class="explore">
                    Cửa hàng
                </a></router-link>
            </div> -->
            
        </div>
    </div>
    <div class="scrollButton">
                    <router-link :to="{ name: 'products' }"><a class="explore">
                        Cửa hàng
                    </a></router-link>
                </div>
</template>
<script>
window.addEventListener('scroll', function () {
    var scrollButton = document.getElementById('scrollButton');

    if (window.scrollY > 0) {
        scrollButton.style.display = 'block';
    } else {
        scrollButton.style.display = 'none';
    }
});
</script>
<style>
* {
    font-family: Nunito, sans-serif;
}

.scrollButton{
    position: fixed;
    top: 50%;
    right:0;
    transform: translate(-50%, 0);
}

.responsive-container-block {
    min-height: 75px;
    height: fit-content;
    width: 100%;
    padding-top: 10px;
    padding-right: 10px;
    padding-bottom: 10px;
    padding-left: 10px;
    display: flex;
    flex-wrap: wrap;
    margin-top: 0px;
    margin-right: auto;
    margin-bottom: 0px;
    margin-left: auto;
    justify-content: flex-start;
}

a {
    text-decoration-line: none;
    text-decoration-thickness: initial;
    text-decoration-style: initial;
    text-decoration-color: initial;
}

.text-blk {
    margin-top: 0px;
    margin-right: 0px;
    margin-bottom: 0px;
    margin-left: 0px;
    padding-top: 10px;
    padding-right: 10px;
    padding-bottom: 10px;
    padding-left: 10px;
    line-height: 25px;
}

.responsive-container-block.bigContainer {
    padding-top: 10px;
    padding-right: 30px;
    padding-bottom: 10px;
    padding-left: 30px;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 10px 50px 10px 50px;
}

.mainImg {
    color: black;
    width: 100%;
    height: auto;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
    border-bottom-right-radius: 10px;
    border-bottom-left-radius: 10px;
}

.text-blk.headingText {
    font-size: 22px;
    font-weight: 700;
    line-height: 30px;
    color: rgb(176, 98, 255);
    padding-top: 0px;
    padding-right: 10px;
    padding-bottom: 0px;
    padding-left: 0px;
    margin-top: 0px;
    margin-right: 0px;
    margin-bottom: 5px;
    margin-left: 0px;
}

.allText {
    padding-top: 0px;
    padding-right: 0px;
    padding-bottom: 0px;
    padding-left: 0px;
    width: 40%;
    margin-top: 0px;
    margin-right: 0px;
    margin-bottom: 0px;
    margin-left: 0px;
}

.text-blk.subHeadingText {
    color: rgb(102, 102, 102);
    font-size: 26px;
    line-height: 32px;
    font-weight: 700;
    margin-top: 0px;
    margin-right: 0px;
    margin-bottom: 15px;
    margin-left: 0px;
    padding-top: 0px;
    padding-right: 10px;
    padding-bottom: 0px;
    padding-left: 0px;
}

.text-blk.description {
    font-size: 18px;
    line-height: 26px;
    color: rgb(102, 102, 102);
    margin-top: 0px;
    margin-right: 0px;
    margin-bottom: 50px;
    margin-left: 0px;
    font-weight: 400;
    padding-top: 0px;
    padding-right: 10px;
    padding-bottom: 0px;
    padding-left: 0px;
}

.explore {
    font-size: 16px;
    line-height: 28px;
    color: rgb(102, 102, 102);
    border-top-width: 2px;
    border-right-width: 2px;
    border-bottom-width: 2px;
    border-left-width: 2px;
    border-top-style: solid;
    border-right-style: solid;
    border-bottom-style: solid;
    border-left-style: solid;
    border-top-color: rgb(102, 102, 102);
    border-right-color: rgb(102, 102, 102);
    border-bottom-color: rgb(102, 102, 102);
    border-left-color: rgb(102, 102, 102);
    border-image-source: initial;
    border-image-slice: initial;
    border-image-width: initial;
    border-image-outset: initial;
    border-image-repeat: initial;
    cursor: pointer;
    background-color: white;
    margin-top: 0px;
    margin-right: 0px;
    margin-bottom: 0px;
    margin-left: 0px;
    padding-top: 8px;
    padding-right: 40px;
    padding-bottom: 8px;
    padding-left: 40px;
}

.explore:hover {
    background-image: initial;
    background-position-x: initial;
    background-position-y: initial;
    background-size: initial;
    background-repeat-x: initial;
    background-repeat-y: initial;
    background-attachment: initial;
    background-origin: initial;
    background-clip: initial;
    background-color: #2b2d42;
    color: white;
    border-top-width: initial;
    border-right-width: initial;
    border-bottom-width: initial;
    border-left-width: initial;
    border-top-style: none;
    border-right-style: none;
    border-bottom-style: none;
    border-left-style: none;
    border-top-color: initial;
    border-right-color: initial;
    border-bottom-color: initial;
    border-left-color: initial;
    border-image-source: initial;
    border-image-slice: initial;
    border-image-width: initial;
    border-image-outset: initial;
    border-image-repeat: initial;
}

.responsive-container-block.Container {
    margin-top: 80px;
    margin-right: auto;
    margin-bottom: 50px;
    margin-left: auto;
    justify-content: center;
    align-items: center;
    max-width: 1320px;
    padding-top: 10px;
    padding-right: 10px;
    padding-bottom: 10px;
    padding-left: 10px;
}

.responsive-container-block.Container.bottomContainer {
    flex-direction: row-reverse;
    margin-top: 80px;
    margin-right: auto;
    margin-bottom: 50px;
    margin-left: auto;
    position: static;
}

.allText.aboveText {
    margin-top: 0px;
    margin-right: 0px;
    margin-bottom: 0px;
    margin-left: 40px;
}

.allText.bottomText {
    margin-top: 0px;
    margin-right: 40px;
    margin-bottom: 0px;
    margin-left: 0px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    padding-top: 0px;
    padding-right: 15px;
    padding-bottom: 0px;
    padding-left: 0px;
}

.purpleBox {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    max-width: 430px;
    background-color: rgb(176, 98, 255);
    padding-top: 20px;
    padding-right: 20px;
    padding-bottom: 20px;
    padding-left: 20px;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
    border-bottom-right-radius: 10px;
    border-bottom-left-radius: 10px;
    position: absolute;
    bottom: -35px;
    left: -8%;
}

.purpleText {
    font-size: 18px;
    line-height: 26px;
    color: white;
    margin-top: 0px;
    margin-right: 0px;
    margin-bottom: 10px;
    margin-left: 0px;
}

.ultimateImg {
    position: relative;
}

@media (max-width: 1024px) {
    .responsive-container-block.Container {
        max-width: 850px;
    }

    .mainImg {
        width: 55%;
        height: auto;
    }

    .allText {
        width: 40%;
        margin-top: 0px;
        margin-right: 0px;
        margin-bottom: 0px;
        margin-left: 20px;
    }

    .responsive-container-block.bigContainer {
        padding-top: 10px;
        padding-right: 10px;
        padding-bottom: 10px;
        padding-left: 10px;
    }

    .responsive-container-block.Container.bottomContainer {
        margin-top: 80px;
        margin-right: auto;
        margin-bottom: 50px;
        margin-left: auto;
    }

    .responsive-container-block.Container {
        max-width: 830px;
    }

    .allText.aboveText {
        margin-top: 30px;
        margin-right: 0px;
        margin-bottom: 0px;
        margin-left: 40px;
    }

    .allText.bottomText {
        margin-top: 30px;
        margin-right: 40px;
        margin-bottom: 0px;
        margin-left: 0px;
        text-align: left;
    }

    .text-blk.headingText {
        text-align: center;
    }

    .allText.aboveText {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        margin-top: 30px;
        margin-right: 0px;
        margin-bottom: 0px;
        margin-left: 0px;
    }

    .text-blk.subHeadingText {
        text-align: left;
        font-size: 26px;
        line-height: 32px;
    }

    .text-blk.description {
        text-align: left;
        line-height: 24px;
    }

    .explore {
        margin-top: 0px;
        margin-right: 0px;
        margin-bottom: 0px;
        margin-left: 0px;
    }

    .responsive-container-block.bigContainer {
        padding-top: 10px;
        padding-right: 30px;
        padding-bottom: 10px;
        padding-left: 30px;
    }

    .responsive-container-block.Container {
        justify-content: space-evenly;
    }

    .purpleBox {
        bottom: 10%;
    }

    .responsive-container-block.Container.bottomContainer {
        padding-top: 10px;
        padding-right: 0px;
        padding-bottom: 10px;
        padding-left: 0px;
        max-width: 930px;
    }

    .allText.bottomText {
        width: 40%;
    }

    .purpleBox {
        bottom: auto;
        left: -10%;
        top: 70%;
    }

    .mainImg {
        width: 100%;
    }

    .text-blk.headingText {
        text-align: left;
    }
}

@media (max-width: 768px) {
    .allText {
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding-top: 0px;
        padding-right: 0px;
        padding-bottom: 0px;
        padding-left: 0px;
    }

    .responsive-container-block.Container {
        flex-direction: column;
        height: auto;
    }

    .text-blk.headingText {
        text-align: center;
    }

    .text-blk.subHeadingText {
        text-align: center;
        font-size: 24px;
    }

    .text-blk.description {
        text-align: center;
        font-size: 18px;
    }

    .allText {
        margin-top: 40px;
        margin-right: 0px;
        margin-bottom: 0px;
        margin-left: 0px;
    }

    .allText.aboveText {
        margin-top: 40px;
        margin-right: 0px;
        margin-bottom: 0px;
        margin-left: 0px;
    }

    .responsive-container-block.Container {
        margin-top: 80px;
        margin-right: auto;
        margin-bottom: 50px;
        margin-left: auto;
    }

    .responsive-container-block.Container.bottomContainer {
        margin-top: 50px;
        margin-right: auto;
        margin-bottom: 50px;
        margin-left: auto;
    }

    .allText.bottomText {
        margin-top: 40px;
        margin-right: 0px;
        margin-bottom: 0px;
        margin-left: 0px;
    }

    .mainImg {
        width: 100%;
        margin-top: 0px;
        margin-right: 0px;
        margin-bottom: -70px;
        margin-left: 0px;
    }

    .responsive-container-block.Container.bottomContainer {
        flex-direction: column;
    }

    .ultimateImg {
        width: 100%;
    }

    .purpleBox {
        position: static;
    }

    .allText.bottomText {
        width: 100%;
        align-items: flex-start;
    }

    .text-blk.headingText {
        text-align: left;
    }

    .text-blk.subHeadingText {
        text-align: left;
    }

    .text-blk.description {
        text-align: left;
    }

    .ultimateImg {
        position: static;
    }

    .mainImg {
        margin-top: 0px;
        margin-right: 0px;
        margin-bottom: 0px;
        margin-left: 0px;
    }

    .ultimateImg {
        position: relative;
    }

    .purpleBox {
        margin-top: 0px;
        margin-right: 0px;
        margin-bottom: 0px;
        margin-left: 0px;
        position: absolute;
        left: 0px;
        top: 80%;
    }

    .allText.bottomText {
        margin-top: 100px;
        margin-right: 0px;
        margin-bottom: 0px;
        margin-left: 0px;
    }
}

@media (max-width: 500px) {
    .responsive-container-block.Container {
        padding-top: 10px;
        padding-right: 0px;
        padding-bottom: 10px;
        padding-left: 0px;
        width: 100%;
        max-width: 100%;
    }

    .mainImg {
        width: 100%;
    }

    .responsive-container-block.bigContainer {
        padding-top: 10px;
        padding-right: 25px;
        padding-bottom: 10px;
        padding-left: 25px;
    }

    .text-blk.subHeadingText {
        font-size: 24px;
        padding-top: 0px;
        padding-right: 0px;
        padding-bottom: 0px;
        padding-left: 0px;
        line-height: 28px;
    }

    .text-blk.description {
        font-size: 16px;
        padding-top: 0px;
        padding-right: 0px;
        padding-bottom: 0px;
        padding-left: 0px;
        line-height: 22px;
    }

    .allText {
        padding-top: 0px;
        padding-right: 0px;
        padding-bottom: 0px;
        padding-left: 0px;
        width: 100%;
    }

    .allText.bottomText {
        margin-top: 50px;
        margin-right: 0px;
        margin-bottom: 0px;
        margin-left: 0px;
        padding: 0 0 0 0;
        margin: 30px 0 0 0;
    }

    .ultimateImg {
        position: static;
    }

    .purpleBox {
        position: static;
    }

    .stars {
        width: 55%;
    }

    .allText.bottomText {
        margin-top: 75px;
        margin-right: 0px;
        margin-bottom: 0px;
        margin-left: 0px;
    }

    .responsive-container-block.bigContainer {
        padding-top: 10px;
        padding-right: 20px;
        padding-bottom: 10px;
        padding-left: 20px;
    }

    .purpleText {
        font-size: 16px;
        line-height: 22px;
    }

    .explore {
        padding: 6px 35px 6px 35px;
        font-size: 15px;
    }
}
</style>