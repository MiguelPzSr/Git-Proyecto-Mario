<template>
    <div class="marioV2">
        <div class="backmario"></div>
        <div class="floor"></div>
        <div class="arbusticos"></div>
        <div class="mario">
            <img src="../assets/mario.gif" alt="mario deberia estar">
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>
*{
  margin: 0;
  padding: 0;
}

::-webkit-scrollbar{
  display: none;
}

.backmario{
  height: 100vh;
  width: 500vw;
  background-image: url(../assets/back.png);
  background-size: contain;
  background-position: center;
  position: relative;
  overflow-x: hidden;
  background-repeat: repeat-x;
  animation: mountainmove 30s linear infinite;
}

@keyframes mountainmove
{
  100%{
    transform: translateX(-400px);
  }
}

.floor{
  height: 25px;
  width: 500%;
  display: block;
  background-image: url(../assets/ground.png);
  position: absolute;
  bottom: -100;
  left: 0;
  right: 0;
  z-index: 1;
  background-repeat: repeat-x;
  animation: groundmove 15s linear infinite;
}

@keyframes groundmove
{
  100%{
    transform: translateX(-700px);
  }
}

.arbusticos{
  height: 250px;
  width: 500%;
  background-image: url(../assets/bushes.png);
  position: absolute;
  bottom: -309px;
  left: 0;
  right: 0;
  display: block;
  z-index: 1;
  background-repeat: repeat-x;
  animation: arbusticosmove 15s linear infinite;
}

@keyframes arbusticosmove
{
  100%{
    transform: translateX(-700px)
  }
}

.mario{
  width: 0px;
  left: 700px;
  bottom: -145px;
  position: absolute;
  z-index: 2;
}
</style>