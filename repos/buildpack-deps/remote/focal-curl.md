## `buildpack-deps:focal-curl`

```console
$ docker pull buildpack-deps@sha256:7a23a69709868b5e9f80378bc2af1c80c6ce809651023d48ab2bfc589b494f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:focal-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:94e38f42903a67443ad5b6fa21aa7af44330b0ddb7dd8fec07301482dcc274b5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39733311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a602524481be3a1ae09767c761c5669a9b75810e61aefc344e57b79dbd86309`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:59:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:86e5016c269355b382c9cabab4f6646d56d75914f20d545289970436dae431b1`  
		Last Modified: Fri, 11 Oct 2024 08:12:19 GMT  
		Size: 28.6 MB (28583948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3c174c6b504b85dc37643886585b2569b5cdafef538fba161e83e9b4778dda`  
		Last Modified: Wed, 16 Oct 2024 02:08:03 GMT  
		Size: 11.1 MB (11149363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6d5af74c4c9c3fcc10fd966a3aba732b040df8e0f8b64579fe8709abf6828069
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34222511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6793273caf9681cfeeec22a2d20ae25d259ccb4b033642782a446675710937`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:34 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:36 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Fri, 11 Oct 2024 03:38:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7474977cdbc1bb838c947dfdfa420a17f877727196fdf929b5bbfb57ddc59d1e`  
		Last Modified: Wed, 16 Oct 2024 01:27:36 GMT  
		Size: 24.6 MB (24600743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf94ef511a5b70086da0dbde4b10efbb6a0a474eca153a011c1115ac2c3f095`  
		Last Modified: Wed, 16 Oct 2024 01:27:35 GMT  
		Size: 9.6 MB (9621768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:981a354c335094f3746a3364ae7ed63fe12b58e4eb841b2f1d5fc66e3276f29d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38197604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13084ced7fb40b2e72f496978a2b6841e6ccdd0c97df7a2922f8ad2288d180ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:21:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:963ceec6c2ca13b343a25d3157e3e30ffa80fc297ad5e3f78d8f43087427b2d3`  
		Last Modified: Sat, 12 Oct 2024 07:30:30 GMT  
		Size: 27.2 MB (27204259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a26dece8dd0e19868776e664f1845a9814a1f9f8561192d9ab9bb201f219e88`  
		Last Modified: Wed, 16 Oct 2024 01:29:52 GMT  
		Size: 11.0 MB (10993345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5813c44733c05ac8f2e589a10fbb3dff6773488a51e8d2a6b0c19d78a3e2b2fe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46278847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3d1a0327b1c6fabad97bf55eaf53ded9fa9052e73833b3cdd37dab0c60448a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:50:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d534431b5b1c76e43335aa792bdca680eb5ebbeaeea07c6eeae4aa9d2cb8e841`  
		Last Modified: Wed, 16 Oct 2024 01:44:06 GMT  
		Size: 33.3 MB (33315666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5ceded1fb62333ad13f625f4b106d80d9b82c064bbf2410811567d29993427`  
		Last Modified: Wed, 16 Oct 2024 02:01:05 GMT  
		Size: 13.0 MB (12963181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:cf51dfb6844a8168bb45516adac8fe583608d638eb19a4937ed76b1faf10f5eb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33886994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0caf00bd51c4aba7d35a1cfb79ba0956d472c90f6b5ca1ae8db5959711e7e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:55:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:55:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:55:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:55:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:56:05 GMT
ADD file:f99ddac77e3940392223df513cab07fbc1fbae5269b21e7c49c63c99a7e47b14 in / 
# Fri, 11 Oct 2024 03:56:07 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 03:13:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fd752079599d09732ebbf1df6f25eb9d82bba65ae8d0a5b9c9a50198e7b87bcf`  
		Last Modified: Wed, 16 Oct 2024 03:23:21 GMT  
		Size: 24.2 MB (24248406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795dc62932e4af3f391cb1dc8fa846d59ebed7d3c85ad038201d145e6368c75d`  
		Last Modified: Wed, 16 Oct 2024 03:23:11 GMT  
		Size: 9.6 MB (9638588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c5031c9f74e3eebfed6b04291ce3dddf756a7ec7b4ae99f6684662418bd0ec07
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37717933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c51eb46351e70f1ffaf7c77701c0a457ec94962754b90d3c775cf57fdfe893`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:23 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:24 GMT
ADD file:e3e9bad1c3576edf8ddea2dd7af2ed8ecac1ad0b15d714dd9c51f679d44d13b6 in / 
# Fri, 11 Oct 2024 03:38:24 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:09:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:527495b21ae4efd3ff5dea679dc71a1631f2a861f8be8f838ff10c5176246b80`  
		Last Modified: Wed, 16 Oct 2024 01:16:56 GMT  
		Size: 27.0 MB (27012438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e68a2830833de9a843a3ee8d2677504bcdad17830e1e5e98506e72e7b73dfd7`  
		Last Modified: Wed, 16 Oct 2024 01:16:53 GMT  
		Size: 10.7 MB (10705495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
