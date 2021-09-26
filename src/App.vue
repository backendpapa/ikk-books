<template>
  <v-app>
    <v-app-bar
      app
      color="white"
      flat
      
      dense
    >
      <div class="d-flex align-center  mt-3">
       <p class="font-weight-bold text-h6">BOOKS</p>
      </div>

      
<div class="d-flex align-center  " style="margin-left:10%">

      <v-btn text to="/" plain style="text-transform:none" class="text-caption font-weight-bold d-none d-sm-flex" :color="$route.path=='/'?'purple':'black'">Library</v-btn>
       <v-btn text to="/orders" plain style="text-transform:none" class="text-caption font-weight-bold d-none d-sm-flex" :color="$route.path=='/orders'?'purple':'black'">Orders</v-btn>
        <v-btn text to="/admin" plain style="text-transform:none" class="text-caption font-weight-bold d-none d-sm-flex" :color="$route.path=='/admin'?'purple':'black'">Admin</v-btn>
</div>
      <v-spacer></v-spacer>
    <div class="d-flex align-center ">
      <v-avatar class="shade d-none d-sm-flex" size="30" rounded="true">
      <v-img src="./assets/logoing.jpg"></v-img>
    </v-avatar>
    <p class="text-caption mt-4 ml-2 font-weight-bold d-none d-sm-flex"> Backend Papa</p>
    <v-btn text icon plain class="ml-2 d-none d-sm-flex"><v-icon>mdi-logout</v-icon></v-btn>
     
    </div>
    <v-app-bar-nav-icon class="d-flex d-sm-none" @click="drawer=!drawer"></v-app-bar-nav-icon>
    </v-app-bar>

     <v-navigation-drawer
     
      v-model="drawer"
      absolute
      temporary
    >
     <v-row no-gutters justify="center" align="center" style="height:30vh;background-color:#F1F1F1" >
        <div>
           <p class="text-center"><v-avatar  class="shade " size="70" rounded="true">
      <v-img src="./assets/logoing.jpg"></v-img>
    </v-avatar></p>
    <p class="text-body-1 text-center  font-weight-bold "> Backend Papa</p>
     <p class="text-caption text-center mt-n5 grey--text "> Javascript developer</p>
        </div>
     </v-row>

      <v-divider></v-divider>

      <v-list dense>
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title class="font-weight-bold">{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
       <v-list style="position:absolute;bottom:0;width:100%"  dense>
        <v-list-item
         link
        >
          <v-list-item-icon>
            <v-icon>mdi-logout</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title class="font-weight-bold">Logout</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import './App.css'
export default {
  name: 'App',

  data: () => ({
    drawer:false,
    items:[
      {title:"Library",icon:'mdi-library'},
      {title:'Order',icon:'mdi-bookmark-outline'},
      {title:'My Profile',icon:'mdi-account'},
      {title:'My Listing',icon:'mdi-clipboard-text-outline'},
      {title:'Support',icon:'mdi-help-circle'},
      {title:'Settings',icon:'mdi-cog-outline'}
    ]
  }),
};
</script>
<style scoped>
.shade{
   box-shadow: 0 1px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
</style>