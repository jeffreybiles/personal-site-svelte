<script>
  import AccomplishmentBanner from "./AccomplishmentBanner.svelte";

  import squirrellockHolmes from "$lib/assets/squirrellock-holmes.png";
  import vueLogo from '$lib/assets/vue-logo.png';
  import cartMan from '$lib/assets/cart-man.png';
</script>

<div class="banner-list">
  <AccomplishmentBanner
    title="SQuirrelLock Holmes"
    description="Learn SQL with a fun game"
    foregroundImage={squirrellockHolmes}
    gradient="linear-gradient(45deg, rgba(0,0,0,1) 14%, rgba(212,100, 0,1) 67%)"
    
  />
  <AccomplishmentBanner
    title="VueScreencasts"
    description="In-depth tutorial screencasts about VueJS and Nuxt"
    gradient="linear-gradient(45deg, rgba(0,0,0,1) 14%, rgba(9,185,132,1) 67%)"
    foregroundImage={vueLogo}
  />
  <AccomplishmentBanner
    title="E(vil)-Commerce"
    description="Introductory screencasts for Next 13, Nuxt 3, and SvelteKit 1.0.  We build an e-commerce app with a twist!"
    wideDescription={true}
    gradient="linear-gradient(45deg, rgba(0,0,0,1) 14%, rgba(230,230,3,1) 67%)"
    foregroundImage={cartMan}
  />
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