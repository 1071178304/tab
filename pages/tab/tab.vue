<template>
    <view>
        <view class="title">{{title}}</view>
        <!-- 本体样式 -->
        <view class="yx-tab-box">
            <view class="yx-tab-text" @click="yxTab=0" :class="{'yxTabchange' :yxTab===0}">招募中</view>
            <view class="yx-tab-text" @click="yxTab=1" :class="{'yxTabchange' :yxTab===1}">进行中</view>
            <view class="yx-tab-text" @click="yxTab=2" :class="{'yxTabchange' :yxTab===2}">已结束</view>
        </view>
        <!-- 多余样式如：下划线样式 -->
        <view class="yx-tab-box-3">
            <view v-if="yxTab===0" class="yx-tab-text-1 " @click="yxTab=0" :class="{'yxTabchange' :yxTab===0}">
                <view class="hr"></view>
            </view>
            <view v-if="yxTab===1" class="yx-tab-text-2" @click="yxTab=1" :class="{'yxTabchange' :yxTab===1}">
                <view class="hr"></view>
            </view>
            <view v-if="yxTab===2" class="yx-tab-text-3 " @click="yxTab=2" :class="{'yxTabchange' :yxTab===2}">
                <view class="hr"></view>
            </view>
        </view>
        <view style="border-bottom: 1rpx solid #f0f0f0;"></view>
        <!-- 切换内容 -->
        <view v-show="yxTab===0">
            内容1
        </view>
        <view v-show="yxTab===1">
            内容2
        </view>
        <view v-show="yxTab===2">
            内容3
        </view>
    </view>
</template>

<script>
    export default {
        data() {
            return {
                title: '随意修改选项卡',
                yxTab: 0
            }
        },
        methods: {

        }
    }
</script>

<style lang="scss" scoped>
    .bor {
        border: 1rpx solid #007AFF;
    }

    .title {
        text-align: center;
        font-size: 30rpx;
    }

    .yx-tab-box {
        padding-top: 56rpx;
        background: white;
        display: flex;

        .yx-tab-text {
            //无点击事件原始样式
            flex: 1;
            color: #909399;
            font-size: 28rpx;
            text-align: center;
        }

        .yxTabchange {
            font-size: 28rpx;
            color: #4688FA;
        }
    }

    .yx-tab-box-3 {
        width: 100%;
        position: relative;
        background: white;
        height: 40rpx;
        font-weight: bold;

        .yx-tab-text-1 {
            width: 33%;
            display: inline-block;
            color: #909399;
            font-size: 28rpx;
            text-align: center;

            .hr {
                height: 5rpx;
                background-color: #4688FA;
                width: 20%;
                margin: 0 auto;
            }
        }

        .yx-tab-text-2 {
            padding-left: 33%;
            width: 33%;
            display: inline-block;
            color: #909399;
            font-size: 28rpx;
            text-align: center;

            .hr {
                height: 5rpx;
                background-color: #4688FA;
                width: 20%;
                margin: 0 auto;
            }
        }

        .yx-tab-text-3 {
            padding-left: 67%;
            width: 33%;
            display: inline-block;
            color: #909399;
            font-size: 28rpx;
            text-align: center;

            .hr {
                height: 5rpx;
                background-color: #4688FA;
                width: 20%;
                margin: 0 auto;
            }
        }

        .yx-tab-text-4 {
            padding-left: 75%;
            width: 25%;
            display: inline-block;
            color: #909399;
            font-size: 28rpx;
            text-align: center;

            .hr {
                height: 5rpx;
                background-color: #4688FA;
                width: 20%;
                margin: 0 auto;
            }
        }

        .yxTabchange {
            font-size: 28rpx;
            color: #4688FA;
        }
    }
</style>
