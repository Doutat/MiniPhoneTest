<template>
  <f7-page :page-content="false" name="about">
 
    <f7-block-title>About My App</f7-block-title>
  
 
      
  <f7-block strong>
     
  {{msg}}
  <f7-link v-if="!showAll" @click="showAll=true">
    Lire la suite...
  </f7-link>
  <span v-if="showAll">
    {{lireSuite}}
    <f7-link @click="showAll=false">
    Reduire
  </f7-link>
  </span>  
 </f7-block>

  </f7-page>
</template>
<script>
export default {
  data(){
    return{
      msg:'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Magni molestiae laudantium dignissimos est nobis delectus nemo ea alias voluptatum architecto, amet similique, saepe iste',
      lireSuite:' consectetur in repellat ut minus quibusdam! Molestias et distinctio porro nesciunt ratione similique, magni doloribus, rerum nobis, aliquam quae reiciendis quasi modi. Nam a recusandae, fugiat in ea voluptates fuga eius, velit corrupti reprehenderit dignissimos consequatur! Blanditiis, cumque quo adipisci. Molestiae, dolores dolorum quos doloremque ipsa ullam eligendi commodi deserunt doloribus inventore magni? Ea mollitia veniam nostrum nihil, iusto doloribus a at! Ea molestiae ullam delectus!',
      showAll:false
      
    
    }
  }
}
</script>

