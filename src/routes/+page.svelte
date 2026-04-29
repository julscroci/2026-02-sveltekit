<script>
    import Filter from "$lib/components/Filter.svelte"; 
    import Project from "$lib/components/Project.svelte";

    const { data } = $props();

    let currentYear = $state(data.years [0].number) ;
    let projects = $derived.by(() => {
        return data.years.find((year) => {
            return year.number == currentYear;
        }).projects;
    });
</script>


<section class="safe-area hero">
    <h1>
        Benvenuto su t(r)opic, uno spazio dedicato alle mie piante tropicali e alla loro cura quotidiana. 
        Qui condivido esperienze, consigli pratici e aggiornamenti sulla crescita delle diverse varietà, 
        con un approccio semplice e diretto per chi ama il verde indoor.    
    </h1>
</section>

<nav class="safe-area filters">
    {#each data.years as year}
        <Filter bind:group={currentYear} value={year.number} />
    {/each}
</nav>

<section class="safe-area projects">
    {#each projects as project}
        <Project data={project.data} />
    {/each}
</section>

<style>
    .hero {
        padding-block: var(--size-11);
    
        h1 {
            font-size: var(--size-7);
            max-width: 35ch;
        }
    }

    .filters {
        display: flex;
        align-items: center;
        gap: var(--size-5);
    }

    .projects {
        padding-block: var(--size-7);

        display: grid;
        grid-template-columns: repeat(2, minmax(18rem, 1fr));
        gap: var(--size-5);
        width: 100%;
        max-width: calc(2 * 1fr + var(--size-2));
        margin-inline: auto;
        box-sizing: border-box;
    }

    @media (max-width: 745px) {
    .projects {
        grid-template-columns: 1fr;
        width: 100%;
    }
}
    </style>