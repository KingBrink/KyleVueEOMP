<template>
  <nav class="navbar fixed-top mr-4">
    <div class="container">
      <router-link class="navbar-brand" to="/">
        <img class="img-fluid w" src="https://kingbrink.github.io/all-images/images/logo.png" alt="logo">
      </router-link>
      <button class="navbar-toggler" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasNavbar"
        aria-controls="offcanvasNavbar" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="offcanvas offcanvas-end" tabindex="-1" id="offcanvasNavbar" aria-labelledby="offcanvasNavbarLabel">
        <div class="offcanvas-header">
          <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close"></button>
        </div>
        <div class="offcanvas-body">
          <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <router-link class="nav-link" aria-current="page" to="/">Home</router-link>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#about">About</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#resume">Resume</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#testimonials">Testimonials</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#projects">Projects</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#contact">Contact Me</a>
            </li>
          </ul>
        </div>
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
  
  .navbar{
      background-color: #0F4C75;
      /* mix-blend-mode: difference; */
  }
  
  .navigation.black{
    background: rgb(255, 255, 255);
  }
  .nav-link {
    color: black;
    font-weight: 500;
  }
  
  .nav-link:hover{
    opacity: 80%;
  color: blue;
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
    background: #f8f8f8;
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
  
  