---
layout: page
permalink: /cooking/
title: Cooking
description: If you think my research is cooked, at least enjoy some things I actually cooked.
nav: true
nav_order: 2
---

<style>
.post-header .post-description {
  font-size: 1rem;
  line-height: 1.6;
}

.cooking-page {
  width: 100%;
}

.cooking-gallery {
  --gallery-gap: 0.55rem;
  --short-row-height: 139.06px;
  --feature-row-height: 108.1px;
  display: grid;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  grid-template-rows:
    repeat(2, var(--feature-row-height))
    var(--short-row-height)
    repeat(2, var(--feature-row-height))
    var(--short-row-height)
    repeat(2, var(--feature-row-height))
    var(--short-row-height)
    repeat(2, var(--feature-row-height))
    var(--short-row-height)
    repeat(4, var(--feature-row-height));
  grid-template-areas:
    "a  a  d  d"
    "a  a  d  d"
    "b  b  m  p"
    "g  g  i  i"
    "g  g  i  i"
    "h  h  n  e"
    "o  o  c  f"
    "o  o  c  f"
    "l  l  v  ab"
    "u  u  j  k"
    "u  u  j  k"
    "q  q  z  z"
    "y  y  r  s"
    "y  y  r  s"
    "t  w  x  aa"
    "t  w  x  aa";
  gap: var(--gallery-gap);
}

.cooking-photo {
  min-width: 0;
  min-height: 0;
  margin: 0;
  padding: 0;
  overflow: hidden;
  border: 0;
  border-radius: 4px;
  background: transparent;
  box-shadow: 0 5px 16px rgba(0, 0, 0, 0.1);
  cursor: zoom-in;
}

.cooking-photo img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: var(--crop-position, center);
  transition: transform 0.35s ease;
}

.cooking-photo:hover img,
.cooking-photo:focus-visible img {
  transform: scale(1.025);
}

.cooking-photo:focus-visible {
  outline: 2px solid var(--global-theme-color);
  outline-offset: 3px;
}

.cooking-lightbox {
  width: 100vw;
  max-width: none;
  height: 100vh;
  max-height: none;
  margin: 0;
  padding: 0;
  border: 0;
  background: rgba(11, 13, 16, 0.96);
  color: #fff;
}

.cooking-lightbox::backdrop {
  background: rgba(11, 13, 16, 0.96);
}

.cooking-lightbox-frame {
  display: grid;
  grid-template-columns: 3.25rem minmax(0, 1fr) 3.25rem;
  align-items: center;
  width: 100%;
  height: 100%;
  padding: 3.5rem 1rem 1rem;
}

.cooking-lightbox-image {
  justify-self: center;
  max-width: 100%;
  max-height: calc(100vh - 4.5rem);
  object-fit: contain;
}

.cooking-lightbox button {
  display: grid;
  place-items: center;
  width: 2.75rem;
  height: 2.75rem;
  padding: 0;
  border: 0;
  background: transparent;
  color: #fff;
  font-size: 1.55rem;
}

.cooking-lightbox button:hover,
.cooking-lightbox button:focus-visible {
  color: #b8cee6;
}

.cooking-lightbox-close {
  position: absolute;
  top: 0.65rem;
  right: 0.8rem;
}

.cooking-lightbox-next {
  justify-self: end;
}

@media (max-width: 768px) {
  .cooking-gallery {
    display: block;
    columns: 2;
    column-gap: 0;
    aspect-ratio: auto;
  }

  .cooking-photo {
    display: block;
    width: 100%;
    margin-bottom: 0.5rem;
    break-inside: avoid;
    aspect-ratio: var(--mobile-ratio, 1);
  }

  .cooking-photo--mobile-wide {
    column-span: all;
    aspect-ratio: var(--mobile-wide-ratio, 4 / 3);
  }

  .cooking-lightbox-frame {
    grid-template-columns: 2.75rem minmax(0, 1fr) 2.75rem;
    padding: 3.25rem 0.35rem 0.75rem;
  }

  .cooking-lightbox button {
    width: 2.5rem;
    height: 2.5rem;
  }
}

@media (prefers-reduced-motion: reduce) {
  .cooking-photo img {
    transition: none;
  }
}
</style>

