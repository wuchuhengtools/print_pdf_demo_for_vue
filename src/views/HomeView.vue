<script setup lang="ts">
import printJS from "print-js";

const onPrint = () => printJS('tableID', 'html')

</script>

<template>
  <div class="header">header</div>
  <div class="mainWrapper">
    <div class="nav">nav</div>
    <div class="main">
      <table id="tableID">
        <tr>
          <th>Firstname</th>
          <th>Lastname</th>
          <th>Age</th>
        </tr>
        <tr>
          <td>Jill</td>
          <td>Smith</td>
          <td>50</td>
        </tr>
        <tr>
          <td>Eve</td>
          <td>Jackson</td>
          <td>94</td>
        </tr>
        <tr>
          <td>John</td>
          <td>Doe</td>
          <td>80</td>
        </tr>
      </table>
      <button @click="onPrint">Print table to PDF</button>
    </div>

  </div>
</template>
<style>
table, th, td {
  border: 1px solid white;
  border-collapse: collapse;
}
th, td {
  background-color: #96D4D4;
}
.main {
  margin: 1rem;
}

.header {
  height: 5rem;
  background: red;
}
.mainWrapper {
  display: flex;
}

.nav{
  width: 10rem;
  background: yellow;
  height: calc(100vh - 5rem);
}
</style>
