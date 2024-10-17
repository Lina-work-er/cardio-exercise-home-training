<template>
  <div class="head">
    
    <!-- main info from page -->
     <!-- Cardio Exercise -->
    <div class="lead">
        <div>
            <h1>Cardio <br> Exercise</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorum adipisci minima aspernatur quaerat deleniti consectetur iusto at culpa?</p>
            <button class="lead_buttons">Lorem, ipsum dolor.</button>
            <img src="/img/companies.png" alt="Workout">    
        </div>
       <!-- time + distance -->
       <div>
                <img src="/img/lead2.png" alt="Workout">
                <div class="lead__info">
                    <div class="lead__info__km">
                        <i class="fa-solid fa-person-running"></i>
                        <span>4.95</span>
                        km
                    </div>
                    <div class="lead__info__training">
                        <i class="fa-solid fa-play"></i>
                        <span>165+</span>
                        lorem
                    </div>
                    <div class="lead__info__videos">
                        <span>165+</span>
                        lorem
                    </div>
                </div>
            </div>
    </div>
  </div>
</template>

<script>



export default {
    // Код таймера відлік секунд

    data() {
        return {
            showTime: '39:00',
            timerCount: 38 * 60
        }
    }
}
   

</script>

<style lang="scss" scoped>
$backgroundColor: #191919;
$additionColor: #e6533c;
$textColor: #fff;

@keyframes pulse{
    0%{
        transform: scale(0.7);
    }
    100%{
        transform: scale(1);
    }
}

.head{
    margin-top: 70px;
    height:  740px;
    overflow: hidden;

    
    .lead{
        margin-top: 20px;
        display: flex;

        h1{
            letter-spacing: -2px;

            @media(min-width: 1500px){
            font-size: 12em;
            line-height: 170px;}

            @media(max-width: 1500px) and (min-width: 900px){
            font-size: 10.5em;
            line-height: 140px;}

            @media(max-width: 899px) and (min-width: 450px){
            font-size: 8em;
            line-height: 100px;}

            @media(max-width: 449px){
            font-size: 5em;
            line-height: 70px;}
        }
        p{
            color: #868686;
            margin: 20px 0;
            @media(min-width: 1023px){
                width: 600px;
            }
        }
        img{
            display: block;
            margin-top: 60px;
            width: 100%;
            max-width: 600px;
        }
        .lead_buttons{
            background: $additionColor;
            padding: 20px;
            font-weight: 600;
            font-size: 1.2em;
            color: $textColor;
            cursor: pointer;
            border-radius: 10px;
            margin-top: 30px;
            transition: transform 500ms ease;
            border: 1px solid $additionColor;
            
            @media (max-width: 450px) {
               
                display: flex;
                flex-wrap: wrap;
                width: 100%;
                
            }
           
            &:hover{
                transform: translateY(-8px);
                border: 1px solid #fff
            }
            
        }

        >div:first-of-type{
            display: block;
            max-width: 100%;
            margin-top: 70px;
        }

        > div:last-of-type {
            position: relative;
                @media(min-width: 1500px){
                top: 40px;
                right: 80px;}
       
                @media(max-width: 1500px) and (min-width: 1224px){
                    transform: scale(.88);
                    bottom: 0px;
                    right: 60px;
                }
                @media(max-width: 1223px){
                    display: none;
                }
            
        .lead__info {
            position: absolute;
            
            @media(min-width: 1500px){
                top: 200px;
                right: -12px;
            }

            @media(max-width: 1500px){
                top: 200px;
                right: 120px;
            }

            @mixin info-block($background, $color, ) {
                position: relative;
                border-radius: 20px;
                padding: 20px 30px;
                width: 140px;
                font-size: 0.7em;
                margin-bottom: 25px;
                text-align: center;
                background: $background;
                color: $color;

                span {
                    font-weight: 600;
                    color: #fff;
                }
                i{
                    padding: 10px;
                    border-radius: 50%;
                    color: #fff;
                    font-size: 1.3em;
                    width: 14px;
                    height: 14px;
                    text-align: center;
                    line-height: 14px;
                    
                }
            }

            .lead__info__km{
                @include info-block(#ef8964, #efcaba);
                
                @media(min-width: 1500.1px){
                    left: 20px;
                bottom: 240px;
                }
                @media(max-width: 1500px) and (min-width: 1224px){
                    left: 180px;
                bottom: 240px;
                }
                span {
                    font-size: 2.7em;
                    margin-right: 4px;
                }
                i{
                    background: #efcaba;
                    display: block;
                }
            }

            .lead__info__training {
                @include info-block(#303030, #acabab);
                @media(min-width: 1500.1px){
                    right: 320px;
                    top: 50px;
                }
                @media(max-width: 1500px) and (min-width: 1224px){
                    right: 180px;
                    top: 60px;
                }
                
                
                

                span {
                    font-size: 1.7em;
                    float: left;
                    position: relative;
                    top: 8px;
                    margin-right: 8px;
                }
                i{
                   background: #ef8964;
                }
            }
            .lead__info__videos {
                @include info-block(#7a29dc, #c6a8e4);
                
                @media(min-width: 1500.1px){
                   right: -80px;
                top: 20px;
                }
                @media(max-width: 1500px) and (min-width: 1224px){
                    right: -180px;
                top: 20px;
                }

                span {
                    font-size: 2.5em;
                }
            }
        }
    }
    }
    
}



</style>