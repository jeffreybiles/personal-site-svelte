<script>
  import AccomplishmentBanner from "./AccomplishmentBanner.svelte";

  import meshGradientExample from "$lib/assets/mesh-gradient-example.png";
  import squirrellockHolmes from "$lib/assets/squirrellock-holmes.png";
</script>

<AccomplishmentBanner
  title="SQuirrelLock Holmes"
  description="Learn SQL with a fun game"
  backgroundImage={meshGradientExample}
  foregroundImage={squirrellockHolmes}
/>