<script lang="ts">
	import { enhance } from '$app/forms';
	const title = 'Sign up';
</script>

<svelte:head>
	<title>{title}</title>
</svelte:head>

<div class="centered">
	<h1>{title}</h1>
	<form method="POST" use:enhance>
		<input type="text" name="login" required placeholder="Login" />
		<input type="text" name="full-name" required placeholder="Full name" />
		<input type="email" name="email" required placeholder="Email" />
		<input type="password" name="password" required placeholder="Password" />
		<input type="password" name="confirm-password" required placeholder="Confirm password" />
		<div>
			<button>{title}</button>
		</div>
	</form>
</div>

<style>
	.centered {
		max-width: 20em;
		margin: 0 auto;
	}

	form {
		display: flex;
		flex-direction: column;
		row-gap: 1em;
	}
</style>
