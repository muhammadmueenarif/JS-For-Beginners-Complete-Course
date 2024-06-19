lec 01. introduction
lec 02. arrays
lec 03. variables
lec 04. conditional statements
lec 05. functions
lec 06. objects
lec 07. for loop.
lec 08. while loop.
lec 09. do while loop.
lec 10. events.
lec 11. iteration statements.
lec 12. loop control statements. break and continue.
lec 13. if else.
lec 14. switch.
lec 15. animation.
lec 16. operators.
lec 17. comparison operators.
lec 18. logical operators.

we have covered these above 18 lectures in some other videos and repositories so i am not goiing to 
repeat these. 

lec 19. cookies.
used to maintain state on client side. they are stored on the client machine as txt file. when user
revisits the site, data is obtained from cookies. 

for server communication, we submit our page on server side. it comes back after data submit. when we 
submit values in form and send to server, the data is not transferred by the protocol but the address 
is transferred. one problem can occur that data may lose when it come back from server to client. 
we use state management here in client side using cookies. 
we simply create a text file in the client machine and location may vary in each browser. when user 
revisits the page, some data will be get from cookies. even you close or shut down pc, file will be saved. 

2 types of cookies. session and persistent. session cookies that just start and end with session. when you
visit and close the site. 
persistent cookies are those that do not have lifetime or you can add lifetime if you want. you can remove 
by going to memory in that location. below is code. 

<body>
    <form name="myform" action="">
        Enter name: <input type="text" name="customer">
        <input type="button" value="set cookie" onclick="writeCookie();">
    </form>
</body>


 <script language="javascript" type="text/javascript">

        function writeCookie() {
            
            //if input blank, function will not run.
            if (document.myform.customer.value=="")
            {
                alert("Please enter a value");
                return;
            }

            // user entered value will store in cookievalue
            var cookievalue= escape(document.myform.customer.value) + ";";

            // document.cookie will create text file in client machine. name if fixed field
            document.cookie = "name" +cookievalue;
            document.write("setting cookie : " + "name = " + cookievalue);
        }
    </script>

