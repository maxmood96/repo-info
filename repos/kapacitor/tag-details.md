<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.6`](#kapacitor16)
-	[`kapacitor:1.6-alpine`](#kapacitor16-alpine)
-	[`kapacitor:1.6.6`](#kapacitor166)
-	[`kapacitor:1.6.6-alpine`](#kapacitor166-alpine)
-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.5`](#kapacitor175)
-	[`kapacitor:1.7.5-alpine`](#kapacitor175-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.6`

```console
$ docker pull kapacitor@sha256:cd9330ed14f7aabb2e641119f7b36ea946505e42d7f0f4b440eb11481693e21f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:988f428afc115864f5dfbd30df003ece46c8cac244490b44fbd0dc9287f2df16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141381124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8d50b1bf89877880862a8137b99fcd9da1179ef0cd98bb2ba2c6563dee69bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdd47a1c6e1ac7d610f49064cd95fa387d90f32ec99d5bbc6e6076ddb7d1162`  
		Last Modified: Sat, 17 Aug 2024 01:32:05 GMT  
		Size: 7.1 MB (7091635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655154faeb477fe8f2120beb7dcae85fd112ca12d885d1a55b7f24448871cf3b`  
		Last Modified: Sat, 17 Aug 2024 02:04:58 GMT  
		Size: 38.2 MB (38175683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b9015eda3a23127393d5069f7e614c5efde8ef57e84fb05e96c6f6a8ca8526`  
		Last Modified: Sat, 17 Aug 2024 02:04:58 GMT  
		Size: 65.7 MB (65672636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb364cd291fb2e21487cdf4eedbfe1485df9ddadf5a92c3824f8c7d1d615ce`  
		Last Modified: Sat, 17 Aug 2024 02:04:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1aea0f651a50d560ac3bda4f267fc8a43c3a57edfb1833b78dba6d5d588db18`  
		Last Modified: Sat, 17 Aug 2024 02:04:57 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:4a7581dec2c7bb0f8c2f73c9090fbe17ab9961bd95672688a2332dea5c952425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3541794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f48f941642a2586a843005eb33b84cee173e387721edb1ca17c0d647cc9ccb`

```dockerfile
```

-	Layers:
	-	`sha256:e6f256493053cf9d3793206d2b3ee9347efe510cc66227eb1f40a37112509c1f`  
		Last Modified: Sat, 17 Aug 2024 02:04:57 GMT  
		Size: 3.5 MB (3527190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5b3b6dc67a1a53022a4c8f9e62cb6058af98290bd9ebea53b593baaad40b3f9`  
		Last Modified: Sat, 17 Aug 2024 02:04:57 GMT  
		Size: 14.6 KB (14604 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:3328ad86d717f3f3b6acfa1f66023fc9c2aea2bd5b859222ffa9d597a19229ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132398988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436f70ea8b3f609ebd01b8e7b642c890a3c97710453bf08d6e167f0cde8d64b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45a8709da787bbcff9e3e7fbb612c1e49a2ced71990421810ee6ef22d5f2bc4`  
		Last Modified: Sat, 17 Aug 2024 01:25:21 GMT  
		Size: 7.0 MB (7033523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ead049629ee586fb3ba64691f4110a6f8d2a3565a89f8e0ae5e6ff415c60052`  
		Last Modified: Sat, 17 Aug 2024 02:51:00 GMT  
		Size: 35.3 MB (35298028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b95691d0bf544f7c3a17762dda7d7e1a699887aab668786e75439b2968d5c7`  
		Last Modified: Sat, 17 Aug 2024 02:51:01 GMT  
		Size: 61.7 MB (61669873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e832bae440279210d789f6b930df5e0c7d75b1ac532db14171833c66517061d7`  
		Last Modified: Sat, 17 Aug 2024 02:51:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00d8558e3e1374a3516b410f08c6d3d3eeb89625c010e53db69dc4fac4f4cc6`  
		Last Modified: Sat, 17 Aug 2024 02:51:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:f7c7727c3a28d3ee2eb87bc8cebd33a6a5e12b3e6c2302782f9902a6783c2c2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3542350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12c210d8cb48fa74de435650692e434e49c56dcfd5744816435437458cacaf8`

```dockerfile
```

-	Layers:
	-	`sha256:e696b99ac23d1a5567d56516d41333d0e8179de1f6a9542625d4c0b753d69c24`  
		Last Modified: Sat, 17 Aug 2024 02:50:59 GMT  
		Size: 3.5 MB (3527456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a38a2098ce731c681127fe49469fd6c4938ca2a286ab6f4a263140d3109a148`  
		Last Modified: Sat, 17 Aug 2024 02:50:59 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6-alpine`

```console
$ docker pull kapacitor@sha256:12b189c83fb4dab397decb627ef94084aba1bb0ff0829938e38d4722bf5fa7fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e0423ff48b6442c9468543ec16e4240851e84bdd6134ce6ab1552cf497c9cbf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69495535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f00bb014cc36f227c90f56e097ed7f9de8b8724b73d68c594f88dd946a0638e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c268f670c0a685634b444d29fc97e3690f73ca6fc0331600124f5c2753103280`  
		Last Modified: Fri, 06 Sep 2024 23:21:55 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0af18220bb82572dc04f254e71bdb704c3372a49ea537e8d34863a5ccab8e2c`  
		Last Modified: Fri, 06 Sep 2024 23:21:55 GMT  
		Size: 290.9 KB (290882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd619dd3107ddd326fa373840fbb338bd094926a04b095383105b764c3bf07c`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 65.6 MB (65580114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa5f74b3ac49e3fce6a494b7c0a68ab26210242a79515b2f25f77b9ca84bc37`  
		Last Modified: Fri, 06 Sep 2024 23:21:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be98bcea12b74baadc4a3825910fd115dc87bf6510a79349f98e51b9d46815fe`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:094c344947948fbc136c238c5e7866ad6274b87dd403b2deff7a1da39b5516c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.7 KB (369673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85611d22f7f851e6609fd70425f84c2e27f7e0dc0daa0f4066916f98a65e7374`

```dockerfile
```

-	Layers:
	-	`sha256:636f1e95eb7402813159744e6a574302270a4fab364a1af4a77d82638cc6d546`  
		Last Modified: Fri, 06 Sep 2024 23:21:55 GMT  
		Size: 355.1 KB (355131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018e702035c9209905acb839464a6b65f50bed07d5b028b5aabee575529c0d1d`  
		Last Modified: Fri, 06 Sep 2024 23:21:55 GMT  
		Size: 14.5 KB (14542 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6.6`

```console
$ docker pull kapacitor@sha256:cd9330ed14f7aabb2e641119f7b36ea946505e42d7f0f4b440eb11481693e21f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.6.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:988f428afc115864f5dfbd30df003ece46c8cac244490b44fbd0dc9287f2df16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141381124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8d50b1bf89877880862a8137b99fcd9da1179ef0cd98bb2ba2c6563dee69bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdd47a1c6e1ac7d610f49064cd95fa387d90f32ec99d5bbc6e6076ddb7d1162`  
		Last Modified: Sat, 17 Aug 2024 01:32:05 GMT  
		Size: 7.1 MB (7091635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655154faeb477fe8f2120beb7dcae85fd112ca12d885d1a55b7f24448871cf3b`  
		Last Modified: Sat, 17 Aug 2024 02:04:58 GMT  
		Size: 38.2 MB (38175683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b9015eda3a23127393d5069f7e614c5efde8ef57e84fb05e96c6f6a8ca8526`  
		Last Modified: Sat, 17 Aug 2024 02:04:58 GMT  
		Size: 65.7 MB (65672636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb364cd291fb2e21487cdf4eedbfe1485df9ddadf5a92c3824f8c7d1d615ce`  
		Last Modified: Sat, 17 Aug 2024 02:04:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1aea0f651a50d560ac3bda4f267fc8a43c3a57edfb1833b78dba6d5d588db18`  
		Last Modified: Sat, 17 Aug 2024 02:04:57 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:4a7581dec2c7bb0f8c2f73c9090fbe17ab9961bd95672688a2332dea5c952425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3541794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f48f941642a2586a843005eb33b84cee173e387721edb1ca17c0d647cc9ccb`

```dockerfile
```

-	Layers:
	-	`sha256:e6f256493053cf9d3793206d2b3ee9347efe510cc66227eb1f40a37112509c1f`  
		Last Modified: Sat, 17 Aug 2024 02:04:57 GMT  
		Size: 3.5 MB (3527190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5b3b6dc67a1a53022a4c8f9e62cb6058af98290bd9ebea53b593baaad40b3f9`  
		Last Modified: Sat, 17 Aug 2024 02:04:57 GMT  
		Size: 14.6 KB (14604 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.6.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:3328ad86d717f3f3b6acfa1f66023fc9c2aea2bd5b859222ffa9d597a19229ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132398988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436f70ea8b3f609ebd01b8e7b642c890a3c97710453bf08d6e167f0cde8d64b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45a8709da787bbcff9e3e7fbb612c1e49a2ced71990421810ee6ef22d5f2bc4`  
		Last Modified: Sat, 17 Aug 2024 01:25:21 GMT  
		Size: 7.0 MB (7033523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ead049629ee586fb3ba64691f4110a6f8d2a3565a89f8e0ae5e6ff415c60052`  
		Last Modified: Sat, 17 Aug 2024 02:51:00 GMT  
		Size: 35.3 MB (35298028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b95691d0bf544f7c3a17762dda7d7e1a699887aab668786e75439b2968d5c7`  
		Last Modified: Sat, 17 Aug 2024 02:51:01 GMT  
		Size: 61.7 MB (61669873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e832bae440279210d789f6b930df5e0c7d75b1ac532db14171833c66517061d7`  
		Last Modified: Sat, 17 Aug 2024 02:51:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00d8558e3e1374a3516b410f08c6d3d3eeb89625c010e53db69dc4fac4f4cc6`  
		Last Modified: Sat, 17 Aug 2024 02:51:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:f7c7727c3a28d3ee2eb87bc8cebd33a6a5e12b3e6c2302782f9902a6783c2c2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3542350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12c210d8cb48fa74de435650692e434e49c56dcfd5744816435437458cacaf8`

```dockerfile
```

-	Layers:
	-	`sha256:e696b99ac23d1a5567d56516d41333d0e8179de1f6a9542625d4c0b753d69c24`  
		Last Modified: Sat, 17 Aug 2024 02:50:59 GMT  
		Size: 3.5 MB (3527456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a38a2098ce731c681127fe49469fd6c4938ca2a286ab6f4a263140d3109a148`  
		Last Modified: Sat, 17 Aug 2024 02:50:59 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6.6-alpine`

```console
$ docker pull kapacitor@sha256:12b189c83fb4dab397decb627ef94084aba1bb0ff0829938e38d4722bf5fa7fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.6.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e0423ff48b6442c9468543ec16e4240851e84bdd6134ce6ab1552cf497c9cbf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69495535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f00bb014cc36f227c90f56e097ed7f9de8b8724b73d68c594f88dd946a0638e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c268f670c0a685634b444d29fc97e3690f73ca6fc0331600124f5c2753103280`  
		Last Modified: Fri, 06 Sep 2024 23:21:55 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0af18220bb82572dc04f254e71bdb704c3372a49ea537e8d34863a5ccab8e2c`  
		Last Modified: Fri, 06 Sep 2024 23:21:55 GMT  
		Size: 290.9 KB (290882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd619dd3107ddd326fa373840fbb338bd094926a04b095383105b764c3bf07c`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 65.6 MB (65580114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa5f74b3ac49e3fce6a494b7c0a68ab26210242a79515b2f25f77b9ca84bc37`  
		Last Modified: Fri, 06 Sep 2024 23:21:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be98bcea12b74baadc4a3825910fd115dc87bf6510a79349f98e51b9d46815fe`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:094c344947948fbc136c238c5e7866ad6274b87dd403b2deff7a1da39b5516c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.7 KB (369673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85611d22f7f851e6609fd70425f84c2e27f7e0dc0daa0f4066916f98a65e7374`

```dockerfile
```

-	Layers:
	-	`sha256:636f1e95eb7402813159744e6a574302270a4fab364a1af4a77d82638cc6d546`  
		Last Modified: Fri, 06 Sep 2024 23:21:55 GMT  
		Size: 355.1 KB (355131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018e702035c9209905acb839464a6b65f50bed07d5b028b5aabee575529c0d1d`  
		Last Modified: Fri, 06 Sep 2024 23:21:55 GMT  
		Size: 14.5 KB (14542 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7`

```console
$ docker pull kapacitor@sha256:9500c79038d3b2a5c5dfb130476d4f245740a85d6e009988f4341a0e1a8a135e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:90b01399bada05355f111ffd6430eebed614a6c298bfd00972f746b7978fd62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147097902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8796162b711324d67dcd574fee63392bfb336ee50024bede76069466eead421`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdd47a1c6e1ac7d610f49064cd95fa387d90f32ec99d5bbc6e6076ddb7d1162`  
		Last Modified: Sat, 17 Aug 2024 01:32:05 GMT  
		Size: 7.1 MB (7091635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbc16744ccdcf41a9f2a5134d023396285b28f13e8f6e80688eedf561f12ba2`  
		Last Modified: Sat, 17 Aug 2024 02:01:05 GMT  
		Size: 38.2 MB (38175629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d29bb25556874c5ca9210098390eb99afb4ef98e0a4eaa59e06cffe6c67dbfa`  
		Last Modified: Sat, 17 Aug 2024 02:01:05 GMT  
		Size: 71.4 MB (71389403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58352e708e24d1b7301ae09225356e087a7193f85126aa19c53007bd178ac71e`  
		Last Modified: Sat, 17 Aug 2024 02:01:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57497b3d468c06c85cb3a82c0352d701dc8dbed3c988b832b5195a8ef06ec37`  
		Last Modified: Sat, 17 Aug 2024 02:01:05 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7171ddd72b3667b7423a9cc869bf286aec10910a5bab0560ee7d607989329875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3550063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cdad31dd7b2436475c390fe55eb029c982b8defe866bd4d972125ef006565f`

```dockerfile
```

-	Layers:
	-	`sha256:e3aaee25b4936b2968f81694b29b608a9a5684e738341b138b53934faec6ab30`  
		Last Modified: Sat, 17 Aug 2024 02:01:04 GMT  
		Size: 3.5 MB (3535156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed9dfd155aacc2b7949551c61fe44108e0e45b66b0d225ea2998fae5ee3e7bf0`  
		Last Modified: Sat, 17 Aug 2024 02:01:04 GMT  
		Size: 14.9 KB (14907 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:11241936e84473ecb762f9ad80e1c1a8fdafeab0ee0c4850ec59b34fc57dbda3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137844294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4194c696552f5753ea15c7364f4af46c0f9c010bfc840f5a59da1c5c34052995`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45a8709da787bbcff9e3e7fbb612c1e49a2ced71990421810ee6ef22d5f2bc4`  
		Last Modified: Sat, 17 Aug 2024 01:25:21 GMT  
		Size: 7.0 MB (7033523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ead049629ee586fb3ba64691f4110a6f8d2a3565a89f8e0ae5e6ff415c60052`  
		Last Modified: Sat, 17 Aug 2024 02:51:00 GMT  
		Size: 35.3 MB (35298028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbb9a2f3be44dba249993ad058ba3129fd175033cdf615161a00f74d1e73d89`  
		Last Modified: Sat, 17 Aug 2024 02:51:34 GMT  
		Size: 67.1 MB (67115113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd744062b4c50d169a2f39815fd7bef3843561d8da5550c3ae0c335f47df253`  
		Last Modified: Sat, 17 Aug 2024 02:51:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b2d5cd75a5e1cd13fa3cb42ba47aa16e7a46f43987bede5a6b5cec5222ac09`  
		Last Modified: Sat, 17 Aug 2024 02:51:32 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:b8af6079122d2fe3e217d1af100dd9fdc93a652bcc48b8fd717014e035c43d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26175166746529508cd039398c34f0e2fd9b6ed835b5535ba2f512f4f6f6605c`

```dockerfile
```

-	Layers:
	-	`sha256:bee97c32b6a17eb5e04982fc7c7c728e21538e647ce153fd0575b7ae4c45102b`  
		Last Modified: Sat, 17 Aug 2024 02:51:33 GMT  
		Size: 3.5 MB (3534639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b8b662ded9ff144db01227c1a00f9a8aefd5a0909ae37a223423349e7ce91d9`  
		Last Modified: Sat, 17 Aug 2024 02:51:32 GMT  
		Size: 15.2 KB (15210 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:f7e1b5a11518134085443d57633ca0003d6209160799cc76b632673e2715ced9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:a7eb292d00e949e753cf601f1aa459c6e3b90fa71a5333e613c3e32220e97ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75236586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e79a2267ecefc2a687bcb1b688a856d4f07e86a4c6bb99eb2738093c222354`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230d75275092d3e053c8f298afa3cf2cd9bd213f547c234cf89c85e1ddc7206e`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0460a680b1925da179fafe048f8fe0d62be248fb243a328cee52a157fee0752a`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 292.6 KB (292599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb917e1ee259d651521e9ea0d8f4bc3f8fad8e54367adbd0459abe6f150e70dc`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 71.3 MB (71319398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1316a611ed7cbd7df20a7d953ded552204d4a5bebfb8380da29c2e9b5c076cdb`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ee63ec1d6ab9869e89b97caf3c2ea9dab9a77bad93b44530ace58cfb09c04d`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:26fb73f1b0e9f1853dc0633946f0679e282f0d0d39bcb21c9089aa895116fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 KB (380161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e31f8772d2655d00ed42681be3b7356b9c8367558aa71f0ad50339c4cc1c6c`

```dockerfile
```

-	Layers:
	-	`sha256:a0ea976bb0730523b5df0d6b08a1a70872e5b881add3c3d2abce8ac6e9f67548`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 364.7 KB (364698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31112cd797ae22f53dc744d61673a35a886a7f27f6a5dbd454f29e8f19aa5454`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 15.5 KB (15463 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.5`

```console
$ docker pull kapacitor@sha256:9500c79038d3b2a5c5dfb130476d4f245740a85d6e009988f4341a0e1a8a135e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:90b01399bada05355f111ffd6430eebed614a6c298bfd00972f746b7978fd62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147097902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8796162b711324d67dcd574fee63392bfb336ee50024bede76069466eead421`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdd47a1c6e1ac7d610f49064cd95fa387d90f32ec99d5bbc6e6076ddb7d1162`  
		Last Modified: Sat, 17 Aug 2024 01:32:05 GMT  
		Size: 7.1 MB (7091635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbc16744ccdcf41a9f2a5134d023396285b28f13e8f6e80688eedf561f12ba2`  
		Last Modified: Sat, 17 Aug 2024 02:01:05 GMT  
		Size: 38.2 MB (38175629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d29bb25556874c5ca9210098390eb99afb4ef98e0a4eaa59e06cffe6c67dbfa`  
		Last Modified: Sat, 17 Aug 2024 02:01:05 GMT  
		Size: 71.4 MB (71389403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58352e708e24d1b7301ae09225356e087a7193f85126aa19c53007bd178ac71e`  
		Last Modified: Sat, 17 Aug 2024 02:01:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57497b3d468c06c85cb3a82c0352d701dc8dbed3c988b832b5195a8ef06ec37`  
		Last Modified: Sat, 17 Aug 2024 02:01:05 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.5` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7171ddd72b3667b7423a9cc869bf286aec10910a5bab0560ee7d607989329875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3550063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cdad31dd7b2436475c390fe55eb029c982b8defe866bd4d972125ef006565f`

```dockerfile
```

-	Layers:
	-	`sha256:e3aaee25b4936b2968f81694b29b608a9a5684e738341b138b53934faec6ab30`  
		Last Modified: Sat, 17 Aug 2024 02:01:04 GMT  
		Size: 3.5 MB (3535156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed9dfd155aacc2b7949551c61fe44108e0e45b66b0d225ea2998fae5ee3e7bf0`  
		Last Modified: Sat, 17 Aug 2024 02:01:04 GMT  
		Size: 14.9 KB (14907 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:11241936e84473ecb762f9ad80e1c1a8fdafeab0ee0c4850ec59b34fc57dbda3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137844294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4194c696552f5753ea15c7364f4af46c0f9c010bfc840f5a59da1c5c34052995`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45a8709da787bbcff9e3e7fbb612c1e49a2ced71990421810ee6ef22d5f2bc4`  
		Last Modified: Sat, 17 Aug 2024 01:25:21 GMT  
		Size: 7.0 MB (7033523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ead049629ee586fb3ba64691f4110a6f8d2a3565a89f8e0ae5e6ff415c60052`  
		Last Modified: Sat, 17 Aug 2024 02:51:00 GMT  
		Size: 35.3 MB (35298028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbb9a2f3be44dba249993ad058ba3129fd175033cdf615161a00f74d1e73d89`  
		Last Modified: Sat, 17 Aug 2024 02:51:34 GMT  
		Size: 67.1 MB (67115113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd744062b4c50d169a2f39815fd7bef3843561d8da5550c3ae0c335f47df253`  
		Last Modified: Sat, 17 Aug 2024 02:51:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b2d5cd75a5e1cd13fa3cb42ba47aa16e7a46f43987bede5a6b5cec5222ac09`  
		Last Modified: Sat, 17 Aug 2024 02:51:32 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.5` - unknown; unknown

```console
$ docker pull kapacitor@sha256:b8af6079122d2fe3e217d1af100dd9fdc93a652bcc48b8fd717014e035c43d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26175166746529508cd039398c34f0e2fd9b6ed835b5535ba2f512f4f6f6605c`

```dockerfile
```

-	Layers:
	-	`sha256:bee97c32b6a17eb5e04982fc7c7c728e21538e647ce153fd0575b7ae4c45102b`  
		Last Modified: Sat, 17 Aug 2024 02:51:33 GMT  
		Size: 3.5 MB (3534639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b8b662ded9ff144db01227c1a00f9a8aefd5a0909ae37a223423349e7ce91d9`  
		Last Modified: Sat, 17 Aug 2024 02:51:32 GMT  
		Size: 15.2 KB (15210 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.5-alpine`

```console
$ docker pull kapacitor@sha256:f7e1b5a11518134085443d57633ca0003d6209160799cc76b632673e2715ced9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:a7eb292d00e949e753cf601f1aa459c6e3b90fa71a5333e613c3e32220e97ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75236586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e79a2267ecefc2a687bcb1b688a856d4f07e86a4c6bb99eb2738093c222354`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230d75275092d3e053c8f298afa3cf2cd9bd213f547c234cf89c85e1ddc7206e`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0460a680b1925da179fafe048f8fe0d62be248fb243a328cee52a157fee0752a`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 292.6 KB (292599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb917e1ee259d651521e9ea0d8f4bc3f8fad8e54367adbd0459abe6f150e70dc`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 71.3 MB (71319398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1316a611ed7cbd7df20a7d953ded552204d4a5bebfb8380da29c2e9b5c076cdb`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ee63ec1d6ab9869e89b97caf3c2ea9dab9a77bad93b44530ace58cfb09c04d`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.5-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:26fb73f1b0e9f1853dc0633946f0679e282f0d0d39bcb21c9089aa895116fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 KB (380161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e31f8772d2655d00ed42681be3b7356b9c8367558aa71f0ad50339c4cc1c6c`

```dockerfile
```

-	Layers:
	-	`sha256:a0ea976bb0730523b5df0d6b08a1a70872e5b881add3c3d2abce8ac6e9f67548`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 364.7 KB (364698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31112cd797ae22f53dc744d61673a35a886a7f27f6a5dbd454f29e8f19aa5454`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 15.5 KB (15463 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:f7e1b5a11518134085443d57633ca0003d6209160799cc76b632673e2715ced9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:a7eb292d00e949e753cf601f1aa459c6e3b90fa71a5333e613c3e32220e97ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75236586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e79a2267ecefc2a687bcb1b688a856d4f07e86a4c6bb99eb2738093c222354`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230d75275092d3e053c8f298afa3cf2cd9bd213f547c234cf89c85e1ddc7206e`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0460a680b1925da179fafe048f8fe0d62be248fb243a328cee52a157fee0752a`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 292.6 KB (292599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb917e1ee259d651521e9ea0d8f4bc3f8fad8e54367adbd0459abe6f150e70dc`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 71.3 MB (71319398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1316a611ed7cbd7df20a7d953ded552204d4a5bebfb8380da29c2e9b5c076cdb`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ee63ec1d6ab9869e89b97caf3c2ea9dab9a77bad93b44530ace58cfb09c04d`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:26fb73f1b0e9f1853dc0633946f0679e282f0d0d39bcb21c9089aa895116fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 KB (380161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e31f8772d2655d00ed42681be3b7356b9c8367558aa71f0ad50339c4cc1c6c`

```dockerfile
```

-	Layers:
	-	`sha256:a0ea976bb0730523b5df0d6b08a1a70872e5b881add3c3d2abce8ac6e9f67548`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 364.7 KB (364698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31112cd797ae22f53dc744d61673a35a886a7f27f6a5dbd454f29e8f19aa5454`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 15.5 KB (15463 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:9500c79038d3b2a5c5dfb130476d4f245740a85d6e009988f4341a0e1a8a135e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:90b01399bada05355f111ffd6430eebed614a6c298bfd00972f746b7978fd62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147097902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8796162b711324d67dcd574fee63392bfb336ee50024bede76069466eead421`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdd47a1c6e1ac7d610f49064cd95fa387d90f32ec99d5bbc6e6076ddb7d1162`  
		Last Modified: Sat, 17 Aug 2024 01:32:05 GMT  
		Size: 7.1 MB (7091635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbc16744ccdcf41a9f2a5134d023396285b28f13e8f6e80688eedf561f12ba2`  
		Last Modified: Sat, 17 Aug 2024 02:01:05 GMT  
		Size: 38.2 MB (38175629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d29bb25556874c5ca9210098390eb99afb4ef98e0a4eaa59e06cffe6c67dbfa`  
		Last Modified: Sat, 17 Aug 2024 02:01:05 GMT  
		Size: 71.4 MB (71389403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58352e708e24d1b7301ae09225356e087a7193f85126aa19c53007bd178ac71e`  
		Last Modified: Sat, 17 Aug 2024 02:01:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57497b3d468c06c85cb3a82c0352d701dc8dbed3c988b832b5195a8ef06ec37`  
		Last Modified: Sat, 17 Aug 2024 02:01:05 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7171ddd72b3667b7423a9cc869bf286aec10910a5bab0560ee7d607989329875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3550063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cdad31dd7b2436475c390fe55eb029c982b8defe866bd4d972125ef006565f`

```dockerfile
```

-	Layers:
	-	`sha256:e3aaee25b4936b2968f81694b29b608a9a5684e738341b138b53934faec6ab30`  
		Last Modified: Sat, 17 Aug 2024 02:01:04 GMT  
		Size: 3.5 MB (3535156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed9dfd155aacc2b7949551c61fe44108e0e45b66b0d225ea2998fae5ee3e7bf0`  
		Last Modified: Sat, 17 Aug 2024 02:01:04 GMT  
		Size: 14.9 KB (14907 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:11241936e84473ecb762f9ad80e1c1a8fdafeab0ee0c4850ec59b34fc57dbda3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137844294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4194c696552f5753ea15c7364f4af46c0f9c010bfc840f5a59da1c5c34052995`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45a8709da787bbcff9e3e7fbb612c1e49a2ced71990421810ee6ef22d5f2bc4`  
		Last Modified: Sat, 17 Aug 2024 01:25:21 GMT  
		Size: 7.0 MB (7033523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ead049629ee586fb3ba64691f4110a6f8d2a3565a89f8e0ae5e6ff415c60052`  
		Last Modified: Sat, 17 Aug 2024 02:51:00 GMT  
		Size: 35.3 MB (35298028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbb9a2f3be44dba249993ad058ba3129fd175033cdf615161a00f74d1e73d89`  
		Last Modified: Sat, 17 Aug 2024 02:51:34 GMT  
		Size: 67.1 MB (67115113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd744062b4c50d169a2f39815fd7bef3843561d8da5550c3ae0c335f47df253`  
		Last Modified: Sat, 17 Aug 2024 02:51:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b2d5cd75a5e1cd13fa3cb42ba47aa16e7a46f43987bede5a6b5cec5222ac09`  
		Last Modified: Sat, 17 Aug 2024 02:51:32 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:b8af6079122d2fe3e217d1af100dd9fdc93a652bcc48b8fd717014e035c43d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26175166746529508cd039398c34f0e2fd9b6ed835b5535ba2f512f4f6f6605c`

```dockerfile
```

-	Layers:
	-	`sha256:bee97c32b6a17eb5e04982fc7c7c728e21538e647ce153fd0575b7ae4c45102b`  
		Last Modified: Sat, 17 Aug 2024 02:51:33 GMT  
		Size: 3.5 MB (3534639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b8b662ded9ff144db01227c1a00f9a8aefd5a0909ae37a223423349e7ce91d9`  
		Last Modified: Sat, 17 Aug 2024 02:51:32 GMT  
		Size: 15.2 KB (15210 bytes)  
		MIME: application/vnd.in-toto+json
