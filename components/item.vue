<template>
    <div id="item">
        <div id="discount"><p id="distext">{{N}}%</p></div>
        <img id="picture" scr="../icons/runningshoe.jpg">
        <p id="text1">{{brandname}}<br></p>
        <p id="text2">{{name}}<br></p>
        <p id="text3"><span id="text4">{{Pafter}} </span><span id="text5"> {{Pbefore}}</span></p>
        <p id="text6"> تومان</p>
    </div>
</template>

<script>
export default {
    props: ['brandname','address','name','Pbefore','Pafter','N']
}
</script>


<style scoped>
@import '../pages/CSSFiles/general.css';

#item{
    position: relative;
    height: 250px;
    width: 150px;
    top: 90px;
    right: 50px;
}

#picture{
    position: relative;
    top: -40px;
    right: 0px;
    height: 150px;
    width: 145px;
}

#discount{
    position: relative;
    top: -20px;
    right: -20px;
    float: right;
    border-radius: 100%;
    background-color: rgb(243, 35, 122);
    width: 40px;
    height: 40px;
    z-index: 1;
    align-content: center;
}

#distext{
    position: relative;
    top: 9px;
    text-align: center;
}

#text1{
    position: relative;
    top: -35px;
    text-align: center;
    color: rgb(112, 112, 112);
}

#text2{
    position: relative;
    top: -55px;
    text-align: center;
    color: rgb(199, 199, 199);
    font-size: 130%;
}
#text3{
    position: relative;
    top: -68px;
    text-align: center;
}

#text4{
    text-decoration: line-through;
}

#text5{
    color: rgb(255, 31, 125);
}

#text6{
    color: rgb(255, 31, 125);
    position: relative;
    top: -80px;
    text-align: center;
}

</style>


