nuget
==========

LanguageLab code packages are available via Nuget on Github Packages.

Setting up nuget
================

Create an access token on github for the package repository.
<!-- https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line#creating-a-token -->

Copy the ClearTextPassword and add it and your user name to the command below to create an entry for the github package repo in your global nuget.config file - C:\Users\maharryd\AppData\Roaming\NuGet

nuget sources add -name "github" -Source https://nuget.pkg.github.com/<account>/index.json -Username <user> -Password <PAT>

<!-- See https://help.github.com/en/github/managing-packages-with-github-packages/configuring-dotnet-cli-for-use-with-github-packages for full details -->

Installing Packages
===================

Simply add a package to your csproj file as you would any other nuget package and run dotnet restore. If nuget is set up correctly it will check the github package repo for your packages after the main nuget server.