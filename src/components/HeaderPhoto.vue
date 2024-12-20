<script>
export default {
  data() {
    return {
      currentIndex: 0,
      photos: [], // Массив для хранения путей к изображениям
    };
  },
  async mounted() {
    // Загружаем все изображения из папки photo
    const photosFile = import.meta.glob('@/assets/photo/*.jpg'); // Используем правильный путь

    const loadedPhotos = [];
    for (const path in photosFile) {
      const photo = await photosFile[path](); // Динамически загружаем файл
      loadedPhotos.push(photo.default); // Добавляем путь к изображению в массив
    }

    this.photos = loadedPhotos; // Сохраняем в состояние
    setInterval(this.nextPhoto, 3000); // Переход к следующему фото через 3 секунды
  },
  methods: {
    nextPhoto() {
      // Переход к следующему фото с цикличностью
      this.currentIndex = (this.currentIndex + 1) % this.photos.length;
    }
  }
};
</script>

<template>
  <div class="header-photo">
    <div
      class="photo-slide"
      :style="{ transform: `translateX(-${currentIndex * 100}%)`} "
    >
      <img v-for="(photo, index) in photos" :key="index" :src="photo" alt="photo" />
    </div>
  </div>
</template>

<style scoped>
.header-photo {
  width: 100%;
  height: 652px;
  overflow: hidden; /* Чтобы изображения не выходили за пределы контейнера */
  position: relative;
}

.photo-slide {
  display: flex;
  transition: transform 1.5s ease-in-out; /* Плавный переход */
  width: 100%; /* Каждое изображение в контейнере будет занимать 100% ширины */
}

.photo-slide img {
  width: 100vw; /* Каждое изображение заполняет всю ширину экрана */
  height: 80vh; /* Каждое изображение будет занимать 80% высоты экрана */
  object-fit: cover; /* Изображение сохраняет пропорции и не искажается */
}

/* Мобильные стили */
@media (max-width: 768px) {
  .photo-slide {
    width: 100%; /* Для мобильных устройств, контейнер будет занимать 100% ширины */
  }

  .photo-slide img {
    width: 100vw; /* Каждое изображение заполняет всю ширину экрана */
    height: 80vh; /* Каждое изображение будет занимать 80% высоты экрана */
    object-fit: cover; /* Чтобы изображение не искажалось */
  }
}

@media (max-width: 480px) {
  .photo-slide img {
    object-fit: cover; /* При уменьшении экрана, изображение будет обрезаться */
    height: 70vh; /* Можно еще уменьшить высоту на маленьких экранах */
  }
}
</style>
