<template>
    <div>
        <h3>Edit the User</h3>
        <div style="height:700px"></div>
        <button class="btn btn-primary" @click="confirmed = true">Confirmed</button>
        <p id="data">Data Section</p>
    </div>
</template>

<script>
    export default{
        data(){
            return {
                confirmed: false
            }
        },
        beforeRouteLeave(to,from,next){
            if(this.confirmed){
                next();
            }else{
                if(confirm('確定嗎?')){
                    next();
                }else{
                    next(false);
                }
            }
        }
    }
</script>