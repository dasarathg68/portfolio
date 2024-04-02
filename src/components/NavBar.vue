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
          <li><a>Home</a></li>
          <li><a>Services</a></li>
          <li><a>Portfolio</a></li>
          <li><a>Resume</a></li>
        </ul>
      </div>
      <div class="dropdown dropdown-end">
        <div tabindex="0" role="button" class="btn btn-ghost btn-circle avatar">
          <div class="w-10 rounded-full">
            <img alt="Tailwind CSS Navbar component" src="../assets/images/dachu.jpg" />
          </div>
        </div>
      </div>
      <a class="btn btn-ghost text-xl">Dasarath G</a>
    </div>
    <div class="navbar-end hidden lg:flex">
      <ul class="menu menu-horizontal px-1">
        <li><a>Home</a></li>
        <li><a>Services</a></li>
        <li><a>Portfolio</a></li>
        <li><a>Resume</a></li>
      </ul>
    </div>
  </div>
</template>
<script setup lang="ts"></script>
