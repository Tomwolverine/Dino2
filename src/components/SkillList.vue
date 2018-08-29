<template>
    <div class="profile-card">
        <section class="skills-container hidden">
        <h4>Skills</h4>
        <ul class="skills-list">
            <Skill />
        </ul>
        </section>
    </div>
</template>

<script>
import Skill from './Skill'
export default {
    name: "SkillList",
    components: {
        Skill
    }
}
</script>

<style>
.profile-card {
border-radius: 6px;
box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.3);
padding: 10px;
  /* margin: 0 auto 10px auto; */
}
.skills-list {
list-style: none;
}
.hidden {
display: none;
}
</style>
