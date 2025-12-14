# AWS Cloud Cost Optimization – Identifying Stale EBS Snapshots

This project implements an **AWS Lambda–based automation** to identify and delete
**stale Amazon EBS snapshots** that are no longer associated with any active EC2
instance. The goal is to reduce unnecessary storage costs and improve overall
cloud resource hygiene.

---

## 📌 Problem Statement
Over time, AWS environments accumulate unused EBS snapshots due to deleted or
detached volumes. These stale snapshots continue to incur storage costs if not
managed properly.

---

## 🎯 Solution Overview
An AWS Lambda function periodically scans all EBS snapshots owned by the account
and checks whether their associated volumes exist or are attached to active EC2
instances. If a snapshot is found to be unused, it is automatically deleted.

---

## 🏗 Architecture
1. AWS Lambda fetches all EBS snapshots owned by the account  
2. Retrieves all running and stopped EC2 instances  
3. Compares snapshot volume IDs with active volumes  
4. Deletes snapshots whose volumes no longer exist  

---

## 🔧 AWS Services Used
- AWS Lambda
- Amazon EC2
- Amazon EBS
- AWS IAM
- Amazon CloudWatch (Logs & Monitoring)

---

## 🚀 Key Features
- Fully serverless solution
- Automated identification of stale snapshots
- Reduces AWS storage costs
- Improves cloud resource efficiency
- Scalable and event-driven



