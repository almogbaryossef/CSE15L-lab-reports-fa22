# Lab Report 3 (Researching Commands)

I have chosen to explore the command "grep". During the lab in week 4, we saw that grep can be used to find all lines in a file that contain a certain string (we used ".txt" to get the paths in the file find-results.txt of .txt files).
The format which we used was: grep <some string> <file>. The command grep can also be used in the format: 
grep <command-line option(s)> <pattern> <file1> <file2> ...

## Command-line Option 1: -c
**-c** can be used with grep to return the number of lines that contain the pattern provided in the chosen file(s). This command is useful if we want to quickly get an idea of the subject of the text. For example, we might have many files about health conditions and diseases, and we want to find information about asthma. Checking to see the number of times the word "asthma" appeared in each file can give us an indication as to which files focus on asthma are more likely to provide the information we are looking for.
We use the format: grep -c <pattern> <file1> <file2> ....

Example 1:
```
almogbar@Almogs-MacBook-Pro docsearch % grep -c "virus" technical/biomed/rr37.txt
0
almogbar@Almogs-MacBook-Pro docsearch % grep -c "asthma" technical/biomed/rr37.txt
145
```
Here we are trying to search for the word "virus" in one of the text files in biomed, but as we can see there are no instances of it in that file, meaning that if we want to read about viruses, we probably wouldn't spend time reading this text. However, if we wanted to read about asthma, this would most likely be a good source as it contains the words asthma 145 times.
  
