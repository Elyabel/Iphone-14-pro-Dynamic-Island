<template>
    <div id="iphone">

        <!-- volume & power buttons -->
        <div class="leftSideButtons">
            <div></div>
            <div></div>
            <div></div>
            <div></div> <!--power button-->
        </div>

        <!-- top left icons -->
        <div class="leftIcons">
            <p>Free</p>
        </div>

        <!-- Dynamic Island -->
        <div class="DynamicIsland" @mousedown="showDynamicContent" @mouseup="hideDynamicContent">
            <div class="dynamicContent">
                <img src="themove.jpeg" class="musicPic">
                <div class="musicInfo">
                    <p><b>THE MOVE</b></p>
                    <p class="musicAuthor">Space Rangers</p>
                </div>
                <img src="musicWaves.gif" class="musicWaves">
                <div class="playerBar">
                    <p>1:20</p>
                    <div class="playerProgressBar">
                        <div class="Progress"></div>
                    </div>
                    <p>-1:48</p>
                </div>
                <div class="Player">
                    <img src="backward_icon.png">
                    <img src="pause_icon.png">
                    <img src="forward_icon.png">
                    <img src="airplayaudio_icon.png">
                </div>
            </div>
        </div>

         <!-- top right icons -->
        <div class="rightIcons">
            <img src="cellularbars_icon.png">
            <img src="wifi_icon.png">
            <img src="battery_icon.png">
        </div>

        <!-- Date/Hours -->
        <div class="datehourscontent">
            <h4>Friday 29 June</h4>
            <h1>09:41</h1>
        </div>

        <!-- bottom left icon -->
        <div class="BleftIcons">
            <button><img src="flashlight_icon.png"></button>
        </div>

        <!-- bottom right icon -->
        <div class="BrightIcons">
            <button><img src="camera_icon.png"></button>
        </div>

        <!-- home bar -->
        <div class="homeBar"></div>
    </div>
</template>

<script setup>
import $ from 'jquery';

function showDynamicContent() {
    setTimeout(() => {
        $(".dynamicContent").fadeIn(100);
    }, 250)
}

function hideDynamicContent() {
    $(".dynamicContent").hide();
}
</script>

<style scoped>
#iphone {
    width: 380px;
    height: 800px;
    border: 10px solid black;
    border-radius: 50px;
    background-image: url('http://localhost:5173/iPhone_Wallpaper.jpg');
    background-size: cover;
    background-position: center;
}

.Player {
    margin-top: -15px;
    margin-left: 30px;
    position: absolute;
}

.Player img {
    width: 40px;
    margin: 20px;
}

.Player img:nth-child(2){
    width: 25px;
}

.Player img:nth-child(4){
    width: 25px;
}

.playerBar {
    width: 100%;
    display: flex;
    justify-content: center;
}

.playerBar p {
    font-size: 12px;
    color: #555555;
    margin: 12px;
}

.playerProgressBar {
    background: #353535;
    width: 200px;
    border-radius: 100px;
    height: 6px;
    margin-top: 18px;
}

.Progress {
    height: 6px;
    background: white;
    width: 33%;
    border-radius: 100px 0px 0px 100px;
}

.musicPic {
    border-radius: 10px;
    width: 60px;
    float: left;
}

.musicInfo {
    text-align: left;
    margin-top: -10px;
    margin-left: 75px;
    padding-left: 5px;
    width: 115px;
}

.musicAuthor {
    color: #656565;
    margin-top: -20px;
}

.musicWaves {
    width: 20px;
    float: right;
    margin-top: -60px;
}

.leftSideButtons {
    position: absolute;
    height: 300px;
    margin-left: -13px;
    margin-top: 160px;
}

.leftSideButtons div {
    background: #93869f;
    width: 3px;
    height: 20px;
    display: block;
    border-radius: 5px 0px 0px 5px;
}

.leftSideButtons div:nth-child(1) {
   margin-top: -40px;
   position: absolute;
}

.leftSideButtons div:nth-child(n+2) {
    margin-top: 20px;
    height: 50px;
}

.leftSideButtons div:nth-child(3) {
    margin-top: -40px;
    margin-left: 404px;
    position: absolute;
    border-radius: 0px 5px 5px 0px;
    height: 80px;
 }

.datehourscontent {
    width: 380px;
    height: 130px;
    position: absolute;
    margin-top: 50px;
    color: #ffffffab;
}
.datehourscontent h4 {
    font-weight: 600;
    font-size: 17px;
}
.datehourscontent h1 {
    font-size: 80px;
    margin-top: -30px;
    font-weight: 600;
}

.DynamicIsland {
    width: 100px;
    height: 30px;
    background-color: black;
    border-radius: 35px;
    transition: all .3s ease-in-out;
    position: fixed;
    left: 50%;
    margin-top: 10px;
    transform: translateX(-50%);
    z-index: 2;
}
.DynamicIsland:hover {
    width: 180px;
}
.DynamicIsland:active {
    width: 360px;
    height: 200px;
}

.dynamicContent {
    display: none;
    padding: 30px;
}

.leftIcons {
    float: left;
    align-items: center;
    display: flex;
    margin-left: 50px;
    font-weight: bold;
}

.rightIcons {
    float: right;
    align-items: center;
    display: flex;
    margin-right: 20px;
    margin-top: 20px;
}
.rightIcons img {
    width: 18px;
    margin: 5px;
}
.rightIcons img:nth-child(3) {
    width: 25px;
}

.BleftIcons {
    float: left;
    margin-top: 700px;
    margin-left: -35px;
}
.BleftIcons button {
    background-color: #979da293;
    width: 50px;
    height: 50px;
    border-radius: 100px;
}
.BleftIcons button img {
    width: 11px;
}

.BrightIcons {
    float: right;
    margin-top: 700px;
    margin-right: -50px;
}
.BrightIcons button {
    background-color: #979da293;
    width: 50px;
    height: 50px;
    border-radius: 100px;
    text-align: center;
    display: flex;
    align-items: center;
}
.BrightIcons button img {
    width: 23px;
    margin-left: 8px;
    margin-top: -2px;
}

.homeBar {
    width: 150px;
    height: 5px;
    background-color: #fff;
    position: absolute;
    margin-top: 790px;
    margin-left: 110px;
    border-radius: 20px;
}
</style>