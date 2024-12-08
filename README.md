# E-Commerce Platform Deployment with Git, Linux, and AWs
This project is about developing an e-commerce website for a new online marketplace named 'Marketpeak.
## Implementing Version Control with Git
## Initialize Git Repository
- Creating a new directory for the MarketPeak_Ecpmmerce with `mkdir` syntax
![mkdir](./img/1.1.1-mkdir-ecomm.png)
- Change to MarketPeak_Ecommerce directory with `cd` syntax.
![cd](./img/1.12-chdir-ecom.png)
- Initializing using `git Init` syntax.
![initialization](./img/1.13-init-git.png)
## Obtaining the E-commerce website template.
- The website template was downloaded and stored in the created directory
![downloaded website](./img/1.14-downloaded-website.png)
## Stage and commit the Template to Git.
- Add all created files to remote repository using `git add .` synatx.
![git_add](./img/1.21-git-add.png)
- Setting git global configuration.
![git_config_user.name](./img/1.22-git-conf-name.png)
![git_config_user.mail](./img/1.23-git-conf-mail.png)
- commit all added files
![git_commit](./img/1.24-git-commit.png)
## Create and push code to Github repository.
- creating a remote ropository on gitup account
![gitup_rep](./img/1.29-repo-create-on-remote.png)
- linking Gitup to local machine.
![git_remote_add](./img/1.25-add-remote.png)
- Push all added files with `git push -u origin mai` syntax.
![git_push](./img/1.28-git-push.png)
# AWS Deployment
## setting uo an AWS EC2 instance
- create ec2 instance.
![EC2 instance](./img/2.11-instances%20created%20and%20running.png)
- Change user mode for EC2 read only `chmod 400` syntax
![chmod-400](./img/2.12-chmod-400.png)
- Connecting to an ec2
![connect_ec2](./img/2.13-connect-to-instance.png)
## Cloning the repository on the linux server using SSH
- Generating SSH key pair using `ssh-keygen` syntax
![ssh_keypair](./img/2.14-ssh-keygen.png)
- Displaying and copy the public key
![pub_keygen](./img/2.15-cat-ssh-pub.png)
- Adding SSh public key to Gitup account.
![add_ssh_gitup](./img/2.21-copy-ssh-key-to-gitup.png)
- installing git command
![install_git](./img/2.17-sudo-install-git.png)
- cloning the gitup account
## Installing web server on EC2
![clone_gitup](./img/2.16-git_clone.png)
- Installing apache httpd server
![install_httpd](./img/2.25-install%20apache.png)
- Configuring apache httpd server
![configure](./img/2.23-sudo%20rm%20httpd.png)
- Applying apache configuration and reload
![Appply_configure](./img/2.24-sudo%20systemctl-reload.png)
## Accessing website from browser.
- Web browser was opened with public ip of my EC2.
# Continuous Integration and Deployment workflow
To accomondate workflow for developing, testing  anf deploying, version control is created using the following procedure.
## Developing new features
- Creating a new branch using `git branch` syntax
![development_branch](./img/3.1-create-new-branch-development.png)
- Switching to new branch using `git checkout development` syntax
![switch_to_development_branch](./img/3.2-switch-to-development.png)
- Adding new features to the website
![Add_features_development_branch](./img/3.3-new-features-added.png)
- Staging my changes
![git_add](./img/3.4-add-new-files-to-development-branch.png)
- Commit new update.
![git_commit](./img/3.5-commit-development-change.png)
- Create pull request.
![git_push_origin](./img/3.6-push-to-remote-dev-branch.png)
- Switch back to main branch
![git_checkout](./img/3.7-switch-to-main.png)
- Merging pull request into main.
![git_merge](./img/3.8-merge-change%20to%20main.png)
- Pushing the merge changes.
![git_push_origin](./img/3.9-push.png)
-pulling the latest change on the server
![git_pull_origin](./img/3.11-git_pull_origin_main.png)
- Restarting the web server
![git_checkout](./img/3.10-server-reloded.png)
## Testing the new changes
- The new change was observed when the web browser was restarted and it was an expected change.

# Challenges:
During the period of the capstone, I had challenge with commands on after connecting to the server, I needed to install git using `sudo yum` syntax. Also, at interval my server disconnected after launching the web page which makes the web page disappear. This does not provide opportunity for me to explore my website. Additionally, I used Ubuntu(oracle VM) which crashes after some minutes connection is made to the Ec2 server.  I later use git bash for the project which seems ok. Lastly, I realize I had to change the repositoty directory after cloning to the EC2 server which makes me to start over again. 
