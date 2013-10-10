# bob the builder

Minimal deploy tool using git post-receive hooks
After you install it run `bob` to get some help

```
Usage: bob [command] [remote] [options...]

The following commands are available from inside a git repo
All commands can be autocompleted by doing bob <tab><tab>

  bob add [remote] [user@example.com]
  will add and instantiate a new remote to the repository
    --scripts to specify a different script folder than the default one

  bob edit [remote] profile|build|deploy|restart|bundled-launch
  edit the scripts associated with your remote
  bundled-launch is the launch script that is bundled with your application

  bob fetch [remote] (profile|build|deploy|restart|bundled-launch)?
  fetch the current used scripts
  omit the 4th argument to get a tarball of all scripts
    --dir to save it to a directory

  bob push [remote] [branch]
  similar to a git push.
  will issue a build->deploy->restart on the remote

  bob redeploy [remote]
  reruns the deploy routing build->deploy->restart
  this is useful if you have updated any of your scripts or something has failed

  bob restart [remote]
  will execute the restart script on the remote
  this is a lightweight alternative to redeploy
```