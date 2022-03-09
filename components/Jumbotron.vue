<template>
    <div class="rebel__jumbotron">
        <div class="rebel__jumbotron--top">
            <div class="rebel__jumbotron--left">
                <div class="rebel__jumbotron--name">
                    <figure>
                        <img src="@/assets/imgs/REBELLION.png"/>
                    </figure>
                </div>
            </div>
            <div class="rebel__jumbotron--right">
                <span class="rebel__jumbotron--rightbtn" @click="scroll('team')">Team</span>
                <span class="rebel__jumbotron--rightbtn" @click="scroll('roadmap')">Roadmap</span>
                <div class="rebel__jumbotron--socials">
                    <span @click='openLink("https://discord.gg/Hv39nv6HQH")'>
                        <svg xmlns="http://www.w3.org/2000/svg" width="48" height="52" viewBox="0 0 48 52" fill="none">
                            <g filter="url(#filter0_d_15_140)">
                            <path d="M24 44C35.0457 44 44 35.0457 44 24C44 12.9543 35.0457 4 24 4C12.9543 4 4 12.9543 4 24C4 35.0457 12.9543 44 24 44Z" fill="#5865F2"/>
                            <path d="M32.8566 15.781C31.1358 15.026 29.2904 14.4697 27.3609 14.1511C27.3257 14.1449 27.2906 14.1603 27.2725 14.191C27.0352 14.5946 26.7723 15.1212 26.5882 15.5351C24.513 15.238 22.4483 15.238 20.4156 15.5351C20.2315 15.112 19.959 14.5946 19.7206 14.191C19.7025 14.1613 19.6674 14.1459 19.6323 14.1511C17.7039 14.4686 15.8585 15.0249 14.1366 15.781C14.1216 15.7872 14.1089 15.7974 14.1004 15.8107C10.6001 20.8112 9.64116 25.6888 10.1116 30.506C10.1137 30.5295 10.1275 30.5521 10.1467 30.5664C12.4561 32.1881 14.6932 33.1727 16.8887 33.8253C16.9238 33.8355 16.9611 33.8232 16.9834 33.7956C17.5028 33.1174 17.9657 32.4023 18.3627 31.6503C18.3861 31.6062 18.3637 31.554 18.3158 31.5366C17.5815 31.2702 16.8823 30.9454 16.2097 30.5766C16.1565 30.5469 16.1522 30.4742 16.2012 30.4393C16.3427 30.3379 16.4843 30.2324 16.6194 30.1258C16.6439 30.1064 16.678 30.1023 16.7067 30.1146C21.1254 32.0437 25.9092 32.0437 30.2758 30.1146C30.3046 30.1013 30.3386 30.1054 30.3642 30.1248C30.4994 30.2314 30.6409 30.3379 30.7835 30.4393C30.8324 30.4742 30.8292 30.5469 30.776 30.5766C30.1034 30.9526 29.4042 31.2702 28.6688 31.5356C28.6209 31.553 28.5997 31.6062 28.6231 31.6503C29.0285 32.4012 29.4915 33.1163 30.0013 33.7945C30.0226 33.8232 30.0608 33.8355 30.096 33.8253C32.3022 33.1727 34.5392 32.1881 36.8486 30.5664C36.8688 30.5521 36.8816 30.5305 36.8837 30.507C37.4467 24.9378 35.9408 20.1002 32.8917 15.8117C32.8843 15.7974 32.8715 15.7872 32.8566 15.781ZM19.0225 27.5728C17.6922 27.5728 16.596 26.4049 16.596 24.9706C16.596 23.5364 17.6709 22.3685 19.0225 22.3685C20.3847 22.3685 21.4703 23.5466 21.449 24.9706C21.449 26.4049 20.3741 27.5728 19.0225 27.5728ZM27.9941 27.5728C26.6638 27.5728 25.5676 26.4049 25.5676 24.9706C25.5676 23.5364 26.6425 22.3685 27.9941 22.3685C29.3563 22.3685 30.4419 23.5466 30.4206 24.9706C30.4206 26.4049 29.3563 27.5728 27.9941 27.5728Z" fill="white"/>
                            </g>
                            <defs>
                            <filter id="filter0_d_15_140" x="-4" y="0" width="56" height="56" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">
                            <feFlood flood-opacity="0" result="BackgroundImageFix"/>
                            <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>
                            <feOffset dy="4"/>
                            <feGaussianBlur stdDeviation="2"/>
                            <feComposite in2="hardAlpha" operator="out"/>
                            <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0"/>
                            <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_15_140"/>
                            <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_15_140" result="shape"/>
                            </filter>
                            </defs>
                        </svg>
                    </span>
                    <span @click='openLink("https://twitter.com/TherebellionNFT")'>
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

        <div class="rebel__jumbotron--bottom">
            <div class="rebel__jumbotron--text">
                <div class="rebel__jumbotron--text1">
                    <span>
                        <p>When they say go right,</p>
                    </span>
                    <span>
                        <p>We go left.</p>
                    </span>
                    <span>
                        <p>We forge our own path.</p>
                    </span>
                </div>
                <div class="rebel__jumbotron--text2">
                    <span>
                        <p>4444 hand painted NFTs ready to</p>
                    </span>
                    <span>
                        <p>take web3 by storm.</p>
                    </span>
                </div>
                <div class="rebel__jumbotron--text3">
                    <span @click='openLink("https://discord.com/invite/SmtEVXEpgN")' class="rebel__jumbotron--presale">
                        <img src="@/assets/imgs/presale.svg"/>
                    </span>
                </div>
            </div>
            <div class="rebel__jumbotron--imgs">
                <figure class="rebel__jumbotron--imgs" v-bind:class="{ active: currentItem === 3 }">
                    <img src="@/assets/imgs/female-character-144.png"/>
                </figure>
                <figure class="rebel__jumbotron--imgs" v-bind:class="{ active: currentItem === 2 }">
                    <img src="@/assets/imgs/male--character-142.png"/>
                </figure>
                <figure class="rebel__jumbotron--imgs" v-bind:class="{ active: currentItem === 1 }">
                    <img src="@/assets/imgs/male--character-237.png"/>
                </figure>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Jumbotron',
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
            }, 1000);
        },
        openLink(url) {
            window.open(url);
        },
        scroll(id) {
            var element = document.getElementById(`${id}`);

            element.scrollIntoView({behavior: "smooth"});
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

    .rebel__jumbotron {
        height: #{scaleValue(1000)};
        color: #fff;
        padding: #{scaleValue(75)} #{scaleValue(130)}; //3rem 10rem;
        overflow: hidden;


        &--name {
            display: inline-block;
            height: #{scaleValue(30)};
            width: #{scaleValue(40)};
            position: relative;
            cursor: pointer;

            & figure {
                position: absolute;
                top: #{scaleValue(-30)};;
                left: #{scaleValue(-70)};;
                height: #{scaleValue(150)};
                width: #{scaleValue(350)};
            }

            & img {
                object-fit: cover;
                height: 100%;
                width: 100%;
            }
        }

        &--socials {
            display: flex;
            align-items: center;
            margin-left: #{scaleValue(70)};
            transform: translateY(#{scaleValue(-8)});

            & span {
                display: inline-block;
                cursor: pointer;
                
                &:nth-child(2) {
                    margin-left: #{scaleValue(30)};
                }
            }
        }

        &--top {
            display: flex;
            justify-content: space-between;
            position: relative;
            z-index: 1;
        }

        &--right {
            font-size: #{scaleValue(27)};
            display: flex;

            & span {
                display: inline-block;
                
                font-weight: 500;
                cursor: pointer;

                &.rebel__jumbotron--rightbtn {
                    margin-left: #{scaleValue(70)};
                }
            }
        }

        &--bottom {
            margin-top: #{scaleValue(135)};
            font-weight: 500;
            display: flex;
            justify-content: space-between;
        }

        &--text {
            position: relative;
            z-index: 1;
            margin-top: #{scaleValue(90)};
            flex: 1 1;
        }

        &--text1 {
            font-size: #{scaleValue(40)};
        }

        &--text2 {
            margin-top: 1.4rem;
            font-size: #{scaleValue(35)};
            font-weight: 200;
            opacity: .7;
        }

        &--presale {
            display: block;
            margin-top: #{scaleValue(55)};
            width: #{scaleValue(250)};
            height: #{scaleValue(65)};
            cursor: pointer;

            & img {
                object-fit: cover;
                height: 100%;
                width: 100%;
            }
        }

        &--imgs {
            position: relative;
            flex: 1 1;
            transform: translate(#{scaleValue(0)}, #{scaleValue(-150)});

            & figure {
                position: absolute;
                top: 0;
                right: 0;
                height: #{scaleValue(1000)};
                width: #{scaleValue(1000)};
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
    }
</style>
