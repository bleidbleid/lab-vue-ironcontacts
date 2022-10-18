<template>
    <div class="section is-flex is-flex-direction-column ">
        <h1 class="title">IronContacts</h1>
        <button @click="getRandom()" class="button is-black">Afegir contacte aleatori</button>
        <table class="table is-striped is-narrow is-hoverable">
            <thead>
                <tr>
                    <td>Foto</td>
                    <td>Nom</td>
                    <td>Popularitat</td>
                    <td>Té un Oscar</td>
                    <td>Té un Emmy</td>

                </tr>
            </thead>
            <tbody v-for="contact in myContacts">
                <tr>
                    <td> <img :src="`${contact.pictureUrl}`" alt="Placeholder image" class="profile" /></td>
                    <td>{{contact.name}}</td>
                    <td>{{contact.popularity}}</td>
                    <td v-if="contact.wonOscar">🏆</td>
                    <td v-else></td>
                    <td v-if="contact.wonEmmy">🌟</td>
                    <td v-else></td>

                </tr>

            </tbody>
        </table>
    </div>
</template>
<script setup>
import { ref } from 'vue';
import contacts from "./data/contacts.json";
const myContacts = ref()
myContacts.value = contacts.slice(0, 5);

const getRandom = () => {
    const newContact = Math.floor(Math.random() * contacts.length);
    const isIt = (myContacts.value.indexOf(contacts[newContact].id));
    if (isIt == -1) {
        myContacts.value.push(contacts[newContact]);
        return myContacts.value;
    }
}

</script>
<style scoped>
.button {
    margin: 32px 0px;
}

img {
    height: 75px;
}
</style>