<template>
    <div class="videos">
        <div class="video" @click="videos[0] = !videos[0]">
            <p class="nomer">01</p>
            <div class="info">
                <h4>Lorem, ipsum dolor.</h4>
                <p>14 videos</p>
            </div>
            <icon><i class="fa-solid fa-arrow-right"></i></icon>
            <div class="video_open" v-if="videos[0]">
                <iframe  src="https://www.youtube.com/embed/XzLuMtDelGk?si=vl8IptrvGzPYOUP7" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
            </div>
        </div>
        <div class="video" @click="videos[1] = !videos[1]">
            <p class="nomer">02</p>
            <div class="info">
                <h4>Lorem, ipsum dolor.</h4>
                <p>14 videos</p>
            </div>
            <icon><i class="fa-solid fa-arrow-right"></i></icon>
            <div class="video_open" v-if="videos[1]">
                <iframe  src="https://www.youtube.com/embed/XzLuMtDelGk?si=vl8IptrvGzPYOUP7" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
            </div>
        </div>
        <div class="video" @click="videos[2] = !videos[2]">
            <p class="nomer">03</p>
            <div class="info">
                <h4>Lorem, ipsum dolor.</h4>
                <p>14 videos</p>
            </div>
            <icon><i class="fa-solid fa-arrow-right"></i></icon>
            <div class="video_open" v-if="videos[2]">
                <iframe  src="https://www.youtube.com/embed/XzLuMtDelGk?si=vl8IptrvGzPYOUP7" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
            </div>
        </div>
        <div class="video" @click="videos[3] = !videos[3]">
            <p class="nomer">04</p>
            <div class="info">
                <h4>Lorem, ipsum dolor.</h4>
                <p>14 videos</p>
            </div>
            <icon><i class="fa-solid fa-arrow-right"></i></icon>
            <div class="video_open" v-if="videos[3]">
                <iframe  src="https://www.youtube.com/embed/XzLuMtDelGk?si=vl8IptrvGzPYOUP7" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
            </div>
        </div>
        <div class="video" @click="videos[4] = !videos[4]">
            <p class="nomer">05</p>
            <div class="info">
                <h4>Lorem, ipsum dolor.</h4>
                <p>14 videos</p>
            </div>
            <icon><i class="fa-solid fa-arrow-right"></i></icon>
            <div class="video_open" v-if="videos[4]">
                <iframe  src="https://www.youtube.com/embed/XzLuMtDelGk?si=vl8IptrvGzPYOUP7" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return {
            videos: [false, false, false, false, false,]}
    }
}
</script>

<style lang="scss" scoped>

.videos{
    @media (min-width: 723px){
            margin-top: 160px;
        }
        @media (max-width: 722.9px){
            margin-top: 80px;
        }
    
}
.video{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 40px 0;
    cursor: pointer;
    transition: all 1s ease-in;
    flex-wrap: wrap;

    &:not(:last-of-type){
        border-bottom: 1px solid #666;
    }
    &:hover{
        background: #1d1d1d;
        i{
            transform: rotate(90deg);
        }
    }
    .video_open {
        width: 90%;
        height: 0;
        padding-bottom: 56.25%; 
        margin: 30px auto 0;
        position: relative;

        iframe{
            position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        }
    }
    .nomer{
        color: #575757;
        font-weight: 600;
        font-size: 1.2em;
        margin-left: 20px;
    }
    h4{
        @media (min-width: 723px){
            font-size: 2.5em;
        }
        @media (max-width: 722.9px) and (min-width: 450px){
            font-size: 1.6em;
        }
        @media (max-width: 449.9px){
            font-size: 1.3em;
            max-width: 200px;
        }
        font-weight: 400;
    }

    p{
        color: #6f6f6f;
        margin-top: 4px;
    }
    i{
        margin-right: 20px;
        transition: all 1s ease;
    }
}

</style>

