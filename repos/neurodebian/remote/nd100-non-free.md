## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:d5c8df09d1a6dd4914125eb9673a1f36809dd1aa4e6604538420c4890c57ed6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:90af1451f53e1c6742109e4d54dbad70fc89cdb8adb6ef0abdc245c335bb66ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61259749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0a64f9a25c419b96996656c710c481d3a87486d7fa0118a379379009f8e88f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:38 GMT
ADD file:f5e6e6cbfbb36f50f49f06fbac953a130383acb67a1c5e9979441f1915b1077d in / 
# Thu, 23 Mar 2023 01:30:38 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:56:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:56:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:56:25 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:56:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:56:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:4e2befb7f5d18aa27b3619ddf1b93607e62ca82d0c627557537c149893346d86`  
		Last Modified: Thu, 23 Mar 2023 01:34:40 GMT  
		Size: 50.4 MB (50448639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b178d3e9f240e77488752e765509042c03f2bc17a3eab0e5f5a62b7b67c966`  
		Last Modified: Thu, 23 Mar 2023 15:57:49 GMT  
		Size: 10.5 MB (10504479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80f9a76e2eac0f9a3dc42a01f95d1c280aa08207634cb8df83dd30a27f97959`  
		Last Modified: Thu, 23 Mar 2023 15:57:48 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3d9d3002cfeef01f97b0d184b0e841bfdf021850df4b0f6a88c2861c3bab41`  
		Last Modified: Thu, 23 Mar 2023 15:57:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19bb407c9c70c6a8f88ceebbd19e3dde631a527d767bd8d13445707f3ab191f`  
		Last Modified: Thu, 23 Mar 2023 15:57:48 GMT  
		Size: 304.3 KB (304269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e1b98b76491914cf926697dac13d6b087f7d6d5abac8dc4e43f32f2361f611`  
		Last Modified: Thu, 23 Mar 2023 15:57:57 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:707b6b7ee753feff9c0e77fd533fbed40ad0de825780d2e8b0882c058f587dcf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60056690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b48cfaa3525f6d38ee12012c95842484629f74e01fb847be0310142622e9698`
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
# Thu, 23 Mar 2023 09:30:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
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
	-	`sha256:e3932c847bad7a644ef61688a39fe7e6985622bfae24224db72ebfbe22916aab`  
		Last Modified: Thu, 23 Mar 2023 09:31:40 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e3317c07eda65fb456e1fb7372dcf45379845b3fabd59aaf6cb390fabed893fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62382364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf32adb5752d709797e0414a4d9b854663dcd211fd8f990390d1a6356b2cbd7b`
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
# Wed, 01 Mar 2023 14:02:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
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
	-	`sha256:f6a7ebbf20b05aa1bc459f99a4e5299be2866f5a1f1c10119f96e417677ce6f9`  
		Last Modified: Wed, 01 Mar 2023 14:04:12 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
