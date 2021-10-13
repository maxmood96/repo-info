## `spiped:latest`

```console
$ docker pull spiped@sha256:f96c412ad97a7d1f42f7b80e47e2ab66238f610263ae5e10e5fd0cbed2e9e34e
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
$ docker pull spiped@sha256:a696ea93d50ac968bc64ce5ab01eaf4ff13ae39fa9f099b9cd19a8e7a9d07aee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37320955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683078eccb0851809c92a9dfdb1dcdd47c187bd8a7a5cc960a8fa55b1ece7e86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:42 GMT
ADD file:16dc2c6d1932194edec28d730b004fd6deca3d0f0e1a07bc5b8b6e8a1662f7af in / 
# Tue, 12 Oct 2021 01:20:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 16:21:25 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 16:21:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:21:29 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 16:21:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 16:21:56 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 16:21:56 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 16:21:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 16:21:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 16:21:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7d63c13d9b9b6ec5f05a2b07daadacaa9c610d01102a662ae9b1d082105f1ffa`  
		Last Modified: Tue, 12 Oct 2021 01:26:05 GMT  
		Size: 31.4 MB (31357311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c825e91f209a1656f91feea4a2861373b55da8c1c3eb72e742c7f31c3d367918`  
		Last Modified: Tue, 12 Oct 2021 16:22:19 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3f6cb28bad6f7f95e8be3b815465b3d5585c01a7cde8e6c561a81fd08d8e7`  
		Last Modified: Tue, 12 Oct 2021 16:22:19 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbac5321939b951af500d72dc338b30ccdc61d354b3a466ce698a006ca3f4999`  
		Last Modified: Tue, 12 Oct 2021 16:22:20 GMT  
		Size: 6.0 MB (5960389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58545b0e832a28e4b2fe9fe327f35158f38ccc204ce2c8fe1597803e860c0c2`  
		Last Modified: Tue, 12 Oct 2021 16:22:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1557262dbc7e84098fd29719562170e4c257f980350cf3e68318ecd07a8956`  
		Last Modified: Tue, 12 Oct 2021 16:22:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:470773bf2dac565adf268ce74a10c0ca68c421d0de4192c4f6f29f15e8663e54
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33928107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee42cb8fa181c28acac6a722b80b4ea34b101698e1d8886a77f8323f3dbc1d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 00:50:30 GMT
ADD file:fb1afabdc1f93b4866b4c4d696f272b4888519cb5bf35eb7ed1a4c021d1a04c8 in / 
# Tue, 12 Oct 2021 00:50:30 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 11:33:43 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 11:33:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 11:33:53 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 11:34:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 11:34:55 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 11:34:55 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 11:34:56 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 11:34:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 11:34:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5c9bab66abc5c53391435f6fd66e0ff3571295d568f45ac7d2dc480bcbfd56e8`  
		Last Modified: Tue, 12 Oct 2021 01:06:07 GMT  
		Size: 28.9 MB (28899715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29fa5bfe046f908c4024b12760d6a235703129cf889a6b12fe9cb3c909e50ea`  
		Last Modified: Tue, 12 Oct 2021 11:35:35 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15e6ebdfdcc8907dc36ff08f672c463d0fbb6c59b0bb232ff1a229f64e4ea34`  
		Last Modified: Tue, 12 Oct 2021 11:35:35 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0030f062ce13c3eb3f6f0020460e01e4beebed73ca735660e5fe74df98d62119`  
		Last Modified: Tue, 12 Oct 2021 11:35:40 GMT  
		Size: 5.0 MB (5025142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9edc074a3eb9dffdb9440831266c18299dcccc42834d767fc489b92ca7f2a48`  
		Last Modified: Tue, 12 Oct 2021 11:35:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7dd4a1c957efda249f4568cd568c8671c526848a4b9f57ffc9783bf81cef3`  
		Last Modified: Tue, 12 Oct 2021 11:35:35 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:958d2e76bb92a4709c36123b6553d179419227b06b733ec19cf1a4899da20853
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31309843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0880cb9c6c234ff2fe6a3c163710a28845c22e1207ecd0b31cd8887cb77d26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:28:36 GMT
ADD file:89eac94007ac04f9168737686fa0a6c737f2c28fc9e5918d4d512924fe1973be in / 
# Tue, 12 Oct 2021 01:28:37 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 03:43:34 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 03:43:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 03:43:42 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 03:44:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 03:44:37 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 03:44:38 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 03:44:39 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 03:44:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 03:44:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4e5300249f84466df4dc73ea0ce09938ca00c1718bb12619c4f26bd936162331`  
		Last Modified: Tue, 12 Oct 2021 01:44:28 GMT  
		Size: 26.6 MB (26561058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ecc7e48d063e5bf0a086847e03c73699a183e8a9129e1b8ee3cab1482dde2d`  
		Last Modified: Tue, 12 Oct 2021 03:45:39 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584009012f86b47c7e4e6d1fd99c2d00976e77d0c5c66f0179ed3c7ea7c54725`  
		Last Modified: Tue, 12 Oct 2021 03:45:39 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae397080ab7f297afe0c2760bc744f5c6ab5ff8f88b8e0830bc8ae8d97b565f`  
		Last Modified: Tue, 12 Oct 2021 03:45:44 GMT  
		Size: 4.7 MB (4745527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c697bb38b9e3862762d00df70d8a431fd891e25b33a03308c9e1cf59a02c712`  
		Last Modified: Tue, 12 Oct 2021 03:45:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c305948d80dae9d7e0b495eba60d890696dba8079d33af0619bb473c03c079`  
		Last Modified: Tue, 12 Oct 2021 03:45:39 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:e42973d685d58901eca16bda47af6c81d8b31151a53e41a18cc0b1b16516e2d0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35312197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6b7887c5411f5b490101b1a2dfff1e04370eab87e2a7429bd9d12c366a18c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:18 GMT
ADD file:d84144ad575672cd6cc8a00c8e5a88ab0545348f040fc249ea5fcf8193b2bce6 in / 
# Tue, 12 Oct 2021 01:41:18 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 11:49:41 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 11:49:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 11:49:44 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 11:50:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 11:50:06 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 11:50:06 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 11:50:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 11:50:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 11:50:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a9eb63951c1c2ee8efcc12b696928fee3741a2d4eae76f2da3e161a5d90548bf`  
		Last Modified: Tue, 12 Oct 2021 01:48:13 GMT  
		Size: 30.0 MB (30043906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5208c6c75ae69847fd9d6b719ec9e4cfae78e61930069427cd74b19d44684c98`  
		Last Modified: Tue, 12 Oct 2021 11:50:39 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fa3e30a6eb07aa9a34cf2181ded5365f9eee9d8ab90e0ed941f8a4087ab387`  
		Last Modified: Tue, 12 Oct 2021 11:50:39 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b32d1f23ddb9b2da5bc8c3f8d745570720579ba9a54b19e5e119c207449bb10`  
		Last Modified: Tue, 12 Oct 2021 11:50:40 GMT  
		Size: 5.3 MB (5265036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2a99fa27771c452dc5fea2b481ee10562f86d5b4d78962b517d4f9875d74c`  
		Last Modified: Tue, 12 Oct 2021 11:50:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc8e77df2f719fa6c20a8b676f4f5ada4b9d485f189a246f942245fbf2cea24`  
		Last Modified: Tue, 12 Oct 2021 11:50:39 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:7e62ad8ce0310713b81cee83e9f2df9a18a94cf41dc99ba28a629f7554aeefa3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40257794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2bf1ef1d62cb3d5701cdee3834206614fd56059103a424063a602168d47abe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:39:47 GMT
ADD file:42196ffa4c70af8d9f1e7b74edb3bb92d47296acf989adf615e8208230f8bd0c in / 
# Tue, 12 Oct 2021 01:39:47 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 22:29:57 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 22:30:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 22:30:05 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 22:31:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 22:31:03 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 22:31:03 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 22:31:04 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 22:31:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 22:31:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:87318d165b5c0fdf05c8ccf97d83084f56b4608075a3335b1a46c76295b82753`  
		Last Modified: Tue, 12 Oct 2021 01:47:39 GMT  
		Size: 32.4 MB (32370344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4928a77f1df28f1a46c20db916ae41f9f3331dc5058d03d8298439de44db7b91`  
		Last Modified: Tue, 12 Oct 2021 22:31:47 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb53cf6a9579bfadc1f1fd25438cdfad0ff235db1fe68eb4bb2afd7719b791d`  
		Last Modified: Tue, 12 Oct 2021 22:31:47 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aef6d6c4e04c173d1a0914846ba20d15a2f5f95d88f30069d1eca250898b325`  
		Last Modified: Tue, 12 Oct 2021 22:31:49 GMT  
		Size: 7.9 MB (7884197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b6984d7102b271e3fdc811759f7c556d04efe1259b67fab31e59565516fbed`  
		Last Modified: Tue, 12 Oct 2021 22:31:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e088d6a7c91ad6e879108222fefc2fff6a12de71734608e2b594ae36399c1d29`  
		Last Modified: Tue, 12 Oct 2021 22:31:47 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:eff58594b3d812760bbc2b4221d61e20cd31ab2ada880341e6e756d55b0e8dfa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35328007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaccc3d11f7debbf79cd094b33cdae93860e3d40b42f7779edf587b67fc976c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:11:15 GMT
ADD file:f90ca8957172106f42a9096c9a21082d51f3201aa78e6f64621a73117e2b7b6a in / 
# Tue, 12 Oct 2021 01:11:16 GMT
CMD ["bash"]
# Wed, 13 Oct 2021 01:30:36 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 13 Oct 2021 01:30:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 01:30:47 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Wed, 13 Oct 2021 01:31:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 13 Oct 2021 01:31:57 GMT
VOLUME [/spiped]
# Wed, 13 Oct 2021 01:31:58 GMT
WORKDIR /spiped
# Wed, 13 Oct 2021 01:31:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 13 Oct 2021 01:31:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Oct 2021 01:31:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:59ddca50ce05605e6234c1e7213c39cdedabc48ef11637e12156b7bd69afe161`  
		Last Modified: Tue, 12 Oct 2021 01:20:03 GMT  
		Size: 29.6 MB (29618732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195b13cd10a541ef73f29b46be3ae53a62b047ad5919580c0601496f9a63a3f3`  
		Last Modified: Wed, 13 Oct 2021 01:32:10 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11abea7ddca4b5031aa9fdff9ad5b49b60d36fd5940b7805f93333ca5da482f7`  
		Last Modified: Wed, 13 Oct 2021 01:32:10 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b0c25ac4296890c80ee4f1bea71c20c6a8251252085a00c9f764d7601ac9e7`  
		Last Modified: Wed, 13 Oct 2021 01:32:15 GMT  
		Size: 5.7 MB (5706076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb391de145f2fb5b8ba0dda5a96231a88d0c7e58514503ab861743a74f24c3ea`  
		Last Modified: Wed, 13 Oct 2021 01:32:10 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bbf8647f8ba425f0ba8506aa7c276231190bb29fb4f34f2306f160f1c3795b`  
		Last Modified: Wed, 13 Oct 2021 01:32:10 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:b854abceecf263ecd3af9062c9bddf00c657ddc847f0a7beffa3d324806c6bfc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41277029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9de0b22b9d88c7e7b941d2522f2954d1ff0b9cdfde5162978baa1f74ddd6d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 04 Oct 2021 17:55:01 GMT
ADD file:f4b696a766a0d9a808c171a1d5db4f0877b0a784649d63bf461dfcf54b532239 in / 
# Mon, 04 Oct 2021 17:55:06 GMT
CMD ["bash"]
# Wed, 06 Oct 2021 04:33:42 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 06 Oct 2021 04:33:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 04:33:53 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Wed, 06 Oct 2021 04:35:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 06 Oct 2021 04:35:21 GMT
VOLUME [/spiped]
# Wed, 06 Oct 2021 04:35:23 GMT
WORKDIR /spiped
# Wed, 06 Oct 2021 04:35:24 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 06 Oct 2021 04:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Oct 2021 04:35:26 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c3b7af0ed242d09d9fee2dfc48d4553d58ad90c5fb862ab58fb89e2d04c5b922`  
		Last Modified: Mon, 04 Oct 2021 18:07:32 GMT  
		Size: 35.3 MB (35272408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61743fc20904f8539cf80302250d866a1c6417663826735c20362034cef7501a`  
		Last Modified: Wed, 06 Oct 2021 04:36:06 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da94c352893f839938e7606a77c9b6a0c747558c66e01483dd5ef4a69a07383`  
		Last Modified: Wed, 06 Oct 2021 04:36:06 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534d0224ab6f6639dbd9d41948087e426816f7e37e5940c041d0b712088c87b3`  
		Last Modified: Wed, 06 Oct 2021 04:36:08 GMT  
		Size: 6.0 MB (6001359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0eb63df061584de7f6a9d4c754a21f5a3426f46c6704a41d99439d92f398a56`  
		Last Modified: Wed, 06 Oct 2021 04:36:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f8bfc7f69743b3fb3ffefa3ccfdcbc84807fe7c346480cc8313ee1af72d33c`  
		Last Modified: Wed, 06 Oct 2021 04:36:07 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:0ea844713c5be79b86f0ed403e6d7a38c6b37f92d690035d328f933e7d828d3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34828428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224bab1ef5e8e000f26cc5a15fc7f3d3851979e858ee4d475d6f18295d2e5c27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 00:42:27 GMT
ADD file:6038dd6db57fb05c3d39c02c3379667ccd2989e7667ff773a8020fe6a69a760c in / 
# Tue, 12 Oct 2021 00:42:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 04:31:53 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 04:31:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 04:31:56 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 04:32:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 04:32:12 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 04:32:12 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 04:32:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 04:32:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 04:32:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ded751c48f72503973be01be2794cc039490f22b039b8ac106e9f17de4980742`  
		Last Modified: Tue, 12 Oct 2021 00:48:05 GMT  
		Size: 29.6 MB (29641215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9339c2f00e96cfd5d66e69eeaec4b0592b4ff1f2798f167750a1ca9f15264c42`  
		Last Modified: Tue, 12 Oct 2021 04:32:43 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1ae5a6b4870b8387c848046338d1914594cc3738bc5631e96eb22fba322290`  
		Last Modified: Tue, 12 Oct 2021 04:32:42 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61437e76afae45198095fc895e7d4154ce1ca4d68f4a7f7ad160c99b7bb4d341`  
		Last Modified: Tue, 12 Oct 2021 04:32:43 GMT  
		Size: 5.2 MB (5183956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90528d405e1a63caf7013a7715aa3ba6a0d0eabc5ce0955bc7a383eb3dd3cef8`  
		Last Modified: Tue, 12 Oct 2021 04:32:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5158295881f8176e354104f90f22e99b9211b9860e03e398f262f8a6b5828a4`  
		Last Modified: Tue, 12 Oct 2021 04:32:43 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
