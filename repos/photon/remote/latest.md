## `photon:latest`

```console
$ docker pull photon@sha256:73327fdc7544890e27e5c4becd4312977df5e38c41a0322dfa41df4e773caf3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:2b843765960ede71035957a92bd0ff16313b5aee30164957c8243dd9f1b98d32
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15647304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07bc5e332532d8ae5cfd75166f66f3b1c9a1e2e0ec631d9df80982f6a7540c37`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 02 Oct 2020 23:33:00 GMT
ADD file:ea6d4b477ae2fea521ba8a3688555c092f9f7d0758fa9740426bd2bc4cb1b9f6 in / 
# Fri, 02 Oct 2020 23:33:01 GMT
LABEL name=Photon OS x86_64/3.0 Base Image vendor=VMware build-date=20201002
# Fri, 02 Oct 2020 23:33:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dd7e5f7b730b0af3da20c39f845b6430e183edc749345b856c73bd8801a9e120`  
		Last Modified: Fri, 02 Oct 2020 23:33:41 GMT  
		Size: 15.6 MB (15647304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:c70802bf03c036adb11ea53f78302e905f6f03bc26c10b63e88f2b6162e59545
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12994420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03801f0f317058e7c61e2f6a0a4cb65da8e1df62e48ecead9df8e9202165221e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Sep 2020 01:05:38 GMT
ADD file:aec7c0ded80819c2aa4ecba9cc48be150e0b23881218aae757572c57eeb099da in / 
# Sat, 19 Sep 2020 01:05:40 GMT
LABEL name=Photon OS aarch64/3.0 Base Image vendor=VMware build-date=20200918
# Sat, 19 Sep 2020 01:05:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f0acb4964b403b19c2a969071b07f348eb5ae80aad9544269f18d2fa6b33cf8f`  
		Last Modified: Sat, 19 Sep 2020 01:06:08 GMT  
		Size: 13.0 MB (12994420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
