## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:9c6e460b0e6fb5de985ad6c910b589eb2f1e7f525e021ae20b7866ec1a52550a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:fd320abed3711552d46844d8d1be600629fbee7b40f0b6d1bb3f6fca47889fe5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60470718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d06b3f398f8e81cd0fa34198432d3549ff4c8fb985983c08539a6a6f87f31f38`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e85de8b3c72f249640131613d74d6b9b03c3abb7a01a276c154b001fd42367c7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58075831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de61035497a7c4bdbf7b64e70fe7cd9e9e2374e4f718618c9cdac923b11d383a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:23 GMT
ADD file:ecf2c81fa53759cae3e17b1b743a884b747d5d2b2676bb7f14bdb4fb1a5cb38c in / 
# Fri, 11 Dec 2020 02:09:35 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 02:04:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 02:04:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:74944684cd609943dde5912069d99b50bdb10f0cbca3bc5f96b0b17fc41f8c18`  
		Last Modified: Fri, 11 Dec 2020 02:18:35 GMT  
		Size: 44.1 MB (44089598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf108950f8cc0ac18c401de2c89700c6c85e5dbc0c26c5ce342f6c95ff25836`  
		Last Modified: Thu, 17 Dec 2020 02:19:47 GMT  
		Size: 9.8 MB (9826001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2a99d9fc9fe43ac9269dfdead78116e5999565777dfdb0b7b81c65e41a9099`  
		Last Modified: Thu, 17 Dec 2020 02:19:45 GMT  
		Size: 4.2 MB (4160232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b109a1209e5fa0720e02394c5c4ad73b574ee54f8f2a5ff6ba9c5014188c1957
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55483127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39de4c2a2623469e08c368b8f29b4be9d9c6c29f091ec193b3ff62ff90d55548`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:28:06 GMT
ADD file:e74dce76704e3faa6198db5cf4192fd431f5addf55f658277eb5b60d254fee8e in / 
# Fri, 11 Dec 2020 02:28:09 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:24:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:24:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:062f5403576d7e3aca1c92115ff0a9ea110b270cb0b61013efa86744515666fb`  
		Last Modified: Fri, 11 Dec 2020 02:36:48 GMT  
		Size: 42.1 MB (42117949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913e3a9a9e04d7e4fdefdcc5847233d712c26520bf9484ed8e890f521f2bbf41`  
		Last Modified: Thu, 17 Dec 2020 08:56:01 GMT  
		Size: 9.4 MB (9445217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d26373a692630f7276d1b4be2fc66079b5d68123d5ddc98490cc9a4d0775a31`  
		Last Modified: Thu, 17 Dec 2020 08:56:00 GMT  
		Size: 3.9 MB (3919961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2302a8dfb2e9723e060db3ab92e5d74221ec2aae9bf0d406505ebe42b3a66386
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (56973872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421390bfe74587737c15cae920d5370d6e395a7cff2d2496d0d126c04e6b7c29`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:48:16 GMT
ADD file:48e44714f486662ed380343e556f0f7411bd6600d916440063753c55d1f94b45 in / 
# Fri, 11 Dec 2020 02:48:17 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 19:00:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 19:00:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ecefb91918e846819df74a1beb8e41f454bef156738373818c20656a3a46d5f7`  
		Last Modified: Fri, 11 Dec 2020 02:55:36 GMT  
		Size: 43.2 MB (43175941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbc4aa0f5cdb9142c6a132303c43a6ac4227b4756b3f431c9e48499eb9a2904`  
		Last Modified: Fri, 11 Dec 2020 19:11:05 GMT  
		Size: 9.7 MB (9702496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8454d6fa6606ece6f85f95e9fbe351549d84085e6084902e37c0514065cead`  
		Last Modified: Fri, 11 Dec 2020 19:11:03 GMT  
		Size: 4.1 MB (4095435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:bbb246e68b0496090131a9e77f489d9a5d7ff6e5bc2659b39f765baaa14c97d0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61433387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2292b10e05dcbddd6bbe33398409a0fd628af86ca13e8c5fb5673275929042c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:38 GMT
ADD file:65da710638e196cb40b07b1d2461114bb3c8b34d69693449a905397c192f1ac0 in / 
# Fri, 11 Dec 2020 02:05:38 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:12:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c6c30bba175680710c6b02f65235cc2a0b8adf1ec4be1e440e260afda9487b37`  
		Last Modified: Fri, 11 Dec 2020 02:13:22 GMT  
		Size: 46.1 MB (46095117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc0247c6906d18f48f42d4ecdf060009453e884a50dba3d3b52166e5bd61ded`  
		Last Modified: Thu, 17 Dec 2020 08:29:18 GMT  
		Size: 10.8 MB (10774964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75bcca64ffc98da2fb811c456d5ab074caf61174cb723eb8429a5e4ade473a4`  
		Last Modified: Thu, 17 Dec 2020 08:29:15 GMT  
		Size: 4.6 MB (4563306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
