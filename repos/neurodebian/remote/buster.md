## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:1a0f5f5f807a4990f199da7ac7175f2f45b471743f2a87dd902d0aa140f7ca36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:bbddc17c272867a26b7feed992e6ecbff77530ab31f1ccf164387e2e011713eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61259912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83519bdaca7698b3e1ac7c03a156250b231ffd570ab3b8b38b0c735167658d1d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:09 GMT
ADD file:9ea7d74fdfdb29946ab72e1aea5810331debe27db7e50a0fc4e0d5a192ab6166 in / 
# Wed, 01 Mar 2023 04:10:10 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:44:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:44:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:44:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d8a6bce2a40cb0c3e3cc6646bfeccfb2ac5b303c39ea70d67e30406d270f2009`  
		Last Modified: Wed, 01 Mar 2023 04:14:42 GMT  
		Size: 50.4 MB (50449101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f612b2f2d9c74944c483a61ee943e6a24b2007abb878645afa5615ecc0df4c2`  
		Last Modified: Wed, 01 Mar 2023 16:46:00 GMT  
		Size: 10.5 MB (10504458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22335a31d3b76cdfa76c4395a76ff316493877e2615246522b95b9d6a9e354f`  
		Last Modified: Wed, 01 Mar 2023 16:45:58 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f271e3ec83792f994560a4c28bca958e6e8a218dbafde7ca87a9ecab9d5a8f51`  
		Last Modified: Wed, 01 Mar 2023 16:45:58 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f740ee30f013b293d5925c48e7a80c75a12a7aa8347301b39ce884e8f2c3203d`  
		Last Modified: Wed, 01 Mar 2023 16:45:59 GMT  
		Size: 304.3 KB (304342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b32bcd4cafaf47cf6c24e67da7b40242813e58d933b86dc54759c6084f759505
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60056334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5526c79bfe19500886e549b52f3ec14113f2dd8a20a0dc87f2f627d67413642`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:16 GMT
ADD file:35dd833b036748f887e8224e9c5f09846aa5d1d6e1798d12a6355c28e0a087d3 in / 
# Thu, 23 Mar 2023 00:45:16 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:30:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:30:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:30:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a9fffb8d1cb480140dc56a24c58a5d1a284109cd8a640a3719bcda5963d1298`  
		Last Modified: Thu, 23 Mar 2023 00:48:25 GMT  
		Size: 49.2 MB (49239721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23969bd0deb154819623454501293274ed5d84a2980ddfab4a06aa292e2a8c2`  
		Last Modified: Thu, 23 Mar 2023 09:31:32 GMT  
		Size: 10.5 MB (10510313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbd5727c34bbfbac27263abe66d340203b862be36b5956a8a7a1be2e808287f`  
		Last Modified: Thu, 23 Mar 2023 09:31:31 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9105f78f42f3a9a4b9f358a6913d438e595c68c00a3ca058316341700981f2`  
		Last Modified: Thu, 23 Mar 2023 09:31:31 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e54dd992daca6739d936bec0393525b37f84ce18f86441110e7748352193d7`  
		Last Modified: Thu, 23 Mar 2023 09:31:31 GMT  
		Size: 304.3 KB (304287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; 386

```console
$ docker pull neurodebian@sha256:96124b0d939cd9453d1f5bd48eaf28f9604b813af5f93a0ee05a6e5e9843f7c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62382006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513b02edc7b5e1bfa4491c5259504ada968aaf72d7088609818f6f63a6d4e73c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:23 GMT
ADD file:4a87d706ba1c6cdeab729abca0c932709611862dfdf5d46d9f07660a549fd043 in / 
# Wed, 01 Mar 2023 01:39:24 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:01:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:01:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:01:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:01:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:965c7d391035444250e8549e1aa77d80a0692089e844b5c3d6f4e4924f096a99`  
		Last Modified: Wed, 01 Mar 2023 01:45:08 GMT  
		Size: 51.2 MB (51207396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da67baad9b0f9e7bc5adc526954637e4319038c09fb5b88d95602ebb082643f2`  
		Last Modified: Wed, 01 Mar 2023 14:04:03 GMT  
		Size: 10.9 MB (10868322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77d9fb5f6e1a0497e5e5bce467eda0a0f642506ee3d02e91fb20ecaf850021e`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94f20e5d63d935ba225224f7bd32c62b1fde78f1360d8abba264bb6931fd478`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1207f0083a5fba06d163124bc9a5637daf92d4d3bdfc83385a36dce0e78244`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 304.3 KB (304281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
