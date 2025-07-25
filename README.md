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
➜  openstack-ansible-os_glance git:(glancebarbican-bz-2118763) ✗ git status
On branch glancebarbican-bz-2118763
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   templates/glance-api.conf.j2
```

```
➜  openstack-ansible-os_glance git:(glancebarbican-bz-2118763) git review         
remote: 
remote: Processing changes: refs: 1, updated: 1        
remote: Processing changes: refs: 1, updated: 1        
remote: Processing changes: refs: 1, updated: 1        
remote: Processing changes: refs: 1, updated: 1, done            
remote: commit 5f2a7d7: warning: subject >50 characters; use shorter first paragraph        
remote: commit 5f2a7d7: warning: too many message lines longer than 72 characters; manually wrap lines        
remote: 
remote: SUCCESS        
remote: 
remote:   https://review.opendev.org/c/openstack/openstack-ansible-os_glance/+/955891 Enable Barbican Secrets Support for Glance in OpenStack Compute        
remote: 
To ssh://review.opendev.org:29418/openstack/openstack-ansible-os_glance.git
 * [new reference]   HEAD -> refs/for/master%topic=glancebarbican-bz-2118763
➜  openstack-ansible-os_glance git:(glancebarbican-bz-2118763)
```

<p align="center">
  <img src="https://github.com/NileshChandekar/upstream-code-contrib/blob/main/images/4.png" alt="Logo" style="display: block; margin: 0 auto;"/>
</p>


---

✨ Contributing to OpenStack was a rewarding experience! Once everything is set up, the workflow becomes smoother over time.

Happy Hacking! 💻

