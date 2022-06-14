<template>
	<header class="top-nav">
		<h2 class="top-nav-title">BrainGame</h2>
		<div class="top-nav-info">
			<div class="top-nav-money">
				<span>70</span>
				<img width="15" src="../assets/img/coin.svg" alt="">
			</div>
			<img src="@/assets/img/avatar.jpg" alt="" class="top-nav-avatar">
		</div>
	</header>
</template>

<style lang="scss" scoped>
.top-nav{
	width: 100%;
	height: 64px;
	box-shadow: 0 2px 15px rgba(0, 0, 0, .3);
	position: fixed;
	top: 0;
	left: 0;
	padding: .5rem;
	display: flex;
	align-items: center;
	justify-content: space-between;
	&-title{
		font-family: 'Gamja Flower', cursive;
	}
	&-info{
		display: flex;
		align-items: center;
		gap: 20px;
	}
	&-money{
		display: flex;
		align-items: center;
		gap: 2px;
		font-size: 16px;
		font-family: 'Montserrat';
	}
	&-avatar{
		width: 50px;
		height: 50px;
		object-fit: contain;
		border-radius: 50%;
	}
}
</style>