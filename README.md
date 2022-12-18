<html>

<head>
    <script>
        function GEEKFORGEEKS() {
            var name =
                document.forms.RegForm.Name.value;
            var email =
                document.forms.RegForm.EMail.value;
            var phone =
                document.forms.RegForm.Telephone.value;
            var what =
                document.forms.RegForm.Subject.value;
            var password =
                document.forms.RegForm.Password.value;
            var address =
                document.forms.RegForm.Address.value;
            var regEmail = /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/g;
            var regPhone = /^\d{10}$/;
            var regName = /\d+$/g;

            if (name == "" || regName.test(name)) {
                window.alert("Please enter your name properly.");
                name.focus();
                return false;
            }

            if (address == "") {
                window.alert("Please enter your address.");
                address.focus();
                return false;
            }

            if (email == "" || !regEmail.test(email)) {
                window.alert("Please enter a valid e-mail address.");
                email.focus();
                return false;
            }

            if (password == "") {
                alert("Please enter your password");
                password.focus();
                return false;
            }

            if (password.length < 6) {
                alert("Password should be atleast 6 character long");
                password.focus();
                return false;

            }
            if (phone == "" || !regPhone.test(phone)) {
                alert("Please enter valid phone number.");
                phone.focus();
                return false;
            }

            if (what.selectedIndex == -1) {
                alert("Please enter your course.");
                what.focus();
                return false;
            }

            return true;
        }
    </script>

    <style>
        div {
            box-sizing: border-box;
            width: 100%;
            border: 100px solid black;
            float: left;
            align-content: center;
            align-items: center;

        }

        .box {
            display: flex;
            align-items: center;
            justify-content: center;
          }
          
          .box div {
            width: 100px;
            height: 100px;
          }


        form {
            margin: 0 auto;
            width: 600px;
            font-weight: bold;
            font-size: 25px;
            color: rgb(11, 11, 11);
            text-align: center;
            height: 100%;
            width: 100%;
            justify-content: center;
        }

        body {
            background-image: url(1.webp);
            background-repeat: no-repeat;
            background-position: center;
            padding-top: 5%;
            height: 100%;
            width: 100%;

        }
    </style>
</head>

<body>
    <h1 style="text-align: center;"> NEW REGISTRATION FORM</h1>
    <form name="RegForm" onsubmit="return GEEKFORGEEKS()" method="post">

        <p><label for="">Name : </label>      
        <input type="text" size="65" name="Name" /></p>

        <br />

        <p>Address: <input type="text" size="65" name="Address" /></p>
        <br />

        <p>E-mail : <input type="text" size="65" name="EMail" /></p>
        <br />

        <p>Password: <input type="text" size="65" name="Password" /></p>
        <br />

        <p>Telephone: <input type="text" size="65" name="Telephone" /></p>
        <br />


        <p>
            <label for="">SELECT YOUR COURSE</label>
            <select type="text" value="" name="Subject">
                <option>BTECH</option>
                <option>BBA</option>
                <option>BCA</option>
                <option>B.COM</option>
                <option>GEEKFORGEEKS</option>
            </select>
        </p>

        <br />
        <br />

        <p>Comments: </p><textarea cols="55" rows="15" name="Comment"> </textarea>


        <p>
            <input type="submit" value="send" name="Submit" />
            <input type="reset" value="Reset" name="Reset" />
        </p>

    </form>
</body>

</html>
