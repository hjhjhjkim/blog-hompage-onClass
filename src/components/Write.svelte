<script>
  import { navigate } from "svelte-routing";
  import axios from "axios";

  let title;
  let content;

  const submit = async () => {
    const res = await axios.post("http://blog-api.neulhan.com/create", {
      title: title,
      content: content,
    });
    if (res.data === 200) {
      navigate("/list");
    }
  };
</script>

<h1>write</h1>
<input type="text" bind:value={title} />
<input type="text" bind:value={content} />
<button on:click={submit}>작성</button>
