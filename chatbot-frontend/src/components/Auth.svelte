<script lang="ts">
	import supabase from '$lib/supabase';

	let email: string;

	const handleLogin = async () => {
		console.log(email);
		const { error } = await supabase.auth.signIn({ email });
		if (error) throw error;
	};
</script>

<form on:submit|preventDefault={handleLogin}>
	<div class="flex flex-col test-sm mb-2">
		<label class="font-bold mb-2 text-blue-500" for="email">Email</label>
		<input
			class="appearance-none shadow-sm border border-gray-200 p-2 focus:outline-none focus:border-gray-500 rounded-lg"
			type="email"
			placeholder="Your email"
			bind:value={email}
		/>
	</div>
	<button
		class="w-full shadow-sm rounded bg-blue-500 hover:bg-blue-600 test-white py-2 px-4"
		type="submit"
	>
		Log In
	</button>
</form>
