<script lang="ts">
  export let title: string = '';
  export let description: string;
  export let backgroundImage: any;
  export let foregroundImage: any;
</script>

<div class="accomplishment-banner">
  <img class="background" src={backgroundImage} />
  <img class="foreground" src={foregroundImage} />
  <div class="content">
    <div class="title"><div>{title}</div></div>
    <div class="description"><div>{description}</div></div>
  </div>
</div>


<style>
  .accomplishment-banner {
    height: 130px;
    width: 400px;
    border: 1px solid black;
    position: absolute;
    transform: skewX(-20deg);
    overflow: hidden;
    cursor: pointer;
  }
  .content {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: rgb(255, 255, 255);
    transition: margin-left 0.5s;
  }
  .title {
    font-size: 2em;
    font-weight: bold;
    margin: 4px;
    padding: 4px 8px;
    background-color: #0F1111;
  }
  .title div, .description div, img.foreground {
    transform: skewX(20deg);
  }
  .description {
    padding: 4px 8px;
    background-color: #0F1111;
  }
  img.background {
    width: 100%;
    height: 100%;
    object-position: center; /* Center the image within the element */
    object-fit: cover;
    background-color: #0F1111;
    position: absolute;
    z-index: -1;
  }
  img.foreground {
    top: 70px;
    width: 150px;
    position: absolute;
    z-index: 1;
    transition: top 0.5s, width 0.5s;
  }
  .accomplishment-banner:hover img.foreground {
    width: 150px;
    top: 40px;
  }
  .accomplishment-banner:hover .content {
    margin-left: 40px;
  }
</style>