# REGISTRATION
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>REGISTRATION FORM</title>
  

    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
    <style>
        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            background-image: url('7.jpg');
        }

        .form {
            width: 100%;
            max-width: 450px;
            background-color: lightblue;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 15px black;
        }

        .form .button {
            width: 100%;
            
        }
       
    </style>
</head>

<body>
    <section class="container">

        <form class="form" onsubmit="signup(event)">
            <header class="text-center">
                <h1>Book a call</h1>
            </header>
            <p class="text-center">Book a call slot and our representative will call you within 1 hour of the selected time.</p>
            <hr>

            <label for="name">Name:</label>
            <input type="text" id="name" name="name" class="form-control">

            <label for="mail">Email:</label>
            <input type="text" id="mail" name="mail" class="form-control">

            <label for="phone">Phone:</label>
            <input type="text" id="phone" name="phone" class="form-control">

            <label for="datetime">Date and Time for Call:</label>

            <div class="row">
                <div class="col">
                    <input type="date" id="date" class="form-control">
                </div>
                <div class="col">
                    <input type="time" id="time" class="form-control">
                </div>
            </div>

            <button type="submit" class="btn btn-primary mt-3" onclick="handleClick()" onmouseover="handleMouseOver()" onmouseout="handleMouseOut()">GET A CALL</button>

        </form>
    </section>


<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>

<script src="path/to/bootstrap.min.js"></script>
   

<script>
    function handleClick() {
        console.log("Button clicked");
    }

    function handleMouseOver() {
        console.log("Mouse over");
    }

    function handleMouseOut() {
        console.log("Mouse out");
    }

    function signup(event) {
        event.preventDefault(); // Prevent form submission

        // Get form input values
        var name = document.getElementById('name').value;
        var email = document.getElementById('mail').value;
        var phone = document.getElementById('phone').value;
        var date = document.getElementById('date').value;
        var time = document.getElementById('time').value;

        // Form validation
        if (name === '' || email === '' || phone === '' || date === '' || time === '') {
            alert('Please fill in all fields.');
            return;
        }

        // Log form values to console
        console.log("Name: " + name);
        console.log("Email: " + email);
        console.log("Phone: " + phone);
        console.log("Date: " + date);
        console.log("Time: " + time);

        // Reset form fields
        document.getElementById('name').value = '';
        document.getElementById('mail').value = '';
        document.getElementById('phone').value = '';
        document.getElementById('date').value = '';
        document.getElementById('time').value = '';
    }
</script>
</body>

</html>
