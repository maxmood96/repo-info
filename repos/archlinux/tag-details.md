<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20241006.0.268140`](#archlinuxbase-202410060268140)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20241006.0.268140`](#archlinuxbase-devel-202410060268140)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20241006.0.268140`](#archlinuxmultilib-devel-202410060268140)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:76a914dcc991e0b85bb858a94486afb3a44fd5d832e4b230af48b7357a2814c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:121dcbf9be83e639bbff9cdcaf9a68920e7d113f1d7d78ff4b7f9c7db97466f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151191182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67236c95c0f12d778793e2f92c14c93ed269c4259daeda71658157e07f0bbe9b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.version=20241006.0.268140
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.created=2024-10-06T00:07:56+00:00
# Sun, 06 Oct 2024 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Oct 2024 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241006.0.268140' /etc/os-release # buildkit
# Sun, 06 Oct 2024 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 06 Oct 2024 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4a2362ff7b5704a1f75ece04ce778c5a44b0e603954c08a8e1e4652d69f15a89`  
		Last Modified: Mon, 07 Oct 2024 19:58:41 GMT  
		Size: 151.2 MB (151182961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8709a4023469d245d875fee4cddbaf37641554341f6134707626446a7696a965`  
		Last Modified: Mon, 07 Oct 2024 19:58:38 GMT  
		Size: 8.2 KB (8221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:1fb47dc101f419701db2903a3f7d07a63962e560be60d072aebe8a9555446c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8114002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bce9404328d1eec7e00baacb22810a6abd396cde050ce4eb9be873ad3cb36e`

```dockerfile
```

-	Layers:
	-	`sha256:0604647d9390330fe0c267479527feddb627291afb4ff38a65c3088ea1658783`  
		Last Modified: Mon, 07 Oct 2024 19:58:38 GMT  
		Size: 8.1 MB (8102276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667bf954cd4005fb3ee95c2f679cb792880c937ea3db87b3c739a2dc9c848543`  
		Last Modified: Mon, 07 Oct 2024 19:58:38 GMT  
		Size: 11.7 KB (11726 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20241006.0.268140`

```console
$ docker pull archlinux@sha256:76a914dcc991e0b85bb858a94486afb3a44fd5d832e4b230af48b7357a2814c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20241006.0.268140` - linux; amd64

```console
$ docker pull archlinux@sha256:121dcbf9be83e639bbff9cdcaf9a68920e7d113f1d7d78ff4b7f9c7db97466f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151191182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67236c95c0f12d778793e2f92c14c93ed269c4259daeda71658157e07f0bbe9b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.version=20241006.0.268140
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.created=2024-10-06T00:07:56+00:00
# Sun, 06 Oct 2024 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Oct 2024 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241006.0.268140' /etc/os-release # buildkit
# Sun, 06 Oct 2024 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 06 Oct 2024 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4a2362ff7b5704a1f75ece04ce778c5a44b0e603954c08a8e1e4652d69f15a89`  
		Last Modified: Mon, 07 Oct 2024 19:58:41 GMT  
		Size: 151.2 MB (151182961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8709a4023469d245d875fee4cddbaf37641554341f6134707626446a7696a965`  
		Last Modified: Mon, 07 Oct 2024 19:58:38 GMT  
		Size: 8.2 KB (8221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20241006.0.268140` - unknown; unknown

```console
$ docker pull archlinux@sha256:1fb47dc101f419701db2903a3f7d07a63962e560be60d072aebe8a9555446c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8114002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bce9404328d1eec7e00baacb22810a6abd396cde050ce4eb9be873ad3cb36e`

```dockerfile
```

-	Layers:
	-	`sha256:0604647d9390330fe0c267479527feddb627291afb4ff38a65c3088ea1658783`  
		Last Modified: Mon, 07 Oct 2024 19:58:38 GMT  
		Size: 8.1 MB (8102276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667bf954cd4005fb3ee95c2f679cb792880c937ea3db87b3c739a2dc9c848543`  
		Last Modified: Mon, 07 Oct 2024 19:58:38 GMT  
		Size: 11.7 KB (11726 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:7005fdc99327fc48e89005dd615cf60841946d1d5ccb27eb6abb860fd8d103a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:898bf8a910407b6cda843b358b13f67ecb4344ab367a0043ea57fd29951ccc94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272195562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183fc87f7e6f523b82ef186d6a61acb54e95a40e7b21749a7a46100d0482679d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.version=20241006.0.268140
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.created=2024-10-06T00:07:56+00:00
# Sun, 06 Oct 2024 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Oct 2024 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241006.0.268140' /etc/os-release # buildkit
# Sun, 06 Oct 2024 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 06 Oct 2024 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:847aa64f2f293bb49d2b17e764ee9200d747a883b79d54a1c994d479035f926a`  
		Last Modified: Mon, 07 Oct 2024 19:59:05 GMT  
		Size: 272.2 MB (272186561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690b067d888f599b2c2f8c93f736614865740a49ac55d01c4230aebd2def3a8e`  
		Last Modified: Mon, 07 Oct 2024 19:59:02 GMT  
		Size: 9.0 KB (9001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:3f87eb8f85cccbad4d90363d6971e9db4a5f152908fd57b3fe3700933cfe2274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11912075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfdfbf7ec3224a6c79ae6a593230a595f528c14dba4d90e6dfdd641bbdb0012`

```dockerfile
```

-	Layers:
	-	`sha256:dc642c6e736f6172f840f026d90bf885f37c835fbb2335200850d3820b8d86a1`  
		Last Modified: Mon, 07 Oct 2024 19:59:02 GMT  
		Size: 11.9 MB (11900567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e8d5db069b498c291ebdfc756604a1c6db842c359f2d89f6dae7e12b7761400`  
		Last Modified: Mon, 07 Oct 2024 19:59:02 GMT  
		Size: 11.5 KB (11508 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20241006.0.268140`

```console
$ docker pull archlinux@sha256:7005fdc99327fc48e89005dd615cf60841946d1d5ccb27eb6abb860fd8d103a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20241006.0.268140` - linux; amd64

```console
$ docker pull archlinux@sha256:898bf8a910407b6cda843b358b13f67ecb4344ab367a0043ea57fd29951ccc94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272195562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183fc87f7e6f523b82ef186d6a61acb54e95a40e7b21749a7a46100d0482679d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.version=20241006.0.268140
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.created=2024-10-06T00:07:56+00:00
# Sun, 06 Oct 2024 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Oct 2024 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241006.0.268140' /etc/os-release # buildkit
# Sun, 06 Oct 2024 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 06 Oct 2024 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:847aa64f2f293bb49d2b17e764ee9200d747a883b79d54a1c994d479035f926a`  
		Last Modified: Mon, 07 Oct 2024 19:59:05 GMT  
		Size: 272.2 MB (272186561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690b067d888f599b2c2f8c93f736614865740a49ac55d01c4230aebd2def3a8e`  
		Last Modified: Mon, 07 Oct 2024 19:59:02 GMT  
		Size: 9.0 KB (9001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20241006.0.268140` - unknown; unknown

```console
$ docker pull archlinux@sha256:3f87eb8f85cccbad4d90363d6971e9db4a5f152908fd57b3fe3700933cfe2274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11912075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfdfbf7ec3224a6c79ae6a593230a595f528c14dba4d90e6dfdd641bbdb0012`

```dockerfile
```

-	Layers:
	-	`sha256:dc642c6e736f6172f840f026d90bf885f37c835fbb2335200850d3820b8d86a1`  
		Last Modified: Mon, 07 Oct 2024 19:59:02 GMT  
		Size: 11.9 MB (11900567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e8d5db069b498c291ebdfc756604a1c6db842c359f2d89f6dae7e12b7761400`  
		Last Modified: Mon, 07 Oct 2024 19:59:02 GMT  
		Size: 11.5 KB (11508 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:76a914dcc991e0b85bb858a94486afb3a44fd5d832e4b230af48b7357a2814c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:121dcbf9be83e639bbff9cdcaf9a68920e7d113f1d7d78ff4b7f9c7db97466f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151191182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67236c95c0f12d778793e2f92c14c93ed269c4259daeda71658157e07f0bbe9b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.version=20241006.0.268140
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.created=2024-10-06T00:07:56+00:00
# Sun, 06 Oct 2024 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Oct 2024 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241006.0.268140' /etc/os-release # buildkit
# Sun, 06 Oct 2024 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 06 Oct 2024 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4a2362ff7b5704a1f75ece04ce778c5a44b0e603954c08a8e1e4652d69f15a89`  
		Last Modified: Mon, 07 Oct 2024 19:58:41 GMT  
		Size: 151.2 MB (151182961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8709a4023469d245d875fee4cddbaf37641554341f6134707626446a7696a965`  
		Last Modified: Mon, 07 Oct 2024 19:58:38 GMT  
		Size: 8.2 KB (8221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:1fb47dc101f419701db2903a3f7d07a63962e560be60d072aebe8a9555446c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8114002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bce9404328d1eec7e00baacb22810a6abd396cde050ce4eb9be873ad3cb36e`

```dockerfile
```

-	Layers:
	-	`sha256:0604647d9390330fe0c267479527feddb627291afb4ff38a65c3088ea1658783`  
		Last Modified: Mon, 07 Oct 2024 19:58:38 GMT  
		Size: 8.1 MB (8102276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667bf954cd4005fb3ee95c2f679cb792880c937ea3db87b3c739a2dc9c848543`  
		Last Modified: Mon, 07 Oct 2024 19:58:38 GMT  
		Size: 11.7 KB (11726 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:7ffbac0e553cdbe7a05cd35a71843f564ac358bded672a70aa6a83393acfbf36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:1b8c82f5f76c649bf1cb15f1d5ad719ac7e65bf82122a3257ba292ecf8b7bcaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322032803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10cc2bb4a0eea00ab100c4267b0c5fa2ad168ed98a52f7958e3010892758187`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.version=20241006.0.268140
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.created=2024-10-06T00:07:56+00:00
# Sun, 06 Oct 2024 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Oct 2024 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241006.0.268140' /etc/os-release # buildkit
# Sun, 06 Oct 2024 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 06 Oct 2024 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ed7f81b56ae3922a2cb3615198765a6dda3043659a53fdf1d921877520b781fa`  
		Last Modified: Mon, 07 Oct 2024 19:59:39 GMT  
		Size: 322.0 MB (322022685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d2b8de4f4f15dd6257d07071aba84d668121d3b5ef4f8879b82e178dbcbf15`  
		Last Modified: Mon, 07 Oct 2024 19:59:35 GMT  
		Size: 10.1 KB (10118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:4e3405e7758a1d979a5c5d04a1bbf358c39d63f9951355619a08fc0bf5c81261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12179444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2c19d5c6200c96c48b3f0e467ece42a49bf1d90a733824f79d22fef91e1d9f`

```dockerfile
```

-	Layers:
	-	`sha256:38f254e2895409bdc5f108c0803279c05d4cc0928dd3d44463fa4d0c47ebddfc`  
		Last Modified: Mon, 07 Oct 2024 19:59:35 GMT  
		Size: 12.2 MB (12167879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7223f88a5db52a94dcebf542b4b52a8d3f41d7944db5ed61ef0dc3a9816bc40`  
		Last Modified: Mon, 07 Oct 2024 19:59:35 GMT  
		Size: 11.6 KB (11565 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20241006.0.268140`

```console
$ docker pull archlinux@sha256:7ffbac0e553cdbe7a05cd35a71843f564ac358bded672a70aa6a83393acfbf36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20241006.0.268140` - linux; amd64

```console
$ docker pull archlinux@sha256:1b8c82f5f76c649bf1cb15f1d5ad719ac7e65bf82122a3257ba292ecf8b7bcaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322032803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10cc2bb4a0eea00ab100c4267b0c5fa2ad168ed98a52f7958e3010892758187`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.version=20241006.0.268140
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.created=2024-10-06T00:07:56+00:00
# Sun, 06 Oct 2024 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Oct 2024 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241006.0.268140' /etc/os-release # buildkit
# Sun, 06 Oct 2024 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 06 Oct 2024 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ed7f81b56ae3922a2cb3615198765a6dda3043659a53fdf1d921877520b781fa`  
		Last Modified: Mon, 07 Oct 2024 19:59:39 GMT  
		Size: 322.0 MB (322022685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d2b8de4f4f15dd6257d07071aba84d668121d3b5ef4f8879b82e178dbcbf15`  
		Last Modified: Mon, 07 Oct 2024 19:59:35 GMT  
		Size: 10.1 KB (10118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20241006.0.268140` - unknown; unknown

```console
$ docker pull archlinux@sha256:4e3405e7758a1d979a5c5d04a1bbf358c39d63f9951355619a08fc0bf5c81261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12179444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2c19d5c6200c96c48b3f0e467ece42a49bf1d90a733824f79d22fef91e1d9f`

```dockerfile
```

-	Layers:
	-	`sha256:38f254e2895409bdc5f108c0803279c05d4cc0928dd3d44463fa4d0c47ebddfc`  
		Last Modified: Mon, 07 Oct 2024 19:59:35 GMT  
		Size: 12.2 MB (12167879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7223f88a5db52a94dcebf542b4b52a8d3f41d7944db5ed61ef0dc3a9816bc40`  
		Last Modified: Mon, 07 Oct 2024 19:59:35 GMT  
		Size: 11.6 KB (11565 bytes)  
		MIME: application/vnd.in-toto+json
