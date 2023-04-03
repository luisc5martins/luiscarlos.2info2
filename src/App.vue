<script setup>

</script>

<template>

<label name="nome">Nome:</label>
<input type="text" name="nome" placeholder="Digite seu nome">
<label name="email">Email:</label>
<input type="email" name="email" placeholder="Digite seu Email">
<label name="senha">Senha:</label>
<input type="password" name="senha" placeholder="Digite sua Senha">
<label name="confirmasenha">Confirme sua senha:</label>
<input type="password" name="confirmasenha" placeholder="Digite sua senha novamente">
<label name="datanascimento">Data de nascimento</label>
<input type="date" name="datanascimento" placeholder="Digite sua data de nascimento">
<label name="endereco">Endereço:</label>
<input type="text" name="endereco" placeholder="Digite seu endereço">
<label name="cidade">Cidade:</label>
<input type="string" name="cidade" placeholder="Digite sua cidade">
<label name="estado">Estado</label>
<select name="Estado">
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
  <option value="rJ">RJ</option>
  <option value="rn">RN</option>
  <option value="rs">RS</option>
  <option value="ro">RO</option>
  <option value="rr">RR</option>
  <option value="sc">SC</option>
  <option value="sp">SP</option>
  <option value="se">SE</option>
  <option value="to">TO</option>
</select>
<label name="hobbie">Hobbie:</label>
<input type="text" name="hobbie" placeholder="Digite seu hobbie">
<label name="linguagem">Linguagem de Programação</label>
<input type="checkbox" name="linguagemdepgr" placeholder="Digite sua linguagem de programação">


</template>

<style scoped>
button {
  font-weight: bold;
}
</style>