<script lang="ts">
  export let nachoColorLeft: string, nachoColorRight: string;
</script>

<style lang="scss">
  .nacho-container {
    display: flex;
    justify-content: center;
    align-items: center;
    transform: translateX(-40px);

    $size: 250px;

    .nacho-shape {
      border-radius: 90% 10% 22% 78% / 31% 9% 91% 69%;
      width: $size;
      height: $size;
      color: white;
      font-size: calc(#{$size} / 2);
      display: flex;
      justify-content: center;
      align-items: center;

      .material-icons {
        font-size: calc(#{$size} / 2);
      }
    }

    #nacho-left {
      transform: rotate(20deg) translateX(40px);
      z-index: 50;
      animation: move-from-left 3s;

      span {
        transform: rotate(360deg) translate(5px, -30px);
      }

      :nth-child(1) {
        transform: translate(-20px, -40px);
      }
      :nth-child(2) {
        transform: translate(-20px, -45px);
      }
    }

    #nacho-right {
      transform: rotate(170deg);
      z-index: 40;
      animation: move-from-right 3s;

      span {
        transform: rotate(210deg);
      }
    }

    .circle {
      width: 15px;
      height: 15px;
      border-radius: 50%;
      margin: 2px;
      opacity: 0;
      animation: fade-circle 2s 3s forwards;
    }
  }

  $distance: 800px;
  @keyframes move-from-left {
    from {
      transform: rotate(0deg) translateX(-#{$distance});
    }

    to {
      transform: rotate(20deg) translateX(40px);
    }
  }
  @keyframes move-from-right {
    from {
      transform: translateX($distance) rotate(120deg);
    }

    to {
      transform: translateX(0px) rotate(170deg);
    }
  }
  @keyframes fade-circle {
    from {
      opacity: 0;
    }

    to {
      opacity: 1;
    }
  }
</style>

<div class="nacho-container">
  <div
    class="nacho-shape"
    id="nacho-left"
    style={`background-color:${nachoColorLeft}`}
  >
    <div class="circle" style={`background-color:${nachoColorRight}`} />
    <div class="circle" style={`background-color:${nachoColorRight}`} />
    <span>ꜩ</span>
  </div>
  <div
    class="nacho-shape"
    id="nacho-right"
    style={`background-color:${nachoColorRight}`}
  >
    <span class="material-icons"> currency_bitcoin </span>
  </div>
</div>
