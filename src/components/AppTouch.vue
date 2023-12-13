<script>
import { store } from "../store.js"

export default {
    name: "AppCompany",
    props: ["infoContact"],
    data() {
        return {
            store
        }
    },
    methods: {

    },
    mounted() {

    }
}
</script>

<template>
    <div class=" container d-flex">
        <div class="col-6 p-4">
            <h5 class="green">SEND IN TOUCH</h5>
            <h1>Excellence in <span class="green"> Services</span> </h1>
            <P class="grey">We will respond to your message as soon as possible.</P>
            <div class="row g-3 grey">
                <div class="col-6 ">
                    <input type="text" class="form-control bGrey " placeholder="Name" aria-label="First name">
                </div>
                <div class="col-6 ">
                    <input type="text" class="form-control bGrey" placeholder="Email" aria-label="Email">
                </div>
                <div class="col-6">
                    <input type="number" class="form-control bGrey" placeholder="Phone" aria-label="Number">
                </div>

                <div class="col-6 ">
                    <select class="form-select bGrey" aria-label="Default select example">
                        <option selected>-- Please choose an option --</option>
                        <option value="1">One</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                </div>

                <div class="col-12 ">
                    <input type="text" style="height: 100px" class="form-control bGrey" placeholder="Email"
                        aria-label="Last name">
                </div>
            </div>
        </div>

        <div class="col-6 p-4">
            <h5>Example Inc.</h5>
            <p class="grey">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
            <span class="bGreen">
                <p><i class="fas fa-phone"></i> {{ infoContact.telefono }}</p>
                <p><i class="fas fa-envelope"></i> {{ infoContact.mail }}</p>
                <p><i class="fas fa-map-marker"></i> {{ infoContact.indirizzo1 }}</p>
                <p><i class="fas fa-map-marker"></i> {{ infoContact.indirizzo2 }}</p>
            </span>
            <button class="btn btn-primary bGreen">VIEW MAP</button>
        </div>


    </div>


   
</template>

<style scoped lang="scss">
// importo variabili
@use '../styles/partials/variables' as *;

.green{
    color: #058283;
}

.fas{
    color: #058283;
}

.bGreen{
    color: #058283;

}

.bGrey{
    background-color: #ECECEC;
}

.grey{
   color: #828D94;
}
</style>