Example 2:  
```
almogbar@Almogs-MacBook-Pro docsearch % grep -c "cell" technical/biomed/*
technical/biomed/1468-6708-3-1.txt:4
technical/biomed/1468-6708-3-10.txt:0
technical/biomed/1468-6708-3-3.txt:1
technical/biomed/1468-6708-3-4.txt:0
technical/biomed/1468-6708-3-7.txt:3
technical/biomed/1471-2091-2-10.txt:58
technical/biomed/1471-2091-2-11.txt:153
technical/biomed/1471-2091-2-12.txt:3
technical/biomed/1471-2091-2-13.txt:3
technical/biomed/1471-2091-2-16.txt:1
technical/biomed/1471-2091-2-5.txt:180
technical/biomed/1471-2091-2-7.txt:17
technical/biomed/1471-2091-2-9.txt:4
technical/biomed/1471-2091-3-13.txt:2
technical/biomed/1471-2091-3-14.txt:150
technical/biomed/1471-2091-3-15.txt:22
technical/biomed/1471-2091-3-16.txt:17
technical/biomed/1471-2091-3-17.txt:0
technical/biomed/1471-2091-3-18.txt:1
technical/biomed/1471-2091-3-22.txt:32
technical/biomed/1471-2091-3-23.txt:18
technical/biomed/1471-2091-3-30.txt:77
technical/biomed/1471-2091-3-31.txt:22
technical/biomed/1471-2091-3-4.txt:7
technical/biomed/1471-2091-3-8.txt:78
technical/biomed/1471-2091-4-1.txt:80
technical/biomed/1471-2091-4-5.txt:6
technical/biomed/1471-2105-1-1.txt:21
technical/biomed/1471-2105-2-1.txt:22
technical/biomed/1471-2105-2-8.txt:1
technical/biomed/1471-2105-2-9.txt:0
technical/biomed/1471-2105-3-12.txt:0
technical/biomed/1471-2105-3-14.txt:1
technical/biomed/1471-2105-3-16.txt:9
technical/biomed/1471-2105-3-17.txt:1
technical/biomed/1471-2105-3-18.txt:11
technical/biomed/1471-2105-3-2.txt:36
technical/biomed/1471-2105-3-22.txt:9
technical/biomed/1471-2105-3-23.txt:0
technical/biomed/1471-2105-3-24.txt:0
technical/biomed/1471-2105-3-26.txt:30
technical/biomed/1471-2105-3-28.txt:0
technical/biomed/1471-2105-3-3.txt:12
technical/biomed/1471-2105-3-30.txt:1
technical/biomed/1471-2105-3-34.txt:32
technical/biomed/1471-2105-3-37.txt:3
technical/biomed/1471-2105-3-38.txt:4
technical/biomed/1471-2105-3-4.txt:5
technical/biomed/1471-2105-3-6.txt:0
technical/biomed/1471-2105-4-13.txt:9
technical/biomed/1471-2105-4-24.txt:2
technical/biomed/1471-2105-4-25.txt:1
technical/biomed/1471-2105-4-26.txt:1
technical/biomed/1471-2105-4-27.txt:2
technical/biomed/1471-2105-4-28.txt:1
technical/biomed/1471-2105-4-31.txt:0
technical/biomed/1471-2121-1-2.txt:10
technical/biomed/1471-2121-2-1.txt:77
technical/biomed/1471-2121-2-10.txt:143
technical/biomed/1471-2121-2-11.txt:109
technical/biomed/1471-2121-2-12.txt:35
technical/biomed/1471-2121-2-15.txt:107
technical/biomed/1471-2121-2-18.txt:130
technical/biomed/1471-2121-2-21.txt:60
technical/biomed/1471-2121-2-22.txt:1
technical/biomed/1471-2121-2-3.txt:21
technical/biomed/1471-2121-2-6.txt:64
technical/biomed/1471-2121-3-10.txt:174
technical/biomed/1471-2121-3-11.txt:99
technical/biomed/1471-2121-3-12.txt:105
technical/biomed/1471-2121-3-13.txt:60
technical/biomed/1471-2121-3-15.txt:50
technical/biomed/1471-2121-3-16.txt:51
technical/biomed/1471-2121-3-18.txt:66
technical/biomed/1471-2121-3-19.txt:124
technical/biomed/1471-2121-3-2.txt:94
technical/biomed/1471-2121-3-21.txt:41
technical/biomed/1471-2121-3-22.txt:91
technical/biomed/1471-2121-3-25.txt:84
technical/biomed/1471-2121-3-30.txt:73
technical/biomed/1471-2121-3-4.txt:143
technical/biomed/1471-2121-3-6.txt:153
technical/biomed/1471-2121-3-8.txt:108
technical/biomed/1471-2121-4-1.txt:31
technical/biomed/1471-2121-4-2.txt:119
technical/biomed/1471-2121-4-3.txt:34
technical/biomed/1471-2121-4-4.txt:42
technical/biomed/1471-2121-4-5.txt:57
technical/biomed/1471-2121-4-6.txt:75
technical/biomed/1471-213X-1-1.txt:4
technical/biomed/1471-213X-1-10.txt:56
technical/biomed/1471-213X-1-11.txt:128
technical/biomed/1471-213X-1-12.txt:94
technical/biomed/1471-213X-1-13.txt:147
technical/biomed/1471-213X-1-15.txt:65
technical/biomed/1471-213X-1-2.txt:58
technical/biomed/1471-213X-1-3.txt:102
technical/biomed/1471-213X-1-4.txt:20
technical/biomed/1471-213X-1-6.txt:50
technical/biomed/1471-213X-1-9.txt:1
technical/biomed/1471-213X-2-1.txt:29
technical/biomed/1471-213X-2-7.txt:116
technical/biomed/1471-213X-2-8.txt:34
technical/biomed/1471-213X-3-2.txt:91
technical/biomed/1471-213X-3-3.txt:164
technical/biomed/1471-213X-3-4.txt:114
technical/biomed/1471-213X-3-7.txt:8
technical/biomed/1471-2148-1-1.txt:19
technical/biomed/1471-2148-1-14.txt:3
technical/biomed/1471-2148-1-4.txt:3
technical/biomed/1471-2148-1-6.txt:0
technical/biomed/1471-2148-1-8.txt:0
technical/biomed/1471-2148-2-12.txt:6
technical/biomed/1471-2148-2-14.txt:12
technical/biomed/1471-2148-2-15.txt:0
technical/biomed/1471-2148-2-17.txt:1
technical/biomed/1471-2148-2-2.txt:9
technical/biomed/1471-2148-2-5.txt:0
technical/biomed/1471-2148-2-7.txt:0
technical/biomed/1471-2148-2-8.txt:1
technical/biomed/1471-2148-3-1.txt:0
technical/biomed/1471-2148-3-18.txt:5
technical/biomed/1471-2148-3-3.txt:2
technical/biomed/1471-2148-3-4.txt:4
technical/biomed/1471-2148-3-7.txt:6
technical/biomed/1471-2156-2-1.txt:28
technical/biomed/1471-2156-2-12.txt:2
technical/biomed/1471-2156-2-17.txt:2
technical/biomed/1471-2156-2-18.txt:49
technical/biomed/1471-2156-2-3.txt:2
technical/biomed/1471-2156-2-5.txt:4
technical/biomed/1471-2156-2-7.txt:8
technical/biomed/1471-2156-2-8.txt:7
technical/biomed/1471-2156-3-10.txt:0
technical/biomed/1471-2156-3-11.txt:18
technical/biomed/1471-2156-3-16.txt:4
technical/biomed/1471-2156-3-17.txt:46
technical/biomed/1471-2156-3-22.txt:3
technical/biomed/1471-2156-3-3.txt:1
technical/biomed/1471-2156-3-4.txt:52
technical/biomed/1471-2156-4-10.txt:0
technical/biomed/1471-2156-4-5.txt:23
technical/biomed/1471-2156-4-6.txt:94
technical/biomed/1471-2156-4-9.txt:73
technical/biomed/1471-2164-2-1.txt:46
technical/biomed/1471-2164-2-2.txt:14
technical/biomed/1471-2164-2-4.txt:1
technical/biomed/1471-2164-2-6.txt:14
technical/biomed/1471-2164-2-7.txt:2
technical/biomed/1471-2164-2-8.txt:15
technical/biomed/1471-2164-2-9.txt:12
technical/biomed/1471-2164-3-1.txt:19
technical/biomed/1471-2164-3-10.txt:5
technical/biomed/1471-2164-3-13.txt:2
technical/biomed/1471-2164-3-15.txt:4
technical/biomed/1471-2164-3-16.txt:23
technical/biomed/1471-2164-3-18.txt:14
technical/biomed/1471-2164-3-19.txt:8
technical/biomed/1471-2164-3-23.txt:1
technical/biomed/1471-2164-3-24.txt:0
technical/biomed/1471-2164-3-26.txt:3
technical/biomed/1471-2164-3-27.txt:0
technical/biomed/1471-2164-3-28.txt:6
technical/biomed/1471-2164-3-29.txt:16
technical/biomed/1471-2164-3-30.txt:2
technical/biomed/1471-2164-3-31.txt:11
technical/biomed/1471-2164-3-32.txt:10
technical/biomed/1471-2164-3-33.txt:4
technical/biomed/1471-2164-3-34.txt:4
technical/biomed/1471-2164-3-35.txt:0
technical/biomed/1471-2164-3-4.txt:0
technical/biomed/1471-2164-3-6.txt:21
technical/biomed/1471-2164-3-7.txt:1
technical/biomed/1471-2164-3-8.txt:2
technical/biomed/1471-2164-3-9.txt:12
technical/biomed/1471-2164-4-13.txt:8
technical/biomed/1471-2164-4-14.txt:0
technical/biomed/1471-2164-4-15.txt:0
technical/biomed/1471-2164-4-16.txt:3
technical/biomed/1471-2164-4-19.txt:2
technical/biomed/1471-2164-4-2.txt:32
technical/biomed/1471-2164-4-21.txt:0
technical/biomed/1471-2164-4-22.txt:12
technical/biomed/1471-2164-4-23.txt:5
technical/biomed/1471-2164-4-24.txt:8
technical/biomed/1471-2164-4-25.txt:6
technical/biomed/1471-2164-4-26.txt:1
technical/biomed/1471-2164-4-28.txt:27
technical/biomed/1471-2164-4-4.txt:4
technical/biomed/1471-2164-4-5.txt:10
technical/biomed/1471-2164-4-6.txt:0
technical/biomed/1471-2172-1-1.txt:34
technical/biomed/1471-2172-2-10.txt:170
technical/biomed/1471-2172-2-3.txt:79
technical/biomed/1471-2172-2-4.txt:122
technical/biomed/1471-2172-2-9.txt:50
technical/biomed/1471-2172-3-1.txt:44
technical/biomed/1471-2172-3-10.txt:8
technical/biomed/1471-2172-3-12.txt:76
technical/biomed/1471-2172-3-16.txt:100
technical/biomed/1471-2172-3-2.txt:72
technical/biomed/1471-2172-3-4.txt:155
technical/biomed/1471-2172-3-9.txt:97
technical/biomed/1471-2172-4-1.txt:152
technical/biomed/1471-2172-4-2.txt:13
technical/biomed/1471-2180-1-12.txt:12
technical/biomed/1471-2180-1-16.txt:22
technical/biomed/1471-2180-1-26.txt:36
technical/biomed/1471-2180-1-28.txt:45
technical/biomed/1471-2180-1-29.txt:11
technical/biomed/1471-2180-1-31.txt:9
technical/biomed/1471-2180-1-33.txt:1
technical/biomed/1471-2180-1-34.txt:67
technical/biomed/1471-2180-1-7.txt:30
technical/biomed/1471-2180-1-8.txt:59
technical/biomed/1471-2180-2-1.txt:35
technical/biomed/1471-2180-2-13.txt:3
technical/biomed/1471-2180-2-16.txt:18
technical/biomed/1471-2180-2-2.txt:26
technical/biomed/1471-2180-2-20.txt:127
technical/biomed/1471-2180-2-22.txt:12
technical/biomed/1471-2180-2-26.txt:37
technical/biomed/1471-2180-2-29.txt:0
technical/biomed/1471-2180-2-32.txt:10
technical/biomed/1471-2180-2-35.txt:27
technical/biomed/1471-2180-2-38.txt:2
technical/biomed/1471-2180-2-7.txt:17
technical/biomed/1471-2180-3-10.txt:4
technical/biomed/1471-2180-3-11.txt:30
technical/biomed/1471-2180-3-13.txt:0
technical/biomed/1471-2180-3-15.txt:50
technical/biomed/1471-2180-3-4.txt:5
technical/biomed/1471-2180-3-5.txt:95
technical/biomed/1471-2180-3-9.txt:132
technical/biomed/1471-2199-2-1.txt:9
technical/biomed/1471-2199-2-10.txt:3
technical/biomed/1471-2199-2-12.txt:33
technical/biomed/1471-2199-2-2.txt:15
technical/biomed/1471-2199-2-3.txt:11
technical/biomed/1471-2199-2-4.txt:197
technical/biomed/1471-2199-2-5.txt:59
technical/biomed/1471-2199-2-6.txt:2
technical/biomed/1471-2199-3-10.txt:36
technical/biomed/1471-2199-3-11.txt:114
technical/biomed/1471-2199-3-12.txt:13
technical/biomed/1471-2199-3-17.txt:0
technical/biomed/1471-2199-3-3.txt:68
technical/biomed/1471-2199-3-7.txt:26
technical/biomed/1471-2199-4-4.txt:29
technical/biomed/1471-2199-4-5.txt:11
technical/biomed/1471-2202-1-1.txt:15
technical/biomed/1471-2202-2-1.txt:68
technical/biomed/1471-2202-2-10.txt:0
technical/biomed/1471-2202-2-12.txt:34
technical/biomed/1471-2202-2-14.txt:1
technical/biomed/1471-2202-2-15.txt:49
technical/biomed/1471-2202-2-16.txt:80
technical/biomed/1471-2202-2-17.txt:18
technical/biomed/1471-2202-2-18.txt:37
technical/biomed/1471-2202-2-19.txt:19
technical/biomed/1471-2202-2-2.txt:41
technical/biomed/1471-2202-2-20.txt:8
technical/biomed/1471-2202-2-3.txt:46
technical/biomed/1471-2202-2-5.txt:22
technical/biomed/1471-2202-2-6.txt:62
technical/biomed/1471-2202-2-7.txt:13
technical/biomed/1471-2202-2-8.txt:14
technical/biomed/1471-2202-2-9.txt:7
technical/biomed/1471-2202-3-1.txt:1
technical/biomed/1471-2202-3-10.txt:26
technical/biomed/1471-2202-3-11.txt:4
technical/biomed/1471-2202-3-14.txt:4
technical/biomed/1471-2202-3-16.txt:25
technical/biomed/1471-2202-3-17.txt:1
technical/biomed/1471-2202-3-19.txt:31
technical/biomed/1471-2202-3-20.txt:3
technical/biomed/1471-2202-3-3.txt:83
technical/biomed/1471-2202-3-4.txt:18
technical/biomed/1471-2202-3-5.txt:11
technical/biomed/1471-2202-3-7.txt:19
technical/biomed/1471-2202-3-8.txt:4
technical/biomed/1471-2202-4-10.txt:39
technical/biomed/1471-2202-4-11.txt:34
technical/biomed/1471-2202-4-12.txt:6
technical/biomed/1471-2202-4-16.txt:13
technical/biomed/1471-2202-4-17.txt:47
technical/biomed/1471-2202-4-2.txt:83
technical/biomed/1471-2202-4-3.txt:30
technical/biomed/1471-2202-4-5.txt:4
technical/biomed/1471-2202-4-6.txt:68
technical/biomed/1471-2210-1-10.txt:55
technical/biomed/1471-2210-1-2.txt:2
technical/biomed/1471-2210-1-3.txt:72
technical/biomed/1471-2210-1-4.txt:0
technical/biomed/1471-2210-1-7.txt:44
technical/biomed/1471-2210-1-8.txt:46
technical/biomed/1471-2210-2-14.txt:32
technical/biomed/1471-2210-2-4.txt:64
technical/biomed/1471-2210-2-5.txt:60
technical/biomed/1471-2210-2-6.txt:0
technical/biomed/1471-2210-2-8.txt:0
technical/biomed/1471-2210-2-9.txt:22
technical/biomed/1471-2210-3-1.txt:37
technical/biomed/1471-2210-3-3.txt:8
technical/biomed/1471-2229-1-2.txt:8
technical/biomed/1471-2229-1-3.txt:0
technical/biomed/1471-2229-2-11.txt:1
technical/biomed/1471-2229-2-3.txt:17
technical/biomed/1471-2229-2-4.txt:1
technical/biomed/1471-2229-2-8.txt:2
technical/biomed/1471-2229-2-9.txt:5
technical/biomed/1471-2229-3-3.txt:0
technical/biomed/1471-2253-1-1.txt:0
technical/biomed/1471-2253-2-4.txt:0
technical/biomed/1471-2253-2-5.txt:2
technical/biomed/1471-2261-1-6.txt:0
technical/biomed/1471-2261-2-11.txt:43
technical/biomed/1471-2261-3-4.txt:11
technical/biomed/1471-2261-3-5.txt:0
technical/biomed/1471-2288-1-9.txt:0
technical/biomed/1471-2288-2-10.txt:0
technical/biomed/1471-2288-2-11.txt:0
technical/biomed/1471-2288-2-4.txt:1
technical/biomed/1471-2288-3-4.txt:3
technical/biomed/1471-2288-3-8.txt:0
technical/biomed/1471-2288-3-9.txt:3
technical/biomed/1471-2296-3-18.txt:0
technical/biomed/1471-2296-3-19.txt:0
technical/biomed/1471-2296-3-3.txt:0
technical/biomed/1471-230X-1-10.txt:9
technical/biomed/1471-230X-1-5.txt:42
technical/biomed/1471-230X-1-6.txt:0
technical/biomed/1471-230X-1-8.txt:2
technical/biomed/1471-230X-2-17.txt:1
technical/biomed/1471-230X-2-21.txt:8
technical/biomed/1471-230X-2-23.txt:67
technical/biomed/1471-230X-3-3.txt:47
technical/biomed/1471-230X-3-5.txt:15
technical/biomed/1471-2318-3-2.txt:0
technical/biomed/1471-2326-2-4.txt:1
technical/biomed/1471-2334-1-10.txt:2
technical/biomed/1471-2334-1-13.txt:8
technical/biomed/1471-2334-1-17.txt:27
technical/biomed/1471-2334-1-21.txt:3
technical/biomed/1471-2334-1-24.txt:10
technical/biomed/1471-2334-1-9.txt:53
technical/biomed/1471-2334-2-1.txt:2
technical/biomed/1471-2334-2-24.txt:1
technical/biomed/1471-2334-2-26.txt:8
technical/biomed/1471-2334-2-27.txt:30
technical/biomed/1471-2334-2-29.txt:1
technical/biomed/1471-2334-2-5.txt:34
technical/biomed/1471-2334-2-6.txt:22
technical/biomed/1471-2334-2-7.txt:26
technical/biomed/1471-2334-3-10.txt:20
technical/biomed/1471-2334-3-11.txt:0
technical/biomed/1471-2334-3-12.txt:0
technical/biomed/1471-2334-3-13.txt:0
technical/biomed/1471-2334-3-15.txt:7
technical/biomed/1471-2334-3-9.txt:56
technical/biomed/1471-2350-2-11.txt:7
technical/biomed/1471-2350-2-12.txt:4
technical/biomed/1471-2350-2-2.txt:8
technical/biomed/1471-2350-2-8.txt:1
technical/biomed/1471-2350-3-1.txt:5
technical/biomed/1471-2350-3-12.txt:70
technical/biomed/1471-2350-3-7.txt:0
technical/biomed/1471-2350-3-9.txt:0
technical/biomed/1471-2350-4-2.txt:3
technical/biomed/1471-2350-4-3.txt:2
technical/biomed/1471-2350-4-4.txt:6
technical/biomed/1471-2350-4-6.txt:30
technical/biomed/1471-2369-3-1.txt:30
technical/biomed/1471-2369-3-10.txt:1
technical/biomed/1471-2369-3-6.txt:44
technical/biomed/1471-2369-3-9.txt:0
technical/biomed/1471-2369-4-1.txt:0
technical/biomed/1471-2369-4-5.txt:2
technical/biomed/1471-2377-1-2.txt:0
technical/biomed/1471-2377-2-4.txt:2
technical/biomed/1471-2377-2-6.txt:0
technical/biomed/1471-2377-3-4.txt:6
technical/biomed/1471-2407-1-13.txt:0
technical/biomed/1471-2407-1-15.txt:27
technical/biomed/1471-2407-1-19.txt:141
technical/biomed/1471-2407-1-6.txt:49
technical/biomed/1471-2407-2-11.txt:86
technical/biomed/1471-2407-2-12.txt:10
technical/biomed/1471-2407-2-15.txt:108
technical/biomed/1471-2407-2-16.txt:68
technical/biomed/1471-2407-2-17.txt:50
technical/biomed/1471-2407-2-18.txt:93
technical/biomed/1471-2407-2-19.txt:11
technical/biomed/1471-2407-2-22.txt:1
technical/biomed/1471-2407-2-23.txt:0
technical/biomed/1471-2407-2-3.txt:2
technical/biomed/1471-2407-2-31.txt:4
technical/biomed/1471-2407-2-33.txt:31
technical/biomed/1471-2407-2-8.txt:18
technical/biomed/1471-2407-2-9.txt:6
technical/biomed/1471-2407-3-14.txt:0
technical/biomed/1471-2407-3-15.txt:28
technical/biomed/1471-2407-3-16.txt:1
technical/biomed/1471-2407-3-18.txt:1
technical/biomed/1471-2407-3-3.txt:13
technical/biomed/1471-2407-3-4.txt:24
technical/biomed/1471-2407-3-5.txt:0
technical/biomed/1471-2415-3-1.txt:17
technical/biomed/1471-2415-3-3.txt:90
technical/biomed/1471-2415-3-4.txt:16
technical/biomed/1471-2415-3-5.txt:125
technical/biomed/1471-2431-2-1.txt:6
technical/biomed/1471-2431-2-11.txt:0
technical/biomed/1471-2431-2-12.txt:0
technical/biomed/1471-2431-2-4.txt:6
technical/biomed/1471-2431-3-3.txt:0
technical/biomed/1471-2431-3-4.txt:0
technical/biomed/1471-2431-3-5.txt:0
technical/biomed/1471-2431-3-6.txt:3
technical/biomed/1471-244X-2-9.txt:0
technical/biomed/1471-244X-3-5.txt:0
technical/biomed/1471-2458-1-9.txt:0
technical/biomed/1471-2458-2-11.txt:1
technical/biomed/1471-2458-2-16.txt:0
technical/biomed/1471-2458-2-18.txt:3
technical/biomed/1471-2458-2-21.txt:1
technical/biomed/1471-2458-2-25.txt:0
technical/biomed/1471-2458-2-3.txt:0
technical/biomed/1471-2458-2-6.txt:11
technical/biomed/1471-2458-3-11.txt:1
technical/biomed/1471-2458-3-2.txt:2
technical/biomed/1471-2458-3-20.txt:0
technical/biomed/1471-2458-3-5.txt:1
technical/biomed/1471-2458-3-9.txt:0
technical/biomed/1471-2466-1-1.txt:3
technical/biomed/1471-2466-2-3.txt:1
technical/biomed/1471-2466-2-4.txt:6
technical/biomed/1471-2466-3-1.txt:3
technical/biomed/1471-2474-2-1.txt:0
technical/biomed/1471-2474-2-2.txt:15
technical/biomed/1471-2474-2-3.txt:33
technical/biomed/1471-2474-3-23.txt:1
technical/biomed/1471-2474-3-3.txt:0
technical/biomed/1471-2474-4-4.txt:0
technical/biomed/1471-2474-4-8.txt:1
technical/biomed/1471-2490-3-2.txt:2
technical/biomed/1471-5945-1-3.txt:4
technical/biomed/1471-5945-2-13.txt:46
technical/biomed/1471-5945-3-3.txt:21
technical/biomed/1472-6750-1-11.txt:75
technical/biomed/1472-6750-1-12.txt:76
technical/biomed/1472-6750-1-13.txt:14
technical/biomed/1472-6750-1-6.txt:9
technical/biomed/1472-6750-1-8.txt:7
technical/biomed/1472-6750-2-10.txt:4
technical/biomed/1472-6750-2-13.txt:0
technical/biomed/1472-6750-2-14.txt:1
technical/biomed/1472-6750-2-2.txt:4
technical/biomed/1472-6750-2-21.txt:6
technical/biomed/1472-6750-3-11.txt:10
technical/biomed/1472-6750-3-4.txt:93
technical/biomed/1472-6750-3-6.txt:3
technical/biomed/1472-6769-1-1.txt:76
technical/biomed/1472-6769-1-2.txt:1
technical/biomed/1472-6769-1-3.txt:8
technical/biomed/1472-6769-1-4.txt:9
technical/biomed/1472-6785-1-3.txt:0
technical/biomed/1472-6785-1-5.txt:0
technical/biomed/1472-6785-2-6.txt:0
technical/biomed/1472-6785-2-7.txt:0
technical/biomed/1472-6793-1-11.txt:63
technical/biomed/1472-6793-1-12.txt:24
technical/biomed/1472-6793-1-15.txt:35
technical/biomed/1472-6793-1-2.txt:82
technical/biomed/1472-6793-1-6.txt:0
technical/biomed/1472-6793-1-8.txt:65
technical/biomed/1472-6793-2-1.txt:0
technical/biomed/1472-6793-2-11.txt:0
technical/biomed/1472-6793-2-16.txt:0
technical/biomed/1472-6793-2-17.txt:22
technical/biomed/1472-6793-2-18.txt:0
technical/biomed/1472-6793-2-19.txt:1
technical/biomed/1472-6793-2-2.txt:100
technical/biomed/1472-6793-2-4.txt:31
technical/biomed/1472-6793-2-5.txt:10
technical/biomed/1472-6793-2-8.txt:7
technical/biomed/1472-6793-3-3.txt:6
technical/biomed/1472-6793-3-4.txt:1
technical/biomed/1472-6793-3-5.txt:0
technical/biomed/1472-6793-3-6.txt:22
technical/biomed/1472-6807-1-1.txt:12
technical/biomed/1472-6807-2-1.txt:0
technical/biomed/1472-6807-2-2.txt:6
technical/biomed/1472-6807-2-3.txt:5
technical/biomed/1472-6807-2-4.txt:0
technical/biomed/1472-6807-2-5.txt:4
technical/biomed/1472-6807-2-9.txt:0
technical/biomed/1472-6807-3-1.txt:15
technical/biomed/1472-6807-3-2.txt:0
technical/biomed/1472-6815-2-3.txt:1
technical/biomed/1472-6823-2-2.txt:39
technical/biomed/1472-6823-3-1.txt:0
technical/biomed/1472-6831-2-2.txt:1
technical/biomed/1472-6831-3-1.txt:0
technical/biomed/1472-684X-1-5.txt:2
technical/biomed/1472-684X-2-1.txt:0
technical/biomed/1472-684X-2-2.txt:0
technical/biomed/1472-6874-2-1.txt:0
technical/biomed/1472-6874-2-13.txt:1
technical/biomed/1472-6874-2-8.txt:14
technical/biomed/1472-6874-3-2.txt:10
technical/biomed/1472-6882-1-10.txt:5
technical/biomed/1472-6882-1-11.txt:93
technical/biomed/1472-6882-1-12.txt:0
technical/biomed/1472-6882-1-7.txt:0
technical/biomed/1472-6882-2-10.txt:1
technical/biomed/1472-6882-2-5.txt:0
technical/biomed/1472-6882-3-1.txt:0
technical/biomed/1472-6882-3-3.txt:0
technical/biomed/1472-6890-1-4.txt:55
technical/biomed/1472-6890-2-5.txt:99
technical/biomed/1472-6890-3-2.txt:28
technical/biomed/1472-6904-1-2.txt:1
technical/biomed/1472-6904-2-4.txt:1
technical/biomed/1472-6904-2-5.txt:11
technical/biomed/1472-6904-2-7.txt:15
technical/biomed/1472-6904-3-1.txt:2
technical/biomed/1472-6920-1-3.txt:0
technical/biomed/1472-6920-2-1.txt:0
technical/biomed/1472-6920-2-3.txt:0
technical/biomed/1472-6947-1-2.txt:0
technical/biomed/1472-6947-1-5.txt:0
technical/biomed/1472-6947-1-6.txt:0
technical/biomed/1472-6947-2-4.txt:0
technical/biomed/1472-6947-2-7.txt:5
technical/biomed/1472-6947-3-5.txt:1
technical/biomed/1472-6947-3-8.txt:12
technical/biomed/1472-6955-2-1.txt:0
technical/biomed/1472-6963-1-11.txt:1
technical/biomed/1472-6963-1-8.txt:0
technical/biomed/1472-6963-2-10.txt:0
technical/biomed/1472-6963-3-1.txt:0
technical/biomed/1472-6963-3-11.txt:0
technical/biomed/1472-6963-3-12.txt:0
technical/biomed/1472-6963-3-13.txt:0
technical/biomed/1472-6963-3-14.txt:3
technical/biomed/1472-6963-3-6.txt:0
technical/biomed/1472-6963-3-7.txt:0
technical/biomed/1475-2832-1-1.txt:0
technical/biomed/1475-2867-2-10.txt:18
technical/biomed/1475-2867-2-15.txt:55
technical/biomed/1475-2867-2-7.txt:73
technical/biomed/1475-2867-3-12.txt:76
technical/biomed/1475-2867-3-2.txt:90
technical/biomed/1475-2867-3-3.txt:18
technical/biomed/1475-2867-3-4.txt:117
technical/biomed/1475-2875-1-14.txt:12
technical/biomed/1475-2875-1-5.txt:17
technical/biomed/1475-2875-2-10.txt:0
technical/biomed/1475-2875-2-14.txt:24
technical/biomed/1475-2875-2-4.txt:27
technical/biomed/1475-2883-2-11.txt:0
technical/biomed/1475-2891-1-2.txt:54
technical/biomed/1475-2891-2-1.txt:0
technical/biomed/1475-4924-1-10.txt:76
technical/biomed/1475-4924-1-5.txt:3
technical/biomed/1475-925X-2-1.txt:0
technical/biomed/1475-925X-2-10.txt:3
technical/biomed/1475-925X-2-11.txt:2
technical/biomed/1475-925X-2-12.txt:2
technical/biomed/1475-925X-2-3.txt:1
technical/biomed/1475-925X-2-6.txt:2
technical/biomed/1475-9268-1-1.txt:13
technical/biomed/1475-9268-1-2.txt:14
technical/biomed/1475-9276-1-3.txt:0
technical/biomed/1476-069X-1-3.txt:2
technical/biomed/1476-069X-2-2.txt:0
technical/biomed/1476-069X-2-4.txt:1
technical/biomed/1476-069X-2-7.txt:0
technical/biomed/1476-069X-2-9.txt:0
technical/biomed/1476-0711-2-3.txt:0
technical/biomed/1476-0711-2-7.txt:0
technical/biomed/1476-072X-2-3.txt:0
technical/biomed/1476-072X-2-4.txt:0
technical/biomed/1476-4598-1-3.txt:22
technical/biomed/1476-4598-1-5.txt:58
technical/biomed/1476-4598-1-6.txt:79
technical/biomed/1476-4598-1-8.txt:34
technical/biomed/1476-4598-2-1.txt:100
technical/biomed/1476-4598-2-2.txt:42
technical/biomed/1476-4598-2-20.txt:50
technical/biomed/1476-4598-2-22.txt:41
technical/biomed/1476-4598-2-24.txt:61
technical/biomed/1476-4598-2-25.txt:53
technical/biomed/1476-4598-2-28.txt:98
technical/biomed/1476-4598-2-3.txt:28
technical/biomed/1476-511X-1-2.txt:21
technical/biomed/1476-511X-2-2.txt:59
technical/biomed/1476-511X-2-3.txt:0
technical/biomed/1476-5918-1-2.txt:0
technical/biomed/1476-9433-1-2.txt:91
technical/biomed/1476-9433-1-3.txt:5
technical/biomed/1477-5956-1-1.txt:27
technical/biomed/1477-7525-1-10.txt:0
technical/biomed/1477-7525-1-12.txt:1
technical/biomed/1477-7525-1-9.txt:0
technical/biomed/1477-7819-1-10.txt:4
technical/biomed/1477-7827-1-13.txt:103
technical/biomed/1477-7827-1-17.txt:136
technical/biomed/1477-7827-1-21.txt:3
technical/biomed/1477-7827-1-23.txt:11
technical/biomed/1477-7827-1-27.txt:31
technical/biomed/1477-7827-1-31.txt:79
technical/biomed/1477-7827-1-36.txt:141
technical/biomed/1477-7827-1-43.txt:15
technical/biomed/1477-7827-1-46.txt:129
technical/biomed/1477-7827-1-48.txt:92
technical/biomed/1477-7827-1-54.txt:29
technical/biomed/1477-7827-1-6.txt:34
technical/biomed/1477-7827-1-9.txt:48
technical/biomed/1478-1336-1-2.txt:12
technical/biomed/1478-1336-1-3.txt:29
technical/biomed/1478-1336-1-4.txt:6
technical/biomed/1478-7954-1-3.txt:0
technical/biomed/ar104.txt:18
technical/biomed/ar118.txt:45
technical/biomed/ar120.txt:195
technical/biomed/ar130.txt:197
technical/biomed/ar140.txt:250
technical/biomed/ar149.txt:48
technical/biomed/ar297.txt:15
technical/biomed/ar309.txt:3
technical/biomed/ar319.txt:0
technical/biomed/ar321.txt:31
technical/biomed/ar328.txt:4
technical/biomed/ar331.txt:33
technical/biomed/ar383.txt:10
technical/biomed/ar387.txt:0
technical/biomed/ar407.txt:62
technical/biomed/ar408.txt:54
technical/biomed/ar409.txt:49
technical/biomed/ar422.txt:86
technical/biomed/ar429.txt:9
technical/biomed/ar430.txt:4
technical/biomed/ar601.txt:39
technical/biomed/ar612.txt:58
technical/biomed/ar615.txt:10
technical/biomed/ar619.txt:105
technical/biomed/ar624.txt:155
technical/biomed/ar68.txt:88
technical/biomed/ar745.txt:19
technical/biomed/ar750.txt:0
technical/biomed/ar774.txt:20
technical/biomed/ar778.txt:96
technical/biomed/ar79.txt:28
technical/biomed/ar792.txt:54
technical/biomed/ar795.txt:45
technical/biomed/ar799.txt:18
technical/biomed/ar93.txt:0
technical/biomed/bcr273.txt:25
technical/biomed/bcr284.txt:173
technical/biomed/bcr285.txt:4
technical/biomed/bcr294.txt:5
technical/biomed/bcr303.txt:86
technical/biomed/bcr317.txt:2
technical/biomed/bcr45.txt:155
technical/biomed/bcr458.txt:0
technical/biomed/bcr567.txt:0
technical/biomed/bcr568.txt:4
technical/biomed/bcr570.txt:3
technical/biomed/bcr571.txt:62
technical/biomed/bcr583.txt:2
technical/biomed/bcr588.txt:20
technical/biomed/bcr602.txt:29
technical/biomed/bcr605.txt:0
technical/biomed/bcr607.txt:0
technical/biomed/bcr618.txt:3
technical/biomed/bcr620.txt:70
technical/biomed/bcr631.txt:53
technical/biomed/bcr635.txt:81
technical/biomed/cc103.txt:7
technical/biomed/cc1044.txt:0
technical/biomed/cc105.txt:1
technical/biomed/cc1476.txt:0
technical/biomed/cc1477.txt:0
technical/biomed/cc1495.txt:0
technical/biomed/cc1497.txt:0
technical/biomed/cc1498.txt:0
technical/biomed/cc1529.txt:0
technical/biomed/cc1538.txt:0
technical/biomed/cc1547.txt:10
technical/biomed/cc1843.txt:1
technical/biomed/cc1852.txt:4
technical/biomed/cc1856.txt:0
technical/biomed/cc1882.txt:0
technical/biomed/cc2160.txt:4
technical/biomed/cc2167.txt:2
technical/biomed/cc2171.txt:0
technical/biomed/cc2172.txt:0
technical/biomed/cc2190.txt:1
technical/biomed/cc2358.txt:0
technical/biomed/cc3.txt:0
technical/biomed/cc300.txt:9
technical/biomed/cc303.txt:1
technical/biomed/cc343.txt:0
technical/biomed/cc350.txt:0
technical/biomed/cc367.txt:7
technical/biomed/cc4.txt:0
technical/biomed/cc713.txt:1
technical/biomed/cc973.txt:0
technical/biomed/cc991.txt:0
technical/biomed/cvm-2-1-038.txt:1
technical/biomed/cvm-2-4-180.txt:0
technical/biomed/cvm-2-4-187.txt:0
technical/biomed/cvm-2-6-278.txt:26
technical/biomed/cvm-2-6-286.txt:1
technical/biomed/gb-2000-1-1-research002.txt:13
technical/biomed/gb-2000-1-2-research0003.txt:3
technical/biomed/gb-2001-2-10-research0041.txt:78
technical/biomed/gb-2001-2-10-research0042.txt:3
technical/biomed/gb-2001-2-11-research0045.txt:42
technical/biomed/gb-2001-2-11-research0046.txt:1
technical/biomed/gb-2001-2-12-research0051.txt:8
technical/biomed/gb-2001-2-12-research0053.txt:3
technical/biomed/gb-2001-2-12-research0054.txt:9
technical/biomed/gb-2001-2-12-research0055.txt:7
technical/biomed/gb-2001-2-2-research0004.txt:4
technical/biomed/gb-2001-2-3-research0007.txt:6
technical/biomed/gb-2001-2-3-research0008.txt:8
technical/biomed/gb-2001-2-4-research0010.txt:3
technical/biomed/gb-2001-2-4-research0011.txt:5
technical/biomed/gb-2001-2-4-research0012.txt:16
technical/biomed/gb-2001-2-4-research0014.txt:5
technical/biomed/gb-2001-2-6-research0018.txt:13
technical/biomed/gb-2001-2-6-research0020.txt:4
technical/biomed/gb-2001-2-6-research0021.txt:5
technical/biomed/gb-2001-2-7-research0024.txt:40
technical/biomed/gb-2001-2-7-research0025.txt:2
technical/biomed/gb-2001-2-8-research0027.txt:0
technical/biomed/gb-2001-2-8-research0030.txt:19
technical/biomed/gb-2001-2-8-research0031.txt:44
technical/biomed/gb-2001-2-8-research0032.txt:4
technical/biomed/gb-2001-2-9-research0035.txt:4
technical/biomed/gb-2001-2-9-research0037.txt:2
technical/biomed/gb-2001-3-1-research0001.txt:46
technical/biomed/gb-2001-3-1-research0004.txt:1
technical/biomed/gb-2001-3-1-research0005.txt:2
technical/biomed/gb-2002-3-10-research0052.txt:2
technical/biomed/gb-2002-3-10-research0053.txt:1
technical/biomed/gb-2002-3-10-research0054.txt:1
technical/biomed/gb-2002-3-10-research0055.txt:17
technical/biomed/gb-2002-3-10-research0056.txt:18
technical/biomed/gb-2002-3-11-research0059.txt:39
technical/biomed/gb-2002-3-11-research0060.txt:6
technical/biomed/gb-2002-3-11-research0061.txt:3
technical/biomed/gb-2002-3-11-research0062.txt:56
technical/biomed/gb-2002-3-11-research0065.txt:0
technical/biomed/gb-2002-3-12-research0071.txt:12
technical/biomed/gb-2002-3-12-research0072.txt:3
technical/biomed/gb-2002-3-12-research0075.txt:7
technical/biomed/gb-2002-3-12-research0077.txt:1
technical/biomed/gb-2002-3-12-research0078.txt:3
technical/biomed/gb-2002-3-12-research0079.txt:1
technical/biomed/gb-2002-3-12-research0080.txt:3
technical/biomed/gb-2002-3-12-research0081.txt:0
technical/biomed/gb-2002-3-12-research0082.txt:0
technical/biomed/gb-2002-3-12-research0083.txt:7
technical/biomed/gb-2002-3-12-research0085.txt:1
technical/biomed/gb-2002-3-12-research0086.txt:0
technical/biomed/gb-2002-3-12-research0087.txt:2
technical/biomed/gb-2002-3-12-research0088.txt:23
technical/biomed/gb-2002-3-2-research0008.txt:3
technical/biomed/gb-2002-3-2-research0009.txt:3
technical/biomed/gb-2002-3-3-research0011.txt:12
technical/biomed/gb-2002-3-3-research0012.txt:20
technical/biomed/gb-2002-3-4-research0018.txt:2
technical/biomed/gb-2002-3-4-research0019.txt:35
technical/biomed/gb-2002-3-5-research0020.txt:22
technical/biomed/gb-2002-3-5-research0021.txt:3
technical/biomed/gb-2002-3-5-research0022.txt:1
technical/biomed/gb-2002-3-5-research0023.txt:4
technical/biomed/gb-2002-3-5-research0024.txt:1
technical/biomed/gb-2002-3-5-research0025.txt:4
technical/biomed/gb-2002-3-6-research0029.txt:1
technical/biomed/gb-2002-3-6-software0001.txt:5
technical/biomed/gb-2002-3-7-research0032.txt:69
technical/biomed/gb-2002-3-7-research0035.txt:105
technical/biomed/gb-2002-3-7-research0036.txt:30
technical/biomed/gb-2002-3-7-research0037.txt:9
technical/biomed/gb-2002-3-8-research0038.txt:38
technical/biomed/gb-2002-3-8-research0039.txt:1
technical/biomed/gb-2002-3-8-research0040.txt:4
technical/biomed/gb-2002-3-9-research0043.txt:6
technical/biomed/gb-2002-3-9-research0044.txt:3
technical/biomed/gb-2002-3-9-research0045.txt:14
technical/biomed/gb-2002-3-9-research0046.txt:2
technical/biomed/gb-2002-3-9-research0048.txt:6
technical/biomed/gb-2002-3-9-research0049.txt:0
technical/biomed/gb-2002-3-9-research0051.txt:20
technical/biomed/gb-2002-4-1-r1.txt:1
technical/biomed/gb-2002-4-1-r2.txt:102
technical/biomed/gb-2003-4-1-r5.txt:13
technical/biomed/gb-2003-4-1-r7.txt:5
technical/biomed/gb-2003-4-2-r11.txt:33
technical/biomed/gb-2003-4-2-r14.txt:4
technical/biomed/gb-2003-4-2-r16.txt:2
technical/biomed/gb-2003-4-2-r8.txt:12
technical/biomed/gb-2003-4-2-r9.txt:18
technical/biomed/gb-2003-4-3-r17.txt:15
technical/biomed/gb-2003-4-3-r18.txt:5
technical/biomed/gb-2003-4-3-r20.txt:8
technical/biomed/gb-2003-4-4-r24.txt:2
technical/biomed/gb-2003-4-4-r26.txt:22
technical/biomed/gb-2003-4-4-r28.txt:4
technical/biomed/gb-2003-4-5-r30.txt:2
technical/biomed/gb-2003-4-5-r32.txt:17
technical/biomed/gb-2003-4-5-r34.txt:1
technical/biomed/gb-2003-4-6-r37.txt:54
technical/biomed/gb-2003-4-6-r39.txt:11
technical/biomed/gb-2003-4-6-r41.txt:0
technical/biomed/gb-2003-4-7-r42.txt:2
technical/biomed/gb-2003-4-7-r43.txt:5
technical/biomed/gb-2003-4-7-r46.txt:110
technical/biomed/gb-2003-4-8-r50.txt:2
technical/biomed/gb-2003-4-8-r51.txt:2
technical/biomed/gb-2003-4-9-r57.txt:4
technical/biomed/gb-2003-4-9-r58.txt:1
technical/biomed/gb-2003-4-9-r60.txt:6
technical/biomed/rr166.txt:34
technical/biomed/rr167.txt:16
technical/biomed/rr171.txt:52
technical/biomed/rr172.txt:64
technical/biomed/rr191.txt:58
technical/biomed/rr196.txt:0
technical/biomed/rr37.txt:0
technical/biomed/rr73.txt:14
technical/biomed/rr74.txt:2
```
In this command we looked for the count of the word "cell" in all files in the biomed folder. The output contains the full path for each file corresponding to the number of times "cell" appeared in that file.
  

