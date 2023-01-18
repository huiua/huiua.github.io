<template>
  <div id="app" class="flex flex-col justify-between h-screen">
    <div class="flex flex-col justify-start">
      <header class="flex h-fit">
        <div class="flex flex-col min-w-[5%]">
          <div class="bg-brand-darkblue min-h-[70px]"></div>
          <div class="bg-brand-midblue h-full"></div>
        </div>
        <div id="logo-section" class="bg-brand-darkblue p-[21px] min-w-fit">
          <div><img src="./assets/uoa-logo-vertical.png" width="103" alt="UoA Logo" /></div>
        </div>
        <div class="flex flex-col w-full">
          <div class="flex justify-between bg-brand-darkblue text-white align-middle px-6 min-h-[70px]">
            <h3>Media Production</h3>
            <div class="my-auto font-bold text-sm">
              <a href="https://adelaide.atlassian.net/wiki/spaces/LMP/overview?homepageId=221601" target="_blank" rel="noreferrer noopener" class="my-auto">Confluence<i class="far fa-external-link ml-1" /></a>
            </div>
          </div>
          <div class="flex justify-end bg-brand-midblue text-white font-bold h-full">
            <RouterLink to="/" class="header-nav"><i class="fad fa-house mr-2" /><span class="text-lg">Home</span>
            </RouterLink>
          </div>
        </div>
      </header>
      <RouterView />
    </div>

    <footer class="bg-brand-darkblue m-0 h-[120px] py-4 text-white">
      <div class="home-wrapper">
        <div class="flex justify-between my-4">
          <p class="my-auto">&copy; The University of Adelaide</p>
          <img src="@/assets/uoa-logo-horizontal.png" width="180" alt="UoA Logo" />
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>