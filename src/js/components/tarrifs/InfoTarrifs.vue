<template>
<div>
    <div class="blocks">
        <div>
            <h2>Lorem ipsum <br>dolor sit amet.</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic, delectus?</p>
            <span><a href="">Lorem more  <i class="fa-solid fa-arrow-right"></i></a></span>
        </div>
        <div>
            <img src="/img/info-1.png" alt="">
        </div>
    </div>
    <div class="blocks">
        <div>
            <img src="/img/info-2.png" alt="">
        </div>
        <div>
            <h2>Lorem ipsum<br>dolor sit amet.</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic, delectus?</p>
            <span><a href="">Lorem more  <i class="fa-solid fa-arrow-right"></i></a></span>
        </div>
            </div>
</div>
</template>

<script>



export default {
}
</script>

<style lang="scss" scoped>
.blocks{
    display: flex;
    align-items: center;
    @media (min-width: 722px) {
       flex-wrap: wrap; 
       justify-content: space-between;
       margin-top: 80px;
       >div{
        width: 45%;
        h2{
            margin-bottom: 20px;
            font-size: 2.2em;
        }
        p{
            color: #9b9a9b;
            max-width: 450px;
            margin-bottom: 20px;
        }
        
    }
    }
    @media (max-width: 721.9px) {
      flex-direction: column;
      margin-bottom: 10px;
      >div{
        margin-bottom: 60px;
       
      }
      &:last-of-type{
        flex-direction: column-reverse;
      }
      p{
        font-size: 1.2em;
        margin-bottom: 12px;
      }
      span{
        font-size: 1.4em;
        display: flex;
        justify-content: flex-end;
        }
    }
    span{
        &:hover{
                display: inline-block;
                transform: scale(1.2);
            }
            a{
                 color: #0070c9;
                 &:hover{
                    color: #025497;
                    transform: scale(1.2);
                 }
            }
            
            i{               
                margin-left: 8px;
                font-size: 1.2em;
            }
        }
        
    img{
        max-width: 600px;
        width: 100%;
    }
}

</style>