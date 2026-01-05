<script lang="ts">
	import './+layout.scss';
	import './xtras.css';
    import { onMount } from 'svelte';
	import Navbar from '$lib/Navbar.svelte';
	import Footer from "$lib/Footer.svelte"
	import "aos/dist/aos.css"
    import Aos from 'aos';

	onMount(() => {
		Aos.init()
	})

	onMount(async () => {

		let font = new FontFace("inter", "url(inter.woff2)")



		await font.load()

		document.fonts.add(font)
		
	})


	
</script>
<Navbar></Navbar>
<slot></slot>
<Footer></Footer>



