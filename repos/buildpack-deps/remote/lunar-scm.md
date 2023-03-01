## `buildpack-deps:lunar-scm`

```console
$ docker pull buildpack-deps@sha256:606403063d0774c59bdfdf8cec41792762059428f2335758b767a8a6419d131e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:lunar-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f4779bb631cc96f8c601cb3cb2d4d19fc819689d534b0ec2049fb2aeb96b7e49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78694034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90cccf588560d124231ebdcf5f275b4e27dbb214d9bf110989c70b375d2885f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:15:52 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:15:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:15:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:15:52 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:15:54 GMT
ADD file:915f1a27db0a8b9a9dd58d40086cb7d45b2722e8ceb29ed8bcb306d4dcd3688e in / 
# Sat, 28 Jan 2023 05:15:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 18:11:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 18:12:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Feb 2023 18:13:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7610e15a5bf822d71b65f5f7c7d873b70f585cebc9b4bfd76dedd61997f9e1c2`  
		Last Modified: Wed, 01 Feb 2023 18:23:55 GMT  
		Size: 27.4 MB (27419700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc4589b98247ebd93b0b4ca6c08ebf74c1fcb7fe81d1ee3a00ddd0381b99aaa`  
		Last Modified: Wed, 01 Feb 2023 18:23:52 GMT  
		Size: 6.6 MB (6635143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c87abeb95cddddf017930e8ffec58593bd520216c779b25e710376682a56c6`  
		Last Modified: Wed, 01 Feb 2023 18:23:52 GMT  
		Size: 3.7 MB (3690296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540b97131389bee769ba93a32a51aee8b1f6fa2936b506cd9be1296fe2e9ef3d`  
		Last Modified: Wed, 01 Feb 2023 18:24:10 GMT  
		Size: 40.9 MB (40948895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:049d82e7a50c297020943bab44d6ae17ffc80d524d72a34544bdffde74443213
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83349017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbaabfc7bbbedab1780b20eaee19155a1c5b9ebf58df1fc9f4f1df55b732b84e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:11:25 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:11:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:11:31 GMT
ADD file:c0ac354f01ba9deb72bda06f4368650e0cc3ad5c3425ce0eb452561b56a1734a in / 
# Sat, 28 Jan 2023 05:11:32 GMT
CMD ["/bin/bash"]
# Wed, 01 Mar 2023 03:01:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 03:01:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 03:02:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2cf733a376b355703d852c37fb66314a9d27adeb140641f229bd7d5b089c8ef7`  
		Last Modified: Sat, 28 Jan 2023 05:21:37 GMT  
		Size: 25.1 MB (25086001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8391c317b70a65f7c7d5bf15686f27d06e2c79b286c3a86cb70987de2acdc4`  
		Last Modified: Wed, 01 Mar 2023 03:16:32 GMT  
		Size: 5.8 MB (5808831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd77c8b93dd4f4c7b1af018a1de3fc89606fac50a049b8ee85bd1ccd0335294`  
		Last Modified: Wed, 01 Mar 2023 03:16:32 GMT  
		Size: 3.9 MB (3851906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9367c233564b3534a29ad60c3843f0bbd6a4105cc65519f48f91cf119358142`  
		Last Modified: Wed, 01 Mar 2023 03:16:51 GMT  
		Size: 48.6 MB (48602279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:42463b1fa0a388d9801a062d9dd40ea8d72b288e886e5dd7ace63d7c8e99274a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77627268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d5f1d5f2a4e64bbe95c49ca9314c9030fdcc07106445d0f6c7fa7d59d897a6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:11:24 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:11:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:11:29 GMT
ADD file:c6e9b4142d0eef696dbc592460bdbd505f41a98d02ba1c7a84caedbb5f84ea1b in / 
# Sat, 28 Jan 2023 05:11:29 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 18:09:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 18:10:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Feb 2023 18:10:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:86b4004853063d73760cb92de14cb3a62665a38c8761227cbb1afdd83e3c2463`  
		Last Modified: Wed, 01 Feb 2023 18:16:40 GMT  
		Size: 26.8 MB (26755970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf667a5a78f05803b7cfc5334c39586cc72c5e9f5c4b3d057eeaeae60adab9`  
		Last Modified: Wed, 01 Feb 2023 18:16:38 GMT  
		Size: 6.5 MB (6468704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418f5bbd1102042fd3e0960b145074562a58c2191adc81cbc46fe1f667ee5e5c`  
		Last Modified: Wed, 01 Feb 2023 18:16:38 GMT  
		Size: 3.6 MB (3649392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07c999a4e8e593fbc5591306b84b879ccd3dede542421a341ded4ce652345c0`  
		Last Modified: Wed, 01 Feb 2023 18:16:53 GMT  
		Size: 40.8 MB (40753202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a805a109b7caa13d3e7983ef1c11492c18454c10000ddc6c90fc09528e3427ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89714899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76476df3dde3cb0032f781c70db091e82cc22df5fee40845b4036edc34bda10d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:09:15 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:09:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:09:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:09:16 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:09:19 GMT
ADD file:1c6ae50eb1e182a9aa8f750f61a615d5b3578b7c2f94e58678359bf1f43d3780 in / 
# Sat, 28 Jan 2023 05:09:19 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 18:11:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 18:11:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Feb 2023 18:12:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a5151cf1d3445f8b719163cb88c8ee7f7f2368e309dd1d14016546804fc05126`  
		Last Modified: Wed, 01 Feb 2023 18:22:34 GMT  
		Size: 32.0 MB (31980199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d337c3408ba6fc96792e39145bb0a122a3f04a96a5571d97c3f265402359009c`  
		Last Modified: Wed, 01 Feb 2023 18:22:28 GMT  
		Size: 7.6 MB (7605406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1579dbb09dc76707e4839919fcec93b48be4479e103cb1aeed1a50194d1724e8`  
		Last Modified: Wed, 01 Feb 2023 18:22:27 GMT  
		Size: 4.4 MB (4408979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f651ad714aac8d2542de9fc23ff6b10701efb943ac6c9538ea45be37d726bf0e`  
		Last Modified: Wed, 01 Feb 2023 18:22:57 GMT  
		Size: 45.7 MB (45720315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:288d9bb7ed13a2a668f51e523fa6f73bb6cd8611fb7903414940a9b02618f78d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76738358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5814b74a158bb3239700bd17ecef82d37a7e245364d85b0f074b6e447ba0d37a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:10:10 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:10:10 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:10:12 GMT
ADD file:b85f8b675931991dc4361ad29563c508e8cdd381491f1da64b998d7742f72c42 in / 
# Sat, 28 Jan 2023 05:10:12 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 18:15:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 18:15:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Feb 2023 18:16:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ec11bba63863786b2862fe78b2d89ce7f2cf2ab178c9abc17064e250fc6a07b`  
		Last Modified: Wed, 01 Feb 2023 18:22:06 GMT  
		Size: 26.0 MB (26014630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50701e4538cb519cc258f9f917c69bd16c143f281ac369a90c6aba3f40dcff3`  
		Last Modified: Wed, 01 Feb 2023 18:22:04 GMT  
		Size: 6.3 MB (6318048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c474c2328ae2c175dbac9c35c888383f82da2ae100c9197db0e3a1912be9dd3e`  
		Last Modified: Wed, 01 Feb 2023 18:22:03 GMT  
		Size: 3.7 MB (3674786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eabce57ad05a030ae2bc38b37ffdb539eef43109d4503a2b66e82f71391c9bb`  
		Last Modified: Wed, 01 Feb 2023 18:22:20 GMT  
		Size: 40.7 MB (40730894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
