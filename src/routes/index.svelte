<script context="module">
    export const load = async ({ fetch }) => {
        const res =  await fetch('/api/posts');
        const data = await res.json();

        console.log(data);

        return {
            props: {
                data,
            }
        };
    };
</script>

<script>
    export let data;
</script>

<h1>Homepage</h1>
<pre>
    {JSON.stringify(data)}
</pre>