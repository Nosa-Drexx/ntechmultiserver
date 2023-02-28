<script></script>

<template>
  <section :class="$style.reference">
    <span class="fa-solid fa-quote-left" :class="$style['quote-icon']"></span>
    <div :class="$style.quotes">
      <blockquote :class="$style.quote">
        My hire experience from your Nnamdi Azikiwe International Airport Abuja couldn't have been
        better. Great friendly service, no mucking around, efficient, prompt airport transfers,
        clean executive car got me around all the sight seeing places in the city. I will recommend
        Ntech multiverse ltd to everyone I know and use you again in the future.
        <author :class="$style.author">Evans Walter Abuja, Nigeria</author>
      </blockquote>
      <blockquote :class="$style.quote">
        During an official training, I ate their lunch buffet a couple of times and had dinner once.
        The food is exceptionally good, everything is rich in taste and really well cooked. Their
        food wasn't expensive as i expected. The tea breaks lunch and dinner were cooked and served
        to perfection. Try it.. you won't regret it.
        <author :class="$style.author">Benson Rose Abuja, Nigeria</author>
      </blockquote>
    </div>
  </section>
</template>

<style module>
.reference {
  display: flex;
  flex-flow: column nowrap;
  align-items: center;
  gap: 3px;
  padding: 1rem;
  background: var(--lightGray);
  width: 100%;
}
.quote-icon {
  font-size: 4rem;
  color: var(--blue);
  transform: rotate(180deg);
}
.quotes {
  display: flex;
  flex-flow: row nowrap;
  justify-content: center;
  width: 100%;
  gap: 1rem;
  max-width: 800px;
}
.quote {
  color: var(--white);
  background: var(--gray);
  border-radius: 20px;
  margin: auto;
  padding: 1rem;
  display: flex;
  flex-flow: column nowrap;
  justify-content: space-between;
  align-items: flex-end;
  gap: 1.2rem;
  min-height: 530px;
}
.author {
  font-style: italic;
  font-size: 0.9rem;
}

@media (min-width: 800px) {
  .quote-icon {
    align-self: flex-start;
    margin-left: calc((100vw - 800px) / 2);
  }
  .quote {
    min-height: 280px;
  }
  .quotes {
    padding-left: 3rem;
  }
}
</style>
