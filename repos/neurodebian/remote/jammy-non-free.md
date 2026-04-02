## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:392dbeb6af6b687493f63cbc5e1ac017a996efa42b7087014190bdc9ee28d82f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:94ce1db1af85450c8d68a617194541b3ce4701341bd8f5720a7d56aca43c960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33474655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592f6a6e5468c8cd593f014c698ec62fa71c88440f0d5d42793091a5572e2cf8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 Apr 2026 20:15:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 01 Apr 2026 20:15:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:08 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d80b2d6b05311b2bf85ebb53e3a2513e5705d12a9123796d1c6ea60554e651e`  
		Last Modified: Wed, 01 Apr 2026 20:15:14 GMT  
		Size: 3.6 MB (3624576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ea02e1d1ed6638f377e1e099a7b43e52ef2b4298495dae050273e351d29265`  
		Last Modified: Wed, 01 Apr 2026 20:15:14 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf0571466a6f5648b0698f0a4be25f95e6b2505ae70977add87cd1aa6c0733e`  
		Last Modified: Wed, 01 Apr 2026 20:15:14 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78758f11159b40c258ca47ebcc824379dbf5299f8c350a93ee15d41af341bcb5`  
		Last Modified: Wed, 01 Apr 2026 20:15:14 GMT  
		Size: 111.2 KB (111203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58eaec0b4361bb71faec94c13bf7b6ba076efef6e254f966213ffabd6815c3c`  
		Last Modified: Wed, 01 Apr 2026 20:15:15 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:92075526fcd071ad41feb014f0acc16d0a42dde119562cd26d47d86713bba3c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6b55cd81bb43ba395287c451f75717548124cbb1de94496a18b8f0b6cce6c9`

```dockerfile
```

-	Layers:
	-	`sha256:3a39455db87e67b1acb94e008a6bf7932a50406749255cf986e186fdbd987c07`  
		Last Modified: Wed, 01 Apr 2026 20:15:14 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7733d7a85b8661d6ba394101ea5f0a1cec8218b5e283652cd2fddaa756ec7ac`  
		Last Modified: Wed, 01 Apr 2026 20:15:14 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:394de8222acd546223af23904aa1ed27bf129b9229cd1870d371c159048d9a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31325283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51928ab1653f2d374fa511b1c7850b344a4e33a52a58812c7a8ee6ebf75f6a8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:14:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 Apr 2026 20:14:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 01 Apr 2026 20:14:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:14:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4019784363cefaaa0608f44a7c43404f1b49123f5490bd18ff61d334344dcd03`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 3.6 MB (3604713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbac14a880a2f296e4a09554d5f7d84793b55df94e7b4c331567c990b3480470`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7b185bb1d3b8189d1af6df1aeeb5e439b37bb515e3842af0b98424dbe2a5fe`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736213a2d43cf0f24c9174b8fb31963c318bcfb6708f00ace854f394cf5e34f3`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 111.2 KB (111166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a57c1c1d3cafd08cbb99d7170a7ed6f9d171ccb1bebae7ca7ed6a66cb514d61`  
		Last Modified: Wed, 01 Apr 2026 20:14:59 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1c5645de0a996722122f4c9fe0b9ee1feb9f9fa5e235152031b99bd71d3229c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb25718c8f24128797396d2c2b144f786d6ab403adfddb2df3c99adacea0df61`

```dockerfile
```

-	Layers:
	-	`sha256:0957159b9394ba37b209348e8d8a8338cef651a44bbe52536707849659184f84`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8676f87d12d1ed89bca09e6bcafb4093ea3eeaac8b18ba0f5f60591dc4211c78`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json
