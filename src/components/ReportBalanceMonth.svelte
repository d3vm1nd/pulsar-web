<script>
    export let title = "title";
    export let subtitle = "";
    export let host = "";

    let now = new Date();
    let period =
        now.getFullYear() + "" + padWithLeadingZeros(now.getMonth() + 1, 2);
    let propertyName = "";
    let propertyNit = "";

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
            <div class="card-body-row">
                <div class="card-body-column">Nombre Urb:</div>
                <div class="card-body-column">
                    <input type="text" bind:value={propertyName} />
                </div>
            </div>
            <div class="card-body-row">
                <div class="card-body-column">Nit:</div>
                <div class="card-body-column">
                    <input type="text" bind:value={propertyNit} />
                </div>
            </div>
        </div>
        <div class="center">
            <a
                href={host +
                    "/report-balance?period=" +
                    period +
                    "&propertyName=" +
                    propertyName +
                    "&propertyNit=" +
                    propertyNit}
            >
                Get File
            </a>
        </div>
    </div>
</div>

<style>
</style>
