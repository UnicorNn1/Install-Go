# Install-Golang
## Download the Go distribution for Linux from the official website. For example, you can use the following command to download Go version 1.18rc1:

```bash
wget https://golang.org/dl/go1.18rc1.linux-amd64.tar.gz
```
Extract the downloaded archive to the desired installation location. For example, you can use the following command to extract the archive to the `/usr/local` directory:
```bash
sudo tar -xvf go1.18rc1.linux-amd64.tar.gz -C /usr/local
```
Add the Go `bin` directory to your `PATH` environment variable. For example, you can add the following line to your `~/.bashrc` file:
```bash
export PATH=$PATH:/usr/local/go/bin
```
Verify the installation by checking the Go version. You should see the version number that you installed:
```bash
go version
```
### This will install the Go compiler and tools on your system. You can then use the `go` command to compile and run Go programs.

Note: The above instructions are for a Linux system. The installation process may be different for other operating systems. You can find the official installation instructions for other operating systems on the Go website.

In addition, the above instructions are for installing a specific version of Go (1.18rc1). If you want to install a different version, you can replace the version number in the `wget` command and the archive filename with the desired version number.
For example, to install Go version 1.17rc2, you can use the following commands:
```bash
wget https://golang.org/dl/go1.17rc2.linux-amd64.tar.gz
sudo tar -xvf go1.17rc2.linux-amd64.tar.gz -C /usr/local
export PATH=$PATH:/usr/local/go/bin
go version
```
This will install Go version 1.17rc2 on your system. You can use the `go` command to compile and run Go programs with this version.
# Or [install Go](https://go.dev/doc/install) (also known as Golang) 
## Install Golang for Linux/Ubuntu
To install Golang on a Linux/Ubuntu system, you can follow these steps:

First, update your system packages:
```bash
sudo apt update
```
Install the required dependencies:
```bash
sudo apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev curl libbz2-dev
```
Download the latest Golang release from the official website:
```bash
wget https://golang.org/dl/go1.18rc1.linux-amd64.tar.gz
```
Extract the downloaded archive to the `/usr/local` directory:
```bash
sudo tar -xvf go1.18rc1.linux-amd64.tar.gz -C /usr/local
```
Set the `GOPATH` environment variable. This is the directory where your Go workspace will be located. You can add the following line to your `~/.bashrc` file:
```bash
export GOPATH=$HOME/go
```
Add the Go `bin` directory to your PATH environment variable. You can add the following line to your `~/.bashrc` file:
```bash
export PATH=$PATH:/usr/local/go/bin:$GOPATH/bin
```
Apply the changes to your current session:
```bash
source ~/.bashrc
```
Verify the installation by checking the Go version:
```bash
go version
```
This will install Golang on your Linux/Ubuntu system. You can now use the `go` command to compile and run Go programs.
## Note: The above instructions are for a Linux/Ubuntu system. The installation process may be different for other operating systems. You can find the official installation instructions for other operating systems on the Go website.
install [Golang](https://go.dev/doc/tutorial/getting-started)
## Install Golang
```bash
cd $HOME 
wget "https://golang.org/dl/go$ver.linux-amd64.tar.gz" 

sudo rm -rf /usr/local/go 
sudo tar -C /usr/local -xzf "go$ver.linux-amd64.tar.gz" 
rm "go$ver.linux-amd64.tar.gz"

echo "export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin" >> $HOME/.bash_profile
source $HOME/.bash_profile
```
## Install Go 
```bash
rm -rf $HOME/go
sudo rm -rf /usr/local/go
cd $HOME
curl https://dl.google.com/go/go1.20.5.linux-amd64.tar.gz | sudo tar -C/usr/local -zxvf -
cat <<'EOF' >>$HOME/.profile
export GOROOT=/usr/local/go
export GOPATH=$HOME/go
export GO111MODULE=on
export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin
EOF
source $HOME/.profile
go version
```








