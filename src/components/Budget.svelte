<script>
    export let title = "title";
    export let subtitle = "";
    export let host = "";
</script>

<div class="card">
    <div class="card-title">
        {title} <br />
        {subtitle}
    </div>
    <div class="card-body">
        <div class="form"></div>
        <div class="center">
        <a href={host + "/presupuesto"}>
            Get File
        </a>
        </div>
    </div>
</div>

<style>
</style>
