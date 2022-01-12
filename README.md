# LinuxScripting
========================================================================================
# Check for pattern irrespective of Alphabhet case(lower/upper) and get the lines

grep -i "dummy" new-1.txt 


**output:**

![image](https://user-images.githubusercontent.com/80065996/148585888-9bd09e94-d93b-4c83-859f-f3adab4d5f05.png)

Pattern:

![image](https://user-images.githubusercontent.com/80065996/148587389-ea159778-b8aa-4c13-a9e0-51c26226c016.png)


# Count of lines with pattern "dummy" in the file new-1.txt

grep -c "dummy" new-1.txt

![image](https://user-images.githubusercontent.com/80065996/148585954-80ee6bb2-7cff-4186-8b3d-d57ccbe476aa.png)

Pattern:

![image](https://user-images.githubusercontent.com/80065996/148587509-2c8ae957-c3d3-4e3d-8cca-924adc3fa90a.png)


# list all the files in current directory with pattern

grep -l "dummy" *

Pattern:

![image](https://user-images.githubusercontent.com/80065996/148587570-f4faa24f-fd12-4d70-b6cd-b593347ab7fd.png)


  **Files in current directory:**
  
    ![image](https://user-images.githubusercontent.com/80065996/148586247-a43ac6bc-7e98-4629-97a8-6aa34b6b7f88.png)
    
 **** output:****
 
![image](https://user-images.githubusercontent.com/80065996/148586286-71b1cac1-9262-4975-ad2f-998a8595715e.png)

# list the files in the list of files with pattern "dummy"

grep -l "dummy" new-1.txt new-2.txt new-3.txt new-4.txt

![image](https://user-images.githubusercontent.com/80065996/148586526-f8c652a1-0606-4e82-bfe3-19602aa2fcd1.png)


# getting lines from files not matched with pattern

grep -v "dummy" new-1.txt

![image](https://user-images.githubusercontent.com/80065996/148587871-a0c1ba17-6606-41d7-b3d4-d054f8cac2b4.png)

# display lines starting with this pattern

grep "^type" new-1.txt

![image](https://user-images.githubusercontent.com/80065996/148588413-a7b29401-7e39-444a-b982-f82d480c9152.png)

# Pattern chain multiple pattern match

grep -e "an" -e "le" -e DUmmy new-1.txt

![image](https://user-images.githubusercontent.com/80065996/148588872-92b076b0-8722-4998-b4d8-d75722ff532a.png)

# getting pattern from file and search

grep -f pattern.txt new-1.txt

![image](https://user-images.githubusercontent.com/80065996/148589119-0a327a0f-81ce-49db-a1c3-e96dee4ff668.png)

![image](https://user-images.githubusercontent.com/80065996/148589149-957a3a8e-5270-41ef-adf7-6c5b2adcf9db.png)

# search for word instead of pattern

grep -w "dummy" new-1.txt

![image](https://user-images.githubusercontent.com/80065996/148589325-f7362a5e-7a92-4656-adb2-cbc3f47471ea.png)

# Print only matched part of matched line

grep -o "dummy" new-1.txt

![image](https://user-images.githubusercontent.com/80065996/148589434-29700564-5011-443b-81a9-7a790284f931.png)

# display the matched line and line number for pattern

grep -n "dummy" new-1.txt

![image](https://user-images.githubusercontent.com/80065996/148589937-e59439c6-33fb-4f8d-9640-66bc4dd621f0.png)


**"Man" command :**

It will display the helper page for the command we are having doubt

![image](https://user-images.githubusercontent.com/80065996/148650686-d2a7cd07-d326-463e-b415-954bc8997d7c.png)


![image](https://user-images.githubusercontent.com/80065996/148650670-d41c712e-1a14-4b30-9125-0baea5778fb0.png)


**CHMOD and CHOWN command for file related access settings:**

![image](https://user-images.githubusercontent.com/80065996/148650880-bdac5768-74ac-4a55-9689-d0ce393778f5.png)

![image](https://user-images.githubusercontent.com/80065996/148650924-ac54b5bd-20f9-438c-8e04-b2efdf91fb9e.png)

First character (-) denoted the file
First character (d) denotes directory
Remaining 9 characters denoted access related things

ls -la gives even hidden files (files started with dot(.))

![image](https://user-images.githubusercontent.com/80065996/148651005-0c91f75b-0ee8-4f63-87ba-6616e6cde8cb.png)

![image](https://user-images.githubusercontent.com/80065996/148651049-76928d7b-9731-4760-bef7-e380bcb6c0fa.png)

**First 3 digits -- based on user groups (read,write or execute (r,w,x))**

![image](https://user-images.githubusercontent.com/80065996/148651119-3fac7703-d742-4eb4-b838-4f13ce1ddff5.png)

total 9 Permissions -- Fisrt command user 3 permissions, next group user 3 permission, next other users - 3 permissions


For the below file, Current used has only read and write permissions.group user has only read permission. Other user has only read permission


![image](https://user-images.githubusercontent.com/80065996/148651218-c7a3e941-0ea0-4ebb-9392-a19c9abaa612.png)

Removing write permission for User (use -u flag to indicate user and -w to remove the permission)

![image](https://user-images.githubusercontent.com/80065996/148652211-4e668c21-c003-4f93-b6c6-b8f987989467.png)

**chmod ugo+w Myfile.txt - assign write permission to all user(u),group(g),others(o) **

**chmod u-w Myfile.txt - remove write permission to only user(u)**

**chmod can be done by using numbers:**
r - 4 (read)
w - 2 (write)
x - 1 (execute)

**user - rw - 4+2=6 (to give read and write permission to the user(u))**

**user - wx - 2+1=3 (to give write and execute permission to user)**

**user - r - 4=4 (to give only read permission to the user)**

**below image i gave 777 -> user(7==> 4+2+1), group(7 ==> 4+2+1), other(7 == 4+2+1)**

![image](https://user-images.githubusercontent.com/80065996/148652850-076c0c0c-c905-429f-8b8d-c00a1ff3bae5.png)


**WHOAMI - command to check the user logged in currently**

![image](https://user-images.githubusercontent.com/80065996/148686053-e90d026d-5fa7-4ba6-aef3-da9e229ff463.png)

**We can set the password to current user by below command:**


![image](https://user-images.githubusercontent.com/80065996/148686075-5c31aca3-f48c-49cd-a6a7-977337f7cbc1.png)

**Add a user to your linux operating system:**

![image](https://user-images.githubusercontent.com/80065996/148686127-11f7be0f-4914-4d2f-bba4-d6619360d5a9.png)


'Less' command := used to display contents of file one page at a time. Press button 'q' to come out of the 'Less' commmand

![image](https://user-images.githubusercontent.com/80065996/148686588-ee4691c7-ddbd-4d65-af94-40c653f12386.png)

![image](https://user-images.githubusercontent.com/80065996/148686638-8bd6103b-3250-493b-be8c-4ba031999fba.png)


![image](https://user-images.githubusercontent.com/80065996/148686651-8a84557a-7f37-4da1-ab8c-3830ebed1740.png)

**Press 'q' to come out:**

**/etc/passwd  -- folder contains user details of a linux machine**

![image](https://user-images.githubusercontent.com/80065996/148686729-0ed0cd64-04ae-4134-bfbd-77cf07b29794.png)


![image](https://user-images.githubusercontent.com/80065996/148686743-da262993-4cfc-4fe6-a1d2-b43521d64c84.png)


![image](https://user-images.githubusercontent.com/80065996/148686796-74f75998-b198-444f-9eb3-6ca34d168183.png)


**Below file has 'user' and 'group' tagged to 'lxd'. 'lxd' user and group is available in the system. we checked this by command 'ls /etc/passwd'**



![image](https://user-images.githubusercontent.com/80065996/148688720-7e27830d-de41-468b-bcc7-148b61c6d914.png)


**we are changing now with chown command
**

**we changed the user and group of "index.js" file from 'lxd' to 'root:root' root user is available in root group.**

![image](https://user-images.githubusercontent.com/80065996/148688848-a5d8107f-e5c9-49b0-a81f-bc9ddf428ece.png)

**AWK command:**

**File content:**

![image](https://user-images.githubusercontent.com/80065996/148690081-086cb2d6-c009-4e97-9988-10e597ad32fd.png)

**{print} will print all the data in the file**

![image](https://user-images.githubusercontent.com/80065996/148690093-715f3654-ce9e-4716-a1c1-6bdeb31cfc3c.png)

**{print $2} will display only second column in the file**

![image](https://user-images.githubusercontent.com/80065996/148690127-bcbeb8d6-374a-4886-8371-d8043b02cdec.png)

**display the particular row in the file**

![image](https://user-images.githubusercontent.com/80065996/148690358-cc8e82d9-69b9-48a0-8fa9-987fd8899ebb.png)

**Display paricular row and column**

![image](https://user-images.githubusercontent.com/80065996/148690505-c54d60fe-d974-406f-9627-fac054369577.png)

**to find free space in linux machine**

![image](https://user-images.githubusercontent.com/80065996/148690588-93084bfe-3fbc-43cf-a50d-5de88fc89ec1.png)

use above command in pipeline with awk command

![image](https://user-images.githubusercontent.com/80065996/148690827-3dc32569-40b5-4a80-8365-cdbc4285529f.png)

![image](https://user-images.githubusercontent.com/80065996/148690841-9a6eaabe-371c-4975-8771-eea866809b33.png)


**AWK command for .CSV files:**

![image](https://user-images.githubusercontent.com/80065996/148691143-56bbd741-cf0a-4193-b675-540aea2abeab.png)

printing 1st column displays the whole record
printing 2nd column displays the empty record because** its not able to recognize the column in .CSV file**


![image](https://user-images.githubusercontent.com/80065996/148691160-14be6052-6668-4a51-91bc-3e910695c5b9.png)


"captial F" (-F) to identify separators

![image](https://user-images.githubusercontent.com/80065996/148691258-209aaf7b-412b-4958-8deb-fb579b0851ea.png)


![image](https://user-images.githubusercontent.com/80065996/148691280-840c4a31-f36e-4c64-b744-cc8c5153e9cd.png)


# Pipeline using Linux:

# PWD has below manny files

![image](https://user-images.githubusercontent.com/80065996/149188762-6cde0000-b8a7-469a-a1c4-fbd124a7395b.png)


# first command will pass the reslt to second command in the pipeline and second command will pass the filered results to third and go on

![image](https://user-images.githubusercontent.com/80065996/149189494-ce2b1ec3-7072-414e-8e3e-734de6afb94d.png)


![image](https://user-images.githubusercontent.com/80065996/149189599-6ee7bb39-9b45-49ac-bec5-b11a4b02fdf7.png)

# Press q to quit

another example for pipeline

![image](https://user-images.githubusercontent.com/80065996/149189700-b1140c87-bb84-4cf2-a0dd-fc59ac50e36f.png)

# Another example

 ![image](https://user-images.githubusercontent.com/80065996/149190981-3d0bc694-0132-46bf-862d-c3f5b0cf4211.png)

# grep works only for files and not for directory

# how to see only uniq values in the file

**below file has duplicate value for 'row4'**

![image](https://user-images.githubusercontent.com/80065996/149191887-44ebef4b-d46f-47de-a85d-c7e1bed93914.png)

from the current directory, take all the files with pattern 'dups.txt' and find only unique values from the file by printing page by page 


![image](https://user-images.githubusercontent.com/80065996/149192559-2c653662-f6d0-4106-b3f2-c436d1aaffc7.png)



![image](https://user-images.githubusercontent.com/80065996/149192232-1bf45063-74fa-45b8-947c-a106fa6bd22b.png)


![image](https://user-images.githubusercontent.com/80065996/149192607-b34980e4-8da8-43ac-89c6-9a0afe25419d.png)








