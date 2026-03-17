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
$ docker pull kapacitor@sha256:8568a2357f06d04c87988c4f81d1f43ad8ebf74feef09079bca2a9bcdf3f4a4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:60de8ac5601c9be2bd502219d4497353bedf9ee716c40c1f075aef11e4789ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.4 MB (159362954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bfe761397d768e2cdb2b083f6920a787e4b3accbd30651ca2487710a820e7c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:40:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Mar 2026 02:40:10 GMT
ENV KAPACITOR_VERSION=1.7.7
# Tue, 17 Mar 2026 02:40:10 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Mar 2026 02:40:10 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Mar 2026 02:40:10 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Mar 2026 02:40:10 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Mar 2026 02:40:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 02:40:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 02:40:10 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd31ed89fd7d59ba427c9f431e17b158ade8eb04083b8b256c587fc6521fb6b`  
		Last Modified: Tue, 17 Mar 2026 01:15:21 GMT  
		Size: 7.1 MB (7105152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ac82fe77848baf081901bcdfe25c86d8a81c4a86113eaf654f9dc47d2d0b83`  
		Last Modified: Tue, 17 Mar 2026 02:40:26 GMT  
		Size: 50.7 MB (50667720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c7c1c60bb20367459bb55fea85742de64027c2d459c40e58328c90dbae8705`  
		Last Modified: Tue, 17 Mar 2026 02:40:26 GMT  
		Size: 72.1 MB (72051039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd370e1d59266ae8ed08e88119a193dac86aa246aa65178cb0a2feae4a6ffba`  
		Last Modified: Tue, 17 Mar 2026 02:40:24 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e96aeac3bcfe8d63ef7b858a401d5c2510c0b635a82b3c9ef06ff9e2f197da`  
		Last Modified: Tue, 17 Mar 2026 02:40:24 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:68a52e5bfb2b5e7b3eb1e8e6c2b8edac9b3c2aed76633818a23562ccdec81ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c207987cfed1af166147030d2a3afdb74096bd02a963b96b0c78446d72f73b4`

```dockerfile
```

-	Layers:
	-	`sha256:6719adcd9b54ee24bfead49d9cc556e36c7cd82efe7ab82989d50009ec0f08e3`  
		Last Modified: Tue, 17 Mar 2026 02:40:24 GMT  
		Size: 3.7 MB (3716676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e5b28777ec69e01035d456c180da4b2159553ba7fc0d5e138533e53d0c2d8b6`  
		Last Modified: Tue, 17 Mar 2026 02:40:24 GMT  
		Size: 14.7 KB (14716 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:6f53ef35adfca87df63d66e75c817e7da0948d6a9b095ebd70a45d2710f28043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151620974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3c3a857b306b2b6ae612152085d46426114e998bb01c138be4bb8dcd73ef9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:44:20 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Mar 2026 02:44:23 GMT
ENV KAPACITOR_VERSION=1.7.7
# Tue, 17 Mar 2026 02:44:23 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Mar 2026 02:44:23 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Mar 2026 02:44:23 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Mar 2026 02:44:23 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Mar 2026 02:44:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 02:44:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 02:44:23 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6485dc332a06408f602b0cdb9b519fb93ef48ddb953b0ca66a482c8afa276f5e`  
		Last Modified: Tue, 17 Mar 2026 01:15:34 GMT  
		Size: 7.1 MB (7059209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a706e4b0ce2277b46a6267c53f4d53c199f8466da7cec49689930e0258b037e6`  
		Last Modified: Tue, 17 Mar 2026 02:44:38 GMT  
		Size: 49.4 MB (49358472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb94b55a52f1532ad667420df42fc1156f19aa8ea78a5cc603f9b9208d38deb`  
		Last Modified: Tue, 17 Mar 2026 02:44:38 GMT  
		Size: 67.8 MB (67813742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1c2ada3c296312b3dab8215d0efb8ff9c45f7df7f98dec60dce40e8116062f`  
		Last Modified: Tue, 17 Mar 2026 02:44:36 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da277cd004014e3e122a67547ca53d23d882c721dbfc34e25e0df4d204175c4`  
		Last Modified: Tue, 17 Mar 2026 02:44:36 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:f4c1657e4e4ac8ed6244f6fa6b40c4887cd56c32a4601351bde564289ecf55ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f7e0181c01ff6582ab7f2b00cf5a9c78dec06aace52d6e00db202c2b94454b`

```dockerfile
```

-	Layers:
	-	`sha256:65fb05e7996e6a66827f950f29e4b21481caf806ea3b79c1e0d4b7b6dc03da20`  
		Last Modified: Tue, 17 Mar 2026 02:44:36 GMT  
		Size: 3.7 MB (3716138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7feee0e65e9bdc4b097bc5cc542670c9e9f4dfb31cc840e7e9d6fc9d57a15fc5`  
		Last Modified: Tue, 17 Mar 2026 02:44:36 GMT  
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
$ docker pull kapacitor@sha256:8568a2357f06d04c87988c4f81d1f43ad8ebf74feef09079bca2a9bcdf3f4a4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:60de8ac5601c9be2bd502219d4497353bedf9ee716c40c1f075aef11e4789ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.4 MB (159362954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bfe761397d768e2cdb2b083f6920a787e4b3accbd30651ca2487710a820e7c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:40:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Mar 2026 02:40:10 GMT
ENV KAPACITOR_VERSION=1.7.7
# Tue, 17 Mar 2026 02:40:10 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Mar 2026 02:40:10 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Mar 2026 02:40:10 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Mar 2026 02:40:10 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Mar 2026 02:40:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 02:40:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 02:40:10 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd31ed89fd7d59ba427c9f431e17b158ade8eb04083b8b256c587fc6521fb6b`  
		Last Modified: Tue, 17 Mar 2026 01:15:21 GMT  
		Size: 7.1 MB (7105152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ac82fe77848baf081901bcdfe25c86d8a81c4a86113eaf654f9dc47d2d0b83`  
		Last Modified: Tue, 17 Mar 2026 02:40:26 GMT  
		Size: 50.7 MB (50667720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c7c1c60bb20367459bb55fea85742de64027c2d459c40e58328c90dbae8705`  
		Last Modified: Tue, 17 Mar 2026 02:40:26 GMT  
		Size: 72.1 MB (72051039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd370e1d59266ae8ed08e88119a193dac86aa246aa65178cb0a2feae4a6ffba`  
		Last Modified: Tue, 17 Mar 2026 02:40:24 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e96aeac3bcfe8d63ef7b858a401d5c2510c0b635a82b3c9ef06ff9e2f197da`  
		Last Modified: Tue, 17 Mar 2026 02:40:24 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:68a52e5bfb2b5e7b3eb1e8e6c2b8edac9b3c2aed76633818a23562ccdec81ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c207987cfed1af166147030d2a3afdb74096bd02a963b96b0c78446d72f73b4`

```dockerfile
```

-	Layers:
	-	`sha256:6719adcd9b54ee24bfead49d9cc556e36c7cd82efe7ab82989d50009ec0f08e3`  
		Last Modified: Tue, 17 Mar 2026 02:40:24 GMT  
		Size: 3.7 MB (3716676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e5b28777ec69e01035d456c180da4b2159553ba7fc0d5e138533e53d0c2d8b6`  
		Last Modified: Tue, 17 Mar 2026 02:40:24 GMT  
		Size: 14.7 KB (14716 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:6f53ef35adfca87df63d66e75c817e7da0948d6a9b095ebd70a45d2710f28043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151620974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3c3a857b306b2b6ae612152085d46426114e998bb01c138be4bb8dcd73ef9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:44:20 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Mar 2026 02:44:23 GMT
ENV KAPACITOR_VERSION=1.7.7
# Tue, 17 Mar 2026 02:44:23 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Mar 2026 02:44:23 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Mar 2026 02:44:23 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Mar 2026 02:44:23 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Mar 2026 02:44:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 02:44:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 02:44:23 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6485dc332a06408f602b0cdb9b519fb93ef48ddb953b0ca66a482c8afa276f5e`  
		Last Modified: Tue, 17 Mar 2026 01:15:34 GMT  
		Size: 7.1 MB (7059209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a706e4b0ce2277b46a6267c53f4d53c199f8466da7cec49689930e0258b037e6`  
		Last Modified: Tue, 17 Mar 2026 02:44:38 GMT  
		Size: 49.4 MB (49358472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb94b55a52f1532ad667420df42fc1156f19aa8ea78a5cc603f9b9208d38deb`  
		Last Modified: Tue, 17 Mar 2026 02:44:38 GMT  
		Size: 67.8 MB (67813742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1c2ada3c296312b3dab8215d0efb8ff9c45f7df7f98dec60dce40e8116062f`  
		Last Modified: Tue, 17 Mar 2026 02:44:36 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da277cd004014e3e122a67547ca53d23d882c721dbfc34e25e0df4d204175c4`  
		Last Modified: Tue, 17 Mar 2026 02:44:36 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:f4c1657e4e4ac8ed6244f6fa6b40c4887cd56c32a4601351bde564289ecf55ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f7e0181c01ff6582ab7f2b00cf5a9c78dec06aace52d6e00db202c2b94454b`

```dockerfile
```

-	Layers:
	-	`sha256:65fb05e7996e6a66827f950f29e4b21481caf806ea3b79c1e0d4b7b6dc03da20`  
		Last Modified: Tue, 17 Mar 2026 02:44:36 GMT  
		Size: 3.7 MB (3716138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7feee0e65e9bdc4b097bc5cc542670c9e9f4dfb31cc840e7e9d6fc9d57a15fc5`  
		Last Modified: Tue, 17 Mar 2026 02:44:36 GMT  
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
$ docker pull kapacitor@sha256:52f2d991e3a1064e716734de9ec78f085abcfdd090098b542fa658ed1b3d5987
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8` - linux; amd64

```console
$ docker pull kapacitor@sha256:e7a23e3c05070c0aac87695bdf10ee99901f9f5bce1b02b887f4b9afc1680781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (173029078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65dc2ecf364a0976ac5ca0ef6ca7ae10a9ae95e141c0f1ff0315be291cf74dcf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:40:11 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Mar 2026 02:40:18 GMT
ENV KAPACITOR_VERSION=1.8.3
# Tue, 17 Mar 2026 02:40:18 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Mar 2026 02:40:18 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Mar 2026 02:40:18 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Mar 2026 02:40:18 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Mar 2026 02:40:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 02:40:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 02:40:18 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd31ed89fd7d59ba427c9f431e17b158ade8eb04083b8b256c587fc6521fb6b`  
		Last Modified: Tue, 17 Mar 2026 01:15:21 GMT  
		Size: 7.1 MB (7105152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bc0f9c00e2b6e662f7a920d9aef458bbe3eafcc22aba548c21ca3f3a19fb56`  
		Last Modified: Tue, 17 Mar 2026 02:40:39 GMT  
		Size: 50.7 MB (50667718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c760a46d606f2698a2328be4d6c542ab7a1e4edec24d4b8139422fb67ce369`  
		Last Modified: Tue, 17 Mar 2026 02:40:39 GMT  
		Size: 85.7 MB (85717164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9774290e0c67172532dccd10161b619445dc3a257405aea55585b6e5ca3c6224`  
		Last Modified: Tue, 17 Mar 2026 02:40:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acc4c6e25f0b3d98efc5276b357b424ae2f6da7e3f4d2c8368e71afc72fc921`  
		Last Modified: Tue, 17 Mar 2026 02:40:36 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:ebc70055a5cb05d6d6ef496b2aea990633cd87305668f95060870b10f00cb0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b52ab4a74dc29aacce403c2e2acda624b663ab551eed0968450bd1fbcb7355`

```dockerfile
```

-	Layers:
	-	`sha256:2ec3ec59580704e49c96146c8bb4ee65ce1e2e0f3303ef2a37aee13cca63fd49`  
		Last Modified: Tue, 17 Mar 2026 02:40:37 GMT  
		Size: 3.7 MB (3732026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bba61c02d13d363b8f33ead821f8ec2156a03478d4b68ec25295cd0938500636`  
		Last Modified: Tue, 17 Mar 2026 02:40:36 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:6af8187350bb795170c1fe7e4f87853fc11869a75101ca56f5e98acb66fcd612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163951015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9300188ac717d93bddd21409b598a1437595d957079e7dfe31266f0ced6dc689`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:44:20 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Mar 2026 02:44:27 GMT
ENV KAPACITOR_VERSION=1.8.3
# Tue, 17 Mar 2026 02:44:27 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Mar 2026 02:44:27 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Mar 2026 02:44:27 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Mar 2026 02:44:27 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Mar 2026 02:44:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 02:44:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 02:44:27 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6485dc332a06408f602b0cdb9b519fb93ef48ddb953b0ca66a482c8afa276f5e`  
		Last Modified: Tue, 17 Mar 2026 01:15:34 GMT  
		Size: 7.1 MB (7059209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2c68e5a146aa55ebc8b1a2ada5b4f240999c798eb271cf390848ef03a27dc0`  
		Last Modified: Tue, 17 Mar 2026 02:44:47 GMT  
		Size: 49.4 MB (49358453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ed7e0e3f6c7036ca6b8563037442db5e99f3105b176e9af26bc82dd8511aec`  
		Last Modified: Tue, 17 Mar 2026 02:44:48 GMT  
		Size: 80.1 MB (80143804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bde3905ca617547255712cf50cf70d78d5d7b12f049cf9cb1cfc0a06e91158`  
		Last Modified: Tue, 17 Mar 2026 02:44:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da277cd004014e3e122a67547ca53d23d882c721dbfc34e25e0df4d204175c4`  
		Last Modified: Tue, 17 Mar 2026 02:44:36 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:b418bb03b4234d4a8026742ce8672a144ba1ba5232f62bd4feafb4d826fb1f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d10ccd355326985d3f2a6af5dcda26904dbb5671fd0105813a54f64e74a006a`

```dockerfile
```

-	Layers:
	-	`sha256:5ea408d702716cc14d5144e339b9a2053f24b68030e705daf278d949ea4765ad`  
		Last Modified: Tue, 17 Mar 2026 02:44:45 GMT  
		Size: 3.7 MB (3731500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:973cd61ebc180c56813489bdf4ef61d2c374abad013a12e481590837cbd7b972`  
		Last Modified: Tue, 17 Mar 2026 02:44:45 GMT  
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
$ docker pull kapacitor@sha256:52f2d991e3a1064e716734de9ec78f085abcfdd090098b542fa658ed1b3d5987
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8.3` - linux; amd64

```console
$ docker pull kapacitor@sha256:e7a23e3c05070c0aac87695bdf10ee99901f9f5bce1b02b887f4b9afc1680781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (173029078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65dc2ecf364a0976ac5ca0ef6ca7ae10a9ae95e141c0f1ff0315be291cf74dcf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:40:11 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Mar 2026 02:40:18 GMT
ENV KAPACITOR_VERSION=1.8.3
# Tue, 17 Mar 2026 02:40:18 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Mar 2026 02:40:18 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Mar 2026 02:40:18 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Mar 2026 02:40:18 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Mar 2026 02:40:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 02:40:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 02:40:18 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd31ed89fd7d59ba427c9f431e17b158ade8eb04083b8b256c587fc6521fb6b`  
		Last Modified: Tue, 17 Mar 2026 01:15:21 GMT  
		Size: 7.1 MB (7105152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bc0f9c00e2b6e662f7a920d9aef458bbe3eafcc22aba548c21ca3f3a19fb56`  
		Last Modified: Tue, 17 Mar 2026 02:40:39 GMT  
		Size: 50.7 MB (50667718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c760a46d606f2698a2328be4d6c542ab7a1e4edec24d4b8139422fb67ce369`  
		Last Modified: Tue, 17 Mar 2026 02:40:39 GMT  
		Size: 85.7 MB (85717164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9774290e0c67172532dccd10161b619445dc3a257405aea55585b6e5ca3c6224`  
		Last Modified: Tue, 17 Mar 2026 02:40:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acc4c6e25f0b3d98efc5276b357b424ae2f6da7e3f4d2c8368e71afc72fc921`  
		Last Modified: Tue, 17 Mar 2026 02:40:36 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.3` - unknown; unknown

```console
$ docker pull kapacitor@sha256:ebc70055a5cb05d6d6ef496b2aea990633cd87305668f95060870b10f00cb0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b52ab4a74dc29aacce403c2e2acda624b663ab551eed0968450bd1fbcb7355`

```dockerfile
```

-	Layers:
	-	`sha256:2ec3ec59580704e49c96146c8bb4ee65ce1e2e0f3303ef2a37aee13cca63fd49`  
		Last Modified: Tue, 17 Mar 2026 02:40:37 GMT  
		Size: 3.7 MB (3732026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bba61c02d13d363b8f33ead821f8ec2156a03478d4b68ec25295cd0938500636`  
		Last Modified: Tue, 17 Mar 2026 02:40:36 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8.3` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:6af8187350bb795170c1fe7e4f87853fc11869a75101ca56f5e98acb66fcd612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163951015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9300188ac717d93bddd21409b598a1437595d957079e7dfe31266f0ced6dc689`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:44:20 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Mar 2026 02:44:27 GMT
ENV KAPACITOR_VERSION=1.8.3
# Tue, 17 Mar 2026 02:44:27 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Mar 2026 02:44:27 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Mar 2026 02:44:27 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Mar 2026 02:44:27 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Mar 2026 02:44:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 02:44:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 02:44:27 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6485dc332a06408f602b0cdb9b519fb93ef48ddb953b0ca66a482c8afa276f5e`  
		Last Modified: Tue, 17 Mar 2026 01:15:34 GMT  
		Size: 7.1 MB (7059209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2c68e5a146aa55ebc8b1a2ada5b4f240999c798eb271cf390848ef03a27dc0`  
		Last Modified: Tue, 17 Mar 2026 02:44:47 GMT  
		Size: 49.4 MB (49358453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ed7e0e3f6c7036ca6b8563037442db5e99f3105b176e9af26bc82dd8511aec`  
		Last Modified: Tue, 17 Mar 2026 02:44:48 GMT  
		Size: 80.1 MB (80143804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bde3905ca617547255712cf50cf70d78d5d7b12f049cf9cb1cfc0a06e91158`  
		Last Modified: Tue, 17 Mar 2026 02:44:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da277cd004014e3e122a67547ca53d23d882c721dbfc34e25e0df4d204175c4`  
		Last Modified: Tue, 17 Mar 2026 02:44:36 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.3` - unknown; unknown

```console
$ docker pull kapacitor@sha256:b418bb03b4234d4a8026742ce8672a144ba1ba5232f62bd4feafb4d826fb1f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d10ccd355326985d3f2a6af5dcda26904dbb5671fd0105813a54f64e74a006a`

```dockerfile
```

-	Layers:
	-	`sha256:5ea408d702716cc14d5144e339b9a2053f24b68030e705daf278d949ea4765ad`  
		Last Modified: Tue, 17 Mar 2026 02:44:45 GMT  
		Size: 3.7 MB (3731500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:973cd61ebc180c56813489bdf4ef61d2c374abad013a12e481590837cbd7b972`  
		Last Modified: Tue, 17 Mar 2026 02:44:45 GMT  
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
$ docker pull kapacitor@sha256:52f2d991e3a1064e716734de9ec78f085abcfdd090098b542fa658ed1b3d5987
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:e7a23e3c05070c0aac87695bdf10ee99901f9f5bce1b02b887f4b9afc1680781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (173029078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65dc2ecf364a0976ac5ca0ef6ca7ae10a9ae95e141c0f1ff0315be291cf74dcf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:40:11 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Mar 2026 02:40:18 GMT
ENV KAPACITOR_VERSION=1.8.3
# Tue, 17 Mar 2026 02:40:18 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Mar 2026 02:40:18 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Mar 2026 02:40:18 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Mar 2026 02:40:18 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Mar 2026 02:40:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 02:40:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 02:40:18 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd31ed89fd7d59ba427c9f431e17b158ade8eb04083b8b256c587fc6521fb6b`  
		Last Modified: Tue, 17 Mar 2026 01:15:21 GMT  
		Size: 7.1 MB (7105152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bc0f9c00e2b6e662f7a920d9aef458bbe3eafcc22aba548c21ca3f3a19fb56`  
		Last Modified: Tue, 17 Mar 2026 02:40:39 GMT  
		Size: 50.7 MB (50667718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c760a46d606f2698a2328be4d6c542ab7a1e4edec24d4b8139422fb67ce369`  
		Last Modified: Tue, 17 Mar 2026 02:40:39 GMT  
		Size: 85.7 MB (85717164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9774290e0c67172532dccd10161b619445dc3a257405aea55585b6e5ca3c6224`  
		Last Modified: Tue, 17 Mar 2026 02:40:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acc4c6e25f0b3d98efc5276b357b424ae2f6da7e3f4d2c8368e71afc72fc921`  
		Last Modified: Tue, 17 Mar 2026 02:40:36 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:ebc70055a5cb05d6d6ef496b2aea990633cd87305668f95060870b10f00cb0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b52ab4a74dc29aacce403c2e2acda624b663ab551eed0968450bd1fbcb7355`

```dockerfile
```

-	Layers:
	-	`sha256:2ec3ec59580704e49c96146c8bb4ee65ce1e2e0f3303ef2a37aee13cca63fd49`  
		Last Modified: Tue, 17 Mar 2026 02:40:37 GMT  
		Size: 3.7 MB (3732026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bba61c02d13d363b8f33ead821f8ec2156a03478d4b68ec25295cd0938500636`  
		Last Modified: Tue, 17 Mar 2026 02:40:36 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:6af8187350bb795170c1fe7e4f87853fc11869a75101ca56f5e98acb66fcd612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163951015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9300188ac717d93bddd21409b598a1437595d957079e7dfe31266f0ced6dc689`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:44:20 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Mar 2026 02:44:27 GMT
ENV KAPACITOR_VERSION=1.8.3
# Tue, 17 Mar 2026 02:44:27 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Mar 2026 02:44:27 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Mar 2026 02:44:27 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Mar 2026 02:44:27 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Mar 2026 02:44:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 02:44:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 02:44:27 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6485dc332a06408f602b0cdb9b519fb93ef48ddb953b0ca66a482c8afa276f5e`  
		Last Modified: Tue, 17 Mar 2026 01:15:34 GMT  
		Size: 7.1 MB (7059209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2c68e5a146aa55ebc8b1a2ada5b4f240999c798eb271cf390848ef03a27dc0`  
		Last Modified: Tue, 17 Mar 2026 02:44:47 GMT  
		Size: 49.4 MB (49358453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ed7e0e3f6c7036ca6b8563037442db5e99f3105b176e9af26bc82dd8511aec`  
		Last Modified: Tue, 17 Mar 2026 02:44:48 GMT  
		Size: 80.1 MB (80143804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bde3905ca617547255712cf50cf70d78d5d7b12f049cf9cb1cfc0a06e91158`  
		Last Modified: Tue, 17 Mar 2026 02:44:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da277cd004014e3e122a67547ca53d23d882c721dbfc34e25e0df4d204175c4`  
		Last Modified: Tue, 17 Mar 2026 02:44:36 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:b418bb03b4234d4a8026742ce8672a144ba1ba5232f62bd4feafb4d826fb1f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d10ccd355326985d3f2a6af5dcda26904dbb5671fd0105813a54f64e74a006a`

```dockerfile
```

-	Layers:
	-	`sha256:5ea408d702716cc14d5144e339b9a2053f24b68030e705daf278d949ea4765ad`  
		Last Modified: Tue, 17 Mar 2026 02:44:45 GMT  
		Size: 3.7 MB (3731500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:973cd61ebc180c56813489bdf4ef61d2c374abad013a12e481590837cbd7b972`  
		Last Modified: Tue, 17 Mar 2026 02:44:45 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json
