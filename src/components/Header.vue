<template>
 <header>
    <nav>

        <a href="#" class="nav-icon" aria-label="visit homepage" aria-current="page">
          <img src="@/assets/logo.png" alt="logo icon">
          <span>TrouveTaTeam</span>
        </a>
  
        <div class="main-navlinks">
          <div class="hamburger">
                <div class="block">
                  <div class="cta">
                    <div class="toggle-btn type16"></div>
                  </div>
                </div>
          </div>
          <!-- <button class="hamburger" type="button" aria-label="Toggle navigation" aria-expanded="false">
            <span></span>
            <span></span>
            <span></span>
          </button> -->
          <div class="navlinks-container">
            <a href="#" aria-current="page">Accueil</a>
            <a href="#">Parties</a>
            <a href="#">Jeux</a>
            <a href="#">Communautés</a>
            <a href="#">Contact</a>
          </div>
        </div>
  
        <div class="nav-authentication">
          <a href="#" class="sign-user" aria-label="Sign in page">
            <!-- <img src="ressources/user.svg" alt="user-icon"> -->
          </a>
          <div class="sign-btns">
            <button type="button">Connexion</button>
            <button type="button">S'inscrire</button>
          </div>
        </div>
      </nav>
    </header>

</template>

<script>

export default {
  name: 'Header',
  props: { 
    id: Number,
    titre:String,
    image:String,
  }
}
</script>


<style>
nav {
  position: relative;
  width: 100%;
  display: flex !important;
  flex-direction: row;
  align-items: center;
  background: linear-gradient(0deg, rgba(73,138,196,0.8) 0%, rgba(49,129,200,0.8) 50%, rgba(0,0,0,0.8995973389355743) 100%), url(../assets/background.jpg);
  box-shadow: inset 0px -1px 0px #c5c5c6;
  z-index: 1;
}

.nav-icon {
  display: flex;
  align-items: center;
  text-decoration: none;
  order: 2;
  margin: 0 auto;
}

.nav-icon span {
  font-family: Lato , sans-serif;
  font-size: 22px;
  margin-left: 10px;
  font-weight: 400;
  color: #333;
}

.nav-icon img {
  width: 40px;
}

.main-navlinks {
    order: 1;
}

.container {
  display: flex;
  justify-content: center;
}

.row {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap; 
  width: 5%;
}

.block {
  height: 60px;
  width: 60px;
  border-radius: 5px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 10px; 
  transition: all 1s ease;
 background-image: linear-gradient(0deg, rgba(242,148,0,1) 0%, rgba(226,93,5,1) 100%, rgba(0,0,0,0.8995973389355743) 100%);
 box-shadow: 0 2px 18px 0 rgba(248, 94, 122, 0.39), 0 1px 2px 0 rgba(248, 91, 124, 0.33);   
}

.cta {
  height: 50px;
  width: 50px;
  cursor: pointer; }

.toggle-btn {
  height: 2px;
  width: 25px;
  background-color: #fff;
  position: relative;
  top: 50%;
  left: 0;
  margin: auto;
  transition: all 0.3s ease-in-out; }
  .toggle-btn:before {
    content: "";
    height: 2px;
    width: 25px;
    box-shadow: 0 -10px 0 0 #fff;
    position: absolute;
    top: 0;
    left: 0;
    transition: all 0.3s ease-in-out; }
  .toggle-btn:after {
    content: "";
    height: 2px;
    width: 25px;
    box-shadow: 0 10px 0 0 #fff;
    position: absolute;
    top: 0;
    left: 0;
    transition: all 0.3s ease-in-out; }

    .active .toggle-btn {
      background-color: transparent;
      transition: all 0.2s ease-in-out; }
      .active .toggle-btn:before {
        top: 0;
        transition: all 0.3s ease-in-out; }
      .active .toggle-btn:after {
        top: 0;
        transition: all 0.3s ease-in-out; }

.active .type16 {
transform: rotate(360deg);
transition: all 0.6s ease-in-out; }
.active .type16:before {
  left: 6px;
  transform: translateY(6px) rotate(-45deg); }
.active .type16:after {
  left: 6px;
  transform: translateY(-8px) rotate(45deg); }

  .navlinks-container {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    position: absolute;
    background: #fafafa;
    top: 100%;
    left: 0;
    height: 100vh;
    padding: 15px 50px 15px 20px;
    border-right: 1px solid #c5c5c6;
    transform: translate(-100%);
  }
  .open {
    transform: translate(0%);
  }

.navlinks-container a {
  margin:10px 0; 
  font-size: 18px;
  font-weight: 500;
  text-decoration: none !important;
  color: #414141;
  display: inline-block;
  position: relative;
}

.navlinks-container a:hover {
  color: #1e272e;
}
.navlinks-container a::after {
  content: "";
  display: block;
  position: absolute;
  bottom: -3px;
  width: 100%;
  height: 1px;
  transform: scaleX(0);
  transform-origin: left;
  background: #333;
  transition: transform 0.3s ease-out;
}

.navlinks-container a:hover::after {
  transform: scaleX(1)
}

.nav-authentication {
    order: 3;
  margin-left: 0;
}

.sign-btns {
    display: none;
  }

.sign-user {
    display: block;
    cursor: pointer;
    border: none;
}


@media screen and (min-width:901px) {
    nav {
        padding: 15px 25px;
        display: flex !important;
         
      }
    
      .nav-icon {
        order: 1;
        margin: unset;
        margin-right: 20px;
      }
    
      .nav-icon span {
        font-size: 25px;
      }
      
      .nav-icon img {
        width: 40px;
      }
      
      .hamburger {
        display: none;
      }

      .navlinks-container { 
        display: unset;
        flex-direction: unset;
        align-items: unset;
        position: unset;
        background: unset;
        top: unset;
        left: unset;
        height: unset;
        padding: unset;
        border-right: unset;
        transform: 100%;
      }

      .navlinks-container a {
        font-size: 16px;
        margin: 0 10px 
      }
    
      .nav-authentication {
        margin-left: auto;
      }
      .sign-btns {
        display: block;
      }
      .sign-btns button {
        font-family: Lato , sans-serif;
        font-size: 16px;
        min-width: 90px;
        padding: 10px 5px;
        margin: 0 5px;
        border-radius: 5px;
        cursor: pointer;
        border: none; 
        }

        .sign-btns button:nth-child(2) {
        border: none;
        background: rgb(242,148,0);
        background: linear-gradient(0deg, rgba(242,148,0,1) 0%, rgba(226,93,5,1) 100%, rgba(0,0,0,0.8995973389355743) 100%);
        }
      .sign-user {
        display: none;
      }
    
}



</style>


