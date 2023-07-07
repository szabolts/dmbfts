<script>
	import { fade } from "svelte/transition";
	//import { backInOut } from "svelte/easing";
	import Log from "./log_page.svelte";
	let visible = true;

	let ns = 0;
	
	
	function reg() {
        //window.location.href = "/log";
		ns=2;
		visible = false;
    }
</script>

{#if visible}
	<div class="text-column" id="div" 	in:fade={{delay: 0, duration: 1000}} 
										out:fade={{delay: 0, duration: 1000}}>
		<h1>REGISZTRÁCIÓ</h1>

		<form action="">

			<label for="username">FELHASZNÁLÓNÉV</label>
			<input type="text" name="username">

			<label for="email">E-MAIL CÍM</label>
			<input type="text" name="email">

			<label for="password">JELSZÓ</label>
			<input type="password" name="password">

			<label for="password2">JELSZÓ MÉGEGYSZER</label>
			<input type="password" name="password2">


			<button type="button" on:click={reg} >REGISZTRÁCIÓ</button>
			
		</form>
	</div>
{/if}

{#if ns === 2}
	<div transition:fade >
		<Log></Log>
	</div>
{/if}

<style>
    button{
        position: relative;
        left:50%;
		top: 15px;
    }
</style>