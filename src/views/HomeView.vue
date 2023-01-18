<template>
  <div class="home-wrapper py-2">
    <div v-for="group in linkGroups" class="mb-3">
      <div class="flex justify-start">
        <i :class="group.icon" class="text-brand-midblue my-auto mr-2 text-2xl" />
        <h2 class="font-normal">{{ group.groupName }}</h2>
      </div>
      <p class="text-slate-500 mb-1">{{ group.description }}</p>
      <hr>
      <ul class="list-none">
        <li v-for="item in group.links" class="home-list-item">
          <i class="fas fa-circle text-[6px] my-auto align-middle mr-3" />
          <a :href="item.link" class="home-link" target="_blank" rel="noreferrernoopener">{{ item.name }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
const linkGroups = [
  {
    groupName: 'Interactives',
    icon: 'fad fa-bullseye-pointer',
    description: 'Custom interactives for different faculties of the University of Adelaide.',
    links: [
      { name: 'ABLE Interactives', link: 'https://mediaproduction.adelaide.edu.au/able-interactives/#/' },
      { name: 'Alliance Interactives', link: 'https://mediaproduction.adelaide.edu.au/alliance-interactives/#/' },
      { name: 'OUA Interactives', link: 'https://mediaproduction.adelaide.edu.au/oua-interactives/#/' },
      { name: 'UoA Library Referencing Guide', link: 'https://mediaproduction.adelaide.edu.au/referencing-guide/' },
    ]
  },
  {
    groupName: 'Online Tools',
    icon: 'fad fa-toolbox',
    description: 'Online learning and teaching tools.',
    links: [
      { name: 'Banner Tool', link: 'https://mediaproduction.adelaide.edu.au/banner-tool/' },
      { name: 'Media Budget Calculator', link: 'https://mediaproduction.adelaide.edu.au/calculator/#/' },
      { name: 'Smart Storyboard', link: 'https://mediaproduction.adelaide.edu.au/smart-storyboard/#/' },
      { name: 'SSB Pilot Archive', link: 'https://mediaproduction.adelaide.edu.au/ssb-pilot-archive/#/' },
    ]
  },
  {
    groupName: 'Style Guides',
    icon: 'fad fa-palette',
    description: 'Styles and guidelines for UoA theme used in LMS.',
    links: [
      { name: 'UoA Styles', link: 'https://mediaproduction.adelaide.edu.au/uoa-styles/#/' }
    ]
  },
]
</script>
