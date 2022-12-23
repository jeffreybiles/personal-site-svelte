<script>
  import AccomplishmentBanner from "./AccomplishmentBanner.svelte";

  import squirrellockHolmes from "$lib/assets/squirrellock-holmes.png";
  import vueLogo from '$lib/assets/vue-logo.png';
  import cartMan from '$lib/assets/cart-man.png';

  const accomplishments = [
    {
      title: "SQuirrelLock Holmes",
      description: "Learn SQL with a fun game",
      foregroundImage: squirrellockHolmes,
      color: "rgba(212,100, 0,1)"
    },
    {
      title: "VueScreencasts",
      description: "In-depth tutorial screencasts about VueJS and Nuxt",
      color: "rgba(9,185,132,1)",
      foregroundImage: vueLogo
    },
    {
      title: "E(vil)-Commerce",
      description: "Introductory screencasts for Next 13, Nuxt 3, and SvelteKit 1.0.  We build an e-commerce app with a twist!",
      wideDescription: true,
      color: "rgba(255,215,0,1)",
      foregroundImage: cartMan
    },
  ]
</script>

<div class="banner-list">
  {#each accomplishments as accomplishment}
    <AccomplishmentBanner {...accomplishment} />
  {/each}
</div>

<style>
  .banner-list {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .banner-list > :global(*) {
    margin: 8px;
  }
</style>