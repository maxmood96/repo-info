## `buildpack-deps:buster-curl`

```console
$ docker pull buildpack-deps@sha256:44f9a2520d1fdf9372e011d82060459b53163e653dc457ed6849ba12e04a2b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:buster-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a39a61263c8d104bf1ab39c151747547152748544446d2b28c32922b4cbdd0d8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68187637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05d3b2492fad072afc69c05e6875c117dbb80e0b82ae0a900bc75eb51c676ff`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:08 GMT
ADD file:d6d0bdf8cb07a7a0dc32e9df50ac80ca1a524c3fa48136892ded195061f2194c in / 
# Sat, 28 Dec 2019 04:21:09 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:47:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:47:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8f0fdd3eaac017684c880d836abdaf02f9db7ac8ecca970356482e3d8e315650`  
		Last Modified: Sat, 28 Dec 2019 04:25:39 GMT  
		Size: 50.4 MB (50379720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d918eaefd9de8a1595f56900fdb8ab65a03d64b1da1078da7c0b0bf6f7552a14`  
		Last Modified: Sat, 28 Dec 2019 05:01:44 GMT  
		Size: 7.8 MB (7811715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bf3e3107f525b7dea5b3cdfd15f62666066202105a0aaddbab2a02aefad1f7`  
		Last Modified: Sat, 28 Dec 2019 05:01:44 GMT  
		Size: 10.0 MB (9996202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:0f3feb46ff1d49075bd6fd8f9281a4af788b778ad99d7d697bed207b13f4ccba
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65138437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d059cedcf1656fa7c1d78b97b21592da22931ff3f1c86a1b5581d8dd706b41a5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:49:30 GMT
ADD file:dd72fb82d87c4594d064818aab5020766a85e76bd85305fea5eaf6dfd20a97fb in / 
# Sat, 28 Dec 2019 04:49:32 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:23:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:23:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3bf27a5276936429fef3702e21a1cfcfde88ef96196749cdf3e1b7576af5af38`  
		Last Modified: Sat, 28 Dec 2019 04:56:08 GMT  
		Size: 48.1 MB (48092858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bbc9740afdaf5d761dc8d69c82dc5e7fc1f1bcdd19849bd2c6ad632959b19f`  
		Last Modified: Sat, 28 Dec 2019 05:50:24 GMT  
		Size: 7.4 MB (7358639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ac01bbcc7211cc192a2700f12cd017f4d1848837cb4a6984c74d2f4786d14f`  
		Last Modified: Sat, 28 Dec 2019 05:50:24 GMT  
		Size: 9.7 MB (9686940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f89a3a8faaa55f6b3dbf4c68d9ee67998ffdb468f4ef35dcf8b84ec676dcfafc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62299149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c7bfdddf246bc672e9977fe40bff244235b3cee1b98f064f9041e643dbd9f6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:58:42 GMT
ADD file:26fba5cd6ba1fe45f19fb80d1c8e54eac5189e2b93e521b2ba6d5a6b54175e81 in / 
# Sat, 28 Dec 2019 04:58:45 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:43:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:43:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:760e5af4a2ec2472d42b6773d075af9d2a006e0b7725ba9992e530f561d326f8`  
		Last Modified: Sat, 28 Dec 2019 05:07:11 GMT  
		Size: 45.9 MB (45859628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93dc761fecef183bb949ae59f45d1f618cc3e8879cb25946ab48737d1d8a59b0`  
		Last Modified: Sat, 28 Dec 2019 07:07:06 GMT  
		Size: 7.1 MB (7096250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73181b0fe903be79034378988be75730f983b13ada732a04ea4f46f73b332896`  
		Last Modified: Sat, 28 Dec 2019 07:07:06 GMT  
		Size: 9.3 MB (9343271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d7f43d7936c010ae0ecf4208de9ca46dd430b24c6e37feb276630c421935c6da
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66836434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd2adfea6f1376f109eb35d7184b8c4d2d7575ea8b493e7b68320b5e7ead440`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:40:50 GMT
ADD file:b423f4b0ed41dfe1334031fe9b21f7e1c88ccb031d7e8f2ff165d618323424d7 in / 
# Sat, 01 Feb 2020 16:40:53 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:18:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:18:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:bc03a7ced18fc43ea9523dfb256d2c3fbb835dc0bb54bdb7fd309edf936a87e7`  
		Last Modified: Sat, 01 Feb 2020 16:46:06 GMT  
		Size: 49.2 MB (49171687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba9d528c1473d79c18b401d44ca06b9733d9c51a8699b98e8325c9de60b9739`  
		Last Modified: Sat, 01 Feb 2020 17:34:59 GMT  
		Size: 7.7 MB (7680993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981400d5d268dc989681d5f308b7d2e381809f0bcc82429f443f7539cf6117ba`  
		Last Modified: Sat, 01 Feb 2020 17:34:59 GMT  
		Size: 10.0 MB (9983754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ac4d7d014d1a465794dc10508a8b18e19cd5f3250092c1d73c76af9dc0bbd58a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69461934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089bc66ebbb2d8e0f331e5d97fd0d747a11445f858e66bd0ee45256187dc7f4f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:39:21 GMT
ADD file:b637f96d557a570f8ab83b28f7b9cdd128958359dd30dc2e03df70b799e132aa in / 
# Sat, 01 Feb 2020 16:39:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:23:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:24:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2b34644a479c82db66a603c0b0a1d990911345f8646498fa9b050f306d0e6bf2`  
		Last Modified: Sat, 01 Feb 2020 16:44:10 GMT  
		Size: 51.1 MB (51141949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2f611c9392c4fe86735b477d61fda0e95ea77486175a737114c51586ecce86`  
		Last Modified: Sat, 01 Feb 2020 17:42:17 GMT  
		Size: 8.0 MB (7981506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69713757cc2d87c3255331d40f5061a73ef412208961f1ddd67a59a375397fda`  
		Last Modified: Sat, 01 Feb 2020 17:42:17 GMT  
		Size: 10.3 MB (10338479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4bcab2bbd763ae20cb75de333534cf490204ed19b8c71696113048dbc5f0679b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73111682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cf72256d6f34de9e49afa17dbdcada2056aeeffd6b2aadab197c67be1e31ba`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:12 GMT
ADD file:7c5858835ffb42e32df47084d7f85ba9392c5e37ee636e19dfae15d858c5b6c4 in / 
# Sat, 28 Dec 2019 04:20:17 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:51:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:51:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0a9adf09915c3544b1264f206aec99890c8e5e5c358fc4327886fbdab3c9eecc`  
		Last Modified: Sat, 28 Dec 2019 04:27:21 GMT  
		Size: 54.1 MB (54132515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf9e003a90307c0e87a3bace1df7cc0c72889de0f3060d33cc175cd6bd9f40d`  
		Last Modified: Sat, 28 Dec 2019 07:21:47 GMT  
		Size: 8.3 MB (8252099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24889e07923c5eca1933bb3b0b8bdfc25a42834db78bae343f5fdf88cab3a23e`  
		Last Modified: Sat, 28 Dec 2019 07:21:47 GMT  
		Size: 10.7 MB (10727068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:97298d2e4356e25d136da5de50b4514a70d673eff7de5eb84dd6fe607537fba6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66215188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55e1a469dad5526612922a49ec5a556c42b4c02a437e6a9f59cb478b2d844d4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:51 GMT
ADD file:aeaf0b11195b2ba7eb7890ce128ad93c114a8e183a516cf2e4ea42da324c57ea in / 
# Sat, 28 Dec 2019 04:41:51 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:44:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:45:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3596c5a237f76c32832c1879a3d0c763989cb13fac0024673b03e9b549b868ea`  
		Last Modified: Sat, 28 Dec 2019 04:44:54 GMT  
		Size: 49.0 MB (48954508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a87e4c2949f278ec7636f6762169d70bd2588ed301cc3e2721aa830a9227fc`  
		Last Modified: Sat, 28 Dec 2019 05:53:25 GMT  
		Size: 7.4 MB (7380503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33b91142ed28640cd70826a84025844f0fa1e7bc50f10b67f6ee03ed2f013ae`  
		Last Modified: Sat, 28 Dec 2019 05:53:25 GMT  
		Size: 9.9 MB (9880177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
