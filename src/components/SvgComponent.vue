<template>
    <svg v-if="names === 'chat'" xmlns="http://www.w3.org/2000/svg" class="ionicon" viewBox="0 0 512 512"><path d="M87.49 380c1.19-4.38-1.44-10.47-3.95-14.86a44.86 44.86 0 00-2.54-3.8 199.81 199.81 0 01-33-110C47.65 139.09 140.73 48 255.83 48 356.21 48 440 117.54 459.58 209.85a199 199 0 014.42 41.64c0 112.41-89.49 204.93-204.59 204.93-18.3 0-43-4.6-56.47-8.37s-26.92-8.77-30.39-10.11a31.09 31.09 0 00-11.12-2.07 30.71 30.71 0 00-12.09 2.43l-67.83 24.48a16 16 0 01-4.67 1.22 9.6 9.6 0 01-9.57-9.74 15.85 15.85 0 01.6-3.29z" stroke="currentColor" stroke-linecap="round" stroke-miterlimit="10" stroke-width="32"/>
    </svg>

    <svg v-if="names === 'cube'" xmlns="http://www.w3.org/2000/svg" class="ionicon" viewBox="0 0 512 512"><path d="M448 341.37V170.61A32 32 0 00432.11 143l-152-88.46a47.94 47.94 0 00-48.24 0L79.89 143A32 32 0 0064 170.61v170.76A32 32 0 0079.89 369l152 88.46a48 48 0 0048.24 0l152-88.46A32 32 0 00448 341.37z" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="32"/><path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="32" d="M69 153.99l187 110 187-110M256 463.99v-200"/>
    </svg>

    <svg v-if="names === 'heart'" xmlns="http://www.w3.org/2000/svg" class="ionicon" viewBox="0 0 512 512"><path d="M352.92 80C288 80 256 144 256 144s-32-64-96.92-64c-52.76 0-94.54 44.14-95.08 96.81-1.1 109.33 86.73 187.08 183 252.42a16 16 0 0018 0c96.26-65.34 184.09-143.09 183-252.42-.54-52.67-42.32-96.81-95.08-96.81z" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="32"/>
    </svg>

    <svg v-if="names === 'home'"  id="first" xmlns="http://www.w3.org/2000/svg" class="ionicon" viewBox="0 0 512 512"><path d="M80 212v236a16 16 0 0016 16h96V328a24 24 0 0124-24h80a24 24 0 0124 24v136h96a16 16 0 0016-16V212" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="32"/><path d="M480 256L266.89 52c-5-5.28-16.69-5.34-21.78 0L32 256M400 179V64h-48v69" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="32"/>
    </svg>
</template>

<script>
export default{
    props : ['names']
}
</script>