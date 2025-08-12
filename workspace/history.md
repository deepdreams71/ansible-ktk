    1  ls -altr
    2  cd .ssh/authorized_keys 
    3  cat  .ssh/authorized_keys 
    4  ls -latr
    5  cat .ssh/authorized_keys 
    6  ls -latr
    7  ssh-keygen 
    8  cat .ssh/id_rsa.pub 
    9  ssh-copy-id node1 
   10  ssh-copy-id node2 
   11  exit
   12  vi .ssh/authorized_keys 
   13  ansible-inventory --list
   14  cd workspace/
   15  ansible-inventory --list
   16  cat > inventory.yml <<'YAML'
all:
  vars:
    ansible_user: user
  children:
    test:
      hosts:
        node1:
          ansible_host: 91.99.225.102
    production:
      hosts:
        node2:
          ansible_host: 188.245.38.183
YAML

   17  ansible-inventory --list
   18  ansible node1 -m ping
   19  ping 91.99.225.102
   20  cat ~/.ssh/known_hosts
   21  ansible node2 -m ping
   22  ansible-config dump | grep -i INVENTORY
   23  ansible -i ./inventory.ini node2 -m ping -vvv
   24  ansible-inventory -i ./inventory.yml --host node2
   25  ansible-inventory -i ./inventory.yml --graph
   26  history
   27  ls -latr ~/.ssh/
   28  ls -latr ~/.ssh/config 
   29  cat  ~/.ssh/config 
   30  mv ~/.ssh/config  ~/.ssh/config.bkp
   31  ansible -i ./inventory.ini node2 -m ping -vvv
   32  ansible-inventory --list
   33  ssh-add --apple-use-keychain ~/.ssh/id_rsa
   34  ssh-add  ~/.ssh/id_rsa
   35  ls -latr eval "$(ssh-agent -s)"
   36  eval "$(ssh-agent -s)"
   37  ssh-add -l
   38  vi ~/.ssh/config.bkp 
   39  mv ~/.ssh/config.bkp ~/.ssh/config
   40  ansible -i ./inventory.ini node2 -m ping -vvv
   41  ssh-copy-id -i ~/.ssh/id_rsa.pub user@91.99.225.102
   42  ssh-copy-id -i ~/.ssh/id_rsa.pub user@188.245.38.183
   43  ansible -i ./inventory.ini node2 -m ping -vvv
   44  ssh -i ~/.ssh/id_rsa user@91.99.225.102 'hostname && whoami'
   45  ssh -i ~/.ssh/id_rsa user@188.245.38.183 'hostname && whoami'
   46  ansible -i ./inventory.yml node2 -m ping -vvv
   47  ansible node1 -m ping --ask-pass
   48  ansible node1 -m ping
   49   ansible-inventory --list
   50  git status
   51  git add inventory.*
   52  ansible all -m command -a 'whoami'
   53  ansible all -m command -a 'pwd'
   54  ansible all -m file -a 'path=~/ansible state=directory'
   55  ansible all -m command -a 'ls'
   56  ansible all -m command -a 'pwd'
   57  ansible all -m command -a 'tree'
   58  ansible all -m command -a '-latr'
   59  ansible all -m command -a 'ls -latr'
   60  ansible all -m command -a 'cat .ansible'
   61  ansible all -m command -a 'ls -latr .ansible'
   62  ls -altr
   63  history >> history.md
