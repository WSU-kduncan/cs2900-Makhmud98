# Investigate container networking.  

- For Docker, for example, there exists three networking modes - host, none, and bridge.
- For the two engines of your choice (of which Docker can be one choice) state:
### What networking mode(s) are supported and their capabilities?  
Docker: Bridged, Host Mode, Container Mode.
LXC   : Bridged, Router
### What networking mode is used by default?  
Docker: Bridged
LXC   : Bridged
### How to run the container and bind a host port to the container port
Docker:  
``` Docker container run -p 8080:80 -d containerName ```  
LXC   :  
``` lxc config device add containerName port80 proxy listen=tcp:0.0.0.0:80 connect=tcp:localhost:80 ```  

# Investigate vulnerability scanners.  


## Find a Dockerfile linter (command line tool or VSCode plugin)  
- https://hadolint.github.io/hadolint/
### What best practices does it search for?  

### Find a scanner that can scan images for vulnerabilities. You can use Aqua Trivy or something else  
-https://aquasecurity.github.io/trivy/v0.17.0/

### Does it have any limits on what can be scanned?  
- Trivy Scans for Three Artifacts (Container Images, File Systems, Git Repositories)  
### What types of vulnerabilities are scanned? 
- Voulnerabilities of OS packages and application dependencies.   