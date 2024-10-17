<template>
    <!-- <div class="container"> <Nav /></div>
    <div class="container"> <Head /></div>
    <div class="container"> <Trainings :data="courses"/></div>
    <div class="container"> <Features /></div> -->
    <div class="wrapper">
        <div class="container">
           <router-view></router-view>
        </div>
    </div>
</template>

<script>


</script>

<style lang="scss">
    $mainColor: #000;
    $additionColor: #25ab72;
    $textColor: #fff;
    $hoverColor: #c7c7c7;
    $linkColor: #ababab;


    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;400;600&display=swap');

    ::selection{
        background: $additionColor;
    }

 *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
 }
 body{
    background: $mainColor;
    color: $textColor;
    font-family: 'Poppins', sans-serif;
    font-weight: 400;
    outline: none;
    font-size: 1em;
 }
  a{
    color: $linkColor;
    text-decoration: none;
    &:hover{
    color: $hoverColor;
  }
 }

 .wrapper{
    overflow: hidden;
 }

 .container{
    @media(min-width: 1500px){
        width: 1300px;
        margin: 0 auto;
    }

    @media(max-width: 1500px) and (min-width: 900px){
        width: 80%;
        margin: 0 10%;
    }
    
    @media(max-width: 900px){
        width: 90%;
        margin: 0 5%;
    }
 }


</style>