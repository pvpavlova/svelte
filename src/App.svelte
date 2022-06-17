<script>
	import Slider from "../components/Slider.svelte";
	import Color from "../components/Color.svelte";
  
	import { fullColorHex } from "../utils.js";
  
	let red = 100;
	let green = 0;
	let blue = 0;
	let hex = "";
  
	$: hex = fullColorHex(red, green, blue);
  </script>
  
  
  
  <main>
	<h1>Color Picker {hex}</h1>
	<Slider bind:color={red} colorType="Red" />
	<Slider bind:color={green} colorType="Green" />
	<Slider bind:color={blue} colorType="Blue" />
	<Color {hex} />
  </main>