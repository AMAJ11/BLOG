<template>
   <div class="posts">
      <v-row>
         <v-col cols="9">
            <v-row class="pa-8 pt-4 px-16  mb-6" style="max-width:1000px">
               <v-col cols="12" v-for="i in 4">
                  <v-card elevation="10" variant="flat" class="pa-5" style="">
                     <div style="display:flex;justify-content: space-between;"> <v-card-title>Ahmad moh
                        </v-card-title><span style="">2020/5/8</span></div>
                     <v-img src="../assets/logo.png" width="100%" height="200px"></v-img>
                     <v-card-text>Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat commodi pariatur vero,
                        velit
                        eligendi repudiandae magnam laboriosam, tempora corporis modi temporibus! Minima et ipsum at
                        sit, iste
                        quos veritatis tempora?</v-card-text>
                     <v-card-actions>
                        <v-btn color="success">Readmore</v-btn>
                     </v-card-actions>
                  </v-card>
               </v-col>
            </v-row></v-col>
         <v-col class="pa-8" cols="3" >
            <v-list class="pa-5">
               <v-divider></v-divider>
               <h1 v-if="this.lan == 0">Categories</h1>
               <h1 style="direction: rtl;" v-if="this.lan == 1">الاقسام</h1>
               <v-divider></v-divider>
               <v-list-item value="home" v-for="i in 4">home</v-list-item>
            </v-list>
         </v-col>
      </v-row>
   </div>


</template>

<script>
export default {
   name: "PostView",
   data: function () {
      return {
         lan: localStorage.getItem("lan"),
      }
   },
   created: function () {
      let lang = localStorage.getItem("lan");
      this.lan = lang;
   },
}
</script>
<style scoped>
.posts {
   height: auto;
}

@media (max-width:600px) {
   .posts {
      max-width: 99%
   }
}
</style>