Example 3:
```
almogbar@Almogs-MacBook-Pro docsearch % grep -c "public" technical/government/M
edia/Attorney_gives_his_time.txt technical/biomed/cc343.txt technical/911report
/chapter-2.txt
technical/government/Media/Attorney_gives_his_time.txt:1
technical/biomed/cc343.txt:0
technical/911report/chapter-2.txt:12
```
In this example we looked for the count of the word "public" in three spearate specific files. Similarly to example 2, the output contained the paths of each file with the number of instances of "public" in that file.
  
  
  
## Command-line Option 2: -v
**-v** returnss all the lines that do not fulfill the pattern prvided in the chosen file(s). This command is useful if we don't know precisely what we are looking for, but we know what we are not looking for. For example, if someone is looking to buy dresses online, but they don't know what kind of dress they want except for the fact that they don't like floral print dresses, it would be useful and time-efficient if they could search all dresses that don't have any floral patterns.
We use the format: grep -v <pattern> <file1> <file2> ...

Example 1:
```
almogbar@Almogs-MacBook-Pro docsearch % grep -v "a" technical/biomed/cc4.txt

  
    
      
        Introduction
        2 /FiO 
        2 /FiO 
        2 > 20%. In the present study, we
        support.
      
      
        Methods
        
          pressure (ZEEP);
          2 (FiO 
          2 1.0, PEEP 10 cmH 
          excluded (no response to NO, 
          of 10 cmH 
          the study period. FiO 
          O 
        
        
          mm/s.
          2 curves were continuously recorded on
          A ) to V 
          VD 
          A /V 
          T = 1 - (P 
          ET CO 
          2 )
          where P 
          ET CO 
          expired CO 
          2 curve. Expired CO 
          ET CO 
          A /V 
          A /V 
          pressure (RAP), V 
          (Oximetrix 3 SO 
          oxygen (PvO 
          VA /Q 
          2 ], oxygen delivery (DO 
          2 ).
          previously described technique [ 8]. Construction of
          2 O. A PEEP of 10 cmH 
        
        
          5% [ 9].
          FiO 
        
        
          Protocol
          
            2 0.85, PEEP 10 cmH 
            T 728 ± 32 ml.
          
          
          
          
            2)
          
        
        
        
      
      
        Results
        
          Among the 16 men enrolled in the study, eight were
          n = 3; orthopedic surgery, 
          n = 1; digestive surgery, 
          n = 2; neurosurgery, 
          VA /Q 
        
        
        
        
          VA /Q 
          2 /FiO 
          2 . 
          4.5 ppm for MPAP, PVRI, Q 
          VA /Q 
          2 /FiO 
        
        
          2 , VD 
          A /V 
          VA /Q 
          2 /FiO 
          A /V 
          2 /FiO 
        
        
          Effects of septic shock on dose-response
          curves
          VA /Q 
          
          2 /FiO 
          2 /FiO 
          2 /FiO 
          P = 0.047).
        
        
          curves
          2 /FiO 
          2 /FiO 
          2 /FiO 
          2 /FiO 
          2 /FiO 
          2 /FiO 
          2 /FiO 
          2 /FiO 
        
        
          ppm.
        
      
      
        Discussion
        
          curves
          2 tended to be higher (95 ± 16 
          vs 88 ± 11 mmHg), suggesting some
          epinephrine or norepinephrine tend to reinforce hypoxic
          shock.
          to confirm this interesting hypothesis.
        
        
          2 /FiO 
          2 /FiO 
          2 /FiO 
          2 /FiO 
          3, 11]. Recently, however, Lowson 
          could occur either by diffusion through the lung
        
      
    
```
Here we looked for all the lines in one file that do not contain the symbol "a" ("A" is still allowed). As we can see, there are a lot of empty lines used for spacing that are returned.
  
