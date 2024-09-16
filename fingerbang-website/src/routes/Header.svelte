<script>
	let burgerOpen = false;
</script>

<header>
	<nav>
		<!--Logo-->
		<div id="headerlogo">
			<img
				alt="Fingerbang logo"
				src="/images/community_icon_transparent.png"
				style="height:auto; max-width: 50px;"
			/>
		</div>
		<!--Navigation links-->
		<div id="navitem-container">
			<div class="navitem">
				<a href="/">Home</a>
			</div>
			<div class="navitem">
				<a href="/creators">Creators</a>
			</div>
			<div class="navitem">
				<a href="/contact">Contact</a>
			</div>
		</div>
		<!--Hamburger menu-->
		<!-- svelte-ignore a11y-click-events-have-key-events -->
		<!-- svelte-ignore a11y-no-static-element-interactions -->
		<div class="burgericons" on:click={() => (burgerOpen = !burgerOpen)}>
			<img class="iconBurg" src="/images/menu.png" alt="Hamburger Menu Icon" />
			<img class="iconClose" src="/images/close.png" alt="Hamburger Close Icon" />
		</div>
		{#if burgerOpen}
			<div class="burgernav">
				<div class="burgeritem"><a href="/">Home</a></div>
				<div class="burgeritem"><a href="/creators">Creators</a></div>
				<div class="burgeritem"><a href="/contact">Contact</a></div>
			</div>
		{/if}

		<!--Play Free button-->
		<div class="playButtonDiv">
			<a href="https://store.steampowered.com/app/2200380/Fingerbang_All_Bullets_Pointin/">
				<div class="playfreeButton">Download</div>
			</a>
		</div>
	</nav>
</header>

<style>
	.burgernav {
		position: fixed;
		z-index: 99;
		width: 100vw;
		height: auto;
		background-color: #070707;
		padding: 3rem 2rem 3rem 2rem;
		display: flex;
		flex-direction: column;
		gap: 1.5rem;
		top: 0;
	}
	.burgeritem a {
		color: rgb(239, 239, 239);
		text-decoration: none;
	}
	.burgeritem a:hover {
		text-decoration: underline;
	}

	.burgericons {
		z-index: 100;
		cursor: pointer;
		margin-right: 1rem;
		margin-left: auto;
	}
	.burgericons img {
		height: auto;
		max-width: 50px;
	}
	.iconClose {
		display: none;
	}
	header {
		background-color: #070707;
		height: 5rem;
		position: sticky;
		top: 0;
		z-index: 1;
		width: 100vw;
	}
	nav {
		display: flex;
		font-family: 'public pixel', sans-serif !important;
		height: 100%;
		flex-direction: row;
		align-items: center;
		text-transform: uppercase;
	}

	#navitem-container {
		display: flex;
		flex-direction: row;
		width: 500px;
		justify-content: space-between;
		margin-right: 1rem;
		margin-left: 1rem;
	}
	.playButtonDiv {
		margin-left: auto;
		margin-right: 1rem;
	}

	.playfreeButton {
		height: 50px;
		width: 250px;
		background: linear-gradient(to top, #999999 0%, #999999 50%, #d9d9d9 50%, #d9d9d9 100%);
		display: flex;
		justify-content: center;
		align-items: center;
		border: 3px solid #63016d;
		border-radius: 5px;
	}
	.playButtonDiv a {
		text-decoration: none;
		color: #63016d !important;
		font-size: 1.2rem;
		font-weight: 600;
		-webkit-text-stroke: 1px black;
	}

	#headerlogo {
		padding-left: 1rem;
		padding-right: 3rem;
	}

	.navitem {
		margin: 1rem;
	}

	.navitem a {
		color: rgb(239, 239, 239);
		text-decoration: none;
	}
	.navitem a:hover {
		text-decoration: underline;
	}
</style>
