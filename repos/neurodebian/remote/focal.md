## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:d884e75d131af5f772fefa7ae90e3007cf03497a413d18b1d8aec12cefe22fc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:ec026f26f90a1da8ffc3ba59281854c0bb1a0b5f166e58e75d57f34e8424bd0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32980385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68aa3d04109e9bf85dbba55e27e2b0055d3c73ba8b1f21907acb2c7bdb223320`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabac9a159eac99d387c3b1a92d15536e78c12f6596c2dbd37f29d0b63d5dffe`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 5.4 MB (5362390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e9f035d7685c2fdb1e905a640424e5ad669ee2970a32cbec7f8d889e3625f1`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb125018a09465c3a7d0200be55fc6435a06fe742fd5a7a7ef39a0fb83cfbf6`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab46b9b7320bd76241047fcf77910ba82992b5e91e204eefe5390b265739db65`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 105.4 KB (105439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ed731be31bff11d448e1a27d734e900b2e674625af668b3f9b87ba45b1a8f3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fb983f465508bd38f2970b20fcfd3052779b73f8d3b436c6ab4ff79915307d`

```dockerfile
```

-	Layers:
	-	`sha256:079d7ce90a22f0bd844b80ccfaee90ce51150b4f1244f3519448f12bf6c83630`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 2.0 MB (2017825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d275b201a8175e6493a6207f8e73ff2b18780007de8ef8e54adc086578431b8d`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7ec68ffd4ce8b557d7733c44da2dd9db37a8c6e708cce9c26d0135f27ca64ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ae7a295cd2085775954ea846d58735c2a3057c2dfa6e35bb89e58df630802e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050735cec161cd8b6805e37dbf6aa92594ddffe88bfeb882c73207404df64f5b`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 5.3 MB (5340554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a24ffd648ad141a6c5f8d0a6bc9e4d061aabfc66f7ac709961fce88b9f48e6`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd527b60b667b0ed5a04bc8072f39d40c36fbf670cb1b84168920c7e61d839`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c37dedc3365ebdd4053270bd242fa8036af553bea745d2c3dfd61f13f37bb4b`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 105.4 KB (105371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:987268df32ff3b51e2b347c001877f974ac1882341fc0edd71564ad452850039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a57ddd25e6a9969d9a4fcd17f9545019ab29817f41c38313d21901602c83467`

```dockerfile
```

-	Layers:
	-	`sha256:b685d760802ecab2a600f9bba4f037b08fe8fe4cdf5c8a83c33074d14c5172e8`  
		Last Modified: Tue, 04 Mar 2025 00:47:41 GMT  
		Size: 2.0 MB (2017996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdd65cf18ae5378746c3c972db14702272c7a9e1b3d6f34ee01f2eb60b52237f`  
		Last Modified: Tue, 04 Mar 2025 00:47:40 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json
