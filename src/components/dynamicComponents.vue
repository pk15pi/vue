<template>
  <button @click="activeTab = 'TabA'">TabA</button>
  <button @click="activeTab = 'TabB'">TabB</button>
  <button @click="activeTab = 'TabC'">TabC</button>
                                     
                                     
    <component :is="activeTab"/>
  <!--<TabA v-if="activeTab ==='TabA"/>
  <TabB v-if="activeTab ==='TabB'"/>
  <TabC v-if="activeTab ==='TabC'"/> -->
</template>
<script>
import TabA from'./components/TabA.vue'
import TabB from'./components/TabB.vue'
import TabC from'./components/TabC.vue'
export default{
  name:'dynamicComp',
  components:{
     TabA,
     TabB,
     TabC,
  },
}
</script>