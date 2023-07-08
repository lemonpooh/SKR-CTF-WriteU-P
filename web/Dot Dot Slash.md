# Dot Dot Slash

solution:
curl --verbose --path-as-is 'http://skrctf.me:400/../../../../../../flag.txt'

*Thanks to my friend who help me for the chal with a clear and understanding explaination*
```
Because browser will automatically interpret ../../.../../../ before passing to server, meaning that if u type http://xxx.com/../../../../flag.txt in browser will resulted in http://xxx.com/flag.txt before passing to server.

So we can use curl feature called --path-as-is to tell browser to not auto interpret the ../, hence when it passed to server, resulted in LFI (See source code) 
```
