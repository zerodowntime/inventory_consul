Ansibe Consul Inventory
===================


Modified version of [ansibe consul inventory](https://github.com/ansible/ansible/blob/devel/contrib/inventory/consul_io.py), allowing to create host groups similar as  `aws inventory`

**HINT:** Ensure that you have python-consul module installed

```bash
pip install python-consul
```
----------

Example:

(consul)
```
user@@ip-172-22-22-30> consul kv get -recurse
ansible/groups/zerodowntime/ip-ip-172-22-22-30/AnsibleRelease:0.0.1
ansible/groups/zerodowntime/ip-ip-172-22-22-30/AppRelease:None
ansible/groups/zerodowntime/ip-ip-172-22-22-30/InstanceID:117
ansible/groups/zerodowntime/ip-ip-172-22-22-30/Name:testvm
ansible/groups/zerodowntime/ip-ip-172-22-22-30/ServiceVersion:0
ansible/groups/zerodowntime/ip-ip-172-22-22-30/SessionId:0
ansible/groups/zerodowntime/ip-ip-172-22-22-30/Setup:dev
ansible/groups/zerodowntime/ip-ip-172-22-22-30/Space:zerodowntime
ansible/groups/zerodowntime/ip-ip-172-22-22-30/State:True
ansible/groups/zerodowntime/ip-ip-172-22-22-30/Type:None
ansible/groups/zerodowntime/ip-ip-172-22-22-30/UUID:exJgNtAKuexDvHSOlZCnVUJbbCqMlwPvXsZtBKJj
test:sample
```

(output):
 ```
 ./consul_io.py
{
  "zerodowntime": [
    "172.22.22.101",
    "172.22.22.102",
    "172.22.22.103",
    "172.22.22.104",
    "172.22.22.105",
    "172.22.22.30"
  ],
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
        "consul_nodename": "ip-172-22-22-30",
        "host_ip_addr": "172.22.22.30",
        "tag_AnsibleRelease": "0.0.1",
        "tag_AppRelease": "None",
        "tag_InstanceID": "117",
        "tag_Name": "testvm",
        "tag_ServiceVersion": "0",
        "tag_SessionId": "0",
        "tag_Setup": "dev",
        "tag_Space": "zerodowntime",
        "tag_State": "True",
        "tag_Type": "None",
        "tag_UUID": "exJgNtAKuexDvHSOlZCnVUJbbCqMlwPvXsZtBKJj"
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
   "tag_AnsibleRelease_0.0.1": [
    "172.22.22.30"
  ],
  "tag_AppRelease_None": [
    "172.22.22.30"
  ],
  "tag_InstanceID_117": [
    "172.22.22.30"
  ],
  "tag_Name_testvm": [
    "172.22.22.30"
  ],
  "tag_ServiceVersion_0": [
    "172.22.22.30"
  ],
  "tag_SessionId_0": [
    "172.22.22.30"
  ],
  "tag_Setup_dev": [
    "172.22.22.30"
  ],
  "tag_Space_zerodowntime": [
    "172.22.22.30"
  ],
  "tag_State_True": [
    "172.22.22.30"
  ],
  "tag_Type_None": [
    "172.22.22.30"
  ],
  "tag_UUID_exJgNtAKuexDvHSOlZCnVUJbbCqMlwPvXsZtBKJj": [
    "172.22.22.30"
  ]
}
```
