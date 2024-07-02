<template>
  <section class="container-fluid mt-4">
     <div class="row">
       <h1 class="headmain">
         Contact Me
       </h1>
     </div>
     <div class="contact" id="contact">
       <div class="row">
         <div class="contactsec container" id="Contact">
           <form action="https://formspree.io/f/xleqzzyb" method="POST" class="form" id="myForm" style="padding-bottom: 7%;" >
             <div class="row justify-content-center">
               <div class="col-5">
                 <input type="text" class="form-control" name="name" placeholder="First name" aria-label="First name" required>
               </div>
               <div class="col-5">
                 <input type="text" class="form-control" name="lastname" placeholder="Last name" aria-label="Last name" required>
               </div>
             </div>
             <div class="row justify-content-center">
               <div class="col-10 mb-3">
                 <label for="exampleInputEmail1" class="form-label"></label>
                 <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" name="email" placeholder="Your Email" required>
                 <div id="emailHelp" class="form-text"></div>
               </div>

               <div class="col-10 mb-3">
                 <label for="exampleFormControlTextarea1" class="form-label"></label>
                 <textarea class="form-control" id="exampleFormControlTextarea1" rows="5" name="message"
                   placeholder="Enter Message Here" required></textarea>
               </div>
             </div>
             <div class="mx-5">
               <button type="submit" class="btn subButton" name="submit">Submit</button>
               <button type="button" id="clearButton" class="btn" @click.prevent="clearForm()">Clear</button>
             </div>

             <div class="deats row mx-2 cinfo">
               <div class="">
                 <a href="mailto:kyle.brink1602@gmail.com" class="my-3 mail " style="font-size:15px;" mail><i
                     class="fa fa-envelope"></i>kyle.brink1602@gmail.com</a>
               </div>
               <div class="col-12">
                 <text class="" style="font-size:15px;"><i class="fa fa-phone"></i> +27 67 404 6393</text>
               </div>
             </div>
           </form>

         </div>
       </div>
     </div>
   </section>
</template>

<script>
export default{
   data(){
       return {
           
       }
   },
   methods:{

       // Function to clear the form fields
       clearForm() {
         document.getElementById("myForm").reset();
       }
   }
}



</script>

<style>
/* Contact details styles */
.deats {
   margin-top: 20px;
}

.deats a, .deats text {
   margin-bottom: 10px;
   color: blue;
   font: bold;
   font-size: 20px;
}

/* Font Awesome icon styles */
.fa {
   margin-right: 5px;
}

.icons a {
   padding: 0;
   font-size: 20px;
   color: #ff0157;
}

.img-thumbnail{
   max-width: 25vw;
   max-height: 25vh;
}

.products{
   justify-content: center;
   align-items: center;
}

.prodCard{
   height: 550px;
}

.homeCard{
   text-align: center;
}

.btn-grp{
   justify-content: center;
   align-items: center;
}

.contact-details {
   display: flex;
   flex-direction: column;
}

.email-link,
.phone-number {
   margin: 5px; 
   display: flex;
   justify-content: center;
   align-items: center;
}


.footer-bar {
   display: flex;
   justify-content: center;
   align-items: center;
}

.social-icons {
   display: flex;
   justify-content: space-between;
   width: 120px; 
}

.social-icons a {
   text-decoration: none;
   color: inherit;
}

.social-icons i {
   font-size: 24px; /* Adjust icon size as needed */
}
@media (min-width:300px) and (max-width:500px) {
  .cinfo{
    font-size: 5px;
  }
}
</style>