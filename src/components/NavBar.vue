<template>
  <div class="navbar bg-base-100 rounded-lg w-full shadow-lg z-50 fixed">
    <div class="navbar-start">
      <div class="dropdown">
        <div tabindex="0" role="button" class="btn btn-ghost lg:hidden">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-5 w-5"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h8m-8 6h16"
            />
          </svg>
        </div>
        <ul
          tabindex="0"
          class="menu menu-sm dropdown-content mt-3 z-[1] p-2 shadow bg-base-100 rounded-box w-52"
        >
          <li @click="navigateToLink('')"><a>Home</a></li>
          <li @click="navigateToLink('services')"><a>Services</a></li>
          <li @click="navigateToLink('portfolio')"><a>Portfolio</a></li>
          <li @click="navigateToLink('resume')"><a>Resume</a></li>
          <li>
            <div class="dropdown">
              <div tabindex="0">
                Themes
                <span class="badge text-xs bg-blue-300">New</span>
              </div>

              <ul
                tabindex="0"
                class="menu menu-sm dropdown-content z-[1] bg-base-100 rounded-box w-32 mt-80"
              >
                <li v-for="theme in themesAvailable" :key="theme">
                  <div
                    type="radio"
                    name="dropdown"
                    class="btn btn-sm btn-ghost"
                    :aria-label="theme"
                    :value="theme"
                    @click="emits('themeChanged', theme)"
                  >
                    {{ theme }}
                  </div>
                </li>
              </ul>
            </div>
          </li>
        </ul>
      </div>
      <div class="dropdown dropdown-end">
        <div
          tabindex="0"
          role="button"
          class="btn btn-ghost btn-circle avatar"
          @click="navigateToLink('')"
        >
          <div class="w-10 rounded-full">
            <img alt="Tailwind CSS Navbar component" src="../assets/images/dachu.jpg" />
          </div>
        </div>
      </div>

      <a class="btn btn-ghost text-xl menu-dropdown" @click="navigateToLink('')">Dasarath G</a>
    </div>
    <div class="navbar-end hidden lg:flex">
      <ul class="menu menu-horizontal">
        <li @click="navigateToLink('')"><a>Home</a></li>
        <li @click="navigateToLink('about')"><a>About</a></li>
        <li @click="navigateToLink('services')"><a>Services</a></li>
        <li @click="navigateToLink('portfolio')"><a>Portfolio</a></li>
        <li>
          <div class="dropdown">
            <div tabindex="0">
              Themes
              <span class="badge text-xs bg-blue-300">New</span>
            </div>

            <ul
              tabindex="0"
              class="menu menu-sm dropdown-content z-[1] bg-base-100 rounded-box w-32 mt-80"
            >
              <li v-for="theme in themesAvailable" :key="theme">
                <div
                  type="radio"
                  name="dropdown"
                  class="btn btn-sm btn-ghost"
                  :aria-label="theme"
                  :value="theme"
                  @click="emits('themeChanged', theme)"
                >
                  {{ theme }}
                </div>
              </li>
            </ul>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>
<script setup lang="ts">
import { useRouter } from 'vue-router'
defineProps<{
  themesAvailable: string[]
}>()
const emits = defineEmits(['themeChanged'])
const router = useRouter()
function navigateToLink(id: string) {
  router.push('/' + id)
}
</script>
