<template>
    <div class="profile-card">
        <header class="profile-header">
        <img src="{{image}}" />
        <h2>{{name}}</h2>
        </header>
        <section class="skills-container hidden">
        <h4>Skills</h4>
        <ul class="skills-list">
            {{#each skills}}
            <li>{{this}}</li>
            {{/each}}
        </ul>
        </section>
    </div>
</template>

<script>
export default {
    
}
</script>

<style>

</style>
