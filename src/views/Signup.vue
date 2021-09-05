<template>
    <div class="signup">
        <!-- Start Sign Up Page -->
        <div class="login">
            <div class="container-fluid">
                <div class="row">
                    <!-- Start Info -->
                    <div class="col-md-6 read log">
                        <h2>SIGNUP FORM</h2>
                        <h4>Giphy Web App.</h4>
                        <p>Please Create an account to use our gif.</p>
                        <br>
                        <h4>Sign Up With</h4>
                        <!-- Start Social Medial Links -->
                        <div class="social">
                            <i class="fab fa-twitter"></i>
                            <i class="fab fa-youtube"></i>
                            <i class="fab fa-instagram"></i>
                            <i class="fab fa-google"></i>
                            <i class="fa fa-rss"></i>
                            <i class="fab fa-facebook"></i>
                        </div>
                        <!-- End Social Medial Links -->
                        <br>
                        <h5>already have an account <span><router-link to="/signin" tag="li">Sign In</router-link></span></h5><br><br>
                    </div>
                    <!-- End Info -->
                    <div class="col-md-6 form log">
                        <h3>SIGNUP FORM</h3>
                        <!-- Start Form -->
                        <form action="#" method="Post">
                            <div class="error-list"></div>
                            <input class="form-control" type="text" name="fname" id="" placeholder="First Name" autocomplete="off">
                            <input class="form-control" type="text" name="lname" id="" placeholder="Last Name">
                            <input class="form-control" type="text" name="email" id="" placeholder="Email">
                            <input class="form-control" type="text" name="pass" id="" placeholder="Password">
                            <input class="form-control" type="text" name="cpass" id="" placeholder="Confirm Password">
                            <input type="submit" class="btn" value="SIGNUP">
                        </form>
                        <!-- End Form -->
                    </div>
                </div>
            </div>
        </div>
        <!-- End Sign Up Page -->
    </div>
</template>

<script>
export default {
  name: "signup",
  components: {
  },
};
</script>

<style lang="scss" scoped>
.login{
    width: 85%;
    height: 500px;
    margin: 20px auto;
    margin-bottom:50px  !important;

    .log{
        padding: 40px;

        .social i {
            cursor: pointer;
            padding: 15px;
            font-size: 18px;
            margin: 1px;
            border: 2px solid #1345e6;
        }
        .social i:hover {
            transition: .5s;
            background: #1345e6;
            color: #fff;
        }
    }
    .read{
        color: #000000;
        background-color: #ffffff;
        text-align: center;

        h4{
            margin: 25px 0 ;
        }

        span{
            color: #1345e6;
            cursor: pointer;
        }
    }

  p {
    line-height: 30px;
  }

  .form {
    color: #fff;
        background-color: rgba(0, 0, 0, 0.664);

        .form-control{
            background: none;
            border: 2px solid #fff;
        }
        
        input {
      padding: 10px 35px;
            margin-top: 15px;
            font-size: 16px;
            border-radius: 0;
            color: #fff
        }

        .btn{
            background: linear-gradient(to right, #1345e6 0%, #ed239f 51%, #1345e6 100%);
            border: 1px solid #1345e6;
        }
    }
}

@media(max-width:767px){
    .login{
        width: 95%;
    }
}
</style>
