<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazoncorretto`

-	[`amazoncorretto:11`](#amazoncorretto11)
-	[`amazoncorretto:11.0.9`](#amazoncorretto1109)
-	[`amazoncorretto:11.0.9-al2`](#amazoncorretto1109-al2)
-	[`amazoncorretto:11.0.9-alpine`](#amazoncorretto1109-alpine)
-	[`amazoncorretto:11-al2-full`](#amazoncorretto11-al2-full)
-	[`amazoncorretto:11-al2-jdk`](#amazoncorretto11-al2-jdk)
-	[`amazoncorretto:11-alpine`](#amazoncorretto11-alpine)
-	[`amazoncorretto:11-alpine-full`](#amazoncorretto11-alpine-full)
-	[`amazoncorretto:11-alpine-jdk`](#amazoncorretto11-alpine-jdk)
-	[`amazoncorretto:15`](#amazoncorretto15)
-	[`amazoncorretto:15.0.1`](#amazoncorretto1501)
-	[`amazoncorretto:15.0.1-al2`](#amazoncorretto1501-al2)
-	[`amazoncorretto:15.0.1-alpine`](#amazoncorretto1501-alpine)
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
-	[`amazoncorretto:8u275`](#amazoncorretto8u275)
-	[`amazoncorretto:8u275-al2`](#amazoncorretto8u275-al2)
-	[`amazoncorretto:8u275-alpine`](#amazoncorretto8u275-alpine)
-	[`amazoncorretto:8u275-alpine-jre`](#amazoncorretto8u275-alpine-jre)
-	[`amazoncorretto:latest`](#amazoncorrettolatest)

## `amazoncorretto:11`

```console
$ docker pull amazoncorretto@sha256:e8eb0923cedcac7d02a0ab6632f92092e3e8577f286730fe00f3c60151b14e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9e612069601762761f296c13ecb8bca198f1821ab931fa6ca7e7db6fc644ef30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208153381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29632c9add27a9957d8d19b1a32c7f6c348642106a82d8712eb3d1432a5790c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Sat, 07 Nov 2020 00:19:55 GMT
ARG version=11.0.9.12-1
# Sat, 07 Nov 2020 00:20:21 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 07 Nov 2020 00:20:22 GMT
ENV LANG=C.UTF-8
# Sat, 07 Nov 2020 00:20:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82215f6c82ad0f433d877cc8341441ce73e67f294b86c2998e24e34e60d272c9`  
		Last Modified: Sat, 07 Nov 2020 00:21:56 GMT  
		Size: 146.4 MB (146436841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e71b5f2be284dfaa3a19cad2370600d1205fb0a41bbbe53dc530505c3ffcb1cb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207838791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8a1c8f6b10ff712d2b1142a3644948b42a91929644ff129a81ce138bda90f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:43:15 GMT
ADD file:d4c394189445aecbba87f3effbedda61d337d18393fa4b1af22ce498be6f6af0 in / 
# Fri, 31 Jul 2020 22:43:20 GMT
CMD ["/bin/bash"]
# Fri, 06 Nov 2020 23:40:15 GMT
ARG version=11.0.9.12-1
# Fri, 06 Nov 2020 23:40:46 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 06 Nov 2020 23:40:47 GMT
ENV LANG=C.UTF-8
# Fri, 06 Nov 2020 23:40:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:c9ca78f6e1f39219972cf4f8dac027e6f91e01d68c7aefd9c55b86c47f558827`  
		Last Modified: Fri, 31 Jul 2020 22:44:30 GMT  
		Size: 63.4 MB (63354136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbd29edd12813ebfd63352f3807f9ffea1fea3148691fd8206f5abd3f044e77`  
		Last Modified: Fri, 06 Nov 2020 23:42:04 GMT  
		Size: 144.5 MB (144484655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11.0.9`

```console
$ docker pull amazoncorretto@sha256:e8eb0923cedcac7d02a0ab6632f92092e3e8577f286730fe00f3c60151b14e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11.0.9` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9e612069601762761f296c13ecb8bca198f1821ab931fa6ca7e7db6fc644ef30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208153381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29632c9add27a9957d8d19b1a32c7f6c348642106a82d8712eb3d1432a5790c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Sat, 07 Nov 2020 00:19:55 GMT
ARG version=11.0.9.12-1
# Sat, 07 Nov 2020 00:20:21 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 07 Nov 2020 00:20:22 GMT
ENV LANG=C.UTF-8
# Sat, 07 Nov 2020 00:20:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82215f6c82ad0f433d877cc8341441ce73e67f294b86c2998e24e34e60d272c9`  
		Last Modified: Sat, 07 Nov 2020 00:21:56 GMT  
		Size: 146.4 MB (146436841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11.0.9` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e71b5f2be284dfaa3a19cad2370600d1205fb0a41bbbe53dc530505c3ffcb1cb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207838791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8a1c8f6b10ff712d2b1142a3644948b42a91929644ff129a81ce138bda90f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:43:15 GMT
ADD file:d4c394189445aecbba87f3effbedda61d337d18393fa4b1af22ce498be6f6af0 in / 
# Fri, 31 Jul 2020 22:43:20 GMT
CMD ["/bin/bash"]
# Fri, 06 Nov 2020 23:40:15 GMT
ARG version=11.0.9.12-1
# Fri, 06 Nov 2020 23:40:46 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 06 Nov 2020 23:40:47 GMT
ENV LANG=C.UTF-8
# Fri, 06 Nov 2020 23:40:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:c9ca78f6e1f39219972cf4f8dac027e6f91e01d68c7aefd9c55b86c47f558827`  
		Last Modified: Fri, 31 Jul 2020 22:44:30 GMT  
		Size: 63.4 MB (63354136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbd29edd12813ebfd63352f3807f9ffea1fea3148691fd8206f5abd3f044e77`  
		Last Modified: Fri, 06 Nov 2020 23:42:04 GMT  
		Size: 144.5 MB (144484655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11.0.9-al2`

```console
$ docker pull amazoncorretto@sha256:e8eb0923cedcac7d02a0ab6632f92092e3e8577f286730fe00f3c60151b14e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11.0.9-al2` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9e612069601762761f296c13ecb8bca198f1821ab931fa6ca7e7db6fc644ef30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208153381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29632c9add27a9957d8d19b1a32c7f6c348642106a82d8712eb3d1432a5790c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Sat, 07 Nov 2020 00:19:55 GMT
ARG version=11.0.9.12-1
# Sat, 07 Nov 2020 00:20:21 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 07 Nov 2020 00:20:22 GMT
ENV LANG=C.UTF-8
# Sat, 07 Nov 2020 00:20:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82215f6c82ad0f433d877cc8341441ce73e67f294b86c2998e24e34e60d272c9`  
		Last Modified: Sat, 07 Nov 2020 00:21:56 GMT  
		Size: 146.4 MB (146436841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11.0.9-al2` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e71b5f2be284dfaa3a19cad2370600d1205fb0a41bbbe53dc530505c3ffcb1cb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207838791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8a1c8f6b10ff712d2b1142a3644948b42a91929644ff129a81ce138bda90f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:43:15 GMT
ADD file:d4c394189445aecbba87f3effbedda61d337d18393fa4b1af22ce498be6f6af0 in / 
# Fri, 31 Jul 2020 22:43:20 GMT
CMD ["/bin/bash"]
# Fri, 06 Nov 2020 23:40:15 GMT
ARG version=11.0.9.12-1
# Fri, 06 Nov 2020 23:40:46 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 06 Nov 2020 23:40:47 GMT
ENV LANG=C.UTF-8
# Fri, 06 Nov 2020 23:40:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:c9ca78f6e1f39219972cf4f8dac027e6f91e01d68c7aefd9c55b86c47f558827`  
		Last Modified: Fri, 31 Jul 2020 22:44:30 GMT  
		Size: 63.4 MB (63354136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbd29edd12813ebfd63352f3807f9ffea1fea3148691fd8206f5abd3f044e77`  
		Last Modified: Fri, 06 Nov 2020 23:42:04 GMT  
		Size: 144.5 MB (144484655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11.0.9-alpine`

```console
$ docker pull amazoncorretto@sha256:1a89f072bc00f51b3aa4401d315d74dd1bf8a98575ec9dd9e54171f892cf70ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11.0.9-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f540bd83bc69dc00c4fd337851b8775888173270e901b02319d573e319c1e5d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (194994699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833ef1f0967aba46040fadc0b3cd2e3f25bff3fb661eaae090864b619b671369`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:47:40 GMT
ARG version=11.0.9.12.1
# Fri, 11 Dec 2020 02:47:47 GMT
# ARGS: version=11.0.9.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Fri, 11 Dec 2020 02:47:48 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 02:47:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 11 Dec 2020 02:47:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4745f8afc1b0b851828482b818c87de04f0f2428325d2b3b259f694ee4e2c0`  
		Last Modified: Fri, 11 Dec 2020 02:49:43 GMT  
		Size: 192.2 MB (192197754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:e8eb0923cedcac7d02a0ab6632f92092e3e8577f286730fe00f3c60151b14e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9e612069601762761f296c13ecb8bca198f1821ab931fa6ca7e7db6fc644ef30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208153381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29632c9add27a9957d8d19b1a32c7f6c348642106a82d8712eb3d1432a5790c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Sat, 07 Nov 2020 00:19:55 GMT
ARG version=11.0.9.12-1
# Sat, 07 Nov 2020 00:20:21 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 07 Nov 2020 00:20:22 GMT
ENV LANG=C.UTF-8
# Sat, 07 Nov 2020 00:20:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82215f6c82ad0f433d877cc8341441ce73e67f294b86c2998e24e34e60d272c9`  
		Last Modified: Sat, 07 Nov 2020 00:21:56 GMT  
		Size: 146.4 MB (146436841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e71b5f2be284dfaa3a19cad2370600d1205fb0a41bbbe53dc530505c3ffcb1cb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207838791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8a1c8f6b10ff712d2b1142a3644948b42a91929644ff129a81ce138bda90f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:43:15 GMT
ADD file:d4c394189445aecbba87f3effbedda61d337d18393fa4b1af22ce498be6f6af0 in / 
# Fri, 31 Jul 2020 22:43:20 GMT
CMD ["/bin/bash"]
# Fri, 06 Nov 2020 23:40:15 GMT
ARG version=11.0.9.12-1
# Fri, 06 Nov 2020 23:40:46 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 06 Nov 2020 23:40:47 GMT
ENV LANG=C.UTF-8
# Fri, 06 Nov 2020 23:40:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:c9ca78f6e1f39219972cf4f8dac027e6f91e01d68c7aefd9c55b86c47f558827`  
		Last Modified: Fri, 31 Jul 2020 22:44:30 GMT  
		Size: 63.4 MB (63354136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbd29edd12813ebfd63352f3807f9ffea1fea3148691fd8206f5abd3f044e77`  
		Last Modified: Fri, 06 Nov 2020 23:42:04 GMT  
		Size: 144.5 MB (144484655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:e8eb0923cedcac7d02a0ab6632f92092e3e8577f286730fe00f3c60151b14e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9e612069601762761f296c13ecb8bca198f1821ab931fa6ca7e7db6fc644ef30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208153381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29632c9add27a9957d8d19b1a32c7f6c348642106a82d8712eb3d1432a5790c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Sat, 07 Nov 2020 00:19:55 GMT
ARG version=11.0.9.12-1
# Sat, 07 Nov 2020 00:20:21 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 07 Nov 2020 00:20:22 GMT
ENV LANG=C.UTF-8
# Sat, 07 Nov 2020 00:20:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82215f6c82ad0f433d877cc8341441ce73e67f294b86c2998e24e34e60d272c9`  
		Last Modified: Sat, 07 Nov 2020 00:21:56 GMT  
		Size: 146.4 MB (146436841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e71b5f2be284dfaa3a19cad2370600d1205fb0a41bbbe53dc530505c3ffcb1cb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207838791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8a1c8f6b10ff712d2b1142a3644948b42a91929644ff129a81ce138bda90f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:43:15 GMT
ADD file:d4c394189445aecbba87f3effbedda61d337d18393fa4b1af22ce498be6f6af0 in / 
# Fri, 31 Jul 2020 22:43:20 GMT
CMD ["/bin/bash"]
# Fri, 06 Nov 2020 23:40:15 GMT
ARG version=11.0.9.12-1
# Fri, 06 Nov 2020 23:40:46 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 06 Nov 2020 23:40:47 GMT
ENV LANG=C.UTF-8
# Fri, 06 Nov 2020 23:40:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:c9ca78f6e1f39219972cf4f8dac027e6f91e01d68c7aefd9c55b86c47f558827`  
		Last Modified: Fri, 31 Jul 2020 22:44:30 GMT  
		Size: 63.4 MB (63354136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbd29edd12813ebfd63352f3807f9ffea1fea3148691fd8206f5abd3f044e77`  
		Last Modified: Fri, 06 Nov 2020 23:42:04 GMT  
		Size: 144.5 MB (144484655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-alpine`

```console
$ docker pull amazoncorretto@sha256:1a89f072bc00f51b3aa4401d315d74dd1bf8a98575ec9dd9e54171f892cf70ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f540bd83bc69dc00c4fd337851b8775888173270e901b02319d573e319c1e5d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (194994699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833ef1f0967aba46040fadc0b3cd2e3f25bff3fb661eaae090864b619b671369`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:47:40 GMT
ARG version=11.0.9.12.1
# Fri, 11 Dec 2020 02:47:47 GMT
# ARGS: version=11.0.9.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Fri, 11 Dec 2020 02:47:48 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 02:47:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 11 Dec 2020 02:47:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4745f8afc1b0b851828482b818c87de04f0f2428325d2b3b259f694ee4e2c0`  
		Last Modified: Fri, 11 Dec 2020 02:49:43 GMT  
		Size: 192.2 MB (192197754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-alpine-full`

```console
$ docker pull amazoncorretto@sha256:1a89f072bc00f51b3aa4401d315d74dd1bf8a98575ec9dd9e54171f892cf70ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f540bd83bc69dc00c4fd337851b8775888173270e901b02319d573e319c1e5d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (194994699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833ef1f0967aba46040fadc0b3cd2e3f25bff3fb661eaae090864b619b671369`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:47:40 GMT
ARG version=11.0.9.12.1
# Fri, 11 Dec 2020 02:47:47 GMT
# ARGS: version=11.0.9.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Fri, 11 Dec 2020 02:47:48 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 02:47:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 11 Dec 2020 02:47:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4745f8afc1b0b851828482b818c87de04f0f2428325d2b3b259f694ee4e2c0`  
		Last Modified: Fri, 11 Dec 2020 02:49:43 GMT  
		Size: 192.2 MB (192197754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:1a89f072bc00f51b3aa4401d315d74dd1bf8a98575ec9dd9e54171f892cf70ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f540bd83bc69dc00c4fd337851b8775888173270e901b02319d573e319c1e5d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (194994699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833ef1f0967aba46040fadc0b3cd2e3f25bff3fb661eaae090864b619b671369`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:47:40 GMT
ARG version=11.0.9.12.1
# Fri, 11 Dec 2020 02:47:47 GMT
# ARGS: version=11.0.9.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Fri, 11 Dec 2020 02:47:48 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 02:47:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 11 Dec 2020 02:47:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4745f8afc1b0b851828482b818c87de04f0f2428325d2b3b259f694ee4e2c0`  
		Last Modified: Fri, 11 Dec 2020 02:49:43 GMT  
		Size: 192.2 MB (192197754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15`

```console
$ docker pull amazoncorretto@sha256:b1b9eb9e10827cedfd6c10c2e121f1a6afcdc5d8d6b2fdef1d88da40fd5b6ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:15` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8de06d3a5c0cd1c69bf18730214f5f23cfa0bc6745ed1dc53fb1c851add1b9d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217348464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987efd713809d9d86d659d999e9c17a840553850d1d59f45724ff6de9cf925bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 00:20:38 GMT
ARG version=15.0.1.9-1
# Wed, 28 Oct 2020 00:21:04 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 28 Oct 2020 00:21:04 GMT
ENV LANG=C.UTF-8
# Wed, 28 Oct 2020 00:21:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f63bb5d5eb2077eabce2a847bd08bfed17d34b549ba4b4839b065a377194a54`  
		Last Modified: Wed, 28 Oct 2020 00:22:52 GMT  
		Size: 155.6 MB (155631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:15` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:27d8a7fc62043fd7d12dda21eac478b63558106f05ddf8d5b49c430b91757e17
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 MB (218857049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577b845bb89b00f8f2fb899ff74444415edb18bab356e0eb1e9298bb903b12ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:43:15 GMT
ADD file:d4c394189445aecbba87f3effbedda61d337d18393fa4b1af22ce498be6f6af0 in / 
# Fri, 31 Jul 2020 22:43:20 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 00:41:10 GMT
ARG version=15.0.1.9-1
# Wed, 28 Oct 2020 00:41:59 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 28 Oct 2020 00:42:02 GMT
ENV LANG=C.UTF-8
# Wed, 28 Oct 2020 00:42:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:c9ca78f6e1f39219972cf4f8dac027e6f91e01d68c7aefd9c55b86c47f558827`  
		Last Modified: Fri, 31 Jul 2020 22:44:30 GMT  
		Size: 63.4 MB (63354136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4844a846e201e89f85fa7c7c2a2c256867445498cf78b6411d49fb9587517f`  
		Last Modified: Wed, 28 Oct 2020 00:43:35 GMT  
		Size: 155.5 MB (155502913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15.0.1`

```console
$ docker pull amazoncorretto@sha256:b1b9eb9e10827cedfd6c10c2e121f1a6afcdc5d8d6b2fdef1d88da40fd5b6ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:15.0.1` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8de06d3a5c0cd1c69bf18730214f5f23cfa0bc6745ed1dc53fb1c851add1b9d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217348464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987efd713809d9d86d659d999e9c17a840553850d1d59f45724ff6de9cf925bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 00:20:38 GMT
ARG version=15.0.1.9-1
# Wed, 28 Oct 2020 00:21:04 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 28 Oct 2020 00:21:04 GMT
ENV LANG=C.UTF-8
# Wed, 28 Oct 2020 00:21:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f63bb5d5eb2077eabce2a847bd08bfed17d34b549ba4b4839b065a377194a54`  
		Last Modified: Wed, 28 Oct 2020 00:22:52 GMT  
		Size: 155.6 MB (155631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:15.0.1` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:27d8a7fc62043fd7d12dda21eac478b63558106f05ddf8d5b49c430b91757e17
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 MB (218857049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577b845bb89b00f8f2fb899ff74444415edb18bab356e0eb1e9298bb903b12ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:43:15 GMT
ADD file:d4c394189445aecbba87f3effbedda61d337d18393fa4b1af22ce498be6f6af0 in / 
# Fri, 31 Jul 2020 22:43:20 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 00:41:10 GMT
ARG version=15.0.1.9-1
# Wed, 28 Oct 2020 00:41:59 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 28 Oct 2020 00:42:02 GMT
ENV LANG=C.UTF-8
# Wed, 28 Oct 2020 00:42:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:c9ca78f6e1f39219972cf4f8dac027e6f91e01d68c7aefd9c55b86c47f558827`  
		Last Modified: Fri, 31 Jul 2020 22:44:30 GMT  
		Size: 63.4 MB (63354136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4844a846e201e89f85fa7c7c2a2c256867445498cf78b6411d49fb9587517f`  
		Last Modified: Wed, 28 Oct 2020 00:43:35 GMT  
		Size: 155.5 MB (155502913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15.0.1-al2`

```console
$ docker pull amazoncorretto@sha256:b1b9eb9e10827cedfd6c10c2e121f1a6afcdc5d8d6b2fdef1d88da40fd5b6ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:15.0.1-al2` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8de06d3a5c0cd1c69bf18730214f5f23cfa0bc6745ed1dc53fb1c851add1b9d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217348464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987efd713809d9d86d659d999e9c17a840553850d1d59f45724ff6de9cf925bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 00:20:38 GMT
ARG version=15.0.1.9-1
# Wed, 28 Oct 2020 00:21:04 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 28 Oct 2020 00:21:04 GMT
ENV LANG=C.UTF-8
# Wed, 28 Oct 2020 00:21:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f63bb5d5eb2077eabce2a847bd08bfed17d34b549ba4b4839b065a377194a54`  
		Last Modified: Wed, 28 Oct 2020 00:22:52 GMT  
		Size: 155.6 MB (155631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:15.0.1-al2` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:27d8a7fc62043fd7d12dda21eac478b63558106f05ddf8d5b49c430b91757e17
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 MB (218857049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577b845bb89b00f8f2fb899ff74444415edb18bab356e0eb1e9298bb903b12ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:43:15 GMT
ADD file:d4c394189445aecbba87f3effbedda61d337d18393fa4b1af22ce498be6f6af0 in / 
# Fri, 31 Jul 2020 22:43:20 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 00:41:10 GMT
ARG version=15.0.1.9-1
# Wed, 28 Oct 2020 00:41:59 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 28 Oct 2020 00:42:02 GMT
ENV LANG=C.UTF-8
# Wed, 28 Oct 2020 00:42:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:c9ca78f6e1f39219972cf4f8dac027e6f91e01d68c7aefd9c55b86c47f558827`  
		Last Modified: Fri, 31 Jul 2020 22:44:30 GMT  
		Size: 63.4 MB (63354136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4844a846e201e89f85fa7c7c2a2c256867445498cf78b6411d49fb9587517f`  
		Last Modified: Wed, 28 Oct 2020 00:43:35 GMT  
		Size: 155.5 MB (155502913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15.0.1-alpine`

```console
$ docker pull amazoncorretto@sha256:4223f26700e534b251f73de6b0a3c81e6a2201b38f899b560a31c409b06915f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:15.0.1-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7ecdbd7c06dbcdab16d69a4d86256ec395922ddf278144f0e077e647f9c22930
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207714884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c65bf033ee406ac95fc6e2c709f8bb3e291a8b7f31765b6d4e3eba0f18e59b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:47:56 GMT
ARG version=15.0.1.9.1
# Fri, 11 Dec 2020 02:48:05 GMT
# ARGS: version=15.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-15=$version-r0
# Fri, 11 Dec 2020 02:48:08 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 02:48:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 11 Dec 2020 02:48:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d154da8290a272bc25dd6b7c712f4d4829c389afbdea6b9a5e449786db0b9c39`  
		Last Modified: Fri, 11 Dec 2020 02:50:21 GMT  
		Size: 204.9 MB (204917939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15-al2-full`

```console
$ docker pull amazoncorretto@sha256:b1b9eb9e10827cedfd6c10c2e121f1a6afcdc5d8d6b2fdef1d88da40fd5b6ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:15-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8de06d3a5c0cd1c69bf18730214f5f23cfa0bc6745ed1dc53fb1c851add1b9d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217348464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987efd713809d9d86d659d999e9c17a840553850d1d59f45724ff6de9cf925bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 00:20:38 GMT
ARG version=15.0.1.9-1
# Wed, 28 Oct 2020 00:21:04 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 28 Oct 2020 00:21:04 GMT
ENV LANG=C.UTF-8
# Wed, 28 Oct 2020 00:21:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f63bb5d5eb2077eabce2a847bd08bfed17d34b549ba4b4839b065a377194a54`  
		Last Modified: Wed, 28 Oct 2020 00:22:52 GMT  
		Size: 155.6 MB (155631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:15-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:27d8a7fc62043fd7d12dda21eac478b63558106f05ddf8d5b49c430b91757e17
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 MB (218857049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577b845bb89b00f8f2fb899ff74444415edb18bab356e0eb1e9298bb903b12ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:43:15 GMT
ADD file:d4c394189445aecbba87f3effbedda61d337d18393fa4b1af22ce498be6f6af0 in / 
# Fri, 31 Jul 2020 22:43:20 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 00:41:10 GMT
ARG version=15.0.1.9-1
# Wed, 28 Oct 2020 00:41:59 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 28 Oct 2020 00:42:02 GMT
ENV LANG=C.UTF-8
# Wed, 28 Oct 2020 00:42:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:c9ca78f6e1f39219972cf4f8dac027e6f91e01d68c7aefd9c55b86c47f558827`  
		Last Modified: Fri, 31 Jul 2020 22:44:30 GMT  
		Size: 63.4 MB (63354136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4844a846e201e89f85fa7c7c2a2c256867445498cf78b6411d49fb9587517f`  
		Last Modified: Wed, 28 Oct 2020 00:43:35 GMT  
		Size: 155.5 MB (155502913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:b1b9eb9e10827cedfd6c10c2e121f1a6afcdc5d8d6b2fdef1d88da40fd5b6ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:15-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8de06d3a5c0cd1c69bf18730214f5f23cfa0bc6745ed1dc53fb1c851add1b9d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217348464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987efd713809d9d86d659d999e9c17a840553850d1d59f45724ff6de9cf925bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 00:20:38 GMT
ARG version=15.0.1.9-1
# Wed, 28 Oct 2020 00:21:04 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 28 Oct 2020 00:21:04 GMT
ENV LANG=C.UTF-8
# Wed, 28 Oct 2020 00:21:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f63bb5d5eb2077eabce2a847bd08bfed17d34b549ba4b4839b065a377194a54`  
		Last Modified: Wed, 28 Oct 2020 00:22:52 GMT  
		Size: 155.6 MB (155631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:15-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:27d8a7fc62043fd7d12dda21eac478b63558106f05ddf8d5b49c430b91757e17
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 MB (218857049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577b845bb89b00f8f2fb899ff74444415edb18bab356e0eb1e9298bb903b12ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:43:15 GMT
ADD file:d4c394189445aecbba87f3effbedda61d337d18393fa4b1af22ce498be6f6af0 in / 
# Fri, 31 Jul 2020 22:43:20 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 00:41:10 GMT
ARG version=15.0.1.9-1
# Wed, 28 Oct 2020 00:41:59 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 28 Oct 2020 00:42:02 GMT
ENV LANG=C.UTF-8
# Wed, 28 Oct 2020 00:42:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:c9ca78f6e1f39219972cf4f8dac027e6f91e01d68c7aefd9c55b86c47f558827`  
		Last Modified: Fri, 31 Jul 2020 22:44:30 GMT  
		Size: 63.4 MB (63354136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4844a846e201e89f85fa7c7c2a2c256867445498cf78b6411d49fb9587517f`  
		Last Modified: Wed, 28 Oct 2020 00:43:35 GMT  
		Size: 155.5 MB (155502913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15-alpine`

```console
$ docker pull amazoncorretto@sha256:4223f26700e534b251f73de6b0a3c81e6a2201b38f899b560a31c409b06915f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:15-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7ecdbd7c06dbcdab16d69a4d86256ec395922ddf278144f0e077e647f9c22930
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207714884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c65bf033ee406ac95fc6e2c709f8bb3e291a8b7f31765b6d4e3eba0f18e59b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:47:56 GMT
ARG version=15.0.1.9.1
# Fri, 11 Dec 2020 02:48:05 GMT
# ARGS: version=15.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-15=$version-r0
# Fri, 11 Dec 2020 02:48:08 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 02:48:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 11 Dec 2020 02:48:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d154da8290a272bc25dd6b7c712f4d4829c389afbdea6b9a5e449786db0b9c39`  
		Last Modified: Fri, 11 Dec 2020 02:50:21 GMT  
		Size: 204.9 MB (204917939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15-alpine-full`

```console
$ docker pull amazoncorretto@sha256:4223f26700e534b251f73de6b0a3c81e6a2201b38f899b560a31c409b06915f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:15-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7ecdbd7c06dbcdab16d69a4d86256ec395922ddf278144f0e077e647f9c22930
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207714884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c65bf033ee406ac95fc6e2c709f8bb3e291a8b7f31765b6d4e3eba0f18e59b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:47:56 GMT
ARG version=15.0.1.9.1
# Fri, 11 Dec 2020 02:48:05 GMT
# ARGS: version=15.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-15=$version-r0
# Fri, 11 Dec 2020 02:48:08 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 02:48:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 11 Dec 2020 02:48:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d154da8290a272bc25dd6b7c712f4d4829c389afbdea6b9a5e449786db0b9c39`  
		Last Modified: Fri, 11 Dec 2020 02:50:21 GMT  
		Size: 204.9 MB (204917939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:4223f26700e534b251f73de6b0a3c81e6a2201b38f899b560a31c409b06915f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:15-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7ecdbd7c06dbcdab16d69a4d86256ec395922ddf278144f0e077e647f9c22930
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207714884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c65bf033ee406ac95fc6e2c709f8bb3e291a8b7f31765b6d4e3eba0f18e59b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:47:56 GMT
ARG version=15.0.1.9.1
# Fri, 11 Dec 2020 02:48:05 GMT
# ARGS: version=15.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-15=$version-r0
# Fri, 11 Dec 2020 02:48:08 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 02:48:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 11 Dec 2020 02:48:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d154da8290a272bc25dd6b7c712f4d4829c389afbdea6b9a5e449786db0b9c39`  
		Last Modified: Fri, 11 Dec 2020 02:50:21 GMT  
		Size: 204.9 MB (204917939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8`

```console
$ docker pull amazoncorretto@sha256:396097a14f52e5e3bea719ddedda4ff9a0d9bb9ed3f6f4317fbdc1fce421c77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:837c250d03ff508e8600943acde51502769bdf8ed6692a0441a16f61322fdbb3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (136966559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6ef0725171b9b92bb495ab16076cf8887bba4fefe62d0778209b7c4111cd28`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Sat, 07 Nov 2020 00:19:26 GMT
ARG version=1.8.0_275.b01-1
# Sat, 07 Nov 2020 00:19:50 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 07 Nov 2020 00:19:50 GMT
ENV LANG=C.UTF-8
# Sat, 07 Nov 2020 00:19:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2752f6f919bfbcd37e165fe0c67fb744aef5b1af3f0bcb5179b867767145fe`  
		Last Modified: Sat, 07 Nov 2020 00:21:33 GMT  
		Size: 75.3 MB (75250019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ccd5f1a2859c70b5c3d8f69ac8964a63f08c527dcfdf5ebc3382bb7956a2624d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122686962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844a0d1f626288db79eb58bce940bfd12ffd222846888797fc4e63410941b3de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:43:15 GMT
ADD file:d4c394189445aecbba87f3effbedda61d337d18393fa4b1af22ce498be6f6af0 in / 
# Fri, 31 Jul 2020 22:43:20 GMT
CMD ["/bin/bash"]
# Fri, 06 Nov 2020 23:39:33 GMT
ARG version=1.8.0_275.b01-1
# Fri, 06 Nov 2020 23:40:03 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 06 Nov 2020 23:40:04 GMT
ENV LANG=C.UTF-8
# Fri, 06 Nov 2020 23:40:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:c9ca78f6e1f39219972cf4f8dac027e6f91e01d68c7aefd9c55b86c47f558827`  
		Last Modified: Fri, 31 Jul 2020 22:44:30 GMT  
		Size: 63.4 MB (63354136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87433f2cdf56429cf79382ba8c1ae0b2aacb1ca00f4b11e52d3f38922b83943d`  
		Last Modified: Fri, 06 Nov 2020 23:41:26 GMT  
		Size: 59.3 MB (59332826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:396097a14f52e5e3bea719ddedda4ff9a0d9bb9ed3f6f4317fbdc1fce421c77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:837c250d03ff508e8600943acde51502769bdf8ed6692a0441a16f61322fdbb3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (136966559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6ef0725171b9b92bb495ab16076cf8887bba4fefe62d0778209b7c4111cd28`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Sat, 07 Nov 2020 00:19:26 GMT
ARG version=1.8.0_275.b01-1
# Sat, 07 Nov 2020 00:19:50 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 07 Nov 2020 00:19:50 GMT
ENV LANG=C.UTF-8
# Sat, 07 Nov 2020 00:19:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2752f6f919bfbcd37e165fe0c67fb744aef5b1af3f0bcb5179b867767145fe`  
		Last Modified: Sat, 07 Nov 2020 00:21:33 GMT  
		Size: 75.3 MB (75250019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ccd5f1a2859c70b5c3d8f69ac8964a63f08c527dcfdf5ebc3382bb7956a2624d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122686962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844a0d1f626288db79eb58bce940bfd12ffd222846888797fc4e63410941b3de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:43:15 GMT
ADD file:d4c394189445aecbba87f3effbedda61d337d18393fa4b1af22ce498be6f6af0 in / 
# Fri, 31 Jul 2020 22:43:20 GMT
CMD ["/bin/bash"]
# Fri, 06 Nov 2020 23:39:33 GMT
ARG version=1.8.0_275.b01-1
# Fri, 06 Nov 2020 23:40:03 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 06 Nov 2020 23:40:04 GMT
ENV LANG=C.UTF-8
# Fri, 06 Nov 2020 23:40:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:c9ca78f6e1f39219972cf4f8dac027e6f91e01d68c7aefd9c55b86c47f558827`  
		Last Modified: Fri, 31 Jul 2020 22:44:30 GMT  
		Size: 63.4 MB (63354136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87433f2cdf56429cf79382ba8c1ae0b2aacb1ca00f4b11e52d3f38922b83943d`  
		Last Modified: Fri, 06 Nov 2020 23:41:26 GMT  
		Size: 59.3 MB (59332826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:396097a14f52e5e3bea719ddedda4ff9a0d9bb9ed3f6f4317fbdc1fce421c77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:837c250d03ff508e8600943acde51502769bdf8ed6692a0441a16f61322fdbb3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (136966559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6ef0725171b9b92bb495ab16076cf8887bba4fefe62d0778209b7c4111cd28`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Sat, 07 Nov 2020 00:19:26 GMT
ARG version=1.8.0_275.b01-1
# Sat, 07 Nov 2020 00:19:50 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 07 Nov 2020 00:19:50 GMT
ENV LANG=C.UTF-8
# Sat, 07 Nov 2020 00:19:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2752f6f919bfbcd37e165fe0c67fb744aef5b1af3f0bcb5179b867767145fe`  
		Last Modified: Sat, 07 Nov 2020 00:21:33 GMT  
		Size: 75.3 MB (75250019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ccd5f1a2859c70b5c3d8f69ac8964a63f08c527dcfdf5ebc3382bb7956a2624d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122686962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844a0d1f626288db79eb58bce940bfd12ffd222846888797fc4e63410941b3de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:43:15 GMT
ADD file:d4c394189445aecbba87f3effbedda61d337d18393fa4b1af22ce498be6f6af0 in / 
# Fri, 31 Jul 2020 22:43:20 GMT
CMD ["/bin/bash"]
# Fri, 06 Nov 2020 23:39:33 GMT
ARG version=1.8.0_275.b01-1
# Fri, 06 Nov 2020 23:40:03 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 06 Nov 2020 23:40:04 GMT
ENV LANG=C.UTF-8
# Fri, 06 Nov 2020 23:40:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:c9ca78f6e1f39219972cf4f8dac027e6f91e01d68c7aefd9c55b86c47f558827`  
		Last Modified: Fri, 31 Jul 2020 22:44:30 GMT  
		Size: 63.4 MB (63354136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87433f2cdf56429cf79382ba8c1ae0b2aacb1ca00f4b11e52d3f38922b83943d`  
		Last Modified: Fri, 06 Nov 2020 23:41:26 GMT  
		Size: 59.3 MB (59332826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-alpine`

```console
$ docker pull amazoncorretto@sha256:567af54e6223c064b9b2582ff85833c73daa1c03d3070ddca2dac15f2aa44865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3485f9ecd8d69e66934afcb1e8309f9ed32c02e710854824e02756b9e9b440dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101777645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce0c7480c7ca8176cc27651032454e72bbb7763d8510eae34626314953046bc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:47:22 GMT
ARG version=8.275.01.2
# Fri, 11 Dec 2020 02:47:28 GMT
# ARGS: version=8.275.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Fri, 11 Dec 2020 02:47:28 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 02:47:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 11 Dec 2020 02:47:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ef433720cc605cc4903eebaf95ee8578c75d94aef68657e57ef8734cf1a7b6`  
		Last Modified: Fri, 11 Dec 2020 02:49:07 GMT  
		Size: 99.0 MB (98980700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-alpine-full`

```console
$ docker pull amazoncorretto@sha256:567af54e6223c064b9b2582ff85833c73daa1c03d3070ddca2dac15f2aa44865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3485f9ecd8d69e66934afcb1e8309f9ed32c02e710854824e02756b9e9b440dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101777645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce0c7480c7ca8176cc27651032454e72bbb7763d8510eae34626314953046bc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:47:22 GMT
ARG version=8.275.01.2
# Fri, 11 Dec 2020 02:47:28 GMT
# ARGS: version=8.275.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Fri, 11 Dec 2020 02:47:28 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 02:47:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 11 Dec 2020 02:47:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ef433720cc605cc4903eebaf95ee8578c75d94aef68657e57ef8734cf1a7b6`  
		Last Modified: Fri, 11 Dec 2020 02:49:07 GMT  
		Size: 99.0 MB (98980700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:567af54e6223c064b9b2582ff85833c73daa1c03d3070ddca2dac15f2aa44865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3485f9ecd8d69e66934afcb1e8309f9ed32c02e710854824e02756b9e9b440dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101777645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce0c7480c7ca8176cc27651032454e72bbb7763d8510eae34626314953046bc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:47:22 GMT
ARG version=8.275.01.2
# Fri, 11 Dec 2020 02:47:28 GMT
# ARGS: version=8.275.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Fri, 11 Dec 2020 02:47:28 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 02:47:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 11 Dec 2020 02:47:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ef433720cc605cc4903eebaf95ee8578c75d94aef68657e57ef8734cf1a7b6`  
		Last Modified: Fri, 11 Dec 2020 02:49:07 GMT  
		Size: 99.0 MB (98980700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:bf589d2877958cfa423955a9eee3162393acbbaec3a6b15436e8de68b95fbbab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a0357ef50d477c994599c445c4befe270cf43ace5ecf1ce625527708db03db5a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43108328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79958c1f52ea286802cee08e086ceece191f7920e41bea21a5cfff4052ad5054`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:47:22 GMT
ARG version=8.275.01.2
# Fri, 11 Dec 2020 02:47:36 GMT
# ARGS: version=8.275.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Fri, 11 Dec 2020 02:47:36 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 02:47:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cb1bface849848879d3bdf8d3e42ae91fcb1cd361a6484e15b767c72cc69a6`  
		Last Modified: Fri, 11 Dec 2020 02:49:20 GMT  
		Size: 40.3 MB (40311383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u275`

```console
$ docker pull amazoncorretto@sha256:396097a14f52e5e3bea719ddedda4ff9a0d9bb9ed3f6f4317fbdc1fce421c77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8u275` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:837c250d03ff508e8600943acde51502769bdf8ed6692a0441a16f61322fdbb3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (136966559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6ef0725171b9b92bb495ab16076cf8887bba4fefe62d0778209b7c4111cd28`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Sat, 07 Nov 2020 00:19:26 GMT
ARG version=1.8.0_275.b01-1
# Sat, 07 Nov 2020 00:19:50 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 07 Nov 2020 00:19:50 GMT
ENV LANG=C.UTF-8
# Sat, 07 Nov 2020 00:19:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2752f6f919bfbcd37e165fe0c67fb744aef5b1af3f0bcb5179b867767145fe`  
		Last Modified: Sat, 07 Nov 2020 00:21:33 GMT  
		Size: 75.3 MB (75250019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8u275` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ccd5f1a2859c70b5c3d8f69ac8964a63f08c527dcfdf5ebc3382bb7956a2624d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122686962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844a0d1f626288db79eb58bce940bfd12ffd222846888797fc4e63410941b3de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:43:15 GMT
ADD file:d4c394189445aecbba87f3effbedda61d337d18393fa4b1af22ce498be6f6af0 in / 
# Fri, 31 Jul 2020 22:43:20 GMT
CMD ["/bin/bash"]
# Fri, 06 Nov 2020 23:39:33 GMT
ARG version=1.8.0_275.b01-1
# Fri, 06 Nov 2020 23:40:03 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 06 Nov 2020 23:40:04 GMT
ENV LANG=C.UTF-8
# Fri, 06 Nov 2020 23:40:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:c9ca78f6e1f39219972cf4f8dac027e6f91e01d68c7aefd9c55b86c47f558827`  
		Last Modified: Fri, 31 Jul 2020 22:44:30 GMT  
		Size: 63.4 MB (63354136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87433f2cdf56429cf79382ba8c1ae0b2aacb1ca00f4b11e52d3f38922b83943d`  
		Last Modified: Fri, 06 Nov 2020 23:41:26 GMT  
		Size: 59.3 MB (59332826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u275-al2`

```console
$ docker pull amazoncorretto@sha256:396097a14f52e5e3bea719ddedda4ff9a0d9bb9ed3f6f4317fbdc1fce421c77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8u275-al2` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:837c250d03ff508e8600943acde51502769bdf8ed6692a0441a16f61322fdbb3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (136966559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6ef0725171b9b92bb495ab16076cf8887bba4fefe62d0778209b7c4111cd28`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Sat, 07 Nov 2020 00:19:26 GMT
ARG version=1.8.0_275.b01-1
# Sat, 07 Nov 2020 00:19:50 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 07 Nov 2020 00:19:50 GMT
ENV LANG=C.UTF-8
# Sat, 07 Nov 2020 00:19:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2752f6f919bfbcd37e165fe0c67fb744aef5b1af3f0bcb5179b867767145fe`  
		Last Modified: Sat, 07 Nov 2020 00:21:33 GMT  
		Size: 75.3 MB (75250019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8u275-al2` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ccd5f1a2859c70b5c3d8f69ac8964a63f08c527dcfdf5ebc3382bb7956a2624d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122686962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844a0d1f626288db79eb58bce940bfd12ffd222846888797fc4e63410941b3de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:43:15 GMT
ADD file:d4c394189445aecbba87f3effbedda61d337d18393fa4b1af22ce498be6f6af0 in / 
# Fri, 31 Jul 2020 22:43:20 GMT
CMD ["/bin/bash"]
# Fri, 06 Nov 2020 23:39:33 GMT
ARG version=1.8.0_275.b01-1
# Fri, 06 Nov 2020 23:40:03 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 06 Nov 2020 23:40:04 GMT
ENV LANG=C.UTF-8
# Fri, 06 Nov 2020 23:40:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:c9ca78f6e1f39219972cf4f8dac027e6f91e01d68c7aefd9c55b86c47f558827`  
		Last Modified: Fri, 31 Jul 2020 22:44:30 GMT  
		Size: 63.4 MB (63354136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87433f2cdf56429cf79382ba8c1ae0b2aacb1ca00f4b11e52d3f38922b83943d`  
		Last Modified: Fri, 06 Nov 2020 23:41:26 GMT  
		Size: 59.3 MB (59332826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u275-alpine`

```console
$ docker pull amazoncorretto@sha256:567af54e6223c064b9b2582ff85833c73daa1c03d3070ddca2dac15f2aa44865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8u275-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3485f9ecd8d69e66934afcb1e8309f9ed32c02e710854824e02756b9e9b440dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101777645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce0c7480c7ca8176cc27651032454e72bbb7763d8510eae34626314953046bc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:47:22 GMT
ARG version=8.275.01.2
# Fri, 11 Dec 2020 02:47:28 GMT
# ARGS: version=8.275.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Fri, 11 Dec 2020 02:47:28 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 02:47:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 11 Dec 2020 02:47:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ef433720cc605cc4903eebaf95ee8578c75d94aef68657e57ef8734cf1a7b6`  
		Last Modified: Fri, 11 Dec 2020 02:49:07 GMT  
		Size: 99.0 MB (98980700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u275-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:bf589d2877958cfa423955a9eee3162393acbbaec3a6b15436e8de68b95fbbab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8u275-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a0357ef50d477c994599c445c4befe270cf43ace5ecf1ce625527708db03db5a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43108328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79958c1f52ea286802cee08e086ceece191f7920e41bea21a5cfff4052ad5054`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:47:22 GMT
ARG version=8.275.01.2
# Fri, 11 Dec 2020 02:47:36 GMT
# ARGS: version=8.275.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Fri, 11 Dec 2020 02:47:36 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 02:47:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cb1bface849848879d3bdf8d3e42ae91fcb1cd361a6484e15b767c72cc69a6`  
		Last Modified: Fri, 11 Dec 2020 02:49:20 GMT  
		Size: 40.3 MB (40311383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:396097a14f52e5e3bea719ddedda4ff9a0d9bb9ed3f6f4317fbdc1fce421c77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:837c250d03ff508e8600943acde51502769bdf8ed6692a0441a16f61322fdbb3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (136966559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6ef0725171b9b92bb495ab16076cf8887bba4fefe62d0778209b7c4111cd28`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Sat, 07 Nov 2020 00:19:26 GMT
ARG version=1.8.0_275.b01-1
# Sat, 07 Nov 2020 00:19:50 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 07 Nov 2020 00:19:50 GMT
ENV LANG=C.UTF-8
# Sat, 07 Nov 2020 00:19:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2752f6f919bfbcd37e165fe0c67fb744aef5b1af3f0bcb5179b867767145fe`  
		Last Modified: Sat, 07 Nov 2020 00:21:33 GMT  
		Size: 75.3 MB (75250019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:latest` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ccd5f1a2859c70b5c3d8f69ac8964a63f08c527dcfdf5ebc3382bb7956a2624d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122686962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844a0d1f626288db79eb58bce940bfd12ffd222846888797fc4e63410941b3de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:43:15 GMT
ADD file:d4c394189445aecbba87f3effbedda61d337d18393fa4b1af22ce498be6f6af0 in / 
# Fri, 31 Jul 2020 22:43:20 GMT
CMD ["/bin/bash"]
# Fri, 06 Nov 2020 23:39:33 GMT
ARG version=1.8.0_275.b01-1
# Fri, 06 Nov 2020 23:40:03 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 06 Nov 2020 23:40:04 GMT
ENV LANG=C.UTF-8
# Fri, 06 Nov 2020 23:40:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:c9ca78f6e1f39219972cf4f8dac027e6f91e01d68c7aefd9c55b86c47f558827`  
		Last Modified: Fri, 31 Jul 2020 22:44:30 GMT  
		Size: 63.4 MB (63354136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87433f2cdf56429cf79382ba8c1ae0b2aacb1ca00f4b11e52d3f38922b83943d`  
		Last Modified: Fri, 06 Nov 2020 23:41:26 GMT  
		Size: 59.3 MB (59332826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
