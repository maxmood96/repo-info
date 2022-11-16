## `fedora:rawhide`

```console
$ docker pull fedora@sha256:f501d81a388988c83650dfef41e2782bef1bdd55db77930c83b05f5d780d07be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:rawhide` - linux; amd64

```console
$ docker pull fedora@sha256:c7dfa518d9db440fb02362c0f9b014c0e1b8e04bc0f6bf540d1d5ac2ecb43453
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65568074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b902325de1ec96bbbeecd610ef5dcfba06da72e6831eb0ac1049e376d7778a58`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 20:41:02 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Thu, 03 Nov 2022 20:41:08 GMT
ADD file:aea454c4f9f7bccbd03cf61c6477deac629e6b63f8ef39d87667ee4efaf12136 in / 
# Thu, 03 Nov 2022 20:41:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7658a6d4e9efd0ec04b7aca3c754f4441c79d4dedab19a67c5f5293bb0b5e151`  
		Last Modified: Thu, 03 Nov 2022 20:42:25 GMT  
		Size: 65.6 MB (65568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:6e1160094641e19b3ae1aa45382edf003115ed80e7a5eb70920d25f222cef6a7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (64031417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4270e03b1e788ad9f22db2069ca5f46b3b0d202151f26f730d632fbfaabb322a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 19:58:41 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Tue, 15 Nov 2022 23:24:49 GMT
ADD file:f3f02cd039386200c4016153c08090962456cb51379aba9fba1a1523210cab8b in / 
# Tue, 15 Nov 2022 23:24:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:803d75c05eb7ae8a4fdb882e5c8794f4ccd3fd48d9f20dff418bc5f35002e881`  
		Last Modified: Tue, 15 Nov 2022 23:25:51 GMT  
		Size: 64.0 MB (64031417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; ppc64le

```console
$ docker pull fedora@sha256:dd158615a68d1e8c123ee9c66c60fe6057bfb854c6cc22246fe9cc0676e82fb8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71274936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7384891e076d699d03394e69c4dab507ed69a494318da522eb06a938cdaf92f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 21:19:02 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Wed, 16 Nov 2022 03:27:52 GMT
ADD file:505bd40e8fc07c1f04e487dff8486061760cf984120c9579185aecf2f6a2b667 in / 
# Wed, 16 Nov 2022 03:27:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:927284fadef26220f69c8da5b431347afe136913adede95ab92d49b9123e2e7a`  
		Last Modified: Wed, 16 Nov 2022 03:30:04 GMT  
		Size: 71.3 MB (71274936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; s390x

```console
$ docker pull fedora@sha256:6588fbf39a732e1565dd86a964aa887b6ec01d30dc663d2e2559cf7f819275b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63181632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc5bb1579778fdd05c25d2150e102989bdd6dc56474d36ee47708eaf3219b65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 21:31:13 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Wed, 16 Nov 2022 02:11:20 GMT
ADD file:47f6a01ddbce4bf76d1552556ea134308b7e18a706904729ee640b92a5fb081c in / 
# Wed, 16 Nov 2022 02:11:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cb5c3098cd40cba591630ca5088f79ef283785dca831281a621120e480e49f71`  
		Last Modified: Wed, 16 Nov 2022 02:13:03 GMT  
		Size: 63.2 MB (63181632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
