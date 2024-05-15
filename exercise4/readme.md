ansible webservers -m ansible.builtin.yum -a name=httpd state=present -i inventory.yaml --become
ansible webservers -m ansible.builtin.yum -a name=httpd state=present -i inventory.yaml --become
ansible webservers -m ansible.builtin.yum -a name=httpd state=absent -i inventory.yaml --become 
ansible webservers -m ansible.builtin.service -a name=httpd state=started enabled=yes -i inventory.yaml --become
ansible webservers -m ansible.builtin.copy -a src=/home/ubuntu/vprofile/exercise4/test-script.sh dest=/tmp/my-scripts -i inventory.yaml --become
