<template>
    <section class="container">
        <div class="row">
            <div class="col-xs-12 text-center">
                <h1>Your personal definition of good weather</h1>
            </div>
        </div>
        <div class="row">
            <form id="usersettings">
                <div class="col-xs-12 col-sm-6 form-group">
                    <label for="tempmin">Temperature MIN: {{usersettings.temp.min}} °C </label>
                    <input class="form-control" id="tempmin" type="range" v-model.number="usersettings.temp.min">
                </div>
                <div class="col-xs-12 col-sm-6 form-group">
                    <label for="tempmax">Temperature MAX: {{usersettings.temp.max}} °C </label>
                    <input class="form-control" id="tempmax" type="range" v-model.number="usersettings.temp.max">
                </div>

                <div class="col-xs-12 col-sm-6 form-group">
                    <label for="humiditymin">Humidity MIN: {{usersettings.humidity.min}} %</label>
                    <input class="form-control" id="humiditymin" type="range" v-model.number="usersettings.humidity.min">
                </div>
                <div class="col-xs-12 col-sm-6 form-group">
                    <label for="humiditymax">Humidity MAX: {{usersettings.humidity.max}} %</label>
                    <input class="form-control" id="humiditymax" type="range" v-model.number="usersettings.humidity.max">
                </div>

                <div class="col-xs-12 col-sm-6 form-group label-floating">
                    <label class="control-label" for="city">City</label>
                    <input class="form-control" id="city" type="text" v-model="usersettings.city" :disabled="usersettings.useCoordsIfAvailable ? true : false">
                </div>

                <div class="col-xs-12 col-sm-6 form-group">
                    <div class="checkbox">
                        <label>
                            <input type="checkbox" v-model="usersettings.useCoordsIfAvailable"> Use geolocation if available
                        </label>
                    </div>
                </div>

            </form>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'settings',
        props:['usersettings'],

        mounted(){
                $.material.init()

            }


    }


</script>
