<template>
  <div ref="home" class="home">
    <h1 ref="heroHeading" class="home__heading">
      <!-- A Nigerian Civil War Story. -->
      <div><span>A</span></div>
      <div>
        <span>N</span><span>i</span><span>g</span><span>e</span><span>r</span
        ><span>i</span><span>a</span><span>n</span>
      </div>
      <div>
        <span>C</span><span>i</span><span>v</span><span>i</span><span>l</span>
      </div>
      <div><span>W</span><span>a</span><span>r</span></div>
      <div>
        <span>S</span><span>t</span><span>o</span><span>r</span><span>y.</span>
      </div>
    </h1>
    <div ref="body" class="home__body">
      <p ref="subtext" class="home__subtext">
        We’re obsessed with helping a new generation of people understand the
        war that changed Nigeria, and how the world saw Africa, forever.
        Subscribe below to get updates on how we're trying to achieve this
        vision.
      </p>
      <form action="">
        <input
          type="email"
          required
          placeholder="We saved a spot for your email"
        />
        <button>Send</button>
      </form>
    </div>
    <div ref="sun" class="home__sun" @click="triggerPageAnimation()" />
  </div>
</template>

<script>
export default {
  mounted() {
    document.body.style.overflow = 'hidden'
    if (sessionStorage.getItem('triggeredHomepageAnimation') !== 'true') {
      this.handleMouseWheel()
      setTimeout(() => {
        this.$refs.sun.style.setProperty('--translate-y', '25%')
      }, 500)
    } else this.triggerPageAnimation()
  },
  destroyed() {
    document.body.style.background = '#282825'
    document.body.style.color = 'white'
    document.body.style.overflow = 'unset'
    document.documentElement.style.setProperty('--logo-wordmark-color', 'white')
    document.documentElement.style.setProperty('--link-underline', 'white')
  },
  methods: {
    triggerPageAnimation() {
      this.$refs.sun.style.setProperty('--translate-y', '-50%')
      this.$refs.sun.style.setProperty('--hover-translate-y', '-50%')
      this.$refs.sun.style.transformOrigin = '0 0'
      this.$refs.body.style.opacity = 1
      document.body.style.background = 'white'
      document.body.style.color = '#282825'
      document.documentElement.style.setProperty(
        '--logo-wordmark-color',
        '#282825'
      )
      document.documentElement.style.setProperty('--link-underline', '#282825')
      sessionStorage.setItem('triggeredHomepageAnimation', true)
    },
    handleMouseWheel() {
      // let listenToWheelEvent = true

      this.$refs.home.addEventListener('wheel', (e) => {
        // if (!listenToWheelEvent) return
        // listenToWheelEvent = false
        // default is -75
        if (e.wheelDeltaY <= -30) {
          this.triggerPageAnimation()
        }
        // else {
        //   let translateValue = (e.wheelDeltaY * -50) / -75

        //   if (translateValue < 35) {
        //     translateValue = 20
        //   }

        //   this.$refs.sun.style.setProperty(
        //     '--translate-y',
        //     `${translateValue}%`
        //   )
        //   this.$refs.sun.style.setProperty('--scale', 1.2)

        //   setTimeout(() => {
        //     this.$refs.sun.style.setProperty('--translate-y', '25%')
        //     this.$refs.sun.style.setProperty('--scale', 1)
        //     listenToWheelEvent = true
        //   }, 150)
        // }
      })
    },
  },
}
</script>

