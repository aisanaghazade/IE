<template>
    <div id="product">
        <img src="" id="product_img">
        <p id="discount"><br>{{N}}%</p>
    </div>
</template>

<script>
export default {
    props:['N']
}
</script>

<style scoped>
#product{
    position: absolute;
    top: 200px;
    right: 260px;
    width: 450px;
    height: 590px;
}

#product_img{
    width: 450px;
    height: 590px;
}

#discount{
    position: absolute;
    top: 3px;
    left: 3px;
    width: 50px;
    height: 50px;
    border-radius: 100%;
    text-align: center;
    background-color: rgb(255, 2, 129);
}
</style>


