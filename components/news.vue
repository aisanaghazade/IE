<template>
<div>
    <div id = "brands">
         <button id="try"> تمام برند‌های معتبر را با ما تجربه کنید.</button>
    </div>
    <div id = "news">
        <img id="mail" src="../icons/khabarname.png">
                    <p><br></p>
                    <p class="p1">در خبرنامه‌ی ما</p>
                    <p class="p1"><b>عضو شوید!</b></p>
                    <div id="email">
                        <input id="email-address" type="email" placeholder="email address">
                        <img id="emailicon" src="../icons/email.png">
                    </div>
                    <button id="signup"> عضو شوید</button>
    </div>
</div>
</template>

<style scoped>
#news{
    position: absolute;
    width: 300px;
    height: 250px;
    top: 750px;
    right: 700px;
    border-style: solid;
    border-color: rgb(80, 7, 250);
    background-color: rgb(80, 7, 250);
    float: left;
    margin-top: 1%;
}

#email{
    border-color: #6666FF;
    background-color: white;
    width: 80%;
    position: relative;
    top: 20px;
    right: -27px;
    border-radius: 20px;
    margin-top: 5%;
}

#email-address{
    border-style: none;
    margin-left: 2%;
    margin-right: 8%;
    width: 70%;
    border-radius: 20px;
}

#email-address:focus{
    outline: none;
}

#emailicon{
    opacity: 0.5;
}

#mail{
    position: relative;
    top: 20px;
    margin-right: 43%;
    margin-left: 43%;
    margin-top: 2%;
    color: gray;
}

.p1{
    font-size: 90%;
    color: rgb(240, 234, 234);
    margin-right: 35%;
    margin-left: 35%;
    margin-top: 2%;
}

#signup{
    position: relative;
    background-color: slategray;
    color: rgb(236, 236, 236);
    border-style: none;
    border-radius: 10px;
    width: 40%;
    top: 50px;
    right: -80px;
    
}

#brands{
    position: absolute;
    background-image: url("../icons/brands.png");
    width: 550px;
    right: 120px;
    height: 300px;
    float: right;
    top: 750px;
}

#try{
    position: relative;
    top: 40px;
    margin-left: 20%;
    margin-top: 15%;

    float: left;
    width: 60%;
    height: 20%;
    background-color: rgb(80, 7, 250);
    cursor: pointer;
    font-size: 90%;
    border:solid 0px;
    color: rgb(247, 234, 234);
    border-radius: 30px;
}

</style>
