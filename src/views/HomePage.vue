<template>
  <categories-app/>
</template>

<script  lang="ts">
import CategoriesApp from '@/components/CategoriesApp.vue'

export default {
  name: "HomePage",
  components: {
    CategoriesApp
  },
  data() {
    return {
      
    }
  },
  async created() {
    
  },
  methods: {
  }
}
</script>

<style scoped>
#container {
  text-align: center;
  
  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  font-size: 16px;
  line-height: 22px;
  
  color: #8c8c8c;
  
  margin: 0;
}

#container a {
  text-decoration: none;
}
</style>
