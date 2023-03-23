## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:22dea449602d8560942c7b84d9e3bd0813eb0acc4a17fd39ef115e38023819be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:aaf4ace714149fbbd4aa37702ef9a418e815693769d5d6948d9680a098d95065
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea11c1f6a6a05aaedd47a751c5820a89bd89707b688187f4ba1a74e6f4642f6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:29:51 GMT
ADD file:98917c081507795b8ce084d09f5df75e959c5365882d73ca7a52da226c93fdcf in / 
# Thu, 23 Mar 2023 01:29:51 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:56:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:57:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:57:00 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:57:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c15c60aea1a8c926f00ec7713f9ae1fcd349591095bddcc01ee5a6027b8a3998`  
		Last Modified: Thu, 23 Mar 2023 01:33:26 GMT  
		Size: 49.3 MB (49278011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9208dbea1384f0435290a314a68b9e6ad71ba2b9dbc0e8e2e4852875066ddf`  
		Last Modified: Thu, 23 Mar 2023 15:58:27 GMT  
		Size: 11.7 MB (11700942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a15d3deea27d74ff209b653b645539f94afc9c3199da23c2809f8d280b1b3f`  
		Last Modified: Thu, 23 Mar 2023 15:58:26 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1e406df43edaf35d7a6bc4cea702f54397cf137a9d3fc0019407820d04ef31`  
		Last Modified: Thu, 23 Mar 2023 15:58:26 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0a7fbeae0fd84e72219aeeee22cdbe3cb20cc7a557f566b2f22aaf19d9b50e`  
		Last Modified: Thu, 23 Mar 2023 15:58:26 GMT  
		Size: 281.8 KB (281820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0ce04cb955ac097770a113bfbf6a31a982f9b257a46d81310f207bbd3e5a1817
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61274170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4968a17a3b7a5e2f272625f4110217f17c95e107be31ca369b7f03707d564374`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:44:48 GMT
ADD file:fc54d0a42f70d91c654d7ac03aa3d437fad192d9f4fd701e214da74c18630636 in / 
# Thu, 23 Mar 2023 00:44:49 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:30:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:30:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:30:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b813e5ae6de73806a605f44184f1b7d14569e88447b46841154803d1dd1eb646`  
		Last Modified: Thu, 23 Mar 2023 00:47:13 GMT  
		Size: 49.3 MB (49328280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a5450317480d94cb3403d7cde2e56b05a48f2729e28a94049e38b55e2c549`  
		Last Modified: Thu, 23 Mar 2023 09:32:07 GMT  
		Size: 11.7 MB (11661617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eedde67f6e600aa9b9a11df48f5d1062eb19dddf30cc6e3692edcaf48930293`  
		Last Modified: Thu, 23 Mar 2023 09:32:05 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed0b4d2410468a43678d43b81648e033fa5a8ddf3a801c9d297f60d0a31d8f2`  
		Last Modified: Thu, 23 Mar 2023 09:32:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd75676c2211f19e7b64fb9984b6e1bf632dcd2caea07507d60c7effb2eb465c`  
		Last Modified: Thu, 23 Mar 2023 09:32:06 GMT  
		Size: 282.3 KB (282259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:e5113fd09171ab576c1d16b344acf0e917e04d98112db25425b0d5728ea300e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62682194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557d46a191412276903630954b271d01ce46d04c01a44e474ff3e6e2c21a8419`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:38:40 GMT
ADD file:0ccdbb7b1f104c23abcf77c506eed771d5759d210c2284a95f85e558405a5390 in / 
# Wed, 01 Mar 2023 01:38:40 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b5ba6d7d02dd42cc6291ae5b4e129956756f664662a78db71f320107a1b6d189`  
		Last Modified: Wed, 01 Mar 2023 01:43:30 GMT  
		Size: 50.3 MB (50273396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95ed42da246160743d4dc3cd48dce0a186520ce89939f62fa3816eea4269790`  
		Last Modified: Wed, 01 Mar 2023 14:04:49 GMT  
		Size: 12.1 MB (12125266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f543db8bb07019add3d3b7dc751cfde9eb3b093bb895d849804ac7dcfd952383`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2778c4d44308786afcaf59829583bb93d4db04bba362c9b4c6759fb0a9602e06`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf4758461e36efc6a403fd95256a5fefc7161101d33b99ae9d6a109a2c2bbbc`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 281.5 KB (281517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
