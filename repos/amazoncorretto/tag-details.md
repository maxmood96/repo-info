<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazoncorretto`

-	[`amazoncorretto:11`](#amazoncorretto11)
-	[`amazoncorretto:11.0.6`](#amazoncorretto1106)
-	[`amazoncorretto:11-al2-full`](#amazoncorretto11-al2-full)
-	[`amazoncorretto:8`](#amazoncorretto8)
-	[`amazoncorretto:8-al2-full`](#amazoncorretto8-al2-full)
-	[`amazoncorretto:8u242`](#amazoncorretto8u242)
-	[`amazoncorretto:latest`](#amazoncorrettolatest)

## `amazoncorretto:11`

```console
$ docker pull amazoncorretto@sha256:839ce5ed69cd512846b881e5f9d803ff1ee9e649798c6dc0ace4fff291d13382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:53208af0fe7a45fd02eb259d6a4610ed33b67a54a288baeb81a84bb1b240dea2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258779574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee899761d2f952e886840729254e5af2253e1be7fb4c190175cfdf9f9ea3211a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2020 00:40:58 GMT
ARG rpm_x64=java-11-amazon-corretto-devel-11.0.5.10-1.x86_64.rpm
# Fri, 10 Jan 2020 00:40:58 GMT
ARG path_x64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1
# Fri, 10 Jan 2020 00:40:59 GMT
ARG key_x64=13817E35D6AA26BB2D85267712EABAC5209DDBC0
# Fri, 10 Jan 2020 00:40:59 GMT
ARG rpm_aarch64=java-11-amazon-corretto-devel-11.0.5.10-1.aarch64.rpm
# Fri, 10 Jan 2020 00:40:59 GMT
ARG path_aarch64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1
# Fri, 10 Jan 2020 00:40:59 GMT
ARG key_aarch64=13817E35D6AA26BB2D85267712EABAC5209DDBC0
# Fri, 10 Jan 2020 00:41:23 GMT
# ARGS: key_aarch64=13817E35D6AA26BB2D85267712EABAC5209DDBC0 key_x64=13817E35D6AA26BB2D85267712EABAC5209DDBC0 path_aarch64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1 path_x64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1 rpm_aarch64=java-11-amazon-corretto-devel-11.0.5.10-1.aarch64.rpm rpm_x64=java-11-amazon-corretto-devel-11.0.5.10-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Fri, 10 Jan 2020 00:41:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea114604f22597fc99de99c89dfc51029d241802df17d71b77c97352e271ee99`  
		Last Modified: Fri, 10 Jan 2020 00:43:16 GMT  
		Size: 197.2 MB (197226721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:42c34535d05a1bb0f61240dbb12c2a40adf71635f07a085b230234130e727a2d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258286489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90e0cb2f18aa753df578b452ab3ed443fea0e907c96eb810d98e9605115624c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2020 00:25:01 GMT
ARG rpm_x64=java-11-amazon-corretto-devel-11.0.5.10-1.x86_64.rpm
# Fri, 10 Jan 2020 00:25:01 GMT
ARG path_x64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1
# Fri, 10 Jan 2020 00:25:02 GMT
ARG key_x64=13817E35D6AA26BB2D85267712EABAC5209DDBC0
# Fri, 10 Jan 2020 00:25:02 GMT
ARG rpm_aarch64=java-11-amazon-corretto-devel-11.0.5.10-1.aarch64.rpm
# Fri, 10 Jan 2020 00:25:03 GMT
ARG path_aarch64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1
# Fri, 10 Jan 2020 00:25:03 GMT
ARG key_aarch64=13817E35D6AA26BB2D85267712EABAC5209DDBC0
# Fri, 10 Jan 2020 00:25:33 GMT
# ARGS: key_aarch64=13817E35D6AA26BB2D85267712EABAC5209DDBC0 key_x64=13817E35D6AA26BB2D85267712EABAC5209DDBC0 path_aarch64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1 path_x64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1 rpm_aarch64=java-11-amazon-corretto-devel-11.0.5.10-1.aarch64.rpm rpm_x64=java-11-amazon-corretto-devel-11.0.5.10-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Fri, 10 Jan 2020 00:25:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbf30931019961d3fefd22d377461dc4065d0d1d2dd7930d76159809f702594`  
		Last Modified: Fri, 10 Jan 2020 00:28:45 GMT  
		Size: 195.5 MB (195489756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11.0.6`

**does not exist** (yet?)

## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:839ce5ed69cd512846b881e5f9d803ff1ee9e649798c6dc0ace4fff291d13382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:53208af0fe7a45fd02eb259d6a4610ed33b67a54a288baeb81a84bb1b240dea2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258779574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee899761d2f952e886840729254e5af2253e1be7fb4c190175cfdf9f9ea3211a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2020 00:40:58 GMT
ARG rpm_x64=java-11-amazon-corretto-devel-11.0.5.10-1.x86_64.rpm
# Fri, 10 Jan 2020 00:40:58 GMT
ARG path_x64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1
# Fri, 10 Jan 2020 00:40:59 GMT
ARG key_x64=13817E35D6AA26BB2D85267712EABAC5209DDBC0
# Fri, 10 Jan 2020 00:40:59 GMT
ARG rpm_aarch64=java-11-amazon-corretto-devel-11.0.5.10-1.aarch64.rpm
# Fri, 10 Jan 2020 00:40:59 GMT
ARG path_aarch64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1
# Fri, 10 Jan 2020 00:40:59 GMT
ARG key_aarch64=13817E35D6AA26BB2D85267712EABAC5209DDBC0
# Fri, 10 Jan 2020 00:41:23 GMT
# ARGS: key_aarch64=13817E35D6AA26BB2D85267712EABAC5209DDBC0 key_x64=13817E35D6AA26BB2D85267712EABAC5209DDBC0 path_aarch64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1 path_x64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1 rpm_aarch64=java-11-amazon-corretto-devel-11.0.5.10-1.aarch64.rpm rpm_x64=java-11-amazon-corretto-devel-11.0.5.10-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Fri, 10 Jan 2020 00:41:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea114604f22597fc99de99c89dfc51029d241802df17d71b77c97352e271ee99`  
		Last Modified: Fri, 10 Jan 2020 00:43:16 GMT  
		Size: 197.2 MB (197226721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:42c34535d05a1bb0f61240dbb12c2a40adf71635f07a085b230234130e727a2d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258286489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90e0cb2f18aa753df578b452ab3ed443fea0e907c96eb810d98e9605115624c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2020 00:25:01 GMT
ARG rpm_x64=java-11-amazon-corretto-devel-11.0.5.10-1.x86_64.rpm
# Fri, 10 Jan 2020 00:25:01 GMT
ARG path_x64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1
# Fri, 10 Jan 2020 00:25:02 GMT
ARG key_x64=13817E35D6AA26BB2D85267712EABAC5209DDBC0
# Fri, 10 Jan 2020 00:25:02 GMT
ARG rpm_aarch64=java-11-amazon-corretto-devel-11.0.5.10-1.aarch64.rpm
# Fri, 10 Jan 2020 00:25:03 GMT
ARG path_aarch64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1
# Fri, 10 Jan 2020 00:25:03 GMT
ARG key_aarch64=13817E35D6AA26BB2D85267712EABAC5209DDBC0
# Fri, 10 Jan 2020 00:25:33 GMT
# ARGS: key_aarch64=13817E35D6AA26BB2D85267712EABAC5209DDBC0 key_x64=13817E35D6AA26BB2D85267712EABAC5209DDBC0 path_aarch64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1 path_x64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1 rpm_aarch64=java-11-amazon-corretto-devel-11.0.5.10-1.aarch64.rpm rpm_x64=java-11-amazon-corretto-devel-11.0.5.10-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Fri, 10 Jan 2020 00:25:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbf30931019961d3fefd22d377461dc4065d0d1d2dd7930d76159809f702594`  
		Last Modified: Fri, 10 Jan 2020 00:28:45 GMT  
		Size: 195.5 MB (195489756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8`

```console
$ docker pull amazoncorretto@sha256:fa6ef84992f7b7c363043ce994e0cdfc7be319c5ed27b3a5d6495995daa2d977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f855bfef99645840f48dc0bdc1a84417bde006e6eaf2c8346ba933668417ad05
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183099536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d5e55b2b7d507b8e522ac1c0b1a312b4fcd52f53e5550e9beba6ddf99ec090`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2020 00:40:30 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.x86_64.rpm
# Fri, 10 Jan 2020 00:40:31 GMT
ARG path_x64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1
# Fri, 10 Jan 2020 00:40:31 GMT
ARG key_x64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19
# Fri, 10 Jan 2020 00:40:31 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.aarch64.rpm
# Fri, 10 Jan 2020 00:40:31 GMT
ARG path_aarch64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1
# Fri, 10 Jan 2020 00:40:31 GMT
ARG key_aarch64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19
# Fri, 10 Jan 2020 00:40:52 GMT
# ARGS: key_aarch64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19 key_x64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19 path_aarch64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1 path_x64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Fri, 10 Jan 2020 00:40:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958dc053a014ea0286ce7c210872de2b8f6cbc490e81f49bc5341ca50cae3d57`  
		Last Modified: Fri, 10 Jan 2020 00:41:57 GMT  
		Size: 121.5 MB (121546683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0c14f445e1c65ba8eafd8cc67f2e88de3ec57575e64b3d20d9d31e8c26902dab
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167773049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc6d6784499f1e52945355886712e36c0f369dae5da98bb26a66bfa5d9acc02`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2020 00:24:21 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.x86_64.rpm
# Fri, 10 Jan 2020 00:24:22 GMT
ARG path_x64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1
# Fri, 10 Jan 2020 00:24:22 GMT
ARG key_x64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19
# Fri, 10 Jan 2020 00:24:23 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.aarch64.rpm
# Fri, 10 Jan 2020 00:24:24 GMT
ARG path_aarch64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1
# Fri, 10 Jan 2020 00:24:24 GMT
ARG key_aarch64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19
# Fri, 10 Jan 2020 00:24:51 GMT
# ARGS: key_aarch64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19 key_x64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19 path_aarch64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1 path_x64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Fri, 10 Jan 2020 00:24:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a50eae34777174875c769f2ad6ed222cb5a02e9fec1225e68789601b180f8ff`  
		Last Modified: Fri, 10 Jan 2020 00:28:01 GMT  
		Size: 105.0 MB (104976316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:fa6ef84992f7b7c363043ce994e0cdfc7be319c5ed27b3a5d6495995daa2d977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f855bfef99645840f48dc0bdc1a84417bde006e6eaf2c8346ba933668417ad05
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183099536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d5e55b2b7d507b8e522ac1c0b1a312b4fcd52f53e5550e9beba6ddf99ec090`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2020 00:40:30 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.x86_64.rpm
# Fri, 10 Jan 2020 00:40:31 GMT
ARG path_x64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1
# Fri, 10 Jan 2020 00:40:31 GMT
ARG key_x64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19
# Fri, 10 Jan 2020 00:40:31 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.aarch64.rpm
# Fri, 10 Jan 2020 00:40:31 GMT
ARG path_aarch64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1
# Fri, 10 Jan 2020 00:40:31 GMT
ARG key_aarch64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19
# Fri, 10 Jan 2020 00:40:52 GMT
# ARGS: key_aarch64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19 key_x64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19 path_aarch64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1 path_x64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Fri, 10 Jan 2020 00:40:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958dc053a014ea0286ce7c210872de2b8f6cbc490e81f49bc5341ca50cae3d57`  
		Last Modified: Fri, 10 Jan 2020 00:41:57 GMT  
		Size: 121.5 MB (121546683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0c14f445e1c65ba8eafd8cc67f2e88de3ec57575e64b3d20d9d31e8c26902dab
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167773049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc6d6784499f1e52945355886712e36c0f369dae5da98bb26a66bfa5d9acc02`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2020 00:24:21 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.x86_64.rpm
# Fri, 10 Jan 2020 00:24:22 GMT
ARG path_x64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1
# Fri, 10 Jan 2020 00:24:22 GMT
ARG key_x64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19
# Fri, 10 Jan 2020 00:24:23 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.aarch64.rpm
# Fri, 10 Jan 2020 00:24:24 GMT
ARG path_aarch64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1
# Fri, 10 Jan 2020 00:24:24 GMT
ARG key_aarch64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19
# Fri, 10 Jan 2020 00:24:51 GMT
# ARGS: key_aarch64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19 key_x64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19 path_aarch64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1 path_x64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Fri, 10 Jan 2020 00:24:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a50eae34777174875c769f2ad6ed222cb5a02e9fec1225e68789601b180f8ff`  
		Last Modified: Fri, 10 Jan 2020 00:28:01 GMT  
		Size: 105.0 MB (104976316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u242`

**does not exist** (yet?)

## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:fa6ef84992f7b7c363043ce994e0cdfc7be319c5ed27b3a5d6495995daa2d977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f855bfef99645840f48dc0bdc1a84417bde006e6eaf2c8346ba933668417ad05
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183099536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d5e55b2b7d507b8e522ac1c0b1a312b4fcd52f53e5550e9beba6ddf99ec090`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2020 00:40:30 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.x86_64.rpm
# Fri, 10 Jan 2020 00:40:31 GMT
ARG path_x64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1
# Fri, 10 Jan 2020 00:40:31 GMT
ARG key_x64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19
# Fri, 10 Jan 2020 00:40:31 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.aarch64.rpm
# Fri, 10 Jan 2020 00:40:31 GMT
ARG path_aarch64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1
# Fri, 10 Jan 2020 00:40:31 GMT
ARG key_aarch64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19
# Fri, 10 Jan 2020 00:40:52 GMT
# ARGS: key_aarch64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19 key_x64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19 path_aarch64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1 path_x64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Fri, 10 Jan 2020 00:40:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958dc053a014ea0286ce7c210872de2b8f6cbc490e81f49bc5341ca50cae3d57`  
		Last Modified: Fri, 10 Jan 2020 00:41:57 GMT  
		Size: 121.5 MB (121546683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:latest` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0c14f445e1c65ba8eafd8cc67f2e88de3ec57575e64b3d20d9d31e8c26902dab
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167773049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc6d6784499f1e52945355886712e36c0f369dae5da98bb26a66bfa5d9acc02`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2020 00:24:21 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.x86_64.rpm
# Fri, 10 Jan 2020 00:24:22 GMT
ARG path_x64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1
# Fri, 10 Jan 2020 00:24:22 GMT
ARG key_x64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19
# Fri, 10 Jan 2020 00:24:23 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.aarch64.rpm
# Fri, 10 Jan 2020 00:24:24 GMT
ARG path_aarch64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1
# Fri, 10 Jan 2020 00:24:24 GMT
ARG key_aarch64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19
# Fri, 10 Jan 2020 00:24:51 GMT
# ARGS: key_aarch64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19 key_x64=E8EB406377AD2B9E9A4765D19CB3BC6FF6C9FC19 path_aarch64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1 path_x64=https://d3pxv6yz143wms.cloudfront.net/8.232.09.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_232.b09-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Fri, 10 Jan 2020 00:24:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a50eae34777174875c769f2ad6ed222cb5a02e9fec1225e68789601b180f8ff`  
		Last Modified: Fri, 10 Jan 2020 00:28:01 GMT  
		Size: 105.0 MB (104976316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
