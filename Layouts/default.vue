<template>
	<div class="bg-neutral-950 text-white min-h-screen min-w-screen">
		<Sidbar/>
		<main class="sm:pl-28 sm:pr-40 lg:pl-44 sm:pt-6 min-w-screen p-3">
			<slot/>
		 </main>
	  	<Aside/>
		<FooterInfo/>
		<MobileNav/>
	</div>
</template>