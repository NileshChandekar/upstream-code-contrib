```
Author: Nilesh Chandekar
Technical Architect
```

---

# How I Started My First Upstream `OpenStack` Code Contribution

## 🛠️ Tools Used:

- [Launchpad](https://bugs.launchpad.net/)
- [OpenDev Gerrit](https://review.opendev.org/)
- `git`
- `git review`
- `reno`
- `python venv`

## 📖 References:

- [OpenStack Contributor Guide - Gerrit Setup](https://docs.openstack.org/contributors/es_MX/common/setup-gerrit.html)
- [RENO Usage Guide](https://docs.openstack.org/reno/latest/user/usage.html)
- [Developer Certificate of Origin (DCO)](https://docs.openstack.org/contributors/es_MX/common/dco.html#dco-setting-up-your-git-configuration)

## 🚀 Steps Followed:

1. **Identified a Bug or Feature** via Launchpad.
3. **Cloned the Corresponding Repository** from OpenDev.
4. **Created a Python Virtual Environment** for dependency isolation.
5. **Made the Necessary Code Changes.**
6. **Tested Locally** to ensure stability.
7. **Generated Release Notes** using `reno`.
8. **Committed Changes** with proper formatting.
9. **Pushed to Gerrit** using `git review`.
10. **Addressed Review Comments** and got the patch merged. ✅


---

<p align="center">
  <img src="https://github.com/NileshChandekar/upstream-code-contrib/blob/main/images/1.png" alt="Logo" style="display: block; margin: 0 auto;"/>
  <img src="https://github.com/NileshChandekar/upstream-code-contrib/blob/main/images/2.png" alt="Logo" style="display: block; margin: 0 auto;"/>
  <img src="https://github.com/NileshChandekar/upstream-code-contrib/blob/main/images/3.png" alt="Logo" style="display: block; margin: 0 auto;"/>
</p>


# Glance Contribution


```bash
(myenv) ➜  gitprojects # git clone https://opendev.org/openstack/openstack-ansible-os_glance.git
(myenv) ➜  gitprojects 
(myenv) ➜  gitprojects cd openstack-ansible-os_glance    
(myenv) ➜  openstack-ansible-os_glance git:(glancebarbican-bz-2118763) 
(myenv) ➜  openstack-ansible-os_glance git:(glancebarbican-bz-2118763) 
(myenv) ➜  openstack-ansible-os_glance git:(glancebarbican-bz-2118763) ls
bindep.txt        defaults  examples  LICENSE         meta        releasenotes  tasks      tests    Vagrantfile  zuul.d
CONTRIBUTING.rst  doc       handlers  manual-test.rc  README.rst  run_tests.sh  templates  tox.ini  vars
(myenv) ➜  openstack-ansible-os_glance git:(glancebarbican-bz-2118763) 
```

```diff 
+  master
  remotes/gerrit/master
  remotes/gerrit/stable/2024.1
  remotes/gerrit/stable/2024.2
  remotes/gerrit/stable/2025.1
  remotes/gerrit/unmaintained/2023.1
  remotes/gerrit/unmaintained/zed
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
  remotes/origin/stable/2024.1
  remotes/origin/stable/2024.2
  remotes/origin/stable/2025.1
  remotes/origin/unmaintained/2023.1
  remotes/origin/unmaintained/zed
```
```bash
git checkout glancebarbican-bz-2118763
```

```diff
+ glancebarbican-bz-2118763
  master
```

```bash
(myenv) ➜  openstack-ansible-os_glance git:(glancebarbican-bz-2118763) vi releasenotes/notes/glance_barbican_integration-f493d11d6343e3c0.yaml  
```

```bash
(myenv) ➜  openstack-ansible-os_glance git:(glancebarbican-bz-2118763) ✗ git status
On branch glancebarbican-bz-2118763
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   releasenotes/notes/glance_barbican_integration-f493d11d6343e3c0.yaml

no changes added to commit (use "git add" and/or "git commit -a")
(myenv) ➜  openstack-ansible-os_glance git:(glancebarbican-bz-2118763) ✗ 
```

```bash
(myenv) ➜  openstack-ansible-os_glance git:(glancebarbican-bz-2118763) ✗ git add .
(myenv) ➜  openstack-ansible-os_glance git:(glancebarbican-bz-2118763) ✗ 
```

```bash
(myenv) ➜  openstack-ansible-os_glance git:(glancebarbican-bz-2118763) ✗ git status
On branch glancebarbican-bz-2118763
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   releasenotes/notes/glance_barbican_integration-f493d11d6343e3c0.yaml

(myenv) ➜  openstack-ansible-os_glance git:(glancebarbican-bz-2118763) ✗ 
```

```bash
(myenv) ➜  openstack-ansible-os_glance git:(glancebarbican-bz-2118763) ✗ git commit --amend                                                     
[glancebarbican-bz-2118763 6e30534] Enable Barbican Secrets Support for Glance in OpenStack Compute
 Date: Fri Jul 25 17:23:52 2025 +0530
 3 files changed, 22 insertions(+)
 create mode 100644 releasenotes/notes/glance_barbican_integration-f493d11d6343e3c0.yaml
(myenv) ➜  openstack-ansible-os_glance git:(glancebarbican-bz-2118763) 
```



```bash
(myenv) ➜  openstack-ansible-os_glance git:(glancebarbican-bz-2118763) git review                                                             
remote: 
remote: Processing changes: refs: 1, updated: 1        
remote: Processing changes: refs: 1, updated: 1        
remote: Processing changes: refs: 1, updated: 1, done            
remote: commit 6e30534: warning: subject >50 characters; use shorter first paragraph        
remote: 
remote: SUCCESS        
remote: 
remote:   https://review.opendev.org/c/openstack/openstack-ansible-os_glance/+/955891 Enable Barbican Secrets Support for Glance in OpenStack Compute        
remote: 
To ssh://review.opendev.org:29418/openstack/openstack-ansible-os_glance.git
 * [new reference]   HEAD -> refs/for/master%topic=glancebarbican-bz-2118763
(myenv) ➜  openstack-ansible-os_glance git:(glancebarbican-bz-2118763) 

```

<p align="center">
  <img src="https://github.com/NileshChandekar/upstream-code-contrib/blob/main/images/4.png" alt="Logo" style="display: block; margin: 0 auto;"/>
</p>


---


# Maskari Contribution

<p align="center">
  <img src="Masakari" alt="Logo" style="display: block; margin: 0 auto;"/>
</p>


<p align="center">
  <img src="https://github.com/NileshChandekar/upstream-code-contrib/blob/main/images/Screenshot%20from%202025-08-12%2019-49-24.png" alt="Logo" style="display: block; margin: 0 auto;"/>
</p>


```
└─[$]> cd openstack-ansible-os_masakari/
└─[$]> git branch 2120450  
└─[$]> git checkout 2120450
```

```
└─[$]> cd tasks 
└─[$]> ls -lhrt 
total 20K
-rw-rw-r-- 1 nileshchandekar nileshchandekar 3.2K Jul 28 12:44 masakari_post_install.yml
-rw-rw-r-- 1 nileshchandekar nileshchandekar  797 Jul 28 12:44 masakari_db_sync.yml
-rw-rw-r-- 1 nileshchandekar nileshchandekar 7.6K Jul 28 12:44 main.yml
-rw-rw-r-- 1 nileshchandekar nileshchandekar 2.4K Aug 12 19:11 masakari_pre_install.yml
┌─[nileshchandekar@cnilesh] - [~/Downloads/gitprojects/openstack-ansible-os_masakari/tasks] - [Tue Aug 12, 19:12]
└─[$]> 
```

```
└─[$]> vi masakari_pre_install.yml
```

```
diff --git a/tasks/masakari_pre_install.yml b/tasks/masakari_pre_install.yml
```

```
index e449eee..31d4a80 100644
--- a/tasks/masakari_pre_install.yml
+++ b/tasks/masakari_pre_install.yml
@@ -31,6 +31,14 @@
     createhome: "yes"
     home: "{{ masakari_system_user_home }}"
 
+- name: Add masakari user to libvirt Group
+  ansible.builtin.user:
+    name: "{{ masakari_system_user_name }}"
+    groups: "{{ libvirt_group }}"
+    append: "yes"
+  tags:
+    - masakari-config
+
 - name: Create masakari dir
   ansible.builtin.file:
     path: "{{ item.path | realpath }}"
(END)

```

### Documentation 

```
┌─[nileshchandekar@cnilesh] - [~/Downloads/gitprojects] - [Tue Aug 12, 19:17]
└─[$]> source myenv/bin/activate
```

```
└─[$]> reno new Add_Masakari_User_to_Libvirt_Group
no configuration file in: ./releasenotes/config.yaml, ./reno.yaml
Created new notes file in releasenotes/notes/Add_Masakari_User_to_Libvirt_Group-a0fc38ba3a53dd7f.yaml
(myenv) ┌─[nileshchandekar@cnilesh] - [~/Downloads/gitprojects/openstack-ansible-os_masakari] - [Tue Aug 12, 19:19]
```

```
└─[$]> vi releasenotes/notes/Add_Masakari_User_to_Libvirt_Group-a0fc38ba3a53dd7f.yaml
```

```
└─[$]> cat  releasenotes/notes/Add_Masakari_User_to_Libvirt_Group-a0fc38ba3a53dd7f.yaml
---
fixes:
  - |
    Added the Masakari user to the libvirt group to ensure proper permissions
    for accessing libvirt resources. This resolves permission issues that could
    prevent Masakari from monitoring and managing virtual machine instances
    effectively. The fix ensures that the Masakari service can successfully
    interact with the libvirt daemon for instance evacuation and recovery
    operations during host failures.
(myenv) ┌─[nileshchandekar@cnilesh] - [~/Downloads/gitprojects/openstack-ansible-os_masakari] - [Tue Aug 12, 19:22]
└─[$]> 
```

```
(myenv) ┌─[nileshchandekar@cnilesh] - [~/Downloads/gitprojects/openstack-ansible-os_masakari] - [Tue Aug 12, 19:23]
└─[$]> git status
On branch 2120450
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   tasks/masakari_pre_install.yml

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	releasenotes/notes/Add_Masakari_User_to_Libvirt_Group-a0fc38ba3a53dd7f.yaml

no changes added to commit (use "git add" and/or "git commit -a")
(myenv) ┌─[nileshchandekar@cnilesh] - [~/Downloads/gitprojects/openstack-ansible-os_masakari] - [Tue Aug 12, 19:23]
└─[$]> 
```

```
└─[$]> git add .
```

```
└─[$]> git status 
On branch 2120450
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   releasenotes/notes/Add_Masakari_User_to_Libvirt_Group-a0fc38ba3a53dd7f.yaml
	modified:   tasks/masakari_pre_install.yml

└─[$]> 
```

```
└─[$]> git commit
[2120450 4b1325b] Add masakari user to libvirt Group
 2 files changed, 17 insertions(+)
 create mode 100644 releasenotes/notes/Add_Masakari_User_to_Libvirt_Group-a0fc38ba3a53dd7f.yaml
(myenv) ┌─[nileshchandekar@cnilesh] - [~/Downloads/gitprojects/openstack-ansible-os_masakari] - [Tue Aug 12, 19:30]
└─[$]> 
```

```
└─[$]> git review 
Creating a git remote called 'gerrit' that maps to:
	ssh://cNilesh@review.opendev.org:29418/openstack/openstack-ansible-os_masakari.git
Your change was committed before the commit hook was installed.
Amending the commit to add a gerrit change id.
remote: 
remote: Processing changes: refs: 1, new: 1        
remote: Processing changes: refs: 1, new: 1        
remote: Processing changes: refs: 1, new: 1, done            
remote: commit 518e4cc: warning: too many message lines longer than 72 characters; manually wrap lines        
remote: 
remote: SUCCESS        
remote: 
remote:   https://review.opendev.org/c/openstack/openstack-ansible-os_masakari/+/957142 Add masakari user to libvirt Group [NEW]        
remote: 
To ssh://review.opendev.org:29418/openstack/openstack-ansible-os_masakari.git
 * [new reference]   HEAD -> refs/for/master%topic=2120450
(myenv) ┌─[nileshchandekar@cnilesh] - [~/Downloads/gitprojects/openstack-ansible-os_masakari] - [Tue Aug 12, 19:32]
└─[$]> 
```



<p align="center">
  <img src="https://github.com/NileshChandekar/upstream-code-contrib/blob/main/images/Screenshot%20from%202025-08-12%2019-49-09.png" alt="Logo" style="display: block; margin: 0 auto;"/>
</p>

---



✨ Contributing to OpenStack was a rewarding experience! Once everything is set up, the workflow becomes smoother over time.

Happy Hacking! 💻

