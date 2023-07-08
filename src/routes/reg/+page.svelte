<script>
    import { fade } from "svelte/transition";
    var a = 0;
    function reg() {
        window.location.href = "/log";
        a = 1;
    }
</script>


<div class="text-column" id="div">
    <h1>REGISZTRÁCIÓ</h1>

    <form action="">
        <label for="username">FELHASZNÁLÓNÉV</label>
        <input type="text" name="username" />

        <label for="email">E-MAIL CÍM</label>
        <input type="text" name="email" />

        <label for="password">JELSZÓ</label>
        <input type="password" name="password" />

        <label for="password2">JELSZÓ MÉGEGYSZER</label>
        <input type="password" name="password2" />

        <button type="button" on:click={reg}>REGISZTRÁCIÓ</button>
    </form>
</div>
{#if a === 1}
    <style>
        #div {
            animation: fade-out 500ms;
        }
    </style>
{/if}

<style>
    button {
        position: relative;
        left: 50%;
        top: 15px;
    }
</style>
