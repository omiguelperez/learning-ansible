# 03 - Inventories

Hostnames or hostnames list to run ansible commands and playbooks

## Groups

To run **hostname** command under `groupname` host group, type `ansible -i inventory groupname|anothergroupname -a hostname`

```ini
[groupname]
hostname1 xxx.xxx.xx.xxx
hostname2 xxx.xxx.xx.xxx

[anothergroupname]
anotherhostname1 xxx.xxx.xx.xxx
anotherhostname2 xxx.xxx.xx.xxx
anotherhostname3 xxx.xxx.xx.xxx
```

## Groups of groups

To run **hostname** command under group of groups, type `ansible -i inventory groupofgroups -a hostname`

```ini
[groupofgroups:children]
groupname
anothergroupname
```

## Inventories directory

Run all inventories in specific directory, type `ansible all -i inventories -a hostname`

```
+
|--- inventories
|---|
    |--- aws               --> this file contains hosts
    |--- digitalocean      --> this file contains hosts
|--- inventory
|--- README.md
```

