# login to ceph dashboard
Normally password for admin user should be set in the secret ````rook-ceph-dashboard-password````

Didnt work for me, had to create the admin user manually using the ceph toolbox pod and the ceph cli:
```` bash #in the toolbox pod
[rook@rook-ceph-tools-555c879675-x6vkn ~]$ vi pw.txt
[rook@rook-ceph-tools-555c879675-x6vkn ~]$ ceph dashboard ac-user-create admin -i pw.txt
[rook@rook-ceph-tools-555c879675-x6vkn ~]$ ceph dashboard ac-user-add-roles admin administrator
````
