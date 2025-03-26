<template>
    <div id="single-blog">
        <h1>{{ blog.title }}</h1>
        <article>{{ blog.body }}</article>

    </div>
</template>

<script>
// id:this.$route.params.id,(fetches id from url using vue router)
//this.$http.get('http://jsonplaceholder.typicode.com/posts/'+ this.id)  
//makes http request and get blog id
export default{
    data(){
        return{
            id:this.$route.params.id,
            blog:{}
        }
    },

    created()
    {
        this.$http.get('http://jsonplaceholder.typicode.com/posts/'+ this.id).then(function(data)
    {
        console.log(data);
        this.blog=data.body;
    })
    }
}
</script>

<style scoped>
#single-blog{
    max-width: 940px;
    margin: 0 auto;
}
</style>