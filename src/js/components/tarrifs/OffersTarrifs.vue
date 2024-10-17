<template>
    <div>
        <h2>Lorem ipsum dolor sit amet.</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Expedita illum quasi laboriosam!</p>
        <div class="bloks" :style="'left: ' + left + 'px'">
            <div class="item">
                <div class="content">
                    <h3>Lorem, ipsum dolor.</h3>
                    <p>Lorem. Natus assumenda distinctio nesciunt, quidem minima modi?</p>
                </div>
                <i class="fa-solid fa-arrow-right"></i>
            </div>
            <div class="item">
                <div class="content">
                    <h3>Lorem, ipsum dolor.</h3>
                    <p>lorem2 Lorsectetur adipisicing elit. Natus assumenda distinctio nesciunt, quidem minima modi?</p>
                </div>
                <i class="fa-solid fa-arrow-right"></i>
            </div>
            <div class="item">
                <div class="content">
                    <h3>Lorem, ipsum dolor.</h3>
                    <p>Lorsect elit. Natus assumenda distinctio nesciunt, quidem minima modi?</p>
                </div>
                <i class="fa-solid fa-arrow-right"></i>
            </div>
            <div class="item">
                <div class="content">
                    <h3>Lorem, ipsum dolor.</h3>
                    <p>Lors elit. Natus assumenda distinctio nesciunt, quidem minima modi?</p>
                </div>
                <i class="fa-solid fa-arrow-right"></i>
            </div>
            <div class="item">
                <div class="content">
                    <h3>Lorem, ipsum dolor.</h3>
                    <p>Lorem, ipsum dolor. Lorsectetur adipisicing elit. Natus assumenda distinctio nesciunt, quidem minima modi?</p>
                </div>
                <i class="fa-solid fa-arrow-right"></i>
            </div>
            <div class="item">
                <div class="content">
                    <h3>Lorem, ipsum dolor.</h3>
                    <p>Lorsectetur adipisicing elit. Natus assumenda distinctio nesciunt, quidem minima modi?</p>
                </div>
                <i class="fa-solid fa-arrow-right"></i>
            </div>
            <div class="item">
                <div class="content">
                    <h3>Lorem, ipsum dolor.</h3>
                    <p>Lorem ipsum dolor sit amet. Lorsectetur adipisicing elit. Natus assumenda distinctio nesciunt, quidem minima modi?</p>
                </div>
                <i class="fa-solid fa-arrow-right"></i>
            </div>
            <div class="item">
                <div class="content">
                    <h3>Lorem, ipsum dolor.</h3>
                    <p>Lorsectetur adipisicing elit. Natus assumenda distinctio nesciunt, quidem minima modi?</p>
                </div>
                <i class="fa-solid fa-arrow-right"></i>
            </div>
            
        </div>
        <div class="arrows">

    <img src="/img/arrow-next.svg" :class="{ 'hidden': left == 0 }" @click="moveBlock('prev')" alt="Workout">           
    <img src="/img/arrow-next.svg" v-show="this.left>=-1600" @click="moveBlock('next')" class="next" alt="Workout">
        </div>
    </div>
        
</template>

<script>

export default {
    data() {
        return {
            left: 0
        }
    },
    methods: {
        moveBlock(value) {
            let add = 320;
            if (value == 'next' && this.left>=-1600)
                this.left -= add;
            else if (value == "prev" && this.left != 0)
                this.left += add;
        }
    }
}
</script>

<style lang="scss">
  h2{
    margin-top: 80px;
    font-size: 2.8em;
  }
  p{
    color: #9b9a97;
    margin-top: 16px;
  }
  .bloks{
    display: flex;
    margin-top: 36px;
    margin-bottom: 40px;
    width: 3500px;
    position: relative;
    transition: left .4s ease; 
    .item{
        background: #323443;
        padding: 30px;
        border-radius: 12px;
        width: 250px;
        display: flex;

        &:not(:last-of-type){
            margin-right: 24px;
        }
        h3{
            font-size: 1.5em;
        }
            p{
                color: #9b9a97;
            }
      
        i{
           float: right;
           font-size: 1.2em;
           display: flex;
           align-items: center;
           margin-left: 20px;
        }
    }
  }
.arrows{
    margin-bottom: 150px;
   img{
    cursor: pointer;
    transition: transform 1s ease-in;
    margin-right: 30px;

    &:hover{
        transform: scale(1.2);
    }
    &.next{
        
        transform: rotate(180deg);

        &:hover{
            transform: scale(1.2) rotate(180deg);
        }
    }
   } 
   .hidden {
        visibility: hidden;}
}
</style>