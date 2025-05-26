# aws-eks-deployment
1. create an EC2 server with ubuntu
2. Connect to EC2 and install awscli,kubectl,eksctl
kubectl – A command line tool for working with Kubernetes clusters. 
eksctl – A command line tool for working with EKS clusters.
awscli – A command line tool for working with AWS services.(EKS)

=================================
Step-by-Step: Install kubectl
===============================

1. Download the latest kubectl binary
curl -LO "https://dl.k8s.io/release/$(curl -Ls https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
2. Make it executable
chmod +x kubectl
3. Move it to your system path
sudo mv kubectl /usr/local/bin/
4. Verify the installation
kubectl version --client

=================================
Step-by-Step: Install eksctl
===============================

1. Download the latest release
curl --silent --location "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" -o eksctl.tar.gz
2. Extract the archive
tar -xzf eksctl.tar.gz
3. Move the binary to /usr/local/bin
sudo mv eksctl /usr/local/bin/
4. Verify the installation
eksctl version

=================================
Step-by-Step: Install awscli
===============================

1. Update packages
sudo apt-get update
2. Install unzip and curl (if not already installed)
sudo apt-get install -y unzip curl
3. Download the AWS CLI v2 installer
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
4. Unzip the installer
unzip awscliv2.zip
5. Run the installer
sudo ./aws/install
6. Verify the installation
aws --version
