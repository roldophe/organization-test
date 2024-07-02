# organization-test
```bash
#!/bin/bash

# Check if there are unstaged changes in the repository
if [ -n "$(git status --porcelain)" ]; then
    # Add all changes to the index
    git add .
    
    # Commit the changes with a timestamp-based message
    git commit -m "Auto commit $(date +'%Y-%m-%d %H:%M:%S')"
    
    # Push changes to the remote
    git push
else
    echo "No changes to commit. Exiting."
fi
