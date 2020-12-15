# Solution for Ex 1

1. Making directory called LC `mkdir LC`
    Change directory `cd LC`

2. Creating file called test in LC dir `touch test`

3. Adding sh script into test file `cat test` then `cat > test`
    > #!/bin/sh
    > curl --head --silent https://www.google.com/

4&5&6. When excuting the test file with `./test` it says Permission denied
    with `ls -al` it shows that the test file has not excute permission, it has read and write only

### There are 2 solutions for this problem 
 - with `sh test`
 - change permission
   `chmod +x test` then `./test`
   
7. shell knows that the file is supposed to be interpreted using `sh` as it's indicated after shebang sign `#!/bin/sh`

8. Making a Python file in the same way 
   `touch testpy`
   `cat testpy`
   `cat > testpy`
      > #!/bin/python2
      > print "Hello World"
  Then change permissiom in order to enable us excute the file with `./testpy`:
     `chmod +x testpy`
    
 9. `>` sign used to take the output of a program as an input to other program or coping with cat command
     For example:
        `cat testpy > cpd-testpy`
        Then `cat cpd-testpy` it shows:
        
          > #!/bin/python2
          > print "hello world"
         
    `>>` sign used to append 
  
  10. Using Alias to make shortcuts `alias ll='ls -alh'
