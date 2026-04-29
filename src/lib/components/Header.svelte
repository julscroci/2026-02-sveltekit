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
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        width: 100%;
        z-index: 9999;
        /* safe-area aware responsive top padding */
        padding-top: calc(env(safe-area-inset-top, 0px) + clamp(var(--size-2), 3vw, var(--size-6)));
        padding-bottom: var(--size-2);

        display: flex;
        gap: var(--size-8);
        justify-content: space-between;
        align-items: center;

        background: linear-gradient(180deg, rgb(0, 0, 0), rgba(0, 0, 0, 0));

    }
    nav {
        display: flex; gap: var(--size-6); 
        align-items: center;
    }
</style>