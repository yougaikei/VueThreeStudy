<template>
    <div class="vue-bind">
        <h1>v-bind 的使用</h1>
        <div class="bind-link">
            <div class="list-one">
                <a v-bind:href="baiDuLink" target="_blank">百度一下</a>
                <p class="plan-box">方案 01:</p>
                <code>
                    &lt;<span style="color: #569CD6;">a</span> <span style="color: #9CDCFE">v-bind:href="baiDuLink"</span>&gt;百度一下&lt;/<span style="color: #569CD6;">a</span>&gt;
                </code>
                <p class="plan-box">方案 02:</p>
                <code>
                    &lt;<span style="color: #569CD6;">a</span> <span style="color: #9CDCFE">:href="baiDuLink"</span>&gt;百度一下&lt;/<span style="color: #569CD6;">a</span>&gt;
                </code>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'VueBind',
    data() {
        return {
            baiDuLink: "https://www.baidu.com/index.php",
            returnCode: {
                bandAll: `<a v-bind:href="baiDuLink">百度一下</a>`,
                bandSplit: `<a :href="baiDuLink">百度一下</a>`
            }
        }
    }
}
</script>
<style lang="less" scoped>
    .vue-bind{
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 100%;
        height: 100vh;
        background-color: #E1F3D8;
        -webkit-user-select: none;
        -moz-user-select: none;
        -ms-user-select: none;
        user-select: none;
        overflow: hidden;

        h1 {
            font-size: 48px;
            padding: 24px;
        }

        .bind-link {
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 80%;

            .list-one {
                width: 100%;

                a {
                    font-size: 24px;
                    background-color: #409EFF;
                    padding: 10px 20px;
                    border-radius: 8px;
                    color: white;

                    &:hover {
                        background-color: #A0CFFF;
                    }
                }
                
                p {
                    margin-top: 25px;

                    &.plan-box {
                        font-weight: bold;
                        font-style: oblique;
                    }
                }

                code {
                    position: relative;
                    display: block;
                    font-size: 16px;
                    font-weight: bold;
                    width: 80%;
                    color: white;
                    padding: 10px;
                    background-color: black;
                    border-radius: 8px;
                    margin-top: 10px;
                    -webkit-user-select: text;
                    -moz-user-select: text;
                    -ms-user-select: text;
                    user-select: text;
                    cursor: text;
                }
            }
        }
    }
</style>