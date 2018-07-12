<template>
    <div id="category">
        <div id = "background1">
            <img src="../icons/placeholder-image.png" class="Image">
        </div>
        <bottom id="name1">
            <p id="text1">{{name}}</p>
        </bottom>
    </div>
</template>

<script>
export default {
    props: ['name','address']
}
</script>

<style scoped>
    #category{
        position: relative;
        top: 0px;
        right: 0px;

    }
    #background1{
        position: relative;
        width: 250px;
        height: 160px;
        float: right;
        top: 0px;
        right: 0px;
        border-style: solid;
        border-color: rgb(119, 116, 116);
        border-width: 1px;
    }

    #name1{
        position: relative;
        top: 159px;
        float: right;
        right: -250px;
        align-content: center;
        background-color: rgb(170, 167, 167);
        border-style: none solid solid solid;
        border-color: rgb(119, 116, 116);
        border-width: 0.5px;
        color: rgb(218, 210, 210);
        width: 250px;
        height: 50px;
    }

    .Image{
        width: 200px;
        height: 100px;
        opacity: 100%;
        position: relative;
        top: 30px;
        right: -15px;
    }

    #text1{
      position: relative;
        top: 15px;
        float: right;
        right: 120px;
    }
</style>

