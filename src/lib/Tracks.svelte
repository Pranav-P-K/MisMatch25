<script lang="ts">
	import { onMount } from "svelte";
	import trackPage from "../assets/trackPage.png";
	import tracks from "../assets/tracks.png";
	import background from "../assets/background.png";

	let slideIndex = 0;
	let titles = ["FinTech", "Web3", "DevTools", "OpenINO"];
	let texts = [
		"Financial technology is transforming the way we manage, invest, and transact money through innovative solutions like digital banking, blockchain, and AI-driven financial services.",
		"Blockchain and decentralized finance are revolutionizing the digital economy.",
		"Advanced tools and frameworks empower developers to build efficient solutions.",
		"Open Innovation fosters collaboration between industries, startups, and academia to drive technological advancements and solve global challenges.",
	];
	function plusDivs(n: number) {
		slideIndex = (slideIndex + n + titles.length) % titles.length;
	}

	onMount(() => {
		setInterval(() => {
			slideIndex = (slideIndex + 1) % titles.length;
		}, 10000);
	});
</script>

<svelte:head>
	<meta name="description" content="Svelte demo app" />
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" />
	<link
		href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<section id="tracks">
	<div class="welcome">
		<img src={tracks} alt="Welcome" class="trackimg" />
		<div class="trackSliderContainer">
			<img src={trackPage} alt="Track Page" class="trackPage" />
			<div class="trackSlider">
				<div class="tracks">
					<div class="content">
						{#each titles as title, index}
							<div class:hidden={index !== slideIndex}>
								<h1 class="title">{title}</h1>
								<p class="text">{texts[index]}</p>
							</div>
						{/each}
					</div>
					<div class="controlbtn">
						<div class="ctrlsec">
							<button
								class="prev glow-button"
								on:click={() => plusDivs(-1)}>Prev</button
							>
							<button
								class="next glow-button"
								on:click={() => plusDivs(1)}>Next</button
							>
						</div>
					</div>
				</div>
			</div>
		</div>
		<div class="track-bg">
			<img src={background} alt="track-bg">
		</div>
	</div>
</section>

<style>
	section {
		display: flex;
		justify-content: center;
		align-items: center;
		min-height: 100vh;
		margin: 5rem 0;
		padding: 0 1rem;
	}

	.welcome {
		display: flex;
		justify-content: center;
		align-items: center;
		position: relative;
		gap: 5rem;
		width: 100%;
		max-width: 1200px;
		flex-wrap: wrap;
	}

	.track-bg {
		z-index: -1;
		position: absolute;
	}

	.trackimg {
		position: relative;
		width: 100%;
		max-width: 500px;
		height: auto;
	}

	.trackSliderContainer {
		padding: auto;
		position: relative;
		transition: transform 0.4s ease-in-out;
		width: 100%;
		max-width: 500px;
	}

	.trackSliderContainer:hover {
		transform: scale(1.3);
	}

	.trackPage {
		width: 100%;
		height: auto;
		position: relative;
		z-index: 0;
	}

	.trackSlider {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		display: flex;
		justify-content: center;
		align-items: center;
		z-index: 1;
	}

	.content {
		position: absolute;
		top: 36%;
		left: 32%;
		text-align: left;
		color: #81f7ff;
		font-family: "Press Start 2P", cursive;
		width: 190px;
	}

	.title {
		letter-spacing: 1px;
		font-size: 1.2rem;
		color: white;
		margin-bottom: 10px;
	}

	.text {
		padding-left: 15px;
		font-size: 0.6rem;
		line-height: 1.5;
		overflow: auto;
		scrollbar-width: none;
		height: 90px;
	}

	.hidden {
		display: none;
	}

	.glow-button {
		background-color: #260b24;
		border: 3px solid #f99fd9;
		color: #f9bae3;
		width: 115px;
		height: 55px;
		font-size: 17px;
		font-weight: bold;
		cursor: pointer;
		transition: 0.3s;
		border-radius: 15px;
		box-shadow:
			0 0 15px #900a54,
			0 0 20px #900a54 inset;
		text-transform: uppercase;
		letter-spacing: 2px;
		display: flex;
		align-items: center;
		justify-content: center;
		position: relative;
		font-family: "Press Start 2P", serif;
	}

	.glow-button:hover {
		box-shadow:
			0 0 25px #ff00ff,
			0 0 20px #ff007f inset;
		transform: scale(1.1);
	}

	.prev {
		position: absolute;
		bottom: 7%;
		left: 18%;
	}

	.next {
		position: absolute;
		bottom: 7%;
		right: 18%;
	}

	/* Media Queries */
	@media (max-width: 1024px) {
		.welcome {
			gap: 2rem;
		}

		.content {
			width: 160px;
		}

		.title {
			font-size: 1rem;
		}

		.text {
			font-size: 0.5rem;
			height: 80px;
		}

		.glow-button {
			width: 100px;
			height: 45px;
			font-size: 14px;
		}
	}

	@media (max-width: 768px) {
		.welcome {
			flex-direction: column;
			gap: 3rem;
		}

		.trackSliderContainer:hover {
			transform: scale(1.05);
		}

		.glow-button {
			width: 90px;
			height: 40px;
			font-size: 12px;
		}
	}

	@media (max-width: 480px) {
		section {
			margin: 1rem 0;
		}

		.content {
			width: 140px;
		}

		.title {
			font-size: 0.8rem;
		}

		.text {
			font-size: 0.4rem;
			height: 70px;
			padding-left: 10px;
		}

		.glow-button {
			width: 80px;
			height: 35px;
			font-size: 10px;
			letter-spacing: 1px;
		}
	}
</style>
