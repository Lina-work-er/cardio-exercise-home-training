<template>
    <nav class="nav">
        <span class="nav_logo"><router-link to="/">WORKOUT</router-link></span>
        <ul class="nav_links" v-if="screenWidht > 1024">
            <li><router-link> Exercises</router-link></li>
            <li><router-link to="/tarrifs">Training</router-link></li>
            <li><router-link>Prices</router-link></li>
            <li><router-link>About us</router-link></li>
        </ul>
        <i v-else :class="menuIcon" @click="showMenu()"></i>
        <ul class="nav_links--mobile" v-if="screenWidht <= 1024 && mobileMenu">
            <li><router-link>Exercises</router-link></li>
            <li><router-link to="/tarrifs">Training</router-link></li>
            <li><router-link>Prices</router-link></li>
            <li><router-link>About us</router-link></li>
        </ul>
    </nav>
</template>

<script>



export default {
    data() {
        return {
            screenWidht: screen.width,
            mobileMenu: false,
            menuIcon: "fa-solid fa-bars"
        }
    },
    mounted(){
            this.onScreenResize();
    },
    methods: {
        onScreenResize() {
            window.addEventListener("resize", () => {
                this.screenWidht = screen.width;
            })
        },
        showMenu() {
            this.mobileMenu = !this.mobileMenu;
            this.menuIcon = this.menuIcon.includes("bars") ? "fa-regular fa-circle-xmark" : "fa-solid fa-bars";
        }   
    }
}

</script>

<style lang="scss" scoped>
.nav{
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 50px;
    flex-wrap: wrap;

    .nav_logo{
        font-size: 1.8em;
        text-transform: uppercase;
    }
    .nav_links{
        list-style: none;
        text-transform: uppercase;

        >li{
            display: inline-block;
            &:not(:last-of-type){
                margin-right: 28px;
            }
        }
    }
   .nav_links--mobile{
    list-style: none;
    text-align: center;
    width: 100%;

    li{
        margin-top: 24px;
    }
   }
}



</style>