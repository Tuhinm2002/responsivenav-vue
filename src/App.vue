<template>
  <input type="checkbox" id="check">
    <label for="check">
    <svg id="btn" xmlns="http://www.w3.org/2000/svg" class="ionicon" viewBox="0 0 512 512"><rect x="48" y="48" width="176" height="176" rx="20" ry="20" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="32"/><rect x="288" y="48" width="176" height="176" rx="20" ry="20" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="32"/><rect x="48" y="288" width="176" height="176" rx="20" ry="20" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="32"/><rect x="288" y="288" width="176" height="176" rx="20" ry="20" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="32"/>
    </svg>
    <svg id="cancel" xmlns="http://www.w3.org/2000/svg" class="ionicon" viewBox="0 0 512 512"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="48" d="M244 400L100 256l144-144M120 256h292"/>
    </svg>
    </label>
  <NavBar :pages="pages"
:active-page="activePage"
:nav-link-click="(index)=>activePage=index">
</NavBar>
<NavBarMob :pages="pages"
:active-page="activePage"
:nav-link-click="(index)=>activePage=index"></NavBarMob>
<!-- activePage contains the index not any text pages[activePage] will give -->
<SectionDiv :page="pages[activePage]">
</SectionDiv>
</template>

<script>
import NavBar from './components/NavBar.vue';
import SectionDiv from './components/SectionDiv.vue';
import NavBarMob from './components/NavBarMob.vue';

export default{
components : {
  NavBar,
  NavBarMob,
  SectionDiv,
},
data(){
  return{
    activePage : 0,
    pages : [{
      link : {url:"home.html"},
      // 3 heading using object or dictionary then send through sectiondiv
      pageTitle : "Home page",
      content : {h1:"First Heading",
      p1:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo, architecto.",
    h2:"Cool things on the go",p2:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Possimus quibusdam maiores quidem voluptate, delectus fugit eaque porro atque facere tempora libero nostrum sapiente ut inventore nemo iste doloremque reiciendis. Dicta?",
  h3:"Cool images",p3:"Lorem ipsum dolor sit amet."}

    },
    {
      link : {url:"chat.html"},
      pageTitle : "Chat page",
      content : {h1:"Chat Page",
      p1:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo, architecto.",
    h2:"Cool things on the go",p2:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Possimus quibusdam maiores quidem voluptate, delectus fugit eaque porro atque facere tempora libero nostrum sapiente ut inventore nemo iste doloremque reiciendis. Dicta?",
  h3:"Cool images",p3:"Lorem ipsum dolor sit amet."}

    },
    {
      link : {url:"cube.html"},
      pageTitle : "Cube page",
      content : {h1:"Cube page",
      p1:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo, architecto.",
    h2:"Cool things on the go",p2:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Possimus quibusdam maiores quidem voluptate, delectus fugit eaque porro atque facere tempora libero nostrum sapiente ut inventore nemo iste doloremque reiciendis. Dicta?",
  h3:"Cool images",p3:"Lorem ipsum dolor sit amet."}

    },
    {
      link : {url:"like.html"},
      pageTitle : "Like page",
      content : {h1:"Like Page",
      p1:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo, architecto.",
    h2:"Cool things on the go",p2:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Possimus quibusdam maiores quidem voluptate, delectus fugit eaque porro atque facere tempora libero nostrum sapiente ut inventore nemo iste doloremque reiciendis. Dicta?",
  h3:"Cool images",p3:"Lorem ipsum dolor sit amet."}

    },
  ]
  };
},

mounted() {
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry)=>{
    if (entry.isIntersecting){
        console.log(entry);
        entry.target.classList.add('show');
    }
    else{
        entry.target.classList.remove('show');
    }
});
});    
    
const hiddenElements = document.querySelectorAll('.hidden');
hiddenElements.forEach((el) => observer.observe(el));

// const left1 = document.getElementById('navMob');
// console.log(left1.style.left);
},
}
</script>