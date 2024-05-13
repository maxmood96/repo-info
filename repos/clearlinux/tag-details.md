<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:2ab2f7f3ef1744a1d0224d07daf68a9986920fa14d6939174169364635d45123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:ebc7245ef48f35c66dd9c3b2976a8a325fdbfb2553afb58ae47588525c68f507
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69138072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6288e671493348d0a689888b8744d3088aacb4c79dc7bc452ba17dcfbffd07`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 13 May 2024 18:27:16 GMT
ADD file:d811411e80eed55caa5f625469091df337c3ccaa8d217cb4d65d3d0bcd2aa242 in / 
# Mon, 13 May 2024 18:27:17 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 13 May 2024 18:27:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4352a38324fd400c1f0643870b795188e0cfcd8df2a72cd04263083030ae47b6`  
		Last Modified: Mon, 13 May 2024 18:27:34 GMT  
		Size: 69.1 MB (69137858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb469c2f1d4d256887e5cb4108eb7047381d84445edb2de6eef134c9a4c24e69`  
		Last Modified: Mon, 13 May 2024 18:27:26 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:2ab2f7f3ef1744a1d0224d07daf68a9986920fa14d6939174169364635d45123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:ebc7245ef48f35c66dd9c3b2976a8a325fdbfb2553afb58ae47588525c68f507
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69138072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6288e671493348d0a689888b8744d3088aacb4c79dc7bc452ba17dcfbffd07`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 13 May 2024 18:27:16 GMT
ADD file:d811411e80eed55caa5f625469091df337c3ccaa8d217cb4d65d3d0bcd2aa242 in / 
# Mon, 13 May 2024 18:27:17 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 13 May 2024 18:27:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4352a38324fd400c1f0643870b795188e0cfcd8df2a72cd04263083030ae47b6`  
		Last Modified: Mon, 13 May 2024 18:27:34 GMT  
		Size: 69.1 MB (69137858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb469c2f1d4d256887e5cb4108eb7047381d84445edb2de6eef134c9a4c24e69`  
		Last Modified: Mon, 13 May 2024 18:27:26 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
