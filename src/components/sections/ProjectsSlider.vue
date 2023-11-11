<template>
    <Carousel :itemsToShow="1" :wrapAround="true" :transition="500" :breakpoints="breakpoints">

      <Slide v-for="slide in projects" :key="slide">
        <div class="carousel__item">
          <ProjectCard :project="slide" />
        </div>
      </Slide>

      <template #addons>
        <div class="pagination">
          <Pagination />
        </div>
      </template>

    </Carousel>
  </template>
  
  <script>
  import { defineComponent, ref } from 'vue'
  import { Carousel, Pagination, Slide } from 'vue3-carousel'
  import ProjectCard from './ProjectCard.vue'
  import 'vue3-carousel/dist/carousel.css'
  
  export default defineComponent({
    name: 'Autoplay',
    components: {
      Carousel,
      Slide,
      Pagination,
      ProjectCard
    },
    setup(){
      const projects = ref([
        {id: 1, title: 'aix.kz', pic: 'aix.kz_crop.png', desc: '#WordPress', url: 'https://aix.kz'},
        {id: 2, title: 'alataulabs.kz', pic: 'alataulabs.kz_en_crop.png', desc: '#React #NextJs', url: 'https://alataulabs.kz'},
        {id: 3, title: 'cybert.online', pic: 'cybert.online_crop.png', desc: '#Nuxt', url: 'https://cybert.online'},
        {id: 4, title: 'esvhub.com', pic: 'esvhub.com_en_crop.png', desc: '#Nuxt', url: 'https://esvhub.com'},
        {id: 5, title: 'iampartof.org', pic: 'iampartof.org_crop.png', desc: '#React', url: 'https://iampartof.org/'},
        {id: 6, title: 'onlinegibdd.ru', pic: 'onlinegibdd.ru_crop.png', desc: '#SCSS', url: 'https://onlinegibdd.ru'},
        {id: 7, title: 'tredo.co', pic: 'tredo.co_ crop.png', desc: '#Nuxt', url: 'https://tredo.co'},
        {id: 8, title: 'zhkdostyk.kz', pic: 'www.zhkdostyk.kz_ crop.png', desc: '#Jquery', url: 'https://zhkdostyk.kz'},
        {id: 9, title: 'siteforstartup.space', pic: 'siteforstartup.space_.png', desc: '#Hugo', url: 'https://siteforstartup.space'}

      ])      
      return {
        projects,
        breakpoints: {
				// 700px and up
				768: {
					itemsToShow: 2,
					snapAlign: "start"
				},
				// 1024 and up
				1024: {
					itemsToShow: 3,
					snapAlign: "center"
				}
			}
      }
    }
  })
  </script>
  
  <style scoped>

  .carousel__pagination {
    margin: 24px 0 0;
  }
  .carousel__slide {
    padding: 5px;
  }
  
  .carousel__viewport {
    perspective: 2000px;
  }
  
  .carousel__track {
    transform-style: preserve-3d;
  }
  
  .carousel__slide--sliding {
    transition: 0.5s;
  }
  
  .carousel__slide {
    opacity: 0.9;
    transform: rotateY(-20deg) scale(0.9);
  }
  
  .carousel__slide--active ~ .carousel__slide {
    transform: rotateY(20deg) scale(0.9);
  }
  
  .carousel__slide--prev {
    opacity: 1;
    transform: rotateY(-10deg) scale(0.95);
  }
  
  .carousel__slide--next {
    opacity: 1;
    transform: rotateY(10deg) scale(0.95);
  }
  
  .carousel__slide--active {
    opacity: 1;
    transform: rotateY(0) scale(1);
  }

  .carousel__item {
    /* border: 1px solid red; */
  }

  </style>
  