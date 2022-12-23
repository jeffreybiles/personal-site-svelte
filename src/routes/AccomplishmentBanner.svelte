<script lang="ts">
  export let title: string = '';
  export let description: string;
  export let foregroundImage: any;
  export let wideDescription: boolean = false;
  export let color: string;
</script>

<div
  class="accomplishment-banner"
  style="background: linear-gradient(45deg, rgba(0,0,0,1) 14%, {color} 67%);">
  <img class="foreground" src={foregroundImage} />
  <div class="content">
    <div class="title"><div>{title}</div></div>
    <div class="description {wideDescription ? 'wide-description' : ''}"><div>{description}</div></div>
  </div>
</div>


<style>
  .accomplishment-banner {
    height: 130px;
    width: 400px;
    border: 3px solid black;
    transform: skewX(-20deg);
    overflow: hidden;
    cursor: pointer;
    /* box-shadow: 0 0 30px 10px rgba(0, 0, 0, 0.5); */
    
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
    max-width: 200px;
    text-align: center;
  }
  .wide-description {
    max-width: 300px;
  }
  img.foreground {
    top: 70px;
    left: -30px;
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
    margin-left: 20px;
  }
</style>