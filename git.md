
 # Find commit with message
   git log --all --grep='typeahead'
  
 # Show changes in certain commit
  git show 6eeeee3d3bcca730cde2e6c55c4c874ef381b11d
  
 # Checkout certain lines in file
   git checkout -p
   
 # find all deleted/ edited/ new files
   git log --diff-filter=D --summary | grep delete
   
 # find file history by commits
   git log --all "file path"
   
 # pull with automerge using "theirs/ours"
   git pull --strategy-option theirs
