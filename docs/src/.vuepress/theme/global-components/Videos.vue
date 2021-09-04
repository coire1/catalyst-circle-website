<template>
  <div class="videos-wrapper">
    <div class="pagewidth">
      <h2>Meeting Recordings</h2>
      <div class="videos-list">
        <div class="single-video" v-for="video in $frontmatter.videos">
          <video-embed css="video is-16by9" :src="video.link"></video-embed>
          <h4>{{video.title}}</h4>
        </div>
      </div>
    </div>
  </div>
</template>


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
