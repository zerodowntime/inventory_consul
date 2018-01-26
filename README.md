Ansibe Consul Inventory
===================


 Modified version of [ansibe consul inventory](https://github.com/ansible/ansible/blob/devel/contrib/inventory/consul_io.py), allowing to create host groups similar as  `aws inventory`

* HINT: * Ensure that you have python-consul module installed 

```bash
pip install python-consul
```
----------
    
Example:

(consul)
```
consul kv get -recurse
ansible/groups/zerodowntime/c2/Space:els
ansible/groups/zerodowntime/c2/name:router
ansible/groups/zerodowntime/c2/setup:dev
ansible/groups/zerodowntime/c2/state:active
ansible/groups/zerodowntime/c5/Setup:prod
test:sample
```

(output):
 ```
 ./consul_io.py
{
  "_meta": {
    "hostvars": {
      "172.22.22.101": {
        "consul_datacenter": "zerodowntime",
        "consul_nodename": "c1",
        "consul_services": [
          "consul"
        ]
      },
      "172.22.22.102": {
        "consul_datacenter": "zerodowntime",
        "consul_nodename": "c2",
        "consul_services": [
          "consul"
        ]
      },
      "172.22.22.103": {
        "consul_datacenter": "zerodowntime",
        "consul_nodename": "c3",
        "consul_services": [
          "consul"
        ]
      },
      "172.22.22.104": {
        "consul_datacenter": "zerodowntime",
        "consul_nodename": "c4"
      },
      "172.22.22.105": {
        "consul_datacenter": "zerodowntime",
        "consul_nodename": "c5"
      },
      "172.22.22.30": {
        "consul_datacenter": "zerodowntime",
        "consul_nodename": "kotewa.zerodowntime.pl"
      }
    }
  },
  "all": [
    "172.22.22.101",
    "172.22.22.102",
    "172.22.22.103",
    "172.22.22.104",
    "172.22.22.105",
    "172.22.22.30"
  ],
  "consul_servers": [
    "172.22.22.101",
    "172.22.22.102",
    "172.22.22.103"
  ],
  "tag_Setup_prod": [
    "172.22.22.105"
  ],
  "tag_Space_els": [
    "172.22.22.102"
  ],
  "tag_name_router": [
    "172.22.22.102"
  ],
  "tag_setup_dev": [
    "172.22.22.102"
  ],
  "tag_state_active": [
    "172.22.22.102"
  ],
  "zerodowntime": [
    "172.22.22.101",
    "172.22.22.102",
    "172.22.22.103",
    "172.22.22.104",
    "172.22.22.105",
    "172.22.22.30"
  ]
}
```
 
    
