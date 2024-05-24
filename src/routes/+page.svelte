<script>
  let divider = 2
</script>

<svelte:head>
  <link
    href="https://fonts.googleapis.com/css2?family=DM+Mono:ital,wght@0,300;0,400;0,500;1,300;1,400;1,500&family=Roboto+Mono:ital,wght@0,100..700;1,100..700&family=Roboto:wght@400;500&display=swap"
    rel="stylesheet"
  />
</svelte:head>

<div class="container">
  <h1>Welcome to <br />Puzzle Crop Generator</h1>
  <form on:submit|preventDefault class="formContainer">
    <div class="center">
      <label for="divider">{divider}</label>
    </div>
    <input name="divider" type="range" min="0" max="10" bind:value={divider} />
    <button type="submit" class="cropButton dm-mono-light">Crop Image</button>
  </form>
</div>

<style>
  .container {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 20rem 0;
  }
  .formContainer {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  input {
    display: block;
    border-radius: 0.5rem;
    padding: 0.5rem;
    margin-bottom: 0.5rem;
    width: 300px;
    text-align: center;
  }
  .center {
    background: #ffffff;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    border-color: #49566b;
    border-style: solid;
    border-width: 0.2rem;
    display: flex;
    align-items: center;
    text-align: center;
  }
  label {
    display: block;
    padding: auto;
    text-align: center;
    margin: 0.5rem auto;
    font-size: 1.5em;
    font-weight: 500;
    color: #49566b;
    font-family: 'DM Mono', monospace;
  }
  input[type='range'] {
    margin: 1rem auto;
    color: #6a0808;
    background-color: #5568fa;
    border: 0.5px solid #49566b;
    border-radius: 0.5rem;
  }
  .cropButton {
    font-size: 1.5em;
    font-weight: 400;
    border-radius: 1rem;
    border: none;
    color: #49566b;
    padding: 0.5rem 2rem;
    width: 100%;
    max-width: 400px;
    margin: 1rem auto;
    background-color: #ffb300;
    font-family: 'DM Mono', monospace;
  }
  h1 {
    font-family: 'DM Mono', monospace;
    color: #49566b;
    font-size: 4em;
    font-weight: 500;
    text-align: center;
  }
</style>
