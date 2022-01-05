![Github avatar image](https://avatars.githubusercontent.com/u/39529221?size=200)

# Danil Shapilov

## Contact information

**Telegram:** [@shapilov_dev](https://t.me/shapilov_dev)  
**Email:** [danil@shapilov.dev](mailto:danil@shapilov.dev)  
**Discord:** DanilShapilov#5006  
[Linkedin](https://www.linkedin.com/in/danilshapilov/)

---

## Briefly about myself:

Playing around with JS since 2017. Started when was in college by creating simple games with HTML5 Canvas to participate in World Skill Russia Web Development competition.

Done some work for local web studio, worked with SQL, PHP, JS, CSS, ElectronJS.

Still learning, right now interested in 3d graphics on the web, planning to learn ThreeJS and Blender.

---

## Skills

- HTML, SASS, JS
- React, Redux,
- Git, Github
- SQL, MongoDB
- VSCode, WSL2
- RegEx
- Photoshop, Figma
- Familiar with:
  - BEM
  - Gsap
  - Redux-thunk, Redux-Saga, styled-components
  - Webpack, Parcel
  - TypeScript
  - VueJS
  - ElectronJS
  - Big O, Data Structures, Algorithms

---

## Code example:

Solution for the [_'A.'_ task from YandexCup](https://yandex.ru/cup/frontend/analysis/), which works about 2x faster that solution from Yandex on HUGE arrays.  
Why is it faster? Because instead of overriding values with 0, we remove them from array, so with every loop there is less items to loop for.

```
const findLatestWeight = function (weights) {
  if (weights.length <= 1) {
    return weights[0];
  }

  do {
    let big = 0
    let beforeBig = 0
    let bigI = 0
    let beforeBigI = 0
    for (let i = 0; i < weights.length; i++) {
      const weight = weights[i];
      if (weight >= big) {
        beforeBig = big
        big = weight

        beforeBigI = bigI
        bigI = i
      } else if (weight > beforeBig) {
        beforeBig = weight
        beforeBigI = i

      }
    }
    if (beforeBig === 0) {
      return big
    }

    let annigilationResult = big - beforeBig


    if (annigilationResult) {
      weights[bigI] = annigilationResult
      if (weights.length !== beforeBigI + 1) {
        weights[beforeBigI] = weights.pop()
      } else {
        weights.pop()
      }
    } else {

      if (bigI < beforeBigI) {
        [bigI, beforeBigI] = [beforeBigI, bigI]
      }
      if (weights.length === bigI + 1) {
        weights.pop()
      } else {
        weights[bigI] = weights.pop()
      }

      if (weights.length === beforeBigI + 1) {
        weights.pop()
      } else {
        weights[beforeBigI] = weights.pop()
      }
    }
  } while (true);
}
```

---

## Experience:

1. [SliderPlugin](https://github.com/DanilShapilov/sliderPlugin) - Plugin for jQuery written in TS (not refactored, first attempt) was trying to use MVP pattern.
1. [Yelp-Camp](https://github.com/DanilShapilov/YelpCamp) - A website to create, find and rate campgrounds.
   - Express
   - mongoose, mongodb
   - mapbox
   - Bootstrap 5
   - Cloudinary
   - Helmet JS
1. [crwn-clothing](https://github.com/DanilShapilov/crwn-clothing) - Clothes store website.

   - React, Redux, Saga
   - styled-components
   - Firebase
   - Stripe

1. [Todo App](https://github.com/DanilShapilov/todo-app) - Test task for vacancy
   - React, Redux
   - styled-components
