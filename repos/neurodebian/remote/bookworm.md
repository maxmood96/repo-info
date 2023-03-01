## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:eaa0265ef8a83c7230b132b2d7d6efd363ae31d615303003b3093463cabe3847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:932bb55767f864483dabf659bc1478657d9687caa790b3ec66823985442094b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61221640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaaaea80b89361d286ce1a5f78f241b6db808d8ba562e20e6b71d72e7c1a8150`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:21 GMT
ADD file:74b4e0fbcb9cb38344c32a0512a72d8179f885de4b7bb127215f8d96a6262664 in / 
# Wed, 01 Mar 2023 04:09:22 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:44:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:44:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:44:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9d915a4248d2913bb8451eba978ac348a983990eca9186543367f5f44900e0fb`  
		Last Modified: Wed, 01 Mar 2023 04:13:25 GMT  
		Size: 49.2 MB (49237273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52994b17c4fe57d87d958eb629cb4e4209d0970f24f33d1fc9b7d345b09becc6`  
		Last Modified: Wed, 01 Mar 2023 16:46:41 GMT  
		Size: 11.7 MB (11701029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242b6d88a3f003e541f63f77bbfef90ff8da9913559b8f6936040ce19f1054f6`  
		Last Modified: Wed, 01 Mar 2023 16:46:39 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefe2174f024898bc0d4770401ad4c9b4aea1bae0037db73bd30859bcb386613`  
		Last Modified: Wed, 01 Mar 2023 16:46:39 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af7d6227c840a491568c618da76c10e8e0b3f3d5d4174612c084763b90e8cdf`  
		Last Modified: Wed, 01 Mar 2023 16:46:39 GMT  
		Size: 281.3 KB (281327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:dbc36b82a1cd241cb7bc26f648432524ded15a211d3a43bf21a7afd3e4671dac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61218749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87132c851b3adcb16e0de665de571504e31dd1925102fa584944ff7096acd46a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:13 GMT
ADD file:5b81699b80066f9e3bc967bdf130a67f54ebe15cd80df6c952262d6132b1cabf in / 
# Wed, 01 Mar 2023 02:20:14 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:00:57 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:01:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf639a903cc04a00c81ac77b3b9f9a79644c51b7f515895fd60403c20ff34a80`  
		Last Modified: Wed, 01 Mar 2023 02:23:22 GMT  
		Size: 49.3 MB (49273990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e7d14f29f2eb167ac51f770477e6bb0dc04420d33cf62f394b42808e7a2be5`  
		Last Modified: Wed, 01 Mar 2023 05:02:43 GMT  
		Size: 11.7 MB (11660961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09d88f16d7c91eee89e9b9d217651ece28e60d5d05f92faa251979afebb8b4`  
		Last Modified: Wed, 01 Mar 2023 05:02:42 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a0f8f7c18fdea22fd3298506359948881eaa1e6c6c7190649cdcfbbe622fb`  
		Last Modified: Wed, 01 Mar 2023 05:02:42 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfd5333ecc9ccbfbcabc553008048704eda10d202384c917d7dbd5d1a84cbac`  
		Last Modified: Wed, 01 Mar 2023 05:02:42 GMT  
		Size: 281.8 KB (281784 bytes)  
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
