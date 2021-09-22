<template>
  <div class="loader">
    <div class="logo">
      <img src="https://i.ibb.co/mNM16mw/logo-spotify.png" alt="Logo Spotify">
      <img src="https://i.ibb.co/QnDYY6v/Spotify-Logo-CMYK-Green.png" alt="Spotify Text">
    </div>
    <div class="lds"><div></div><div></div><div></div><div></div><div></div><div></div><div></div><div></div><div></div>
    </div>    
  
  </div>
</template>

<script>
export default {
  name: 'Loader'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import '../styles/vars';
  
  .loader {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    img {
      height: 200px;

      &:first-child {
        animation: rotate 0.6s linear infinite both;
      }

      @keyframes rotate {
        0% {
          -webkit-transform: rotate(0);
                  transform: rotate(0);
        }
        100% {
          -webkit-transform: rotate(360deg);
                  transform: rotate(360deg);
        }
      }
    }



    .lds {
    display: inline-block;
    position: relative;
    width: 80px;
    height: 80px;

      div {
        display: inline-block;
        position: absolute;
        left: 8px;
        width: 16px;
        background: #1ed760;
        animation: loading 1s cubic-bezier(0, 0.5, 0.5, 1) infinite;
        
        &:nth-child(1) {
          left: 8px;
          animation-delay: -0.96s;
        }  
        
        &:nth-child(2) {
          left: 32px;
          animation-delay: -0.84s;
        }

        &:nth-child(3) {
          left: 56px;
          animation-delay: -0.72s;
        }
        
        &:nth-child(4) {
          left: 80px;
          animation-delay: -0.60s;
        }  
        
        &:nth-child(5) {
          left: 104px;
          animation-delay: -0.48s;
        }

        &:nth-child(6) {
          left: 128px;
          animation-delay: -0.36s;
        }
        
        &:nth-child(7) {
          left: 152px;
          animation-delay: -0.24s;
        }  
        
        &:nth-child(8) {
          left: 176px;
          animation-delay: -0.12s;
        }

        &:nth-child(9) {
          left: 200px;
          animation-delay: 0;
        }
      }
      
      @keyframes loading {
        0% {
          top: 8px;
          height: 64px;
        }
        50%, 100% {
          top: 24px;
          height: 32px;
        }
      }
    }
  }

</style>
