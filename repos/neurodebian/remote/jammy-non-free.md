## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:97f3c220574924fe964fa06d61fc892692bb1a6b009a039df7d5e66c78d35239
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2623a7c28522a7b25eb3fe44172632fc2b1c20a3ac1433aac85570c3d5a894af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69650e35f150a56a819ebf3c57f2723e3327461a3975bd8a64633add1bb9b27d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c600cd6d952702399348890ccb963cad1adb5d6098ffb092caec1a36545b59`  
		Last Modified: Tue, 02 Jul 2024 03:19:22 GMT  
		Size: 3.6 MB (3622723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ba852eb2127a816ea9594d23647541e8598c273234f40d074e70f717f2b363`  
		Last Modified: Tue, 02 Jul 2024 03:19:21 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb0f24912426a9bcca1a5e3ee9b310973b13df995b7565182f492ab021df7e2`  
		Last Modified: Tue, 02 Jul 2024 03:19:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263c87d1b026352611e6b8267a292c541a135e3842177e774f5f9d5b91f64ef5`  
		Last Modified: Tue, 02 Jul 2024 03:19:22 GMT  
		Size: 110.1 KB (110118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8772a37561b5fd83f6ab10e0506ed41d8922a4fd314dce23f19451b55a5d37ea`  
		Last Modified: Tue, 02 Jul 2024 03:19:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5dd1b06de41553a1c77638c8b54f222974b849d784be607edd211468735b0c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612275f45e18d0d569032ec2fc8952576023e24a60c792c2616ffa5aad12d4f1`

```dockerfile
```

-	Layers:
	-	`sha256:3447301f1f169b1f3acdd1f023f78fe04e8dd87a9de8dc89f3ef9b82fc18a35a`  
		Last Modified: Tue, 02 Jul 2024 03:19:21 GMT  
		Size: 2.0 MB (2015695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7244937c2399932fdc4026b34ea0785d361e1562807e9a3c5a205419dd4a72a`  
		Last Modified: Tue, 02 Jul 2024 03:19:21 GMT  
		Size: 15.6 KB (15635 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1933b2f19205647fc57be0a0ce1f60390d0ca130346609824d899c010635ee7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31066708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d41beebcdb80261bc322b441a2586ca83ceb3ebba450083e4795434e7bc28c5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dc16b23ee00d53f4adf324698b87c709e486e05c5b634739181bbce1d56c82`  
		Last Modified: Tue, 02 Jul 2024 15:59:21 GMT  
		Size: 3.6 MB (3594186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f31c419c5921eb500e6bb4d1394cbc4cce89c991aa6ea0cb14769a2e4ceff8b`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e4d5b48676456aba5e60bf7d682a9253b4301c3e43347c5f6b707ffe70669e`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81d807b10b523db43ea06a66dc581da167eaaa97bc25dc203e08be033b9c646`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 110.2 KB (110240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ad070ba592bf4d760b4956a98ae70ec4651c7f5db0f4e2aabf5ac2bfe3b2c1`  
		Last Modified: Tue, 02 Jul 2024 15:59:38 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:13f5ac4a8e9c0cef26a3377cc0f187b30ff2d40b24c8960944ec77b804232628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2acc579da0541db5b1806051198453ff0806569e736508bcf7c0c8876c064c5`

```dockerfile
```

-	Layers:
	-	`sha256:4fea70f73d3b08b467c57896ed29255771bb9295dba7ed13d1e55b6054cfb260`  
		Last Modified: Tue, 02 Jul 2024 15:59:38 GMT  
		Size: 2.0 MB (2015954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b174930aea8ca924db6c39b0b1980d1d11b0b31e5eb7814b33f219112f583424`  
		Last Modified: Tue, 02 Jul 2024 15:59:38 GMT  
		Size: 15.9 KB (15913 bytes)  
		MIME: application/vnd.in-toto+json
