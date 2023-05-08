<template>
      <svg viewBox="0 0 160 100" class="blue-curve">
        <path d="M 0 0 C 100 0 -50 180 500 60 L 0 500 L 0 0" fill="hsl(243, 100%, 72%)" opacity="0.8"></path>
      </svg>

      <div class="confettis">
        <div class="springle springle-left"></div>
        <div class="springle springle-center"></div>
        <div class="springle springle-right"></div>
      </div>

      <div class="yellow-circle"></div>
      
       <svg id="svg-blob" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg" class="red-blob">
        <path fill="#ED667FFF" d="M25.5,-30.5C28.3,-22.8,22.4,-11.4,20.9,-1.5C19.4,8.4,22.2,16.8,19.5,22.4C16.8,28.1,8.4,31,-0.2,31.2C-8.8,31.5,-17.6,29,-24.8,23.3C-32,17.6,-37.5,8.8,-35.1,2.4C-32.7,-4,-22.3,-7.9,-15.1,-15.6C-7.9,-23.2,-4,-34.6,3.7,-38.3C11.4,-42,22.8,-38.1,25.5,-30.5Z" width="100%" height="100%" transform="translate(50 50)" stroke-width="0" style="transition: all 0.3s ease 0s;"></path>
      </svg>
</template>

<style scoped lang="scss">


    .red-blob {
      position: absolute;
      right: -150px;
      bottom: -150px;
      width: 350px;
    }

    .blue-curve {
      position: absolute;
      bottom: 0;
      left: 0;
    }

    .yellow-circle {
      position: absolute;
      bottom: 15px;
      left: -70px;
      height: 135px;
      width: 135px;
      background-color: #ffaf7e;
      border-radius: 50%;
    }

    .confettis {
      position: absolute;
      bottom: 70px;
      right: 50px;
      width: 50px;
      z-index: 2;

      .springle {
        position: absolute;
        background: color(neutral, white);
        width: 20px;
        height: 5px;
        border-radius: 50px;

        &-left {
          transform: rotate(-45deg);
          left: -15px;
          bottom: 35px;
        }

        &-center {
          transform: rotate(110deg);
          bottom: 0;
        }

        &-right {
          transform: rotate(35deg);
          bottom: 25px;
          right: 10px;
        }
      }
    }
  </style>