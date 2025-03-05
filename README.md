# Cellulose-builder_mac
Work-around for running cellulose-builder in Apple silicon Mac I did


# setting up dependency
## VMD, NAMD, Octave, gnu-sed (!)
VMD and NAMD can be installed from https://www.ks.uiuc.edu. Set PATH for them.
Octave and gnu-sed can be installed via homebrew.

# modify cellulose-builder/I-beta.sh and others
If you've got an error as following, that might be due to the differences in sed command in mac and other platform.
'''
sed: 1: "auxiliary_script_for_sed": command a expects \ followed by text
 Program aborted due to error during octave execution. Octave returned non-zero exit status!
'''

# Modify I-beta.sh (and others if necessary) to use gsed instead of sed
Change all sed commands to gsed in I-beta.sh (and others if you need).
And run cellulose-buider.sh for testing
'''
cellulose-builder.sh fibril 5 # to check if cellulose-builder can run properly
'''
