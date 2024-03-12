## `spiped:latest`

```console
$ docker pull spiped@sha256:d03ccf152b46e319e9d17c501ed52262d6fc7636221ef91146f9c0defdfa2a03
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

### `spiped:latest` - linux; amd64

```console
$ docker pull spiped@sha256:96db7707bb5d8916a791ed0907165e489c61e917c1821714173b14f18b5ed6a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38186578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dfb514b64830e18e7f24f11a5355db63e676c8819afb9a98870a1c9a9047ce9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:50:10 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Mar 2024 05:50:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:50:14 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 12 Mar 2024 05:50:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 05:50:38 GMT
VOLUME [/spiped]
# Tue, 12 Mar 2024 05:50:38 GMT
WORKDIR /spiped
# Tue, 12 Mar 2024 05:50:38 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Mar 2024 05:50:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 05:50:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbebceebfdc39d4c5ba18adca7968edd57fbf652c06e3279d8099ec0b126fbe5`  
		Last Modified: Tue, 12 Mar 2024 05:50:53 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04298cad5e310111491cb51e62449f82c37687f0f9cf1f8e57a477491de1477c`  
		Last Modified: Tue, 12 Mar 2024 05:50:53 GMT  
		Size: 2.6 MB (2590286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740979e6024d92b7e3ba0cef4c4dc73ca0b13fbd50f362072ea8fcbae0952cc9`  
		Last Modified: Tue, 12 Mar 2024 05:50:54 GMT  
		Size: 6.5 MB (6470515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9e2427729f125df3f1b3b6afa759050ca4cb6e4959e3813ea9df595a150eaf`  
		Last Modified: Tue, 12 Mar 2024 05:50:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e580953049d7a6f7d9f15c382c37bdef422d4fd4018605853d1e5e842071ec97`  
		Last Modified: Tue, 12 Mar 2024 05:50:53 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:62129f2575c4a8ccc8930e144b2a7b93250483198a77e85c30d8afa73ba44207
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34209304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80cb7e5ebbc828060f0c47f49d13efc5977fb8f9df638b3f8931944c79983c77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:31 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Tue, 12 Mar 2024 00:48:31 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 08:02:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Mar 2024 08:02:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 08:02:07 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 12 Mar 2024 08:02:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 08:02:28 GMT
VOLUME [/spiped]
# Tue, 12 Mar 2024 08:02:28 GMT
WORKDIR /spiped
# Tue, 12 Mar 2024 08:02:28 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Mar 2024 08:02:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 08:02:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cba582a8425521ac0c5972e48237cd9502b75878eb913603eb9559b47ea40fd`  
		Last Modified: Tue, 12 Mar 2024 08:02:40 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4923d27af522ac6034058ebea0bbab5d76663d3e55e0950be43577f7ddcfa73`  
		Last Modified: Tue, 12 Mar 2024 08:02:40 GMT  
		Size: 2.2 MB (2185978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b04bdb9719edb47a735924402ecd2f99a40c5403add6faa6fb37a08b77544d2`  
		Last Modified: Tue, 12 Mar 2024 08:02:41 GMT  
		Size: 5.1 MB (5137703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf17339e072b7ac20b2549e74c6d81ea386016faeb61a8436c1851e1e3e9400`  
		Last Modified: Tue, 12 Mar 2024 08:02:40 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c503125129ad74fe884ec3944c1df58a09ba6592f2ef0c095d6018bd87037d`  
		Last Modified: Tue, 12 Mar 2024 08:02:40 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:deea9a9e8ddbeef53e47be755526ab645a215f752e3a879ce9086d25c666a950
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31642445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aae8a257b249f63fee7c2fb9a2972f61301fba2e0008ceda9ae4471ae4f2231`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:13:16 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Mar 2024 07:13:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:13:20 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 12 Mar 2024 07:13:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 07:13:38 GMT
VOLUME [/spiped]
# Tue, 12 Mar 2024 07:13:39 GMT
WORKDIR /spiped
# Tue, 12 Mar 2024 07:13:39 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Mar 2024 07:13:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 07:13:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7231e458b7bd29405b9cb28267dedddffc6b83faa02c36fe03c77e657190d4b`  
		Last Modified: Tue, 12 Mar 2024 07:13:52 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8304e2c1b497b8d8c84dddf269714df957b2abda3faf8fb4a98e32a712303a7a`  
		Last Modified: Tue, 12 Mar 2024 07:13:52 GMT  
		Size: 2.0 MB (2044480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9fc59042ecc4edbdf2a609784e64119229b6f064898e848151e5766b85456c`  
		Last Modified: Tue, 12 Mar 2024 07:13:53 GMT  
		Size: 4.9 MB (4879642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aad7398ad856fd267bbd893444de8a78724bcf410391910ccd9d43a748d1de9`  
		Last Modified: Tue, 12 Mar 2024 07:13:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf27d404e50a20a1bac081e1fc349debb2c7bfc0d7cd8277b0f8fc3fc726ae5f`  
		Last Modified: Tue, 12 Mar 2024 07:13:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:c312d4d136a7cb679fbfec265e96f2c48b7ffdab7ab653c35db5647d715201c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37072008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5650ab795d2697271cf70947895fbbabcb67b62bc4ed87fe7a9d1cfc8a322053`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 09:54:53 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Mar 2024 09:54:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 09:54:56 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 12 Mar 2024 09:55:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 09:55:15 GMT
VOLUME [/spiped]
# Tue, 12 Mar 2024 09:55:15 GMT
WORKDIR /spiped
# Tue, 12 Mar 2024 09:55:15 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Mar 2024 09:55:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 09:55:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e5911ae5086ecfbf310ce6ccdd4d2b210958fe872a6b1e855477743c89ea9a`  
		Last Modified: Tue, 12 Mar 2024 09:55:29 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6735152d8568e1474a1663d67e6275f68f29612ce7ff128fb3c160ad0c3841d`  
		Last Modified: Tue, 12 Mar 2024 09:55:30 GMT  
		Size: 2.4 MB (2433264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4c98721da38f3cf2270ed724e5a3a7983cb48ef379f8b197a56b0dba63e581`  
		Last Modified: Tue, 12 Mar 2024 09:55:30 GMT  
		Size: 5.5 MB (5480711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a9228a8dc129cc0356babbad2dcf33a406f9aa3cf4649855b64f96667dff1b`  
		Last Modified: Tue, 12 Mar 2024 09:55:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b968d36331bab68a920b91f741805960abc46b9c1a862c071ede8772ba3f0212`  
		Last Modified: Tue, 12 Mar 2024 09:55:29 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:2ff36ce323082a7f4f1b0569476c0e0a67df0f4dc9f95a1193f7b602f03a6868
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38671964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2170ba886c1ad6a5c05ad951dc7d331c0eece021024beb7bff49d1738b1101e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:59 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 12 Mar 2024 00:58:00 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 13:47:18 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Mar 2024 13:47:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 13:47:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 12 Mar 2024 13:47:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 13:47:54 GMT
VOLUME [/spiped]
# Tue, 12 Mar 2024 13:47:54 GMT
WORKDIR /spiped
# Tue, 12 Mar 2024 13:47:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Mar 2024 13:47:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 13:47:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8050d2e14db556ecc65c323333b1fd0e2b99a968cad5112de2322d8176a92d1`  
		Last Modified: Tue, 12 Mar 2024 13:48:06 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cadbd2db55ef87274f55ef1cdd450b09f8c75f2682c49d6e41eff0d74cc209`  
		Last Modified: Tue, 12 Mar 2024 13:48:07 GMT  
		Size: 2.6 MB (2586924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ae80f708a4a3f10c85e8604c9778c71a07a19666ccb7bab9276db9fe4a0481`  
		Last Modified: Tue, 12 Mar 2024 13:48:07 GMT  
		Size: 5.9 MB (5941567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8766c4f5591962c0fdc2ff0090d640ce036d3fa12b7754fe596cc105c254e8`  
		Last Modified: Tue, 12 Mar 2024 13:48:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3610128fd2fbf8de8dcb4da26acd5f9f555ffa344398d9b5cee1c23741f12d4`  
		Last Modified: Tue, 12 Mar 2024 13:48:06 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:77588ba56fb6f3e2e0e1b69222e45ed2b5da937e2889b3087a28a435a35ea5f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36758416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7fdc27e325036131660ea1c8b58d9397ab01e6f836e80f0755d85ac7420218`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 19:34:04 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Mar 2024 19:34:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 19:34:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 12 Mar 2024 19:36:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 19:36:03 GMT
VOLUME [/spiped]
# Tue, 12 Mar 2024 19:36:06 GMT
WORKDIR /spiped
# Tue, 12 Mar 2024 19:36:08 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Mar 2024 19:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 19:36:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c56f028793c6c05d71887d8be3b11333ad131334f6239739f1bddabc46f1a1`  
		Last Modified: Tue, 12 Mar 2024 19:36:35 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c9ed54848a9e8b750fab53ced2ec7fcb4347779da19ba71042ca157bb718dc`  
		Last Modified: Tue, 12 Mar 2024 19:36:36 GMT  
		Size: 1.8 MB (1834530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9730968f0db3242a09a217ecb60528fbf7ff5ddceab7bb113e1f71c80af6d959`  
		Last Modified: Tue, 12 Mar 2024 19:36:39 GMT  
		Size: 5.8 MB (5803169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c172a1c04f8ee17ffe7befc5c1b57a30814a9edfafceffaf55be0fbb741f8a02`  
		Last Modified: Tue, 12 Mar 2024 19:36:35 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b943c9c7169f05d09a9e37dac35c50baa33be013c638638536f64a212f03f29`  
		Last Modified: Tue, 12 Mar 2024 19:36:35 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:09ca365da3240e5351ea05c51b4246443722ea25a47ff59619e6c25adb2c2cfb
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42312215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306bc18ff021f130a4a495714c5f600fa415a2a16f42595daa6692404c5e963f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 15:11:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Mar 2024 15:11:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 15:11:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 12 Mar 2024 15:12:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 15:12:50 GMT
VOLUME [/spiped]
# Tue, 12 Mar 2024 15:12:51 GMT
WORKDIR /spiped
# Tue, 12 Mar 2024 15:12:51 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Mar 2024 15:12:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 15:12:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce7f34db66d21815012180614769b95dc74f9ee223ceae0ad734c0e0a0a3635`  
		Last Modified: Tue, 12 Mar 2024 15:13:08 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e71710444a7036be10c7e897f3e85fed632415eb6cdd18e9d2abe4590628371`  
		Last Modified: Tue, 12 Mar 2024 15:13:09 GMT  
		Size: 2.8 MB (2769339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418f774749c94e9c610e0ca0e532d5692602e4b668c6efc3ae97038e17f150a5`  
		Last Modified: Tue, 12 Mar 2024 15:13:10 GMT  
		Size: 6.4 MB (6422253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ae62619b348cb24852882c321162147a2575e6dea19cc5cce2edf6a8fe1ef7`  
		Last Modified: Tue, 12 Mar 2024 15:13:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab06bee826a625eb6052f157d4d152724bb80bf1fcad7365567aa63883b6d410`  
		Last Modified: Tue, 12 Mar 2024 15:13:08 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:618cceaec06fe624d46633e39666906a8d6c72e5db2b74c5549e2d57b68ccfb5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35136366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2380efee6676e0d50a84b7dc3f732fc0418df10de6306b04f85527bb0801f63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 04:30:57 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Mar 2024 04:31:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 04:31:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 12 Mar 2024 04:31:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 04:31:14 GMT
VOLUME [/spiped]
# Tue, 12 Mar 2024 04:31:15 GMT
WORKDIR /spiped
# Tue, 12 Mar 2024 04:31:15 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Mar 2024 04:31:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 04:31:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f54ea7310e615c1f481c4ae4207377e309f7cde880b23d89627934858e35469`  
		Last Modified: Tue, 12 Mar 2024 04:33:33 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f304d0449087312897272f8917c09c105a674deb71e57e73b1e379684176d4b5`  
		Last Modified: Tue, 12 Mar 2024 04:33:34 GMT  
		Size: 2.3 MB (2260899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38ad6c82e6650ba142e209eaa0772f399b23b9057423e4bdc984e283859d470`  
		Last Modified: Tue, 12 Mar 2024 04:33:34 GMT  
		Size: 5.4 MB (5385188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6006ba2ba840f930164e5b7a37b1d440234233408cfa8247dc5e522143ee708b`  
		Last Modified: Tue, 12 Mar 2024 04:33:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5df9a7a38c8525b84c3d25106f2a15cedb9f28a591c208d053c3f12c32121b`  
		Last Modified: Tue, 12 Mar 2024 04:33:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
