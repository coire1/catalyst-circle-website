<template>
  <div class="page-wrapper">
    <cheader />
    <div class="home">
      <section id="intro" class="intro">
        <img class="bkg" :src="$withBase('images/intro.jpg')">
        <div class="centered">
          <div class="pagewidth">
            <Content slot-key="intro" />
          </div>
        </div>
      </section>
      <section id="description" class="big-text">
        <div class="pagewidth">
          <Content slot-key="description" />
        </div>
      </section>
      <section id="team" class="dark">
        <team />
      </section>
      <section id="videos" class="light">
        <videos />
      </section>
      <section id="gitbook" class="big-text with-button">
        <div class="pagewidth">
          <Content class="half" slot-key="gitbook" />
          <gitbook />
        </div>
      </section>
      <section id="contact" class="dark big-text align-center">
        <div class="pagewidth">
          <Content slot-key="contact" />
        </div>
      </section>
    </div>
  </div>
</template>