Example 2:  
```
almogbar@Almogs-MacBook-Pro docsearch % grep -v "e" technical/government/Gen_Ac
count_Office/ai00134.txt technical/government/Gen_Account_Office/ai2132.txt 
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:Division
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:April 2000
technical/government/Gen_Account_Office/ai00134.txt:EXECUTIVE GUIDE
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:GAO/AIMD-00-134
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:following:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:Background
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:Background
technical/government/Gen_Account_Office/ai00134.txt:1
technical/government/Gen_Account_Office/ai00134.txt:1997).
technical/government/Gen_Account_Office/ai00134.txt:2
technical/government/Gen_Account_Office/ai00134.txt:4
technical/government/Gen_Account_Office/ai00134.txt:information.
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:organizations.
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:6
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:8
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:Build a Foundation of Control and Accountability That Supports
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:3
technical/government/Gen_Account_Office/ai00134.txt:10
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:accountability.
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:monthly).
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:12
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:actions.
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:4
technical/government/Gen_Account_Office/ai00134.txt:16
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:or product cost.
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:(3)
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:(5)
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:(7)
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:could:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:18
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:5
technical/government/Gen_Account_Office/ai00134.txt:1995).
technical/government/Gen_Account_Office/ai00134.txt:6
technical/government/Gen_Account_Office/ai00134.txt:20
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:opportunity.
technical/government/Gen_Account_Office/ai00134.txt:by:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:capital);
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:and
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:could:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:22
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:7
technical/government/Gen_Account_Office/ai00134.txt:Functions (GAO/AIMD/NSIAD9843).
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:24
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:8
technical/government/Gen_Account_Office/ai00134.txt:26
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:28
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:control.
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:analysis.
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:and profitability information.
technical/government/Gen_Account_Office/ai00134.txt:30
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:by
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:and
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:32
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:34
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:36
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:38
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:capital planning.
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:9
technical/government/Gen_Account_Office/ai00134.txt:10
technical/government/Gen_Account_Office/ai00134.txt:January 1998).
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:40
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:capital planning
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:(1)
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:(5)
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:auditors.
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:11
technical/government/Gen_Account_Office/ai00134.txt:42
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:46
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:costs ��
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:•
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:48
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:1997
technical/government/Gen_Account_Office/ai00134.txt:$3,100,000
technical/government/Gen_Account_Office/ai00134.txt:(max.)
technical/government/Gen_Account_Office/ai00134.txt:$1,145,429
technical/government/Gen_Account_Office/ai00134.txt:$1,797,596
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:52
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:Accountants-www.aicpa.org
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:Financial Accounting Standards Board- www.fasb.org
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:Information Links, and Tools
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:Auditing
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:www.iibt.org
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:Information Links, and Tools
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:Bibliography
technical/government/Gen_Account_Office/ai00134.txt:1997.
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:Company
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:www.toysmart.com
technical/government/Gen_Account_Office/ai00134.txt:Riso
technical/government/Gen_Account_Office/ai00134.txt:56
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:6791986
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:P.O. Box 37050 Washington, DC 20013
technical/government/Gen_Account_Office/ai00134.txt:G Sts. NW)
technical/government/Gen_Account_Office/ai00134.txt:512-2537
technical/government/Gen_Account_Office/ai00134.txt:to:
technical/government/Gen_Account_Office/ai00134.txt:info@www.gao.gov
technical/government/Gen_Account_Office/ai00134.txt:http://www.gao.gov
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai00134.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:May 2000
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:GAO/AIMD21.3.2
technical/government/Gen_Account_Office/ai2132.txt:Introduction
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:Washington, D.C. 20548, or by calling (202) 5126000 or TDD (202)
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:Introduction
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:Background
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:(3)
technical/government/Gen_Account_Office/ai2132.txt:authorization, and
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:(5)
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:first
technical/government/Gen_Account_Office/ai2132.txt:Background
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:•
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:•
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:•
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:•
technical/government/Gen_Account_Office/ai2132.txt:and
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:•
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:and limitations.
technical/government/Gen_Account_Office/ai2132.txt:Background
technical/government/Gen_Account_Office/ai2132.txt:Background
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:4
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:Background
technical/government/Gen_Account_Office/ai2132.txt:Background
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:AccountabilityControl.
technical/government/Gen_Account_Office/ai2132.txt:6
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:Background
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:•
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:•
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:•
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:8
technical/government/Gen_Account_Office/ai2132.txt:(GAO/AIMD0021.3.1), pp. 1618.
technical/government/Gen_Account_Office/ai2132.txt:9
technical/government/Gen_Account_Office/ai2132.txt:10
technical/government/Gen_Account_Office/ai2132.txt:11
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:capability.
technical/government/Gen_Account_Office/ai2132.txt:towards full automation.
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:Authorization (Fast Pay)
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:Combining Statistical Sampling With Fast Pay
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:14
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:Controls Exist
technical/government/Gen_Account_Office/ai2132.txt:statistical sampling.
technical/government/Gen_Account_Office/ai2132.txt:$25,000 limitation of fast pay.
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:15
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:(2)
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:(3)
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:16
technical/government/Gen_Account_Office/ai2132.txt:17
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:auditors.
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:particular application.
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:18
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:19
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:JFMIP
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:(4)
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:(6)
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:(922280)
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:P.O. Box 37050 Washington, DC 20013
technical/government/Gen_Account_Office/ai2132.txt:G Sts. NW)
technical/government/Gen_Account_Office/ai2132.txt:512-2537
technical/government/Gen_Account_Office/ai2132.txt:to:
technical/government/Gen_Account_Office/ai2132.txt:info@www.gao.gov
technical/government/Gen_Account_Office/ai2132.txt:http://www.gao.gov
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
technical/government/Gen_Account_Office/ai2132.txt:
```
In this example we searched for all the lines in two specific files that do not contain the symbol "e". As we can see, the output contains the path to each file next to each line of it that was identified as not containing "e". There are a lot of paths with "nothing" next to them because they represent spaces/empty lines that were added to separate between sections in the different file texts. Java first lists all matching lines from the first file we provided as an input, then those from the second file (so the paths in the first part are all the same, and the paths in the second part are also the same, each corresponding to one file).
  

