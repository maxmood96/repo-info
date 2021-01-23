<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazoncorretto`

-	[`amazoncorretto:11`](#amazoncorretto11)
-	[`amazoncorretto:11.0.10`](#amazoncorretto11010)
-	[`amazoncorretto:11.0.10-al2`](#amazoncorretto11010-al2)
-	[`amazoncorretto:11.0.10-alpine`](#amazoncorretto11010-alpine)
-	[`amazoncorretto:11-al2-full`](#amazoncorretto11-al2-full)
-	[`amazoncorretto:11-al2-jdk`](#amazoncorretto11-al2-jdk)
-	[`amazoncorretto:11-alpine`](#amazoncorretto11-alpine)
-	[`amazoncorretto:11-alpine-full`](#amazoncorretto11-alpine-full)
-	[`amazoncorretto:11-alpine-jdk`](#amazoncorretto11-alpine-jdk)
-	[`amazoncorretto:15`](#amazoncorretto15)
-	[`amazoncorretto:15.0.2`](#amazoncorretto1502)
-	[`amazoncorretto:15.0.2-al2`](#amazoncorretto1502-al2)
-	[`amazoncorretto:15.0.2-alpine`](#amazoncorretto1502-alpine)
-	[`amazoncorretto:15-al2-full`](#amazoncorretto15-al2-full)
-	[`amazoncorretto:15-al2-jdk`](#amazoncorretto15-al2-jdk)
-	[`amazoncorretto:15-alpine`](#amazoncorretto15-alpine)
-	[`amazoncorretto:15-alpine-full`](#amazoncorretto15-alpine-full)
-	[`amazoncorretto:15-alpine-jdk`](#amazoncorretto15-alpine-jdk)
-	[`amazoncorretto:8`](#amazoncorretto8)
-	[`amazoncorretto:8-al2-full`](#amazoncorretto8-al2-full)
-	[`amazoncorretto:8-al2-jdk`](#amazoncorretto8-al2-jdk)
-	[`amazoncorretto:8-alpine`](#amazoncorretto8-alpine)
-	[`amazoncorretto:8-alpine-full`](#amazoncorretto8-alpine-full)
-	[`amazoncorretto:8-alpine-jdk`](#amazoncorretto8-alpine-jdk)
-	[`amazoncorretto:8-alpine-jre`](#amazoncorretto8-alpine-jre)
-	[`amazoncorretto:8u282`](#amazoncorretto8u282)
-	[`amazoncorretto:8u282-al2`](#amazoncorretto8u282-al2)
-	[`amazoncorretto:8u282-alpine`](#amazoncorretto8u282-alpine)
-	[`amazoncorretto:8u282-alpine-jre`](#amazoncorretto8u282-alpine-jre)
-	[`amazoncorretto:latest`](#amazoncorrettolatest)

## `amazoncorretto:11`

```console
$ docker pull amazoncorretto@sha256:2761a3509de723a1da1b168ae3ed4214a92c0c2a97bab39f2b107910c7cecd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0887fe50a08a79e3a49905496bdc4e4e0ff3a7e46780fd2523baeb7c634b5d80
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208538271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702fddf65318b8961e6d70c184dc9b2420bc7c6c901ed131f096ed5af9e539da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 20:20:09 GMT
ADD file:15991ffbefc01e13f134972ce0eabc6b7901ea9ab4d56347bee5057302cf4848 in / 
# Wed, 23 Dec 2020 20:20:09 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 19:19:56 GMT
ARG version=11.0.10.9-1
# Thu, 21 Jan 2021 19:20:12 GMT
# ARGS: version=11.0.10.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 19:20:12 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:20:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:4232b9ee675bb1f9a32337ec3f266a570b75c54c3c3f173b1abb998e9984ad8c`  
		Last Modified: Wed, 23 Dec 2020 20:21:42 GMT  
		Size: 62.0 MB (62007428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132220740555f6a23e53b52a8be783f695ea89bc701d7aa6eefe5cc9abc31df3`  
		Last Modified: Thu, 21 Jan 2021 19:22:07 GMT  
		Size: 146.5 MB (146530843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9d953f0f482d5e71af840bf8428b842de0c4a12942fc809aa4eab8eb09e47eda
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208296245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd067172ee4dd75c541ab606da819a7af951b749a414e5426c0000f8c0da199`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 18:40:26 GMT
ARG version=11.0.10.9-1
# Thu, 21 Jan 2021 18:40:55 GMT
# ARGS: version=11.0.10.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 18:40:57 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 18:40:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03d2b79d43eb79a680e95539063ef30a4e64bb5d44c8ae1f6984f8876a4a8cc`  
		Last Modified: Thu, 21 Jan 2021 18:42:35 GMT  
		Size: 144.6 MB (144588331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11.0.10`

```console
$ docker pull amazoncorretto@sha256:2761a3509de723a1da1b168ae3ed4214a92c0c2a97bab39f2b107910c7cecd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11.0.10` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0887fe50a08a79e3a49905496bdc4e4e0ff3a7e46780fd2523baeb7c634b5d80
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208538271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702fddf65318b8961e6d70c184dc9b2420bc7c6c901ed131f096ed5af9e539da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 20:20:09 GMT
ADD file:15991ffbefc01e13f134972ce0eabc6b7901ea9ab4d56347bee5057302cf4848 in / 
# Wed, 23 Dec 2020 20:20:09 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 19:19:56 GMT
ARG version=11.0.10.9-1
# Thu, 21 Jan 2021 19:20:12 GMT
# ARGS: version=11.0.10.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 19:20:12 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:20:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:4232b9ee675bb1f9a32337ec3f266a570b75c54c3c3f173b1abb998e9984ad8c`  
		Last Modified: Wed, 23 Dec 2020 20:21:42 GMT  
		Size: 62.0 MB (62007428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132220740555f6a23e53b52a8be783f695ea89bc701d7aa6eefe5cc9abc31df3`  
		Last Modified: Thu, 21 Jan 2021 19:22:07 GMT  
		Size: 146.5 MB (146530843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11.0.10` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9d953f0f482d5e71af840bf8428b842de0c4a12942fc809aa4eab8eb09e47eda
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208296245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd067172ee4dd75c541ab606da819a7af951b749a414e5426c0000f8c0da199`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 18:40:26 GMT
ARG version=11.0.10.9-1
# Thu, 21 Jan 2021 18:40:55 GMT
# ARGS: version=11.0.10.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 18:40:57 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 18:40:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03d2b79d43eb79a680e95539063ef30a4e64bb5d44c8ae1f6984f8876a4a8cc`  
		Last Modified: Thu, 21 Jan 2021 18:42:35 GMT  
		Size: 144.6 MB (144588331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11.0.10-al2`

```console
$ docker pull amazoncorretto@sha256:2761a3509de723a1da1b168ae3ed4214a92c0c2a97bab39f2b107910c7cecd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11.0.10-al2` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0887fe50a08a79e3a49905496bdc4e4e0ff3a7e46780fd2523baeb7c634b5d80
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208538271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702fddf65318b8961e6d70c184dc9b2420bc7c6c901ed131f096ed5af9e539da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 20:20:09 GMT
ADD file:15991ffbefc01e13f134972ce0eabc6b7901ea9ab4d56347bee5057302cf4848 in / 
# Wed, 23 Dec 2020 20:20:09 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 19:19:56 GMT
ARG version=11.0.10.9-1
# Thu, 21 Jan 2021 19:20:12 GMT
# ARGS: version=11.0.10.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 19:20:12 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:20:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:4232b9ee675bb1f9a32337ec3f266a570b75c54c3c3f173b1abb998e9984ad8c`  
		Last Modified: Wed, 23 Dec 2020 20:21:42 GMT  
		Size: 62.0 MB (62007428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132220740555f6a23e53b52a8be783f695ea89bc701d7aa6eefe5cc9abc31df3`  
		Last Modified: Thu, 21 Jan 2021 19:22:07 GMT  
		Size: 146.5 MB (146530843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11.0.10-al2` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9d953f0f482d5e71af840bf8428b842de0c4a12942fc809aa4eab8eb09e47eda
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208296245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd067172ee4dd75c541ab606da819a7af951b749a414e5426c0000f8c0da199`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 18:40:26 GMT
ARG version=11.0.10.9-1
# Thu, 21 Jan 2021 18:40:55 GMT
# ARGS: version=11.0.10.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 18:40:57 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 18:40:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03d2b79d43eb79a680e95539063ef30a4e64bb5d44c8ae1f6984f8876a4a8cc`  
		Last Modified: Thu, 21 Jan 2021 18:42:35 GMT  
		Size: 144.6 MB (144588331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11.0.10-alpine`

```console
$ docker pull amazoncorretto@sha256:b9d5e959586c21e4d2e5fc1e83eb1b2b5b1dfe9a991a499d26e83956d604264c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11.0.10-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dd7e8cb7ba5970b12d36568cbe66162d9c4cd44f8eff8a197be209422ca39234
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195086483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e0d1ca1e0196adfa963a5c4fdcf548b5f5e8afd21039b542d338ef08ed9d18`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 21 Jan 2021 19:20:36 GMT
ARG version=11.0.10.9.1
# Thu, 21 Jan 2021 19:20:43 GMT
# ARGS: version=11.0.10.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Thu, 21 Jan 2021 19:20:43 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:20:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 21 Jan 2021 19:20:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c85d4dd6beb5e76ff7ecf4549e9588d8ae1d73ea6c1045e3b3a6530ff03062b`  
		Last Modified: Thu, 21 Jan 2021 19:23:20 GMT  
		Size: 192.3 MB (192287417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:2761a3509de723a1da1b168ae3ed4214a92c0c2a97bab39f2b107910c7cecd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0887fe50a08a79e3a49905496bdc4e4e0ff3a7e46780fd2523baeb7c634b5d80
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208538271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702fddf65318b8961e6d70c184dc9b2420bc7c6c901ed131f096ed5af9e539da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 20:20:09 GMT
ADD file:15991ffbefc01e13f134972ce0eabc6b7901ea9ab4d56347bee5057302cf4848 in / 
# Wed, 23 Dec 2020 20:20:09 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 19:19:56 GMT
ARG version=11.0.10.9-1
# Thu, 21 Jan 2021 19:20:12 GMT
# ARGS: version=11.0.10.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 19:20:12 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:20:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:4232b9ee675bb1f9a32337ec3f266a570b75c54c3c3f173b1abb998e9984ad8c`  
		Last Modified: Wed, 23 Dec 2020 20:21:42 GMT  
		Size: 62.0 MB (62007428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132220740555f6a23e53b52a8be783f695ea89bc701d7aa6eefe5cc9abc31df3`  
		Last Modified: Thu, 21 Jan 2021 19:22:07 GMT  
		Size: 146.5 MB (146530843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9d953f0f482d5e71af840bf8428b842de0c4a12942fc809aa4eab8eb09e47eda
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208296245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd067172ee4dd75c541ab606da819a7af951b749a414e5426c0000f8c0da199`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 18:40:26 GMT
ARG version=11.0.10.9-1
# Thu, 21 Jan 2021 18:40:55 GMT
# ARGS: version=11.0.10.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 18:40:57 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 18:40:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03d2b79d43eb79a680e95539063ef30a4e64bb5d44c8ae1f6984f8876a4a8cc`  
		Last Modified: Thu, 21 Jan 2021 18:42:35 GMT  
		Size: 144.6 MB (144588331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:2761a3509de723a1da1b168ae3ed4214a92c0c2a97bab39f2b107910c7cecd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0887fe50a08a79e3a49905496bdc4e4e0ff3a7e46780fd2523baeb7c634b5d80
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208538271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702fddf65318b8961e6d70c184dc9b2420bc7c6c901ed131f096ed5af9e539da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 20:20:09 GMT
ADD file:15991ffbefc01e13f134972ce0eabc6b7901ea9ab4d56347bee5057302cf4848 in / 
# Wed, 23 Dec 2020 20:20:09 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 19:19:56 GMT
ARG version=11.0.10.9-1
# Thu, 21 Jan 2021 19:20:12 GMT
# ARGS: version=11.0.10.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 19:20:12 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:20:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:4232b9ee675bb1f9a32337ec3f266a570b75c54c3c3f173b1abb998e9984ad8c`  
		Last Modified: Wed, 23 Dec 2020 20:21:42 GMT  
		Size: 62.0 MB (62007428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132220740555f6a23e53b52a8be783f695ea89bc701d7aa6eefe5cc9abc31df3`  
		Last Modified: Thu, 21 Jan 2021 19:22:07 GMT  
		Size: 146.5 MB (146530843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9d953f0f482d5e71af840bf8428b842de0c4a12942fc809aa4eab8eb09e47eda
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208296245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd067172ee4dd75c541ab606da819a7af951b749a414e5426c0000f8c0da199`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 18:40:26 GMT
ARG version=11.0.10.9-1
# Thu, 21 Jan 2021 18:40:55 GMT
# ARGS: version=11.0.10.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 18:40:57 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 18:40:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03d2b79d43eb79a680e95539063ef30a4e64bb5d44c8ae1f6984f8876a4a8cc`  
		Last Modified: Thu, 21 Jan 2021 18:42:35 GMT  
		Size: 144.6 MB (144588331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-alpine`

```console
$ docker pull amazoncorretto@sha256:b9d5e959586c21e4d2e5fc1e83eb1b2b5b1dfe9a991a499d26e83956d604264c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dd7e8cb7ba5970b12d36568cbe66162d9c4cd44f8eff8a197be209422ca39234
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195086483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e0d1ca1e0196adfa963a5c4fdcf548b5f5e8afd21039b542d338ef08ed9d18`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 21 Jan 2021 19:20:36 GMT
ARG version=11.0.10.9.1
# Thu, 21 Jan 2021 19:20:43 GMT
# ARGS: version=11.0.10.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Thu, 21 Jan 2021 19:20:43 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:20:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 21 Jan 2021 19:20:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c85d4dd6beb5e76ff7ecf4549e9588d8ae1d73ea6c1045e3b3a6530ff03062b`  
		Last Modified: Thu, 21 Jan 2021 19:23:20 GMT  
		Size: 192.3 MB (192287417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-alpine-full`

```console
$ docker pull amazoncorretto@sha256:b9d5e959586c21e4d2e5fc1e83eb1b2b5b1dfe9a991a499d26e83956d604264c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dd7e8cb7ba5970b12d36568cbe66162d9c4cd44f8eff8a197be209422ca39234
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195086483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e0d1ca1e0196adfa963a5c4fdcf548b5f5e8afd21039b542d338ef08ed9d18`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 21 Jan 2021 19:20:36 GMT
ARG version=11.0.10.9.1
# Thu, 21 Jan 2021 19:20:43 GMT
# ARGS: version=11.0.10.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Thu, 21 Jan 2021 19:20:43 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:20:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 21 Jan 2021 19:20:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c85d4dd6beb5e76ff7ecf4549e9588d8ae1d73ea6c1045e3b3a6530ff03062b`  
		Last Modified: Thu, 21 Jan 2021 19:23:20 GMT  
		Size: 192.3 MB (192287417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:b9d5e959586c21e4d2e5fc1e83eb1b2b5b1dfe9a991a499d26e83956d604264c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dd7e8cb7ba5970b12d36568cbe66162d9c4cd44f8eff8a197be209422ca39234
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195086483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e0d1ca1e0196adfa963a5c4fdcf548b5f5e8afd21039b542d338ef08ed9d18`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 21 Jan 2021 19:20:36 GMT
ARG version=11.0.10.9.1
# Thu, 21 Jan 2021 19:20:43 GMT
# ARGS: version=11.0.10.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Thu, 21 Jan 2021 19:20:43 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:20:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 21 Jan 2021 19:20:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c85d4dd6beb5e76ff7ecf4549e9588d8ae1d73ea6c1045e3b3a6530ff03062b`  
		Last Modified: Thu, 21 Jan 2021 19:23:20 GMT  
		Size: 192.3 MB (192287417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15`

```console
$ docker pull amazoncorretto@sha256:5d44cf594cd4e4de912bc559e5f13b1c36d4b83521216598dbb9e44a4367d25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:15` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3c1e48b8f4425b79d9362dce8c60a88b176dfa21f56376eae85dc35c6749b482
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217674174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a27ac94a60e769b27d4855d5e2323483542468f10499edf1a85ae070366d35`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 20:20:09 GMT
ADD file:15991ffbefc01e13f134972ce0eabc6b7901ea9ab4d56347bee5057302cf4848 in / 
# Wed, 23 Dec 2020 20:20:09 GMT
CMD ["/bin/bash"]
# Fri, 22 Jan 2021 23:20:01 GMT
ARG version=15.0.2.7-1
# Fri, 22 Jan 2021 23:20:19 GMT
# ARGS: version=15.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Jan 2021 23:20:20 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jan 2021 23:20:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:4232b9ee675bb1f9a32337ec3f266a570b75c54c3c3f173b1abb998e9984ad8c`  
		Last Modified: Wed, 23 Dec 2020 20:21:42 GMT  
		Size: 62.0 MB (62007428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75963262766311d0a7d40f30c07fffa202b9e5b32f35d6cfb70ad51ce630e0f6`  
		Last Modified: Fri, 22 Jan 2021 23:21:25 GMT  
		Size: 155.7 MB (155666746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:15` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b6402bb83f45546a8ba0f4b7ed67c1bdb0b179d8ba3a6e22ef168aa345e47537
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219246874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e086e2e140090c710c358ccc49358023e86b0e1f23f38e7a00b15862d7afba7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Fri, 22 Jan 2021 23:39:43 GMT
ARG version=15.0.2.7-1
# Fri, 22 Jan 2021 23:40:19 GMT
# ARGS: version=15.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Jan 2021 23:40:21 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jan 2021 23:40:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97903ed68d862654dd466114bfa7e540200c8cdced49a5d6dc002e7cdd346f38`  
		Last Modified: Fri, 22 Jan 2021 23:41:13 GMT  
		Size: 155.5 MB (155538960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15.0.2`

```console
$ docker pull amazoncorretto@sha256:5d44cf594cd4e4de912bc559e5f13b1c36d4b83521216598dbb9e44a4367d25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:15.0.2` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3c1e48b8f4425b79d9362dce8c60a88b176dfa21f56376eae85dc35c6749b482
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217674174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a27ac94a60e769b27d4855d5e2323483542468f10499edf1a85ae070366d35`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 20:20:09 GMT
ADD file:15991ffbefc01e13f134972ce0eabc6b7901ea9ab4d56347bee5057302cf4848 in / 
# Wed, 23 Dec 2020 20:20:09 GMT
CMD ["/bin/bash"]
# Fri, 22 Jan 2021 23:20:01 GMT
ARG version=15.0.2.7-1
# Fri, 22 Jan 2021 23:20:19 GMT
# ARGS: version=15.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Jan 2021 23:20:20 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jan 2021 23:20:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:4232b9ee675bb1f9a32337ec3f266a570b75c54c3c3f173b1abb998e9984ad8c`  
		Last Modified: Wed, 23 Dec 2020 20:21:42 GMT  
		Size: 62.0 MB (62007428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75963262766311d0a7d40f30c07fffa202b9e5b32f35d6cfb70ad51ce630e0f6`  
		Last Modified: Fri, 22 Jan 2021 23:21:25 GMT  
		Size: 155.7 MB (155666746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:15.0.2` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b6402bb83f45546a8ba0f4b7ed67c1bdb0b179d8ba3a6e22ef168aa345e47537
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219246874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e086e2e140090c710c358ccc49358023e86b0e1f23f38e7a00b15862d7afba7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Fri, 22 Jan 2021 23:39:43 GMT
ARG version=15.0.2.7-1
# Fri, 22 Jan 2021 23:40:19 GMT
# ARGS: version=15.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Jan 2021 23:40:21 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jan 2021 23:40:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97903ed68d862654dd466114bfa7e540200c8cdced49a5d6dc002e7cdd346f38`  
		Last Modified: Fri, 22 Jan 2021 23:41:13 GMT  
		Size: 155.5 MB (155538960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15.0.2-al2`

```console
$ docker pull amazoncorretto@sha256:5d44cf594cd4e4de912bc559e5f13b1c36d4b83521216598dbb9e44a4367d25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:15.0.2-al2` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3c1e48b8f4425b79d9362dce8c60a88b176dfa21f56376eae85dc35c6749b482
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217674174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a27ac94a60e769b27d4855d5e2323483542468f10499edf1a85ae070366d35`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 20:20:09 GMT
ADD file:15991ffbefc01e13f134972ce0eabc6b7901ea9ab4d56347bee5057302cf4848 in / 
# Wed, 23 Dec 2020 20:20:09 GMT
CMD ["/bin/bash"]
# Fri, 22 Jan 2021 23:20:01 GMT
ARG version=15.0.2.7-1
# Fri, 22 Jan 2021 23:20:19 GMT
# ARGS: version=15.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Jan 2021 23:20:20 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jan 2021 23:20:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:4232b9ee675bb1f9a32337ec3f266a570b75c54c3c3f173b1abb998e9984ad8c`  
		Last Modified: Wed, 23 Dec 2020 20:21:42 GMT  
		Size: 62.0 MB (62007428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75963262766311d0a7d40f30c07fffa202b9e5b32f35d6cfb70ad51ce630e0f6`  
		Last Modified: Fri, 22 Jan 2021 23:21:25 GMT  
		Size: 155.7 MB (155666746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:15.0.2-al2` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b6402bb83f45546a8ba0f4b7ed67c1bdb0b179d8ba3a6e22ef168aa345e47537
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219246874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e086e2e140090c710c358ccc49358023e86b0e1f23f38e7a00b15862d7afba7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Fri, 22 Jan 2021 23:39:43 GMT
ARG version=15.0.2.7-1
# Fri, 22 Jan 2021 23:40:19 GMT
# ARGS: version=15.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Jan 2021 23:40:21 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jan 2021 23:40:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97903ed68d862654dd466114bfa7e540200c8cdced49a5d6dc002e7cdd346f38`  
		Last Modified: Fri, 22 Jan 2021 23:41:13 GMT  
		Size: 155.5 MB (155538960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15.0.2-alpine`

```console
$ docker pull amazoncorretto@sha256:91d7a26a3f2a4d3b8dd2ad7fcf08e9cfa6d9aa35a54edd6d3f7b1a5f48d3cfc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:15.0.2-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2edee727b1c760a96dd0d5267dbbd382e797199806ec701708637d73ef908400
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207722795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c34d404df62de60345bc5826297c3c55e10e2aced6060569dea0b200c74041`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Fri, 22 Jan 2021 23:20:26 GMT
ARG version=15.0.2.7.1
# Fri, 22 Jan 2021 23:20:33 GMT
# ARGS: version=15.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-15=$version-r0
# Fri, 22 Jan 2021 23:20:34 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jan 2021 23:20:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 22 Jan 2021 23:20:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283c15272aa4724dc3ab01a3af98281a0c0c7696cd21929df1cd2f7951c411b6`  
		Last Modified: Fri, 22 Jan 2021 23:21:50 GMT  
		Size: 204.9 MB (204923729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15-al2-full`

```console
$ docker pull amazoncorretto@sha256:5d44cf594cd4e4de912bc559e5f13b1c36d4b83521216598dbb9e44a4367d25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:15-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3c1e48b8f4425b79d9362dce8c60a88b176dfa21f56376eae85dc35c6749b482
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217674174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a27ac94a60e769b27d4855d5e2323483542468f10499edf1a85ae070366d35`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 20:20:09 GMT
ADD file:15991ffbefc01e13f134972ce0eabc6b7901ea9ab4d56347bee5057302cf4848 in / 
# Wed, 23 Dec 2020 20:20:09 GMT
CMD ["/bin/bash"]
# Fri, 22 Jan 2021 23:20:01 GMT
ARG version=15.0.2.7-1
# Fri, 22 Jan 2021 23:20:19 GMT
# ARGS: version=15.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Jan 2021 23:20:20 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jan 2021 23:20:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:4232b9ee675bb1f9a32337ec3f266a570b75c54c3c3f173b1abb998e9984ad8c`  
		Last Modified: Wed, 23 Dec 2020 20:21:42 GMT  
		Size: 62.0 MB (62007428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75963262766311d0a7d40f30c07fffa202b9e5b32f35d6cfb70ad51ce630e0f6`  
		Last Modified: Fri, 22 Jan 2021 23:21:25 GMT  
		Size: 155.7 MB (155666746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:15-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b6402bb83f45546a8ba0f4b7ed67c1bdb0b179d8ba3a6e22ef168aa345e47537
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219246874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e086e2e140090c710c358ccc49358023e86b0e1f23f38e7a00b15862d7afba7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Fri, 22 Jan 2021 23:39:43 GMT
ARG version=15.0.2.7-1
# Fri, 22 Jan 2021 23:40:19 GMT
# ARGS: version=15.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Jan 2021 23:40:21 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jan 2021 23:40:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97903ed68d862654dd466114bfa7e540200c8cdced49a5d6dc002e7cdd346f38`  
		Last Modified: Fri, 22 Jan 2021 23:41:13 GMT  
		Size: 155.5 MB (155538960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:5d44cf594cd4e4de912bc559e5f13b1c36d4b83521216598dbb9e44a4367d25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:15-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3c1e48b8f4425b79d9362dce8c60a88b176dfa21f56376eae85dc35c6749b482
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217674174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a27ac94a60e769b27d4855d5e2323483542468f10499edf1a85ae070366d35`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 20:20:09 GMT
ADD file:15991ffbefc01e13f134972ce0eabc6b7901ea9ab4d56347bee5057302cf4848 in / 
# Wed, 23 Dec 2020 20:20:09 GMT
CMD ["/bin/bash"]
# Fri, 22 Jan 2021 23:20:01 GMT
ARG version=15.0.2.7-1
# Fri, 22 Jan 2021 23:20:19 GMT
# ARGS: version=15.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Jan 2021 23:20:20 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jan 2021 23:20:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:4232b9ee675bb1f9a32337ec3f266a570b75c54c3c3f173b1abb998e9984ad8c`  
		Last Modified: Wed, 23 Dec 2020 20:21:42 GMT  
		Size: 62.0 MB (62007428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75963262766311d0a7d40f30c07fffa202b9e5b32f35d6cfb70ad51ce630e0f6`  
		Last Modified: Fri, 22 Jan 2021 23:21:25 GMT  
		Size: 155.7 MB (155666746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:15-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b6402bb83f45546a8ba0f4b7ed67c1bdb0b179d8ba3a6e22ef168aa345e47537
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219246874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e086e2e140090c710c358ccc49358023e86b0e1f23f38e7a00b15862d7afba7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Fri, 22 Jan 2021 23:39:43 GMT
ARG version=15.0.2.7-1
# Fri, 22 Jan 2021 23:40:19 GMT
# ARGS: version=15.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Jan 2021 23:40:21 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jan 2021 23:40:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97903ed68d862654dd466114bfa7e540200c8cdced49a5d6dc002e7cdd346f38`  
		Last Modified: Fri, 22 Jan 2021 23:41:13 GMT  
		Size: 155.5 MB (155538960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15-alpine`

```console
$ docker pull amazoncorretto@sha256:91d7a26a3f2a4d3b8dd2ad7fcf08e9cfa6d9aa35a54edd6d3f7b1a5f48d3cfc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:15-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2edee727b1c760a96dd0d5267dbbd382e797199806ec701708637d73ef908400
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207722795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c34d404df62de60345bc5826297c3c55e10e2aced6060569dea0b200c74041`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Fri, 22 Jan 2021 23:20:26 GMT
ARG version=15.0.2.7.1
# Fri, 22 Jan 2021 23:20:33 GMT
# ARGS: version=15.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-15=$version-r0
# Fri, 22 Jan 2021 23:20:34 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jan 2021 23:20:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 22 Jan 2021 23:20:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283c15272aa4724dc3ab01a3af98281a0c0c7696cd21929df1cd2f7951c411b6`  
		Last Modified: Fri, 22 Jan 2021 23:21:50 GMT  
		Size: 204.9 MB (204923729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15-alpine-full`

```console
$ docker pull amazoncorretto@sha256:91d7a26a3f2a4d3b8dd2ad7fcf08e9cfa6d9aa35a54edd6d3f7b1a5f48d3cfc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:15-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2edee727b1c760a96dd0d5267dbbd382e797199806ec701708637d73ef908400
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207722795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c34d404df62de60345bc5826297c3c55e10e2aced6060569dea0b200c74041`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Fri, 22 Jan 2021 23:20:26 GMT
ARG version=15.0.2.7.1
# Fri, 22 Jan 2021 23:20:33 GMT
# ARGS: version=15.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-15=$version-r0
# Fri, 22 Jan 2021 23:20:34 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jan 2021 23:20:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 22 Jan 2021 23:20:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283c15272aa4724dc3ab01a3af98281a0c0c7696cd21929df1cd2f7951c411b6`  
		Last Modified: Fri, 22 Jan 2021 23:21:50 GMT  
		Size: 204.9 MB (204923729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:91d7a26a3f2a4d3b8dd2ad7fcf08e9cfa6d9aa35a54edd6d3f7b1a5f48d3cfc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:15-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2edee727b1c760a96dd0d5267dbbd382e797199806ec701708637d73ef908400
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207722795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c34d404df62de60345bc5826297c3c55e10e2aced6060569dea0b200c74041`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Fri, 22 Jan 2021 23:20:26 GMT
ARG version=15.0.2.7.1
# Fri, 22 Jan 2021 23:20:33 GMT
# ARGS: version=15.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-15=$version-r0
# Fri, 22 Jan 2021 23:20:34 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jan 2021 23:20:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 22 Jan 2021 23:20:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283c15272aa4724dc3ab01a3af98281a0c0c7696cd21929df1cd2f7951c411b6`  
		Last Modified: Fri, 22 Jan 2021 23:21:50 GMT  
		Size: 204.9 MB (204923729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8`

```console
$ docker pull amazoncorretto@sha256:0de32cab53565592434db5368a580060daa176f14daee0635f44524511560bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:59c8903ef83ed1f10cd55047666a029088bff338c4ae972cfc40187f880d6a51
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137284163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e72afafb4d20afe3d117fd70a544e8e97d0074185838573d16214da6c67dda0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 20:20:09 GMT
ADD file:15991ffbefc01e13f134972ce0eabc6b7901ea9ab4d56347bee5057302cf4848 in / 
# Wed, 23 Dec 2020 20:20:09 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 19:19:37 GMT
ARG version=1.8.0_282.b08-1
# Thu, 21 Jan 2021 19:19:51 GMT
# ARGS: version=1.8.0_282.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 19:19:51 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:19:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:4232b9ee675bb1f9a32337ec3f266a570b75c54c3c3f173b1abb998e9984ad8c`  
		Last Modified: Wed, 23 Dec 2020 20:21:42 GMT  
		Size: 62.0 MB (62007428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638373d2fdada0614a24cd0be71916ad9ea4352fef0d34bdbad351b04607dbc3`  
		Last Modified: Thu, 21 Jan 2021 19:21:40 GMT  
		Size: 75.3 MB (75276735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:481d7d20235deae616ffe6c47d252710641c2ec206e60f03e9c852b7e052a208
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123054872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d715113edd46309a55014ebe016e5deb142aefc371342c1afaf23af21d075edf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 18:39:41 GMT
ARG version=1.8.0_282.b08-1
# Thu, 21 Jan 2021 18:40:14 GMT
# ARGS: version=1.8.0_282.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 18:40:15 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 18:40:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb58219db59f1e5124e1253221af1a76e61b1327094d34728bc493a7b761bd0`  
		Last Modified: Thu, 21 Jan 2021 18:41:54 GMT  
		Size: 59.3 MB (59346958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:0de32cab53565592434db5368a580060daa176f14daee0635f44524511560bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:59c8903ef83ed1f10cd55047666a029088bff338c4ae972cfc40187f880d6a51
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137284163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e72afafb4d20afe3d117fd70a544e8e97d0074185838573d16214da6c67dda0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 20:20:09 GMT
ADD file:15991ffbefc01e13f134972ce0eabc6b7901ea9ab4d56347bee5057302cf4848 in / 
# Wed, 23 Dec 2020 20:20:09 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 19:19:37 GMT
ARG version=1.8.0_282.b08-1
# Thu, 21 Jan 2021 19:19:51 GMT
# ARGS: version=1.8.0_282.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 19:19:51 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:19:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:4232b9ee675bb1f9a32337ec3f266a570b75c54c3c3f173b1abb998e9984ad8c`  
		Last Modified: Wed, 23 Dec 2020 20:21:42 GMT  
		Size: 62.0 MB (62007428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638373d2fdada0614a24cd0be71916ad9ea4352fef0d34bdbad351b04607dbc3`  
		Last Modified: Thu, 21 Jan 2021 19:21:40 GMT  
		Size: 75.3 MB (75276735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:481d7d20235deae616ffe6c47d252710641c2ec206e60f03e9c852b7e052a208
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123054872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d715113edd46309a55014ebe016e5deb142aefc371342c1afaf23af21d075edf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 18:39:41 GMT
ARG version=1.8.0_282.b08-1
# Thu, 21 Jan 2021 18:40:14 GMT
# ARGS: version=1.8.0_282.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 18:40:15 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 18:40:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb58219db59f1e5124e1253221af1a76e61b1327094d34728bc493a7b761bd0`  
		Last Modified: Thu, 21 Jan 2021 18:41:54 GMT  
		Size: 59.3 MB (59346958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:0de32cab53565592434db5368a580060daa176f14daee0635f44524511560bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:59c8903ef83ed1f10cd55047666a029088bff338c4ae972cfc40187f880d6a51
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137284163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e72afafb4d20afe3d117fd70a544e8e97d0074185838573d16214da6c67dda0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 20:20:09 GMT
ADD file:15991ffbefc01e13f134972ce0eabc6b7901ea9ab4d56347bee5057302cf4848 in / 
# Wed, 23 Dec 2020 20:20:09 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 19:19:37 GMT
ARG version=1.8.0_282.b08-1
# Thu, 21 Jan 2021 19:19:51 GMT
# ARGS: version=1.8.0_282.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 19:19:51 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:19:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:4232b9ee675bb1f9a32337ec3f266a570b75c54c3c3f173b1abb998e9984ad8c`  
		Last Modified: Wed, 23 Dec 2020 20:21:42 GMT  
		Size: 62.0 MB (62007428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638373d2fdada0614a24cd0be71916ad9ea4352fef0d34bdbad351b04607dbc3`  
		Last Modified: Thu, 21 Jan 2021 19:21:40 GMT  
		Size: 75.3 MB (75276735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:481d7d20235deae616ffe6c47d252710641c2ec206e60f03e9c852b7e052a208
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123054872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d715113edd46309a55014ebe016e5deb142aefc371342c1afaf23af21d075edf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 18:39:41 GMT
ARG version=1.8.0_282.b08-1
# Thu, 21 Jan 2021 18:40:14 GMT
# ARGS: version=1.8.0_282.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 18:40:15 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 18:40:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb58219db59f1e5124e1253221af1a76e61b1327094d34728bc493a7b761bd0`  
		Last Modified: Thu, 21 Jan 2021 18:41:54 GMT  
		Size: 59.3 MB (59346958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-alpine`

```console
$ docker pull amazoncorretto@sha256:bfe9b77d5ec4f4083cf1db58ea06c7404c193f1f7589a37073f501716e39bb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c816e1cf210b0638c68d0b2b2323835ccf2775eff15920c9632a89a7f19cdf45
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101783426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578c324b3a924889de20419aa30535ec714f24223bf6cc698fbc80234a919bef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 21 Jan 2021 19:20:18 GMT
ARG version=8.282.08.1
# Thu, 21 Jan 2021 19:20:23 GMT
# ARGS: version=8.282.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Thu, 21 Jan 2021 19:20:23 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:20:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 21 Jan 2021 19:20:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5540e4aac0d3797e100a2625f1fe943bff0aca8b0da1330d1002097ba1155ca0`  
		Last Modified: Thu, 21 Jan 2021 19:22:30 GMT  
		Size: 99.0 MB (98984360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-alpine-full`

```console
$ docker pull amazoncorretto@sha256:bfe9b77d5ec4f4083cf1db58ea06c7404c193f1f7589a37073f501716e39bb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c816e1cf210b0638c68d0b2b2323835ccf2775eff15920c9632a89a7f19cdf45
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101783426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578c324b3a924889de20419aa30535ec714f24223bf6cc698fbc80234a919bef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 21 Jan 2021 19:20:18 GMT
ARG version=8.282.08.1
# Thu, 21 Jan 2021 19:20:23 GMT
# ARGS: version=8.282.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Thu, 21 Jan 2021 19:20:23 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:20:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 21 Jan 2021 19:20:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5540e4aac0d3797e100a2625f1fe943bff0aca8b0da1330d1002097ba1155ca0`  
		Last Modified: Thu, 21 Jan 2021 19:22:30 GMT  
		Size: 99.0 MB (98984360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:bfe9b77d5ec4f4083cf1db58ea06c7404c193f1f7589a37073f501716e39bb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c816e1cf210b0638c68d0b2b2323835ccf2775eff15920c9632a89a7f19cdf45
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101783426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578c324b3a924889de20419aa30535ec714f24223bf6cc698fbc80234a919bef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 21 Jan 2021 19:20:18 GMT
ARG version=8.282.08.1
# Thu, 21 Jan 2021 19:20:23 GMT
# ARGS: version=8.282.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Thu, 21 Jan 2021 19:20:23 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:20:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 21 Jan 2021 19:20:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5540e4aac0d3797e100a2625f1fe943bff0aca8b0da1330d1002097ba1155ca0`  
		Last Modified: Thu, 21 Jan 2021 19:22:30 GMT  
		Size: 99.0 MB (98984360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:2a9b8456e2be4b7800bc2fa211ae96ee0012837dfa3244450446388a1b5070a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:535b615bf745b687d051723208e32aaed7cc261887023d768d74e9ff57790a0b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43115036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f7ef31b78fe3dbd53785d3c1c6de44d20487e98001f25613719e1af3f36b43`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 21 Jan 2021 19:20:18 GMT
ARG version=8.282.08.1
# Thu, 21 Jan 2021 19:20:31 GMT
# ARGS: version=8.282.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Thu, 21 Jan 2021 19:20:31 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:20:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50eef058fea4bf48f1b6db08ac87bc5f9616790b21fc46c2a2ea241fbe87d983`  
		Last Modified: Thu, 21 Jan 2021 19:22:47 GMT  
		Size: 40.3 MB (40315970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u282`

```console
$ docker pull amazoncorretto@sha256:0de32cab53565592434db5368a580060daa176f14daee0635f44524511560bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8u282` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:59c8903ef83ed1f10cd55047666a029088bff338c4ae972cfc40187f880d6a51
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137284163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e72afafb4d20afe3d117fd70a544e8e97d0074185838573d16214da6c67dda0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 20:20:09 GMT
ADD file:15991ffbefc01e13f134972ce0eabc6b7901ea9ab4d56347bee5057302cf4848 in / 
# Wed, 23 Dec 2020 20:20:09 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 19:19:37 GMT
ARG version=1.8.0_282.b08-1
# Thu, 21 Jan 2021 19:19:51 GMT
# ARGS: version=1.8.0_282.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 19:19:51 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:19:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:4232b9ee675bb1f9a32337ec3f266a570b75c54c3c3f173b1abb998e9984ad8c`  
		Last Modified: Wed, 23 Dec 2020 20:21:42 GMT  
		Size: 62.0 MB (62007428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638373d2fdada0614a24cd0be71916ad9ea4352fef0d34bdbad351b04607dbc3`  
		Last Modified: Thu, 21 Jan 2021 19:21:40 GMT  
		Size: 75.3 MB (75276735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8u282` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:481d7d20235deae616ffe6c47d252710641c2ec206e60f03e9c852b7e052a208
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123054872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d715113edd46309a55014ebe016e5deb142aefc371342c1afaf23af21d075edf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 18:39:41 GMT
ARG version=1.8.0_282.b08-1
# Thu, 21 Jan 2021 18:40:14 GMT
# ARGS: version=1.8.0_282.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 18:40:15 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 18:40:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb58219db59f1e5124e1253221af1a76e61b1327094d34728bc493a7b761bd0`  
		Last Modified: Thu, 21 Jan 2021 18:41:54 GMT  
		Size: 59.3 MB (59346958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u282-al2`

```console
$ docker pull amazoncorretto@sha256:0de32cab53565592434db5368a580060daa176f14daee0635f44524511560bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8u282-al2` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:59c8903ef83ed1f10cd55047666a029088bff338c4ae972cfc40187f880d6a51
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137284163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e72afafb4d20afe3d117fd70a544e8e97d0074185838573d16214da6c67dda0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 20:20:09 GMT
ADD file:15991ffbefc01e13f134972ce0eabc6b7901ea9ab4d56347bee5057302cf4848 in / 
# Wed, 23 Dec 2020 20:20:09 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 19:19:37 GMT
ARG version=1.8.0_282.b08-1
# Thu, 21 Jan 2021 19:19:51 GMT
# ARGS: version=1.8.0_282.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 19:19:51 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:19:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:4232b9ee675bb1f9a32337ec3f266a570b75c54c3c3f173b1abb998e9984ad8c`  
		Last Modified: Wed, 23 Dec 2020 20:21:42 GMT  
		Size: 62.0 MB (62007428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638373d2fdada0614a24cd0be71916ad9ea4352fef0d34bdbad351b04607dbc3`  
		Last Modified: Thu, 21 Jan 2021 19:21:40 GMT  
		Size: 75.3 MB (75276735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8u282-al2` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:481d7d20235deae616ffe6c47d252710641c2ec206e60f03e9c852b7e052a208
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123054872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d715113edd46309a55014ebe016e5deb142aefc371342c1afaf23af21d075edf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 18:39:41 GMT
ARG version=1.8.0_282.b08-1
# Thu, 21 Jan 2021 18:40:14 GMT
# ARGS: version=1.8.0_282.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 18:40:15 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 18:40:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb58219db59f1e5124e1253221af1a76e61b1327094d34728bc493a7b761bd0`  
		Last Modified: Thu, 21 Jan 2021 18:41:54 GMT  
		Size: 59.3 MB (59346958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u282-alpine`

```console
$ docker pull amazoncorretto@sha256:bfe9b77d5ec4f4083cf1db58ea06c7404c193f1f7589a37073f501716e39bb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8u282-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c816e1cf210b0638c68d0b2b2323835ccf2775eff15920c9632a89a7f19cdf45
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101783426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578c324b3a924889de20419aa30535ec714f24223bf6cc698fbc80234a919bef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 21 Jan 2021 19:20:18 GMT
ARG version=8.282.08.1
# Thu, 21 Jan 2021 19:20:23 GMT
# ARGS: version=8.282.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Thu, 21 Jan 2021 19:20:23 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:20:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 21 Jan 2021 19:20:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5540e4aac0d3797e100a2625f1fe943bff0aca8b0da1330d1002097ba1155ca0`  
		Last Modified: Thu, 21 Jan 2021 19:22:30 GMT  
		Size: 99.0 MB (98984360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u282-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:2a9b8456e2be4b7800bc2fa211ae96ee0012837dfa3244450446388a1b5070a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8u282-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:535b615bf745b687d051723208e32aaed7cc261887023d768d74e9ff57790a0b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43115036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f7ef31b78fe3dbd53785d3c1c6de44d20487e98001f25613719e1af3f36b43`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 21 Jan 2021 19:20:18 GMT
ARG version=8.282.08.1
# Thu, 21 Jan 2021 19:20:31 GMT
# ARGS: version=8.282.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Thu, 21 Jan 2021 19:20:31 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:20:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50eef058fea4bf48f1b6db08ac87bc5f9616790b21fc46c2a2ea241fbe87d983`  
		Last Modified: Thu, 21 Jan 2021 19:22:47 GMT  
		Size: 40.3 MB (40315970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:0de32cab53565592434db5368a580060daa176f14daee0635f44524511560bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:59c8903ef83ed1f10cd55047666a029088bff338c4ae972cfc40187f880d6a51
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137284163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e72afafb4d20afe3d117fd70a544e8e97d0074185838573d16214da6c67dda0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 20:20:09 GMT
ADD file:15991ffbefc01e13f134972ce0eabc6b7901ea9ab4d56347bee5057302cf4848 in / 
# Wed, 23 Dec 2020 20:20:09 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 19:19:37 GMT
ARG version=1.8.0_282.b08-1
# Thu, 21 Jan 2021 19:19:51 GMT
# ARGS: version=1.8.0_282.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 19:19:51 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 19:19:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:4232b9ee675bb1f9a32337ec3f266a570b75c54c3c3f173b1abb998e9984ad8c`  
		Last Modified: Wed, 23 Dec 2020 20:21:42 GMT  
		Size: 62.0 MB (62007428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638373d2fdada0614a24cd0be71916ad9ea4352fef0d34bdbad351b04607dbc3`  
		Last Modified: Thu, 21 Jan 2021 19:21:40 GMT  
		Size: 75.3 MB (75276735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:latest` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:481d7d20235deae616ffe6c47d252710641c2ec206e60f03e9c852b7e052a208
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123054872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d715113edd46309a55014ebe016e5deb142aefc371342c1afaf23af21d075edf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 18:39:41 GMT
ARG version=1.8.0_282.b08-1
# Thu, 21 Jan 2021 18:40:14 GMT
# ARGS: version=1.8.0_282.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Jan 2021 18:40:15 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 18:40:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb58219db59f1e5124e1253221af1a76e61b1327094d34728bc493a7b761bd0`  
		Last Modified: Thu, 21 Jan 2021 18:41:54 GMT  
		Size: 59.3 MB (59346958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
