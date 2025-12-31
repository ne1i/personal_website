<script lang="ts">
	let { data } = $props();
	let textContent = $state(
		`<h1>This is a very cool website :P</h1>
<span>Thx guys !!!!</span>`
	);

	let linesCount = $derived(Math.max(textContent.split('\n').length, 10));
</script>

<div
	class="my-2 border-2 py-1 border-[#4c7797] bg-[#285577] font-mono font-bold mb-6 text-shadow-2xs"
>
	<h1 class="text-center text-3xl space-x-8">
		<img class="inline-block h-[1.5em]" src="/under_construction.gif" alt="Under construction" />
		<a class="hover:underline" href="/">
			<span> ~/Projects/aubetoile.dev </span>
		</a>
		<img class="inline-block h-[1.5em]" src="/under_construction.gif" alt="Under construction" />
	</h1>
</div>

<section class="flex justify-center mb-2"></section>

<section class="font-serif">
	<h2 class="text-3xl mb-2">
		<img src="/globe05.gif" alt="Globe" class="inline-block mr-2" /> Navigation
	</h2>
	<nav class="mb-4 pl-6">
		<ul class="list-disc flex gap-6">
			<li><a class="text-blue-500 hover:text-blue-600 visited:bg-purple-500" href="/">/home</a></li>
			<li>
				<a class="text-blue-500 hover:text-blue-600 visited:bg-purple-500" href="/tools">/tools</a>
			</li>
			<li>
				<a class="text-blue-500 hover:text-blue-600 visited:bg-purple-500" href="/edit">/edit</a>
			</li>
			<li>
				<a class="text-blue-500 hover:text-blue-600 visited:bg-purple-500" href="/code">/code</a>
			</li>
		</ul>
	</nav>
</section>

<div class="border-white border-3 flex font-mono relative mb-2">
	<div class="border-r-2 border-r-red-600 px-1 min-w-[3ch]">
		{#each Array(linesCount).keys() as i}
			{i + 1}
			<br />
		{/each}
	</div>
	<textarea
		bind:value={textContent}
		class="to-neutral-800 bg-linear-to-br from-neutral-950 grow outline-0 font-mono pl-2"
		name=""
		id=""
	></textarea>
	<div class="absolute bottom-2 right-2 opacity-40 flex gap-2">
		<img class="" src="/EmacsNow.gif" alt="Emacs Now!" />
		<img class="" src="/html_learn_it_today.gif" alt="HTML, learn it today !" />
	</div>
</div>

<p class="font-bold italic font-serif">Valentin's Custom Code Editor (VCCE)</p>

<footer class="text-sm font-serif font-bold italic">
	(C) {new Date().getFullYear()} -
	<a class="underline" href="https://aubetoile.dev">aubetoile.dev</a>
</footer>
