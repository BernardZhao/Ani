<template>
  <div class="hero">
    <svg class="heroText" viewBox="0 0 2000 1000">
      <defs>
        <linearGradient id="gradient" x1="0%" y1="0%" x2="0%" y2="100%">  
          <stop offset="0" stop-color="white" stop-opacity="0.5" />  
          <stop offset="1" stop-color="white" stop-opacity="1" />  
        </linearGradient>

        <mask id="mask">
          <rect width="100%" height="100%" fill="url(#gradient)" />
          <text x="50%" y="70%" class="title">Ani</text>
          <text x="50%" y="80%" class="subtitle">Crowdsourced animation.</text>
        </mask>
      </defs>
      <rect 
        class="base"
        x="0"
        y="0"
        width="100%"
        height="100%"
        fill="rgba(255, 255, 255, 1)"
        mask="url(#mask)"
      />
    </svg>
    
    <video id="video" autoplay="autoplay" muted="muted" preload="auto" loop="loop">
      <source src="http://mazwai.com/system/posts/videos/000/000/123/original/victor_ciurus--5d_mark_iii_magic_lantern_14_bits_raw_video.mp4?1412890624" type="video/mp4">
      <source src="http://mazwai.com/system/posts/videos/000/000/123/webm/victor_ciurus--5d_mark_iii_magic_lantern_14_bits_raw_video.webm?1412890624" type="video/webm">
    </video>
  </div>
</template>

<style scoped>
.hero {
  width: 100%;
  position: relative;
  overflow: hidden;
}
.heroText {
  margin-bottom: -1%;
}

#video {
  position: absolute;
  top: 0%;
  left: 0%;
  min-width: 100%;
  min-height: 100%;
  width: auto;
  height: auto;
  z-index: -1;
}

.title {
  font-size: 600px;
  font-style: bold;
  fill: #000;
}

.subtitle {
  font-size: 50px;
  font-style: bold;
  fill: #000;
}

.title, .subtitle {
  text-anchor: middle
}
 
.base {
  mask: url("#mask");
}
</style>