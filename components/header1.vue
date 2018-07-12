<template>
     <div id="header1">
            <div id = "page_title"> Clouthster</div>
        
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
        </div>
</template>

<style scoped>
@import '../pages/CSSFiles/general.css';
</style>

<script>
export default {
    props: []
}
</script>