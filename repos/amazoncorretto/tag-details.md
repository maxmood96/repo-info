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
$ docker pull amazoncorretto@sha256:13384ec927e4724fd91217fbe6e593de6db3fae43e0fea2372dfe74fdbd29252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d941cb32b983e992ac600ebe63a1a1e64fa99b90dde66640bb035744a94ac682
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (259048463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2a640d4c1d6f20ef3265fafb17452b65d9760cadbb3396578859f83767378c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2020 21:19:53 GMT
ARG rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
# Wed, 15 Jan 2020 21:19:53 GMT
ARG path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 15 Jan 2020 21:19:53 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 15 Jan 2020 21:19:54 GMT
ARG rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm
# Wed, 15 Jan 2020 21:19:54 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 15 Jan 2020 21:19:54 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 15 Jan 2020 21:20:15 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1 path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1 rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jan 2020 21:20:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6433498f093ea7337102f34b01b34fd62fc0e53fa3bfbcdf13dab58f1b6cbb4`  
		Last Modified: Wed, 15 Jan 2020 21:21:13 GMT  
		Size: 197.5 MB (197495610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b9efb05043d2b1f1475d9387a54883be20151ef6011047b2f995f4910879f2d5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258543820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068c2f1c98c32e76a3d553f51880966426795df68bc8b64b99bd01305e1b54c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2020 21:40:10 GMT
ARG rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
# Wed, 15 Jan 2020 21:40:10 GMT
ARG path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 15 Jan 2020 21:40:11 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 15 Jan 2020 21:40:12 GMT
ARG rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm
# Wed, 15 Jan 2020 21:40:12 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 15 Jan 2020 21:40:13 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 15 Jan 2020 21:40:40 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1 path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1 rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jan 2020 21:40:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36da2db97f6fae3dad031512af96b94e04f8f044e961aa09b35cc5b70c1db57b`  
		Last Modified: Wed, 15 Jan 2020 21:42:02 GMT  
		Size: 195.7 MB (195747087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11.0.6`

```console
$ docker pull amazoncorretto@sha256:13384ec927e4724fd91217fbe6e593de6db3fae43e0fea2372dfe74fdbd29252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11.0.6` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d941cb32b983e992ac600ebe63a1a1e64fa99b90dde66640bb035744a94ac682
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (259048463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2a640d4c1d6f20ef3265fafb17452b65d9760cadbb3396578859f83767378c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2020 21:19:53 GMT
ARG rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
# Wed, 15 Jan 2020 21:19:53 GMT
ARG path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 15 Jan 2020 21:19:53 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 15 Jan 2020 21:19:54 GMT
ARG rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm
# Wed, 15 Jan 2020 21:19:54 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 15 Jan 2020 21:19:54 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 15 Jan 2020 21:20:15 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1 path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1 rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jan 2020 21:20:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6433498f093ea7337102f34b01b34fd62fc0e53fa3bfbcdf13dab58f1b6cbb4`  
		Last Modified: Wed, 15 Jan 2020 21:21:13 GMT  
		Size: 197.5 MB (197495610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11.0.6` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b9efb05043d2b1f1475d9387a54883be20151ef6011047b2f995f4910879f2d5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258543820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068c2f1c98c32e76a3d553f51880966426795df68bc8b64b99bd01305e1b54c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2020 21:40:10 GMT
ARG rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
# Wed, 15 Jan 2020 21:40:10 GMT
ARG path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 15 Jan 2020 21:40:11 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 15 Jan 2020 21:40:12 GMT
ARG rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm
# Wed, 15 Jan 2020 21:40:12 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 15 Jan 2020 21:40:13 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 15 Jan 2020 21:40:40 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1 path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1 rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jan 2020 21:40:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36da2db97f6fae3dad031512af96b94e04f8f044e961aa09b35cc5b70c1db57b`  
		Last Modified: Wed, 15 Jan 2020 21:42:02 GMT  
		Size: 195.7 MB (195747087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:13384ec927e4724fd91217fbe6e593de6db3fae43e0fea2372dfe74fdbd29252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d941cb32b983e992ac600ebe63a1a1e64fa99b90dde66640bb035744a94ac682
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (259048463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2a640d4c1d6f20ef3265fafb17452b65d9760cadbb3396578859f83767378c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2020 21:19:53 GMT
ARG rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
# Wed, 15 Jan 2020 21:19:53 GMT
ARG path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 15 Jan 2020 21:19:53 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 15 Jan 2020 21:19:54 GMT
ARG rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm
# Wed, 15 Jan 2020 21:19:54 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 15 Jan 2020 21:19:54 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 15 Jan 2020 21:20:15 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1 path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1 rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jan 2020 21:20:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6433498f093ea7337102f34b01b34fd62fc0e53fa3bfbcdf13dab58f1b6cbb4`  
		Last Modified: Wed, 15 Jan 2020 21:21:13 GMT  
		Size: 197.5 MB (197495610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b9efb05043d2b1f1475d9387a54883be20151ef6011047b2f995f4910879f2d5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258543820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068c2f1c98c32e76a3d553f51880966426795df68bc8b64b99bd01305e1b54c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2020 21:40:10 GMT
ARG rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
# Wed, 15 Jan 2020 21:40:10 GMT
ARG path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 15 Jan 2020 21:40:11 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 15 Jan 2020 21:40:12 GMT
ARG rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm
# Wed, 15 Jan 2020 21:40:12 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1
# Wed, 15 Jan 2020 21:40:13 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Wed, 15 Jan 2020 21:40:40 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/11.0.6.10.1 path_x64=https://corretto.aws/downloads/resources/11.0.6.10.1 rpm_aarch64=java-11-amazon-corretto-devel-11.0.6.10-1.aarch64.rpm rpm_x64=java-11-amazon-corretto-devel-11.0.6.10-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jan 2020 21:40:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36da2db97f6fae3dad031512af96b94e04f8f044e961aa09b35cc5b70c1db57b`  
		Last Modified: Wed, 15 Jan 2020 21:42:02 GMT  
		Size: 195.7 MB (195747087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8`

```console
$ docker pull amazoncorretto@sha256:74731ce0d8e704cac0fed73de00340f391a6a6bfd1248d5d80188845c0538b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8856d3064480e11616daa1ec274a0e4e365e2b417aa1587ee02a7a3f059dab16
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183152201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98dbda58eb65e1423a3be784663af17bfb5dd8e9cb3a59ce0b4839473035b41`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2020 21:19:25 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
# Tue, 21 Jan 2020 21:19:25 GMT
ARG path_x64=https://corretto.aws/downloads/resources/8.242.08.1
# Tue, 21 Jan 2020 21:19:25 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Tue, 21 Jan 2020 21:19:25 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm
# Tue, 21 Jan 2020 21:19:26 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1
# Tue, 21 Jan 2020 21:19:26 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Tue, 21 Jan 2020 21:19:45 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1 path_x64=https://corretto.aws/downloads/resources/8.242.08.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Tue, 21 Jan 2020 21:19:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6be758ae644465d0bac918d97e86933e19c5fd0263a96e6f8095cdf4948ba5`  
		Last Modified: Tue, 21 Jan 2020 21:20:48 GMT  
		Size: 121.6 MB (121599348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0c0612e3a00b501541e3f5d40b2bd84e5cda5029bb9f4dc663b40f43b8e90d2e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167788001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d773e4e93075e550c2f458586c58356ce8b46d5c58375b45bfa0cf339680685e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2020 21:39:29 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
# Tue, 21 Jan 2020 21:39:30 GMT
ARG path_x64=https://corretto.aws/downloads/resources/8.242.08.1
# Tue, 21 Jan 2020 21:39:30 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Tue, 21 Jan 2020 21:39:31 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm
# Tue, 21 Jan 2020 21:39:31 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1
# Tue, 21 Jan 2020 21:39:32 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Tue, 21 Jan 2020 21:40:02 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1 path_x64=https://corretto.aws/downloads/resources/8.242.08.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Tue, 21 Jan 2020 21:40:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaec8732fb50a7de9f9ecd690a6d9332d74b91fec4d162418fe3a0584a9283c`  
		Last Modified: Tue, 21 Jan 2020 21:40:39 GMT  
		Size: 105.0 MB (104991268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:74731ce0d8e704cac0fed73de00340f391a6a6bfd1248d5d80188845c0538b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8856d3064480e11616daa1ec274a0e4e365e2b417aa1587ee02a7a3f059dab16
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183152201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98dbda58eb65e1423a3be784663af17bfb5dd8e9cb3a59ce0b4839473035b41`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2020 21:19:25 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
# Tue, 21 Jan 2020 21:19:25 GMT
ARG path_x64=https://corretto.aws/downloads/resources/8.242.08.1
# Tue, 21 Jan 2020 21:19:25 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Tue, 21 Jan 2020 21:19:25 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm
# Tue, 21 Jan 2020 21:19:26 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1
# Tue, 21 Jan 2020 21:19:26 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Tue, 21 Jan 2020 21:19:45 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1 path_x64=https://corretto.aws/downloads/resources/8.242.08.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Tue, 21 Jan 2020 21:19:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6be758ae644465d0bac918d97e86933e19c5fd0263a96e6f8095cdf4948ba5`  
		Last Modified: Tue, 21 Jan 2020 21:20:48 GMT  
		Size: 121.6 MB (121599348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0c0612e3a00b501541e3f5d40b2bd84e5cda5029bb9f4dc663b40f43b8e90d2e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167788001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d773e4e93075e550c2f458586c58356ce8b46d5c58375b45bfa0cf339680685e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2020 21:39:29 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
# Tue, 21 Jan 2020 21:39:30 GMT
ARG path_x64=https://corretto.aws/downloads/resources/8.242.08.1
# Tue, 21 Jan 2020 21:39:30 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Tue, 21 Jan 2020 21:39:31 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm
# Tue, 21 Jan 2020 21:39:31 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1
# Tue, 21 Jan 2020 21:39:32 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Tue, 21 Jan 2020 21:40:02 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1 path_x64=https://corretto.aws/downloads/resources/8.242.08.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Tue, 21 Jan 2020 21:40:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaec8732fb50a7de9f9ecd690a6d9332d74b91fec4d162418fe3a0584a9283c`  
		Last Modified: Tue, 21 Jan 2020 21:40:39 GMT  
		Size: 105.0 MB (104991268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u242`

```console
$ docker pull amazoncorretto@sha256:74731ce0d8e704cac0fed73de00340f391a6a6bfd1248d5d80188845c0538b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8u242` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8856d3064480e11616daa1ec274a0e4e365e2b417aa1587ee02a7a3f059dab16
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183152201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98dbda58eb65e1423a3be784663af17bfb5dd8e9cb3a59ce0b4839473035b41`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2020 21:19:25 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
# Tue, 21 Jan 2020 21:19:25 GMT
ARG path_x64=https://corretto.aws/downloads/resources/8.242.08.1
# Tue, 21 Jan 2020 21:19:25 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Tue, 21 Jan 2020 21:19:25 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm
# Tue, 21 Jan 2020 21:19:26 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1
# Tue, 21 Jan 2020 21:19:26 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Tue, 21 Jan 2020 21:19:45 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1 path_x64=https://corretto.aws/downloads/resources/8.242.08.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Tue, 21 Jan 2020 21:19:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6be758ae644465d0bac918d97e86933e19c5fd0263a96e6f8095cdf4948ba5`  
		Last Modified: Tue, 21 Jan 2020 21:20:48 GMT  
		Size: 121.6 MB (121599348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8u242` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0c0612e3a00b501541e3f5d40b2bd84e5cda5029bb9f4dc663b40f43b8e90d2e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167788001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d773e4e93075e550c2f458586c58356ce8b46d5c58375b45bfa0cf339680685e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2020 21:39:29 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
# Tue, 21 Jan 2020 21:39:30 GMT
ARG path_x64=https://corretto.aws/downloads/resources/8.242.08.1
# Tue, 21 Jan 2020 21:39:30 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Tue, 21 Jan 2020 21:39:31 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm
# Tue, 21 Jan 2020 21:39:31 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1
# Tue, 21 Jan 2020 21:39:32 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Tue, 21 Jan 2020 21:40:02 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1 path_x64=https://corretto.aws/downloads/resources/8.242.08.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Tue, 21 Jan 2020 21:40:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaec8732fb50a7de9f9ecd690a6d9332d74b91fec4d162418fe3a0584a9283c`  
		Last Modified: Tue, 21 Jan 2020 21:40:39 GMT  
		Size: 105.0 MB (104991268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:74731ce0d8e704cac0fed73de00340f391a6a6bfd1248d5d80188845c0538b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8856d3064480e11616daa1ec274a0e4e365e2b417aa1587ee02a7a3f059dab16
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183152201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98dbda58eb65e1423a3be784663af17bfb5dd8e9cb3a59ce0b4839473035b41`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2020 21:19:25 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
# Tue, 21 Jan 2020 21:19:25 GMT
ARG path_x64=https://corretto.aws/downloads/resources/8.242.08.1
# Tue, 21 Jan 2020 21:19:25 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Tue, 21 Jan 2020 21:19:25 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm
# Tue, 21 Jan 2020 21:19:26 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1
# Tue, 21 Jan 2020 21:19:26 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Tue, 21 Jan 2020 21:19:45 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1 path_x64=https://corretto.aws/downloads/resources/8.242.08.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Tue, 21 Jan 2020 21:19:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6be758ae644465d0bac918d97e86933e19c5fd0263a96e6f8095cdf4948ba5`  
		Last Modified: Tue, 21 Jan 2020 21:20:48 GMT  
		Size: 121.6 MB (121599348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:latest` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0c0612e3a00b501541e3f5d40b2bd84e5cda5029bb9f4dc663b40f43b8e90d2e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167788001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d773e4e93075e550c2f458586c58356ce8b46d5c58375b45bfa0cf339680685e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2020 21:39:29 GMT
ARG rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
# Tue, 21 Jan 2020 21:39:30 GMT
ARG path_x64=https://corretto.aws/downloads/resources/8.242.08.1
# Tue, 21 Jan 2020 21:39:30 GMT
ARG key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Tue, 21 Jan 2020 21:39:31 GMT
ARG rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm
# Tue, 21 Jan 2020 21:39:31 GMT
ARG path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1
# Tue, 21 Jan 2020 21:39:32 GMT
ARG key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3
# Tue, 21 Jan 2020 21:40:02 GMT
# ARGS: key_aarch64=6DC3636DAE534049C8B94623A122542AB04F24E3 key_x64=6DC3636DAE534049C8B94623A122542AB04F24E3 path_aarch64=https://corretto.aws/downloads/resources/8.242.08.1 path_x64=https://corretto.aws/downloads/resources/8.242.08.1 rpm_aarch64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.aarch64.rpm rpm_x64=java-1.8.0-amazon-corretto-devel-1.8.0_242.b08-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Tue, 21 Jan 2020 21:40:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaec8732fb50a7de9f9ecd690a6d9332d74b91fec4d162418fe3a0584a9283c`  
		Last Modified: Tue, 21 Jan 2020 21:40:39 GMT  
		Size: 105.0 MB (104991268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
