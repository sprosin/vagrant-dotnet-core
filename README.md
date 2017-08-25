# Vagrant dotnet core VM

The idea of this project is to build up-to-date vagrant file for compiling linux-based .net core-enabled VM.

As you know there is no "official" vagrant file from Microsoft and Docker images are provided instead. However, current version of Docker for Windows runs on 64bit Windows 10 only! The idea of this repository is to provide an easy option to test .net core apps in linux environment.

Quick Links:

*  [Contributing](#contributing)
*  [Prerequisites](#prerequisites)
*  [Building VM](#building)
*  [Using VM](#using)

## <a name="contributing"></a> Contributing

Have an idea how to make the vagrant file better? The following options are available:

- Create issue with bug, enhancement or new feature requested
- Send pull request
- Let me know any other way ;)

## <a name="prerequisites"></a> Prerequisites

- [Virtual Box](https://www.virtualbox.org/)
- [Vagrant](https://www.vagrantup.com/downloads.html)
- [Vagrant Omnibus](https://github.com/chef/vagrant-omnibus) to install chef on VM
- [Vagrant Berkshelf Plugin](https://github.com/berkshelf/vagrant-berkshelf) to track chef package dependencies

## <a name="building"></a> Building VM

````
c:\projects> git clone https://github.com/sprosin/vagrant-dotnet-core.git
c:\projects> cd vagrant-dotnet-core\
c:\projects> vagrant up
````

## <a name="running"></a> Using VM

````
c:\projects\vagrant-dotnet-core> vagrant ssh
ubuntu@dotnetcore:~$ dotnet --version
ubuntu@dotnetcore:~$ cd src
ubuntu@dotnetcore:~/src$ mkdir consoleApp
ubuntu@dotnetcore:~/src$ cd consoleApp
ubuntu@dotnetcore:~/src/consoleApp$ dotnet new console
ubuntu@dotnetcore:~/src/consoleApp$ dotnet run
Hello World!
````
