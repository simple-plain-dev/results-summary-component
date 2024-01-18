<script lang="ts">
  import memory from "$lib/assets/images/icon-memory.svg"
  import reaction from "$lib/assets/images/icon-reaction.svg"
  import verbal from "$lib/assets/images/icon-verbal.svg"
  import visual from "$lib/assets/images/icon-visual.svg"
</script>

<article>
  <section class="summary">
    <p class="text-grey bold">Your Result</p>
    <div class="score">
      <h2 class="text-white" style="font-size: xx-large;">76</h2>
      <p class="text-grey">of 100</p>
    </div>
    <h3 class="text-white">Great</h3>
    <p class="text-grey " >You scored higher than 65% of the people who have taken these tests.</p>
  </section>
  <section class="details">
    <h4>Summary</h4>
    <div class="list red bold">
      <img src={reaction} alt="reaction icon" >
      <p class=" text-red">Reaction</p>
      <p>80<span class="text-grey">/100</span></p>
    </div>
    <div class="list yellow bold">
      <img src={memory} alt="memory icon" >
      <p class=" text-yellow">Memory</p>
      <p>92<span class="text-grey">/100</span></p>
    </div>
    <div class="list green bold">
      <img src={verbal} alt="verbal icon" >
      <p class=" text-green">Verbal</p>
      <p>61<span class="text-grey">/100</span></p>
    </div>
    <div class="list blue bold">
      <img src={visual} alt="visual icon" >
      <p class=" text-blue">Visual</p>
      <p>72<span class="text-grey">/100</span></p>
    </div>
    <button>Continue</button>
  </section>
</article>

<style>
  article {
    margin-inline: 2rem;
    /* border: 1px solid red; */
    border-radius: 2rem;
    box-shadow: 2px 4px 6px 8px var(--color-neutral-2);
    display: grid;
    grid-template-rows: 1fr 1fr;
  }

  @media(width >= 640px){
    article {
      grid-template-columns: 1fr 1fr;
      grid-template-rows: 1fr;
    }
  }

  .summary {
    background-image: radial-gradient(80% 80% at center , var(--color-gradient-1) 20% , var(--color-gradient-2)) ;
    border-radius: 2rem;
    display: grid;
    place-content: center;
    text-align: center;
    gap: 1rem;
    padding: 1rem;
    max-width: 20rem;
  }

  .score {
    background-image: linear-gradient(var(--color-gradient-3), var(--color-gradient-2));
    margin-inline: auto;
    padding: 2rem;
    border-radius: 50%;
    aspect-ratio: 1;
  }

  .details{
    background-color: var(--color-neutral-1);
    border-radius: 0 0 2rem 2rem;
    overflow: hidden;
    display: grid;
    padding-block: 1rem;
    padding-inline: 1.2rem;
    /* border: 1px solid red; */
    gap: 0.8rem;
  }

  .list {
    display: grid;
    grid-template-columns: auto 1fr auto;
    border-radius: 0.5rem;
    padding: 0.8rem;
    gap: 1rem;
    align-items: center;
  }

  /* color */
  .red {
    background-color: var(--color-primary-1);
  }
  
  .text-red{
    color: var(--fc-primary-1);
  }

  .yellow {
    background-color: var(--color-primary-2);
  }
  
  .text-yellow{
    color: var(--fc-primary-2);
  }

  .green {
    background-color: var(--color-primary-3);
  }
  
  .text-green{
    color: var(--fc-primary-3);
  }

  .blue{
    background-color: var(--color-primary-4);
  }
  
  .text-blue{
    color: var(--fc-primary-4);
  }

  .text-grey{
    color: var(--color-neutral-3);
  }

  .text-white{
    color: var(--color-neutral-1)
  }


  .bold {
    font-weight: var(--fw-bold);
    letter-spacing: 1.5px;
  }

  button {
    padding: 0.8rem;
    border-radius: 2rem;
    /* background-color: transparent; */
    border: none;
    background-color: var(--color-neutral-4);
    color: var(--color-neutral-1);
    margin-block: 0.5rem;
  }
</style>