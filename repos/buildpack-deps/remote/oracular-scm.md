## `buildpack-deps:oracular-scm`

```console
$ docker pull buildpack-deps@sha256:400675c9f31f95df51dc1a53754e64c451d52626a17e58e141e8b47a9587a842
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:oracular-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2e1a10606d94d1341f4291bfe145a175659c824965e8fd3865cf838d843ce4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92385945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0113271dcab80bce9700ced13a5585c0c989e1b56647edc2486bdbf7e270ae92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:c6c1fcc53cf2d3beb705eee292dd1e6ef2980e7f6221cba9d5c4081038760fc1 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:372111cb3b6e75bbceae9a3a6c2d060e2fb7b2573e9ff6e1931f6de2798246c4`  
		Last Modified: Wed, 09 Oct 2024 16:53:13 GMT  
		Size: 30.6 MB (30600773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a944d883315edf8742919f6ef5b3c26a8ad272f5008425c60a2142fb1f5df853`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 15.4 MB (15357098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d878515a2f78c562568bfe3981dd590eda252ccb805e73b9e3bb9f4485eee6`  
		Last Modified: Sat, 19 Oct 2024 02:52:39 GMT  
		Size: 46.4 MB (46428074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1e3606b1ecf3ff7025ba8e1ea5e42df37408b840635cb63b334f037e41989f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10503c61c856cf28d7a99d4c07c844f5c8055fc334e6a3789c4c5d7d52bcbf1`

```dockerfile
```

-	Layers:
	-	`sha256:78722da52930ac15ebf0a6bcfd0e1fe261a2746c127f81b162b628725a8bdabc`  
		Last Modified: Sat, 19 Oct 2024 02:52:38 GMT  
		Size: 5.1 MB (5090433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ebf53812943cf5a8aa3587eeb1d7aa692dfc6b67872b34031c7959d49e6fbd2`  
		Last Modified: Sat, 19 Oct 2024 02:52:37 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a3b8436385f7e5f61c631de58b96267ca63424b7a1f2edddd2d8ade83de6b753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (90993709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b52a03a0d1525d7c051d4c6bd661df3d4d7fee021c5a779c43e15834a45a7a9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:8e23d3c59f96fb90ac280b31339b3cdff6ade1865ca64b22d81f85a66b3808c2 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c481ad0a3e91be308525ddb3271f2aa7bc25d4f2a1241c1e05f6552ebecd91b1`  
		Last Modified: Wed, 09 Oct 2024 16:53:25 GMT  
		Size: 27.5 MB (27546645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a20a0e501d15d9e4692975ca8c07ba367bbaed9ea09bf0a9d8382aca8abe0a4`  
		Last Modified: Sat, 19 Oct 2024 06:47:28 GMT  
		Size: 14.0 MB (14044586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804a8684eb96a4656dd0e6aee99ef9f42b140a0e1e97b15155ef8a8e3d346151`  
		Last Modified: Sat, 19 Oct 2024 08:21:23 GMT  
		Size: 49.4 MB (49402478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d103e4ed295a6a17ce4ca2aaf307617dc876868f98530c47d5092cf36e24df7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5099116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f11a591fe13fa3511e7c434069e50379f13bca29a10d3e0fe37f00752ec2444`

```dockerfile
```

-	Layers:
	-	`sha256:41a132977d310714ddf9c74d7d7f6bb0c0fc8fc8d203c5ee774807bde513510e`  
		Last Modified: Sat, 19 Oct 2024 08:21:21 GMT  
		Size: 5.1 MB (5091733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93f60af3718c85df129bbd180f5861a4d382da0308f6619ba9d48d10963992d1`  
		Last Modified: Sat, 19 Oct 2024 08:21:21 GMT  
		Size: 7.4 KB (7383 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bdc102418f7661b306dba7cd1da9a44bf88dace880f30af2f9c99b3a14a70b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91745942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4ce0d24b5556cec948c7c2fef72f177b0aea727b2a74df8bfc0697e3acf7df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:897556c1de01d47a95fb4d7011c66a17502f56fb3838b2231407a26c3ec19779 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e311dff5272f98c3a90f3b733cf3131b33de66a713a49c4dc345811451dabaf7`  
		Last Modified: Wed, 09 Oct 2024 16:53:19 GMT  
		Size: 30.3 MB (30284490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d09b70567f67458b69e57931b7ba0045a67a5ea93d03cd34ced355035e4ddb4`  
		Last Modified: Sat, 19 Oct 2024 05:24:26 GMT  
		Size: 15.1 MB (15130151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69ca0bd1e67582a527f0561d210442a28387165346cd80417b469dfff4c9547`  
		Last Modified: Sat, 19 Oct 2024 06:28:24 GMT  
		Size: 46.3 MB (46331301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ab39cbabd5fe378c4643b80257a53677158249d426e7dd238dafa3b47e2c23c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5105038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59aa480168513e7b6e1132c5fce9ca710815717ec675bb7f7683906de832e0ad`

```dockerfile
```

-	Layers:
	-	`sha256:3fe20449803338205830ae7041a7b5f211304706c435c32c2b2d96c4343ef0ba`  
		Last Modified: Sat, 19 Oct 2024 06:28:19 GMT  
		Size: 5.1 MB (5097634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:186178c3e379c352c1f9be0efb33fe165a2c5b8523674617e0abe790219eda5a`  
		Last Modified: Sat, 19 Oct 2024 06:28:19 GMT  
		Size: 7.4 KB (7404 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0ac0c11864cbe79f5d7936b1647a570a0f2ba6cd664790f20cfc6f15b37608bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (103968082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a3610d9b7eaf58f24c59c9906fb1fdcf0a7a86990394f21a175fad79451913`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:1f33027337aeb38d1fecb5ee33f2c55c6bd442e269ee902f5364ec863e957998 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fc0886b1c0801753f6a7a5ef62947406857faa2987b1df5781427e2c559ea218`  
		Last Modified: Wed, 09 Oct 2024 16:53:31 GMT  
		Size: 35.1 MB (35062896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c073ca505f4363ebfcb898f4d2a8b23427ba6069a5fb5b06cc80cb0df05291`  
		Last Modified: Sat, 19 Oct 2024 04:15:45 GMT  
		Size: 17.2 MB (17233776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce660df8e8e7bcaf60343fbb14080cb0995f3ab4cdfa5765f101525c99d3070`  
		Last Modified: Sat, 19 Oct 2024 05:32:02 GMT  
		Size: 51.7 MB (51671410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e02463caf7de9f88f37613d8aa094b11341b4cf12a34e9c0cb5027b0a9154cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5105493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235e9b4dcf3d3b82a5b8a27770b6a8e1a16ee59f6f386771ef017a1d1f0d09b7`

```dockerfile
```

-	Layers:
	-	`sha256:18870027b00c8c1377dd93c6eae92bb606dbca04aeab0de9c5fcd1072358b90d`  
		Last Modified: Sat, 19 Oct 2024 05:32:01 GMT  
		Size: 5.1 MB (5098137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:644e927eea334c580d389006aa4b50d25abb00af7db86adaccf02768e08bb128`  
		Last Modified: Sat, 19 Oct 2024 05:32:00 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:7dcd4c9c250173f5241136de13c5d76c68cb13aea4202921dea27c75ff1bec55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102189461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45f5a29ff8520f0558ca8e6608ba4ed24e3bf003240379dc112d01b77636ca0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:9744fb771a3525b1ecc8bb8c4ca623db4381f3fa78cd865afd2dc853a7ec0106 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c4c3b7ce35ec01feb67389e9cc9ac164fd53001e09b63553078d8d1e6ad0c713`  
		Last Modified: Wed, 09 Oct 2024 16:53:37 GMT  
		Size: 31.8 MB (31787862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe51613addcb9aebac5d02d07ded0ea6c171908f331d835d7c75b1cebb4be19`  
		Last Modified: Sat, 19 Oct 2024 04:11:36 GMT  
		Size: 15.9 MB (15873939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fb3831c114a36b0b2c3c75c497b9581ec083768d0aa69432339a049abe6101`  
		Last Modified: Sat, 19 Oct 2024 05:47:19 GMT  
		Size: 54.5 MB (54527660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d9075d5353086f9f8f1d5ad1a4b08c86a8a2c42556bffdbed753c0d64f0af4fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5088341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eba17dc0ec912cb2bacd4d472b7bddedb156b6ade5d5d3950856afc4543f185`

```dockerfile
```

-	Layers:
	-	`sha256:a64d8c8fd891c47bfc45a5d57836ddd52829df56f468a9fa971eb9937cffe786`  
		Last Modified: Sat, 19 Oct 2024 05:47:12 GMT  
		Size: 5.1 MB (5080985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c8e227a3bf93254df4fb125746e67c01e90854fe7dba6b678862e2db84837cf`  
		Last Modified: Sat, 19 Oct 2024 05:47:11 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a3ac7dc97eb63d9013a092f3db71cfad7e4540dbe0e97a8b436c75e9add963f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95437293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a958ada935a3b94f4f9b08c16d40617d4a578b02c03f0bb7608f066c501304`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:e8f85fdb92ac3e5e436757449ac2447ad1520aad2682c8e0077efcce841566a1 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:303831814b37c8b218003169a08ba9ba85ed2a888e73d505841b5db92ec79efa`  
		Last Modified: Wed, 09 Oct 2024 16:53:43 GMT  
		Size: 30.8 MB (30774664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e574d553080236f570c1f83ee295b636102f93cefde1b709e84380c22d451f3f`  
		Last Modified: Sat, 19 Oct 2024 03:53:04 GMT  
		Size: 16.9 MB (16920088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e923714151c14f08933fe23d1283ee8fe44eabf4047feae2eb487e323f6a4b75`  
		Last Modified: Sat, 19 Oct 2024 05:14:35 GMT  
		Size: 47.7 MB (47742541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eb8d26565a771439c11809356c7869ad7aeb0eb7eb0858f7c608d5356ef72274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8bd351ec2a646df3fff90485d2df39f601e0944b80d8b4143c9ccb3320d507f`

```dockerfile
```

-	Layers:
	-	`sha256:816052d2a74f2d518fe4b39b3f4c2ac66c3da2d731a25c9a46406294074d0043`  
		Last Modified: Sat, 19 Oct 2024 05:14:34 GMT  
		Size: 5.1 MB (5092768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb149f548535a0814f4e007c20ce2d36141cfc59043d9afd9bc1ff5f4bd4f4af`  
		Last Modified: Sat, 19 Oct 2024 05:14:34 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json
