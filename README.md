ThisisLegal
===========

http://www.thisislegal.com/

#Challenge 1
afficher la source de la page :
```
      <!-- The password is: easy123 -->
```

#Challenge 2
afficher la source de la page :
```
<script type="text/javascript">
function Login(form) { 
if (form.username.value=="admin") {
if (form.password.value=="imageek") { 
location="f.ID+1";   
} 
else { 
alert("Sorry, wrong username or password provided."); 
}  
}
else { 
alert("Sorry, wrong username or password provided."); 
}  
} 
</script>
```

#Challenge 3
http://www.thisislegal.com/challenge3/index.php?file=http://www.thisislegal.com/challenge3/c_99.txt

#Challenge 4
editer la valeur cookie ALLOWED_ACCESS = NO => YES
rafraichir la page

#Challenge 5
Tamper data, changer la valeur du champ to pour mettre une adresse email valide. 
contenu de l'email : 
```
well done, if you are reading this you manipulated the form. the password is: email403
```

#Challenge 6
http://www.thisislegal.com/robots.txt
```
User-agent: *
Crawl-Delay: 10
Disallow: /robotspage
```
aller sur http://www.thisislegal.com/robotspage

#Challenge 7
fontpage ! => http://www.ouah.org/hfag.txt
aller sur http://www.thisislegal.com/challenge7/_vti_pvt/
récupérer administrators.pwd
```
admin:dut4HlQyu4dSA
```
utiliser john the ripper.
```
# john administrators.pwd 
Created directory: /root/.john
Loaded 1 password hash (Traditional DES [128/128 BS SSE2-16])
a1b2c3           (admin)
guesses: 1  time: 0:00:00:00 100% (2)  c/s: 15840  trying: 123456 - marley
Use the "--show" option to display all of the cracked passwords reliably
```

#Challenge 8
dans ollydbg à l'adresse 402148 JE => JNZ
==> Correct! pass is crackedapp175

#Challenge 9
http://www.chaos.org.uk/~eddy/craft/substitute.html
ywddzflh = password
==>     well done you have cracked it the password is nowtheleader 

#Challenge 10 
télécharger http://www.thisislegal.com/password.swf
décompilation avec http://www.showmycode.com/
```
if (password == "flashking") { txt3var = "Correct! enter into password box"; } else { txt3var = "Wrong :( Try Again"; }
```

