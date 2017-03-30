# GrabSpotlightImages

If you like the "spotlight" images that are displayed on the Windows 10 lock screen and would like
to be able to use them in a slide show on your Windows desktop, this program can help.

The program is written in Synergy .NET, so you will need a Synergy .NET development environment
in order to build the code.

Each time it is executed the program looks in the special folder where Windows saves copies of the
recent spotlight images (and other miscellaneous images) and searches for JPEG images that are
over a certain size and in a landscape orientation. Matching files are copied to another folder to
preserve them.

The program checks if the user has OneDrive configured, and if so it will copy the files to:

    \<*OneDriveFolder*\>\\SpotlightImages

Otherwise it will copy the files to:

    \<*Pictures*\>\\SpotlightImages

As files are copied to the target folder the names of the files are recorded in a text file
named index.txt. As files are copied the program first checks index.txt to make sure the file
has not already been provided. If found the file will not be copied. This mechanism makes it
possible to delete any images that you don't like and they will not be re-copied the next time
the program runs.

Once you have the images in the target folder, you can use the "Personalize Desktop" tool to
specify that a slideshow of the images in the folder be displayed on your desktop.

You can run this program periodically to update the images. Personally I defined a scheduled
task that runs the program each time I log in to Windows. That way any new imagas just start
appearing on my desktop.

Enjoy!

Steve Ives