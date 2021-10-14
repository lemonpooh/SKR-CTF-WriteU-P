# VerdeSEC CommChallenges
## Gaius
` Description: I had rather be first in a village than second at Rome.

Flag format: verdesec{XXX} `
`<addr>`
From the description, we can simply google the quote. And we can know that it is relate to caeser cipher.
But sadly it is not relate to caeser cipher i guess due to the encoded flag are involved with some special characters. AHAHAHAHA
Then i giveup and ask for the solutions.
The solution is dealing with the ASCII table.
Another hints was the flag foramt. So, we match the flag format with the encoded flag one by one then we calculate the differences of the ascii (DEC)number between two characters, 
we can see that the number is decrement by one in starting from the first character till the last character.
So, we just continue it for the rest by finding the ASCII number for first row and added with the decremented number, and convert it to the ASCII characters.We got the flag!

## Image solution
![image](https://user-images.githubusercontent.com/59368650/137259464-f3b3dd4b-3d2f-4cbb-9ec6-17aa55e1f8ec.png)


