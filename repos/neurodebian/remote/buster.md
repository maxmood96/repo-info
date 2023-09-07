## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:9cd86d6cf0e0c55836019196159db9d05d6790504d473d33a78a25b3b59b2565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:91bad85094213a23503ec7de105f76ea853905fef37664d9d805972dedc1bde3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61302857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0047b777908e5afa6a3d6428f84b62a51621edbe81d91fad822c69c8fda2ba0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:23 GMT
ADD file:d9c3e291731c1f06d615709ebc665a41f6d6355607d87ae00768e3be4b330bed in / 
# Thu, 07 Sep 2023 00:21:24 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 14:37:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 14:37:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 07 Sep 2023 14:37:18 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 07 Sep 2023 14:37:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:311da6c465ea1576925360eba391bcd32dece9be95960a0bc9ffcb25fe712017`  
		Last Modified: Thu, 07 Sep 2023 00:26:22 GMT  
		Size: 50.5 MB (50497598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65889c056ce3c15df2ccdf04e989bf5eb3d5675ee6aafa1b9d08b43a761045ce`  
		Last Modified: Thu, 07 Sep 2023 14:38:56 GMT  
		Size: 10.5 MB (10504694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeed76e78a8a72539573cd58e7150b487f0f89e943f6df2d1d0b67172fe3357`  
		Last Modified: Thu, 07 Sep 2023 14:38:54 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cb98d49b7c8ab46b449589f317b7ce9c64a0e4795c54e3c47b327503c4ca30`  
		Last Modified: Thu, 07 Sep 2023 14:38:54 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c51d2968ed057ea2e02d12598053103e4dce954bd220e597fa3e63f761190c6`  
		Last Modified: Thu, 07 Sep 2023 14:38:54 GMT  
		Size: 298.6 KB (298562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:da63776b0c9b852f50b40c8b4cc0b5a8788154364cc92c6226456a296fa74cad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60101739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bef327a24f8a558a0f40d3cd279700e3786cdaa21c827bdc76f64dc063964ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:40:00 GMT
ADD file:d9e56538de5f967fc9a8327ecb4e67562f6f95e56b455b9494e35d3b57c89332 in / 
# Thu, 07 Sep 2023 00:40:00 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 09:33:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 09:33:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 07 Sep 2023 09:33:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 07 Sep 2023 09:33:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:26ee4ff96582b6c5e191414a6b74b283e3039e003d1b6f546cc00d6b14ff8abb`  
		Last Modified: Thu, 07 Sep 2023 00:43:57 GMT  
		Size: 49.3 MB (49290609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b049c66961bb51a7ca001e84631f235b0b1baa774f6fdba684d7c3a46bd5be6`  
		Last Modified: Thu, 07 Sep 2023 09:35:11 GMT  
		Size: 10.5 MB (10510606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b17b6a6b8a31d0da61e017c5500355633bf0c332ef1a4eeffb0880c3bb0003`  
		Last Modified: Thu, 07 Sep 2023 09:35:10 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4d9c7af78a8420e6e523a9101728e05a554839288629c4cc955088b2ebfdac`  
		Last Modified: Thu, 07 Sep 2023 09:35:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2863a8454ec23a756c292290c3fc214e424ae6c7a16a82d07ae524598b4e41c9`  
		Last Modified: Thu, 07 Sep 2023 09:35:10 GMT  
		Size: 298.5 KB (298512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; 386

```console
$ docker pull neurodebian@sha256:f03ccd686cca341fae93d8670d9292c8a7d807634127f736d4fa4c5853041068
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62424044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c93039e4a48e4f4c1133fd0fa465f24b471165bec7c1dd00fd2666b08b567c3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:35 GMT
ADD file:e361f508945f7d4a295d9dd30a26c2eec74e47dd5a1b49328c7a6a7ed2d94d63 in / 
# Thu, 07 Sep 2023 00:39:36 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:05:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:05:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 07 Sep 2023 01:05:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 07 Sep 2023 01:05:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fa64faf93a921e8d6df313df0ab0ce8255885730dc1fc137cb62b66633477d02`  
		Last Modified: Thu, 07 Sep 2023 00:45:01 GMT  
		Size: 51.3 MB (51255123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0e4b79d61677d66a62c42c585a8a1e725012534e25ac9674286e07551a1445`  
		Last Modified: Thu, 07 Sep 2023 01:07:22 GMT  
		Size: 10.9 MB (10868419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aadbb0399c30d27a48a06609b3fbf2d605377e91fc5240f9a6f757a64d94c7`  
		Last Modified: Thu, 07 Sep 2023 01:07:21 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26f43c3c0242c6196f4e32021f858ff620b38dcb164f94f2092c4375ab4b294`  
		Last Modified: Thu, 07 Sep 2023 01:07:21 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a69230fb59e85c5eb0210f6a1d77a751b0c7686eb38c1232a6e971f0a56f57`  
		Last Modified: Thu, 07 Sep 2023 01:07:21 GMT  
		Size: 298.5 KB (298491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
