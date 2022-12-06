## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:6691ce3296a8b4ea3644c272a63ebc0565a0186d5ba460e04016e8be81b03473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:e734f3350fc8e3cbffcfe3dcb42a88099785465637c76e2601dfd3ad685ee7a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61259424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2cf5a83fdf39152c071428b83ada395e7c3858aeb326a500370c09e1fc39d26`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 04:05:03 GMT
ADD file:96ca7e18b6141668321140f8ae1a496641f631313035513f1f9314e9dad2cd71 in / 
# Tue, 15 Nov 2022 04:05:04 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:10:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:10:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 15 Nov 2022 13:10:56 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 15 Nov 2022 13:11:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2730d739afad9b8ff3e3029e23fd69d9533603751d6e42053ce0068c2b58e258`  
		Last Modified: Tue, 15 Nov 2022 04:09:05 GMT  
		Size: 50.4 MB (50448823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fca1bc133dec52587564a08d86ecf97ccbd619c537a10d7523e214fd7dc979`  
		Last Modified: Tue, 15 Nov 2022 13:12:52 GMT  
		Size: 10.5 MB (10504260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e431fb20443b2100d30c4dbaee3fc077f7cdf06ea25db1a50095ae44f9bf01b4`  
		Last Modified: Tue, 15 Nov 2022 13:12:50 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5daab9e1641bf6cd75e404663309d1587f798a59e047761730a172bb06d8671`  
		Last Modified: Tue, 15 Nov 2022 13:12:50 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3932639071cd8a9aed3bca4f449664c9c7021d039099b1d7a4b562f2bfe2d8`  
		Last Modified: Tue, 15 Nov 2022 13:12:51 GMT  
		Size: 304.3 KB (304328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:34d59376bb6fd369dba04ad0229ec246b3b1835141a985ae973bbaf611b75ca9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60050268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f80b22fe316ddafbc045a99cfd3625d95c45761bd47817503c24a8e0b4986e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:24 GMT
ADD file:2deba7c04e28d01997b865f366cdc8d38a80aa39720c4e4d1fc581ac17e8ce4a in / 
# Tue, 06 Dec 2022 01:40:25 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:06:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:06:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 06 Dec 2022 04:06:24 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 06 Dec 2022 04:06:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:47d0ec2abdb05569eada58143acd16d47ee4b07a33535544cf5bf267bde20cc3`  
		Last Modified: Tue, 06 Dec 2022 01:44:13 GMT  
		Size: 49.2 MB (49233737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e928f3f303597bfd9fba2e92cdcf920d9fcafe42efca63103692d4366569b`  
		Last Modified: Tue, 06 Dec 2022 04:08:12 GMT  
		Size: 10.5 MB (10510258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8461cf556d4a4eaeaf44cbe29b1878cf0ad26ef6e36e98337ecc9eb7377b8367`  
		Last Modified: Tue, 06 Dec 2022 04:08:11 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feef9992ce9a2afe0529457ef73f13aca535f78aab518de102c86fe7217e2d1d`  
		Last Modified: Tue, 06 Dec 2022 04:08:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7ec231f354dd9452eb9dd010b908af0dee64ae8f3539f3420ce581f6bc97f8`  
		Last Modified: Tue, 06 Dec 2022 04:08:11 GMT  
		Size: 304.3 KB (304260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; 386

```console
$ docker pull neurodebian@sha256:c98f606d9cae2023b25752a3bac24dbcb3b6f342ca0381796e5ba196153e5ee3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61990755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba2ec4bd299fd6589a114ee49db27c75e4f2d9d22afd4929f25088d36e5c801`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:05 GMT
ADD file:0688532a537bb23756917f3d062da18668cd55041d0ae6610cff386043ffbdd3 in / 
# Tue, 06 Dec 2022 01:40:05 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:36:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:36:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 06 Dec 2022 02:36:20 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 06 Dec 2022 02:36:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:54f3d93b8ab6f3a5195d99724d5bc911156006687d577448bd8e94d2fe049d4a`  
		Last Modified: Tue, 06 Dec 2022 01:46:02 GMT  
		Size: 51.2 MB (51207714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52f14263b329659da79ea4fcc974aadef164b5153566c19de9ced29a459fb32`  
		Last Modified: Tue, 06 Dec 2022 02:38:35 GMT  
		Size: 10.7 MB (10672362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000af179d21568271868a60e00d3a02ba057f979b6ecc853c0e63acb3936c2b3`  
		Last Modified: Tue, 06 Dec 2022 02:38:33 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49bc8df4bf8edf0ca1930f9ae62123cb277fa05e81a481284d4224fd2b8eda74`  
		Last Modified: Tue, 06 Dec 2022 02:38:34 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f82edf13dc6975ebfb768a45e0428cd2a014991ed06cc785ae36ac908b64602`  
		Last Modified: Tue, 06 Dec 2022 02:38:34 GMT  
		Size: 108.7 KB (108695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
