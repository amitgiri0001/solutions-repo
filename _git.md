#Undo a commit and redo

$ git commit -m "Something terribly misguided"              (1)

$ git reset HEAD~                                           (2)

<< edit files as necessary >>                               (3)

$ git add ...                                               (4)

$ git commit -c ORIG_HEAD    
