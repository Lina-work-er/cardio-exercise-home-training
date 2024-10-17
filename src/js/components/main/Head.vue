<template>
  <div class="head">
    <!-- promotion new -->
    <div class="promotion">
        <span>NEW</span>
        Lorem, ipsum dolor.
    </div>
    <!-- main info from page -->
     <!-- Cardio Exercise -->
    <div class="lead">
        <div><h1>Cardio <br> Exercise</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorum adipisci minima aspernatur quaerat deleniti consectetur iusto at culpa?</p>
            <button class="lead_buttons">Start</button>
            <button class="lead_buttons">In more detail</button>
        </div>
       <!-- time + distance -->
       <div>
                <img src="/img/lead.png" alt="Workout">
                <div class="lead__info">
                    <div class="lead__info__time">
                        <span>{{showTime}}</span>
                        ВРЕМЯ
                    </div>
                    <div class="lead__info__cl">
                        <span>165</span>
                        КАЛОРИИ
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
    },
    watch: {
        timerCount: {
            handler() {
                setTimeout(() => {
                    if (this.timerCount <= 0) return;

                    this.timerCount--;
                    // const minutes = this.timerCount / 60;
                    const minutes = Math.ceil(this.timerCount / 60);
                    const seconds = this.timerCount - minutes * 60 + 60;
                    let txtSeconds = 0;
                    if (seconds == 60)
                        txtSeconds == "00";
                    else if (seconds < 10 && seconds > 0)
                        txtSeconds = "0" + seconds;
                    else
                        txtSeconds = seconds;
                    this.showTime = (txtSeconds == "00" ? minutes + 1 : minutes) + ":" + txtSeconds;
                }, 1000)
            },
            immediate: true
        }
    }
}
    // Реалізація таймера
//     data() {
//         return {
//             seconds: 0 // Змінна для лічильника секунд
//         };
//     },
//     computed: {
//         showTime() {
//             const minutes = Math.floor(this.seconds / 60);
//             const remainingSeconds = this.seconds % 60;
//             // Форматування часу у вигляді "MM:SS"
//             return `${String(minutes).padStart(2, '0')}:${String(remainingSeconds).padStart(2, '0')}`;
//         }
//     },
//     mounted() {
//         // Запуск таймера при монтуванні компонента
//         setInterval(() => {
//             this.seconds++;
//         }, 1000);
//     }
// };


</script>

<style lang="scss" scoped>
$backgroundColor: #191919;
$additionColor: #25ab72;
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

    .promotion{
        background: $backgroundColor;
        border-radius: 200px;
        padding: 10px 8px;
        color: #d1d1d1;
        width: 330px;
        animation: pulse infinite ease-in-out 1.5s alternate;

        @media(min-width: 450px){
        width: 360px;}
        @media(max-width: 450px){
        width: 280px;
        font-size: 0.85em;}

        span{
            background: $additionColor;
            border-radius: 200px;
            color: #fff;
            padding: 4px 10px;
            margin-right: 10px;
            font-weight: 600;
        }
    }
    .lead{
        margin-top: 20px;
        display: flex;

        h1{
            letter-spacing: -2px;

            @media(min-width: 1500px){
            font-size: 12em;
            line-height: 170px;}

            @media(max-width: 1500px) and (min-width: 900px){
            font-size: 10em;
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
        .lead_buttons{
            background: $additionColor;
            padding: 20px;
            
            width: 180px;
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
            &:first-of-type{
                margin-right: 36px;
            }
            &:last-of-type{
                background: $backgroundColor;
                border: 1px solid $backgroundColor;
                
                &:hover{
                    background: #141313;
                }
            }
            &:hover{
                transform: translateY(-8px);
                border: 1px solid #fff
            }
            &:first-of-type:hover{
               background: #00aa60; 
            }
        }
    
        > div:last-of-type {
            position: relative;
                @media(min-width: 1500px){
                bottom: 255px;
                right: 270px;}
        //     img {
        //         position: relative;
        //         bottom: 255px;
        //         right: 270px;
        // }
            
                @media(max-width: 1500px) and (min-width: 1224px){
                    transform: scale(.85);
                    bottom: 308px;
                    right: 280px;
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

            @mixin info-block {
                background: #191919;
                border-radius: 20px;
                padding: 20px 30px;
                width: 140px;
                font-size: 0.7em;
                margin-bottom: 25px;
                text-align: center;

                span {
                    font-weight: 600;
                    font-size: 3em;
                    display: block;
                }
            }

            .lead__info__time {
                @include info-block;

                span {
                    color: #FFE642;
                }
            }

            .lead__info__cl {
                @include info-block;

                span {
                    color: #FB1351;
                }
            }
        }
    }
    }
    
}



</style>