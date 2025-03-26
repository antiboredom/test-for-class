<script>
  let count = $state(1);
  let numbers = $state([]);
  let doubled = $derived(count * 2);

  function increment() {
    numbers.push(count);
    count = count + 1;
  }
</script>

<main>
  The count is {count}. Times 2 that is {doubled}!!!!!!!!!!

  <button onclick={increment}>Click me!</button>

  {#if count > 5}
    <div>You clicked more than 5 times!</div>
  {/if}

  {#each numbers as n}
    <div>{n}</div>
  {/each}
</main>

<style>
  main {
    text-align: center;
    font: 18px sans-serif;
  }
</style>
