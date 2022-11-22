<template>
    <footer class="footer">
      <div class="container">
          <div class="footer-col">
            <h4>Compagnie</h4>
            <ul>
              <li><a href="#">A propos</a></li>
              <li><a href="#">our services</a></li>
              <li><a href="#">privacy policy</a></li>
              <li><a href="#">affiliate program</a></li>
            </ul>
          </div>
          <div class="footer-col">
            <h4>get help</h4>
            <ul>
              <li><a href="#">FAQ</a></li>
              <li><a href="#">shipping</a></li>
              <li><a href="#">returns</a></li>
              <li><a href="#">order status</a></li>
              <li><a href="#">payment options</a></li>
            </ul>
          </div>
          <div class="footer-col">
            <h4>Suivez-nous</h4>
            <div class="social-links"></div>
              <a href="#"><i class="fab fa-facebook-f"></i></a>
              <a href="#"><i class="fab fa-twitter"></i></a>
              <a href="#"><i class="fab fa-instagram"></i></a>
              <a href="#"><i class="fab fa-linkedin-in"></i></a>
          </div>
      </div>
    </footer>
    
    </template>
    
    <script>
    export default {
      name: 'Footer',
      props: {
       
        titre:String,
        image:String,
      }
    }
    </script>
    <style>
   .container{
  max-width: 1170px;
  background-color: #24262b;
  margin: auto;
}

ul{
  list-style: none;
}

footer{
  background-color: #24262b;
}

.footer-col{
  width: 100%;
  padding: 0 15px;
  margin-bottom: 30px;
}

.footer-col h4{
  font-size: 18px;
  color: #ffffff;
  text-transform: capitalize;
  margin-bottom: 35px;
  font-weight: 500;
  position: relative;
}

.footer-col h4::before{
  content:"";
  position: absolute;
  left: 0;
  bottom: -10px;
  background-color: rgb(242,148,0);
  height: 2px;
  box-sizing: border-box;
  width: 50px;
}

.footer-col ul li:not(:last-child){
  margin-bottom: 10px;
}

.footer-col ul li a {
  font-size: 16px;
  text-transform: capitalize;
  color: #fff;
  text-decoration: none;
  font-weight: 300;
  color: #bbbbbb;
  display: block;
  transition: all 0.3s ease;
}

.footer-col ul li a:hover{
  color: #fff;
  padding-left: 8px;
}

.footer-col .social-links a{
  display: inline-block;
  height: 40px;
  width: 40px;
  background-color: rgba(255,255,255,0.2);
  margin: 0 10px 10px 0;
  text-align: center;
  line-height: 40px;
  border-radius: 50%;
  color: #fff;
  transition: all 0.5s ease;
}

.footer-col .social-links a:hover{
  color: #24262b;
  background-color: #fff;
}


@media screen and (min-width:768px) {
  .container {
    display: flex;
    flex-direction: row;
  }
  .footer-col {
  width: 25%;
  margin-bottom: none;
  }
}
    
    
    </style>