Example 3:
```
almogbar@Almogs-MacBook-Pro docsearch % grep -v "" technical/biomed/*
almogbar@Almogs-MacBook-Pro docsearch % grep -v "" technical/*/*
grep: technical/government/About_LSC: Is a directory
grep: technical/government/Alcohol_Problems: Is a directory
grep: technical/government/Env_Prot_Agen: Is a directory
grep: technical/government/Gen_Account_Office: Is a directory
grep: technical/government/Media: Is a directory
grep: technical/government/Post_Rate_Comm: Is a directory
```
Here I first attempted to search for all lines in biomed that don't have "", or an empty string. Since by the nature of String any string s is equal to s+"", no lines were foound that matched this pattern. When I tried to look for "" in technical, an error was returned because the government sub-directory has sub-directories, so java could not complete the process of searching for "" in folders that are not text files.
  
  
  
## Command-line Option 3: -A n
-A n returns the line containing the pattern as well as n lines after that line. This command can be useful in many situtations. For example, if we are looking for the definiton of something, we might want to find the word to be defined as well as the few lines afterwards since they are likely to contain the definition. Another instance we might want to use it is if we are looking for a specific quatation in a book and can only remember its beginning. Also, we might want to look for something more general that can have different descriptions. For example, if Bob is a student who wants to register for a course that uses ptyhon, he could search in the course catalog all the places the word "python" appears as well as the few sentences after the word in order to read more about the course.
We use the format: grep -A n <pattern> <file1> <file2> ...

