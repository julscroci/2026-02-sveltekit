<script>
    import Link from "$lib/components/Link.svelte";
</script>

<header class="safe-area">
    <Link title="t(r)opic" ref="/" />

    <nav>
        <Link title="About" ref="/about" />
        <Link title="@julscroci" ref="https://www.instagram.com/julscroci" 
        />
    </nav>
</header>


<style>
    header{
        padding-block: var(--size-0);
        display: flex; gap: var(--size-8); 
        justify-content: space-between; 
        align-items: center;
    }
    nav {
        display: flex; 
        gap: var(--size-6); 
        align-items: center;
    }
</style>