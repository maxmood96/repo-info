<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.34`](#telegraf134)
-	[`telegraf:1.34-alpine`](#telegraf134-alpine)
-	[`telegraf:1.34.4`](#telegraf1344)
-	[`telegraf:1.34.4-alpine`](#telegraf1344-alpine)
-	[`telegraf:1.35`](#telegraf135)
-	[`telegraf:1.35-alpine`](#telegraf135-alpine)
-	[`telegraf:1.35.4`](#telegraf1354)
-	[`telegraf:1.35.4-alpine`](#telegraf1354-alpine)
-	[`telegraf:1.36`](#telegraf136)
-	[`telegraf:1.36-alpine`](#telegraf136-alpine)
-	[`telegraf:1.36.3`](#telegraf1363)
-	[`telegraf:1.36.3-alpine`](#telegraf1363-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.34`

```console
$ docker pull telegraf@sha256:6b49dbafc167e1151c70030716860be2ef08f8b9fd8ba018b9431fb54b153a97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34` - linux; amd64

```console
$ docker pull telegraf@sha256:8d06a112c6cffbbb36278dd305c747fe77424583014c3d1baaa9d0c3a9a05dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168903593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c26b59032d1484e3d7fe183ecf22b46b6a9706325224968044302af42f8516`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:29:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:29:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 04:29:25 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 04 Nov 2025 04:29:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 04:29:25 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 04:29:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 04:29:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 04:29:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb445e472b1bad54f5a28edd51b11aec79eca8513394866a261891be9da6a343`  
		Last Modified: Tue, 04 Nov 2025 00:28:00 GMT  
		Size: 24.0 MB (24029301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e83e4e227cdd3650f26cce50414310c8b45e548374490eace00d781f2c8b72`  
		Last Modified: Tue, 04 Nov 2025 04:29:51 GMT  
		Size: 18.9 MB (18942933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b9ecbe24af67c39cc8a3069b335569a376c3f81826da6f65e3ab3a5bd800c7`  
		Last Modified: Tue, 04 Nov 2025 04:29:50 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd16358eac7454afd0ed0ddb7ed8658edcd4daef4cd095039e02126c8d4eabc`  
		Last Modified: Tue, 04 Nov 2025 04:29:58 GMT  
		Size: 77.4 MB (77446226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fed8ee33f793eaea4eba74922d0f0a54e510ad8199c4b2ef97a3793394515d7`  
		Last Modified: Tue, 04 Nov 2025 04:29:52 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:3d2732f09f5f192aac88593a3e595cd1158bc510e707d0533cd58f87c941b82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80e79fde95e9bb58139740b51b70d617c0931c1c35c7772673539323114b1ea`

```dockerfile
```

-	Layers:
	-	`sha256:246c96a8a87e491d96403f26fb8e382965ddd84b03c94b671e1cb0442c2ef3f6`  
		Last Modified: Tue, 04 Nov 2025 10:10:29 GMT  
		Size: 6.6 MB (6630220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d96a22d589951da1a871f33303abbbb0fe20a1f9ae9021e8f5afaa945fec30`  
		Last Modified: Tue, 04 Nov 2025 10:10:29 GMT  
		Size: 14.4 KB (14426 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:adcf34a900a8d3567ad02e68c3e40467cf35040192c1b0b9e31024fede1e2001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155384929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a28d46083e1d15ae71a366532bb56793912c3e5baaa7bed566f73c9f4d57ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:39:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:39:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 02:39:10 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 04 Nov 2025 02:39:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 02:39:10 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 02:39:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 02:39:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 02:39:11 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:461f215c759f019a0fb4d33c976a91c4c2e4b033762b07a2f81bac66dee9e613`  
		Last Modified: Tue, 04 Nov 2025 00:12:30 GMT  
		Size: 44.2 MB (44196437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad602f359c1ad647108cc57270e592fc1f62f8ffd947a100fecee62a4a0d017`  
		Last Modified: Tue, 04 Nov 2025 00:39:15 GMT  
		Size: 21.9 MB (21934879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5207eacc0a636b8c0b0753ace942e14c051938d7aac0efb93c5a8a055bd312`  
		Last Modified: Tue, 04 Nov 2025 02:39:34 GMT  
		Size: 17.7 MB (17722410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00102ab6e81a9d64a6dbc8926419879ef6abccddbf68907fdbfc2a34a1f5dc0`  
		Last Modified: Tue, 04 Nov 2025 02:39:33 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236ffcacb1796a21ab499c5a127fda3fdb3dc9339e275f34cabef3ddd6ad5e77`  
		Last Modified: Tue, 04 Nov 2025 02:39:39 GMT  
		Size: 71.5 MB (71527138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ce6ada745c29621a74ebcfd4156a27ca384e44a271870183c4857cb37424cc`  
		Last Modified: Tue, 04 Nov 2025 02:39:33 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:1dbd478fd29e5fe8679ca6568e8b51438741804a3d3b20a46d0137a13a8823d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6639332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8293d34916d69ccf2f1d63aa7967f656de0e5d926bdd9fcf553bf87ffa0fc6`

```dockerfile
```

-	Layers:
	-	`sha256:8991ce1cc7d04ac88029e7de575436deb62fa24d50079dedc001a43f0c7b7be0`  
		Last Modified: Tue, 04 Nov 2025 10:10:35 GMT  
		Size: 6.6 MB (6624815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa6e07867ec83d799c467ae8223719c075b8a32ed35ac57b0d20620ce95f37df`  
		Last Modified: Tue, 04 Nov 2025 10:10:36 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3f13a41b18a1fffcc0c3e7304e5aeaa3707914cb0ffc1c879fec630b7ebbe43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161047668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8111fc259468679fa343e1a1a3114b994f3ff7fe1d0a8b15357003692830bf6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:42:48 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:42:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 01:42:52 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 04 Nov 2025 01:42:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 01:42:52 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 01:42:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 01:42:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 01:42:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463896571d3ff5317461a64229e9e4cb27d6d877114079419cf8b4fc96b0c02`  
		Last Modified: Tue, 04 Nov 2025 00:30:33 GMT  
		Size: 23.6 MB (23598514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024b597534d3993aa4c83ef331684e6c11a8401545ac4519de73921418155aba`  
		Last Modified: Tue, 04 Nov 2025 01:43:28 GMT  
		Size: 18.9 MB (18884427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5034d238a4c6d86be446643dc569cdd313d64582c7df8530a8c830352e3fe9`  
		Last Modified: Tue, 04 Nov 2025 01:43:26 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6be212265235120248eb27642c7d5f3db59b657fceecc31b08661a74f7f942`  
		Last Modified: Tue, 04 Nov 2025 01:43:37 GMT  
		Size: 70.2 MB (70201188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ad9c451f8972fad05099e2c725d90193ffb1abdc6512d836f40a244007c318`  
		Last Modified: Tue, 04 Nov 2025 01:43:26 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:fc8ddb37ad80b56942a4a88b21ee06d63c036aa9d2ff50e5e14a966e7de3a295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6645433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77be9a38a1af8ea9b8b510a2a7d4880b863a0362dd8b1d0321d91c857ff7da9d`

```dockerfile
```

-	Layers:
	-	`sha256:3b2b3f9c18fcd86e771fb53623dfddd24fe6d1476047fb49048b930bb98aefff`  
		Last Modified: Tue, 04 Nov 2025 10:36:15 GMT  
		Size: 6.6 MB (6630896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6e0183f3a0e6ffe746ddf3fd3b10fe976941ca48cb9fc6b715864e14f806552`  
		Last Modified: Tue, 04 Nov 2025 10:36:16 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34-alpine`

```console
$ docker pull telegraf@sha256:a3b7b41d457aaba6bbf693ac582488cb0eef9189e0123228d6d73b5ddbecf3d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:af13b793aa1dce69208718cd1a5e52ee46c4fbbc66dd3482802244da07004de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83310068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c734f900c2cc54d55ee1c3608e192247e73d9d77db94c72301e8af7b0cf4cc3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d70c842384492021fdcd617e3e57dbc08546ebeb0a55cf5f01aa575170280c6`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac3b64855296be028704ca1d2bdbcaae40b9d4c034875c7d2e1d19a637cb9ba`  
		Last Modified: Wed, 08 Oct 2025 23:21:24 GMT  
		Size: 2.4 MB (2446002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c0ccc8f4b7cdee3ffc55785877dd2d581e631f44db1c9273a55f4b1a3ca54`  
		Last Modified: Wed, 08 Oct 2025 23:21:34 GMT  
		Size: 77.2 MB (77236402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a75aa1ed1e0e691f32d3b2541b96ee1c6992482ea6123523007989090e2eee`  
		Last Modified: Wed, 08 Oct 2025 23:21:24 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:0f71f1cf17498be8fd0065e60ded60735877224cb9e944bcdc6cdb93d2989504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1117749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4ae4f8be5c6ec51fb0b53e97e765bf86a5b5bb24f54af62f06331612ddc487`

```dockerfile
```

-	Layers:
	-	`sha256:6c5d8506040a5778f7f878513986c23cc8a163a4350c0a06768c33507d6878f1`  
		Last Modified: Thu, 09 Oct 2025 00:10:21 GMT  
		Size: 1.1 MB (1102789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba82ca0ac2c265c7cc6c07a2b174b33a447c7789031192fe81b028bd4cb3ee5a`  
		Last Modified: Thu, 09 Oct 2025 00:10:22 GMT  
		Size: 15.0 KB (14960 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6aa7aa23f4efce9034251674a6146bec7ba0afed83de490ae1fcc009bbfd927d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76618603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94050c98410bd57b667d3082abc1644fef314f392475a2a56e455c7c71bfee19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5141f6585ef76c126161606642d71be3a680014fb406af77ccd75e5b599e1bf4`  
		Last Modified: Wed, 08 Oct 2025 22:10:04 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5912684419f3dc0457cd6ad63dccc9aa5136f2a64160a2644f8870b703024c81`  
		Last Modified: Wed, 08 Oct 2025 22:10:05 GMT  
		Size: 2.5 MB (2531896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a09e09af7872ce5a0604c4669bb70f24e21906b015babebfb76e540fda9fd87`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 70.0 MB (69996727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd0f429f0ae9c0dfcbe4e4a0a000c40c0f51c66b3f27ca3a24e49d773e2af3c`  
		Last Modified: Wed, 08 Oct 2025 22:10:05 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:f569a6c02470d9b48f6a9719b16f8a2ef536cbe1211ecc12f936487aba61c777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1113486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4b3e083f9b4fa0c40a8082ad1ce012ab2c1b9e22fa7beb132420241f4ba444`

```dockerfile
```

-	Layers:
	-	`sha256:3fdf8a231bfa0803332f5275e62890777cf63dc47fcb8d137a896246cbd0affe`  
		Last Modified: Thu, 09 Oct 2025 00:10:25 GMT  
		Size: 1.1 MB (1098416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f5a824629380351fa0100a1f00c0e438e44a10630ca74c4090aed4df9cec1b8`  
		Last Modified: Thu, 09 Oct 2025 00:10:26 GMT  
		Size: 15.1 KB (15070 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34.4`

```console
$ docker pull telegraf@sha256:6b49dbafc167e1151c70030716860be2ef08f8b9fd8ba018b9431fb54b153a97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34.4` - linux; amd64

```console
$ docker pull telegraf@sha256:8d06a112c6cffbbb36278dd305c747fe77424583014c3d1baaa9d0c3a9a05dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168903593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c26b59032d1484e3d7fe183ecf22b46b6a9706325224968044302af42f8516`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:29:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:29:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 04:29:25 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 04 Nov 2025 04:29:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 04:29:25 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 04:29:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 04:29:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 04:29:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb445e472b1bad54f5a28edd51b11aec79eca8513394866a261891be9da6a343`  
		Last Modified: Tue, 04 Nov 2025 00:28:00 GMT  
		Size: 24.0 MB (24029301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e83e4e227cdd3650f26cce50414310c8b45e548374490eace00d781f2c8b72`  
		Last Modified: Tue, 04 Nov 2025 04:29:51 GMT  
		Size: 18.9 MB (18942933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b9ecbe24af67c39cc8a3069b335569a376c3f81826da6f65e3ab3a5bd800c7`  
		Last Modified: Tue, 04 Nov 2025 04:29:50 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd16358eac7454afd0ed0ddb7ed8658edcd4daef4cd095039e02126c8d4eabc`  
		Last Modified: Tue, 04 Nov 2025 04:29:58 GMT  
		Size: 77.4 MB (77446226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fed8ee33f793eaea4eba74922d0f0a54e510ad8199c4b2ef97a3793394515d7`  
		Last Modified: Tue, 04 Nov 2025 04:29:52 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:3d2732f09f5f192aac88593a3e595cd1158bc510e707d0533cd58f87c941b82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80e79fde95e9bb58139740b51b70d617c0931c1c35c7772673539323114b1ea`

```dockerfile
```

-	Layers:
	-	`sha256:246c96a8a87e491d96403f26fb8e382965ddd84b03c94b671e1cb0442c2ef3f6`  
		Last Modified: Tue, 04 Nov 2025 10:10:29 GMT  
		Size: 6.6 MB (6630220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d96a22d589951da1a871f33303abbbb0fe20a1f9ae9021e8f5afaa945fec30`  
		Last Modified: Tue, 04 Nov 2025 10:10:29 GMT  
		Size: 14.4 KB (14426 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:adcf34a900a8d3567ad02e68c3e40467cf35040192c1b0b9e31024fede1e2001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155384929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a28d46083e1d15ae71a366532bb56793912c3e5baaa7bed566f73c9f4d57ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:39:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:39:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 02:39:10 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 04 Nov 2025 02:39:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 02:39:10 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 02:39:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 02:39:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 02:39:11 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:461f215c759f019a0fb4d33c976a91c4c2e4b033762b07a2f81bac66dee9e613`  
		Last Modified: Tue, 04 Nov 2025 00:12:30 GMT  
		Size: 44.2 MB (44196437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad602f359c1ad647108cc57270e592fc1f62f8ffd947a100fecee62a4a0d017`  
		Last Modified: Tue, 04 Nov 2025 00:39:15 GMT  
		Size: 21.9 MB (21934879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5207eacc0a636b8c0b0753ace942e14c051938d7aac0efb93c5a8a055bd312`  
		Last Modified: Tue, 04 Nov 2025 02:39:34 GMT  
		Size: 17.7 MB (17722410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00102ab6e81a9d64a6dbc8926419879ef6abccddbf68907fdbfc2a34a1f5dc0`  
		Last Modified: Tue, 04 Nov 2025 02:39:33 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236ffcacb1796a21ab499c5a127fda3fdb3dc9339e275f34cabef3ddd6ad5e77`  
		Last Modified: Tue, 04 Nov 2025 02:39:39 GMT  
		Size: 71.5 MB (71527138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ce6ada745c29621a74ebcfd4156a27ca384e44a271870183c4857cb37424cc`  
		Last Modified: Tue, 04 Nov 2025 02:39:33 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:1dbd478fd29e5fe8679ca6568e8b51438741804a3d3b20a46d0137a13a8823d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6639332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8293d34916d69ccf2f1d63aa7967f656de0e5d926bdd9fcf553bf87ffa0fc6`

```dockerfile
```

-	Layers:
	-	`sha256:8991ce1cc7d04ac88029e7de575436deb62fa24d50079dedc001a43f0c7b7be0`  
		Last Modified: Tue, 04 Nov 2025 10:10:35 GMT  
		Size: 6.6 MB (6624815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa6e07867ec83d799c467ae8223719c075b8a32ed35ac57b0d20620ce95f37df`  
		Last Modified: Tue, 04 Nov 2025 10:10:36 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3f13a41b18a1fffcc0c3e7304e5aeaa3707914cb0ffc1c879fec630b7ebbe43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161047668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8111fc259468679fa343e1a1a3114b994f3ff7fe1d0a8b15357003692830bf6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:42:48 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:42:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 01:42:52 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 04 Nov 2025 01:42:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 01:42:52 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 01:42:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 01:42:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 01:42:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463896571d3ff5317461a64229e9e4cb27d6d877114079419cf8b4fc96b0c02`  
		Last Modified: Tue, 04 Nov 2025 00:30:33 GMT  
		Size: 23.6 MB (23598514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024b597534d3993aa4c83ef331684e6c11a8401545ac4519de73921418155aba`  
		Last Modified: Tue, 04 Nov 2025 01:43:28 GMT  
		Size: 18.9 MB (18884427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5034d238a4c6d86be446643dc569cdd313d64582c7df8530a8c830352e3fe9`  
		Last Modified: Tue, 04 Nov 2025 01:43:26 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6be212265235120248eb27642c7d5f3db59b657fceecc31b08661a74f7f942`  
		Last Modified: Tue, 04 Nov 2025 01:43:37 GMT  
		Size: 70.2 MB (70201188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ad9c451f8972fad05099e2c725d90193ffb1abdc6512d836f40a244007c318`  
		Last Modified: Tue, 04 Nov 2025 01:43:26 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:fc8ddb37ad80b56942a4a88b21ee06d63c036aa9d2ff50e5e14a966e7de3a295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6645433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77be9a38a1af8ea9b8b510a2a7d4880b863a0362dd8b1d0321d91c857ff7da9d`

```dockerfile
```

-	Layers:
	-	`sha256:3b2b3f9c18fcd86e771fb53623dfddd24fe6d1476047fb49048b930bb98aefff`  
		Last Modified: Tue, 04 Nov 2025 10:36:15 GMT  
		Size: 6.6 MB (6630896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6e0183f3a0e6ffe746ddf3fd3b10fe976941ca48cb9fc6b715864e14f806552`  
		Last Modified: Tue, 04 Nov 2025 10:36:16 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34.4-alpine`

```console
$ docker pull telegraf@sha256:a3b7b41d457aaba6bbf693ac582488cb0eef9189e0123228d6d73b5ddbecf3d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:af13b793aa1dce69208718cd1a5e52ee46c4fbbc66dd3482802244da07004de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83310068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c734f900c2cc54d55ee1c3608e192247e73d9d77db94c72301e8af7b0cf4cc3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d70c842384492021fdcd617e3e57dbc08546ebeb0a55cf5f01aa575170280c6`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac3b64855296be028704ca1d2bdbcaae40b9d4c034875c7d2e1d19a637cb9ba`  
		Last Modified: Wed, 08 Oct 2025 23:21:24 GMT  
		Size: 2.4 MB (2446002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c0ccc8f4b7cdee3ffc55785877dd2d581e631f44db1c9273a55f4b1a3ca54`  
		Last Modified: Wed, 08 Oct 2025 23:21:34 GMT  
		Size: 77.2 MB (77236402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a75aa1ed1e0e691f32d3b2541b96ee1c6992482ea6123523007989090e2eee`  
		Last Modified: Wed, 08 Oct 2025 23:21:24 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:0f71f1cf17498be8fd0065e60ded60735877224cb9e944bcdc6cdb93d2989504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1117749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4ae4f8be5c6ec51fb0b53e97e765bf86a5b5bb24f54af62f06331612ddc487`

```dockerfile
```

-	Layers:
	-	`sha256:6c5d8506040a5778f7f878513986c23cc8a163a4350c0a06768c33507d6878f1`  
		Last Modified: Thu, 09 Oct 2025 00:10:21 GMT  
		Size: 1.1 MB (1102789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba82ca0ac2c265c7cc6c07a2b174b33a447c7789031192fe81b028bd4cb3ee5a`  
		Last Modified: Thu, 09 Oct 2025 00:10:22 GMT  
		Size: 15.0 KB (14960 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6aa7aa23f4efce9034251674a6146bec7ba0afed83de490ae1fcc009bbfd927d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76618603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94050c98410bd57b667d3082abc1644fef314f392475a2a56e455c7c71bfee19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5141f6585ef76c126161606642d71be3a680014fb406af77ccd75e5b599e1bf4`  
		Last Modified: Wed, 08 Oct 2025 22:10:04 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5912684419f3dc0457cd6ad63dccc9aa5136f2a64160a2644f8870b703024c81`  
		Last Modified: Wed, 08 Oct 2025 22:10:05 GMT  
		Size: 2.5 MB (2531896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a09e09af7872ce5a0604c4669bb70f24e21906b015babebfb76e540fda9fd87`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 70.0 MB (69996727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd0f429f0ae9c0dfcbe4e4a0a000c40c0f51c66b3f27ca3a24e49d773e2af3c`  
		Last Modified: Wed, 08 Oct 2025 22:10:05 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:f569a6c02470d9b48f6a9719b16f8a2ef536cbe1211ecc12f936487aba61c777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1113486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4b3e083f9b4fa0c40a8082ad1ce012ab2c1b9e22fa7beb132420241f4ba444`

```dockerfile
```

-	Layers:
	-	`sha256:3fdf8a231bfa0803332f5275e62890777cf63dc47fcb8d137a896246cbd0affe`  
		Last Modified: Thu, 09 Oct 2025 00:10:25 GMT  
		Size: 1.1 MB (1098416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f5a824629380351fa0100a1f00c0e438e44a10630ca74c4090aed4df9cec1b8`  
		Last Modified: Thu, 09 Oct 2025 00:10:26 GMT  
		Size: 15.1 KB (15070 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35`

```console
$ docker pull telegraf@sha256:f8c3299f47bab24dbc41acf46e692f9dc653b035d956c82fcb4ad6664bd6d3df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35` - linux; amd64

```console
$ docker pull telegraf@sha256:6ff4de824062eb00f5e039b120c1b0f6ab45dfccc4fde210294feabef6d74bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171028185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107fcb9a6c1cd7f3b4470758f21e021c4e496461a528f00cde40e4e2593e5e25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:29:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:29:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 04:29:35 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 04 Nov 2025 04:29:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 04:29:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 04:29:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 04:29:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 04:29:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb445e472b1bad54f5a28edd51b11aec79eca8513394866a261891be9da6a343`  
		Last Modified: Tue, 04 Nov 2025 00:28:00 GMT  
		Size: 24.0 MB (24029301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96cc09aef6ed3c77d9b5704a689421533ddd110610e6c7d48a4bed108d11b16`  
		Last Modified: Tue, 04 Nov 2025 04:30:01 GMT  
		Size: 18.9 MB (18943070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13f6733bc1c20419bad8c8534a383e8597e26530c6f055ad3f7880407dd6624`  
		Last Modified: Tue, 04 Nov 2025 04:29:59 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334e7438e6f1e50a09a3a831ac697ead7c2ed47b7974e2f9672ac57ccd0c9b94`  
		Last Modified: Tue, 04 Nov 2025 04:30:06 GMT  
		Size: 79.6 MB (79570683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bac977df5fd0d2fd1c69f6264ddc17f23a8e9f630c5d9271499c2d00ebd25c`  
		Last Modified: Tue, 04 Nov 2025 04:29:59 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:88258424c2516f2878ca2f07454d9a75591777e289ef06f6a9b837921fb3762b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6659373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7abdfc36bf25250cb4c5c615af619bee74e92c7654224b2b9b1c47172113b6`

```dockerfile
```

-	Layers:
	-	`sha256:b61ede61c894a7bebeb5461e2d3b58a7d59a1674016fa1d1a6f7ff37af182f16`  
		Last Modified: Tue, 04 Nov 2025 10:10:46 GMT  
		Size: 6.6 MB (6644946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4129abe788d2e864a011b017f72e9017089adae31530d6c380f4419d1bb274`  
		Last Modified: Tue, 04 Nov 2025 10:10:47 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:fa6f7e75536f0367826e16ca9c2c7fd360cc222d77b83c35887007e2b79df1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157148712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cad37c5b357c92e0439c5b7fb5c960503555fc36489b8c07b315d9e454f28c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:39:43 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:39:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 02:39:50 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 04 Nov 2025 02:39:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 02:39:50 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 02:39:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 02:39:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 02:39:50 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:461f215c759f019a0fb4d33c976a91c4c2e4b033762b07a2f81bac66dee9e613`  
		Last Modified: Tue, 04 Nov 2025 00:12:30 GMT  
		Size: 44.2 MB (44196437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad602f359c1ad647108cc57270e592fc1f62f8ffd947a100fecee62a4a0d017`  
		Last Modified: Tue, 04 Nov 2025 00:39:15 GMT  
		Size: 21.9 MB (21934879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fae1c69af26861f65d9004c689ea4c2c9450fad59c414210bfda2559c8f3c3`  
		Last Modified: Tue, 04 Nov 2025 02:40:18 GMT  
		Size: 17.7 MB (17722580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53adae231cc08f3b841311dab16e20b852e4b45c1c2c16853a2a0d8603ad76e3`  
		Last Modified: Tue, 04 Nov 2025 02:40:16 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f141c13cb7af65c7eb6c7bfdfc08a15e3677f092c4e2b8ad1c3762166b85fe7`  
		Last Modified: Tue, 04 Nov 2025 02:40:21 GMT  
		Size: 73.3 MB (73290741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f99c9819e7307c39d86bed080f060eeb5702546aa1eac4f5af47d9b9ad72da`  
		Last Modified: Tue, 04 Nov 2025 02:40:07 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:982fbd9391d8e58a01cfce338511481085cb2e2d7d02495a7b76490c63863c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6654060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492494b6365c3385fe755a995d46da553703aeff2afe2b8ba35381cf201f4ad3`

```dockerfile
```

-	Layers:
	-	`sha256:5886325d1946e4a5dc4101ec73b6260fc932852263d2bdeecd79703937f781ac`  
		Last Modified: Tue, 04 Nov 2025 10:10:52 GMT  
		Size: 6.6 MB (6639543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dd72ccbd6be158901c6abb018aa03dce9052914a288e64c39fd3f0a49032b9d`  
		Last Modified: Tue, 04 Nov 2025 10:10:52 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:21ea69cf7c6c45a2c6c1513d147d7a24c349d8bfb3c3ec89acb401530d7213e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162925859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b85e8ede4fbf48ce9c001ddc2623a14d3aa7184613a5d0479a93584fda6ab7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:42:57 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:42:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 01:43:01 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 04 Nov 2025 01:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 01:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 01:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 01:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 01:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463896571d3ff5317461a64229e9e4cb27d6d877114079419cf8b4fc96b0c02`  
		Last Modified: Tue, 04 Nov 2025 00:30:33 GMT  
		Size: 23.6 MB (23598514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50562b77a80b15d71bfd3d81c4e77c19647ae2ebb49a1659a86a13787904724`  
		Last Modified: Tue, 04 Nov 2025 01:43:27 GMT  
		Size: 18.9 MB (18884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791a261af422cc9250bc87e8f13bda104d6afdd0076f4282ebebf84bf019c846`  
		Last Modified: Tue, 04 Nov 2025 01:43:26 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f99d3d0b622590dcedd63eb82b5ca9601be35b0a700b68458165a34f2aa35f`  
		Last Modified: Tue, 04 Nov 2025 01:43:35 GMT  
		Size: 72.1 MB (72079375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e0044a3e60577bf4f14151bc6c0249ebde1b9a4fff226dfa0b486e2b60f801`  
		Last Modified: Tue, 04 Nov 2025 01:43:26 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:4faecc761f0e0b4f16405c46964c19ce1944f70d51c7572c43fd60135d51a23d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868a802226343ab16f71909ac1893ef1ddab6990c37f8003fbd71d1c8923332e`

```dockerfile
```

-	Layers:
	-	`sha256:f6a2a8f8b4cbd17887c8741da672271714e124ae3cdd29e23dd7f6183044a005`  
		Last Modified: Tue, 04 Nov 2025 10:10:58 GMT  
		Size: 6.6 MB (6645622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55fb1ceb45897bf16dc54ca9d0241d0e5a0c63109a158ad947468f1dfa85cf3`  
		Last Modified: Tue, 04 Nov 2025 10:10:59 GMT  
		Size: 14.5 KB (14536 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35-alpine`

```console
$ docker pull telegraf@sha256:07f7dcf2b3827f051657569751cb64d5faff3e5a72a868693ffb9120e8235879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:218877c5f874e303ce9eff463bd641cd6524d5cb4bf594a918719ce7cb049492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85735517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c39d7be492e6591caa8ad4bed3b416b8e1b0012dabf4da111f2a659a79b3111`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccca5a3c76061483f8823e5d77dd23416fdb6c1db125a11118301458c29897c`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2332823178d0061e80a1f95c48765dbaf18df2dd31878bac57f31fc7e9a9feeb`  
		Last Modified: Wed, 08 Oct 2025 23:21:36 GMT  
		Size: 2.6 MB (2563472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251b8f38f4c764d714567e5ca660283254c5c1f76d6a3eb579385593c3db441f`  
		Last Modified: Thu, 09 Oct 2025 00:11:14 GMT  
		Size: 79.4 MB (79368696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2523c7a219f6fba7e1e9fd8f9a81fbc8fb21f84c41aa6b03e5f001f54fa7d4f`  
		Last Modified: Wed, 08 Oct 2025 23:21:37 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d5f21a0772915320f389bebe6d06e7068c9cfb1211b785a9b3f6333c50c294c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1148969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc15951201cadcadb797550a067ab3695eb31ecadbb317a8dbb86766c39fb43f`

```dockerfile
```

-	Layers:
	-	`sha256:f609b510765575f46fd07751df9253b9e0bef412ef4d52e9f96a165469460ed0`  
		Last Modified: Thu, 09 Oct 2025 00:10:32 GMT  
		Size: 1.1 MB (1134008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b8d9f56ca4b6828b99375d962b74da6a704fd9f3bb65cb4e937fc29576512b`  
		Last Modified: Thu, 09 Oct 2025 00:10:33 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2dc98b18a3b682b4d47915f648c59570b29ce00624355c476e03ec8b7437e844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78643760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a73c4abccf0bdf3e9ed8b9eb7c3415a9215de1a7580eefdf2b21df5e598d2ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb651d889db2dee7911408fa57f1d7539c6e6d834e35cef0953d16bae75bf92b`  
		Last Modified: Wed, 08 Oct 2025 22:10:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d79a0d11e911af062cf834a3903c2474ae8e732b43633aba958f2e6ad1016b9`  
		Last Modified: Wed, 08 Oct 2025 22:10:06 GMT  
		Size: 2.6 MB (2627489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564facf9ae36962cd5148a9e7a58a23d64ee343b817bdf79fbe0febc06402a3c`  
		Last Modified: Wed, 08 Oct 2025 22:10:15 GMT  
		Size: 71.9 MB (71877304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1f7ca04417cf2ffd90adfbbaee47bb81f8f7ebd0b7537bfd13f76b41d9bf2c`  
		Last Modified: Wed, 08 Oct 2025 22:10:07 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4753dbe48b97e81e45692abc4a4cc8c2bea6375210f9d3db090253c6327d3b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1144706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ef814572f43a3f8c71c902f5ec20cd44a4e27fb3aa10c609a6532bf95e196a`

```dockerfile
```

-	Layers:
	-	`sha256:eb88913d7607490638a82238d8cb692ac25949af926c0aae25a744e853aec341`  
		Last Modified: Thu, 09 Oct 2025 00:10:36 GMT  
		Size: 1.1 MB (1129635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a5c5dcdefea06875f2d3c71b915b1573aa37fde54d0649aa9189ca1bc85d5a`  
		Last Modified: Thu, 09 Oct 2025 00:10:37 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4`

```console
$ docker pull telegraf@sha256:f8c3299f47bab24dbc41acf46e692f9dc653b035d956c82fcb4ad6664bd6d3df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.4` - linux; amd64

```console
$ docker pull telegraf@sha256:6ff4de824062eb00f5e039b120c1b0f6ab45dfccc4fde210294feabef6d74bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171028185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107fcb9a6c1cd7f3b4470758f21e021c4e496461a528f00cde40e4e2593e5e25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:29:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:29:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 04:29:35 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 04 Nov 2025 04:29:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 04:29:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 04:29:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 04:29:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 04:29:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb445e472b1bad54f5a28edd51b11aec79eca8513394866a261891be9da6a343`  
		Last Modified: Tue, 04 Nov 2025 00:28:00 GMT  
		Size: 24.0 MB (24029301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96cc09aef6ed3c77d9b5704a689421533ddd110610e6c7d48a4bed108d11b16`  
		Last Modified: Tue, 04 Nov 2025 04:30:01 GMT  
		Size: 18.9 MB (18943070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13f6733bc1c20419bad8c8534a383e8597e26530c6f055ad3f7880407dd6624`  
		Last Modified: Tue, 04 Nov 2025 04:29:59 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334e7438e6f1e50a09a3a831ac697ead7c2ed47b7974e2f9672ac57ccd0c9b94`  
		Last Modified: Tue, 04 Nov 2025 04:30:06 GMT  
		Size: 79.6 MB (79570683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bac977df5fd0d2fd1c69f6264ddc17f23a8e9f630c5d9271499c2d00ebd25c`  
		Last Modified: Tue, 04 Nov 2025 04:29:59 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:88258424c2516f2878ca2f07454d9a75591777e289ef06f6a9b837921fb3762b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6659373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7abdfc36bf25250cb4c5c615af619bee74e92c7654224b2b9b1c47172113b6`

```dockerfile
```

-	Layers:
	-	`sha256:b61ede61c894a7bebeb5461e2d3b58a7d59a1674016fa1d1a6f7ff37af182f16`  
		Last Modified: Tue, 04 Nov 2025 10:10:46 GMT  
		Size: 6.6 MB (6644946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4129abe788d2e864a011b017f72e9017089adae31530d6c380f4419d1bb274`  
		Last Modified: Tue, 04 Nov 2025 10:10:47 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:fa6f7e75536f0367826e16ca9c2c7fd360cc222d77b83c35887007e2b79df1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157148712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cad37c5b357c92e0439c5b7fb5c960503555fc36489b8c07b315d9e454f28c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:39:43 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:39:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 02:39:50 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 04 Nov 2025 02:39:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 02:39:50 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 02:39:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 02:39:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 02:39:50 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:461f215c759f019a0fb4d33c976a91c4c2e4b033762b07a2f81bac66dee9e613`  
		Last Modified: Tue, 04 Nov 2025 00:12:30 GMT  
		Size: 44.2 MB (44196437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad602f359c1ad647108cc57270e592fc1f62f8ffd947a100fecee62a4a0d017`  
		Last Modified: Tue, 04 Nov 2025 00:39:15 GMT  
		Size: 21.9 MB (21934879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fae1c69af26861f65d9004c689ea4c2c9450fad59c414210bfda2559c8f3c3`  
		Last Modified: Tue, 04 Nov 2025 02:40:18 GMT  
		Size: 17.7 MB (17722580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53adae231cc08f3b841311dab16e20b852e4b45c1c2c16853a2a0d8603ad76e3`  
		Last Modified: Tue, 04 Nov 2025 02:40:16 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f141c13cb7af65c7eb6c7bfdfc08a15e3677f092c4e2b8ad1c3762166b85fe7`  
		Last Modified: Tue, 04 Nov 2025 02:40:21 GMT  
		Size: 73.3 MB (73290741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f99c9819e7307c39d86bed080f060eeb5702546aa1eac4f5af47d9b9ad72da`  
		Last Modified: Tue, 04 Nov 2025 02:40:07 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:982fbd9391d8e58a01cfce338511481085cb2e2d7d02495a7b76490c63863c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6654060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492494b6365c3385fe755a995d46da553703aeff2afe2b8ba35381cf201f4ad3`

```dockerfile
```

-	Layers:
	-	`sha256:5886325d1946e4a5dc4101ec73b6260fc932852263d2bdeecd79703937f781ac`  
		Last Modified: Tue, 04 Nov 2025 10:10:52 GMT  
		Size: 6.6 MB (6639543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dd72ccbd6be158901c6abb018aa03dce9052914a288e64c39fd3f0a49032b9d`  
		Last Modified: Tue, 04 Nov 2025 10:10:52 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:21ea69cf7c6c45a2c6c1513d147d7a24c349d8bfb3c3ec89acb401530d7213e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162925859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b85e8ede4fbf48ce9c001ddc2623a14d3aa7184613a5d0479a93584fda6ab7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:42:57 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:42:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 01:43:01 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 04 Nov 2025 01:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 01:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 01:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 01:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 01:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463896571d3ff5317461a64229e9e4cb27d6d877114079419cf8b4fc96b0c02`  
		Last Modified: Tue, 04 Nov 2025 00:30:33 GMT  
		Size: 23.6 MB (23598514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50562b77a80b15d71bfd3d81c4e77c19647ae2ebb49a1659a86a13787904724`  
		Last Modified: Tue, 04 Nov 2025 01:43:27 GMT  
		Size: 18.9 MB (18884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791a261af422cc9250bc87e8f13bda104d6afdd0076f4282ebebf84bf019c846`  
		Last Modified: Tue, 04 Nov 2025 01:43:26 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f99d3d0b622590dcedd63eb82b5ca9601be35b0a700b68458165a34f2aa35f`  
		Last Modified: Tue, 04 Nov 2025 01:43:35 GMT  
		Size: 72.1 MB (72079375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e0044a3e60577bf4f14151bc6c0249ebde1b9a4fff226dfa0b486e2b60f801`  
		Last Modified: Tue, 04 Nov 2025 01:43:26 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:4faecc761f0e0b4f16405c46964c19ce1944f70d51c7572c43fd60135d51a23d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868a802226343ab16f71909ac1893ef1ddab6990c37f8003fbd71d1c8923332e`

```dockerfile
```

-	Layers:
	-	`sha256:f6a2a8f8b4cbd17887c8741da672271714e124ae3cdd29e23dd7f6183044a005`  
		Last Modified: Tue, 04 Nov 2025 10:10:58 GMT  
		Size: 6.6 MB (6645622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55fb1ceb45897bf16dc54ca9d0241d0e5a0c63109a158ad947468f1dfa85cf3`  
		Last Modified: Tue, 04 Nov 2025 10:10:59 GMT  
		Size: 14.5 KB (14536 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4-alpine`

```console
$ docker pull telegraf@sha256:07f7dcf2b3827f051657569751cb64d5faff3e5a72a868693ffb9120e8235879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:218877c5f874e303ce9eff463bd641cd6524d5cb4bf594a918719ce7cb049492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85735517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c39d7be492e6591caa8ad4bed3b416b8e1b0012dabf4da111f2a659a79b3111`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccca5a3c76061483f8823e5d77dd23416fdb6c1db125a11118301458c29897c`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2332823178d0061e80a1f95c48765dbaf18df2dd31878bac57f31fc7e9a9feeb`  
		Last Modified: Wed, 08 Oct 2025 23:21:36 GMT  
		Size: 2.6 MB (2563472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251b8f38f4c764d714567e5ca660283254c5c1f76d6a3eb579385593c3db441f`  
		Last Modified: Thu, 09 Oct 2025 00:11:14 GMT  
		Size: 79.4 MB (79368696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2523c7a219f6fba7e1e9fd8f9a81fbc8fb21f84c41aa6b03e5f001f54fa7d4f`  
		Last Modified: Wed, 08 Oct 2025 23:21:37 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d5f21a0772915320f389bebe6d06e7068c9cfb1211b785a9b3f6333c50c294c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1148969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc15951201cadcadb797550a067ab3695eb31ecadbb317a8dbb86766c39fb43f`

```dockerfile
```

-	Layers:
	-	`sha256:f609b510765575f46fd07751df9253b9e0bef412ef4d52e9f96a165469460ed0`  
		Last Modified: Thu, 09 Oct 2025 00:10:32 GMT  
		Size: 1.1 MB (1134008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b8d9f56ca4b6828b99375d962b74da6a704fd9f3bb65cb4e937fc29576512b`  
		Last Modified: Thu, 09 Oct 2025 00:10:33 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2dc98b18a3b682b4d47915f648c59570b29ce00624355c476e03ec8b7437e844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78643760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a73c4abccf0bdf3e9ed8b9eb7c3415a9215de1a7580eefdf2b21df5e598d2ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb651d889db2dee7911408fa57f1d7539c6e6d834e35cef0953d16bae75bf92b`  
		Last Modified: Wed, 08 Oct 2025 22:10:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d79a0d11e911af062cf834a3903c2474ae8e732b43633aba958f2e6ad1016b9`  
		Last Modified: Wed, 08 Oct 2025 22:10:06 GMT  
		Size: 2.6 MB (2627489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564facf9ae36962cd5148a9e7a58a23d64ee343b817bdf79fbe0febc06402a3c`  
		Last Modified: Wed, 08 Oct 2025 22:10:15 GMT  
		Size: 71.9 MB (71877304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1f7ca04417cf2ffd90adfbbaee47bb81f8f7ebd0b7537bfd13f76b41d9bf2c`  
		Last Modified: Wed, 08 Oct 2025 22:10:07 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4753dbe48b97e81e45692abc4a4cc8c2bea6375210f9d3db090253c6327d3b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1144706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ef814572f43a3f8c71c902f5ec20cd44a4e27fb3aa10c609a6532bf95e196a`

```dockerfile
```

-	Layers:
	-	`sha256:eb88913d7607490638a82238d8cb692ac25949af926c0aae25a744e853aec341`  
		Last Modified: Thu, 09 Oct 2025 00:10:36 GMT  
		Size: 1.1 MB (1129635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a5c5dcdefea06875f2d3c71b915b1573aa37fde54d0649aa9189ca1bc85d5a`  
		Last Modified: Thu, 09 Oct 2025 00:10:37 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36`

```console
$ docker pull telegraf@sha256:532feb6341c2eb835eac808160f3011f3e5b0f87cb05e53797e6c98e107708dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36` - linux; amd64

```console
$ docker pull telegraf@sha256:0eccf97c41df048cd65c5fda6e277509513f363409c01eddb7f12fb8d0e6d92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171811238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0aab2138b5e5435b33d5d10b7e074b1c2788a205f0f167c1daa4b67f12111c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:29:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:29:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 04:29:37 GMT
ENV TELEGRAF_VERSION=1.36.3
# Tue, 04 Nov 2025 04:29:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 04:29:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 04:29:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 04:29:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 04:29:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb445e472b1bad54f5a28edd51b11aec79eca8513394866a261891be9da6a343`  
		Last Modified: Tue, 04 Nov 2025 00:28:00 GMT  
		Size: 24.0 MB (24029301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29cf6fb1834bc56f1820d5c84abc85f28695e95209a58393b1b26c9be121e69`  
		Last Modified: Tue, 04 Nov 2025 04:30:05 GMT  
		Size: 18.9 MB (18942926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b539859c7750f1249bb257b45a45b5f5ae305336e7bb8d90ac7a4d85015853f2`  
		Last Modified: Tue, 04 Nov 2025 04:30:03 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de777dc026ca1f1c8a52009c786da780f79b0974fe24d990991d63a040798c4`  
		Last Modified: Tue, 04 Nov 2025 04:30:11 GMT  
		Size: 80.4 MB (80353890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd426182f8e9b22e08d9c77eb985516563b545b8b4e72c57d5927d1863ecb0d0`  
		Last Modified: Tue, 04 Nov 2025 04:30:03 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:2dd6d812624bd07bda519a13abfb5f323108fdce3db208ee678b61716383c4bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6667434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9e2c337067463aec9c7fbb04e06c7038082371a84ae481c582d5b7b0e84d65`

```dockerfile
```

-	Layers:
	-	`sha256:214abe2901caf515feb72b6094317cc8b5156f2a540371abd1a0f73d6aee0f5f`  
		Last Modified: Tue, 04 Nov 2025 10:10:57 GMT  
		Size: 6.7 MB (6652705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:773612aaa5d3e5bd971e2a11ee5d3fc63d82b5b9ee67047ed48660ab1e2d1b59`  
		Last Modified: Tue, 04 Nov 2025 10:10:57 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:d665d3ec2da8e0875403b8e3acba6dcba67b59146e072f31cc012e82d5ff038d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157763649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066b7460db2684c096d017a087ba33208afc64b6edbff3db8b555f6b102f9532`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:39:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:39:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 02:39:43 GMT
ENV TELEGRAF_VERSION=1.36.3
# Tue, 04 Nov 2025 02:39:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 02:39:43 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 02:39:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 02:39:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 02:39:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:461f215c759f019a0fb4d33c976a91c4c2e4b033762b07a2f81bac66dee9e613`  
		Last Modified: Tue, 04 Nov 2025 00:12:30 GMT  
		Size: 44.2 MB (44196437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad602f359c1ad647108cc57270e592fc1f62f8ffd947a100fecee62a4a0d017`  
		Last Modified: Tue, 04 Nov 2025 00:39:15 GMT  
		Size: 21.9 MB (21934879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5207eacc0a636b8c0b0753ace942e14c051938d7aac0efb93c5a8a055bd312`  
		Last Modified: Tue, 04 Nov 2025 02:39:34 GMT  
		Size: 17.7 MB (17722410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00102ab6e81a9d64a6dbc8926419879ef6abccddbf68907fdbfc2a34a1f5dc0`  
		Last Modified: Tue, 04 Nov 2025 02:39:33 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60591fa952c11ef51933b7620508c7dd6f22a817271d52648335ddb4ce4bfbaf`  
		Last Modified: Tue, 04 Nov 2025 02:40:12 GMT  
		Size: 73.9 MB (73905858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f99c9819e7307c39d86bed080f060eeb5702546aa1eac4f5af47d9b9ad72da`  
		Last Modified: Tue, 04 Nov 2025 02:40:07 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:bcd463f3e90460200222d69e02e4009c91a797217c0f23e54a32aef67a83697b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804a4a55b056299edb7b984c408f203a2843ba6665899dd851c480282cee3a1f`

```dockerfile
```

-	Layers:
	-	`sha256:94f71825792615d055ebf7128970d032049db252208ff814851cf9892959aafc`  
		Last Modified: Tue, 04 Nov 2025 10:11:03 GMT  
		Size: 6.6 MB (6647310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93098f53e840a56d2933448aaf8de66a10e1e7b620d2e8ff9e7a56e80a867046`  
		Last Modified: Tue, 04 Nov 2025 10:11:04 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:77821a3b64585c47d06a94fbb482b55ab9d9d61e17de611c384d489545600fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162542379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cac55e111a130abb2ff7feae1dafd6a9cc179514d562c696921800942737cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:43:11 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:43:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 01:43:18 GMT
ENV TELEGRAF_VERSION=1.36.3
# Tue, 04 Nov 2025 01:43:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 01:43:18 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 01:43:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 01:43:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 01:43:18 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463896571d3ff5317461a64229e9e4cb27d6d877114079419cf8b4fc96b0c02`  
		Last Modified: Tue, 04 Nov 2025 00:30:33 GMT  
		Size: 23.6 MB (23598514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c9d59ad07179a8b0bc11da6ff910f4e751034bdf10bc03cb10f471d4dcfa26`  
		Last Modified: Tue, 04 Nov 2025 01:43:48 GMT  
		Size: 18.9 MB (18884193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d744edeb94bccdc025987feb82d5cf1c9ff0891355078bd049854bf32f85c9`  
		Last Modified: Tue, 04 Nov 2025 01:43:43 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c431dc7814280cfeac572c62ebf1bb79c797363cfc8f840e9c09f5891f253e`  
		Last Modified: Tue, 04 Nov 2025 01:43:49 GMT  
		Size: 71.7 MB (71696117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276c544e3a2d3349d4cc60169e6c49066766fd34b505119c53b92d06e130929d`  
		Last Modified: Tue, 04 Nov 2025 01:43:43 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:6f9676fd40264a609bf14834028aa5224af90b4abe27a36374f715e7a199ab41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6668244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1069351a285bc6288881d43209281d63049e94433d0a883905231c3e1c5470`

```dockerfile
```

-	Layers:
	-	`sha256:a90aeefb3f8b624abe0dbf283181184b613d8c398b731a488b37a398abf05f9c`  
		Last Modified: Tue, 04 Nov 2025 10:11:10 GMT  
		Size: 6.7 MB (6653393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cea634030cd9efd95c9adf2c31b3e1d45218270c9eb8efdc49a92c7fb470bff`  
		Last Modified: Tue, 04 Nov 2025 10:11:11 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36-alpine`

```console
$ docker pull telegraf@sha256:359556c05757bb26b973c5c03a9a290ae760c524ed72a8ae8f727614a13fec14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:3142c216dfbdc6576f522fde55ae0ccbb7335b6e03a1713311d0b4186838c505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86515645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e427efdea4a8fb5cb736a1377986faa86ecf7335403ba2efabdd7f74b17d6b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 12:55:43 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
ENV TELEGRAF_VERSION=1.36.3
# Tue, 21 Oct 2025 12:55:43 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 Oct 2025 12:55:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 12:55:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d97e0baba7acf4bad059d1f73d3314b45dc33c7c593c8a2afe5127ae695cfad`  
		Last Modified: Tue, 21 Oct 2025 20:21:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1dbc49469a3450880069f33164aaf832e3b41a98294e5938612570b2630dd0`  
		Last Modified: Tue, 21 Oct 2025 20:21:14 GMT  
		Size: 2.6 MB (2563453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253325094274804e685bd9523494dfca9ab8281fcc801072e66d33455c5d4ac4`  
		Last Modified: Tue, 21 Oct 2025 20:21:26 GMT  
		Size: 80.1 MB (80148841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8e8bc2c82ff62deefc92d60a7a46599001cbb37e70f7cdca7617671628501`  
		Last Modified: Tue, 21 Oct 2025 20:21:14 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:7b0ca25a5086ab700dc49ca6ea177f7768a971e3d86b4be7fccf1522b599c63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd777b3f82fe13274b76ed3104c24416c2f63ea534837be62965f0832289697`

```dockerfile
```

-	Layers:
	-	`sha256:0f57d03aeb4cb42475efbaad6252cfaf402560a49529c2665cfbcaa3c13bc874`  
		Last Modified: Wed, 22 Oct 2025 00:10:58 GMT  
		Size: 1.1 MB (1141767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0419a26e2b5039ae28ac84e491de6a5a719ebebbaaf1d2479fca01af905e6c0f`  
		Last Modified: Wed, 22 Oct 2025 00:10:59 GMT  
		Size: 15.3 KB (15260 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:bf5c23ac8cadb2228ab6621416112bc53ebfa79bda400c791bbcafa79dec0a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78253306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db508a1945b88c36627cad7cc09a5fbcd0486972a2060cc8e258d350f2f7725`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 12:55:43 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
ENV TELEGRAF_VERSION=1.36.3
# Tue, 21 Oct 2025 12:55:43 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 Oct 2025 12:55:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 12:55:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb909cb53ca9e6bb86134f146d1ca33c6dedb0821167413407e410ee200ee59`  
		Last Modified: Tue, 21 Oct 2025 19:54:54 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e007e67ea32dca87e6823192db2644b80a2ee8366143ca57b7c8f98010cc0e7`  
		Last Modified: Tue, 21 Oct 2025 19:54:54 GMT  
		Size: 2.6 MB (2627477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a7ce1279e4d16c85bd6d98f42db9b350023b91b09896aaee9d611e420d2cd8`  
		Last Modified: Tue, 21 Oct 2025 19:55:01 GMT  
		Size: 71.5 MB (71486861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed0cac4dda5fbfdcd57c065601b6de3cdd6172278d40c0c2b25b992c85d992d`  
		Last Modified: Tue, 21 Oct 2025 19:54:54 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:36cf9a48fcfa646d6c706b0df84b4b787d9e92252cbe7754a281357a1b83045e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1152791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b669839cd367293902ceb9b6cf8a704e516b55a3446c0bcabdafb1af77dc98`

```dockerfile
```

-	Layers:
	-	`sha256:5ef6d9fc9ecbcd708cd794080616bcd53d927c1c005b22e066637e82f99e8881`  
		Last Modified: Tue, 21 Oct 2025 21:10:33 GMT  
		Size: 1.1 MB (1137406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a4cbae9c9557f3f04efbaf078129d875871edfb35cc2e553132562c78cad93`  
		Last Modified: Tue, 21 Oct 2025 21:10:33 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.3`

```console
$ docker pull telegraf@sha256:532feb6341c2eb835eac808160f3011f3e5b0f87cb05e53797e6c98e107708dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.3` - linux; amd64

```console
$ docker pull telegraf@sha256:0eccf97c41df048cd65c5fda6e277509513f363409c01eddb7f12fb8d0e6d92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171811238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0aab2138b5e5435b33d5d10b7e074b1c2788a205f0f167c1daa4b67f12111c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:29:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:29:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 04:29:37 GMT
ENV TELEGRAF_VERSION=1.36.3
# Tue, 04 Nov 2025 04:29:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 04:29:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 04:29:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 04:29:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 04:29:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb445e472b1bad54f5a28edd51b11aec79eca8513394866a261891be9da6a343`  
		Last Modified: Tue, 04 Nov 2025 00:28:00 GMT  
		Size: 24.0 MB (24029301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29cf6fb1834bc56f1820d5c84abc85f28695e95209a58393b1b26c9be121e69`  
		Last Modified: Tue, 04 Nov 2025 04:30:05 GMT  
		Size: 18.9 MB (18942926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b539859c7750f1249bb257b45a45b5f5ae305336e7bb8d90ac7a4d85015853f2`  
		Last Modified: Tue, 04 Nov 2025 04:30:03 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de777dc026ca1f1c8a52009c786da780f79b0974fe24d990991d63a040798c4`  
		Last Modified: Tue, 04 Nov 2025 04:30:11 GMT  
		Size: 80.4 MB (80353890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd426182f8e9b22e08d9c77eb985516563b545b8b4e72c57d5927d1863ecb0d0`  
		Last Modified: Tue, 04 Nov 2025 04:30:03 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:2dd6d812624bd07bda519a13abfb5f323108fdce3db208ee678b61716383c4bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6667434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9e2c337067463aec9c7fbb04e06c7038082371a84ae481c582d5b7b0e84d65`

```dockerfile
```

-	Layers:
	-	`sha256:214abe2901caf515feb72b6094317cc8b5156f2a540371abd1a0f73d6aee0f5f`  
		Last Modified: Tue, 04 Nov 2025 10:10:57 GMT  
		Size: 6.7 MB (6652705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:773612aaa5d3e5bd971e2a11ee5d3fc63d82b5b9ee67047ed48660ab1e2d1b59`  
		Last Modified: Tue, 04 Nov 2025 10:10:57 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:d665d3ec2da8e0875403b8e3acba6dcba67b59146e072f31cc012e82d5ff038d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157763649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066b7460db2684c096d017a087ba33208afc64b6edbff3db8b555f6b102f9532`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:39:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:39:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 02:39:43 GMT
ENV TELEGRAF_VERSION=1.36.3
# Tue, 04 Nov 2025 02:39:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 02:39:43 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 02:39:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 02:39:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 02:39:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:461f215c759f019a0fb4d33c976a91c4c2e4b033762b07a2f81bac66dee9e613`  
		Last Modified: Tue, 04 Nov 2025 00:12:30 GMT  
		Size: 44.2 MB (44196437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad602f359c1ad647108cc57270e592fc1f62f8ffd947a100fecee62a4a0d017`  
		Last Modified: Tue, 04 Nov 2025 00:39:15 GMT  
		Size: 21.9 MB (21934879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5207eacc0a636b8c0b0753ace942e14c051938d7aac0efb93c5a8a055bd312`  
		Last Modified: Tue, 04 Nov 2025 02:39:34 GMT  
		Size: 17.7 MB (17722410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00102ab6e81a9d64a6dbc8926419879ef6abccddbf68907fdbfc2a34a1f5dc0`  
		Last Modified: Tue, 04 Nov 2025 02:39:33 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60591fa952c11ef51933b7620508c7dd6f22a817271d52648335ddb4ce4bfbaf`  
		Last Modified: Tue, 04 Nov 2025 02:40:12 GMT  
		Size: 73.9 MB (73905858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f99c9819e7307c39d86bed080f060eeb5702546aa1eac4f5af47d9b9ad72da`  
		Last Modified: Tue, 04 Nov 2025 02:40:07 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:bcd463f3e90460200222d69e02e4009c91a797217c0f23e54a32aef67a83697b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804a4a55b056299edb7b984c408f203a2843ba6665899dd851c480282cee3a1f`

```dockerfile
```

-	Layers:
	-	`sha256:94f71825792615d055ebf7128970d032049db252208ff814851cf9892959aafc`  
		Last Modified: Tue, 04 Nov 2025 10:11:03 GMT  
		Size: 6.6 MB (6647310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93098f53e840a56d2933448aaf8de66a10e1e7b620d2e8ff9e7a56e80a867046`  
		Last Modified: Tue, 04 Nov 2025 10:11:04 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:77821a3b64585c47d06a94fbb482b55ab9d9d61e17de611c384d489545600fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162542379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cac55e111a130abb2ff7feae1dafd6a9cc179514d562c696921800942737cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:43:11 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:43:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 01:43:18 GMT
ENV TELEGRAF_VERSION=1.36.3
# Tue, 04 Nov 2025 01:43:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 01:43:18 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 01:43:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 01:43:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 01:43:18 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463896571d3ff5317461a64229e9e4cb27d6d877114079419cf8b4fc96b0c02`  
		Last Modified: Tue, 04 Nov 2025 00:30:33 GMT  
		Size: 23.6 MB (23598514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c9d59ad07179a8b0bc11da6ff910f4e751034bdf10bc03cb10f471d4dcfa26`  
		Last Modified: Tue, 04 Nov 2025 01:43:48 GMT  
		Size: 18.9 MB (18884193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d744edeb94bccdc025987feb82d5cf1c9ff0891355078bd049854bf32f85c9`  
		Last Modified: Tue, 04 Nov 2025 01:43:43 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c431dc7814280cfeac572c62ebf1bb79c797363cfc8f840e9c09f5891f253e`  
		Last Modified: Tue, 04 Nov 2025 01:43:49 GMT  
		Size: 71.7 MB (71696117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276c544e3a2d3349d4cc60169e6c49066766fd34b505119c53b92d06e130929d`  
		Last Modified: Tue, 04 Nov 2025 01:43:43 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:6f9676fd40264a609bf14834028aa5224af90b4abe27a36374f715e7a199ab41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6668244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1069351a285bc6288881d43209281d63049e94433d0a883905231c3e1c5470`

```dockerfile
```

-	Layers:
	-	`sha256:a90aeefb3f8b624abe0dbf283181184b613d8c398b731a488b37a398abf05f9c`  
		Last Modified: Tue, 04 Nov 2025 10:11:10 GMT  
		Size: 6.7 MB (6653393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cea634030cd9efd95c9adf2c31b3e1d45218270c9eb8efdc49a92c7fb470bff`  
		Last Modified: Tue, 04 Nov 2025 10:11:11 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.3-alpine`

```console
$ docker pull telegraf@sha256:359556c05757bb26b973c5c03a9a290ae760c524ed72a8ae8f727614a13fec14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:3142c216dfbdc6576f522fde55ae0ccbb7335b6e03a1713311d0b4186838c505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86515645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e427efdea4a8fb5cb736a1377986faa86ecf7335403ba2efabdd7f74b17d6b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 12:55:43 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
ENV TELEGRAF_VERSION=1.36.3
# Tue, 21 Oct 2025 12:55:43 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 Oct 2025 12:55:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 12:55:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d97e0baba7acf4bad059d1f73d3314b45dc33c7c593c8a2afe5127ae695cfad`  
		Last Modified: Tue, 21 Oct 2025 20:21:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1dbc49469a3450880069f33164aaf832e3b41a98294e5938612570b2630dd0`  
		Last Modified: Tue, 21 Oct 2025 20:21:14 GMT  
		Size: 2.6 MB (2563453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253325094274804e685bd9523494dfca9ab8281fcc801072e66d33455c5d4ac4`  
		Last Modified: Tue, 21 Oct 2025 20:21:26 GMT  
		Size: 80.1 MB (80148841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8e8bc2c82ff62deefc92d60a7a46599001cbb37e70f7cdca7617671628501`  
		Last Modified: Tue, 21 Oct 2025 20:21:14 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:7b0ca25a5086ab700dc49ca6ea177f7768a971e3d86b4be7fccf1522b599c63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd777b3f82fe13274b76ed3104c24416c2f63ea534837be62965f0832289697`

```dockerfile
```

-	Layers:
	-	`sha256:0f57d03aeb4cb42475efbaad6252cfaf402560a49529c2665cfbcaa3c13bc874`  
		Last Modified: Wed, 22 Oct 2025 00:10:58 GMT  
		Size: 1.1 MB (1141767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0419a26e2b5039ae28ac84e491de6a5a719ebebbaaf1d2479fca01af905e6c0f`  
		Last Modified: Wed, 22 Oct 2025 00:10:59 GMT  
		Size: 15.3 KB (15260 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:bf5c23ac8cadb2228ab6621416112bc53ebfa79bda400c791bbcafa79dec0a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78253306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db508a1945b88c36627cad7cc09a5fbcd0486972a2060cc8e258d350f2f7725`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 12:55:43 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
ENV TELEGRAF_VERSION=1.36.3
# Tue, 21 Oct 2025 12:55:43 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 Oct 2025 12:55:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 12:55:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb909cb53ca9e6bb86134f146d1ca33c6dedb0821167413407e410ee200ee59`  
		Last Modified: Tue, 21 Oct 2025 19:54:54 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e007e67ea32dca87e6823192db2644b80a2ee8366143ca57b7c8f98010cc0e7`  
		Last Modified: Tue, 21 Oct 2025 19:54:54 GMT  
		Size: 2.6 MB (2627477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a7ce1279e4d16c85bd6d98f42db9b350023b91b09896aaee9d611e420d2cd8`  
		Last Modified: Tue, 21 Oct 2025 19:55:01 GMT  
		Size: 71.5 MB (71486861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed0cac4dda5fbfdcd57c065601b6de3cdd6172278d40c0c2b25b992c85d992d`  
		Last Modified: Tue, 21 Oct 2025 19:54:54 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:36cf9a48fcfa646d6c706b0df84b4b787d9e92252cbe7754a281357a1b83045e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1152791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b669839cd367293902ceb9b6cf8a704e516b55a3446c0bcabdafb1af77dc98`

```dockerfile
```

-	Layers:
	-	`sha256:5ef6d9fc9ecbcd708cd794080616bcd53d927c1c005b22e066637e82f99e8881`  
		Last Modified: Tue, 21 Oct 2025 21:10:33 GMT  
		Size: 1.1 MB (1137406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a4cbae9c9557f3f04efbaf078129d875871edfb35cc2e553132562c78cad93`  
		Last Modified: Tue, 21 Oct 2025 21:10:33 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:359556c05757bb26b973c5c03a9a290ae760c524ed72a8ae8f727614a13fec14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:3142c216dfbdc6576f522fde55ae0ccbb7335b6e03a1713311d0b4186838c505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86515645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e427efdea4a8fb5cb736a1377986faa86ecf7335403ba2efabdd7f74b17d6b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 12:55:43 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
ENV TELEGRAF_VERSION=1.36.3
# Tue, 21 Oct 2025 12:55:43 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 Oct 2025 12:55:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 12:55:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d97e0baba7acf4bad059d1f73d3314b45dc33c7c593c8a2afe5127ae695cfad`  
		Last Modified: Tue, 21 Oct 2025 20:21:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1dbc49469a3450880069f33164aaf832e3b41a98294e5938612570b2630dd0`  
		Last Modified: Tue, 21 Oct 2025 20:21:14 GMT  
		Size: 2.6 MB (2563453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253325094274804e685bd9523494dfca9ab8281fcc801072e66d33455c5d4ac4`  
		Last Modified: Tue, 21 Oct 2025 20:21:26 GMT  
		Size: 80.1 MB (80148841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8e8bc2c82ff62deefc92d60a7a46599001cbb37e70f7cdca7617671628501`  
		Last Modified: Tue, 21 Oct 2025 20:21:14 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:7b0ca25a5086ab700dc49ca6ea177f7768a971e3d86b4be7fccf1522b599c63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd777b3f82fe13274b76ed3104c24416c2f63ea534837be62965f0832289697`

```dockerfile
```

-	Layers:
	-	`sha256:0f57d03aeb4cb42475efbaad6252cfaf402560a49529c2665cfbcaa3c13bc874`  
		Last Modified: Wed, 22 Oct 2025 00:10:58 GMT  
		Size: 1.1 MB (1141767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0419a26e2b5039ae28ac84e491de6a5a719ebebbaaf1d2479fca01af905e6c0f`  
		Last Modified: Wed, 22 Oct 2025 00:10:59 GMT  
		Size: 15.3 KB (15260 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:bf5c23ac8cadb2228ab6621416112bc53ebfa79bda400c791bbcafa79dec0a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78253306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db508a1945b88c36627cad7cc09a5fbcd0486972a2060cc8e258d350f2f7725`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 12:55:43 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
ENV TELEGRAF_VERSION=1.36.3
# Tue, 21 Oct 2025 12:55:43 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 Oct 2025 12:55:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 Oct 2025 12:55:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 12:55:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb909cb53ca9e6bb86134f146d1ca33c6dedb0821167413407e410ee200ee59`  
		Last Modified: Tue, 21 Oct 2025 19:54:54 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e007e67ea32dca87e6823192db2644b80a2ee8366143ca57b7c8f98010cc0e7`  
		Last Modified: Tue, 21 Oct 2025 19:54:54 GMT  
		Size: 2.6 MB (2627477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a7ce1279e4d16c85bd6d98f42db9b350023b91b09896aaee9d611e420d2cd8`  
		Last Modified: Tue, 21 Oct 2025 19:55:01 GMT  
		Size: 71.5 MB (71486861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed0cac4dda5fbfdcd57c065601b6de3cdd6172278d40c0c2b25b992c85d992d`  
		Last Modified: Tue, 21 Oct 2025 19:54:54 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:36cf9a48fcfa646d6c706b0df84b4b787d9e92252cbe7754a281357a1b83045e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1152791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b669839cd367293902ceb9b6cf8a704e516b55a3446c0bcabdafb1af77dc98`

```dockerfile
```

-	Layers:
	-	`sha256:5ef6d9fc9ecbcd708cd794080616bcd53d927c1c005b22e066637e82f99e8881`  
		Last Modified: Tue, 21 Oct 2025 21:10:33 GMT  
		Size: 1.1 MB (1137406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a4cbae9c9557f3f04efbaf078129d875871edfb35cc2e553132562c78cad93`  
		Last Modified: Tue, 21 Oct 2025 21:10:33 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:532feb6341c2eb835eac808160f3011f3e5b0f87cb05e53797e6c98e107708dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:0eccf97c41df048cd65c5fda6e277509513f363409c01eddb7f12fb8d0e6d92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171811238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0aab2138b5e5435b33d5d10b7e074b1c2788a205f0f167c1daa4b67f12111c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:29:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:29:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 04:29:37 GMT
ENV TELEGRAF_VERSION=1.36.3
# Tue, 04 Nov 2025 04:29:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 04:29:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 04:29:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 04:29:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 04:29:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb445e472b1bad54f5a28edd51b11aec79eca8513394866a261891be9da6a343`  
		Last Modified: Tue, 04 Nov 2025 00:28:00 GMT  
		Size: 24.0 MB (24029301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29cf6fb1834bc56f1820d5c84abc85f28695e95209a58393b1b26c9be121e69`  
		Last Modified: Tue, 04 Nov 2025 04:30:05 GMT  
		Size: 18.9 MB (18942926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b539859c7750f1249bb257b45a45b5f5ae305336e7bb8d90ac7a4d85015853f2`  
		Last Modified: Tue, 04 Nov 2025 04:30:03 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de777dc026ca1f1c8a52009c786da780f79b0974fe24d990991d63a040798c4`  
		Last Modified: Tue, 04 Nov 2025 04:30:11 GMT  
		Size: 80.4 MB (80353890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd426182f8e9b22e08d9c77eb985516563b545b8b4e72c57d5927d1863ecb0d0`  
		Last Modified: Tue, 04 Nov 2025 04:30:03 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:2dd6d812624bd07bda519a13abfb5f323108fdce3db208ee678b61716383c4bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6667434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9e2c337067463aec9c7fbb04e06c7038082371a84ae481c582d5b7b0e84d65`

```dockerfile
```

-	Layers:
	-	`sha256:214abe2901caf515feb72b6094317cc8b5156f2a540371abd1a0f73d6aee0f5f`  
		Last Modified: Tue, 04 Nov 2025 10:10:57 GMT  
		Size: 6.7 MB (6652705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:773612aaa5d3e5bd971e2a11ee5d3fc63d82b5b9ee67047ed48660ab1e2d1b59`  
		Last Modified: Tue, 04 Nov 2025 10:10:57 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:d665d3ec2da8e0875403b8e3acba6dcba67b59146e072f31cc012e82d5ff038d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157763649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066b7460db2684c096d017a087ba33208afc64b6edbff3db8b555f6b102f9532`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:39:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:39:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 02:39:43 GMT
ENV TELEGRAF_VERSION=1.36.3
# Tue, 04 Nov 2025 02:39:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 02:39:43 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 02:39:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 02:39:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 02:39:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:461f215c759f019a0fb4d33c976a91c4c2e4b033762b07a2f81bac66dee9e613`  
		Last Modified: Tue, 04 Nov 2025 00:12:30 GMT  
		Size: 44.2 MB (44196437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad602f359c1ad647108cc57270e592fc1f62f8ffd947a100fecee62a4a0d017`  
		Last Modified: Tue, 04 Nov 2025 00:39:15 GMT  
		Size: 21.9 MB (21934879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5207eacc0a636b8c0b0753ace942e14c051938d7aac0efb93c5a8a055bd312`  
		Last Modified: Tue, 04 Nov 2025 02:39:34 GMT  
		Size: 17.7 MB (17722410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00102ab6e81a9d64a6dbc8926419879ef6abccddbf68907fdbfc2a34a1f5dc0`  
		Last Modified: Tue, 04 Nov 2025 02:39:33 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60591fa952c11ef51933b7620508c7dd6f22a817271d52648335ddb4ce4bfbaf`  
		Last Modified: Tue, 04 Nov 2025 02:40:12 GMT  
		Size: 73.9 MB (73905858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f99c9819e7307c39d86bed080f060eeb5702546aa1eac4f5af47d9b9ad72da`  
		Last Modified: Tue, 04 Nov 2025 02:40:07 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:bcd463f3e90460200222d69e02e4009c91a797217c0f23e54a32aef67a83697b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804a4a55b056299edb7b984c408f203a2843ba6665899dd851c480282cee3a1f`

```dockerfile
```

-	Layers:
	-	`sha256:94f71825792615d055ebf7128970d032049db252208ff814851cf9892959aafc`  
		Last Modified: Tue, 04 Nov 2025 10:11:03 GMT  
		Size: 6.6 MB (6647310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93098f53e840a56d2933448aaf8de66a10e1e7b620d2e8ff9e7a56e80a867046`  
		Last Modified: Tue, 04 Nov 2025 10:11:04 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:77821a3b64585c47d06a94fbb482b55ab9d9d61e17de611c384d489545600fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162542379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cac55e111a130abb2ff7feae1dafd6a9cc179514d562c696921800942737cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:43:11 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:43:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 01:43:18 GMT
ENV TELEGRAF_VERSION=1.36.3
# Tue, 04 Nov 2025 01:43:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 01:43:18 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 01:43:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 01:43:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 01:43:18 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463896571d3ff5317461a64229e9e4cb27d6d877114079419cf8b4fc96b0c02`  
		Last Modified: Tue, 04 Nov 2025 00:30:33 GMT  
		Size: 23.6 MB (23598514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c9d59ad07179a8b0bc11da6ff910f4e751034bdf10bc03cb10f471d4dcfa26`  
		Last Modified: Tue, 04 Nov 2025 01:43:48 GMT  
		Size: 18.9 MB (18884193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d744edeb94bccdc025987feb82d5cf1c9ff0891355078bd049854bf32f85c9`  
		Last Modified: Tue, 04 Nov 2025 01:43:43 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c431dc7814280cfeac572c62ebf1bb79c797363cfc8f840e9c09f5891f253e`  
		Last Modified: Tue, 04 Nov 2025 01:43:49 GMT  
		Size: 71.7 MB (71696117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276c544e3a2d3349d4cc60169e6c49066766fd34b505119c53b92d06e130929d`  
		Last Modified: Tue, 04 Nov 2025 01:43:43 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:6f9676fd40264a609bf14834028aa5224af90b4abe27a36374f715e7a199ab41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6668244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1069351a285bc6288881d43209281d63049e94433d0a883905231c3e1c5470`

```dockerfile
```

-	Layers:
	-	`sha256:a90aeefb3f8b624abe0dbf283181184b613d8c398b731a488b37a398abf05f9c`  
		Last Modified: Tue, 04 Nov 2025 10:11:10 GMT  
		Size: 6.7 MB (6653393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cea634030cd9efd95c9adf2c31b3e1d45218270c9eb8efdc49a92c7fb470bff`  
		Last Modified: Tue, 04 Nov 2025 10:11:11 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
