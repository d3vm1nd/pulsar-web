<script>
    export let title = "title";
    export let subtitle = "";
    export let host = "";

    let now = new Date();
    let year = now.getFullYear();
</script>

<div class="card">
    <div class="card-title">
        {title} <br />
        {subtitle}
    </div>
    <div class="card-body">
        <div class="form">
            <div class="card-body-row">
                <div class="card-body-column">Anio:</div>
                <div class="card-body-column">
                    <input type="text" bind:value={year} />
                </div>
            </div>
        </div>
        <div class="center">
            <a href={host + "/balance?year=" + year}> Get File </a>
        </div>
    </div>
</div>

<style>
</style>
