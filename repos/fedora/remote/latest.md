## `fedora:latest`

```console
$ docker pull fedora@sha256:c4555750ab68c2e7dc4cf74fa8d0d2fcf58bd9c1f1b9366b6058323fdc6dfeff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:latest` - linux; amd64

```console
$ docker pull fedora@sha256:762d7c5766839057fd9f96a0f2cedf143e2b818feb7767dc1bb70c00c4c3890a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54650610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78af7a836928efd44317e82c8f2f9c86bb83ae915deef1b58dc6465dfa5436e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 01 Oct 2021 23:02:34 GMT
ENV DISTTAG=f35container FGC=f35 FBR=f35
# Mon, 29 Nov 2021 20:28:56 GMT
ADD file:f495e5783588b218023a03e0df69da3cee25a8b88e399369afcf89dcd0a31501 in / 
# Mon, 29 Nov 2021 20:28:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:edad61c68e675e3c0fe2d02c0d21b9ca85334fcd8de115fc56764e72cb5bed6c`  
		Last Modified: Mon, 29 Nov 2021 20:30:02 GMT  
		Size: 54.7 MB (54650610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm variant v7

```console
$ docker pull fedora@sha256:13d64bd68de3af7f428d3847fbec9f72b10d58e19097640d306eb1dcdcb6fb62
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51309121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68b367f7abe9ad1a99f86b5e8664baeed77fa018c38339c6ef65319f8151a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 19:03:21 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sat, 02 Oct 2021 18:49:21 GMT
ENV DISTTAG=f35container FGC=f35 FBR=f35
# Mon, 29 Nov 2021 20:14:58 GMT
ADD file:39b44fc1fab7d5f630e39c29210b9621455268e24c7e78adb5b30ef8a83f0465 in / 
# Mon, 29 Nov 2021 20:15:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:94c6a630001edd6bf566f359e42d260c67a06c9affcb1d15bc2499efd314fb36`  
		Last Modified: Mon, 29 Nov 2021 20:18:19 GMT  
		Size: 51.3 MB (51309121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:acf39c9fb7cd0fa51ee423f9536667007a1b52e98c6030c823007cf5686c7765
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53608583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775b4cdd6b58e0dd0077142af08f123c9ed90ac24c4004f161afd01f86c3c95b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Nov 2021 21:12:33 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Tue, 02 Nov 2021 21:12:58 GMT
ENV DISTTAG=f35container FGC=f35 FBR=f35
# Sat, 19 Mar 2022 19:19:32 GMT
ADD file:a7d0a8d9a9133b3614c6961097e462a1e98ed32bd2a7d73f21552362e625edb0 in / 
# Sat, 19 Mar 2022 19:19:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:623fc6c8f399e6dde93fc82beed08af10e667fa3896b48d4d41b3f93d652dd0c`  
		Last Modified: Sat, 19 Mar 2022 19:20:45 GMT  
		Size: 53.6 MB (53608583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; ppc64le

```console
$ docker pull fedora@sha256:063d1866ae6d3be6a9c660fe8db72c1c11db8087d1a849d02d947484bf0ca139
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59441111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e73dc9e3f6db82ad2b32fdcd006ddc410f853c177d54337c614fb72f4a27e75`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 23:32:50 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 04 Oct 2021 19:40:14 GMT
ENV DISTTAG=f35container FGC=f35 FBR=f35
# Mon, 29 Nov 2021 20:33:10 GMT
ADD file:c4b06121190c5665d0b47752a083ebc2dcc91abe965150a25c19a6a3e1fe2d66 in / 
# Mon, 29 Nov 2021 20:33:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c7d756f7f3ddeaa56c5aa21d5d65559423e975ac4b466a0a2185b8c060bed683`  
		Last Modified: Mon, 29 Nov 2021 20:34:52 GMT  
		Size: 59.4 MB (59441111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; s390x

```console
$ docker pull fedora@sha256:3d63aa1da663b274bf158281d07e77db1e7b199116aac54f1bc7175c856a937b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52571418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b6c80727783f4c6c0668e3c208f9f77a15c86986799066ce6c1139f5587ac6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 01 Oct 2021 22:42:23 GMT
ENV DISTTAG=f35container FGC=f35 FBR=f35
# Sat, 19 Mar 2022 04:31:18 GMT
ADD file:e08d7b2813b14e6ceb9044105795f7f567a3346596ba733cd7e50607d0b21f99 in / 
# Sat, 19 Mar 2022 04:31:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:068a470be0289c24db02bcbfc57bd4bc7fce673b9b1f6da92a0807e164713882`  
		Last Modified: Sat, 19 Mar 2022 04:32:42 GMT  
		Size: 52.6 MB (52571418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
