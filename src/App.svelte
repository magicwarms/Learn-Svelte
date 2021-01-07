<script>
	import Nested from "../src/Nested.svelte";
	import ButtonClick from "../src/ButtonClick.svelte";
	import KeyedEachIterating from "./KeyedEachIterating.svelte";
	import Await from "./Await.svelte";
	import Events from "./Events.svelte";
	import InnerDispatcher from "./InnerDispatcher.svelte";
	import EventForwarding from "./EventForwarding.svelte";
	import BindingTextInput from "./BindingTextInput.svelte";
	export let name;
	const theAnswer = "Gak ada jawaban tu";

	function handleMessage(event) {
		alert(event.detail.text);
	}

	function eventForwardingYo() {
		alert("Apa kau bengak!");
	}
</script>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		/* text-transform: uppercase; */
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
	.telorKambing {
		color: blue;
	}
</style>

<main>
	<h1>Hello {name.toUpperCase()}!</h1>
	<p class="telorKambing">
		Visit the
		<a href="https://svelte.dev/tutorial">Svelte tutorial</a>
		to learn how to build Svelte apps.
	</p>
	<BindingTextInput />
	<EventForwarding on:click={eventForwardingYo} />
	<InnerDispatcher on:dispatchHello={handleMessage} />
	<Events />
	<ButtonClick />
	<Nested {theAnswer} />
	<KeyedEachIterating />
	<Await />
</main>
