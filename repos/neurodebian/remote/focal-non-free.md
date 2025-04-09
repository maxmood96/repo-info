## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:cb17f55606211baae2fee858087cd83a23fa12652ede76a32c50640baf78a32c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5b5f12c95fa70eba84ed0d9a8cfd320ff1f928e0f4ecc665553188865bc1fdb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32980712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77302996458a5ea42a30e362fe60a32b80399042312ed4461165057feaadc3a7`
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
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09894bd673fc3443fa4aac9c04f3790e80821023e1b647cb36b0dbb3295685a1`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 5.4 MB (5362436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b567f68d429f42a824fdac7d380831ff3ee4e919d2c1f56ac4ba2d5c728dab9`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe211eff3c4623dbc046e34c08495b6c3665295d30178fc8053cd5baff9b469`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd93ed51b316d633e53abd6403ccacb66bf2b80b807810d40df2342572077415`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 105.4 KB (105442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ca65e65a74419b6f595b799268195de974952d7e1558d9a39092265337398f`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:451612c81608c2bebc8d3e36a6a521b28025afe8d027348134cdac02a7ec34d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81e43683e94761e4cae4d1f50b39b3b1ced64f4fb773232eb29f20df0b386bb`

```dockerfile
```

-	Layers:
	-	`sha256:79b4a3ef3b60d9c20c2340237fe4236376a35581ce8f29f76d044ea8920b97d3`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 2.0 MB (2017861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd949e8f808ff83620701f51061d8dc60e04b6e7afc9a968a71e3ed0ef991e1`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f1af2ecb9a21feb330cd347ed15068db050f289105e2bdf3ec7c73f721a67af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31422194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d1dc7b4acf605a88141b16452a82bed6ded61f584d1707889d5ce9f825742d`
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
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
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
	-	`sha256:ae865708d0b42dee9438a375c5a94efff641f15bc2df26488f326dda1626bf73`  
		Last Modified: Tue, 04 Mar 2025 00:47:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5594276a7d675b1211afa73a5e4657d666801fd628a86b3e04ca8a52ebd10688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94d6272d376b63c6522aab8d8e26167f6837ec440e8e0baeb30b5b9dfbd486c`

```dockerfile
```

-	Layers:
	-	`sha256:8eb4f3c5431a7fdd04e4a39d527cc69eaeb72da6950844801223bd43c47882c9`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 2.0 MB (2018032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a6eee93eb123d95d55402c9840f3c21fe2a23eda49d445843b210eb6c751b8c`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json
