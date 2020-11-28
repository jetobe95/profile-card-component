<script>
  import Avatar from "./components/Avatar.svelte";
  import StaticItem from "./components/StatItem.svelte";

  let statics = [
    { staticName: "Followers", staticNum: "80k" },
    { staticName: "Likes", staticNum: "803k" },
    { staticName: "Photos", staticNum: "1.4k" },
  ];
</script>

<style>
  .container {
    background-image: url("/images/bg-pattern-card.svg");
    background-position: top center;
    background-size: contain;
    background-repeat: no-repeat;
    background-color: white;
    border-radius: 12px;
    width: 400px;
    height: 350px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .row {
    display: flex;
    width: 100%;
    justify-content: space-around;
    margin-top: 1rem;
  }
  @media (max-width: 375px) {
    .container {
      width: 300px;
    }
  }
  h1 {
    margin-bottom: 0;
    font-size: 1rem;
    color: hsl(229, 23%, 23%);
  }
  span,
  p {
    margin-bottom: 0;
    color: hsl(227, 10%, 46%);
    font-size: 1rem;
    font-weight: 400;
  }
  p {
    font-size: 0.85rem;
    margin-bottom: 1rem;
    margin-top: 0.6rem;
  }
  hr {
    width: 100%;
    background-color: hsl(0, 0%, 59%);
    height: 0.7px;
    border-width: 0;
    margin: 10px 0 10px 0;
  }
  .info-container{
      text-align: center;
  }
</style>

<div class="container">
  <Avatar />
  <div class="info-container">
    <h1>Victor Crest <span>26</span></h1>
    <p>London</p>
  </div>
  <hr />
  <div class="row">
    {#each statics as stat}
      <StaticItem staticName={stat.staticName} staticNum={stat.staticNum} />
    {/each}
  </div>
</div>
