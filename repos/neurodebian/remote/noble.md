## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:fb5a9b84f03fe9d8efbf78fc2c9db12a2d059415bc29ecdd2af485a487785c70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:296921b62459bbac430852b26c6692166bf8fef8beb858a744d9441179b88132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33399547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9708e34821c47d5e629074d5310da922ae19b1b7f15249ae4d5f673ed2c0fce0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Feb 2026 20:29:06 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Feb 2026 20:29:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb34238297f5b8613b7d370930a7b034d568524ce9adfe07ee07f974b3e6b08`  
		Last Modified: Tue, 17 Feb 2026 20:29:20 GMT  
		Size: 3.6 MB (3564556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead13ec2ade6c1e6e97c47486d1404d84726c50f5d1fcfd9023b7f8ded07476f`  
		Last Modified: Tue, 17 Feb 2026 20:29:20 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccf2a267f02e5b4325edcf3ddf6b0a5f63f74f1cf2ac070660addfbd727a61d`  
		Last Modified: Tue, 17 Feb 2026 20:29:20 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77327192069226ab34e24f4ac7854786228abd92c76922782a6a94d7fb395267`  
		Last Modified: Tue, 17 Feb 2026 20:29:21 GMT  
		Size: 104.5 KB (104468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aa38f5270a4a80ed6c0a3d4138d793f0e5c15737218363953f0c7f6704aecf40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc8bef4d278616f49e0ed02c234adb961cdaca47a4036602bc5794d8350e349`

```dockerfile
```

-	Layers:
	-	`sha256:840f89ef6247a578e0f987d63a118ca4c7277eaab4841eded94714cb4c6b05c9`  
		Last Modified: Tue, 17 Feb 2026 20:29:20 GMT  
		Size: 2.1 MB (2120873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30886ab36b6744f136e3bfd9f1ddd62e28adf8049e4798d56dc2527c8bd44b3`  
		Last Modified: Tue, 17 Feb 2026 20:29:20 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f245aafa6ac8f69e6188bebb3508fdad80fbdd1fb625fd621adb8a081b73a203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32539513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c56ee68d80089c3f0925d8e58f1aadbf3c27908dd7512fc85c2c23e22163e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:45:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:45:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:45:26 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:45:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533c5edf582f6c749ef6a1c980c83140c19790fba01e023270d953596d6728eb`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 3.6 MB (3561698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e00b53b8e4686217ad4464335977ad206a0b44b2c815209a57b92579deb2c3`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4150071e6c680a3e30636e054b5eb864727fe3c9b6bc8e4e894a63bb147d2e8`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf622f6ce748df581fde435236c4025fce1294e846eb31a4c2bb114ad60de5e`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 105.2 KB (105195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:345880f970f78bca78609af939641e1ee75bb8f43c66a887fa2d8ee357bf4356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33261a958005f1391a059daad1bcaac28d5b8b86b44eabd34be6e413a13c46d1`

```dockerfile
```

-	Layers:
	-	`sha256:4bcad4951b4567ba4ce52d8f30dd9930b9a357da1219bb3fbdc23e3ae7caab35`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 2.1 MB (2121934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506182a496a21e1b4cab38177081115a703e24a5ca3745eda65191d95f3a7545`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json
