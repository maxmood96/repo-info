## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:53c609d43abfb9c368fc067af13c96e07000dac98e58a97370c11e1833280a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f391f82c3b729d0feea06e9be75b1423d517a4f46d9e00d9349cecf78b588418
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100622213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b4ce94126c2632397e5decaa27e831c9f0a8b20c0d852a25edff953312c350`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:36:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:37:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe58a6f17884dd17b0751f2ab6886f31292b6b2d42ef75ce8726d7525798c21`  
		Last Modified: Tue, 16 Apr 2024 03:52:42 GMT  
		Size: 11.1 MB (11131101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aae6d74559e63793e109c4e7302a9a1bb12df25c9f8e6db8937130970054cf8`  
		Last Modified: Tue, 16 Apr 2024 03:53:02 GMT  
		Size: 60.9 MB (60906606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2a1bf844b68bd0d14949565ec42a6699226d8c923aa8e9dc8c4a7aa1db0bd7ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90074280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bea4e700e30d386b4a4d540c73b0d448eabacbb172a88a6392973c806da0259`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:40 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:52:51 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Wed, 10 Apr 2024 18:52:52 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:15:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:15:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:415e9bbd0769b29f08b5782353a86f2e8e29ba55d4d4d1e7fe999652679005c5`  
		Last Modified: Tue, 16 Apr 2024 01:53:17 GMT  
		Size: 24.6 MB (24602624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb5e0f9a8123efc9edf4ed4a3a071bda75e2e0678a53d646c8e6c0b3ff6df70`  
		Last Modified: Tue, 16 Apr 2024 02:31:55 GMT  
		Size: 9.6 MB (9604241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe0762329df1909a1314fc970b65988a47ae49a3d6eb8bace711b09364313eb`  
		Last Modified: Tue, 16 Apr 2024 02:32:13 GMT  
		Size: 55.9 MB (55867415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:eee0af0aa69ff70b89ffc6be740345676d3bf8b89adc2008fde97bcd58b63c79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99236698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3f2e3f9f80c8238eeade5d2d3235e39e3dcfa4cb77ca7f3ab537c5e645cec9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:50:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:51:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f9e24831b35659f11dda56ed6229046a1aa11ed7d76373cb21a01b415fc51a`  
		Last Modified: Tue, 16 Apr 2024 02:10:29 GMT  
		Size: 11.0 MB (10982960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d94608895359e7ebf7493231f818b215ada755a377c25d53dd41663616f2db`  
		Last Modified: Tue, 16 Apr 2024 02:10:47 GMT  
		Size: 61.0 MB (61048754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f4fb435defd3ed123c379d7ea6657e0e16298a9937db0bd5a5bd9b3f6ccbdaa0
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115896223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ebca3ee076a7ed6dc3365898c3ef522819aec679792be13b8df271e14144f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:04:56 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:04:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:04:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:04:56 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:04:59 GMT
ADD file:8efe37e124c3eb7c9e2b3ba1f33a019526490b9a49cbe8997abf72caf6bb7ece in / 
# Wed, 10 Apr 2024 19:04:59 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:57:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0c372adcddc32347cef56486050a9e3f15243cd4c6b2ef3b7de6d5d6f7bf9ef1`  
		Last Modified: Tue, 16 Apr 2024 02:49:17 GMT  
		Size: 33.3 MB (33315676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04712a59991e1b0784ad92727b7b6d6432a880ab5579b91ef637a0b3bb9a543f`  
		Last Modified: Tue, 16 Apr 2024 03:30:35 GMT  
		Size: 12.9 MB (12940665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3905c6570c57c33c32c7daea87d229ca9938b6522c9ff4819d25f56d45e2b289`  
		Last Modified: Tue, 16 Apr 2024 03:30:56 GMT  
		Size: 69.6 MB (69639882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a4990ec866ba156797117255a461c1a9bad60ccadbdceefd81b1399486fb434f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98021981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b54e8062c6ef9f28ac77f5b64f8372eca578655be85c6a77f848da130e71a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:38:36 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:38:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:38:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:38:36 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:38:40 GMT
ADD file:da0ff0dbc934fe8a302da2a67ea8c5ff869d6bfdd919e1e1956c06f0cf34caf5 in / 
# Wed, 17 Apr 2024 18:38:40 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 20:08:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 20:09:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0820294584b3892c5ee83c185febb4613e73d261e74e3fa651fbe35b0f997d0`  
		Last Modified: Thu, 25 Apr 2024 20:57:22 GMT  
		Size: 27.0 MB (27013669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f56ea049cf49cc715420b456371bc4769d7d37f5acaa9056f27fdb87c24713f`  
		Last Modified: Thu, 25 Apr 2024 20:57:21 GMT  
		Size: 10.7 MB (10690122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d79eaa04d8e6c5fd7ecf572a1bf445c11c214f114b4684d9e62a30871216fe`  
		Last Modified: Thu, 25 Apr 2024 20:57:39 GMT  
		Size: 60.3 MB (60318190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
