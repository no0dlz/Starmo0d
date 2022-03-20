Starmo0d

The main repository of my Stardev Valley Mods.


Mainly used for sharing objects between my mod repositories.


#########################
########## USAGE ########
#########################

1. Create a new GIT repository
2. Navigate to it

3. Add this repository as submodule
   git submodule add https://github.com/no0dlz/Starmo0d.git

4. Open the new Project in VS.

5. Go to your Project settings under Build -> Events
6. Add the following lines to the Pre Build Event:
   ------------------------------------
   if not exist "$(SolutionDir)Starmo0d\" (
       mkdir "$(SolutionDir)\Starmo0d"
   )

   for /F %%i in ('dir /b "$(SolutionDir)Starmo0d\*.*"') do (
       cd $(SolutionDir)Starmo0d\
       git remote show origin
       git checkout master
       goto :EOF
   )
   
   cd $(SolutionDir)\
   git submodule update --init --recursive --remote
   ------------------------------------
   
   
