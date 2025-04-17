<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Portfolio Website Design</title>
    <link rel="stylesheet" href="style.css">
    <!----Font awesome cdn  font icon css -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.2.1/css/all.min.css">
</head>
<body>
     <div class="hero-header">
        <div class="wrapper">
            <header>
                <div class="logo">
                    <i class="fa-solid fa-a"></i>
                    <div class="logo-text">Sander Haugli</div>
                </div>
                <nav>
                    <div class="togglebtn">
                        <span></span>
                        <span></span>
                        <span></span>
                    </div>
                    <ul class="navlinks">
                        <li><a href="#">Home</a></li>
                        <li><a href="#">Portfolio</a></li>
                        <li><a href="#">Resume</a></li>
                        <li><a href="#">Blog</a></li>
                        <li><a href="#">Contact</a></li>
                    </ul>
                </nav>
            </header>
            <div class="container">
                 <div class="hero-pic">
                    <img src="images/main_photo.jpg" alt="profile pic">
                 </div>
                 <div class="hero-text">
                    <h5>Hi I'm a <span class="input">Frontend Developer</span></h5>
                    <h1>Sander Haugli</h1>
                    <p> Hi! i'm a it security and networking student from Norway,<br>while i study this lecture i also take back and front end degrees on my sparetime
                    </p>

                    <div class="btn-group">
                       <a href="#" class="btn active">Download CV</a>
                       <a href="#" class="btn">Contact</a>
                    </div>

                    <div class="social">
                        <a href="#"><i class="fa-brands fa-facebook"></i></a>
                        <a href="#"><i class="fa-brands fa-linkedin"></i></a>
                        <a href="#"><i class="fa-brands fa-instagram"></i></a>
                        <a href="#"><i class="fa-brands fa-dribbble"></i></a>
                        <a href="#"><i class="fa-brands fa-pintrest"></i></a>
                    </div>
                 </div>
            </div>
        </div>
     </div>
     <!---typed js for typing text effect-->
     <script src="https://cdnjs.cloudflare.com/ajax/libs/typed.js/2.0.10/typed.min.js"></script>
     <script>
        /** creating button click show hide navbar **/
        var togglebtn=document.querySelector(".togglebtn");
        var nav=document.querySelector(".navlinks");
        var links=document.querySelector(".navlinks li");

        togglebtn.addEventListener("click", function(){
            this.classList.toggle("click");
            nav.classList.toggle("open");
        })

        var typed=new Typed(".input",{
            strings:["Frontend Developer","IT Security","Web Developer"],
            typedSpeed:70,
            backSpeed:55,
            loop:true
        })
     </script>
</body>
</html>


*{
  box-sizing: border-box;
  padding: 0;
  margin: 0;
  font-family: poppins,sans-serif;
  text-decoration: none;
}
body{
  overflow-x: hidden;
}
.hero-header{
  width:100%;
  height: 100%;
  min-height: 100vh;
  background: #222;
}
.wrapper{
  width:1280px;
  max-width: 95%;
  margin: 0 auto;
  padding: 0 20px;
}
header{
  padding: 40px 0 30px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}
.logo{
  display: inline-flex;
  justify-content: center;
  align-items: center;
}
.logo i{
  height: 45px;
  width:45px;
  background-color: #007ced;
  border-radius: 50%;
  color:#fff;
  font-weight: 700;
  font-size: 1.5rem;
  padding: 10px;
  margin-right: 5px;
  cursor: pointer;
  text-align: center;
  
}
.logo .logo-text{
  font-size: 24px;
  font-weight: 500;
  color:#fff;
}
nav .togglebtn{
  width: 35px;
  height: 35px;
  position: absolute;
  top:45px;
  right: 3%;
  z-index: 5;
  cursor: pointer;
  display: none;
}
nav .togglebtn span{
  display: block;
  background-color: #007ced;
  margin: 5px 0px;
  width:100%;
  height:3px;
  transition: 0.3s;
  transition-property:  transform, opacity;

}
nav .navlinks{
  list-style-type: none;
}
nav .navlinks li{
  display: inline-block;
}
nav .navlinks li a{
   color:#e5e5e5;
   margin-right: 2.5rem;
}
.container {
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding-top:4rem;
}
.container .hero-pic{
  width: 300px;
  height: 300px;
  border-radius: 50%;
  overflow: hidden;
  border: 15px solid #444;
  box-shadow: 5px 7px 25px rgba(0,0,0,0.5);
}
.hero-pic img{
  height: 100%;
  width:100%;
  transition: 0.5s;
}
.hero-pic img:hover{
  transform: scale(1.2);
}
.hero-text{
  max-width: 500px;
  display: flex;
  flex-direction: column;
}
.hero-text h5{
  color:#e5e5e5;
  font-size: 14px;
}
.hero-text h5 span{
  color:#007ced;
  font-size: 16px;
}
.hero-text h1{
  color: #007ced;
  font-size: 3rem;
}
.hero-text p{
  color:#e5e5e5;

}
.btn-group{
  margin:45px 0;
}
.btn-group .btn{
  border-color: #d5d5d5;
  color:#fff;
  background-color: #333;
  padding: 12px 25px;
  margin: 5px 0px;
  margin-right:7px;
  border-radius: 30px;
  border:2px solid #e5e5e5;
  box-shadow:  0 10px 10px -8px rgb(0 0 0 / 78%);
}
.btn.active{
  border-color: #007ced;
}
.hero-text .social i{
  color: #e5e5e5;
  font-size: 18px;
  margin-right: 10px;
  transition: 0.5s;
}
.hero-text .social i:hover{
  color:#007ced;
  transform: rotate(360deg);
}
/* Respnosiv design & displaying navbar for small screen */
@media(max-width:930px)
{
  nav .togglebtn{
      display: initial;
  }
  /* for toggle button**/
  .click {
      top:45px;
  }
  .click span{
      position: absolute;
      margin-top:12px
  }
  .click span:first-child{
      transform: rotate(-40deg);
  }
  .click span:nth-child(2)
  {
      opacity: 0;
      margin:0;
  }
  .click span:last-child{
      transform: rotate(45deg);
      top:0;
  }
  nav .navlinks{
      position: absolute;
      top:110px;
      right:-100%;
      bottom: 0;
      width: 60%;
      height: 100vh;
      background-color: #222;
      z-index: 3;
      box-shadow: 5px 13px 30px rgba(0,0,0,0.1);
      transition: 0.5s;
      padding: 25px 0px;
  }
  nav .navlinks li{
      display: block;
  }
  nav .navlinks li a{
      display: block;
      margin-bottom: 15px;
      text-align: center;
  }
  nav .navlinks.open{
      right:0;
  }
}
@media(max-width:768px)
{
  .container{
      flex-direction: column;
      padding-top:2rem
  }
  .hero-text{
      padding:40px 0px;
  }
}
