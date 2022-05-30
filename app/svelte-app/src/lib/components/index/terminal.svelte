<section>
  <div id="screen">
    <p>Example text</p>
  </div>
</section>

<style lang="scss">
  p {
    margin: 0;
    padding: 0;
  }

  section {
    min-height: 100vh;
    background-color: gray;
    padding: 20px;
    display: flex;
  }

  div#screen {
    /* text effects */
    font-size: 20px;
    font-family: monospace, monospace;
    color: rgb(142, 210, 82);
    text-shadow: 0 0 5px #c8c8c8;
    p {
      filter: blur(0.5px);
    }

    /* Spacing and size */
    width: 100%;
    padding: 10px;

    /*transform: scale3d(1.05, 1.05, 2);*/

    /* Screen backlight gradient */
    z-index: 99999;

    background-image: radial-gradient(rgba(20, 100, 20, 0.7), black 120%);

    /* Lines on screen */
    position: relative;
    &::after {
      content: "";
      position: absolute;
      background-size: 100%;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: repeating-linear-gradient(
        0deg,
        rgba(black, 0.15),
        rgba(black, 0.15) 1px,
        transparent 1px,
        transparent 2px
      );
    }
  }
</style>
