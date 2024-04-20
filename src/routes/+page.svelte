<script lang="ts">
	import { Button } from '$lib/components/ui/button';
	import { Label } from '$lib/components/ui/label';
	import { Textarea } from '$lib/components/ui/textarea';
	import MagnifierFrame from './MagnifierFrame.svelte';
</script>

<main class="px-8 pb-12 pt-6 sm:pt-12 md:pb-28 md:pt-20 lg:pt-28">
	<section
		class="container grid grid-cols-1 items-start gap-x-24 gap-y-4 sm:gap-y-8 md:grid-rows-[auto_auto_auto] md:gap-y-10 lg:justify-between xl:grid-cols-[610px_1fr]"
	>
		<div>
			<h1 class="font-recoleta text-4xl/[120%] font-bold md:text-5xl/[120%] lg:text-[54px]/[120%]">
				Terms &amp; Conditions<br /><span class="text-primary">Analyser</span>
			</h1>
		</div>
		<div class="flex justify-center md:col-start-2 md:row-span-full">
			<MagnifierFrame
				class="h-auto w-10/12 max-w-xs sm:w-full md:max-w-sm lg:max-w-md xl:max-w-lg"
			/>
		</div>
		<div>
			<div class="space-y-4 @container @md:space-y-8">
				<Label class="block space-y-1">
					<h5>Paste terms and conditions</h5>
					<Textarea class="h-40 resize-none" placeholder="Paste terms and conditions here" />
				</Label>
				<div class="grid grid-cols-1 items-center @md:flex @md:justify-end">
					<Button size="lg">Analyse</Button>
				</div>
			</div>
		</div>
	</section>
</main>
