# openshift-kvm
How to build an openshift origin cluster on Ubuntu using kvm

#1. Configure laptop

- Verify that hardware virtualization is enabled (needs to return greater than 0):

```egrep -c '(svm|vmx)' /proc/cpuinfo```
 
- Install required packages :

```sudo apt-get install qemu-kvm libvirt-bin bridge-utils virt-manager```

- Add user to libvirtd group :

```sudo adduser $(whoami) libvirtd```

- Log out and back in and verify that your uer has permission to run kvm commands (should return empty list of vm's):

```virsh -c qemu:///system list```


#2. Configure o/s install

- Download Centos 7 dvd iso (google is your friend)
