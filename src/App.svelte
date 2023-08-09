<script>
    let input = "";
</script>

<div class="container">
    <h1 class="nameh1">QR Code Generator</h1>

    <div class="input-group">
        <label class="label">Enter your text here</label>
        <input
            autocomplete="off"
            name="qrtext"
            id="qrtext"
            class="input"
            type="text"
            bind:value={input}
        />
        <div />
    </div>

    {#if input}
        <img
            src="http://qrcoder.ru/code/?{input}&4&0"
            width="156"
            height="156"
            class="qrcode"
            alt="QR"
        />
    {:else}
        <img
            src="http://qrcoder.ru/code/?Welcome to the QR code generator&4&0"
            width="156"
            height="156"
            class="qrcode"
            alt="QR"
        />
    {/if}
</div>

<style>
</style>
