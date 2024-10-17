<template>
    <div>
        <div class="features">
            <div class="features__heading">
                <img src="/img/yellow-line.svg" alt="Workout">
                <h3>Тренировки Специально Для тебя</h3>
            </div>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua consectetur adipiscing.</p>
            <button>Начать</button>
        </div>
        <div class="pictures">
            <div>
                <img src="/img/trener-1.png" alt="">
                <h4>Саманта Вильям</h4>
                <p>Тренер</p>
            </div>
            <div class="middle">
                <img src="/img/trener-2.png" alt="">
                <h4>Алина Реймонд</h4>
                <p>Тренер</p>
            </div>
            <div class="big">
                <img src="/img/trener-3.png" alt="">
                <h4>Джонатан Вайз</h4>
                <p>Тренер</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
$backgroundColor: #191919;
$additionColor: #25ab72;
$textColor: #fff;

.features {
    
    background: #191919;
    position: relative;
    // Міксін для кнопок
@mixin button-styles {
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

  &:hover {
    transform: translateY(-8px);
    border: 1px solid #fff;
  }
}

// Міксін для тексту параграфа
@mixin paragraph-styles($padding) {
  color: #ababab;
  font-size: 1.2em;
  line-height: 170%;
  width: 100%;
  padding-left: $padding;
}

// Міксін для заголовків h3
@mixin h3-styles($font-size, $width, $padding-left) {
  font-size: $font-size;
  width: $width;
  padding-left: $padding-left;
}

// Основні стилі
@media (min-width: 1124px) {
  width: 1500px;
  margin-left: 30%;
  padding: 120px 5% 320px 15%;

  .features__heading {
    position: absolute;
    top: 0;
    left: -320px;

    h3 {
      @include h3-styles(4.5em, 500px, 0);
      top: -100px;
      position: relative;
    }

    img {
      position: relative;
      top: 320px;
    }
  }

  p {
    @include paragraph-styles(128px);
    width: 560px;
  }

  button {
    margin-left: 128px;
    @include button-styles;
  }
}

@media (max-width: 1123.9px) and (min-width: 724px) {
  width: 1000px;
  margin-left: 8%;
  padding: 80px 5% 60px;
  position: relative;

  .features__heading {
    img {
      margin-bottom: 20px;
      max-width: 450px;
      margin-left: 50px;
      position: absolute;
      top: -100px;
    }

    h3 {
      @include h3-styles(3em, 450px, 40px);
      margin-bottom: 20px;
    }
  }

  p {
    @include paragraph-styles(40px);
    width: 70%;
  }

  button {
    margin-left: 40px;
    @include button-styles;
  }
}

@media (max-width: 722.9px) {
  padding: 60px 5%;

  .features__heading {
    h3 {
      @include h3-styles(3em, 100%, 0);
      margin-bottom: 30px;
    }

    img {
      display: none;
    }
  }

  p {
    @include paragraph-styles(0);
  }

  button {
    @include button-styles;
  }
}}


.pictures {
    margin-bottom: 100px;
    display: flex;
    
    
    @media(min-width: 1280px) {
        padding-left: 70px;
    }
    @media(max-width: 1279.9px) and (min-width: 722px) {
        flex-wrap: wrap;
        justify-content: space-between;
        
    }
    @media(max-width: 721.9px){
        flex-direction: column;
        width: 100%;
        img{
            width: 100%;
        }
    }
    > div {
        @media(min-width: 1279.9px) {
            position: relative;
        }
        @media(max-width: 1279.9px) {
            margin-top: 100px;
            
        }

        &.middle {
            top: 321px;
        }

        &.big {
            top: -193px;

            h4, p {
                margin-left: 20px;
            }
        }

        h4 {
            font-weight: 400;
        }

        p {
            color: #ABABAB;
            font-size: 0.9em;
        }
    }
}
</style>