<section id="contact">
  <h2>Contact</h2>
  <div class="contacts">
    <a href="https://t.me/Vladislav_01a">
      <div class="contact">
        <img src="./contacts/telegram.png">
        <h4>Telegram</h4>
      </div>
    </a>
    <a href="#" on:click|preventDefault={() => open = true}>
      <div class="contact">
        <img src="./contacts/discord.png">
        <h4>Discord</h4>
      </div>
    </a>
  </div>
</section>

<script>
	let open = false;
	const discord = "vladislav1a";
	let copied = false;

	async function copy() {
		await navigator.clipboard.writeText(discord);
		copied = true;

		setTimeout(() => {
			copied = false;
		}, 1500);
	}
</script>

{#if open}
	<div class="dialog" on:click={() => open = false}>
		<div on:click|stopPropagation>
			<h3>Discord</h3>
			<div class="row">
				<span>{discord}</span>
				<button on:click={copy}>
					{copied ? "Copied ✔" : "Copy"}
				</button>
			</div>
			<button class="close" on:click={() => open = false}>✕</button>
		</div>
	</div>
{/if}


<style>
  .contacts {
    display: flex;
    justify-content: center;
  }
  .contact {
    margin: 3rem;
  }

  img {
    height: 3rem;
    filter: invert(1);
    padding: 0;
  }

  .dialog {
    position: fixed;
	  inset: 0;
	  background: rgba(0,0,0,.5);
	  display: flex;
	  align-items: center;
	  justify-content: center;
  }
  .dialog div {
    background: var(--bg);
	  padding: 1rem;
	  border-radius: 1.5rem;
	  position: relative;
  }
  .row {
    display: flex;
	  gap: 1rem;
	  align-items: center;
  }
  .row span {
    font-family: monospace;
    background: var(--fg);
    padding: 0.6em 1em;
    border-radius: 8px;
  }
  .close {
    position: absolute;
	  top: 0.5rem;
    right: 0.5rem;
    color: var(--accent);
	  background: none;
	  font-size: 1.2rem;
  }
</style>
