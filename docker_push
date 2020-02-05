#!/bin/bash

echo "$DOCKER_PASSWORD" | docker login -u "$DOCKER_USERNAME" --password-stdin

# Changelog
docker build -t $DOCKER_USERNAME/my-sample-app-changelog sample-application-db-changelog-job/
docker tag $DOCKER_USERNAME/my-sample-app-changelog $DOCKER_USERNAME/my-sample-app-changelog:develop
docker push $DOCKER_USERNAME/my-sample-app-changelog:develop

# API
docker build -t $DOCKER_USERNAME/my-sample-app-api sample-application-http-api-server/
docker tag $DOCKER_USERNAME/my-sample-app-api $DOCKER_USERNAME/my-sample-app-api:develop
docker push $DOCKER_USERNAME/my-sample-app-api:develop
