<script>
  import {characters} from "./lib/vars";
</script>

<div class="mainCont">

  <div class="logo">
    <img src="imagenes/logo.png" alt='logo'>
  </div>
  <div class="charCont">
    {#each characters as character}
  <a class="character" id={character} href="{character}.html">
    <img src="SmashCharacters/{character}.png" alt={character}>
  </a>
{/each}
  </div>
  <div class="button" id="pressing"></div>
</div>

<style>
.mainCont {
    display: flex;
    position: absolute;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100%;
    width: 50%;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    margin: auto;
}

.logo {
    display: flex;
    position: relative;
    justify-content: center;
    align-items: center;
    height: 40%;
    width: 100%;
}

.logo img {
    position: absolute;
    width: 75%;
}

.charCont {
    display: flex;
    position: relative;
    flex-direction: row;
    align-content: center;
    justify-content: space-between;
    align-items: flex-start;
    flex-wrap: wrap;
    width: 100%;
}

.character {
    display: flex;
    position: relative;
    justify-content: center;
    align-items: center;
    width: 10%;
    border: 0.5cqmin solid #353535; 
    background-image: url("imagenes/select_fighter.png");
    overflow: hidden;
    aspect-ratio: 1 / 1;
}

.character:focus {
    outline: none;
    border: 0.5cqmin solid #EBEBEB;
}

.character img {
    position: absolute;
    height: 95%;
}

#young_link img{
    height: 110%;
}

#kirby img, #pikachu img {
    height: 120%;
}

#jigglypuff img {
    height: 80%;
}

#lucas img{
    height: 85%;
}
</style>
