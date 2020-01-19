<template>
    <div class="col-md-12 grid-margin">
        <div class="card bg-white">
            <div class="card-body d-flex align-items-center justify-content-between">
                <h4 class="mt-1 mb-1">Hi {{ userName }}, Welcome back!</h4>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Welcomeback',
    data() {
        return {
            userName: {}
        }
    },
    created() {
        fetch('https://inlupp-fa.azurewebsites.net/api/users?firstname=Tobias&lastname=Englund')
        .then(res => res.text())
        .then(data => {
            this.userName = data;
        })
    }
}
</script>

<style>

</style>