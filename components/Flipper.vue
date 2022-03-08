<template>
    <div class="flipper">
        <div class="flipper__imgs">
            <figure class="flipper__img" v-bind:class="{ active: currentItem === 3 }">
                <img src="@/assets/imgs/female-character-144.png"/>
            </figure>
            <figure class="flipper__img" v-bind:class="{ active: currentItem === 2 }">
                <img src="@/assets/imgs/male--character-142.png"/>
            </figure>
            <figure class="flipper__img" v-bind:class="{ active: currentItem === 1 }">
                <img src="@/assets/imgs/male--character-237.png"/>
            </figure>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Flipper",
        data() {
            return {
                currentItem: 1,
            }
        },
        methods: {
            slide() {
                setInterval(()=> {
                    if (this.currentItem === 3) {
                        return this.currentItem = 1;
                    }

                        this.currentItem = this.currentItem +=1;
                }, 300);
            }
        },
        mounted() {
            this.slide();
        }        
    }
</script>

<style scoped lang="scss">
  @function scaleValue($value) {
    @return calc(
      #{$value} * (clamp(350px, 100vw, 3840px) / var(--ideal-viewport-width))
    );
  }
  
  .flipper {
      height: 100%;
      width: 100%;
      overflow: hidden;
      border-radius: 1rem;

      &__imgs {
        height: 100%;
        width: 100%;
        position: relative;
      }

      &__img {
        height: 100%;
        width: 100%;
        position: absolute;
        top: 0;
        right: 0;
        opacity: 0;
        transition: all .3s ease;

        &.active {
            opacity: 1;
        }

          & img {
            object-fit: cover;
            height: 100%;
            width: 100%;
          }
      }
  }
  </style>