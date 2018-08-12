<template>
        <nuxt-link :to="id">
        <div class="post-preview">
            <div 
            :style="{backgroundImage:'url('+thumbnailImage+')'}" 
            class="post-preview-thumbnail">
            </div>

            <div class="post-preview-content">
                <h1>{{title}}</h1>
                <p>{{excerpt}}</p>
            </div>
            
        </div>
        </nuxt-link>
     
</template>

<script>
    export default{
        props: {
            title: {
                type: String,
                required: true
            },
            excerpt: {
                type: String,
                required: true
            },
            thumbnailImage: {
                type: String,
                required: true
            },
            id:{
                type: String,
                required: true
            }
        }
    }
</script>

<style scoped>
a{
    text-decoration: none;
    color: black;
}
.post-preview{
    box-shadow: 5px 5px 15px 5px #888;
    border-radius: 5px;
    border: 1px solid black;
    width: 90%;
    margin: 2rem;
    height: 20rem;
}

.post-preview-thumbnail{
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 10rem; 
}

.post-preview-content{
    text-align: center;
    padding: 1rem;
}

@media(min-width: 35rem){
    .post-preview{
        width: 25rem; 
        }
}

</style>
