<template>
  <section id="posts">
    <PostPreview v-for="post in posts" 
    :key="post.id"
    :title="post.title"
    :excerpt="post.previewText"
    :thumbnailImage="post.thumbnailUrl"
    :id="post.id"
    />
  </section>
</template>

<script>

import PostPreview from "~/components/Blog/PostPreview.vue";

export default {
  components:{
    PostPreview
  },
  data(){
    return {
      posts:[
        {
          title: "A New Beginning", 
          previewText:"This will be awesome, don\'t miss it",
          thumbnailUrl:"https://upload.wikimedia.org/wikipedia/commons/thumb/6/6d/Good_Food_Display_-_NCI_Visuals_Online.jpg/1200px-Good_Food_Display_-_NCI_Visuals_Online.jpg",
          id: "a-new-beginning"
        },
        {
          title: "A Second Beginning", 
          previewText:"This will be awesome again, don\'t miss it",
          thumbnailUrl:"https://upload.wikimedia.org/wikipedia/commons/thumb/6/6d/Good_Food_Display_-_NCI_Visuals_Online.jpg/1200px-Good_Food_Display_-_NCI_Visuals_Online.jpg",
          id: "a-2nd-beginning"
        }

      ]
    }
  }
}
</script>

<style scoped>

#posts{
  padding-top: 2rem;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
@media(min-width:35rem){
  #posts{
    align-items: center;
    flex-direction: row;
  }
}
</style>
