## `photon:latest`

```console
$ docker pull photon@sha256:4c575f517372a8ce1d62c79130b9d79941c17027e7d57f1b07b8daa97f96f0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:ebb2123045cbf7de92e75e342febcb36c00698cdea4b336e0066986ebdbdb03b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7b2c18b2ac25fcbedea4a2a2df29bc74f7018779763bedbc78f8f509dcf3f3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:19:12 GMT
ADD file:b7fa5c56d1277974bd171f6ff7abdf540683effde39a21863f9911dff90f0f0b in / 
# Wed, 22 Jul 2020 01:19:12 GMT
LABEL name=Photon OS x86_64/3.0 Base Image vendor=VMware build-date=20200721
# Wed, 22 Jul 2020 01:19:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e50362f330bc3b41e0d1ccb12a1c005754dde0fc0607d33afa5e3344e59b34cf`  
		Last Modified: Wed, 22 Jul 2020 01:19:45 GMT  
		Size: 15.2 MB (15198752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:001a6cbfaaeab63198376955936e11402436f0a44c5a06a69e3aea44d5c52821
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12985975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f695fb248b3c2f9672f966c38be2bdef26212fc65e4930b2291b03ec6822654`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:02:54 GMT
ADD file:aca1e703f9904f4931abe2c2dba309190ff2c401b3ef0bf0197bb7a3801b3b07 in / 
# Wed, 22 Jul 2020 00:02:56 GMT
LABEL name=Photon OS aarch64/3.0 Base Image vendor=VMware build-date=20200721
# Wed, 22 Jul 2020 00:02:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6526e28ef1d419770aa036501f34ba8564f874b20bc04c7270a266bfec15e9f8`  
		Last Modified: Wed, 22 Jul 2020 00:03:19 GMT  
		Size: 13.0 MB (12985975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
