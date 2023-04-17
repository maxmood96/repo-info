<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:d5f01498a85081aa48d2d6dbd941e6dd117fbeaf84bc1c5ffeb18a48c0ce7e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:d318e2d7e290606567abc1dc103a5b4a5a78de80ba2fa0cdd611f4ca30674ef7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (88992528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bdbd9203c47a0ce82ac63e7d197ebd8722d47d4c17d6e631ee37b4aa6855802`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 17 Apr 2023 19:24:10 GMT
ADD file:4ee7863f3d5cb617d2a362e60fb935dbaa72a36dfa6036ccbe7c097e6f669c6f in / 
# Mon, 17 Apr 2023 19:24:11 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 17 Apr 2023 19:24:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4b8c4b341064dfe84a3e92c86f5711ffbd50d1cd92ede051130d20d7295cad59`  
		Last Modified: Mon, 17 Apr 2023 19:24:30 GMT  
		Size: 89.0 MB (88992310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03453facb45341129977f28914138628d42bc1bb47828563cb08b90ac83ecf1`  
		Last Modified: Mon, 17 Apr 2023 19:24:20 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:d5f01498a85081aa48d2d6dbd941e6dd117fbeaf84bc1c5ffeb18a48c0ce7e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:d318e2d7e290606567abc1dc103a5b4a5a78de80ba2fa0cdd611f4ca30674ef7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (88992528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bdbd9203c47a0ce82ac63e7d197ebd8722d47d4c17d6e631ee37b4aa6855802`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 17 Apr 2023 19:24:10 GMT
ADD file:4ee7863f3d5cb617d2a362e60fb935dbaa72a36dfa6036ccbe7c097e6f669c6f in / 
# Mon, 17 Apr 2023 19:24:11 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 17 Apr 2023 19:24:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4b8c4b341064dfe84a3e92c86f5711ffbd50d1cd92ede051130d20d7295cad59`  
		Last Modified: Mon, 17 Apr 2023 19:24:30 GMT  
		Size: 89.0 MB (88992310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03453facb45341129977f28914138628d42bc1bb47828563cb08b90ac83ecf1`  
		Last Modified: Mon, 17 Apr 2023 19:24:20 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
