<template>
    <section>
        <h1>Login page</h1>
        <form>
            <div class="form-group">
                <input type="text" class="form-control">  
                <button class="btn btn-primary" type="submit">Login</button>  
            </div>
        </form>
        <p>
            <nuxt-link to="/">To home page</nuxt-link>
        </p>
    </section>
</template>
<script>
export default {
    layout: 'empty'
}
</script>
<style scoped>
.form-group{
    display: flex;
    justify-content: center;
}
.form-control{
    width: 300px;
}
</style>