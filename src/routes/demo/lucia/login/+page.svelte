<script lang='ts'>
	import { enhance } from '$app/forms';
	import type { ActionData } from './$types';

	let { form }: { form: ActionData } = $props();
</script>

<h1>Login/Register</h1>
<form method='post' action='?/login' use:enhance>
	<label for='username'>Username</label>
	<input id='username' name='username' />
	<br/>
	<label for = 'password'>Password</label>
	<input type='text' id='password' name='password' />
	<br/>
	<button>Login</button>
	<button formaction='?/register'>Register</button>
</form>
<p style='color: red'>{form?.message ?? ''}</p>
