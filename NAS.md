# NAS (Network Attached Storage)

Used for resources that we will all access frequently, or that require time to query (e.g. ENTSO-E API).

Mount as a SAMBA drive.

IP: 192.168.1.38
Username: pi
Password: raspberry
Drive to mount: `public`

## Mount on MacOS

In the finder, type ⌘k, then enter `smb://192.168.1.38/`

## Use with `bentso`

On my computer, the NAS mounts as `/Volumes/public/`. So to use the NAS data:

    import bentso
    cl = bentso.CachingDataClient("/Volumes/public/disk1/bentso/")
