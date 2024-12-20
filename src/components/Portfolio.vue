<script>
export default {
	
}
</script>

<template>
<div class="porfolio">
	<h1>ПОРТФОЛІО ТА ТАРИФИ</h1>
</div>
<div class="photo">
	<div class="coladzh">
		<img src="@/assets/coladg/coladg.jpg" alt="first">
</div>
</div>

</template>
<style scoped>
.porfolio {
	height: 50px;
	display: flex;
	align-items: center;
	justify-content: center;
}
.porfolio h1 {
	font-weight: 400;
	font-size: 14px;
}
.photo {
  display: flex; 
  align-items: center; 
  justify-content: center; 
  height: 500px;
}
.coladzh {
	width: 300px;
	height: 500px;
	display: flex;
	align-items: center;
	justify-content: center;
	margin-top: 20px;
}
.coladzh img {
	width: 100%;
}
</style>