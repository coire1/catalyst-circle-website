<template>
  <div class="videos-wrapper">
    <div class="pagewidth">
      <h2>Meeting Recordings</h2>
      <div class="videos-list">
        <div class="single-video" v-for="video in $frontmatter.videos">
          <div class="video is-16by9">
            <iframe width="560" height="315" :src="getEmbedLink(video.link)" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
          <h4>{{video.title}}</h4>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    methods: {
      getEmbedLink(link) {
        link = link.replace('https://www.youtube.com/watch?v=', '')
        return `https://www.youtube.com/embed/${link}`
      }
    }
  }
</script>

<style lang="scss">
.videos-wrapper {
  width: 100%;
  h2 {
    margin-bottom: 50px
  }
}
.videos-list {
  display: flex;
  flex-wrap: wrap;
  .single-video {
    width: 33.333%;
    padding: 0 30px;
    .video {
      position: relative;
      display: block;
      width: 100%;
      padding: 0;
      overflow: hidden;
      margin-bottom: 20px;
      &.is-21by9 {
        padding-top: 42.85714%
      }
      &.is-16by9 {
        padding-top: 56.25%
      }
      &.is-4by3 {
        padding-top: 75%
      }
      &.is-1by1 {
        padding-top: 100%
      }
      iframe, embed, object, video {
        position: absolute;
        top: 0;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 100%;
        border: 0
      }
    }
  }
}
</style>
