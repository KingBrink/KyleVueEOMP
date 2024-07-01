<template>
    <nav class="navbar navbar-expand-lg sticky-top">
            <div class="container-fluid">
                <router-link class="navbar-brand" to="/"><img class="img-fluid w"
                        src="https://kingbrink.github.io/all-images/images/logo.png" alt="logo"></router-link>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
                    data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false"
                    aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                    <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
                        <li class="nav-item">
                            <router-link class="nav-link" aria-current="page" to="/">Home</router-link>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" aria-current="page" href="#about">About</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" aria-current="page" href="#resume">Resume</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" aria-current="page" href="#testimonials">Testimonials</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" aria-current="page" href="#projects">Projects</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" aria-current="page" href="#contact">Contact Me</a>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
    </template>
    <style  scoped>
    
    .logo{
      background-color: white;
      width: 80px;
      height: 40px;
    }
    
    .title{
      font-weight: 600;
    }
    
    .navigation{
        background: #fff;
        color: #000;
        mix-blend-mode: difference;
    }
    
    .navigation.black{
      background: rgb(0, 0, 0);
    }
    .nav-link {
      color: black;
      font-weight: 500;
    }
    
    .nav-link:hover{
      opacity: 80%;
    }
    
    .navbar-dark .navbar-nav .nav-link {
      font-size: 18px;
        color: rgba(255,255,255);
    }
    
    .navbar-dark .navbar-nav .nav-link:hover {
        color: rgba(255, 255, 255, 0.468);
    }
    .navigation2{
      display: none;
    }
    
    .offcanvas{
      text-align: left;
      background: black;
      opacity: 90%;
      max-width: 70vw;
    }
    .footer-bar a{
      font-size: 25px;
      margin: 3px;
    }
    .footer-bar a i{
        color: rgb(255, 255, 255) !important;
    }
    .footer-bar a i:hover{
        color: rgba(255, 255, 255, 0.721) !important;
    }
    
    @media screen and (width < 1000px) {
    .navigation{
      display: none;
    }
    
    .navigation2{
      display: block;
    }
    
    .nav-link:hover{
      opacity: 80%;
    }
    }
    </style>