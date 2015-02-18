# gravatarhtml
Gravatar that is done in HTML

!--
Creating a simple gravatar that saves and validates the message when possible.
-->
<html>
<body>
<script type="text/javascript" src="gravatar.js">
function validate_form ( )
{
	valid = true;
		// this needs to be filled in, when the person enters their name in.
	   if (document.contact_form.name.value == "" )
        {
                alert ( "Please fill in the 'Name' box." );
				document.getElementById("name").style.backgroundColor="rgb(255,182,255)";
				document.getElementById("name").style.borderColor="red";
                valid = false;
        }
		// this should return, if there is no input and there is no '@' symbol there
		if ((document.contact_form.email.value == "") || (document.contact_form.email.value == "@"))
        {
                alert ( "Please fill in the 'Email address' box." );
				document.getElementById("email").style.backgroundColor="rgb(255,182,255)";
				document.getElementById("email").style.borderColor="red";
                valid = false;
        }

        return valid;	
}
</script>
			<form name="contact_form" method='post' onSubmit="return validate_form();">
					<fieldset id="contact">
						<legend> Contact Information </legend>

						 <label class="blockLabel"> <br/>Name <span>*</span>
							<input type="text" id="name" name="name" />
						 </label>
						 <br/>
						 	<label class="blockLabel"><br/> Email Address <span>*</span>
								<input type="text" id="email" name="email" />
							</label>
						 <br/>
						 <br/>
						 <tr>
							<td>Message:<br><textarea name="message" rows='10' cols='60'></textarea></td>
						</tr>
						 <br/>
						 <br/>
						 <p><input type="submit" name="send" value="Send Details"></p>
						<p> * - Indicates required fields </p>		
					 </fieldset>
					 
					 
			</form>
<!-- I was not able to add the submitted comment after processing a javascript file using the submit button 
If I have done this in PHP, it would take me a while as it does take some more time to produce a database for this one -->					
</body>
</html>
