<main>
	<header>
		<h1>Cinema Etiquette</h1>
	</header>

	<div class="intro">
		<p>You’re not bingeing Netflix on your couch.</p>
		<p>You’re in public, surrounded by people who also paid to be here.</p>
		<p>Respect the movie, respect the audience, and follow these simple rules:</p>
	</div>

	<ol>
		<li>
			<h2>
				<span class="number-bullet" style="--n: 1;">1</span>
				Be on time.
			</h2>
			<p>
				The movie starts 15 minutes after the advertised time. Ads and trailers give you plenty of
				buffer to grab snacks and drinks before the lights go down. Running late? Slide in quietly
				like a ninja, not like a lighthouse waving your phone torch.
			</p>
		</li>
		<li>
			<h2>
				<span class="number-bullet" style="--n: 2;">2</span>
				Phones away. Seriously.
			</h2>
			<p>
				No texts, no TikTok scrolling: turn it off or switch to airplane mode. If you must glance at
				the time, do it discreetly and with your screen dimmed. A glowing phone in the dark is more
				distracting than you think.
			</p>
		</li>
		<li>
			<h2>
				<span class="number-bullet" style="--n: 3;">3</span>
				Silence is golden.
			</h2>
			<p>
				A quick whisper is forgivable. A full conversation or a running commentary, not so much.
				Save your hot takes for after the credits.
			</p>
		</li>
		<li>
			<h2>
				<span class="number-bullet" style="--n: 4;">4</span>
				Snack smart.
			</h2>
			<p>
				Nibbling is fine, an endless rustling concert of popcorn and crisp packets is not.
				Eat quietly, and clean up after yourself — the staff shouldn’t have to shovel your leftovers
				off the carpet.
			</p>
		</li>
		<li>
			<h2>
				<span class="number-bullet" style="--n: 5;">5</span>
				Feet stay in check.
			</h2>
			<p>
				This isn’t 4DX. Don’t kick the seat in front of you, don’t take your shoes off, and
				definitely don’t put your feet on the headrest. We’re here for surround sound, not
				surround smell.
			</p>
		</li>
	</ol>

	<div class="outro">
		<p>Don’t be the villain.</p>
		<p>Be the reason cinema feels like magic every time.</p>
	</div>
</main>

<style lang="scss">
	main {
		width: 92vw;
		margin: 0 auto;
		display: flex;
		flex-direction: column;
		align-items: center;

		header {
			border: 4px solid goldenrod;
			border-radius: 2px;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
			width: 100%;
			max-width: 420px;
			height: 150px;
			margin: 32px auto;
			position: relative;
			transform-origin: center;

			background: linear-gradient(to bottom, lightgrey, lightgrey 3px, white 3px, white 100%);
			background-size: 100% 27px;
			background-position: 0 -10px;

			h1 {
				font-family: 'Duke', sans-serif;
				font-size: 4rem;
				color: black;
				text-transform: uppercase;
				text-align: center;
				display: table-caption;
				margin: 0;
			}

			@media (max-width: 420px) {
				height: 120px;
				background-size: 100% 21.6px;
				background-position: 0 -9px;

				h1 {
					font-size: 3.2rem;
				}
			}
		}

		p {
			text-align: center;
			margin: 4px 0;
			width: 100%;
			max-width: 720px;
			font-size: 1.1rem;
			line-height: 150%;
		}

		.outro {
			color: goldenrod;
			font-style: italic;
		}

		h2 {
			font-size: 1.1rem;
			text-align: center;
			display: inline-flex;
			flex-direction: column;
			align-items: center;
			margin: 0 0 10px;
			gap: 10px;
			color: goldenrod;

			.number-bullet {
				width: 36px;
				height: 36px;
				display: inline-flex;
				justify-content: center;
				align-items: center;
				font-family: 'Duke', sans-serif;
				font-size: 1.5rem;
				line-height: 100%;
				border: 1px solid goldenrod;
				border-radius: 50%;
				position: relative;

				&::before {
					content: '';
					position: absolute;
					inset: 0;
					border-radius: 50%;
					background-color: goldenrod;
					opacity: 0.4;
					/* clip-path: shape(
							from top,
							arc to calc(50% + 50% * sin(var(--n) * 60deg)) calc(50% - 50% * cos(var(--n) * 60deg))
							of 50% cw large,
							line to center
						);
					*/
					mask-image: conic-gradient(
						black 0deg calc(var(--n) * 60deg),
						transparent calc(var(--n) * 60deg) 360deg
					);
					mask-composite: add;
				}

				&::after {
					content: '';
					position: absolute;
					inset: 2px;
					border: 1px solid goldenrod;
					border-radius: 50%;
				}
			}
		}

		ol {
			list-style-type: none;
			display: flex;
			flex-wrap: wrap;
			justify-content: center;
			width: 100%;
			max-width: 1170px;
			margin: 32px 0 48px;
			padding: 0;
			column-gap: 48px;
			row-gap: 32px;

			li {
				display: flex;
				flex-direction: column;
				align-items: center;
				flex: 0 0 calc(33% - 32px);

				p {
					font-size: 1rem;
				}

				@media (max-width: 1300px) {
					flex: 0 0 calc(50% - 32px);
				}

				@media (max-width: 750px) {
					flex: 0 0 auto;
					width: 100%;
					max-width: 420px;
				}
			}
		}
	}
</style>