<div class="cooking-page">
  <div class="cooking-gallery">
    <button class="cooking-photo cooking-photo--feature cooking-photo--mobile-wide" type="button" style="grid-area: a; --crop-position: center 48%; --mobile-wide-ratio: 4 / 3;" data-full="/assets/img/cooking/dinner-spread.jpg" aria-label="View a home-cooked dinner spread">
      <img src="/assets/img/cooking/dinner-spread.jpg" alt="An overhead view of a home-cooked dinner spread" loading="eager">
    </button>
    <button class="cooking-photo cooking-photo--wide" type="button" style="grid-area: b; --crop-position: center 58%; --mobile-ratio: 4 / 3;" data-full="/assets/img/cooking/congee-and-tomato-eggs.jpg" aria-label="View congee and tomato eggs">
      <img src="/assets/img/cooking/congee-and-tomato-eggs.jpg" alt="Congee and tomato eggs on a dining table" loading="lazy">
    </button>
    <button class="cooking-photo cooking-photo--tall" type="button" style="grid-area: c; --crop-position: center 54%; --mobile-ratio: 3 / 4;" data-full="/assets/img/cooking/steak-and-bread.jpg" aria-label="View steak dinner and bread">
      <img src="/assets/img/cooking/steak-and-bread.jpg" alt="Steak dinner with vegetables and homemade bread" loading="lazy">
    </button>

    <button class="cooking-photo cooking-photo--feature cooking-photo--mobile-wide" type="button" style="grid-area: d; --crop-position: center 54%; --mobile-wide-ratio: 4 / 3;" data-full="/assets/img/cooking/hot-pot-table.jpg" aria-label="View a home hot pot spread">
      <img src="/assets/img/cooking/hot-pot-table.jpg" alt="A home hot pot spread with beef, tofu, vegetables, and rice" loading="lazy">
    </button>
    <button class="cooking-photo" type="button" style="grid-area: e; --crop-position: center 54%; --mobile-ratio: 4 / 3;" data-full="/assets/img/cooking/tofu-and-greens.jpg" aria-label="View tofu and greens">
      <img src="/assets/img/cooking/tofu-and-greens.jpg" alt="Braised tofu with greens" loading="lazy">
    </button>
    <button class="cooking-photo cooking-photo--tall" type="button" style="grid-area: f; --crop-position: center 60%; --mobile-ratio: 3 / 4;" data-full="/assets/img/cooking/salmon-and-brussels-sprouts.jpg" aria-label="View salmon and Brussels sprouts">
      <img src="/assets/img/cooking/salmon-and-brussels-sprouts.jpg" alt="Garlic salmon with rosemary and Brussels sprouts" loading="lazy">
    </button>
    <button class="cooking-photo cooking-photo--feature cooking-photo--mobile-wide" type="button" style="grid-area: g; --crop-position: center 53%; --mobile-wide-ratio: 4 / 3;" data-full="/assets/img/cooking/soy-glazed-shrimp.jpg" aria-label="View soy-glazed shrimp">
      <img src="/assets/img/cooking/soy-glazed-shrimp.jpg" alt="Soy-glazed shrimp on a serving plate" loading="lazy">
    </button>
    <button class="cooking-photo cooking-photo--wide" type="button" style="grid-area: h; --crop-position: center 58%; --mobile-ratio: 4 / 3;" data-full="/assets/img/cooking/stir-fried-noodles.jpg" aria-label="View stir-fried noodles">
      <img src="/assets/img/cooking/stir-fried-noodles.jpg" alt="Stir-fried noodles with eggs and vegetables" loading="lazy">
    </button>
    <button class="cooking-photo cooking-photo--feature" type="button" style="grid-area: i; --crop-position: center 52%; --mobile-ratio: 3 / 4;" data-full="/assets/img/cooking/steak-dinner-for-two.jpg" aria-label="View steak dinner for two">
      <img src="/assets/img/cooking/steak-dinner-for-two.jpg" alt="Two steak dinners with spinach, carrots, and iced drinks" loading="lazy">
    </button>

    <button class="cooking-photo cooking-photo--tall" type="button" style="grid-area: j; --crop-position: center 52%; --mobile-ratio: 3 / 4;" data-full="/assets/img/cooking/braised-ribs-and-greens.jpg" aria-label="View braised ribs and greens">
      <img src="/assets/img/cooking/braised-ribs-and-greens.jpg" alt="Braised ribs and greens in serving bowls" loading="lazy">
    </button>
    <button class="cooking-photo cooking-photo--tall" type="button" style="grid-area: k; --crop-position: center 58%; --mobile-ratio: 3 / 4;" data-full="/assets/img/cooking/glazed-ribs.jpg" aria-label="View glazed ribs">
      <img src="/assets/img/cooking/glazed-ribs.jpg" alt="Glazed ribs topped with scallions" loading="lazy">
    </button>
    <button class="cooking-photo cooking-photo--wide" type="button" style="grid-area: l; --crop-position: center 52%; --mobile-ratio: 3 / 2;" data-full="/assets/img/cooking/beef-egg-and-soup.jpg" aria-label="View beef, eggs, vegetables, and soup">
      <img src="/assets/img/cooking/beef-egg-and-soup.jpg" alt="Home-cooked beef, eggs, vegetables, and soup" loading="lazy">
    </button>
    <button class="cooking-photo" type="button" style="grid-area: m; --crop-position: center 52%; --mobile-ratio: 3 / 4;" data-full="/assets/img/cooking/layered-drinks.jpg" aria-label="View layered iced drinks">
      <img src="/assets/img/cooking/layered-drinks.jpg" alt="Pink and green layered iced drinks" loading="lazy">
    </button>
    <button class="cooking-photo" type="button" style="grid-area: n; --crop-position: center 62%; --mobile-ratio: 3 / 4;" data-full="/assets/img/cooking/pink-drink.jpg" aria-label="View a pink iced drink">
      <img src="/assets/img/cooking/pink-drink.jpg" alt="A pink iced drink beside a floral mug" loading="lazy">
    </button>
    <button class="cooking-photo cooking-photo--feature" type="button" style="grid-area: o; --crop-position: center 62%; --mobile-ratio: 3 / 4;" data-full="/assets/img/cooking/matcha-basque-finished.jpg" aria-label="View a finished matcha Basque cheesecake">
      <img src="/assets/img/cooking/matcha-basque-finished.jpg" alt="A finished matcha Basque cheesecake with a slice cut out" loading="lazy">
    </button>
    <button class="cooking-photo cooking-photo--wide" type="button" style="grid-area: q; --crop-position: center 50%; --mobile-ratio: 4 / 3;" data-full="/assets/img/cooking/egg-and-peppers.jpg" aria-label="View eggs and peppers">
      <img src="/assets/img/cooking/egg-and-peppers.jpg" alt="Eggs and peppers with a side of lettuce" loading="lazy">
    </button>
    <button class="cooking-photo cooking-photo--tall" type="button" style="grid-area: r; --crop-position: center 58%; --mobile-ratio: 3 / 4;" data-full="/assets/img/cooking/beef-tofu-stew.jpg" aria-label="View beef and tofu stew">
      <img src="/assets/img/cooking/beef-tofu-stew.jpg" alt="Beef and tofu stew with vegetables" loading="lazy">
    </button>
    <button class="cooking-photo cooking-photo--tall" type="button" style="grid-area: s; --crop-position: center 58%; --mobile-ratio: 3 / 4;" data-full="/assets/img/cooking/braised-beef.jpg" aria-label="View sliced braised beef">
      <img src="/assets/img/cooking/braised-beef.jpg" alt="Sliced braised beef on a cutting board" loading="lazy">
    </button>
    <button class="cooking-photo cooking-photo--tall" type="button" style="grid-area: p; --crop-position: center 70%; --mobile-ratio: 3 / 4;" data-full="/assets/img/cooking/matcha-basque-baking.jpg" aria-label="View a matcha Basque cheesecake while baking">
      <img src="/assets/img/cooking/matcha-basque-baking.jpg" alt="A matcha Basque cheesecake baking in parchment paper" loading="lazy">
    </button>
    <button class="cooking-photo cooking-photo--tall" type="button" style="grid-area: t; --crop-position: center 58%; --mobile-ratio: 3 / 4;" data-full="/assets/img/cooking/salmon-rice.jpg" aria-label="View salmon and asparagus rice">
      <img src="/assets/img/cooking/salmon-rice.jpg" alt="Salmon and asparagus rice served with papaya" loading="lazy">
    </button>
    <button class="cooking-photo cooking-photo--feature" type="button" style="grid-area: u; --crop-position: center 58%; --mobile-ratio: 1;" data-full="/assets/img/cooking/braised-pork-and-cucumber-eggs.jpg" aria-label="View braised pork and cucumber eggs">
      <img src="/assets/img/cooking/braised-pork-and-cucumber-eggs.jpg" alt="Braised pork with chestnuts and cucumber eggs" loading="lazy">
    </button>

    <button class="cooking-photo" type="button" style="grid-area: v; --crop-position: center 48%; --mobile-ratio: 16 / 9;" data-full="/assets/img/cooking/tomato-eggs-and-rice.jpg" aria-label="View tomato eggs and rice">
      <img src="/assets/img/cooking/tomato-eggs-and-rice.jpg" alt="Tomato eggs with rice" loading="lazy">
    </button>
    <button class="cooking-photo cooking-photo--tall" type="button" style="grid-area: w; --crop-position: center 58%; --mobile-ratio: 3 / 4;" data-full="/assets/img/cooking/dumpling-filling.jpg" aria-label="View homemade dumpling filling">
      <img src="/assets/img/cooking/dumpling-filling.jpg" alt="Mixing homemade dumpling filling" loading="lazy">
    </button>
    <button class="cooking-photo cooking-photo--tall" type="button" style="grid-area: x; --crop-position: center 64%; --mobile-ratio: 3 / 4;" data-full="/assets/img/cooking/omelette.jpg" aria-label="View homemade omelette">
      <img src="/assets/img/cooking/omelette.jpg" alt="A homemade omelette" loading="lazy">
    </button>
    <button class="cooking-photo cooking-photo--feature" type="button" style="grid-area: y; --crop-position: center 52%; --mobile-ratio: 4 / 3;" data-full="/assets/img/cooking/tomato-stew.jpg" aria-label="View tomato stew with rice and vegetables">
      <img src="/assets/img/cooking/tomato-stew.jpg" alt="Tomato stew served with rice and vegetables" loading="lazy">
    </button>
    <button class="cooking-photo cooking-photo--wide" type="button" style="grid-area: z; --crop-position: center 48%; --mobile-ratio: 1;" data-full="/assets/img/cooking/fried-rice.jpg" aria-label="View homemade fried rice">
      <img src="/assets/img/cooking/fried-rice.jpg" alt="Homemade fried rice on a red plate" loading="lazy">
    </button>
    <button class="cooking-photo cooking-photo--tall" type="button" style="grid-area: aa; --crop-position: center 68%; --mobile-ratio: 3 / 4;" data-full="/assets/img/cooking/pumpkin-in-pan.jpg" aria-label="View pumpkin cooking in a pan">
      <img src="/assets/img/cooking/pumpkin-in-pan.jpg" alt="Pumpkin cooking in a pan" loading="lazy">
    </button>
    <button class="cooking-photo" type="button" style="grid-area: ab; --crop-position: center 50%; --mobile-ratio: 1;" data-full="/assets/img/cooking/dumplings.jpg" aria-label="View homemade dumplings">
      <img src="/assets/img/cooking/dumplings.jpg" alt="Homemade dumplings on a red plate" loading="lazy">
    </button>
  </div>
