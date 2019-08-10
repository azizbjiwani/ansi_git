# ansi_git  
ansible to setup git over ssh  
echo "# ansi_git" >> README.md  
git init  
git add README.md  
git commit -m "first commit"  
git remote add origin https://github.com/azizbjiwani/ansi_git.git  
git push -u origin master  
  
ansible-playbook install_git.yaml --extra-vars="hostname=git"  
[ec2-user@ip-172-31-43-65 git]$ ansible-playbook install_git.yaml -i hosts  
[ec2-user@ip-172-31-43-65 git]$ ansible-playbook user_setup_with_params.yaml -i hosts --extra-vars="username=git"  

