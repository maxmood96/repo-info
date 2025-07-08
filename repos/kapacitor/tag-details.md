<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.7`](#kapacitor177)
-	[`kapacitor:1.7.7-alpine`](#kapacitor177-alpine)
-	[`kapacitor:1.8`](#kapacitor18)
-	[`kapacitor:1.8-alpine`](#kapacitor18-alpine)
-	[`kapacitor:1.8.0`](#kapacitor180)
-	[`kapacitor:1.8.0-alpine`](#kapacitor180-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.7`

```console
$ docker pull kapacitor@sha256:776798b9951f56ff73ddf9cdafcc51bee2812a140966e66c936c1319ad921b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:e7e52738b6e0bf569fd3cedb08ed8c77b00c97b3ab56157625c798fe34cb6406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153229217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b211a795863372d615eadc5b4c53a0479bba27a7beba855dffa0f108fd1f28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 May 2025 13:09:59 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 May 2025 13:09:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 May 2025 13:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 13:09:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678e87101798c1c992d7c441a146a64a4a76a20702382a0e0ad72a873e291446`  
		Last Modified: Wed, 02 Jul 2025 03:09:59 GMT  
		Size: 7.1 MB (7103261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c26a15a16bdbe250aae6019528bcdfb09b2037b4239c10f7aeaab0edf6fc13e`  
		Last Modified: Wed, 02 Jul 2025 07:22:17 GMT  
		Size: 44.5 MB (44538684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7766f98f67fecf2a4a6c545e95dae0742cd65f4ac55cdd508f9376dc059c1428`  
		Last Modified: Wed, 02 Jul 2025 07:22:21 GMT  
		Size: 72.1 MB (72051065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba942f4c1f31e598a4d1b2c84366703cde0002481f03d18cc1051c5de8c52c2`  
		Last Modified: Wed, 02 Jul 2025 05:46:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6157048c75d4432dbf326add57dccdeec099ac63a260cc62f2daa9121bc591b8`  
		Last Modified: Wed, 02 Jul 2025 05:46:28 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:39f2b69a796d1cb0d0510123074d6baa1f7a202820420befbad26c438794d1cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df07daba630818b12f54ac665b138cf6ec905b1606da4f877a7eb7ac9afc0937`

```dockerfile
```

-	Layers:
	-	`sha256:328570750c505851916b85f47aae0976ef9ade0d9e0e56480fb3bb9292a3094b`  
		Last Modified: Wed, 02 Jul 2025 07:21:23 GMT  
		Size: 3.7 MB (3716964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2cd8f3c51ad22f7e506f7395eeabcb98e7fabd19eed75609282a890c690a559`  
		Last Modified: Wed, 02 Jul 2025 07:21:24 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:7389057fbb6ab456086cec4d38150bbaa7a64c34645a07da6e14a1b68ea07ffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144095235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf8a864000b159cb1445c28416115140279cf5ad6056283448d61cffcd3f01a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 May 2025 13:09:59 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 May 2025 13:09:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 May 2025 13:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 13:09:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44131f96e79008ec3b856a988d4d1fc58f4660f7ca12f41dfc747b162fe5ac2b`  
		Last Modified: Wed, 02 Jul 2025 04:18:53 GMT  
		Size: 7.0 MB (7049144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f42c87db2e6f52e316a4a1ee97021f9ab32ff2ca6871b2de26ee41b237deb4f`  
		Last Modified: Wed, 02 Jul 2025 08:36:47 GMT  
		Size: 41.9 MB (41872519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c9ab37201540012dd00c3ac6a8f249979973800dd9f01e6a70d5c1d9649b54`  
		Last Modified: Wed, 02 Jul 2025 18:36:12 GMT  
		Size: 67.8 MB (67813779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282341eecda9b5dc260dde612876817aaa91be2a7c11bf791e2bc579e3900c26`  
		Last Modified: Wed, 02 Jul 2025 08:37:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22abddff152c8397ff13be2b54ddd839077aac8ca623e0487c4691a9cd00ad7`  
		Last Modified: Wed, 02 Jul 2025 08:37:15 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:a6f5e79b9a8a61515c75d2f98642e04d7a6ee7eb514eaeeabd026bbe130a4308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b1ea7e28c8d5e9869ea65c3129c2cca0d3eca25ccfcbd867dd1d94b4ece39f`

```dockerfile
```

-	Layers:
	-	`sha256:2c1edc1fa273e104742188fd885fcd4eb0b1fb0002277ba5bf848df847a5ec29`  
		Last Modified: Wed, 02 Jul 2025 10:21:26 GMT  
		Size: 3.7 MB (3716438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f6f7621dd1153451fcab779371fd3f407cd2c48a3d8b72b8892bf83c96ae0f3`  
		Last Modified: Wed, 02 Jul 2025 10:21:27 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:89c0134a1fe8f16be0eb018ec821b2f35d5a28b12b2df9d4fefdd8b4c7531127
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:19c160f01a12c421a9618c032af651e4431e99b950c6e8b40d50d68615c03150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75906650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c09b3fd200d86d3901d6c6992ee87be103eba081d05262b144e827b8373c49e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 28 May 2025 13:09:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 May 2025 13:09:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 28 May 2025 13:09:59 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 May 2025 13:09:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 May 2025 13:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 13:09:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8050187616735b3a2eca88508aac28bef5adff25592089a08c2584db65c676`  
		Last Modified: Tue, 03 Jun 2025 14:28:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1818d7c593b71416e16718e6b8ae7023185be1b8e2a8392d819a70fa98c058`  
		Last Modified: Tue, 03 Jun 2025 14:28:14 GMT  
		Size: 296.5 KB (296509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d64b53402bf4db19ed5b642d9d2ce5742c41eca4320dd5da1cf2e5192a997c5`  
		Last Modified: Tue, 03 Jun 2025 14:28:21 GMT  
		Size: 72.0 MB (71982465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85316051b6ae6980fa600e7aad098095c72d879f28f69ab821e0336ea4b2fcb2`  
		Last Modified: Tue, 03 Jun 2025 14:28:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bc54915f27603d346c83ec9056f3063d97df863106ed951f6f27c86a807cef`  
		Last Modified: Tue, 03 Jun 2025 14:28:16 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:1c701c0e3f02c51c0b5a416fe2eeb3515e11fbbad452adcf2a6c750cf1dda44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.1 KB (384135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9313b7324de8a37c1323838da614894068e2e5c005651348296d5318ee9d7d`

```dockerfile
```

-	Layers:
	-	`sha256:9765178dab88f44d5afbb350178567db3bacbce39dbac097bdd793ef4cab928f`  
		Last Modified: Tue, 10 Jun 2025 06:09:21 GMT  
		Size: 368.5 KB (368451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29329adfb7df227bbd4c8aeb6e7b1af9c3cee347c2b209742b71f506b86e41c8`  
		Last Modified: Tue, 10 Jun 2025 06:09:23 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.7`

```console
$ docker pull kapacitor@sha256:776798b9951f56ff73ddf9cdafcc51bee2812a140966e66c936c1319ad921b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:e7e52738b6e0bf569fd3cedb08ed8c77b00c97b3ab56157625c798fe34cb6406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153229217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b211a795863372d615eadc5b4c53a0479bba27a7beba855dffa0f108fd1f28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 May 2025 13:09:59 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 May 2025 13:09:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 May 2025 13:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 13:09:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678e87101798c1c992d7c441a146a64a4a76a20702382a0e0ad72a873e291446`  
		Last Modified: Wed, 02 Jul 2025 03:09:59 GMT  
		Size: 7.1 MB (7103261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c26a15a16bdbe250aae6019528bcdfb09b2037b4239c10f7aeaab0edf6fc13e`  
		Last Modified: Wed, 02 Jul 2025 07:22:17 GMT  
		Size: 44.5 MB (44538684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7766f98f67fecf2a4a6c545e95dae0742cd65f4ac55cdd508f9376dc059c1428`  
		Last Modified: Wed, 02 Jul 2025 07:22:21 GMT  
		Size: 72.1 MB (72051065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba942f4c1f31e598a4d1b2c84366703cde0002481f03d18cc1051c5de8c52c2`  
		Last Modified: Wed, 02 Jul 2025 05:46:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6157048c75d4432dbf326add57dccdeec099ac63a260cc62f2daa9121bc591b8`  
		Last Modified: Wed, 02 Jul 2025 05:46:28 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:39f2b69a796d1cb0d0510123074d6baa1f7a202820420befbad26c438794d1cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df07daba630818b12f54ac665b138cf6ec905b1606da4f877a7eb7ac9afc0937`

```dockerfile
```

-	Layers:
	-	`sha256:328570750c505851916b85f47aae0976ef9ade0d9e0e56480fb3bb9292a3094b`  
		Last Modified: Wed, 02 Jul 2025 07:21:23 GMT  
		Size: 3.7 MB (3716964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2cd8f3c51ad22f7e506f7395eeabcb98e7fabd19eed75609282a890c690a559`  
		Last Modified: Wed, 02 Jul 2025 07:21:24 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:7389057fbb6ab456086cec4d38150bbaa7a64c34645a07da6e14a1b68ea07ffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144095235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf8a864000b159cb1445c28416115140279cf5ad6056283448d61cffcd3f01a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 May 2025 13:09:59 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 May 2025 13:09:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 May 2025 13:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 13:09:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44131f96e79008ec3b856a988d4d1fc58f4660f7ca12f41dfc747b162fe5ac2b`  
		Last Modified: Wed, 02 Jul 2025 04:18:53 GMT  
		Size: 7.0 MB (7049144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f42c87db2e6f52e316a4a1ee97021f9ab32ff2ca6871b2de26ee41b237deb4f`  
		Last Modified: Wed, 02 Jul 2025 08:36:47 GMT  
		Size: 41.9 MB (41872519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c9ab37201540012dd00c3ac6a8f249979973800dd9f01e6a70d5c1d9649b54`  
		Last Modified: Wed, 02 Jul 2025 18:36:12 GMT  
		Size: 67.8 MB (67813779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282341eecda9b5dc260dde612876817aaa91be2a7c11bf791e2bc579e3900c26`  
		Last Modified: Wed, 02 Jul 2025 08:37:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22abddff152c8397ff13be2b54ddd839077aac8ca623e0487c4691a9cd00ad7`  
		Last Modified: Wed, 02 Jul 2025 08:37:15 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:a6f5e79b9a8a61515c75d2f98642e04d7a6ee7eb514eaeeabd026bbe130a4308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b1ea7e28c8d5e9869ea65c3129c2cca0d3eca25ccfcbd867dd1d94b4ece39f`

```dockerfile
```

-	Layers:
	-	`sha256:2c1edc1fa273e104742188fd885fcd4eb0b1fb0002277ba5bf848df847a5ec29`  
		Last Modified: Wed, 02 Jul 2025 10:21:26 GMT  
		Size: 3.7 MB (3716438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f6f7621dd1153451fcab779371fd3f407cd2c48a3d8b72b8892bf83c96ae0f3`  
		Last Modified: Wed, 02 Jul 2025 10:21:27 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.7-alpine`

```console
$ docker pull kapacitor@sha256:89c0134a1fe8f16be0eb018ec821b2f35d5a28b12b2df9d4fefdd8b4c7531127
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:19c160f01a12c421a9618c032af651e4431e99b950c6e8b40d50d68615c03150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75906650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c09b3fd200d86d3901d6c6992ee87be103eba081d05262b144e827b8373c49e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 28 May 2025 13:09:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 May 2025 13:09:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 28 May 2025 13:09:59 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 May 2025 13:09:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 May 2025 13:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 13:09:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8050187616735b3a2eca88508aac28bef5adff25592089a08c2584db65c676`  
		Last Modified: Tue, 03 Jun 2025 14:28:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1818d7c593b71416e16718e6b8ae7023185be1b8e2a8392d819a70fa98c058`  
		Last Modified: Tue, 03 Jun 2025 14:28:14 GMT  
		Size: 296.5 KB (296509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d64b53402bf4db19ed5b642d9d2ce5742c41eca4320dd5da1cf2e5192a997c5`  
		Last Modified: Tue, 03 Jun 2025 14:28:21 GMT  
		Size: 72.0 MB (71982465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85316051b6ae6980fa600e7aad098095c72d879f28f69ab821e0336ea4b2fcb2`  
		Last Modified: Tue, 03 Jun 2025 14:28:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bc54915f27603d346c83ec9056f3063d97df863106ed951f6f27c86a807cef`  
		Last Modified: Tue, 03 Jun 2025 14:28:16 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:1c701c0e3f02c51c0b5a416fe2eeb3515e11fbbad452adcf2a6c750cf1dda44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.1 KB (384135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9313b7324de8a37c1323838da614894068e2e5c005651348296d5318ee9d7d`

```dockerfile
```

-	Layers:
	-	`sha256:9765178dab88f44d5afbb350178567db3bacbce39dbac097bdd793ef4cab928f`  
		Last Modified: Tue, 10 Jun 2025 06:09:21 GMT  
		Size: 368.5 KB (368451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29329adfb7df227bbd4c8aeb6e7b1af9c3cee347c2b209742b71f506b86e41c8`  
		Last Modified: Tue, 10 Jun 2025 06:09:23 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8`

```console
$ docker pull kapacitor@sha256:e2c0e7cddd7ffd05dfd2019900a23a1522f37eadcec4d2e5b96be3f89617f8e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8` - linux; amd64

```console
$ docker pull kapacitor@sha256:9799127f3e5b2a3c7ee7364ab52b307eb3f1789e2a21a9066f1f48008a4e2f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168629898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed05e50023be38b571b5e53b49384520033966ad2403b48c89e86147be660e1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.8.0
# Tue, 08 Jul 2025 13:10:35 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 08 Jul 2025 13:10:35 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 08 Jul 2025 13:10:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678e87101798c1c992d7c441a146a64a4a76a20702382a0e0ad72a873e291446`  
		Last Modified: Wed, 02 Jul 2025 03:09:59 GMT  
		Size: 7.1 MB (7103261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3fb189475f235fa5fa468196e072cc3a7cb5172a491a3dee1b031aa10852c7`  
		Last Modified: Tue, 08 Jul 2025 16:47:32 GMT  
		Size: 44.6 MB (44624162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d40e1d5643f976e7a66e20dd39368fc24572a5c63c8f156de985917f6ee96aa`  
		Last Modified: Tue, 08 Jul 2025 16:47:33 GMT  
		Size: 87.4 MB (87366264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad1ebc91713fb02ce3fff78f23504296b029389dda6703789d5b9cda2254691`  
		Last Modified: Tue, 08 Jul 2025 16:47:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df85c240bde0263995d36147b81e5e6f425977856047a67ec5e499158a59b8c`  
		Last Modified: Tue, 08 Jul 2025 16:47:30 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:ebe99aeea602766811a9a33b086af9f4ccae8454526b1ddc603f83f327edb033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25fa6f8eddbf7dd516cb43fc18e0a0630160cab24db3fda4795873d8b96739e7`

```dockerfile
```

-	Layers:
	-	`sha256:5465d91c6148324ba5d5ac4939f89dd7e3aff17dbda351e8597127a0aaa84e5e`  
		Last Modified: Tue, 08 Jul 2025 19:21:23 GMT  
		Size: 3.7 MB (3730949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0703b0c74286d057783772a6f0b76f9a9042136d55d21396feb4216b69a8e2d3`  
		Last Modified: Tue, 08 Jul 2025 19:21:24 GMT  
		Size: 14.8 KB (14759 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:2a52a5945c2cc33dbafb5364d3f6721d54d4556ac5a9931cde6bc838788fec20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157745148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e38bf9fafcac20cfd93b05696bd7fd19cafedcccffcbff1cce9511938cb282a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.8.0
# Tue, 08 Jul 2025 13:10:35 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 08 Jul 2025 13:10:35 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 08 Jul 2025 13:10:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44131f96e79008ec3b856a988d4d1fc58f4660f7ca12f41dfc747b162fe5ac2b`  
		Last Modified: Wed, 02 Jul 2025 04:18:53 GMT  
		Size: 7.0 MB (7049144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f42c87db2e6f52e316a4a1ee97021f9ab32ff2ca6871b2de26ee41b237deb4f`  
		Last Modified: Wed, 02 Jul 2025 08:36:47 GMT  
		Size: 41.9 MB (41872519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b40dbe3d0f06f18a3496a4b2f11a459e3ed24a67836928272cc909dddd6216`  
		Last Modified: Tue, 08 Jul 2025 16:46:50 GMT  
		Size: 81.5 MB (81463691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eef5b0adf833efc8c348d4c5067f8c962befa0d55d025b8870b76b7484c03c`  
		Last Modified: Tue, 08 Jul 2025 16:46:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc2b13a765911e59c2a8da554c7269fd09518bf0a4f09a5b30e32595283d364`  
		Last Modified: Tue, 08 Jul 2025 16:46:48 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:a0f6273cd3562142d554a4d566df9e4372c4b2fbcdb6a5020e5a7019580c10dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd10c6570f79d869212c1c3f39575ad2a0f992e5649f0eb14f5ebbec1e87c4cc`

```dockerfile
```

-	Layers:
	-	`sha256:b973677f52b63af2148ad016b70930ab53cc1f2ac55d083cd11b24207750bffd`  
		Last Modified: Tue, 08 Jul 2025 19:21:29 GMT  
		Size: 3.7 MB (3730411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cddf44c1bc98dec5d0f93e39ee630953120253aa35919743e89d8be6fdc8cda`  
		Last Modified: Tue, 08 Jul 2025 19:21:29 GMT  
		Size: 14.9 KB (14854 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8-alpine`

```console
$ docker pull kapacitor@sha256:f96b8716e08ed67faf6c66a1f363a1765ed54caef07c0b500eff5829ff2d99ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:cbb710a71590a2bb50a2836aa44e7a8b01069ef7a74e8bebae501c7893db6faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91410920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7323971862d2333685a92ebc62e0436f19203002c174975f31546c9d481a6786`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.8.0
# Tue, 08 Jul 2025 13:10:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 08 Jul 2025 13:10:35 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 08 Jul 2025 13:10:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6e959004231dea7f1db1ce8f9ec6c9a2c678f7c7f427a1e224fe959dd308e6`  
		Last Modified: Tue, 08 Jul 2025 16:47:12 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7e5a318c183be58ca1d7a930f4e13b06f8c3f45d9dc1b29c2a534aa3421450`  
		Last Modified: Tue, 08 Jul 2025 16:47:12 GMT  
		Size: 318.6 KB (318592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33a580d081caf6ab093623378abdbf9a40f5f7614d439f6bd56d8e84d3d763b`  
		Last Modified: Tue, 08 Jul 2025 16:47:14 GMT  
		Size: 87.3 MB (87294683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f844617c0583d655644db9df1a43014cf19a62416e5f73373dc42ffd902cea`  
		Last Modified: Tue, 08 Jul 2025 16:47:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9748604017a2bdfab3146680c3e7e06e5b8c29878392f00c65d7be7d297c16fb`  
		Last Modified: Tue, 08 Jul 2025 16:47:13 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7e1ea29c8f3aeea247cd046eb458ba7d34b346ca8597de4dda361e120d82b15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.2 KB (408225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbb7be51596932a6ea271a58b39579760af1727fc1512c152df96ec2ec568bb`

```dockerfile
```

-	Layers:
	-	`sha256:123eda639551fa0444975eb60485222805f4870cd53978043fd636a64fa7a296`  
		Last Modified: Tue, 08 Jul 2025 19:21:27 GMT  
		Size: 392.8 KB (392845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61c0b7828740c16f501522ae619027f671581d59012aadcb64bccd80342b5d67`  
		Last Modified: Tue, 08 Jul 2025 19:21:28 GMT  
		Size: 15.4 KB (15380 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.0`

```console
$ docker pull kapacitor@sha256:e2c0e7cddd7ffd05dfd2019900a23a1522f37eadcec4d2e5b96be3f89617f8e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8.0` - linux; amd64

```console
$ docker pull kapacitor@sha256:9799127f3e5b2a3c7ee7364ab52b307eb3f1789e2a21a9066f1f48008a4e2f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168629898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed05e50023be38b571b5e53b49384520033966ad2403b48c89e86147be660e1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.8.0
# Tue, 08 Jul 2025 13:10:35 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 08 Jul 2025 13:10:35 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 08 Jul 2025 13:10:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678e87101798c1c992d7c441a146a64a4a76a20702382a0e0ad72a873e291446`  
		Last Modified: Wed, 02 Jul 2025 03:09:59 GMT  
		Size: 7.1 MB (7103261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3fb189475f235fa5fa468196e072cc3a7cb5172a491a3dee1b031aa10852c7`  
		Last Modified: Tue, 08 Jul 2025 16:47:32 GMT  
		Size: 44.6 MB (44624162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d40e1d5643f976e7a66e20dd39368fc24572a5c63c8f156de985917f6ee96aa`  
		Last Modified: Tue, 08 Jul 2025 16:47:33 GMT  
		Size: 87.4 MB (87366264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad1ebc91713fb02ce3fff78f23504296b029389dda6703789d5b9cda2254691`  
		Last Modified: Tue, 08 Jul 2025 16:47:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df85c240bde0263995d36147b81e5e6f425977856047a67ec5e499158a59b8c`  
		Last Modified: Tue, 08 Jul 2025 16:47:30 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.0` - unknown; unknown

```console
$ docker pull kapacitor@sha256:ebe99aeea602766811a9a33b086af9f4ccae8454526b1ddc603f83f327edb033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25fa6f8eddbf7dd516cb43fc18e0a0630160cab24db3fda4795873d8b96739e7`

```dockerfile
```

-	Layers:
	-	`sha256:5465d91c6148324ba5d5ac4939f89dd7e3aff17dbda351e8597127a0aaa84e5e`  
		Last Modified: Tue, 08 Jul 2025 19:21:23 GMT  
		Size: 3.7 MB (3730949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0703b0c74286d057783772a6f0b76f9a9042136d55d21396feb4216b69a8e2d3`  
		Last Modified: Tue, 08 Jul 2025 19:21:24 GMT  
		Size: 14.8 KB (14759 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8.0` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:2a52a5945c2cc33dbafb5364d3f6721d54d4556ac5a9931cde6bc838788fec20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157745148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e38bf9fafcac20cfd93b05696bd7fd19cafedcccffcbff1cce9511938cb282a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.8.0
# Tue, 08 Jul 2025 13:10:35 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 08 Jul 2025 13:10:35 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 08 Jul 2025 13:10:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44131f96e79008ec3b856a988d4d1fc58f4660f7ca12f41dfc747b162fe5ac2b`  
		Last Modified: Wed, 02 Jul 2025 04:18:53 GMT  
		Size: 7.0 MB (7049144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f42c87db2e6f52e316a4a1ee97021f9ab32ff2ca6871b2de26ee41b237deb4f`  
		Last Modified: Wed, 02 Jul 2025 08:36:47 GMT  
		Size: 41.9 MB (41872519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b40dbe3d0f06f18a3496a4b2f11a459e3ed24a67836928272cc909dddd6216`  
		Last Modified: Tue, 08 Jul 2025 16:46:50 GMT  
		Size: 81.5 MB (81463691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eef5b0adf833efc8c348d4c5067f8c962befa0d55d025b8870b76b7484c03c`  
		Last Modified: Tue, 08 Jul 2025 16:46:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc2b13a765911e59c2a8da554c7269fd09518bf0a4f09a5b30e32595283d364`  
		Last Modified: Tue, 08 Jul 2025 16:46:48 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.0` - unknown; unknown

```console
$ docker pull kapacitor@sha256:a0f6273cd3562142d554a4d566df9e4372c4b2fbcdb6a5020e5a7019580c10dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd10c6570f79d869212c1c3f39575ad2a0f992e5649f0eb14f5ebbec1e87c4cc`

```dockerfile
```

-	Layers:
	-	`sha256:b973677f52b63af2148ad016b70930ab53cc1f2ac55d083cd11b24207750bffd`  
		Last Modified: Tue, 08 Jul 2025 19:21:29 GMT  
		Size: 3.7 MB (3730411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cddf44c1bc98dec5d0f93e39ee630953120253aa35919743e89d8be6fdc8cda`  
		Last Modified: Tue, 08 Jul 2025 19:21:29 GMT  
		Size: 14.9 KB (14854 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.0-alpine`

```console
$ docker pull kapacitor@sha256:f96b8716e08ed67faf6c66a1f363a1765ed54caef07c0b500eff5829ff2d99ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8.0-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:cbb710a71590a2bb50a2836aa44e7a8b01069ef7a74e8bebae501c7893db6faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91410920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7323971862d2333685a92ebc62e0436f19203002c174975f31546c9d481a6786`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.8.0
# Tue, 08 Jul 2025 13:10:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 08 Jul 2025 13:10:35 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 08 Jul 2025 13:10:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6e959004231dea7f1db1ce8f9ec6c9a2c678f7c7f427a1e224fe959dd308e6`  
		Last Modified: Tue, 08 Jul 2025 16:47:12 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7e5a318c183be58ca1d7a930f4e13b06f8c3f45d9dc1b29c2a534aa3421450`  
		Last Modified: Tue, 08 Jul 2025 16:47:12 GMT  
		Size: 318.6 KB (318592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33a580d081caf6ab093623378abdbf9a40f5f7614d439f6bd56d8e84d3d763b`  
		Last Modified: Tue, 08 Jul 2025 16:47:14 GMT  
		Size: 87.3 MB (87294683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f844617c0583d655644db9df1a43014cf19a62416e5f73373dc42ffd902cea`  
		Last Modified: Tue, 08 Jul 2025 16:47:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9748604017a2bdfab3146680c3e7e06e5b8c29878392f00c65d7be7d297c16fb`  
		Last Modified: Tue, 08 Jul 2025 16:47:13 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.0-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7e1ea29c8f3aeea247cd046eb458ba7d34b346ca8597de4dda361e120d82b15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.2 KB (408225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbb7be51596932a6ea271a58b39579760af1727fc1512c152df96ec2ec568bb`

```dockerfile
```

-	Layers:
	-	`sha256:123eda639551fa0444975eb60485222805f4870cd53978043fd636a64fa7a296`  
		Last Modified: Tue, 08 Jul 2025 19:21:27 GMT  
		Size: 392.8 KB (392845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61c0b7828740c16f501522ae619027f671581d59012aadcb64bccd80342b5d67`  
		Last Modified: Tue, 08 Jul 2025 19:21:28 GMT  
		Size: 15.4 KB (15380 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:89c0134a1fe8f16be0eb018ec821b2f35d5a28b12b2df9d4fefdd8b4c7531127
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:19c160f01a12c421a9618c032af651e4431e99b950c6e8b40d50d68615c03150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75906650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c09b3fd200d86d3901d6c6992ee87be103eba081d05262b144e827b8373c49e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 28 May 2025 13:09:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 May 2025 13:09:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 28 May 2025 13:09:59 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 May 2025 13:09:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 May 2025 13:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 13:09:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8050187616735b3a2eca88508aac28bef5adff25592089a08c2584db65c676`  
		Last Modified: Tue, 03 Jun 2025 14:28:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1818d7c593b71416e16718e6b8ae7023185be1b8e2a8392d819a70fa98c058`  
		Last Modified: Tue, 03 Jun 2025 14:28:14 GMT  
		Size: 296.5 KB (296509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d64b53402bf4db19ed5b642d9d2ce5742c41eca4320dd5da1cf2e5192a997c5`  
		Last Modified: Tue, 03 Jun 2025 14:28:21 GMT  
		Size: 72.0 MB (71982465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85316051b6ae6980fa600e7aad098095c72d879f28f69ab821e0336ea4b2fcb2`  
		Last Modified: Tue, 03 Jun 2025 14:28:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bc54915f27603d346c83ec9056f3063d97df863106ed951f6f27c86a807cef`  
		Last Modified: Tue, 03 Jun 2025 14:28:16 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:1c701c0e3f02c51c0b5a416fe2eeb3515e11fbbad452adcf2a6c750cf1dda44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.1 KB (384135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9313b7324de8a37c1323838da614894068e2e5c005651348296d5318ee9d7d`

```dockerfile
```

-	Layers:
	-	`sha256:9765178dab88f44d5afbb350178567db3bacbce39dbac097bdd793ef4cab928f`  
		Last Modified: Tue, 10 Jun 2025 06:09:21 GMT  
		Size: 368.5 KB (368451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29329adfb7df227bbd4c8aeb6e7b1af9c3cee347c2b209742b71f506b86e41c8`  
		Last Modified: Tue, 10 Jun 2025 06:09:23 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:776798b9951f56ff73ddf9cdafcc51bee2812a140966e66c936c1319ad921b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:e7e52738b6e0bf569fd3cedb08ed8c77b00c97b3ab56157625c798fe34cb6406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153229217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b211a795863372d615eadc5b4c53a0479bba27a7beba855dffa0f108fd1f28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 May 2025 13:09:59 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 May 2025 13:09:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 May 2025 13:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 13:09:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678e87101798c1c992d7c441a146a64a4a76a20702382a0e0ad72a873e291446`  
		Last Modified: Wed, 02 Jul 2025 03:09:59 GMT  
		Size: 7.1 MB (7103261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c26a15a16bdbe250aae6019528bcdfb09b2037b4239c10f7aeaab0edf6fc13e`  
		Last Modified: Wed, 02 Jul 2025 07:22:17 GMT  
		Size: 44.5 MB (44538684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7766f98f67fecf2a4a6c545e95dae0742cd65f4ac55cdd508f9376dc059c1428`  
		Last Modified: Wed, 02 Jul 2025 07:22:21 GMT  
		Size: 72.1 MB (72051065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba942f4c1f31e598a4d1b2c84366703cde0002481f03d18cc1051c5de8c52c2`  
		Last Modified: Wed, 02 Jul 2025 05:46:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6157048c75d4432dbf326add57dccdeec099ac63a260cc62f2daa9121bc591b8`  
		Last Modified: Wed, 02 Jul 2025 05:46:28 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:39f2b69a796d1cb0d0510123074d6baa1f7a202820420befbad26c438794d1cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df07daba630818b12f54ac665b138cf6ec905b1606da4f877a7eb7ac9afc0937`

```dockerfile
```

-	Layers:
	-	`sha256:328570750c505851916b85f47aae0976ef9ade0d9e0e56480fb3bb9292a3094b`  
		Last Modified: Wed, 02 Jul 2025 07:21:23 GMT  
		Size: 3.7 MB (3716964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2cd8f3c51ad22f7e506f7395eeabcb98e7fabd19eed75609282a890c690a559`  
		Last Modified: Wed, 02 Jul 2025 07:21:24 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:7389057fbb6ab456086cec4d38150bbaa7a64c34645a07da6e14a1b68ea07ffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144095235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf8a864000b159cb1445c28416115140279cf5ad6056283448d61cffcd3f01a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 May 2025 13:09:59 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 May 2025 13:09:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 May 2025 13:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 13:09:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44131f96e79008ec3b856a988d4d1fc58f4660f7ca12f41dfc747b162fe5ac2b`  
		Last Modified: Wed, 02 Jul 2025 04:18:53 GMT  
		Size: 7.0 MB (7049144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f42c87db2e6f52e316a4a1ee97021f9ab32ff2ca6871b2de26ee41b237deb4f`  
		Last Modified: Wed, 02 Jul 2025 08:36:47 GMT  
		Size: 41.9 MB (41872519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c9ab37201540012dd00c3ac6a8f249979973800dd9f01e6a70d5c1d9649b54`  
		Last Modified: Wed, 02 Jul 2025 18:36:12 GMT  
		Size: 67.8 MB (67813779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282341eecda9b5dc260dde612876817aaa91be2a7c11bf791e2bc579e3900c26`  
		Last Modified: Wed, 02 Jul 2025 08:37:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22abddff152c8397ff13be2b54ddd839077aac8ca623e0487c4691a9cd00ad7`  
		Last Modified: Wed, 02 Jul 2025 08:37:15 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:a6f5e79b9a8a61515c75d2f98642e04d7a6ee7eb514eaeeabd026bbe130a4308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b1ea7e28c8d5e9869ea65c3129c2cca0d3eca25ccfcbd867dd1d94b4ece39f`

```dockerfile
```

-	Layers:
	-	`sha256:2c1edc1fa273e104742188fd885fcd4eb0b1fb0002277ba5bf848df847a5ec29`  
		Last Modified: Wed, 02 Jul 2025 10:21:26 GMT  
		Size: 3.7 MB (3716438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f6f7621dd1153451fcab779371fd3f407cd2c48a3d8b72b8892bf83c96ae0f3`  
		Last Modified: Wed, 02 Jul 2025 10:21:27 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json
