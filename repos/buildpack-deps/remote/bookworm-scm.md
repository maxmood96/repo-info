## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:7bd1956e0ce7ec9abcc78713b9da8a350e34dd4ac0d1e7b8e2f1520cf667cc35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bookworm-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2013c74f4073941aeb480e626b09e96af04ac27ef0753ff25f4bae0652d371de
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137746786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518ad877b15b4376479e313ba2a4927f064855bcaadf5f529244464086b62456`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:24:49 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Tue, 02 Jul 2024 01:24:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:48:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:48:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbed71fc5444cf6889a21b002de3e7805e810aa88f91a9ca941b4e3880246d1`  
		Last Modified: Tue, 02 Jul 2024 02:00:35 GMT  
		Size: 64.1 MB (64142928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fe4ea7a88ba109e23d9c524c89f4ad599de8d0abfb0c659d3c8906ae0c62938b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131567966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04a1233f9d3ba2640543d9cefa771d09da0d2cf88dc04c48e7dd7290c0ea548`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:48:18 GMT
ADD file:e0c33927a1af62d353710ab02fe9345a8805475ab99685993742946d38302465 in / 
# Tue, 02 Jul 2024 00:48:19 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:12:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:13:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f1ff7b6851f56d19040d12cd1d8757075037a3e51cd0d20ddfedfe600e399be6`  
		Last Modified: Tue, 02 Jul 2024 00:51:07 GMT  
		Size: 47.3 MB (47320358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03ec281dca54581a50ec4a927c64bebe7b6ef47dad0b260009c44ae5a8feddc`  
		Last Modified: Tue, 02 Jul 2024 01:22:39 GMT  
		Size: 22.7 MB (22727504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c366b742114f1b314834ae656bee5e41f5e30629107aed4bd693207e1ed0df`  
		Last Modified: Tue, 02 Jul 2024 01:23:00 GMT  
		Size: 61.5 MB (61520104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ce6126d6a09136f836c19b15f0e5fc5acc7be969ac284d4b7c375fd87c0b4582
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126324543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d79dfddabf4f6af4ca1998340feac6bf6c41ed7188a2ca406882aaf17d73859`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:59:52 GMT
ADD file:526dbb34ac449ae8f3c9025d71b3ffeb0e24fa5dc1a01da707f0a8b834eb4e33 in / 
# Tue, 02 Jul 2024 00:59:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:24:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:24:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:335f2c484898b910fac13d5650ed3c78e5e673fe8dab1b06a071c71478a153d0`  
		Last Modified: Tue, 02 Jul 2024 01:02:57 GMT  
		Size: 45.1 MB (45148097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa30b2bcbde45c2fc67abf425197af3af3e67d55296f168143343ef1b0e2d3e`  
		Last Modified: Tue, 02 Jul 2024 01:39:04 GMT  
		Size: 22.0 MB (21954038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4650a14deed524a46f7f7b410ff5d81e5ff66e51c7345e2b05887b6e3f4030`  
		Last Modified: Tue, 02 Jul 2024 01:39:24 GMT  
		Size: 59.2 MB (59222408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ef0610482c2e5909b3035c731b58fe4e0e92503aa55184971b4c76225a1a6d71
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137174230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8237381f2e62f9c64dce46304e239cc2525c498fa324df76649544daabd946`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 02 Jul 2024 00:39:29 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:51:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a6ab51b82df5ee608db374a16686eefb99bc53834af17064184653121729b3`  
		Last Modified: Tue, 02 Jul 2024 04:01:58 GMT  
		Size: 64.0 MB (63994637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a7150f3650abc01bb01b6994950dd8c35acd9c433bfadcfc1a434a2ea9949290
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141458173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26c2afa207dfb7cc2d7949fc10ca1b4b1b8eca3441c61c7c21f34722f75254e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:38:40 GMT
ADD file:262529672396993121e97bbbdda3d91ce43c7548adf11a263b7ec53bb7cda4d2 in / 
# Tue, 02 Jul 2024 00:38:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:05:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:05:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:04a42c358dbd9e835f8ae412589572f1bb5a19d9428a4854e4e845c88e34cb31`  
		Last Modified: Tue, 02 Jul 2024 00:42:16 GMT  
		Size: 50.6 MB (50579307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fc07fa7086d431c647128f1beada8efce9ea5808c01b2bf497e7e85b1fda1b`  
		Last Modified: Tue, 02 Jul 2024 01:14:02 GMT  
		Size: 24.9 MB (24890132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bff6c9a28c036769727a4cf9dbe067b96273c0352a50922f6e950491245fc03`  
		Last Modified: Tue, 02 Jul 2024 01:14:24 GMT  
		Size: 66.0 MB (65988734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8a04c418d221f88c661ce9fe8d82e529a1defa8a456c524b5f43de0297711bef
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136165457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d65e857df7d381ad6a1edab761c02e89f343484180e7d10d5fdca547f9dc7e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:36:56 GMT
ADD file:bc2014dd4183b8b941ef345add7dfa4a5b389afd70c64828331a9e51522a8c03 in / 
# Tue, 23 Jul 2024 00:37:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 01:26:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:05c2d132d3391d998ebae95f3de018ca09dc34d9bfbb160a1b6d662ebfe22612`  
		Last Modified: Tue, 23 Jul 2024 00:48:21 GMT  
		Size: 49.6 MB (49563161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b431e247f5dc02821a251567e4e81f86ada15613f56a6428e9d515728a3248cc`  
		Last Modified: Tue, 23 Jul 2024 01:58:32 GMT  
		Size: 23.6 MB (23636541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b6025db3aeb726503a6d775307c4881743edbf88fbefd8a997f66bb236e568`  
		Last Modified: Tue, 23 Jul 2024 01:59:26 GMT  
		Size: 63.0 MB (62965755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:59fad96d845621440d0ea25364fecb6fd032c65ce53b07df77cb6b3d3c51b1ad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148834808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf5d917a1d1b050133d4e48093febe11d2ea19d61e4a1cab54dcb39dba62c40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:29:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820239b953ebf111106a2c9f4d7ea847e4b73b2b422aaecff3b5ee0f1771ba9d`  
		Last Modified: Tue, 23 Jul 2024 02:42:17 GMT  
		Size: 69.6 MB (69582229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3692df3e163e1d1b79853ce8768644124e6ec91dc0618f18f8c6058a777aa9e3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135105561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198927bd3675fc9635a036a7b0ee1822b905c031c39c6a147c071fe0f8c542bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:43:28 GMT
ADD file:397aa43721bc5ca67ab359263843a05c62e131f07114e92f39927f59790c9a5b in / 
# Tue, 02 Jul 2024 00:43:30 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:32:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:33:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1b8bfe08588d8939b4d39134c5c614351649e3890ceb7c234b7542f58d7bcc28`  
		Last Modified: Tue, 02 Jul 2024 00:48:16 GMT  
		Size: 47.9 MB (47931511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37bf3d98ae5de59851adab45daeaaca9d29f76110a2923bd8937c4ad2e8cd52`  
		Last Modified: Tue, 02 Jul 2024 03:44:34 GMT  
		Size: 24.0 MB (24048872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6cb3bef78d7b20f095bd16b5a39e3ffec90c96f6d1307f8672edb9deef1c5f`  
		Last Modified: Tue, 02 Jul 2024 03:44:49 GMT  
		Size: 63.1 MB (63125178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
