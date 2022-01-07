## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:01f5d452c5d8e28d23e74b5b0c4e0c18e201faa2ce913a20fca02e9bdaeba230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:142e894b51240b5be325b851b5f6e8b8f9b8e47370c20d42d471c8c4547e4587
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100679093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680fba8e5201cc27b92b78986f10d0c914df8019acfbf6d0eac5c5ad40803dd2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:06:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:06:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 07 Jan 2022 03:07:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834e0a8674808fa73f8b978050ff284e134ae71d6ec86e10c6ebe9594e21c517`  
		Last Modified: Fri, 07 Jan 2022 03:22:53 GMT  
		Size: 7.8 MB (7770020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6baf4eafe45b6341ad33dd7b43f94a2134e55179f37a1e1bdf4f623ed782149b`  
		Last Modified: Fri, 07 Jan 2022 03:22:52 GMT  
		Size: 3.6 MB (3624052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b1d30ad81f4c85d46556aba8f54ce9b50c36d91e1c8b8307317b097c860947`  
		Last Modified: Fri, 07 Jan 2022 03:23:12 GMT  
		Size: 60.7 MB (60718596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7e270e16145b400d807f9f4195d851d462918140ea12b9cc8dd361fb3a784b28
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89389746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e182ffb9d8f7bcc3e57ff508b29ab5ccae4ccee965d5c56559a9fcd0f08d67`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:26:25 GMT
ADD file:ac83e0dc7e48a0dc1805c0fd7b71b8eb119b3eeafd1fdcab93e11fbc9c0bcda0 in / 
# Fri, 07 Jan 2022 02:26:26 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:55:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:55:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 07 Jan 2022 02:56:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b8080fa0945580f29aa3abed4664f8ab849229eca04510b5d259a9e29616064`  
		Last Modified: Fri, 07 Jan 2022 02:30:39 GMT  
		Size: 24.1 MB (24064434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4f5ac986fb2302307430f337877a74f25cef564b5897896bf51bd24eabb73f`  
		Last Modified: Fri, 07 Jan 2022 03:14:57 GMT  
		Size: 6.8 MB (6764352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366c1fe67b8386773ee8309296879b5c86ada193c48eb3db46a6f624925de904`  
		Last Modified: Fri, 07 Jan 2022 03:14:54 GMT  
		Size: 3.1 MB (3104123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6ff45168046470a19bd0f91947fda960bfa501e5539cb8ba301af57bbd25ea`  
		Last Modified: Fri, 07 Jan 2022 03:15:49 GMT  
		Size: 55.5 MB (55456837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2d752c83f2a95128c285ebb43ceab787d6300df433ad54f70d851a5e9d47219a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (98970174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c21aed8346a147ef6ef4df139432fc2207d35d184a47d81a40ca0b3973534ef`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:45 GMT
ADD file:521a8ada4ac06e6f7720904486d481d216a8c3e08c0c7db1376c39a33e709668 in / 
# Fri, 07 Jan 2022 01:53:45 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:20:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:20:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 07 Jan 2022 02:20:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5f3d23ccb99f6c9462a15efcf35aef0863858073a06d56df671d0e791b26222a`  
		Last Modified: Fri, 07 Jan 2022 01:55:32 GMT  
		Size: 27.2 MB (27171074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc1dd0bcf88f183f6a1d2bb5790ef7a9090213a61ab5a3f3d5d4c2f0c291615`  
		Last Modified: Fri, 07 Jan 2022 02:29:11 GMT  
		Size: 7.6 MB (7635797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628f4089e92df3a2913781cc1ce318758f9239cdbcb27e1b8202f4523c7df34b`  
		Last Modified: Fri, 07 Jan 2022 02:29:10 GMT  
		Size: 3.4 MB (3386743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a33187a7144417d0fbe9b14bddb8bfed2eac5484e79ad04a0617721e387cb`  
		Last Modified: Fri, 07 Jan 2022 02:29:31 GMT  
		Size: 60.8 MB (60776560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2de4312d3d03798ce35b2e238e7b0568c0d068f0134fa1bb7b4d2ff1e8f406d6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115854052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9984e25abeb81a0d0a33c7254c9b7e2bc26eb68d6ad8721b9a3b3311580d10c7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:20:15 GMT
ADD file:014236839eaee978894ae0bd6aecc246177a0a2c11af73f86d9cfafe5478ce18 in / 
# Fri, 07 Jan 2022 02:20:19 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:48:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:48:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 07 Jan 2022 02:50:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6e6dea5a8cc4bdc9e5e51e2bfa948159b69d5fbc2dca99bc41776fb04dab967`  
		Last Modified: Fri, 07 Jan 2022 02:22:43 GMT  
		Size: 33.3 MB (33286892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df240dad3e63f63cb2326c9d04c0532b7c072d07f35ac4b81b9cb83bdeb7d3f5`  
		Last Modified: Fri, 07 Jan 2022 03:10:40 GMT  
		Size: 8.7 MB (8723923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29845154343d23fc50f9d31eaade39c9aa1f43be65b1749f8452d4880c7106fc`  
		Last Modified: Fri, 07 Jan 2022 03:10:39 GMT  
		Size: 4.5 MB (4456010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f312e18112e96d7d273f854686917a36760ed958faba8f1f335bd2c61fb67607`  
		Last Modified: Fri, 07 Jan 2022 03:11:05 GMT  
		Size: 69.4 MB (69387227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b89f8ec02de41c451f5e7c03e2eb174c563894173a916f1864b47912434d4b0c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98094067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205402675a99b86b7d9809f9dfca199f59e8ebd04927ccf0bc7b2d93125521b1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:20 GMT
ADD file:b6119f4fcd6a113749f515278b315ffd96aecce7006f086acb060f981e5c59db in / 
# Fri, 07 Jan 2022 01:42:22 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:03:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:03:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 07 Jan 2022 02:04:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6d200361446626b53394c2a1a520a74a1221795562eac9b318c58e0abe147e23`  
		Last Modified: Fri, 07 Jan 2022 01:44:09 GMT  
		Size: 27.1 MB (27120999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf3df5dddba4efddf54d80d77a6d2c1d39db6b3efc4f5a8db383b10fefff7ad`  
		Last Modified: Fri, 07 Jan 2022 02:12:30 GMT  
		Size: 7.4 MB (7425846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d3dbf32c00380b12c8db08651275503461ad49d1865a45826b9bcb8404e3ed`  
		Last Modified: Fri, 07 Jan 2022 02:12:29 GMT  
		Size: 3.5 MB (3542232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c2fbcab75a340024689323b00f913ef247a8d4a53fc3494d23268de99f128b`  
		Last Modified: Fri, 07 Jan 2022 02:12:46 GMT  
		Size: 60.0 MB (60004990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
