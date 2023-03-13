<template>
  <div class="hello">
    <h1>Rekha Bhupatiraju</h1>
    <p>
      Full stack software engineer 
      <a href="https://constructionanalytics.trimble.com/">
      @Trimble MEP
      </a>
    </p>
    <div class="socmed">
      <a href="https://www.linkedin.com/in/rekha-bhupatiraju-992ba214b/">
        <img :src="pictureHover('linkedin')" 
        @mouseover="linkedInHover = true" 
        @mouseleave="linkedInHover  = false">
      </a>
      <a href="https://github.com/therekha">
        <img :src="pictureHover('github')"
        @mouseover="githubHover = true" 
        @mouseleave="githubHover = false">
      </a>
      <a href="https://twitter.com/therekharaju">
        <img :src="pictureHover('twitter')" 
        @mouseover="twitterHover = true" 
        @mouseleave="twitterHover = false">
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      linkedin: require('../assets/socmed/linkedin.png'),
      twitter: require('../assets/socmed/twitter.png'),
      github: require('../assets/socmed/github.png'),
      linkedinHI: require('../assets/socmed/linkedin_hover.png'),
      twitterHI: require('../assets/socmed/twitter_hover.png'),
      githubHI: require('../assets/socmed/github_hover.png'),
      linkedInHover: false,
      twitterHover: false,
      githubHover: false
    }
  },
  methods: {
    pictureHover: function(targetSite) {
      switch(targetSite){
        case('linkedin'):
          return this.linkedInHover ? this.linkedinHI : this.linkedin;
        case('twitter'):
          return this.twitterHover ? this.twitterHI : this.twitter; 
        case('github'):
          return this.githubHover ? this.githubHI : this.github;
        default:
      }
    }
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  p{
    color: var(--oldyellow)
  }
  img {
    width: 20%;
    height: auto;
}
</style>
