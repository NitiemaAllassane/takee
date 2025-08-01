<script>
    let { content, color="#fff", border="6px" }  = $props();
</script>

<span 
    class="text-black py-1 px-2 rounded-md font-bold"
    style="background-color: {color}; border-radius: {border}; "
>
    { content }
</span>