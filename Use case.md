# Use case

### Untrack files which are already added in gitignore file
#### Scenario  
    Files were added (or push to remote git repository) before adding to `.gitignore` file.
#### Solution
    ````bash
    git rm -r --cache <path-to-file>
    git rm -r --cache .
    
    // add <path-to-file> to `.gitignore` file
    git add <path-to-file>
    git add .
  
    git commit -m 'fix .gitignore'
    git push origin main
    ````