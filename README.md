# Sign-In-Form

<!DOCTYPE html>
<html lang="en">

<head>
    <!-- cssStartsHere -->
    <style>
        * {
            margin: 0;
            padding: 0;
            font-family: 'poppins', sans-serif;
            box-sizing: border-box;
        }


        .container {
            width: 100vh;
            height: 100vh;
            background-image: linear-gradient(rgba(32, 31, 31, 0.8), rgba(102, 102, 104, 0.8)), url(benches2.jpg);
            background-position: center;
            background-size: contain;
            position: relative;
            background-repeat: repeat-x;
        }

        .form-box {

            height: 50%;
            max-width: 450px;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: #fff;
            padding: 50px 60px 70px;
            text-align: center;
        }

        .form-box h1 {
            padding-top: initial;
            padding-bottom: initial;
            bottom: 50px;
            font-size: 40px;
            margin-bottom: 60px;
            color: rgb(159, 208, 210);
            position: relative;
        }

        .form-box h1::after {
            content: '';
            width: 40px;
            height: 4px;
            border-radius: 3px;
            background: rgb(159, 208, 210);
            position: absolute;
            bottom: -12px;
            left: 50%;
            transform: translatex(-50%)
        }



        .input-field {
            background: #eaeaea;
            margin: 15px 0;
            border-radius: 3px;
            display: flex;
            align-items: center;
            position: relative;
            max-height: 65px;
            transition: max-height 0.5s;
            overflow: hidden;
        }

        input {
            position: relative;
            width: 100%;
            background: transparent;
            border: 0;
            outline: 0;
            padding: 18px 15px;
        }

        .input-field i {
            margin-left: 15px;
            color: #999;
        }

        .input-group {
            padding-top: initial;
            padding-bottom: initial;
            bottom: 70px;
        }
    </style>

    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Sign In & Sign Up Form</title>
    <!-- <link rel="stylesheet" href="sign.css"> -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
    <!-- <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet"
    integrity="sha384-4bw+/aepP/YC94hEpVNVgiZdgIC5+VKNBQNGCHeKRQN+PtmoHDEXuppvnDJzQIu9" crossorigin="anonymous"> -->
</head>

<body>
    <div class="container"></div>
    <div class="form-box">
        <h1 id="title">Sign Up</h1>
        <form>
            <div class="input-group">
                <div class="input-field">
                    <i class="glyphicon glyphicon-user"></i>
                    <input type="text" placeholder="Username">
                </div>

                <div class="input-field">
                    <i class="glyphicon glyphicon-pencil"></i>
                    <input type="password" placeholder="Password">
                </div>

                <div class="input-field" id="cpasswrd">
                    <i class="glyphicon glyphicon-ok"></i>
                    <input type="password" placeholder="Confirm password">
                </div>

                <!-- <div class="col-md-12 text-center">
                    <button type="submit" class="btn btn-primary">Accept</button>
                </div>

                <div class="col-md-12 text-center">
                    <button type="submit" class="btn btn-primary">Sign In</button>
                </div> -->

                <div class="btn-field">

                    <button type="button" class="btn btn-primary" id="SignInbtn">Sign in</button>
                    <button type="button" class="btn btn-primary" id="Acceptbtn">Accept</button>
                </div>
            </div>
        </form>
    </div>
    <script>

        let SignInbtn = document.getElementById("SignInbtn");
        let Acceptbtn = document.getElementById("Acceptbtn");
        let cpasswrd = document.getElementById("cpasswrd");
        let title = document.getElementById("title");

        SignInbtn.onclick = function () {
            cpasswrd.style.maxHeight = "0";
            title.innerHTML = "Sign In";
            SignInbtn.classList.add("disable");
            SignInbtn.classList.remove("disable");

            


        }
    </script>
</body>

</html>
