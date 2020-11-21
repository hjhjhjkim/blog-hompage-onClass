<script>
  import { onMount } from "svelte";
  import axios from "axios";

  export let id;
  let post;

  onMount(async () => {
    const res = await axios.get(`http://blog-api.neulhan.com/post/${id}`);
    post = res.data;
  });
</script>

{#if post}
  <h1>{post.title}</h1>
  <p>{post.content}</p>
{:else}
  <p>로딩중...</p>
{/if}
