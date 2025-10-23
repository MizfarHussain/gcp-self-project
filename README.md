# gcp-self-project
This project demonstrates deploying a Dockerized Flask application to Google Kubernetes Engine (GKE) using Cloud Build for automated CI/CD.
All GCP resources (GKE, Cloud Build Trigger, and Cloud Run) were created via the Google Cloud Console.

# 🧱 Project Overview
  1. Flask app containerized with Docker  
  2. Source code hosted on GitHub  
  3. Cloud Build Trigger automates build and deployment  
  4. GKE Cluster hosts the application  
  5. Service exposes the app publicly  

# ⚙️ Setup Summary
  1. Flask App & Dockerfile
  2. Created and tested locally.
  3. Pushed to GitHub repository.
  4. Created Resources in Console
  5. GKE Cluster created in GCP Console.
  6. Cloud Build connected to GitHub repository.
  7. Build Trigger created to run on pushes to main branch.
  8. Cloud Run service configured (optional for testing).
  9. Added Configuration Files
  10. cloudbuild.yaml: Defines build and deploy steps.
  11. gke.yaml: Contains Kubernetes Deployment and Service specs.
  12. Automated Deployment
  13. On every code push, Cloud Build:
  14. Builds and pushes Docker image to GCR
  15. Deploys to GKE using kubectl apply -f gke.yaml

# 🚀 Deploy
  Once setup is done, simply push your changes:
  
  1. git add .
  2. git commit -m "Deploy updated Flask app"
  3. git push origin main


  
# 🌐 Access the App

  After deployment:
  - kubectl get svc  
  Copy the External IP from the service output and open it in your browser.
