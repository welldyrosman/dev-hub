<template>
    <div class="l-navbar" :class="menuopen?'expander':''" id="navbar">
        <nav class="nav">
            <div>
                <div class="nav__brand">
                    <ion-icon name="menu-outline" v-on:click="showMenu()" class="nav__toggle" id="nav-toggle"></ion-icon>
                </div>
                <div class="nav__title" :class="menuopen?'hidden-title':''" id ="nav-logo">
                    <span class="nav_title">PARKLAND<br>DIGITAL<br>SYSTEM</span>
                </div>
                <div class="nav__list">
                    <div href="#" v-for="menu in menus" v-on:click="togglecollapse(menu.id)" :key="menu.id" class="nav__link collapse" :class="isactive==menu.id?'active':''">
                        <ion-icon name="document-text-outline" class="nav__icon"></ion-icon>
                        <span class="nav_name">{{menu.label}}</span>

                        <ion-icon name="chevron-down-outline" :class="isactive==menu.id?'rotate':''" class="collapse__link"></ion-icon>

                        <div class="collapse__menu" :class="isactive==menu.id?'showCollapse':''">
                            <div v-for="submenu in menu.submenus" v-on:click="menuactive(submenu.id)" :key="submenu.id" 
                            :class="issubactv==submenu.id?'subactive':''" 
                            class="collapse__sublink">{{submenu.label}}</div>
                        </div>
                    </div>   
                   
                </div>
            </div>
        </nav>

        <!-- <a href="#" class="menu"><p> GROUPWARE </p> </a> -->
    </div>
</template>
<script>
export default {
    data(){
        return{
            menuopen:false,
            isactive:null,
            issubactv:null,
            menus:[
                {
                    id:11,
                    label:"REPORTS",
                    submenus:[
                        {id:1,label:"Data"},
                        {id:2,label:"Group"},
                        {id:3,label:"Members"}
                   ],
                },
                {
                    id:12,
                    label:"NOTICE",
                    submenus:[
                       {id:4,label:"Data"},
                        {id:5,label:"Group"},
                        {id:6,label:"Members"}
                   ],
                },
                {
                    id:13,
                    label:"BOARD",
                    submenus:[
                       {id:7,label:"Data"},
                        {id:8,label:"Group"},
                        {id:9,label:"Members"}
                   ],
                },
            ]
        }
    },
    methods:{
        showMenu(){
           this.menuopen=!this.menuopen
           document.body.classList.toggle('body-pd');
           //console.log();
        },
        togglecollapse(id){
            this.isactive=id
        },
        menuactive(id){
            this.issubactv=id
        }
    }
}
</script>