## Steaganography
### 1. Coffee Or Tea?

**This challenge need a bit high level critical thinking skill as i also been stuck this chall for long time too. But I got the hints from one of the legend from skr* 

from the image that I have downloaded, firstly I check the file size.
![image](https://user-images.githubusercontent.com/59368650/121174835-f10bef80-c88c-11eb-99d8-178aa145d7e3.png)

the file size of the coffee_or_tea.png is big. Could it be another file hidden in the image?
So, i check with binwalk.
![image](https://user-images.githubusercontent.com/59368650/121177751-5d3c2280-c890-11eb-8104-afdf5a846c32.png)

yea, there is a zip file. I try to open it. 

![image](https://user-images.githubusercontent.com/59368650/121178016-a1c7be00-c890-11eb-8356-94f323782eb1.png)

OH WHAT? its not a normal file
Then we check again with the hints.

from the hints given , it tell us coffee or tea? what if we think of binary 0 or 1
![image](https://user-images.githubusercontent.com/59368650/121173830-d422ec80-c88b-11eb-9a54-a5b0c29e36d1.png)

Inside the coffee_or_tea.png image, there is 12 group with 8 picture each. So, to form a character, it needs 8bits binary to form.
So, there's what i got 

![image](https://user-images.githubusercontent.com/59368650/121178636-4e09a480-c891-11eb-95cb-9fb95a0cd134.png)

no character...
This making me almost giveup.

Think deeply, the title stated coffee or tea. So I need to guess from the every picture inside the image whether is coffee or tea and 0 or 1. Since, legend had gave me hints for this which is coffee be 1 and tea be 0.
So, after I decode it one by one by grouping 8bit in one group. Here's what I got the flag SKR{coffee} *This is not the flag, I have forgotten the flag, you need to decode it by your self! glhf!
