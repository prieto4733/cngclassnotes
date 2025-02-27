# Lab 13

---

1a. I have two repos in my list. In the first repo there is 19,363 packages available and in the second there is 9,285 packages 
    available

2. I have all the repos except for the two I have that are disabled. 

3. To enable and disable repos just run enablerepo=<repoid> or disablerepo=<repoid>

4a. I have 1380 total packages

4b. I have 96 packages installed that are related to python

4c. The command that I used to find the answer for 4a is: 
   
```bash
    rpm -qa | wc -l
```

To find the answer for 4b is:

```bash
    rpm -qa | grep python | wc -l
```

5a. Thunderbird resides in repo: rhel-8-for-x86_64-appstream-rpms

5b. Version: 91.3.0 Release: 2.el8.4 Architecture: x86_64 Size: 100M

5d. Thunderbird did not have any dependencies or upgrade requirements

6a. Guile does need dependencies.

6b. When trying to remove gc it tried to remove guile too.

