<template>
  <div class="container">
    <!-- code here -->
    <div class="card" >
      <div class="card-img skeleton">
        <!-- waiting for img to load from javascript -->
      </div>
      <div class="card-body">
        <h2 class="card-title skeleton">
          <!-- wating for title to load from javascript -->
        </h2>
        <p class="card-intro skeleton">
          <!-- waiting for intro to load from Javascript -->
        </p>
      </div>
    </div>
  </div>
</template>

<script></script>

<style lang="scss">
  *, *:after, *:before {
    box-sizing: border-box;
  }

  body {
    font-family: "Inter", sans-serif;
    background-color: #f2f5f7;
  }

  // THE CARD
  .card {
    display: flex;
    flex-direction: column;
    flex-basis: 300px;
    flex-shrink: 0;
    flex-grow: 0;
    max-width: 100%;
    background-color: #FFF;
    box-shadow: 0 5px 10px 0 rgba(#000, .15);
    border-radius: 10px;
    overflow: hidden;
    margin: 1rem;
  }

  .card-img {
    padding-bottom: 56.25%;
    position: relative;
    img {
      position: absolute;
      width: 100%;
    }
  }

  .card-body {
    padding: 1.5rem;
  }

  .card-title {
    font-size: 1.25rem;
    line-height: 1.33;
    font-weight: 700;
    &.skeleton { // NOTICE THIS
      min-height: 28px;
      border-radius: 4px;
    }
  }

  .card-intro {
    margin-top: .75rem;
    line-height: 1.5;
    &.skeleton { // NOTICE THIS
      min-height: 72px;
      border-radius: 4px;
    }
  }

  // THE LOADING EFFECT
  .skeleton {
    background-color: #e2e5e7;
  // The shine that's going to move across the skeleton:
    background-image:
        linear-gradient(
            90deg,
            rgba(#fff, 0),
            rgba(#fff, 0.5),
            rgba(#fff, 0)
        );
    background-size: 40px 100%; // width of the shine
    background-repeat: no-repeat; // No need to repeat the shine effect
    background-position: left -40px top 0; // Place shine on the left side, with offset on the left based on the width of the shine - see background-size
    animation: shine 1s ease infinite; // increase animation time to see effect in 'slow-mo'
  }

  @keyframes shine {
    to {
    // Move shine from left to right, with offset on the right based on the width of the shine - see background-size
      background-position: right -40px top 0;
    }
  }


  // Codepen spesific styling - only to center the elements in the pen preview and viewport
  .container {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
  }
  // End Codepen spesific styling

  @media (max-width: 1023px) and (min-width: 0px) {
    .card {
      min-width: 214px;
      display: flex;
      justify-content: center;
      flex-direction: column;
      flex-basis: 214px;
      flex-shrink: 0;
      flex-grow: 0;
      max-width: 100%;
      background-color: #FFF;
      box-shadow: 0 5px 10px 0 rgba(#000, .15);
      border-radius: 10px;
      overflow: hidden;
      margin: 1rem;
    }

    .card-img {
      padding-bottom: 56.25%;
      position: relative;
      width: 214px;
      height: 321px;
      img {
        position: absolute;
        width: 214px;
        height: 321px;
      }
    }

    .card-body {
      padding: 1.5rem;
    }

    .card-title {
      font-size: 1.25rem;
      line-height: 1.33;
      font-weight: 700;
      &.skeleton { // NOTICE THIS
        min-height: 18px;
        width: 136px;
        border-radius: 4px;
      }
    }

    .card-intro {
      margin-top: .75rem;
      line-height: 1.5;
      &.skeleton { // NOTICE THIS
        min-height: 20px;
        width: 90px;
        border-radius: 4px;
      }
    }
  }


  @media (max-width: 1439px) and (min-width: 1023px) {
    .card {
      min-width: 256px;
      display: flex;
      justify-content: center;
      flex-direction: column;
      flex-basis: 256px;
      flex-shrink: 0;
      flex-grow: 0;
      max-width: 100%;
      background-color: #FFF;
      box-shadow: 0 5px 10px 0 rgba(#000, .15);
      border-radius: 10px;
      overflow: hidden;
      margin: 1rem;
    }

    .card-img {
      padding-bottom: 56.25%;
      position: relative;
      width: 256px;
      height: 384px;
      img {
        position: absolute;
        width: 256px;
        height: 384px;
      }
    }

    .card-body {
      padding: 1.5rem;
    }

    .card-title {
      font-size: 1.25rem;
      line-height: 1.33;
      font-weight: 700;
      &.skeleton { // NOTICE THIS
        min-height: 15px;
        width: 103px;
        border-radius: 4px;
      }
    }

    .card-intro {
      margin-top: .75rem;
      line-height: 1.5;
      &.skeleton { // NOTICE THIS
        min-height: 20px;
        width: 91px;
        border-radius: 4px;
      }
    }
  }

  @media (max-width: 1919px) and (min-width: 1440px)  {
    .card {
      min-width: 360px;
      display: flex;
      justify-content: center;
      flex-direction: column;
      flex-basis: 360px;
      flex-shrink: 0;
      flex-grow: 0;
      max-width: 100%;
      background-color: #FFF;
      box-shadow: 0 5px 10px 0 rgba(#000, .15);
      border-radius: 10px;
      overflow: hidden;
      margin: 1rem;
    }

    .card-img {
      padding-bottom: 56.25%;
      position: relative;
      width: 360px;
      height: 540px;
      img {
        position: absolute;
        width: 360px;
        height: 540px;
      }
    }

    .card-body {
      padding: 1.5rem;
    }

    .card-title {
      font-size: 1.25rem;
      line-height: 1.33;
      font-weight: 700;
      &.skeleton { // NOTICE THIS
        min-height: 18px;
        width: 143px;
        border-radius: 4px;
      }
    }

    .card-intro {
      margin-top: .75rem;
      line-height: 1.5;
      &.skeleton { // NOTICE THIS
        min-height: 25px;
        width: 119px;
        border-radius: 4px;
      }
    }
  }

  @media (max-width: 4479px) and (min-width: 1920px) {

    .card {
      min-width: 383px;
      display: flex;
      justify-content: center;
      flex-direction: column;
      flex-basis: 383px;
      flex-shrink: 0;
      flex-grow: 0;
      max-width: 100%;
      background-color: #FFF;
      box-shadow: 0 5px 10px 0 rgba(#000, .15);
      border-radius: 10px;
      overflow: hidden;
      margin: 1rem;
    }

    .card-img {
      padding-bottom: 56.25%;
      position: relative;
      width: 383px;
      height: 575px;
      img {
        position: absolute;
        width: 383px;
        height: 575px;
      }
    }

    .card-body {
      padding: 1.5rem;
    }

    .card-title {
      font-size: 1.25rem;
      line-height: 1.33;
      font-weight: 700;
      &.skeleton { // NOTICE THIS
        min-height: 18px;
        width: 143px;
        border-radius: 4px;
      }
    }

    .card-intro {
      margin-top: .75rem;
      line-height: 1.5;
      &.skeleton { // NOTICE THIS
        min-height: 25px;
        width: 119px;
        border-radius: 4px;
      }
    }
  }

  @media (min-width: 4480px) {

    .card {
      min-width: 746px;
      display: flex;
      justify-content: center;
      flex-direction: column;
      flex-basis: 746px;
      flex-shrink: 0;
      flex-grow: 0;
      max-width: 100%;
      background-color: #FFF;
      box-shadow: 0 5px 10px 0 rgba(#000, .15);
      border-radius: 10px;
      overflow: hidden;
      margin: 1rem;
    }

    .card-img {
      padding-bottom: 56.25%;
      position: relative;
      width: 746px;
      height: 1119px;
      img {
        position: absolute;
        width: 746px;
        height: 1119px;
      }
    }

    .card-body {
      padding: 1.5rem;
    }

    .card-title {
      font-size: 1.25rem;
      line-height: 1.33;
      font-weight: 700;
      &.skeleton { // NOTICE THIS
        min-height: 38px;
        width: 307px;
        border-radius: 4px;
      }
    }

    .card-intro {
      margin-top: .75rem;
      line-height: 1.5;
      &.skeleton { // NOTICE THIS
        min-height: 38px;
        width: 178px;
        border-radius: 4px;
      }
    }
  }
</style>