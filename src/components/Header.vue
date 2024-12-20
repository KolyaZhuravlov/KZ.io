<script>
export default {
 data() {
	return {
		isDropdownVisible: false
	}
 },
 methods: {
	toogleDrop() {
		this.isDropdownVisible = !this.isDropdownVisible;
	}
 }
}
</script>

<template>
	<header class="container">
		<nav class="container-nav">
			<ul>
				<li class="left">KATYA ZHURAVLOVA</li>
				<li class="right" @click="toogleDrop">
					<svg v-if="!isDropdownVisible" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512" width="24px" height="24px">
						<path d="M0 96C0 78.3 14.3 64 32 64l384 0c17.7 0 32 14.3 32 32s-14.3 32-32 32L32 128C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32l384 0c17.7 0 32 14.3 32 32s-14.3 32-32 32L32 288c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32L32 448c-17.7 0-32-14.3-32-32s14.3-32 32-32l384 0c17.7 0 32 14.3 32 32z"/>
					</svg>
					</li>
			</ul>
		</nav>

		<!-- Выпадающий список -->
		<div v-if="isDropdownVisible" class="dropdown-menu">
			<div class="svg">
				<svg v-if="isDropdownVisible"
			@click="toogleDrop"
			 xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512" width="24px" height="24px">
						<path d="M376.6 84.5c11.3-13.6 9.5-33.8-4.1-45.1s-33.8-9.5-45.1 4.1L192 206 56.6 43.5C45.3 29.9 25.1 28.1 11.5 39.4S-3.9 70.9 7.4 84.5L150.3 256 7.4 427.5c-11.3 13.6-9.5 33.8 4.1 45.1s33.8 9.5 45.1-4.1L192 306 327.4 468.5c11.3 13.6 31.5 15.4 45.1 4.1s15.4-31.5 4.1-45.1L233.7 256 376.6 84.5z"/>
					</svg>
			</div>
			<nav class="navigation">
				<ul>
				<li>Home</li>
				<li>Портфоліо</li>
				<li>Інфо</li>
				<li>Відгуки</li>
				<li>Контакти</li>
			</ul>
			</nav>
		</div>
	</header>
</template>

<style scoped>
.container {
	width: 100%;
	height: 120px;
	justify-content: center;
	align-items: center;
}
.container-nav {
	width: 100%;
}

.container-nav ul {
	display: flex;
	justify-content: space-between;
	padding: 0;
	list-style-type: none;
	margin: 0;
}

.container-nav li {
	display: flex;
	align-items: center;
	margin-top: 45px;
}

.left {
	margin-left: 20px;
	cursor: pointer; 
}

.right {
	margin-right: 20px;
	cursor: pointer; 
	position: fixed;
	right: 0;
	z-index: 999;
}
.dropdown-menu {
	position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: #fff;
  color: black;
  z-index: 1000;
}
.navigation {
	margin-top: 150px;
}
.navigation li {
	cursor: pointer;
	margin-top: 20px;
	margin-left: 30px;
}
.svg {
	position: absolute;
  top: 42px;
  right: 20px;
  cursor: pointer;
}


</style>