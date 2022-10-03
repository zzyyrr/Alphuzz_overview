# **Docker image**

We publish two docker images on docker hub. The size of the images are about 14.7GB.
For Unifuzz and 12-real-world binaries, we build a docker image on top of ubuntu16.04 X86.
For CGC dataset, we build a docker image on top of ubuntu16.04 i386.

![](img/9.png)

## ** docker image X86**

```bash
$ sudo docker pull yiruzhaozhao/alphuzz:artifact

$ sudo docker run --privileged -it yiruzhaozhao/alphuzz:artifact /bin/bash
```

We put the datasets binaries and initial seeds under the root directory.

![](img/10.png)


We put the Alphuzz and Alpuzzplusplus under the */home* directory. 

![](img/11.png)


## **Example**
Take Unifuzz dataset for example.

### **Alphuzz**

```bash
$ /home/Alphuzz-main/afl-fuzz -i /unifuzz/seeds/exiv2 -o /home/out -Q -- /unifuzz/binaries/exiv2 @@ 
```
![](img/12.png)
![](img/13.png)


### **Alphuzzplusplus**
```bash
$ /home/Alphuzzplusplus-main/afl-fuzz -i /unifuzz/seeds/cflow -o /home/out -Q -t 3000+ -- /unifuzz/binaries/cflow @@ 
```

![](img/14.png)
![](img/15.png)

## ** docker image i386**

```bash
$ sudo docker pull yiruzhaozhao/alphuzz:i386artifact

$ sudo docker run --privileged -it yiruzhaozhao/alphuzz:i386artifact /bin/bash
```

We put the datasets binaries, Alphuzz and Alpuzzplusplus under the */* directory. 

![](img/16.png)


## **Example**
Take Unifuzz dataset for example.

### **Alphuzz**

```bash
$ /Alphuzz-main/afl-fuzz -i ./in -o ./out -Q -- /CGC/CROMU/CROMU_00001
```
![](img/17.png)

![](img/18.png)

### **Alphuzzplusplus**

```bash
$ /Alphuzzplusplus-main/afl-fuzz -i ./in -o ./out -Q -- /CGC/CROMU/CROMU_00001
```
![](img/19.png)

![](img/20.png)
