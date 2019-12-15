<template>
  <footer class="Footer">
     <mdb-container fluid>
        <center>&copy;  Copyright: <a href="https://www.linkedin.com/in/debjyoti-mohapatra-73a73b123/"> Debjyoti Mohapatra </a></center>
      </mdb-container>
  </footer>
</template>

<script>
export default {
  name: "Footer"
}
</script>

<style scoped>
  .Footer {
    background: #333;
    color: #fff;
    text-align: center;
    padding: 10px;
     position: absolute;
    bottom: 0;
    width: 100%;
    height: 2.5rem;        
  }

  .Footer a {
    color: #fff;
    padding-right: 5px;
    text-decoration: none;
  }
</style>


