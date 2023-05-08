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

</script>

<template>
  <form class="info" @submit.prevent="enviar()">
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
    <input type="text" name="hobbie" placeholder="Digite seu hobbie">
    <br>
    <label name="linguagem">Linguagens de Programação:</label>
    <br>
    <input type="checkbox" v-model="linguagemdepgr" value="languagecode">
    <label for="linguagemdepgr">C++</label>
    <br>
    <input type="checkbox" v-model="linguagemdepgr" value="languagecode">
    <label for="linguagemdepgr">JavaScript</label>
    <br>
    <input type="checkbox" v-model="linguagemdepgr" value="languagecode">
    <label for="linguagemdepgr">Java</label>
    <br>
    <input type="checkbox" v-model="linguagemdepgr" value="languagecode">
    <label for="linguagemdepgr">Python</label>
    <br>
    <label name="hobbie">Biografia:</label>
    <br>
    <input type="text" name="biografia" placeholder="Escreva sua biografia">

    <button type="submit" @click="aceitar = !aceitar">Submit</button>

    <div v-if="aceitar" id="div">
      <img :src="user.avatar" />
      <p>{{ nome }}</p>
      <p>{{ email }}</p>
      <p>{{ senha }}</p>
      <p>{{ data }}</p>
      <p>{{ endereço }}</p>
      <p>{{ cidade }}</p>
      <p>{{ estado }}</p>
      <p>{{ hobbies }}</p>
      <p>{{ linguagemProg }}</p>
      <p>{{ biografia }}</p>
    </div>

  </form>
</template>

<style scoped>
form {
  background-color: rgb(0, 20, 110);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
}

#div {
  background-color: rgba(35, 12, 22, 1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
  text-align: center;
  margin: 0px 0px 0px 50px;
  height: fit-content;
}
</style>