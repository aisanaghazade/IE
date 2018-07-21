<template>
     <div id="header1">
            <div id = "page_title"> Clouthster</div>
        <div id = "login">
            <button class = "signin-up" href="#" @click="show()">   ورود  </button>
            <button class = "signin-up" href="#" @click="show()">  عضویت  </button>
        </div>
        <div id = "search">
            <input type="text" id="search_term">
            <button type="submit" id="search_button"><img src="../icons/search.png"></button>
            
        </div>
        <nav id = "menu" >
            <ul id = "nav" class="inline">
                <li class="item"><a class="menu1_link" href="#">مردانه</a> </li>
                <li class="item"><a class="menu1_link" href="#">زنانه</a> </li>
                <li class="item"><a class="menu1_link" href="#">بچه‌گانه</a> </li>
                <li class="item"><a class="menu1_link" href="#">ورزشی</a> </li>
                <li class="item"><a class="menu1_link" href="#">تخفیف</a> </li>
                <li class="item"><a class="menu1_link" href="#">برند</a> </li>
            </ul>
        </nav>

        <div id="modal" v-if="modal">
            <div id="closebut">
        <buttun v-on:click="close()" id="closemodalbut"><span><img id="closebutimg" src="../icons/cross.png"/></span></buttun>
            </div>
        <form id="form" action="">
        <div id="innerform">
            <div id="vorodtext"><b>ورود </b></div>
          <label class="formlabel"><b>شماره تلفن یا ایمیل</b></label>
          <input class="forminput" type="text" placeholder="aaghazaden@gmail.com" name="numberOrEmail" required>
          <label class="formlabel"><b>رمز عبور</b></label>
          <input class="forminput" type="password" name="password" required>
          <div id="forgetpassText">رمز عبور خود را فراموش کرده اید؟ <a href="#">کلیک کنید</a></div>
          <button class="submitFormbut" type="submit">ورود</button>
        </div>
        </form>
        </div>

    </div>
</template>

<style scoped>
@import '../pages/CSSFiles/general.css';

</style>

<script>
export default {
    props: [],
    data(){
        return{
            modal:false
        }
    },
    methods:{
        show: function () {
            this.modal = true
        },
        close: function () {
            this.modal = false
        }
    }
}
</script>