<script setup lang="ts">
import { ref, onMounted } from 'vue'
import { useRouter } from 'vue-router'
const router = useRouter()
const optionList = ref(['HOME', 'ABOUT', 'CARE', 'VISIT'])
const activeId = ref('HOME')
const showHamburger = ref(false)

const scrollTo = (id: string) => {
  activeId.value = id
  showHamburger.value = false

  const element = document.getElementById(id)
  const header = document.querySelector('.site-header')
  const headerHeight = header ? header.getBoundingClientRect().height : 92
  if (element) {
    const offsetPosition = element.getBoundingClientRect().top + window.pageYOffset - headerHeight
    window.scrollTo({
      top: offsetPosition,
      behavior: 'smooth'
    })
  }
}

onMounted(() => {
  const choice = new URLSearchParams(window.location.search).get('font')
  const family = choice === 'kaisei'
    ? 'KaiseiDecol, serif'
    : '"Playfair Display", serif'
  document.documentElement.style.setProperty('--display-font', family)
})
</script>
<template>
  <header class="site-header">
    <a class="brand" href="/" @click.prevent="router.push('/')">Yoomi</a>
    <nav class="site-nav" aria-label="Site">
      <button
        v-for="link in optionList"
        :key="link"
        type="button"
        class="nav-link"
        :class="{ 'is-active': activeId === link }"
        @click="scrollTo(link)"
      >
        {{ link.charAt(0) + link.slice(1).toLowerCase() }}
      </button>
    </nav>
    <a class="book" href="tel:646-379-9995">Book Now</a>
  </header>
</template>
<style lang="scss" scoped>
.site-header {
  position: sticky;
  top: 0;
  z-index: 50;
  display: flex;
  align-items: center;
  height: 92px;
  padding: 0 28px;
  background: #333333;
  gap: 12px;
}

.brand {
  flex: 0 0 auto;
  margin-right: 12px;
  color: #ffffff;
  font-family: var(--display-font), "Playfair Display", serif;
  font-size: 32px;
  font-weight: 700;
  line-height: 1;
  text-decoration: none;
}

.site-nav {
  display: flex;
  align-items: center;
  min-width: 0;
  overflow-x: auto;
  scrollbar-width: none;

  &::-webkit-scrollbar {
    display: none;
  }
}

.nav-link {
  flex: 0 0 auto;
  border: 0;
  background: transparent;
  padding: 0 10px;
  color: #ffffff;
  font-family: var(--display-font), "Playfair Display", serif;
  font-size: 17px;
  font-weight: 700;
  line-height: 20px;
  cursor: pointer;

  &.is-active {
    color: #fe8072;
  }
}

.book {
  flex: 0 0 auto;
  margin-left: auto;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 142px;
  height: 40px;
  background: #e394a4;
  color: #ffffff;
  border-radius: 0;
  font-family: "InriaSans", "Noto Sans", sans-serif;
  font-size: 16px;
  font-weight: 700;
  line-height: 16px;
  text-decoration: none;
}

@media (max-width: 949px) {
  .site-header {
    height: 72px;
    padding: 0 12px;
  }

  .brand {
    font-size: 26px;
  }

  .book {
    width: 108px;
  }
}
</style>
