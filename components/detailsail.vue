<template>

<div id="detailsail" v-if="c==1">

<div class="right">
  <input type="radio" id = "radiob">
</div>

  <div class="up">
    <div class="bailee">تحویل گیرنده: {{bailee}}</div>
    <div class="homenumber">شماره تلفن ثابت: {{homenumber}} </div>
    <div class="phonenumber">شماره تلفن همراه: {{phonenumber}}</div>
  </div>

  <div class="bottom">
    <div class="address">آدرس: {{address}}</div>
    <div class="postalcode">کد پستی: {{postalcode}}</div>
  </div>

  <div class="left">
    <div class="edit"></div>
    <div class="delete">
      <button id="delete" @click = "del()"><img id="image1" src="../icons/delete.png"></button>
    </div>
  </div>
</div>
</template>

<script>
export default {
  props:[
    'address', 'bailee', 'homenumber', 'phonenumber', 'postalcode','c'
  ],
  methods:{
    del: function(){
            this.a--;
            this.c--;
        }
  },
  data: function(){
    return{
      a:1
    }
  }
}
</script>


<style>
#radiob{
  position: relative;
  top:20px;
  left: 10px;
}
#image1{
    width: 10px;
    height: 10px;
}
#delete{
    width: 15px;
    height: 15px;
    position: relative;
    top: -30px;
    right: -10px;
    background-color: rgba(241,245,248);
    border-style: none;
}
  #detailsail
  {
    position: relative;
    width: 1000px;
    height: 80px;
    margin-right: 10%;
    border: solid 0.5px rgb(136, 136, 136);
    float: right;

  }

  .right{
    width: 4%;
    height: 100%;
    float: right;
    background-color: aliceblue;
  }
  .up
  {
    border: solid 0.5px white;
    width: 92%;
    height: 50%;
    border-right-color: #dbe1ec;
    float: right;
  }
  .bottom
  {
    border: solid 0.5px white;
    width: 92%;
    height: 50%;
    border-left-color: #dbe1ec;
    float: right;
  }
  .bailee
  {
    border: solid 0.5px white;
    height: 100%;
    width: 30%;
    border-bottom-color: #dbe1ec;
    border-right-color: #dbe1ec;
    float: right;
    text-align: right;
    padding-right: 2%;
    padding-top: 0.5%;
  }
  .homenumber
  {
    border: solid 0.5px white;
    height: 100%;
    width: 40%;
    border-bottom-color: #dbe1ec;
    border-right-color: #dbe1ec;
    float: right;
    text-align: right;
    padding-right: 2%;
    padding-top: 0.5%;
  }
  .phonenumber
  {
    border: solid 0.5px white;
    height: 100%;
    width: 30%;
    border-bottom-color: #dbe1ec;
    border-left-color: #dbe1ec;
    border-right-color: #dbe1ec;
    float: right;
    text-align: right;
    padding-right: 2%;
    padding-top: 0.5%;
  }
  .postalcode
  {
    height: 100%;
    width: 30%;
    float: right;
    text-align: right;
    padding-right: 2%;
    padding-top: 0.5%;
  }
  .address
  {
    border: solid 0.5px white;
    height: 100%;
    width: 70%;
    border-left-color: #dbe1ec;
    border-right-color: #dbe1ec;
    float: right;
    text-align: right;
    padding-right: 2%;
    padding-top: 0.5%;
  }
  .left{
    width: 4%;
    height: 100%;
    background-color: aliceblue;
  }
  .edit
  {
    border-top: solid 0.5px #dbe1ec;
    width: 100%;
    height: 50%;
    float: right;

  }
  .delete
  {
    width: 100%;
    height: 50%;
    float: right;
  }
</style>
