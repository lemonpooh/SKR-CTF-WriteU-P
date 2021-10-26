Extract the The_kolona_virus.zip file.
Open the python source code.

```python
kolona_genome = open("MN908947",'r').read() # Read the Genome
kolona_rna = open("kolona_virus","r").read() # Read the RNA
kolona_virus = ""

for i,k in enumerate(kolona_rna): # Decode RNA
	kolona_virus += chr(ord(k) ^ ord(kolona_genome[i % len(kolona_genome)]))

exec(kolona_virus) # Spread the virus
```

`kolona_genome` is the variable to save content from reading `MN908947` file.
`kolona_rna` is the variable to save content from reading `kolona_virus` file.
`kolona_virus` is empty string.
Then, the for() loop to loop every char from `kolona_rna` var. and XOR with the `kolona_genome` array.
So, we know that it is XOR. we put it into [cyberchef](https://gchq.github.io/CyberChef/#recipe=XOR(%7B'option':'Hex','string':''%7D,'Standard',false))

Upload the kolona_virus file.

![image](https://user-images.githubusercontent.com/59368650/138826663-07e7b82e-546e-4194-a732-76b954bfd83d.png)

Input the key from `MN908947` file. and change the output format to UTF8

![image](https://user-images.githubusercontent.com/59368650/138826802-ba39472a-5241-4250-b1db-68b950a34296.png)

we will saw another output which is python source file.

```python
flag = open("flag.jpg","r")
kolona = open("flag.kolona","w+")
key = "COVID-19"

for i,c in enumerate(flag.read()):
	kolona.write(chr(ord(c) ^ ord(key[i % len(key)])))
```

From the code given, `flag` open flag.jpg file and `kolona` is use to write the output into flag.kolona file.
The key given is "COVID-19".
We try to change the flag.kolona file that we downloaded just now into flag.jpg. But when you open it, the file is still corrupted.
what we can do is, upload the `flag.kolona` file into [cyberchef](https://gchq.github.io/CyberChef/#recipe=XOR(%7B'option':'UTF8','string':'COVID-19'%7D,'Standard',false)).
Input the XOR key value "COVID-19".
Rmb to change the output format to UTF8.
![image](https://user-images.githubusercontent.com/59368650/138828877-0e9bfdf1-93b2-457e-a570-addf0eb8ca7f.png)

Then we will see the output with `JFIF` file signature. Although it is JFIF file but we cannot directly convert the file signature from where we have downloaded. Because the file image has aldy been encrypted with XOR key.So，we cannot directly change the file signiture to JFIF.
As we can see, the magic pen appeared.

![image](https://user-images.githubusercontent.com/59368650/138829610-0a56d968-db8d-4284-9f5e-a44216b866e3.png)

click on that pen, the flag image will showed up.

![image](https://user-images.githubusercontent.com/59368650/138829829-6b686c43-192b-48b1-bfaf-5a22aeaf4c39.png)







