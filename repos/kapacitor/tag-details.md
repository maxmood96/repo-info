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
$ docker pull kapacitor@sha256:ffbe920e1fdc20e109feedb355c136ac8677591a24e3163d8160e658e8243f3f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:54146bc5230851492d2dfd33992f638e19e6bf08bba05776e0e9c7b20c90f2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154338088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590ed61f622b06d6a118e84959e2a25b91adc0df51b9b9d9d6b99fec32eb87d0`
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
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.7.7
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
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1718e536deb534924f0e24d75c0ad8cbe941526cffc1ff3ec1e0d1c6ec3f68`  
		Last Modified: Tue, 12 Aug 2025 17:23:37 GMT  
		Size: 7.1 MB (7106301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e1c0c39fe978a6726430a7c9f81d5fd2555f921b900bae9e810d14fb309883`  
		Last Modified: Tue, 12 Aug 2025 18:33:49 GMT  
		Size: 45.6 MB (45643199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7444eb66c3b33f94a04e0d8bac884eae197a2ba575a75bffb8a6fd6033eea42`  
		Last Modified: Tue, 12 Aug 2025 18:33:53 GMT  
		Size: 72.1 MB (72051072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802175a844b7789e2e76d898003184e818b232abf982fc446f0252c4c869338a`  
		Last Modified: Tue, 12 Aug 2025 18:33:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f021ed19c93a27e7be7facbe75792e9c3c08ec108b681b87f4c1b01dee2735d`  
		Last Modified: Tue, 12 Aug 2025 18:33:43 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:a26e50cba0464052fa1b16817f92440bc80a629af28a70fdb653cd354061af56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e5fb3800ba6d1f5e7cd1a26febe5fd5d18c2eea73c689430ab607f72e6d9f`

```dockerfile
```

-	Layers:
	-	`sha256:d6e7eccdeef70a26269ff078f5fe89122fe156abff2dfea9a692b0b9505cf7dd`  
		Last Modified: Tue, 12 Aug 2025 19:21:18 GMT  
		Size: 3.7 MB (3716660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d503b322d2f9c60ea1ac06b15db6867ec0f86105a755715b6ef85ab4bb15409`  
		Last Modified: Tue, 12 Aug 2025 19:21:19 GMT  
		Size: 14.8 KB (14759 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:d946ceb5d2b6b8d5552b349f792f9d9c4535c5ba8f2b6871004f46d69a6984f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145372867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3f44f4a208e1bcc4416907d7cd7601efa543207a84ae04cb6fa4804671ad57`
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
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.7.7
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
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476a9430580cac739e29f524f2d4fa032c5bfb4d16c97a34238459efc663af4e`  
		Last Modified: Tue, 12 Aug 2025 17:24:37 GMT  
		Size: 7.1 MB (7051909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2e62eaf5273f9309d0110fd3120778a77557e5aa2a49de27595f55ec44f2d7`  
		Last Modified: Wed, 13 Aug 2025 01:24:27 GMT  
		Size: 43.1 MB (43147465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1125961f24472ab6a86af3a51a2c72fdf178c78b78f298d98ca36c8342beb8`  
		Last Modified: Wed, 13 Aug 2025 01:24:35 GMT  
		Size: 67.8 MB (67813723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1616243e97aa3863a0589b1bec272b924c2ccd7dd65dc7ca4ede9d179536495`  
		Last Modified: Tue, 12 Aug 2025 23:39:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9dbc6ad85250949431a2c7cced7999a716babfe88df2c37d9170bddd56e76e`  
		Last Modified: Tue, 12 Aug 2025 23:40:02 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:92dc287505e3efcafbcde234d46df9c5352bf8e5e94b9d4bf2a0eb579d08caff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0679d991f76cc30593bd3a9d5a1e8b0c187a978c055768e8d23cdd72777cee63`

```dockerfile
```

-	Layers:
	-	`sha256:8ccc3b90a562a8b9b8e6d25daee5f6d27627be485cd2ce1c4474c7fc13366561`  
		Last Modified: Wed, 13 Aug 2025 01:21:20 GMT  
		Size: 3.7 MB (3716122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8895c161a1ad38888c65ef764bf3911f33036e240d1260f7572e7cc3f834e177`  
		Last Modified: Wed, 13 Aug 2025 01:21:21 GMT  
		Size: 14.9 KB (14854 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:4a740c633b90375fc4613465ead786b393b1106ff2a748d895d51967f5c8eb55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:495481bc51bb09cd677a387761815568fac2fdf0165b74652e05308d252fc673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75887885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e6e758f84077ab7831577cf3aa0a3c1ee4fae198f9eee13120886d468b4d5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 08 Jul 2025 13:10:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.7.7
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
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7cd59a170b5fff4759056f3021cd3a0f8b8b93fd86f3b540f889da699918c6`  
		Last Modified: Tue, 15 Jul 2025 20:46:46 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a6ffa563fb7d136af9cbd8379cf5ceacbf2926fadcd8e281c43b0cd52cb334`  
		Last Modified: Wed, 16 Jul 2025 06:05:34 GMT  
		Size: 283.8 KB (283794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd34a060f527e5af8a18b24cf3308e10ffd9c472cc20593e106f406d6efe7f1`  
		Last Modified: Wed, 16 Jul 2025 08:14:17 GMT  
		Size: 72.0 MB (71982834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b96d9ad903da395c8acc30237a367d0349015a659efa7b235443f051909f89`  
		Last Modified: Wed, 16 Jul 2025 05:59:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cba525bdf0c3a03182ebbbf50f501d2ad26bdbb63fb2e4bd01963a644155449`  
		Last Modified: Wed, 16 Jul 2025 05:59:25 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:2f1b54a2048c3a3b338544b0c408b33dd54dbc449f63a8dbde7990f697a68a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 KB (379593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf0662c60fc4bc189a7c968c0a97009e090f806295b18433651f515500f4bd1`

```dockerfile
```

-	Layers:
	-	`sha256:7129167326340ece8825cd0b82133d5059b3bceaaa807a7903b1c31ce09f5e9d`  
		Last Modified: Tue, 15 Jul 2025 22:21:18 GMT  
		Size: 363.9 KB (363909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e7c0e7967c42b262e03d986132f124a458856a89945a10b72681d79a9d610c`  
		Last Modified: Tue, 15 Jul 2025 22:21:19 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.7`

```console
$ docker pull kapacitor@sha256:ffbe920e1fdc20e109feedb355c136ac8677591a24e3163d8160e658e8243f3f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:54146bc5230851492d2dfd33992f638e19e6bf08bba05776e0e9c7b20c90f2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154338088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590ed61f622b06d6a118e84959e2a25b91adc0df51b9b9d9d6b99fec32eb87d0`
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
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.7.7
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
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1718e536deb534924f0e24d75c0ad8cbe941526cffc1ff3ec1e0d1c6ec3f68`  
		Last Modified: Tue, 12 Aug 2025 17:23:37 GMT  
		Size: 7.1 MB (7106301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e1c0c39fe978a6726430a7c9f81d5fd2555f921b900bae9e810d14fb309883`  
		Last Modified: Tue, 12 Aug 2025 18:33:49 GMT  
		Size: 45.6 MB (45643199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7444eb66c3b33f94a04e0d8bac884eae197a2ba575a75bffb8a6fd6033eea42`  
		Last Modified: Tue, 12 Aug 2025 18:33:53 GMT  
		Size: 72.1 MB (72051072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802175a844b7789e2e76d898003184e818b232abf982fc446f0252c4c869338a`  
		Last Modified: Tue, 12 Aug 2025 18:33:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f021ed19c93a27e7be7facbe75792e9c3c08ec108b681b87f4c1b01dee2735d`  
		Last Modified: Tue, 12 Aug 2025 18:33:43 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:a26e50cba0464052fa1b16817f92440bc80a629af28a70fdb653cd354061af56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e5fb3800ba6d1f5e7cd1a26febe5fd5d18c2eea73c689430ab607f72e6d9f`

```dockerfile
```

-	Layers:
	-	`sha256:d6e7eccdeef70a26269ff078f5fe89122fe156abff2dfea9a692b0b9505cf7dd`  
		Last Modified: Tue, 12 Aug 2025 19:21:18 GMT  
		Size: 3.7 MB (3716660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d503b322d2f9c60ea1ac06b15db6867ec0f86105a755715b6ef85ab4bb15409`  
		Last Modified: Tue, 12 Aug 2025 19:21:19 GMT  
		Size: 14.8 KB (14759 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:d946ceb5d2b6b8d5552b349f792f9d9c4535c5ba8f2b6871004f46d69a6984f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145372867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3f44f4a208e1bcc4416907d7cd7601efa543207a84ae04cb6fa4804671ad57`
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
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.7.7
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
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476a9430580cac739e29f524f2d4fa032c5bfb4d16c97a34238459efc663af4e`  
		Last Modified: Tue, 12 Aug 2025 17:24:37 GMT  
		Size: 7.1 MB (7051909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2e62eaf5273f9309d0110fd3120778a77557e5aa2a49de27595f55ec44f2d7`  
		Last Modified: Wed, 13 Aug 2025 01:24:27 GMT  
		Size: 43.1 MB (43147465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1125961f24472ab6a86af3a51a2c72fdf178c78b78f298d98ca36c8342beb8`  
		Last Modified: Wed, 13 Aug 2025 01:24:35 GMT  
		Size: 67.8 MB (67813723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1616243e97aa3863a0589b1bec272b924c2ccd7dd65dc7ca4ede9d179536495`  
		Last Modified: Tue, 12 Aug 2025 23:39:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9dbc6ad85250949431a2c7cced7999a716babfe88df2c37d9170bddd56e76e`  
		Last Modified: Tue, 12 Aug 2025 23:40:02 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:92dc287505e3efcafbcde234d46df9c5352bf8e5e94b9d4bf2a0eb579d08caff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0679d991f76cc30593bd3a9d5a1e8b0c187a978c055768e8d23cdd72777cee63`

```dockerfile
```

-	Layers:
	-	`sha256:8ccc3b90a562a8b9b8e6d25daee5f6d27627be485cd2ce1c4474c7fc13366561`  
		Last Modified: Wed, 13 Aug 2025 01:21:20 GMT  
		Size: 3.7 MB (3716122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8895c161a1ad38888c65ef764bf3911f33036e240d1260f7572e7cc3f834e177`  
		Last Modified: Wed, 13 Aug 2025 01:21:21 GMT  
		Size: 14.9 KB (14854 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.7-alpine`

```console
$ docker pull kapacitor@sha256:4a740c633b90375fc4613465ead786b393b1106ff2a748d895d51967f5c8eb55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:495481bc51bb09cd677a387761815568fac2fdf0165b74652e05308d252fc673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75887885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e6e758f84077ab7831577cf3aa0a3c1ee4fae198f9eee13120886d468b4d5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 08 Jul 2025 13:10:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.7.7
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
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7cd59a170b5fff4759056f3021cd3a0f8b8b93fd86f3b540f889da699918c6`  
		Last Modified: Tue, 15 Jul 2025 20:46:46 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a6ffa563fb7d136af9cbd8379cf5ceacbf2926fadcd8e281c43b0cd52cb334`  
		Last Modified: Wed, 16 Jul 2025 06:05:34 GMT  
		Size: 283.8 KB (283794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd34a060f527e5af8a18b24cf3308e10ffd9c472cc20593e106f406d6efe7f1`  
		Last Modified: Wed, 16 Jul 2025 08:14:17 GMT  
		Size: 72.0 MB (71982834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b96d9ad903da395c8acc30237a367d0349015a659efa7b235443f051909f89`  
		Last Modified: Wed, 16 Jul 2025 05:59:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cba525bdf0c3a03182ebbbf50f501d2ad26bdbb63fb2e4bd01963a644155449`  
		Last Modified: Wed, 16 Jul 2025 05:59:25 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:2f1b54a2048c3a3b338544b0c408b33dd54dbc449f63a8dbde7990f697a68a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 KB (379593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf0662c60fc4bc189a7c968c0a97009e090f806295b18433651f515500f4bd1`

```dockerfile
```

-	Layers:
	-	`sha256:7129167326340ece8825cd0b82133d5059b3bceaaa807a7903b1c31ce09f5e9d`  
		Last Modified: Tue, 15 Jul 2025 22:21:18 GMT  
		Size: 363.9 KB (363909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e7c0e7967c42b262e03d986132f124a458856a89945a10b72681d79a9d610c`  
		Last Modified: Tue, 15 Jul 2025 22:21:19 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8`

```console
$ docker pull kapacitor@sha256:2cc6de2e799cbe1012b0da297de4a508a380d2e4afff2bc2eb3c2537074dc306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8` - linux; amd64

```console
$ docker pull kapacitor@sha256:e14a1a081c6e90e9b6994d2c28fe16afc881c35a01e8a8226f798225e69d98a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169653283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9362a79edf5995c9f05c55fdeaf660052d39f9b23214fcaf53ca545a5e964839`
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
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
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
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1718e536deb534924f0e24d75c0ad8cbe941526cffc1ff3ec1e0d1c6ec3f68`  
		Last Modified: Tue, 12 Aug 2025 17:23:37 GMT  
		Size: 7.1 MB (7106301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a40004787fb09ea05e7f72892df1c2b554e1ae05bf36d5ee6c86cf3f0349201`  
		Last Modified: Tue, 12 Aug 2025 18:33:53 GMT  
		Size: 45.6 MB (45643206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ed28f150dec03899d9b84c9b6b388c9963f54122c90b38bdc525f958613faa`  
		Last Modified: Tue, 12 Aug 2025 18:33:53 GMT  
		Size: 87.4 MB (87366262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8dec99a0cb2712d15b2f593cb84fdfaff562469bec38c7668546d9f0e71dfe`  
		Last Modified: Tue, 12 Aug 2025 18:33:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdd0230f3ac689129a3409637bf0e4543421b1689fc65fa3a9a8859cce29397`  
		Last Modified: Tue, 12 Aug 2025 18:33:47 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:0081a8bf7976870890c91bcbdb4395ec2e878305cc4739e72e0d94eff828ca96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173bf62902807b8d110e202a6de203ae6a0a8a68bcf9fe1c49fcf7ebde6a7a27`

```dockerfile
```

-	Layers:
	-	`sha256:827290ae5bb73a0229370187641487e9b070bcdb20a667342b4b4a6a80ec3b41`  
		Last Modified: Tue, 12 Aug 2025 19:21:27 GMT  
		Size: 3.7 MB (3731253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3c503667dd479af4a224b216ff20361d90611461a8b5b1006894f188c0ad0f1`  
		Last Modified: Tue, 12 Aug 2025 19:21:27 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:46cf79ad0f89fe2687bf1acf59cffb7b441ba07de25b182d92d31b5431661190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159022868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5000def53d67cb759c435f8cc5cb1e26363bd7c4259d26dab4c1a70a26a841a`
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
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
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
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476a9430580cac739e29f524f2d4fa032c5bfb4d16c97a34238459efc663af4e`  
		Last Modified: Tue, 12 Aug 2025 17:24:37 GMT  
		Size: 7.1 MB (7051909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2e62eaf5273f9309d0110fd3120778a77557e5aa2a49de27595f55ec44f2d7`  
		Last Modified: Wed, 13 Aug 2025 01:24:27 GMT  
		Size: 43.1 MB (43147465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b364ad99c784d84f60ae66ff3cdd21f20c030193b0c0b0af2895b3e0d9b35c9e`  
		Last Modified: Wed, 13 Aug 2025 17:26:11 GMT  
		Size: 81.5 MB (81463725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8912af52b80bd0db4ff2b6a51d9dbaab0894cf46c5643ad3fde44abb25506227`  
		Last Modified: Tue, 12 Aug 2025 23:39:52 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972ce250eaa6760f24d454e096fdb6d3a90403816a740376563e03a0eb4b9551`  
		Last Modified: Tue, 12 Aug 2025 23:39:55 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:4a6cfebe7936fac5c6b97373033c597d080f60c1db0de2c0499fb6f5da34b8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235cd7f1bcbe49cac80ccf74839f903b9e0f20810ddb7a19ea1cecb6863a4aec`

```dockerfile
```

-	Layers:
	-	`sha256:b7cb9d0ca0e96b8909bdfbe958ac467d13bb6353dc514fb639d4433f726a767a`  
		Last Modified: Wed, 13 Aug 2025 01:21:28 GMT  
		Size: 3.7 MB (3730727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2f331b1f233cd78e7f048bc860290261080c2374350c15561202d4dd58fb7cb`  
		Last Modified: Wed, 13 Aug 2025 01:21:29 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8-alpine`

```console
$ docker pull kapacitor@sha256:2825d7196fb304f3a04865fc4dec75870843bc4764300d6fde593d329478e7b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:4743478781d2a7c047ad95226eba4024a3de6d4d64c0bd967ec116be3343e643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91400915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4fa050f17c04c7e0f84978129ab42af6e09dd33d65b3b32f2277fb18a8c835`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 08 Jul 2025 13:10:35 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38e79fd324639f0fb04fac74b91a3fdd03f987bf17d22bf2e2f9e8fad895cd1`  
		Last Modified: Tue, 15 Jul 2025 19:27:45 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235c4218322a4624970ccfa65b12c9ddad2435ac444b450a39dc418785c8bc68`  
		Last Modified: Tue, 15 Jul 2025 19:27:45 GMT  
		Size: 305.9 KB (305883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cd64a5b29e44b24472bd128a39c6b4cc1cc22d52e52e98d7ea1ce6468da965`  
		Last Modified: Tue, 15 Jul 2025 19:27:56 GMT  
		Size: 87.3 MB (87294543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc02c4b7af262620386fceaf1713b9e5849367fdcf1f5991f1e09c9426cceaf8`  
		Last Modified: Tue, 15 Jul 2025 19:27:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2132b1ef163276aa1d02da1827290d21bf76105bd972ebec937d0055ccf86c2`  
		Last Modified: Tue, 15 Jul 2025 19:27:46 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:958bb89f875d5bd08234cdab7e8380cda7dc4eea714aa5dd2163fd3464a49c22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.7 KB (403682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb6e26545a47362444044a81a947549427a112135537a3a393226508b9d00f8`

```dockerfile
```

-	Layers:
	-	`sha256:da8d3e8bf8525002c6b07e29f473dad97c32ab76bc541156db43124ee078d3bf`  
		Last Modified: Tue, 15 Jul 2025 22:21:23 GMT  
		Size: 388.3 KB (388303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12fea95b71b3d4b8fc770dfe58e742da102df6dba1beb0c4f901e5b944b97a3`  
		Last Modified: Tue, 15 Jul 2025 22:21:24 GMT  
		Size: 15.4 KB (15379 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.0`

```console
$ docker pull kapacitor@sha256:2cc6de2e799cbe1012b0da297de4a508a380d2e4afff2bc2eb3c2537074dc306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8.0` - linux; amd64

```console
$ docker pull kapacitor@sha256:e14a1a081c6e90e9b6994d2c28fe16afc881c35a01e8a8226f798225e69d98a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169653283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9362a79edf5995c9f05c55fdeaf660052d39f9b23214fcaf53ca545a5e964839`
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
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
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
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1718e536deb534924f0e24d75c0ad8cbe941526cffc1ff3ec1e0d1c6ec3f68`  
		Last Modified: Tue, 12 Aug 2025 17:23:37 GMT  
		Size: 7.1 MB (7106301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a40004787fb09ea05e7f72892df1c2b554e1ae05bf36d5ee6c86cf3f0349201`  
		Last Modified: Tue, 12 Aug 2025 18:33:53 GMT  
		Size: 45.6 MB (45643206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ed28f150dec03899d9b84c9b6b388c9963f54122c90b38bdc525f958613faa`  
		Last Modified: Tue, 12 Aug 2025 18:33:53 GMT  
		Size: 87.4 MB (87366262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8dec99a0cb2712d15b2f593cb84fdfaff562469bec38c7668546d9f0e71dfe`  
		Last Modified: Tue, 12 Aug 2025 18:33:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdd0230f3ac689129a3409637bf0e4543421b1689fc65fa3a9a8859cce29397`  
		Last Modified: Tue, 12 Aug 2025 18:33:47 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.0` - unknown; unknown

```console
$ docker pull kapacitor@sha256:0081a8bf7976870890c91bcbdb4395ec2e878305cc4739e72e0d94eff828ca96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173bf62902807b8d110e202a6de203ae6a0a8a68bcf9fe1c49fcf7ebde6a7a27`

```dockerfile
```

-	Layers:
	-	`sha256:827290ae5bb73a0229370187641487e9b070bcdb20a667342b4b4a6a80ec3b41`  
		Last Modified: Tue, 12 Aug 2025 19:21:27 GMT  
		Size: 3.7 MB (3731253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3c503667dd479af4a224b216ff20361d90611461a8b5b1006894f188c0ad0f1`  
		Last Modified: Tue, 12 Aug 2025 19:21:27 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8.0` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:46cf79ad0f89fe2687bf1acf59cffb7b441ba07de25b182d92d31b5431661190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159022868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5000def53d67cb759c435f8cc5cb1e26363bd7c4259d26dab4c1a70a26a841a`
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
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
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
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476a9430580cac739e29f524f2d4fa032c5bfb4d16c97a34238459efc663af4e`  
		Last Modified: Tue, 12 Aug 2025 17:24:37 GMT  
		Size: 7.1 MB (7051909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2e62eaf5273f9309d0110fd3120778a77557e5aa2a49de27595f55ec44f2d7`  
		Last Modified: Wed, 13 Aug 2025 01:24:27 GMT  
		Size: 43.1 MB (43147465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b364ad99c784d84f60ae66ff3cdd21f20c030193b0c0b0af2895b3e0d9b35c9e`  
		Last Modified: Wed, 13 Aug 2025 17:26:11 GMT  
		Size: 81.5 MB (81463725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8912af52b80bd0db4ff2b6a51d9dbaab0894cf46c5643ad3fde44abb25506227`  
		Last Modified: Tue, 12 Aug 2025 23:39:52 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972ce250eaa6760f24d454e096fdb6d3a90403816a740376563e03a0eb4b9551`  
		Last Modified: Tue, 12 Aug 2025 23:39:55 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.0` - unknown; unknown

```console
$ docker pull kapacitor@sha256:4a6cfebe7936fac5c6b97373033c597d080f60c1db0de2c0499fb6f5da34b8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235cd7f1bcbe49cac80ccf74839f903b9e0f20810ddb7a19ea1cecb6863a4aec`

```dockerfile
```

-	Layers:
	-	`sha256:b7cb9d0ca0e96b8909bdfbe958ac467d13bb6353dc514fb639d4433f726a767a`  
		Last Modified: Wed, 13 Aug 2025 01:21:28 GMT  
		Size: 3.7 MB (3730727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2f331b1f233cd78e7f048bc860290261080c2374350c15561202d4dd58fb7cb`  
		Last Modified: Wed, 13 Aug 2025 01:21:29 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.0-alpine`

```console
$ docker pull kapacitor@sha256:2825d7196fb304f3a04865fc4dec75870843bc4764300d6fde593d329478e7b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8.0-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:4743478781d2a7c047ad95226eba4024a3de6d4d64c0bd967ec116be3343e643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91400915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4fa050f17c04c7e0f84978129ab42af6e09dd33d65b3b32f2277fb18a8c835`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 08 Jul 2025 13:10:35 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38e79fd324639f0fb04fac74b91a3fdd03f987bf17d22bf2e2f9e8fad895cd1`  
		Last Modified: Tue, 15 Jul 2025 19:27:45 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235c4218322a4624970ccfa65b12c9ddad2435ac444b450a39dc418785c8bc68`  
		Last Modified: Tue, 15 Jul 2025 19:27:45 GMT  
		Size: 305.9 KB (305883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cd64a5b29e44b24472bd128a39c6b4cc1cc22d52e52e98d7ea1ce6468da965`  
		Last Modified: Tue, 15 Jul 2025 19:27:56 GMT  
		Size: 87.3 MB (87294543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc02c4b7af262620386fceaf1713b9e5849367fdcf1f5991f1e09c9426cceaf8`  
		Last Modified: Tue, 15 Jul 2025 19:27:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2132b1ef163276aa1d02da1827290d21bf76105bd972ebec937d0055ccf86c2`  
		Last Modified: Tue, 15 Jul 2025 19:27:46 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.0-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:958bb89f875d5bd08234cdab7e8380cda7dc4eea714aa5dd2163fd3464a49c22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.7 KB (403682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb6e26545a47362444044a81a947549427a112135537a3a393226508b9d00f8`

```dockerfile
```

-	Layers:
	-	`sha256:da8d3e8bf8525002c6b07e29f473dad97c32ab76bc541156db43124ee078d3bf`  
		Last Modified: Tue, 15 Jul 2025 22:21:23 GMT  
		Size: 388.3 KB (388303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12fea95b71b3d4b8fc770dfe58e742da102df6dba1beb0c4f901e5b944b97a3`  
		Last Modified: Tue, 15 Jul 2025 22:21:24 GMT  
		Size: 15.4 KB (15379 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:4a740c633b90375fc4613465ead786b393b1106ff2a748d895d51967f5c8eb55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:495481bc51bb09cd677a387761815568fac2fdf0165b74652e05308d252fc673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75887885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e6e758f84077ab7831577cf3aa0a3c1ee4fae198f9eee13120886d468b4d5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 08 Jul 2025 13:10:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.7.7
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
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7cd59a170b5fff4759056f3021cd3a0f8b8b93fd86f3b540f889da699918c6`  
		Last Modified: Tue, 15 Jul 2025 20:46:46 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a6ffa563fb7d136af9cbd8379cf5ceacbf2926fadcd8e281c43b0cd52cb334`  
		Last Modified: Wed, 16 Jul 2025 06:05:34 GMT  
		Size: 283.8 KB (283794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd34a060f527e5af8a18b24cf3308e10ffd9c472cc20593e106f406d6efe7f1`  
		Last Modified: Wed, 16 Jul 2025 08:14:17 GMT  
		Size: 72.0 MB (71982834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b96d9ad903da395c8acc30237a367d0349015a659efa7b235443f051909f89`  
		Last Modified: Wed, 16 Jul 2025 05:59:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cba525bdf0c3a03182ebbbf50f501d2ad26bdbb63fb2e4bd01963a644155449`  
		Last Modified: Wed, 16 Jul 2025 05:59:25 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:2f1b54a2048c3a3b338544b0c408b33dd54dbc449f63a8dbde7990f697a68a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 KB (379593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf0662c60fc4bc189a7c968c0a97009e090f806295b18433651f515500f4bd1`

```dockerfile
```

-	Layers:
	-	`sha256:7129167326340ece8825cd0b82133d5059b3bceaaa807a7903b1c31ce09f5e9d`  
		Last Modified: Tue, 15 Jul 2025 22:21:18 GMT  
		Size: 363.9 KB (363909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e7c0e7967c42b262e03d986132f124a458856a89945a10b72681d79a9d610c`  
		Last Modified: Tue, 15 Jul 2025 22:21:19 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:2cc6de2e799cbe1012b0da297de4a508a380d2e4afff2bc2eb3c2537074dc306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:e14a1a081c6e90e9b6994d2c28fe16afc881c35a01e8a8226f798225e69d98a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169653283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9362a79edf5995c9f05c55fdeaf660052d39f9b23214fcaf53ca545a5e964839`
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
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
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
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1718e536deb534924f0e24d75c0ad8cbe941526cffc1ff3ec1e0d1c6ec3f68`  
		Last Modified: Tue, 12 Aug 2025 17:23:37 GMT  
		Size: 7.1 MB (7106301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a40004787fb09ea05e7f72892df1c2b554e1ae05bf36d5ee6c86cf3f0349201`  
		Last Modified: Tue, 12 Aug 2025 18:33:53 GMT  
		Size: 45.6 MB (45643206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ed28f150dec03899d9b84c9b6b388c9963f54122c90b38bdc525f958613faa`  
		Last Modified: Tue, 12 Aug 2025 18:33:53 GMT  
		Size: 87.4 MB (87366262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8dec99a0cb2712d15b2f593cb84fdfaff562469bec38c7668546d9f0e71dfe`  
		Last Modified: Tue, 12 Aug 2025 18:33:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdd0230f3ac689129a3409637bf0e4543421b1689fc65fa3a9a8859cce29397`  
		Last Modified: Tue, 12 Aug 2025 18:33:47 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:0081a8bf7976870890c91bcbdb4395ec2e878305cc4739e72e0d94eff828ca96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173bf62902807b8d110e202a6de203ae6a0a8a68bcf9fe1c49fcf7ebde6a7a27`

```dockerfile
```

-	Layers:
	-	`sha256:827290ae5bb73a0229370187641487e9b070bcdb20a667342b4b4a6a80ec3b41`  
		Last Modified: Tue, 12 Aug 2025 19:21:27 GMT  
		Size: 3.7 MB (3731253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3c503667dd479af4a224b216ff20361d90611461a8b5b1006894f188c0ad0f1`  
		Last Modified: Tue, 12 Aug 2025 19:21:27 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:46cf79ad0f89fe2687bf1acf59cffb7b441ba07de25b182d92d31b5431661190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159022868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5000def53d67cb759c435f8cc5cb1e26363bd7c4259d26dab4c1a70a26a841a`
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
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
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
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476a9430580cac739e29f524f2d4fa032c5bfb4d16c97a34238459efc663af4e`  
		Last Modified: Tue, 12 Aug 2025 17:24:37 GMT  
		Size: 7.1 MB (7051909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2e62eaf5273f9309d0110fd3120778a77557e5aa2a49de27595f55ec44f2d7`  
		Last Modified: Wed, 13 Aug 2025 01:24:27 GMT  
		Size: 43.1 MB (43147465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b364ad99c784d84f60ae66ff3cdd21f20c030193b0c0b0af2895b3e0d9b35c9e`  
		Last Modified: Wed, 13 Aug 2025 17:26:11 GMT  
		Size: 81.5 MB (81463725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8912af52b80bd0db4ff2b6a51d9dbaab0894cf46c5643ad3fde44abb25506227`  
		Last Modified: Tue, 12 Aug 2025 23:39:52 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972ce250eaa6760f24d454e096fdb6d3a90403816a740376563e03a0eb4b9551`  
		Last Modified: Tue, 12 Aug 2025 23:39:55 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:4a6cfebe7936fac5c6b97373033c597d080f60c1db0de2c0499fb6f5da34b8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235cd7f1bcbe49cac80ccf74839f903b9e0f20810ddb7a19ea1cecb6863a4aec`

```dockerfile
```

-	Layers:
	-	`sha256:b7cb9d0ca0e96b8909bdfbe958ac467d13bb6353dc514fb639d4433f726a767a`  
		Last Modified: Wed, 13 Aug 2025 01:21:28 GMT  
		Size: 3.7 MB (3730727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2f331b1f233cd78e7f048bc860290261080c2374350c15561202d4dd58fb7cb`  
		Last Modified: Wed, 13 Aug 2025 01:21:29 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json