Example 1:
```
almogbar@Almogs-MacBook-Pro docsearch % grep -A 3 "Although the evidence" technical/plos/journal.pbio.0020001.txt
        Although the evidence presented here demonstrates that there is a long way to go before
        developing countries contribute a more equitable share to the international scientific
        community, there are also reasons to be optimistic. The relative increase in the number of
        publications, especially when corrected for the amount of money available in research and
```
In this example, I knew that there is a line in the file journal.pbio.0020001.txt that starts with "Although the evidence". Thus, I used grep to find the line containing this phrase as well as the three lines following that line. I now know that there aren't any other sentences in that file that contain the string "Although the evidence" since only one result was returned.
  
  
Example 2:
```
almogbar@Almogs-MacBook-Pro docsearch % grep -A 2 "however" technical/911report
/chapter-9.txt
                all times. The FDNY requested, however, that the repeater be turned on only when it
                was actually needed because the channel could cause interference with other FDNY
                operations in Lower Manhattan. The repeater system was installed at the Port
--
                safety for the WTC complex perished in the South Tower's collapse. Clearly, however,
                the prospect of another plane hitting the second building was beyond the
                contemplation of anyone giving advice. According to one of the first fire chiefs to
--
                was destroyed by the fireball. Lights were functioning, however, and the air was
                clear of smoke.
            
--
                initiate rooftop rescues. At 8:58, however, after assessing the North Tower roof, a
                helicopter pilot advised the ESU team that they could not land on the roof,
                because"it is too engulfed in flames and heavy smoke condition."
--
                and handrails were a significant help. Several flights down, however, the evacuee
                became confused when he reached a smoke door that caused him to believe the stairway
                had ended. He was able to exit that stairwell and switch to another.
--
                70s, however, stairwells A and B were well-lit, and conditions were generally
                    normal.
            
--
                the building was hit. A group of people trapped on the 97th floor, however, made
                repeated references in calls to 911 to having heard "announcements" to go down the
                stairs. Evacuation tones were heard in locations both above and below the impact
--
                of transmission on the master handset required, however, that a second button be
                pressed. That second button was never activated on the morning of September 11.
            
--
                partially, however, on portable FDNY radios, and firefighters subsequently used
                repeater channel 7 in the South Tower.
            
--
                to reach FDNY dispatch by radio or phone. Out on West Street, however, the FDNY
                Chief of Department had already dismissed any rooftop rescue as impossible.
            
--
                responder. They were not, however, joined right away by a sizable number of fire
                companies, as units that had been in or en route to the North Tower lobby at 9:03
                were not reallocated to the South Tower.
--
                event. According to two eyewitnesses, however, one senior FDNY chief who knew that
                the SouthTower had collapsed strongly expressed the opinion that the NorthTower
                would not collapse, because unlike the South Tower, it had not been hit on a
--
                Rudimentary improvements, however, such as the addition of glow strips to the
                handrails and stairs, were credited by some as the reason for their survival. The
                general evacuation time for the towers dropped from more than four hours in 1993 to
--
                understandable, however, when considered in its context. At that moment, no one
                appears to have thought a second plane could hit the South Tower. The evacuation of
                thousands of people was seen as inherently dangerous. Additionally, conditions were
--
            It is also clear, however, that the response operations lacked the kind of integrated
                communications and unified command contemplated in the directive. These problems
                existed both within and among individual responding agencies.
--
                reported to the same ESU command post. It is unclear, however, whether non-ESU NYPD
                officers operating on the ground floors, and in a few cases on upper floors, of the
                WTC were as well coordinated.
--
                dispatch channel. Because of internal breakdowns within the department, however,
                this information was not disseminated to FDNY personnel on the scene.
            The FDNY, PAPD, and NYPD did not coordinate their units that were searching the WTC
--
                It is equally clear, however, that the Incident Command System did not function to
                integrate awareness among agencies or to facilitate interagency response.
            
```
In this example, I looked for all instances of the word "however" in a specific file a well as the two first lines following it. 
  
