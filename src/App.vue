<script setup>

import { ref } from 'vue'

const name = ref('')
const email = ref('')
const senha = ref('')
const confirmasenha = ref('')
const datanascimento = ref('')
const endereco = ref('')
const cidade = ref('')
const estado = ref('')
const hobbie = ref('')
const linguagemdepgr = ref('')
const biografia = ref('')
const aceitar = ref(true)

function Submit() {
  if (senha.value != confirmasenha.value) {
    alert("As senhas estão diferentes")
  }
  else {
    aceitar.value = !aceitar.value
  }
}
</script>

<template>
  <form class="info" @submit.prevent="Submit()">
    <label name="name">Nome:</label>
    <br>
    <input type="text" v-model="name" placeholder="Digite seu nome">
    <br>
    <label name="email">Email:</label>
    <br>
    <input type="email" v-model="email" placeholder="Digite seu Email">
    <br>
    <label name="senha">Senha:</label>
    <br>
    <input type="password" v-model="senha" placeholder="Digite sua Senha">
    <br>
    <label name="confirmasenha">Confirme sua senha:</label>
    <br>
    <input type="password" v-model="confirmasenha" placeholder="Digite sua senha novamente">
    <br>
    <label name="datanascimento">Data de nascimento</label>
    <br>
    <input type="date" v-model="datanascimento" placeholder="Digite sua data de nascimento">
    <br>
    <label name="endereco">Endereço:</label>
    <br>
    <input type="text" v-model="endereco" placeholder="Digite seu endereço">
    <br>
    <label name="cidade">Cidade:</label>
    <br>
    <input type="string" v-model="cidade" placeholder="Digite sua cidade">
    <br>
    <label name="estado">Estado</label>
    <br>
    <select v-model="estado">
      <option value="vazio">selecione seu estado</option>
      <option value="ac">AC</option>
      <option value="al">AL</option>
      <option value="ap">AP</option>
      <option value="am">AM</option>
      <option value="ba">BA</option>
      <option value="ce">CE</option>
      <option value="df">DF</option>
      <option value="es">ES</option>
      <option value="go">GO</option>
      <option value="ma">MA</option>
      <option value="mt">MT</option>
      <option value="ms">MS</option>
      <option value="mg">MG</option>
      <option value="pa">PA</option>
      <option value="pb">PB</option>
      <option value="pe">PE</option>
      <option value="pi">PI</option>
      <option value="pr">PR</option>
      <option value="rj">RJ</option>
      <option value="rn">RN</option>
      <option value="rs">RS</option>
      <option value="ro">RO</option>
      <option value="rr">RR</option>
      <option value="sc">SC</option>
      <option value="sp">SP</option>
      <option value="se">SE</option>
      <option value="to">TO</option>
    </select>
    <br>
    <label name="hobbie">Hobbie:</label>
    <br>
    <input type="text" v-model="hobbie" placeholder="Digite seu hobbie">
    <br>
    <label for="linguagemdepgr">Digite suas Linguagens:</label>
    <br>
    <input type="text" v-model="linguagemdepgr">
    <br>
    <label name="biografia">Biografia:</label>
    <br>
    <textarea v-model="biografia" placeholder="Escreva sua biografia" rows="9"></textarea>
    <br>
    <button type="submit" @click="aceitar = !aceitar">Submit</button>

  </form>

  <div v-if="aceitar" id="div">
      <p>Seu nome é: {{ name }}</p>
      <p>Seu email é: {{ email }}</p>
      <p>Sua senha é: {{ senha }}</p>
      <p>Sua data de nascimento é: {{ datanascimento }}</p>
      <p>Seu endereo é: {{ endereco }}</p>
      <p>Sua cidade é: {{ cidade }}</p>
      <p>Seu estado é: {{ estado }}</p>
      <p>Seu Hobbie: {{ hobbie }}</p>
      <p>Linguagens de programação dominantes: {{ linguagemdepgr }}</p>
      <p>Sua biografia: {{ biografia }}</p>
    </div>
</template>

<style scoped>
form {
  background-color: rgb(110, 0, 0);
  padding: 20px 30px;
  color: white;
  border-radius: 10px;
}

#div {
  background-color: rgb(110, 0, 0);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
  text-align: center;
  margin: 0px 0px 0px 50px;
  height: fit-content;
}
</style>