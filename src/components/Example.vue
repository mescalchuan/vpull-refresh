<template>
    <div>
        <pull-refresh :refreshing="isRefreshing" :on-refresh="onRefresh" pull-height="400px">
            <div class="list">
                <button @click="open">手动刷新</button>
                <ul>
                    <li v-for="n in 20">goodsId -- {{n}}</li>
                </ul>
            </div>
        </pull-refresh>
    </div>
</template>

<script>
import pullRefresh from "@/components/pullRefresh.vue";
export default {
    name: 'Example',
    data() {
        return {
            isRefreshing: false
        }
    },
    methods: {
        onRefresh() {
            this.isRefreshing = true;
            setTimeout(() => {
                this.isRefreshing = false;
            }, 5000)
        },
        open() {
            this.isRefreshing = true;
            setTimeout(() => {
                this.isRefreshing = false;
            }, 5000)
        }
    },
    components: {
        pullRefresh
    }
}
</script>

<style scoped>
    ul {
        margin-top: 0;
    }
    button {
        border: 0;
        background-color: #ff4f4f;
        color: white;
        padding: 5px 10px;
        display: block;
        margin: 20px auto;
    }
    .list {
        width: 100%;
        background-color: white;
        overflow: hidden;
    }
</style>
