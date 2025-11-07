# Eshare for personal use

This is .deb file of EShare from its official website that is being modified by me for personal use.

# How-To modifying .deb file

1. Download the .deb file
2. create empty directory '''mkdir eshare''' then '''cd eshare/''' 
4. extract the .deb file with '''ar x ../<file_name>'''
5. create empty directory the same as the file that will be extracted '''mkdir <folder_name>''' '''cd <folder_name>/''' 
6. extract tar file (control or data) with '''tar -xJf <file_name> -C <folder_name>'''
7. edit as much as you like
8. compress the file into tar again with '''tar -cJf ../<file_name> ./*''' (e.g ''' tar -cJf ../control.tar.xz '''
9. recreate the .deb file with ''' ar rcs <file_name>.deb debian-binary control.tar.xz data.tar.xz'''
10. install the .deb file with ''' dpkg -i <file_name>.deb ''' 
