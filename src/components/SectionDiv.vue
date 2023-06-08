<template>
   <section class="hidden">
        <h1>
            {{ page.content.h1 }}
        </h1>
        <p>
            {{ page.content.p1 }}
        </p>
   </section>

   <section class="hidden">
        <h1>
            {{ page.content.h2 }}
        </h1>
        <p>
            {{ page.content.p2 }}
        </p>
   </section>

   <section class="hidden">
        <h1>{{ page.content.h3 }}</h1>
        <p>
            {{ page.content.p3 }}
        </p>
        <div class="images">
            <ImageSection></ImageSection>
        </div>
   </section>
</template>


<script>
import ImageSection from './ImageSection.vue';

export default{
props : ['page'],
components : {
    ImageSection,
}
}
</script>