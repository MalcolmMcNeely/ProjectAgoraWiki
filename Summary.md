Project Agora is an bespoke internet forum board catered for World of Warcraft guilds. In addition to basic forum requirements there is a need to build guild specific tools for raid and information management.

##Setting Azure Artifact Feed
Left-pad was the Chernobyl of the internet. We'll be using the artifact feed **Agora-latest** as our intermediate nuget and npm server. Package.locks should only contain references to our artifact feed. 

If you have just set your npm registry, whether by default or by profile, you may need to do the following if you have already added reference to npmjs.org to your package.lock:
* nuke *node modules* folder in your project directory
* nuke *npm cache* in wherever-that-lives (default is app roaming)
* nuke *package.lock* 
* run *npm cache clean --force* 
* run *npm install*.
