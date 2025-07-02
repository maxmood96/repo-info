<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.6`](#kapacitor16)
-	[`kapacitor:1.6-alpine`](#kapacitor16-alpine)
-	[`kapacitor:1.6.6`](#kapacitor166)
-	[`kapacitor:1.6.6-alpine`](#kapacitor166-alpine)
-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.7`](#kapacitor177)
-	[`kapacitor:1.7.7-alpine`](#kapacitor177-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.6`

```console
$ docker pull kapacitor@sha256:cd63018df4fb1c0f5dfa334939f3a929475bede457007ec143fe6a0388a7c0f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:24f519bf6bf7fdfe0a835fdcaab9bb6aff8164660656cd037a33cfeb7129f908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146851030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9521969e6b0b7bbb7109e9087626aa097e88959d42d758ee59768d15b5d6cdc3`
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
ENV KAPACITOR_VERSION=1.6.6
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
	-	`sha256:1e633410ddb09991d96c811457febc0592b9cfc4b62ce26239adc6b4ca774d4d`  
		Last Modified: Wed, 02 Jul 2025 04:12:46 GMT  
		Size: 44.5 MB (44538691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbcec5ad76e60121e5858e7074ced40dc3c457aef82f4e9d987846eb64666d41`  
		Last Modified: Wed, 02 Jul 2025 04:12:46 GMT  
		Size: 65.7 MB (65672935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2140f27f3bd045bce9746d75b60d606b2cba3e53c7684db547560b6c71123e25`  
		Last Modified: Wed, 02 Jul 2025 04:12:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8efe4b985f2b50e26f6d77d91573a848c8f6d4d8ee4e0df33bc33b49d84cb40`  
		Last Modified: Wed, 02 Jul 2025 04:12:45 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:c15df3ce4d18a58df05945f34e08a17f9ba2176dfe754d8f9e65e3f8d93e5f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a78e0457879cd361c3186e49ac4672e646625f6a697678acdfede9075649886c`

```dockerfile
```

-	Layers:
	-	`sha256:e77a23db344dcf478e9e26487b0e953a1924c983d9e01af8ff684cc31d60303e`  
		Last Modified: Wed, 02 Jul 2025 07:21:17 GMT  
		Size: 3.7 MB (3708904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa99ce0313219f4b755c8faa128abb29217eeea4c49806e757864c1087fa53bf`  
		Last Modified: Wed, 02 Jul 2025 07:21:18 GMT  
		Size: 14.8 KB (14758 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:7b8faddbe0eb8e4af36009d4cdf2365a8d89e5e20eb14518d54944a9744cf1bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136883273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c879cdbe12ccbff8a1643db424e81266b365a5113de4fb043aeb8840969635`
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
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.6.6
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc8f9e3619942200ecbccd8a285496c9f5f75c9e60a1de3a2f4dc84b79a25af`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 7.0 MB (7049073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ede18b2697a9821a74a4c9c6fea26a7c6ee4ad8b8c5472833d6d9ffade1b45`  
		Last Modified: Tue, 03 Jun 2025 13:46:24 GMT  
		Size: 40.8 MB (40808035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a479b5d7c646b226e6841efe5650690bd67da18e32384c0476cc110e20ad714`  
		Last Modified: Tue, 03 Jun 2025 13:46:30 GMT  
		Size: 61.7 MB (61670127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6703cc342369ae6839d857c27b2867a92b067769ecaf52ab4066dc3d8113a6`  
		Last Modified: Tue, 03 Jun 2025 13:46:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78904dd66e481c2f587105f42fd43aff1568b6542da61e330c1040e8da9593d8`  
		Last Modified: Tue, 03 Jun 2025 13:46:29 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:e1ecd6d820b0f950a208895f149350170fcfa06dee002a4511b17d7ea58d3d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4002b473e154d1346ccea478ad6d919bda4a298ee040f3a8d813cc43105191dd`

```dockerfile
```

-	Layers:
	-	`sha256:4ae3ba52170199918fa8bd7fcc3ddf24f77d4e4eb2672ffd79040fdcc839b480`  
		Last Modified: Tue, 03 Jun 2025 17:35:14 GMT  
		Size: 3.6 MB (3574875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ca3e02b2866fb8797977a43dd24e114baafff0c128b139b136695b39d734596`  
		Last Modified: Tue, 03 Jun 2025 17:35:16 GMT  
		Size: 14.9 KB (14854 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6-alpine`

```console
$ docker pull kapacitor@sha256:eabd8acf11d549814eaca65a093747b22d7f056e8b8695ba6ba89ecb0eb368c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:acf95a57ee1bd5344bb08d22e94189d38735725f0d445a5e20e321975ac5824e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69502141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6c1556e33f80dbbeb72c104bd18352d9bfcef58d892e69e363d02cdf78f02a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 28 Oct 2024 16:40:55 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.6.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b7c4bcd6376f58b15fa52176845abf5128e2c9151d217518b4bc0dbae467c4`  
		Last Modified: Sat, 15 Feb 2025 00:26:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11769bb0f663d8458ef7ce2717f85df6f471c6a3e71503f4f42dc8b3a04edbde`  
		Last Modified: Sat, 15 Feb 2025 00:26:12 GMT  
		Size: 294.4 KB (294381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92cf72361b0dade2ad8c0daee300e7282d512572968ad88ad12a30a66ce40a`  
		Last Modified: Sat, 15 Feb 2025 00:26:15 GMT  
		Size: 65.6 MB (65580130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec75cc769591ab3223bacd6530eb8ec0a52abaa396705ca766e48998fa8ab5e3`  
		Last Modified: Sat, 15 Feb 2025 00:26:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce9bbc84973835a4410eb3dbe59f08279662eccd66fa3d75c37d98ee926b949`  
		Last Modified: Sat, 15 Feb 2025 00:26:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:96a7504fd082256e9460b4656393509609395679ca29ee244ef0616f5af19565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.4 KB (373441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc92318d6da0674edbeb7f030464518d1c466d4ceb96293a271417108654e6e`

```dockerfile
```

-	Layers:
	-	`sha256:12a7f472e13033d632c5cdb7aab55ab918a7bee2548ea56b8469b34b12a37bf3`  
		Last Modified: Fri, 14 Feb 2025 23:21:16 GMT  
		Size: 358.7 KB (358678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae98ee822f327180c826fe1fbbf733f6098cdc27f8b4684d23c7a6d8bb116831`  
		Last Modified: Fri, 14 Feb 2025 23:21:16 GMT  
		Size: 14.8 KB (14763 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6.6`

```console
$ docker pull kapacitor@sha256:cd63018df4fb1c0f5dfa334939f3a929475bede457007ec143fe6a0388a7c0f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.6.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:24f519bf6bf7fdfe0a835fdcaab9bb6aff8164660656cd037a33cfeb7129f908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146851030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9521969e6b0b7bbb7109e9087626aa097e88959d42d758ee59768d15b5d6cdc3`
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
ENV KAPACITOR_VERSION=1.6.6
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
	-	`sha256:1e633410ddb09991d96c811457febc0592b9cfc4b62ce26239adc6b4ca774d4d`  
		Last Modified: Wed, 02 Jul 2025 04:12:46 GMT  
		Size: 44.5 MB (44538691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbcec5ad76e60121e5858e7074ced40dc3c457aef82f4e9d987846eb64666d41`  
		Last Modified: Wed, 02 Jul 2025 04:12:46 GMT  
		Size: 65.7 MB (65672935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2140f27f3bd045bce9746d75b60d606b2cba3e53c7684db547560b6c71123e25`  
		Last Modified: Wed, 02 Jul 2025 04:12:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8efe4b985f2b50e26f6d77d91573a848c8f6d4d8ee4e0df33bc33b49d84cb40`  
		Last Modified: Wed, 02 Jul 2025 04:12:45 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:c15df3ce4d18a58df05945f34e08a17f9ba2176dfe754d8f9e65e3f8d93e5f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a78e0457879cd361c3186e49ac4672e646625f6a697678acdfede9075649886c`

```dockerfile
```

-	Layers:
	-	`sha256:e77a23db344dcf478e9e26487b0e953a1924c983d9e01af8ff684cc31d60303e`  
		Last Modified: Wed, 02 Jul 2025 07:21:17 GMT  
		Size: 3.7 MB (3708904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa99ce0313219f4b755c8faa128abb29217eeea4c49806e757864c1087fa53bf`  
		Last Modified: Wed, 02 Jul 2025 07:21:18 GMT  
		Size: 14.8 KB (14758 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.6.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:7b8faddbe0eb8e4af36009d4cdf2365a8d89e5e20eb14518d54944a9744cf1bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136883273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c879cdbe12ccbff8a1643db424e81266b365a5113de4fb043aeb8840969635`
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
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.6.6
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc8f9e3619942200ecbccd8a285496c9f5f75c9e60a1de3a2f4dc84b79a25af`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 7.0 MB (7049073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ede18b2697a9821a74a4c9c6fea26a7c6ee4ad8b8c5472833d6d9ffade1b45`  
		Last Modified: Tue, 03 Jun 2025 13:46:24 GMT  
		Size: 40.8 MB (40808035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a479b5d7c646b226e6841efe5650690bd67da18e32384c0476cc110e20ad714`  
		Last Modified: Tue, 03 Jun 2025 13:46:30 GMT  
		Size: 61.7 MB (61670127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6703cc342369ae6839d857c27b2867a92b067769ecaf52ab4066dc3d8113a6`  
		Last Modified: Tue, 03 Jun 2025 13:46:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78904dd66e481c2f587105f42fd43aff1568b6542da61e330c1040e8da9593d8`  
		Last Modified: Tue, 03 Jun 2025 13:46:29 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:e1ecd6d820b0f950a208895f149350170fcfa06dee002a4511b17d7ea58d3d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4002b473e154d1346ccea478ad6d919bda4a298ee040f3a8d813cc43105191dd`

```dockerfile
```

-	Layers:
	-	`sha256:4ae3ba52170199918fa8bd7fcc3ddf24f77d4e4eb2672ffd79040fdcc839b480`  
		Last Modified: Tue, 03 Jun 2025 17:35:14 GMT  
		Size: 3.6 MB (3574875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ca3e02b2866fb8797977a43dd24e114baafff0c128b139b136695b39d734596`  
		Last Modified: Tue, 03 Jun 2025 17:35:16 GMT  
		Size: 14.9 KB (14854 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6.6-alpine`

```console
$ docker pull kapacitor@sha256:eabd8acf11d549814eaca65a093747b22d7f056e8b8695ba6ba89ecb0eb368c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.6.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:acf95a57ee1bd5344bb08d22e94189d38735725f0d445a5e20e321975ac5824e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69502141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6c1556e33f80dbbeb72c104bd18352d9bfcef58d892e69e363d02cdf78f02a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 28 Oct 2024 16:40:55 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.6.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b7c4bcd6376f58b15fa52176845abf5128e2c9151d217518b4bc0dbae467c4`  
		Last Modified: Sat, 15 Feb 2025 00:26:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11769bb0f663d8458ef7ce2717f85df6f471c6a3e71503f4f42dc8b3a04edbde`  
		Last Modified: Sat, 15 Feb 2025 00:26:12 GMT  
		Size: 294.4 KB (294381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92cf72361b0dade2ad8c0daee300e7282d512572968ad88ad12a30a66ce40a`  
		Last Modified: Sat, 15 Feb 2025 00:26:15 GMT  
		Size: 65.6 MB (65580130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec75cc769591ab3223bacd6530eb8ec0a52abaa396705ca766e48998fa8ab5e3`  
		Last Modified: Sat, 15 Feb 2025 00:26:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce9bbc84973835a4410eb3dbe59f08279662eccd66fa3d75c37d98ee926b949`  
		Last Modified: Sat, 15 Feb 2025 00:26:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:96a7504fd082256e9460b4656393509609395679ca29ee244ef0616f5af19565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.4 KB (373441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc92318d6da0674edbeb7f030464518d1c466d4ceb96293a271417108654e6e`

```dockerfile
```

-	Layers:
	-	`sha256:12a7f472e13033d632c5cdb7aab55ab918a7bee2548ea56b8469b34b12a37bf3`  
		Last Modified: Fri, 14 Feb 2025 23:21:16 GMT  
		Size: 358.7 KB (358678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae98ee822f327180c826fe1fbbf733f6098cdc27f8b4684d23c7a6d8bb116831`  
		Last Modified: Fri, 14 Feb 2025 23:21:16 GMT  
		Size: 14.8 KB (14763 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7`

```console
$ docker pull kapacitor@sha256:1cd28615f3d04f9ff8bea6d07e2057f399be4a4982c0014ea43ed9a5733598e3
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
$ docker pull kapacitor@sha256:16febdb45d0695cccea4a2a632b3358fe899e4b846e7712916ef12c558dc202c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143026939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a526adfc4f22f57028fff9728cd0b6a5485113436c8499041e713af40e742e`
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
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc8f9e3619942200ecbccd8a285496c9f5f75c9e60a1de3a2f4dc84b79a25af`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 7.0 MB (7049073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ede18b2697a9821a74a4c9c6fea26a7c6ee4ad8b8c5472833d6d9ffade1b45`  
		Last Modified: Tue, 03 Jun 2025 13:46:24 GMT  
		Size: 40.8 MB (40808035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e4792fa6ad5d81b9c30cb67436ab23b852ce06e05b289e1107fd1342f23c37`  
		Last Modified: Thu, 05 Jun 2025 04:38:19 GMT  
		Size: 67.8 MB (67813728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4990d453161f11fbc333be5ac6267e7e95f969c8f3be4dfd124ec0d1ea86e13d`  
		Last Modified: Tue, 03 Jun 2025 21:05:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc78a4f7e13158073f7489833bff5466dc9983fec345090b73d3b62bbd7853ee`  
		Last Modified: Tue, 03 Jun 2025 21:05:32 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:9c3d763d08a3d9732e9edb0d0c51e9e2959eb40131b18eb9b3902d9a39265185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3597312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9763e1204134e20d5be1de1eff9a73f922585bb89c04c89574886317c9657ad`

```dockerfile
```

-	Layers:
	-	`sha256:648dc42e3187f17d4518d03ab5878b6d481f5bf89b6bdb6a266a4b5ccbade699`  
		Last Modified: Mon, 09 Jun 2025 17:40:10 GMT  
		Size: 3.6 MB (3582142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90292be3ad63d09b3de03ed6f0f0f74815563a66e9112ae385de5847ba1c4354`  
		Last Modified: Mon, 09 Jun 2025 17:40:09 GMT  
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
$ docker pull kapacitor@sha256:1cd28615f3d04f9ff8bea6d07e2057f399be4a4982c0014ea43ed9a5733598e3
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
$ docker pull kapacitor@sha256:16febdb45d0695cccea4a2a632b3358fe899e4b846e7712916ef12c558dc202c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143026939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a526adfc4f22f57028fff9728cd0b6a5485113436c8499041e713af40e742e`
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
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc8f9e3619942200ecbccd8a285496c9f5f75c9e60a1de3a2f4dc84b79a25af`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 7.0 MB (7049073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ede18b2697a9821a74a4c9c6fea26a7c6ee4ad8b8c5472833d6d9ffade1b45`  
		Last Modified: Tue, 03 Jun 2025 13:46:24 GMT  
		Size: 40.8 MB (40808035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e4792fa6ad5d81b9c30cb67436ab23b852ce06e05b289e1107fd1342f23c37`  
		Last Modified: Thu, 05 Jun 2025 04:38:19 GMT  
		Size: 67.8 MB (67813728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4990d453161f11fbc333be5ac6267e7e95f969c8f3be4dfd124ec0d1ea86e13d`  
		Last Modified: Tue, 03 Jun 2025 21:05:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc78a4f7e13158073f7489833bff5466dc9983fec345090b73d3b62bbd7853ee`  
		Last Modified: Tue, 03 Jun 2025 21:05:32 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:9c3d763d08a3d9732e9edb0d0c51e9e2959eb40131b18eb9b3902d9a39265185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3597312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9763e1204134e20d5be1de1eff9a73f922585bb89c04c89574886317c9657ad`

```dockerfile
```

-	Layers:
	-	`sha256:648dc42e3187f17d4518d03ab5878b6d481f5bf89b6bdb6a266a4b5ccbade699`  
		Last Modified: Mon, 09 Jun 2025 17:40:10 GMT  
		Size: 3.6 MB (3582142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90292be3ad63d09b3de03ed6f0f0f74815563a66e9112ae385de5847ba1c4354`  
		Last Modified: Mon, 09 Jun 2025 17:40:09 GMT  
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
$ docker pull kapacitor@sha256:1cd28615f3d04f9ff8bea6d07e2057f399be4a4982c0014ea43ed9a5733598e3
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
$ docker pull kapacitor@sha256:16febdb45d0695cccea4a2a632b3358fe899e4b846e7712916ef12c558dc202c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143026939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a526adfc4f22f57028fff9728cd0b6a5485113436c8499041e713af40e742e`
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
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc8f9e3619942200ecbccd8a285496c9f5f75c9e60a1de3a2f4dc84b79a25af`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 7.0 MB (7049073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ede18b2697a9821a74a4c9c6fea26a7c6ee4ad8b8c5472833d6d9ffade1b45`  
		Last Modified: Tue, 03 Jun 2025 13:46:24 GMT  
		Size: 40.8 MB (40808035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e4792fa6ad5d81b9c30cb67436ab23b852ce06e05b289e1107fd1342f23c37`  
		Last Modified: Thu, 05 Jun 2025 04:38:19 GMT  
		Size: 67.8 MB (67813728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4990d453161f11fbc333be5ac6267e7e95f969c8f3be4dfd124ec0d1ea86e13d`  
		Last Modified: Tue, 03 Jun 2025 21:05:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc78a4f7e13158073f7489833bff5466dc9983fec345090b73d3b62bbd7853ee`  
		Last Modified: Tue, 03 Jun 2025 21:05:32 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:9c3d763d08a3d9732e9edb0d0c51e9e2959eb40131b18eb9b3902d9a39265185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3597312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9763e1204134e20d5be1de1eff9a73f922585bb89c04c89574886317c9657ad`

```dockerfile
```

-	Layers:
	-	`sha256:648dc42e3187f17d4518d03ab5878b6d481f5bf89b6bdb6a266a4b5ccbade699`  
		Last Modified: Mon, 09 Jun 2025 17:40:10 GMT  
		Size: 3.6 MB (3582142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90292be3ad63d09b3de03ed6f0f0f74815563a66e9112ae385de5847ba1c4354`  
		Last Modified: Mon, 09 Jun 2025 17:40:09 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json
