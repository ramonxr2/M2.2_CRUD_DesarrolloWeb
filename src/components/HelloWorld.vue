<template>
  <v-card
   class="mx-auto"
   max-width="500"
 >
   <v-container fluid>
     <v-row dense>
       <v-col
         v-for="card in cards"
         :key="card.title"
         :cols="card.flex"
       >
         <v-card>
           <v-img
             :src="card.src"
             class="align-end"
             gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
             height="200px"
             cover
           >
             <v-card-title class="text-white" v-text="card.title"></v-card-title>
           </v-img>

           <v-card-actions>
             <v-spacer></v-spacer>

             <v-btn size="small" color="surface-variant" variant="text" icon="mdi-heart"></v-btn>

             <v-btn size="small" color="surface-variant" variant="text" icon="mdi-bookmark"></v-btn>

             <v-btn size="small" color="surface-variant" variant="text" icon="mdi-share-variant"></v-btn>
           </v-card-actions>
         </v-card>
       </v-col>
     </v-row>
   </v-container>
 </v-card>
   
</template>

<script setup>
import { ref } from 'vue';
const cards = ref( [
       { title: 'Super Tarea M2.2', src: 'https://citecuvp.tij.uabc.mx/wp-content/uploads/2022/10/ISOTIPO-UABC-COLORORIGINAL.png', flex: 12 },
       { title: 'Jesús Ramón Ruiz Soto 1182367', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', flex: 6 },
       { title: 'Desarrollo de Aplicaciones Web', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 6 },
     ])
</script>
