FROM alpine:latest

RUN apk add --no-cache curl bash

CMD while true; do \
    echo "Checking google.com at $(date)"; \
    if curl -s --head https://www.google.com | head -n 1 | grep "200 OK" > /dev/null; then \
        echo "Server is UP"; \
    else \
        echo "Server is DOWN"; \
    fi; \
    sleep 60; \
done
