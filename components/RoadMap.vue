<template>
    <div>
        <div class="roadmap">
            <h2 class="roadmap__header">Road Map</h2>
            <div class="roadmap__paragraph">
                <figure class="roadmap__artboard">

                </figure>
                <!--<p>
                    Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Donec rutrum congue leo eget malesuada. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Pellentesque in ipsum id orci porta dapibus. Mauris blandit aliquet elit, eget tincidunt nibh pulvinar a.
                </p>-->
            </div>
            <div class="roadmap__seemap">
                <span class="roadmap__seemap--btn">
                 <!--   <button>See map</button>-->
                </span>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "RoadMap"
    }
</script>

<style scoped lang="scss">
  @function scaleValue($value) {
    @return calc(
      #{$value} * (clamp(350px, 100vw, 3840px) / var(--ideal-viewport-width))
    );
  }
  
  .roadmap {
     padding: #{scaleValue(75)} #{scaleValue(130)};
     padding-bottom: #{scaleValue(10)};

      &__header {
          color: #fff;
          text-align: center;
          font-size: #{scaleValue(40)};
          margin-bottom: #{scaleValue(50)};
      }   

      &__paragraph {
          font-size: #{scaleValue(25)};
          color: #fff;
          display: flex;
          justify-content: center;
          align-items: center;
      } 

      &__artboard {
        background-image: url("@/assets/imgs/artboard.png");
        background-size: cover;
        background-position: top;
        position: relative;

        height: #{scaleValue(900)};
        width: #{scaleValue(1500)};
      }

      &__seemap {
          display: flex;
          justify-content: center;
          align-items: center;
          margin-top: #{scaleValue(55)};
          

          /*&--btn {
              display: inline-block;
              border-radius: 3rem;
              background: #C4C4C4;
              margin-top: #{scaleValue(50)};
              transition: all .3s ease-in;

              &:hover {
                transform: translateY(#{scaleValue(-2)});
              } 

              & button {
                  font-weight: 600;
                  font-size: #{scaleValue(30)};

                  &,
                  &:focus,
                  &:hover {
                      border: none;
                      outline: none;
                      background: transparent;
                      padding: #{scaleValue(20)} #{scaleValue(100)};
                      cursor: pointer;
                  }
              }
          }*/
      }
  }
  </style>