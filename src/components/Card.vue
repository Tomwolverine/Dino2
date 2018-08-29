<template>
    <li>
        <div class="profile-card">
        <header>
            <img :src="dino.image" />
            <h2>{{dino.name}}</h2>
        </header>
        <!-- <section class="skills-container hidden"> -->
            <!-- <SkillList /> -->
        <!-- </section>     -->
        </div>
    </li>    
</template>

<script>
// import SkillList from './SkillList'

export default {
    name: 'Card',
    components:{
        // SkillList
    },
    props: ['dino']
    
}
</script>

<style>
.profile-card {
    border-radius: 6px;
    box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.3);
    padding: 10px;
  /* margin: 0 auto 10px auto; */
}

.profile-header {
    display: flex;
    flex-flow: row nowrap;
}

.profile-header img {
    width: 100px;
    height: 100px;
    border: 1px solid darkgrey;
    margin: 0 10px 0 10px;
}

.skills-list {
    list-style: none;
}
</style>
