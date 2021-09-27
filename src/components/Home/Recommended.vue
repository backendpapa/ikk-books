<template>
  <div style="background-color:#F3F2F7">
      
    
          <carousel class="d-none d-sm-flex" items="6" style="height:50vh">

    <v-card flat v-for="i in 13" :key="i.i" width="200" height="300"  class="white pa-2">
       <div>
           <v-row no-gutters>
               <v-spacer></v-spacer>
              
                   <p class="text-center"> <v-img width="170" src="https://placeimg.com/200/200/any?1"></v-img></p>
                   
               
               <v-spacer></v-spacer>

           </v-row>
          <p style="font-size:14px" class=" ml-1 ">The sales Development Playbook</p>   
          <p class="mt-n3 ml-1 font-weight-bold text-caption ">Allie Well</p> 
          <p class="mt-n3 ml-1 font-weight-bold text-caption ">4,5<span class="grey--text">/5</span></p> 
       </div>
    </v-card>

</carousel>

<carousel autoWidth class="d-flex d-sm-none" items="1" loop center style="height:50vh">

    <v-card flat v-for="i in 13" :key="i.i" width="200" height="300"  class="white pa-2 ma-1">
       <div>
           <v-row no-gutters>
               <v-spacer></v-spacer>
              
                   <p class="text-center"> <v-img width="170" src="https://placeimg.com/200/200/any?1"></v-img></p>
                   
               
               <v-spacer></v-spacer>

           </v-row>
          <p style="font-size:14px" class=" ml-1 ">The sales Development Playbook</p>   
          <p class="mt-n3 ml-1 font-weight-bold text-caption ">Allie Well</p> 
          <p class="mt-n3 ml-1 font-weight-bold text-caption ">4,5<span class="grey--text">/5</span></p> 
       </div>
    </v-card>

</carousel>
     
      
  </div>
</template>

<script>
 import carousel from 'vue-owl-carousel'
export default {
    components: { carousel },
    data(){
        return {
           
    }
}
}
</script>

<style>

</style>