<template>
  <div>
    <!-- <p class="note">
      Demo based on
      <a href="https://color-mode.nuxtjs.org">@nuxtjs/color-mode</a> module.
    </p> -->
    <header class="max-w-container-max-width m-auto px-4 h-14 md:h-20">
      <div class="h-full flex items-center justify-between">
        <h1
          class="text-base leading-base font-bold-body-weight uppercase md:text-six md:leading-six"
        >
          Yangbo
        </h1>
        <!-- @click="switchTheme" -->
        <div>
          <ColorModePicker />
        </div>
      </div>
    </header>
    <main>
      <div>
        <div class="px-4 max-w-container-max-width my-10 mx-auto">
          <div
            class="text-sm leading-sm w-full max-w-readable-line-length md:text-eight md:leading-eight nuxt-content"
          >
            <p>
              Hello! I am <em>Yangbo</em>
              . I am a web developer
            </p>
            <br />
            <p>I am also on JueJin</p>
          </div>
        </div>
        <div
          class="bg-light-mode-surface-color dark:bg-dark-mode-surface-color"
        ></div>
      </div>
    </main>
    <!-- <h1>Color mode: {{ $colorMode.value }}</h1> -->
    <footer
      class="max-w-container-max-width m-auto p-4 h-20 text-sm leading-sm flex flex-col justify-center md:text-base md:leading-base md:flex-row md:justify-between md:items-center"
    >
      <div>
        <span class="text-grey-base"> © 2021 </span>
        <span>YangBo</span>
      </div>
      <div>
        <ul class="flex">
          <li class="mr-2 flex">
            <a href="/" target="_blank" rel="noopener noreferrer" class="mr-2">Email</a>
            <span class="text-grey-base">/</span>
          </li>
          <li class="mr-2 flex">
            <a
              href="https://juejin.cn/user/2594503171260199"
              target="_blank"
              rel="noopener noreferrer"
              class="mr-2"
            >
              JueJin
            </a>
            <span class="text-grey-base">/</span>
          </li>
          <li class="mr-2 flex">
            <a href="https://github.com/ybb926426" target="_blank" rel="noopener noreferrer" class="mr-2">
              GitHub
            </a>
          </li>
        </ul>
      </div>
    </footer>
  </div>
</template>

<script>
import ColorModePicker from '@/components/ColorModePicker'
export default {
  components: {
    ColorModePicker,
  },
  data() {
    return {
      theme: 'light',
    }
  },
  methods: {
    switchTheme() {
      if (this.$colorMode.preference === 'dark') {
        this.$colorMode.preference = 'light'
      } else {
        this.$colorMode.preference = 'dark'
      }
    },
  },
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.note {
  transition: all 0.3s;
  display: inline-block;
  padding: 15px 15px;
  border-radius: 5px;
  background-color: var(--bg-secondary);
  color: var(--color-secondary);
}
</style>
