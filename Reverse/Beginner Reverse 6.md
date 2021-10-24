```c
#include <stdio.h>
#include <string.h>
#include <ctype.h>

int checkPassword(char* pass){
	size_t length = strlen(pass);
	if(length != 17){
		return 0;//false
	}
	if(pass[0] != 'R'){
		return 0;//false
	}
	if(pass[1] - pass[0] != -31 || pass[1] != pass[3]){
		return 0; //false
	}
	if(pass[4] != tolower(pass[0]) || pass[2] - pass[4] != 4){
		return 0;//false
	}
	if(pass[5] != '5' || pass[5] - pass[6] != 4){
		return 0;//false
	}
	if(pass[7] != pass[0] + 28 || pass[2] - pass[8] != 47){
		return 0;//false
	}
	if(pass[9] != '_' || pass[12] != pass[9] || strncmp(pass+13,"Fun!",4) != 0 || strncmp(pass+10,"1s",2) != 0){
		return 0;//false
	}
	return 1;//true
}


int main () {
	char password[20];
	printf("Enter password: ");
	scanf("%19s",password);
	if (checkPassword(password))
	{
		printf("Welcome admin!\nFlag: SKR{%s}",password);
	}else{
		printf("Login failed!");
	}
}
```

I have no experience on reverse tools using but this easy challenges you can do it as forward engineering HAHAHA.
Refer to ascii table
![image](https://user-images.githubusercontent.com/59368650/138586699-4c54c0d8-6fad-476c-a514-33ceab7f827f.png)

```
if(length != 17){
		return 0;//false
	}
 ```
The length of the flag = 17

sO, the 1st if() to check 1st char is `R`

```
pass[1] - pass[0] != -31
``` 
which is pass[1] - 'R' != -31 --> pass[1] = 82-31 = `3`

```
pass[1] = pass[3]
```
pass[3] = `3`

```
pass[4] != tolower(pass[0]
```
pass[4] = `r`

```
pass[2] - pass[4] != 4
```
pass[2] = pass[4] + 4 = 114 + 4 = 118 = `v`

```
pass[5] != '5' 
```
pass[5]  = `5`

```
pass[5] - pass[6] != 4
```
pass[6] = 53 - 4 = 49 = `1`

```
pass[7] != pass[0] + 28 
```
pass[7] = `R` + 28 = 110 = `n`

```
pass[2] - pass[8] != 47
```
pass[8] = `v` - 47 = 118 - 47 = 71 = `G`

```
pass[9] != '_'
```
pass[9] = '_'

```
pass[12] != pass[9]
```
pass[12]='_'

```
strncmp(pass+13,"Fun!",4) != 0
```
![image](https://user-images.githubusercontent.com/59368650/138587002-08f11186-4003-4ee1-abd4-d9b66c234b49.png)
insert 4 characters starting at position 13

```
strncmp(pass+10,"1s",2) != 0
```
insert 2 characters starting at position 10

Last `flag: SKR{R3v3r51nG_1s_Fun!}`