</div>

<dialog class="cooking-lightbox" aria-label="Cooking photo viewer">
  <button class="cooking-lightbox-close" type="button" aria-label="Close photo viewer" title="Close"><i class="fas fa-xmark" aria-hidden="true"></i></button>
  <div class="cooking-lightbox-frame">
    <button class="cooking-lightbox-prev" type="button" aria-label="Previous photo" title="Previous photo"><i class="fas fa-chevron-left" aria-hidden="true"></i></button>
    <img class="cooking-lightbox-image" src="" alt="">
    <button class="cooking-lightbox-next" type="button" aria-label="Next photo" title="Next photo"><i class="fas fa-chevron-right" aria-hidden="true"></i></button>
  </div>
</dialog>

<script>
  document.addEventListener('DOMContentLoaded', function () {
    var gallery = document.querySelector('.cooking-gallery');
    var lightbox = document.querySelector('.cooking-lightbox');
    if (!gallery || !lightbox) return;

    var photos = Array.prototype.slice.call(gallery.querySelectorAll('.cooking-photo'));
    var lightboxImage = lightbox.querySelector('.cooking-lightbox-image');
    var closeButton = lightbox.querySelector('.cooking-lightbox-close');
    var previousButton = lightbox.querySelector('.cooking-lightbox-prev');
    var nextButton = lightbox.querySelector('.cooking-lightbox-next');
    var activeIndex = 0;

    function showPhoto(index) {
      activeIndex = (index + photos.length) % photos.length;
      var photo = photos[activeIndex];
      var thumbnail = photo.querySelector('img');
      lightboxImage.src = photo.getAttribute('data-full');
      lightboxImage.alt = thumbnail.alt;
    }

    function openLightbox(index) {
      showPhoto(index);
      if (typeof lightbox.showModal === 'function') {
        lightbox.showModal();
      } else {
        lightbox.setAttribute('open', '');
      }
      closeButton.focus();
    }

    photos.forEach(function (photo, index) {
      photo.addEventListener('click', function () {
        openLightbox(index);
      });
    });

    closeButton.addEventListener('click', function () {
      lightbox.close();
    });
    previousButton.addEventListener('click', function () {
      showPhoto(activeIndex - 1);
    });
    nextButton.addEventListener('click', function () {
      showPhoto(activeIndex + 1);
    });
    lightbox.addEventListener('click', function (event) {
      if (event.target === lightbox) lightbox.close();
    });
    lightbox.addEventListener('keydown', function (event) {
      if (event.key === 'ArrowLeft') showPhoto(activeIndex - 1);
      if (event.key === 'ArrowRight') showPhoto(activeIndex + 1);
    });
    lightbox.addEventListener('close', function () {
      photos[activeIndex].focus();
      lightboxImage.src = '';
    });
  });
</script>
