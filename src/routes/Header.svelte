<script>
	let isOpen = $state(false);
</script>

<header>
	<nav class="navbar bg-primary px-4 py-5 text-primary-content md:px-10">
		<div class="navbar-start">
			<a href="/" class="btn btn-ghost text-[90%] md:text-4xl lg:flex">
				<p class="logo text-[90%] font-black md:text-4xl dark:text-white z-50">OFF-BEAT TOURS</p></a
			>
		</div>

		<!-- Mobile menu -->
		{#if isOpen}
			<div class="fixed right-0 top-[6rem] w-[50%] rounded-md bg-primary p-4 lg:hidden ">
				<div class="flex flex-col gap-4">
					<a href="/" class="btn btn-ghost w-full text-left" onclick={() => (isOpen = false)}
						>Gallery</a
					>
					<a href="/aboutUs" class="btn btn-ghost w-full text-left" onclick={() => (isOpen = false)}
						>About</a
					>
					<a href="/itenary" class="btn btn-ghost w-full text-left" onclick={() => (isOpen = false)}
						>Itenary</a
					>
					<p class="px-2 text-sm underline">Contact: +91 789662400</p>
				</div>
			</div>
		{/if}

		<!-- Desktop menu -->
		<div class="navbar-center hidden justify-between lg:flex">
			<a href="/" class="btn btn-ghost">Tour of Dima Hasao</a>
			<a href="/itenary" class="btn btn-ghost">Itenary</a>
			<a href="/" class="btn btn-ghost">Gallery</a>
			<a href="/aboutUs" class="btn btn-ghost">About</a>
		</div>
		<div class="navbar-end">
			<p class="hidden px-5 text-sm underline lg:flex">Contact: +91 789662400</p>
			<div class="lg:hidden">
				<!-- Hamburger button -->
				<button class="btn btn-ghost" onclick={() => (isOpen = !isOpen)}>
					{#if !isOpen}
						<i class="fas fa-bars text-2xl"></i>
					{:else}
						<i class="fas fa-times text-2xl"></i>
					{/if}
				</button>
			</div>
		</div>
	</nav>
</header>

<style>
	.logo {
		color: transparent;
		-webkit-background-clip: text;
		background-clip: text;
		background-image: url('https://images.unsplash.com/photo-1533053157386-fec89c75d8a7?q=80&w=1975&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D');
		background-image: contain;
		background-position: top;
		padding: 0 5rem;
		text-shadow: -5px -3px 10px rgba(101, 103, 89, 0.5);
	}

	/* Add smooth transition for mobile menu */
</style>
