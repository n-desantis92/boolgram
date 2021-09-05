<template>
    <div id="main-right-bottom" class="main-right-bottom">
        <ul>
            <li>Informazioni</li>
            
            <li>Assistenza</li>
            
            <li>Stampa</li>
            
            <li>Api</li>
            
            <li>Lavora con noi</li>
            
            <li>Privacy</li>
            
            <li>Condizioni</li>
            
            <li>Luoghi</li>
            
            <li>Account più popolari</li>
            
            <li>hashtag</li>
            
            <li>lingua</li>
        </ul>
        <div class="copi">
            &copy; 2021 INSTAGRAM DI FACEBOOK
        </div>
    </div>
</template>

<script>
export default {
    name: 'main-right-bottom',
    data() {
        return {
            
        }
    },
    props: {
        
    }
}
</script>

<style lang="scss">
    .main-right-bottom {
        color: rgb(193, 193, 193);
        font-size: 12px;
        width: 100%;
        ul {
            width: 100%;
            display: flex;
            flex-wrap: wrap;
            list-style-type: none;
            li {
                cursor: pointer;
                margin: 5px;
            }
        }
        .copi {
            margin-top: 20px;
        }
    }
</style>