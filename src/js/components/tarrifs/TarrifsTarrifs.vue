<template>
<div>
    <h3>Lorem, ipsum.</h3>
    <div class="tarrifs">
        <div>
            <h4>Lorem, ipsum.</h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur id voluptatibus inventore?</p>
            <ul>
                <li>Lorem ipsum dolor sit amet.</li>
                <li>Lorem ipsum, dolor sit amet consectetur adipisicing.</li>
                <li>Lorem ipsum, dolor sit amet consectetur.</li>
                <li>Lorem ipsum, dolor sit.</li>
                <li>Lorem ipsum, dolor sit amet consectetur</li>
                <li>Lorem ipsum, dolor sit amet consectetur</li>
            </ul>
            <span><a href="">Lorem more  <i class="fa-solid fa-arrow-right"></i></a></span>
       
        </div>
        <div>
             <h4>Lorem, ipsum +</h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur id voluptatibus inventore?</p>
            <ul>
                <li>Lorem ipsum dolor sit amet.</li>
                <li>Lorem ipsum, dolor sit amet consectetur adipisicing.</li>
                <li>Lorem ipsum, dolor sit amet consectetur.</li>
                <li>Lorem ipsum, dolor sit.</li>
                <li>Lorem ipsum, dolor sit amet consectetur</li>
                <li>Lorem ipsum, dolor sit amet consectetur</li>
            </ul>
           <button>Lorem, ipsum.</button>
        </div>
    </div>
</div>
</template>

<script>



export default {
}
</script>

<style lang="scss" scoped>
h3{
    margin: 70px 0;
    font-size: 3em;
    font-weight: 400;
}
.tarrifs{
    display: flex;
    @media (min-width: 822px){
        justify-content: space-between;
        flex-wrap: wrap;
        margin-bottom: 120px;    
        }
    @media (max-width: 821.9px){
        flex-direction: column;
        width: 100%;
    }

    >div{
        @media (min-width: 822px){
        width: 45%;
        padding: 50px 4%;   
        }
    @media (max-width: 821.9px){
        width: 100%;
        padding: 50px 8%;

        &:first-of-type{
            margin-bottom: 40px;
        }
    }
        
        background: #232532;
        color: #a8a7a8;
        
        h4{
            color: #fff;
            font-size: 2em;
            margin-bottom: 30px;
        }
        ul{
            margin: 20px 30px; 
            @media (max-width: 821.9px){
                margin-bottom: 40px;
            }      
        }
        span{
            
            &:hover{
                display: inline-block;
                transform: scale(1.2);
            }
    @media (max-width: 821.9px){
        font-size: 1.4em;
        display: flex;
        justify-content: flex-end;
        margin-top: 20px;
    }
            a{
                 color: #0070c9;
                 &:hover{
                    color: #025497;
                    
                 }
            }
            
            i{               
                margin-left: 8px;
                font-size: 1.2em;
            }
            
        }
        button{
                background: #0070c9;
                border: 0;
                border-radius: 12px;
                color: #fff;
                cursor: pointer;
                padding: 10px 12px ;

                
                @media (max-width: 821.9px){
                    
                padding: 20px;
                width: 100%;
                }
                &:hover{
                    background: #034e8c;
                }
            }
    }
}
</style>