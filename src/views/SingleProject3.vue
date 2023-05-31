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
			<a class="text-white hover:underline text-2xl font-bold" href="https://ness0100.github.io/" target="_blank" style="font-family: 'Roboto', sans-serif;">Live Demo</a>
			<br><br>
			<a class="text-white hover:underline text-2xl font-bold" href="https://github.com/ness0100/ness0100.github.io" target="_blank" style="font-family: 'Roboto', sans-serif;">Source Code</a>

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
		  singleProjectTitle: 'Desain Portofolio Sederhana ',
		  singleProjectDate: 'February 21, 2023',
		  singleProjectTag: 'UI / Frontend',
		},
		projectImages: [
		  {
			id: 1,
			title: 'Kabul Project Management UI',
			img: require('@/assets/images/port1.png'),
		  },
		  {
			id: 2,
			title: 'Kabul Project Management UI',
			img: require('@/assets/images/port2.png'),
		  },
		  {
			id: 3,
			title: 'Kabul Project Management UI',
			img: require('@/assets/images/port3.png'),
		  },
		],
		projectInfo: {
		  clientHeading: 'Tentang Tugas Ini',
		  objectivesDetails:
			'Membuat website berisi portfolio saya, seperti hobi dan kesukaan saya.',
		  technologies: [
			{
			  title: 'Tools & Technologies',
			  techs: [
				'Javascript',
				'HTML',
				'CSS'
			  ],
			},
		  ],
		  
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
  