<template>
  <div class="teams-wrapper">
    <div class="pagewidth">
      <h2>Catalyst Circle Members</h2>
      <div class="members-list">
        <div class="member" v-for="member,idx in $frontmatter.team" :key="`member${idx}`">
          <div class="image-wrapper">
            <img :src="$withBase(`images/${member.image}`)" :alt="member.name">
          </div>
          <h3>{{ member.name }}</h3>
          <h4>{{ member.role }}</h4>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.members-list {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  .member {
    width: 25%;
    padding: 0 30px;
    text-align: center;
    margin-bottom: 60px;
    .image-wrapper {
      height: 0;
      position: relative;
      padding-top: 100%;
      border-radius: 100%;
      overflow: hidden;
      margin-bottom: 20px;
      img {
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
        object-fit: cover;
      }

    }
  }
}
</style>
