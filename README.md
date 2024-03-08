# Pyke's Postgres YAML Manifest Based on PhoenixNAP Tutorial

Original link [here](https://phoenixnap.com/kb/postgresql-kubernetes)

Need some suggestions to make it better for deployment.

## How to use?
1. You'll need to use kubectl to run it.
2. `$ kubectl apply -f 1postgres-configmap.yaml`
3. `$ kubectl apply -f 2postgres-storage.yaml`
4. `$ kubectl apply -f 3postgres-deployment.yaml`
5. `$ kubectl apply -f 4postgres-service.yaml`
6. Or
7. `$ kubectl apply -f full-postgres.yaml`

## Notes
- By following PhoenixNAP I understand that:
  - Config Map == environment values (in Docker)
  - Storage == for Persistant Volumes (PV) and to enable a "tunnel" or "access card" for the Pods to access said volumes a.k.a Persistant Volume Claim (PVC)
  - Deployment == your Docker Image specifications
  - Service == your network
  - Full == all in one file.

## How to End?
1. `$ kubectl delete -f full-postgres.yaml`

## Workflow
1. Using [PK Rancher Server](), type `$ docker exec -it rancher-web bash` to log into your container.
2. Download it and put into `/var/lib/rancher/kubemani/postgres`.
3. Change Directory to `/var/lib/rancher/kubemani/postgres`.
4. Follow the [guide above](#how-to-use).
