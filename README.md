Installation Instructions for jsdoc toolkit
==================================================

Checkout the repository

    git clone https://github.com/SparkartGroupInc/jsdoc-Installer
    
The primary working component of the jsdoc install is in the root of the repo, under the directory "jsdoc-toolkit".  
You may copy this directory to another location on your machine, or you may keep it exactly where it is.  
If you do move it, remember where, as you'll need to provide the installer with that path during setup.

**NOTE: If you install jsdoc with this script, and then move the jsdoc-toolkit later on, jsdoc will cease to function properly.  This is why you should move it NOW if you don't like running code directly from the repo**

Go back to the root of our repository and list the contents.

    cd REPO_PATH

    ls

You'll see a script "install_jsdoc."  Run this as root.

    sudo install_jsdoc

You will be asked a series of questions about how you'd like the system to operate.
The only answer that actually matters for the installation to be successful is:

    "Where has the jsdoc toolkit been installed?"

The answer to this question is the path to jsdoc-toolkit which we asked you to remember above (only if you've moved it).  If you haven't moved it, selecting the default will work just fine.


You should also note what your answer is to:

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

Making changes later on
--------------------------------

The installation script does two things:

* Creates the default config file that jsdoc will use in the future.
* Writes the executable jsdoc using the values you provided during the installation

If you want to change the configuration resulting from this process, you may either rerun in install script, or
remember where you told the installer to place the config file, and edit that manually.  On OS X, it should default to

    ~/.jsdoc/jsdoc.conf

You may also wish to make changes to the default flags used by the **jsdoc** executable.  To view the contents of this script and/or make changes,
try:

    sudo vi `which jsdoc`

If you completely ruin everything, I suggest rerunning the **install_jsdoc** script, which should always produce a usable base config.

Enjoy!!

Enjoy!