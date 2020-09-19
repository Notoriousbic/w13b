<template>
<div>
<h1>Your Tweets:</h1>
<div v-bind:class = "{tweetcontainer:grid}"> 
    <h3 v-for="tweet in tweets" v-bind:key="tweet.tweet">{{tweet.name+ ":  " + tweet.tweet}}</h3>
</div>
<button @click="grid=!grid" type="button" id ="button">change view</button>
</div> 
</template>

<script>
export default {
    name: "page-body",
    data : function() {
    return {
    tweets: [{name: "john", tweet:"hello"}, {name: "bill", tweet: "merry xmas"}, {name: "fred", tweet: "heck yeah!"}, {name:"carl", tweet: "I love vue!"}],
    grid: false
    }


}
}

</script>

<style scoped>
* {
    padding: 0;
    margin: 0;
    text-align: center;
}

.tweetcontainer {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
}


</style>