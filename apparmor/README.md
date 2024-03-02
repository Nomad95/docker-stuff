# AppArmor

### Commands

```
docker info: -> SecurityOptions
sudo apparmor_status
sudo cat  /sys/kernel/security/apparmor/profiles

```

even if we do mount the apparmor rule should deny it

```
docker run --rm -it --cap-add SYS_ADMIN alpine
mount --bind 1 2
```

to disable apparmor

```
docker run --rm -it --cap-add SYS_ADMIN --security-opt apparmor=unconfined alpine
```

Load profile
```
sudo apparmor_parser myarmor
```