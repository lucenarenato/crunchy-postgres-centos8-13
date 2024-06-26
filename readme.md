# Docker Postgres 13
## ERROR: Couldn't find env file: env
`cp .env.example .en`
WARNING: The DEV_DB_PRIMARY_PASSWORD variable is not set. Defaulting to a blank string.
WARNING: The DEV_DB_ROOT_PASSWORD variable is not set. Defaulting to a blank string.


# crunchy-postgres
Custom crunchy-postgres with postgresql extensions for supabase compatibility

# Build Docker image
``` bash
docker buildx build \
    --push --platform linux/amd64 \
    --build-arg BUILD_DATE=$(date -u +'%Y-%m-%dT%H:%M:%SZ') \
    --build-arg VCS_REF=$(git rev-parse --short HEAD) \
    --tag quay.io/wundercomm/wundercomm-postgres:latest \
    --tag quay.io/wundercomm/wundercomm-postgres:centos8-supabase-14.2-0 .
```