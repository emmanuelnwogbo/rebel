<template>
    <div class="roadmapmobile" id="roadmapmobile">
        <!--<h2 class="roadmapmobile__header">Road Map</h2>-->
        <div class="roadmapmobile__paragraph">
            <figure class="roadmapmobile__artboard">

            </figure>
            <!--<p>
                Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Donec rutrum congue leo eget malesuada. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Pellentesque in ipsum id orci porta dapibus. Mauris blandit aliquet elit, eget tincidunt nibh pulvinar a.
            </p>-->
        </div>
      <!--  <div class="roadmapmobile__seemap">
            <span class="roadmapmobile__seemap--btn">
               <button>See map</button>
            </span>
        </div>-->
    </div>
</template>

<script>
    export default {
        name: "RoadMapMobile"
    }
</script>

<style scoped lang="scss">
  @function scaleValue($value) {
    @return calc(
      #{$value} * (clamp(350px, 100vw, 3840px) / var(--ideal-viewport-width))
    );
  }

  .roadmapmobile {
      padding-top: #{scaleValue(80)};
      margin-top: #{scaleValue(30)};

      &__header {
          color: #fff;
          text-align: left;
          font-size: #{scaleValue(90)};
          margin-bottom: #{scaleValue(130)};
      }

      &__paragraph {
          color: #fff;
          line-height: #{scaleValue(100)};
          font-size: #{scaleValue(65)};
      }

      &__artboard {
        background-image: url("@/assets/imgs/artboard.png");
        background-size: cover;
        background-position: top;
        position: relative;

        height: #{scaleValue(1000)};
        width: #{scaleValue(1500)};
      }

      &__seemap {

          &--btn {
              display: inline-block;
              border-radius: 3rem;
              background: #C4C4C4;
              margin-top: #{scaleValue(120)};
              overflow: hidden;
              background: #fff;
              padding: #{scaleValue(50)} #{scaleValue(140)};

              & button {

                  &,
                  &:focus,
                  &:hover {
                      outline: none;
                      border: none;
                      background: transparent;
                      font-weight: 600;
                      font-size: #{scaleValue(75)};
                      height: 100%;
                      width: 100%;
                      color: #000000;
                  }
              }
          }
      }
  }
</style>