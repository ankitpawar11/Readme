# Readme

# Assignment 2

This project is made with the intention to automate the application dashboard.

## Import the project to the workspace

### Cloning a Project from Git:
- Cloning a remote repository will copy a repository from Git to your local file system.

- To clone a remote repository first, click Import from File on the Welcome to Provar screen.
- Then, select Clone URI and click Next.
Enter the information as follows:

1. URI: The complete URI of the remote repository or the path on the file system. This field is automatically synchronized with the other fields.
2. Host: The name of the remote host
3. Repository Path: Path to the remote repository
4. Protocol: The following Protocols are supported:
5. file: File system access to the repository
6. ftp: File Transfer Protocol
7. git: The most efficient built-in git protocol (default port 9418). This protocol doesn’t provide authentication. Typically used for anonymous read access to the repository
8. http: Hypertext Transfer Protocol can be tunneled through firewalls
9. https: Hypertext Transfer Protocol Secure can be tunneled through firewalls
10. sftp: SSH File Transfer Protocol
11. ssh: Git over secure shell (SSH) protocol. Typically used for authenticated write access to the repository
12. Port: Port number
13. User: The username used for authentication
14. Password: The password used for authentication
Store in Secure Store: Whether the password is saved in the Eclipse secure store

- Click Next. 
- The Branch Selection screen will display branches available in the repository. If you have multiple repositories, select the one which contains your project.
- Click Next.
- Click Browse to select the workspace.
- Click Next.
- Click Finish to import the project.


## Troubleshooting some common issues:

#### Test case steps do not display:

- If you notice that on opening a test case, the test steps are not getting displayed with the error:
  ##### The Test API is not available. Please check that its Test Plug-in is started in the Test Plug-ins view:

- This implies that for some reason the Provar Test Plug-in – Salesforce APIs is not running correctly.
- To resolve this, you need to Refresh and Recompile your test project following the steps below:

  ###### Step 1: Click on the Tools menu.

  ###### Step 2: Click Refresh and Recompile sub-menu.

- After this process is done, restart Provar and you will have the test plugin in a running state. Now you can open up your test cases and verify that you can now see the test steps just fine.

#### In the problem section if you see Bundled ‘com.provar.core.model.base’ cannot be resolved in MANIFEST file error:

- Remove the configuration part from the target file (can be found in 
  the .metadata folder). Search for *.target in the .metadata folder, 
  open each target file and remove the configuration path and save the 
  file. 
- Restart Provar and check

#### Error while opening project "Problem occurred while trying to save the state of workbench":

- This could be because of a corrupted workspace that is used for 
  multiple versions. The solution would be to delete the .metadata 
  folder and then re-import the project or create a new workspace

#### Class file is not getting created in the bin folder so the user is not able to see the Page object in the test case: 

- Delete the bin folder from the Project Location and refresh the 
  project. Then Refresh & Recompile the project.

- In the .testproject file check for connection duplication ( multiple 
  tags 
  <connectionClasses> ). If multiple connections are observed, remove 
  those.
- If the above does not resolve the issue, try changing the Java version 
  from the build path.

#### Duplicate callable test case registered with id in the Problem section:

- Delete the errors from the Problems section.
- Restart Provar.
- Refresh and Recompile the project.

#### Missing external jars in the build path results to compile failure:

- Add the missing external jars in the build path

#### Provar licensing issue:

[Refer to this link for license-related issue](https://www.provartesting.com/documentation/licensing-provar/activating-your-license/)

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## Authors and acknowledgment
This project is created by Ankit Pawar


