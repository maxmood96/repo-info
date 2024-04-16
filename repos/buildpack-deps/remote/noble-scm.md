## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:aac6c9fd45ed5640f8d6907b6f07cc84af9d7b5f55b757679cbdd9ee4a380a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:noble-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e43c3e34a53dce68d563e649080229cbb53ac55992a35e06c4f23cb2f29a46e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89751495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97da8472260a449f47595b95361c39f80c26a5894437f82fce55171b89b43d8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:22:40 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:22:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:22:42 GMT
ADD file:93f7775e4e5ce50f9e61bbd8f651e279ddd3add435e095c503b909e3da650623 in / 
# Sun, 25 Feb 2024 04:22:42 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80edb1aaf132005ee2bb2f811872efbbbf0cb9b8ec36897c5849798408c7047b`  
		Last Modified: Wed, 06 Mar 2024 04:17:28 GMT  
		Size: 30.6 MB (30551664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6aec9cb3192e03ad86531dfe44b7ee4ba8d368c7d645de6cccf2c8dffd0942`  
		Last Modified: Wed, 06 Mar 2024 04:17:25 GMT  
		Size: 13.5 MB (13455900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8382e640dd0ca6f92e2593a14d2863e9b909da9090d0f355787601b074e7e19c`  
		Last Modified: Wed, 06 Mar 2024 04:17:44 GMT  
		Size: 45.7 MB (45743931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:27735ee07214b2f855072fcd4e72b7ad7424f03fc6e9df5c952927a8fda5a98e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90095073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bdee64687fff39f7a4891dd02e5902accecc0de732d5aee169f276d2af04cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:29:12 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:29:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:29:15 GMT
ADD file:23f3bed4668146daee4397de493e7552ac025df8df189085e9e494a96fa0c387 in / 
# Sun, 25 Feb 2024 04:29:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:04:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:05:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c45e0810ab1c7fc30d716f075d506d33fd67be1ee3c90239200d7ce6b1030bfe`  
		Last Modified: Wed, 06 Mar 2024 03:13:33 GMT  
		Size: 27.7 MB (27731114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20942a9851c4aab23d43b8f866570d29f4316a78b3da8425e34c056c008745c`  
		Last Modified: Wed, 06 Mar 2024 03:13:29 GMT  
		Size: 12.6 MB (12602765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f349b2b4241ab3d83537ee61a9cad53d88310fbb5248f6e04b49a1285e9aba79`  
		Last Modified: Wed, 06 Mar 2024 03:13:51 GMT  
		Size: 49.8 MB (49761194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:257020a2cf4445996e0a6d9e636c95960ae5535fa037c2f4618b9cddd4a5b649
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (88952093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27519f55dbc4b5484ee5cdac3b1b800f530a6d11c3700d462f995d64c53e97e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:17 GMT
ADD file:d70383c2066380d512b8d983092c0ca9faeb5eea2890bca883d43f049d7ae8fc in / 
# Sun, 25 Feb 2024 04:24:17 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:45:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:45:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:29440aefa520893bd718db0f6410e6e526dff0029d9bae385123a40bdfaac005`  
		Last Modified: Wed, 06 Mar 2024 03:52:21 GMT  
		Size: 29.9 MB (29875465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f3d34b3b4ec03b04a5b27194ca3da88544ac3dba2211387389425c0ac8648`  
		Last Modified: Wed, 06 Mar 2024 03:52:18 GMT  
		Size: 13.3 MB (13271020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9974eadb59c4c8a7258a03bdd5d5182c454d60c821a9dd902e3c04eb031390`  
		Last Modified: Wed, 06 Mar 2024 03:52:35 GMT  
		Size: 45.8 MB (45805608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4abfcbfcbd30feb2b4bfa41fc5fd1b18dc1b0e215977949d3c6a6302f99ef900
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102467463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb035723872aeb49e171babb083d8929637be280313d4c03325efabf9a82b98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:08 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:12 GMT
ADD file:4a02618d84dcab4bbb05f776869d999a8c26745e9e74e185ff8cc5dd1adef67a in / 
# Sun, 25 Feb 2024 04:24:12 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:44:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:948c41f680a2c1a00eb8d31747ec9f9bf3450ef13555dd70b044362577b93e63`  
		Last Modified: Wed, 06 Mar 2024 02:55:19 GMT  
		Size: 35.7 MB (35655105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22da2fade9ea6248ac088068db05e59c62ffb846b88d481b80df6a1d935846a`  
		Last Modified: Wed, 06 Mar 2024 02:55:14 GMT  
		Size: 15.8 MB (15759946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6aadf819f0aa05de123e377fd7bdc60300c1a6221aa1b4e955c92679e6771c`  
		Last Modified: Wed, 06 Mar 2024 02:55:46 GMT  
		Size: 51.1 MB (51052412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cca370e5b75191b5b671735358dee69e58ecae7e6391fe5e8338069b83263e41
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92739455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd04339f493296265e48877d859dfdcd6bfd02c3b650d605f46eb0f0e448d0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:07:28 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:07:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:07:31 GMT
ADD file:6aac414b77cc20b9f3f49047a900b0cd7688ca9aafee23883f0221ebccb250f1 in / 
# Sun, 07 Apr 2024 17:07:31 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:32:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:32:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0f8b3814528d1a4f48050c53a434c342d156d2c17e42c4995b43378d312b9a0d`  
		Last Modified: Tue, 16 Apr 2024 01:38:44 GMT  
		Size: 29.7 MB (29730630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7301652c4369a1a4573103c28643b88888a84fa00e1a3d3502ff8a7254d2ba7`  
		Last Modified: Tue, 16 Apr 2024 01:38:41 GMT  
		Size: 15.7 MB (15718546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54a0dcd66d035aac0741bc236991e5f9e83f328a425f1144d663d2d22217020`  
		Last Modified: Tue, 16 Apr 2024 01:38:56 GMT  
		Size: 47.3 MB (47290279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
