## `debian:trixie-backports`

```console
$ docker pull debian@sha256:844ce9841fdbaf33450814932c2edc509cbe52b920f74fb53064fcb47a73d091
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:fa2016c58b4df666286dfa14b2402c05d60c556ecfd4c60635b64ad21380edba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52361047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4108fa7ca7c7315b221a60b3ad25923af179d8e6ad71a3bf452629619a45417e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:23:42 GMT
ADD file:93e647bfd891e82156d7a13e0f0b194003855008967ec51e962ea0d70fc59ff6 in / 
# Tue, 12 Mar 2024 01:23:43 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:23:47 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6fbaa46799c378c8b00a06cb5a2319bdd5ab7abe194cd97bbc9aec2daf476e9c`  
		Last Modified: Tue, 12 Mar 2024 01:29:57 GMT  
		Size: 52.4 MB (52360823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d030c5a8084ea98c5d133310c557903db0c667992319593f3eda4df96ab1f8a9`  
		Last Modified: Tue, 12 Mar 2024 01:30:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:3ee7c65e76cf5675d18a156f96f0593f3096a6db7e78ba40c756d8080a1d6d76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49418253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8cd7cec8a659c0bc3c41a8c0d75c0df1c08f13f66165c04dc2639a2c7e2aeb7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:49:56 GMT
ADD file:3e60918b2fc6eb291458158f2b94b782320f758effe373fd6d0a5c58dd3e2319 in / 
# Tue, 12 Mar 2024 00:49:56 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 00:49:59 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5d768e5bf180c947f8692477b575df3498b64f65e904bac933d0260cd957c8aa`  
		Last Modified: Tue, 12 Mar 2024 00:55:26 GMT  
		Size: 49.4 MB (49418029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c934c7ddc7d8576afe78a9c9fc58e774b560f51c788dcc0fa053cf9edd7d85d`  
		Last Modified: Tue, 12 Mar 2024 00:55:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:e9c9baf2387441e6060b769532b20a38414303bf82a83e53b574c160ab99f95e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46919359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aac1e2b89ac3f363b674d6e0885cddc50fd34c6b0ff73363586e51f2f724cf5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:01:42 GMT
ADD file:653b30d78a37c262fc23750e2a51b4c22f86c5a03a005268cedcb42011759039 in / 
# Tue, 12 Mar 2024 01:01:45 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:01:48 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:84940e63db1cf18d5cf1aa5d0b2d913f1cfeaf6d1392975ee4542b2b21627246`  
		Last Modified: Tue, 12 Mar 2024 01:08:19 GMT  
		Size: 46.9 MB (46919137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a328f8d6de79ff5ad5349975e74ef1ab710ee2b2c1140ed7d297288f11fad168`  
		Last Modified: Tue, 12 Mar 2024 01:08:27 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:92555e50616fdc10bd50ef0fcd0bd1fa0b9930951cc537321e3d6f7454105842
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52191576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c546184b0e75b2f3c08f9bb7d92f51266dd3165d9a9e09f25f02e87207ba0f3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:47:23 GMT
ADD file:822f8ebf81dcb8d0c3abe6092460eb4cd185e7a4b5b794a9ebc4221cc30518c9 in / 
# Tue, 12 Mar 2024 00:47:24 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 00:47:26 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:abb8ff6184544bf5d189fbbab4286e594f2b7adc7d1feb51af49c007cff0e2c6`  
		Last Modified: Tue, 12 Mar 2024 00:53:00 GMT  
		Size: 52.2 MB (52191351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b8358668d3c381f8aedc3ae8c93326c22568043a90d44d259e33ec7cab120`  
		Last Modified: Tue, 12 Mar 2024 00:53:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:d39b19d7f809a891c45b6b2ecfe60a432e2b0b011742aedd7a1f132464ff9262
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53172888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8313293498393360dd9bfb2ac031fbeab77051643822166842236963e28b6e0e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:00:45 GMT
ADD file:37f9337bf11dc9e80356b325a83e455996065eb5a0bb7e34196dd3ab715908c3 in / 
# Tue, 12 Mar 2024 01:00:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:00:50 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d38fd1f357db42e901e77bda285b7bc07b7f9c002000df3fbd114813ff6b7831`  
		Last Modified: Tue, 12 Mar 2024 01:07:51 GMT  
		Size: 53.2 MB (53172667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e71e1b74d730952d58785770bc239a23c24f7f85f52dacc1b59546f1faffaee`  
		Last Modified: Tue, 12 Mar 2024 01:08:00 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; mips64le

```console
$ docker pull debian@sha256:5623959c6ba45c6bcf162192dbefc9724053fe2ab4ee13d0ea5ca6c62fd62a9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51407949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f156c346b8defeaba30303c0d2fce7b77666d7d6e54c0d538c72c13276239b5a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:12:54 GMT
ADD file:b1a1fd9e7f874d3dc6cae10f09e49e08335ad86924ba543f9ff6c777d93c7314 in / 
# Tue, 12 Mar 2024 01:12:59 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:13:14 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9b0712382998885f6ab26afd04e80c46f04069a2491aab0d33d167a8539090c2`  
		Last Modified: Tue, 12 Mar 2024 01:25:01 GMT  
		Size: 51.4 MB (51407725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7b0c7946086d4d9ed1acd33504bd2c8efbd2b7cc5d3776d9f3f297c8d9e4b`  
		Last Modified: Tue, 12 Mar 2024 01:25:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:3e00017b3d062f5e410201c14274d254a5db064f47d1e40b6a770f21f8207939
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56241014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8b00858bfe20d8e8ffa0258a90bce2b595a6e11a8b46803e5bf315264034bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:34:27 GMT
ADD file:ee3f9725c5da5d09634af5073dc8d63c0cf10c6ece6c7b0084a82d44eeaa487e in / 
# Tue, 12 Mar 2024 00:34:33 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 00:34:40 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:df0d8d793e684337100029abc1076242a4e60e57c67bb9ee5002155393dd3737`  
		Last Modified: Tue, 12 Mar 2024 00:41:55 GMT  
		Size: 56.2 MB (56240791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7036b6b7950361dd35cce2276f5da673b1f4293056c00defb44aaabe7be9a39e`  
		Last Modified: Tue, 12 Mar 2024 00:42:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:0e637ada7d34cf6776db80eb6267f9664bbcf44793bf08dce649af7f8daee081
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51738741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53f7cc4bf7903eb573d97e81b2bbb8db532744a4d221ca6a46859d680d83a5d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:12:17 GMT
ADD file:a763a87b7a749afb8ffcbc72555a671734dd9d842834384eebb8dd784135bfc9 in / 
# Tue, 12 Mar 2024 01:12:19 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:13:20 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2f13ce6fc956957d2abf0abd272bd88a159c9cdf4a731647c572eb2581973c57`  
		Last Modified: Tue, 12 Mar 2024 01:23:47 GMT  
		Size: 51.7 MB (51738519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff9f77e0c4d031413411c2feaeccf3d2af9b241ea088b23f6ad5d917b398a50`  
		Last Modified: Tue, 12 Mar 2024 01:23:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
