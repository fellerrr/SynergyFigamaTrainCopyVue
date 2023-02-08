<template>
  <v-col>
   <v-col align="center">
    <video aria-label="Nothing great is made alone" 
      role="heading" aria-level="1" 
      src="https://cdn.sanity.io/files/599r6htc/localized/4caa8274fa1a76f5df188b7969c41e2b00890801.mp4" 
      autoplay="" muted="" loop="" playsinline="" class="figma-bfu23f"
      style="max-width:70%;">
    </video>
    <h3 >Figma connects everyone in the design process so teams
     can deliver better products, faster.</h3>
    <v-btn depressed color="primary" style="margin-top:15px;" @click="scrollToForm">Sign up free</v-btn>
   </v-col>
   <v-col>
     <v-img src="https://cdn.sanity.io/images/599r6htc/localized/455e29e0d05e64300b4a2aa99bcd25fa10a341a7-6969x2010.png?rect=0,1,6969,2008&amp;w=2016&amp;h=581&amp;q=75&amp;fit=max&amp;auto=format" 
     srcset="https://cdn.sanity.io/images/599r6htc/localized/455e29e0d05e64300b4a2aa99bcd25fa10a341a7-6969x2010.png?w=2016&amp;q=75&amp;fit=max&amp;auto=format&amp;dpr=0.5 1008w,https://cdn.sanity.io/images/599r6htc/localized/455e29e0d05e64300b4a2aa99bcd25fa10a341a7-6969x2010.png?w=2016&amp;q=75&amp;fit=max&amp;auto=format&amp;dpr=0.75 1512w,https://cdn.sanity.io/images/599r6htc/localized/455e29e0d05e64300b4a2aa99bcd25fa10a341a7-6969x2010.png?w=2016&amp;q=75&amp;fit=max&amp;auto=format 2016w,https://cdn.sanity.io/images/599r6htc/localized/455e29e0d05e64300b4a2aa99bcd25fa10a341a7-6969x2010.png?w=2016&amp;q=75&amp;fit=max&amp;auto=format&amp;dpr=1.5 3024w,https://cdn.sanity.io/images/599r6htc/localized/455e29e0d05e64300b4a2aa99bcd25fa10a341a7-6969x2010.png?w=2016&amp;q=75&amp;fit=max&amp;auto=format&amp;dpr=2 4032w" 
     loading="eager" alt="FigJam and Figma product windows" 
     sizes="(max-width: 1440px) 150vw, 2016w" 
     class="figma-5qi4nv"
     style="width:100%;">
     </v-img>
   </v-col>
   <SocialCard/>
   <v-container ref = "registerForm">
    <RegisterForm/>
   </v-container>
  </v-col>
</template>

<script>
import SocialCard from '../components/SocialCard.vue'
export default {
  name: 'IndexPage',
  components: {SocialCard},
  methods:{
    scrollToForm(){
      const el = this.$refs.registerForm
      if (el){
        el.scrollIntoView({behavior:'smooth'})
      }
    }

  }
}
</script>

