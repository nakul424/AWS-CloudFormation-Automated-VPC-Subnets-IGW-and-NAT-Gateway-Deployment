# 🌩️ AWS CloudFormation – Automated VPC, Subnets, IGW & NAT Gateway Deployment

This project contains an AWS CloudFormation template that **automatically creates a production-ready VPC network**, including public/private subnets, Internet Gateway, NAT Gateway, route tables, and required associations.

It is designed to give you a fully functional and scalable AWS networking foundation with zero manual configuration.

---

## 📘 Features Provisioned by the Template

✔ **VPC (Custom CIDR block)**  
✔ **Two Public Subnets**  
✔ **Two Private Subnets**  
✔ **Internet Gateway (IGW)**  
✔ **NAT Gateway** (with Elastic IP)  
✔ **Public Route Table + default route to IGW**  
✔ **Private Route Table + default route to NAT Gateway**  
✔ **Subnet associations for correct routing**

---

## 🏗️ Architecture Diagram

Below is the logical architecture represented by the CloudFormation stack:


---

## 🚀 How to Deploy the Stack

### **Method 1 — Upload via AWS Console**

1. Open AWS Console → **CloudFormation**
2. Click **Create stack**
3. Choose **Upload a template file**
4. Select `template.yaml`
5. Click **Next**, configure stack name, and deploy.

---

### **Method 2 — Deploy using AWS CLI**

Before running, configure AWS:

```sh
aws configure
Then deploy:

aws cloudformation deploy \
  --template-file template.yaml \
  --stack-name vpc-automation-stack \
  --capabilities CAPABILITY_NAMED_IAM


  🔄 Updating the Stack
aws cloudformation update-stack \
  --stack-name vpc-automation-stack \
  --template-body file://template.yaml
readme.md[+] [unix] (05:29 01/01/1970)


🧹 Delete Stack
aws cloudformation delete-stack \
  --stack-name vpc-automation-stack


  🎯 Purpose of This Project

This project demonstrates how infrastructure automation is achieved using AWS CloudFormation, eliminating the need for manual VPC creation and ensuring:

Consistency

Repeatability

Version-controlled infrastructure

Fast provisioning

It is suitable for students, DevOps engineers, and cloud practitioners.

🤝 Contribution

Feel free to open issues or submit pull requests to improve the template.


📜 License

This project is licensed under the MIT License.


---

If you want, I can also:

✅ Add your **architecture diagram as an image**
✅ Create a **better ASCII diagram**
✅ Add **steps with screenshots**
✅ Generate a **badge-style header for GitHub**
