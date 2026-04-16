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
$ docker pull kapacitor@sha256:656c2dd86b1a11c9fa73c985a54bb4cb335be38e3b70e7d7a98b7dd6bb316c20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:b1d61f6c9d7eedf07f7f421c39d7f4ae7873feda2f507b638c5f41d926c3cf5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75903698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168fcf9b2f142305619b781d38caee32bb205260c8f6b488640d37f280ee3c4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:27:05 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:27:05 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:27:11 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 Jan 2026 03:27:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 Jan 2026 03:27:12 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 Jan 2026 03:27:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:12 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a585510c235336f1b768ba7a6bf719de8862edd4de8bab4478f7143dd713ec`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09eb36c87d43883a2445c1cc908f02d656272af80af315350c48ed43226abf8`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 292.5 KB (292469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d03f75f30654c33dd087a69f5886f260f34677b2a96b36e3eea9c24463859ff`  
		Last Modified: Wed, 28 Jan 2026 03:27:24 GMT  
		Size: 72.0 MB (71982585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e37e8342e3694b5063b4991c1590a9422921ca7d4b546ef869d103f6fa04b9`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d21e4716448dd70a66c3fd55b61f1785b3d5986c261ed93b8ad038da9148135`  
		Last Modified: Wed, 28 Jan 2026 03:27:23 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:5003cd167566bb65defab27200a7d312c071e712e46749d5cdd35d3e1e3ceb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 KB (382162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4f2c0991bc53bb04c83c53a02fd6a5c9242159e43ab17158ffb778aa343c8e`

```dockerfile
```

-	Layers:
	-	`sha256:88336f50a8e4328e09abfae2f573fc9edf649cfa0c6d3a785238d3b1c703b49f`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 366.5 KB (366522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff17a7f1d689f60bc9158243e3980a866fa6d4ce9b91ec9f4688fecbab497f60`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 15.6 KB (15640 bytes)  
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
$ docker pull kapacitor@sha256:656c2dd86b1a11c9fa73c985a54bb4cb335be38e3b70e7d7a98b7dd6bb316c20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:b1d61f6c9d7eedf07f7f421c39d7f4ae7873feda2f507b638c5f41d926c3cf5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75903698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168fcf9b2f142305619b781d38caee32bb205260c8f6b488640d37f280ee3c4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:27:05 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:27:05 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:27:11 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 Jan 2026 03:27:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 Jan 2026 03:27:12 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 Jan 2026 03:27:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:12 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a585510c235336f1b768ba7a6bf719de8862edd4de8bab4478f7143dd713ec`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09eb36c87d43883a2445c1cc908f02d656272af80af315350c48ed43226abf8`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 292.5 KB (292469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d03f75f30654c33dd087a69f5886f260f34677b2a96b36e3eea9c24463859ff`  
		Last Modified: Wed, 28 Jan 2026 03:27:24 GMT  
		Size: 72.0 MB (71982585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e37e8342e3694b5063b4991c1590a9422921ca7d4b546ef869d103f6fa04b9`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d21e4716448dd70a66c3fd55b61f1785b3d5986c261ed93b8ad038da9148135`  
		Last Modified: Wed, 28 Jan 2026 03:27:23 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:5003cd167566bb65defab27200a7d312c071e712e46749d5cdd35d3e1e3ceb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 KB (382162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4f2c0991bc53bb04c83c53a02fd6a5c9242159e43ab17158ffb778aa343c8e`

```dockerfile
```

-	Layers:
	-	`sha256:88336f50a8e4328e09abfae2f573fc9edf649cfa0c6d3a785238d3b1c703b49f`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 366.5 KB (366522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff17a7f1d689f60bc9158243e3980a866fa6d4ce9b91ec9f4688fecbab497f60`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 15.6 KB (15640 bytes)  
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
$ docker pull kapacitor@sha256:df40767f92f21632e43fcdea811a98a7155deba8ccbad1eb34d95276f028de89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:8032a02add12a7a4d55a9d1286c55621e2a49e67863c3a97f90af2775bdc1878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89768225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af40bddf792c673011b6d23a2414fc750bb23561d91c6ca7a2f3753afe2088dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 18:15:47 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 11 Mar 2026 18:15:47 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
ENV KAPACITOR_VERSION=1.8.3
# Wed, 11 Mar 2026 18:15:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 11 Mar 2026 18:15:56 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 11 Mar 2026 18:15:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Mar 2026 18:15:56 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3d23749b45de6d1bff188c596b64bf8cbc4571f640a0742fde8914fd06de31`  
		Last Modified: Wed, 11 Mar 2026 18:16:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318adb4486d9748c72594fac0d372a52e8c23ccc7b9b968b10c91c546aa20706`  
		Last Modified: Wed, 11 Mar 2026 18:16:11 GMT  
		Size: 314.6 KB (314631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ad5e5278bc2c70818690289be2d242b0b4c8c19a0e3760baee03e61a353f1b`  
		Last Modified: Wed, 11 Mar 2026 18:16:13 GMT  
		Size: 85.6 MB (85647918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0cc42bef465492e58bc45a66f45063734b6dfa2c35f122b2e4d727725fb078`  
		Last Modified: Wed, 11 Mar 2026 18:16:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a25094aa2b4871d5b57710ea8c2744cb8f6e6ae0925f30a54d1fdec23b11574`  
		Last Modified: Wed, 11 Mar 2026 18:16:13 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:2078676dd7e1327521aaf5f507135e1dfc297e9cde91d98d759f268ef4a2b7f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.0 KB (407010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bac43789d9959dd74126116e44626a56414434faf48d68ab2b7a1b12a037e04`

```dockerfile
```

-	Layers:
	-	`sha256:746d6873825a09596eb9871f68ce272afc4890afa70e6db536387eea343f78d7`  
		Last Modified: Wed, 11 Mar 2026 18:16:11 GMT  
		Size: 391.7 KB (391673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a6968954b0b936cfb18afe3e011b520c21cdddf0d857adbc50f887bc02fdf0f`  
		Last Modified: Wed, 11 Mar 2026 18:16:11 GMT  
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
$ docker pull kapacitor@sha256:df40767f92f21632e43fcdea811a98a7155deba8ccbad1eb34d95276f028de89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8.3-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:8032a02add12a7a4d55a9d1286c55621e2a49e67863c3a97f90af2775bdc1878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89768225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af40bddf792c673011b6d23a2414fc750bb23561d91c6ca7a2f3753afe2088dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 18:15:47 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 11 Mar 2026 18:15:47 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
ENV KAPACITOR_VERSION=1.8.3
# Wed, 11 Mar 2026 18:15:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 11 Mar 2026 18:15:56 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 11 Mar 2026 18:15:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Mar 2026 18:15:56 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3d23749b45de6d1bff188c596b64bf8cbc4571f640a0742fde8914fd06de31`  
		Last Modified: Wed, 11 Mar 2026 18:16:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318adb4486d9748c72594fac0d372a52e8c23ccc7b9b968b10c91c546aa20706`  
		Last Modified: Wed, 11 Mar 2026 18:16:11 GMT  
		Size: 314.6 KB (314631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ad5e5278bc2c70818690289be2d242b0b4c8c19a0e3760baee03e61a353f1b`  
		Last Modified: Wed, 11 Mar 2026 18:16:13 GMT  
		Size: 85.6 MB (85647918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0cc42bef465492e58bc45a66f45063734b6dfa2c35f122b2e4d727725fb078`  
		Last Modified: Wed, 11 Mar 2026 18:16:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a25094aa2b4871d5b57710ea8c2744cb8f6e6ae0925f30a54d1fdec23b11574`  
		Last Modified: Wed, 11 Mar 2026 18:16:13 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.3-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:2078676dd7e1327521aaf5f507135e1dfc297e9cde91d98d759f268ef4a2b7f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.0 KB (407010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bac43789d9959dd74126116e44626a56414434faf48d68ab2b7a1b12a037e04`

```dockerfile
```

-	Layers:
	-	`sha256:746d6873825a09596eb9871f68ce272afc4890afa70e6db536387eea343f78d7`  
		Last Modified: Wed, 11 Mar 2026 18:16:11 GMT  
		Size: 391.7 KB (391673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a6968954b0b936cfb18afe3e011b520c21cdddf0d857adbc50f887bc02fdf0f`  
		Last Modified: Wed, 11 Mar 2026 18:16:11 GMT  
		Size: 15.3 KB (15337 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:656c2dd86b1a11c9fa73c985a54bb4cb335be38e3b70e7d7a98b7dd6bb316c20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:b1d61f6c9d7eedf07f7f421c39d7f4ae7873feda2f507b638c5f41d926c3cf5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75903698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168fcf9b2f142305619b781d38caee32bb205260c8f6b488640d37f280ee3c4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:27:05 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:27:05 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:27:11 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 Jan 2026 03:27:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 Jan 2026 03:27:12 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 Jan 2026 03:27:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:12 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a585510c235336f1b768ba7a6bf719de8862edd4de8bab4478f7143dd713ec`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09eb36c87d43883a2445c1cc908f02d656272af80af315350c48ed43226abf8`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 292.5 KB (292469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d03f75f30654c33dd087a69f5886f260f34677b2a96b36e3eea9c24463859ff`  
		Last Modified: Wed, 28 Jan 2026 03:27:24 GMT  
		Size: 72.0 MB (71982585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e37e8342e3694b5063b4991c1590a9422921ca7d4b546ef869d103f6fa04b9`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d21e4716448dd70a66c3fd55b61f1785b3d5986c261ed93b8ad038da9148135`  
		Last Modified: Wed, 28 Jan 2026 03:27:23 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:5003cd167566bb65defab27200a7d312c071e712e46749d5cdd35d3e1e3ceb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 KB (382162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4f2c0991bc53bb04c83c53a02fd6a5c9242159e43ab17158ffb778aa343c8e`

```dockerfile
```

-	Layers:
	-	`sha256:88336f50a8e4328e09abfae2f573fc9edf649cfa0c6d3a785238d3b1c703b49f`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 366.5 KB (366522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff17a7f1d689f60bc9158243e3980a866fa6d4ce9b91ec9f4688fecbab497f60`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 15.6 KB (15640 bytes)  
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
