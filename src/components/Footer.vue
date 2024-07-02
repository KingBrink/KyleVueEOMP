<template>
    <footer class="container">
        <div class="row">
            <p class="lead">Kyle's portfolio &copy; <span class="shadow">{{ currentYear }}</span></p>
        </div>
    </footer>
</template>
<script>
    export default {
        name: 'FooterComp',
        data(){
            return{
                currentYear: new Date().getUTCFullYear()
            }
        }
    }
</script>

