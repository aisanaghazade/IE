<template>
   <div id="footer1">
        <nav>
        <ul id="partition">
            <li id="CS">
                <a class="FP" href="#"><b><br>خدمات مشتریان</b></a>
                <a class="FP" href="#"><br>سؤالات متداول</a>
                <a class="FP" href="#"><br>بازگرداندن کالا</a>
                <a class="FP" href="#"><br>شرایط استفاده</a>
                <a class="FP" href="#"><br>حریم شخصی</a>
            </li>
            <li id="aboutus">
                <a class="FP" href="#"><b><br>اطلاعات ما</b></a>
                <a class="FP" href="#"><br>درباره ما</a>
                <a class="FP" href="#"><br>تماس با ما</a>
            </li>
            <li id="icons">
              <b>به ما در رسانه‌های اجتماعی بپیوندید<br> </b>
                <table id="table">
                    <tr></tr>
                    <tr>
                        <td class="iconcell"><a href="#"> <img src="../icons/twitter.png" class="i"></a> </td>
                        <td class="iconcell"><a href="#"> <img src="../icons/instagram.png" class="i"></a></td>
                        <td class="iconcell"><a href="#"> <img src="../icons/facebook.png" class="i"></a></td>
                    </tr>
                    <tr>
                        <td class="iconcell"><a href="#"> <img src="../icons/twitter.png" class="i"></a></td>
                        <td class="iconcell"><a href="#"> <img src="../icons/instagram.png" class="i"></a> </td>
                        <td class="iconcell"><a href="#"> <img src="../icons/facebook.png" class="i"></a> </td>
                    </tr>
                </table>
            </li>
            <li id="copyright">
                <p class="FP"> تمامی حقوق این سایت متعلق به دانشگاه امیرکبیر بوده و هرگونه استفاده از منابع و طراحی‌های این سایت توسط نهادهای خارج دانشگاه با پیگرد قانون همراه خواهد بود.</p>
            </li>
        </ul>
        </nav>
    </div>
</template>

<style scoped>
   
 #footer1{
    background-color: #E0E0E0;
    position: relative;
    height: 230px;
    bottom: -1100px;
    right: 0px;
    direction: rtl;
    width: 1300px;
    display: block;
}

#partition{
    position: relative;
    top: -20px;
    display: block;
    list-style-type: none;
    width: 100%;
    direction: rtl;
}

#CS{
    /*width: 10%;*/
    /*margin-right: 10%;*/
    border-style: none;
    width: 10%;
    margin-right: 10%;
    direction: rtl;
    float: right;
}

.FP{
    font-size: 90%;
    margin-top: 1%;
    font-style: normal;
    color: darkslategrey;
    text-decoration: none;
    float: inherit;
    margin-right: 0%;
    direction: rtl;

}
.i{
    opacity: 0.5;
}

#aboutus{
    border-style: none;
    width: 7%;
    margin-right: 5%;
    direction: rtl;
    float: right;
}


#table{
    position: relative;
    right: 70px;
    top: 15px;
}

#icons{
    position: relative;
    margin-top: 1.5%;
    margin-right: 3%;
    float: right;
    color: darkslategrey;
}

.iconcell{
    width: 40px;
    height: 40px;
    margin-right: 20px;
    margin-left: 10px;
}
#copyright{
    width: 35%;
    margin-right: 3%;
    margin-top: 3%;
    font-size: 90%;
    color: darkslategrey;
    float: right;
}

.text{
    margin-right: 1%;
    font-size: 90%;
    color: gray;
    direction: rtl;
}

.title{
    font-size: 100%;
    color: gray;
}


</style>


