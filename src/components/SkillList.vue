<template>
    <div>
        <h4>Skills</h4>
        <ul class="skills-list">
            <Skill v-for="skill in skills" :key='skill.id' :skill='skill'/>
        </ul>
    </div>
</template>

<script>
import Skill from './Skill'

export default {
    name: "SkillList",
    components: {
        Skill
    },
    props: ['skills']
}
</script>

<style>

.skills-list {
list-style: none;
}

</style>
