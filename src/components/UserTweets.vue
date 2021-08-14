<template>
    <div> 
        <div class="tweetContent"
            v-for="tweet in tweets"
            :key="tweet">
        <h2> {{ tweet.user }} </h2>
        <p>
            "{{ tweet.content }}"
        </p>
        <h5> {{ tweet.postDate }} </h5>
        </div>
    </div>
</template>

<script>
    export default {
        name: "UserTweets",
        data: () => {
            return {
                tweets: [
                    {
                        user: "Jim Halpert",
                        id: 1,
                        content: "I am about to do something very bold in this job that I’ve never done before: try.",
                        postDate: "January/01/2010"
                    },
                    {
                        user: "Dwight Schrute",
                        id: 2,
                        content: "I am faster than 80% of all snakes",
                        postDate: "February/02/2010"
                    },
                    {
                        user: "Michael Scott",
                        id: 3,
                        content: "And I knew exactly what to do. But in a much more real sense, I had no idea what to do.",
                        postDate: "March/04/2010"
                    },
                    {
                        user: "Pam Beesley",
                        id: 4,
                        content: "I feel God in this Chili’s tonight.",
                        postDate: "April/05/2010"
                    },
                    {
                        user: "Stanley Hudson",
                        id: 5,
                        content: "BOY HAVE YOU LOST YOUR MIND? 'CAUSE I'LL HELP YOU FIND IT.",
                        postDate: "May/06/2010"
                    },
                    {
                        user: "Phyllis Vance",
                        id: 6,
                        content: "You have a lot to learn about this town sweetie.",
                        postDate: "June/07/2010"
                    },
                    {
                        user: "Ryan Howard",
                        id: 7,
                        content: "I'd rather she be alone than with somebody else. Is that love?",
                        postDate: "July/08/2010"
                    },
                    {
                        user: "Kevin Malone",
                        id: 8,
                        content: "Why waste time, say lot word when few word do trick?",
                        postDate: "August/09/2010"
                    },
                    {
                        user: "Creed Bratton",
                        id: 9,
                        content: "I’ve been involved in a number of cults, both as a leader and a follower. You have more fun as a follower. But you make more money as a leader.",
                        postDate: "September/10/2010"
                    },
                ]
            }
        },
        methods: {
            toggleViewType() {
                this.listView = !this.listView;
            }
        }
    }
</script>

<style scoped>

h2 {
    text-align: left;
    padding-left: 1.5vw;
}

h5 {
    text-align: right;
    padding-right: 1.5vw;
    text-decoration: none;
}

p {
    font-size: larger;
    font-style: italic;
    padding-left: 1vw;
    padding-right: 1vw;
}

.tweetContent {
    border: 2px solid black;
    border-radius: 12px;
    background-color: rgb(190, 209, 228);
}

</style>