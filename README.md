# bedrock-wsl
Instructions for a bedrock walkthrough on wsl

#### System:
Windows
Version 1909 
Build: 18363.535

#### WSL:
Ubuntu WSL 18.04

Directory example:
`C:\Users\me\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows...`

#### Unzip
```
sudo apt-get install unzip zip 
```

#### Fabrikate
```
mkdir tmp
cd tmp
wget https://github.com/microsoft/fabrikate/releases/download/0.17.3/fab-v0.17.3-linux-amd64.zip 
unzip fab-v0.17.3-linux-amd64.zip
chmod +x ./fab 
```

You will need to either move the executables to `/usr/local/bin`, or modify `~/.bashrc` to add them to PATH and persist the new additions across restarts.
Example:
```
sudo cp fab /usr/local/bin
```

#### Helm
helm - use helm 2.16.1 
```
cd tmp
wget https://get.helm.sh/helm-v2.16.1-linux-amd64.tar.gz
tar xvzf helm-v2.16.1-linux-amd64.tar.gz linux-amd64/
sudo cp helm /usr/local/bin
sudo cp tiller /usr/local/bin
```

#### Terraform
```
cd tmp
wget -q https://releases.hashicorp.com/terraform/0.12.18/terraform_0.12.18_linux_amd64.zip
unzip terraform_0.12.18_linux_amd64.zip
sudo cp terraform /usr/local/bin
```

#### Kubectl
```
cd tmp
curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl
chmod +x ./kubectl
sudo cp kubectl /usr/local/bin
```

#### Azure cli
```
cd tmp
curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
```
Resource [Install Azure CLI with apt](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli-apt?view=azure-cli-latest#manual-install-instructions)