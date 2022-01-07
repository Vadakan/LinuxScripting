# LinuxScripting
========================================================================================
# Input file - **new-1.txt**
What is Lorem Ipsum?
Lorem Ipsum is simply 
dummy small
DUMMY captial 
DUmmy mixed
and typesetting industry. Lorem 
Ipsum has been the industry's standard
dummy text ever since the 1500s,  
when an unknown printer took a galley of type 
and scrambled it to make a 
type specimen book. It has survived 
not only five centuries, but also the
leap into electronic typesetting, remaining
essentially unchanged. It was popularised
in the 1960s with the release of Letraset
sheets containing Lorem Ipsum passages, 
and more recently with desktop publishing 
software like Aldus PageMaker including versions of 
Lorem Ipsum.
========================================================================================
# Check for pattern irrespective of case number and get the lines
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

