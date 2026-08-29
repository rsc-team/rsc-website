<script>
	const goldCount = 4;
</script>

{#snippet slotBox(sizeClass)}
	<div class="sponsor-slot rounded-3xl bg-navy {sizeClass}"></div>
{/snippet}

<div class="relative w-full font-sweetsquare">
	<div
		class="pointer-events-none fixed inset-0 z-0 bg-navy bg-[url(/assets/sponsors-bg.png)] bg-cover bg-center"
	>
		<div class="absolute inset-0 bg-gradient-to-b from-black/45 via-navy/70 to-black/90"></div>
	</div>

	<!-- Hero -->
	<section class="relative z-10 flex h-screen w-full items-center justify-center px-6">
		<div class="flex max-w-5xl flex-col items-center text-center">
			<h1
				class="text-6xl font-black text-gold drop-shadow-logo sm:text-7xl lg:text-8xl xl:text-9xl"
			>
				Sponsors
			</h1>
			<div class="mt-4 h-[3px] w-48 bg-red sm:w-64 lg:w-80"></div>
			<p
				class="mt-8 max-w-3xl text-lg font-bold text-white drop-shadow-small sm:text-2xl lg:text-3xl"
			>
				Rutgers Solar Car would not exist without your help! We appreciate any and
				all donations.
			</p>
			<p
				class="mt-8 max-w-3xl text-lg font-bold text-white drop-shadow-small sm:text-2xl lg:text-3xl"
			>
				If you're interested in becoming one of our sponsors, please contact us
				through our email or social media platforms!
			</p>
			<div class="mt-12 flex flex-col gap-5 sm:flex-row sm:gap-8">
				<a
					href="#"
					class="rounded-full bg-red px-10 py-4 text-xl font-black text-white transition-all hover:bg-white hover:text-navy sm:text-2xl lg:px-12 lg:text-3xl"
				>
					Become A Sponsor
				</a>
				<a
					href="#"
					class="rounded-full bg-red px-10 py-4 text-xl font-black text-white transition-all hover:bg-white hover:text-navy sm:text-2xl lg:px-12 lg:text-3xl"
				>
					Our Sponsor Packet
				</a>
			</div>
		</div>
	</section>

	<!-- Scarlet -->
	<section class="relative z-10 flex h-screen w-full flex-col items-center justify-center px-6 pt-16">
		<h2 class="text-5xl font-black text-red drop-shadow-logo sm:text-6xl lg:text-7xl xl:text-8xl">
			Scarlet
		</h2>
		<div class="mt-3 h-[3px] w-40 bg-red sm:w-56 lg:w-72"></div>
		<div class="mt-10 flex flex-col items-center gap-6 lg:mt-14 lg:gap-8">
			<div class="flex flex-wrap justify-center gap-5 lg:gap-8">
				{#each { length: 3 } as _}
					{@render slotBox('size-28 sm:size-36 lg:size-48')}
				{/each}
			</div>
			<div class="flex flex-wrap justify-center gap-5 lg:gap-8">
				{#each { length: 2 } as _}
					{@render slotBox('size-28 sm:size-36 lg:size-48')}
				{/each}
			</div>
		</div>
	</section>

	<!-- Gold -->
	<section class="relative z-10 flex h-screen w-full flex-col items-center justify-center px-6 pt-16">
		<h2
			class="text-5xl font-black text-gold drop-shadow-[0_4px_0_#b07d12] sm:text-6xl lg:text-7xl xl:text-8xl"
		>
			Gold
		</h2>
		<div class="mt-3 h-[3px] w-32 bg-gold sm:w-44 lg:w-56"></div>
		<div class="mt-10 grid grid-cols-2 gap-5 lg:mt-14 lg:gap-8">
			{#each { length: goldCount } as _}
				{@render slotBox('size-32 sm:size-40 lg:size-52')}
			{/each}
		</div>
	</section>

	<!-- Silver -->
	<section class="relative z-10 flex h-screen w-full flex-col items-center justify-center px-6 pt-16">
		<h2
			class="text-5xl font-black text-silver drop-shadow-logo sm:text-6xl lg:text-7xl xl:text-8xl"
		>
			Silver
		</h2>
		<div class="mt-3 h-[3px] w-36 bg-silver sm:w-52 lg:w-64"></div>
		<div class="mt-10 flex flex-col items-center gap-5 lg:mt-14 lg:gap-7">
			<div class="flex flex-wrap justify-center gap-4 lg:gap-6">
				{#each { length: 4 } as _}
					{@render slotBox('size-20 sm:size-28 lg:size-40')}
				{/each}
			</div>
			<div class="flex flex-wrap justify-center gap-4 lg:gap-6">
				{#each { length: 3 } as _}
					{@render slotBox('size-20 sm:size-28 lg:size-40')}
				{/each}
			</div>
		</div>
	</section>
</div>

<style>
	.sponsor-slot {
		position: relative;
		overflow: hidden;
		cursor: pointer;
		transition:
			transform 0.4s var(--ease-frame),
			box-shadow 0.4s ease;
	}

	.sponsor-slot:hover {
		transform: scale(1.08) translateY(-6px);
		box-shadow: -4px 8px 0 var(--color-shadow);
	}

	.sponsor-slot::after {
		content: '';
		position: absolute;
		inset: 0;
		background: linear-gradient(
			120deg,
			transparent 30%,
			rgba(255, 255, 255, 0.22) 50%,
			transparent 70%
		);
		transform: translateX(-130%);
		pointer-events: none;
	}

	.sponsor-slot:hover::after {
		animation: slot-shine 0.55s ease-out;
	}

	@keyframes slot-shine {
		to {
			transform: translateX(130%);
		}
	}
</style>
