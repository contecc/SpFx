# SpFx
**How to Setup SpFx Developer Workstation**

Note: Why version specific?  Using the Latest version of Node (v14) with the
latest Gulp (3.9.1) will result in an error scaffolding. 
I have succesfully tested Node 10.x with Gulp
3.9.1 and Yoman 3.1.0

**Install Node**
https://nodejs.org/en/download/
Previous Releases > Node.js 10.x  (node-v10.24.1-x64)
(a reboot is NOT needed)
Open a Cmd Prompt (Admin NOT needed)
Verify/Check the Node and NPM Version (node -v   and   npm -v)

**Install Gulp**
npm install -g gulp@3.9.1
Verify/check the gulp version (gulp -v)

**Install Yeoman**
npm install -g yo@3.1.0
Verify/check the yeoman version (yo -v)

**Install Yeoman - SharePoint Generator (Allows scaffolding of Spfx Projects)**
npm install -g @microsoft/generator-sharepoint

Note: Trust Dev Cert >  You can't run the trust gulp trust-dev-cert command
unless you are running in a scaffolded Spfx project.  So...First, create an
SpFx project

**Create a Spfx Project Folder**
cd \   (go to root)
md code (make a code folder)
cd code (navigate to the code folder)
md hello-world (make a hello-world folder to host the project)
cd hello-world (navigate to the code\hello-world folder)

**Scaffold the project**
Type YO and then choose the @microsoft/sharepoint generator or do it all in
one line as follows:  yo @microsoft/sharepoint
Take all the defaults

**Trust the Dev Cert**
gulp trust-dev-cert
Answer 'OK' to the popup

**Test the SharePoint Workbench**
gulp serve
