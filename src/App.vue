<template>
	<div class="fixed top-0 left-0 w-full h-screen bg-gray-500 bg-opacity-50 hidden" id="mark" v-on:click="hide"></div>
	<div class="flex flex-row">
		
		<!-- sidebar -->
		<aside class="flex-shrink-0 max-w-xs min-w-64 w-full h-screen overflow-auto p-6 justify-center fixed top-0 left-0 bg-white lg:static shadow-xl lg:shadow-none hidden flex flex-col z-50">
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
		</aside>

		<!-- main -->
		<main class="flex-grow h-screen overflow-auto bg-theme-body py-8 px-6">
			<div class="flex flex-wrap">
				<i class="fa fa-bars mr-4 block sm:hidden" v-on:click="show"></i>
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
						<div class="w-8/12 p-3">
							<div class="w-full h-full bg-white p-5 rounded-2xl">
								<div class="flex flex-row items-center justify-between">
									<div class="ubuntu font-medium">Patient Statistic</div>
									<div class="text-indigo-300 text-xs">VIEW ALL</div>
								</div>
								<div class="flex flex-row items-center justify-between mt-2">
									<div>
										<div class="ubuntu text-xs text-gray-400">In Today</div>
										<div class="ubuntu text-2xl">248</div>
										<div class="ubuntu text-red-500 text-xs"><i class="fa fa-arrow-up"></i>15.45%</div>
									</div>
									<img :src="require('@/assets/images/chart-1.png')" alt="chart" class="w-3/5">
								</div>
								<div class="flex flex-row items-center justify-between mt-2">
									<div>
										<div class="ubuntu text-xs text-gray-400">Out Today</div>
										<div class="ubuntu text-2xl">139</div>
										<div class="ubuntu text-green-500 text-xs"><i class="fa fa-arrow-up"></i>43%</div>
									</div>
									<img :src="require('@/assets/images/chart-2.png')" alt="chart" class="w-3/5">
								</div>
							</div>
						</div>
						<!-- end card-1 -->

						<!-- card-2 -->
						<div class="w-4/12 p-3">
							<div class="w-full h-full bg-white p-5 rounded-2xl text-center">
								<div class="ubuntu font-medium">Hospital Capacity</div>
								<img :src="require('@/assets/images/chart-3.png')" alt="chart" class="w-full mt-2">
							</div>
						</div>
						<!-- end card-2 -->

						<!-- card-5 -->
						<div class="w-full p-3">
							<div class="w-full h-full bg-white p-5 rounded-2xl">
								<div class="flex flex-row justify-between">
									<div class="ubuntu font-bold">Room Waiting List</div>
									<div class="text-xs text-indigo-300">VIEW COMPLETE LIST</div>
								</div>
								<table class="table-auto w-full mt-4 text-sm">
									<thead class="font-medium text-left text-gray-300 border-b border-gray-200 ubuntu">
										<tr>
											<th class="py-4">Name</th>
											<th class="py-4">Status</th>
											<th class="py-4">Date</th>
										</tr>
									</thead>
									<tbody>
										<tr>
											<td class="p-2 text-gray-800">
												<img :src="require('@/assets/images/avatar-2.png')" alt="avatar" class="w-10 h-10 rounded-full object-cover inline-block mr-4">Jessica Islander
											</td>
											<td class="p-4"><span class="bg-indigo-200 py-2 px-3 text-indigo-700 rounded-full font-bold text-xs">VIP</span></td>
											<td class="p-4 text-gray-300">January 30, 2021</td>
										</tr>
										<tr>
											<td class="p-2 text-gray-800">
												<img :src="require('@/assets/images/avatar-3.png')" alt="avatar" class="w-10 h-10 rounded-full object-cover inline-block mr-4">
												Iyem
											</td>
											<td class="p-4"><span class="bg-yellow-200 py-2 px-3 text-yellow-700 rounded-full font-bold text-xs">STD</span></td>
											<td class="p-4 text-gray-300">February 05,2021</td>
										</tr>
										<tr>
											<td class="p-2 text-gray-800">
												<img :src="require('@/assets/images/avatar-4.png')" alt="avatar" class="w-10 h-10 rounded-full object-cover inline-block mr-4">
												Sujiwan Parmin
											</td>
											<td class="p-4"><span class="bg-indigo-200 py-2 px-3 text-indigo-700 rounded-full font-bold text-xs">VIP</span></td>
											<td class="p-4 text-gray-300">February 10,2021</td>
										</tr>
										<tr>
											<td class="p-2 text-gray-800">
												<img :src="require('@/assets/images/avatar-5.png')" alt="avatar" class="w-10 h-10 rounded-full object-cover inline-block mr-4">
												Parno Marpin
											</td>
											<td class="p-4"><span class="bg-yellow-200 py-2 px-3 text-yellow-700 rounded-full font-bold text-xs">STD</span></td>
											<td class="p-4 text-gray-300">February 15,2021</td>
										</tr>
										<tr>
											<td class="p-2 text-gray-800">
												<img :src="require('@/assets/images/avatar-6.png')" alt="avatar" class="w-10 h-10 rounded-full object-cover inline-block mr-4">
												Paimer suka amer
											</td>
											<td class="p-4"><span class="bg-yellow-200 py-2 px-3 text-yellow-700 rounded-full font-bold text-xs">STD</span></td>
											<td class="p-4 text-gray-300">February 20,2021</td>
										</tr>
									</tbody>
								</table>
							</div>
						</div>
						<!-- end card-5 -->
					</div>
				</div>
				<div class="w-full h-full lg:w-1/2">
					<!-- group card-2 -->
					<div class="flex flex-wrap">
						<!-- card-3 -->
						<div class="w-1/2 px-3 py-4">
							<div class="card-1 py-4 px-5 rounded-2xl">
								<div class="flex flex-row">
									<svg width="49" height="44" viewBox="0 0 49 44" fill="none" xmlns="http://www.w3.org/2000/svg">
										<mask id="path-1-inside-1" fill="white">
											<path d="M28.5 4.38859C28.5 3.62168 29.1224 2.99509 29.8876 3.04699C32.8596 3.24861 35.7579 4.09606 38.3779 5.53677C41.4043 7.20096 43.9611 9.60279 45.8111 12.5193C47.6611 15.4358 48.7442 18.7724 48.96 22.2195C49.1757 25.6665 48.5171 29.1121 47.0452 32.2365C45.5733 35.3609 43.3358 38.0628 40.5406 40.0914C37.7453 42.1199 34.4829 43.4094 31.0561 43.84C27.6293 44.2706 24.1492 43.8285 20.9389 42.5547C18.1598 41.4519 15.6608 39.7567 13.6129 37.5934C13.0857 37.0365 13.1725 36.1576 13.7638 35.6692C14.3552 35.1809 15.2267 35.2687 15.7598 35.82C17.5056 37.6254 19.6191 39.0431 21.9633 39.9732C24.7386 41.0745 27.7472 41.4568 30.7098 41.0845C33.6723 40.7122 36.4928 39.5974 38.9094 37.8437C41.326 36.0899 43.2603 33.7541 44.5328 31.053C45.8053 28.3518 46.3747 25.373 46.1882 22.3929C46.0017 19.4129 45.0653 16.5283 43.4659 14.0069C41.8665 11.4855 39.6561 9.40906 37.0397 7.97032C34.8298 6.75512 32.3909 6.02814 29.8872 5.83157C29.1227 5.77155 28.5 5.1555 28.5 4.38859Z"/>
										</mask>
										<path d="M28.5 4.38859C28.5 3.62168 29.1224 2.99509 29.8876 3.04699C32.8596 3.24861 35.7579 4.09606 38.3779 5.53677C41.4043 7.20096 43.9611 9.60279 45.8111 12.5193C47.6611 15.4358 48.7442 18.7724 48.96 22.2195C49.1757 25.6665 48.5171 29.1121 47.0452 32.2365C45.5733 35.3609 43.3358 38.0628 40.5406 40.0914C37.7453 42.1199 34.4829 43.4094 31.0561 43.84C27.6293 44.2706 24.1492 43.8285 20.9389 42.5547C18.1598 41.4519 15.6608 39.7567 13.6129 37.5934C13.0857 37.0365 13.1725 36.1576 13.7638 35.6692C14.3552 35.1809 15.2267 35.2687 15.7598 35.82C17.5056 37.6254 19.6191 39.0431 21.9633 39.9732C24.7386 41.0745 27.7472 41.4568 30.7098 41.0845C33.6723 40.7122 36.4928 39.5974 38.9094 37.8437C41.326 36.0899 43.2603 33.7541 44.5328 31.053C45.8053 28.3518 46.3747 25.373 46.1882 22.3929C46.0017 19.4129 45.0653 16.5283 43.4659 14.0069C41.8665 11.4855 39.6561 9.40906 37.0397 7.97032C34.8298 6.75512 32.3909 6.02814 29.8872 5.83157C29.1227 5.77155 28.5 5.1555 28.5 4.38859Z" fill="#FEFAF6" stroke="#FEFAF6" stroke-width="2" mask="url(#path-1-inside-1)"/>
										<g opacity="0.5">
											<mask id="path-2-inside-2" fill="white">
												<path d="M12.3627 33.7388C11.7151 34.1497 10.8525 33.9598 10.4865 33.2859C9.06713 30.6733 8.23038 27.7779 8.04119 24.7996C7.8226 21.3584 8.47554 17.9177 9.93959 14.7958C11.4036 11.6739 13.6315 8.9718 16.417 6.93944C18.8278 5.18044 21.589 3.97235 24.5052 3.39297C25.2574 3.24353 25.955 3.78529 26.0532 4.54588C26.1514 5.30648 25.6127 5.99717 24.8621 6.15459C22.4089 6.66909 20.0873 7.69937 18.0539 9.18296C15.6458 10.94 13.7198 13.2761 12.454 15.975C11.1883 18.6739 10.6238 21.6485 10.8128 24.6235C10.9724 27.1355 11.6648 29.5793 12.8379 31.7944C13.1968 32.4721 13.0102 33.3279 12.3627 33.7388Z"/>
											</mask>
											<path d="M12.3627 33.7388C11.7151 34.1497 10.8525 33.9598 10.4865 33.2859C9.06713 30.6733 8.23038 27.7779 8.04119 24.7996C7.8226 21.3584 8.47554 17.9177 9.93959 14.7958C11.4036 11.6739 13.6315 8.9718 16.417 6.93944C18.8278 5.18044 21.589 3.97235 24.5052 3.39297C25.2574 3.24353 25.955 3.78529 26.0532 4.54588C26.1514 5.30648 25.6127 5.99717 24.8621 6.15459C22.4089 6.66909 20.0873 7.69937 18.0539 9.18296C15.6458 10.94 13.7198 13.2761 12.454 15.975C11.1883 18.6739 10.6238 21.6485 10.8128 24.6235C10.9724 27.1355 11.6648 29.5793 12.8379 31.7944C13.1968 32.4721 13.0102 33.3279 12.3627 33.7388Z" fill="#FEFAF6" stroke="#FEFAF6" stroke-width="2" mask="url(#path-2-inside-2)"/>
										</g>
										<path d="M28.0025 18.2517L23.0617 26.5C22.9598 26.6764 22.9059 26.8764 22.9053 27.0801C22.9048 27.2838 22.9575 27.4842 23.0584 27.6611C23.1593 27.8381 23.3048 27.9856 23.4803 28.0889C23.6559 28.1922 23.8555 28.2478 24.0592 28.25H33.9408C34.1445 28.2478 34.3441 28.1922 34.5197 28.0889C34.6952 27.9856 34.8407 27.8381 34.9416 27.6611C35.0425 27.4842 35.0952 27.2838 35.0947 27.0801C35.0941 26.8764 35.0402 26.6764 34.9383 26.5L29.9975 18.2517C29.8935 18.0802 29.7471 17.9385 29.5724 17.8401C29.3976 17.7417 29.2005 17.6901 29 17.6901C28.7995 17.6901 28.6024 17.7417 28.4276 17.8401C28.2529 17.9385 28.1065 18.0802 28.0025 18.2517V18.2517Z" stroke="#FEFAF6" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
										<path d="M29 21.25V23.5833" stroke="#FEFAF6" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
										<path d="M29 25.9167H29.0067" stroke="#FEFAF6" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
									</svg>
									<div class="ml-3">
										<div class="ubuntu text-sm text-white">Doctor Availability</div>
										<div class="ubuntu text-2xl text-white">75%</div>
									</div>
								</div>
								<div class="flex flex-row mt-2 h-8 items-center">
									<div class="relative w-full h-8">
										<img :src="require('@/assets/images/avatar-2.png')" alt="avatar" class="w-8 h-8 object-cover border-white border-2 rounded-full absolute left-0">
										<img :src="require('@/assets/images/avatar-3.png')" alt="avatar" class="w-8 h-8 object-cover border-white border-2 rounded-full absolute left-6">
										<img :src="require('@/assets/images/avatar-4.png')" alt="avatar" class="w-8 h-8 object-cover border-white border-2 rounded-full absolute left-12">
										<img :src="require('@/assets/images/avatar-5.png')" alt="avatar" class="w-8 h-8 object-cover border-white border-2 rounded-full absolute left-24 transform -translate-x-3/4">
									</div>
									<div class="text-xs text-white opacity-50 w-24">VIEW ALL</div>
								</div>
							</div>
						</div>
						<!-- end card-4 -->

						<!-- card-4 -->
						<div class="w-1/2 px-3 py-4">
							<div class="card-2 py-4 px-5 rounded-2xl">
								<div class="flex flex-row">
									<svg width="58" height="58" viewBox="0 0 58 58" fill="none" xmlns="http://www.w3.org/2000/svg">
										<path d="M24 29L27.5 33L34.5 26" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
										<mask id="path-2-inside-1" fill="white">
											<path d="M28.9914 9.87997C28.9914 9.11306 29.6139 8.48646 30.379 8.53835C34.8221 8.83967 39.0607 10.5817 42.4406 13.5198C46.1709 16.7625 48.604 21.2437 49.2919 26.1383C49.9798 31.0329 48.8762 36.0112 46.1842 40.1564C43.4922 44.3017 39.3932 47.3348 34.642 48.6972C29.8908 50.0596 24.8074 49.6595 20.3278 47.5707C15.8482 45.4819 12.2742 41.8449 10.2638 37.3295C8.25339 32.8142 7.94207 27.7245 9.38715 22.9978C10.6965 18.7151 13.3679 14.9916 16.9762 12.3816C17.5975 11.9321 18.4574 12.1337 18.8639 12.784V12.784C19.2703 13.4344 19.0686 14.2868 18.452 14.7429C15.4095 16.9933 13.1565 20.1676 12.043 23.8098C10.7937 27.8962 11.0629 32.2963 12.8009 36.1999C14.5389 40.1036 17.6288 43.2478 21.5015 45.0537C25.3742 46.8595 29.769 47.2054 33.8765 46.0276C37.9841 44.8498 41.5277 42.2276 43.855 38.6439C46.1823 35.0602 47.1364 30.7563 46.5417 26.5248C45.947 22.2933 43.8435 18.4192 40.6186 15.6158C37.7442 13.1171 34.1514 11.6191 30.3787 11.3229C29.6142 11.2629 28.9914 10.6469 28.9914 9.87997V9.87997Z"/>
										</mask>
										<path d="M28.9914 9.87997C28.9914 9.11306 29.6139 8.48646 30.379 8.53835C34.8221 8.83967 39.0607 10.5817 42.4406 13.5198C46.1709 16.7625 48.604 21.2437 49.2919 26.1383C49.9798 31.0329 48.8762 36.0112 46.1842 40.1564C43.4922 44.3017 39.3932 47.3348 34.642 48.6972C29.8908 50.0596 24.8074 49.6595 20.3278 47.5707C15.8482 45.4819 12.2742 41.8449 10.2638 37.3295C8.25339 32.8142 7.94207 27.7245 9.38715 22.9978C10.6965 18.7151 13.3679 14.9916 16.9762 12.3816C17.5975 11.9321 18.4574 12.1337 18.8639 12.784V12.784C19.2703 13.4344 19.0686 14.2868 18.452 14.7429C15.4095 16.9933 13.1565 20.1676 12.043 23.8098C10.7937 27.8962 11.0629 32.2963 12.8009 36.1999C14.5389 40.1036 17.6288 43.2478 21.5015 45.0537C25.3742 46.8595 29.769 47.2054 33.8765 46.0276C37.9841 44.8498 41.5277 42.2276 43.855 38.6439C46.1823 35.0602 47.1364 30.7563 46.5417 26.5248C45.947 22.2933 43.8435 18.4192 40.6186 15.6158C37.7442 13.1171 34.1514 11.6191 30.3787 11.3229C29.6142 11.2629 28.9914 10.6469 28.9914 9.87997V9.87997Z" fill="#FEFAF6" stroke="#FEFAF6" stroke-width="2" mask="url(#path-2-inside-1)"/>
										<g opacity="0.5">
											<mask id="path-3-inside-2" fill="white">
												<path d="M20.4408 11.8995C20.0977 11.2136 20.374 10.3747 21.0815 10.0788C22.2929 9.57219 23.5502 9.18311 24.836 8.91695C25.587 8.7615 26.2888 9.29766 26.393 10.0574V10.0574C26.4973 10.8172 25.9642 11.5122 25.2149 11.6756C24.2286 11.8907 23.2625 12.1897 22.3271 12.5693C21.6164 12.8577 20.784 12.5853 20.4408 11.8995V11.8995Z"/>
											</mask>
											<path d="M20.4408 11.8995C20.0977 11.2136 20.374 10.3747 21.0815 10.0788C22.2929 9.57219 23.5502 9.18311 24.836 8.91695C25.587 8.7615 26.2888 9.29766 26.393 10.0574V10.0574C26.4973 10.8172 25.9642 11.5122 25.2149 11.6756C24.2286 11.8907 23.2625 12.1897 22.3271 12.5693C21.6164 12.8577 20.784 12.5853 20.4408 11.8995V11.8995Z" fill="#FEFAF6" stroke="#FEFAF6" stroke-width="2" mask="url(#path-3-inside-2)"/>
										</g>
									</svg>
									<div class="ml-3">
										<div class="ubuntu text-sm text-white">Nurse Availability</div>
										<div class="ubuntu text-2xl text-white">98%</div>
									</div>
								</div>
								<div class="flex flex-row mt-2 h-8 items-center">
									<div class="relative w-full h-8">
										<img :src="require('@/assets/images/avatar-6.png')" alt="avatar" class="w-8 h-8 object-cover border-white border-2 rounded-full absolute left-0">
										<img :src="require('@/assets/images/avatar-7.png')" alt="avatar" class="w-8 h-8 object-cover border-white border-2 rounded-full absolute left-6">
										<img :src="require('@/assets/images/avatar-8.png')" alt="avatar" class="w-8 h-8 object-cover border-white border-2 rounded-full absolute left-12">
										<img :src="require('@/assets/images/avatar-9.png')" alt="avatar" class="w-8 h-8 object-cover border-white border-2 rounded-full absolute left-24 transform -translate-x-3/4">
									</div>
									<div class="text-xs text-white opacity-50 w-24">VIEW ALL</div>
								</div>
							</div>
						</div>
						<!-- end card-4 -->

						<!-- card-6 -->
						<div class="w-full px-3 py-4">
							<div class="w-full h-full bg-white p-5 rounded-2xl">
								<div class="flex flex-row justify-between mb-4">
									<div>
										<div class="ubuntu font-bold">Nurse Chat Room</div>
										<div class="relative w-full h-8 transform scale-80">
											<img :src="require('@/assets/images/avatar-6.png')" alt="avatar" class="w-8 h-8 object-cover border-white border-2 rounded-full absolute left-0">
											<img :src="require('@/assets/images/avatar-7.png')" alt="avatar" class="w-8 h-8 object-cover border-white border-2 rounded-full absolute left-6">
											<img :src="require('@/assets/images/avatar-8.png')" alt="avatar" class="w-8 h-8 object-cover border-white border-2 rounded-full absolute left-12">
											<img :src="require('@/assets/images/avatar-9.png')" alt="avatar" class="w-8 h-8 object-cover border-white border-2 rounded-full absolute left-24 transform -translate-x-3/4">
										</div>
									</div>
									<div class="text-xs bg-indigo-200 text-indigo-800 px-4 py-2 rounded-lg table">Start new chat</div>
								</div>
								<div class="border-t border-gray-200 pt-4">
									<div class="flex flex-row">
										<img :src="require('@/assets/images/avatar-2.png')" alt="avatar" class="w-8 h-8 object-cover rounded-full">
										<div class="ml-4 text-xs p-2 bg-chat rounded-full ubuntu">Botak, can you come to room no. 312 ?</div>
									</div>
									<div class="flex flex-row justify-end mt-2">
										<div class="ml-4 text-xs p-2 bg-chat-2 rounded-full ubuntu">I’m lazy, why ?</div>
										<img :src="require('@/assets/images/avatar.png')" alt="avatar" class="w-8 h-8 object-cover rounded-full">
									</div>
									<div class="flex flex-row mt-2">
										<img :src="require('@/assets/images/avatar-2.png')" alt="avatar" class="w-8 h-8 object-cover rounded-full">
										<div class="ml-4 text-xs p-2 bg-chat rounded-full ubuntu">Patient was dying, you better come here</div>
									</div>
									<div class="flex flex-row justify-end mt-2">
										<div class="ml-4 text-xs p-2 bg-chat-2 rounded-full ubuntu">Let him die then</div>
										<img :src="require('@/assets/images/avatar.png')" alt="avatar" class="w-8 h-8 object-cover rounded-full">
									</div>
									<div class="flex flex-row mt-2">
										<img :src="require('@/assets/images/avatar-3.png')" alt="avatar" class="w-8 h-8 object-cover rounded-full">
										<div class="ml-4 text-xs p-2 bg-chat rounded-full ubuntu">You’re fired. Get your ass outa here.</div>
									</div>
									<div class="mt-6 relative">
										<input type="text" placeholder="Type a message..." class="w-full p-3 rounded-lg border text-sm pr-12">
										<i class="fa fa-paper-plane absolute top-0 right-0 p-4 text-indigo-600"></i>
									</div>
								</div>
							</div>
						</div>
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

	export default {
		name: 'App',
		components: {
			NavItem,
			Reports,
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