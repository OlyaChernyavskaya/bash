Go to home directory

'''$ cd'''

Create folder test 3

'''$ mkdir "test 3"'''

Add three files 4, 5 and 6 to the test 3 folder, each of which should contain 4 lines row1, row2, row3, row4

'''
$ echo -e "row1\nrow2\nrow3\nrow4"> ~/"test 3"/4
$ echo -e "row1\nrow2\nrow3\nrow4"> ~/"test 3"/5
$ echo -e "row1\nrow2\nrow3\nrow4"> ~/"test 3"/6
'''

'''
$ cat *
row1
row2
row3
row4
row1
row2
row3
row4
row1
row2
row3
row4
'''

Find the line row2 in file 5

'''
$ grep row2 5
row2
'''
Find the row row in the test3 folder

'''
$ grep -r row .
./4:row1
./4:row2
./4:row3
./4:row4
./5:row1
./5:row2
./5:row3
./5:row4
./6:row1
./6:row2
./6:row3
./6:row4
'''
Count how many lines with row content in file 6
'''
$ grep -c row 6
4
'''
Find file 5 inside test3 folder
'''
$ find . -name "5"
./5
'''
Using find command delete file 5

'''$ find . -name "5" -delete'''
'''
$ ls -1
4
6
'''
Using the echo command, add the word test to file 4

'''$ echo test >> 4'''

'''
$ cat 4
row1
row2
row3
row4
test
'''
Change the word test in file 4 to fail

'''$ sed -i "s/test/fail/" 4'''
'''
$ cat 4
row1
row2
row3
row4
fail
'''
Add the word test to file 4 so that the contents are preserved

'''$ echo test >> 4'''
'''
$ cat 4
row1
row2
row3
row4
fail
test
'''

View all processes for users not only in the console that occur in the system

'''
$ ps -u Olya
      PID    PPID    PGID     WINPID   TTY         UID    STIME COMMAND
      270      71     270      12280  cons0     197611 12:57:44 /usr/bin/ps
       71       1      71      11784  cons0     197611 12:14:47 /usr/bin/bash
'''
Kill process 666 in console
'''
$ kill 666
bash: kill: (666) - No such process
'''
Find out the availability of the artsiomrusau.com resource using ping

'''
$ ping artsiomrusau.com

Pinging artsiomrusau.com [185.215.4.92] with 32 bytes of data:
Request timed out.
Request timed out.
Request timed out.
Request timed out.

Ping statistics for 185.215.4.92:
    Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),
'''
Submit 5 packages to artsiomrusau.com
'''
ping -c 5 artsiomrusau.com

PING artsiomrusau.com (185.215.4.92) 56(84) bytes of data.

--- artsiomrusau.com ping statistics ---
5 packets transmitted, 0 received, 100% packet loss, time 4006ms
'''

Using GET and curl command, get information about registered pets at https://petstore.swagger.io/

'''
$ curl -X 'GET' \
>   'https://petstore.swagger.io/v2/pet/findByStatus?status=available&status=pending&status=sold' \
>   -H 'accept: application/json'
[{"id":9223372036854293093,"category":{"id":0,"name":"string"},
'''
Using POST and curl command, create a new user at https://petstore.swagger.io/

'''
> $ curl -X 'POST' \
>   'https://petstore.swagger.io/v2/user' \
>   -H 'accept: application/json' \        
>   -H 'Content-Type: application/json' \
>   -d '{
>   "id": 91234,
>   "username": "HelenB",
>   "firstName": "Helen",
>   "lastName": "Bloom",
>   "email": "blHe@wof.com",     
>   "password": "str98765654768",
>   "phone": "s123456789",
>   "userStatus": 0       
> }'
{"code":200,"type":"unknown","message":"91234"}
'''
