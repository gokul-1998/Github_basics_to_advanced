# This file will give solutions to problems i face during my development

- I added three commits which are wrong i want to revert back the commits and set the previous commit as the head  of the branch
   - Go to the desired commit `git reset --hard <commit_id>`
   - now do `git push -f origin <branch>`
   - This would make the three commits disappear.
