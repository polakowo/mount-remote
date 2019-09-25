# mount-remote-macos

To mount a remote Mac as a folder:
- Install [FUSE for macOS](https://osxfuse.github.io)
- Install [SSHFS](https://osxfuse.github.io)
- Create a folder which will point to the remote host:
```bash
mkdir $local_folder
```
- Mount the remote folder:
```bash
sshfs $remote_user@$remote_host:$remote_folder $local_folder
```
- Then to unmount the folder:
```bash
umount $local_folder
rm -rf $local_folder
```
