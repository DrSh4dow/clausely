<script>
	import '../fonts.css';
	import '../app.pcss';
	import { Button } from '$lib/components/ui/button';
	import { ArrowDownIcon, MenuIcon } from 'lucide-svelte';
	import * as DropdownMenu from '$lib/components/ui/dropdown-menu';
	import * as Popover from '$lib/components/ui/popover';
</script>

<header class="px-8 pt-8 sm:pt-12 md:pt-14 lg:pt-16">
	<nav class="container flex items-center justify-between gap-x-8">
		<div class="flex items-center gap-x-8">
			<a href="/" class="font-recoleta text-[32px] font-black">Clausely</a>
		</div>
		<div class="hidden sm:block">
			<Popover.Root>
				<Popover.Trigger>
					<Button variant="outlinePrimary">
						<div class="flex items-center justify-center gap-x-1">
							<ArrowDownIcon class="h-6 w-6 min-w-6" />
							<h5>Clausely extension</h5>
						</div>
					</Button>
				</Popover.Trigger>
				<Popover.Content>Work in progress</Popover.Content>
			</Popover.Root>
		</div>
		<div class="sm:hidden">
			<DropdownMenu.Root>
				<DropdownMenu.Trigger>
					<MenuIcon class="h-6 w-6 min-w-6" />
				</DropdownMenu.Trigger>
				<DropdownMenu.Content>
					<DropdownMenu.Group>
						<DropdownMenu.Label>Options</DropdownMenu.Label>
						<DropdownMenu.Separator />
						<DropdownMenu.Item>Download extension</DropdownMenu.Item>
					</DropdownMenu.Group>
				</DropdownMenu.Content>
			</DropdownMenu.Root>
		</div>
	</nav>
</header>
<slot />
