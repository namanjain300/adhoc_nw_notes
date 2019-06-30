# Hadoop v2
* HDFS -> to distribute more data with much more speed
* YARN -> Programmable distributed framework which does the job in multiple systems with same code in a single machine and gets the output in single machine of all the systems

**NOTE:-** If you have lost the key of nany aws instance then create a AMI image of that instance and make a new OS and then choose or create a key.

```Python program of Pandas and for data visualize is  in Google Colab```

## Pandas
* Python based Machine library
* Convert different format type into a common type which is called ```Data Frame```
* It is used for Data manipulation and data analysis
* It imports Excel file data

### Data Visualize

* Matplotlib
* SeaBorn-> It can be integrated with Pandas
* gplot
* mpld3

### Seaborn
* For installing Seaborn and Pandas in RedHat
```
pip3 install pandas seaborn
```

---

# Cloud

---
# Redhat
for accessing websites from dns 

```vi /etc/resolve.conf```
```

```
Make a file immutable(not changeable) even for root and for disable use ```-i```; i= immutable
```
chattr +i /etc/resolve.conf
```
for checking the immutable files 
```
lsattr
```

### Chrony(NTP= Network Time Protocol)[Chrony is for RHEL 8 and NTP is for RHEL 7]

```
yum install chrony
```
```
systemctl restart chronyd
systemctl enable chronyd
```
```
rpm -qc chrony
```
```vi chrony.conf```

```
chronyc
```

### **Swap:- For making HDD memory as a RAM**

check memory
```
free -m
```
firstly make a partition 
then format it to swap format

```
mkswap /dev/vde
```
for mounting
```
swapon /dev/vde
```
for unmount
```
swapoff /dev/vde
```
for UUID
```
blkid /dev/vde
OR
lsblk --output=UUID /dev/vde
```
now entry in fstab
```
UUID=_UUID_   swap   swap  defaults 0 0
```

For Extending Partition size at run time (increasing 100 MB in current storage); -r= formats automatically with current formated type
```
lvextend --size +100M /dev/saksham/shubham 
OR
lvextend --size +100M /dev/saksham/shubham -r
```
for formatting new memory which appends in current memory
```
xfs_growfs /dev/saksham
```
for formatting new storage with exist storage format just except xfs format
```
resize2fs
```


