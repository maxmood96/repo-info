<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazoncorretto`

-	[`amazoncorretto:11`](#amazoncorretto11)
-	[`amazoncorretto:11.0.7`](#amazoncorretto1107)
-	[`amazoncorretto:11-al2-full`](#amazoncorretto11-al2-full)
-	[`amazoncorretto:8`](#amazoncorretto8)
-	[`amazoncorretto:8-al2-full`](#amazoncorretto8-al2-full)
-	[`amazoncorretto:8u252`](#amazoncorretto8u252)
-	[`amazoncorretto:latest`](#amazoncorrettolatest)

## `amazoncorretto:11`

```console
$ docker pull amazoncorretto@sha256:e20e71463e9a7d0e33e4e8ebd587e8088583c2454d9b355bc180e1b5a5543b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:070ef71e303bc62cd32c9f1003480368330b7dacfb5807c19cdb00ebdb5ac679
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259145916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acf862bb8fbc06d3a646a50d54a62f26f0e71f993b60e8469d14ad1394f6e81`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2020 06:46:32 GMT
ADD file:119ae574c5d5b6e59e83ecadbe4c8dc4e7b535508e63704e74939df696c9b9a1 in / 
# Wed, 01 Apr 2020 06:46:33 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2020 13:48:33 GMT
ARG rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
# Wed, 01 Apr 2020 13:48:34 GMT
ARG path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 01 Apr 2020 13:48:34 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 13:48:34 GMT
ARG rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm
# Wed, 01 Apr 2020 13:48:34 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 01 Apr 2020 13:48:34 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 13:48:56 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1 path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1 rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 01 Apr 2020 13:48:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a8d577519c9fb37ef239a77026a16c019d20cce14b25867f57a44459b3bbf387`  
		Last Modified: Wed, 01 Apr 2020 06:48:00 GMT  
		Size: 61.7 MB (61655014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4635e638cc9af1a6d6d9e1db17ce3964d199a9b7395a249c437ae791c2ea4a95`  
		Last Modified: Wed, 01 Apr 2020 13:49:39 GMT  
		Size: 197.5 MB (197490902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5dc5f338360b25847b978c66a868eeaa11d30860fef88dd1faa7ef740ffcb9ab
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258814417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f552d6bfdaf5ac8ed252c4ca8da0fc91f1921b3ed1824dcb6f7544f09775ff44`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2020 05:22:43 GMT
ADD file:40b8f329ad6d591029e1a4cde76c1d097315b136796d31bb9d3df35183423c14 in / 
# Wed, 01 Apr 2020 05:22:46 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2020 08:29:36 GMT
ARG rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
# Wed, 01 Apr 2020 08:29:37 GMT
ARG path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 01 Apr 2020 08:29:37 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 08:29:38 GMT
ARG rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm
# Wed, 01 Apr 2020 08:29:38 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 01 Apr 2020 08:29:39 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 08:30:06 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1 path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1 rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 01 Apr 2020 08:30:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:01d0a3bd5b98a6512409a10e5e5b065e87b794f924f3f9f7662939925aac631b`  
		Last Modified: Wed, 01 Apr 2020 05:24:01 GMT  
		Size: 63.1 MB (63072580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609ca5b883384db65353f55f91bc6a4c738f6fcfc23e18d46bc4a1d2580bfadc`  
		Last Modified: Wed, 01 Apr 2020 08:31:39 GMT  
		Size: 195.7 MB (195741837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11.0.7`

**does not exist** (yet?)

## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:e20e71463e9a7d0e33e4e8ebd587e8088583c2454d9b355bc180e1b5a5543b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:070ef71e303bc62cd32c9f1003480368330b7dacfb5807c19cdb00ebdb5ac679
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259145916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acf862bb8fbc06d3a646a50d54a62f26f0e71f993b60e8469d14ad1394f6e81`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2020 06:46:32 GMT
ADD file:119ae574c5d5b6e59e83ecadbe4c8dc4e7b535508e63704e74939df696c9b9a1 in / 
# Wed, 01 Apr 2020 06:46:33 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2020 13:48:33 GMT
ARG rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
# Wed, 01 Apr 2020 13:48:34 GMT
ARG path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 01 Apr 2020 13:48:34 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 13:48:34 GMT
ARG rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm
# Wed, 01 Apr 2020 13:48:34 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 01 Apr 2020 13:48:34 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 13:48:56 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1 path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1 rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 01 Apr 2020 13:48:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a8d577519c9fb37ef239a77026a16c019d20cce14b25867f57a44459b3bbf387`  
		Last Modified: Wed, 01 Apr 2020 06:48:00 GMT  
		Size: 61.7 MB (61655014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4635e638cc9af1a6d6d9e1db17ce3964d199a9b7395a249c437ae791c2ea4a95`  
		Last Modified: Wed, 01 Apr 2020 13:49:39 GMT  
		Size: 197.5 MB (197490902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5dc5f338360b25847b978c66a868eeaa11d30860fef88dd1faa7ef740ffcb9ab
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258814417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f552d6bfdaf5ac8ed252c4ca8da0fc91f1921b3ed1824dcb6f7544f09775ff44`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2020 05:22:43 GMT
ADD file:40b8f329ad6d591029e1a4cde76c1d097315b136796d31bb9d3df35183423c14 in / 
# Wed, 01 Apr 2020 05:22:46 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2020 08:29:36 GMT
ARG rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
# Wed, 01 Apr 2020 08:29:37 GMT
ARG path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 01 Apr 2020 08:29:37 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 08:29:38 GMT
ARG rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm
# Wed, 01 Apr 2020 08:29:38 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 01 Apr 2020 08:29:39 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 08:30:06 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1 path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1 rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 01 Apr 2020 08:30:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:01d0a3bd5b98a6512409a10e5e5b065e87b794f924f3f9f7662939925aac631b`  
		Last Modified: Wed, 01 Apr 2020 05:24:01 GMT  
		Size: 63.1 MB (63072580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609ca5b883384db65353f55f91bc6a4c738f6fcfc23e18d46bc4a1d2580bfadc`  
		Last Modified: Wed, 01 Apr 2020 08:31:39 GMT  
		Size: 195.7 MB (195741837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8`

```console
$ docker pull amazoncorretto@sha256:df00af9b9775aa8423681c3d46b15a233f6b344b43c7c57bc441891dffdfeb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8e0da5527d3b3b8ebfde1b288a908e66ace7a654b949aec92094fbecae675414
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183246697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6eade3fd441ab70bca3a794af6716f75889a71465eb73fbd776385dd32e0a6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2020 06:46:32 GMT
ADD file:119ae574c5d5b6e59e83ecadbe4c8dc4e7b535508e63704e74939df696c9b9a1 in / 
# Wed, 01 Apr 2020 06:46:33 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2020 13:48:10 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
# Wed, 01 Apr 2020 13:48:10 GMT
ARG path_x64=https://corretto.aws/downloads/resources/8.242.08.1
# Wed, 01 Apr 2020 13:48:10 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 13:48:10 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm
# Wed, 01 Apr 2020 13:48:10 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1
# Wed, 01 Apr 2020 13:48:11 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 13:48:29 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1 path_x64=https://corretto.aws/downloads/resources/8.242.08.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 01 Apr 2020 13:48:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:a8d577519c9fb37ef239a77026a16c019d20cce14b25867f57a44459b3bbf387`  
		Last Modified: Wed, 01 Apr 2020 06:48:00 GMT  
		Size: 61.7 MB (61655014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ad584aa484a0420ddb045725aaf2dbfe7319ee40021e1a55cae65ce104b4d`  
		Last Modified: Wed, 01 Apr 2020 13:49:17 GMT  
		Size: 121.6 MB (121591683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f1f2edd2811c891c40caa419ba985f0d66f176611b3b2edabd1ece100bdd4656
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (168046929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613c2fa7083aba3dc20cbf42b6fc6f1366e85158678096ce820f7b3cd65e2d92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2020 05:22:43 GMT
ADD file:40b8f329ad6d591029e1a4cde76c1d097315b136796d31bb9d3df35183423c14 in / 
# Wed, 01 Apr 2020 05:22:46 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2020 08:29:02 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
# Wed, 01 Apr 2020 08:29:02 GMT
ARG path_x64=https://corretto.aws/downloads/resources/8.242.08.1
# Wed, 01 Apr 2020 08:29:03 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 08:29:03 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm
# Wed, 01 Apr 2020 08:29:04 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1
# Wed, 01 Apr 2020 08:29:04 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 08:29:27 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1 path_x64=https://corretto.aws/downloads/resources/8.242.08.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 01 Apr 2020 08:29:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:01d0a3bd5b98a6512409a10e5e5b065e87b794f924f3f9f7662939925aac631b`  
		Last Modified: Wed, 01 Apr 2020 05:24:01 GMT  
		Size: 63.1 MB (63072580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b897bb90f24638d350f41e113472509d7732f6a6d4f27763cf180b28a4f8c6`  
		Last Modified: Wed, 01 Apr 2020 08:30:57 GMT  
		Size: 105.0 MB (104974349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:df00af9b9775aa8423681c3d46b15a233f6b344b43c7c57bc441891dffdfeb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8e0da5527d3b3b8ebfde1b288a908e66ace7a654b949aec92094fbecae675414
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183246697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6eade3fd441ab70bca3a794af6716f75889a71465eb73fbd776385dd32e0a6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2020 06:46:32 GMT
ADD file:119ae574c5d5b6e59e83ecadbe4c8dc4e7b535508e63704e74939df696c9b9a1 in / 
# Wed, 01 Apr 2020 06:46:33 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2020 13:48:10 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
# Wed, 01 Apr 2020 13:48:10 GMT
ARG path_x64=https://corretto.aws/downloads/resources/8.242.08.1
# Wed, 01 Apr 2020 13:48:10 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 13:48:10 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm
# Wed, 01 Apr 2020 13:48:10 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1
# Wed, 01 Apr 2020 13:48:11 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 13:48:29 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1 path_x64=https://corretto.aws/downloads/resources/8.242.08.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 01 Apr 2020 13:48:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:a8d577519c9fb37ef239a77026a16c019d20cce14b25867f57a44459b3bbf387`  
		Last Modified: Wed, 01 Apr 2020 06:48:00 GMT  
		Size: 61.7 MB (61655014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ad584aa484a0420ddb045725aaf2dbfe7319ee40021e1a55cae65ce104b4d`  
		Last Modified: Wed, 01 Apr 2020 13:49:17 GMT  
		Size: 121.6 MB (121591683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f1f2edd2811c891c40caa419ba985f0d66f176611b3b2edabd1ece100bdd4656
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (168046929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613c2fa7083aba3dc20cbf42b6fc6f1366e85158678096ce820f7b3cd65e2d92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2020 05:22:43 GMT
ADD file:40b8f329ad6d591029e1a4cde76c1d097315b136796d31bb9d3df35183423c14 in / 
# Wed, 01 Apr 2020 05:22:46 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2020 08:29:02 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
# Wed, 01 Apr 2020 08:29:02 GMT
ARG path_x64=https://corretto.aws/downloads/resources/8.242.08.1
# Wed, 01 Apr 2020 08:29:03 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 08:29:03 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm
# Wed, 01 Apr 2020 08:29:04 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1
# Wed, 01 Apr 2020 08:29:04 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 08:29:27 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1 path_x64=https://corretto.aws/downloads/resources/8.242.08.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 01 Apr 2020 08:29:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:01d0a3bd5b98a6512409a10e5e5b065e87b794f924f3f9f7662939925aac631b`  
		Last Modified: Wed, 01 Apr 2020 05:24:01 GMT  
		Size: 63.1 MB (63072580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b897bb90f24638d350f41e113472509d7732f6a6d4f27763cf180b28a4f8c6`  
		Last Modified: Wed, 01 Apr 2020 08:30:57 GMT  
		Size: 105.0 MB (104974349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u252`

**does not exist** (yet?)

## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:df00af9b9775aa8423681c3d46b15a233f6b344b43c7c57bc441891dffdfeb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8e0da5527d3b3b8ebfde1b288a908e66ace7a654b949aec92094fbecae675414
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183246697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6eade3fd441ab70bca3a794af6716f75889a71465eb73fbd776385dd32e0a6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2020 06:46:32 GMT
ADD file:119ae574c5d5b6e59e83ecadbe4c8dc4e7b535508e63704e74939df696c9b9a1 in / 
# Wed, 01 Apr 2020 06:46:33 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2020 13:48:10 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
# Wed, 01 Apr 2020 13:48:10 GMT
ARG path_x64=https://corretto.aws/downloads/resources/8.242.08.1
# Wed, 01 Apr 2020 13:48:10 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 13:48:10 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm
# Wed, 01 Apr 2020 13:48:10 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1
# Wed, 01 Apr 2020 13:48:11 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 13:48:29 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1 path_x64=https://corretto.aws/downloads/resources/8.242.08.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 01 Apr 2020 13:48:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:a8d577519c9fb37ef239a77026a16c019d20cce14b25867f57a44459b3bbf387`  
		Last Modified: Wed, 01 Apr 2020 06:48:00 GMT  
		Size: 61.7 MB (61655014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ad584aa484a0420ddb045725aaf2dbfe7319ee40021e1a55cae65ce104b4d`  
		Last Modified: Wed, 01 Apr 2020 13:49:17 GMT  
		Size: 121.6 MB (121591683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:latest` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f1f2edd2811c891c40caa419ba985f0d66f176611b3b2edabd1ece100bdd4656
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (168046929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613c2fa7083aba3dc20cbf42b6fc6f1366e85158678096ce820f7b3cd65e2d92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2020 05:22:43 GMT
ADD file:40b8f329ad6d591029e1a4cde76c1d097315b136796d31bb9d3df35183423c14 in / 
# Wed, 01 Apr 2020 05:22:46 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2020 08:29:02 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
# Wed, 01 Apr 2020 08:29:02 GMT
ARG path_x64=https://corretto.aws/downloads/resources/8.242.08.1
# Wed, 01 Apr 2020 08:29:03 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 08:29:03 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm
# Wed, 01 Apr 2020 08:29:04 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1
# Wed, 01 Apr 2020 08:29:04 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 01 Apr 2020 08:29:27 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1 path_x64=https://corretto.aws/downloads/resources/8.242.08.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 01 Apr 2020 08:29:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:01d0a3bd5b98a6512409a10e5e5b065e87b794f924f3f9f7662939925aac631b`  
		Last Modified: Wed, 01 Apr 2020 05:24:01 GMT  
		Size: 63.1 MB (63072580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b897bb90f24638d350f41e113472509d7732f6a6d4f27763cf180b28a4f8c6`  
		Last Modified: Wed, 01 Apr 2020 08:30:57 GMT  
		Size: 105.0 MB (104974349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
