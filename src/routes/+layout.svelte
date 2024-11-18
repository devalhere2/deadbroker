<script lang="ts">
	import '../app.css';
    import { Input } from "$lib/components/ui/input";
	import * as Avatar from "$lib/components/ui/avatar/index.js";
	let { children } = $props();
</script>

<nav class="flex h-12" style="border-bottom: 1px solid gray; box-sizing: border-box;">
	<div class="grow flex items-center">
		<div class="site-name mx-8">deadbroker</div>
	</div>
	<div class="search-bar w-80 flex items-center mx-8">
		<Input type="text" placeholder="Search Locality ..." class="h-8 bg-green-200"/>
	</div>
	<div class="profile">
		<Avatar.Root>
			<Avatar.Image src="https://github.com/shadcn.png" alt="@shadcn" />
			<Avatar.Fallback>CN</Avatar.Fallback>
		</Avatar.Root>
	</div>
</nav>


{@render children()}
