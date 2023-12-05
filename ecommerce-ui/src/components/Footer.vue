<template>
  <footer>
    <div class="container pt-5">
      <div class="row">
        <div class="col-md-3 col-6">
          <ul style="list-style-type: none">
            <li class="text-light font-weight-bold pb-2">Rólunk</li>
            <li><a class="footer-link font-weight-light" href="#">Rólunk</a></li>
            <li><a class="footer-link font-weight-light" href="#">Android Applikáció</a><br></li>
            <li><a class="footer-link font-weight-light" href="#">iOS Applikáció</a><br></li>
          </ul>
        </div>

        <div class="col-md-3 col-6">
          <ul style="list-style-type: none">
            <li class="text-light font-weight-bold">Eléhetőségeink</li>
            <li><a class="footer-link font-weight-light" href="#">Facebook</a></li>
            <li><a class="footer-link font-weight-light" href="#">Twitter</a><br></li>
            <li><a class="footer-link font-weight-light" href="#">Instagram</a><br></li>
          </ul>
        </div>

        <div class="col-md-3 col-6">
          <ul style="list-style-type: none">
            <li class="text-light font-weight-bold">Dolgozz velünk</li>
            <li><a class="footer-link font-weight-light" href="#">Adj el velünk</a></li>
            <li><a class="footer-link font-weight-light" href="#">Legyél partner</a><br></li>
            <li><a class="footer-link font-weight-light" href="#">Hirdess nálunk</a><br></li>
          </ul>
        </div>

        <div class="col-md-3 col-6">
          <ul style="list-style-type: none">
            <li class="text-light font-weight-bold">Segítség kell?</li>
            <li><a class="footer-link font-weight-light" href="#">Visszajelzés küldése</a></li>
            <li><a class="footer-link font-weight-light" href="#">Biztosítás</a><br></li>
            <li><a class="footer-link font-weight-light" href="#">Súgó</a><br></li>
            <li><a class="footer-link font-weight-light" href="#"></a><br></li>
          </ul>
        </div>
      </div>

      <div class="row">
        <div class="col-12">
          <div class="text-center py-5">
            <img id="logo" src="../assets/icon.png" />
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name : 'FooterMain'
}
</script>

<style>
footer {
  margin-top : 100px;
  background-color:#232F3E;
  font-size:16px;
}

li {
  padding-left: 0;
  padding-bottom: 10px;
}

a {
  text-decoration: none;
}

.footer-link {
  color: #DDD;
}

#logo {
  width: 150px;
}

footer {
  font-family: 'Roboto', sans-serif;
}


</style>
