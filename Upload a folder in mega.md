---
type: 
tags: mega
category: work
for_inteview: 
creation_date: 2023-07-03 18:02
modification_date: 2023-07-03 18:02
---

Current Folder : 




[[03-07-2023]]

To upload a local folder to a mega cloud folder using megacmd in terminal Linux, you can use the mega-put command, which takes a local path and a remote path as arguments. For example, to upload a folder named /home/user/myfolder to a folder named /backup in your MEGA account, you can run the following command:

```bash
mega-put /home/user/myfolder /backup
```

Copy

This will upload the contents of your local folder to your MEGA cloud folder. You can also use the -c or --create flag to create the remote folder if it does not exist. For example:

```bash
mega-put -c /home/user/myfolder /newfolder
```

Copy

This will create a new folder named /newfolder in your MEGA account and upload the contents of your local folder to it.

You can also use the --ignore-quota flag to ignore the storage quota limit and upload as much as possible. For example:

```bash
mega-put --ignore-quota /home/user/mybigfolder /backup
```
