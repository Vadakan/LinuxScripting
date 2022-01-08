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




