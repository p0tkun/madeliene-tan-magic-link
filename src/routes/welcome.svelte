<script>
    import supabase from '$lib/db';

    async function signOut() {
   	 const { error } = await supabase.auth.signOut();

   	 if (error) alert(error.message); // alert if error
    }
</script>

<div class="text-center">
    <h1 class="bg-warning p-5">Welcome!</h1>

    <button on:click={signOut}>Logout</button>
</div>