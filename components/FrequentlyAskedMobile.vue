<template>
    <div class="frequentlyaskedmobile">
        <h2 class="frequentlyaskedmobile__header">Frequently Asked Question</h2>
        <div class="frequentlyaskedmobile__items">
            <div v-for="question in questions" class="frequentlyaskedmobile__item">
                <div class="frequentlyaskedmobile__item--top">
                    <div class="frequentlyaskedmobile__item--question">
                        {{ question.question }}
                    </div>
                </div>
                <div class="frequentlyaskedmobile__item--answer">
                    {{ question.answer }}
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "FrequentlyAskedMobile",
        data() {
            return {
                currentquestion: 0,
                questions: [
                    {
                        id: "1",
                        question: "Wen mint?",
                        answer: "Wen mint : Our presale will go live on 22nd of march while public sales will  happen on 23rd of march"
                    },
                    {
                        id: "2",
                        question: "How much?",
                        answer: "Each REBEL in the collection will go for 0.044 eth"
                    },
                    {
                        id: "3",
                        question: "Do I own the IP of the minted NFT?",
                        answer: "Yes. Holding each REBEL comes with the rights to its intellectual property and also to create and distribute derivatives. You also get a lifetime access to a suit of ever evolving and up to date NFT minting tools and WEB3 infra"
                    },
                    {
                        id: "4",
                        question: "How many can I mint?",
                        answer: "Each Redlisted wallet can mint up to 3 REBELS"
                    }
                ]
            }
        },
        methods: {
            reveal(id) {
                this.currentquestion === id ? this.currentquestion = 0 : this.currentquestion = id;
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

  .frequentlyaskedmobile {
      padding-top: #{scaleValue(50)};

      &__header {
          color: #fff;
          text-align: left;
          font-size: #{scaleValue(90)};
          margin-bottom: #{scaleValue(130)};
      }

      &__item {
          background: #fff;
          border-radius: 1rem;
          padding: #{scaleValue(95)};
          margin-bottom: #{scaleValue(130)};

          &--top {
              position: relative;
          }

          &--question {
              font-weight: 600;
              font-size: #{scaleValue(90)};
              margin-bottom: #{scaleValue(70)};
          }

          &--answer {
              line-height: #{scaleValue(100)};
              font-size: #{scaleValue(65)};
          }
      }
  }
</style>