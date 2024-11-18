<script lang="ts">
	import '../app.css';
    import { Input } from "$lib/components/ui/input";

	let { children } = $props();
</script>

<nav class="flex h-12">
	<div class="grow flex ">
		<div class="site-name">deadbroker</div>
	</div>
	<div class="search-bar w-80">
		<Input type="text" placeholder="Search Locality ..." class="h-8"/>
	</div>
	<div class="profile">Profile</div>
</nav>


{@render children()}
