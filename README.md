# Vagrant dotnet core image

The idea of this project is to build up-to-date vagrant file for compiling linux-based .net core-enabled VM.

As you know there is no "official" vagrant file from Microsoft so let's create it!

Quick Links:

*  [Contributing](#contributing)
*  [Building VM](#building)
*  [Using VM](#using)

## <a name="contributing"></a> Contributing

Have an idea how to make the vagrant file better? The following options are available:

- Create issue with bug, enhancement or new feature requested
- Send pull request
- Let me know any other way ;)

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