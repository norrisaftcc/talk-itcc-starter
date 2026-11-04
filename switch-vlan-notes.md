# Switch VLAN Notes (Lab)

Purpose: a small VLAN plan for a practice lab switch, and the commands to add one VLAN.

Lab only. No passwords, real hostnames, or campus configs in this file.

| VLAN | Name     | Ports      | Use                 |
|------|----------|------------|---------------------|
| 10   | STAFF    | Gi0/1-8    | Staff PCs           |
| 20   | STUDENTS | Gi0/9-16   | Student PCs         |
| 30   | PRINTERS | Gi0/17-18  | Network printers    |
| 99   | MGMT     | Gi0/24     | Switch management   |

Add one VLAN (Cisco IOS, example: VLAN 30 on port Gi0/17):

```
configure terminal
vlan 30
 name PRINTERS
interface GigabitEthernet0/17
 switchport mode access
 switchport access vlan 30
end
show vlan brief
```

Check: `show vlan brief` lists VLAN 30 with port Gi0/17.
