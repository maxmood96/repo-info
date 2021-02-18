<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spiped`

-	[`spiped:1`](#spiped1)
-	[`spiped:1.6`](#spiped16)
-	[`spiped:1.6.1`](#spiped161)
-	[`spiped:1.6.1-alpine`](#spiped161-alpine)
-	[`spiped:1.6-alpine`](#spiped16-alpine)
-	[`spiped:1-alpine`](#spiped1-alpine)
-	[`spiped:alpine`](#spipedalpine)
-	[`spiped:latest`](#spipedlatest)

## `spiped:1`

```console
$ docker pull spiped@sha256:4e0757d83a01c2abc624d004ea3feb13bbd81c33ff0294e91744575688e0e92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `spiped:1` - linux; amd64

```console
$ docker pull spiped@sha256:de2d45b0f59312e4abff77a82b78eaac004c3224734eedbc7334680c7ec5443f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36262768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897fcb40d5e49b8a35aa9e61c14eff1f62c615775ab19bff009fbbeafff2b106`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 11:21:37 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 13 Feb 2021 00:09:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 13 Feb 2021 00:09:09 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 00:09:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 13 Feb 2021 00:09:59 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 00:10:00 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 00:10:01 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 00:10:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 00:10:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de752b69da20dffa4f368194c801b91db7f8109eb73f00e28fcf2534595c2391`  
		Last Modified: Tue, 09 Feb 2021 11:22:39 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d13c52f8d2f79744057e6229950b1dfc5bd6291a85638e41c94d0bf6ae4e29`  
		Last Modified: Sat, 13 Feb 2021 00:11:29 GMT  
		Size: 2.1 MB (2128155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce83854aeaf080766f7945048114fa3e9b3416b345ca8aff96978c9c7f54953`  
		Last Modified: Sat, 13 Feb 2021 00:11:31 GMT  
		Size: 7.0 MB (7037301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb829d6ea4836c4cb76df6e6b6006024c209af26a1c18390c00a81ae68243bb`  
		Last Modified: Sat, 13 Feb 2021 00:11:28 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98a7fedb7f92d778864b0fcf2422f4ef009b2ab40c930b69020c825e6dec72c`  
		Last Modified: Sat, 13 Feb 2021 00:11:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:5fdf9146d8023cd6e901dbceff493b9883020acd456eb8bfbd5c480fcd681210
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32160479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1781b7c6ba805844ffb5302f90107b4f5d7cc5f1fd80060ce54ea64fbad5616c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 11:43:19 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 12 Feb 2021 22:52:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 12 Feb 2021 22:52:10 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Feb 2021 22:53:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 12 Feb 2021 22:53:05 GMT
VOLUME [/spiped]
# Fri, 12 Feb 2021 22:53:06 GMT
WORKDIR /spiped
# Fri, 12 Feb 2021 22:53:07 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Feb 2021 22:53:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Feb 2021 22:53:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346f1f77623bfcedac114c95542f4a432dbfac2903c21d7af096733db6f08d7a`  
		Last Modified: Tue, 09 Feb 2021 11:44:58 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b20e94947775259ce6bf04cfa19152b029d3365a89d4ccc0843ae79aa8bd4f2`  
		Last Modified: Fri, 12 Feb 2021 22:53:24 GMT  
		Size: 1.8 MB (1839109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5daf79a4e2ff35a482480dc5ed9294bc9b4a8973856555b77b39e3db207b7e`  
		Last Modified: Fri, 12 Feb 2021 22:53:26 GMT  
		Size: 5.5 MB (5479875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384e633e1a26bfac8686c377988482dd352c68b9f02ba80edcda2501879211a1`  
		Last Modified: Fri, 12 Feb 2021 22:53:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e3d0ff8a742e94655d7e9b5e7444b78818640156c0ca4672cfa957a605307f`  
		Last Modified: Fri, 12 Feb 2021 22:53:23 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:3f1874e1134dbfca6d910ae69ff8d37e2a72d12404d8a9fd0fe0bd0c91e6db78
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29750488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c287c25628c3da85c966ccc96d6e3e6e7a542d2487caaa805d5fa8a0525ea5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 19:35:37 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 12 Feb 2021 22:38:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 12 Feb 2021 22:38:45 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Feb 2021 22:39:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 12 Feb 2021 22:39:30 GMT
VOLUME [/spiped]
# Fri, 12 Feb 2021 22:39:30 GMT
WORKDIR /spiped
# Fri, 12 Feb 2021 22:39:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Feb 2021 22:39:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Feb 2021 22:39:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5afe0266f6b6542f91658ca8ec8b87ac3e40c9e40d88f3ebfb311da27ffaa976`  
		Last Modified: Tue, 09 Feb 2021 19:37:10 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a439028cc7f7cbb2502897e215fe8142424bac7b8461519a3721306ca16262`  
		Last Modified: Fri, 12 Feb 2021 22:40:38 GMT  
		Size: 1.8 MB (1759313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e175e160ff82eee0dc76239d6e920ad6fce1b07298b3bd90e8120c021b7af0dd`  
		Last Modified: Fri, 12 Feb 2021 22:40:40 GMT  
		Size: 5.3 MB (5285596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4c31222b7eba85c87a5dbbee1012985dae7f842a0c60e03cc2641b409aa474`  
		Last Modified: Fri, 12 Feb 2021 22:40:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88900a0b87f635433ee9e3c471b1a10b21ea199374733be54fb2595691999e2`  
		Last Modified: Fri, 12 Feb 2021 22:40:38 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:aeb7d15ee44fc1b03bfd46be858735700424119244cb66f38e14e9630c63e7ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33766524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e1f2dc0e564ffcc34b5a7d98c4213648ab3f8a22f84e0db2b43178567f3a12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 18:18:32 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 13 Feb 2021 01:48:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 13 Feb 2021 01:48:09 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 01:48:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 13 Feb 2021 01:48:57 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 01:48:58 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 01:48:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 01:49:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 01:49:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516c8ae6b6958174393d642fd4693aea0a041e432ce8d8758b052224d96cb2fa`  
		Last Modified: Tue, 09 Feb 2021 18:20:06 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03005b703ccb19a3569b35a5b9bf1bfef156941eaf489b91ff81efde2e7ea584`  
		Last Modified: Sat, 13 Feb 2021 01:50:07 GMT  
		Size: 2.0 MB (2007571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c581bbabc2c122ca024c49c3aa7d735e4cfba75a1560c8c873223c66d0c57e6a`  
		Last Modified: Sat, 13 Feb 2021 01:50:08 GMT  
		Size: 5.9 MB (5905293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c709ad2716ce7723cf89c0c553985816902e98c25f46520d8faa51d120c7508f`  
		Last Modified: Sat, 13 Feb 2021 01:50:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe585f4a68228bec2b5b6765c7a8a860d41e59a842e3b43871e7120172ab40c7`  
		Last Modified: Sat, 13 Feb 2021 01:50:06 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:4f80cd66b8eb83d68da1b3cd894fe37462760fe5278f6973301e26f1af90bc91
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41520139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96e1652c7ef7e3d880320ae65765f36dfe4d599e1ca9ac8c0154dcf0e54633a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 18:39:55 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 13 Feb 2021 00:58:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 13 Feb 2021 00:58:43 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 00:59:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 13 Feb 2021 00:59:17 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 00:59:17 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 00:59:18 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 00:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 00:59:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbea90aac4746d1c996386053d6406bfa4610451eae6d17da249dee74c9b3a68`  
		Last Modified: Tue, 09 Feb 2021 18:40:55 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b87a23d1edb8994421e0ef8e6ae3e7a6364755d7e174130d7b4076dfa2119e`  
		Last Modified: Sat, 13 Feb 2021 01:00:08 GMT  
		Size: 2.1 MB (2132258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7cffa8181e625c430a03c89cc64ae89e03825bd80c01986ce5486ad61b4c12`  
		Last Modified: Sat, 13 Feb 2021 01:00:11 GMT  
		Size: 11.6 MB (11632985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15dfc8a7a89424ce7b74424465fcef8b14d61f39590f94169b3a7afd30130b0`  
		Last Modified: Sat, 13 Feb 2021 01:00:08 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3837cf2d6a87c1b6e64337cafb4ddb0959d201146a766002cc849caa670bae`  
		Last Modified: Sat, 13 Feb 2021 01:00:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:25a5e4c9bfecee13942120bcc34a2cdb13e00addd065a17df1302153ead12de4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33895238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818a59f972b27eb92864d12c7304285f5966446e58096f31ad3b67a0bc8d07d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:51:48 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 12 Feb 2021 23:11:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 12 Feb 2021 23:11:03 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Feb 2021 23:12:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 12 Feb 2021 23:12:11 GMT
VOLUME [/spiped]
# Fri, 12 Feb 2021 23:12:12 GMT
WORKDIR /spiped
# Fri, 12 Feb 2021 23:12:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Feb 2021 23:12:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Feb 2021 23:12:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8e1cbf99b578f9b5da0b78824733a66db880b685f597795dd41a08ac6b4f2f`  
		Last Modified: Tue, 09 Feb 2021 17:53:36 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5463eef3d8ce71368876b45ca24071008cc083ea16ea90ad16da78aee1b06eb0`  
		Last Modified: Fri, 12 Feb 2021 23:12:26 GMT  
		Size: 1.7 MB (1712078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07c83f952ec2caa0e8a9319f93360620700120836fe9678c29036c7cf9868e9`  
		Last Modified: Fri, 12 Feb 2021 23:12:31 GMT  
		Size: 6.4 MB (6416347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b88510861e3f585271a563d2bee51e8dc1659e7abc654317636fd8a6e35956`  
		Last Modified: Fri, 12 Feb 2021 23:12:24 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8a904b2624ec463e93f83225ac51eebd738a0473f323cf0121dcf664488951`  
		Last Modified: Fri, 12 Feb 2021 23:12:25 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:864f9629da12aace742df3cd8167639ca43ff06a00763b99c31dcba10699a00e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39490261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749c18efc7646905a7417cb2107c88294bb750ed6bc8039f46b4311923b6e779`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:15:19 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 13 Feb 2021 02:30:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 13 Feb 2021 02:30:40 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 02:33:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 13 Feb 2021 02:34:02 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 02:34:09 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 02:34:10 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 02:34:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 02:34:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46b97146405ece3ed453ad4ebc496b4b66b0fff54fdc49d2f4d3175043dffaf`  
		Last Modified: Tue, 09 Feb 2021 04:26:38 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47130d66484e5dc6224d68f7eaf7129048723a038246f1ba3288bc669594ce4d`  
		Last Modified: Sat, 13 Feb 2021 02:36:06 GMT  
		Size: 2.2 MB (2224915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f7be408970c00a6f67d09788fe2ae7d9bee14d0ddedf38e826cbedc4e12d6e`  
		Last Modified: Sat, 13 Feb 2021 02:36:07 GMT  
		Size: 6.7 MB (6743622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed58efc2e2df4e58c29b6b3946f036cdf35e85ba6b21cf906c7fe425b1efc82a`  
		Last Modified: Sat, 13 Feb 2021 02:36:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5da930633055937f1ba62f43cf83b555b527d1cd8255d66ac9d6281f3afa41d`  
		Last Modified: Sat, 13 Feb 2021 02:36:06 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:f1fc57dae92710b70032be2526f79e54964e55f92c1743f69ec7cf0a676d8116
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33477416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dda528269da27ad9d1592ca7bc595ecbacc814c873d1441327b98560f8a43b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:33:39 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 13 Feb 2021 03:10:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 13 Feb 2021 03:10:56 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 03:11:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 13 Feb 2021 03:11:22 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 03:11:22 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 03:11:22 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 03:11:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 03:11:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b494d8c5eab48f88712e47a52fa76da28e3b84d610e47c02ef6554cc1e57e98a`  
		Last Modified: Tue, 09 Feb 2021 06:34:18 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916e90eba0ded4a99e0c1e86e0657b977665bf19661f2c18005fc6d6745d7fd4`  
		Last Modified: Sat, 13 Feb 2021 03:12:19 GMT  
		Size: 1.8 MB (1821717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9478c638398830f42321041df73fb7c8005dd7c336c933045b5f043fe1e8786`  
		Last Modified: Sat, 13 Feb 2021 03:12:19 GMT  
		Size: 5.9 MB (5943471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fb1c3cf1445657cf0a44894ccf3da2d62b39264d89fcbecc0e2db075fcfdcf`  
		Last Modified: Sat, 13 Feb 2021 03:12:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f2ae3abab433a32b5e6ba282e6544117d7a01f4fd183d4a7582a4c5a64479f`  
		Last Modified: Sat, 13 Feb 2021 03:12:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6`

```console
$ docker pull spiped@sha256:4e0757d83a01c2abc624d004ea3feb13bbd81c33ff0294e91744575688e0e92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `spiped:1.6` - linux; amd64

```console
$ docker pull spiped@sha256:de2d45b0f59312e4abff77a82b78eaac004c3224734eedbc7334680c7ec5443f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36262768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897fcb40d5e49b8a35aa9e61c14eff1f62c615775ab19bff009fbbeafff2b106`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 11:21:37 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 13 Feb 2021 00:09:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 13 Feb 2021 00:09:09 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 00:09:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 13 Feb 2021 00:09:59 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 00:10:00 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 00:10:01 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 00:10:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 00:10:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de752b69da20dffa4f368194c801b91db7f8109eb73f00e28fcf2534595c2391`  
		Last Modified: Tue, 09 Feb 2021 11:22:39 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d13c52f8d2f79744057e6229950b1dfc5bd6291a85638e41c94d0bf6ae4e29`  
		Last Modified: Sat, 13 Feb 2021 00:11:29 GMT  
		Size: 2.1 MB (2128155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce83854aeaf080766f7945048114fa3e9b3416b345ca8aff96978c9c7f54953`  
		Last Modified: Sat, 13 Feb 2021 00:11:31 GMT  
		Size: 7.0 MB (7037301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb829d6ea4836c4cb76df6e6b6006024c209af26a1c18390c00a81ae68243bb`  
		Last Modified: Sat, 13 Feb 2021 00:11:28 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98a7fedb7f92d778864b0fcf2422f4ef009b2ab40c930b69020c825e6dec72c`  
		Last Modified: Sat, 13 Feb 2021 00:11:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:5fdf9146d8023cd6e901dbceff493b9883020acd456eb8bfbd5c480fcd681210
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32160479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1781b7c6ba805844ffb5302f90107b4f5d7cc5f1fd80060ce54ea64fbad5616c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 11:43:19 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 12 Feb 2021 22:52:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 12 Feb 2021 22:52:10 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Feb 2021 22:53:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 12 Feb 2021 22:53:05 GMT
VOLUME [/spiped]
# Fri, 12 Feb 2021 22:53:06 GMT
WORKDIR /spiped
# Fri, 12 Feb 2021 22:53:07 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Feb 2021 22:53:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Feb 2021 22:53:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346f1f77623bfcedac114c95542f4a432dbfac2903c21d7af096733db6f08d7a`  
		Last Modified: Tue, 09 Feb 2021 11:44:58 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b20e94947775259ce6bf04cfa19152b029d3365a89d4ccc0843ae79aa8bd4f2`  
		Last Modified: Fri, 12 Feb 2021 22:53:24 GMT  
		Size: 1.8 MB (1839109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5daf79a4e2ff35a482480dc5ed9294bc9b4a8973856555b77b39e3db207b7e`  
		Last Modified: Fri, 12 Feb 2021 22:53:26 GMT  
		Size: 5.5 MB (5479875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384e633e1a26bfac8686c377988482dd352c68b9f02ba80edcda2501879211a1`  
		Last Modified: Fri, 12 Feb 2021 22:53:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e3d0ff8a742e94655d7e9b5e7444b78818640156c0ca4672cfa957a605307f`  
		Last Modified: Fri, 12 Feb 2021 22:53:23 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:3f1874e1134dbfca6d910ae69ff8d37e2a72d12404d8a9fd0fe0bd0c91e6db78
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29750488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c287c25628c3da85c966ccc96d6e3e6e7a542d2487caaa805d5fa8a0525ea5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 19:35:37 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 12 Feb 2021 22:38:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 12 Feb 2021 22:38:45 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Feb 2021 22:39:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 12 Feb 2021 22:39:30 GMT
VOLUME [/spiped]
# Fri, 12 Feb 2021 22:39:30 GMT
WORKDIR /spiped
# Fri, 12 Feb 2021 22:39:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Feb 2021 22:39:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Feb 2021 22:39:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5afe0266f6b6542f91658ca8ec8b87ac3e40c9e40d88f3ebfb311da27ffaa976`  
		Last Modified: Tue, 09 Feb 2021 19:37:10 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a439028cc7f7cbb2502897e215fe8142424bac7b8461519a3721306ca16262`  
		Last Modified: Fri, 12 Feb 2021 22:40:38 GMT  
		Size: 1.8 MB (1759313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e175e160ff82eee0dc76239d6e920ad6fce1b07298b3bd90e8120c021b7af0dd`  
		Last Modified: Fri, 12 Feb 2021 22:40:40 GMT  
		Size: 5.3 MB (5285596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4c31222b7eba85c87a5dbbee1012985dae7f842a0c60e03cc2641b409aa474`  
		Last Modified: Fri, 12 Feb 2021 22:40:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88900a0b87f635433ee9e3c471b1a10b21ea199374733be54fb2595691999e2`  
		Last Modified: Fri, 12 Feb 2021 22:40:38 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:aeb7d15ee44fc1b03bfd46be858735700424119244cb66f38e14e9630c63e7ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33766524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e1f2dc0e564ffcc34b5a7d98c4213648ab3f8a22f84e0db2b43178567f3a12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 18:18:32 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 13 Feb 2021 01:48:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 13 Feb 2021 01:48:09 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 01:48:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 13 Feb 2021 01:48:57 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 01:48:58 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 01:48:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 01:49:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 01:49:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516c8ae6b6958174393d642fd4693aea0a041e432ce8d8758b052224d96cb2fa`  
		Last Modified: Tue, 09 Feb 2021 18:20:06 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03005b703ccb19a3569b35a5b9bf1bfef156941eaf489b91ff81efde2e7ea584`  
		Last Modified: Sat, 13 Feb 2021 01:50:07 GMT  
		Size: 2.0 MB (2007571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c581bbabc2c122ca024c49c3aa7d735e4cfba75a1560c8c873223c66d0c57e6a`  
		Last Modified: Sat, 13 Feb 2021 01:50:08 GMT  
		Size: 5.9 MB (5905293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c709ad2716ce7723cf89c0c553985816902e98c25f46520d8faa51d120c7508f`  
		Last Modified: Sat, 13 Feb 2021 01:50:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe585f4a68228bec2b5b6765c7a8a860d41e59a842e3b43871e7120172ab40c7`  
		Last Modified: Sat, 13 Feb 2021 01:50:06 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:4f80cd66b8eb83d68da1b3cd894fe37462760fe5278f6973301e26f1af90bc91
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41520139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96e1652c7ef7e3d880320ae65765f36dfe4d599e1ca9ac8c0154dcf0e54633a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 18:39:55 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 13 Feb 2021 00:58:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 13 Feb 2021 00:58:43 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 00:59:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 13 Feb 2021 00:59:17 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 00:59:17 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 00:59:18 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 00:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 00:59:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbea90aac4746d1c996386053d6406bfa4610451eae6d17da249dee74c9b3a68`  
		Last Modified: Tue, 09 Feb 2021 18:40:55 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b87a23d1edb8994421e0ef8e6ae3e7a6364755d7e174130d7b4076dfa2119e`  
		Last Modified: Sat, 13 Feb 2021 01:00:08 GMT  
		Size: 2.1 MB (2132258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7cffa8181e625c430a03c89cc64ae89e03825bd80c01986ce5486ad61b4c12`  
		Last Modified: Sat, 13 Feb 2021 01:00:11 GMT  
		Size: 11.6 MB (11632985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15dfc8a7a89424ce7b74424465fcef8b14d61f39590f94169b3a7afd30130b0`  
		Last Modified: Sat, 13 Feb 2021 01:00:08 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3837cf2d6a87c1b6e64337cafb4ddb0959d201146a766002cc849caa670bae`  
		Last Modified: Sat, 13 Feb 2021 01:00:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:25a5e4c9bfecee13942120bcc34a2cdb13e00addd065a17df1302153ead12de4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33895238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818a59f972b27eb92864d12c7304285f5966446e58096f31ad3b67a0bc8d07d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:51:48 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 12 Feb 2021 23:11:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 12 Feb 2021 23:11:03 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Feb 2021 23:12:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 12 Feb 2021 23:12:11 GMT
VOLUME [/spiped]
# Fri, 12 Feb 2021 23:12:12 GMT
WORKDIR /spiped
# Fri, 12 Feb 2021 23:12:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Feb 2021 23:12:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Feb 2021 23:12:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8e1cbf99b578f9b5da0b78824733a66db880b685f597795dd41a08ac6b4f2f`  
		Last Modified: Tue, 09 Feb 2021 17:53:36 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5463eef3d8ce71368876b45ca24071008cc083ea16ea90ad16da78aee1b06eb0`  
		Last Modified: Fri, 12 Feb 2021 23:12:26 GMT  
		Size: 1.7 MB (1712078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07c83f952ec2caa0e8a9319f93360620700120836fe9678c29036c7cf9868e9`  
		Last Modified: Fri, 12 Feb 2021 23:12:31 GMT  
		Size: 6.4 MB (6416347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b88510861e3f585271a563d2bee51e8dc1659e7abc654317636fd8a6e35956`  
		Last Modified: Fri, 12 Feb 2021 23:12:24 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8a904b2624ec463e93f83225ac51eebd738a0473f323cf0121dcf664488951`  
		Last Modified: Fri, 12 Feb 2021 23:12:25 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:864f9629da12aace742df3cd8167639ca43ff06a00763b99c31dcba10699a00e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39490261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749c18efc7646905a7417cb2107c88294bb750ed6bc8039f46b4311923b6e779`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:15:19 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 13 Feb 2021 02:30:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 13 Feb 2021 02:30:40 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 02:33:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 13 Feb 2021 02:34:02 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 02:34:09 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 02:34:10 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 02:34:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 02:34:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46b97146405ece3ed453ad4ebc496b4b66b0fff54fdc49d2f4d3175043dffaf`  
		Last Modified: Tue, 09 Feb 2021 04:26:38 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47130d66484e5dc6224d68f7eaf7129048723a038246f1ba3288bc669594ce4d`  
		Last Modified: Sat, 13 Feb 2021 02:36:06 GMT  
		Size: 2.2 MB (2224915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f7be408970c00a6f67d09788fe2ae7d9bee14d0ddedf38e826cbedc4e12d6e`  
		Last Modified: Sat, 13 Feb 2021 02:36:07 GMT  
		Size: 6.7 MB (6743622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed58efc2e2df4e58c29b6b3946f036cdf35e85ba6b21cf906c7fe425b1efc82a`  
		Last Modified: Sat, 13 Feb 2021 02:36:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5da930633055937f1ba62f43cf83b555b527d1cd8255d66ac9d6281f3afa41d`  
		Last Modified: Sat, 13 Feb 2021 02:36:06 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:f1fc57dae92710b70032be2526f79e54964e55f92c1743f69ec7cf0a676d8116
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33477416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dda528269da27ad9d1592ca7bc595ecbacc814c873d1441327b98560f8a43b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:33:39 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 13 Feb 2021 03:10:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 13 Feb 2021 03:10:56 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 03:11:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 13 Feb 2021 03:11:22 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 03:11:22 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 03:11:22 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 03:11:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 03:11:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b494d8c5eab48f88712e47a52fa76da28e3b84d610e47c02ef6554cc1e57e98a`  
		Last Modified: Tue, 09 Feb 2021 06:34:18 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916e90eba0ded4a99e0c1e86e0657b977665bf19661f2c18005fc6d6745d7fd4`  
		Last Modified: Sat, 13 Feb 2021 03:12:19 GMT  
		Size: 1.8 MB (1821717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9478c638398830f42321041df73fb7c8005dd7c336c933045b5f043fe1e8786`  
		Last Modified: Sat, 13 Feb 2021 03:12:19 GMT  
		Size: 5.9 MB (5943471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fb1c3cf1445657cf0a44894ccf3da2d62b39264d89fcbecc0e2db075fcfdcf`  
		Last Modified: Sat, 13 Feb 2021 03:12:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f2ae3abab433a32b5e6ba282e6544117d7a01f4fd183d4a7582a4c5a64479f`  
		Last Modified: Sat, 13 Feb 2021 03:12:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.1`

```console
$ docker pull spiped@sha256:4e0757d83a01c2abc624d004ea3feb13bbd81c33ff0294e91744575688e0e92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `spiped:1.6.1` - linux; amd64

```console
$ docker pull spiped@sha256:de2d45b0f59312e4abff77a82b78eaac004c3224734eedbc7334680c7ec5443f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36262768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897fcb40d5e49b8a35aa9e61c14eff1f62c615775ab19bff009fbbeafff2b106`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 11:21:37 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 13 Feb 2021 00:09:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 13 Feb 2021 00:09:09 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 00:09:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 13 Feb 2021 00:09:59 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 00:10:00 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 00:10:01 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 00:10:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 00:10:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de752b69da20dffa4f368194c801b91db7f8109eb73f00e28fcf2534595c2391`  
		Last Modified: Tue, 09 Feb 2021 11:22:39 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d13c52f8d2f79744057e6229950b1dfc5bd6291a85638e41c94d0bf6ae4e29`  
		Last Modified: Sat, 13 Feb 2021 00:11:29 GMT  
		Size: 2.1 MB (2128155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce83854aeaf080766f7945048114fa3e9b3416b345ca8aff96978c9c7f54953`  
		Last Modified: Sat, 13 Feb 2021 00:11:31 GMT  
		Size: 7.0 MB (7037301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb829d6ea4836c4cb76df6e6b6006024c209af26a1c18390c00a81ae68243bb`  
		Last Modified: Sat, 13 Feb 2021 00:11:28 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98a7fedb7f92d778864b0fcf2422f4ef009b2ab40c930b69020c825e6dec72c`  
		Last Modified: Sat, 13 Feb 2021 00:11:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:5fdf9146d8023cd6e901dbceff493b9883020acd456eb8bfbd5c480fcd681210
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32160479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1781b7c6ba805844ffb5302f90107b4f5d7cc5f1fd80060ce54ea64fbad5616c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 11:43:19 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 12 Feb 2021 22:52:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 12 Feb 2021 22:52:10 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Feb 2021 22:53:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 12 Feb 2021 22:53:05 GMT
VOLUME [/spiped]
# Fri, 12 Feb 2021 22:53:06 GMT
WORKDIR /spiped
# Fri, 12 Feb 2021 22:53:07 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Feb 2021 22:53:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Feb 2021 22:53:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346f1f77623bfcedac114c95542f4a432dbfac2903c21d7af096733db6f08d7a`  
		Last Modified: Tue, 09 Feb 2021 11:44:58 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b20e94947775259ce6bf04cfa19152b029d3365a89d4ccc0843ae79aa8bd4f2`  
		Last Modified: Fri, 12 Feb 2021 22:53:24 GMT  
		Size: 1.8 MB (1839109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5daf79a4e2ff35a482480dc5ed9294bc9b4a8973856555b77b39e3db207b7e`  
		Last Modified: Fri, 12 Feb 2021 22:53:26 GMT  
		Size: 5.5 MB (5479875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384e633e1a26bfac8686c377988482dd352c68b9f02ba80edcda2501879211a1`  
		Last Modified: Fri, 12 Feb 2021 22:53:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e3d0ff8a742e94655d7e9b5e7444b78818640156c0ca4672cfa957a605307f`  
		Last Modified: Fri, 12 Feb 2021 22:53:23 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:3f1874e1134dbfca6d910ae69ff8d37e2a72d12404d8a9fd0fe0bd0c91e6db78
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29750488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c287c25628c3da85c966ccc96d6e3e6e7a542d2487caaa805d5fa8a0525ea5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 19:35:37 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 12 Feb 2021 22:38:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 12 Feb 2021 22:38:45 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Feb 2021 22:39:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 12 Feb 2021 22:39:30 GMT
VOLUME [/spiped]
# Fri, 12 Feb 2021 22:39:30 GMT
WORKDIR /spiped
# Fri, 12 Feb 2021 22:39:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Feb 2021 22:39:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Feb 2021 22:39:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5afe0266f6b6542f91658ca8ec8b87ac3e40c9e40d88f3ebfb311da27ffaa976`  
		Last Modified: Tue, 09 Feb 2021 19:37:10 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a439028cc7f7cbb2502897e215fe8142424bac7b8461519a3721306ca16262`  
		Last Modified: Fri, 12 Feb 2021 22:40:38 GMT  
		Size: 1.8 MB (1759313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e175e160ff82eee0dc76239d6e920ad6fce1b07298b3bd90e8120c021b7af0dd`  
		Last Modified: Fri, 12 Feb 2021 22:40:40 GMT  
		Size: 5.3 MB (5285596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4c31222b7eba85c87a5dbbee1012985dae7f842a0c60e03cc2641b409aa474`  
		Last Modified: Fri, 12 Feb 2021 22:40:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88900a0b87f635433ee9e3c471b1a10b21ea199374733be54fb2595691999e2`  
		Last Modified: Fri, 12 Feb 2021 22:40:38 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:aeb7d15ee44fc1b03bfd46be858735700424119244cb66f38e14e9630c63e7ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33766524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e1f2dc0e564ffcc34b5a7d98c4213648ab3f8a22f84e0db2b43178567f3a12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 18:18:32 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 13 Feb 2021 01:48:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 13 Feb 2021 01:48:09 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 01:48:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 13 Feb 2021 01:48:57 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 01:48:58 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 01:48:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 01:49:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 01:49:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516c8ae6b6958174393d642fd4693aea0a041e432ce8d8758b052224d96cb2fa`  
		Last Modified: Tue, 09 Feb 2021 18:20:06 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03005b703ccb19a3569b35a5b9bf1bfef156941eaf489b91ff81efde2e7ea584`  
		Last Modified: Sat, 13 Feb 2021 01:50:07 GMT  
		Size: 2.0 MB (2007571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c581bbabc2c122ca024c49c3aa7d735e4cfba75a1560c8c873223c66d0c57e6a`  
		Last Modified: Sat, 13 Feb 2021 01:50:08 GMT  
		Size: 5.9 MB (5905293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c709ad2716ce7723cf89c0c553985816902e98c25f46520d8faa51d120c7508f`  
		Last Modified: Sat, 13 Feb 2021 01:50:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe585f4a68228bec2b5b6765c7a8a860d41e59a842e3b43871e7120172ab40c7`  
		Last Modified: Sat, 13 Feb 2021 01:50:06 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1` - linux; 386

```console
$ docker pull spiped@sha256:4f80cd66b8eb83d68da1b3cd894fe37462760fe5278f6973301e26f1af90bc91
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41520139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96e1652c7ef7e3d880320ae65765f36dfe4d599e1ca9ac8c0154dcf0e54633a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 18:39:55 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 13 Feb 2021 00:58:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 13 Feb 2021 00:58:43 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 00:59:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 13 Feb 2021 00:59:17 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 00:59:17 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 00:59:18 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 00:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 00:59:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbea90aac4746d1c996386053d6406bfa4610451eae6d17da249dee74c9b3a68`  
		Last Modified: Tue, 09 Feb 2021 18:40:55 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b87a23d1edb8994421e0ef8e6ae3e7a6364755d7e174130d7b4076dfa2119e`  
		Last Modified: Sat, 13 Feb 2021 01:00:08 GMT  
		Size: 2.1 MB (2132258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7cffa8181e625c430a03c89cc64ae89e03825bd80c01986ce5486ad61b4c12`  
		Last Modified: Sat, 13 Feb 2021 01:00:11 GMT  
		Size: 11.6 MB (11632985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15dfc8a7a89424ce7b74424465fcef8b14d61f39590f94169b3a7afd30130b0`  
		Last Modified: Sat, 13 Feb 2021 01:00:08 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3837cf2d6a87c1b6e64337cafb4ddb0959d201146a766002cc849caa670bae`  
		Last Modified: Sat, 13 Feb 2021 01:00:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1` - linux; mips64le

```console
$ docker pull spiped@sha256:25a5e4c9bfecee13942120bcc34a2cdb13e00addd065a17df1302153ead12de4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33895238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818a59f972b27eb92864d12c7304285f5966446e58096f31ad3b67a0bc8d07d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:51:48 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 12 Feb 2021 23:11:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 12 Feb 2021 23:11:03 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Feb 2021 23:12:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 12 Feb 2021 23:12:11 GMT
VOLUME [/spiped]
# Fri, 12 Feb 2021 23:12:12 GMT
WORKDIR /spiped
# Fri, 12 Feb 2021 23:12:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Feb 2021 23:12:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Feb 2021 23:12:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8e1cbf99b578f9b5da0b78824733a66db880b685f597795dd41a08ac6b4f2f`  
		Last Modified: Tue, 09 Feb 2021 17:53:36 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5463eef3d8ce71368876b45ca24071008cc083ea16ea90ad16da78aee1b06eb0`  
		Last Modified: Fri, 12 Feb 2021 23:12:26 GMT  
		Size: 1.7 MB (1712078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07c83f952ec2caa0e8a9319f93360620700120836fe9678c29036c7cf9868e9`  
		Last Modified: Fri, 12 Feb 2021 23:12:31 GMT  
		Size: 6.4 MB (6416347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b88510861e3f585271a563d2bee51e8dc1659e7abc654317636fd8a6e35956`  
		Last Modified: Fri, 12 Feb 2021 23:12:24 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8a904b2624ec463e93f83225ac51eebd738a0473f323cf0121dcf664488951`  
		Last Modified: Fri, 12 Feb 2021 23:12:25 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1` - linux; ppc64le

```console
$ docker pull spiped@sha256:864f9629da12aace742df3cd8167639ca43ff06a00763b99c31dcba10699a00e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39490261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749c18efc7646905a7417cb2107c88294bb750ed6bc8039f46b4311923b6e779`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:15:19 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 13 Feb 2021 02:30:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 13 Feb 2021 02:30:40 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 02:33:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 13 Feb 2021 02:34:02 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 02:34:09 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 02:34:10 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 02:34:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 02:34:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46b97146405ece3ed453ad4ebc496b4b66b0fff54fdc49d2f4d3175043dffaf`  
		Last Modified: Tue, 09 Feb 2021 04:26:38 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47130d66484e5dc6224d68f7eaf7129048723a038246f1ba3288bc669594ce4d`  
		Last Modified: Sat, 13 Feb 2021 02:36:06 GMT  
		Size: 2.2 MB (2224915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f7be408970c00a6f67d09788fe2ae7d9bee14d0ddedf38e826cbedc4e12d6e`  
		Last Modified: Sat, 13 Feb 2021 02:36:07 GMT  
		Size: 6.7 MB (6743622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed58efc2e2df4e58c29b6b3946f036cdf35e85ba6b21cf906c7fe425b1efc82a`  
		Last Modified: Sat, 13 Feb 2021 02:36:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5da930633055937f1ba62f43cf83b555b527d1cd8255d66ac9d6281f3afa41d`  
		Last Modified: Sat, 13 Feb 2021 02:36:06 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1` - linux; s390x

```console
$ docker pull spiped@sha256:f1fc57dae92710b70032be2526f79e54964e55f92c1743f69ec7cf0a676d8116
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33477416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dda528269da27ad9d1592ca7bc595ecbacc814c873d1441327b98560f8a43b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:33:39 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 13 Feb 2021 03:10:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 13 Feb 2021 03:10:56 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 03:11:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 13 Feb 2021 03:11:22 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 03:11:22 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 03:11:22 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 03:11:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 03:11:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b494d8c5eab48f88712e47a52fa76da28e3b84d610e47c02ef6554cc1e57e98a`  
		Last Modified: Tue, 09 Feb 2021 06:34:18 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916e90eba0ded4a99e0c1e86e0657b977665bf19661f2c18005fc6d6745d7fd4`  
		Last Modified: Sat, 13 Feb 2021 03:12:19 GMT  
		Size: 1.8 MB (1821717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9478c638398830f42321041df73fb7c8005dd7c336c933045b5f043fe1e8786`  
		Last Modified: Sat, 13 Feb 2021 03:12:19 GMT  
		Size: 5.9 MB (5943471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fb1c3cf1445657cf0a44894ccf3da2d62b39264d89fcbecc0e2db075fcfdcf`  
		Last Modified: Sat, 13 Feb 2021 03:12:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f2ae3abab433a32b5e6ba282e6544117d7a01f4fd183d4a7582a4c5a64479f`  
		Last Modified: Sat, 13 Feb 2021 03:12:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.1-alpine`

```console
$ docker pull spiped@sha256:886262c118e20a9aa89de8bbf0a61835f8afe0325ea28dc8184a7d4b7dfd0b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `spiped:1.6.1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:9eee70516db65a980bef1efe2e6e5b88ebbaa4229d8c1273e363b339bb612368
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3032631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8213dd1cadb262ee6e4dbcf4ae7a82ab4498d06d536d91375c781052de00d13f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 07:00:06 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 07:00:07 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 07:00:08 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 07:00:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 07:00:27 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 07:00:27 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 07:00:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 07:00:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 07:00:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69ac6217dde93c3dd112e58c5744c01af3e4d53cf7ed6113c97b16766f1b066`  
		Last Modified: Thu, 18 Feb 2021 07:00:46 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6106fdda164ef63287cb4917bc8bc36d9623619e720820bafceefb5b75f9cc23`  
		Last Modified: Thu, 18 Feb 2021 07:00:46 GMT  
		Size: 7.0 KB (7042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3644c0e57965933d3ecd22e174cf93d6b997ea76d59fcb9f87680683a7373a7`  
		Last Modified: Thu, 18 Feb 2021 07:00:46 GMT  
		Size: 212.3 KB (212265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369eba833b7db361a3110d17bbb4cdb4ba5cf9a9d719f3324c9bd78787799bc2`  
		Last Modified: Thu, 18 Feb 2021 07:00:46 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e6a2868335e22dc53d8da4bcfc867f019d34380a35d856ee1aae318c7f3b5e`  
		Last Modified: Thu, 18 Feb 2021 07:00:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:a4eae04b6b59fa1465464612d582ab381eae7d0fd508089e99a2d9642d83d589
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2833085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa0d64ae65bd0aed1fae629f2219ead07f2df4d55520aa67fa73701725be6a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:08:57 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 01:09:00 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 01:09:00 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 01:09:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 01:09:29 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 01:09:30 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 01:09:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 01:09:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 01:09:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56478beef0e3bf335b5084e01725a07c247a0df1c2ae4d79a9b37d8d7c1d8c6b`  
		Last Modified: Thu, 18 Feb 2021 01:09:52 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09965b504ec1fcd372f0f74e2de05a28c8cfc7546e5f9abac13b9969308fffc7`  
		Last Modified: Thu, 18 Feb 2021 01:09:52 GMT  
		Size: 7.1 KB (7053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca4d95213096352ef307626e2b9b743cd56d9e041d9bad475b082bdda7cd8fb`  
		Last Modified: Thu, 18 Feb 2021 01:09:52 GMT  
		Size: 202.3 KB (202264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448a184417c9c40109716c2bf6eb26c63873720e7d14b4e852ffe5da738e4871`  
		Last Modified: Thu, 18 Feb 2021 01:09:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb506bcaf6432a313382d4600f3ae27df33c73cfc17f1d9615fee63b17b95c3`  
		Last Modified: Thu, 18 Feb 2021 01:09:51 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e91e8dfd1379e2029d929ab8d21b5b7cacda7a1ac496cecd8c37417d9d48e708
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8d028bc188683c4af6ec6c0afa9cf33c5e88a0569d98c54eebd1e02b4b78b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:11:51 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 01:11:53 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 01:11:55 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 01:12:23 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 01:12:24 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 01:12:25 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 01:12:26 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 01:12:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 01:12:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdfb8a36c4de90dba3240099eb1d0348f8627ed1bc968f7e4271d75b265ccf2`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ab61a202577acd7159b1a345fcb97d20c63e42a6a170dfe22345caa4af688f`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374409fe6217df96932998b712912ebad072a21d4d4e7817b70b6dbb23d0f0a3`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 195.5 KB (195539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592de5c2b9cc50ddf43d871cb052d160ae2dc235c136a1731e45e1cf529b7b80`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562929d72557b487b48b0dcc0ca66188d993a95431efb6ba6e82ecece7035616`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b0ca7cbad488b0fcb44506f1c6c65ae77f5573dc072c30c390b75e29a9d2c64c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2924800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffde3212b34beb453841e58f5ca6bcdbd5dee1c658ff1861926718f1f9c5499`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:23:27 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 01:23:30 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 01:23:31 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 01:24:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 01:24:05 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 01:24:06 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 01:24:07 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 01:24:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 01:24:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991947bc8299281c0212c4f9312423d52074ad210f1eab639db0f6df247937b2`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a8e0ee83f949ca3f11000f9df3c4b551cff205fc9d645ed6aa3c13d4b41a14`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 7.1 KB (7059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da8757762737713d5ff919736307c7a18ea61e4e68e7a6f051974461de14f8a`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 204.4 KB (204440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a12b508a6a8ce19fd3eee0367c035a60aebd09e422b169e7e3acb5ec2cc376`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd46a081f7acce468799a1512f765f8f304e396d48824de8d10a33c1e6416619`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:3d16165c8f992a38d2df40c20281086c5f5655653cf50dda22de666ef2dfcf30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3050132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea168ec2a7774bd98f1283bf24bdc8f202dfd0c1071519cee94ad2c4082e6516`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 03:56:04 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 03:56:05 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 03:56:05 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 03:56:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 03:56:26 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 03:56:26 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 03:56:26 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 03:56:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 03:56:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9e21e3816b5b789fd74f3cb743abbf67d3298c24befb2247ce9a2e9f6dc4ee`  
		Last Modified: Thu, 18 Feb 2021 03:56:43 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e3731978edf44edb0ea58d3a380f30a1402d3049d91b8cc65c057dc80e4c25`  
		Last Modified: Thu, 18 Feb 2021 03:56:43 GMT  
		Size: 7.0 KB (7039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb54a0fa65c0be0bc6620ead1c5ce4a48c5d1e7774c58b1b703f44e51e2cd42`  
		Last Modified: Thu, 18 Feb 2021 03:56:43 GMT  
		Size: 223.3 KB (223251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123864fcdf8cb6f3b2a564539d7190ca8b2d9d1984376b571607cae2f897c7d6`  
		Last Modified: Thu, 18 Feb 2021 03:56:43 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd413ae59a6361f5ea3ce2d327d2b023222758d67f597a866a84fd8216d6fc66`  
		Last Modified: Thu, 18 Feb 2021 03:56:43 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:c289f487ff74d19e50727c07507d1609f142b15a496f3e829a8232e797f8fa86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3042847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5452ec7d0568f7fa053d286ed0069f9ddd4be9dde9b516049498ade4047aa340`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 03:26:01 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 03:26:27 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 03:26:34 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 03:27:18 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 03:27:34 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 03:27:46 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 03:27:51 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 03:28:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 03:28:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60920645f2e5501fee7aa26e0c7d56e1e6b86944323cc7d2bc446665f8f00296`  
		Last Modified: Thu, 18 Feb 2021 03:28:43 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99be5791d197e7173e97bcde4c0cb34e0b0b041b0cfd0dd2e52ee1aeac336327`  
		Last Modified: Thu, 18 Feb 2021 03:28:43 GMT  
		Size: 7.1 KB (7058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b707542d6d894ec7ee45192bff36b0d35538f59e7f201a07e84ba7b2b3d9a216`  
		Last Modified: Thu, 18 Feb 2021 03:28:43 GMT  
		Size: 221.0 KB (220976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646679d9c65db513723f9e3d9b1e14a6ff198910adb40d95218a19fd2075e12c`  
		Last Modified: Thu, 18 Feb 2021 03:28:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d625be0be9dedbd5e83f126a8a7cce9eb5ca9932ee03459ebb286fbaca7fa39f`  
		Last Modified: Thu, 18 Feb 2021 03:28:43 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:84eb47cc2762f89ced7dac3994d19fd866beb6d7edf1ce8ab89075b9e965894d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2816196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931664821077383b17442b73db19b44e519072a6c656d5d071fb35e73856df97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:38:50 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 00:38:52 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 00:38:53 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 00:39:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 00:39:08 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 00:39:08 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 00:39:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 00:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 00:39:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e67382afc352947106dc6c166d812d215925da3b965c062a036336a3b0aa2eb`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c645ec8297a3a8a63091e1f2c1a83b18b9649d25e3a0c009ce595fa0f9ab2d01`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 7.0 KB (7048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7ec4619ba6c3e05a4793024f6fc431995072c29d096c87ef92b93acf2fe0ff`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 205.0 KB (205040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c09c00004fe0ea62d74d7d3cd3c7252e1586cb457fbd2d87147cc88c27d799`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8302a33625b439acc9b2f489b57ea79b1d58f06bf3ae086534f499d28e4f951`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:886262c118e20a9aa89de8bbf0a61835f8afe0325ea28dc8184a7d4b7dfd0b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `spiped:1.6-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:9eee70516db65a980bef1efe2e6e5b88ebbaa4229d8c1273e363b339bb612368
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3032631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8213dd1cadb262ee6e4dbcf4ae7a82ab4498d06d536d91375c781052de00d13f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 07:00:06 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 07:00:07 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 07:00:08 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 07:00:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 07:00:27 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 07:00:27 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 07:00:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 07:00:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 07:00:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69ac6217dde93c3dd112e58c5744c01af3e4d53cf7ed6113c97b16766f1b066`  
		Last Modified: Thu, 18 Feb 2021 07:00:46 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6106fdda164ef63287cb4917bc8bc36d9623619e720820bafceefb5b75f9cc23`  
		Last Modified: Thu, 18 Feb 2021 07:00:46 GMT  
		Size: 7.0 KB (7042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3644c0e57965933d3ecd22e174cf93d6b997ea76d59fcb9f87680683a7373a7`  
		Last Modified: Thu, 18 Feb 2021 07:00:46 GMT  
		Size: 212.3 KB (212265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369eba833b7db361a3110d17bbb4cdb4ba5cf9a9d719f3324c9bd78787799bc2`  
		Last Modified: Thu, 18 Feb 2021 07:00:46 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e6a2868335e22dc53d8da4bcfc867f019d34380a35d856ee1aae318c7f3b5e`  
		Last Modified: Thu, 18 Feb 2021 07:00:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:a4eae04b6b59fa1465464612d582ab381eae7d0fd508089e99a2d9642d83d589
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2833085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa0d64ae65bd0aed1fae629f2219ead07f2df4d55520aa67fa73701725be6a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:08:57 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 01:09:00 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 01:09:00 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 01:09:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 01:09:29 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 01:09:30 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 01:09:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 01:09:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 01:09:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56478beef0e3bf335b5084e01725a07c247a0df1c2ae4d79a9b37d8d7c1d8c6b`  
		Last Modified: Thu, 18 Feb 2021 01:09:52 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09965b504ec1fcd372f0f74e2de05a28c8cfc7546e5f9abac13b9969308fffc7`  
		Last Modified: Thu, 18 Feb 2021 01:09:52 GMT  
		Size: 7.1 KB (7053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca4d95213096352ef307626e2b9b743cd56d9e041d9bad475b082bdda7cd8fb`  
		Last Modified: Thu, 18 Feb 2021 01:09:52 GMT  
		Size: 202.3 KB (202264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448a184417c9c40109716c2bf6eb26c63873720e7d14b4e852ffe5da738e4871`  
		Last Modified: Thu, 18 Feb 2021 01:09:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb506bcaf6432a313382d4600f3ae27df33c73cfc17f1d9615fee63b17b95c3`  
		Last Modified: Thu, 18 Feb 2021 01:09:51 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e91e8dfd1379e2029d929ab8d21b5b7cacda7a1ac496cecd8c37417d9d48e708
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8d028bc188683c4af6ec6c0afa9cf33c5e88a0569d98c54eebd1e02b4b78b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:11:51 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 01:11:53 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 01:11:55 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 01:12:23 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 01:12:24 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 01:12:25 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 01:12:26 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 01:12:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 01:12:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdfb8a36c4de90dba3240099eb1d0348f8627ed1bc968f7e4271d75b265ccf2`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ab61a202577acd7159b1a345fcb97d20c63e42a6a170dfe22345caa4af688f`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374409fe6217df96932998b712912ebad072a21d4d4e7817b70b6dbb23d0f0a3`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 195.5 KB (195539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592de5c2b9cc50ddf43d871cb052d160ae2dc235c136a1731e45e1cf529b7b80`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562929d72557b487b48b0dcc0ca66188d993a95431efb6ba6e82ecece7035616`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b0ca7cbad488b0fcb44506f1c6c65ae77f5573dc072c30c390b75e29a9d2c64c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2924800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffde3212b34beb453841e58f5ca6bcdbd5dee1c658ff1861926718f1f9c5499`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:23:27 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 01:23:30 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 01:23:31 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 01:24:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 01:24:05 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 01:24:06 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 01:24:07 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 01:24:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 01:24:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991947bc8299281c0212c4f9312423d52074ad210f1eab639db0f6df247937b2`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a8e0ee83f949ca3f11000f9df3c4b551cff205fc9d645ed6aa3c13d4b41a14`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 7.1 KB (7059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da8757762737713d5ff919736307c7a18ea61e4e68e7a6f051974461de14f8a`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 204.4 KB (204440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a12b508a6a8ce19fd3eee0367c035a60aebd09e422b169e7e3acb5ec2cc376`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd46a081f7acce468799a1512f765f8f304e396d48824de8d10a33c1e6416619`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:3d16165c8f992a38d2df40c20281086c5f5655653cf50dda22de666ef2dfcf30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3050132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea168ec2a7774bd98f1283bf24bdc8f202dfd0c1071519cee94ad2c4082e6516`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 03:56:04 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 03:56:05 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 03:56:05 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 03:56:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 03:56:26 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 03:56:26 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 03:56:26 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 03:56:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 03:56:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9e21e3816b5b789fd74f3cb743abbf67d3298c24befb2247ce9a2e9f6dc4ee`  
		Last Modified: Thu, 18 Feb 2021 03:56:43 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e3731978edf44edb0ea58d3a380f30a1402d3049d91b8cc65c057dc80e4c25`  
		Last Modified: Thu, 18 Feb 2021 03:56:43 GMT  
		Size: 7.0 KB (7039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb54a0fa65c0be0bc6620ead1c5ce4a48c5d1e7774c58b1b703f44e51e2cd42`  
		Last Modified: Thu, 18 Feb 2021 03:56:43 GMT  
		Size: 223.3 KB (223251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123864fcdf8cb6f3b2a564539d7190ca8b2d9d1984376b571607cae2f897c7d6`  
		Last Modified: Thu, 18 Feb 2021 03:56:43 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd413ae59a6361f5ea3ce2d327d2b023222758d67f597a866a84fd8216d6fc66`  
		Last Modified: Thu, 18 Feb 2021 03:56:43 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:c289f487ff74d19e50727c07507d1609f142b15a496f3e829a8232e797f8fa86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3042847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5452ec7d0568f7fa053d286ed0069f9ddd4be9dde9b516049498ade4047aa340`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 03:26:01 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 03:26:27 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 03:26:34 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 03:27:18 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 03:27:34 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 03:27:46 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 03:27:51 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 03:28:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 03:28:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60920645f2e5501fee7aa26e0c7d56e1e6b86944323cc7d2bc446665f8f00296`  
		Last Modified: Thu, 18 Feb 2021 03:28:43 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99be5791d197e7173e97bcde4c0cb34e0b0b041b0cfd0dd2e52ee1aeac336327`  
		Last Modified: Thu, 18 Feb 2021 03:28:43 GMT  
		Size: 7.1 KB (7058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b707542d6d894ec7ee45192bff36b0d35538f59e7f201a07e84ba7b2b3d9a216`  
		Last Modified: Thu, 18 Feb 2021 03:28:43 GMT  
		Size: 221.0 KB (220976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646679d9c65db513723f9e3d9b1e14a6ff198910adb40d95218a19fd2075e12c`  
		Last Modified: Thu, 18 Feb 2021 03:28:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d625be0be9dedbd5e83f126a8a7cce9eb5ca9932ee03459ebb286fbaca7fa39f`  
		Last Modified: Thu, 18 Feb 2021 03:28:43 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:84eb47cc2762f89ced7dac3994d19fd866beb6d7edf1ce8ab89075b9e965894d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2816196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931664821077383b17442b73db19b44e519072a6c656d5d071fb35e73856df97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:38:50 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 00:38:52 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 00:38:53 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 00:39:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 00:39:08 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 00:39:08 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 00:39:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 00:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 00:39:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e67382afc352947106dc6c166d812d215925da3b965c062a036336a3b0aa2eb`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c645ec8297a3a8a63091e1f2c1a83b18b9649d25e3a0c009ce595fa0f9ab2d01`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 7.0 KB (7048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7ec4619ba6c3e05a4793024f6fc431995072c29d096c87ef92b93acf2fe0ff`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 205.0 KB (205040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c09c00004fe0ea62d74d7d3cd3c7252e1586cb457fbd2d87147cc88c27d799`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8302a33625b439acc9b2f489b57ea79b1d58f06bf3ae086534f499d28e4f951`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:886262c118e20a9aa89de8bbf0a61835f8afe0325ea28dc8184a7d4b7dfd0b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `spiped:1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:9eee70516db65a980bef1efe2e6e5b88ebbaa4229d8c1273e363b339bb612368
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3032631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8213dd1cadb262ee6e4dbcf4ae7a82ab4498d06d536d91375c781052de00d13f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 07:00:06 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 07:00:07 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 07:00:08 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 07:00:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 07:00:27 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 07:00:27 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 07:00:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 07:00:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 07:00:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69ac6217dde93c3dd112e58c5744c01af3e4d53cf7ed6113c97b16766f1b066`  
		Last Modified: Thu, 18 Feb 2021 07:00:46 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6106fdda164ef63287cb4917bc8bc36d9623619e720820bafceefb5b75f9cc23`  
		Last Modified: Thu, 18 Feb 2021 07:00:46 GMT  
		Size: 7.0 KB (7042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3644c0e57965933d3ecd22e174cf93d6b997ea76d59fcb9f87680683a7373a7`  
		Last Modified: Thu, 18 Feb 2021 07:00:46 GMT  
		Size: 212.3 KB (212265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369eba833b7db361a3110d17bbb4cdb4ba5cf9a9d719f3324c9bd78787799bc2`  
		Last Modified: Thu, 18 Feb 2021 07:00:46 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e6a2868335e22dc53d8da4bcfc867f019d34380a35d856ee1aae318c7f3b5e`  
		Last Modified: Thu, 18 Feb 2021 07:00:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:a4eae04b6b59fa1465464612d582ab381eae7d0fd508089e99a2d9642d83d589
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2833085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa0d64ae65bd0aed1fae629f2219ead07f2df4d55520aa67fa73701725be6a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:08:57 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 01:09:00 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 01:09:00 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 01:09:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 01:09:29 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 01:09:30 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 01:09:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 01:09:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 01:09:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56478beef0e3bf335b5084e01725a07c247a0df1c2ae4d79a9b37d8d7c1d8c6b`  
		Last Modified: Thu, 18 Feb 2021 01:09:52 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09965b504ec1fcd372f0f74e2de05a28c8cfc7546e5f9abac13b9969308fffc7`  
		Last Modified: Thu, 18 Feb 2021 01:09:52 GMT  
		Size: 7.1 KB (7053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca4d95213096352ef307626e2b9b743cd56d9e041d9bad475b082bdda7cd8fb`  
		Last Modified: Thu, 18 Feb 2021 01:09:52 GMT  
		Size: 202.3 KB (202264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448a184417c9c40109716c2bf6eb26c63873720e7d14b4e852ffe5da738e4871`  
		Last Modified: Thu, 18 Feb 2021 01:09:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb506bcaf6432a313382d4600f3ae27df33c73cfc17f1d9615fee63b17b95c3`  
		Last Modified: Thu, 18 Feb 2021 01:09:51 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e91e8dfd1379e2029d929ab8d21b5b7cacda7a1ac496cecd8c37417d9d48e708
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8d028bc188683c4af6ec6c0afa9cf33c5e88a0569d98c54eebd1e02b4b78b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:11:51 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 01:11:53 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 01:11:55 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 01:12:23 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 01:12:24 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 01:12:25 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 01:12:26 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 01:12:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 01:12:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdfb8a36c4de90dba3240099eb1d0348f8627ed1bc968f7e4271d75b265ccf2`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ab61a202577acd7159b1a345fcb97d20c63e42a6a170dfe22345caa4af688f`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374409fe6217df96932998b712912ebad072a21d4d4e7817b70b6dbb23d0f0a3`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 195.5 KB (195539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592de5c2b9cc50ddf43d871cb052d160ae2dc235c136a1731e45e1cf529b7b80`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562929d72557b487b48b0dcc0ca66188d993a95431efb6ba6e82ecece7035616`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b0ca7cbad488b0fcb44506f1c6c65ae77f5573dc072c30c390b75e29a9d2c64c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2924800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffde3212b34beb453841e58f5ca6bcdbd5dee1c658ff1861926718f1f9c5499`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:23:27 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 01:23:30 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 01:23:31 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 01:24:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 01:24:05 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 01:24:06 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 01:24:07 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 01:24:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 01:24:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991947bc8299281c0212c4f9312423d52074ad210f1eab639db0f6df247937b2`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a8e0ee83f949ca3f11000f9df3c4b551cff205fc9d645ed6aa3c13d4b41a14`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 7.1 KB (7059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da8757762737713d5ff919736307c7a18ea61e4e68e7a6f051974461de14f8a`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 204.4 KB (204440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a12b508a6a8ce19fd3eee0367c035a60aebd09e422b169e7e3acb5ec2cc376`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd46a081f7acce468799a1512f765f8f304e396d48824de8d10a33c1e6416619`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:3d16165c8f992a38d2df40c20281086c5f5655653cf50dda22de666ef2dfcf30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3050132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea168ec2a7774bd98f1283bf24bdc8f202dfd0c1071519cee94ad2c4082e6516`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 03:56:04 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 03:56:05 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 03:56:05 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 03:56:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 03:56:26 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 03:56:26 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 03:56:26 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 03:56:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 03:56:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9e21e3816b5b789fd74f3cb743abbf67d3298c24befb2247ce9a2e9f6dc4ee`  
		Last Modified: Thu, 18 Feb 2021 03:56:43 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e3731978edf44edb0ea58d3a380f30a1402d3049d91b8cc65c057dc80e4c25`  
		Last Modified: Thu, 18 Feb 2021 03:56:43 GMT  
		Size: 7.0 KB (7039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb54a0fa65c0be0bc6620ead1c5ce4a48c5d1e7774c58b1b703f44e51e2cd42`  
		Last Modified: Thu, 18 Feb 2021 03:56:43 GMT  
		Size: 223.3 KB (223251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123864fcdf8cb6f3b2a564539d7190ca8b2d9d1984376b571607cae2f897c7d6`  
		Last Modified: Thu, 18 Feb 2021 03:56:43 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd413ae59a6361f5ea3ce2d327d2b023222758d67f597a866a84fd8216d6fc66`  
		Last Modified: Thu, 18 Feb 2021 03:56:43 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:c289f487ff74d19e50727c07507d1609f142b15a496f3e829a8232e797f8fa86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3042847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5452ec7d0568f7fa053d286ed0069f9ddd4be9dde9b516049498ade4047aa340`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 03:26:01 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 03:26:27 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 03:26:34 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 03:27:18 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 03:27:34 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 03:27:46 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 03:27:51 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 03:28:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 03:28:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60920645f2e5501fee7aa26e0c7d56e1e6b86944323cc7d2bc446665f8f00296`  
		Last Modified: Thu, 18 Feb 2021 03:28:43 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99be5791d197e7173e97bcde4c0cb34e0b0b041b0cfd0dd2e52ee1aeac336327`  
		Last Modified: Thu, 18 Feb 2021 03:28:43 GMT  
		Size: 7.1 KB (7058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b707542d6d894ec7ee45192bff36b0d35538f59e7f201a07e84ba7b2b3d9a216`  
		Last Modified: Thu, 18 Feb 2021 03:28:43 GMT  
		Size: 221.0 KB (220976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646679d9c65db513723f9e3d9b1e14a6ff198910adb40d95218a19fd2075e12c`  
		Last Modified: Thu, 18 Feb 2021 03:28:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d625be0be9dedbd5e83f126a8a7cce9eb5ca9932ee03459ebb286fbaca7fa39f`  
		Last Modified: Thu, 18 Feb 2021 03:28:43 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:84eb47cc2762f89ced7dac3994d19fd866beb6d7edf1ce8ab89075b9e965894d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2816196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931664821077383b17442b73db19b44e519072a6c656d5d071fb35e73856df97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:38:50 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 00:38:52 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 00:38:53 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 00:39:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 00:39:08 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 00:39:08 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 00:39:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 00:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 00:39:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e67382afc352947106dc6c166d812d215925da3b965c062a036336a3b0aa2eb`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c645ec8297a3a8a63091e1f2c1a83b18b9649d25e3a0c009ce595fa0f9ab2d01`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 7.0 KB (7048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7ec4619ba6c3e05a4793024f6fc431995072c29d096c87ef92b93acf2fe0ff`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 205.0 KB (205040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c09c00004fe0ea62d74d7d3cd3c7252e1586cb457fbd2d87147cc88c27d799`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8302a33625b439acc9b2f489b57ea79b1d58f06bf3ae086534f499d28e4f951`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:alpine`

```console
$ docker pull spiped@sha256:886262c118e20a9aa89de8bbf0a61835f8afe0325ea28dc8184a7d4b7dfd0b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `spiped:alpine` - linux; amd64

```console
$ docker pull spiped@sha256:9eee70516db65a980bef1efe2e6e5b88ebbaa4229d8c1273e363b339bb612368
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3032631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8213dd1cadb262ee6e4dbcf4ae7a82ab4498d06d536d91375c781052de00d13f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 07:00:06 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 07:00:07 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 07:00:08 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 07:00:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 07:00:27 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 07:00:27 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 07:00:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 07:00:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 07:00:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69ac6217dde93c3dd112e58c5744c01af3e4d53cf7ed6113c97b16766f1b066`  
		Last Modified: Thu, 18 Feb 2021 07:00:46 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6106fdda164ef63287cb4917bc8bc36d9623619e720820bafceefb5b75f9cc23`  
		Last Modified: Thu, 18 Feb 2021 07:00:46 GMT  
		Size: 7.0 KB (7042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3644c0e57965933d3ecd22e174cf93d6b997ea76d59fcb9f87680683a7373a7`  
		Last Modified: Thu, 18 Feb 2021 07:00:46 GMT  
		Size: 212.3 KB (212265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369eba833b7db361a3110d17bbb4cdb4ba5cf9a9d719f3324c9bd78787799bc2`  
		Last Modified: Thu, 18 Feb 2021 07:00:46 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e6a2868335e22dc53d8da4bcfc867f019d34380a35d856ee1aae318c7f3b5e`  
		Last Modified: Thu, 18 Feb 2021 07:00:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:a4eae04b6b59fa1465464612d582ab381eae7d0fd508089e99a2d9642d83d589
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2833085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa0d64ae65bd0aed1fae629f2219ead07f2df4d55520aa67fa73701725be6a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:08:57 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 01:09:00 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 01:09:00 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 01:09:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 01:09:29 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 01:09:30 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 01:09:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 01:09:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 01:09:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56478beef0e3bf335b5084e01725a07c247a0df1c2ae4d79a9b37d8d7c1d8c6b`  
		Last Modified: Thu, 18 Feb 2021 01:09:52 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09965b504ec1fcd372f0f74e2de05a28c8cfc7546e5f9abac13b9969308fffc7`  
		Last Modified: Thu, 18 Feb 2021 01:09:52 GMT  
		Size: 7.1 KB (7053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca4d95213096352ef307626e2b9b743cd56d9e041d9bad475b082bdda7cd8fb`  
		Last Modified: Thu, 18 Feb 2021 01:09:52 GMT  
		Size: 202.3 KB (202264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448a184417c9c40109716c2bf6eb26c63873720e7d14b4e852ffe5da738e4871`  
		Last Modified: Thu, 18 Feb 2021 01:09:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb506bcaf6432a313382d4600f3ae27df33c73cfc17f1d9615fee63b17b95c3`  
		Last Modified: Thu, 18 Feb 2021 01:09:51 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e91e8dfd1379e2029d929ab8d21b5b7cacda7a1ac496cecd8c37417d9d48e708
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8d028bc188683c4af6ec6c0afa9cf33c5e88a0569d98c54eebd1e02b4b78b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:11:51 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 01:11:53 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 01:11:55 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 01:12:23 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 01:12:24 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 01:12:25 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 01:12:26 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 01:12:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 01:12:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdfb8a36c4de90dba3240099eb1d0348f8627ed1bc968f7e4271d75b265ccf2`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ab61a202577acd7159b1a345fcb97d20c63e42a6a170dfe22345caa4af688f`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374409fe6217df96932998b712912ebad072a21d4d4e7817b70b6dbb23d0f0a3`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 195.5 KB (195539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592de5c2b9cc50ddf43d871cb052d160ae2dc235c136a1731e45e1cf529b7b80`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562929d72557b487b48b0dcc0ca66188d993a95431efb6ba6e82ecece7035616`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b0ca7cbad488b0fcb44506f1c6c65ae77f5573dc072c30c390b75e29a9d2c64c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2924800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffde3212b34beb453841e58f5ca6bcdbd5dee1c658ff1861926718f1f9c5499`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:23:27 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 01:23:30 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 01:23:31 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 01:24:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 01:24:05 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 01:24:06 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 01:24:07 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 01:24:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 01:24:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991947bc8299281c0212c4f9312423d52074ad210f1eab639db0f6df247937b2`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a8e0ee83f949ca3f11000f9df3c4b551cff205fc9d645ed6aa3c13d4b41a14`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 7.1 KB (7059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da8757762737713d5ff919736307c7a18ea61e4e68e7a6f051974461de14f8a`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 204.4 KB (204440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a12b508a6a8ce19fd3eee0367c035a60aebd09e422b169e7e3acb5ec2cc376`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd46a081f7acce468799a1512f765f8f304e396d48824de8d10a33c1e6416619`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:3d16165c8f992a38d2df40c20281086c5f5655653cf50dda22de666ef2dfcf30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3050132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea168ec2a7774bd98f1283bf24bdc8f202dfd0c1071519cee94ad2c4082e6516`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 03:56:04 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 03:56:05 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 03:56:05 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 03:56:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 03:56:26 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 03:56:26 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 03:56:26 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 03:56:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 03:56:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9e21e3816b5b789fd74f3cb743abbf67d3298c24befb2247ce9a2e9f6dc4ee`  
		Last Modified: Thu, 18 Feb 2021 03:56:43 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e3731978edf44edb0ea58d3a380f30a1402d3049d91b8cc65c057dc80e4c25`  
		Last Modified: Thu, 18 Feb 2021 03:56:43 GMT  
		Size: 7.0 KB (7039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb54a0fa65c0be0bc6620ead1c5ce4a48c5d1e7774c58b1b703f44e51e2cd42`  
		Last Modified: Thu, 18 Feb 2021 03:56:43 GMT  
		Size: 223.3 KB (223251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123864fcdf8cb6f3b2a564539d7190ca8b2d9d1984376b571607cae2f897c7d6`  
		Last Modified: Thu, 18 Feb 2021 03:56:43 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd413ae59a6361f5ea3ce2d327d2b023222758d67f597a866a84fd8216d6fc66`  
		Last Modified: Thu, 18 Feb 2021 03:56:43 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:c289f487ff74d19e50727c07507d1609f142b15a496f3e829a8232e797f8fa86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3042847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5452ec7d0568f7fa053d286ed0069f9ddd4be9dde9b516049498ade4047aa340`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 03:26:01 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 03:26:27 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 03:26:34 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 03:27:18 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 03:27:34 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 03:27:46 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 03:27:51 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 03:28:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 03:28:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60920645f2e5501fee7aa26e0c7d56e1e6b86944323cc7d2bc446665f8f00296`  
		Last Modified: Thu, 18 Feb 2021 03:28:43 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99be5791d197e7173e97bcde4c0cb34e0b0b041b0cfd0dd2e52ee1aeac336327`  
		Last Modified: Thu, 18 Feb 2021 03:28:43 GMT  
		Size: 7.1 KB (7058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b707542d6d894ec7ee45192bff36b0d35538f59e7f201a07e84ba7b2b3d9a216`  
		Last Modified: Thu, 18 Feb 2021 03:28:43 GMT  
		Size: 221.0 KB (220976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646679d9c65db513723f9e3d9b1e14a6ff198910adb40d95218a19fd2075e12c`  
		Last Modified: Thu, 18 Feb 2021 03:28:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d625be0be9dedbd5e83f126a8a7cce9eb5ca9932ee03459ebb286fbaca7fa39f`  
		Last Modified: Thu, 18 Feb 2021 03:28:43 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:84eb47cc2762f89ced7dac3994d19fd866beb6d7edf1ce8ab89075b9e965894d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2816196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931664821077383b17442b73db19b44e519072a6c656d5d071fb35e73856df97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:38:50 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 00:38:52 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 00:38:53 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 00:39:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 00:39:08 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 00:39:08 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 00:39:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 00:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 00:39:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e67382afc352947106dc6c166d812d215925da3b965c062a036336a3b0aa2eb`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c645ec8297a3a8a63091e1f2c1a83b18b9649d25e3a0c009ce595fa0f9ab2d01`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 7.0 KB (7048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7ec4619ba6c3e05a4793024f6fc431995072c29d096c87ef92b93acf2fe0ff`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 205.0 KB (205040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c09c00004fe0ea62d74d7d3cd3c7252e1586cb457fbd2d87147cc88c27d799`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8302a33625b439acc9b2f489b57ea79b1d58f06bf3ae086534f499d28e4f951`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:latest`

```console
$ docker pull spiped@sha256:4e0757d83a01c2abc624d004ea3feb13bbd81c33ff0294e91744575688e0e92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `spiped:latest` - linux; amd64

```console
$ docker pull spiped@sha256:de2d45b0f59312e4abff77a82b78eaac004c3224734eedbc7334680c7ec5443f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36262768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897fcb40d5e49b8a35aa9e61c14eff1f62c615775ab19bff009fbbeafff2b106`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 11:21:37 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 13 Feb 2021 00:09:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 13 Feb 2021 00:09:09 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 00:09:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 13 Feb 2021 00:09:59 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 00:10:00 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 00:10:01 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 00:10:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 00:10:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de752b69da20dffa4f368194c801b91db7f8109eb73f00e28fcf2534595c2391`  
		Last Modified: Tue, 09 Feb 2021 11:22:39 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d13c52f8d2f79744057e6229950b1dfc5bd6291a85638e41c94d0bf6ae4e29`  
		Last Modified: Sat, 13 Feb 2021 00:11:29 GMT  
		Size: 2.1 MB (2128155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce83854aeaf080766f7945048114fa3e9b3416b345ca8aff96978c9c7f54953`  
		Last Modified: Sat, 13 Feb 2021 00:11:31 GMT  
		Size: 7.0 MB (7037301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb829d6ea4836c4cb76df6e6b6006024c209af26a1c18390c00a81ae68243bb`  
		Last Modified: Sat, 13 Feb 2021 00:11:28 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98a7fedb7f92d778864b0fcf2422f4ef009b2ab40c930b69020c825e6dec72c`  
		Last Modified: Sat, 13 Feb 2021 00:11:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:5fdf9146d8023cd6e901dbceff493b9883020acd456eb8bfbd5c480fcd681210
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32160479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1781b7c6ba805844ffb5302f90107b4f5d7cc5f1fd80060ce54ea64fbad5616c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 11:43:19 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 12 Feb 2021 22:52:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 12 Feb 2021 22:52:10 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Feb 2021 22:53:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 12 Feb 2021 22:53:05 GMT
VOLUME [/spiped]
# Fri, 12 Feb 2021 22:53:06 GMT
WORKDIR /spiped
# Fri, 12 Feb 2021 22:53:07 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Feb 2021 22:53:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Feb 2021 22:53:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346f1f77623bfcedac114c95542f4a432dbfac2903c21d7af096733db6f08d7a`  
		Last Modified: Tue, 09 Feb 2021 11:44:58 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b20e94947775259ce6bf04cfa19152b029d3365a89d4ccc0843ae79aa8bd4f2`  
		Last Modified: Fri, 12 Feb 2021 22:53:24 GMT  
		Size: 1.8 MB (1839109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5daf79a4e2ff35a482480dc5ed9294bc9b4a8973856555b77b39e3db207b7e`  
		Last Modified: Fri, 12 Feb 2021 22:53:26 GMT  
		Size: 5.5 MB (5479875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384e633e1a26bfac8686c377988482dd352c68b9f02ba80edcda2501879211a1`  
		Last Modified: Fri, 12 Feb 2021 22:53:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e3d0ff8a742e94655d7e9b5e7444b78818640156c0ca4672cfa957a605307f`  
		Last Modified: Fri, 12 Feb 2021 22:53:23 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:3f1874e1134dbfca6d910ae69ff8d37e2a72d12404d8a9fd0fe0bd0c91e6db78
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29750488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c287c25628c3da85c966ccc96d6e3e6e7a542d2487caaa805d5fa8a0525ea5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 19:35:37 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 12 Feb 2021 22:38:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 12 Feb 2021 22:38:45 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Feb 2021 22:39:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 12 Feb 2021 22:39:30 GMT
VOLUME [/spiped]
# Fri, 12 Feb 2021 22:39:30 GMT
WORKDIR /spiped
# Fri, 12 Feb 2021 22:39:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Feb 2021 22:39:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Feb 2021 22:39:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5afe0266f6b6542f91658ca8ec8b87ac3e40c9e40d88f3ebfb311da27ffaa976`  
		Last Modified: Tue, 09 Feb 2021 19:37:10 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a439028cc7f7cbb2502897e215fe8142424bac7b8461519a3721306ca16262`  
		Last Modified: Fri, 12 Feb 2021 22:40:38 GMT  
		Size: 1.8 MB (1759313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e175e160ff82eee0dc76239d6e920ad6fce1b07298b3bd90e8120c021b7af0dd`  
		Last Modified: Fri, 12 Feb 2021 22:40:40 GMT  
		Size: 5.3 MB (5285596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4c31222b7eba85c87a5dbbee1012985dae7f842a0c60e03cc2641b409aa474`  
		Last Modified: Fri, 12 Feb 2021 22:40:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88900a0b87f635433ee9e3c471b1a10b21ea199374733be54fb2595691999e2`  
		Last Modified: Fri, 12 Feb 2021 22:40:38 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:aeb7d15ee44fc1b03bfd46be858735700424119244cb66f38e14e9630c63e7ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33766524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e1f2dc0e564ffcc34b5a7d98c4213648ab3f8a22f84e0db2b43178567f3a12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 18:18:32 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 13 Feb 2021 01:48:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 13 Feb 2021 01:48:09 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 01:48:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 13 Feb 2021 01:48:57 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 01:48:58 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 01:48:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 01:49:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 01:49:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516c8ae6b6958174393d642fd4693aea0a041e432ce8d8758b052224d96cb2fa`  
		Last Modified: Tue, 09 Feb 2021 18:20:06 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03005b703ccb19a3569b35a5b9bf1bfef156941eaf489b91ff81efde2e7ea584`  
		Last Modified: Sat, 13 Feb 2021 01:50:07 GMT  
		Size: 2.0 MB (2007571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c581bbabc2c122ca024c49c3aa7d735e4cfba75a1560c8c873223c66d0c57e6a`  
		Last Modified: Sat, 13 Feb 2021 01:50:08 GMT  
		Size: 5.9 MB (5905293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c709ad2716ce7723cf89c0c553985816902e98c25f46520d8faa51d120c7508f`  
		Last Modified: Sat, 13 Feb 2021 01:50:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe585f4a68228bec2b5b6765c7a8a860d41e59a842e3b43871e7120172ab40c7`  
		Last Modified: Sat, 13 Feb 2021 01:50:06 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:4f80cd66b8eb83d68da1b3cd894fe37462760fe5278f6973301e26f1af90bc91
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41520139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96e1652c7ef7e3d880320ae65765f36dfe4d599e1ca9ac8c0154dcf0e54633a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 18:39:55 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 13 Feb 2021 00:58:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 13 Feb 2021 00:58:43 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 00:59:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 13 Feb 2021 00:59:17 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 00:59:17 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 00:59:18 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 00:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 00:59:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbea90aac4746d1c996386053d6406bfa4610451eae6d17da249dee74c9b3a68`  
		Last Modified: Tue, 09 Feb 2021 18:40:55 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b87a23d1edb8994421e0ef8e6ae3e7a6364755d7e174130d7b4076dfa2119e`  
		Last Modified: Sat, 13 Feb 2021 01:00:08 GMT  
		Size: 2.1 MB (2132258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7cffa8181e625c430a03c89cc64ae89e03825bd80c01986ce5486ad61b4c12`  
		Last Modified: Sat, 13 Feb 2021 01:00:11 GMT  
		Size: 11.6 MB (11632985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15dfc8a7a89424ce7b74424465fcef8b14d61f39590f94169b3a7afd30130b0`  
		Last Modified: Sat, 13 Feb 2021 01:00:08 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3837cf2d6a87c1b6e64337cafb4ddb0959d201146a766002cc849caa670bae`  
		Last Modified: Sat, 13 Feb 2021 01:00:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:25a5e4c9bfecee13942120bcc34a2cdb13e00addd065a17df1302153ead12de4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33895238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818a59f972b27eb92864d12c7304285f5966446e58096f31ad3b67a0bc8d07d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:51:48 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 12 Feb 2021 23:11:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 12 Feb 2021 23:11:03 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Feb 2021 23:12:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 12 Feb 2021 23:12:11 GMT
VOLUME [/spiped]
# Fri, 12 Feb 2021 23:12:12 GMT
WORKDIR /spiped
# Fri, 12 Feb 2021 23:12:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Feb 2021 23:12:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Feb 2021 23:12:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8e1cbf99b578f9b5da0b78824733a66db880b685f597795dd41a08ac6b4f2f`  
		Last Modified: Tue, 09 Feb 2021 17:53:36 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5463eef3d8ce71368876b45ca24071008cc083ea16ea90ad16da78aee1b06eb0`  
		Last Modified: Fri, 12 Feb 2021 23:12:26 GMT  
		Size: 1.7 MB (1712078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07c83f952ec2caa0e8a9319f93360620700120836fe9678c29036c7cf9868e9`  
		Last Modified: Fri, 12 Feb 2021 23:12:31 GMT  
		Size: 6.4 MB (6416347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b88510861e3f585271a563d2bee51e8dc1659e7abc654317636fd8a6e35956`  
		Last Modified: Fri, 12 Feb 2021 23:12:24 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8a904b2624ec463e93f83225ac51eebd738a0473f323cf0121dcf664488951`  
		Last Modified: Fri, 12 Feb 2021 23:12:25 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:864f9629da12aace742df3cd8167639ca43ff06a00763b99c31dcba10699a00e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39490261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749c18efc7646905a7417cb2107c88294bb750ed6bc8039f46b4311923b6e779`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:15:19 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 13 Feb 2021 02:30:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 13 Feb 2021 02:30:40 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 02:33:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 13 Feb 2021 02:34:02 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 02:34:09 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 02:34:10 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 02:34:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 02:34:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46b97146405ece3ed453ad4ebc496b4b66b0fff54fdc49d2f4d3175043dffaf`  
		Last Modified: Tue, 09 Feb 2021 04:26:38 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47130d66484e5dc6224d68f7eaf7129048723a038246f1ba3288bc669594ce4d`  
		Last Modified: Sat, 13 Feb 2021 02:36:06 GMT  
		Size: 2.2 MB (2224915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f7be408970c00a6f67d09788fe2ae7d9bee14d0ddedf38e826cbedc4e12d6e`  
		Last Modified: Sat, 13 Feb 2021 02:36:07 GMT  
		Size: 6.7 MB (6743622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed58efc2e2df4e58c29b6b3946f036cdf35e85ba6b21cf906c7fe425b1efc82a`  
		Last Modified: Sat, 13 Feb 2021 02:36:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5da930633055937f1ba62f43cf83b555b527d1cd8255d66ac9d6281f3afa41d`  
		Last Modified: Sat, 13 Feb 2021 02:36:06 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:f1fc57dae92710b70032be2526f79e54964e55f92c1743f69ec7cf0a676d8116
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33477416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dda528269da27ad9d1592ca7bc595ecbacc814c873d1441327b98560f8a43b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:33:39 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 13 Feb 2021 03:10:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 13 Feb 2021 03:10:56 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 03:11:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 13 Feb 2021 03:11:22 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 03:11:22 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 03:11:22 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 03:11:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 03:11:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b494d8c5eab48f88712e47a52fa76da28e3b84d610e47c02ef6554cc1e57e98a`  
		Last Modified: Tue, 09 Feb 2021 06:34:18 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916e90eba0ded4a99e0c1e86e0657b977665bf19661f2c18005fc6d6745d7fd4`  
		Last Modified: Sat, 13 Feb 2021 03:12:19 GMT  
		Size: 1.8 MB (1821717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9478c638398830f42321041df73fb7c8005dd7c336c933045b5f043fe1e8786`  
		Last Modified: Sat, 13 Feb 2021 03:12:19 GMT  
		Size: 5.9 MB (5943471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fb1c3cf1445657cf0a44894ccf3da2d62b39264d89fcbecc0e2db075fcfdcf`  
		Last Modified: Sat, 13 Feb 2021 03:12:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f2ae3abab433a32b5e6ba282e6544117d7a01f4fd183d4a7582a4c5a64479f`  
		Last Modified: Sat, 13 Feb 2021 03:12:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
