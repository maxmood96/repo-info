<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.7`](#chronograf1107)
-	[`chronograf:1.10.7-alpine`](#chronograf1107-alpine)
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
$ docker pull chronograf@sha256:f6ef7852b2257d0e7756589757627a50d2bb6ce74c4abf3c7e4297483f52b7f8
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
$ docker pull chronograf@sha256:7dd16daa289079744a3485a5dc1f9c4d1b42fecd1c091ac8c1d060658407316a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85361259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01bfcfdf38b10aa4664a875462af00c39c7f6e34a93c9736540134e2bc239b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.10.7
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d948a6e444038248d3837d2e8bb8e9f5e347ce21fe67592ddea6c9636511d6f4`  
		Last Modified: Thu, 08 May 2025 17:47:22 GMT  
		Size: 7.9 MB (7875415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7b2f54616466e283cb5bdb7c5192c06c8a43136da9bb6c0c13ab2018dad9d9`  
		Last Modified: Thu, 08 May 2025 17:47:25 GMT  
		Size: 49.2 MB (49233737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ded7601090ccd78e1baae3c56e7ad4c6b68a4d47cb778c98699674602e64b2`  
		Last Modified: Thu, 08 May 2025 17:47:21 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf9cdfbc80b60b5c327f81fec79b30bfd2450f2f23ed002d7d5e63ed4733f33`  
		Last Modified: Thu, 08 May 2025 17:47:22 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c7ee215395492598d52c252485f37e9039a61a48d0d0fb41af03be3a62d516`  
		Last Modified: Thu, 08 May 2025 17:47:22 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:ba793e2f75ea28a7dbd2d1b3b0d61d7cf41106200aa00db12355a6592706cd34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00aafccdf15c39046c13083c2fff37f46e3cc03c62ecdc4dbab730297fdd6639`

```dockerfile
```

-	Layers:
	-	`sha256:f1be7e3349428f3b74e918ce10522157cd3695f6a43cecb7e501641bee8edb82`  
		Last Modified: Mon, 28 Apr 2025 21:55:43 GMT  
		Size: 2.7 MB (2704173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db1d5b909ceaa65802b09fa72f781272a332d157a79826d4971e5fddf194bc4e`  
		Last Modified: Mon, 28 Apr 2025 21:55:43 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d992d8064ea3aad5c61f05876d3d5f9b27f9caf4853f85c70115ff5b4cc7ae47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76025160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da52e8ccf76be4f48112c327593ba48cc696024c71fad43e6ae8b1126d10724c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.10.7
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Thu, 08 May 2025 17:05:07 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97cc1bc73cdd53d1fb65b54eb2237cb2d74423ba085e2b4becb0d0fec7905be`  
		Last Modified: Fri, 09 May 2025 02:58:40 GMT  
		Size: 6.5 MB (6497913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44517418a9729926f5d635549a4bd6176f13585afd47adb69f7c8b08e74c693a`  
		Last Modified: Fri, 09 May 2025 01:20:25 GMT  
		Size: 45.6 MB (45564703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5462df3243fd46d86ee7086f625bec52780ef4a05deaa42a8e4083e43f8907bf`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d817a3e3afb21bf13b393479698fe8c14f39f2e3b20100e747706b51f9ccd6e`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103414f6d083444387facc3936ec4c26348ad1954d8a891d00fa696bf2469258`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:c424dca1169ea1980d8fe4891c7075b2692db626aa001bc8823714a7922df094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab36315c728813f16e98f9c535baaad3f4a8addd707f1171e03623d893f4dafd`

```dockerfile
```

-	Layers:
	-	`sha256:76c614e1be50a565a7207409c707c416355ea43389084da3c9088bc6b51a6bae`  
		Last Modified: Tue, 29 Apr 2025 03:42:01 GMT  
		Size: 2.7 MB (2706470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eafd7093a3f3afb7cf09e97668195e911eb6927ef0f6699fe685e894611f0791`  
		Last Modified: Tue, 29 Apr 2025 03:42:01 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:45bd113eb85e7c27fedf83a7a9313e66d29cdc60dc9604f04b8da0e89567a04a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82763754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf23023139d2a5bba31fefbde296786407516e54bd44429fe5e3517c7627f3da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.10.7
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687d6d5f2d0622b294a8ce4c8f55da85356ba61e9a9ddecaa09b12c45f5dc71b`  
		Last Modified: Thu, 08 May 2025 17:56:48 GMT  
		Size: 7.7 MB (7652116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d52f1039bbb6fba3a0e7fc09bf372afbfc17d60d1bcd56c4659f0045214bbcf`  
		Last Modified: Thu, 08 May 2025 17:56:53 GMT  
		Size: 47.0 MB (47020557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9028c3e134f78f6ced2c1fc90dfc47fdb06ef46ccb86f256ce6507c93d0dacc`  
		Last Modified: Thu, 08 May 2025 17:56:47 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb7f61774f9814fa36e7925e9db6154efe72e897177610f87539565ae136d52`  
		Last Modified: Thu, 08 May 2025 17:56:48 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98fc839e4715c63a63e686672b0df5d47e4674fffc5f611891d705038ce7b65`  
		Last Modified: Thu, 08 May 2025 17:56:54 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:2b906c51825ebb95a9dc2c20a92a02cd282237452e5dd08e795b8fed5cb95a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a4bb964b36817b761823beb95bd7a1cf2d7be749bc8ac3013b70003e81696a`

```dockerfile
```

-	Layers:
	-	`sha256:aa39a818f83b457c77e9ed04b7dcdee0288b378f1c5bdaf38944c955f3dcb32b`  
		Last Modified: Tue, 29 Apr 2025 01:50:04 GMT  
		Size: 2.7 MB (2704446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b99ea6e4585f33d2ac9e33b0ef61919a71762bf46928bc59fb30ae003b16e0`  
		Last Modified: Tue, 29 Apr 2025 01:50:03 GMT  
		Size: 16.2 KB (16234 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:e7ff1d3334696cbcf6faf91a64d45738b8daeaf63314fadc96c1a56c7fd20edf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c0ef21afbcd6bda572425dc4d8e041cfa055ed3164a8e286f2f616da5ab1a4dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32473370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f884624fe4a2eb691052a7a35ced9a118b8b5650b1595cfe1749f87aa15bcd7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.10.7
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32870b6e9c13c57b3e4492e862a1cbd13fa1a832304155c5f64e44173ac7210a`  
		Last Modified: Thu, 08 May 2025 19:49:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b6cec5e7cadf8751915b4bf4bd5d891cfe0949da529d90ae52a376a6dd2f2`  
		Last Modified: Thu, 08 May 2025 19:49:22 GMT  
		Size: 296.5 KB (296501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385cb22c2e9fc67ba1ab880b4400b1ea27a4aaaa54082ef5c2bf93e2b1dfe26a`  
		Last Modified: Thu, 08 May 2025 19:49:31 GMT  
		Size: 28.5 MB (28525260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a0e6e70a2efdf0942ca9130a6373a2a8aba0e8d0220d1d25700421f387b216`  
		Last Modified: Thu, 08 May 2025 19:49:23 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70db9642e4277afac9c14dfb2b300c68da5b2cb5ffb4fe1820dd613997f944`  
		Last Modified: Thu, 08 May 2025 19:49:23 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cd8a31daaa972542ed9037d7b7b3ef390e0cb3be4e346df11439e64cb47419`  
		Last Modified: Thu, 08 May 2025 19:49:23 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:b6a6d39e20abbc3db33205d680f93a1d19657299aa2b0b48b8d5cc77a9837a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 KB (258396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e58e4c4963b9d8238a6d2a1125754474bbfbfb5e32bb8aa8cba8fcac7db72c3`

```dockerfile
```

-	Layers:
	-	`sha256:5195b085c22b585bbb874c8273bee971bfc5088c086391d9ae9c8cb92b96f599`  
		Last Modified: Wed, 16 Apr 2025 16:54:32 GMT  
		Size: 240.5 KB (240541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfdd35f7cb83c7a7195c2e7e30f801140fb9d8c443199e4d501a3a9211b8d82b`  
		Last Modified: Wed, 16 Apr 2025 16:54:32 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.7`

```console
$ docker pull chronograf@sha256:f6ef7852b2257d0e7756589757627a50d2bb6ce74c4abf3c7e4297483f52b7f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10.7` - linux; amd64

```console
$ docker pull chronograf@sha256:7dd16daa289079744a3485a5dc1f9c4d1b42fecd1c091ac8c1d060658407316a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85361259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01bfcfdf38b10aa4664a875462af00c39c7f6e34a93c9736540134e2bc239b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.10.7
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d948a6e444038248d3837d2e8bb8e9f5e347ce21fe67592ddea6c9636511d6f4`  
		Last Modified: Thu, 08 May 2025 17:47:22 GMT  
		Size: 7.9 MB (7875415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7b2f54616466e283cb5bdb7c5192c06c8a43136da9bb6c0c13ab2018dad9d9`  
		Last Modified: Thu, 08 May 2025 17:47:25 GMT  
		Size: 49.2 MB (49233737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ded7601090ccd78e1baae3c56e7ad4c6b68a4d47cb778c98699674602e64b2`  
		Last Modified: Thu, 08 May 2025 17:47:21 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf9cdfbc80b60b5c327f81fec79b30bfd2450f2f23ed002d7d5e63ed4733f33`  
		Last Modified: Thu, 08 May 2025 17:47:22 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c7ee215395492598d52c252485f37e9039a61a48d0d0fb41af03be3a62d516`  
		Last Modified: Thu, 08 May 2025 17:47:22 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:ba793e2f75ea28a7dbd2d1b3b0d61d7cf41106200aa00db12355a6592706cd34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00aafccdf15c39046c13083c2fff37f46e3cc03c62ecdc4dbab730297fdd6639`

```dockerfile
```

-	Layers:
	-	`sha256:f1be7e3349428f3b74e918ce10522157cd3695f6a43cecb7e501641bee8edb82`  
		Last Modified: Mon, 28 Apr 2025 21:55:43 GMT  
		Size: 2.7 MB (2704173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db1d5b909ceaa65802b09fa72f781272a332d157a79826d4971e5fddf194bc4e`  
		Last Modified: Mon, 28 Apr 2025 21:55:43 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d992d8064ea3aad5c61f05876d3d5f9b27f9caf4853f85c70115ff5b4cc7ae47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76025160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da52e8ccf76be4f48112c327593ba48cc696024c71fad43e6ae8b1126d10724c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.10.7
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Thu, 08 May 2025 17:05:07 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97cc1bc73cdd53d1fb65b54eb2237cb2d74423ba085e2b4becb0d0fec7905be`  
		Last Modified: Fri, 09 May 2025 02:58:40 GMT  
		Size: 6.5 MB (6497913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44517418a9729926f5d635549a4bd6176f13585afd47adb69f7c8b08e74c693a`  
		Last Modified: Fri, 09 May 2025 01:20:25 GMT  
		Size: 45.6 MB (45564703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5462df3243fd46d86ee7086f625bec52780ef4a05deaa42a8e4083e43f8907bf`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d817a3e3afb21bf13b393479698fe8c14f39f2e3b20100e747706b51f9ccd6e`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103414f6d083444387facc3936ec4c26348ad1954d8a891d00fa696bf2469258`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:c424dca1169ea1980d8fe4891c7075b2692db626aa001bc8823714a7922df094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab36315c728813f16e98f9c535baaad3f4a8addd707f1171e03623d893f4dafd`

```dockerfile
```

-	Layers:
	-	`sha256:76c614e1be50a565a7207409c707c416355ea43389084da3c9088bc6b51a6bae`  
		Last Modified: Tue, 29 Apr 2025 03:42:01 GMT  
		Size: 2.7 MB (2706470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eafd7093a3f3afb7cf09e97668195e911eb6927ef0f6699fe685e894611f0791`  
		Last Modified: Tue, 29 Apr 2025 03:42:01 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:45bd113eb85e7c27fedf83a7a9313e66d29cdc60dc9604f04b8da0e89567a04a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82763754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf23023139d2a5bba31fefbde296786407516e54bd44429fe5e3517c7627f3da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.10.7
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687d6d5f2d0622b294a8ce4c8f55da85356ba61e9a9ddecaa09b12c45f5dc71b`  
		Last Modified: Thu, 08 May 2025 17:56:48 GMT  
		Size: 7.7 MB (7652116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d52f1039bbb6fba3a0e7fc09bf372afbfc17d60d1bcd56c4659f0045214bbcf`  
		Last Modified: Thu, 08 May 2025 17:56:53 GMT  
		Size: 47.0 MB (47020557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9028c3e134f78f6ced2c1fc90dfc47fdb06ef46ccb86f256ce6507c93d0dacc`  
		Last Modified: Thu, 08 May 2025 17:56:47 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb7f61774f9814fa36e7925e9db6154efe72e897177610f87539565ae136d52`  
		Last Modified: Thu, 08 May 2025 17:56:48 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98fc839e4715c63a63e686672b0df5d47e4674fffc5f611891d705038ce7b65`  
		Last Modified: Thu, 08 May 2025 17:56:54 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:2b906c51825ebb95a9dc2c20a92a02cd282237452e5dd08e795b8fed5cb95a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a4bb964b36817b761823beb95bd7a1cf2d7be749bc8ac3013b70003e81696a`

```dockerfile
```

-	Layers:
	-	`sha256:aa39a818f83b457c77e9ed04b7dcdee0288b378f1c5bdaf38944c955f3dcb32b`  
		Last Modified: Tue, 29 Apr 2025 01:50:04 GMT  
		Size: 2.7 MB (2704446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b99ea6e4585f33d2ac9e33b0ef61919a71762bf46928bc59fb30ae003b16e0`  
		Last Modified: Tue, 29 Apr 2025 01:50:03 GMT  
		Size: 16.2 KB (16234 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.7-alpine`

```console
$ docker pull chronograf@sha256:e7ff1d3334696cbcf6faf91a64d45738b8daeaf63314fadc96c1a56c7fd20edf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c0ef21afbcd6bda572425dc4d8e041cfa055ed3164a8e286f2f616da5ab1a4dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32473370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f884624fe4a2eb691052a7a35ced9a118b8b5650b1595cfe1749f87aa15bcd7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.10.7
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32870b6e9c13c57b3e4492e862a1cbd13fa1a832304155c5f64e44173ac7210a`  
		Last Modified: Thu, 08 May 2025 19:49:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b6cec5e7cadf8751915b4bf4bd5d891cfe0949da529d90ae52a376a6dd2f2`  
		Last Modified: Thu, 08 May 2025 19:49:22 GMT  
		Size: 296.5 KB (296501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385cb22c2e9fc67ba1ab880b4400b1ea27a4aaaa54082ef5c2bf93e2b1dfe26a`  
		Last Modified: Thu, 08 May 2025 19:49:31 GMT  
		Size: 28.5 MB (28525260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a0e6e70a2efdf0942ca9130a6373a2a8aba0e8d0220d1d25700421f387b216`  
		Last Modified: Thu, 08 May 2025 19:49:23 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70db9642e4277afac9c14dfb2b300c68da5b2cb5ffb4fe1820dd613997f944`  
		Last Modified: Thu, 08 May 2025 19:49:23 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cd8a31daaa972542ed9037d7b7b3ef390e0cb3be4e346df11439e64cb47419`  
		Last Modified: Thu, 08 May 2025 19:49:23 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:b6a6d39e20abbc3db33205d680f93a1d19657299aa2b0b48b8d5cc77a9837a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 KB (258396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e58e4c4963b9d8238a6d2a1125754474bbfbfb5e32bb8aa8cba8fcac7db72c3`

```dockerfile
```

-	Layers:
	-	`sha256:5195b085c22b585bbb874c8273bee971bfc5088c086391d9ae9c8cb92b96f599`  
		Last Modified: Wed, 16 Apr 2025 16:54:32 GMT  
		Size: 240.5 KB (240541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfdd35f7cb83c7a7195c2e7e30f801140fb9d8c443199e4d501a3a9211b8d82b`  
		Last Modified: Wed, 16 Apr 2025 16:54:32 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:187049760dfac18e7198a96201031954136762807a3bf6b03f9e6e9428908729
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
$ docker pull chronograf@sha256:eb0516d609187b824b45b014b3784cc00dbb3efa0c1fd475513a8fac0d222307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69226912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b39b1d8e74b045f8154aaf9e37fcf521996081be57dc09b2bcc21759dbd5d87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d3ed1f9fbb6a42b1a2fd6c75bcf9568c2fbf01ffc7ff440fb857b52f316ea8`  
		Last Modified: Mon, 28 Apr 2025 21:55:25 GMT  
		Size: 4.2 MB (4209289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca61a1115157499a33217a2294803ea7c8321f2bedbac3270d7139151d4008e5`  
		Last Modified: Mon, 28 Apr 2025 21:55:25 GMT  
		Size: 34.7 MB (34738617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed19d31251e18d3a223e48f4378686f1584dde2451d702d69b4058f144a54495`  
		Last Modified: Mon, 28 Apr 2025 21:55:24 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078878797338b1ad6ac167c1928341dde71a8c839014e17d69ca1cf6e25b9bbb`  
		Last Modified: Mon, 28 Apr 2025 21:55:25 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2d8d4129ee20df04d26e0f9fafb0d14e507453798dc93b0b9389dca50e2041`  
		Last Modified: Mon, 28 Apr 2025 21:55:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:7b88499f251b84425f80f8db29a68d41da49ae79be1510f793cbcc1186f02ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582932b6ddfe5524b5f1bb44949075ba3cbce2a5a48ad79dc22878e62e01c3de`

```dockerfile
```

-	Layers:
	-	`sha256:3ed4e8542d120734b8ffd63dd9473917624c714b517354499af30cbf0a012cad`  
		Last Modified: Mon, 28 Apr 2025 21:55:25 GMT  
		Size: 2.9 MB (2907357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e6340ca3002e0a9a49b3c84cac2fb321624556ef6a275695776872ceb3d110c`  
		Last Modified: Mon, 28 Apr 2025 21:55:24 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:18681c9b0adc0a071ebf2a7f5daef9ac15a15a9a825a70d8bedde617b83b26e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62176018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c27dea8d01b0cb0581ed90a18235172b37c0d2ee2b0d3c27103bbfb8894c77`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:93c17983cb6e26d53fe6219e705b968f8a22ae1b4cb559618bdff5ba501ae39d`  
		Last Modified: Thu, 08 May 2025 18:14:26 GMT  
		Size: 25.5 MB (25542427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d92854b27558cb93aa21d451f6a925c9fa6b2a605baaf32166d58d0616cc4f`  
		Last Modified: Tue, 29 Apr 2025 03:40:05 GMT  
		Size: 3.5 MB (3511665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2b6e0be94f6084321f9824543854b7bd00749d4a1ffeeb9082dd2b873e4a0a`  
		Last Modified: Tue, 29 Apr 2025 03:40:06 GMT  
		Size: 33.1 MB (33097524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82028759040df3ccde468dff7e950146982a59a84d97bf4116ac210b399e296`  
		Last Modified: Tue, 29 Apr 2025 03:40:05 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7825091403ebb7e68fb874d4fe87dfc602fa535b9f7e98ff47f30e18a0c439`  
		Last Modified: Tue, 29 Apr 2025 03:40:05 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de960719403a18f780798bd5c845e8b7e231100b0264bcd666d6c87c3eb1a3f`  
		Last Modified: Tue, 29 Apr 2025 03:40:06 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:7bc16dbc4a96cfe1297f2499cfbe817af386b7899b59f82e099b2825ad219010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2925478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5401bbae468dfc4c71464bc70dfb125dd5a11279849548c3a12af3d94e9b21f6`

```dockerfile
```

-	Layers:
	-	`sha256:d1a047aeae09ebe87f28afcd50c5b3f7bae039839631ee1f790b37b527c92333`  
		Last Modified: Tue, 29 Apr 2025 03:40:05 GMT  
		Size: 2.9 MB (2909628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5ce8fe3d4857273fd44c3ed4eb73da1cb2bcba4a161a63dac2cf102e23272e`  
		Last Modified: Tue, 29 Apr 2025 03:40:04 GMT  
		Size: 15.8 KB (15850 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:956f69cc7065d830400e455ac70cb66a8cdb018f4cc3fb00807a46301d0ea306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66217584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb0f44e55acdc0635a33f5d43046dad1cbb838f630c9b237327bd06ac7270b30`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead16cde526af63b69c657ac676e4e2e7f6f9a41d40cdff3b0dc10560152f526`  
		Last Modified: Tue, 29 Apr 2025 01:48:44 GMT  
		Size: 4.2 MB (4210653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee93c9e40b514407d4d280ae3cca297e728179244e5ed9321f8dac0975f6212`  
		Last Modified: Tue, 29 Apr 2025 01:48:45 GMT  
		Size: 33.2 MB (33237907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fa905106b74c998a48587a2774ca4ca5f6893a4e19a926f14efce7e6572dbf`  
		Last Modified: Tue, 29 Apr 2025 01:48:43 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2273a92af502ce439aa554d12ed84c240865db49f958a37c19e6030cb0aede8e`  
		Last Modified: Tue, 29 Apr 2025 01:48:43 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa2ff3bfbbd1fbd8035060bdf96634164371f6affd9a7bddd97b8562a48a0ed`  
		Last Modified: Tue, 29 Apr 2025 01:48:44 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:e127ee00008180a9c8dd9e474d020161fd6412c4f20eae6a0bc8066be3fdc91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbaf492558f992e9ccbe8ffd215ab8153fdc240c9894ed8a1453aa5861f323c`

```dockerfile
```

-	Layers:
	-	`sha256:328155addae0d87d7ab49591b78f88ebe653e5b272c17e6630c65b4715617a77`  
		Last Modified: Tue, 29 Apr 2025 01:48:44 GMT  
		Size: 2.9 MB (2907606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc19d2c4f34f983744b6d0c2996f6ecc0015b82edbad4f570cef69224f494eb2`  
		Last Modified: Tue, 29 Apr 2025 01:48:43 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:df924b85652b1a3cf6ee401da68f4ef42a31256cd06244016ae21cec9f8952d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f033d37b112e959a0534de672abf91b9c3aa43535d685738ea85e838e904e8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23502749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137abfa83685c0597819295c4b3ef856c9395a461bd9bd70ff91ec3a4cd5921a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8ae06deb09ed334ed8eba44b6e425cced470152dbdd9c0e3c6125578263f57`  
		Last Modified: Fri, 14 Feb 2025 22:44:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69641bcb67c77b895509abb75bf637ce2b76f0acdd981fd282b113d82c04c619`  
		Last Modified: Fri, 14 Feb 2025 22:44:07 GMT  
		Size: 294.4 KB (294383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c71c1a03f44724b1796ddc3866d8fe5c4a5af8862448eabb7b2ebdc7a47748`  
		Last Modified: Fri, 14 Feb 2025 22:44:09 GMT  
		Size: 19.6 MB (19556823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29450f6d74de26216b10dc587e69dd4443992a6aea3c7b424c7aaad08ceef29`  
		Last Modified: Fri, 14 Feb 2025 22:44:07 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e84d9f6956c08b6776f1b3db99e0226246d044677f2e4cf470051da809c34e`  
		Last Modified: Fri, 14 Feb 2025 22:44:08 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030349c6370852b4bfb957d5c0dc77ca8ab49cfd26485c0b053651d825d6caf9`  
		Last Modified: Fri, 14 Feb 2025 22:44:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:0c38d57135acbd91b733dbd02beff4e0339d76bf9f15f687bd8c4f5a2f887e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 KB (189257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471658777992e65c6b6d0f2da3225f4e41179e9be460d18106df6b906e69e00b`

```dockerfile
```

-	Layers:
	-	`sha256:6592097eed7dd5f5abfbbe36bb576489b44efd68487a9d4d946f1dc3e7aeac87`  
		Last Modified: Fri, 14 Feb 2025 22:38:25 GMT  
		Size: 172.3 KB (172345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2af6f071245b63b559b430cac0c4aba0ef1cc49a72e9b52d3edae3f8b2d6ad95`  
		Last Modified: Fri, 14 Feb 2025 22:38:25 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:187049760dfac18e7198a96201031954136762807a3bf6b03f9e6e9428908729
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
$ docker pull chronograf@sha256:eb0516d609187b824b45b014b3784cc00dbb3efa0c1fd475513a8fac0d222307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69226912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b39b1d8e74b045f8154aaf9e37fcf521996081be57dc09b2bcc21759dbd5d87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d3ed1f9fbb6a42b1a2fd6c75bcf9568c2fbf01ffc7ff440fb857b52f316ea8`  
		Last Modified: Mon, 28 Apr 2025 21:55:25 GMT  
		Size: 4.2 MB (4209289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca61a1115157499a33217a2294803ea7c8321f2bedbac3270d7139151d4008e5`  
		Last Modified: Mon, 28 Apr 2025 21:55:25 GMT  
		Size: 34.7 MB (34738617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed19d31251e18d3a223e48f4378686f1584dde2451d702d69b4058f144a54495`  
		Last Modified: Mon, 28 Apr 2025 21:55:24 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078878797338b1ad6ac167c1928341dde71a8c839014e17d69ca1cf6e25b9bbb`  
		Last Modified: Mon, 28 Apr 2025 21:55:25 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2d8d4129ee20df04d26e0f9fafb0d14e507453798dc93b0b9389dca50e2041`  
		Last Modified: Mon, 28 Apr 2025 21:55:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:7b88499f251b84425f80f8db29a68d41da49ae79be1510f793cbcc1186f02ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582932b6ddfe5524b5f1bb44949075ba3cbce2a5a48ad79dc22878e62e01c3de`

```dockerfile
```

-	Layers:
	-	`sha256:3ed4e8542d120734b8ffd63dd9473917624c714b517354499af30cbf0a012cad`  
		Last Modified: Mon, 28 Apr 2025 21:55:25 GMT  
		Size: 2.9 MB (2907357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e6340ca3002e0a9a49b3c84cac2fb321624556ef6a275695776872ceb3d110c`  
		Last Modified: Mon, 28 Apr 2025 21:55:24 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:18681c9b0adc0a071ebf2a7f5daef9ac15a15a9a825a70d8bedde617b83b26e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62176018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c27dea8d01b0cb0581ed90a18235172b37c0d2ee2b0d3c27103bbfb8894c77`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:93c17983cb6e26d53fe6219e705b968f8a22ae1b4cb559618bdff5ba501ae39d`  
		Last Modified: Thu, 08 May 2025 18:14:26 GMT  
		Size: 25.5 MB (25542427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d92854b27558cb93aa21d451f6a925c9fa6b2a605baaf32166d58d0616cc4f`  
		Last Modified: Tue, 29 Apr 2025 03:40:05 GMT  
		Size: 3.5 MB (3511665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2b6e0be94f6084321f9824543854b7bd00749d4a1ffeeb9082dd2b873e4a0a`  
		Last Modified: Tue, 29 Apr 2025 03:40:06 GMT  
		Size: 33.1 MB (33097524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82028759040df3ccde468dff7e950146982a59a84d97bf4116ac210b399e296`  
		Last Modified: Tue, 29 Apr 2025 03:40:05 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7825091403ebb7e68fb874d4fe87dfc602fa535b9f7e98ff47f30e18a0c439`  
		Last Modified: Tue, 29 Apr 2025 03:40:05 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de960719403a18f780798bd5c845e8b7e231100b0264bcd666d6c87c3eb1a3f`  
		Last Modified: Tue, 29 Apr 2025 03:40:06 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:7bc16dbc4a96cfe1297f2499cfbe817af386b7899b59f82e099b2825ad219010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2925478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5401bbae468dfc4c71464bc70dfb125dd5a11279849548c3a12af3d94e9b21f6`

```dockerfile
```

-	Layers:
	-	`sha256:d1a047aeae09ebe87f28afcd50c5b3f7bae039839631ee1f790b37b527c92333`  
		Last Modified: Tue, 29 Apr 2025 03:40:05 GMT  
		Size: 2.9 MB (2909628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5ce8fe3d4857273fd44c3ed4eb73da1cb2bcba4a161a63dac2cf102e23272e`  
		Last Modified: Tue, 29 Apr 2025 03:40:04 GMT  
		Size: 15.8 KB (15850 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:956f69cc7065d830400e455ac70cb66a8cdb018f4cc3fb00807a46301d0ea306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66217584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb0f44e55acdc0635a33f5d43046dad1cbb838f630c9b237327bd06ac7270b30`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead16cde526af63b69c657ac676e4e2e7f6f9a41d40cdff3b0dc10560152f526`  
		Last Modified: Tue, 29 Apr 2025 01:48:44 GMT  
		Size: 4.2 MB (4210653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee93c9e40b514407d4d280ae3cca297e728179244e5ed9321f8dac0975f6212`  
		Last Modified: Tue, 29 Apr 2025 01:48:45 GMT  
		Size: 33.2 MB (33237907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fa905106b74c998a48587a2774ca4ca5f6893a4e19a926f14efce7e6572dbf`  
		Last Modified: Tue, 29 Apr 2025 01:48:43 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2273a92af502ce439aa554d12ed84c240865db49f958a37c19e6030cb0aede8e`  
		Last Modified: Tue, 29 Apr 2025 01:48:43 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa2ff3bfbbd1fbd8035060bdf96634164371f6affd9a7bddd97b8562a48a0ed`  
		Last Modified: Tue, 29 Apr 2025 01:48:44 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:e127ee00008180a9c8dd9e474d020161fd6412c4f20eae6a0bc8066be3fdc91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbaf492558f992e9ccbe8ffd215ab8153fdc240c9894ed8a1453aa5861f323c`

```dockerfile
```

-	Layers:
	-	`sha256:328155addae0d87d7ab49591b78f88ebe653e5b272c17e6630c65b4715617a77`  
		Last Modified: Tue, 29 Apr 2025 01:48:44 GMT  
		Size: 2.9 MB (2907606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc19d2c4f34f983744b6d0c2996f6ecc0015b82edbad4f570cef69224f494eb2`  
		Last Modified: Tue, 29 Apr 2025 01:48:43 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:df924b85652b1a3cf6ee401da68f4ef42a31256cd06244016ae21cec9f8952d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f033d37b112e959a0534de672abf91b9c3aa43535d685738ea85e838e904e8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23502749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137abfa83685c0597819295c4b3ef856c9395a461bd9bd70ff91ec3a4cd5921a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8ae06deb09ed334ed8eba44b6e425cced470152dbdd9c0e3c6125578263f57`  
		Last Modified: Fri, 14 Feb 2025 22:44:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69641bcb67c77b895509abb75bf637ce2b76f0acdd981fd282b113d82c04c619`  
		Last Modified: Fri, 14 Feb 2025 22:44:07 GMT  
		Size: 294.4 KB (294383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c71c1a03f44724b1796ddc3866d8fe5c4a5af8862448eabb7b2ebdc7a47748`  
		Last Modified: Fri, 14 Feb 2025 22:44:09 GMT  
		Size: 19.6 MB (19556823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29450f6d74de26216b10dc587e69dd4443992a6aea3c7b424c7aaad08ceef29`  
		Last Modified: Fri, 14 Feb 2025 22:44:07 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e84d9f6956c08b6776f1b3db99e0226246d044677f2e4cf470051da809c34e`  
		Last Modified: Fri, 14 Feb 2025 22:44:08 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030349c6370852b4bfb957d5c0dc77ca8ab49cfd26485c0b053651d825d6caf9`  
		Last Modified: Fri, 14 Feb 2025 22:44:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:0c38d57135acbd91b733dbd02beff4e0339d76bf9f15f687bd8c4f5a2f887e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 KB (189257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471658777992e65c6b6d0f2da3225f4e41179e9be460d18106df6b906e69e00b`

```dockerfile
```

-	Layers:
	-	`sha256:6592097eed7dd5f5abfbbe36bb576489b44efd68487a9d4d946f1dc3e7aeac87`  
		Last Modified: Fri, 14 Feb 2025 22:38:25 GMT  
		Size: 172.3 KB (172345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2af6f071245b63b559b430cac0c4aba0ef1cc49a72e9b52d3edae3f8b2d6ad95`  
		Last Modified: Fri, 14 Feb 2025 22:38:25 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:833736bbdcba6bfdb5b6a4acdc8853dc8034348fd2320f91f23baf2a971d646c
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
$ docker pull chronograf@sha256:1d24ab627379ad482dc88cebd8266d40c5505f5becff2eabb6e7739f7c6ef268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69867431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968f9a83f206ffbcfa50e5350ab40d1720c1a2b8062fa1795f376ae3bc0b6b5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b72039036d17d9727d1ef1b02508da21e10c6611b6836d620642a4792a47890`  
		Last Modified: Fri, 09 May 2025 06:13:41 GMT  
		Size: 5.2 MB (5224191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01266d5c6bac20ae328a34c2d0b5c6d416cc6e65011506d765b982d88c6c4470`  
		Last Modified: Fri, 09 May 2025 06:13:48 GMT  
		Size: 34.4 MB (34364243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b466880141037b87b3b0059813708d21918d86b0fcd8f803751530cab6f041c1`  
		Last Modified: Fri, 09 May 2025 06:13:44 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512b80821b60e26967a31030208fb281d2b47a721f35e12d7b76b7faebe7bccc`  
		Last Modified: Fri, 09 May 2025 06:13:48 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab7a8c9f8c157ad167602b157b6ac7cf651243bf90fc889fafd1fade6a68cde`  
		Last Modified: Fri, 09 May 2025 06:13:49 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:c33a058bd7610291e90aca10522e5e38343353ce4eed29d5861fb43a83abdf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2978815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5100a57199c1f549d7a505ad5017dcea82f7671e9cec2cc69e83679ba581b4e2`

```dockerfile
```

-	Layers:
	-	`sha256:407e11f0d22b709dec777a9ad6917c2e0ee858dab21ec81ae9154e180e5279e0`  
		Last Modified: Mon, 28 Apr 2025 21:55:27 GMT  
		Size: 3.0 MB (2962999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b16a4d0dc4bd74cf2a1f8f721a9d673c7f06f492c1e0248bca404c31e8aea65`  
		Last Modified: Mon, 28 Apr 2025 21:55:27 GMT  
		Size: 15.8 KB (15816 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:07fda19639cfde7431d65263b3dfd6ce5580b5cac565d6793444f8c50aa47bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62591892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa083d44fd7d57994ad6f34d254fcd7bd366f8d270f6596799c946e7636f2577`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:93c17983cb6e26d53fe6219e705b968f8a22ae1b4cb559618bdff5ba501ae39d`  
		Last Modified: Thu, 08 May 2025 18:14:26 GMT  
		Size: 25.5 MB (25542427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20e22601a15ea1dd5f35f32cefc572707cda790050915a2cbbca16133aca8bd`  
		Last Modified: Tue, 29 Apr 2025 03:40:45 GMT  
		Size: 4.5 MB (4490260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5216b65a0ad43bfc10b57259a9ad2081f3b4a79b88959001df3b31f57dbd9481`  
		Last Modified: Tue, 29 Apr 2025 03:40:45 GMT  
		Size: 32.5 MB (32534810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bb6f0255aa5d00a3c662de849fa42627242427303cc0f22a64fe557037bcff`  
		Last Modified: Tue, 29 Apr 2025 03:40:44 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d368dbf308fbb26321346c8af658ab314001c65cb5c9d38ae629c8af35d2ce`  
		Last Modified: Tue, 29 Apr 2025 03:40:44 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1950c7d59bd25f1df23ed70a48dcae4a12c502c57974cc9b086670127f7079a`  
		Last Modified: Tue, 29 Apr 2025 03:40:45 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:d728a0702eb17b5f13ed836ec0a42c460997eaeec33694cd4c503b0d3723ee16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053c13ff43c4ea6addce6704990608142e75053256aa022b973b23f26368c6a0`

```dockerfile
```

-	Layers:
	-	`sha256:c37979136ecb0da7cc66694f5b908eebd2b78f2c5111b6f70d7e9295792d562e`  
		Last Modified: Tue, 29 Apr 2025 03:40:45 GMT  
		Size: 3.0 MB (2965270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92f707ac40656d34580368b34ab22d27f1afd6ca663c90bb89b2b84997b0d47a`  
		Last Modified: Tue, 29 Apr 2025 03:40:44 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:655dab353c7e70e6b83067eb1cc48f030957b79b529d70ea29b2ae210986acec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66406752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9095941e8509eb0cf2b26af488dcdc2a451707b37204f8f527aeaf2cc8cd6ccf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92791a007455893c58cd01e71ba642180d9321ee1a0068d3c9642ad71e95bac`  
		Last Modified: Tue, 29 Apr 2025 01:49:11 GMT  
		Size: 5.2 MB (5208195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab0e618f1bb81280fd16756841db1500acafc0cbd2e026bd7ccbc1ea9dbcb17`  
		Last Modified: Tue, 29 Apr 2025 01:49:11 GMT  
		Size: 32.4 MB (32429526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404892f09dff28eacf960d70db2ed04a4f2e41567f6c54d156a0d86a313c8fa`  
		Last Modified: Tue, 29 Apr 2025 01:49:10 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd607b53faba852fd325abfbd6ac472327be171750f3e7ff4b8364d7703041b5`  
		Last Modified: Tue, 29 Apr 2025 01:49:10 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb37ad526898b10d7915f96c5c562ac222187209879429583fcaecf631b5ee77`  
		Last Modified: Tue, 29 Apr 2025 01:49:11 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:0cd0f61f44ecd37dc7dda204bb43cafc8e8a8cbb73043bdc3df166fcb7b42324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2979159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1dd483133857c01d540fef7902564f88a5f944133ec1f9eea54ac998e6d5028`

```dockerfile
```

-	Layers:
	-	`sha256:7555a52e2af5f4f854db70404cbfcc5bf8c14967b09d7942fc1c8d4294bdba23`  
		Last Modified: Tue, 29 Apr 2025 01:49:11 GMT  
		Size: 3.0 MB (2963248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:584bf5dbc8906b4406cdcfcafa8f90274ee8a2ca7aabc6d3b09ec2a3e28649a2`  
		Last Modified: Tue, 29 Apr 2025 01:49:10 GMT  
		Size: 15.9 KB (15911 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:830cefde62b7fa5d1e719c9cdbd90e36b6111165338d6a63589967af3b425932
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:1bc656b7ebda40ceb3556472bac3163ab7b63970a38964aba666e23cab083110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23150080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1f3cf9f33249acb43998ce431a893a6196e54c6623a39388c922e747600326`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c39259f86321f91341426ea2b7c8164eb8c8a538841604f969c31abd195acba`  
		Last Modified: Fri, 14 Feb 2025 22:43:26 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bf003f24079392a7a29452383a6db1f26978c48f54533c79153b28b82b7257`  
		Last Modified: Fri, 14 Feb 2025 22:43:26 GMT  
		Size: 294.4 KB (294385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb15ecadba26a5095f16beac190b0f35fa020ee3fff220c3243ebb39f58712a`  
		Last Modified: Fri, 14 Feb 2025 22:43:28 GMT  
		Size: 19.2 MB (19204154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402cd540f74e77bd8181c883cf26fa3525fd15513ad005bc58b5bed6ddb9d248`  
		Last Modified: Fri, 14 Feb 2025 22:43:27 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c299e5fdf7b7064f6b152ef78a715eefeff0a18c48c95e7a2b74b34bc318c7f5`  
		Last Modified: Fri, 14 Feb 2025 22:43:27 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ff2dde7922e46ced41d599cff59f593b600debe56130e43867bb3be500e704`  
		Last Modified: Fri, 14 Feb 2025 22:43:28 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:cdd0db3358b43541330dbf7e54517d4cbd7e2c4dfcdf798c5197cdc28507a544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 KB (246816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4af8a7ead9ebe09b9d15f6a3a39569c97af7c6664e752144193917be3f3928e`

```dockerfile
```

-	Layers:
	-	`sha256:41a2c152911589c4db3aec41c07d7ba26ba8320255380bc8e9f5dad25980a11b`  
		Last Modified: Fri, 14 Feb 2025 22:38:30 GMT  
		Size: 229.9 KB (229904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ad8d123c697deeb31e83f6f288bbb9095d82109f9902675e157e8b88f35c2b`  
		Last Modified: Fri, 14 Feb 2025 22:38:30 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:833736bbdcba6bfdb5b6a4acdc8853dc8034348fd2320f91f23baf2a971d646c
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
$ docker pull chronograf@sha256:1d24ab627379ad482dc88cebd8266d40c5505f5becff2eabb6e7739f7c6ef268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69867431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968f9a83f206ffbcfa50e5350ab40d1720c1a2b8062fa1795f376ae3bc0b6b5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b72039036d17d9727d1ef1b02508da21e10c6611b6836d620642a4792a47890`  
		Last Modified: Fri, 09 May 2025 06:13:41 GMT  
		Size: 5.2 MB (5224191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01266d5c6bac20ae328a34c2d0b5c6d416cc6e65011506d765b982d88c6c4470`  
		Last Modified: Fri, 09 May 2025 06:13:48 GMT  
		Size: 34.4 MB (34364243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b466880141037b87b3b0059813708d21918d86b0fcd8f803751530cab6f041c1`  
		Last Modified: Fri, 09 May 2025 06:13:44 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512b80821b60e26967a31030208fb281d2b47a721f35e12d7b76b7faebe7bccc`  
		Last Modified: Fri, 09 May 2025 06:13:48 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab7a8c9f8c157ad167602b157b6ac7cf651243bf90fc889fafd1fade6a68cde`  
		Last Modified: Fri, 09 May 2025 06:13:49 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:c33a058bd7610291e90aca10522e5e38343353ce4eed29d5861fb43a83abdf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2978815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5100a57199c1f549d7a505ad5017dcea82f7671e9cec2cc69e83679ba581b4e2`

```dockerfile
```

-	Layers:
	-	`sha256:407e11f0d22b709dec777a9ad6917c2e0ee858dab21ec81ae9154e180e5279e0`  
		Last Modified: Mon, 28 Apr 2025 21:55:27 GMT  
		Size: 3.0 MB (2962999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b16a4d0dc4bd74cf2a1f8f721a9d673c7f06f492c1e0248bca404c31e8aea65`  
		Last Modified: Mon, 28 Apr 2025 21:55:27 GMT  
		Size: 15.8 KB (15816 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:07fda19639cfde7431d65263b3dfd6ce5580b5cac565d6793444f8c50aa47bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62591892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa083d44fd7d57994ad6f34d254fcd7bd366f8d270f6596799c946e7636f2577`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:93c17983cb6e26d53fe6219e705b968f8a22ae1b4cb559618bdff5ba501ae39d`  
		Last Modified: Thu, 08 May 2025 18:14:26 GMT  
		Size: 25.5 MB (25542427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20e22601a15ea1dd5f35f32cefc572707cda790050915a2cbbca16133aca8bd`  
		Last Modified: Tue, 29 Apr 2025 03:40:45 GMT  
		Size: 4.5 MB (4490260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5216b65a0ad43bfc10b57259a9ad2081f3b4a79b88959001df3b31f57dbd9481`  
		Last Modified: Tue, 29 Apr 2025 03:40:45 GMT  
		Size: 32.5 MB (32534810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bb6f0255aa5d00a3c662de849fa42627242427303cc0f22a64fe557037bcff`  
		Last Modified: Tue, 29 Apr 2025 03:40:44 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d368dbf308fbb26321346c8af658ab314001c65cb5c9d38ae629c8af35d2ce`  
		Last Modified: Tue, 29 Apr 2025 03:40:44 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1950c7d59bd25f1df23ed70a48dcae4a12c502c57974cc9b086670127f7079a`  
		Last Modified: Tue, 29 Apr 2025 03:40:45 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:d728a0702eb17b5f13ed836ec0a42c460997eaeec33694cd4c503b0d3723ee16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053c13ff43c4ea6addce6704990608142e75053256aa022b973b23f26368c6a0`

```dockerfile
```

-	Layers:
	-	`sha256:c37979136ecb0da7cc66694f5b908eebd2b78f2c5111b6f70d7e9295792d562e`  
		Last Modified: Tue, 29 Apr 2025 03:40:45 GMT  
		Size: 3.0 MB (2965270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92f707ac40656d34580368b34ab22d27f1afd6ca663c90bb89b2b84997b0d47a`  
		Last Modified: Tue, 29 Apr 2025 03:40:44 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:655dab353c7e70e6b83067eb1cc48f030957b79b529d70ea29b2ae210986acec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66406752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9095941e8509eb0cf2b26af488dcdc2a451707b37204f8f527aeaf2cc8cd6ccf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92791a007455893c58cd01e71ba642180d9321ee1a0068d3c9642ad71e95bac`  
		Last Modified: Tue, 29 Apr 2025 01:49:11 GMT  
		Size: 5.2 MB (5208195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab0e618f1bb81280fd16756841db1500acafc0cbd2e026bd7ccbc1ea9dbcb17`  
		Last Modified: Tue, 29 Apr 2025 01:49:11 GMT  
		Size: 32.4 MB (32429526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404892f09dff28eacf960d70db2ed04a4f2e41567f6c54d156a0d86a313c8fa`  
		Last Modified: Tue, 29 Apr 2025 01:49:10 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd607b53faba852fd325abfbd6ac472327be171750f3e7ff4b8364d7703041b5`  
		Last Modified: Tue, 29 Apr 2025 01:49:10 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb37ad526898b10d7915f96c5c562ac222187209879429583fcaecf631b5ee77`  
		Last Modified: Tue, 29 Apr 2025 01:49:11 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:0cd0f61f44ecd37dc7dda204bb43cafc8e8a8cbb73043bdc3df166fcb7b42324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2979159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1dd483133857c01d540fef7902564f88a5f944133ec1f9eea54ac998e6d5028`

```dockerfile
```

-	Layers:
	-	`sha256:7555a52e2af5f4f854db70404cbfcc5bf8c14967b09d7942fc1c8d4294bdba23`  
		Last Modified: Tue, 29 Apr 2025 01:49:11 GMT  
		Size: 3.0 MB (2963248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:584bf5dbc8906b4406cdcfcafa8f90274ee8a2ca7aabc6d3b09ec2a3e28649a2`  
		Last Modified: Tue, 29 Apr 2025 01:49:10 GMT  
		Size: 15.9 KB (15911 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:830cefde62b7fa5d1e719c9cdbd90e36b6111165338d6a63589967af3b425932
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:1bc656b7ebda40ceb3556472bac3163ab7b63970a38964aba666e23cab083110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23150080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1f3cf9f33249acb43998ce431a893a6196e54c6623a39388c922e747600326`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c39259f86321f91341426ea2b7c8164eb8c8a538841604f969c31abd195acba`  
		Last Modified: Fri, 14 Feb 2025 22:43:26 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bf003f24079392a7a29452383a6db1f26978c48f54533c79153b28b82b7257`  
		Last Modified: Fri, 14 Feb 2025 22:43:26 GMT  
		Size: 294.4 KB (294385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb15ecadba26a5095f16beac190b0f35fa020ee3fff220c3243ebb39f58712a`  
		Last Modified: Fri, 14 Feb 2025 22:43:28 GMT  
		Size: 19.2 MB (19204154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402cd540f74e77bd8181c883cf26fa3525fd15513ad005bc58b5bed6ddb9d248`  
		Last Modified: Fri, 14 Feb 2025 22:43:27 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c299e5fdf7b7064f6b152ef78a715eefeff0a18c48c95e7a2b74b34bc318c7f5`  
		Last Modified: Fri, 14 Feb 2025 22:43:27 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ff2dde7922e46ced41d599cff59f593b600debe56130e43867bb3be500e704`  
		Last Modified: Fri, 14 Feb 2025 22:43:28 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:cdd0db3358b43541330dbf7e54517d4cbd7e2c4dfcdf798c5197cdc28507a544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 KB (246816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4af8a7ead9ebe09b9d15f6a3a39569c97af7c6664e752144193917be3f3928e`

```dockerfile
```

-	Layers:
	-	`sha256:41a2c152911589c4db3aec41c07d7ba26ba8320255380bc8e9f5dad25980a11b`  
		Last Modified: Fri, 14 Feb 2025 22:38:30 GMT  
		Size: 229.9 KB (229904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ad8d123c697deeb31e83f6f288bbb9095d82109f9902675e157e8b88f35c2b`  
		Last Modified: Fri, 14 Feb 2025 22:38:30 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:6b167d0c58df6bc596b637f331d7a75ef6c23fa43c2c8b473a584c64871de51d
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
$ docker pull chronograf@sha256:87bcf539b315c7657d8e9b3c3fbeed19893ec8c88dd89fe9ccbc3b0f5f8970f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70514817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f255e574936ccafd2227e7335feb0ee308c3e85076114a47df5c5187993bd49`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a52789b15462db0542fb180e0bd0f1f0a615b8905b45b4da7ee062c1e060596`  
		Last Modified: Thu, 08 May 2025 18:46:32 GMT  
		Size: 5.2 MB (5224155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939e14365ff873564f75c588838061d661a0a03f2dd5e4dfe4df73038bda3cb6`  
		Last Modified: Thu, 08 May 2025 18:46:35 GMT  
		Size: 35.0 MB (35011669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14357cbe11764714bd7f68b9c88414eb8f4650e34e423610fd5449806391dae6`  
		Last Modified: Thu, 08 May 2025 18:46:32 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a468ac897d2cc880a4b91371f499f1c789536d8f8c44694ce26be70dd74c0350`  
		Last Modified: Thu, 08 May 2025 18:46:32 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3f0c434094cbc59ad3e6f7bfd1a080bf5d93c682f6917ea30ef736f5f7d709`  
		Last Modified: Thu, 08 May 2025 18:46:33 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:0584a606baca075c59eefbaf340aa23740424654e5b6cbdab12e0fcc0234b125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274f42d7ffed3d79ed64327b73d5d1384c061e02dd4f7d9e6894f2479fd23fc7`

```dockerfile
```

-	Layers:
	-	`sha256:2709eb79e6766d2a1208d8f7b9b21ad1dcee2d96511f9bc22edb2d8b7497eeaf`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 3.0 MB (2968209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f7f12c3addd84acb2285b922dc557a2cc1bf6086127771398b9675969a14695`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:dc655ef5280396cea28f3b5ef04bc4890aa07d857e2dd8c9f94c198b787df637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63368515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e622c62edefaa703f093bdc6464020bb6c517e682ba1c79e8575549aaa6d08bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:93c17983cb6e26d53fe6219e705b968f8a22ae1b4cb559618bdff5ba501ae39d`  
		Last Modified: Thu, 08 May 2025 18:14:26 GMT  
		Size: 25.5 MB (25542427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20e22601a15ea1dd5f35f32cefc572707cda790050915a2cbbca16133aca8bd`  
		Last Modified: Tue, 29 Apr 2025 03:40:45 GMT  
		Size: 4.5 MB (4490260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a267a73c5f914a317947a30cb2d7d9b17ba971334a8521a9a2ff2a2750b2b433`  
		Last Modified: Tue, 29 Apr 2025 03:41:15 GMT  
		Size: 33.3 MB (33311435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261368bb54677dcb816d4799d04ab583b00432b6c7d94b8288247dced7883f03`  
		Last Modified: Tue, 29 Apr 2025 03:41:14 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11253f1232eb2d1ba3217b07e2a3186cee70d28b0b878d1d255ac7fbb3d7e555`  
		Last Modified: Tue, 29 Apr 2025 03:41:14 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd73c1269d0bee06b4b189eebd13deb7df47c8c1d66d7bc7fe71efbf82eb635`  
		Last Modified: Tue, 29 Apr 2025 03:41:14 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:c19c39b15ec026348df17612225f1b24084e1d79cb74c929eca4bc3b9e8967a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0042add9241853c1eb67de252af3b0c8c577a91c270d87451e76dede3e2d37b7`

```dockerfile
```

-	Layers:
	-	`sha256:a9fa2d189df5b1ad00011fc91c20fe4e6c29dc993515bf5771f29d60fe13d57a`  
		Last Modified: Tue, 29 Apr 2025 03:41:14 GMT  
		Size: 3.0 MB (2970480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e22be32b19e350bbdaa57d82787ea65e17f49d7f2fc2a412acc423fe31ccb85`  
		Last Modified: Tue, 29 Apr 2025 03:41:14 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f44af7dac0bab41cf50c5dc18e2217bb265c75a75d98ee87d4a24b070eeaf812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67158828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c697f27a80932e71a7018ae2c14e3c0d635b6981e28ca7b7767b39ec0acc9691`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92791a007455893c58cd01e71ba642180d9321ee1a0068d3c9642ad71e95bac`  
		Last Modified: Tue, 29 Apr 2025 01:49:11 GMT  
		Size: 5.2 MB (5208195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84c6bde34330cecf42a66275584f96ba038553684e58d146a6030cf8a5b824f`  
		Last Modified: Tue, 29 Apr 2025 01:49:33 GMT  
		Size: 33.2 MB (33181591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf44b0553b1577b1ef037163c41596be4f999d301f63fde3e50890c1312b7696`  
		Last Modified: Tue, 29 Apr 2025 01:49:32 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2a6bbc8f18835a6a0cc8bf1de8db020aea93ae21c386eca6b82fc2cf7b637f`  
		Last Modified: Tue, 29 Apr 2025 01:49:32 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a37cfe38bbcc3f777a67f48446424de20ec293ffba6c33e78c0b015498c941`  
		Last Modified: Tue, 29 Apr 2025 01:49:32 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:a26ac679affc8dce43bb516b731c79cc4f4914cdd5cc4035191d29ffe4ea7004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcffdf172b66c4381ce61ef6a7c46b27fcc1fe9a707033271cea06cb127e4ac7`

```dockerfile
```

-	Layers:
	-	`sha256:fe2ce58ff97bef416c46abf23a0baa2d57911ec0fa8d659f3ed75125fcac9107`  
		Last Modified: Tue, 29 Apr 2025 01:49:32 GMT  
		Size: 3.0 MB (2968458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5d1de48e0c7300060116991be3f65dab23e5a297e8dfcfc4f9d578b9e22bdf9`  
		Last Modified: Tue, 29 Apr 2025 01:49:32 GMT  
		Size: 15.9 KB (15905 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:540ce018515beb499f291d9455b2a9d1c289f8fae572d53fd54246fd7e7146d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:a4dfb7641118d30a6585c108ec369459880e88c6faf92790e05d3593e3353a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23617935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c262c4b7eed1867c635b60b6ffc799536825070ed1596c83b1c42ad21c4105`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de662ab890de5cb0e03103817de459544467d4b3f0784c60d26b56b9057ad500`  
		Last Modified: Sat, 15 Feb 2025 08:18:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69641bcb67c77b895509abb75bf637ce2b76f0acdd981fd282b113d82c04c619`  
		Last Modified: Fri, 14 Feb 2025 22:44:07 GMT  
		Size: 294.4 KB (294383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc476e87cc64ce09a8be67509b3baee59f88525efcf0dbb7aa18f0aeeb0823b`  
		Last Modified: Sat, 15 Feb 2025 08:18:51 GMT  
		Size: 19.7 MB (19672009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29450f6d74de26216b10dc587e69dd4443992a6aea3c7b424c7aaad08ceef29`  
		Last Modified: Fri, 14 Feb 2025 22:44:07 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e84d9f6956c08b6776f1b3db99e0226246d044677f2e4cf470051da809c34e`  
		Last Modified: Fri, 14 Feb 2025 22:44:08 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030349c6370852b4bfb957d5c0dc77ca8ab49cfd26485c0b053651d825d6caf9`  
		Last Modified: Fri, 14 Feb 2025 22:44:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:50d32d3aaaf4e53754ad80987dede42204c13fb95cb686e2c2513f3385048a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 KB (252025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0aafa46d648297defb395a6fbfbb62467880874da481dd27cd19da3182e2433`

```dockerfile
```

-	Layers:
	-	`sha256:4486aa18fc3114703709ddebe3fb35b7b024a9c27bc87effa33b6909ae7fe370`  
		Last Modified: Fri, 14 Feb 2025 22:38:37 GMT  
		Size: 235.1 KB (235116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b34d12538bfcd1dd3e2b34c8aa09be9693afe86e4462d7341bee3cf95202f0`  
		Last Modified: Fri, 14 Feb 2025 22:38:37 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:6b167d0c58df6bc596b637f331d7a75ef6c23fa43c2c8b473a584c64871de51d
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
$ docker pull chronograf@sha256:87bcf539b315c7657d8e9b3c3fbeed19893ec8c88dd89fe9ccbc3b0f5f8970f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70514817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f255e574936ccafd2227e7335feb0ee308c3e85076114a47df5c5187993bd49`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a52789b15462db0542fb180e0bd0f1f0a615b8905b45b4da7ee062c1e060596`  
		Last Modified: Thu, 08 May 2025 18:46:32 GMT  
		Size: 5.2 MB (5224155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939e14365ff873564f75c588838061d661a0a03f2dd5e4dfe4df73038bda3cb6`  
		Last Modified: Thu, 08 May 2025 18:46:35 GMT  
		Size: 35.0 MB (35011669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14357cbe11764714bd7f68b9c88414eb8f4650e34e423610fd5449806391dae6`  
		Last Modified: Thu, 08 May 2025 18:46:32 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a468ac897d2cc880a4b91371f499f1c789536d8f8c44694ce26be70dd74c0350`  
		Last Modified: Thu, 08 May 2025 18:46:32 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3f0c434094cbc59ad3e6f7bfd1a080bf5d93c682f6917ea30ef736f5f7d709`  
		Last Modified: Thu, 08 May 2025 18:46:33 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:0584a606baca075c59eefbaf340aa23740424654e5b6cbdab12e0fcc0234b125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274f42d7ffed3d79ed64327b73d5d1384c061e02dd4f7d9e6894f2479fd23fc7`

```dockerfile
```

-	Layers:
	-	`sha256:2709eb79e6766d2a1208d8f7b9b21ad1dcee2d96511f9bc22edb2d8b7497eeaf`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 3.0 MB (2968209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f7f12c3addd84acb2285b922dc557a2cc1bf6086127771398b9675969a14695`  
		Last Modified: Mon, 28 Apr 2025 21:56:02 GMT  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:dc655ef5280396cea28f3b5ef04bc4890aa07d857e2dd8c9f94c198b787df637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63368515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e622c62edefaa703f093bdc6464020bb6c517e682ba1c79e8575549aaa6d08bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:93c17983cb6e26d53fe6219e705b968f8a22ae1b4cb559618bdff5ba501ae39d`  
		Last Modified: Thu, 08 May 2025 18:14:26 GMT  
		Size: 25.5 MB (25542427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20e22601a15ea1dd5f35f32cefc572707cda790050915a2cbbca16133aca8bd`  
		Last Modified: Tue, 29 Apr 2025 03:40:45 GMT  
		Size: 4.5 MB (4490260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a267a73c5f914a317947a30cb2d7d9b17ba971334a8521a9a2ff2a2750b2b433`  
		Last Modified: Tue, 29 Apr 2025 03:41:15 GMT  
		Size: 33.3 MB (33311435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261368bb54677dcb816d4799d04ab583b00432b6c7d94b8288247dced7883f03`  
		Last Modified: Tue, 29 Apr 2025 03:41:14 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11253f1232eb2d1ba3217b07e2a3186cee70d28b0b878d1d255ac7fbb3d7e555`  
		Last Modified: Tue, 29 Apr 2025 03:41:14 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd73c1269d0bee06b4b189eebd13deb7df47c8c1d66d7bc7fe71efbf82eb635`  
		Last Modified: Tue, 29 Apr 2025 03:41:14 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:c19c39b15ec026348df17612225f1b24084e1d79cb74c929eca4bc3b9e8967a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0042add9241853c1eb67de252af3b0c8c577a91c270d87451e76dede3e2d37b7`

```dockerfile
```

-	Layers:
	-	`sha256:a9fa2d189df5b1ad00011fc91c20fe4e6c29dc993515bf5771f29d60fe13d57a`  
		Last Modified: Tue, 29 Apr 2025 03:41:14 GMT  
		Size: 3.0 MB (2970480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e22be32b19e350bbdaa57d82787ea65e17f49d7f2fc2a412acc423fe31ccb85`  
		Last Modified: Tue, 29 Apr 2025 03:41:14 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f44af7dac0bab41cf50c5dc18e2217bb265c75a75d98ee87d4a24b070eeaf812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67158828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c697f27a80932e71a7018ae2c14e3c0d635b6981e28ca7b7767b39ec0acc9691`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92791a007455893c58cd01e71ba642180d9321ee1a0068d3c9642ad71e95bac`  
		Last Modified: Tue, 29 Apr 2025 01:49:11 GMT  
		Size: 5.2 MB (5208195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84c6bde34330cecf42a66275584f96ba038553684e58d146a6030cf8a5b824f`  
		Last Modified: Tue, 29 Apr 2025 01:49:33 GMT  
		Size: 33.2 MB (33181591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf44b0553b1577b1ef037163c41596be4f999d301f63fde3e50890c1312b7696`  
		Last Modified: Tue, 29 Apr 2025 01:49:32 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2a6bbc8f18835a6a0cc8bf1de8db020aea93ae21c386eca6b82fc2cf7b637f`  
		Last Modified: Tue, 29 Apr 2025 01:49:32 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a37cfe38bbcc3f777a67f48446424de20ec293ffba6c33e78c0b015498c941`  
		Last Modified: Tue, 29 Apr 2025 01:49:32 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:a26ac679affc8dce43bb516b731c79cc4f4914cdd5cc4035191d29ffe4ea7004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcffdf172b66c4381ce61ef6a7c46b27fcc1fe9a707033271cea06cb127e4ac7`

```dockerfile
```

-	Layers:
	-	`sha256:fe2ce58ff97bef416c46abf23a0baa2d57911ec0fa8d659f3ed75125fcac9107`  
		Last Modified: Tue, 29 Apr 2025 01:49:32 GMT  
		Size: 3.0 MB (2968458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5d1de48e0c7300060116991be3f65dab23e5a297e8dfcfc4f9d578b9e22bdf9`  
		Last Modified: Tue, 29 Apr 2025 01:49:32 GMT  
		Size: 15.9 KB (15905 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:540ce018515beb499f291d9455b2a9d1c289f8fae572d53fd54246fd7e7146d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:a4dfb7641118d30a6585c108ec369459880e88c6faf92790e05d3593e3353a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23617935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c262c4b7eed1867c635b60b6ffc799536825070ed1596c83b1c42ad21c4105`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de662ab890de5cb0e03103817de459544467d4b3f0784c60d26b56b9057ad500`  
		Last Modified: Sat, 15 Feb 2025 08:18:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69641bcb67c77b895509abb75bf637ce2b76f0acdd981fd282b113d82c04c619`  
		Last Modified: Fri, 14 Feb 2025 22:44:07 GMT  
		Size: 294.4 KB (294383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc476e87cc64ce09a8be67509b3baee59f88525efcf0dbb7aa18f0aeeb0823b`  
		Last Modified: Sat, 15 Feb 2025 08:18:51 GMT  
		Size: 19.7 MB (19672009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29450f6d74de26216b10dc587e69dd4443992a6aea3c7b424c7aaad08ceef29`  
		Last Modified: Fri, 14 Feb 2025 22:44:07 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e84d9f6956c08b6776f1b3db99e0226246d044677f2e4cf470051da809c34e`  
		Last Modified: Fri, 14 Feb 2025 22:44:08 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030349c6370852b4bfb957d5c0dc77ca8ab49cfd26485c0b053651d825d6caf9`  
		Last Modified: Fri, 14 Feb 2025 22:44:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:50d32d3aaaf4e53754ad80987dede42204c13fb95cb686e2c2513f3385048a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 KB (252025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0aafa46d648297defb395a6fbfbb62467880874da481dd27cd19da3182e2433`

```dockerfile
```

-	Layers:
	-	`sha256:4486aa18fc3114703709ddebe3fb35b7b024a9c27bc87effa33b6909ae7fe370`  
		Last Modified: Fri, 14 Feb 2025 22:38:37 GMT  
		Size: 235.1 KB (235116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b34d12538bfcd1dd3e2b34c8aa09be9693afe86e4462d7341bee3cf95202f0`  
		Last Modified: Fri, 14 Feb 2025 22:38:37 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:e7ff1d3334696cbcf6faf91a64d45738b8daeaf63314fadc96c1a56c7fd20edf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c0ef21afbcd6bda572425dc4d8e041cfa055ed3164a8e286f2f616da5ab1a4dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32473370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f884624fe4a2eb691052a7a35ced9a118b8b5650b1595cfe1749f87aa15bcd7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.10.7
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32870b6e9c13c57b3e4492e862a1cbd13fa1a832304155c5f64e44173ac7210a`  
		Last Modified: Thu, 08 May 2025 19:49:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b6cec5e7cadf8751915b4bf4bd5d891cfe0949da529d90ae52a376a6dd2f2`  
		Last Modified: Thu, 08 May 2025 19:49:22 GMT  
		Size: 296.5 KB (296501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385cb22c2e9fc67ba1ab880b4400b1ea27a4aaaa54082ef5c2bf93e2b1dfe26a`  
		Last Modified: Thu, 08 May 2025 19:49:31 GMT  
		Size: 28.5 MB (28525260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a0e6e70a2efdf0942ca9130a6373a2a8aba0e8d0220d1d25700421f387b216`  
		Last Modified: Thu, 08 May 2025 19:49:23 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70db9642e4277afac9c14dfb2b300c68da5b2cb5ffb4fe1820dd613997f944`  
		Last Modified: Thu, 08 May 2025 19:49:23 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cd8a31daaa972542ed9037d7b7b3ef390e0cb3be4e346df11439e64cb47419`  
		Last Modified: Thu, 08 May 2025 19:49:23 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:b6a6d39e20abbc3db33205d680f93a1d19657299aa2b0b48b8d5cc77a9837a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 KB (258396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e58e4c4963b9d8238a6d2a1125754474bbfbfb5e32bb8aa8cba8fcac7db72c3`

```dockerfile
```

-	Layers:
	-	`sha256:5195b085c22b585bbb874c8273bee971bfc5088c086391d9ae9c8cb92b96f599`  
		Last Modified: Wed, 16 Apr 2025 16:54:32 GMT  
		Size: 240.5 KB (240541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfdd35f7cb83c7a7195c2e7e30f801140fb9d8c443199e4d501a3a9211b8d82b`  
		Last Modified: Wed, 16 Apr 2025 16:54:32 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:f6ef7852b2257d0e7756589757627a50d2bb6ce74c4abf3c7e4297483f52b7f8
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
$ docker pull chronograf@sha256:7dd16daa289079744a3485a5dc1f9c4d1b42fecd1c091ac8c1d060658407316a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85361259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01bfcfdf38b10aa4664a875462af00c39c7f6e34a93c9736540134e2bc239b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.10.7
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d948a6e444038248d3837d2e8bb8e9f5e347ce21fe67592ddea6c9636511d6f4`  
		Last Modified: Thu, 08 May 2025 17:47:22 GMT  
		Size: 7.9 MB (7875415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7b2f54616466e283cb5bdb7c5192c06c8a43136da9bb6c0c13ab2018dad9d9`  
		Last Modified: Thu, 08 May 2025 17:47:25 GMT  
		Size: 49.2 MB (49233737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ded7601090ccd78e1baae3c56e7ad4c6b68a4d47cb778c98699674602e64b2`  
		Last Modified: Thu, 08 May 2025 17:47:21 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf9cdfbc80b60b5c327f81fec79b30bfd2450f2f23ed002d7d5e63ed4733f33`  
		Last Modified: Thu, 08 May 2025 17:47:22 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c7ee215395492598d52c252485f37e9039a61a48d0d0fb41af03be3a62d516`  
		Last Modified: Thu, 08 May 2025 17:47:22 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:ba793e2f75ea28a7dbd2d1b3b0d61d7cf41106200aa00db12355a6592706cd34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00aafccdf15c39046c13083c2fff37f46e3cc03c62ecdc4dbab730297fdd6639`

```dockerfile
```

-	Layers:
	-	`sha256:f1be7e3349428f3b74e918ce10522157cd3695f6a43cecb7e501641bee8edb82`  
		Last Modified: Mon, 28 Apr 2025 21:55:43 GMT  
		Size: 2.7 MB (2704173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db1d5b909ceaa65802b09fa72f781272a332d157a79826d4971e5fddf194bc4e`  
		Last Modified: Mon, 28 Apr 2025 21:55:43 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d992d8064ea3aad5c61f05876d3d5f9b27f9caf4853f85c70115ff5b4cc7ae47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76025160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da52e8ccf76be4f48112c327593ba48cc696024c71fad43e6ae8b1126d10724c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.10.7
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Thu, 08 May 2025 17:05:07 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97cc1bc73cdd53d1fb65b54eb2237cb2d74423ba085e2b4becb0d0fec7905be`  
		Last Modified: Fri, 09 May 2025 02:58:40 GMT  
		Size: 6.5 MB (6497913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44517418a9729926f5d635549a4bd6176f13585afd47adb69f7c8b08e74c693a`  
		Last Modified: Fri, 09 May 2025 01:20:25 GMT  
		Size: 45.6 MB (45564703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5462df3243fd46d86ee7086f625bec52780ef4a05deaa42a8e4083e43f8907bf`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d817a3e3afb21bf13b393479698fe8c14f39f2e3b20100e747706b51f9ccd6e`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103414f6d083444387facc3936ec4c26348ad1954d8a891d00fa696bf2469258`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:c424dca1169ea1980d8fe4891c7075b2692db626aa001bc8823714a7922df094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab36315c728813f16e98f9c535baaad3f4a8addd707f1171e03623d893f4dafd`

```dockerfile
```

-	Layers:
	-	`sha256:76c614e1be50a565a7207409c707c416355ea43389084da3c9088bc6b51a6bae`  
		Last Modified: Tue, 29 Apr 2025 03:42:01 GMT  
		Size: 2.7 MB (2706470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eafd7093a3f3afb7cf09e97668195e911eb6927ef0f6699fe685e894611f0791`  
		Last Modified: Tue, 29 Apr 2025 03:42:01 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:45bd113eb85e7c27fedf83a7a9313e66d29cdc60dc9604f04b8da0e89567a04a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82763754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf23023139d2a5bba31fefbde296786407516e54bd44429fe5e3517c7627f3da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.10.7
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687d6d5f2d0622b294a8ce4c8f55da85356ba61e9a9ddecaa09b12c45f5dc71b`  
		Last Modified: Thu, 08 May 2025 17:56:48 GMT  
		Size: 7.7 MB (7652116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d52f1039bbb6fba3a0e7fc09bf372afbfc17d60d1bcd56c4659f0045214bbcf`  
		Last Modified: Thu, 08 May 2025 17:56:53 GMT  
		Size: 47.0 MB (47020557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9028c3e134f78f6ced2c1fc90dfc47fdb06ef46ccb86f256ce6507c93d0dacc`  
		Last Modified: Thu, 08 May 2025 17:56:47 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb7f61774f9814fa36e7925e9db6154efe72e897177610f87539565ae136d52`  
		Last Modified: Thu, 08 May 2025 17:56:48 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98fc839e4715c63a63e686672b0df5d47e4674fffc5f611891d705038ce7b65`  
		Last Modified: Thu, 08 May 2025 17:56:54 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:2b906c51825ebb95a9dc2c20a92a02cd282237452e5dd08e795b8fed5cb95a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a4bb964b36817b761823beb95bd7a1cf2d7be749bc8ac3013b70003e81696a`

```dockerfile
```

-	Layers:
	-	`sha256:aa39a818f83b457c77e9ed04b7dcdee0288b378f1c5bdaf38944c955f3dcb32b`  
		Last Modified: Tue, 29 Apr 2025 01:50:04 GMT  
		Size: 2.7 MB (2704446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b99ea6e4585f33d2ac9e33b0ef61919a71762bf46928bc59fb30ae003b16e0`  
		Last Modified: Tue, 29 Apr 2025 01:50:03 GMT  
		Size: 16.2 KB (16234 bytes)  
		MIME: application/vnd.in-toto+json
