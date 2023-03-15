#!/bin/bash
#-------------------------------------------------------------------------------------
# by runing this script, the files with certain extension in all the sub-directories
#         of the current working directory will be copied to new single directory
#                                 Magdy Feb, 2023
#--------------------------------------------------------------------------------------

echo ' ==========================================================================================================='
echo '   You are going to copy all the files of a certain extension in all the sub-dictories to a new directory'
echo '   Please enter the extension and the directory to copy to, or a new directory path to be created'
echo '   Warning: Pls use "absolute" directory paths, relative paths may cause failure'
echo ' ============================================================================================================'
read -p "Extension is: " extension
read -p "Path is: " path
#path=/lustre/cms/store/user/mlouka/HH_2B4L/root_files_2018UL_4mu
if [ -d "$path" ];
then
  echo '  The directory allready exist'
  echo '  Proceding to copying to the directory'
else
mkdir $path
fi
#path=/lustre/cms/store/user/mlouka/HH_2B4L/root_files_2018UL_4mu
#mkdir -p /lustre/cms/store/user/mlouka/HH_2B4L/root_files_2018UL_4mu
#mkdir $path
echo '  The' $extension files will be copied to:  $path
echo '  You can ignore the [cannot find/stat] messages for now'
echo '--------------------------------------------------------------'
echo '                      C O P Y I N G . . .                     '
echo '--------------------------------------------------------------'
for d in */*; do
 cd $d
 cp *.$extension $path
 cd ../../
 #echo $d
done
echo '-------------------------------------------------------------------------------------------------------------------------------------------------'
echo '  The messages [cp: cannot stat' *.$extension: No such file or directory], mostly were for the directories that do not contain $extension files
echo '  Copying is done to : '  $path
echo '-------------------------------------------------------------------------------------------------------------------------------------------------'

