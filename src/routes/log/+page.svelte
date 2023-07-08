<script>
	import { fade } from "svelte/transition";
    var a = 0;
    function log() {
        window.location.href = "/home";
        a= 1;
    }
</script>


<div class="text-column" id="div" >
	<h1>BEJELENTKEZÉS</h1>

	<form action="">

		<label for="username">FELHASZNÁLÓNÉV</label>
		<input type="text" name="username">

		

		<label for="password">JELSZÓ</label>
		<input type="password" name="password">

        
        <button type="button" on:click={log} >BEJELENTKEZÉS</button>
		

	</form>
</div>
{#if a === 1}
    <style>
        #div{
            animation: fade-out 500ms;
        }
    </style>
{/if}
<style>
    button{
        position: relative;
        left:50%;
        top: 15px;
    }
</style>