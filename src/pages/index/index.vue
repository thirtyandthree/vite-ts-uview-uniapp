<template>
  <view >
    <view class="header">
			首页...
		</view>
    
  </view>
</template>



<script setup lang="ts">


</script>


<style>
.header {
		background: white;
		padding: 10px;
		position: sticky;
		top: 0;
		z-index: 9999999999;
	}


	.item {
		position: relative;
		display: flex;
		flex-direction: column;
		background: white;
		margin: 10px 0;
		padding: 10px;
    border-radius: 16rpx;
	}

	.flex {
		display: flex;
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

	.dd {
		justify-content: space-between;
		font-size: 12px;
		padding: 10px 0;
		color: black;
	}
	.info {
    color: #ccc;
	}

</style>