<style lang="scss" scoped>
.home {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  min-height: inherit;
  height: 100vh;
  // position: absolute;
  // top: 0;
  // width: 100%;
  position: relative;
  overflow: hidden;
  width: 100vw;
  left: calc(-50vw + 50%);
  margin-top: -6.2rem;

  @keyframes slide {
    to {
      transform: translateY(0%);
    }
  }

  @keyframes fade {
    to {
      opacity: 1;
    }
  }

  @keyframes animate-gradient {
    0% {
      background-position: 0 0;
    }
    50% {
      background-position: 350% 0;
    }
    100% {
      background-position: 0 0;
    }
  }

  &__sun {
    --transition-time: 1.6s;
    --translate-y: 80%;
    --hover-translate-y: 20%;
    --scale: 1;
    --hover-scale: 1.2;
    --size: 70.2rem;
    position: absolute;
    display: flex;
    flex-direction: column;
    width: var(--size);
    height: var(--size);
    background-color: var(--color-orange);
    border-radius: 100%;
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
    box-shadow: 4px 4px 35px 35px rgba(230, 169, 41, 0.25),
      -4px -4px 35px 35px rgba(230, 169, 41, 0.25);
    margin: auto auto;
    top: 50%;
    left: 50%;
    transform: scale(var(--scale)) translate(-50%, var(--translate-y));
    transition: var(--transition-time) $ease-out-expo;
    transform-origin: left;
    cursor: pointer;

    @include screen(small) {
      --scale: 0.7;
      --size: 64rem;
      --hover-scale: 0.7;
    }

    &:hover {
      transform: scale(var(--hover-scale))
        translate(-50%, var(--hover-translate-y));
    }

    &::before,
    &::after {
      border-radius: inherit;
      content: '';
      position: absolute;
      width: calc(100% + 6px);
      height: calc(100% + 6px);
      background: linear-gradient(
        45deg,
        rgba(230, 169, 41, 0.25),
        var(--color-orange),
        rgba(230, 169, 41, 0.25),
        var(--color-orange),
        rgba(230, 169, 41, 0.25),
        var(--color-orange),
        rgba(230, 169, 41, 0.25),
        var(--color-orange),
        rgba(230, 169, 41, 0.25),
        rgba(230, 169, 41, 0.25)
      );
      background-size: 400%;
      z-index: -1;
      transform: translateZ(0);
      animation: animate-gradient 20s linear infinite;
    }

    &::after {
      filter: blur(20px);
    }
  }

  &__heading {
    position: relative;
    font-size: 3.6rem;
    z-index: 3;

    @include screen(small) {
      font-size: 7vw;
      // font-size: 3rem;
    }

    div {
      display: inline-block;
    }

    span {
      --delay: 0.1s;
      position: relative;
      display: inline-block;
      transform: translateY(50%);
      opacity: 0;
      animation: slide 0.8s $ease-out-expo forwards var(--delay),
        fade 1s linear forwards var(--delay);

      @for $i from 1 through 9 {
        &:nth-child(#{$i}) {
          --delay: #{$i * 0.14s};
        }
      }
    }
  }

  &__body {
    display: flex;
    flex-direction: column;
    z-index: 3;
    opacity: 0;
    transition: 1.8s linear 1s;

    @include screen(small) {
      width: 90%;
    }
  }

  &__subtext {
    max-width: 52rem;
    margin-top: 2.6rem;
    line-height: 2.7rem;
    color: $color-dark;
    text-align: center;
    pointer-events: none;

    @include screen(small) {
      font-size: 1.6rem;
      line-height: 2.5rem;
    }
  }

  form {
    display: flex;
    justify-content: space-between;
    margin: 7rem auto 0;
    border-bottom: 1px dotted $color-dark;

    @include screen(small) {
      margin-top: 4rem;
      width: 75vw;
    }

    input,
    button {
      background: transparent;
      border: none;
      outline: none;
    }

    input {
      min-width: 26rem;
      font-size: 1.9rem;

      @include screen(small) {
        font-size: 1.6rem;
        min-width: 22rem;
      }

      &::placeholder {
        color: rgba($color-dark, 1);
      }
    }

    button {
      font-weight: bold;
      opacity: 0.7;
      margin-left: 2rem;
      font-size: 1.6rem;
      text-transform: uppercase;

      @include screen(small) {
        font-size: 1.5rem;
      }
    }
  }
}
</style>
