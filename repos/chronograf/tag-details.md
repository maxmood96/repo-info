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
$ docker pull chronograf@sha256:84af7bc8a2265fa109f149bcf0543c6c47d201f86f56ce9b37ed470c807d3db8
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
$ docker pull chronograf@sha256:f9a4491704d2ad6bb41a681ac7a22c7ddfd21792810a0190317b80c9eb7f538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85361392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e633a3cc758266abbcfda81a9213440ce128c909435f912398ad89cba7510fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8efa8a4370fd03594063cc027a3a187f10071b20f22d25026b1e024b06c0609`  
		Last Modified: Wed, 21 May 2025 23:21:09 GMT  
		Size: 7.9 MB (7877884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9631558f3e9059ec4e0def4253294a8d1b50d84cc67f10879f0f3e193d5f5d9`  
		Last Modified: Wed, 21 May 2025 23:21:10 GMT  
		Size: 49.2 MB (49233712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112fb2921522a7cd62b4c6166b3791ab71c8860f860283d16ebb28dea6707658`  
		Last Modified: Wed, 21 May 2025 23:21:09 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32a6d2434b94c306e78b79e5e1d7d433f8d23ac27b31db416f974aff7b6631`  
		Last Modified: Wed, 21 May 2025 23:21:09 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd2295dbeed42367f8d5d0c0ae63fc8ef1b7abcfcdc6f4df03ce78d0277da60`  
		Last Modified: Wed, 21 May 2025 23:21:10 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:3a4df444990a16fc80179a029c2aadf80c468bd7cc33f53b43ca72224ddd0071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2745386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2991dea8d3d98549f302ecc388a3f9dccf40d62a040a0b61bf9f0de46ca55b91`

```dockerfile
```

-	Layers:
	-	`sha256:72c746fd4572d6798ecbda4f3011a2121dea40b97cad8c2e204df9fa5754484d`  
		Last Modified: Wed, 21 May 2025 23:21:09 GMT  
		Size: 2.7 MB (2729258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:994a599fa2adc8ef0a9cf6ee98866268caa6f5fd9e24b39e88c31f56b3846d10`  
		Last Modified: Wed, 21 May 2025 23:21:09 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97cc1bc73cdd53d1fb65b54eb2237cb2d74423ba085e2b4becb0d0fec7905be`  
		Last Modified: Tue, 29 Apr 2025 03:42:01 GMT  
		Size: 6.5 MB (6497913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44517418a9729926f5d635549a4bd6176f13585afd47adb69f7c8b08e74c693a`  
		Last Modified: Tue, 29 Apr 2025 03:42:02 GMT  
		Size: 45.6 MB (45564703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5462df3243fd46d86ee7086f625bec52780ef4a05deaa42a8e4083e43f8907bf`  
		Last Modified: Tue, 29 Apr 2025 03:42:00 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d817a3e3afb21bf13b393479698fe8c14f39f2e3b20100e747706b51f9ccd6e`  
		Last Modified: Tue, 29 Apr 2025 03:42:01 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103414f6d083444387facc3936ec4c26348ad1954d8a891d00fa696bf2469258`  
		Last Modified: Tue, 29 Apr 2025 03:42:01 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687d6d5f2d0622b294a8ce4c8f55da85356ba61e9a9ddecaa09b12c45f5dc71b`  
		Last Modified: Tue, 29 Apr 2025 01:50:04 GMT  
		Size: 7.7 MB (7652116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d52f1039bbb6fba3a0e7fc09bf372afbfc17d60d1bcd56c4659f0045214bbcf`  
		Last Modified: Tue, 29 Apr 2025 01:50:05 GMT  
		Size: 47.0 MB (47020557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9028c3e134f78f6ced2c1fc90dfc47fdb06ef46ccb86f256ce6507c93d0dacc`  
		Last Modified: Tue, 29 Apr 2025 01:50:03 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb7f61774f9814fa36e7925e9db6154efe72e897177610f87539565ae136d52`  
		Last Modified: Tue, 29 Apr 2025 01:50:03 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98fc839e4715c63a63e686672b0df5d47e4674fffc5f611891d705038ce7b65`  
		Last Modified: Tue, 29 Apr 2025 01:50:04 GMT  
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
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32870b6e9c13c57b3e4492e862a1cbd13fa1a832304155c5f64e44173ac7210a`  
		Last Modified: Wed, 16 Apr 2025 16:54:32 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b6cec5e7cadf8751915b4bf4bd5d891cfe0949da529d90ae52a376a6dd2f2`  
		Last Modified: Wed, 16 Apr 2025 16:54:32 GMT  
		Size: 296.5 KB (296501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385cb22c2e9fc67ba1ab880b4400b1ea27a4aaaa54082ef5c2bf93e2b1dfe26a`  
		Last Modified: Wed, 16 Apr 2025 16:54:34 GMT  
		Size: 28.5 MB (28525260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a0e6e70a2efdf0942ca9130a6373a2a8aba0e8d0220d1d25700421f387b216`  
		Last Modified: Wed, 16 Apr 2025 16:54:32 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70db9642e4277afac9c14dfb2b300c68da5b2cb5ffb4fe1820dd613997f944`  
		Last Modified: Wed, 16 Apr 2025 16:54:33 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cd8a31daaa972542ed9037d7b7b3ef390e0cb3be4e346df11439e64cb47419`  
		Last Modified: Wed, 16 Apr 2025 16:54:33 GMT  
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
$ docker pull chronograf@sha256:84af7bc8a2265fa109f149bcf0543c6c47d201f86f56ce9b37ed470c807d3db8
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
$ docker pull chronograf@sha256:f9a4491704d2ad6bb41a681ac7a22c7ddfd21792810a0190317b80c9eb7f538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85361392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e633a3cc758266abbcfda81a9213440ce128c909435f912398ad89cba7510fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8efa8a4370fd03594063cc027a3a187f10071b20f22d25026b1e024b06c0609`  
		Last Modified: Wed, 21 May 2025 23:21:09 GMT  
		Size: 7.9 MB (7877884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9631558f3e9059ec4e0def4253294a8d1b50d84cc67f10879f0f3e193d5f5d9`  
		Last Modified: Wed, 21 May 2025 23:21:10 GMT  
		Size: 49.2 MB (49233712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112fb2921522a7cd62b4c6166b3791ab71c8860f860283d16ebb28dea6707658`  
		Last Modified: Wed, 21 May 2025 23:21:09 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32a6d2434b94c306e78b79e5e1d7d433f8d23ac27b31db416f974aff7b6631`  
		Last Modified: Wed, 21 May 2025 23:21:09 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd2295dbeed42367f8d5d0c0ae63fc8ef1b7abcfcdc6f4df03ce78d0277da60`  
		Last Modified: Wed, 21 May 2025 23:21:10 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:3a4df444990a16fc80179a029c2aadf80c468bd7cc33f53b43ca72224ddd0071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2745386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2991dea8d3d98549f302ecc388a3f9dccf40d62a040a0b61bf9f0de46ca55b91`

```dockerfile
```

-	Layers:
	-	`sha256:72c746fd4572d6798ecbda4f3011a2121dea40b97cad8c2e204df9fa5754484d`  
		Last Modified: Wed, 21 May 2025 23:21:09 GMT  
		Size: 2.7 MB (2729258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:994a599fa2adc8ef0a9cf6ee98866268caa6f5fd9e24b39e88c31f56b3846d10`  
		Last Modified: Wed, 21 May 2025 23:21:09 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97cc1bc73cdd53d1fb65b54eb2237cb2d74423ba085e2b4becb0d0fec7905be`  
		Last Modified: Tue, 29 Apr 2025 03:42:01 GMT  
		Size: 6.5 MB (6497913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44517418a9729926f5d635549a4bd6176f13585afd47adb69f7c8b08e74c693a`  
		Last Modified: Tue, 29 Apr 2025 03:42:02 GMT  
		Size: 45.6 MB (45564703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5462df3243fd46d86ee7086f625bec52780ef4a05deaa42a8e4083e43f8907bf`  
		Last Modified: Tue, 29 Apr 2025 03:42:00 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d817a3e3afb21bf13b393479698fe8c14f39f2e3b20100e747706b51f9ccd6e`  
		Last Modified: Tue, 29 Apr 2025 03:42:01 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103414f6d083444387facc3936ec4c26348ad1954d8a891d00fa696bf2469258`  
		Last Modified: Tue, 29 Apr 2025 03:42:01 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687d6d5f2d0622b294a8ce4c8f55da85356ba61e9a9ddecaa09b12c45f5dc71b`  
		Last Modified: Tue, 29 Apr 2025 01:50:04 GMT  
		Size: 7.7 MB (7652116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d52f1039bbb6fba3a0e7fc09bf372afbfc17d60d1bcd56c4659f0045214bbcf`  
		Last Modified: Tue, 29 Apr 2025 01:50:05 GMT  
		Size: 47.0 MB (47020557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9028c3e134f78f6ced2c1fc90dfc47fdb06ef46ccb86f256ce6507c93d0dacc`  
		Last Modified: Tue, 29 Apr 2025 01:50:03 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb7f61774f9814fa36e7925e9db6154efe72e897177610f87539565ae136d52`  
		Last Modified: Tue, 29 Apr 2025 01:50:03 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98fc839e4715c63a63e686672b0df5d47e4674fffc5f611891d705038ce7b65`  
		Last Modified: Tue, 29 Apr 2025 01:50:04 GMT  
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
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32870b6e9c13c57b3e4492e862a1cbd13fa1a832304155c5f64e44173ac7210a`  
		Last Modified: Wed, 16 Apr 2025 16:54:32 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b6cec5e7cadf8751915b4bf4bd5d891cfe0949da529d90ae52a376a6dd2f2`  
		Last Modified: Wed, 16 Apr 2025 16:54:32 GMT  
		Size: 296.5 KB (296501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385cb22c2e9fc67ba1ab880b4400b1ea27a4aaaa54082ef5c2bf93e2b1dfe26a`  
		Last Modified: Wed, 16 Apr 2025 16:54:34 GMT  
		Size: 28.5 MB (28525260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a0e6e70a2efdf0942ca9130a6373a2a8aba0e8d0220d1d25700421f387b216`  
		Last Modified: Wed, 16 Apr 2025 16:54:32 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70db9642e4277afac9c14dfb2b300c68da5b2cb5ffb4fe1820dd613997f944`  
		Last Modified: Wed, 16 Apr 2025 16:54:33 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cd8a31daaa972542ed9037d7b7b3ef390e0cb3be4e346df11439e64cb47419`  
		Last Modified: Wed, 16 Apr 2025 16:54:33 GMT  
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
$ docker pull chronograf@sha256:f1d8726f9acdd40a18f40bd66926ec6f36b9def626b19da39d01e8b59f309f22
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
$ docker pull chronograf@sha256:e5b9a084c6331c0f55ffb8fc19d067b2b617692b4aee732f89818565711a9927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69229270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f39a26997d4e77ee60e568809b06ed4bb36ec1c647c7a1afca4be9e43d5572`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f2416513833f78bbb74265592ef4085530b64ac128a890560f08ae85b4420d`  
		Last Modified: Wed, 21 May 2025 23:20:46 GMT  
		Size: 4.2 MB (4209270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f10adffb2e09ed44bc5ee7af0c8456102f5aa3ceb4a88079a95e7f23177207`  
		Last Modified: Wed, 21 May 2025 23:20:47 GMT  
		Size: 34.7 MB (34739672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c789953e61a7c3da7c684e5eb32302d77311acdd8aeef3eeed08ab56307772`  
		Last Modified: Wed, 21 May 2025 23:20:46 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2221c4f920a4b811a19eb24592c4c1a80ccca66f0d29c59bc965914a5c1d7722`  
		Last Modified: Wed, 21 May 2025 23:20:46 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975b723f287caa1b1c8ef3456109c28c5f479e63444940af3fc031eee57b0521`  
		Last Modified: Wed, 21 May 2025 23:20:47 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:b42693b65a49096cedbd27e8f742a19b520e828a854dad80440d9520f3f15a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2948848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d33d3becd3c22ceece634bbdd71e24e0f9e4da62c87c463b7de2b8071085e6a`

```dockerfile
```

-	Layers:
	-	`sha256:105f147cf8ee51788299466c38d4d39807e326c6346b9d76de7dd9f08988ebf5`  
		Last Modified: Wed, 21 May 2025 23:20:46 GMT  
		Size: 2.9 MB (2933071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb1e7f802d3f45cd80d325d9479a2217f5e8ca31b3ff02fe3f99d817dd195e12`  
		Last Modified: Wed, 21 May 2025 23:20:46 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:16:22 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
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
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8ae06deb09ed334ed8eba44b6e425cced470152dbdd9c0e3c6125578263f57`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69641bcb67c77b895509abb75bf637ce2b76f0acdd981fd282b113d82c04c619`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 294.4 KB (294383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c71c1a03f44724b1796ddc3866d8fe5c4a5af8862448eabb7b2ebdc7a47748`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 19.6 MB (19556823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29450f6d74de26216b10dc587e69dd4443992a6aea3c7b424c7aaad08ceef29`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e84d9f6956c08b6776f1b3db99e0226246d044677f2e4cf470051da809c34e`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030349c6370852b4bfb957d5c0dc77ca8ab49cfd26485c0b053651d825d6caf9`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
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
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 172.3 KB (172345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2af6f071245b63b559b430cac0c4aba0ef1cc49a72e9b52d3edae3f8b2d6ad95`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:f1d8726f9acdd40a18f40bd66926ec6f36b9def626b19da39d01e8b59f309f22
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
$ docker pull chronograf@sha256:e5b9a084c6331c0f55ffb8fc19d067b2b617692b4aee732f89818565711a9927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69229270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f39a26997d4e77ee60e568809b06ed4bb36ec1c647c7a1afca4be9e43d5572`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f2416513833f78bbb74265592ef4085530b64ac128a890560f08ae85b4420d`  
		Last Modified: Wed, 21 May 2025 23:20:46 GMT  
		Size: 4.2 MB (4209270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f10adffb2e09ed44bc5ee7af0c8456102f5aa3ceb4a88079a95e7f23177207`  
		Last Modified: Wed, 21 May 2025 23:20:47 GMT  
		Size: 34.7 MB (34739672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c789953e61a7c3da7c684e5eb32302d77311acdd8aeef3eeed08ab56307772`  
		Last Modified: Wed, 21 May 2025 23:20:46 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2221c4f920a4b811a19eb24592c4c1a80ccca66f0d29c59bc965914a5c1d7722`  
		Last Modified: Wed, 21 May 2025 23:20:46 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975b723f287caa1b1c8ef3456109c28c5f479e63444940af3fc031eee57b0521`  
		Last Modified: Wed, 21 May 2025 23:20:47 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:b42693b65a49096cedbd27e8f742a19b520e828a854dad80440d9520f3f15a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2948848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d33d3becd3c22ceece634bbdd71e24e0f9e4da62c87c463b7de2b8071085e6a`

```dockerfile
```

-	Layers:
	-	`sha256:105f147cf8ee51788299466c38d4d39807e326c6346b9d76de7dd9f08988ebf5`  
		Last Modified: Wed, 21 May 2025 23:20:46 GMT  
		Size: 2.9 MB (2933071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb1e7f802d3f45cd80d325d9479a2217f5e8ca31b3ff02fe3f99d817dd195e12`  
		Last Modified: Wed, 21 May 2025 23:20:46 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:16:22 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
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
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8ae06deb09ed334ed8eba44b6e425cced470152dbdd9c0e3c6125578263f57`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69641bcb67c77b895509abb75bf637ce2b76f0acdd981fd282b113d82c04c619`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 294.4 KB (294383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c71c1a03f44724b1796ddc3866d8fe5c4a5af8862448eabb7b2ebdc7a47748`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 19.6 MB (19556823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29450f6d74de26216b10dc587e69dd4443992a6aea3c7b424c7aaad08ceef29`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e84d9f6956c08b6776f1b3db99e0226246d044677f2e4cf470051da809c34e`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030349c6370852b4bfb957d5c0dc77ca8ab49cfd26485c0b053651d825d6caf9`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
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
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 172.3 KB (172345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2af6f071245b63b559b430cac0c4aba0ef1cc49a72e9b52d3edae3f8b2d6ad95`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:42777e6241a5908a648188f954e868d349e203dd917f928f4d0bd0a187497e6c
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
$ docker pull chronograf@sha256:d7c01691fdb7ac779d832378ce1f7e397ff39955f0803ed1981d375bee6d0416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69870519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d4a67a014633d8e5f436c22b448bb778d83cda7569b0b8d1240dbb34ccfb11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4862f4ebfb20cc55d060d2a2e8f50551aeb26b8920cb9977acf1db346f7148c0`  
		Last Modified: Wed, 21 May 2025 23:20:48 GMT  
		Size: 5.2 MB (5225943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c428ba944b0a1b7918b49f63edb3ad257e55704de41b5578cb872c2b9d481be5`  
		Last Modified: Wed, 21 May 2025 23:20:49 GMT  
		Size: 34.4 MB (34364251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7913a26566c602b4e61b0427c6383b65c03f4af68e2d0ca7418c1a32274f13`  
		Last Modified: Wed, 21 May 2025 23:20:48 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fcaed8ff8d86d5a29c5d5c2b358a30ba7767df91af6ba74d29d04c6d11559d`  
		Last Modified: Wed, 21 May 2025 23:20:48 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec19e0ea44f9a9ad1d2576aa61ea28fd294961252ec4163707df8fe2aeb97c7a`  
		Last Modified: Wed, 21 May 2025 23:20:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:d8c95d07caedd253427afe408f8a43a9cb45fe1a14f56fe46df867d23d4b1b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3004529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a9c85ed922bc71cc926c1e8b925e06972bd51f696755aa17030f4a7b747db8`

```dockerfile
```

-	Layers:
	-	`sha256:c69d5109e9f0c892c42e55cf530d9ee1b27037022daa8c4ab971d36c89eb8d35`  
		Last Modified: Wed, 21 May 2025 23:20:48 GMT  
		Size: 3.0 MB (2988713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9dda0c286be137a9acb601582af564400f0e7551818993121af104151d8b4ad`  
		Last Modified: Wed, 21 May 2025 23:20:48 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:16:22 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
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
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c39259f86321f91341426ea2b7c8164eb8c8a538841604f969c31abd195acba`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bf003f24079392a7a29452383a6db1f26978c48f54533c79153b28b82b7257`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 294.4 KB (294385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb15ecadba26a5095f16beac190b0f35fa020ee3fff220c3243ebb39f58712a`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 19.2 MB (19204154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402cd540f74e77bd8181c883cf26fa3525fd15513ad005bc58b5bed6ddb9d248`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c299e5fdf7b7064f6b152ef78a715eefeff0a18c48c95e7a2b74b34bc318c7f5`  
		Last Modified: Fri, 14 Feb 2025 19:24:45 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ff2dde7922e46ced41d599cff59f593b600debe56130e43867bb3be500e704`  
		Last Modified: Fri, 14 Feb 2025 19:24:45 GMT  
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
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 229.9 KB (229904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ad8d123c697deeb31e83f6f288bbb9095d82109f9902675e157e8b88f35c2b`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:42777e6241a5908a648188f954e868d349e203dd917f928f4d0bd0a187497e6c
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
$ docker pull chronograf@sha256:d7c01691fdb7ac779d832378ce1f7e397ff39955f0803ed1981d375bee6d0416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69870519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d4a67a014633d8e5f436c22b448bb778d83cda7569b0b8d1240dbb34ccfb11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4862f4ebfb20cc55d060d2a2e8f50551aeb26b8920cb9977acf1db346f7148c0`  
		Last Modified: Wed, 21 May 2025 23:20:48 GMT  
		Size: 5.2 MB (5225943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c428ba944b0a1b7918b49f63edb3ad257e55704de41b5578cb872c2b9d481be5`  
		Last Modified: Wed, 21 May 2025 23:20:49 GMT  
		Size: 34.4 MB (34364251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7913a26566c602b4e61b0427c6383b65c03f4af68e2d0ca7418c1a32274f13`  
		Last Modified: Wed, 21 May 2025 23:20:48 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fcaed8ff8d86d5a29c5d5c2b358a30ba7767df91af6ba74d29d04c6d11559d`  
		Last Modified: Wed, 21 May 2025 23:20:48 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec19e0ea44f9a9ad1d2576aa61ea28fd294961252ec4163707df8fe2aeb97c7a`  
		Last Modified: Wed, 21 May 2025 23:20:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:d8c95d07caedd253427afe408f8a43a9cb45fe1a14f56fe46df867d23d4b1b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3004529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a9c85ed922bc71cc926c1e8b925e06972bd51f696755aa17030f4a7b747db8`

```dockerfile
```

-	Layers:
	-	`sha256:c69d5109e9f0c892c42e55cf530d9ee1b27037022daa8c4ab971d36c89eb8d35`  
		Last Modified: Wed, 21 May 2025 23:20:48 GMT  
		Size: 3.0 MB (2988713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9dda0c286be137a9acb601582af564400f0e7551818993121af104151d8b4ad`  
		Last Modified: Wed, 21 May 2025 23:20:48 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:16:22 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
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
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c39259f86321f91341426ea2b7c8164eb8c8a538841604f969c31abd195acba`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bf003f24079392a7a29452383a6db1f26978c48f54533c79153b28b82b7257`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 294.4 KB (294385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb15ecadba26a5095f16beac190b0f35fa020ee3fff220c3243ebb39f58712a`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 19.2 MB (19204154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402cd540f74e77bd8181c883cf26fa3525fd15513ad005bc58b5bed6ddb9d248`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c299e5fdf7b7064f6b152ef78a715eefeff0a18c48c95e7a2b74b34bc318c7f5`  
		Last Modified: Fri, 14 Feb 2025 19:24:45 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ff2dde7922e46ced41d599cff59f593b600debe56130e43867bb3be500e704`  
		Last Modified: Fri, 14 Feb 2025 19:24:45 GMT  
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
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 229.9 KB (229904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ad8d123c697deeb31e83f6f288bbb9095d82109f9902675e157e8b88f35c2b`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:65ce31e214119d9469e6dbe1edd3996dd6bb0690388db934074834d97dd8d6be
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
$ docker pull chronograf@sha256:de6ebfd31e0b5b3037d567150eef45bf91144b2af1458787c8fa54a08e4c787e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70517963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94712f30eb3fa41df1a74e21f902f676ec8c54fd72a4c7584a7ca9cea00a1b42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714ac4bafa8d73d3038414b90c92748e39939815d6dc82a3e4c7dbfd7cc337a4`  
		Last Modified: Wed, 21 May 2025 23:20:54 GMT  
		Size: 5.2 MB (5225959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54758910dd422048a6a9b4a0f8870cf8cc0e1812afe1f8914be4ab45492ed1c9`  
		Last Modified: Wed, 21 May 2025 23:20:55 GMT  
		Size: 35.0 MB (35011674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ad923ae3c78ddf3ae8f0ebd951595e8ad3d3c4ef45bd1fa4c7f20e88012fbd`  
		Last Modified: Wed, 21 May 2025 23:20:54 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30991e179f20d54d09afb2c90b5e1a9664d395b8d4be74bb01355b26e17d146c`  
		Last Modified: Wed, 21 May 2025 23:20:54 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5537981b3b9057ecafb04fd4e19ff0071bedba8f5b8d8d2e2081c1e4f2231d`  
		Last Modified: Wed, 21 May 2025 23:20:55 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:59d9d1f0b301ede329669296bc9e487f198c42a1451c32ab5a8ee45ab1564977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3009732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09951bc7da3ce2621f50ab2400b29ff772f2ce41e86f3ae8d99f4ff6c2b32c96`

```dockerfile
```

-	Layers:
	-	`sha256:a9ffb4428310025af101288f8b77c65e52ea1fbc3453f97771e05bf0c7165c15`  
		Last Modified: Wed, 21 May 2025 23:20:54 GMT  
		Size: 3.0 MB (2993923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a088daf7d333862ed7c3e0d0a99d721d342d3373c0055fa886b04111fa00a3f`  
		Last Modified: Wed, 21 May 2025 23:20:54 GMT  
		Size: 15.8 KB (15809 bytes)  
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
		Last Modified: Mon, 28 Apr 2025 21:16:22 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
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
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de662ab890de5cb0e03103817de459544467d4b3f0784c60d26b56b9057ad500`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69641bcb67c77b895509abb75bf637ce2b76f0acdd981fd282b113d82c04c619`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 294.4 KB (294383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc476e87cc64ce09a8be67509b3baee59f88525efcf0dbb7aa18f0aeeb0823b`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 19.7 MB (19672009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29450f6d74de26216b10dc587e69dd4443992a6aea3c7b424c7aaad08ceef29`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e84d9f6956c08b6776f1b3db99e0226246d044677f2e4cf470051da809c34e`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030349c6370852b4bfb957d5c0dc77ca8ab49cfd26485c0b053651d825d6caf9`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
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
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 235.1 KB (235116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b34d12538bfcd1dd3e2b34c8aa09be9693afe86e4462d7341bee3cf95202f0`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:65ce31e214119d9469e6dbe1edd3996dd6bb0690388db934074834d97dd8d6be
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
$ docker pull chronograf@sha256:de6ebfd31e0b5b3037d567150eef45bf91144b2af1458787c8fa54a08e4c787e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70517963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94712f30eb3fa41df1a74e21f902f676ec8c54fd72a4c7584a7ca9cea00a1b42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714ac4bafa8d73d3038414b90c92748e39939815d6dc82a3e4c7dbfd7cc337a4`  
		Last Modified: Wed, 21 May 2025 23:20:54 GMT  
		Size: 5.2 MB (5225959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54758910dd422048a6a9b4a0f8870cf8cc0e1812afe1f8914be4ab45492ed1c9`  
		Last Modified: Wed, 21 May 2025 23:20:55 GMT  
		Size: 35.0 MB (35011674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ad923ae3c78ddf3ae8f0ebd951595e8ad3d3c4ef45bd1fa4c7f20e88012fbd`  
		Last Modified: Wed, 21 May 2025 23:20:54 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30991e179f20d54d09afb2c90b5e1a9664d395b8d4be74bb01355b26e17d146c`  
		Last Modified: Wed, 21 May 2025 23:20:54 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5537981b3b9057ecafb04fd4e19ff0071bedba8f5b8d8d2e2081c1e4f2231d`  
		Last Modified: Wed, 21 May 2025 23:20:55 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:59d9d1f0b301ede329669296bc9e487f198c42a1451c32ab5a8ee45ab1564977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3009732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09951bc7da3ce2621f50ab2400b29ff772f2ce41e86f3ae8d99f4ff6c2b32c96`

```dockerfile
```

-	Layers:
	-	`sha256:a9ffb4428310025af101288f8b77c65e52ea1fbc3453f97771e05bf0c7165c15`  
		Last Modified: Wed, 21 May 2025 23:20:54 GMT  
		Size: 3.0 MB (2993923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a088daf7d333862ed7c3e0d0a99d721d342d3373c0055fa886b04111fa00a3f`  
		Last Modified: Wed, 21 May 2025 23:20:54 GMT  
		Size: 15.8 KB (15809 bytes)  
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
		Last Modified: Mon, 28 Apr 2025 21:16:22 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
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
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de662ab890de5cb0e03103817de459544467d4b3f0784c60d26b56b9057ad500`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69641bcb67c77b895509abb75bf637ce2b76f0acdd981fd282b113d82c04c619`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 294.4 KB (294383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc476e87cc64ce09a8be67509b3baee59f88525efcf0dbb7aa18f0aeeb0823b`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 19.7 MB (19672009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29450f6d74de26216b10dc587e69dd4443992a6aea3c7b424c7aaad08ceef29`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e84d9f6956c08b6776f1b3db99e0226246d044677f2e4cf470051da809c34e`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030349c6370852b4bfb957d5c0dc77ca8ab49cfd26485c0b053651d825d6caf9`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
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
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 235.1 KB (235116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b34d12538bfcd1dd3e2b34c8aa09be9693afe86e4462d7341bee3cf95202f0`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
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
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32870b6e9c13c57b3e4492e862a1cbd13fa1a832304155c5f64e44173ac7210a`  
		Last Modified: Wed, 16 Apr 2025 16:54:32 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b6cec5e7cadf8751915b4bf4bd5d891cfe0949da529d90ae52a376a6dd2f2`  
		Last Modified: Wed, 16 Apr 2025 16:54:32 GMT  
		Size: 296.5 KB (296501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385cb22c2e9fc67ba1ab880b4400b1ea27a4aaaa54082ef5c2bf93e2b1dfe26a`  
		Last Modified: Wed, 16 Apr 2025 16:54:34 GMT  
		Size: 28.5 MB (28525260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a0e6e70a2efdf0942ca9130a6373a2a8aba0e8d0220d1d25700421f387b216`  
		Last Modified: Wed, 16 Apr 2025 16:54:32 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70db9642e4277afac9c14dfb2b300c68da5b2cb5ffb4fe1820dd613997f944`  
		Last Modified: Wed, 16 Apr 2025 16:54:33 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cd8a31daaa972542ed9037d7b7b3ef390e0cb3be4e346df11439e64cb47419`  
		Last Modified: Wed, 16 Apr 2025 16:54:33 GMT  
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
$ docker pull chronograf@sha256:84af7bc8a2265fa109f149bcf0543c6c47d201f86f56ce9b37ed470c807d3db8
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
$ docker pull chronograf@sha256:f9a4491704d2ad6bb41a681ac7a22c7ddfd21792810a0190317b80c9eb7f538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85361392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e633a3cc758266abbcfda81a9213440ce128c909435f912398ad89cba7510fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8efa8a4370fd03594063cc027a3a187f10071b20f22d25026b1e024b06c0609`  
		Last Modified: Wed, 21 May 2025 23:21:09 GMT  
		Size: 7.9 MB (7877884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9631558f3e9059ec4e0def4253294a8d1b50d84cc67f10879f0f3e193d5f5d9`  
		Last Modified: Wed, 21 May 2025 23:21:10 GMT  
		Size: 49.2 MB (49233712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112fb2921522a7cd62b4c6166b3791ab71c8860f860283d16ebb28dea6707658`  
		Last Modified: Wed, 21 May 2025 23:21:09 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32a6d2434b94c306e78b79e5e1d7d433f8d23ac27b31db416f974aff7b6631`  
		Last Modified: Wed, 21 May 2025 23:21:09 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd2295dbeed42367f8d5d0c0ae63fc8ef1b7abcfcdc6f4df03ce78d0277da60`  
		Last Modified: Wed, 21 May 2025 23:21:10 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:3a4df444990a16fc80179a029c2aadf80c468bd7cc33f53b43ca72224ddd0071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2745386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2991dea8d3d98549f302ecc388a3f9dccf40d62a040a0b61bf9f0de46ca55b91`

```dockerfile
```

-	Layers:
	-	`sha256:72c746fd4572d6798ecbda4f3011a2121dea40b97cad8c2e204df9fa5754484d`  
		Last Modified: Wed, 21 May 2025 23:21:09 GMT  
		Size: 2.7 MB (2729258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:994a599fa2adc8ef0a9cf6ee98866268caa6f5fd9e24b39e88c31f56b3846d10`  
		Last Modified: Wed, 21 May 2025 23:21:09 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97cc1bc73cdd53d1fb65b54eb2237cb2d74423ba085e2b4becb0d0fec7905be`  
		Last Modified: Tue, 29 Apr 2025 03:42:01 GMT  
		Size: 6.5 MB (6497913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44517418a9729926f5d635549a4bd6176f13585afd47adb69f7c8b08e74c693a`  
		Last Modified: Tue, 29 Apr 2025 03:42:02 GMT  
		Size: 45.6 MB (45564703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5462df3243fd46d86ee7086f625bec52780ef4a05deaa42a8e4083e43f8907bf`  
		Last Modified: Tue, 29 Apr 2025 03:42:00 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d817a3e3afb21bf13b393479698fe8c14f39f2e3b20100e747706b51f9ccd6e`  
		Last Modified: Tue, 29 Apr 2025 03:42:01 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103414f6d083444387facc3936ec4c26348ad1954d8a891d00fa696bf2469258`  
		Last Modified: Tue, 29 Apr 2025 03:42:01 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687d6d5f2d0622b294a8ce4c8f55da85356ba61e9a9ddecaa09b12c45f5dc71b`  
		Last Modified: Tue, 29 Apr 2025 01:50:04 GMT  
		Size: 7.7 MB (7652116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d52f1039bbb6fba3a0e7fc09bf372afbfc17d60d1bcd56c4659f0045214bbcf`  
		Last Modified: Tue, 29 Apr 2025 01:50:05 GMT  
		Size: 47.0 MB (47020557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9028c3e134f78f6ced2c1fc90dfc47fdb06ef46ccb86f256ce6507c93d0dacc`  
		Last Modified: Tue, 29 Apr 2025 01:50:03 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb7f61774f9814fa36e7925e9db6154efe72e897177610f87539565ae136d52`  
		Last Modified: Tue, 29 Apr 2025 01:50:03 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98fc839e4715c63a63e686672b0df5d47e4674fffc5f611891d705038ce7b65`  
		Last Modified: Tue, 29 Apr 2025 01:50:04 GMT  
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
