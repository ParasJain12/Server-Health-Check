### Pipeline Script

#!/bin/bash

#Check if server is down
if docker logs health-check --tail 10 | grep -q "Server is DOWN"; then
    echo "Server is down!"
    exit 1
else
    echo "Server is up!"
    exit 0
fi

### ChatGPT Link: https://chatgpt.com/share/68c81f98-1404-8012-a076-2603b5c503ba
