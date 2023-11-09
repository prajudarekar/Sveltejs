
<div class="card">
    <div class="header">
        <slot name="header">

        </slot>
    </div>

    <div class="content">
        <slot name="content">
            
        </slot>
    </div>
    <div class="footer">
        <slot name="footer">
            
        </slot>
    </div>
</div>

<style>
    .card{
        border:2px solid gray;
        box-shadow: 5px;
        margin: 5px;
    }
</style>