Example 3:
```
almogbar@Almogs-MacBook-Pro docsearch % grep -A 5 "The family" technical/biomed
/*
technical/biomed/1471-2121-2-21.txt:        The family of RGS proteins are established to interact
technical/biomed/1471-2121-2-21.txt-        with various Gα-protein subunits, thereby antagonizing
technical/biomed/1471-2121-2-21.txt-        their activities [ 13 14 15 16 17 18 24 ] . Indeed, we
technical/biomed/1471-2121-2-21.txt-        previously reported that RGS3 bound Gqα [ 9 ] , the G
technical/biomed/1471-2121-2-21.txt-        protein subunit that mediates GnRH receptor signaling [ 38
technical/biomed/1471-2121-2-21.txt-        ] . Here, we have extended those binding studies to include
--
technical/biomed/1471-2164-2-6.txt:        family. The family includes the Y-linked 
technical/biomed/1471-2164-2-6.txt-        DAZ genes that are present only in
technical/biomed/1471-2164-2-6.txt-        great apes and old world monkeys [ 3 ] , and the autosomal 
technical/biomed/1471-2164-2-6.txt-        DAZL1 (DAZ-like 1) and BOULE genes [
technical/biomed/1471-2164-2-6.txt-        4 5 ] in all mammals. Deletion of the 
technical/biomed/1471-2164-2-6.txt-        DAZ genes is found in about 10% of
--
technical/biomed/1471-2210-2-4.txt:        9-cis retinoic acid. The family of
technical/biomed/1471-2210-2-4.txt-        retinoic acid receptors includes those that bind only 
technical/biomed/1471-2210-2-4.txt-        all-trans retinoic acid (RAR α,β,γ
technical/biomed/1471-2210-2-4.txt-        and those that bind either 
technical/biomed/1471-2210-2-4.txt-        all-trans retinoic acid or 
technical/biomed/1471-2210-2-4.txt-        9-cis retinoic acid (RXR α,β,γ Since

```
Since I looked for the phrase "The family" in all text files in biomed, each line returned (5 + the one with "The family") is placed in the output to the right of the path of the file that it is from. Whenever we use string with more than one file, we will always get the path of the file next to the result so we know exactly what output corresponds to each file.
