STEP 1:

export ANSIBLE_HOST_KEY_CHECKING=False

ansible-playbook addtosudoers.yml -i hosts.yml -u cloudadmin --extra-vars "ansible_sudo_pass=password"

STEP 2:

ansible-playbook server-updates.yml -i hosts.yml

STEP 3:

ansible-playbook -i hosts.yml k8s-prereq.yml

ansible-playbook -i hosts.yml k8s-cluster.yml

STEP 4:

ansible-playbook -i hosts.yml k8s-nfs.yml

ansible-playbook -i hosts.yml k8s-metallb.yml

ansible-playbook -i hosts.yml k8s-istio.yml

ansible-playbook -i hosts.yml k8s-jenkins.yml
