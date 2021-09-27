<template>
 <div>
   <v-row class="mt-4 animate__animated animate__fadeIn animate__slow" justify="center" align="center" no-gutters >
     <v-spacer></v-spacer>
     <v-text-field  filled  placeholder="Type book name or author" append-icon="mdi-magnify"   class="black--text text-caption font-weight-bold" @click:append="toggleMarker" solo flat color="none" background-color="white" ></v-text-field>
  
      <v-select
      class="ml-4 text-caption font-weight-bold"
          :items="select"
          v-model="category"
          placeholder="Category"
        
          solo
          flat
          filled
          style="width:4rem;font-size:10px"
        ></v-select>
     <v-spacer></v-spacer>
   </v-row>
   <Tab />
 </div>
</template>

<script>
 import Tab from '../components/Home/Tab.vue'
  export default {
    name: 'Home',

    components: {
     Tab
    },
    data(){
      return {
        select:['Fictions','Tech','DIY','Science and Art'],
        category:'Category'
      }
    },
    methods:{
      toggleMarker(){
        // alert("searching")
      }
    }
  }
</script>
<style >
::-webkit-scrollbar {
  display: none;
}


</style>
