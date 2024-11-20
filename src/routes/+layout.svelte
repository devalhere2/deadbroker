<script lang="ts">
	import '../app.css';
	import * as Avatar from "$lib/components/ui/avatar/index.js";
	let { children } = $props();

	import Calculator from "lucide-svelte/icons/calculator";
	import Calendar from "lucide-svelte/icons/calendar";
	import CreditCard from "lucide-svelte/icons/credit-card";
	import Settings from "lucide-svelte/icons/settings";
	import Smile from "lucide-svelte/icons/smile";
	import User from "lucide-svelte/icons/user";
	import * as Command from "$lib/components/ui/command/index.js";
</script>

<nav class="flex h-12" style="border-bottom: 1px solid #ccc; box-sizing: border-box;">
	<div class="grow flex items-center">
		<div class="site-name mx-8">webName</div>
	</div>
	<div class="search-bar w-80 flex items-center">
		<Command.Root class="max-w-[450px] h-8 rounded-lg border shadow-md">
		  <Command.Input class="h-8" placeholder="Type a command or search..." />
		  <Command.List >
			<Command.Empty>No results found.</Command.Empty>
			<Command.Group heading="Suggestions">
			  <Command.Item>
				<Calendar class="mr-2 h-4 w-4" />
				<span>Calendar</span>
			  </Command.Item>
			  <Command.Item>
				<Smile class="mr-2 h-4 w-4" />
				<span>Search Emoji</span>
			  </Command.Item>
			  <Command.Item>
				<Calculator class="mr-2 h-4 w-4" />
				<span>Calculator</span>
			  </Command.Item>
			</Command.Group>
			<Command.Separator />
			<Command.Group heading="Settings">
			  <Command.Item>
				<User class="mr-2 h-4 w-4" />
				<span>Profile</span>
				<Command.Shortcut>⌘P</Command.Shortcut>
			  </Command.Item>
			  <Command.Item>
				<CreditCard class="mr-2 h-4 w-4" />
				<span>Billing</span>
				<Command.Shortcut>⌘B</Command.Shortcut>
			  </Command.Item>
			  <Command.Item>
				<Settings class="mr-2 h-4 w-4" />
				<span>Settings</span>
				<Command.Shortcut>⌘S</Command.Shortcut>
			  </Command.Item>
			</Command.Group>
		  </Command.List>
		</Command.Root>
	  </div>
	<div class="profile flex items-center mx-4">
		<Avatar.Root class="h-8 w-8">
			<Avatar.Image src="https://github.com/shadcn.png" alt="@shadcn" />
			<Avatar.Fallback>
				<svg
				       xmlns="http://www.w3.org/2000/svg"
				         viewBox="0 0 24 24"
				         width="24"
				         height="24"
				         fill="#0088ff"
				     >
				         <path d="M12 12c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4     4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z"/>
			  
			</Avatar.Fallback>
		</Avatar.Root>
	</div>
	
</nav>

{@render children()}
