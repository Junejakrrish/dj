

DigitalOcean and AWS (Amazon Web Services) are both cloud computing platforms that offer a variety of services to help individuals and businesses deploy, manage, and scale applications and websites. Droplets are a specific product of DigitalOcean, and they are comparable to instances or virtual machines on AWS.
DigitalOcean:
.
Droplets:
.
.DigitalOcean's virtual private servers are called "Droplets." They are scalable, on-demand compute platforms that allow you to deploy and manage applications in the cloud.
.Droplets come in various sizes and configurations, allowing you to choose the resources that best fit your needs.
.Commonly used for hosting websites, applications, and development environments.
.
Other Services:
.
.DigitalOcean provides additional services like managed databases, object storage (Spaces), networking solutions (Load Balancers), and monitoring tools.
.
Developer-Friendly:
.
.Known for its simplicity and user-friendly interface, making it accessible for developers and startups.
.Offers straightforward pricing with predictable costs.
AWS (Amazon Web Services):
.
EC2 Instances:
.
.AWS Elastic Compute Cloud (EC2) provides scalable virtual servers, allowing users to run applications and workloads in the cloud.
.Offers a wide range of instance types to cater to different performance and resource requirements.
.
Extensive Service Portfolio:
.
.AWS has a vast portfolio of services beyond compute, including storage (S3), databases (RDS), machine learning (SageMaker), serverless computing (Lambda), and more.
.Provides services for virtually every aspect of cloud computing.
.
Enterprise-Grade:
.
.AWS is often used by large enterprises due to its comprehensive feature set and the ability to handle complex and large-scale applications.
Uses:
.
DigitalOcean:
.
.Well-suited for startups, small to medium-sized businesses, and individual developers.
.Great for projects that require simplicity, ease of use, and predictable pricing.
.Commonly used for web hosting, application deployment, and development environments.
.
AWS:
.
.Ideal for enterprises and large organizations with diverse and complex computing needs.
.Suitable for a wide range of use cases, from hosting simple websites to running sophisticated machine learning models and big data analytics.
.Offers a vast ecosystem of services, making it versatile for various applications.
In summary, DigitalOcean and AWS cater to different audiences and use cases. DigitalOcean is often favored for its simplicity and ease of use, while AWS provides an extensive set of services suitable for large-scale enterprise applications. The choice between them depends on factors such as project requirements, scale, and the complexity of the application architecture.




<!DOCTYPE html>
<html>
<head>
    <title>Form Validation</title>
    <script type="text/javascript">
        // Function to validate the form
        function validateForm() {
            var firstName = document.forms["myForm"]["first_name"].value;
            var lastName = document.forms["myForm"]["last_name"].value;
            
            if (firstName === "") {
                alert("First name must not be blank");
                return false;
            }

            if (!isTextOnly(firstName)) {
                alert("First name must contain only letters");
                return false;
            }
            
            if (lastName === "") {
                alert("Last name must not be blank");
                return false;
            }

            if (!isTextOnly(lastName)) {
                alert("Last name must contain only letters");
                return false;
            }
            else{
                alert("SUBMITTED");
            }
        }

        // Function to check if a string contains only letters (text)
        function isTextOnly(input) {
            var textPattern = /^[a-zA-Z]+$/;
            return textPattern.test(input);
        }
    </script>
</head>
<body>
    <form name="myForm" onsubmit="return validateForm()" method="post">
        First name: <input type="text" name="first_name"><br>
        Last name: <input type="text" name="last_name"><br>
        <input type="submit" value="Submit">
    </form>
</body>
</html>



<!DOCTYPE html>
<html>
<head>
<title>Form Validation</title>
<script type="text/javascript">

//Function to validate the form

function validateForm() {
var firstName = document.forms["myForm"]["first_name"].value;
var rolln = document.forms["myForm"]["rn"].value;
var email = document.forms["myForm"]["email"].value;

// Validate first name
if (firstName == "") {
  alert("First name must not be blank");
  return false;
}

// Validate roll number
if (!/^\d+$/.test(rolln)) {
  alert("Roll number must contain only numbers");
  return false;
}

// Validate email
var emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
if (!emailRegex.test(email)) {
  alert("Email is not valid");
  return false;
}

// If all validations pass, submit the form
alert("Form submitted");
return true;
}

// Function to check if a string contains only letters (text)
function isTextOnly(input) {
var textPattern = /^[a-zA-Z]+$/;
return textPattern.test(input);
}
</script>
</head>
<body>
<form name="myForm" onsubmit="return validateForm()" method="post">
<br>
First name: <br><input type="text" name="first_name" placeholder="John"><br>
<br>
Roll.No. <br><input type="text" name="rn" placeholder="Doe"><br>
<br>
Email: <input type="email" name="email" placeholder="ss@gmail.com"><br><br>
<input type="submit" value="Submit">
</form>
</body>
</html>



# button

<!DOCTYPE html>
<html>
<head>
<script>
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
</script>
</head>
<body>
<h2>Demo JavaScript in Head</h2>

<p id="demo">A Paragraph</p>
<button type="button" onclick="myFunction()">Try it</button>
</body>
</html>

# date

<!DOCTYPE html>
<html>
<body>

<h1>JavaScript Dates</h1>
<h2>Using new Date()</h2>

<p id="demo"></p>

<script>
const d = new Date("2022-03-25");
document.getElementById("demo").innerHTML = d;
</script>

</body>
</html>

<!DOCTYPE html>
<html>
<body>

<h1>JavaScript Dates</h1>
<h2>The getFullYear() Method</h2>
<p>Return the full year of a date object:</p>

<p id="demo"></p>

<script>
const d = new Date();
document.getElementById("demo").innerHTML = d.getFullYear();
</script>

</body>
</html>



<!DOCTYPE html>
<html>
<body>
<h1>JavaScript Dates</h1>
<h2>JavaScript getMonth()</h2>
<p>Return the month as a number.</p>
<p>You can use an array of names to return the month as a name:</p>

<p id="demo"></p>

<script>
const months = ["January","February","March","April","May","June","July","August","September","October","November","December"];

const d = new Date();
let month = months[d.getMonth()];
document.getElementById("demo").innerHTML = month;
</script>

</body>
</html>



setDate() Set the day as a number (1-31)
setFullYear() Set the year (optionally month and day)
setHours() Set the hour (0-23)
setMilliseconds() Set the milliseconds (0-999)
setMinutes() Set the minutes (0-59)
setMonth() Set the month (0-11)
setSeconds() Set the seconds (0-59)
setTime()

# for promise

!DOCTYPE html>
<html>
<body>

<h1>JavaScript Functions</h1>

<p>Call a function which performs a calculation and returns the result:</p>

<p id="demo"></p>

<script>
let x = myFunction(4, 3);
document.getElementById("demo").innerHTML = x;

function myFunction(a, b) {
  return a * b;
}
</script>

</body>
</html>
