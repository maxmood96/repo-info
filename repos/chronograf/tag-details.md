<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.8`](#chronograf1108)
-	[`chronograf:1.10.8-alpine`](#chronograf1108-alpine)
-	[`chronograf:1.7`](#chronograf17)
-	[`chronograf:1.7-alpine`](#chronograf17-alpine)
-	[`chronograf:1.7.17`](#chronograf1717)
-	[`chronograf:1.7.17-alpine`](#chronograf1717-alpine)
-	[`chronograf:1.8`](#chronograf18)
-	[`chronograf:1.8-alpine`](#chronograf18-alpine)
-	[`chronograf:1.8.10`](#chronograf1810)
-	[`chronograf:1.8.10-alpine`](#chronograf1810-alpine)
-	[`chronograf:1.9`](#chronograf19)
-	[`chronograf:1.9-alpine`](#chronograf19-alpine)
-	[`chronograf:1.9.4`](#chronograf194)
-	[`chronograf:1.9.4-alpine`](#chronograf194-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.10`

```console
$ docker pull chronograf@sha256:3fbfcc3a6c9d72e1b7765dd3a8617f26653cbde2babd26fd1f1bbf6f6a42922e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10` - linux; amd64

```console
$ docker pull chronograf@sha256:c594743eb2d70ae09c739c7f93f920ea5f8e2258327cdaf71c148f833399f8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e9db47282885f54445b4d03fe07231a41e1f4f772bceb462bdd39de558bc8e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:07:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 23:08:06 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Mon, 08 Dec 2025 23:08:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:08:06 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 08 Dec 2025 23:08:06 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 08 Dec 2025 23:08:06 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 08 Dec 2025 23:08:06 GMT
VOLUME [/var/lib/chronograf]
# Mon, 08 Dec 2025 23:08:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:08:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:08:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b906813b3c7a1bc726013079d276cd811916f16af222a4ed7269ef82a3804e59`  
		Last Modified: Mon, 08 Dec 2025 23:08:25 GMT  
		Size: 7.9 MB (7878852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc666d4835937e2220b9396c52bd685f7545872a63881e132dcfcc540e550a1`  
		Last Modified: Mon, 08 Dec 2025 23:08:28 GMT  
		Size: 49.3 MB (49276694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537dd4e73ab9539d97d15157388ba9eedb176847cdfb06fc9f04d8af4f3ff935`  
		Last Modified: Mon, 08 Dec 2025 23:08:24 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1039be48ca2a044e939d7a8ec44d50c0aee42328b0e094acfb5742f4a5e07b2c`  
		Last Modified: Mon, 08 Dec 2025 23:08:24 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a52c4ea51584a7918b2aab6e64828c05d85e2390bd3e2db89beb7e0d3cc3a2`  
		Last Modified: Mon, 08 Dec 2025 23:08:26 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:5ed955d5b41a4ca8c8686a747cad5e2136cc7c213c5052ef3e3e4352df9c4e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33606a1852dc6f5af831d9cb1239547a04661b51b8ff432785af1782dd8d741`

```dockerfile
```

-	Layers:
	-	`sha256:662a9044cb1e525ac17b3c81c0708e9c00bf781da0acf6cfa174985604359918`  
		Last Modified: Tue, 09 Dec 2025 01:38:55 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e87e18c4c0dd20814ec877db8a5ac05ec20762fa6ab91c57f2c6a031ef91ea69`  
		Last Modified: Tue, 09 Dec 2025 01:38:56 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:a9eee760c300ed74ee00152e204aeb74c6f76614d290fb956a0b0cada62bda71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76088485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbb5df25cb1608648b241d8634ce8c1411ab2e8501ed6abdfe11cf19d123c8d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:10:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:10:36 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 09 Dec 2025 00:10:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 00:10:36 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 09 Dec 2025 00:10:36 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 09 Dec 2025 00:10:36 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 09 Dec 2025 00:10:36 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Dec 2025 00:10:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:10:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:10:36 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15653d8ecaaadc3f2ca2a299e2702e2799dde21b5d7a9a157da62081d255895`  
		Last Modified: Tue, 09 Dec 2025 00:10:58 GMT  
		Size: 6.5 MB (6508169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af2847cc0300fea9798f3dda808d44a9b4b4a05e7c6e019b961216aed8791ee`  
		Last Modified: Tue, 09 Dec 2025 00:11:04 GMT  
		Size: 45.6 MB (45621825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d392f4402076132ae69246cf56715e534f4a4d4cf3ca27073a1ec0fe3cddf2b`  
		Last Modified: Tue, 09 Dec 2025 00:11:00 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97486948da4815691f7338de8bcb0f809d2de68ef3644528121a1b79a86054d4`  
		Last Modified: Tue, 09 Dec 2025 00:10:58 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8db7b8a1e9e7447dca72eeecc6a7dff0bf8746c5df349f7d2cd3fbce33311b5`  
		Last Modified: Tue, 09 Dec 2025 00:10:58 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:42c0504831fd00f642f77e1347e342ce1f8a491c9783b1d6cd2a0c1844fd4b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7158fba3b2d6bab026e84ed139ec0a33375ad427c587cc7f4715fa5f8ca14411`

```dockerfile
```

-	Layers:
	-	`sha256:75f34ec3a9cae186aded26cf43ddceacb375351828a69aa13b33c73daba78ea8`  
		Last Modified: Tue, 09 Dec 2025 01:39:00 GMT  
		Size: 2.9 MB (2856371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80697cb76ffad47e142ce75fd04a0907f851f27a0a85d6b6e896c1ad80f10b53`  
		Last Modified: Tue, 09 Dec 2025 01:39:01 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:87ab5c23ab1a4c827c6a9b34d360c43e829d7d06099af1f5c5d1a871e998ae0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e45d4f9fdaae74ec9f04cd4921c414fd6de0a04451ff20d55b5636b612298c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:11:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 23:11:40 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Mon, 08 Dec 2025 23:11:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 08 Dec 2025 23:11:41 GMT
VOLUME [/var/lib/chronograf]
# Mon, 08 Dec 2025 23:11:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:11:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc423e736d4142acab17607c7d704550cfc05ad1c695f77c250684aae7a09bf6`  
		Last Modified: Mon, 08 Dec 2025 23:12:01 GMT  
		Size: 7.7 MB (7691839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b597abbe4c4905b7ab605402dfcc46262acda2dd39a8915607a2f20b19cad0`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 47.1 MB (47066807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778b97fcbd0bd3bb26271f20f6bfeb70e3eeba84b57b3644a7a44d3077181010`  
		Last Modified: Mon, 08 Dec 2025 23:12:00 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e164a20ab4b35b55ce2c689cba71f953a2f2bfc932eb157a8325a5015a85cfe`  
		Last Modified: Mon, 08 Dec 2025 23:12:00 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e44701a97eeac8bf17ee2dcec6d77bd75ec0f0f2af22fc55408552a7950e22`  
		Last Modified: Mon, 08 Dec 2025 23:12:00 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:8c9bdcf49bc1033ebd11f9fc95668cc1860c67717b36ba5d5d5ec54e3c319c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d959dc1f6ed009446107a9ada80e7f9ee95082f6bc9189c63b98b24c571e683a`

```dockerfile
```

-	Layers:
	-	`sha256:2e78cf8d179bf6aa7db8b2ae7a6b8a4473e962ccf8809ae85db1c5d75af8f8b0`  
		Last Modified: Tue, 09 Dec 2025 01:39:06 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9565350ae9696c60f4ce5ef731af5798064640086fed3a1eb67df68a2ddd7363`  
		Last Modified: Tue, 09 Dec 2025 01:39:06 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:efc72c285cae492b0fb820a7794f2da69a70ef77caa8d28282e0df6f79856029
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:08463b31a0a2617a51e230161f997b525214640155e291a423ae53004330c719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32700225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af178eb7af41f52d85b69957fc583d381f6a24a9e604b40818766ecf3004a1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08cd1461c07b6d2b803ff1e365582cea280da85884cb0fe20c1b539046e9c0f`  
		Last Modified: Mon, 08 Dec 2025 02:53:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642952c8832a913bc8124d8c1f9800b4c40ed32aa2d21f4bbd9c85e32729fdf2`  
		Last Modified: Mon, 08 Dec 2025 02:53:47 GMT  
		Size: 314.6 KB (314639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff188fbd44ef51d6c15c61b590915a7d108294cea3cebd1224f569cf88dbfbd2`  
		Last Modified: Mon, 08 Dec 2025 02:53:50 GMT  
		Size: 28.6 MB (28558408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ada6ea712a91804f080e3ac3a6fec72f1bf330d8affb0a76902b1f0b78a5046`  
		Last Modified: Mon, 08 Dec 2025 02:53:48 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322d214c5daa6878e468360de897da9cd0cad1be05283f5529b5e2ce07c9e72f`  
		Last Modified: Mon, 08 Dec 2025 02:53:48 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175f9d62a6d73ab836332ca97429aec6104967dc35d5ab6aaa103f374c1539bd`  
		Last Modified: Mon, 08 Dec 2025 02:53:49 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:dd3236bd7a2263357f0c7258a9a36c7fef283fd9f58f17f5fc2cbfa8330df313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 KB (268238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808a56c94ce865ff68fe325760f90b15b31758031ea028455935f57e4d2afe56`

```dockerfile
```

-	Layers:
	-	`sha256:d62aac69b78bc656cc8510a0566537353a4cda897cdaf124ca24ad68c0fa7fb1`  
		Last Modified: Mon, 08 Dec 2025 03:44:43 GMT  
		Size: 250.4 KB (250383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c7ffc31e817e3fff1eade663dcae6dc3da5bb4370e43abaf921eebc9dd7f0a1`  
		Last Modified: Mon, 08 Dec 2025 03:44:44 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.8`

```console
$ docker pull chronograf@sha256:3fbfcc3a6c9d72e1b7765dd3a8617f26653cbde2babd26fd1f1bbf6f6a42922e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10.8` - linux; amd64

```console
$ docker pull chronograf@sha256:c594743eb2d70ae09c739c7f93f920ea5f8e2258327cdaf71c148f833399f8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e9db47282885f54445b4d03fe07231a41e1f4f772bceb462bdd39de558bc8e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:07:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 23:08:06 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Mon, 08 Dec 2025 23:08:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:08:06 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 08 Dec 2025 23:08:06 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 08 Dec 2025 23:08:06 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 08 Dec 2025 23:08:06 GMT
VOLUME [/var/lib/chronograf]
# Mon, 08 Dec 2025 23:08:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:08:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:08:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b906813b3c7a1bc726013079d276cd811916f16af222a4ed7269ef82a3804e59`  
		Last Modified: Mon, 08 Dec 2025 23:08:25 GMT  
		Size: 7.9 MB (7878852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc666d4835937e2220b9396c52bd685f7545872a63881e132dcfcc540e550a1`  
		Last Modified: Mon, 08 Dec 2025 23:08:28 GMT  
		Size: 49.3 MB (49276694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537dd4e73ab9539d97d15157388ba9eedb176847cdfb06fc9f04d8af4f3ff935`  
		Last Modified: Mon, 08 Dec 2025 23:08:24 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1039be48ca2a044e939d7a8ec44d50c0aee42328b0e094acfb5742f4a5e07b2c`  
		Last Modified: Mon, 08 Dec 2025 23:08:24 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a52c4ea51584a7918b2aab6e64828c05d85e2390bd3e2db89beb7e0d3cc3a2`  
		Last Modified: Mon, 08 Dec 2025 23:08:26 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:5ed955d5b41a4ca8c8686a747cad5e2136cc7c213c5052ef3e3e4352df9c4e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33606a1852dc6f5af831d9cb1239547a04661b51b8ff432785af1782dd8d741`

```dockerfile
```

-	Layers:
	-	`sha256:662a9044cb1e525ac17b3c81c0708e9c00bf781da0acf6cfa174985604359918`  
		Last Modified: Tue, 09 Dec 2025 01:38:55 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e87e18c4c0dd20814ec877db8a5ac05ec20762fa6ab91c57f2c6a031ef91ea69`  
		Last Modified: Tue, 09 Dec 2025 01:38:56 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:a9eee760c300ed74ee00152e204aeb74c6f76614d290fb956a0b0cada62bda71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76088485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbb5df25cb1608648b241d8634ce8c1411ab2e8501ed6abdfe11cf19d123c8d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:10:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:10:36 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 09 Dec 2025 00:10:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 00:10:36 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 09 Dec 2025 00:10:36 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 09 Dec 2025 00:10:36 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 09 Dec 2025 00:10:36 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Dec 2025 00:10:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:10:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:10:36 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15653d8ecaaadc3f2ca2a299e2702e2799dde21b5d7a9a157da62081d255895`  
		Last Modified: Tue, 09 Dec 2025 00:10:58 GMT  
		Size: 6.5 MB (6508169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af2847cc0300fea9798f3dda808d44a9b4b4a05e7c6e019b961216aed8791ee`  
		Last Modified: Tue, 09 Dec 2025 00:11:04 GMT  
		Size: 45.6 MB (45621825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d392f4402076132ae69246cf56715e534f4a4d4cf3ca27073a1ec0fe3cddf2b`  
		Last Modified: Tue, 09 Dec 2025 00:11:00 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97486948da4815691f7338de8bcb0f809d2de68ef3644528121a1b79a86054d4`  
		Last Modified: Tue, 09 Dec 2025 00:10:58 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8db7b8a1e9e7447dca72eeecc6a7dff0bf8746c5df349f7d2cd3fbce33311b5`  
		Last Modified: Tue, 09 Dec 2025 00:10:58 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:42c0504831fd00f642f77e1347e342ce1f8a491c9783b1d6cd2a0c1844fd4b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7158fba3b2d6bab026e84ed139ec0a33375ad427c587cc7f4715fa5f8ca14411`

```dockerfile
```

-	Layers:
	-	`sha256:75f34ec3a9cae186aded26cf43ddceacb375351828a69aa13b33c73daba78ea8`  
		Last Modified: Tue, 09 Dec 2025 01:39:00 GMT  
		Size: 2.9 MB (2856371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80697cb76ffad47e142ce75fd04a0907f851f27a0a85d6b6e896c1ad80f10b53`  
		Last Modified: Tue, 09 Dec 2025 01:39:01 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:87ab5c23ab1a4c827c6a9b34d360c43e829d7d06099af1f5c5d1a871e998ae0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e45d4f9fdaae74ec9f04cd4921c414fd6de0a04451ff20d55b5636b612298c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:11:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 23:11:40 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Mon, 08 Dec 2025 23:11:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 08 Dec 2025 23:11:41 GMT
VOLUME [/var/lib/chronograf]
# Mon, 08 Dec 2025 23:11:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:11:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc423e736d4142acab17607c7d704550cfc05ad1c695f77c250684aae7a09bf6`  
		Last Modified: Mon, 08 Dec 2025 23:12:01 GMT  
		Size: 7.7 MB (7691839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b597abbe4c4905b7ab605402dfcc46262acda2dd39a8915607a2f20b19cad0`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 47.1 MB (47066807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778b97fcbd0bd3bb26271f20f6bfeb70e3eeba84b57b3644a7a44d3077181010`  
		Last Modified: Mon, 08 Dec 2025 23:12:00 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e164a20ab4b35b55ce2c689cba71f953a2f2bfc932eb157a8325a5015a85cfe`  
		Last Modified: Mon, 08 Dec 2025 23:12:00 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e44701a97eeac8bf17ee2dcec6d77bd75ec0f0f2af22fc55408552a7950e22`  
		Last Modified: Mon, 08 Dec 2025 23:12:00 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:8c9bdcf49bc1033ebd11f9fc95668cc1860c67717b36ba5d5d5ec54e3c319c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d959dc1f6ed009446107a9ada80e7f9ee95082f6bc9189c63b98b24c571e683a`

```dockerfile
```

-	Layers:
	-	`sha256:2e78cf8d179bf6aa7db8b2ae7a6b8a4473e962ccf8809ae85db1c5d75af8f8b0`  
		Last Modified: Tue, 09 Dec 2025 01:39:06 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9565350ae9696c60f4ce5ef731af5798064640086fed3a1eb67df68a2ddd7363`  
		Last Modified: Tue, 09 Dec 2025 01:39:06 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.8-alpine`

```console
$ docker pull chronograf@sha256:efc72c285cae492b0fb820a7794f2da69a70ef77caa8d28282e0df6f79856029
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:08463b31a0a2617a51e230161f997b525214640155e291a423ae53004330c719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32700225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af178eb7af41f52d85b69957fc583d381f6a24a9e604b40818766ecf3004a1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08cd1461c07b6d2b803ff1e365582cea280da85884cb0fe20c1b539046e9c0f`  
		Last Modified: Mon, 08 Dec 2025 02:53:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642952c8832a913bc8124d8c1f9800b4c40ed32aa2d21f4bbd9c85e32729fdf2`  
		Last Modified: Mon, 08 Dec 2025 02:53:47 GMT  
		Size: 314.6 KB (314639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff188fbd44ef51d6c15c61b590915a7d108294cea3cebd1224f569cf88dbfbd2`  
		Last Modified: Mon, 08 Dec 2025 02:53:50 GMT  
		Size: 28.6 MB (28558408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ada6ea712a91804f080e3ac3a6fec72f1bf330d8affb0a76902b1f0b78a5046`  
		Last Modified: Mon, 08 Dec 2025 02:53:48 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322d214c5daa6878e468360de897da9cd0cad1be05283f5529b5e2ce07c9e72f`  
		Last Modified: Mon, 08 Dec 2025 02:53:48 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175f9d62a6d73ab836332ca97429aec6104967dc35d5ab6aaa103f374c1539bd`  
		Last Modified: Mon, 08 Dec 2025 02:53:49 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:dd3236bd7a2263357f0c7258a9a36c7fef283fd9f58f17f5fc2cbfa8330df313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 KB (268238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808a56c94ce865ff68fe325760f90b15b31758031ea028455935f57e4d2afe56`

```dockerfile
```

-	Layers:
	-	`sha256:d62aac69b78bc656cc8510a0566537353a4cda897cdaf124ca24ad68c0fa7fb1`  
		Last Modified: Mon, 08 Dec 2025 03:44:43 GMT  
		Size: 250.4 KB (250383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c7ffc31e817e3fff1eade663dcae6dc3da5bb4370e43abaf921eebc9dd7f0a1`  
		Last Modified: Mon, 08 Dec 2025 03:44:44 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:a8676204db74efef3881a20450abb618ef115dcd811cdfa8735bcf1e92bb2db6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:1e636466f1c82afd1bcb5d13f6fa71520d5bd623abfe7b1cbb31d9884dbbfb7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69230714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95bcc778b4944e036ee5640ec66d35ec3f3f2d3fb7c9ab517f3ddeb1331c95d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 23:07:32 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 08 Dec 2025 23:07:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:07:32 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 08 Dec 2025 23:07:32 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 08 Dec 2025 23:07:32 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 08 Dec 2025 23:07:32 GMT
VOLUME [/var/lib/chronograf]
# Mon, 08 Dec 2025 23:07:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:07:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:07:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92e6bcce1516565d8b1ad1f7f7c6c1d989b0a686b2091d3b9435443e9175c51`  
		Last Modified: Mon, 08 Dec 2025 23:07:49 GMT  
		Size: 4.2 MB (4209307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2030301738b54f612a456eb1d83cfcf890c1985f55c0087bf3ee6b32cfe8533f`  
		Last Modified: Mon, 08 Dec 2025 23:07:52 GMT  
		Size: 34.7 MB (34738547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6017ba365ef419f133acf349bd651da44335769890082187421b61d9749fe66b`  
		Last Modified: Mon, 08 Dec 2025 23:07:48 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e241b8d85615c2f27bd8738324ee23bc788d7d37f54eb5509366076da99d58`  
		Last Modified: Mon, 08 Dec 2025 23:07:49 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c921271aafc08129470c97c4d52b419e2e6c486f97002e9ea5ff1c23f6ce1e`  
		Last Modified: Mon, 08 Dec 2025 23:07:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:fbaba5fe8dd1bfda12ad2ede35821edf83d42a19d3c0d0981a23f896955188e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcd2808833cb5448bfc31be40e56a4a42bc02299bf8e0249802f25117a30e3b`

```dockerfile
```

-	Layers:
	-	`sha256:ad8325218fc17b5950ce1e2e0fc8981bbf803108af37d416427a6579dd120a6f`  
		Last Modified: Tue, 09 Dec 2025 01:39:08 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95fcbee4e21104e72edd754e5153a404e7d7a7d2a52366df895f621219880a06`  
		Last Modified: Tue, 09 Dec 2025 01:39:09 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:5d674728ecfa51122c54be2147198dba962b425391f3f692f9d58386477dc303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62179816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37298c854857bbf1c40a0e0049436225805c4c7633573c0efcb9f7fd47aaf92b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1765152000'
# Tue, 09 Dec 2025 00:07:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:07:55 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 09 Dec 2025 00:07:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 00:07:55 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 09 Dec 2025 00:07:55 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 09 Dec 2025 00:07:55 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 09 Dec 2025 00:07:55 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Dec 2025 00:07:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:07:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:07:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:189d7c8243253070696fcc5bcaa526823c4016a5dd57614057cc9107756082b2`  
		Last Modified: Mon, 08 Dec 2025 22:16:40 GMT  
		Size: 25.5 MB (25546219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4a18ae603478c063ac7ca42e4289e9560d3c27ce1923c6c88003a1e2890241`  
		Last Modified: Tue, 09 Dec 2025 00:08:12 GMT  
		Size: 3.5 MB (3511653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc1d1fcd4a0bbc8e5cfba6544566d2c37588cd2bdea2679d4d14a727264ee2c`  
		Last Modified: Tue, 09 Dec 2025 00:08:15 GMT  
		Size: 33.1 MB (33097551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8b3bcf0dbdb98e3ef5a8b95514a0c05dae707f863bde37e4d75384b0ac654d`  
		Last Modified: Tue, 09 Dec 2025 00:08:12 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096d03efeb4de132901e3276b4b05193328e70a6b3bbf4231628977ead8a6527`  
		Last Modified: Tue, 09 Dec 2025 00:08:12 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaef3cee340c01947ed79c49ff329d6a09940a6dbe56a8a622b6c0e2ce3e8895`  
		Last Modified: Tue, 09 Dec 2025 00:08:12 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:ccfdd9bb34bdee897e4d6acfc42cb562086378589e80cad9fc12f6510b6006b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f75763e3c7a816469ec629378ca912d57ec35e32aaef3b4cce1e9e84e7d98b9`

```dockerfile
```

-	Layers:
	-	`sha256:77593608be5bc96369433a26f1eb0bbe160a6976a6aad60937d3662c5895b0d5`  
		Last Modified: Tue, 09 Dec 2025 01:39:18 GMT  
		Size: 3.1 MB (3051144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e754a23780d28b32a3eeb77dd3a6eafcafcd292635a706225e511084a19b9e2`  
		Last Modified: Tue, 09 Dec 2025 01:39:18 GMT  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b37ce065c464282dfcf4f9b40b13b901d25a61db20ef37458c744897c960768f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66221653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325d7ebfb167b0e627829978e996d50c6299da6f9532f2958c3a765277c26a1b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:10:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 23:10:52 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 08 Dec 2025 23:10:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:10:52 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 08 Dec 2025 23:10:52 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 08 Dec 2025 23:10:52 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 08 Dec 2025 23:10:52 GMT
VOLUME [/var/lib/chronograf]
# Mon, 08 Dec 2025 23:10:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:10:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:10:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239d3a6ec8aab2184c8afafe917eabe0dd52cedde0d6806101b9aaa551aa399f`  
		Last Modified: Mon, 08 Dec 2025 23:11:10 GMT  
		Size: 4.2 MB (4210635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e4ff07a6ce476c580d38f4ef6927577d9c06ed899570949bfd715d3e4bb0cd`  
		Last Modified: Mon, 08 Dec 2025 23:11:20 GMT  
		Size: 33.2 MB (33238141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6503bc88abcf80835f5ad3aac2b6d7a453d269f8e019252d595725aa16236f3c`  
		Last Modified: Mon, 08 Dec 2025 23:11:08 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb32cf8a83ec155acf31869395f28420bf312ab032ec9030209eca76f41053c`  
		Last Modified: Mon, 08 Dec 2025 23:11:09 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fe49d99114bd9d2f614da24132acc01e1ab81189497e74a43dd4b3d620f5b3`  
		Last Modified: Mon, 08 Dec 2025 23:11:08 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:b1e07eb7cac265e3c02baa04ff95782e9387428bfb7d07c2ac36531ce1aa24e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b0a680597f23a24567f6c6ecb825aac0f07d2f8ed7eb39e5f7b53f434ebc31`

```dockerfile
```

-	Layers:
	-	`sha256:7391f2553de070bff6323a5b7ab2a90b453dd610c8721c048ef4e752c724fa07`  
		Last Modified: Tue, 09 Dec 2025 01:39:23 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed220d9fb1494c45fa99c29e3402714ef7c15e882ddede04d1181f29d778de68`  
		Last Modified: Tue, 09 Dec 2025 01:39:24 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:f9bf8a3a9499f5324ca9b5f428e7ecbf8a4714d366e8a7920a8d06292f7d0511
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:0e68a8f6a33cec3ad19c936e80df9706efc6f4a6651f78b3373920f503a90deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23499028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5704e6698a8163ec6cf9a9f4d2fc39455f7394b4b089fd3fe4fbbfcd3c84f5fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af74a58a446b59e39793a690435f78e585a91ea73edb6406a99a3283db12a3a2`  
		Last Modified: Wed, 08 Oct 2025 23:01:00 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053646d1ede74b4422e0751427c045b128d56b4d9c7521a34d9a3e2fd81f2fa6`  
		Last Modified: Wed, 08 Oct 2025 23:01:00 GMT  
		Size: 290.8 KB (290771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fddb95d664d6dacdb2318596d88bdbacf9e5bde5abe2b7e4335d05288276ea`  
		Last Modified: Wed, 08 Oct 2025 23:01:01 GMT  
		Size: 19.6 MB (19556558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f367635d83aeb5f5f554e62a06a02ad833c17339cf302d30013629399527c0`  
		Last Modified: Wed, 08 Oct 2025 23:01:00 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07f90ee1715c3ce00ef0c8e4958732cd35aeb06708db0a00e83afbe1f17da89`  
		Last Modified: Wed, 08 Oct 2025 23:01:01 GMT  
		Size: 11.9 KB (11891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9166e539db1f38a4aa1b578555a8c92c86979cbc08b8098fba9661f87ffe6167`  
		Last Modified: Wed, 08 Oct 2025 23:01:01 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:bcbb31392ab3215af685b41ca6842da95b2e263604620ad5d7a30c80609bc543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 KB (188744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862b2564bbbfa2013c4f206e9af5027911bf83448426df87b517b51fb5f596e0`

```dockerfile
```

-	Layers:
	-	`sha256:7d486241e7d5fad65401d86ed4cecac735dc744dd18c05a5530b79d0bc9ae6ac`  
		Last Modified: Wed, 08 Oct 2025 23:01:00 GMT  
		Size: 171.8 KB (171832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87486fae9bd6ba27ac7806fc6b1c5c571f4d3de5fc46fd1b292df95f203bc24e`  
		Last Modified: Wed, 08 Oct 2025 23:01:00 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:a8676204db74efef3881a20450abb618ef115dcd811cdfa8735bcf1e92bb2db6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:1e636466f1c82afd1bcb5d13f6fa71520d5bd623abfe7b1cbb31d9884dbbfb7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69230714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95bcc778b4944e036ee5640ec66d35ec3f3f2d3fb7c9ab517f3ddeb1331c95d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 23:07:32 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 08 Dec 2025 23:07:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:07:32 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 08 Dec 2025 23:07:32 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 08 Dec 2025 23:07:32 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 08 Dec 2025 23:07:32 GMT
VOLUME [/var/lib/chronograf]
# Mon, 08 Dec 2025 23:07:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:07:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:07:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92e6bcce1516565d8b1ad1f7f7c6c1d989b0a686b2091d3b9435443e9175c51`  
		Last Modified: Mon, 08 Dec 2025 23:07:49 GMT  
		Size: 4.2 MB (4209307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2030301738b54f612a456eb1d83cfcf890c1985f55c0087bf3ee6b32cfe8533f`  
		Last Modified: Mon, 08 Dec 2025 23:07:52 GMT  
		Size: 34.7 MB (34738547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6017ba365ef419f133acf349bd651da44335769890082187421b61d9749fe66b`  
		Last Modified: Mon, 08 Dec 2025 23:07:48 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e241b8d85615c2f27bd8738324ee23bc788d7d37f54eb5509366076da99d58`  
		Last Modified: Mon, 08 Dec 2025 23:07:49 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c921271aafc08129470c97c4d52b419e2e6c486f97002e9ea5ff1c23f6ce1e`  
		Last Modified: Mon, 08 Dec 2025 23:07:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:fbaba5fe8dd1bfda12ad2ede35821edf83d42a19d3c0d0981a23f896955188e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcd2808833cb5448bfc31be40e56a4a42bc02299bf8e0249802f25117a30e3b`

```dockerfile
```

-	Layers:
	-	`sha256:ad8325218fc17b5950ce1e2e0fc8981bbf803108af37d416427a6579dd120a6f`  
		Last Modified: Tue, 09 Dec 2025 01:39:08 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95fcbee4e21104e72edd754e5153a404e7d7a7d2a52366df895f621219880a06`  
		Last Modified: Tue, 09 Dec 2025 01:39:09 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:5d674728ecfa51122c54be2147198dba962b425391f3f692f9d58386477dc303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62179816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37298c854857bbf1c40a0e0049436225805c4c7633573c0efcb9f7fd47aaf92b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1765152000'
# Tue, 09 Dec 2025 00:07:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:07:55 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 09 Dec 2025 00:07:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 00:07:55 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 09 Dec 2025 00:07:55 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 09 Dec 2025 00:07:55 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 09 Dec 2025 00:07:55 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Dec 2025 00:07:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:07:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:07:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:189d7c8243253070696fcc5bcaa526823c4016a5dd57614057cc9107756082b2`  
		Last Modified: Mon, 08 Dec 2025 22:16:40 GMT  
		Size: 25.5 MB (25546219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4a18ae603478c063ac7ca42e4289e9560d3c27ce1923c6c88003a1e2890241`  
		Last Modified: Tue, 09 Dec 2025 00:08:12 GMT  
		Size: 3.5 MB (3511653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc1d1fcd4a0bbc8e5cfba6544566d2c37588cd2bdea2679d4d14a727264ee2c`  
		Last Modified: Tue, 09 Dec 2025 00:08:15 GMT  
		Size: 33.1 MB (33097551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8b3bcf0dbdb98e3ef5a8b95514a0c05dae707f863bde37e4d75384b0ac654d`  
		Last Modified: Tue, 09 Dec 2025 00:08:12 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096d03efeb4de132901e3276b4b05193328e70a6b3bbf4231628977ead8a6527`  
		Last Modified: Tue, 09 Dec 2025 00:08:12 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaef3cee340c01947ed79c49ff329d6a09940a6dbe56a8a622b6c0e2ce3e8895`  
		Last Modified: Tue, 09 Dec 2025 00:08:12 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:ccfdd9bb34bdee897e4d6acfc42cb562086378589e80cad9fc12f6510b6006b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f75763e3c7a816469ec629378ca912d57ec35e32aaef3b4cce1e9e84e7d98b9`

```dockerfile
```

-	Layers:
	-	`sha256:77593608be5bc96369433a26f1eb0bbe160a6976a6aad60937d3662c5895b0d5`  
		Last Modified: Tue, 09 Dec 2025 01:39:18 GMT  
		Size: 3.1 MB (3051144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e754a23780d28b32a3eeb77dd3a6eafcafcd292635a706225e511084a19b9e2`  
		Last Modified: Tue, 09 Dec 2025 01:39:18 GMT  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b37ce065c464282dfcf4f9b40b13b901d25a61db20ef37458c744897c960768f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66221653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325d7ebfb167b0e627829978e996d50c6299da6f9532f2958c3a765277c26a1b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:10:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 23:10:52 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 08 Dec 2025 23:10:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:10:52 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 08 Dec 2025 23:10:52 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 08 Dec 2025 23:10:52 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 08 Dec 2025 23:10:52 GMT
VOLUME [/var/lib/chronograf]
# Mon, 08 Dec 2025 23:10:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:10:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:10:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239d3a6ec8aab2184c8afafe917eabe0dd52cedde0d6806101b9aaa551aa399f`  
		Last Modified: Mon, 08 Dec 2025 23:11:10 GMT  
		Size: 4.2 MB (4210635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e4ff07a6ce476c580d38f4ef6927577d9c06ed899570949bfd715d3e4bb0cd`  
		Last Modified: Mon, 08 Dec 2025 23:11:20 GMT  
		Size: 33.2 MB (33238141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6503bc88abcf80835f5ad3aac2b6d7a453d269f8e019252d595725aa16236f3c`  
		Last Modified: Mon, 08 Dec 2025 23:11:08 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb32cf8a83ec155acf31869395f28420bf312ab032ec9030209eca76f41053c`  
		Last Modified: Mon, 08 Dec 2025 23:11:09 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fe49d99114bd9d2f614da24132acc01e1ab81189497e74a43dd4b3d620f5b3`  
		Last Modified: Mon, 08 Dec 2025 23:11:08 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:b1e07eb7cac265e3c02baa04ff95782e9387428bfb7d07c2ac36531ce1aa24e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b0a680597f23a24567f6c6ecb825aac0f07d2f8ed7eb39e5f7b53f434ebc31`

```dockerfile
```

-	Layers:
	-	`sha256:7391f2553de070bff6323a5b7ab2a90b453dd610c8721c048ef4e752c724fa07`  
		Last Modified: Tue, 09 Dec 2025 01:39:23 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed220d9fb1494c45fa99c29e3402714ef7c15e882ddede04d1181f29d778de68`  
		Last Modified: Tue, 09 Dec 2025 01:39:24 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:f9bf8a3a9499f5324ca9b5f428e7ecbf8a4714d366e8a7920a8d06292f7d0511
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:0e68a8f6a33cec3ad19c936e80df9706efc6f4a6651f78b3373920f503a90deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23499028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5704e6698a8163ec6cf9a9f4d2fc39455f7394b4b089fd3fe4fbbfcd3c84f5fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af74a58a446b59e39793a690435f78e585a91ea73edb6406a99a3283db12a3a2`  
		Last Modified: Wed, 08 Oct 2025 23:01:00 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053646d1ede74b4422e0751427c045b128d56b4d9c7521a34d9a3e2fd81f2fa6`  
		Last Modified: Wed, 08 Oct 2025 23:01:00 GMT  
		Size: 290.8 KB (290771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fddb95d664d6dacdb2318596d88bdbacf9e5bde5abe2b7e4335d05288276ea`  
		Last Modified: Wed, 08 Oct 2025 23:01:01 GMT  
		Size: 19.6 MB (19556558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f367635d83aeb5f5f554e62a06a02ad833c17339cf302d30013629399527c0`  
		Last Modified: Wed, 08 Oct 2025 23:01:00 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07f90ee1715c3ce00ef0c8e4958732cd35aeb06708db0a00e83afbe1f17da89`  
		Last Modified: Wed, 08 Oct 2025 23:01:01 GMT  
		Size: 11.9 KB (11891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9166e539db1f38a4aa1b578555a8c92c86979cbc08b8098fba9661f87ffe6167`  
		Last Modified: Wed, 08 Oct 2025 23:01:01 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:bcbb31392ab3215af685b41ca6842da95b2e263604620ad5d7a30c80609bc543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 KB (188744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862b2564bbbfa2013c4f206e9af5027911bf83448426df87b517b51fb5f596e0`

```dockerfile
```

-	Layers:
	-	`sha256:7d486241e7d5fad65401d86ed4cecac735dc744dd18c05a5530b79d0bc9ae6ac`  
		Last Modified: Wed, 08 Oct 2025 23:01:00 GMT  
		Size: 171.8 KB (171832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87486fae9bd6ba27ac7806fc6b1c5c571f4d3de5fc46fd1b292df95f203bc24e`  
		Last Modified: Wed, 08 Oct 2025 23:01:00 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:c8049465559dcd91cb340eabeade10b5c57804f6198b7884dc069b3e51ba8d8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:2bb2c50013ca2f46c7780fb34ccd9b8cdaa78b2a02bbc3aba45d718647eab2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69871388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2c089c48c7e92ff542f7cb514907109cbdcb80dd8124d227477aef76cf9dde`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:07:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 23:07:45 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 08 Dec 2025 23:07:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:07:45 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 08 Dec 2025 23:07:45 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 08 Dec 2025 23:07:45 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 08 Dec 2025 23:07:45 GMT
VOLUME [/var/lib/chronograf]
# Mon, 08 Dec 2025 23:07:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:07:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:07:45 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01214b21e1066bb7014cdebd05f52103da1b3c4fb49b4f34c7f02e5a8978d6b`  
		Last Modified: Mon, 08 Dec 2025 23:08:02 GMT  
		Size: 5.2 MB (5224216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec3937ad45dce7ae55bc4d785b2b4d464ebe1fc4c5f6659fc7335fc4e3f5e0a`  
		Last Modified: Mon, 08 Dec 2025 23:08:04 GMT  
		Size: 34.4 MB (34364321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c2d2713cd01965fc74dbbc5112015deaf33f1cc7b43c455979252cb4229ce6`  
		Last Modified: Mon, 08 Dec 2025 23:08:01 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096a16845b85350726e183b4d88db87ba13acb60ee984f557915e6530698cdc0`  
		Last Modified: Mon, 08 Dec 2025 23:08:01 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f872108a55e5da8edb15dc83ef4e4ddda442c2fefaaa216336fdff95619a53`  
		Last Modified: Mon, 08 Dec 2025 23:08:01 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:fee2db984b6e348bd2d9d4e0b7c813c8abbafdee7b82267b3ddf9cd0fcc7ca74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1f63c5229f30cfd0bb6e94b0d1826186d5625c7d3a7def41b434d1208ccc73`

```dockerfile
```

-	Layers:
	-	`sha256:97fc3c4f4831652a11685cf155ab34cf77e5d6a8cacdafbc5e76066588f02dbf`  
		Last Modified: Tue, 09 Dec 2025 01:39:24 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ba8b8200a6fb96006eb2254cc4a4936bb6a9a3ade3024d1a656f4611c452763`  
		Last Modified: Tue, 09 Dec 2025 01:39:27 GMT  
		Size: 15.8 KB (15773 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:97ea7ccbfc51dce51140a532c5c066044317a4b43ee68bdc8bcac8aa68d1fdd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6391d679c1c83892baa2e48c2602428242187c591ef4456e62bb9aeb82c44b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1765152000'
# Tue, 09 Dec 2025 00:08:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:08:33 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 09 Dec 2025 00:08:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 00:08:34 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 09 Dec 2025 00:08:34 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 09 Dec 2025 00:08:34 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 09 Dec 2025 00:08:34 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Dec 2025 00:08:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:08:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:08:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:189d7c8243253070696fcc5bcaa526823c4016a5dd57614057cc9107756082b2`  
		Last Modified: Mon, 08 Dec 2025 22:16:40 GMT  
		Size: 25.5 MB (25546219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e455c900371fa92aa98c035a5e00bb71ee4af963256cd6a9d0480df1f95cb1`  
		Last Modified: Tue, 09 Dec 2025 00:08:50 GMT  
		Size: 4.5 MB (4490183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2952cb7565220483af6cafcb8a14fadde48867508b5d34c925f8bc2cd2cf4dc`  
		Last Modified: Tue, 09 Dec 2025 00:08:52 GMT  
		Size: 32.5 MB (32534920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f441122822954f1e939050361aca7db7674b47bc435e4fa197d206a0fc585899`  
		Last Modified: Tue, 09 Dec 2025 00:08:49 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3caeaf92e3c5be287d9714201704563ddc5bf641981cdd6a375f65d4c3b65e`  
		Last Modified: Tue, 09 Dec 2025 00:08:49 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0bc967d9586b267b347d9085fec32e1867d4ebe6167c0055e14338ac14a203`  
		Last Modified: Tue, 09 Dec 2025 00:08:49 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:eda9c098617b45fe62406363dd45c8d1061b5da78ecc9d1bda41034eebcee474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d0de524cf3655691c3a888ba43955507eeee560a55048c6f66d33a3608221f`

```dockerfile
```

-	Layers:
	-	`sha256:f717b9a0527f54afdf458602d004042c03816efe8daeb7965377b4a41ed0df7a`  
		Last Modified: Tue, 09 Dec 2025 00:08:43 GMT  
		Size: 3.1 MB (3106782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7688a524bbc55e6ab184625368bec3b22ded1ed599a55de647174f52921b400c`  
		Last Modified: Tue, 09 Dec 2025 00:08:42 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:033cc68f77cb97a5322b9c41ccdb97a992d5feda0c8fdc5fd95013f8ccc51ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66410478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3800a045f74e853cc12ef7922d383b84f1aabcdea8149fac45b977f324e57d24`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:11:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 23:11:14 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 08 Dec 2025 23:11:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:11:14 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 08 Dec 2025 23:11:14 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 08 Dec 2025 23:11:14 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 08 Dec 2025 23:11:14 GMT
VOLUME [/var/lib/chronograf]
# Mon, 08 Dec 2025 23:11:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:11:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:11:14 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884359c65643e9aba686dbe577aafd1180f897934092a75636548e2b801c8d6a`  
		Last Modified: Mon, 08 Dec 2025 23:11:30 GMT  
		Size: 5.2 MB (5208112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ccd1383c3328356be9dfea85574a97d99c804508217ad28e537277ccf97a45`  
		Last Modified: Mon, 08 Dec 2025 23:11:33 GMT  
		Size: 32.4 MB (32429486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00d9984c0a1786a737115f63a84743b346c12d7e838476a7791237e3e168e6e`  
		Last Modified: Mon, 08 Dec 2025 23:11:29 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7f1fecd018739cef762a48929d3d16aa2c87889998179893e169f8d904647e`  
		Last Modified: Mon, 08 Dec 2025 23:11:29 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6347abdabd29977ae1988072ebbc9b58426f9d206293083a5e05e9fb98e0787`  
		Last Modified: Mon, 08 Dec 2025 23:11:29 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:bf309f9b8065e73a2d661240b36e100ecb25ea3154fed5f91070032f55cba853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7783d3cdb3d69a53779cb84d066c8ceac7f576a1aab8fa8b551b6c47bc2f9631`

```dockerfile
```

-	Layers:
	-	`sha256:fe198cdbf563cc32920cb7793d6b02a646d4f297ed876139a78a6037c5155342`  
		Last Modified: Mon, 08 Dec 2025 23:11:24 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c357eefb2c66c787382f16ea6b510dc9b171a42cb0026741021b4fc58a691b1`  
		Last Modified: Mon, 08 Dec 2025 23:11:24 GMT  
		Size: 15.9 KB (15868 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:8f246b11bed20824de500e732e0e0c1a9df2e2adcf60340444da2c4d2e7d83bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4fae84330ab9094200744d44140ff3695efc2a2085251cd4066103541bffbe5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23146498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6035189b6fd6fc001306a038b9c5678123af0b1f907f2a31efe3e96b3b689b22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaabc96984af774b48937345c7cc275e3315d3a9a42aeb994f6946de24556be`  
		Last Modified: Mon, 08 Dec 2025 07:57:14 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff81f10ae11b38f809feee3b7a44d508880916016658ca83647ff9d1c294aba`  
		Last Modified: Mon, 08 Dec 2025 07:57:14 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cf4bd3a04c4941275f4aa1db1887c01bcdadeb973d9c95d34bc905b974dce`  
		Last Modified: Mon, 08 Dec 2025 07:57:15 GMT  
		Size: 19.2 MB (19204014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4732a865d574eb12cd7075d139d6bbd7d47fea3c367baf1a1f56ff51506906fb`  
		Last Modified: Mon, 08 Dec 2025 07:57:22 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0733dea6fe6d3cf04ef8c52dec6540501fbf0e79664e84fd00853fab32410e15`  
		Last Modified: Mon, 08 Dec 2025 07:57:25 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe58005a9627e476ca3528af5a14e30f0d4549afa8e314dcde58ee7ec5fd6671`  
		Last Modified: Mon, 08 Dec 2025 07:57:47 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:07f09e7f03af9efcf88f89d7ad0f207d0e5ab57b9423663591e3c7aa0b3bc6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 KB (245253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2779ee449137493a2aca535f4363cae748d5a6c40f2c306362a97daf2d51bf6b`

```dockerfile
```

-	Layers:
	-	`sha256:4376140096bd52be7b1473ee7e7d625fff88ab2e731a2d509ed5b7861eab79fe`  
		Last Modified: Tue, 09 Dec 2025 03:48:01 GMT  
		Size: 228.3 KB (228341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61687d781240db246500ccffe6dc5608d9be7a5e7c809173a2694ffec485f7c3`  
		Last Modified: Tue, 09 Dec 2025 03:48:01 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:c8049465559dcd91cb340eabeade10b5c57804f6198b7884dc069b3e51ba8d8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:2bb2c50013ca2f46c7780fb34ccd9b8cdaa78b2a02bbc3aba45d718647eab2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69871388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2c089c48c7e92ff542f7cb514907109cbdcb80dd8124d227477aef76cf9dde`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:07:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 23:07:45 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 08 Dec 2025 23:07:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:07:45 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 08 Dec 2025 23:07:45 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 08 Dec 2025 23:07:45 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 08 Dec 2025 23:07:45 GMT
VOLUME [/var/lib/chronograf]
# Mon, 08 Dec 2025 23:07:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:07:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:07:45 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01214b21e1066bb7014cdebd05f52103da1b3c4fb49b4f34c7f02e5a8978d6b`  
		Last Modified: Mon, 08 Dec 2025 23:08:02 GMT  
		Size: 5.2 MB (5224216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec3937ad45dce7ae55bc4d785b2b4d464ebe1fc4c5f6659fc7335fc4e3f5e0a`  
		Last Modified: Mon, 08 Dec 2025 23:08:04 GMT  
		Size: 34.4 MB (34364321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c2d2713cd01965fc74dbbc5112015deaf33f1cc7b43c455979252cb4229ce6`  
		Last Modified: Mon, 08 Dec 2025 23:08:01 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096a16845b85350726e183b4d88db87ba13acb60ee984f557915e6530698cdc0`  
		Last Modified: Mon, 08 Dec 2025 23:08:01 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f872108a55e5da8edb15dc83ef4e4ddda442c2fefaaa216336fdff95619a53`  
		Last Modified: Mon, 08 Dec 2025 23:08:01 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:fee2db984b6e348bd2d9d4e0b7c813c8abbafdee7b82267b3ddf9cd0fcc7ca74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1f63c5229f30cfd0bb6e94b0d1826186d5625c7d3a7def41b434d1208ccc73`

```dockerfile
```

-	Layers:
	-	`sha256:97fc3c4f4831652a11685cf155ab34cf77e5d6a8cacdafbc5e76066588f02dbf`  
		Last Modified: Tue, 09 Dec 2025 01:39:24 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ba8b8200a6fb96006eb2254cc4a4936bb6a9a3ade3024d1a656f4611c452763`  
		Last Modified: Tue, 09 Dec 2025 01:39:27 GMT  
		Size: 15.8 KB (15773 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:97ea7ccbfc51dce51140a532c5c066044317a4b43ee68bdc8bcac8aa68d1fdd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6391d679c1c83892baa2e48c2602428242187c591ef4456e62bb9aeb82c44b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1765152000'
# Tue, 09 Dec 2025 00:08:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:08:33 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 09 Dec 2025 00:08:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 00:08:34 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 09 Dec 2025 00:08:34 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 09 Dec 2025 00:08:34 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 09 Dec 2025 00:08:34 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Dec 2025 00:08:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:08:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:08:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:189d7c8243253070696fcc5bcaa526823c4016a5dd57614057cc9107756082b2`  
		Last Modified: Mon, 08 Dec 2025 22:16:40 GMT  
		Size: 25.5 MB (25546219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e455c900371fa92aa98c035a5e00bb71ee4af963256cd6a9d0480df1f95cb1`  
		Last Modified: Tue, 09 Dec 2025 00:08:50 GMT  
		Size: 4.5 MB (4490183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2952cb7565220483af6cafcb8a14fadde48867508b5d34c925f8bc2cd2cf4dc`  
		Last Modified: Tue, 09 Dec 2025 00:08:52 GMT  
		Size: 32.5 MB (32534920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f441122822954f1e939050361aca7db7674b47bc435e4fa197d206a0fc585899`  
		Last Modified: Tue, 09 Dec 2025 00:08:49 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3caeaf92e3c5be287d9714201704563ddc5bf641981cdd6a375f65d4c3b65e`  
		Last Modified: Tue, 09 Dec 2025 00:08:49 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0bc967d9586b267b347d9085fec32e1867d4ebe6167c0055e14338ac14a203`  
		Last Modified: Tue, 09 Dec 2025 00:08:49 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:eda9c098617b45fe62406363dd45c8d1061b5da78ecc9d1bda41034eebcee474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d0de524cf3655691c3a888ba43955507eeee560a55048c6f66d33a3608221f`

```dockerfile
```

-	Layers:
	-	`sha256:f717b9a0527f54afdf458602d004042c03816efe8daeb7965377b4a41ed0df7a`  
		Last Modified: Tue, 09 Dec 2025 00:08:43 GMT  
		Size: 3.1 MB (3106782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7688a524bbc55e6ab184625368bec3b22ded1ed599a55de647174f52921b400c`  
		Last Modified: Tue, 09 Dec 2025 00:08:42 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:033cc68f77cb97a5322b9c41ccdb97a992d5feda0c8fdc5fd95013f8ccc51ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66410478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3800a045f74e853cc12ef7922d383b84f1aabcdea8149fac45b977f324e57d24`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:11:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 23:11:14 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 08 Dec 2025 23:11:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:11:14 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 08 Dec 2025 23:11:14 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 08 Dec 2025 23:11:14 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 08 Dec 2025 23:11:14 GMT
VOLUME [/var/lib/chronograf]
# Mon, 08 Dec 2025 23:11:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:11:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:11:14 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884359c65643e9aba686dbe577aafd1180f897934092a75636548e2b801c8d6a`  
		Last Modified: Mon, 08 Dec 2025 23:11:30 GMT  
		Size: 5.2 MB (5208112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ccd1383c3328356be9dfea85574a97d99c804508217ad28e537277ccf97a45`  
		Last Modified: Mon, 08 Dec 2025 23:11:33 GMT  
		Size: 32.4 MB (32429486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00d9984c0a1786a737115f63a84743b346c12d7e838476a7791237e3e168e6e`  
		Last Modified: Mon, 08 Dec 2025 23:11:29 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7f1fecd018739cef762a48929d3d16aa2c87889998179893e169f8d904647e`  
		Last Modified: Mon, 08 Dec 2025 23:11:29 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6347abdabd29977ae1988072ebbc9b58426f9d206293083a5e05e9fb98e0787`  
		Last Modified: Mon, 08 Dec 2025 23:11:29 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:bf309f9b8065e73a2d661240b36e100ecb25ea3154fed5f91070032f55cba853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7783d3cdb3d69a53779cb84d066c8ceac7f576a1aab8fa8b551b6c47bc2f9631`

```dockerfile
```

-	Layers:
	-	`sha256:fe198cdbf563cc32920cb7793d6b02a646d4f297ed876139a78a6037c5155342`  
		Last Modified: Mon, 08 Dec 2025 23:11:24 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c357eefb2c66c787382f16ea6b510dc9b171a42cb0026741021b4fc58a691b1`  
		Last Modified: Mon, 08 Dec 2025 23:11:24 GMT  
		Size: 15.9 KB (15868 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:8f246b11bed20824de500e732e0e0c1a9df2e2adcf60340444da2c4d2e7d83bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4fae84330ab9094200744d44140ff3695efc2a2085251cd4066103541bffbe5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23146498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6035189b6fd6fc001306a038b9c5678123af0b1f907f2a31efe3e96b3b689b22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaabc96984af774b48937345c7cc275e3315d3a9a42aeb994f6946de24556be`  
		Last Modified: Mon, 08 Dec 2025 07:57:14 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff81f10ae11b38f809feee3b7a44d508880916016658ca83647ff9d1c294aba`  
		Last Modified: Mon, 08 Dec 2025 07:57:14 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cf4bd3a04c4941275f4aa1db1887c01bcdadeb973d9c95d34bc905b974dce`  
		Last Modified: Mon, 08 Dec 2025 07:57:15 GMT  
		Size: 19.2 MB (19204014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4732a865d574eb12cd7075d139d6bbd7d47fea3c367baf1a1f56ff51506906fb`  
		Last Modified: Mon, 08 Dec 2025 07:57:22 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0733dea6fe6d3cf04ef8c52dec6540501fbf0e79664e84fd00853fab32410e15`  
		Last Modified: Mon, 08 Dec 2025 07:57:25 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe58005a9627e476ca3528af5a14e30f0d4549afa8e314dcde58ee7ec5fd6671`  
		Last Modified: Mon, 08 Dec 2025 07:57:47 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:07f09e7f03af9efcf88f89d7ad0f207d0e5ab57b9423663591e3c7aa0b3bc6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 KB (245253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2779ee449137493a2aca535f4363cae748d5a6c40f2c306362a97daf2d51bf6b`

```dockerfile
```

-	Layers:
	-	`sha256:4376140096bd52be7b1473ee7e7d625fff88ab2e731a2d509ed5b7861eab79fe`  
		Last Modified: Tue, 09 Dec 2025 03:48:01 GMT  
		Size: 228.3 KB (228341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61687d781240db246500ccffe6dc5608d9be7a5e7c809173a2694ffec485f7c3`  
		Last Modified: Tue, 09 Dec 2025 03:48:01 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:4f393401233c18f91df39334370754425f02c9fd2fddf35d79e16a6986ac230b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:eccfe44c00d477977abfd30f6cd9a40f7941f4c46d09332d06e84ddd5b0380a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a962139ba91e653dd6af11e289a94ed5ad3deb672adc189407dcbf90dee94b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:08:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 23:08:04 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 08 Dec 2025 23:08:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:08:04 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 08 Dec 2025 23:08:04 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 08 Dec 2025 23:08:04 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 08 Dec 2025 23:08:04 GMT
VOLUME [/var/lib/chronograf]
# Mon, 08 Dec 2025 23:08:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:08:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:08:04 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f4e6e0e421f31271e061ac0c56a7eb00fac89c4b230bd1ce9df044d11aae03`  
		Last Modified: Mon, 08 Dec 2025 23:08:22 GMT  
		Size: 5.2 MB (5224265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040725f4071b999f88ba66d1cf023bc666202104aa4102c02d923d77f90b8703`  
		Last Modified: Mon, 08 Dec 2025 23:08:28 GMT  
		Size: 35.0 MB (35011811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d465621e0086a658d9c22b82d054717d62ae543ae92ce921c6251111c094d879`  
		Last Modified: Mon, 08 Dec 2025 23:08:21 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1a4e66dea5b5cecfef689fd08ba38740de1efd3d8cf645465ee03adb77da42`  
		Last Modified: Mon, 08 Dec 2025 23:08:21 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6700560a76849b3c1cdcee91a8bf2fb65c0842aba7625756ebbeaf86f4e7ce8e`  
		Last Modified: Mon, 08 Dec 2025 23:08:22 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:95c2f713bac3b9fdcf4590cb11f804390faa86c370a889c72b70099b05cd53fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b543d85496092f4f2f33ab7821b89c5c5f80451ed4ddfb3842138f06ff6c44e`

```dockerfile
```

-	Layers:
	-	`sha256:8cd9c0921cf5ef8dc3f3ed28c24b0f26ea4e1e907e33baeb6c6a552acd2862a5`  
		Last Modified: Tue, 09 Dec 2025 01:39:36 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:735e0a1f40045210d8c827761821b6b4d0941a2b252d4c2b02c95aa80f3e849f`  
		Last Modified: Tue, 09 Dec 2025 01:39:37 GMT  
		Size: 15.8 KB (15767 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:7e66d90d8769acf7ed47229b6d2c9df65b47a49d16ee3633f8a684c26798e77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63372393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ab6570134d1296f9b19e1459cedca0cb4ea5fc94f2f0b3e23dad6483555abb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1765152000'
# Tue, 09 Dec 2025 00:08:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:09:04 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 09 Dec 2025 00:09:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 00:09:04 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 09 Dec 2025 00:09:05 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 09 Dec 2025 00:09:05 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 09 Dec 2025 00:09:05 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Dec 2025 00:09:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:09:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:09:05 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:189d7c8243253070696fcc5bcaa526823c4016a5dd57614057cc9107756082b2`  
		Last Modified: Mon, 08 Dec 2025 22:16:40 GMT  
		Size: 25.5 MB (25546219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e455c900371fa92aa98c035a5e00bb71ee4af963256cd6a9d0480df1f95cb1`  
		Last Modified: Tue, 09 Dec 2025 00:08:50 GMT  
		Size: 4.5 MB (4490183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8f62ef34593fd70cd1062ae80c95486cf8c09bb3187632814b2c5f85976a12`  
		Last Modified: Tue, 09 Dec 2025 00:09:24 GMT  
		Size: 33.3 MB (33311608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bceebdc91c4a4044149be600f69b8f6110340fe61e751387422d3792caf814`  
		Last Modified: Tue, 09 Dec 2025 00:09:19 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd96f98db44930b77cb2611315b798b5abd85cfbf42927382950fb953f1adc29`  
		Last Modified: Tue, 09 Dec 2025 00:09:19 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a780cfaee5dc48bdd8c5644e81daf29abf9bd702bdc6031aecb3fbd031d746`  
		Last Modified: Tue, 09 Dec 2025 00:09:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:bad4313b6691d8f85f662ecee3a1beb771054cf756b88352b12d164e42f98f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789c64c54011b7b9afcd39c57c6097370e1095cccdd1469f05b9349a7a9bdda2`

```dockerfile
```

-	Layers:
	-	`sha256:0999efa4657262c0b18867d0c2f6ef883f97fd1e8553093ba4e378a579fa9ffb`  
		Last Modified: Tue, 09 Dec 2025 01:39:41 GMT  
		Size: 3.1 MB (3111992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1699a68807dbaf6f1d20aef89c939ce0071984566e04c14541861745c884f476`  
		Last Modified: Tue, 09 Dec 2025 01:39:42 GMT  
		Size: 15.8 KB (15842 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:cb33ee99ff3b9b315a398a34c26e9cbb157e9ebbbf0eb46684f8a2784ad620cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67163248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439ae44e06358fcf310bfc612bcac9ea67287204fe037847241b7c76e1a0d84a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:11:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 08 Dec 2025 23:11:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 08 Dec 2025 23:11:41 GMT
VOLUME [/var/lib/chronograf]
# Mon, 08 Dec 2025 23:11:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:11:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70eb5d899e0a5a5d0a6d13889555b139eacdd568f851440adff0c539f5dd6e3`  
		Last Modified: Mon, 08 Dec 2025 23:12:00 GMT  
		Size: 5.2 MB (5208214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1df79eda7b4be2c077f0de9e120212df915866ad36fb8b1f7c592cea00fb512`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 33.2 MB (33182170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8222bfd6cd667342b53cf44cb9a8a5153c35a1a666d1860840cb2a3402eef65`  
		Last Modified: Mon, 08 Dec 2025 23:12:00 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2980321dc9b67585a126c243402c6afbc0be8e349eda4da49ca9603ec32f0310`  
		Last Modified: Mon, 08 Dec 2025 23:12:00 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5790201855ee0cc99dbeef35085ab713565838485c33b19b90d6af9a32ae297`  
		Last Modified: Mon, 08 Dec 2025 23:12:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:d6f4f026b049061da1a1cdd86e94fa6d6ecdd4c472302f342b34315a061c4f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4637de337edaa09d1f816c46ae8680038ee9099d888045b8ea916c63cf6c1b60`

```dockerfile
```

-	Layers:
	-	`sha256:7ff85c57c9e2cf63797fbbe1bb6a0406bc988123353ad1f8b2f5dc53a9817d78`  
		Last Modified: Tue, 09 Dec 2025 04:38:45 GMT  
		Size: 3.1 MB (3109970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c583ffb4ec430a9354bde05ec8bab0bd8a3d92c991f37e832fcaa43f7f75a179`  
		Last Modified: Tue, 09 Dec 2025 04:38:46 GMT  
		Size: 15.9 KB (15862 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:b3fee5aad5c22c71cb04bbd41eea4af839aeb7d359a82d9b4233795d4cee5130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:2d4252cb73b369cd488e239afeef5f7a6b44a46a01cfe8ab7d068d6397d5311d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23614563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9964a18d639210346c0ff7c26e65b91960ad4afbf36654d3a88e1c03026a1437`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d70c842384492021fdcd617e3e57dbc08546ebeb0a55cf5f01aa575170280c6`  
		Last Modified: Mon, 08 Dec 2025 00:01:59 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6c508c6ab14eb797ff6524630894eea223ff1b5a3f02be3595aff5713c5112`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43383a0cdbbe70773cd822a7089d90f254cc6923262bc86a209c0c182a190472`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 19.7 MB (19672095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11524f4d626f224d1faadbb2537a398d423351e2a0d854a4a43b4692fab631c6`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811766d26cc20ed9c9dee509c4ef17aa945fbbf00be418890deec226cbeae620`  
		Last Modified: Wed, 08 Oct 2025 23:01:19 GMT  
		Size: 11.9 KB (11888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90296708765453bd34d3b31917ee366ec4e86d0d341504ddd046c032d6f85842`  
		Last Modified: Wed, 08 Oct 2025 23:01:19 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:c5e372192d09b31155c48fb1472089780f956a2cdeba37b4eda3358869e38aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 KB (250462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad16fab4bfdaa94339daa5b35ee736124878a90af7d436293dd5657f43ac1f79`

```dockerfile
```

-	Layers:
	-	`sha256:6ed1879bf7ef8eb915186029d90ae2f6c3d14aa17bd74c3708035ff07dfcc75e`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 233.6 KB (233553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5586220b931721e2b29f86f48af9fa3579d18c357b0351f043fc2e76a05ebc52`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:4f393401233c18f91df39334370754425f02c9fd2fddf35d79e16a6986ac230b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:eccfe44c00d477977abfd30f6cd9a40f7941f4c46d09332d06e84ddd5b0380a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a962139ba91e653dd6af11e289a94ed5ad3deb672adc189407dcbf90dee94b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:08:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 23:08:04 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 08 Dec 2025 23:08:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:08:04 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 08 Dec 2025 23:08:04 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 08 Dec 2025 23:08:04 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 08 Dec 2025 23:08:04 GMT
VOLUME [/var/lib/chronograf]
# Mon, 08 Dec 2025 23:08:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:08:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:08:04 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f4e6e0e421f31271e061ac0c56a7eb00fac89c4b230bd1ce9df044d11aae03`  
		Last Modified: Mon, 08 Dec 2025 23:08:22 GMT  
		Size: 5.2 MB (5224265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040725f4071b999f88ba66d1cf023bc666202104aa4102c02d923d77f90b8703`  
		Last Modified: Mon, 08 Dec 2025 23:08:28 GMT  
		Size: 35.0 MB (35011811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d465621e0086a658d9c22b82d054717d62ae543ae92ce921c6251111c094d879`  
		Last Modified: Mon, 08 Dec 2025 23:08:21 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1a4e66dea5b5cecfef689fd08ba38740de1efd3d8cf645465ee03adb77da42`  
		Last Modified: Mon, 08 Dec 2025 23:08:21 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6700560a76849b3c1cdcee91a8bf2fb65c0842aba7625756ebbeaf86f4e7ce8e`  
		Last Modified: Mon, 08 Dec 2025 23:08:22 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:95c2f713bac3b9fdcf4590cb11f804390faa86c370a889c72b70099b05cd53fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b543d85496092f4f2f33ab7821b89c5c5f80451ed4ddfb3842138f06ff6c44e`

```dockerfile
```

-	Layers:
	-	`sha256:8cd9c0921cf5ef8dc3f3ed28c24b0f26ea4e1e907e33baeb6c6a552acd2862a5`  
		Last Modified: Tue, 09 Dec 2025 01:39:36 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:735e0a1f40045210d8c827761821b6b4d0941a2b252d4c2b02c95aa80f3e849f`  
		Last Modified: Tue, 09 Dec 2025 01:39:37 GMT  
		Size: 15.8 KB (15767 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:7e66d90d8769acf7ed47229b6d2c9df65b47a49d16ee3633f8a684c26798e77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63372393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ab6570134d1296f9b19e1459cedca0cb4ea5fc94f2f0b3e23dad6483555abb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1765152000'
# Tue, 09 Dec 2025 00:08:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:09:04 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 09 Dec 2025 00:09:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 00:09:04 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 09 Dec 2025 00:09:05 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 09 Dec 2025 00:09:05 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 09 Dec 2025 00:09:05 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Dec 2025 00:09:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:09:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:09:05 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:189d7c8243253070696fcc5bcaa526823c4016a5dd57614057cc9107756082b2`  
		Last Modified: Mon, 08 Dec 2025 22:16:40 GMT  
		Size: 25.5 MB (25546219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e455c900371fa92aa98c035a5e00bb71ee4af963256cd6a9d0480df1f95cb1`  
		Last Modified: Tue, 09 Dec 2025 00:08:50 GMT  
		Size: 4.5 MB (4490183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8f62ef34593fd70cd1062ae80c95486cf8c09bb3187632814b2c5f85976a12`  
		Last Modified: Tue, 09 Dec 2025 00:09:24 GMT  
		Size: 33.3 MB (33311608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bceebdc91c4a4044149be600f69b8f6110340fe61e751387422d3792caf814`  
		Last Modified: Tue, 09 Dec 2025 00:09:19 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd96f98db44930b77cb2611315b798b5abd85cfbf42927382950fb953f1adc29`  
		Last Modified: Tue, 09 Dec 2025 00:09:19 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a780cfaee5dc48bdd8c5644e81daf29abf9bd702bdc6031aecb3fbd031d746`  
		Last Modified: Tue, 09 Dec 2025 00:09:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:bad4313b6691d8f85f662ecee3a1beb771054cf756b88352b12d164e42f98f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789c64c54011b7b9afcd39c57c6097370e1095cccdd1469f05b9349a7a9bdda2`

```dockerfile
```

-	Layers:
	-	`sha256:0999efa4657262c0b18867d0c2f6ef883f97fd1e8553093ba4e378a579fa9ffb`  
		Last Modified: Tue, 09 Dec 2025 01:39:41 GMT  
		Size: 3.1 MB (3111992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1699a68807dbaf6f1d20aef89c939ce0071984566e04c14541861745c884f476`  
		Last Modified: Tue, 09 Dec 2025 01:39:42 GMT  
		Size: 15.8 KB (15842 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:cb33ee99ff3b9b315a398a34c26e9cbb157e9ebbbf0eb46684f8a2784ad620cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67163248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439ae44e06358fcf310bfc612bcac9ea67287204fe037847241b7c76e1a0d84a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:11:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 08 Dec 2025 23:11:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 08 Dec 2025 23:11:41 GMT
VOLUME [/var/lib/chronograf]
# Mon, 08 Dec 2025 23:11:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:11:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70eb5d899e0a5a5d0a6d13889555b139eacdd568f851440adff0c539f5dd6e3`  
		Last Modified: Mon, 08 Dec 2025 23:12:00 GMT  
		Size: 5.2 MB (5208214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1df79eda7b4be2c077f0de9e120212df915866ad36fb8b1f7c592cea00fb512`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 33.2 MB (33182170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8222bfd6cd667342b53cf44cb9a8a5153c35a1a666d1860840cb2a3402eef65`  
		Last Modified: Mon, 08 Dec 2025 23:12:00 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2980321dc9b67585a126c243402c6afbc0be8e349eda4da49ca9603ec32f0310`  
		Last Modified: Mon, 08 Dec 2025 23:12:00 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5790201855ee0cc99dbeef35085ab713565838485c33b19b90d6af9a32ae297`  
		Last Modified: Mon, 08 Dec 2025 23:12:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:d6f4f026b049061da1a1cdd86e94fa6d6ecdd4c472302f342b34315a061c4f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4637de337edaa09d1f816c46ae8680038ee9099d888045b8ea916c63cf6c1b60`

```dockerfile
```

-	Layers:
	-	`sha256:7ff85c57c9e2cf63797fbbe1bb6a0406bc988123353ad1f8b2f5dc53a9817d78`  
		Last Modified: Tue, 09 Dec 2025 04:38:45 GMT  
		Size: 3.1 MB (3109970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c583ffb4ec430a9354bde05ec8bab0bd8a3d92c991f37e832fcaa43f7f75a179`  
		Last Modified: Tue, 09 Dec 2025 04:38:46 GMT  
		Size: 15.9 KB (15862 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:b3fee5aad5c22c71cb04bbd41eea4af839aeb7d359a82d9b4233795d4cee5130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:2d4252cb73b369cd488e239afeef5f7a6b44a46a01cfe8ab7d068d6397d5311d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23614563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9964a18d639210346c0ff7c26e65b91960ad4afbf36654d3a88e1c03026a1437`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d70c842384492021fdcd617e3e57dbc08546ebeb0a55cf5f01aa575170280c6`  
		Last Modified: Mon, 08 Dec 2025 00:01:59 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6c508c6ab14eb797ff6524630894eea223ff1b5a3f02be3595aff5713c5112`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43383a0cdbbe70773cd822a7089d90f254cc6923262bc86a209c0c182a190472`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 19.7 MB (19672095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11524f4d626f224d1faadbb2537a398d423351e2a0d854a4a43b4692fab631c6`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811766d26cc20ed9c9dee509c4ef17aa945fbbf00be418890deec226cbeae620`  
		Last Modified: Wed, 08 Oct 2025 23:01:19 GMT  
		Size: 11.9 KB (11888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90296708765453bd34d3b31917ee366ec4e86d0d341504ddd046c032d6f85842`  
		Last Modified: Wed, 08 Oct 2025 23:01:19 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:c5e372192d09b31155c48fb1472089780f956a2cdeba37b4eda3358869e38aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 KB (250462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad16fab4bfdaa94339daa5b35ee736124878a90af7d436293dd5657f43ac1f79`

```dockerfile
```

-	Layers:
	-	`sha256:6ed1879bf7ef8eb915186029d90ae2f6c3d14aa17bd74c3708035ff07dfcc75e`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 233.6 KB (233553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5586220b931721e2b29f86f48af9fa3579d18c357b0351f043fc2e76a05ebc52`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:efc72c285cae492b0fb820a7794f2da69a70ef77caa8d28282e0df6f79856029
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:08463b31a0a2617a51e230161f997b525214640155e291a423ae53004330c719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32700225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af178eb7af41f52d85b69957fc583d381f6a24a9e604b40818766ecf3004a1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08cd1461c07b6d2b803ff1e365582cea280da85884cb0fe20c1b539046e9c0f`  
		Last Modified: Mon, 08 Dec 2025 02:53:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642952c8832a913bc8124d8c1f9800b4c40ed32aa2d21f4bbd9c85e32729fdf2`  
		Last Modified: Mon, 08 Dec 2025 02:53:47 GMT  
		Size: 314.6 KB (314639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff188fbd44ef51d6c15c61b590915a7d108294cea3cebd1224f569cf88dbfbd2`  
		Last Modified: Mon, 08 Dec 2025 02:53:50 GMT  
		Size: 28.6 MB (28558408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ada6ea712a91804f080e3ac3a6fec72f1bf330d8affb0a76902b1f0b78a5046`  
		Last Modified: Mon, 08 Dec 2025 02:53:48 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322d214c5daa6878e468360de897da9cd0cad1be05283f5529b5e2ce07c9e72f`  
		Last Modified: Mon, 08 Dec 2025 02:53:48 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175f9d62a6d73ab836332ca97429aec6104967dc35d5ab6aaa103f374c1539bd`  
		Last Modified: Mon, 08 Dec 2025 02:53:49 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:dd3236bd7a2263357f0c7258a9a36c7fef283fd9f58f17f5fc2cbfa8330df313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 KB (268238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808a56c94ce865ff68fe325760f90b15b31758031ea028455935f57e4d2afe56`

```dockerfile
```

-	Layers:
	-	`sha256:d62aac69b78bc656cc8510a0566537353a4cda897cdaf124ca24ad68c0fa7fb1`  
		Last Modified: Mon, 08 Dec 2025 03:44:43 GMT  
		Size: 250.4 KB (250383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c7ffc31e817e3fff1eade663dcae6dc3da5bb4370e43abaf921eebc9dd7f0a1`  
		Last Modified: Mon, 08 Dec 2025 03:44:44 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:3fbfcc3a6c9d72e1b7765dd3a8617f26653cbde2babd26fd1f1bbf6f6a42922e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:c594743eb2d70ae09c739c7f93f920ea5f8e2258327cdaf71c148f833399f8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e9db47282885f54445b4d03fe07231a41e1f4f772bceb462bdd39de558bc8e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:07:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 23:08:06 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Mon, 08 Dec 2025 23:08:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:08:06 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 08 Dec 2025 23:08:06 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 08 Dec 2025 23:08:06 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 08 Dec 2025 23:08:06 GMT
VOLUME [/var/lib/chronograf]
# Mon, 08 Dec 2025 23:08:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:08:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:08:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b906813b3c7a1bc726013079d276cd811916f16af222a4ed7269ef82a3804e59`  
		Last Modified: Mon, 08 Dec 2025 23:08:25 GMT  
		Size: 7.9 MB (7878852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc666d4835937e2220b9396c52bd685f7545872a63881e132dcfcc540e550a1`  
		Last Modified: Mon, 08 Dec 2025 23:08:28 GMT  
		Size: 49.3 MB (49276694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537dd4e73ab9539d97d15157388ba9eedb176847cdfb06fc9f04d8af4f3ff935`  
		Last Modified: Mon, 08 Dec 2025 23:08:24 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1039be48ca2a044e939d7a8ec44d50c0aee42328b0e094acfb5742f4a5e07b2c`  
		Last Modified: Mon, 08 Dec 2025 23:08:24 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a52c4ea51584a7918b2aab6e64828c05d85e2390bd3e2db89beb7e0d3cc3a2`  
		Last Modified: Mon, 08 Dec 2025 23:08:26 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:5ed955d5b41a4ca8c8686a747cad5e2136cc7c213c5052ef3e3e4352df9c4e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33606a1852dc6f5af831d9cb1239547a04661b51b8ff432785af1782dd8d741`

```dockerfile
```

-	Layers:
	-	`sha256:662a9044cb1e525ac17b3c81c0708e9c00bf781da0acf6cfa174985604359918`  
		Last Modified: Tue, 09 Dec 2025 01:38:55 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e87e18c4c0dd20814ec877db8a5ac05ec20762fa6ab91c57f2c6a031ef91ea69`  
		Last Modified: Tue, 09 Dec 2025 01:38:56 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:a9eee760c300ed74ee00152e204aeb74c6f76614d290fb956a0b0cada62bda71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76088485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbb5df25cb1608648b241d8634ce8c1411ab2e8501ed6abdfe11cf19d123c8d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:10:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:10:36 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 09 Dec 2025 00:10:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 00:10:36 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 09 Dec 2025 00:10:36 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 09 Dec 2025 00:10:36 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 09 Dec 2025 00:10:36 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Dec 2025 00:10:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:10:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:10:36 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15653d8ecaaadc3f2ca2a299e2702e2799dde21b5d7a9a157da62081d255895`  
		Last Modified: Tue, 09 Dec 2025 00:10:58 GMT  
		Size: 6.5 MB (6508169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af2847cc0300fea9798f3dda808d44a9b4b4a05e7c6e019b961216aed8791ee`  
		Last Modified: Tue, 09 Dec 2025 00:11:04 GMT  
		Size: 45.6 MB (45621825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d392f4402076132ae69246cf56715e534f4a4d4cf3ca27073a1ec0fe3cddf2b`  
		Last Modified: Tue, 09 Dec 2025 00:11:00 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97486948da4815691f7338de8bcb0f809d2de68ef3644528121a1b79a86054d4`  
		Last Modified: Tue, 09 Dec 2025 00:10:58 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8db7b8a1e9e7447dca72eeecc6a7dff0bf8746c5df349f7d2cd3fbce33311b5`  
		Last Modified: Tue, 09 Dec 2025 00:10:58 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:42c0504831fd00f642f77e1347e342ce1f8a491c9783b1d6cd2a0c1844fd4b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7158fba3b2d6bab026e84ed139ec0a33375ad427c587cc7f4715fa5f8ca14411`

```dockerfile
```

-	Layers:
	-	`sha256:75f34ec3a9cae186aded26cf43ddceacb375351828a69aa13b33c73daba78ea8`  
		Last Modified: Tue, 09 Dec 2025 01:39:00 GMT  
		Size: 2.9 MB (2856371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80697cb76ffad47e142ce75fd04a0907f851f27a0a85d6b6e896c1ad80f10b53`  
		Last Modified: Tue, 09 Dec 2025 01:39:01 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:87ab5c23ab1a4c827c6a9b34d360c43e829d7d06099af1f5c5d1a871e998ae0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e45d4f9fdaae74ec9f04cd4921c414fd6de0a04451ff20d55b5636b612298c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:11:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 23:11:40 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Mon, 08 Dec 2025 23:11:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 08 Dec 2025 23:11:41 GMT
VOLUME [/var/lib/chronograf]
# Mon, 08 Dec 2025 23:11:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:11:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:11:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc423e736d4142acab17607c7d704550cfc05ad1c695f77c250684aae7a09bf6`  
		Last Modified: Mon, 08 Dec 2025 23:12:01 GMT  
		Size: 7.7 MB (7691839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b597abbe4c4905b7ab605402dfcc46262acda2dd39a8915607a2f20b19cad0`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 47.1 MB (47066807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778b97fcbd0bd3bb26271f20f6bfeb70e3eeba84b57b3644a7a44d3077181010`  
		Last Modified: Mon, 08 Dec 2025 23:12:00 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e164a20ab4b35b55ce2c689cba71f953a2f2bfc932eb157a8325a5015a85cfe`  
		Last Modified: Mon, 08 Dec 2025 23:12:00 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e44701a97eeac8bf17ee2dcec6d77bd75ec0f0f2af22fc55408552a7950e22`  
		Last Modified: Mon, 08 Dec 2025 23:12:00 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:8c9bdcf49bc1033ebd11f9fc95668cc1860c67717b36ba5d5d5ec54e3c319c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d959dc1f6ed009446107a9ada80e7f9ee95082f6bc9189c63b98b24c571e683a`

```dockerfile
```

-	Layers:
	-	`sha256:2e78cf8d179bf6aa7db8b2ae7a6b8a4473e962ccf8809ae85db1c5d75af8f8b0`  
		Last Modified: Tue, 09 Dec 2025 01:39:06 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9565350ae9696c60f4ce5ef731af5798064640086fed3a1eb67df68a2ddd7363`  
		Last Modified: Tue, 09 Dec 2025 01:39:06 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json
