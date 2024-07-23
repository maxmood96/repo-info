## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:b334c22228e82e48cb0c20eefbd620a6ea28c2b2937cd9b5f8b436fd530cd94c
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

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5c00b1b02a702a0a5c10a0c39de2b3534ca77f48014eb9369879b46822682885
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73603858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57307da48a041f146ebc02cade9cff052aedd24b9c9c797d99cc488097c920a9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:24:49 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Tue, 02 Jul 2024 01:24:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:48:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4bc6251bd1bf7924bdd071d2f8e8a03475c3e69391f962e607c8439e184e5a18
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70047862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f5c00b221473b36b60a5dc32b584b5b5b80fb0203beae0e791ca040f5a7e92`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:48:18 GMT
ADD file:e0c33927a1af62d353710ab02fe9345a8805475ab99685993742946d38302465 in / 
# Tue, 02 Jul 2024 00:48:19 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:12:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0a5605902d45ef0417ea17b5dd427638ed2b12e334e19bdc8d0267ea76089132
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67102135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854fef5d2b580eabfe521263962beaf8bf54bd75f69fa01812760eb5c19ef11d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:59:52 GMT
ADD file:526dbb34ac449ae8f3c9025d71b3ffeb0e24fa5dc1a01da707f0a8b834eb4e33 in / 
# Tue, 02 Jul 2024 00:59:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:24:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a8155f724f1e6e368526d3793b1e62b186bc19d14d3bc9017ac2b29aa075cb8e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73179593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc5c4b620ecc5a3f564f49bbc825a6843e429303da6ec5de922ca9a2fe13fe6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 02 Jul 2024 00:39:29 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:bdf54b2f808e3990b7498c35f230d3eb509cd2280622e6529039bd2cb64795ad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75469439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8183189c4f926141d9fcd3f4ba7a1c216409847481eeb12165c1774e5e2338`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:38:40 GMT
ADD file:262529672396993121e97bbbdda3d91ce43c7548adf11a263b7ec53bb7cda4d2 in / 
# Tue, 02 Jul 2024 00:38:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:05:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:59005510b61f0f0ef977e4f2962bab45b50e47a53845aa5cc1d7786d44a5ada4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73199702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84595c9eabc4b54f273d65e511c9cf48b6e5d6e8409b6ae5813074faa4797603`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:36:56 GMT
ADD file:bc2014dd4183b8b941ef345add7dfa4a5b389afd70c64828331a9e51522a8c03 in / 
# Tue, 23 Jul 2024 00:37:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:44a13b4fd2ecaf87d3361e50327286868a7ff3b7a41b6e877c1b5e4b22990de1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79252579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7a3cedc1cf1f38c69c9e9ccb44c8ddcdb8c4513da74fdf516f7837f69ad38b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6668f3a82b2afde87f4bf8624afffe3c2b8666dca25a89f8dabe8907c8a64c54
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71980383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1d89a33a9cd59d306aff923b32fb31c0e67238ae467347e20ca2e2490102ff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:43:28 GMT
ADD file:397aa43721bc5ca67ab359263843a05c62e131f07114e92f39927f59790c9a5b in / 
# Tue, 02 Jul 2024 00:43:30 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:32:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
