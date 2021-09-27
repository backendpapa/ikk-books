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

    <div class="d-none d-sm-flex">
   <v-simple-table style="width:100%" class="mt-4 ma-4  animate__animated animate__fadeIn animate__slower">
    <template v-slot:default>
      <thead>
        <tr>
          <th class="text-left">
            Title
          </th>
          <th class="text-left">
            Rating
          </th>
          <th class="text-left">
            Category
          </th>
          <th class="text-left">
            Status
          </th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="item in desserts"
          :key="item.name"
        >
         <td>
           <v-row no-gutters  class="pa-2" s align="center" >
             <v-col cols="2">
               <p class="text-center"> <v-img width="60" height="70" src="https://placeimg.com/200/200/any?2"></v-img></p>
             
             </v-col>
             <v-col cols="7" style="width:100%" >
               <div class="ml-3">
               <p class="text-caption">Super-Modified: The Behance book of Creative Work</p>
               <p class="font-weight-bold text-caption mt-n4">Ash Murya</p>
             </div>
             </v-col>
           </v-row>
         </td>
         <td>4,5<span class="grey--text">/5</span></td>
         <td>
          <v-row style="height:100%" align="center" no-gutters>
            <v-avatar color="#E6F5FE" size="30" rounded="true" ><span class="" style="color:#577398">D</span></v-avatar>
            <p class="ml-2 mt-3 text-caption">Design & UX</p>
          </v-row>
         </td>
         <td>
           <v-btn style="text-transform:none"  block color="#F5F1FE" depressed  class="text-caption purple--text" dark>Take book</v-btn>
         </td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>
    </div>
    <v-simple-table class="mt-4 ma-4 d-flex d-sm-none animate__animated animate__fadeIn animate__slower">
    <template v-slot:default>
      <thead>
        <tr>
          <th class="text-left">
            Title
          </th>
          <th class="text-left">
            Rating
          </th>
          <th class="text-left">
            Category
          </th>
          <th class="text-left">
            Status
          </th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="item in desserts"
          :key="item.name"
        >
         <td>
           <v-row no-gutters  class="pa-2" style="width:13rem" align="center" >
             <v-col cols="5">
               <p class="text-center"> <v-img width="60" height="70" src="https://placeimg.com/200/200/any?2"></v-img></p>
             
             </v-col>
             <v-col cols="7" style="width:100%" >
               <div class="ml-3">
               <p class="text-caption">Super-Modified: The Behance book of Creative Work</p>
               <p class="font-weight-bold text-caption mt-n4">Ash Murya</p>
             </div>
             </v-col>
           </v-row>
         </td>
         <td>4,5<span class="grey--text">/5</span></td>
         <td>
          <v-row style="width:8rem;height:100%" align="center" no-gutters>
            <v-avatar color="#E6F5FE" size="30" rounded="true" ><span class="" style="color:#577398">D</span></v-avatar>
            <p class="ml-2 mt-3 text-caption">Design & UX</p>
          </v-row>
         </td>
         <td>
           <v-btn style="text-transform:none"  block color="#F5F1FE" depressed  class="text-caption purple--text" dark>Take book</v-btn>
         </td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>


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
        category:'Category',
        desserts: [
          {
            name: 'Frozen Yogurt',
            calories: 159,
          },
          {
            name: 'Ice cream sandwich',
            calories: 237,
          },]
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
