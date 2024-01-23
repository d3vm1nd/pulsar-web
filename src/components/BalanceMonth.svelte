<script>
    export let title = "title";
    export let subtitle = "";
    export let host = "";

    let now = new Date();
    let period =
        now.getFullYear() + "" + padWithLeadingZeros(now.getMonth() + 1, 2);

    function padWithLeadingZeros(num, totalLength) {
        return String(num).padStart(totalLength, "0");
    }
</script>

<div class="card">
    <div class="card-title">
        {title} <br />
        {subtitle}
    </div>
    <div class="card-body">
        <div class="form">
            <div class="card-body-row">
                <div class="card-body-column">Periodo:</div>
                <div class="card-body-column">
                    <input type="text" bind:value={period} />
                </div>
            </div>
        </div>
        <div class="center">
            <a href={host + "/balance?period=" + period}> Get File </a>
        </div>
    </div>
</div>

<style>
</style>
