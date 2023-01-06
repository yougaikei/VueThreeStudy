<template>
    <div class="test-vue">
        <div class="test-main">
            <h1>{{ testContent }}</h1>
            <input type="text" placeholder="请选择功能" class="search-box" v-model="searchTerm">
            <ul>
                <li v-for="(item, index) in getSearchForTestList" :key="index">{{ item }}</li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TestVue',
    data() {
        return {
            testContent: "测试内容",
            testList: ["公司简介", "企业许可", "联系我们"],
            searchTerm: "",
        }
    },
    computed: {
        getSearchForTestList() {
            if (this.searchTerm) {
                return this.testList.filter(data => 
                    data.toLowerCase().includes(this.searchTerm.toLowerCase())
                )
            } else {
                return this.testList
            }
        }
    }
}
</script>

<style lang="less" scoped>
.test-vue {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100vh;
    color: #2c3e50;
    background-color: #F0F9EB;
    overflow: hidden;

    .test-main {
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 400px;
        background-color: #f2f2f2;
        height: 500px;

        h1 {
            font-size: 64px;
        }
        
        .search-box {
            width: 80%;
            background-color: #f8f8f8;
            border-radius: 8px;
            padding: 10px;
            font-size: 18px;
            margin: 24px 0;

            &::placeholder {
                color: #d5dbe3;
            }
        }
        
        ul {
            color: #425066;
    
            li {
                margin-bottom: 24px;
            }
        }
    }
}
</style>