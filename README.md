### Phishing campaign documentation

The campaign's purpose is launch a phishing for Facebook credentials attack using setoolkit(tool) for further use in other explorations using matching credentials
with using the gathered credentials as like: passwords or even emails or phone number synchronized with.

Goal: Impersonate the Facebook webpage connected to a web server running in a virtual machine like Kali Linux or similar Linux environment.

## Credential Harvest attack walkthrough 

*First steps*

Create the web page that'll be impersonating the Facebook web page. For this i had use the Social Engineering Tool Kit(setoolkit) running these commands: 
	
	$sudo setoolkit

and pops out this screen with these options:
![image](/imgs/Screenshot%202025-07-01%20221450.png)
-- The Ilustration--


After we review the menu we select the 1st option listed as: "1) Social-Engineering Attacks", the pops out another screen with others options where we must to chose the 2nd option listed as: "2) Website Attack Vectors"

![image](/imgs/image.png)

-- The Ilustration--

Now we have another menu with some explanation of each attack and their uses:
![image](/imgs/Screenshot%202025-07-01%20222725.png)
--The Ilustration--

After review all the information about each one attack, the one that fits better in our scenario is the 3th option listed as: "3) Credential Harvest Attack Method".
This option allows to clone a web site by using a specific url. i.e: http://www.facebook.com(in our case we used Facebook).

*Note* The url must have a HTTP protocol instead a HTTPS protocol. This is to avoid to be detected blocked by the Facebook's certificate authories.

After select the 3th option in the menu, this another screen will pops out:
![image](/imgs/Screenshot%202025-07-01%20223603.png)
--The Ilustration--

Here we must select the 2nd option listed as: "2) Site Cloner", and this is the output:
![image](/imgs/Screenshot%202025-07-01%20223941.png)
--The ilustration--

Now you must to set up the attack. The first choice is the IP adress of receiver(Your IP adress or your server's IP).

In this camping were used NGROK as the server tunel to my virtual machine, but you can use your own IP adress for it.

After set up your server(or IP adress) to receive the data came from the user(the victim) you must to give the URL from the page you want to clone.
![image](/imgs/Screenshot%202025-07-01%20224532.png)
-- The Ilustration--

This is the output after the URL set up:

![image](/imgs/Screenshot%202025-07-01%20224822.png)
-- The Ilustration--

Now you just copy the server adress or your machine adress and send to the victm.

## The attack delivery

Now your have a several options to deliver the attack. Mostly of Social-Engineering attacks happens through email, but there's a lot more ways as like: SMS, Phone calls impersonating the Facebook support center contact.

*Note* I'll not deep dive into Social-Engineering operations because the purpose of this documentation is just to show how phishing could be exploit by an attacker. 

## The Attack

Passed all the Steps, now is the time to gathers and analyze the information coming from target(the victim).

- Fist: The victim receives the link, and this is screen after cliked on it:
![image](/imgs/Screenshot%202025-07-01%20225722.png)
-- The Ilustration --

Looks exactly the same as the Facebook's login page !

The victim will put the credentials on the browser and you will receive the output from the Email and Password fields on your server or terminal if you chose to put your machine ip.

## The information

After all this is the output you'll receive:
![image](/imgs/Screenshot%202025-07-01%20230301.png)
-- The Ilustration --

Voilà ! Now you have the headers containing the user and password. You must to manipulate the request and fill with this information. 

## The final
This is an basic explanation about Credential Harvest Attack using Social-Engineering techniques to achieve the goal. 

To feel confident with this kind of attacks you need to reseach some resources to learn more deeply into Social-Engineering techniques, and take a deep knowledge of that. My purpose here is just to show as a simple way to launch this attack.

Best Regards.

Marcelo Lones | Cyber Security Specialist


