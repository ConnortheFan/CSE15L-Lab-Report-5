# Grep Variants
## grep

`grep` is a command used on the bash command-line. The most basic format for it is `grep "[keyword]" [directories]` where `[keyword]` is replaced with a string you want to search for and [directories] is the files that you want to search for that keyword. By default, grep will return the line that contains the word with the file path. By using various options, you can change how it searches or the output. These options are placed after `grep` and before the keyword. When using multiple options, you can either format them as `-l -r` or as `-lr`.

## -l

`-l` will only show the names of the files where a word match is found rather than the line with the words. It is useful if you need to find only the files containing a certain keyword without needing the exact passage itself.

![Screenshot_20230213_095414](https://user-images.githubusercontent.com/110417453/218652353-29c3a057-b0e0-4144-9d72-310ec4bb1175.png)

In this example, I needed to find the files containing the keyword `vista` within the directory `written2/travel_guides/berlitz1`. Using `-l`, I was able to keep the output short and simple for further use, such as redirecting the output into a .txt file.

![Screenshot_20230213_101641](https://user-images.githubusercontent.com/110417453/218654955-f2acd5bd-8688-43d6-a02a-6d98b1dba8e6.png)

This is another similar example, but using multiple directories. It uses the same directory as the previous example, but also the `written2/travel_guides/berlitz2` directory as well. `-l` continues to work with multiple directories, printing only the file names with `vista`.

Source: 
[Finding a File Containing a Particular Text String In Linux Server](https://www.cyberciti.biz/faq/howto-search-find-file-for-text-string/#:~:text=You%20need%20to%20use%20the,match%20or%20a%20text%20string.)

## -r

`-r` allows you to recursively search through a directory for files, rather than only being able to look through one directory. This is helpful if you have files and directories that are nested, while wanting to search through all of them.

![Screenshot_20230213_095514](https://user-images.githubusercontent.com/110417453/218652374-56a29191-270e-4caf-b7ab-26d45b859f1e.png)

In this example, I use `-r` to search through all the files within the `written2/` directory. `written2/` has multiple nested directories inside it, so using `-r` made it convenient to find `Lucayans` out of all the files and directories within.

![Screenshot_20230213_095534](https://user-images.githubusercontent.com/110417453/218652384-b4be28bc-3539-41e1-8901-d12fe71f8a44.png)

This is another example of using `-r`, but it is used in conjunction with `-l` as `-rl`. The particular order of options doesn't matter as `-lr` would work the same. This allowed me to search through all files within `written2/` and only show the file names, which helps make searching more convenient.

Source: 
[Finding a File Containing a Particular Text String In Linux Server](https://www.cyberciti.biz/faq/howto-search-find-file-for-text-string/#:~:text=You%20need%20to%20use%20the,match%20or%20a%20text%20string.)

## -n

The `-n` option shows the line number that the word is found on. You can find the line number after the file name, before the text itself. This is useful if you want to both search for the file that contains a word, but also find the exact location in that file with the word.

![Screenshot_20230213_101001](https://user-images.githubusercontent.com/110417453/218654007-e06e59c5-492f-4823-ba2d-121ac77d8142.png)

Here `-n` is used to find `vista` along with the line number that the word is on. It can be seen directly after the file name and before the line of text that contains the word. This is useful if I were to go to that file and wanted to find the word in the file exactly.

![Screenshot_20230213_101045](https://user-images.githubusercontent.com/110417453/218654043-466c82da-20c2-4df9-a5dc-2f4b4231d6df.png)

Here `-n` is being used with `-r` as `-nr` along with `--color`, which will be covered in the next section. `grep` is searching through all of `written2/` for the word `Lucayans` and with the results, the line number is shown as well, in color after the file name. The use is similar to that of `-n` and `-r`, but combined.

Source: 
[Finding a File Containing a Particular Text String In Linux Server](https://www.cyberciti.biz/faq/howto-search-find-file-for-text-string/#:~:text=You%20need%20to%20use%20the,match%20or%20a%20text%20string.)

## --color

`--color` color codes your output to make it easier for you to find various important information. It changes the color of the file name, line number, and word within the text to make it easier and faster to extract information.

![Screenshot_20230213_095845](https://user-images.githubusercontent.com/110417453/218652435-9445c3ef-e7cc-4f70-b7fb-ef9c1057422c.png)

Here `grep` is searching recursively with `-r` for the word `vistas` in `written2/`. As seen by the output, the word itself is colored red, while the file name is purple. These colors make it easier to locate the word, which would be useful if you needed to find surrounding words or to find which instances counted `vistas` or some word that contains `vista` within it coincidentally.

![Screenshot_20230213_095811](https://user-images.githubusercontent.com/110417453/218652420-b681536d-a344-4e1e-a524-54328a58ece0.png)

Here `grep` looks for `Lucayans` in `written2/` using `-r`. The line where `Lucayans` is found is displayed, but since the line is so long, it may be difficult to find the word exactly in the text. `--color` makes `Lucayans` red in the text, which draws you eyes to it and makes is extremely easy to locate it.

Source: 
[Finding a File Containing a Particular Text String In Linux Server](https://www.cyberciti.biz/faq/howto-search-find-file-for-text-string/#:~:text=You%20need%20to%20use%20the,match%20or%20a%20text%20string.)
