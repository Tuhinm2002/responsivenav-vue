<template>
    <nav class="nav-bar" id="nav">
        <ul>
            <li v-for="(page,index) in pages" :key="index">
                <a :class="{active:activePage == index}"
                :href="page.link.url"
                :title="page.pageTitle"            
                v-on:click.prevent="navLinkClick(index)"
                ><i><SVG :names=list[index]></SVG></i></a>
                <!-- prevent heps us by not navigating or routing to the url or .html file -->
            </li>
        </ul>
    </nav>
</template>


<script>
import SvgComponent from './SvgComponent.vue';

export default{
    props : ["pages","activePage","navLinkClick"], 
components : {
SVG : SvgComponent
},
data() {
    return {
        list : ['home','chat','cube','heart'], 
    }
},
}
</script>
