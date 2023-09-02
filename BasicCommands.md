# Task 1
# 1. Open the home directory
```cd ~

# 2. Find the name of the folder you are in
pwd  # Output: /c/Users/Olya

# 3. Create a directory named "test1" inside this folder
mkdir test1

# 4. Move to the directory "test1"
cd test1

# 5. Create files named 1, 2, and 3 inside "test1"
touch 1 2 3

# 6. Check the contents of "test1"
ls  # Output: 1 2 3

# 7. Move back to the home directory
cd ~

# 8. Create a directory named "test2" inside the home directory
mkdir test2

# 9. Remove the directory "test2"
rmdir test2

# 10. Remove the file "2" from "test1"
rm ~/test1/2

# 11. Create a directory named "test3" and add two files to it
mkdir test3
touch ~/test3/cat ~/test3/dog

# 12. Remove the directory "test3"
rm -rf test3

# 13. Create a directory named "test4"
mkdir test4

# 14. Move files 1 and 3 from "test1" to "test4"
mv ~/test1/1 ~/test4
mv ~/test1/3 ~/test4

# 15. Add three lines to file "1"
echo "line1" > ~/test4/1
echo "line2" >> ~/test4/1
echo "line3" >> ~/test4/1

# 16. View the contents of file "1"
cat ~/test4/1  # Output: line1, line2, line3

# 17. Add three lines to file "3"
echo "black line" > ~/test4/3
echo "blue line" >> ~/test4/3
echo "pink line" >> ~/test4/3

# 18. View the contents of files "1" and "3"
cat ~/test4/1 ~/test4/3  # Output: Merged contents of both files

# 19. Edit file "1" using nano editor
nano ~/test4/1

