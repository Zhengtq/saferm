# What is saferm?
A safe deletion script to prevent you from wrongly delete important files in your linux system.
# How it works?
Everytime when you delete a file, it actually move the file to a hidden folder named .saferm_xxx_yyy in the same location where you delete. xxx means the timastamp when you delete, yyy is a random number. This hidden folder will keep for serveral days(which is depended on your appointament) before it is trully deleted. So you can restore your deleted files within the keepping time of the file.
# How to use it?
After you clone our project, there are two ways to use it
### First way
To put the two scripts in your /usr/bin/ folder, then to alias rm='saferm' to use it.
### Second way
To put the two scripts in wherevery you want, then to add the path to your PATH system environment. Finally to alias rm='saferm' to use it.
### The useful command
To delete a file.
```bash
rm xxx
```
The file xxx will keep in serveral days.

To delete a file right now.
```bash
rm -now yyy
```
The file yyy will keep in a very short time.

For safety concerns, to use * to delete is restricted.If you want to use 'rm * ' to delete everything in your folder, you can use the following command.
```bash
rm -all *
```

# Personal Customization
Firstly you can decide how long you want to the deleted file to be kept. You can edit the 'saferm' file, then modify the 'KEEP_TIME_LONG' variable to the time(second) you want to set.
If you want to delete the file right now, you can set the variable 'KEEP_TIME_INSTANT' in the script 'saferm'.




















