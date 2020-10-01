<template>
  <div class="hello">
    <div class="wrap">
      <h1>Exercice</h1>
      <p>
        J'aimerais ajouter une class active <code>:class="{ 'active': letter.active }"</code> quand je clique sur une lettre.<br/>
        Mais ma fonction <code>addActiveOnLetter</code> ne fonctionne pas.<br/>
        Pourtant dans la console, la clé <code>active</code> a bien été ajouté a l'objet sur lequel j'ai cliqué...
      </p>
      <p>Une idée ? 🧐</p>
      <i>Tu ne peux pas modifier l'array letters dans data()</i>
      <p>
      Ensuite, tu peux modifier la fonction pour ajouter les fonctionalités suivantes :<br/>
      - Déselectionner une lettre<br/>
      - N'avoir qu'une seule lettre active
      </p>
    </div>
    <div class="exercise">
      <ul class="flex wrap">
        <li v-for="letter in letters" :class="{ 'active': letter.active }" :key="letter.key">
          <button @click="addActiveOnLetter(letter)">{{ letter.value }}</button>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import letters from './letters.js'

export default {
  name: 'HelloWorld',
  data() {
    return {
      letters
    }
  },
  methods: {
    addActiveOnLetter(letter) {
      letter.active = true

      console.log(letter)
    }
  }
}
</script>

<style scoped>
  .flex {
    display: flex
  }
  .wrap {
    flex-wrap: wrap
  }
  ul {
    list-style: none;
    padding: 0
  }
  li {
    margin: 0 15px 0 0
  }
  .wrap {
    width: 600px;
    margin: 0 auto
  }
  button {
    background-color: pink;
    padding: 15px;
    border: 0
  }
  button:hover {
    background-color: green
  }
  .active button {
    background-color: aliceblue
  }
  .exercise {
    margin: 65px auto 0
  }
</style>
