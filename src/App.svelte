<script>
  // import BindingSelectInput from "./BindingSelectInput.svelte";

  import MotionTweened from "./MotionTweened.svelte";
  import Stores from "./Stores.svelte";
  import Transitions from "./Transitions.svelte";

  // import BeforeAndAfterUpdate from "./BeforeAndAfterUpdate.svelte";
  // import Tick from "./Tick.svelte";

  // import BindingComponent from "./BindingComponent.svelte";
  // import OnMount from "./OnMount.svelte";
  // import Nested from "../src/Nested.svelte";
  // import ButtonClick from "../src/ButtonClick.svelte";
  // import KeyedEachIterating from "./KeyedEachIterating.svelte";
  // import Await from "./Await.svelte";
  // import Events from "./Events.svelte";
  // import InnerDispatcher from "./InnerDispatcher.svelte";
  // import EventForwarding from "./EventForwarding.svelte";
  // import BindingTextInput from "./BindingTextInput.svelte";
  // import BindingNumericInput from "./BindingNumericInput.svelte";
  // import BindingCheckboxInput from "./BindingCheckboxInput.svelte";
  // import BindingGroupInput from "./BindingGroupInput.svelte";
  // import BindingContenteditable from "./BindingContenteditable.svelte";
  // import BindingEach from "./BindingEach.svelte";
  // import BindingDimensions from "./BindingDimensions.svelte";
  // import BindingMediaElements from "./BindingMediaElements.svelte";
  // import BindingThis from "./BindingThis.svelte";
  // import BindingTextareaInput from "./BindingTextareaInput.svelte";
  export let name;
  // const theAnswer = "Gak ada jawaban tu";

  // function handleMessage(event) {
  // 	alert(event.detail.text);
  // }

  // function eventForwardingYo() {
  // 	alert("Apa kau bengak!");
  // }
  // for Binding Component
  // let pin;
  // $: view = pin ? pin.replace(/\d(?!$)/g, "*") : "enter your pin";

  // function handleSubmit() {
  //   alert(`submitted ${pin}`);
  // }
</script>

<main>
  <h1>Hello {name.toUpperCase()}!</h1>
  <p class="telorKambing">
    Visit the
    <a href="https://svelte.dev/tutorial">Svelte tutorial</a>
    to learn how to build Svelte apps.
  </p>
  <!-- <BindingSelectInput /> -->
  <!-- <BindingTextareaInput /><br /> -->
  <!-- <BindingGroupInput /> -->
  <!-- <BindingCheckboxInput />
	<BindingTextInput />
	<BindingNumericInput />
	<EventForwarding on:click={eventForwardingYo} />
	<InnerDispatcher on:dispatchHello={handleMessage} />
	<Events />
	<ButtonClick />
	<Nested {theAnswer} />
	<KeyedEachIterating />
	<Await /> -->
  <!-- <BindingContenteditable /> -->
  <!-- <BindingEach /> -->
  <!-- <BindingMediaElements /> -->
  <!-- <BindingDimensions /> -->
  <!-- <BindingThis /> -->
  <!-- for Binding Component START -->
  <!-- <h1 style="color: {pin ? '#333' : '#ccc'}">{view}</h1> -->
  <!-- <BindingComponent bind:value={pin} on:submit={handleSubmit} /> -->
  <!-- for Binding Component END -->
  <!-- <OnMount /> -->
  <!-- <BeforeAndAfterUpdate /> -->
  <!-- <Tick /> -->
  <!-- <Stores /> -->
  <!-- <MotionTweened /> -->
  <Transitions />
</main>

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
