<script>
    export let staticNum;
    export let staticName;
</script>
<style>
    .container{
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    strong{
        margin-bottom: 0.12rem;
    }
    span{
        font-size: 0.6rem;
        letter-spacing: 1.4px;
    }
</style>
<div class='container'>
    <strong>{staticNum}</strong>
    <span>{staticName}</span>
</div>