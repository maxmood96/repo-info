## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:658b81fc7b6abab8f6c7ec216a34eedec275c523b628a5597c9bce280567e964
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:dff773b7560d263c582e2b4a10cb710f42a1c3c52c64ea8a04817cd0308c762a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33414437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97e0f663f97c61d8d3b77245c102959f22f0cdb0c658b0f8a911affbc6c77e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bb8d306692844672bbfa1d36b12ac9e70dcba3afed1b205da716bd98445dfd`  
		Last Modified: Tue, 03 Dec 2024 02:31:15 GMT  
		Size: 3.6 MB (3558848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060c4cfbe42dcf01c60754dde056484b11eb0bf692306f5b6e056073296c5dbd`  
		Last Modified: Tue, 03 Dec 2024 02:31:15 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10363b67b7c7df5a7f19aeb132cc2e1c148a4850360cbfea065de604e7e84689`  
		Last Modified: Tue, 03 Dec 2024 02:31:15 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148844dcd0fea449935fdfbce9218162d22b312bdf46e3e6b3944aacbf3d4402`  
		Last Modified: Tue, 03 Dec 2024 02:31:15 GMT  
		Size: 101.6 KB (101627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0dd7607b772e7d3e7a9f3c08dcd17fe3fd5d72058d713f657cae66f6cd6c0b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2000857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6499b40b283bd5ef8afc18820da824ee815169303bba4e1cef554e42997c6f27`

```dockerfile
```

-	Layers:
	-	`sha256:912e8b547af7012c23de9e51dad8c0b49a0297f34835163f0a7c0c466ac833f6`  
		Last Modified: Tue, 03 Dec 2024 02:31:15 GMT  
		Size: 2.0 MB (1987197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50eac1b2f08d5d06cf4f78d38044ff517d06861bd698f3072184621c47feb780`  
		Last Modified: Tue, 03 Dec 2024 02:31:15 GMT  
		Size: 13.7 KB (13660 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d64f68ae17f5144e471f9a21a1cda36c1b06ec1f9b28334d51b36756f721afc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40fc3afe6374d9c363c91f2623c230a34460eefc40c745d48d530be8be422f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c806577d234470cc5e1375c6c84e7102c2e92ed2f155ce9a119a4b67e98f9e3`  
		Last Modified: Tue, 03 Dec 2024 06:15:50 GMT  
		Size: 3.6 MB (3557863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5dc9f05589119104912fa1a1717ff92659e13dab1440dc6b266b58957e5ee8`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc2614b4bbf71177097aa4d12c46d11d7578598e10aa3592123e9463cdfb0e7`  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2df2b4e0bcd2792b731ac676570a2eeed647f45c932ddece55a8243a41bca9`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 102.2 KB (102155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fadec3f89a7e65d06897f8d31756c5c2b70d389671fc741c2ccb854732c6950a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2002026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b683ca6c0f1e2df2c80bea9c23df15d7ead46960c997d86d5ecde29072f03e7a`

```dockerfile
```

-	Layers:
	-	`sha256:8f17c09c31cf4b5cd87bde14628854326c2007d643625d168d5ed82a41251647`  
		Last Modified: Tue, 03 Dec 2024 06:15:50 GMT  
		Size: 2.0 MB (1988242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebc91794bcf6ed620350bcd79c932cb607a78ee37e21fb3a7ac0cc318172128e`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 13.8 KB (13784 bytes)  
		MIME: application/vnd.in-toto+json
