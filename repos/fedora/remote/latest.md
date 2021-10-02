## `fedora:latest`

```console
$ docker pull fedora@sha256:adcd1683380f58b38c70ab02d17941e04bdfc2eeb71d56bc74ac8ba9100c4ae7
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
$ docker pull fedora@sha256:b1f95b4bf817417973513dff2fc70974f5f7792eb56506c8b992e49a98fe5c6d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64999360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e58495b280f3ace00dd8da68d5553753237b081f3ca4d894459c4924b279416`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 01 Apr 2021 18:00:19 GMT
ENV DISTTAG=f34container FGC=f34 FBR=f34
# Fri, 01 Oct 2021 23:02:22 GMT
ADD file:bb7421925b61afcef18e92afc61e098e418d857d13757d09f785ee426e2d1888 in / 
# Fri, 01 Oct 2021 23:02:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:70fb9965a23f2226fef622992fdf507b8333c61d68259766d4721cc4ba1e5dae`  
		Last Modified: Fri, 01 Oct 2021 23:03:40 GMT  
		Size: 65.0 MB (64999360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm variant v7

```console
$ docker pull fedora@sha256:3ba338a4c1cfe2772d59b1b8e061113eb11d9fd05780d63307374b29f214e3c3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61364579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d770a70d59c46ca9e10648e6c636a3baa35cfdb92f22fe54c54c4580b58fae1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 19:03:21 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 23 Jul 2021 19:04:30 GMT
ENV DISTTAG=f34container FGC=f34 FBR=f34
# Fri, 23 Jul 2021 19:04:47 GMT
ADD file:c353423cdd460373f838584da868d12a5f5339e5ff19632d794a967112162077 in / 
# Fri, 23 Jul 2021 19:04:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:619faf1102da7d7df8241c3a5037eb7bef39a01632a0fed3659b08dfabe4563e`  
		Last Modified: Fri, 23 Jul 2021 19:08:14 GMT  
		Size: 61.4 MB (61364579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:adffb1674fb57f758ba27d7968148aa5cf90b0aaa15d4b6fb58923c650c78d38
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64692518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d60a39ca0424cfca60b4ce026f22f4cbea21f2016e95f9ffd5b46747b0a9df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 01:32:26 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 23 Jul 2021 01:32:50 GMT
ENV DISTTAG=f34container FGC=f34 FBR=f34
# Fri, 01 Oct 2021 23:28:49 GMT
ADD file:dd0c1fd3851dc390f265d652d16108034eb217bdbe268282b62e7fa76a864058 in / 
# Fri, 01 Oct 2021 23:28:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:72621145c58c39731ea1caba1e293420938b7643c3f0be5acc3f50a15580ac4f`  
		Last Modified: Fri, 01 Oct 2021 23:30:09 GMT  
		Size: 64.7 MB (64692518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; ppc64le

```console
$ docker pull fedora@sha256:adcf0689bc6403e69aded731af6822b4e14189f88107c544672dd46f95e06424
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70754182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440c7f233ae6acf434201b3ac4ca1461cbbadd72fc7f129c597b2a4d3ac34b5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 23:32:50 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 23 Jul 2021 23:34:39 GMT
ENV DISTTAG=f34container FGC=f34 FBR=f34
# Fri, 23 Jul 2021 23:34:49 GMT
ADD file:6472b37d42e912954b06a62f055cf1257e171a5ceacc51a4b1233934908daab7 in / 
# Fri, 23 Jul 2021 23:35:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:10cb0eecbe24b9437d48a6f70218700ad08d2facf246f40b748fe57b8f743b57`  
		Last Modified: Fri, 23 Jul 2021 23:36:32 GMT  
		Size: 70.8 MB (70754182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; s390x

```console
$ docker pull fedora@sha256:8b4776425f4d3069aab2dcdb53809ef66b185e4f1613ed7e62e51c8fdfff781b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62548577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0348488b0185dda161d41d3085f5224664534b298fa6cc513e69e0586710cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 23 Jul 2021 02:30:59 GMT
ENV DISTTAG=f34container FGC=f34 FBR=f34
# Fri, 01 Oct 2021 22:42:12 GMT
ADD file:e84d9ebd7d1e95617829df96803ed9c13addf0d97ff92aa2e4e6d774b7c5b528 in / 
# Fri, 01 Oct 2021 22:42:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8c06e697a614d97c184fac440ab0114000c656af19e5052a13db1a80d54814bf`  
		Last Modified: Fri, 01 Oct 2021 22:43:28 GMT  
		Size: 62.5 MB (62548577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
