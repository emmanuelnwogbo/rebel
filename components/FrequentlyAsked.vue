<template>
    <div>
    <div>
        <div class="frequentlyasked">
            <h2 class="frequentlyasked__header">Frequently Asked Questions</h2>
            <div class="frequentlyasked__items">
                <div v-for="question in questions" class="frequentlyasked__item" @click="reveal(question.id)">
                    <div class="frequentlyasked__item--question">
                        {{ question.question }}
                    </div>
                    <div class="frequentlyasked__item--answer" v-if="currentquestion === question.id">
                        {{ question.answer }}
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
    export default {
        name: 'FrequentlyAsked',
        data() {
            return {
                currentquestion: 0,
                questions: [
                    {
                        id: "1",
                        question: "Wen mint?",
                        answer: "Wen mint : Our presale will go live on 22nd of march while public sales will  happen on 10 of April"
                    },
                    {
                        id: "2",
                        question: "How much?",
                        answer: "Each REBEL in the collection will go for 0.044 eth"
                    },
                    {
                        id: "3",
                        question: "Do I own the IP of the minted NFT?",
                        answer: "Yes. Holding each REBEL comes with the rights to its intellectual property and also to create and distribute derivatives"
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
  
  .frequentlyasked {
      padding: #{scaleValue(75)} #{scaleValue(130)};
      padding-bottom: #{scaleValue(65)};

      &__header {
          color: #fff;
          text-align: center;
          font-size: #{scaleValue(40)};
          margin-bottom: #{scaleValue(50)};
      }

      &__item {
          background: #fff;
          border-radius: 3rem;
          padding: #{scaleValue(40)};
          font-size: #{scaleValue(25)};
          margin-bottom: #{scaleValue(50)};
          cursor: pointer;
          transition: all .3s ease-in;

          &:hover {
              transform: translateY(#{scaleValue(-5)});
          }

          &:nth-last-child(1){
             margin-bottom: #{scaleValue(0)};
          }

          &--question {
              font-weight: 600;
              font-size: #{scaleValue(30)};
              margin-bottom: #{scaleValue(25)};
          }

          &--answer {
              line-height: #{scaleValue(35)};
          }
      }
  }
  </style>