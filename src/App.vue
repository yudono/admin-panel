<template>
	<div class="fixed top-0 left-0 w-full h-screen bg-gray-500 bg-opacity-50 hidden" id="mark" v-on:click="hide"></div>
	<div class="flex flex-row">
		
		<!-- sidebar -->
		<aside class="flex-shrink-0 max-w-xs min-w-64 w-full h-screen overflow-auto p-6 justify-center fixed top-0 left-0 bg-white lg:static shadow-xl lg:shadow-none hidden lg:block z-50">
			<div class="w-full h-full flex flex-col">
				<img src="./assets/logo.png" alt="logo" class="w-12">
				<div class="my-3 ubuntu text-theme-primary font-medium text-xl">Husada SIMRS</div>

				<!-- menu -->
				<div class="mt-2">
					<NavItem name="Home" icon="Activity.png" active="true" title="Home"></NavItem>
					<NavItem name="Waiting List" icon="Users.png" title="Waiting List"></NavItem>
					<NavItem name="Schedules" icon="Calendar.png" title="Schedules"></NavItem>
					<NavItem name="Settings" icon="Setting.png" title="Settings"></NavItem>
					<NavItem name="Help Center" icon="Help.png" title="Help Center"></NavItem>
				</div>

				<div class="flex-grow"></div>

				<!-- Today reports -->
				<Reports></Reports>
			</div>
		</aside>

		<!-- main -->
		<main class="flex-grow h-screen overflow-auto bg-theme-body py-8 px-6">
			<div class="flex flex-wrap">
				<div class="block lg:hidden">
					<i class="fa fa-bars mr-4" v-on:click="show"></i>
				</div>
				<div class="ubuntu font-black text-3xl">Overview</div>
				<div class="flex-grow"></div>
				<div class="ubuntu bg-white px-4 py-2 text-sm rounded-full w-48 flex-shrink-0"><i class="far fa-calendar mr-1"></i> Jan - Feb 2021 <i class="fa fa-chevron-down ml-4"></i></div>
				<div class='ml-5 lw-8 lg:w-auto flex-shrink-0'><img :src="require('@/assets/images/avatar.png')" alt="avatar" class="w-8 h-8 inline-block"><div class="lg:inline-block ubuntu font-medium ml-3 hidden">Botak Sebelah</div></div>
			</div>

			<div class="flex flex-wrap mt-10">
				<div class="w-full h-full lg:w-1/2">
					<!-- group card-1 -->
					<div class="flex flex-wrap">
						<!-- card-1 -->
						<CardPatient></CardPatient>
						<!-- end card-1 -->

						<!-- card-2 -->
						<CardHospital></CardHospital>
						<!-- end card-2 -->

						<!-- card-5 -->
						<CardRoom></CardRoom>
						<!-- end card-5 -->
					</div>
				</div>
				<div class="w-full h-full lg:w-1/2">
					<!-- group card-2 -->
					<div class="flex flex-wrap">
						<!-- card-3 -->
						<CardDoctor></CardDoctor>
						<!-- end card-3 -->

						<!-- card-4 -->
						<CardNurse></CardNurse>
						<!-- end card-4 -->

						<!-- card-6 -->
						<CardChat></CardChat>
						<!-- end card-6 -->
					</div>
				</div>
			</div>
		</main>

	</div>
</template>

<script>
	import NavItem from './components/NavItem.vue'
	import Reports from './components/Reports.vue'
	// card
	import CardPatient from './components/CardPatient.vue';
	import CardHospital from './components/CardHospital.vue';
	import CardDoctor from './components/CardDoctor.vue';
	import CardNurse from './components/CardNurse.vue';
	import CardRoom from './components/CardRoom.vue';
	import CardChat from './components/CardChat.vue';

	export default {
		name: 'App',
		components: {
			NavItem,
			Reports,
			CardPatient,
			CardHospital,
			CardDoctor,
			CardNurse,
			CardRoom,
			CardChat
		},
		methods: {
			show: function() {
				const aside = document.querySelector('aside')
				const mark = document.querySelector('#mark')
				aside.classList.remove('hidden')
				mark.classList.remove('hidden')
			},
			hide: function() {
				const aside = document.querySelector('aside')
				const mark = document.querySelector('#mark')
				aside.classList.add('hidden')
				mark.classList.add('hidden')
			}
		}
	}
</script>

<style>
.bg-theme-primary,.hover-bg-theme-primary:hover{background: rgba(54,79,205,1)}
.text-theme-primary, .hover-text-theme-primary:hover{color: rgba(54,79,205,1)}
.bg-theme-secondary, .hover-bg-theme-secondary:hover{background: rgba(235,237,250,1)}
.text-theme-secondary, .hover-text-theme-secondary:hover{color: rgba(235,237,250,1)}
.bg-theme-body, .hover-bg-theme-body:hover{background: rgba(247,248,253,1)}
.text-theme-body, .hover-text-theme-body:hover{color: rgba(247,248,253,1)}
.bg-theme-gray, .hover-bg-theme-gray:hover{background: rgba(51,51,51,1)}
.text-theme-gray, .hover-text-theme-gray:hover{color: rgba(51,51,51,1)}
.card-1{background: #F5955F;}
.card-2{background: #219653;}
.default-width{width:272px;}
.bg-chat{background: #FAFAFA;}
.bg-chat-2{background: #F6F9FE;}
.ubuntu{
	font-family: 'Ubuntu', sans-serif;
}
</style>