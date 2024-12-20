<script>
export default {
	methods: {
	GoToTelegram() {
		window.open("https://web.telegram.org/a/#691012199")
	}
	}
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
<div class="footer">
	<div class="individyal">
	<h2>ІНДИВІДУАЛЬНА ФОТОСЕСІЯ</h2>
	<div class="paragraf">
		<p>Це про - впевненість в собі, прожити свій внутрішній стан.
		Lorem ipsum dolor sit amet consectetur, adipisicing elit. Accusantium at velit ex molestias soluta aliquid aperiam amet, dolores, saepe dolorem, 
		sed laboriosam doloribus consequatur iusto non vero pariatur suscipit expedita.
	</p>
	<h2>800 | година</h2>
	</div>
	<button class="btn" @click="GoToTelegram">Запис на фотосесію</button>
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
	border-radius: 4px;
}
.coladzh img {
	width: 100%;
}
.footer {
	display: flex;
	align-items: center;
	justify-content: center;
	margin-top: 50px;
}
.individyal {
  width: 100%;
  max-width: 350px;
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  align-items: flex-start; 
  justify-content: flex-start;
  padding-left: 10px; 
}

/* Для заголовков и текста внутри .individyal */
.individyal h2 {
  font-size: 18px;
  margin-bottom: 10px;
}

.paragraf p {
  margin-bottom: 10px;
  font-size: 14px;
}

.individyal h2 + .paragraf h2 {
  margin-top: 10px;
}

.individyal .btn {
  margin-top: 20px;
  padding: 10px 20px;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.individyal .btn:hover {
  background-color: #0056b3;
}

/* Медиазапрос для экрана iPhone 14 Pro */
@media (max-width: 430px) {
  .porfolio h1 {
    font-size: 16px; /* Увеличиваем шрифт заголовка */
  }

  .coladzh {
    max-width: 100%; /* Делаем блок более гибким на маленьких экранах */
    height: 350px; /* Уменьшаем высоту */
  }

  .individyal {
    width: 90%; /* Делаем блок индивидуальной фотосессии чуть меньше */
    margin-top: 10px;
    padding-left: 5px; /* Уменьшаем отступ слева */
  }

  .individyal h2 {
    font-size: 16px; /* Уменьшаем шрифт заголовка */
  }

  .paragraf p {
    font-size: 12px; /* Уменьшаем шрифт текста */
  }

  .individyal .btn {
    padding: 8px 16px;
    font-size: 14px;
	 cursor: pointer;
  }
}
</style>