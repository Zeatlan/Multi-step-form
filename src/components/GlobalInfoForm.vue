<template>
    <div class="form-container">
        <div class="form-container__header">
            <h1>Personal info</h1>
            <p>Please provide your name, email address, and phone number.</p>
        </div>

        <form class="form-container__form">

            <div class="form-inputs">
                <div class="input-container">
                    <label for="name">Name</label>
                    <input type="text" name="name" placeholder="e.g. Stephen King" />
                </div>
                
                <div class="input-container">
                    <label for="mail">Email Address</label>
                    <input type="mail" name="mail" placeholder="e.g. stephenking@lorem.com" />
                </div>
    
                <div class="input-container">
                    <label for="phone">Phone Number</label>
                    <input type="text" name="name" placeholder="e.g. +1 234 567 890" />
                </div>
            </div>

            <button type="submit">Next Step</button>
        </form>
    </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss"></style>