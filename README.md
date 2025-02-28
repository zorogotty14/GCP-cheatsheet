# GCP CLI (gcloud) Cheatsheet

## **GCP CLI Overview**
Google Cloud CLI (`gcloud`) is a command-line tool used to manage resources on Google Cloud Platform (GCP).

---

## **GCP CLI Setup**
```sh
gcloud --version                 # Check gcloud version
gcloud auth login                # Authenticate with Google Cloud
gcloud config set project <project-id>  # Set active project
gcloud config list               # List current configuration
```

---

## **Project & Billing Management**
```sh
gcloud projects list             # List all projects
gcloud projects create <project-id>  # Create a new project
gcloud projects delete <project-id>  # Delete a project
gcloud billing accounts list     # List billing accounts
gcloud billing projects link <project-id> --billing-account <billing-account-id>  # Link billing account to project
```

---

## **Compute Engine (VMs)**
```sh
gcloud compute instances list     # List all VM instances
gcloud compute instances create <vm-name> --zone=<zone> --machine-type=e2-medium --image-family=debian-11 --image-project=debian-cloud  # Create a VM instance
gcloud compute instances start <vm-name> --zone=<zone>  # Start a VM instance
gcloud compute instances stop <vm-name> --zone=<zone>   # Stop a VM instance
gcloud compute instances delete <vm-name> --zone=<zone>  # Delete a VM instance
```

---

## **Cloud Storage (GCS)**
```sh
gcloud storage buckets list       # List all storage buckets
gcloud storage buckets create <bucket-name> --location=<region>  # Create a new bucket
gcloud storage cp <local-file> gs://<bucket-name>/  # Upload a file to GCS
gcloud storage rm gs://<bucket-name>/<file-name>  # Delete a file from GCS
```

---

## **Kubernetes Engine (GKE)**
```sh
gcloud container clusters list     # List all GKE clusters
gcloud container clusters create <cluster-name> --zone=<zone> --num-nodes=2  # Create a GKE cluster
gcloud container clusters get-credentials <cluster-name> --zone=<zone>  # Connect to a GKE cluster
gcloud container clusters delete <cluster-name> --zone=<zone>  # Delete a GKE cluster
```

---

## **Cloud SQL (Managed Databases)**
```sh
gcloud sql instances list         # List Cloud SQL instances
gcloud sql instances create <instance-name> --tier=db-f1-micro --region=<region>  # Create a Cloud SQL instance
gcloud sql databases create <db-name> --instance=<instance-name>  # Create a database in Cloud SQL
gcloud sql instances delete <instance-name>  # Delete a Cloud SQL instance
```

---

## **Networking (VPC & Firewall)**
```sh
gcloud compute networks list      # List all VPC networks
gcloud compute networks create <network-name> --subnet-mode=custom  # Create a new VPC
gcloud compute firewall-rules create <rule-name> --network=<network-name> --allow tcp:22  # Create a firewall rule
```

---

## **Cloud Functions (Serverless Functions)**
```sh
gcloud functions list             # List all Cloud Functions
gcloud functions deploy <function-name> --runtime=nodejs16 --trigger-http --entry-point=<entry-function>  # Deploy a Cloud Function
gcloud functions delete <function-name>  # Delete a Cloud Function
```

---

## **Cloud Logging & Monitoring**
```sh
gcloud logging logs list          # List available logs
gcloud logging read "logName=projects/<project-id>/logs/cloudaudit.googleapis.com%2Factivity" --limit=10  # Read logs
```

---

## **IAM (Identity & Access Management)**
```sh
gcloud iam roles list             # List IAM roles
gcloud projects add-iam-policy-binding <project-id> --member=user:<email> --role=roles/editor  # Assign a role to a user
gcloud projects remove-iam-policy-binding <project-id> --member=user:<email> --role=roles/editor  # Remove a role from a user
```

---

## **Cloud Pub/Sub (Messaging Service)**
```sh
gcloud pubsub topics list         # List Pub/Sub topics
gcloud pubsub topics create <topic-name>  # Create a Pub/Sub topic
gcloud pubsub subscriptions create <sub-name> --topic=<topic-name>  # Create a subscription
```

---

## **Useful GCP CLI Resources**
- [GCP CLI Documentation](https://cloud.google.com/sdk/docs/)
- [GCP CLI Command Reference](https://cloud.google.com/sdk/gcloud/reference)
- [GCP Best Practices](https://cloud.google.com/architecture/framework)

---

This cheatsheet provides a quick reference for GCP CLI (`gcloud`) commands across various services. Let me know if you have any suggestions or improvements!

