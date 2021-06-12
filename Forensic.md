# Forensic

## 1. Corrupted Image

Let's first check the file signature by using tools ```Hexeditor```.
	![image](https://user-images.githubusercontent.com/59368650/121786568-1ed99700-cbf3-11eb-8985-da087fb839f2.png)
	
From the image, we can see the word SKR.
Let's just change the hex to the right file signature hex format. (Change the first 4groups hex values)

![image](https://user-images.githubusercontent.com/59368650/121786875-40d41900-cbf5-11eb-9fd8-73a5dfe47e21.png)

Here is the files signature list that you can refer for: <a href="https://en.wikipedia.org/wiki/List_of_file_signatures"> File Signature Lists </a>
<br>	
After changing file extension to .PNG, you will get the flag image.

![image](https://user-images.githubusercontent.com/59368650/121786982-e6878800-cbf5-11eb-9d3c-03db0f51b05b.png)

<br>

By extracting all capital letter, you will get the flag.

![image](https://user-images.githubusercontent.com/59368650/121787024-4120e400-cbf6-11eb-8ff4-ecc8744b7f42.png)


	
