# Challenge link
URL:      [http://18.184.219.56:8080/](http://18.184.219.56:8080/) (maybe the server was shut down)

# Challenge description
Hopefully you know how web works...

# Challenge source file
Blackbox

# Difficulty
Very easy

# Author
MapnaCTF team

# Approach
- This message is given to me when I connect to the website:
  ![image](https://github.com/NoSpaceAvailable/MapnaCTF2023/assets/143888307/91a8bed4-8b84-4942-9a37-2610b3c9aaf0)

- Suddenly, I think about adding *Referer* header to the HTTP request. I use Burpsuite for that purpose and this is what happened:
  ![image](https://github.com/NoSpaceAvailable/MapnaCTF2023/assets/143888307/4998b772-e2b5-4389-871c-116896069467)

- I tried to find a header that relevant to this message but got nothing. Maybe *secret* is a request parameter:
  ![image](https://github.com/NoSpaceAvailable/MapnaCTF2023/assets/143888307/156a81f9-f829-466c-b4aa-10e223de141e)

- The response text gave me a hint that *secret* should be the name of the request protocol we are using. In this case, it is HTTP:
  ![image](https://github.com/NoSpaceAvailable/MapnaCTF2023/assets/143888307/1b1c50cc-e2b2-48be-a263-b9e1e9462197)
  
- It said that I should use *FLAG* request method instead of *GET*:
  ![image](https://github.com/NoSpaceAvailable/MapnaCTF2023/assets/143888307/b6f8145e-7d6a-4140-b166-f1502717aecf)

- Flag: MAPNA{533m5-l1k3-y0u-kn0w-h77p-1836a2f}
