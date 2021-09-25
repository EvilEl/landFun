<template>
  <div id="app">
    <Header />
    <Hero />
    <Services />
    <Specialist />
    <Features />
    <Recall />
    <Started />
    <Cards />
  </div>
</template>

<script>
import "normalize.css";
import Header from "@/components/Header";
import Hero from "@/components/Hero";
import Services from "@/components/Services";
import Specialist from "@/components/Specialist";
import Features from "@/components/Features";
import Recall from "@/components/Recall";
import Started from "@/components/Started";
import Cards from "@/components/Cards";

export default {
  name: "App",
  components: {
    Header,
    Hero,
    Services,
    Specialist,
    Features,
    Recall,
    Started,
    Cards,
  },
};
</script>

<style lang="scss">
*,
*::before,
*::after {
  box-sizing: border-box;
}

/* Remove default margin */
body,
h1,
h2,
h3,
h4,
p,
figure,
blockquote,
dl,
dd {
  margin: 0;
}

/* Remove list styles on ul, ol elements with a list role, which suggests default styling will be removed */
ul[role="list"],
ol[role="list"] {
  list-style: none;
}

/* Set core root defaults */
html:focus-within {
  scroll-behavior: smooth;
}

/* Set core body defaults */
body {
  min-height: 100vh;
  text-rendering: optimizeSpeed;
  line-height: 1.5;
}

/* A elements that don't have a class get default styles */
a:not([class]) {
  text-decoration-skip-ink: auto;
}

/* Make images easier to work with */
img,
picture {
  max-width: 100%;
  display: block;
}

/* Inherit fonts for inputs and buttons */
input,
button,
textarea,
select {
  font: inherit;
}

/* Remove all animations and transitions for people that prefer not to see them */
@media (prefers-reduced-motion: reduce) {
  html:focus-within {
    scroll-behavior: auto;
  }
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}

._container {
  max-width: 1170px;
  padding: 0 15px;
  margin: 0 auto;
}
.menu {
  flex: 1 1 auto;
}
.menu__list {
  display: flex;
}
.button {
}

._img {
  position: relative;
}
.title {
  font-style: normal;
  font-weight: 700;
  font-size: 38px;
  line-height: calc(45 / 38 * 100%);
  color: #252626;
}
.subtitle {
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 160%;
  text-align: center;
  color: #707273;
}
.main-content {
  & > *:not(:last-child) {
    margin-bottom: 25px;
  }
}
.title__column {
  font-style: normal;
  font-weight: 600;
  font-size: 21px;
  line-height: 150%;
  text-align: center;
  color: #252626;
}
.subtitle__column {
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 160%;
  text-align: center;
  color: #707273;
}
._img img {
  width: 100%;
  height: 100%;
  // position: absolute;
  object-fit: cover;
}
</style>
