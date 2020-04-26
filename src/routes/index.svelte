<script>
  let C, Db, D, Eb, E, F, Gb, G, Ab, A, Bb, B;
  let CKey = false;
  let DbKey = false;
  let DKey = false;
  let EbKey = false;
  let EKey = false;
  let FKey = false;
  let GbKey = false;
  let GKey = false;
  let AbKey = false;
  let AKey = false;
  let BbKey = false;
  let BKey = false;

  document.addEventListener("keydown", e => {
    if (e.repeat) return;
  });

  function playNote(key) {
    if (key === "C") {
      C.currentTime = 0;
      C.play();
      CKey = true;
      C.addEventListener("ended", () => {
        CKey = false;
      });
    }
    if (key === "Db") {
      Db.currentTime = 0;
      Db.play();
      DbKey = true;
      Db.addEventListener("ended", () => {
        DbKey = false;
      });
    }
    if (key === "D") {
      D.currentTime = 0;
      D.play();
      DKey = true;
      D.addEventListener("ended", () => {
        DKey = false;
      });
    }
    if (key === "Eb") {
      Eb.currentTime = 0;
      Eb.play();
      EbKey = true;
      Eb.addEventListener("ended", () => {
        EbKey = false;
      });
    }
    if (key === "E") {
      E.currentTime = 0;
      E.play();
      EKey = true;
      E.addEventListener("ended", () => {
        EKey = false;
      });
    }
    if (key === "F") {
      F.currentTime = 0;
      F.play();
      FKey = true;
      F.addEventListener("ended", () => {
        FKey = false;
      });
    }
    if (key === "Gb") {
      Gb.currentTime = 0;
      Gb.play();
      GbKey = true;
      Gb.addEventListener("ended", () => {
        GbKey = false;
      });
    }
    if (key === "G") {
      G.currentTime = 0;
      G.play();
      GKey = true;
      G.addEventListener("ended", () => {
        GKey = false;
      });
    }
    if (key === "Ab") {
      Ab.currentTime = 0;
      Ab.play();
      AbKey = true;
      Ab.addEventListener("ended", () => {
        AbKey = false;
      });
    }
    if (key === "A") {
      A.currentTime = 0;
      A.play();
      AKey = true;
      A.addEventListener("ended", () => {
        AKey = false;
      });
    }
    if (key === "Bb") {
      Bb.currentTime = 0;
      Bb.play();
      BbKey = true;
      Bb.addEventListener("ended", () => {
        BbKey = false;
      });
    }
    if (key === "B") {
      B.currentTime = 0;
      B.play();
      BKey = true;
      B.addEventListener("ended", () => {
        BKey = false;
      });
    }
  }
</script>

<style>
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  .piano {
    background-color: #143f6b;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .box {
    display: flex;
  }

  .key {
    height: calc(var(--width) * 4);
    width: var(--width);
  }

  .white {
    --width: 100px;
    background-color: white;
    border: 1px solid #333;
  }

  .white.active {
    background-color: #ccc;
  }

  .black {
    --width: 60px;
    background-color: black;
    margin-left: calc(var(--width) / -2);
    margin-right: calc(var(--width) / -2);
    z-index: 2;
  }

  .black.active {
    background-color: #333;
  }
</style>

<div class="piano">
  <div class="box">
    <div on:click={() => playNote('C')} class:active={CKey} class="key white" />
    <div
      on:click={() => playNote('Db')}
      class:active={DbKey}
      class="key black" />
    <div on:click={() => playNote('D')} class:active={DKey} class="key white" />
    <div
      on:click={() => playNote('Eb')}
      class:active={EbKey}
      class="key black" />
    <div on:click={() => playNote('E')} class:active={EKey} class="key white" />
    <div on:click={() => playNote('F')} class:active={FKey} class="key white" />
    <div
      on:click={() => playNote('Gb')}
      class:active={GbKey}
      class="key black" />
    <div on:click={() => playNote('G')} class:active={GKey} class="key white" />
    <div
      on:click={() => playNote('Ab')}
      class:active={AbKey}
      class="key black" />
    <div on:click={() => playNote('A')} class:active={AKey} class="key white" />
    <div
      on:click={() => playNote('Bb')}
      class:active={BbKey}
      class="key black" />
    <div on:click={() => playNote('B')} class:active={BKey} class="key white" />
  </div>
</div>

<audio bind:this={C} src="/C.mp3" />
<audio bind:this={Db} src="/Db.mp3" />
<audio bind:this={D} src="/D.mp3" />
<audio bind:this={Eb} src="/Eb.mp3" />
<audio bind:this={E} src="/E.mp3" />
<audio bind:this={F} src="/F.mp3" />
<audio bind:this={Gb} src="/Gb.mp3" />
<audio bind:this={G} src="/G.mp3" />
<audio bind:this={Ab} src="/Ab.mp3" />
<audio bind:this={A} src="/A.mp3" />
<audio bind:this={Bb} src="/Bb.mp3" />
<audio bind:this={B} src="/B.mp3" />
