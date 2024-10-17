<template>
    <div>
        
        <div class="heading">
            <h2>Lorem, ipsum.</h2>
            <a href="" class="link-more">Lorem, ipsum dolor.</a>
        </div>
        <div class="courses">
            <div class="courses_item" v-for="el in courses" :key="el/title">
                <img :src="'/img/' + el.img" alt="el.title">
                <h2>{{ el.title }}</h2>
                <p>{{ el.cl }}</p>
                <div class="time">{{el.time  }}</div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['data'],
    created() {
        this.courses = this.data
    },
    data() {
        return {
            courses: []
        }
    }
}
</script>

<style lang="scss" scoped>
    $mainColor: #000;
    $additionColor: #25ab72;
    $textColor: #fff;
    $hoverColor: #c7c7c7;
    $linkColor: #ababab;

.heading{
    @media (min-width: 1024px) {
        display: flex;
    }
    @media (max-width: 1024px) {
        margin-top: -100px;
        display: block;
    }
    @media (max-width: 1500px) and (min-width: 1024px) {
        margin-top: -60px;
        
    }
    justify-content: space-between;
    align-items: center;
    margin-bottom: 40px;
    

    .link-more{
        text-transform: uppercase;
    
    }

    h2{
        font-size: 2.2em;
        line-height: 2.2em;
    }
    a{
        font-size: 0,8em;

    }
}
.courses{
    margin-bottom: 150px;
    display: flex;
    @media (min-width: 1024px){
        justify-content: space-between; 
        flex-wrap: wrap;}
    
    

    @media (max-width: 1024px){
    justify-content: center;
    flex-direction: column;
    }

    .courses_item{
        margin-top: 70px;
        cursor: pointer;
        position: relative;
        overflow: hidden;
        border-radius: 12px;
        max-width: 100%;

        .time{
            position: absolute;
            right: 0;
            bottom: 56px;    
            background: #000;
            padding: 4px;
            font-weight: 600;
            border-top-left-radius: 4px;
        }

        h2{
            font-size: 2em;
            margin-left: 10px;
            position: relative;
            bottom: 32px;
        }

        p{
            color: $linkColor ;
            position: relative;
            margin-left: 10px;
            bottom: 32px;
            font-size: 0.9em;
        }
        img{
            width: 100%;
            opacity: 0.8;
            transition: all 500ms ease-in-out;
            

            &:hover{
                opacity: 1;
                transform: scale(1.2);
            }
        }
    }

}


</style>