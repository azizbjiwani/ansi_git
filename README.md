# ansi_git  
ansible to setup git over ssh  
echo "# ansi_git" >> README.md  
git init  
git add README.md  
git commit -m "first commit"  
git remote add origin https://github.com/azizbjiwani/ansi_git.git  
git push -u origin master  
  
https://opensource.com/article/17/8/ansible-environment-management    
ansible-playbook install_git.yaml --extra-vars="hostname=git"  
[ec2-user@ip-172-31-43-65 git]$ ansible-playbook install_git.yaml -i hosts  
[ec2-user@ip-172-31-43-65 git]$ ansible-playbook user_setup_with_params.yaml -i hosts --extra-vars="username=git"  
[ec2-user@ip-172-31-43-65 git]$ ansible-playbook initialize_git.yaml -i hosts --extra-vars="git_base_dir=/home/git/ project=newgitproject"  
[ec2-user@ip-172-31-43-65 git]$ ansible-playbook install_ssh_keys.yaml -i hosts --extra-vars="username=git"  
  
#checkout the code and contribute to project  
[ec2-user@ip-172-31-43-65 delete]$ git clone ssh://git@ip-172-31-38-150/home/git/newgitproject  
Cloning into 'newgitproject'...  
warning: You appear to have cloned an empty repository.  
[ec2-user@ip-172-31-43-65 delete]$ ls -l  
drwxrwxr-x 3 ec2-user ec2-user 4096 Aug 11 00:29 newgitproject  
[ec2-user@ip-172-31-43-65 delete]$ ls -lrht newgitproject/  
total 0  
[ec2-user@ip-172-31-43-65 delete]$  
  
[ec2-user@ip-172-31-43-65 delete]$ cd newgitproject  
[ec2-user@ip-172-31-43-65 newgitproject]$ touch test.txt  
[ec2-user@ip-172-31-43-65 newgitproject]$ git add test.txt  
[ec2-user@ip-172-31-43-65 newgitproject]$ git commit -m "first commit of test.txt"  
[ec2-user@ip-172-31-43-65 newgitproject]$ git commit --amend --reset-author  
