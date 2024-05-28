<!DOCTYPE html>  
<html>  
<head>  
  <link href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" rel="stylesheet">
<meta name="viewport" content="width=device-width, initial-scale=1">  
<style>  
body{  
  font-family: Calibri, Helvetica, sans-serif;  
  background-color: aliceblue;  
}  
.container {  
    padding: 50px;  
  background-color: lightblue;  
}  
  
input[type=text], input[type=password], textarea {  
  width: 100%;  
  padding: 15px;  
  margin: 5px 0 22px 0;  
  display: inline-block;  
  border: none;  
  background: #f1f1f1;  
}  
input[type=text]:focus, input[type=password]:focus {  
  background-color: orange;  
  outline: none;  
}  
 div {  
            padding: 10px 0;  
         }  
hr {  
  border: 1px solid #f1f1f1;  
  margin-bottom: 25px;  
}  
.registerbtn {  
  background-color: #4CAF50;  
  color: white;  
  padding: 16px 20px;  
  margin: 8px 0;  
  border: none;  
  cursor: pointer;  
  width: 100%;  
  opacity: 0.9;  
}  
.registerbtn:hover {  
  opacity: 1;  
}  
</style>  
</head>  
<body>  
<form>  
  <div class="container mt-5">
    <h2 class="text-center mb-4">TechVolution 2024 Registration</h2>
    <form id="registrationForm" class="needs-validation" novalidate>
        <!-- Personal Information -->
        <div class="form-group">
            <label for="name">Name</label>
            <input type="text" class="form-control" id="name" placeholder="Enter your name" required>
            <div class="invalid-feedback">Please enter your name.</div>
        </div>
        <div class="form-group">
            <label for="dob">Date of Birth</label>
            <input type="date" class="form-control" id="dob" required>
            <div class="invalid-feedback">Please enter your date of birth.</div>
        </div>
        <div class="form-group">
            <label>Gender</label><br>
            <div class="form-check form-check-inline">
                <input class="form-check-input" type="radio" name="gender" id="male" value="Male" required>
                <label class="form-check-label custom-radio-label" for="male">Male</label>
            </div>
            <div class="form-check form-check-inline">
                <input class="form-check-input" type="radio" name="gender" id="female" value="Female" required>
                <label class="form-check-label custom-radio-label" for="female">Female</label>
            </div>
            <div class="form-check form-check-inline">
                <input class="form-check-input" type="radio" name="gender" id="nonBinary" value="Non-binary" required>
                <label class="form-check-label custom-radio-label" for="nonBinary">Non-binary</label>
            </div>
            <div class="invalid-feedback">Please select your gender.</div>
        </div>
        <!-- Contact Details -->
        <div class="form-group">
            <label for="email">Email Address</label>
            <input type="email" class="form-control" id="email" placeholder="Enter your email" required>
            <div class="invalid-feedback">Please enter a valid email address.</div>
        </div>
        <div class="form-group">
            <label for="phone">Phone Number</label>
            <input type="text" class="form-control" id="phone" placeholder="Enter your phone number" required pattern="\d{10}">
            <div class="invalid-feedback">Please enter a valid phone number (10 digits).</div>
        </div>
        <!-- Address -->
        <div class="form-group">
            <label for="street">Street Address</label>
            <input type="text" class="form-control" id="street" placeholder="Enter your street address" required>
            <div class="invalid-feedback">Please enter your street address.</div>
        </div>
        <div class="form-group">
            <label for="city">City</label>
            <input type="text" class="form-control" id="city" placeholder="Enter your city" required>
            <div class="invalid-feedback">Please enter your city.</div>
        </div>
        <div class="form-group">
            <label for="state">State</label>
            <select class="form-control" id="state" required>
                <option value="">Select your state</option>
                <option value="CA">California</option>
                <option value="TX">Texas</option>
                <option value="NY">New York</option>
            </select>
            <div class="invalid-feedback">Please select your state.</div>
        </div>
        <div class="form-group">
            <label for="zip">Zip Code</label>
            <input type="text" class="form-control" id="zip" placeholder="Enter your zip code" required pattern="\d{5}">
            <div class="invalid-feedback">Please enter a valid zip code (5 digits).</div>
        </div>
        <!-- Additional Information -->
        <div class="form-group">
            <label for="preferences">Event Preferences</label>
            <select class="form-control" id="preferences"  required>
                <option value="workshops">Workshops</option>
                <option value="keynotes">Keynote Sessions</option>
                <option value="networking">Networking</option>
                <option value="exhibits">Exhibits</option>
            </select>
            <div class="invalid-feedback">Please select at least one preference.</div>
        </div>
        <div class="form-group">
            <label for="dietary">Dietary Restrictions</label>
            <textarea class="form-control" id="dietary" rows="3" placeholder="Enter any dietary restrictions"></textarea>
        </div>
        <div class="form-group">
            <label for="tshirt">T-shirt Size</label>
            <select class="form-control" id="tshirt" required>
                <option value="">Select your t-shirt size</option>
                <option value="S">Small</option>
                <option value="M">Medium</option>
                <option value="L">Large</option>
                <option value="XL">X-Large</option>
            </select>
            <div class="invalid-feedback">Please select your t-shirt size.</div>
        </div>
        <button type="submit" class="btn btn-primary">Register</button>
    </form>
</div>

<!-- Confirmation Modal -->
<div class="modal fade" id="confirmationModal" tabindex="-1" aria-labelledby="confirmationModalLabel" aria-hidden="true">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title" id="confirmationModalLabel">Registration Successful</h5>
                <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                    <span aria-hidden="true">&times;</span>
                </button>
            </div>
            <div class="modal-body">
                Thank you for registering for TechVolution 2024!
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
            </div>
        </div>
    </div>
</div>

<script src="https://code.jquery.com/jquery-3.5.1.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.5.4/dist/umd/popper.min.js"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
<script>
    // JavaScript for form validation
    (function() {
        'use strict';
        window.addEventListener('load', function() {
            var forms = document.getElementsByClassName('needs-validation');
            Array.prototype.filter.call(forms, function(form) {
                form.addEventListener('submit', function(event) {
                    if (form.checkValidity() === false) {
                        event.preventDefault();
                        event.stopPropagation();
                    } else {
                        event.preventDefault();
                        $('#confirmationModal').modal('show');
                        form.reset();
                        form.classList.remove('was-validated');
                    }
                    form.classList.add('was-validated');
                }, false);
            });
        }, false);
    })();
</script>
</body>
</html>

</form>  
</body>  
</html>  
