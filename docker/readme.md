# Commande

## Remove all containers and its volume 

> docker image prune

## Removing images according to a pattern

### list

> docker images -a |  grep "pattern"

### remove 

> docker images -a | grep "pattern" | awk '{print $1":"$2}' | xargs docker rmi

## Remove all images

### list

> docker images -a

### remove 

> docker rmi $(docker images -a -q)

## Removing volumes

## Remove one or more specific volumes

### list

> docker volume ls

### remove 

> docker volume rm volume_name volume_name

## Remove dangling volumes

### list 

> docker volume ls -f dangling=true

### remove 

> docker volume prune

