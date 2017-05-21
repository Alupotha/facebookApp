# facebookApp

In this include FaceBook App development using OAUTH.OAuth is an open standard for token based authentication and authorization on the internet. This framework which allows an end user's account information to be used by third party services, such as Face book, GitHub etc. without exposing the user's passwords.

First of all we need to create an web app using any lanugage to login in to face book.

<html>

<head>

<style>

body{ width:100%; height:100%;margin:0px; background-color:SkyBlue  ;}

.containerX{width:500px;height:500px;background-color:;margin:0 auto;border-radius:10px; margin-top:20px; border: 5px solid Blue; border-radius: 6px;}

.containerXXX{ width:500px;height:70px;background-color:;margin:0px 100px;border-radius:10px; margin-top:100px; position:absolute; bottom:200px; right:150px; }


#login{ background-color:; padding-left: 0px; margin:auto; margin-top:50px; width:500px; height:100px; border-radius:10px; }


input{ padding-right: 10px; font-size:20px; margin-right:20px; margin-top:10px; }

button{ padding-right: 10px; font-size:20px; margin-right:20px; margin-top:10px; bottom:10px; }


h1{ font-family: "Arial"; margin:0px; padding-top:40px; font-size:50px; color:MidnightBlue; text-align:center;}


table{ font-family: "Arial";padding-left: 0px; margin-left:60px; font-size:25px; background-color:;color:MidnightBlue;}


.subm{width:180px; border-radius:60px; color:white; background-color:LimeGreen ; height:35px;}

.buttonn{width:200px; border-radius:50px; color:white; background-color:MidnightBlue ; height:70px;}

.center{position: absolute; left: 0; top: 55%; width: 100%; text-align: center; font-size: 20px; color:MidnightBlue; font-family: "Arial";}

tr,td{height:60px;}


</style>

    <script src="//code.jquery.com/jquery-1.11.3.min.js"></script>

    <script>

        $(document).ready(function () {

            $("#goButton").click(makeRequest);

        });

        function makeRequest() {

// Define properties

            var AUTH_ENDPOINT = "https://www.facebook.com/dialog/oauth";

            var RESPONSE_TYPE = "code";

            var CLIENT_ID = "Your_app ID";

            var REDIRECT_URI = "Your_URL";

            var SCOPE = "public_profile user_posts user_friends user_photos";

// Build authorization request endpoint

            var requestEndpoint = AUTH_ENDPOINT + "?" +

                    "response_type=" + encodeURIComponent(RESPONSE_TYPE) + "&" +

                    "client_id=" + encodeURIComponent(CLIENT_ID) + "&" +

                    "redirect_uri=" + encodeURIComponent(REDIRECT_URI) + "&" +

                    "scope=" + encodeURIComponent(SCOPE);

// Send to authorization request endpoint

            window.location.href = requestEndpoint;
        }
    </script>
</head><body>
        <div class="containerXXX"><nav>
                 <button id="goButton" type="button" class="buttonn"> Continue with Facebook </button>
        </nav> </div>
	<div class="containerX">
	<h1 id="head">LOGIN</h1>
	<div id="container">
                 <div id="results"></div>
		<form name="form" id="login" method="POST" action= >
		<table><tr>
		<td id="td1">Username</td>
		<td><input type="text" id="username" name="username"></td>
		</tr><tr>
		<td>Password</td>
		<td><input type="password" id="password" name="password"></td>
		</tr><tr><td></td><td>
                 <input type="Submit" value="Log in" id="submit" class="subm">
                </td></tr>
		</table></form></div><div class="center"> Or </div>
	</div>
</body>
</html>


