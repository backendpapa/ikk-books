<template>
  <div>
       <v-tabs background-color="transparent"  v-model="tab" hide-slider >
        <v-tab v-for="item in items" class="text-caption font-weight-bold" style="text-transform:none" :key="item.tab">
          {{ item.tab }}
        </v-tab>
      </v-tabs>
      <v-tabs-items touchless v-model="tab"  >
        <v-tab-item  v-for="item in items" :key="item.tab">
          <v-card color="" style="background-color:#F3F2F7" flat>
            <v-card-text>
              <component v-bind:is="item.content"></component>
            </v-card-text>
          </v-card>
        </v-tab-item>
      </v-tabs-items>
  </div>
</template>

<script>
import Recommended from './Recommended.vue'
import LastAdded from './LastAdded.vue'
export default {
    components:{
        Recommended,
        LastAdded
    },
    data(){
        return {
        tab: null,
      items: [
        { tab: 'Recommended', content: 'Recommended' },
        { tab: 'Last Added', content: 'LastAdded' }
      ]
    }
    }
}
</script>

<style>

</style>