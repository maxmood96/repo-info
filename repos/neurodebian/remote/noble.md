## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:a5fd8dc96fe160273ac4e64b70425043d21e14470b575ef56219f04ee9465cb6
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
$ docker pull neurodebian@sha256:26f1d0d385cf82027ae57ca6cbc7007a4b7d132f1e566b801cf10ef0b8b654a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32535009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e5c00df62c05232c9d7b8871ad1030b19be63813dd9ebea268d3cebb98c513`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:28:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Feb 2026 20:28:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Feb 2026 20:28:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e7316dbfae6dd222c357dbe9aaf868d76b489e30e640acfcaba47a08ce59f8`  
		Last Modified: Tue, 17 Feb 2026 20:28:16 GMT  
		Size: 3.6 MB (3561698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c002f1a335f1daaaae8323887a0027d43c05f691289234494041dddeb6f881c`  
		Last Modified: Tue, 17 Feb 2026 20:28:15 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0bca696156cfbc26d553bdccaff890f742e2574263bc9e690e0e7fe037db8e`  
		Last Modified: Tue, 17 Feb 2026 20:28:16 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5fe069503b5d997eea7278bb6d6abbd559ebd212dde8f92ed45b148e8ccc32`  
		Last Modified: Tue, 17 Feb 2026 20:28:16 GMT  
		Size: 105.3 KB (105282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fc99001a6032175aa166efa18d248a3bea93f690fa1583a07fb020fb7cfe7f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d0306ac76623af51c325f1db6d506acd6949c1371982f48ac01f73b062e363`

```dockerfile
```

-	Layers:
	-	`sha256:65fa0570331e1f52d8fa465a55624af69e8bbb237e319c264eff88046a003138`  
		Last Modified: Tue, 17 Feb 2026 20:28:16 GMT  
		Size: 2.1 MB (2121918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0c48c59d3326fb7774af68595690d0b8af81c6593727fea7df33e08f5360423`  
		Last Modified: Tue, 17 Feb 2026 20:28:16 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json
