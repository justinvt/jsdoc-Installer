Installation Instructions for jsdoc toolkit
==================================================

Checkout the repository

    git clone https://github.com/SparkartGroupInc/jsdoc-Installer
    
Copy the repository to a convenient location on your machine.  You may immediately
move the directory "jsdoc-toolkit" inside the repository to wherever you'd like, 
but take note of where you've placed it.  You'll need this in a sec.

    mkdir -p /Users/sparkartguy/dev/jsdoc/
    cp jsdoc-Installer/jsdoc-toolkit /Users/sparkartguy/dev/jsdoc/

For this example, we'll I copied it to **/Users/sparkartguy/dev/jsdoc/jsdoc-toolkit**.  From now on
I'll refer to that path as **JSDOC_ROOT**.

Go back to the root jsdoc folder, where you'll see a script "install_jsdoc."  Run this as root.

    sudo install_jsdoc

You will be asked a series of questions about how you'd like the system to operate.
The only answer that actually matters for the installation to be successful is:

    "Where has the jsdoc toolkit been installed?"

The answer to this question is **JSDOC_ROOT** path mentioned above (once again, in our example
 it would be **/Users/sparkartguy/dev/jsdoc/jsdoc-toolkit**).  You should also note what your answer is to:

    "Where should jsdoc documentation be output?"

This is where compiled documentation will end up after it's been created.  If you choose the default, the output will be
sent to the jsdoc-toolkit directory mentioned above  (**/Users/sparkartguy/dev/jsdoc/jsdoc-toolkit**), in a subdirectory 
named "out".


Using the jsdoc script
----------------------------------

After the install script has completed, restart the terminal.  You now have access to the "jsdoc" command.  Find a piece of javascript with jsdoc
compatible commentary in it, and try running the following

```bash
jsdoc my_script.js
```

**NOTE: replace my_script.js with the actual name of your javascript file or a directory containing javascript**

If the documentation has been compiled successfully, you will now find an "index.html" file in the directory you chose to output documentation to.
In our case, that was **/Users/sparkartguy/dev/jsdoc/jsdoc-toolkit/out**.  Opening that file in a browser will show you the finalized jsdoc documentation
in html for your project.

Enjoy!