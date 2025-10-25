🛡️ Universal Drag-and-Drop CAPTCHA for Web Projects

A secure, interactive drag-and-drop CAPTCHA that can be easily integrated into PHP, JSP, or ASP.NET web projects. Simply modify the form and validation logic to fit your project.

✨ Features

Drag-and-drop interaction (puzzle piece or icon to correct target)

Works in PHP, JSP, and ASP.NET

Dynamic CAPTCHA generation with randomized pieces and positions

Server-side validation ensures bot protection

Responsive design for desktop and mobile

Easy integration into any login, registration, or sensitive form

Customizable puzzle size, images, complexity, and token expiration

🧩 How It Works

Generate CAPTCHA on Server

PHP → GD Library

JSP → BufferedImage / Servlet

ASP.NET → System.Drawing

Client-Side Drag-and-Drop

HTML5 Drag-and-Drop API (draggable, droppable)

Optional: jQuery UI for easier handling

Validation

User drags puzzle piece to target

Coordinates/order sent to server on form submit

Server validates solution stored in session or token

⚙️ Integration
PHP
<!-- Include in your form -->
<?php include 'captcha.php'; ?>
<input type="submit" value="Submit">

<!-- Validate -->
<?php
include 'validate_captcha.php';
if(validateCaptcha($_POST)) {
    // Proceed with form
} else {
    // Reload CAPTCHA / show error
}
?>

JSP
<!-- Include in your JSP form -->
<%@ include file="captcha.jsp" %>
<input type="submit" value="Submit">

// Servlet validation
if(CaptchaValidator.isValid(request)) {
    // Proceed
} else {
    // Reload CAPTCHA / show error
}

ASP.NET (C#)
<!-- Add in your ASPX form -->
<uc1:DragDropCaptcha ID="Captcha1" runat="server" />
<asp:Button ID="SubmitBtn" runat="server" Text="Submit" OnClick="SubmitBtn_Click" />

// Code-behind validation
protected void SubmitBtn_Click(object sender, EventArgs e)
{
    if(Captcha1.Validate())
    {
        // Proceed
    }
    else
    {
        // Reload CAPTCHA / show error
    }
}

🔒 Security Tips

Randomize puzzle pieces on every load

Validate CAPTCHA only on server

Use session tokens to prevent replay attacks

Set an expiry time for each CAPTCHA

🛠️ Technologies
Platform	Libraries / APIs
PHP	GD Library, HTML5 Drag-and-Drop, AJAX
JSP	Servlet, BufferedImage, HTML5 Drag-and-Drop, jQuery UI
ASP.NET	System.Drawing, HTML5 Drag-and-Drop, jQuery UI
🎨 Customization

Change puzzle image or icon

Adjust number of pieces

Modify drag behavior (snap-to-grid, rotation)

Update validation logic to integrate with your database or user system

🏷️ Tags

#captcha #draganddrop #php #jsp #aspnet #websecurity #html5 #javascript #formvalidation #botprotection
