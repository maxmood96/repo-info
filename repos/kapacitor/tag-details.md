<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.7`](#kapacitor177)
-	[`kapacitor:1.7.7-alpine`](#kapacitor177-alpine)
-	[`kapacitor:1.8`](#kapacitor18)
-	[`kapacitor:1.8-alpine`](#kapacitor18-alpine)
-	[`kapacitor:1.8.4`](#kapacitor184)
-	[`kapacitor:1.8.4-alpine`](#kapacitor184-alpine)
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
$ docker pull kapacitor@sha256:3d7cecac56c01fcf99659885ffe565f7596ec46416fdd273fd2c381cbbf3148a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8` - linux; amd64

```console
$ docker pull kapacitor@sha256:699b72f76b9a248ecd05ad1143e6fc0fc0fb51ba2e112b96ffc9887bccdca26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.0 MB (174022752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2548a31957b8456612fbd0a641e6925d77e37e9c2b4b4c0d8689af5b8a4c55b2`
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
# Fri, 17 Apr 2026 23:04:22 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 17 Apr 2026 23:04:30 GMT
ENV KAPACITOR_VERSION=1.8.4
# Fri, 17 Apr 2026 23:04:30 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 17 Apr 2026 23:04:30 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 17 Apr 2026 23:04:30 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 17 Apr 2026 23:04:30 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 17 Apr 2026 23:04:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 23:04:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 23:04:30 GMT
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
	-	`sha256:b3beef5682cb7b24586fe4a3d3e7318126e5fe8272bd4355bde09fdf77d27470`  
		Last Modified: Fri, 17 Apr 2026 23:04:51 GMT  
		Size: 51.4 MB (51437188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f8eab0b40d93a92cdc619ac9c29a21f5ca961d4ef85bad2899a6c741989a69`  
		Last Modified: Fri, 17 Apr 2026 23:04:52 GMT  
		Size: 85.7 MB (85742153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea028de130d494c837099a1a61a747b716ea2678da4e988b5ff3a2d97299e590`  
		Last Modified: Fri, 17 Apr 2026 23:04:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9aadef0dddaf83fb9b13af5bfab54d170fcb4ac58a0f505ebb044b11ac2aeb4`  
		Last Modified: Fri, 17 Apr 2026 23:04:49 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:173a210c18bb0e01376d593e9b4a9fd07bae3d8fe00f8dcc68a00996e68981d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aecc98699561312aa3d75333c3d3f74bb72d9da0150b13e601b0296435981573`

```dockerfile
```

-	Layers:
	-	`sha256:123890be50005c9ef8821471dc324aac069a34b23a50c84a2c86170c2e4b8859`  
		Last Modified: Fri, 17 Apr 2026 23:04:49 GMT  
		Size: 3.7 MB (3732026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:152b143df9640ac197d92f890a70d2dd623db98d0195928dd25a4adc9ee9ab5e`  
		Last Modified: Fri, 17 Apr 2026 23:04:48 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:11052f6aa60f56a8183da387c50e69c0d978d34e839ddfc784abf71d27dc0d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165170826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2980b688dc52d0baef0b0fc781f4aa2c564a7d977796f14e604dd789b8f8a7`
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
# Fri, 17 Apr 2026 23:04:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 17 Apr 2026 23:04:38 GMT
ENV KAPACITOR_VERSION=1.8.4
# Fri, 17 Apr 2026 23:04:38 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 17 Apr 2026 23:04:38 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 17 Apr 2026 23:04:38 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 17 Apr 2026 23:04:38 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 17 Apr 2026 23:04:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 23:04:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 23:04:39 GMT
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
	-	`sha256:a149c27eb1efac9664516908b95edeff7462eead0c9cd924e316fd298de3521c`  
		Last Modified: Fri, 17 Apr 2026 23:04:58 GMT  
		Size: 50.3 MB (50345945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a5112431f6359412234fd5a88f41d05ac92286f3eb76b6784793d75b512428`  
		Last Modified: Fri, 17 Apr 2026 23:04:59 GMT  
		Size: 80.2 MB (80156689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8a3c29672e5f739f9b8afe63ab5d956a38fc268f5aa7496c41f6ff59433868`  
		Last Modified: Fri, 17 Apr 2026 23:04:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e994c4e716bf2141882295af7108de7d77bb9d67fbeb60c29947de2cd44e5e01`  
		Last Modified: Fri, 17 Apr 2026 23:04:56 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:167ea60c50e441e126245d5d448384518e77ebc013ffc46bf4164324f60937c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec453d97879cb9b6c899acd407fc75b85142b7ee4e1e5f23cb11f0846b5f6b2`

```dockerfile
```

-	Layers:
	-	`sha256:4b2c43a0bfb5095137b6a85f116d74fe756bd1a0f7b69275b0945e24a25400d0`  
		Last Modified: Fri, 17 Apr 2026 23:04:57 GMT  
		Size: 3.7 MB (3731500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebd20beefb033f50d7b265d300710f6f6dd2faea2a30db4accf581d1af274be3`  
		Last Modified: Fri, 17 Apr 2026 23:04:56 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8-alpine`

```console
$ docker pull kapacitor@sha256:0d2289fb587fcae5a397c096b1903672f8c780a91f27e15f2899ed7fbf08e5f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:ee30977237666f3500f38d91b59630b0004e7460e0d7ddd0172b6dad9cdbeb22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89836757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26616d2dbbe6ba9ec3e236425a3e456e55597a0cc647033461bd9644851b9d4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 23:04:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 23:04:59 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 23:05:08 GMT
ENV KAPACITOR_VERSION=1.8.4
# Fri, 17 Apr 2026 23:05:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Fri, 17 Apr 2026 23:05:08 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 17 Apr 2026 23:05:08 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 17 Apr 2026 23:05:08 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 17 Apr 2026 23:05:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 23:05:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 23:05:08 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbca7cf77e31c2a3b887395beddfdcf42ce7bcc3bacd7faca9f1cf7b4e51d8b`  
		Last Modified: Fri, 17 Apr 2026 23:05:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287e478edd268c99bf9802212916b91421e7dd7fea9d1bd1a2568a28f2786f1d`  
		Last Modified: Fri, 17 Apr 2026 23:05:23 GMT  
		Size: 313.1 KB (313056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed034c68fa903a57b6514a2fe36e431ecf65685e68c81b2c414468a6ef1b41e8`  
		Last Modified: Fri, 17 Apr 2026 23:05:26 GMT  
		Size: 85.7 MB (85658710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d9ceffb2bc980b2a4785434922fb81ae0f34673f16e6c73852b9a18a8fa14d`  
		Last Modified: Fri, 17 Apr 2026 23:05:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c242c65b0ad95912acc56d93b5d96504e5216478795ef7be36c20cb07f265c79`  
		Last Modified: Fri, 17 Apr 2026 23:05:24 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:eafc985da7c73cfac194de0fa9f6246332beb29a6a31952680303abec235fb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.1 KB (405052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7da54bf9c72d0d0ba9ff454ca042a2bf5d033e58c60d35a4d7fd79139677705`

```dockerfile
```

-	Layers:
	-	`sha256:20fc2b8fa4308592d6b52d7af4ae3a493f04664746b75294a146cf5759413d76`  
		Last Modified: Fri, 17 Apr 2026 23:05:23 GMT  
		Size: 389.7 KB (389715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb06aa25435c6c18f9b095c29ebc37796cecc7bfd714191ee753b7ac0465dd99`  
		Last Modified: Fri, 17 Apr 2026 23:05:23 GMT  
		Size: 15.3 KB (15337 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.4`

```console
$ docker pull kapacitor@sha256:3d7cecac56c01fcf99659885ffe565f7596ec46416fdd273fd2c381cbbf3148a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8.4` - linux; amd64

```console
$ docker pull kapacitor@sha256:699b72f76b9a248ecd05ad1143e6fc0fc0fb51ba2e112b96ffc9887bccdca26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.0 MB (174022752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2548a31957b8456612fbd0a641e6925d77e37e9c2b4b4c0d8689af5b8a4c55b2`
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
# Fri, 17 Apr 2026 23:04:22 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 17 Apr 2026 23:04:30 GMT
ENV KAPACITOR_VERSION=1.8.4
# Fri, 17 Apr 2026 23:04:30 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 17 Apr 2026 23:04:30 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 17 Apr 2026 23:04:30 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 17 Apr 2026 23:04:30 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 17 Apr 2026 23:04:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 23:04:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 23:04:30 GMT
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
	-	`sha256:b3beef5682cb7b24586fe4a3d3e7318126e5fe8272bd4355bde09fdf77d27470`  
		Last Modified: Fri, 17 Apr 2026 23:04:51 GMT  
		Size: 51.4 MB (51437188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f8eab0b40d93a92cdc619ac9c29a21f5ca961d4ef85bad2899a6c741989a69`  
		Last Modified: Fri, 17 Apr 2026 23:04:52 GMT  
		Size: 85.7 MB (85742153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea028de130d494c837099a1a61a747b716ea2678da4e988b5ff3a2d97299e590`  
		Last Modified: Fri, 17 Apr 2026 23:04:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9aadef0dddaf83fb9b13af5bfab54d170fcb4ac58a0f505ebb044b11ac2aeb4`  
		Last Modified: Fri, 17 Apr 2026 23:04:49 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.4` - unknown; unknown

```console
$ docker pull kapacitor@sha256:173a210c18bb0e01376d593e9b4a9fd07bae3d8fe00f8dcc68a00996e68981d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aecc98699561312aa3d75333c3d3f74bb72d9da0150b13e601b0296435981573`

```dockerfile
```

-	Layers:
	-	`sha256:123890be50005c9ef8821471dc324aac069a34b23a50c84a2c86170c2e4b8859`  
		Last Modified: Fri, 17 Apr 2026 23:04:49 GMT  
		Size: 3.7 MB (3732026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:152b143df9640ac197d92f890a70d2dd623db98d0195928dd25a4adc9ee9ab5e`  
		Last Modified: Fri, 17 Apr 2026 23:04:48 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8.4` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:11052f6aa60f56a8183da387c50e69c0d978d34e839ddfc784abf71d27dc0d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165170826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2980b688dc52d0baef0b0fc781f4aa2c564a7d977796f14e604dd789b8f8a7`
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
# Fri, 17 Apr 2026 23:04:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 17 Apr 2026 23:04:38 GMT
ENV KAPACITOR_VERSION=1.8.4
# Fri, 17 Apr 2026 23:04:38 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 17 Apr 2026 23:04:38 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 17 Apr 2026 23:04:38 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 17 Apr 2026 23:04:38 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 17 Apr 2026 23:04:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 23:04:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 23:04:39 GMT
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
	-	`sha256:a149c27eb1efac9664516908b95edeff7462eead0c9cd924e316fd298de3521c`  
		Last Modified: Fri, 17 Apr 2026 23:04:58 GMT  
		Size: 50.3 MB (50345945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a5112431f6359412234fd5a88f41d05ac92286f3eb76b6784793d75b512428`  
		Last Modified: Fri, 17 Apr 2026 23:04:59 GMT  
		Size: 80.2 MB (80156689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8a3c29672e5f739f9b8afe63ab5d956a38fc268f5aa7496c41f6ff59433868`  
		Last Modified: Fri, 17 Apr 2026 23:04:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e994c4e716bf2141882295af7108de7d77bb9d67fbeb60c29947de2cd44e5e01`  
		Last Modified: Fri, 17 Apr 2026 23:04:56 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.4` - unknown; unknown

```console
$ docker pull kapacitor@sha256:167ea60c50e441e126245d5d448384518e77ebc013ffc46bf4164324f60937c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec453d97879cb9b6c899acd407fc75b85142b7ee4e1e5f23cb11f0846b5f6b2`

```dockerfile
```

-	Layers:
	-	`sha256:4b2c43a0bfb5095137b6a85f116d74fe756bd1a0f7b69275b0945e24a25400d0`  
		Last Modified: Fri, 17 Apr 2026 23:04:57 GMT  
		Size: 3.7 MB (3731500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebd20beefb033f50d7b265d300710f6f6dd2faea2a30db4accf581d1af274be3`  
		Last Modified: Fri, 17 Apr 2026 23:04:56 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.4-alpine`

```console
$ docker pull kapacitor@sha256:0d2289fb587fcae5a397c096b1903672f8c780a91f27e15f2899ed7fbf08e5f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8.4-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:ee30977237666f3500f38d91b59630b0004e7460e0d7ddd0172b6dad9cdbeb22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89836757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26616d2dbbe6ba9ec3e236425a3e456e55597a0cc647033461bd9644851b9d4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 23:04:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 23:04:59 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 23:05:08 GMT
ENV KAPACITOR_VERSION=1.8.4
# Fri, 17 Apr 2026 23:05:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Fri, 17 Apr 2026 23:05:08 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 17 Apr 2026 23:05:08 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 17 Apr 2026 23:05:08 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 17 Apr 2026 23:05:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 23:05:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 23:05:08 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbca7cf77e31c2a3b887395beddfdcf42ce7bcc3bacd7faca9f1cf7b4e51d8b`  
		Last Modified: Fri, 17 Apr 2026 23:05:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287e478edd268c99bf9802212916b91421e7dd7fea9d1bd1a2568a28f2786f1d`  
		Last Modified: Fri, 17 Apr 2026 23:05:23 GMT  
		Size: 313.1 KB (313056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed034c68fa903a57b6514a2fe36e431ecf65685e68c81b2c414468a6ef1b41e8`  
		Last Modified: Fri, 17 Apr 2026 23:05:26 GMT  
		Size: 85.7 MB (85658710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d9ceffb2bc980b2a4785434922fb81ae0f34673f16e6c73852b9a18a8fa14d`  
		Last Modified: Fri, 17 Apr 2026 23:05:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c242c65b0ad95912acc56d93b5d96504e5216478795ef7be36c20cb07f265c79`  
		Last Modified: Fri, 17 Apr 2026 23:05:24 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.4-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:eafc985da7c73cfac194de0fa9f6246332beb29a6a31952680303abec235fb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.1 KB (405052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7da54bf9c72d0d0ba9ff454ca042a2bf5d033e58c60d35a4d7fd79139677705`

```dockerfile
```

-	Layers:
	-	`sha256:20fc2b8fa4308592d6b52d7af4ae3a493f04664746b75294a146cf5759413d76`  
		Last Modified: Fri, 17 Apr 2026 23:05:23 GMT  
		Size: 389.7 KB (389715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb06aa25435c6c18f9b095c29ebc37796cecc7bfd714191ee753b7ac0465dd99`  
		Last Modified: Fri, 17 Apr 2026 23:05:23 GMT  
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
$ docker pull kapacitor@sha256:3d7cecac56c01fcf99659885ffe565f7596ec46416fdd273fd2c381cbbf3148a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:699b72f76b9a248ecd05ad1143e6fc0fc0fb51ba2e112b96ffc9887bccdca26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.0 MB (174022752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2548a31957b8456612fbd0a641e6925d77e37e9c2b4b4c0d8689af5b8a4c55b2`
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
# Fri, 17 Apr 2026 23:04:22 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 17 Apr 2026 23:04:30 GMT
ENV KAPACITOR_VERSION=1.8.4
# Fri, 17 Apr 2026 23:04:30 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 17 Apr 2026 23:04:30 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 17 Apr 2026 23:04:30 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 17 Apr 2026 23:04:30 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 17 Apr 2026 23:04:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 23:04:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 23:04:30 GMT
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
	-	`sha256:b3beef5682cb7b24586fe4a3d3e7318126e5fe8272bd4355bde09fdf77d27470`  
		Last Modified: Fri, 17 Apr 2026 23:04:51 GMT  
		Size: 51.4 MB (51437188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f8eab0b40d93a92cdc619ac9c29a21f5ca961d4ef85bad2899a6c741989a69`  
		Last Modified: Fri, 17 Apr 2026 23:04:52 GMT  
		Size: 85.7 MB (85742153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea028de130d494c837099a1a61a747b716ea2678da4e988b5ff3a2d97299e590`  
		Last Modified: Fri, 17 Apr 2026 23:04:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9aadef0dddaf83fb9b13af5bfab54d170fcb4ac58a0f505ebb044b11ac2aeb4`  
		Last Modified: Fri, 17 Apr 2026 23:04:49 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:173a210c18bb0e01376d593e9b4a9fd07bae3d8fe00f8dcc68a00996e68981d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aecc98699561312aa3d75333c3d3f74bb72d9da0150b13e601b0296435981573`

```dockerfile
```

-	Layers:
	-	`sha256:123890be50005c9ef8821471dc324aac069a34b23a50c84a2c86170c2e4b8859`  
		Last Modified: Fri, 17 Apr 2026 23:04:49 GMT  
		Size: 3.7 MB (3732026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:152b143df9640ac197d92f890a70d2dd623db98d0195928dd25a4adc9ee9ab5e`  
		Last Modified: Fri, 17 Apr 2026 23:04:48 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:11052f6aa60f56a8183da387c50e69c0d978d34e839ddfc784abf71d27dc0d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165170826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2980b688dc52d0baef0b0fc781f4aa2c564a7d977796f14e604dd789b8f8a7`
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
# Fri, 17 Apr 2026 23:04:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 17 Apr 2026 23:04:38 GMT
ENV KAPACITOR_VERSION=1.8.4
# Fri, 17 Apr 2026 23:04:38 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 17 Apr 2026 23:04:38 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 17 Apr 2026 23:04:38 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 17 Apr 2026 23:04:38 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 17 Apr 2026 23:04:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 23:04:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 23:04:39 GMT
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
	-	`sha256:a149c27eb1efac9664516908b95edeff7462eead0c9cd924e316fd298de3521c`  
		Last Modified: Fri, 17 Apr 2026 23:04:58 GMT  
		Size: 50.3 MB (50345945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a5112431f6359412234fd5a88f41d05ac92286f3eb76b6784793d75b512428`  
		Last Modified: Fri, 17 Apr 2026 23:04:59 GMT  
		Size: 80.2 MB (80156689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8a3c29672e5f739f9b8afe63ab5d956a38fc268f5aa7496c41f6ff59433868`  
		Last Modified: Fri, 17 Apr 2026 23:04:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e994c4e716bf2141882295af7108de7d77bb9d67fbeb60c29947de2cd44e5e01`  
		Last Modified: Fri, 17 Apr 2026 23:04:56 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:167ea60c50e441e126245d5d448384518e77ebc013ffc46bf4164324f60937c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec453d97879cb9b6c899acd407fc75b85142b7ee4e1e5f23cb11f0846b5f6b2`

```dockerfile
```

-	Layers:
	-	`sha256:4b2c43a0bfb5095137b6a85f116d74fe756bd1a0f7b69275b0945e24a25400d0`  
		Last Modified: Fri, 17 Apr 2026 23:04:57 GMT  
		Size: 3.7 MB (3731500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebd20beefb033f50d7b265d300710f6f6dd2faea2a30db4accf581d1af274be3`  
		Last Modified: Fri, 17 Apr 2026 23:04:56 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json
