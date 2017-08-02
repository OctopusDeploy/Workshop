**Resources**

[https://octopus.com/downloads](https://octopus.com/downloads)

[https://octopus.com/docs/installation/installing-octopus](https://octopus.com/docs/installation/installing-octopus)

[https://octopus.com/docs/installation/installing-tentacles](https://octopus.com/docs/installation/installing-tentacles "https://octopus.com/docs/installation/installing-tentacles")

## Notes

* It is [good practice to use a user account](https://octopus.com/docs/installation/installing-octopus/permissions-required-for-the-octopus-windows-service) when installing Octopus services

## Hint

Take time to see the options available and to read the text on each page.

## Exercise - Installation

1. Unless you are installing Octopus Server on your local machine, log into the remote machine 
2. Download and Install Octopus Server. Accept the default options except for
   1. Licence key, either sign up, or use the supplied key
   2. User Account, use the account you are logged in as
   3. Database `localhost\SQLEXPRESS` for the server and `OctopusDeploy` as the database \(it does not exist\)
   4. Use `http://localhost/Octopus` for the Web Portal url
   5. Use `Admin` for the username, and choose a good password and leave the rest of the options as the default
   6. Unselect the `Automatically Check for new releases` checkbox
3. Verify that the installation was successful by going to `http://<hostname>/Octopus/`in your local browser \(ie not via remote desktop\) and logging in
4. Download and Install a Tentacle on the same machine. Accept the default options except for
   1. Thumbprint, find this at `http://<hostname>/Octopus/app#/configuration/certificates`

## Exercise - Create an environment

1. Add an new environment named `Sandpit`
2. Add a deployment target
   1. Choose `Listening Tentacle`
   2. Enter `localhost` as the hostname, and `10933` for the port
   3. Choose to `Discover` the remaining details
   4. Fill out the remaining details, giving it a name of `local` and a role of `Web`

## Exercise - Setup a project

1. Upload the sample website package via `http://<hostname>/Octopus/app#/library/packages/upload`
2. Add a new project, suggested name `Frist`
3. Add a step 



