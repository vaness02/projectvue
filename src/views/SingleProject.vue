<template>
	<div class="container mx-auto mt-10 sm:mt-20">
		
		<!-- Project header -->
		<ProjectHeader :singleProjectHeader="singleProjectHeader" />

		<!-- Project gallery -->
		<ProjectGallery :projectImages="projectImages" />

		<!-- Project information -->
		<ProjectInfo :projectInfo="projectInfo" />

		<!-- Live Demo -->
		<div class="mt-8">
			<a class="text-white hover:underline text-2xl font-bold" href="https://vaness02.github.io/PRAKTIKUM/index.html" target="_blank" style="font-family: 'Roboto', sans-serif;">Live Demo</a>
			<br><br>
			<a class="text-white hover:underline text-2xl font-bold" href="https://github.com/vaness02/PRAKTIKUM" target="_blank" style="font-family: 'Roboto', sans-serif;">Source Code</a>

		</div>
	</div>
</template>

<style scoped>
.text-white {
	color: white;
}
.text-black {
	color: black;
}
.font-bold {
	font-weight: bold;
}
.text-2xl {
	font-size: 1.5rem;
}
.light .text-white {
	color: black;
}
.light .dark:text-white {
	color: white;
}
.light .dark:hover:text-gray-300 {
	color: #d1d5db;
}
</style>

  
  <script>
  import feather from 'feather-icons';
  import ProjectHeader from '../components/projects/ProjectHeader.vue';
  import ProjectGallery from '../components/projects/ProjectGallery.vue';
  import ProjectInfo from '../components/projects/ProjectInfo.vue';
  import { ref } from 'vue';
  import { hasScopeRef } from '@vue/compiler-core';
  
  export default {
	name: 'Projects',
	components: {
	  ProjectHeader,
	  ProjectGallery,
	  ProjectInfo,
	},
	data: () => {
	  return {
		singleProjectHeader: {
		  singleProjectTitle: 'Praktikum ',
		  singleProjectDate: 'September 20, 2021',
		  singleProjectTag: 'UI / Frontend',
		},
		projectImages: [
		  {
			id: 1,
			title: 'Kabul Project Management UI',
			img: require('@/assets/images/dazz1.png'),
		  },
		  {
			id: 2,
			title: 'Kabul Project Management UI',
			img: require('@/assets/images/dazz2.png'),
		  },
		  {
			id: 3,
			title: 'Kabul Project Management UI',
			img: require('@/assets/images/dazz3.png'),
		  },
		],
		projectInfo: {
		  clientHeading: 'Tentang Tugas Ini',
		  objectivesDetails:
			'Membuat website online shop. Pada tugas ini saya memilih produk sepatu untuk dijual-belikan.',
		  technologies: [
			{
			  title: 'Tools & Technologies',
			  techs: [
				'HTML',
				'CSS',
				'JavaScript'
			  ],
			},
		  ],
		  liveDemoLink: 'https://vaness02.github.io/Kelompok_2_4us/index.html', // Tambahkan properti liveDemoLink
		},
	  };
	},
	mounted() {
	  feather.replace();
	},
	updated() {
	  feather.replace();
	},
	methods: {},
  };
  </script>
  
  <style scoped>
  .text-white {
	color: white;
  }
  .font-bold {
	font-weight: bold;
  }
  .text-2xl {
	font-size: 1.5rem;
  }
  </style>
  