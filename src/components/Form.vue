<template>
   <div>
      <form>
         <p>Jūsų vardas</p>
         <input class="personal-info" type="text" required v-model="name" />
         <p>Jūsų pavardė</p>
         <input class="personal-info" type="text" required v-model='surname' />
         <p>Jūsų amžius</p>
         <input class="personal-info" type="number" required v-model='age' />
         <p>Lytis:</p>
         <input v-model='gender' id='man' name="gender" type="radio" value="Vyras">
         <label for="man">Vyras</label>
         <input v-model='gender' id='woman' name="gender" type="radio" value="Moteris">
         <label for="woman">Moteris</label>
         <p>Kokie jūsų programavimo įgūdžiai?</p>
         <input v-model='languages' type="checkbox" id="language1" value="HTML">
         <label for="language1">HTML</label>
         <br>
         <input v-model='languages' type="checkbox" id="language2" value="CSS">
         <label for="language2">CSS</label>
         <br>
         <input v-model='languages' type="checkbox" id="language3" value='JavaScript'>
         <label for="language3">JavaScript</label>
         <br>
         <input v-model='languages' type="checkbox" id="language4" value='PHP'>
         <label for="languag4">PHP</label>
         <p>Kokią transporto priemonę mieliau vairuojat?</p>
         <select v-model='transport' name="better-transport" id="better-transport">
            <option selected>{{transport}}</option>
            <option value="Dviratis">Dviratį</option>
            <option value="Automobilis">Automobilį</option>
            <option value="Paspirtukas">Paspirtuką</option>
            <option value="Kita">Kita</option>
         </select>
         <p>Papasakokite daugiau apie savo vairavimo patirtį</p>
         <textarea v-model='moreInfo' name="more-info" id="more-info"></textarea>
      </form>
      <p class="answers">Vardas: {{name}}</p>
      <p class="answers">Pavardė: {{surname}}</p>
      <p class="answers">Amžius: {{age}}</p>
      <p class="answers">Lytis: {{gender}}</p>
      <p class="answers">Įgūdžiai: {{languages}}</p>
      <p class="answers">Transportas: {{transport}}</p>
      <p class="answers">Daugiau informacijos: {{moreInfo}}</p>
   </div>
</template>

<script lang="ts">

   export default {
    data() {
        return {
            name: "",
            surname: "",
            age: "",
            transport: "--Nepasirinkta--",
            languages: [],
            gender: "",
            moreInfo: ""
        }
    }
}
</script>

<style scoped>
form {
   max-width: 33em;
   margin: 1em auto;
   background: white;
   padding: 4em;
   border-radius: 10px;
}

label {
   display: inline-block;
   margin: 0.5em;
   font-size: 0.8em;
   text-transform: uppercase;
   color: #aaa;
   font-weight: 500;
}

.personal-info,
select {
   display: block;
   box-sizing: border-box;
   padding: 1em;
   border: none;
   border: 1px solid #ddd;
   margin: 2px;
   width: 100%;
   border-radius: 10px;
}

p {
   margin: 1em 0 1em 0;
   color: #aaa;
   text-transform: uppercase;
   font-size: 0.9em;
   font-weight: bold;
}

textarea {
   width: 100%;
   padding: 1em;
   height: 8em;
   resize: none;
   font-family: Arial, Helvetica, sans-serif;
   letter-spacing: 0.1ch;
   border-radius: 10px;
   border: 1px solid #ddd;
}

.answers {
   color: black;
   text-transform: none;
   font-weight: 400;
   font-size: 1.2em;
}
</style>