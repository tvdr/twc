<template>
    <div id="app">
        <div class="navbar navbar-default">
            <div class="container-fluid">
                <div class="navbar-header">
                    <button type="button" class="navbar-toggle" data-toggle="collapse"
                            data-target=".navbar-responsive-collapse">
                        <span class="icon-bar"></span>
                        <span class="icon-bar"></span>
                        <span class="icon-bar"></span>
                    </button>
                    <a class="navbar-brand" href="/#/">TWC Weather</a>
                </div>
                <div class="navbar-collapse collapse navbar-responsive-collapse">
                    <ul class="nav navbar-nav">
                        <li><a href="/#/settings">Settings</a></li>
                    </ul>
                </div>
            </div>
        </div>
        <router-view :usersettings="usersettings"></router-view>
    </div>
</template>

<script>
    export default {
        name: 'app',
        data()
            {
                return {
                    usersettings: {
                        temp: {
                            min: 20,
                            max: 30
                        },

                        humidity: {
                            min: 20,
                            max: 30
                        },
                        city: '',
                        useCoordsIfAvailable: true
                    }
                }
            },
            mounted(){
                $.material.init()
            }
}

</script>
