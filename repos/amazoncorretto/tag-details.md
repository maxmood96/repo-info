<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazoncorretto`

-	[`amazoncorretto:11`](#amazoncorretto11)
-	[`amazoncorretto:11-al2-full`](#amazoncorretto11-al2-full)
-	[`amazoncorretto:11-al2-jdk`](#amazoncorretto11-al2-jdk)
-	[`amazoncorretto:11-alpine`](#amazoncorretto11-alpine)
-	[`amazoncorretto:11-alpine-full`](#amazoncorretto11-alpine-full)
-	[`amazoncorretto:11-alpine-jdk`](#amazoncorretto11-alpine-jdk)
-	[`amazoncorretto:11.0.11`](#amazoncorretto11011)
-	[`amazoncorretto:11.0.11-al2`](#amazoncorretto11011-al2)
-	[`amazoncorretto:11.0.11-alpine`](#amazoncorretto11011-alpine)
-	[`amazoncorretto:16`](#amazoncorretto16)
-	[`amazoncorretto:16-al2-full`](#amazoncorretto16-al2-full)
-	[`amazoncorretto:16-al2-jdk`](#amazoncorretto16-al2-jdk)
-	[`amazoncorretto:16-alpine`](#amazoncorretto16-alpine)
-	[`amazoncorretto:16-alpine-full`](#amazoncorretto16-alpine-full)
-	[`amazoncorretto:16-alpine-jdk`](#amazoncorretto16-alpine-jdk)
-	[`amazoncorretto:16.0.1`](#amazoncorretto1601)
-	[`amazoncorretto:16.0.1-al2`](#amazoncorretto1601-al2)
-	[`amazoncorretto:16.0.1-alpine`](#amazoncorretto1601-alpine)
-	[`amazoncorretto:8`](#amazoncorretto8)
-	[`amazoncorretto:8-al2-full`](#amazoncorretto8-al2-full)
-	[`amazoncorretto:8-al2-jdk`](#amazoncorretto8-al2-jdk)
-	[`amazoncorretto:8-alpine`](#amazoncorretto8-alpine)
-	[`amazoncorretto:8-alpine-full`](#amazoncorretto8-alpine-full)
-	[`amazoncorretto:8-alpine-jdk`](#amazoncorretto8-alpine-jdk)
-	[`amazoncorretto:8-alpine-jre`](#amazoncorretto8-alpine-jre)
-	[`amazoncorretto:8u292`](#amazoncorretto8u292)
-	[`amazoncorretto:8u292-al2`](#amazoncorretto8u292-al2)
-	[`amazoncorretto:8u292-alpine`](#amazoncorretto8u292-alpine)
-	[`amazoncorretto:8u292-alpine-jre`](#amazoncorretto8u292-alpine-jre)
-	[`amazoncorretto:latest`](#amazoncorrettolatest)

## `amazoncorretto:11`

```console
$ docker pull amazoncorretto@sha256:46c36a4ff51b2086ca3db1d2bdeb4301639b9b6d0dc6a95ce9fca092adb6b935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5dc3bce6711ac7a3f904219451ce3e09b0b5620454843b5aefaa106c15de6071
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208606062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2ad6213ef5d93db9f40d4dbaddb3a50a152c29658295da045fa582336f696b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:38:48 GMT
ARG version=11.0.11.9-1
# Mon, 14 Jun 2021 22:39:13 GMT
# ARGS: version=11.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:39:13 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b37e01106c98e894c76d05de2f709ac3a06a7f0af9da36b6e845a2e33b7f85`  
		Last Modified: Mon, 14 Jun 2021 22:41:06 GMT  
		Size: 146.7 MB (146657005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4af2e3844c234ea30d30450d4b118edb9fbde9ee34621e4408b99f4fd81202ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208194948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b2d496558e2f4e95ba67ca976f0bd29cd9f81d1ecbabfad85b3e26eead4b23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:56:55 GMT
ARG version=11.0.11.9-1
# Mon, 14 Jun 2021 22:57:19 GMT
# ARGS: version=11.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:57:19 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:57:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de1e45995d71f78ff46702cbd7e7d0c754917bc9856f439f5f6d7820335afb7`  
		Last Modified: Mon, 14 Jun 2021 22:59:17 GMT  
		Size: 144.7 MB (144746421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:46c36a4ff51b2086ca3db1d2bdeb4301639b9b6d0dc6a95ce9fca092adb6b935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5dc3bce6711ac7a3f904219451ce3e09b0b5620454843b5aefaa106c15de6071
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208606062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2ad6213ef5d93db9f40d4dbaddb3a50a152c29658295da045fa582336f696b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:38:48 GMT
ARG version=11.0.11.9-1
# Mon, 14 Jun 2021 22:39:13 GMT
# ARGS: version=11.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:39:13 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b37e01106c98e894c76d05de2f709ac3a06a7f0af9da36b6e845a2e33b7f85`  
		Last Modified: Mon, 14 Jun 2021 22:41:06 GMT  
		Size: 146.7 MB (146657005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4af2e3844c234ea30d30450d4b118edb9fbde9ee34621e4408b99f4fd81202ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208194948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b2d496558e2f4e95ba67ca976f0bd29cd9f81d1ecbabfad85b3e26eead4b23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:56:55 GMT
ARG version=11.0.11.9-1
# Mon, 14 Jun 2021 22:57:19 GMT
# ARGS: version=11.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:57:19 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:57:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de1e45995d71f78ff46702cbd7e7d0c754917bc9856f439f5f6d7820335afb7`  
		Last Modified: Mon, 14 Jun 2021 22:59:17 GMT  
		Size: 144.7 MB (144746421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:46c36a4ff51b2086ca3db1d2bdeb4301639b9b6d0dc6a95ce9fca092adb6b935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5dc3bce6711ac7a3f904219451ce3e09b0b5620454843b5aefaa106c15de6071
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208606062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2ad6213ef5d93db9f40d4dbaddb3a50a152c29658295da045fa582336f696b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:38:48 GMT
ARG version=11.0.11.9-1
# Mon, 14 Jun 2021 22:39:13 GMT
# ARGS: version=11.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:39:13 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b37e01106c98e894c76d05de2f709ac3a06a7f0af9da36b6e845a2e33b7f85`  
		Last Modified: Mon, 14 Jun 2021 22:41:06 GMT  
		Size: 146.7 MB (146657005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4af2e3844c234ea30d30450d4b118edb9fbde9ee34621e4408b99f4fd81202ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208194948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b2d496558e2f4e95ba67ca976f0bd29cd9f81d1ecbabfad85b3e26eead4b23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:56:55 GMT
ARG version=11.0.11.9-1
# Mon, 14 Jun 2021 22:57:19 GMT
# ARGS: version=11.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:57:19 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:57:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de1e45995d71f78ff46702cbd7e7d0c754917bc9856f439f5f6d7820335afb7`  
		Last Modified: Mon, 14 Jun 2021 22:59:17 GMT  
		Size: 144.7 MB (144746421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-alpine`

```console
$ docker pull amazoncorretto@sha256:35e8797e008eac2e05264c8a3894767b8cd4661ddca0837db1df7795d142ed1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4201449d2c1ccd174ed6dd41ec90d21a88e5d12ef00e30ba29a1d642b7bc3a0b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196029750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a895b16a7e33d9d36955302d1cd0844f09db71db7afac4b94263a3d347419c3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Tue, 20 Apr 2021 23:20:30 GMT
ARG version=11.0.11.9.1
# Tue, 20 Apr 2021 23:20:37 GMT
# ARGS: version=11.0.11.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Tue, 20 Apr 2021 23:20:37 GMT
ENV LANG=C.UTF-8
# Tue, 20 Apr 2021 23:20:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 20 Apr 2021 23:20:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2531042875644865f91c5f2fa487ccced5f1edb710eb483a2f11059a879156`  
		Last Modified: Tue, 20 Apr 2021 23:23:14 GMT  
		Size: 193.2 MB (193229183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-alpine-full`

```console
$ docker pull amazoncorretto@sha256:35e8797e008eac2e05264c8a3894767b8cd4661ddca0837db1df7795d142ed1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4201449d2c1ccd174ed6dd41ec90d21a88e5d12ef00e30ba29a1d642b7bc3a0b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196029750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a895b16a7e33d9d36955302d1cd0844f09db71db7afac4b94263a3d347419c3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Tue, 20 Apr 2021 23:20:30 GMT
ARG version=11.0.11.9.1
# Tue, 20 Apr 2021 23:20:37 GMT
# ARGS: version=11.0.11.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Tue, 20 Apr 2021 23:20:37 GMT
ENV LANG=C.UTF-8
# Tue, 20 Apr 2021 23:20:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 20 Apr 2021 23:20:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2531042875644865f91c5f2fa487ccced5f1edb710eb483a2f11059a879156`  
		Last Modified: Tue, 20 Apr 2021 23:23:14 GMT  
		Size: 193.2 MB (193229183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:35e8797e008eac2e05264c8a3894767b8cd4661ddca0837db1df7795d142ed1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4201449d2c1ccd174ed6dd41ec90d21a88e5d12ef00e30ba29a1d642b7bc3a0b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196029750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a895b16a7e33d9d36955302d1cd0844f09db71db7afac4b94263a3d347419c3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Tue, 20 Apr 2021 23:20:30 GMT
ARG version=11.0.11.9.1
# Tue, 20 Apr 2021 23:20:37 GMT
# ARGS: version=11.0.11.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Tue, 20 Apr 2021 23:20:37 GMT
ENV LANG=C.UTF-8
# Tue, 20 Apr 2021 23:20:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 20 Apr 2021 23:20:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2531042875644865f91c5f2fa487ccced5f1edb710eb483a2f11059a879156`  
		Last Modified: Tue, 20 Apr 2021 23:23:14 GMT  
		Size: 193.2 MB (193229183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11.0.11`

```console
$ docker pull amazoncorretto@sha256:46c36a4ff51b2086ca3db1d2bdeb4301639b9b6d0dc6a95ce9fca092adb6b935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11.0.11` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5dc3bce6711ac7a3f904219451ce3e09b0b5620454843b5aefaa106c15de6071
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208606062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2ad6213ef5d93db9f40d4dbaddb3a50a152c29658295da045fa582336f696b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:38:48 GMT
ARG version=11.0.11.9-1
# Mon, 14 Jun 2021 22:39:13 GMT
# ARGS: version=11.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:39:13 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b37e01106c98e894c76d05de2f709ac3a06a7f0af9da36b6e845a2e33b7f85`  
		Last Modified: Mon, 14 Jun 2021 22:41:06 GMT  
		Size: 146.7 MB (146657005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11.0.11` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4af2e3844c234ea30d30450d4b118edb9fbde9ee34621e4408b99f4fd81202ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208194948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b2d496558e2f4e95ba67ca976f0bd29cd9f81d1ecbabfad85b3e26eead4b23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:56:55 GMT
ARG version=11.0.11.9-1
# Mon, 14 Jun 2021 22:57:19 GMT
# ARGS: version=11.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:57:19 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:57:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de1e45995d71f78ff46702cbd7e7d0c754917bc9856f439f5f6d7820335afb7`  
		Last Modified: Mon, 14 Jun 2021 22:59:17 GMT  
		Size: 144.7 MB (144746421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11.0.11-al2`

```console
$ docker pull amazoncorretto@sha256:46c36a4ff51b2086ca3db1d2bdeb4301639b9b6d0dc6a95ce9fca092adb6b935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11.0.11-al2` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5dc3bce6711ac7a3f904219451ce3e09b0b5620454843b5aefaa106c15de6071
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208606062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2ad6213ef5d93db9f40d4dbaddb3a50a152c29658295da045fa582336f696b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:38:48 GMT
ARG version=11.0.11.9-1
# Mon, 14 Jun 2021 22:39:13 GMT
# ARGS: version=11.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:39:13 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b37e01106c98e894c76d05de2f709ac3a06a7f0af9da36b6e845a2e33b7f85`  
		Last Modified: Mon, 14 Jun 2021 22:41:06 GMT  
		Size: 146.7 MB (146657005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11.0.11-al2` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4af2e3844c234ea30d30450d4b118edb9fbde9ee34621e4408b99f4fd81202ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208194948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b2d496558e2f4e95ba67ca976f0bd29cd9f81d1ecbabfad85b3e26eead4b23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:56:55 GMT
ARG version=11.0.11.9-1
# Mon, 14 Jun 2021 22:57:19 GMT
# ARGS: version=11.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:57:19 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:57:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de1e45995d71f78ff46702cbd7e7d0c754917bc9856f439f5f6d7820335afb7`  
		Last Modified: Mon, 14 Jun 2021 22:59:17 GMT  
		Size: 144.7 MB (144746421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11.0.11-alpine`

```console
$ docker pull amazoncorretto@sha256:35e8797e008eac2e05264c8a3894767b8cd4661ddca0837db1df7795d142ed1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11.0.11-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4201449d2c1ccd174ed6dd41ec90d21a88e5d12ef00e30ba29a1d642b7bc3a0b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196029750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a895b16a7e33d9d36955302d1cd0844f09db71db7afac4b94263a3d347419c3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Tue, 20 Apr 2021 23:20:30 GMT
ARG version=11.0.11.9.1
# Tue, 20 Apr 2021 23:20:37 GMT
# ARGS: version=11.0.11.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Tue, 20 Apr 2021 23:20:37 GMT
ENV LANG=C.UTF-8
# Tue, 20 Apr 2021 23:20:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 20 Apr 2021 23:20:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2531042875644865f91c5f2fa487ccced5f1edb710eb483a2f11059a879156`  
		Last Modified: Tue, 20 Apr 2021 23:23:14 GMT  
		Size: 193.2 MB (193229183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:16`

```console
$ docker pull amazoncorretto@sha256:c90f9338d8a1a5788db2c77ea853cb4bdbafb3a953ea08eed9ecc75644f30a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:16` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7d3c4763c0e2abf1ea6a92e262afc1a64abed49301879fac76c957aacc91d89f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221892540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a852bea8bc07f33ee743060e9fcc79e6fc00332872c62ba7b655749e72b47b51`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:39:26 GMT
ARG version=16.0.1.9-1
# Mon, 14 Jun 2021 22:39:48 GMT
# ARGS: version=16.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:39:49 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:39:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d47f3a5aebc9df1b6beb67ad88ecf895637897682242d0cefb068414e38e606`  
		Last Modified: Mon, 14 Jun 2021 22:41:42 GMT  
		Size: 159.9 MB (159943483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:16` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e9ddd09da77249483478a40b89a033b0c13f94f2a359931e751e75c7a8d81fc2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223376292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359d42b7f71821497a2bb49bb81a67a62dd100c6c73b7184136e2e3943666ae8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:57:26 GMT
ARG version=16.0.1.9-1
# Mon, 14 Jun 2021 22:57:47 GMT
# ARGS: version=16.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:57:48 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:57:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94b510dae9b488c119034982e25017574f0769cd7d8b9c193e8981a7646541d`  
		Last Modified: Mon, 14 Jun 2021 22:59:55 GMT  
		Size: 159.9 MB (159927765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:16-al2-full`

```console
$ docker pull amazoncorretto@sha256:c90f9338d8a1a5788db2c77ea853cb4bdbafb3a953ea08eed9ecc75644f30a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:16-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7d3c4763c0e2abf1ea6a92e262afc1a64abed49301879fac76c957aacc91d89f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221892540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a852bea8bc07f33ee743060e9fcc79e6fc00332872c62ba7b655749e72b47b51`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:39:26 GMT
ARG version=16.0.1.9-1
# Mon, 14 Jun 2021 22:39:48 GMT
# ARGS: version=16.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:39:49 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:39:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d47f3a5aebc9df1b6beb67ad88ecf895637897682242d0cefb068414e38e606`  
		Last Modified: Mon, 14 Jun 2021 22:41:42 GMT  
		Size: 159.9 MB (159943483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:16-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e9ddd09da77249483478a40b89a033b0c13f94f2a359931e751e75c7a8d81fc2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223376292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359d42b7f71821497a2bb49bb81a67a62dd100c6c73b7184136e2e3943666ae8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:57:26 GMT
ARG version=16.0.1.9-1
# Mon, 14 Jun 2021 22:57:47 GMT
# ARGS: version=16.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:57:48 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:57:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94b510dae9b488c119034982e25017574f0769cd7d8b9c193e8981a7646541d`  
		Last Modified: Mon, 14 Jun 2021 22:59:55 GMT  
		Size: 159.9 MB (159927765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:16-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:c90f9338d8a1a5788db2c77ea853cb4bdbafb3a953ea08eed9ecc75644f30a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:16-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7d3c4763c0e2abf1ea6a92e262afc1a64abed49301879fac76c957aacc91d89f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221892540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a852bea8bc07f33ee743060e9fcc79e6fc00332872c62ba7b655749e72b47b51`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:39:26 GMT
ARG version=16.0.1.9-1
# Mon, 14 Jun 2021 22:39:48 GMT
# ARGS: version=16.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:39:49 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:39:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d47f3a5aebc9df1b6beb67ad88ecf895637897682242d0cefb068414e38e606`  
		Last Modified: Mon, 14 Jun 2021 22:41:42 GMT  
		Size: 159.9 MB (159943483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:16-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e9ddd09da77249483478a40b89a033b0c13f94f2a359931e751e75c7a8d81fc2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223376292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359d42b7f71821497a2bb49bb81a67a62dd100c6c73b7184136e2e3943666ae8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:57:26 GMT
ARG version=16.0.1.9-1
# Mon, 14 Jun 2021 22:57:47 GMT
# ARGS: version=16.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:57:48 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:57:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94b510dae9b488c119034982e25017574f0769cd7d8b9c193e8981a7646541d`  
		Last Modified: Mon, 14 Jun 2021 22:59:55 GMT  
		Size: 159.9 MB (159927765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:16-alpine`

```console
$ docker pull amazoncorretto@sha256:da67cfe4028e29830be8096e81fb46e44cee2481c529b066663808b76947ebf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:16-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:404f02e2ef1cc041b323a7976f631917badeec3b4d43f8ae5b0f0361dab0439e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212433843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2ad03654b54cda4c95f8b862f1f47b7c0e9287be30ce020dfb51973ae161c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Sat, 24 Apr 2021 04:41:25 GMT
ARG version=16.0.1.9.1
# Sat, 24 Apr 2021 04:41:33 GMT
# ARGS: version=16.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-16=$version-r0
# Sat, 24 Apr 2021 04:41:33 GMT
ENV LANG=C.UTF-8
# Sat, 24 Apr 2021 04:41:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 24 Apr 2021 04:41:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5d31824e596a5e7174f37f27e0af4babbe7745e7a1eb51f3ee8bc2ee3dcdbe`  
		Last Modified: Sat, 24 Apr 2021 04:43:04 GMT  
		Size: 209.6 MB (209633276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:16-alpine-full`

```console
$ docker pull amazoncorretto@sha256:da67cfe4028e29830be8096e81fb46e44cee2481c529b066663808b76947ebf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:16-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:404f02e2ef1cc041b323a7976f631917badeec3b4d43f8ae5b0f0361dab0439e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212433843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2ad03654b54cda4c95f8b862f1f47b7c0e9287be30ce020dfb51973ae161c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Sat, 24 Apr 2021 04:41:25 GMT
ARG version=16.0.1.9.1
# Sat, 24 Apr 2021 04:41:33 GMT
# ARGS: version=16.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-16=$version-r0
# Sat, 24 Apr 2021 04:41:33 GMT
ENV LANG=C.UTF-8
# Sat, 24 Apr 2021 04:41:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 24 Apr 2021 04:41:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5d31824e596a5e7174f37f27e0af4babbe7745e7a1eb51f3ee8bc2ee3dcdbe`  
		Last Modified: Sat, 24 Apr 2021 04:43:04 GMT  
		Size: 209.6 MB (209633276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:16-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:da67cfe4028e29830be8096e81fb46e44cee2481c529b066663808b76947ebf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:16-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:404f02e2ef1cc041b323a7976f631917badeec3b4d43f8ae5b0f0361dab0439e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212433843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2ad03654b54cda4c95f8b862f1f47b7c0e9287be30ce020dfb51973ae161c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Sat, 24 Apr 2021 04:41:25 GMT
ARG version=16.0.1.9.1
# Sat, 24 Apr 2021 04:41:33 GMT
# ARGS: version=16.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-16=$version-r0
# Sat, 24 Apr 2021 04:41:33 GMT
ENV LANG=C.UTF-8
# Sat, 24 Apr 2021 04:41:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 24 Apr 2021 04:41:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5d31824e596a5e7174f37f27e0af4babbe7745e7a1eb51f3ee8bc2ee3dcdbe`  
		Last Modified: Sat, 24 Apr 2021 04:43:04 GMT  
		Size: 209.6 MB (209633276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:16.0.1`

```console
$ docker pull amazoncorretto@sha256:c90f9338d8a1a5788db2c77ea853cb4bdbafb3a953ea08eed9ecc75644f30a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:16.0.1` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7d3c4763c0e2abf1ea6a92e262afc1a64abed49301879fac76c957aacc91d89f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221892540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a852bea8bc07f33ee743060e9fcc79e6fc00332872c62ba7b655749e72b47b51`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:39:26 GMT
ARG version=16.0.1.9-1
# Mon, 14 Jun 2021 22:39:48 GMT
# ARGS: version=16.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:39:49 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:39:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d47f3a5aebc9df1b6beb67ad88ecf895637897682242d0cefb068414e38e606`  
		Last Modified: Mon, 14 Jun 2021 22:41:42 GMT  
		Size: 159.9 MB (159943483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:16.0.1` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e9ddd09da77249483478a40b89a033b0c13f94f2a359931e751e75c7a8d81fc2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223376292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359d42b7f71821497a2bb49bb81a67a62dd100c6c73b7184136e2e3943666ae8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:57:26 GMT
ARG version=16.0.1.9-1
# Mon, 14 Jun 2021 22:57:47 GMT
# ARGS: version=16.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:57:48 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:57:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94b510dae9b488c119034982e25017574f0769cd7d8b9c193e8981a7646541d`  
		Last Modified: Mon, 14 Jun 2021 22:59:55 GMT  
		Size: 159.9 MB (159927765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:16.0.1-al2`

```console
$ docker pull amazoncorretto@sha256:c90f9338d8a1a5788db2c77ea853cb4bdbafb3a953ea08eed9ecc75644f30a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:16.0.1-al2` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7d3c4763c0e2abf1ea6a92e262afc1a64abed49301879fac76c957aacc91d89f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221892540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a852bea8bc07f33ee743060e9fcc79e6fc00332872c62ba7b655749e72b47b51`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:39:26 GMT
ARG version=16.0.1.9-1
# Mon, 14 Jun 2021 22:39:48 GMT
# ARGS: version=16.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:39:49 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:39:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d47f3a5aebc9df1b6beb67ad88ecf895637897682242d0cefb068414e38e606`  
		Last Modified: Mon, 14 Jun 2021 22:41:42 GMT  
		Size: 159.9 MB (159943483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:16.0.1-al2` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e9ddd09da77249483478a40b89a033b0c13f94f2a359931e751e75c7a8d81fc2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223376292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359d42b7f71821497a2bb49bb81a67a62dd100c6c73b7184136e2e3943666ae8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:57:26 GMT
ARG version=16.0.1.9-1
# Mon, 14 Jun 2021 22:57:47 GMT
# ARGS: version=16.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:57:48 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:57:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94b510dae9b488c119034982e25017574f0769cd7d8b9c193e8981a7646541d`  
		Last Modified: Mon, 14 Jun 2021 22:59:55 GMT  
		Size: 159.9 MB (159927765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:16.0.1-alpine`

```console
$ docker pull amazoncorretto@sha256:da67cfe4028e29830be8096e81fb46e44cee2481c529b066663808b76947ebf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:16.0.1-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:404f02e2ef1cc041b323a7976f631917badeec3b4d43f8ae5b0f0361dab0439e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212433843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2ad03654b54cda4c95f8b862f1f47b7c0e9287be30ce020dfb51973ae161c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Sat, 24 Apr 2021 04:41:25 GMT
ARG version=16.0.1.9.1
# Sat, 24 Apr 2021 04:41:33 GMT
# ARGS: version=16.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-16=$version-r0
# Sat, 24 Apr 2021 04:41:33 GMT
ENV LANG=C.UTF-8
# Sat, 24 Apr 2021 04:41:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 24 Apr 2021 04:41:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5d31824e596a5e7174f37f27e0af4babbe7745e7a1eb51f3ee8bc2ee3dcdbe`  
		Last Modified: Sat, 24 Apr 2021 04:43:04 GMT  
		Size: 209.6 MB (209633276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8`

```console
$ docker pull amazoncorretto@sha256:e633693a03f576923a12203d3fa91628626450cebeab710f9ff48d1bd98a76f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:34062aeeb7827aff5fec2ceff9cfc8684ddcdaa7bf99106c029ff88544461f7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137240949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab161ed37a2582ae003ac0c25c10cd44c988b0b93ba14f4431585e632795226`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:38:22 GMT
ARG version=1.8.0_292.b10-1
# Mon, 14 Jun 2021 22:38:43 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && if [[ `arch` == 'aarch64' ]]; then version=1.8.0_292.b10-2; fi     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:38:43 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:38:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e193093e22cf1a77fdcc1c527def33d1086e31d65ca054cbfb9d77d24deb473`  
		Last Modified: Mon, 14 Jun 2021 22:40:33 GMT  
		Size: 75.3 MB (75291892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:aba72985c215ae94d41cea675151b287e37a693ceb54c29203585b17708b0c5b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122839461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd7c95671cf56a308295921e3f825a9736c134059ee3abf470b08d8def96d50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:56:28 GMT
ARG version=1.8.0_292.b10-1
# Mon, 14 Jun 2021 22:56:47 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && if [[ `arch` == 'aarch64' ]]; then version=1.8.0_292.b10-2; fi     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:56:47 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:56:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9093114e80fa08ebd40a61b8d81f6c5747109872aa78c8b047b7fbd170f894`  
		Last Modified: Mon, 14 Jun 2021 22:58:38 GMT  
		Size: 59.4 MB (59390934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:e633693a03f576923a12203d3fa91628626450cebeab710f9ff48d1bd98a76f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:34062aeeb7827aff5fec2ceff9cfc8684ddcdaa7bf99106c029ff88544461f7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137240949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab161ed37a2582ae003ac0c25c10cd44c988b0b93ba14f4431585e632795226`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:38:22 GMT
ARG version=1.8.0_292.b10-1
# Mon, 14 Jun 2021 22:38:43 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && if [[ `arch` == 'aarch64' ]]; then version=1.8.0_292.b10-2; fi     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:38:43 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:38:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e193093e22cf1a77fdcc1c527def33d1086e31d65ca054cbfb9d77d24deb473`  
		Last Modified: Mon, 14 Jun 2021 22:40:33 GMT  
		Size: 75.3 MB (75291892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:aba72985c215ae94d41cea675151b287e37a693ceb54c29203585b17708b0c5b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122839461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd7c95671cf56a308295921e3f825a9736c134059ee3abf470b08d8def96d50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:56:28 GMT
ARG version=1.8.0_292.b10-1
# Mon, 14 Jun 2021 22:56:47 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && if [[ `arch` == 'aarch64' ]]; then version=1.8.0_292.b10-2; fi     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:56:47 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:56:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9093114e80fa08ebd40a61b8d81f6c5747109872aa78c8b047b7fbd170f894`  
		Last Modified: Mon, 14 Jun 2021 22:58:38 GMT  
		Size: 59.4 MB (59390934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:e633693a03f576923a12203d3fa91628626450cebeab710f9ff48d1bd98a76f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:34062aeeb7827aff5fec2ceff9cfc8684ddcdaa7bf99106c029ff88544461f7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137240949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab161ed37a2582ae003ac0c25c10cd44c988b0b93ba14f4431585e632795226`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:38:22 GMT
ARG version=1.8.0_292.b10-1
# Mon, 14 Jun 2021 22:38:43 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && if [[ `arch` == 'aarch64' ]]; then version=1.8.0_292.b10-2; fi     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:38:43 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:38:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e193093e22cf1a77fdcc1c527def33d1086e31d65ca054cbfb9d77d24deb473`  
		Last Modified: Mon, 14 Jun 2021 22:40:33 GMT  
		Size: 75.3 MB (75291892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:aba72985c215ae94d41cea675151b287e37a693ceb54c29203585b17708b0c5b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122839461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd7c95671cf56a308295921e3f825a9736c134059ee3abf470b08d8def96d50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:56:28 GMT
ARG version=1.8.0_292.b10-1
# Mon, 14 Jun 2021 22:56:47 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && if [[ `arch` == 'aarch64' ]]; then version=1.8.0_292.b10-2; fi     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:56:47 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:56:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9093114e80fa08ebd40a61b8d81f6c5747109872aa78c8b047b7fbd170f894`  
		Last Modified: Mon, 14 Jun 2021 22:58:38 GMT  
		Size: 59.4 MB (59390934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-alpine`

```console
$ docker pull amazoncorretto@sha256:73939d6cb017bdb3885ea35ae18af6c6bf403ae0000b25e59c84b1e95ec9ffea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1a3472c57788ef9c33e2b830bea1f5227562e197aac294e3b27305c4a3429b9d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101815532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49dc0e3993ba2b79800dfa61af11876aad3ac15bfb8d280b35e81049b7a6ef3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Tue, 20 Apr 2021 23:20:11 GMT
ARG version=8.292.10.1
# Tue, 20 Apr 2021 23:20:19 GMT
# ARGS: version=8.292.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Tue, 20 Apr 2021 23:20:19 GMT
ENV LANG=C.UTF-8
# Tue, 20 Apr 2021 23:20:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 20 Apr 2021 23:20:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ec31fbf474c99d6924bc337c81bd4bfd0bfadb5a7e318c5456a3e110d4e9b9`  
		Last Modified: Tue, 20 Apr 2021 23:22:28 GMT  
		Size: 99.0 MB (99014965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-alpine-full`

```console
$ docker pull amazoncorretto@sha256:73939d6cb017bdb3885ea35ae18af6c6bf403ae0000b25e59c84b1e95ec9ffea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1a3472c57788ef9c33e2b830bea1f5227562e197aac294e3b27305c4a3429b9d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101815532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49dc0e3993ba2b79800dfa61af11876aad3ac15bfb8d280b35e81049b7a6ef3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Tue, 20 Apr 2021 23:20:11 GMT
ARG version=8.292.10.1
# Tue, 20 Apr 2021 23:20:19 GMT
# ARGS: version=8.292.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Tue, 20 Apr 2021 23:20:19 GMT
ENV LANG=C.UTF-8
# Tue, 20 Apr 2021 23:20:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 20 Apr 2021 23:20:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ec31fbf474c99d6924bc337c81bd4bfd0bfadb5a7e318c5456a3e110d4e9b9`  
		Last Modified: Tue, 20 Apr 2021 23:22:28 GMT  
		Size: 99.0 MB (99014965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:73939d6cb017bdb3885ea35ae18af6c6bf403ae0000b25e59c84b1e95ec9ffea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1a3472c57788ef9c33e2b830bea1f5227562e197aac294e3b27305c4a3429b9d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101815532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49dc0e3993ba2b79800dfa61af11876aad3ac15bfb8d280b35e81049b7a6ef3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Tue, 20 Apr 2021 23:20:11 GMT
ARG version=8.292.10.1
# Tue, 20 Apr 2021 23:20:19 GMT
# ARGS: version=8.292.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Tue, 20 Apr 2021 23:20:19 GMT
ENV LANG=C.UTF-8
# Tue, 20 Apr 2021 23:20:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 20 Apr 2021 23:20:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ec31fbf474c99d6924bc337c81bd4bfd0bfadb5a7e318c5456a3e110d4e9b9`  
		Last Modified: Tue, 20 Apr 2021 23:22:28 GMT  
		Size: 99.0 MB (99014965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:9b512161b10206d94138a47759ca3e1a503f01d6b97169f99bd9fc52f76fb7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:efdb98e9a99c921602eed17fb06c2f0661abfdff42a9490589d523a55afad5b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43136777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a944531e0b8aaf3cecdd7a3e65440030e6e4cfca9c15b10481a1ef41aa52d423`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Tue, 20 Apr 2021 23:20:11 GMT
ARG version=8.292.10.1
# Tue, 20 Apr 2021 23:20:26 GMT
# ARGS: version=8.292.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Tue, 20 Apr 2021 23:20:27 GMT
ENV LANG=C.UTF-8
# Tue, 20 Apr 2021 23:20:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4daa33c191f16afa306f7b3db9d2d8b3d1acf292d71a9414a041e146d4ba97a`  
		Last Modified: Tue, 20 Apr 2021 23:22:49 GMT  
		Size: 40.3 MB (40336210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u292`

```console
$ docker pull amazoncorretto@sha256:e633693a03f576923a12203d3fa91628626450cebeab710f9ff48d1bd98a76f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8u292` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:34062aeeb7827aff5fec2ceff9cfc8684ddcdaa7bf99106c029ff88544461f7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137240949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab161ed37a2582ae003ac0c25c10cd44c988b0b93ba14f4431585e632795226`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:38:22 GMT
ARG version=1.8.0_292.b10-1
# Mon, 14 Jun 2021 22:38:43 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && if [[ `arch` == 'aarch64' ]]; then version=1.8.0_292.b10-2; fi     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:38:43 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:38:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e193093e22cf1a77fdcc1c527def33d1086e31d65ca054cbfb9d77d24deb473`  
		Last Modified: Mon, 14 Jun 2021 22:40:33 GMT  
		Size: 75.3 MB (75291892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8u292` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:aba72985c215ae94d41cea675151b287e37a693ceb54c29203585b17708b0c5b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122839461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd7c95671cf56a308295921e3f825a9736c134059ee3abf470b08d8def96d50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:56:28 GMT
ARG version=1.8.0_292.b10-1
# Mon, 14 Jun 2021 22:56:47 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && if [[ `arch` == 'aarch64' ]]; then version=1.8.0_292.b10-2; fi     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:56:47 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:56:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9093114e80fa08ebd40a61b8d81f6c5747109872aa78c8b047b7fbd170f894`  
		Last Modified: Mon, 14 Jun 2021 22:58:38 GMT  
		Size: 59.4 MB (59390934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u292-al2`

```console
$ docker pull amazoncorretto@sha256:e633693a03f576923a12203d3fa91628626450cebeab710f9ff48d1bd98a76f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8u292-al2` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:34062aeeb7827aff5fec2ceff9cfc8684ddcdaa7bf99106c029ff88544461f7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137240949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab161ed37a2582ae003ac0c25c10cd44c988b0b93ba14f4431585e632795226`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:38:22 GMT
ARG version=1.8.0_292.b10-1
# Mon, 14 Jun 2021 22:38:43 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && if [[ `arch` == 'aarch64' ]]; then version=1.8.0_292.b10-2; fi     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:38:43 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:38:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e193093e22cf1a77fdcc1c527def33d1086e31d65ca054cbfb9d77d24deb473`  
		Last Modified: Mon, 14 Jun 2021 22:40:33 GMT  
		Size: 75.3 MB (75291892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8u292-al2` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:aba72985c215ae94d41cea675151b287e37a693ceb54c29203585b17708b0c5b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122839461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd7c95671cf56a308295921e3f825a9736c134059ee3abf470b08d8def96d50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:56:28 GMT
ARG version=1.8.0_292.b10-1
# Mon, 14 Jun 2021 22:56:47 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && if [[ `arch` == 'aarch64' ]]; then version=1.8.0_292.b10-2; fi     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:56:47 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:56:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9093114e80fa08ebd40a61b8d81f6c5747109872aa78c8b047b7fbd170f894`  
		Last Modified: Mon, 14 Jun 2021 22:58:38 GMT  
		Size: 59.4 MB (59390934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u292-alpine`

```console
$ docker pull amazoncorretto@sha256:73939d6cb017bdb3885ea35ae18af6c6bf403ae0000b25e59c84b1e95ec9ffea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8u292-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1a3472c57788ef9c33e2b830bea1f5227562e197aac294e3b27305c4a3429b9d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101815532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49dc0e3993ba2b79800dfa61af11876aad3ac15bfb8d280b35e81049b7a6ef3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Tue, 20 Apr 2021 23:20:11 GMT
ARG version=8.292.10.1
# Tue, 20 Apr 2021 23:20:19 GMT
# ARGS: version=8.292.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Tue, 20 Apr 2021 23:20:19 GMT
ENV LANG=C.UTF-8
# Tue, 20 Apr 2021 23:20:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 20 Apr 2021 23:20:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ec31fbf474c99d6924bc337c81bd4bfd0bfadb5a7e318c5456a3e110d4e9b9`  
		Last Modified: Tue, 20 Apr 2021 23:22:28 GMT  
		Size: 99.0 MB (99014965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u292-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:9b512161b10206d94138a47759ca3e1a503f01d6b97169f99bd9fc52f76fb7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8u292-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:efdb98e9a99c921602eed17fb06c2f0661abfdff42a9490589d523a55afad5b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43136777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a944531e0b8aaf3cecdd7a3e65440030e6e4cfca9c15b10481a1ef41aa52d423`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Tue, 20 Apr 2021 23:20:11 GMT
ARG version=8.292.10.1
# Tue, 20 Apr 2021 23:20:26 GMT
# ARGS: version=8.292.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Tue, 20 Apr 2021 23:20:27 GMT
ENV LANG=C.UTF-8
# Tue, 20 Apr 2021 23:20:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4daa33c191f16afa306f7b3db9d2d8b3d1acf292d71a9414a041e146d4ba97a`  
		Last Modified: Tue, 20 Apr 2021 23:22:49 GMT  
		Size: 40.3 MB (40336210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:e633693a03f576923a12203d3fa91628626450cebeab710f9ff48d1bd98a76f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:34062aeeb7827aff5fec2ceff9cfc8684ddcdaa7bf99106c029ff88544461f7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137240949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab161ed37a2582ae003ac0c25c10cd44c988b0b93ba14f4431585e632795226`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:38:22 GMT
ARG version=1.8.0_292.b10-1
# Mon, 14 Jun 2021 22:38:43 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && if [[ `arch` == 'aarch64' ]]; then version=1.8.0_292.b10-2; fi     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:38:43 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:38:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e193093e22cf1a77fdcc1c527def33d1086e31d65ca054cbfb9d77d24deb473`  
		Last Modified: Mon, 14 Jun 2021 22:40:33 GMT  
		Size: 75.3 MB (75291892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:latest` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:aba72985c215ae94d41cea675151b287e37a693ceb54c29203585b17708b0c5b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122839461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd7c95671cf56a308295921e3f825a9736c134059ee3abf470b08d8def96d50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:56:28 GMT
ARG version=1.8.0_292.b10-1
# Mon, 14 Jun 2021 22:56:47 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && if [[ `arch` == 'aarch64' ]]; then version=1.8.0_292.b10-2; fi     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:56:47 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:56:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9093114e80fa08ebd40a61b8d81f6c5747109872aa78c8b047b7fbd170f894`  
		Last Modified: Mon, 14 Jun 2021 22:58:38 GMT  
		Size: 59.4 MB (59390934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
