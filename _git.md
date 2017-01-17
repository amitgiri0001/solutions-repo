#Undo a commit and redo

$ git commit -m "Something terribly misguided"              (1)

$ git reset HEAD~                                           (2)

<< edit files as necessary >>                               (3)

$ git add ...                                               (4)

$ git commit -c ORIG_HEAD    


#Check for byebug and debugger "Pre-commit"

-#!/bin/sh

-#

-# Check for debugging statements before commiting your code.

-#


-# List of keywords to search for in regex format
TARGETS='byebug|debugger'

echo "Running debug check..."

RES="$(egrep -nr --include=*.rb --include=*.erb --include=*.js --include=*.haml --include=*.html  $TARGETS)"
COUNT="$(egrep -nr --include=*.rb --include=*.erb --include=*.js --include=*.haml --include=*.html  $TARGETS | wc -l)"

if [ "$COUNT" -gt "0" ]; then
  echo "\033[31m \n$RES"

  echo "\033[33m \nDebugging functions were found in your code!"
  echo "\033[31m \nChanges were not committed."
  exit 1
else
  echo "\033[32m \nNo debugger or byebug were found.  Nice job, Ace!\n";
  exit 0
fi
