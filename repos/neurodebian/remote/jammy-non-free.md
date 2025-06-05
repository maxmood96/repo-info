## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:7481cf83e704b3af7a5b48b3edcdaa6c8359604a90aee37431c2027bc8d9f36a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:106a157335593089bd9167471a43ac4e4a300c21bca0dfac7ab5e8ca330e11b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33270122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c425b94e9e05e94a3588a5ed5fa50798b770c5964ee80eb3108e2c2b854734`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833f05bf4a56287336922533369cb272b043579abea2c4588fb7a28586dccbb7`  
		Last Modified: Tue, 03 Jun 2025 17:31:23 GMT  
		Size: 3.6 MB (3624096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd5f30655f789d9aaabd83e43e19fd42000e70a6d62d06ddf046576bfb3eb56`  
		Last Modified: Tue, 03 Jun 2025 17:31:22 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b76c5daef076a6ef3131ece85a9ede4b5366f8b35563943c61f3ca36393de48`  
		Last Modified: Tue, 03 Jun 2025 17:31:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b346a922dadb495203fa86390fce5ab7f4746b373ff8ee37ae89b1570fab89`  
		Last Modified: Tue, 03 Jun 2025 17:31:24 GMT  
		Size: 110.6 KB (110563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96bb241c37c54f5099c6ee4be792e3df22a12f314a81846062a58b160223e7a`  
		Last Modified: Tue, 03 Jun 2025 17:31:24 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8aae46358cf11c3d67fb2b0bf9adbc7de24122f7bcae1bfe2c595b1a62233e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2096668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14479c1656b173c0100892f3c715ee08d6396fbbddd70f0eb6c7d400c28dc177`

```dockerfile
```

-	Layers:
	-	`sha256:1e817e7f07a5533079454f7b46be380fb1a89f65ee260bfd9d08395ebf6e86fa`  
		Last Modified: Tue, 03 Jun 2025 04:16:58 GMT  
		Size: 2.1 MB (2080462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb30aac33316b47ec98bca470a0a0a66269cdd7aa22f62d98e749d5c5e1c494`  
		Last Modified: Tue, 03 Jun 2025 04:16:58 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5f069651f05d3e6c7a096a41a3242a53b7f5067e15c35b139bc0844d2c622254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31064137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b33835d3e532c457a861b46b17a2ecc210b0019baeec6bf4b85319109ae9d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb392c94ac75bcd9a3d1c9227d1748af1accbe8187fbfc8c5d1775fec406ddf7`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 3.6 MB (3595613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f75ee17aabcbf6b4cb401f1209ba36e9b65a6e79abf95f372b0962049a2f26`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98432ecc9d6cca1469e31ff7f3a6d9ea401d199b788649c06c39bfc96c390eb5`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ff97a05d308956eaaf43302acc738b08bbc3ab11833a62a219be760d787277`  
		Last Modified: Wed, 04 Jun 2025 23:45:32 GMT  
		Size: 110.5 KB (110480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc12a5156209348208485de93d3b89460edf23f23fdded16678f39a46448c25`  
		Last Modified: Tue, 03 Jun 2025 05:19:07 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2fb96a9daec1ce2a7e9ea4dd1144aa633c2bc1d97d73ba0bece51586ec46fc88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2097068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f25ae2c3ba2f40b6fa187203997315827f50c3c023a8f4ce4137f6b8994a5c1`

```dockerfile
```

-	Layers:
	-	`sha256:f8f474f858ffefa2d71ad93a00640e481fbbfd9d23b677cb8ee70750c1123694`  
		Last Modified: Tue, 03 Jun 2025 05:19:07 GMT  
		Size: 2.1 MB (2080722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09220ec00b43fe2a6638b49308e372f11987cceec9eefdf11f6781cec1b7a417`  
		Last Modified: Tue, 03 Jun 2025 05:19:06 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json
