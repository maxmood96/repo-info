<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.7`](#kapacitor177)
-	[`kapacitor:1.7.7-alpine`](#kapacitor177-alpine)
-	[`kapacitor:1.8`](#kapacitor18)
-	[`kapacitor:1.8-alpine`](#kapacitor18-alpine)
-	[`kapacitor:1.8.3`](#kapacitor183)
-	[`kapacitor:1.8.3-alpine`](#kapacitor183-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.7`

```console
$ docker pull kapacitor@sha256:12ae80ac4650f29e5f7d69bec5b938a2e6cf3811beb7fab1ac3a62d1b443aae9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:31ab20fccc84060568dd276c37f6c0b6751df8fca6bc3f141ad2d04c455ec7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160094938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c0b30264f02c3f8536fc1572e86b6716e2bae38005e8851ff1d6ba778d144e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:38:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 15 Apr 2026 21:38:34 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 15 Apr 2026 21:38:34 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 15 Apr 2026 21:38:34 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 15 Apr 2026 21:38:34 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 15 Apr 2026 21:38:34 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 15 Apr 2026 21:38:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:38:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:38:34 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ecec50759c3bd60116bddbffcebabb3dcd76303cf36ce83784b5ba0cf93040`  
		Last Modified: Wed, 15 Apr 2026 20:24:53 GMT  
		Size: 7.1 MB (7106390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d872063ec20ae797630be1cc0444647f3789682c8ed31db054cece983053a3`  
		Last Modified: Wed, 15 Apr 2026 21:38:49 GMT  
		Size: 51.2 MB (51200453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2385b26bb9e3d2d5692619812a16ad20b8297f5eed4538de40b0d7f234d8f0d8`  
		Last Modified: Wed, 15 Apr 2026 21:38:50 GMT  
		Size: 72.1 MB (72051076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d349a5a02ec14b457df7c5a8c4b44e00b8e41992901f2cdf88c51b227d6333ed`  
		Last Modified: Wed, 15 Apr 2026 21:38:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8699d9338a81b1b653c5c16fcd4ba1396d1230b4ea61d86ab36f4dc349d35cd3`  
		Last Modified: Wed, 15 Apr 2026 21:38:47 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:f431c610e8621346f3f14c373f7a743d56da2a6273c649bd0075477de003dd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c6434729296df80cda704912d98d8b30849542fe86f07d2922dc0b61070fa0`

```dockerfile
```

-	Layers:
	-	`sha256:2b6e8a1a24ce93ba7b7595ce705a4f03148a08fdce139e2e87d0c3a827f2d39c`  
		Last Modified: Wed, 15 Apr 2026 21:38:47 GMT  
		Size: 3.7 MB (3716676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d72418d023eb4ee2e49464529512d0987cc36191e905d821c5a1376c72def294`  
		Last Modified: Wed, 15 Apr 2026 21:38:47 GMT  
		Size: 14.7 KB (14716 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:a307725469fbbe286fed80130bd3de04fe9e0d27dec8ae9f7334a43f0f94d4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152507800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c111ca6d1f9454c76ebe77cbd7c040970435624ebea17c8864d384ef94f86809`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:50:22 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 15 Apr 2026 21:50:28 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 15 Apr 2026 21:50:28 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 15 Apr 2026 21:50:28 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 15 Apr 2026 21:50:28 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 15 Apr 2026 21:50:28 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 15 Apr 2026 21:50:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:50:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:50:28 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a5bc53c1a6e7cc1735f8944574d4921d9d23f26d4b1025adf1c324ad2b07b6`  
		Last Modified: Wed, 15 Apr 2026 20:24:21 GMT  
		Size: 7.1 MB (7061127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b391d6fc2b46334ffa468b37a842ec6b756efe6ffac4d34145aa5a73259e1c2f`  
		Last Modified: Wed, 15 Apr 2026 21:50:43 GMT  
		Size: 50.0 MB (50025948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801fda96ef071798f35c4b24202edb709b4aa47f0c268dea7248875f3eb48748`  
		Last Modified: Wed, 15 Apr 2026 21:50:44 GMT  
		Size: 67.8 MB (67813660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699e1547b40b92ccd07d4076a675b386b5de401ff037d0351af6df754b808d8e`  
		Last Modified: Wed, 15 Apr 2026 21:50:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47734d45e24a3a1a5428ee532a92c39e9c0e03d3c59223524960fc6af5786805`  
		Last Modified: Wed, 15 Apr 2026 21:50:41 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:2a2afcf9bf5fbaf9abea9ac892d6846eaed7f80817cf3afd018186c0cab21f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27eabd288efa3965d8010ed5f60ba7c51399f5ad30cd913b8ed3ff9b9343d80`

```dockerfile
```

-	Layers:
	-	`sha256:aa507243e9cf1a7466111e00bcda6ff5e06b9b0e6a5c3d31857f669e606a1bb9`  
		Last Modified: Wed, 15 Apr 2026 21:50:41 GMT  
		Size: 3.7 MB (3716138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6839d3ba660c76a40ce88b705d6eaa8729d03baa7fbad3354d4f312d14ab3146`  
		Last Modified: Wed, 15 Apr 2026 21:50:41 GMT  
		Size: 14.8 KB (14811 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:d413cc02810588e8c459ea5be842408894d80457fd6bf3d17c76054bd4fbeba6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:7dd27bf99a95c88a227895984474aed5a5acd9e005ee8c4ca5d230c5adce430d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75904570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3afb14c37dc00503a0e3d186c16cca67e6e6cf79f380e0768c83b473ab21723`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:29:59 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
ENV KAPACITOR_VERSION=1.7.7
# Fri, 17 Apr 2026 00:30:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 17 Apr 2026 00:30:05 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 17 Apr 2026 00:30:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:05 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e69077797f1a90c5b8946765d6547bd0bbe62c5edf87016fc687d8691b62a`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d26afc56a247d157e5130fafb0c3e1596d90cb798a74bcd18085a2e60f5e83`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 290.8 KB (290778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62dd12f58262d16aa469c538fe54969fbd41faab46b0c454ce33250afdb5cf9`  
		Last Modified: Fri, 17 Apr 2026 00:30:19 GMT  
		Size: 72.0 MB (71982697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55baa52346461779ddbbe16b9bcbe892cdd293e258d25759833687ed332ec26f`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b697b2c16e0d0a74ce9cec7f52e70573e6c357c63cea20d805fa64c4bd2a984c`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:c43b268a38b55473ac82d1c64d91b2abf473cfd8498dadaf61b7b610b7a0a384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.5 KB (381476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c6c8a59270545d801e93fbec290d5e3507d4c0ef7d1b17af7ac1a44b9f91e2`

```dockerfile
```

-	Layers:
	-	`sha256:5e93c3927eafe526f00d32bfce704d302d02d4cbe2d4104d9f70f6c2132c0cee`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 365.8 KB (365835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d021a80b9241fd4aceb41e3907131caf439210759adcdaa248d89c1e12091d7`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 15.6 KB (15641 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.7`

```console
$ docker pull kapacitor@sha256:12ae80ac4650f29e5f7d69bec5b938a2e6cf3811beb7fab1ac3a62d1b443aae9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:31ab20fccc84060568dd276c37f6c0b6751df8fca6bc3f141ad2d04c455ec7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160094938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c0b30264f02c3f8536fc1572e86b6716e2bae38005e8851ff1d6ba778d144e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:38:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 15 Apr 2026 21:38:34 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 15 Apr 2026 21:38:34 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 15 Apr 2026 21:38:34 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 15 Apr 2026 21:38:34 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 15 Apr 2026 21:38:34 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 15 Apr 2026 21:38:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:38:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:38:34 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ecec50759c3bd60116bddbffcebabb3dcd76303cf36ce83784b5ba0cf93040`  
		Last Modified: Wed, 15 Apr 2026 20:24:53 GMT  
		Size: 7.1 MB (7106390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d872063ec20ae797630be1cc0444647f3789682c8ed31db054cece983053a3`  
		Last Modified: Wed, 15 Apr 2026 21:38:49 GMT  
		Size: 51.2 MB (51200453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2385b26bb9e3d2d5692619812a16ad20b8297f5eed4538de40b0d7f234d8f0d8`  
		Last Modified: Wed, 15 Apr 2026 21:38:50 GMT  
		Size: 72.1 MB (72051076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d349a5a02ec14b457df7c5a8c4b44e00b8e41992901f2cdf88c51b227d6333ed`  
		Last Modified: Wed, 15 Apr 2026 21:38:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8699d9338a81b1b653c5c16fcd4ba1396d1230b4ea61d86ab36f4dc349d35cd3`  
		Last Modified: Wed, 15 Apr 2026 21:38:47 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:f431c610e8621346f3f14c373f7a743d56da2a6273c649bd0075477de003dd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c6434729296df80cda704912d98d8b30849542fe86f07d2922dc0b61070fa0`

```dockerfile
```

-	Layers:
	-	`sha256:2b6e8a1a24ce93ba7b7595ce705a4f03148a08fdce139e2e87d0c3a827f2d39c`  
		Last Modified: Wed, 15 Apr 2026 21:38:47 GMT  
		Size: 3.7 MB (3716676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d72418d023eb4ee2e49464529512d0987cc36191e905d821c5a1376c72def294`  
		Last Modified: Wed, 15 Apr 2026 21:38:47 GMT  
		Size: 14.7 KB (14716 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:a307725469fbbe286fed80130bd3de04fe9e0d27dec8ae9f7334a43f0f94d4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152507800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c111ca6d1f9454c76ebe77cbd7c040970435624ebea17c8864d384ef94f86809`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:50:22 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 15 Apr 2026 21:50:28 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 15 Apr 2026 21:50:28 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 15 Apr 2026 21:50:28 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 15 Apr 2026 21:50:28 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 15 Apr 2026 21:50:28 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 15 Apr 2026 21:50:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:50:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:50:28 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a5bc53c1a6e7cc1735f8944574d4921d9d23f26d4b1025adf1c324ad2b07b6`  
		Last Modified: Wed, 15 Apr 2026 20:24:21 GMT  
		Size: 7.1 MB (7061127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b391d6fc2b46334ffa468b37a842ec6b756efe6ffac4d34145aa5a73259e1c2f`  
		Last Modified: Wed, 15 Apr 2026 21:50:43 GMT  
		Size: 50.0 MB (50025948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801fda96ef071798f35c4b24202edb709b4aa47f0c268dea7248875f3eb48748`  
		Last Modified: Wed, 15 Apr 2026 21:50:44 GMT  
		Size: 67.8 MB (67813660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699e1547b40b92ccd07d4076a675b386b5de401ff037d0351af6df754b808d8e`  
		Last Modified: Wed, 15 Apr 2026 21:50:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47734d45e24a3a1a5428ee532a92c39e9c0e03d3c59223524960fc6af5786805`  
		Last Modified: Wed, 15 Apr 2026 21:50:41 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:2a2afcf9bf5fbaf9abea9ac892d6846eaed7f80817cf3afd018186c0cab21f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27eabd288efa3965d8010ed5f60ba7c51399f5ad30cd913b8ed3ff9b9343d80`

```dockerfile
```

-	Layers:
	-	`sha256:aa507243e9cf1a7466111e00bcda6ff5e06b9b0e6a5c3d31857f669e606a1bb9`  
		Last Modified: Wed, 15 Apr 2026 21:50:41 GMT  
		Size: 3.7 MB (3716138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6839d3ba660c76a40ce88b705d6eaa8729d03baa7fbad3354d4f312d14ab3146`  
		Last Modified: Wed, 15 Apr 2026 21:50:41 GMT  
		Size: 14.8 KB (14811 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.7-alpine`

```console
$ docker pull kapacitor@sha256:d413cc02810588e8c459ea5be842408894d80457fd6bf3d17c76054bd4fbeba6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:7dd27bf99a95c88a227895984474aed5a5acd9e005ee8c4ca5d230c5adce430d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75904570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3afb14c37dc00503a0e3d186c16cca67e6e6cf79f380e0768c83b473ab21723`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:29:59 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
ENV KAPACITOR_VERSION=1.7.7
# Fri, 17 Apr 2026 00:30:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 17 Apr 2026 00:30:05 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 17 Apr 2026 00:30:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:05 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e69077797f1a90c5b8946765d6547bd0bbe62c5edf87016fc687d8691b62a`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d26afc56a247d157e5130fafb0c3e1596d90cb798a74bcd18085a2e60f5e83`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 290.8 KB (290778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62dd12f58262d16aa469c538fe54969fbd41faab46b0c454ce33250afdb5cf9`  
		Last Modified: Fri, 17 Apr 2026 00:30:19 GMT  
		Size: 72.0 MB (71982697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55baa52346461779ddbbe16b9bcbe892cdd293e258d25759833687ed332ec26f`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b697b2c16e0d0a74ce9cec7f52e70573e6c357c63cea20d805fa64c4bd2a984c`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:c43b268a38b55473ac82d1c64d91b2abf473cfd8498dadaf61b7b610b7a0a384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.5 KB (381476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c6c8a59270545d801e93fbec290d5e3507d4c0ef7d1b17af7ac1a44b9f91e2`

```dockerfile
```

-	Layers:
	-	`sha256:5e93c3927eafe526f00d32bfce704d302d02d4cbe2d4104d9f70f6c2132c0cee`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 365.8 KB (365835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d021a80b9241fd4aceb41e3907131caf439210759adcdaa248d89c1e12091d7`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 15.6 KB (15641 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8`

```console
$ docker pull kapacitor@sha256:5df91bcb0474b6d08bf0ffa369b82e62b8a0fb4fef519222b363828881f9ee0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8` - linux; amd64

```console
$ docker pull kapacitor@sha256:c0855e9cd530f07cc10be83981e9614e7034719b94dd5a969e6c0b645ba58120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173760985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5674827fdcb913babbef9302cd7bdbfd417fa976b5eb81d1aa1c5e8c8bf73bbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:38:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 15 Apr 2026 21:38:39 GMT
ENV KAPACITOR_VERSION=1.8.3
# Wed, 15 Apr 2026 21:38:39 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 15 Apr 2026 21:38:39 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 15 Apr 2026 21:38:39 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 15 Apr 2026 21:38:39 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 15 Apr 2026 21:38:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:38:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:38:39 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ecec50759c3bd60116bddbffcebabb3dcd76303cf36ce83784b5ba0cf93040`  
		Last Modified: Wed, 15 Apr 2026 20:24:53 GMT  
		Size: 7.1 MB (7106390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0355fd0a289c9e1fc0e582341ee884ee3b5f51ea2f62216592cac166ca5886`  
		Last Modified: Wed, 15 Apr 2026 21:38:59 GMT  
		Size: 51.2 MB (51200434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9ef7bc84021a181a8301526bcb11e66e019b6b537652edc516d8c316b9610d`  
		Last Modified: Wed, 15 Apr 2026 21:38:59 GMT  
		Size: 85.7 MB (85717143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9bb17e0cc34f462b8be7cba31ae11940c055cfafb9c9a36d7870beaf1eb1f2`  
		Last Modified: Wed, 15 Apr 2026 21:38:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c9475db5d34d016f3b0cc16792c2b9a9d73870286835a2dd79c2681a73b469`  
		Last Modified: Wed, 15 Apr 2026 21:38:56 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:a5cb547d06870d1af4058f1f4c7d62087a8cd88735e1bccfe492fdbb0fe98795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a38cbbbe2ced84f85bfb8a7bbbc6ff676b0ceda8665914de1c6832c1cd675f1`

```dockerfile
```

-	Layers:
	-	`sha256:78c41c67c140ce31bca87928a740b31bade0de7fb9fa311abe59731bc5729ab0`  
		Last Modified: Wed, 15 Apr 2026 21:38:57 GMT  
		Size: 3.7 MB (3732026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:271d8add4bad5c63d1e4ca0e4fa86512f0d66fc59d414346cba2bbaa8b3c9d31`  
		Last Modified: Wed, 15 Apr 2026 21:38:56 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:de7a0de979d59d1fac479ace99d43117842726b941460a075bec3dc7849046ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164837935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5517d2b4f020ed444ddf72ca356398bb36a3fb69bdbfb1abde2a7facb791bd70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:50:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 15 Apr 2026 21:50:30 GMT
ENV KAPACITOR_VERSION=1.8.3
# Wed, 15 Apr 2026 21:50:30 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 15 Apr 2026 21:50:30 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 15 Apr 2026 21:50:30 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 15 Apr 2026 21:50:30 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 15 Apr 2026 21:50:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:50:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:50:30 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a5bc53c1a6e7cc1735f8944574d4921d9d23f26d4b1025adf1c324ad2b07b6`  
		Last Modified: Wed, 15 Apr 2026 20:24:21 GMT  
		Size: 7.1 MB (7061127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8253c17f41481d9665070d5329435bfe22d3462ed60ac866d6bdd1b31897f1`  
		Last Modified: Wed, 15 Apr 2026 21:50:51 GMT  
		Size: 50.0 MB (50025919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a94ae577fdd1ed6a07d39c6f0082568b7813d2851eefed166b2fff1d112e8f`  
		Last Modified: Wed, 15 Apr 2026 21:50:51 GMT  
		Size: 80.1 MB (80143825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfabb3b05d8d7aa18e9e44904bdeda34473e52ec5630228af11a5d792fc1210c`  
		Last Modified: Wed, 15 Apr 2026 21:50:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47734d45e24a3a1a5428ee532a92c39e9c0e03d3c59223524960fc6af5786805`  
		Last Modified: Wed, 15 Apr 2026 21:50:41 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:6bc6729705f6d72c3e41900a4af5d314af7409d5ede3fb750ce0907a005a9719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be03f0d05a52eacd2219f438a6d435375b33e3dae45578537a1ad280fc5fbfb0`

```dockerfile
```

-	Layers:
	-	`sha256:9dc615d2b0978915bdf645b98590c637052699f053efa9805725d39a7d753dd3`  
		Last Modified: Wed, 15 Apr 2026 21:50:48 GMT  
		Size: 3.7 MB (3731500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:658a3d3158e6b073d70109ae3306b49721d52a818d0b72669cc0492e4569eabd`  
		Last Modified: Wed, 15 Apr 2026 21:50:48 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8-alpine`

```console
$ docker pull kapacitor@sha256:8f93b4719a695800ef0205cd67b81a05742f5eb39be5e79431cb9d8d23e9fe5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:5048ec7e26f89f356d6757cca3e88b17170a180e2b2c9553b1eafe36aa3000d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89769005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afda6ea0147f33ecaf87ef60fca6a960fb88271250b392e27c8e1510b2b6c151`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:30:13 GMT
ENV KAPACITOR_VERSION=1.8.3
# Fri, 17 Apr 2026 00:30:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Fri, 17 Apr 2026 00:30:14 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 17 Apr 2026 00:30:14 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 17 Apr 2026 00:30:14 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 17 Apr 2026 00:30:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:14 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7600c85c12c2ddea00a9ffd598e19d68011c93d7ff61b76b12d615b618d996`  
		Last Modified: Fri, 17 Apr 2026 00:30:27 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84d70e9e59e04b2f75a8baaf0c314273eee2dc5008619ad29f41800a63a1a31`  
		Last Modified: Fri, 17 Apr 2026 00:30:27 GMT  
		Size: 312.2 KB (312186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e129d6ca8cd99a1e93ee26bb88b137ac94c569d5552512899ce8bee3c225d5`  
		Last Modified: Fri, 17 Apr 2026 00:30:30 GMT  
		Size: 85.6 MB (85647831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423b8e9d00199c8917dfbe7200cbc09673af2f53f1f6e3b72e703bcea5169164`  
		Last Modified: Fri, 17 Apr 2026 00:30:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b99004e6f6eb0effdd787277e195acd18389ff25e6383090577fdc2cb74c73`  
		Last Modified: Fri, 17 Apr 2026 00:30:29 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:6004a9c8100c6533266b01d2d759534fbd85ed464935129af283748b0a323de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.3 KB (406323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c03a6c08967867981d35dddb081fda7545d049072e8eee94272bd7ab9b08c6`

```dockerfile
```

-	Layers:
	-	`sha256:3583731805b7e8bf8957226e3ab500e773928d18519f5357c98c0c07807fc2e9`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 391.0 KB (390986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01aa1961366d235bb96e30432c6a41f2c2e37b5d9216893d26d499da7121377e`  
		Last Modified: Fri, 17 Apr 2026 00:30:27 GMT  
		Size: 15.3 KB (15337 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.3`

```console
$ docker pull kapacitor@sha256:5df91bcb0474b6d08bf0ffa369b82e62b8a0fb4fef519222b363828881f9ee0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8.3` - linux; amd64

```console
$ docker pull kapacitor@sha256:c0855e9cd530f07cc10be83981e9614e7034719b94dd5a969e6c0b645ba58120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173760985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5674827fdcb913babbef9302cd7bdbfd417fa976b5eb81d1aa1c5e8c8bf73bbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:38:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 15 Apr 2026 21:38:39 GMT
ENV KAPACITOR_VERSION=1.8.3
# Wed, 15 Apr 2026 21:38:39 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 15 Apr 2026 21:38:39 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 15 Apr 2026 21:38:39 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 15 Apr 2026 21:38:39 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 15 Apr 2026 21:38:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:38:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:38:39 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ecec50759c3bd60116bddbffcebabb3dcd76303cf36ce83784b5ba0cf93040`  
		Last Modified: Wed, 15 Apr 2026 20:24:53 GMT  
		Size: 7.1 MB (7106390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0355fd0a289c9e1fc0e582341ee884ee3b5f51ea2f62216592cac166ca5886`  
		Last Modified: Wed, 15 Apr 2026 21:38:59 GMT  
		Size: 51.2 MB (51200434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9ef7bc84021a181a8301526bcb11e66e019b6b537652edc516d8c316b9610d`  
		Last Modified: Wed, 15 Apr 2026 21:38:59 GMT  
		Size: 85.7 MB (85717143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9bb17e0cc34f462b8be7cba31ae11940c055cfafb9c9a36d7870beaf1eb1f2`  
		Last Modified: Wed, 15 Apr 2026 21:38:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c9475db5d34d016f3b0cc16792c2b9a9d73870286835a2dd79c2681a73b469`  
		Last Modified: Wed, 15 Apr 2026 21:38:56 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.3` - unknown; unknown

```console
$ docker pull kapacitor@sha256:a5cb547d06870d1af4058f1f4c7d62087a8cd88735e1bccfe492fdbb0fe98795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a38cbbbe2ced84f85bfb8a7bbbc6ff676b0ceda8665914de1c6832c1cd675f1`

```dockerfile
```

-	Layers:
	-	`sha256:78c41c67c140ce31bca87928a740b31bade0de7fb9fa311abe59731bc5729ab0`  
		Last Modified: Wed, 15 Apr 2026 21:38:57 GMT  
		Size: 3.7 MB (3732026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:271d8add4bad5c63d1e4ca0e4fa86512f0d66fc59d414346cba2bbaa8b3c9d31`  
		Last Modified: Wed, 15 Apr 2026 21:38:56 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8.3` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:de7a0de979d59d1fac479ace99d43117842726b941460a075bec3dc7849046ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164837935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5517d2b4f020ed444ddf72ca356398bb36a3fb69bdbfb1abde2a7facb791bd70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:50:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 15 Apr 2026 21:50:30 GMT
ENV KAPACITOR_VERSION=1.8.3
# Wed, 15 Apr 2026 21:50:30 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 15 Apr 2026 21:50:30 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 15 Apr 2026 21:50:30 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 15 Apr 2026 21:50:30 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 15 Apr 2026 21:50:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:50:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:50:30 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a5bc53c1a6e7cc1735f8944574d4921d9d23f26d4b1025adf1c324ad2b07b6`  
		Last Modified: Wed, 15 Apr 2026 20:24:21 GMT  
		Size: 7.1 MB (7061127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8253c17f41481d9665070d5329435bfe22d3462ed60ac866d6bdd1b31897f1`  
		Last Modified: Wed, 15 Apr 2026 21:50:51 GMT  
		Size: 50.0 MB (50025919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a94ae577fdd1ed6a07d39c6f0082568b7813d2851eefed166b2fff1d112e8f`  
		Last Modified: Wed, 15 Apr 2026 21:50:51 GMT  
		Size: 80.1 MB (80143825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfabb3b05d8d7aa18e9e44904bdeda34473e52ec5630228af11a5d792fc1210c`  
		Last Modified: Wed, 15 Apr 2026 21:50:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47734d45e24a3a1a5428ee532a92c39e9c0e03d3c59223524960fc6af5786805`  
		Last Modified: Wed, 15 Apr 2026 21:50:41 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.3` - unknown; unknown

```console
$ docker pull kapacitor@sha256:6bc6729705f6d72c3e41900a4af5d314af7409d5ede3fb750ce0907a005a9719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be03f0d05a52eacd2219f438a6d435375b33e3dae45578537a1ad280fc5fbfb0`

```dockerfile
```

-	Layers:
	-	`sha256:9dc615d2b0978915bdf645b98590c637052699f053efa9805725d39a7d753dd3`  
		Last Modified: Wed, 15 Apr 2026 21:50:48 GMT  
		Size: 3.7 MB (3731500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:658a3d3158e6b073d70109ae3306b49721d52a818d0b72669cc0492e4569eabd`  
		Last Modified: Wed, 15 Apr 2026 21:50:48 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.3-alpine`

```console
$ docker pull kapacitor@sha256:8f93b4719a695800ef0205cd67b81a05742f5eb39be5e79431cb9d8d23e9fe5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8.3-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:5048ec7e26f89f356d6757cca3e88b17170a180e2b2c9553b1eafe36aa3000d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89769005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afda6ea0147f33ecaf87ef60fca6a960fb88271250b392e27c8e1510b2b6c151`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:30:13 GMT
ENV KAPACITOR_VERSION=1.8.3
# Fri, 17 Apr 2026 00:30:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Fri, 17 Apr 2026 00:30:14 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 17 Apr 2026 00:30:14 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 17 Apr 2026 00:30:14 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 17 Apr 2026 00:30:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:14 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7600c85c12c2ddea00a9ffd598e19d68011c93d7ff61b76b12d615b618d996`  
		Last Modified: Fri, 17 Apr 2026 00:30:27 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84d70e9e59e04b2f75a8baaf0c314273eee2dc5008619ad29f41800a63a1a31`  
		Last Modified: Fri, 17 Apr 2026 00:30:27 GMT  
		Size: 312.2 KB (312186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e129d6ca8cd99a1e93ee26bb88b137ac94c569d5552512899ce8bee3c225d5`  
		Last Modified: Fri, 17 Apr 2026 00:30:30 GMT  
		Size: 85.6 MB (85647831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423b8e9d00199c8917dfbe7200cbc09673af2f53f1f6e3b72e703bcea5169164`  
		Last Modified: Fri, 17 Apr 2026 00:30:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b99004e6f6eb0effdd787277e195acd18389ff25e6383090577fdc2cb74c73`  
		Last Modified: Fri, 17 Apr 2026 00:30:29 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.3-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:6004a9c8100c6533266b01d2d759534fbd85ed464935129af283748b0a323de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.3 KB (406323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c03a6c08967867981d35dddb081fda7545d049072e8eee94272bd7ab9b08c6`

```dockerfile
```

-	Layers:
	-	`sha256:3583731805b7e8bf8957226e3ab500e773928d18519f5357c98c0c07807fc2e9`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 391.0 KB (390986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01aa1961366d235bb96e30432c6a41f2c2e37b5d9216893d26d499da7121377e`  
		Last Modified: Fri, 17 Apr 2026 00:30:27 GMT  
		Size: 15.3 KB (15337 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:d413cc02810588e8c459ea5be842408894d80457fd6bf3d17c76054bd4fbeba6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:7dd27bf99a95c88a227895984474aed5a5acd9e005ee8c4ca5d230c5adce430d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75904570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3afb14c37dc00503a0e3d186c16cca67e6e6cf79f380e0768c83b473ab21723`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:29:59 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
ENV KAPACITOR_VERSION=1.7.7
# Fri, 17 Apr 2026 00:30:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 17 Apr 2026 00:30:05 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 17 Apr 2026 00:30:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:05 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e69077797f1a90c5b8946765d6547bd0bbe62c5edf87016fc687d8691b62a`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d26afc56a247d157e5130fafb0c3e1596d90cb798a74bcd18085a2e60f5e83`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 290.8 KB (290778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62dd12f58262d16aa469c538fe54969fbd41faab46b0c454ce33250afdb5cf9`  
		Last Modified: Fri, 17 Apr 2026 00:30:19 GMT  
		Size: 72.0 MB (71982697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55baa52346461779ddbbe16b9bcbe892cdd293e258d25759833687ed332ec26f`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b697b2c16e0d0a74ce9cec7f52e70573e6c357c63cea20d805fa64c4bd2a984c`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:c43b268a38b55473ac82d1c64d91b2abf473cfd8498dadaf61b7b610b7a0a384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.5 KB (381476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c6c8a59270545d801e93fbec290d5e3507d4c0ef7d1b17af7ac1a44b9f91e2`

```dockerfile
```

-	Layers:
	-	`sha256:5e93c3927eafe526f00d32bfce704d302d02d4cbe2d4104d9f70f6c2132c0cee`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 365.8 KB (365835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d021a80b9241fd4aceb41e3907131caf439210759adcdaa248d89c1e12091d7`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 15.6 KB (15641 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:5df91bcb0474b6d08bf0ffa369b82e62b8a0fb4fef519222b363828881f9ee0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:c0855e9cd530f07cc10be83981e9614e7034719b94dd5a969e6c0b645ba58120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173760985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5674827fdcb913babbef9302cd7bdbfd417fa976b5eb81d1aa1c5e8c8bf73bbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:38:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 15 Apr 2026 21:38:39 GMT
ENV KAPACITOR_VERSION=1.8.3
# Wed, 15 Apr 2026 21:38:39 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 15 Apr 2026 21:38:39 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 15 Apr 2026 21:38:39 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 15 Apr 2026 21:38:39 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 15 Apr 2026 21:38:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:38:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:38:39 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ecec50759c3bd60116bddbffcebabb3dcd76303cf36ce83784b5ba0cf93040`  
		Last Modified: Wed, 15 Apr 2026 20:24:53 GMT  
		Size: 7.1 MB (7106390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0355fd0a289c9e1fc0e582341ee884ee3b5f51ea2f62216592cac166ca5886`  
		Last Modified: Wed, 15 Apr 2026 21:38:59 GMT  
		Size: 51.2 MB (51200434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9ef7bc84021a181a8301526bcb11e66e019b6b537652edc516d8c316b9610d`  
		Last Modified: Wed, 15 Apr 2026 21:38:59 GMT  
		Size: 85.7 MB (85717143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9bb17e0cc34f462b8be7cba31ae11940c055cfafb9c9a36d7870beaf1eb1f2`  
		Last Modified: Wed, 15 Apr 2026 21:38:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c9475db5d34d016f3b0cc16792c2b9a9d73870286835a2dd79c2681a73b469`  
		Last Modified: Wed, 15 Apr 2026 21:38:56 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:a5cb547d06870d1af4058f1f4c7d62087a8cd88735e1bccfe492fdbb0fe98795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a38cbbbe2ced84f85bfb8a7bbbc6ff676b0ceda8665914de1c6832c1cd675f1`

```dockerfile
```

-	Layers:
	-	`sha256:78c41c67c140ce31bca87928a740b31bade0de7fb9fa311abe59731bc5729ab0`  
		Last Modified: Wed, 15 Apr 2026 21:38:57 GMT  
		Size: 3.7 MB (3732026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:271d8add4bad5c63d1e4ca0e4fa86512f0d66fc59d414346cba2bbaa8b3c9d31`  
		Last Modified: Wed, 15 Apr 2026 21:38:56 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:de7a0de979d59d1fac479ace99d43117842726b941460a075bec3dc7849046ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164837935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5517d2b4f020ed444ddf72ca356398bb36a3fb69bdbfb1abde2a7facb791bd70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:50:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 15 Apr 2026 21:50:30 GMT
ENV KAPACITOR_VERSION=1.8.3
# Wed, 15 Apr 2026 21:50:30 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 15 Apr 2026 21:50:30 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 15 Apr 2026 21:50:30 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 15 Apr 2026 21:50:30 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 15 Apr 2026 21:50:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:50:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:50:30 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a5bc53c1a6e7cc1735f8944574d4921d9d23f26d4b1025adf1c324ad2b07b6`  
		Last Modified: Wed, 15 Apr 2026 20:24:21 GMT  
		Size: 7.1 MB (7061127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8253c17f41481d9665070d5329435bfe22d3462ed60ac866d6bdd1b31897f1`  
		Last Modified: Wed, 15 Apr 2026 21:50:51 GMT  
		Size: 50.0 MB (50025919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a94ae577fdd1ed6a07d39c6f0082568b7813d2851eefed166b2fff1d112e8f`  
		Last Modified: Wed, 15 Apr 2026 21:50:51 GMT  
		Size: 80.1 MB (80143825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfabb3b05d8d7aa18e9e44904bdeda34473e52ec5630228af11a5d792fc1210c`  
		Last Modified: Wed, 15 Apr 2026 21:50:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47734d45e24a3a1a5428ee532a92c39e9c0e03d3c59223524960fc6af5786805`  
		Last Modified: Wed, 15 Apr 2026 21:50:41 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:6bc6729705f6d72c3e41900a4af5d314af7409d5ede3fb750ce0907a005a9719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be03f0d05a52eacd2219f438a6d435375b33e3dae45578537a1ad280fc5fbfb0`

```dockerfile
```

-	Layers:
	-	`sha256:9dc615d2b0978915bdf645b98590c637052699f053efa9805725d39a7d753dd3`  
		Last Modified: Wed, 15 Apr 2026 21:50:48 GMT  
		Size: 3.7 MB (3731500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:658a3d3158e6b073d70109ae3306b49721d52a818d0b72669cc0492e4569eabd`  
		Last Modified: Wed, 15 Apr 2026 21:50:48 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json
