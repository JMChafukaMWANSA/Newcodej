# Newcodej
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>Contact form To Email Using JavaScript</title>
	<link rel="stylesheet" href="christiner.css">
</head>
<body>
	<div class="container">
		<form onsubmit="sendEmail(); reset(); return false;">
			<h3>GET IN TOUCH</h3>

			<input type="text" id="name" placeholder="Your Name" required>
			<input type="text" id="email" placeholder="Email id" required>
			<input type="text" id="phone no" placeholder="Phone No" required>
			<input type="text" id="province" placeholder="Province" required>
			<input type="text" id="Developed by james" placeholder="Developed by james" required>
			<textarea id="message" rows="4" placeholder="How can we help you?"></textarea>
			<button type="submit">send</button>
		</form>
	</div>
	<script src="https://smtpjs.com/v3/smtp.js"></script>
	<script>
		function sendEmail(){
			Email.send({
    Host : "smtp.gmail.com",
    Username : "mwajames185@gmail.com",
    Password : "Mwansa19",
    To : 'andrewgama987@gmail.com',
    From : document.getElementById("email").value,
    Subject : "New contact form Enquiry",
    Body : "And this is the body"
}).then(
  message => alert(message)
);
		}
	</script>

</body>
</html>
