<template>
  <view>
    <view class="header item_head">
      <view class="flex user" style="align-items: center;">
							<image :src="'http://124.93.196.45:10001'+detail.imgUrl" mode=""></image>
							<text style="margin: 0 5px;">{{detail.author}}</text>
					</view>
    </view>
    <u-parse :content="detail.content"></u-parse>
  </view>
</template>


<script setup lang="ts">
import { onLoad } from '@dcloudio/uni-app'
import { newsDetail } from '~/api/garbage'

const detail = ref()
onLoad(async ({id})=>{
  const ret = await newsDetail(id)
  detail.value = ret['data']
})
</script>

<style>

.header{
		padding: 10px;
		position: sticky;
		top: 0;
		z-index: 9999999999;
    background: #f2f3f8;
}

.item_head {
		display: flex;
		justify-content: space-between;
		border-bottom: 1px #eee solid;
		padding: 5px 0;
    width: 100%;
	}
  .user{
    width: 100%;
    justify-content: space-between;
    color: gray;
    font-weight: 900;
  }

	.item_head image {
		width: 50px;
		height: 50px;
    border-radius: 100%;
	}
</style>