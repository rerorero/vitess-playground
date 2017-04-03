# vitess-playground
```
pip install -r requirements.txt
vagrant up

# set up (vttablets hasn't been created yet)
ansible-playbook provision.yml

# initialize new shard
ansible-playbook new-shard.yml
```
See http://192.168.50.11:15000 with the browser.
