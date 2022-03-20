Starmo0d

The main repository of my Stardev Valley Mods.


Mainly used for sharing objects between my mod repositories.


#########################
########## USAGE ########
#########################

1. Create a new GIT repository
2. Navigate to it

3. Add this repository as submodule
   



((( OLD OLD OLD )))
3. Add this repository as remote:
   git remote add -f Starmo0d-Base https://github.com/no0dlz/Starmo0d.git

4. Add the subtree to the new repository:
   git subtree add --prefix Starmo0d Starmo0d-Base master --squash


5. To update the subtree (best is to update before every build):
   git fetch Starmo0d-Base master
   git subtree pull --prefix Starmo0d Starmo0d-Base master --squash