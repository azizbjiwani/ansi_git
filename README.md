# ansi_git  
ansible to setup git over ssh  
echo "# ansi_git" >> README.md  
git init  
git add README.md  
git commit -m "first commit"  
git remote add origin https://github.com/azizbjiwani/ansi_git.git  
git push -u origin master  
  
ansible-playbook install_git.yaml --extra-vars="hostname=git"  

