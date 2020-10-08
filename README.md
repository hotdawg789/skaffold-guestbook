# skaffold-example
Skaffold Example


## Steps
```
Install Skaffold 
    https://skaffold.dev/docs/install/

Install Docker
    https://docs.docker.com/engine/install/ubuntu/


point kubectl config to the cluster you want skaffold to deploy to
```

## skaffold dev 
```
bust@devm:~/skaffold-guestbook$ skaffold dev
Listing files to watch...
 - hotdawg789/nodejs-guestbook-backend
 - hotdawg789/nodejs-guestbook-frontend
Generating tags...
 - hotdawg789/nodejs-guestbook-backend -> hotdawg789/nodejs-guestbook-backend:latest
 - hotdawg789/nodejs-guestbook-frontend -> hotdawg789/nodejs-guestbook-frontend:latest
Checking cache...
 - hotdawg789/nodejs-guestbook-backend: Found Remotely
 - hotdawg789/nodejs-guestbook-frontend: Found Remotely
Tags used in deployment:
 - hotdawg789/nodejs-guestbook-backend -> hotdawg789/nodejs-guestbook-backend:latest@sha256:478cb94ade8316491fac4601304239730961d5e489fedba243c550823484fc10
 - hotdawg789/nodejs-guestbook-frontend -> hotdawg789/nodejs-guestbook-frontend:latest@sha256:b5c06dfc46e602b1c20e6cd2a12453b15ab752b0a6567ff324201125867c8f59
Starting deploy...
 - deployment.apps/nodejs-guestbook-backend created
 - service/nodejs-guestbook-backend created
 - deployment.apps/nodejs-guestbook-frontend created
 - service/nodejs-guestbook-frontend created
 - deployment.apps/nodejs-guestbook-mongodb created
 - service/nodejs-guestbook-mongodb created
Waiting for deployments to stabilize...
 - deployment/nodejs-guestbook-mongodb is ready. [2/3 deployment(s) still pending]
 - deployment/nodejs-guestbook-backend: waiting for init container init-db-ready to complete
    - pod/nodejs-guestbook-backend-8c5458fd8-bgsdb: waiting for init container init-db-ready to complete
      > [nodejs-guestbook-backend-8c5458fd8-bgsdb init-db-ready] Waiting for mongodb to start...
      > [nodejs-guestbook-backend-8c5458fd8-bgsdb init-db-ready] Waiting for connection for 2 sec.
 - deployment/nodejs-guestbook-frontend: creating container frontend
    - pod/nodejs-guestbook-frontend-85f995744-679p4: creating container frontend
 - deployment/nodejs-guestbook-frontend is ready. [1/3 deployment(s) still pending]
 - deployment/nodejs-guestbook-backend is ready.
Deployments stabilized in 9.595825594s

```