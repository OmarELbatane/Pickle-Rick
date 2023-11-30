# Pickle-Rick

![Image Description](/ctf1.png)

<h2> First ingredient </h2>

After seeing that we needed to exploit a web app, I went directly to a browser and typed the IP address of the server (10.10.17.247), and I got this.
  
![Image Description](/ctf2.png)

When I was a kid, I really liked playing jokes on my friends. One of the pranks was that when we were together, I told them to put their username and password in Facebook, for example, and then I clicked on "inspect element" and removed the password from the HTML code, which revealed their password.
So my first instinct in this challenge was to inspect the element, and after a small search, I found this.

![Image Description](/ctf3.png)

And since this is my first CTF, I heard that a lot of easy lobbies put a robots.txt on the server, so I decided why not try it, and "BOOM," I found this text.

![Image Description](/ctf4.png)

After that, I used the Gobuster command so I could find any other files, but I couldn't find any. I could have used other commands, but since Gobuster didn't work, I didn't use the others (and I was wrong).

![Image Description](/ctf5.png)

I tried using the username and the other text in the photos above, and I was able to access this command page.


![Image Description](/ctf6.png)

With this page, I was able to use a lot of commands; however, to make it more difficult for us, they decided to remove a lot of known ones such as cat, more, less, etc., but fortunately, the commands ls and cd were usable.

![Image Description](/ctf7.png)

After using ls, I was able to find a text file, and when I checked it, I found this.
And this is how I found my first ingredient.

![Image Description](/ctf8.png)

![Image Description](/ctf9.png)

<h2>👨‍💻 Second ingredient </h2>
After finding the first ingredient, I was a little bit tired, so that's why you might notice that the IP address is changing.
After reconnecting, I kept using the ls command to find any hidden files, and it took me a little bit of time to remember that if I can use cd .., for example, to go back to other directories, then why not use ls as well. So I kept using every possibility until I used ls ../../.. and found this.
Oh! I forgot to mention that I found a file before that says that the ingredients are in system files.


![Image Description](/ctf10.png)



After checking the common ones, I found that the directory home has Rick as a directory.


![Image Description](/ctf11.png)

So I used this command to see what's inside.

![Image Description](/ctf12.png)

Nice, now I had to use another command that could help me read the file, and I decided to use nl (tac can work as well).


![Image Description](/ctf13.png)

Yes, I found the second ingredient, I'll go to sleep now.


![Image Description](/ctf14.png)

- <h2> Final ingredient </h2>


Now, because of my lack of experience, I basically used every command to find any kind of info in the system directories, and I couldn't find any. The only option left for me was to see the root file. And after some research, I was able to find this command: sudo.
Note: The sudo command in Unix-like operating systems, such as Linux and macOS, stands for "superuser do." It allows a permitted user to execute a command as the superuser or another user, as specified in the sudoers file.

![Image Description](/ctf15.png)

So, I used this command with ls, and I found the 3rd.txt file, and used the command below to read the text and "BAAAAM."


![Image Description](/ctf17.png)

![Image Description](/ctf18.png)

