<template>
    <div class="team">
        <h2 class="team__header">Meet the Core Team</h2>  
        <div class="team__items">
            <div class="team__item">
                <div class="team__item--left">
                    <div class="team__item--flipper">
                        <Flipper />
                    </div>
                    <figure class="team__item--fig">
                        <img src="@/assets/imgs/samson.png"/>
                    </figure>
                </div>
                <div class="team__item--right">
                    <h3>Samson</h3>
                    <p>founder/artist</p>
                    <span class="team__item--social" @click='openLink("https://twitter.com/kvngspice_")'>
                        <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="45" height="45" viewBox="0 0 45 45" fill="none">
                            <rect width="45" height="45" fill="url(#pattern0)"/>
                            <defs>
                            <pattern id="pattern0" patternContentUnits="objectBoundingBox" width="1" height="1">
                            <use xlink:href="#image0_15_143" transform="scale(0.0104167)"/>
                            </pattern>
                            <image id="image0_15_143" width="96" height="96" xlink:href="data:image/png;base64,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"/>
                            </defs>
                        </svg>
                    </span>
                </div>
            </div>
             <div class="team__item">
                <div class="team__item--left">
                    <div class="team__item--flipper">
                        <Flipper />
                    </div>
                    <figure class="team__item--fig">
                        <img src="@/assets/imgs/imam.png"/>
                    </figure>
                </div>
                <div class="team__item--right">
                    <h3>Imam</h3>
                    <p>project manager</p>
                    <span class="team__item--social" @click='openLink("https://twitter.com/theimamadetona")'>
                        <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="45" height="45" viewBox="0 0 45 45" fill="none">
                            <rect width="45" height="45" fill="url(#pattern0)"/>
                            <defs>
                            <pattern id="pattern0" patternContentUnits="objectBoundingBox" width="1" height="1">
                            <use xlink:href="#image0_15_143" transform="scale(0.0104167)"/>
                            </pattern>
                            <image id="image0_15_143" width="96" height="96" xlink:href="data:image/png;base64,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"/>
                            </defs>
                        </svg>
                    </span>
                </div>
            </div>
             <div class="team__item">
                <div class="team__item--left">
                    <div class="team__item--flipper">
                        <Flipper />
                    </div>  
                    <figure class="team__item--fig">
                        <img src="@/assets/imgs/emmanuel.png"/>
                    </figure>
                </div>
                <div class="team__item--right">
                    <h3>Emmanuel</h3>
                    <p>engineering</p>
                    <span class="team__item--social" @click='openLink("https://twitter.com/nerdyemmanuel")'>
                        <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="45" height="45" viewBox="0 0 45 45" fill="none">
                            <rect width="45" height="45" fill="url(#pattern0)"/>
                            <defs>
                            <pattern id="pattern0" patternContentUnits="objectBoundingBox" width="1" height="1">
                            <use xlink:href="#image0_15_143" transform="scale(0.0104167)"/>
                            </pattern>
                            <image id="image0_15_143" width="96" height="96" xlink:href="data:image/png;base64,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"/>
                            </defs>
                        </svg>
                    </span>
                </div>
            </div>
             <div class="team__item">
                <div class="team__item--left">
                    <div class="team__item--flipper">
                        <Flipper />
                    </div>
                    <figure class="team__item--fig">
                        <img src="@/assets/imgs/kate.png"/>
                    </figure>
                </div>
                <div class="team__item--right">
                    <h3>Kate</h3>
                    <p>community</p>
                    <span class="team__item--social" @click='openLink("https://twitter.com/octomint2000")'>
                        <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="45" height="45" viewBox="0 0 45 45" fill="none">
                            <rect width="45" height="45" fill="url(#pattern0)"/>
                            <defs>
                            <pattern id="pattern0" patternContentUnits="objectBoundingBox" width="1" height="1">
                            <use xlink:href="#image0_15_143" transform="scale(0.0104167)"/>
                            </pattern>
                            <image id="image0_15_143" width="96" height="96" xlink:href="data:image/png;base64,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"/>
                            </defs>
                        </svg>
                    </span>
                </div>
            </div>
        </div>  
    </div>
</template>

<script>
    export default {
        name: "Team",
        methods: {
            openLink(url) {
                window.open(url);
            }
        }
    }
</script>

<style scoped lang="scss">
  @function scaleValue($value) {
    @return calc(
      #{$value} * (clamp(350px, 100vw, 3840px) / var(--ideal-viewport-width))
    );
  }

  .team {
     padding: #{scaleValue(75)} #{scaleValue(130)};
     padding-bottom: #{scaleValue(60)};
     padding-top: 0;

      &__header {
          color: #fff;
          text-align: center;
          font-size: #{scaleValue(40)};
          margin-bottom: #{scaleValue(50)};
      }

      &__items {
          display: flex;
          justify-content: space-between;
      }

      &__item {
          background: #C4C4C4;
          padding: #{scaleValue(10)};
          display: flex;
          align-items: center;
          width: #{scaleValue(320)};
          border-radius: 1rem;
          flex-shrink: 0;
          cursor: pointer;

          &:hover > &--left > &--flipper {
              opacity: 1;
          }

          &--left {
              margin-right: #{scaleValue(15)};
              position: relative;
          }

          &--flipper {
              position: absolute;
              top: 0;
              left: 0;
              width: 100%;
              height: 100%;
              z-index: 2;
              opacity: 0;
              transition: all .3s ease-in;
          }

          &--fig {
              height: #{scaleValue(152)};
              width: #{scaleValue(140)};
              border-radius: 1rem;
              overflow: hidden;

              & img {
                  height: 100%;
                  width: 100%;
                  object-fit: cover;
              }
          }

          &--right {
              height: 100%;
              padding-top: #{scaleValue(40)};
              text-transform: uppercase;

              & h3 {
                  font-size: #{scaleValue(17)};
                  margin-bottom: #{scaleValue(5)};
              }

              & p {
                  font-size: #{scaleValue(13)};
                  font-weight: 500;
              }
          }

          &--social {
              display: inline-block;
              margin-top: #{scaleValue(10)};
              cursor: pointer;
              transition: all .3s ease-in;

              &:hover {
                transform: translateY(#{scaleValue(-2)});
              } 

              & svg {
                  height: #{scaleValue(35)};
                  width: #{scaleValue(35)};
              }
          }
      }
  }
</style>