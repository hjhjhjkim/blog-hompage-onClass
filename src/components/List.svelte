import axios from "axios";
import { onMount } from "svelte";
import {Link} from "svelt-routing";

let posts;

onMount(async () => {
    const res = await axios.get("http://blog-api.neulhan.com/posts");
    posts = res.data;
})
</script>

<h1>LIST</h1>
{#if posts}
{#each posts as post}
<p><Link to="/detail/{post.id}">{post.title}</Link></p>
{/each}
{:else}
<p>로딩중...</p>
{/if}
