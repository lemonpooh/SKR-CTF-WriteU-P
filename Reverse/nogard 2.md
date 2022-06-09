# IDA tools

- press F5

See there is a if() statement, probably checking the flag with a param.

![image](https://user-images.githubusercontent.com/59368650/172778490-3cfae50d-4e0c-442a-af51-a8b7c52821be.png)

double click the `param`, you would see two param showing hex values.

![image](https://user-images.githubusercontent.com/59368650/172778877-cb1e59f0-0070-4cb3-9947-ca4cacd0342b.png)

Translate it into ASCII code.
You will see the other half is being encrypted.
- Copy the 2nd part of the key
- place it into `Cyberchef` online tools
- choose XOR, insert the part1 key value to the XOR enc and choose UTF8. As image below

![image](https://user-images.githubusercontent.com/59368650/172779543-5e08a960-069d-4411-b85f-35de0f9edf78.png)

- you'l see the other half of the flag.
- combine the part1 flag with this half of the flag, submit it.
 
