<template>
    <div class="container">
        <div class="row">
            <div class="col-sm-9">
                <h1 class="text-dark">Giới thiệu</h1>
                <section>
                    <h4>Câu chuyện thương hiệu</h4>
                    <p>Thành lập vào tháng 12/2010 từ tình yêu với những chiếc bánh, Fresh Garden khởi nguồn cùng slogan “Bánh tươi mỗi ngày” và sứ mệnh xuyên suốt về mang tới những sản phẩm thơm ngon nhất. Những năm đầu, sản phẩm chủ lực của Fresh Garden là bánh kem và bánh mì tươi. Trong mỗi dịp lễ hay sinh nhật, bánh kem của Fresh Garden luôn là một trong những lựa chọn hàng đầu, bởi độ ngọt vừa phải, mẫu bánh đẹp, giá thành hợp lý. Bên cạnh đó, đồng hành mỗi ngày của khách hàng là các sản phẩm bánh mì tươi dinh dưỡng, thơm ngon.</p>
                    <img src="https://file.hstatic.net/200000411281/file/fresh-garden-toii-min_134715d24cff47a8ac17406f87b7b3da_grande.jpg" alt="m1">
                </section>
                <section>
                    <h4>Dấu ấn hành trình</h4>
                    <p>Với hơn 100 cửa hàng và đại lý phân phối phủ khắp các tỉnh phía Bắc, Fresh Garden tự hào là thương hiệu bánh tươi uy tín bậc nhất với dây chuyền sản xuất tiên tiến hiện đại cùng gần 1000 nhân sự làm việc chăm chỉ không ngừng sáng tạo. Với tín đồ của bánh ngọt, mặn, bánh kem thì thật sự Fresh Garden chính là một "thế giới thu nhỏ" của bánh trái, chiều lòng bất kì vị khách nào ghé ngang. Trải qua một thập kỷ với những cung bậc sáng tạo, Fresh Garden không chỉ ghi dấu bởi chất lượng mà còn vì sự tinh tế trong từng nấc hương vị, đa dạng bánh Âu, Á và dần trở thành thói quen trong văn hóa tiêu dùng của những tín đồ yêu bánh.
                    </p>
                    <p>
                    Thế mạnh của Fresh Garden nằm ở những dòng bánh kem tươi mềm mịn ngọt dịu tươi mới, bánh mì nướng đặc biệt giòn thơm, bánh cuộn chuẩn Nhật với lớp kem sữa Hokkaido… rất được ưa chuộng. Trong mỗi dịp lễ hay sinh nhật, bánh kem của Fresh Garden luôn là một lựa chọn hàng đầu, bởi độ ngọt vừa phải, mẫu bánh đẹp, giá thành hợp lý. Bên cạnh đó, đồng hành với khách hàng mỗi ngày là các sản phẩm bánh mì tươi – bánh mỳ kẹp tiện lợi, dinh dưỡng.</p>
                        <img src="https://file.hstatic.net/200000411281/file/banh-gato-fresh-garden-min_24ddfc8a20c84fc48d6413b8b2e0b370_grande.jpg" alt="m2">
                </section>
                <section>
                    <h4>Sứ mệnh và tầm nhìn</h4>
                    <p>
                        Đằng sau Fresh Garden là đội ngũ nhân viên, chuyên gia đầu bếp luôn nỗ lực sáng tạo, không ngừng đam mê để có thể đưa ra những sản phẩm ngon, chất lượng, đẹp mắt và an toàn cho sức khỏe khách hàng. Đi cùng quy trình làm bánh nghiêm ngặt, khép kín, đòi hỏi nhân viên phải cẩn thận, tỉ mỉ và chăm chút trong từng công đoạn nhỏ nhất. Fresh Garden cam kết mang đến những sản phẩm đạt chất lượng cao nhất như một lời tri ân đối với sự yêu mến và tin dùng.
                    </p>
                    <img src="https://file.hstatic.net/200000411281/file/banh-my-tuoi-fresh-garden-min_aa5a4a7dbb9246f2a277f13ee2213858_grande.jpg" alt="m3">
                </section>
            </div>
            <div class="scrollButton">
                    <router-link :to="{ name: 'products' }"><a class="explore">
                        Cửa hàng
                    </a></router-link>
            </div>
        </div>
    </div>
</template>
<script>
    window.addEventListener('scroll', function() {
        var scrollButton = document.getElementById('scrollButton');

        if (window.scrollY > 0) {
            scrollButton.style.display = 'block';
        } else {
            scrollButton.style.display = 'none';
        }
    });
</script>
<style>
.scrollButton{
    position: fixed;
    top: 50%;
    left: 90%;
  transform: translate(-50%, -90%);
    display: none;
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

section h4{
    color: #4B494E;
    line-height: 20px;
}
</style>