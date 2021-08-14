<template>
    <div>
        <header>
            <button id="toggleViewBtn"
                @click="toggleViewType()">Toggle View
            </button>
        </header>
        <UserTweets
            id="tweetView"
            :class="this.listView ? 'listView' : 'cardView' ">
        </UserTweets>
    </div>
</template>

<script>
import UserTweets from './UserTweets.vue'
    export default {
        name: "TweetContainer",
        components: {
            UserTweets
        },
        data: () => {
            return {
                listView: false,
            }
        },
        methods: {
            toggleViewType() {
                console.log(!this.listView);
                this.listView = !this.listView;
            }
        }
    }
</script>

<style scoped>

* {
    margin-left: 1vw;
    margin-right: 1vw;
}

#UserTweets {
    display: grid;
    grid-auto-columns: 1fr;
    grid-auto-rows: auto;
    gap: 1vw;
}

#tweetView {
    display: grid;
    gap: 1vw;
}

.listView {
    display: grid;
    grid-template-columns: 1fr;
    gap: 1vw;
}

.cardView {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 1vw;
}

header {
    display: flex;
    flex-direction: row-reverse;
    padding-bottom: 1vh;
}

#toggleViewBtn {
    display: inline-block;
    padding: 0.3em 1em;
    margin: 0 0.3em 0.3em 0;
    border-radius: 8px;
    box-sizing: border-box;
    text-decoration: none;
    color: #FFFFFF;
    background-color: #41545ffd;
    transition: all 0.2s;
}

#toggleViewBtn:hover{
    background-color:rgba(28, 28, 31, 0.898);
}

</style>