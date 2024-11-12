<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.5`](#chronograf1105)
-	[`chronograf:1.10.5-alpine`](#chronograf1105-alpine)
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
$ docker pull chronograf@sha256:18200f03814c9cb448ed2604d3593447dda4056c967b2f12bcac3d1e22222d33
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
$ docker pull chronograf@sha256:cbb2398ca1e9c1e79905f76a6f508c0b84e124ed19d8bd1ef329113df6bd0554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84245436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef430dd9bd942ea971170a9ad41a7b86bf2b0bd54963f64e172414e8bbf7b6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1224e7e2d3fcfa467dc4f217326c057f4f2dd7300e13ef8f9e857ce39d3b4a1a`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 7.9 MB (7875383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156341f7966c50570025c0aa511f08d25d6323a659a42aed5dbf0d667f59476a`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 47.2 MB (47217593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc833227a91630f06fdbd4aa78c70728725f847e7108c30819c0dd7b1bcc2f1`  
		Last Modified: Tue, 12 Nov 2024 02:38:19 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942d7292f5707350b55e75b6962c10f687a2f79cd6897f52184d0d756f3640af`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59b128af6ad42b6a2e4237a81330a24126fa56928cb1282247f5a0b2e934cce`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:d283d9166d23e08f8f2ecab79a9506abca9aca59180582cf53a41af1716e8570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dff9e10e6a0907fdc037209f268bd74095409b257480933f04b1cad3729d68f`

```dockerfile
```

-	Layers:
	-	`sha256:3e81168bed413e125218f95a0a4120c7164a7f95a704ffc312fa47035416659c`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 2.7 MB (2706777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da14de2590a125267c353c750cc1c061c345a17e9a5da32b3651a9e5dc1c2ec`  
		Last Modified: Tue, 12 Nov 2024 02:38:19 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:45f678c553711d2db70d58535b9794b3ad28d4d84f59d79a55f54f272827789b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75517507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902c66527b2d96a1b1c3a0c88cbe54876f2dbd2a511a4c5fcb504a5a7838819d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6550685acd063dc6cce640c6f10c1dfac73cc458f5b8b19ec449579a08ab1401`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 6.5 MB (6497842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d9638c811aa475e3ef3dd738ebb9839a72c09623ca60283c170c2babda7f6`  
		Last Modified: Tue, 12 Nov 2024 16:06:27 GMT  
		Size: 44.3 MB (44276286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009a1e4b1ee7537b61421076ee24fd717c335f249c42420356c0539a1f6899b9`  
		Last Modified: Tue, 12 Nov 2024 16:06:25 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f869afcceefe33812d97f686e429f4d846795d1cd930495accf77f409f2506`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3c728782b2eeb8dd6001ebe7610861c011ebe762fcafbd576160449ed7bcb0`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:b310981b0390adbddba27b5ffa275d03002a50389474dc02ab36dd4e8c5b9ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2725282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621bb400573b68da87ad02e9d81f7ae8827c3ae22bd31fdb1d8e42dd93d4bd88`

```dockerfile
```

-	Layers:
	-	`sha256:a7b6c982a3a1c70e9c895470939fb5317eb615837e1c7b10cdac4960efaf1f79`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 2.7 MB (2709073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bda2b8c1e48a2737a6f3b881aea6e27ed53014051c50ff50e1613800ad657f8`  
		Last Modified: Tue, 12 Nov 2024 16:06:25 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:55b50dea2f2137ce54f443d25b2abfeae47947ee823b2f08388d6eda47d37d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81804433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22992893a7f71a7317d6d6a37c09a42bd342530c32f54b834b877cf5e2c5ab0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5311845117483a02d47c2a837750ed149b17f6ad45451557d3edf3b2361b65d1`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 7.7 MB (7652059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f1f751938fc31cf6a008145a362d6ef94697cef76dd2dcd3a8bb9c969ba5f5`  
		Last Modified: Tue, 12 Nov 2024 11:20:19 GMT  
		Size: 45.0 MB (44970549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa6316747afbf579f3ace66f98703019df3b8b3d7083660d7e299b89205fc7b`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ad95dbffe5e0b91bcdb9f70a444a19e3b49b1f65366caee2370468e451a8ff`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522a008c121d0b587cccc212b8a01b87d0893dd790681b545ce2777b6031c31f`  
		Last Modified: Tue, 12 Nov 2024 11:20:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:8005aae06ed87a042209bcd22fd86c390c027dfefd1ab385657eb9c4ff90b1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57bfeb1040a95763cafa6296c548fbc9a7c9d83b29c2a572fdd51e3e6aa28ce`

```dockerfile
```

-	Layers:
	-	`sha256:519a1a88095896e326f6589cb0448391ad985d186bae96a9b24df79476d03244`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 2.7 MB (2707049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6e694a5a62286326bdb76d6c68673eb2b6e170f2c7e26eb255c0224ddbc61be`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:e917c05d49569ffc91363b69db1139b3aec3ea352d7e4ab116ac73b5276c1e63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:9177fbf8d1abc0941d457afc9b0e50767dab53c0fa38968d0935948927429e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31808028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09dbf6891fc635a202a911272984b230346ed88f7ed61e7c5b4e6699d84faef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d999415b039365cadf590cb0dee4382b11889c724dd0eab32e010a66c2dda7`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd85d2cc53952cb93e416bed6638ae8631ac933e78edf15edc8f453889c78a4b`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 292.6 KB (292626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c8ac47ff12105d7e2e63bdfecfe44bad8e9ed2abbb6bf69e824e6185e38c30`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 27.9 MB (27866799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e56c6035356fa99cb81386116d4e7f9647b9d607a8d8bf3c7bad00f71e5ae4`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 12.2 KB (12234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404105c04126e648e925115b31e8503e9be79bff0ac07d22b960fce01cc68627`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2d0f282dc22ee43b73a0bfff8802169fb0b6a1285ee756c538a46c2ffc4303`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:fcf8a567d3540090f865ac052c59bda542cc0aebd2c1ad4413eadd03d956c0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 KB (257758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6ab8b16a87c767b2f89aa09b99f84a49a0f574642aff41a53d43e44085627d`

```dockerfile
```

-	Layers:
	-	`sha256:608de47fe583d55de96c34e4f648a275957c4723931f32f5bf45243c183b05fb`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 239.9 KB (239903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cf620aebcdf5b9e70ca057c32bcd31da203ea2fc4f7048080488c8522073c0c`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5`

```console
$ docker pull chronograf@sha256:18200f03814c9cb448ed2604d3593447dda4056c967b2f12bcac3d1e22222d33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10.5` - linux; amd64

```console
$ docker pull chronograf@sha256:cbb2398ca1e9c1e79905f76a6f508c0b84e124ed19d8bd1ef329113df6bd0554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84245436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef430dd9bd942ea971170a9ad41a7b86bf2b0bd54963f64e172414e8bbf7b6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1224e7e2d3fcfa467dc4f217326c057f4f2dd7300e13ef8f9e857ce39d3b4a1a`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 7.9 MB (7875383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156341f7966c50570025c0aa511f08d25d6323a659a42aed5dbf0d667f59476a`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 47.2 MB (47217593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc833227a91630f06fdbd4aa78c70728725f847e7108c30819c0dd7b1bcc2f1`  
		Last Modified: Tue, 12 Nov 2024 02:38:19 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942d7292f5707350b55e75b6962c10f687a2f79cd6897f52184d0d756f3640af`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59b128af6ad42b6a2e4237a81330a24126fa56928cb1282247f5a0b2e934cce`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:d283d9166d23e08f8f2ecab79a9506abca9aca59180582cf53a41af1716e8570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dff9e10e6a0907fdc037209f268bd74095409b257480933f04b1cad3729d68f`

```dockerfile
```

-	Layers:
	-	`sha256:3e81168bed413e125218f95a0a4120c7164a7f95a704ffc312fa47035416659c`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 2.7 MB (2706777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da14de2590a125267c353c750cc1c061c345a17e9a5da32b3651a9e5dc1c2ec`  
		Last Modified: Tue, 12 Nov 2024 02:38:19 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:45f678c553711d2db70d58535b9794b3ad28d4d84f59d79a55f54f272827789b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75517507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902c66527b2d96a1b1c3a0c88cbe54876f2dbd2a511a4c5fcb504a5a7838819d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6550685acd063dc6cce640c6f10c1dfac73cc458f5b8b19ec449579a08ab1401`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 6.5 MB (6497842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d9638c811aa475e3ef3dd738ebb9839a72c09623ca60283c170c2babda7f6`  
		Last Modified: Tue, 12 Nov 2024 16:06:27 GMT  
		Size: 44.3 MB (44276286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009a1e4b1ee7537b61421076ee24fd717c335f249c42420356c0539a1f6899b9`  
		Last Modified: Tue, 12 Nov 2024 16:06:25 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f869afcceefe33812d97f686e429f4d846795d1cd930495accf77f409f2506`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3c728782b2eeb8dd6001ebe7610861c011ebe762fcafbd576160449ed7bcb0`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:b310981b0390adbddba27b5ffa275d03002a50389474dc02ab36dd4e8c5b9ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2725282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621bb400573b68da87ad02e9d81f7ae8827c3ae22bd31fdb1d8e42dd93d4bd88`

```dockerfile
```

-	Layers:
	-	`sha256:a7b6c982a3a1c70e9c895470939fb5317eb615837e1c7b10cdac4960efaf1f79`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 2.7 MB (2709073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bda2b8c1e48a2737a6f3b881aea6e27ed53014051c50ff50e1613800ad657f8`  
		Last Modified: Tue, 12 Nov 2024 16:06:25 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:55b50dea2f2137ce54f443d25b2abfeae47947ee823b2f08388d6eda47d37d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81804433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22992893a7f71a7317d6d6a37c09a42bd342530c32f54b834b877cf5e2c5ab0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5311845117483a02d47c2a837750ed149b17f6ad45451557d3edf3b2361b65d1`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 7.7 MB (7652059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f1f751938fc31cf6a008145a362d6ef94697cef76dd2dcd3a8bb9c969ba5f5`  
		Last Modified: Tue, 12 Nov 2024 11:20:19 GMT  
		Size: 45.0 MB (44970549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa6316747afbf579f3ace66f98703019df3b8b3d7083660d7e299b89205fc7b`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ad95dbffe5e0b91bcdb9f70a444a19e3b49b1f65366caee2370468e451a8ff`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522a008c121d0b587cccc212b8a01b87d0893dd790681b545ce2777b6031c31f`  
		Last Modified: Tue, 12 Nov 2024 11:20:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:8005aae06ed87a042209bcd22fd86c390c027dfefd1ab385657eb9c4ff90b1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57bfeb1040a95763cafa6296c548fbc9a7c9d83b29c2a572fdd51e3e6aa28ce`

```dockerfile
```

-	Layers:
	-	`sha256:519a1a88095896e326f6589cb0448391ad985d186bae96a9b24df79476d03244`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 2.7 MB (2707049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6e694a5a62286326bdb76d6c68673eb2b6e170f2c7e26eb255c0224ddbc61be`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5-alpine`

```console
$ docker pull chronograf@sha256:e917c05d49569ffc91363b69db1139b3aec3ea352d7e4ab116ac73b5276c1e63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.5-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:9177fbf8d1abc0941d457afc9b0e50767dab53c0fa38968d0935948927429e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31808028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09dbf6891fc635a202a911272984b230346ed88f7ed61e7c5b4e6699d84faef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d999415b039365cadf590cb0dee4382b11889c724dd0eab32e010a66c2dda7`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd85d2cc53952cb93e416bed6638ae8631ac933e78edf15edc8f453889c78a4b`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 292.6 KB (292626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c8ac47ff12105d7e2e63bdfecfe44bad8e9ed2abbb6bf69e824e6185e38c30`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 27.9 MB (27866799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e56c6035356fa99cb81386116d4e7f9647b9d607a8d8bf3c7bad00f71e5ae4`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 12.2 KB (12234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404105c04126e648e925115b31e8503e9be79bff0ac07d22b960fce01cc68627`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2d0f282dc22ee43b73a0bfff8802169fb0b6a1285ee756c538a46c2ffc4303`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:fcf8a567d3540090f865ac052c59bda542cc0aebd2c1ad4413eadd03d956c0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 KB (257758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6ab8b16a87c767b2f89aa09b99f84a49a0f574642aff41a53d43e44085627d`

```dockerfile
```

-	Layers:
	-	`sha256:608de47fe583d55de96c34e4f648a275957c4723931f32f5bf45243c183b05fb`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 239.9 KB (239903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cf620aebcdf5b9e70ca057c32bcd31da203ea2fc4f7048080488c8522073c0c`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:c1307ae8a73a38f19015a96e8e9c6ecbe893e50891efab9b3ff632268bb9f55f
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
$ docker pull chronograf@sha256:2e049b9a32b3c7088f9c802f7923d91d4242c8ef07f8d1c5694c657730b344a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70218746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05d82d0aa19e8425c3e53f13b83e8901ef2d875a7ddc5bf7348a6e80d68e438`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd178515fec27036d2917939188bb7e5fe2f7221764e88a3cd02e69f2eb56b4`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 4.2 MB (4209304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebac161544dc4658cc814aad81b0ff86bd1d898e91f0338551c49b3016088402`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 34.5 MB (34533493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60528a108f9e014fac4c88d7296bc87640fa6dc870be9556a38b77052eb37d17`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d765878602b49619efdfaf06bad80588374d00c52cd8bcb12e58e429353ff33c`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c578b6b26676ec6f489b38e7793a1c9f45f29f1b6b2d08f0cbfb56cfdf15eb1a`  
		Last Modified: Tue, 12 Nov 2024 02:38:22 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:239a24ec96d5152a662ed774fd93d6370d8d1af285516c25c7903fbb742ca3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2925487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc474012545f814205c43db413af10950e0de4ae35bad155ee8f62215822d9d3`

```dockerfile
```

-	Layers:
	-	`sha256:26661d4e888049dfe670c2fc04261cdfcd4555b0f715a38a5ef4d762e1ed17c8`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 2.9 MB (2909710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e019200dd299ab18cc283e7937105f43642f6b99cde77a24a7ec9350cddd98d`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c1c5f694705fce3fbe449e7ed1b7bb044b5c15604880f4b148295401932e1fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63038303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3544fa788e4eb9d2fa9e298d55283f7e96616ccbba747ad15d0bcd9821b8bc49`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e86de284799b39b69899ac399f34a7e299d0ca33cebde1afa32aa2fce74e7c`  
		Last Modified: Tue, 12 Nov 2024 16:03:41 GMT  
		Size: 3.5 MB (3511727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f595c92af9e20b5ce1f7f0d0b17c42f7b8d5fe65ee105cc8d6653f82c00d65f`  
		Last Modified: Tue, 12 Nov 2024 16:03:42 GMT  
		Size: 32.9 MB (32892923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d3d977cf89ece02f427f7939d8234b22f1aa42137ee568d635f0b0d153e3e1`  
		Last Modified: Tue, 12 Nov 2024 16:03:41 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd85221d37ddf5147c2ab226fdfa2606e9efa138e5efaded81d945fda08fe98`  
		Last Modified: Tue, 12 Nov 2024 16:03:41 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9cdb5db7614542db1972a5e5227c5b5ae80fc3431a52f8a2e5ba9a264960b6`  
		Last Modified: Tue, 12 Nov 2024 16:03:42 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:ec43459aa0a16c69bf7f8625ae42ed8708bb247c9bcf3a06d91765694723aa6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2927829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c0716827457303b9a452dd07c6643bc521dd374f0036bc41b11efe82ba15b2`

```dockerfile
```

-	Layers:
	-	`sha256:5b7dd43acae4dd22ac445e34bc88f5a97b86c965136335b517dade9815bddb18`  
		Last Modified: Tue, 12 Nov 2024 16:03:41 GMT  
		Size: 2.9 MB (2911980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:764ac41752faa72e6c79507c775d81dd2f15bee47ab151c89e50f10188a04218`  
		Last Modified: Tue, 12 Nov 2024 16:03:41 GMT  
		Size: 15.8 KB (15849 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c25706ba1c9d2b372a3b1e97d82ce91bac528f55ae185f1f081336251ddba04e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67359641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec7cc6a5deff5011b0630a01114cdbbad2dddb6114a12d1a82be13a03313759`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d02a969d1f41b971ddae3fa5af00628a2e782311821ecd4f1ff08089347c28f`  
		Last Modified: Tue, 12 Nov 2024 11:18:18 GMT  
		Size: 4.2 MB (4210589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2b48722c160770ed4cdb2930ee221f32f577fd275a106df4930fdda8d995e4`  
		Last Modified: Tue, 12 Nov 2024 11:18:19 GMT  
		Size: 33.0 MB (33033065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a194ce2cc1ab2334d19529b6553ef8bae28edd86629399b02e996d25c75a3c`  
		Last Modified: Tue, 12 Nov 2024 11:18:18 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0684c6dd8bffd4c18ccd41827c63081ee4c49502ed57ecdf08e8fe0b03a24eb4`  
		Last Modified: Tue, 12 Nov 2024 11:18:18 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4e2104220746412771eb1850ca0382fc3b11b8f4be2eec3c6d2f79550c1606`  
		Last Modified: Tue, 12 Nov 2024 11:18:19 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:38ef3edfb866be7846da28646c96116894f1ea6822d7a70043358a4477552e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2925830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd09bd747a3183ce1e73bb2bf96b5a8b9bb2a90d94ef23f84b0e0632b07f4c4c`

```dockerfile
```

-	Layers:
	-	`sha256:b34056a0a4ee3ef4e8aaa0e840f77dad498ba262c4c588c46d1c7b1964c23fc4`  
		Last Modified: Tue, 12 Nov 2024 11:18:18 GMT  
		Size: 2.9 MB (2909958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:197a67cb9d671b66f0cc466ea3491a84e86717199847a1d4a8af26c1a0e16764`  
		Last Modified: Tue, 12 Nov 2024 11:18:18 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:287ff0fe62f1d938c9f5a4276ffdac4b96b80a9fe3f1c5cd2a5fe136a8b60b07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:e590b22cd07479b45e4b1e21199857d7b8dad3afdadf9fbf74affe9e22fbaeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23496129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ee9cbce84cddf5af1b3cec11a1bec04e7c131c56c4e0ab88301e36b1c61f66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d999415b039365cadf590cb0dee4382b11889c724dd0eab32e010a66c2dda7`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bb0c63a516b7d1c4b6f1b8b33078458f7cbd1898070843f549e6d43cd5324d`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 290.9 KB (290886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9ab55224078be68f4a7871e8058733688c9eb20b9ac31ef4ecad44b26714f0`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 19.6 MB (19556696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782f73fe87195977b450fc5374cb4eb5706d48954c1f955f9a381f81c91a51b8`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 12.2 KB (12233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14c1d264bde5e62a8767474eb0bbec13ddf17d34ee732fe1b1fcfed60e89672`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e310fd68fe32a67bc64c8924a620d071699d04bea0e7015d71946c0ab8d28c43`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:43cb3142ea3dde7754a8511a1bf59b24c421ce486acc40e35e5d2ca247019c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 KB (188251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f960e3661dbab4d85d385021946762c4fe6b9774a09368fcf9fb0ef400426ed`

```dockerfile
```

-	Layers:
	-	`sha256:247771501dba854ae3371fbeb61ba23468ea08d067b3a7b9ce93ea0def7bd516`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 171.3 KB (171339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae95d3380a26f742724416d959bc64a1d708327eda838c26bff991cbbcd839e3`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:c1307ae8a73a38f19015a96e8e9c6ecbe893e50891efab9b3ff632268bb9f55f
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
$ docker pull chronograf@sha256:2e049b9a32b3c7088f9c802f7923d91d4242c8ef07f8d1c5694c657730b344a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70218746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05d82d0aa19e8425c3e53f13b83e8901ef2d875a7ddc5bf7348a6e80d68e438`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd178515fec27036d2917939188bb7e5fe2f7221764e88a3cd02e69f2eb56b4`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 4.2 MB (4209304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebac161544dc4658cc814aad81b0ff86bd1d898e91f0338551c49b3016088402`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 34.5 MB (34533493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60528a108f9e014fac4c88d7296bc87640fa6dc870be9556a38b77052eb37d17`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d765878602b49619efdfaf06bad80588374d00c52cd8bcb12e58e429353ff33c`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c578b6b26676ec6f489b38e7793a1c9f45f29f1b6b2d08f0cbfb56cfdf15eb1a`  
		Last Modified: Tue, 12 Nov 2024 02:38:22 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:239a24ec96d5152a662ed774fd93d6370d8d1af285516c25c7903fbb742ca3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2925487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc474012545f814205c43db413af10950e0de4ae35bad155ee8f62215822d9d3`

```dockerfile
```

-	Layers:
	-	`sha256:26661d4e888049dfe670c2fc04261cdfcd4555b0f715a38a5ef4d762e1ed17c8`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 2.9 MB (2909710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e019200dd299ab18cc283e7937105f43642f6b99cde77a24a7ec9350cddd98d`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c1c5f694705fce3fbe449e7ed1b7bb044b5c15604880f4b148295401932e1fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63038303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3544fa788e4eb9d2fa9e298d55283f7e96616ccbba747ad15d0bcd9821b8bc49`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e86de284799b39b69899ac399f34a7e299d0ca33cebde1afa32aa2fce74e7c`  
		Last Modified: Tue, 12 Nov 2024 16:03:41 GMT  
		Size: 3.5 MB (3511727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f595c92af9e20b5ce1f7f0d0b17c42f7b8d5fe65ee105cc8d6653f82c00d65f`  
		Last Modified: Tue, 12 Nov 2024 16:03:42 GMT  
		Size: 32.9 MB (32892923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d3d977cf89ece02f427f7939d8234b22f1aa42137ee568d635f0b0d153e3e1`  
		Last Modified: Tue, 12 Nov 2024 16:03:41 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd85221d37ddf5147c2ab226fdfa2606e9efa138e5efaded81d945fda08fe98`  
		Last Modified: Tue, 12 Nov 2024 16:03:41 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9cdb5db7614542db1972a5e5227c5b5ae80fc3431a52f8a2e5ba9a264960b6`  
		Last Modified: Tue, 12 Nov 2024 16:03:42 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:ec43459aa0a16c69bf7f8625ae42ed8708bb247c9bcf3a06d91765694723aa6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2927829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c0716827457303b9a452dd07c6643bc521dd374f0036bc41b11efe82ba15b2`

```dockerfile
```

-	Layers:
	-	`sha256:5b7dd43acae4dd22ac445e34bc88f5a97b86c965136335b517dade9815bddb18`  
		Last Modified: Tue, 12 Nov 2024 16:03:41 GMT  
		Size: 2.9 MB (2911980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:764ac41752faa72e6c79507c775d81dd2f15bee47ab151c89e50f10188a04218`  
		Last Modified: Tue, 12 Nov 2024 16:03:41 GMT  
		Size: 15.8 KB (15849 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c25706ba1c9d2b372a3b1e97d82ce91bac528f55ae185f1f081336251ddba04e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67359641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec7cc6a5deff5011b0630a01114cdbbad2dddb6114a12d1a82be13a03313759`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d02a969d1f41b971ddae3fa5af00628a2e782311821ecd4f1ff08089347c28f`  
		Last Modified: Tue, 12 Nov 2024 11:18:18 GMT  
		Size: 4.2 MB (4210589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2b48722c160770ed4cdb2930ee221f32f577fd275a106df4930fdda8d995e4`  
		Last Modified: Tue, 12 Nov 2024 11:18:19 GMT  
		Size: 33.0 MB (33033065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a194ce2cc1ab2334d19529b6553ef8bae28edd86629399b02e996d25c75a3c`  
		Last Modified: Tue, 12 Nov 2024 11:18:18 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0684c6dd8bffd4c18ccd41827c63081ee4c49502ed57ecdf08e8fe0b03a24eb4`  
		Last Modified: Tue, 12 Nov 2024 11:18:18 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4e2104220746412771eb1850ca0382fc3b11b8f4be2eec3c6d2f79550c1606`  
		Last Modified: Tue, 12 Nov 2024 11:18:19 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:38ef3edfb866be7846da28646c96116894f1ea6822d7a70043358a4477552e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2925830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd09bd747a3183ce1e73bb2bf96b5a8b9bb2a90d94ef23f84b0e0632b07f4c4c`

```dockerfile
```

-	Layers:
	-	`sha256:b34056a0a4ee3ef4e8aaa0e840f77dad498ba262c4c588c46d1c7b1964c23fc4`  
		Last Modified: Tue, 12 Nov 2024 11:18:18 GMT  
		Size: 2.9 MB (2909958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:197a67cb9d671b66f0cc466ea3491a84e86717199847a1d4a8af26c1a0e16764`  
		Last Modified: Tue, 12 Nov 2024 11:18:18 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:287ff0fe62f1d938c9f5a4276ffdac4b96b80a9fe3f1c5cd2a5fe136a8b60b07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:e590b22cd07479b45e4b1e21199857d7b8dad3afdadf9fbf74affe9e22fbaeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23496129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ee9cbce84cddf5af1b3cec11a1bec04e7c131c56c4e0ab88301e36b1c61f66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d999415b039365cadf590cb0dee4382b11889c724dd0eab32e010a66c2dda7`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bb0c63a516b7d1c4b6f1b8b33078458f7cbd1898070843f549e6d43cd5324d`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 290.9 KB (290886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9ab55224078be68f4a7871e8058733688c9eb20b9ac31ef4ecad44b26714f0`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 19.6 MB (19556696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782f73fe87195977b450fc5374cb4eb5706d48954c1f955f9a381f81c91a51b8`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 12.2 KB (12233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14c1d264bde5e62a8767474eb0bbec13ddf17d34ee732fe1b1fcfed60e89672`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e310fd68fe32a67bc64c8924a620d071699d04bea0e7015d71946c0ab8d28c43`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:43cb3142ea3dde7754a8511a1bf59b24c421ce486acc40e35e5d2ca247019c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 KB (188251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f960e3661dbab4d85d385021946762c4fe6b9774a09368fcf9fb0ef400426ed`

```dockerfile
```

-	Layers:
	-	`sha256:247771501dba854ae3371fbeb61ba23468ea08d067b3a7b9ce93ea0def7bd516`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 171.3 KB (171339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae95d3380a26f742724416d959bc64a1d708327eda838c26bff991cbbcd839e3`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:a6be835c39ef9fec291da6454b93a4a8e1b1e37dd18757e9af57e4e68d772490
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
$ docker pull chronograf@sha256:c6e9646764e6944c7c8fc138539632b3bd8cc064914a36174e6c576ae6465403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70860520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389c547c19e9286bc658a37a71155ccd5486f7d8fbc5d51268af58036fbbf446`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7074b6f8a051b34df09afd81984702756eac1a6d80ba80df612d4e91b9dbe3`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 5.0 MB (5020317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e8ce1b138a4e7eb1283d723db328262df8d9d3856abe75faa754077f200881`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 34.4 MB (34364253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73f9633ce34099e462eab26842cf9f3573f170e0f4d0ffdaf317e269f5c8d73`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120606c6913bce6b726210d1c4b0140fda3e7b5fc8a4414471d50fe1dbb6da81`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383e51ee302fafcf5b6a9f4152f42d85cc2539d4b381d9d88c85799a610537af`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:43f24eee2e8d6fb1ad09c47e1a7fe8c9e702bc0f131c2cefbd795e740d2f8f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c42cfda542739a5405cfc3abc2e1d0aab363bfc81fe03c246d12d32c34ca3e`

```dockerfile
```

-	Layers:
	-	`sha256:818a923debf8be6a6daa6a0ce0a06e8c5920c4d05e010ae252bbb4363deade66`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 3.0 MB (2965808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6739731f2a91e929f4d41f825d19d398803be2aa001feef1d0b9c709e05b699`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d7d6954d7fd4aab60890b8d7624bda675bcd549a9e54c8b1744a80ca07a85260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63453986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99eb1856242f898da63b992fdd037edaa885004b3032c9ba497d8d6e201d97e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76d0fca1db4a044faf08522a97847fc66e7e267da5542f8bc65fe610e106f08`  
		Last Modified: Tue, 12 Nov 2024 16:04:50 GMT  
		Size: 4.3 MB (4285456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fcfa7230636b263ff76ac4fe23a9870068288825083d14e0f44f8aa58120d6`  
		Last Modified: Tue, 12 Nov 2024 16:04:51 GMT  
		Size: 32.5 MB (32534875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77488472c2eb5f2d59dee7492b3e11d348378c2766df3a7bd3eb1d7529a8430`  
		Last Modified: Tue, 12 Nov 2024 16:04:50 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ecc94ed5fa6cc46954c64eccdfeffce3f3a39fb6ec27cad3e9d782fc4e18df`  
		Last Modified: Tue, 12 Nov 2024 16:04:50 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed11325cad19cc333b89724dfc65d6f9fb0a427e7d283cecfb3d4c957486c1d1`  
		Last Modified: Tue, 12 Nov 2024 16:04:51 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:345fd6d64437794416af8b10c449de17a799b508c606e9370c4d0914a878985e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958f2d498caf8465e94d71fa69743fb005c5cbd421727c7c546f1644374003dc`

```dockerfile
```

-	Layers:
	-	`sha256:ccacc90fc91acc02bd6fe5c06e4af6a45b91cd022df7f360fc21e0bacbbfd397`  
		Last Modified: Tue, 12 Nov 2024 16:04:50 GMT  
		Size: 3.0 MB (2968078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22e52bbdfb233b28907f03d1027ca9b3da799269f95c42f01363cb4a5a227743`  
		Last Modified: Tue, 12 Nov 2024 16:04:49 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:21e2d46265df24f26b4b248b1839a379eaa67f013bafd65f8dee3af1932bbdd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67549023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b861d4287146fe96efc22772a772136179fa72593d6f0d3a616acf6e3ee3928`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f1bb528f6fc096401d9e476b66580bf822afa9857615e63939165ad97eb6f5`  
		Last Modified: Tue, 12 Nov 2024 11:19:03 GMT  
		Size: 5.0 MB (5003579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c12be78e894a65ab3ce98677ac15fdec36b7fd13946fd9b7643f40350d4abfc`  
		Last Modified: Tue, 12 Nov 2024 11:19:03 GMT  
		Size: 32.4 MB (32429460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e308a39fae1aee730583bb57e11542aa9e565cbfc530f8fc37e67324aa559720`  
		Last Modified: Tue, 12 Nov 2024 11:19:02 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5001351647235b4a825b44c2938d796f1effdc49ff76394ef2e8bcfa5e12d3`  
		Last Modified: Tue, 12 Nov 2024 11:19:02 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68d3cc3618480410999ed5483f11039991a3899e1b61cb500455eb9096afb8d`  
		Last Modified: Tue, 12 Nov 2024 11:19:03 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:665226dc93485284593da4bf9557e295271452eedd817cd77bef693778653288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47565d1effbb35f20fe97b8f709fd7ada309b63b71defc9ec7870e13d2027061`

```dockerfile
```

-	Layers:
	-	`sha256:2f89e12fb9564c72b6f86c327b8bd265490d7d796d6cb9e8d6a1cb91d0eaa5b0`  
		Last Modified: Tue, 12 Nov 2024 11:19:03 GMT  
		Size: 3.0 MB (2966056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c677b931baa45df9244fec08823c18f591e9b2fcddf1e5b5ef05bd4c17678ad0`  
		Last Modified: Tue, 12 Nov 2024 11:19:02 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:92dc915f49a171a9bff9c19efc9a24e8c79d4b27b352785d02e8b337da5c9289
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:bcb0d37b5c18fb36680f7eb5ce3e0453be8e8385449c26644be8e3f92518aa62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23143481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be622339b1663b25fee8bc1addea46f9fe079dbde554e6cea10b9988b928b57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f837f0e9fa34b0ee2116e7f1db559192bed2b3210feab89b723dd970f6fdb28b`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3982c112ae596e0cf07497f1016dc504b80fd0ad68cc723f7f2066e1aa7c0a55`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 290.9 KB (290887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e7272e467da9f0a75a0f807ca4b262a06aee61541f7014b554868ade8fc95b`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 19.2 MB (19204040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29657181aa450b81b61910eeb70b371a8216c40ae4a395a7a79a49f5956181f7`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2062c76035454d3284bbc7ca4f0c61310bbb4d60df320b9c9c456b4fdd023e8`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b05a1c7abb5eb31b653dd382a993cea9700df0838f570c317de0e5d211af6fc`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:f8bddac8d03188aa5158f46ab76e02927dc923117f8eac59fa9ab0750bf56ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 KB (245222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3beca0b115f7a7d4f457168aa29385f5b3134e4b669263817d46a2a82e0370a4`

```dockerfile
```

-	Layers:
	-	`sha256:35214902caaa7ed50f2443bb8424883e23a2fe8f20c545e1260430164b8c05d9`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 228.3 KB (228310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14c355a1a64de3b8bb5d6a1704de421d53d0023b84d87ae4e790f4724694481`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:a6be835c39ef9fec291da6454b93a4a8e1b1e37dd18757e9af57e4e68d772490
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
$ docker pull chronograf@sha256:c6e9646764e6944c7c8fc138539632b3bd8cc064914a36174e6c576ae6465403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70860520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389c547c19e9286bc658a37a71155ccd5486f7d8fbc5d51268af58036fbbf446`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7074b6f8a051b34df09afd81984702756eac1a6d80ba80df612d4e91b9dbe3`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 5.0 MB (5020317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e8ce1b138a4e7eb1283d723db328262df8d9d3856abe75faa754077f200881`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 34.4 MB (34364253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73f9633ce34099e462eab26842cf9f3573f170e0f4d0ffdaf317e269f5c8d73`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120606c6913bce6b726210d1c4b0140fda3e7b5fc8a4414471d50fe1dbb6da81`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383e51ee302fafcf5b6a9f4152f42d85cc2539d4b381d9d88c85799a610537af`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:43f24eee2e8d6fb1ad09c47e1a7fe8c9e702bc0f131c2cefbd795e740d2f8f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c42cfda542739a5405cfc3abc2e1d0aab363bfc81fe03c246d12d32c34ca3e`

```dockerfile
```

-	Layers:
	-	`sha256:818a923debf8be6a6daa6a0ce0a06e8c5920c4d05e010ae252bbb4363deade66`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 3.0 MB (2965808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6739731f2a91e929f4d41f825d19d398803be2aa001feef1d0b9c709e05b699`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d7d6954d7fd4aab60890b8d7624bda675bcd549a9e54c8b1744a80ca07a85260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63453986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99eb1856242f898da63b992fdd037edaa885004b3032c9ba497d8d6e201d97e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76d0fca1db4a044faf08522a97847fc66e7e267da5542f8bc65fe610e106f08`  
		Last Modified: Tue, 12 Nov 2024 16:04:50 GMT  
		Size: 4.3 MB (4285456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fcfa7230636b263ff76ac4fe23a9870068288825083d14e0f44f8aa58120d6`  
		Last Modified: Tue, 12 Nov 2024 16:04:51 GMT  
		Size: 32.5 MB (32534875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77488472c2eb5f2d59dee7492b3e11d348378c2766df3a7bd3eb1d7529a8430`  
		Last Modified: Tue, 12 Nov 2024 16:04:50 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ecc94ed5fa6cc46954c64eccdfeffce3f3a39fb6ec27cad3e9d782fc4e18df`  
		Last Modified: Tue, 12 Nov 2024 16:04:50 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed11325cad19cc333b89724dfc65d6f9fb0a427e7d283cecfb3d4c957486c1d1`  
		Last Modified: Tue, 12 Nov 2024 16:04:51 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:345fd6d64437794416af8b10c449de17a799b508c606e9370c4d0914a878985e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958f2d498caf8465e94d71fa69743fb005c5cbd421727c7c546f1644374003dc`

```dockerfile
```

-	Layers:
	-	`sha256:ccacc90fc91acc02bd6fe5c06e4af6a45b91cd022df7f360fc21e0bacbbfd397`  
		Last Modified: Tue, 12 Nov 2024 16:04:50 GMT  
		Size: 3.0 MB (2968078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22e52bbdfb233b28907f03d1027ca9b3da799269f95c42f01363cb4a5a227743`  
		Last Modified: Tue, 12 Nov 2024 16:04:49 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:21e2d46265df24f26b4b248b1839a379eaa67f013bafd65f8dee3af1932bbdd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67549023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b861d4287146fe96efc22772a772136179fa72593d6f0d3a616acf6e3ee3928`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f1bb528f6fc096401d9e476b66580bf822afa9857615e63939165ad97eb6f5`  
		Last Modified: Tue, 12 Nov 2024 11:19:03 GMT  
		Size: 5.0 MB (5003579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c12be78e894a65ab3ce98677ac15fdec36b7fd13946fd9b7643f40350d4abfc`  
		Last Modified: Tue, 12 Nov 2024 11:19:03 GMT  
		Size: 32.4 MB (32429460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e308a39fae1aee730583bb57e11542aa9e565cbfc530f8fc37e67324aa559720`  
		Last Modified: Tue, 12 Nov 2024 11:19:02 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5001351647235b4a825b44c2938d796f1effdc49ff76394ef2e8bcfa5e12d3`  
		Last Modified: Tue, 12 Nov 2024 11:19:02 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68d3cc3618480410999ed5483f11039991a3899e1b61cb500455eb9096afb8d`  
		Last Modified: Tue, 12 Nov 2024 11:19:03 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:665226dc93485284593da4bf9557e295271452eedd817cd77bef693778653288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47565d1effbb35f20fe97b8f709fd7ada309b63b71defc9ec7870e13d2027061`

```dockerfile
```

-	Layers:
	-	`sha256:2f89e12fb9564c72b6f86c327b8bd265490d7d796d6cb9e8d6a1cb91d0eaa5b0`  
		Last Modified: Tue, 12 Nov 2024 11:19:03 GMT  
		Size: 3.0 MB (2966056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c677b931baa45df9244fec08823c18f591e9b2fcddf1e5b5ef05bd4c17678ad0`  
		Last Modified: Tue, 12 Nov 2024 11:19:02 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:92dc915f49a171a9bff9c19efc9a24e8c79d4b27b352785d02e8b337da5c9289
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:bcb0d37b5c18fb36680f7eb5ce3e0453be8e8385449c26644be8e3f92518aa62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23143481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be622339b1663b25fee8bc1addea46f9fe079dbde554e6cea10b9988b928b57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f837f0e9fa34b0ee2116e7f1db559192bed2b3210feab89b723dd970f6fdb28b`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3982c112ae596e0cf07497f1016dc504b80fd0ad68cc723f7f2066e1aa7c0a55`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 290.9 KB (290887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e7272e467da9f0a75a0f807ca4b262a06aee61541f7014b554868ade8fc95b`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 19.2 MB (19204040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29657181aa450b81b61910eeb70b371a8216c40ae4a395a7a79a49f5956181f7`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2062c76035454d3284bbc7ca4f0c61310bbb4d60df320b9c9c456b4fdd023e8`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b05a1c7abb5eb31b653dd382a993cea9700df0838f570c317de0e5d211af6fc`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:f8bddac8d03188aa5158f46ab76e02927dc923117f8eac59fa9ab0750bf56ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 KB (245222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3beca0b115f7a7d4f457168aa29385f5b3134e4b669263817d46a2a82e0370a4`

```dockerfile
```

-	Layers:
	-	`sha256:35214902caaa7ed50f2443bb8424883e23a2fe8f20c545e1260430164b8c05d9`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 228.3 KB (228310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14c355a1a64de3b8bb5d6a1704de421d53d0023b84d87ae4e790f4724694481`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:59ebc28e702536afac90c1c4b58839ff30a9e01322ad2e1177fbe813b481760c
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
$ docker pull chronograf@sha256:50f64bb06992802aa96de3033cf731c736f1621cded83feb97eda1dd42166e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71507977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc626241470aaf35f5fe1d297c6353899e98a2324d39e8863317365d9cd53a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38acb0bdae8b7299b96bef5f8d902e06eaa5730c3353379420ad02145e6ea8e5`  
		Last Modified: Tue, 12 Nov 2024 02:38:17 GMT  
		Size: 5.0 MB (5020322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c0badaffefb66097a9ebaef1b2a1698156c9e65188a72882f4dc3419e05eec`  
		Last Modified: Tue, 12 Nov 2024 02:38:18 GMT  
		Size: 35.0 MB (35011707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8281a0a1524081d8e4a61cac212e2a2c5134e0c2a5c0d194a4ee158128fc06da`  
		Last Modified: Tue, 12 Nov 2024 02:38:17 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac6883e6ccb3f1e5a4a1492b27006fe8cdf3e0f52a8bbfdd8a41432df91ed3b`  
		Last Modified: Tue, 12 Nov 2024 02:38:17 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6c6eb440cc51a6837c2ebf0c98b854b841dbc69474306bad8d42ff03d78946`  
		Last Modified: Tue, 12 Nov 2024 02:38:18 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:13662c24a905ca7e3f1c449c9cb46fdad1e5413ba932ec9949986a7247ca174e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0e4422cf787b178201e3619b3205102559c6d459e9a73bf0901e7770f43bf`

```dockerfile
```

-	Layers:
	-	`sha256:708ce5c455fb8bc4b30f6c09c73121f1e8bdc2192c4ab924d32cbd6cfd8a5826`  
		Last Modified: Tue, 12 Nov 2024 02:38:17 GMT  
		Size: 3.0 MB (2970958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fcacb9190786f8752ff5e11b6c18da279269f786f6d08106626b1ca38baa6e`  
		Last Modified: Tue, 12 Nov 2024 02:38:17 GMT  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:be1bc44ad7a448f8b76ed626885dd87bf8a64a4439948161d1b84dfb9da24c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64230635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de60101b590c14bee87d0954707bf670bf8ee4fedb77b9da37d4c60708a1b5ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76d0fca1db4a044faf08522a97847fc66e7e267da5542f8bc65fe610e106f08`  
		Last Modified: Tue, 12 Nov 2024 16:04:50 GMT  
		Size: 4.3 MB (4285456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925fe4b840e6b2aa003870d0a452f0c22fb0f736d62b6158e8d47cf0917a56f`  
		Last Modified: Tue, 12 Nov 2024 16:05:32 GMT  
		Size: 33.3 MB (33311523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a93dc802863f365b023bbdfa88ec35de4d4093e176cb5b89e698c26c9ab5d0b`  
		Last Modified: Tue, 12 Nov 2024 16:05:31 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddde9edf2a28beda7cc59a41fa8cbdf4d7054ff2e6d736760ea37deb61ec0e94`  
		Last Modified: Tue, 12 Nov 2024 16:05:31 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53b6ad43a1916d84c5640b4c9c8046ce758fafc39f1dac7887492f182fcb03b`  
		Last Modified: Tue, 12 Nov 2024 16:05:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:a7a1ceb05758d05082c0a423533b7248fdf7d291aab10d2745f599b7169178ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2989111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a9810a211ebfde38c90dee4d98d754313fe38f54e661363ac0fe34d4831dda`

```dockerfile
```

-	Layers:
	-	`sha256:bef13d45e3ddfd22f3337a796ae159b53a972132c5b63be4a7fe23b36d83f8e2`  
		Last Modified: Tue, 12 Nov 2024 16:05:31 GMT  
		Size: 3.0 MB (2973228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:177f0c391e14922c9b7ef31b6218c5499bcda996876d5a7e4215fd535aceae20`  
		Last Modified: Tue, 12 Nov 2024 16:05:31 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:0e02e909b958d0b13f422b018a39cb6b5a229628caa0d90464c47f696e7fede4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68301073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e06e425c41e2492545ed4f5de31b5f520bfc1db3b13b6573ff0e68d02646d5f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f1bb528f6fc096401d9e476b66580bf822afa9857615e63939165ad97eb6f5`  
		Last Modified: Tue, 12 Nov 2024 11:19:03 GMT  
		Size: 5.0 MB (5003579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30d137d96eec0c6c14194fd60544937658999c185476f77b74829d0611ab469`  
		Last Modified: Tue, 12 Nov 2024 11:19:31 GMT  
		Size: 33.2 MB (33181500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9f082ae9ddc143e967720686dcc862bef2a59bf02358bc86d87524eb1d3f17`  
		Last Modified: Tue, 12 Nov 2024 11:19:29 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498940ca92bda8e3e4610318efeb838d755812144ef66a31dfda0dc040a6a66d`  
		Last Modified: Tue, 12 Nov 2024 11:19:29 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fd7c6b66993576aa75ad6111a957adf90c7d965e9712f7e4cb5cf24563e9be`  
		Last Modified: Tue, 12 Nov 2024 11:19:30 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:239b8ba0cdd6231d5f9de0bc0488f7f2cd96ddce6706a5e0f34543979171bdec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77be2912e984774b4aea209d0e3ce7b966524cb14848c190fd396e807a54e087`

```dockerfile
```

-	Layers:
	-	`sha256:c4bc386e2f7efb200f6cc734d1900319ad1f505fef41f654ba2951bc76831ef6`  
		Last Modified: Tue, 12 Nov 2024 11:19:30 GMT  
		Size: 3.0 MB (2971206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f13d25fbc33a64362a8126c6b93ffc580f6a1b28d34fb571680e8a0d4a3dec18`  
		Last Modified: Tue, 12 Nov 2024 11:19:29 GMT  
		Size: 15.9 KB (15905 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:b52ddf6c80429a91e462840afcb013b449c5fa7b4b356c92a83490e61debe3c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:e0b078ddef48edabb3edd67587d73dce0886f1676d777da47062ab1eed88b0da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23611520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c5bb53ba7aca946cba46980d5ab416af7a303ae1e8c442f2ddfdd0486a3297`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a938a04d3b903456f3b0c899a1ee719f0fbe0c20572ce8f8a333cbd7204c9424`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e403debb40518414e6b358a892a18b3e5f0f7e54081cfeb9b07c2b3101c971a6`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 290.9 KB (290888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac7ca426c5927695eb459153d6e03440a125f298ee6e62fc6919e2107e3567b`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 19.7 MB (19672077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b5a34d409580ae00a43acde566afb4380ddaf799697c813b6950eb6182c8e3`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eed6f91e2c5f917da15268635d210a1b9b6578179b3c6e3ca8ddf34bfe965eb`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e9b4f4321537230681e57bb52a6ee546109b0a5ce852c867370658982bab4a`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:e401a0ae1338217c8774af1a7e7659865b503b32642d6b625261d45b377ad8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 KB (250371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3f1efc9c7e0a00983a84864956c0978fe19267c7224a63934dad2143b6116b`

```dockerfile
```

-	Layers:
	-	`sha256:b6b58d80490c4f66b398d6fe9770891de0d7a7dc51a5f8f529ef457e3b7c94f6`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 233.5 KB (233462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9fe607b78ca533bf4dab527c8ab91e259f9b0e65f7abef6ead17fae5eb09ef2`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:59ebc28e702536afac90c1c4b58839ff30a9e01322ad2e1177fbe813b481760c
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
$ docker pull chronograf@sha256:50f64bb06992802aa96de3033cf731c736f1621cded83feb97eda1dd42166e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71507977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc626241470aaf35f5fe1d297c6353899e98a2324d39e8863317365d9cd53a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38acb0bdae8b7299b96bef5f8d902e06eaa5730c3353379420ad02145e6ea8e5`  
		Last Modified: Tue, 12 Nov 2024 02:38:17 GMT  
		Size: 5.0 MB (5020322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c0badaffefb66097a9ebaef1b2a1698156c9e65188a72882f4dc3419e05eec`  
		Last Modified: Tue, 12 Nov 2024 02:38:18 GMT  
		Size: 35.0 MB (35011707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8281a0a1524081d8e4a61cac212e2a2c5134e0c2a5c0d194a4ee158128fc06da`  
		Last Modified: Tue, 12 Nov 2024 02:38:17 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac6883e6ccb3f1e5a4a1492b27006fe8cdf3e0f52a8bbfdd8a41432df91ed3b`  
		Last Modified: Tue, 12 Nov 2024 02:38:17 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6c6eb440cc51a6837c2ebf0c98b854b841dbc69474306bad8d42ff03d78946`  
		Last Modified: Tue, 12 Nov 2024 02:38:18 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:13662c24a905ca7e3f1c449c9cb46fdad1e5413ba932ec9949986a7247ca174e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0e4422cf787b178201e3619b3205102559c6d459e9a73bf0901e7770f43bf`

```dockerfile
```

-	Layers:
	-	`sha256:708ce5c455fb8bc4b30f6c09c73121f1e8bdc2192c4ab924d32cbd6cfd8a5826`  
		Last Modified: Tue, 12 Nov 2024 02:38:17 GMT  
		Size: 3.0 MB (2970958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fcacb9190786f8752ff5e11b6c18da279269f786f6d08106626b1ca38baa6e`  
		Last Modified: Tue, 12 Nov 2024 02:38:17 GMT  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:be1bc44ad7a448f8b76ed626885dd87bf8a64a4439948161d1b84dfb9da24c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64230635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de60101b590c14bee87d0954707bf670bf8ee4fedb77b9da37d4c60708a1b5ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76d0fca1db4a044faf08522a97847fc66e7e267da5542f8bc65fe610e106f08`  
		Last Modified: Tue, 12 Nov 2024 16:04:50 GMT  
		Size: 4.3 MB (4285456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925fe4b840e6b2aa003870d0a452f0c22fb0f736d62b6158e8d47cf0917a56f`  
		Last Modified: Tue, 12 Nov 2024 16:05:32 GMT  
		Size: 33.3 MB (33311523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a93dc802863f365b023bbdfa88ec35de4d4093e176cb5b89e698c26c9ab5d0b`  
		Last Modified: Tue, 12 Nov 2024 16:05:31 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddde9edf2a28beda7cc59a41fa8cbdf4d7054ff2e6d736760ea37deb61ec0e94`  
		Last Modified: Tue, 12 Nov 2024 16:05:31 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53b6ad43a1916d84c5640b4c9c8046ce758fafc39f1dac7887492f182fcb03b`  
		Last Modified: Tue, 12 Nov 2024 16:05:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:a7a1ceb05758d05082c0a423533b7248fdf7d291aab10d2745f599b7169178ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2989111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a9810a211ebfde38c90dee4d98d754313fe38f54e661363ac0fe34d4831dda`

```dockerfile
```

-	Layers:
	-	`sha256:bef13d45e3ddfd22f3337a796ae159b53a972132c5b63be4a7fe23b36d83f8e2`  
		Last Modified: Tue, 12 Nov 2024 16:05:31 GMT  
		Size: 3.0 MB (2973228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:177f0c391e14922c9b7ef31b6218c5499bcda996876d5a7e4215fd535aceae20`  
		Last Modified: Tue, 12 Nov 2024 16:05:31 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:0e02e909b958d0b13f422b018a39cb6b5a229628caa0d90464c47f696e7fede4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68301073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e06e425c41e2492545ed4f5de31b5f520bfc1db3b13b6573ff0e68d02646d5f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f1bb528f6fc096401d9e476b66580bf822afa9857615e63939165ad97eb6f5`  
		Last Modified: Tue, 12 Nov 2024 11:19:03 GMT  
		Size: 5.0 MB (5003579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30d137d96eec0c6c14194fd60544937658999c185476f77b74829d0611ab469`  
		Last Modified: Tue, 12 Nov 2024 11:19:31 GMT  
		Size: 33.2 MB (33181500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9f082ae9ddc143e967720686dcc862bef2a59bf02358bc86d87524eb1d3f17`  
		Last Modified: Tue, 12 Nov 2024 11:19:29 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498940ca92bda8e3e4610318efeb838d755812144ef66a31dfda0dc040a6a66d`  
		Last Modified: Tue, 12 Nov 2024 11:19:29 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fd7c6b66993576aa75ad6111a957adf90c7d965e9712f7e4cb5cf24563e9be`  
		Last Modified: Tue, 12 Nov 2024 11:19:30 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:239b8ba0cdd6231d5f9de0bc0488f7f2cd96ddce6706a5e0f34543979171bdec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77be2912e984774b4aea209d0e3ce7b966524cb14848c190fd396e807a54e087`

```dockerfile
```

-	Layers:
	-	`sha256:c4bc386e2f7efb200f6cc734d1900319ad1f505fef41f654ba2951bc76831ef6`  
		Last Modified: Tue, 12 Nov 2024 11:19:30 GMT  
		Size: 3.0 MB (2971206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f13d25fbc33a64362a8126c6b93ffc580f6a1b28d34fb571680e8a0d4a3dec18`  
		Last Modified: Tue, 12 Nov 2024 11:19:29 GMT  
		Size: 15.9 KB (15905 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:b52ddf6c80429a91e462840afcb013b449c5fa7b4b356c92a83490e61debe3c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:e0b078ddef48edabb3edd67587d73dce0886f1676d777da47062ab1eed88b0da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23611520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c5bb53ba7aca946cba46980d5ab416af7a303ae1e8c442f2ddfdd0486a3297`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a938a04d3b903456f3b0c899a1ee719f0fbe0c20572ce8f8a333cbd7204c9424`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e403debb40518414e6b358a892a18b3e5f0f7e54081cfeb9b07c2b3101c971a6`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 290.9 KB (290888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac7ca426c5927695eb459153d6e03440a125f298ee6e62fc6919e2107e3567b`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 19.7 MB (19672077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b5a34d409580ae00a43acde566afb4380ddaf799697c813b6950eb6182c8e3`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eed6f91e2c5f917da15268635d210a1b9b6578179b3c6e3ca8ddf34bfe965eb`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e9b4f4321537230681e57bb52a6ee546109b0a5ce852c867370658982bab4a`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:e401a0ae1338217c8774af1a7e7659865b503b32642d6b625261d45b377ad8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 KB (250371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3f1efc9c7e0a00983a84864956c0978fe19267c7224a63934dad2143b6116b`

```dockerfile
```

-	Layers:
	-	`sha256:b6b58d80490c4f66b398d6fe9770891de0d7a7dc51a5f8f529ef457e3b7c94f6`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 233.5 KB (233462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9fe607b78ca533bf4dab527c8ab91e259f9b0e65f7abef6ead17fae5eb09ef2`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:e917c05d49569ffc91363b69db1139b3aec3ea352d7e4ab116ac73b5276c1e63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:9177fbf8d1abc0941d457afc9b0e50767dab53c0fa38968d0935948927429e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31808028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09dbf6891fc635a202a911272984b230346ed88f7ed61e7c5b4e6699d84faef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d999415b039365cadf590cb0dee4382b11889c724dd0eab32e010a66c2dda7`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd85d2cc53952cb93e416bed6638ae8631ac933e78edf15edc8f453889c78a4b`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 292.6 KB (292626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c8ac47ff12105d7e2e63bdfecfe44bad8e9ed2abbb6bf69e824e6185e38c30`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 27.9 MB (27866799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e56c6035356fa99cb81386116d4e7f9647b9d607a8d8bf3c7bad00f71e5ae4`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 12.2 KB (12234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404105c04126e648e925115b31e8503e9be79bff0ac07d22b960fce01cc68627`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2d0f282dc22ee43b73a0bfff8802169fb0b6a1285ee756c538a46c2ffc4303`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:fcf8a567d3540090f865ac052c59bda542cc0aebd2c1ad4413eadd03d956c0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 KB (257758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6ab8b16a87c767b2f89aa09b99f84a49a0f574642aff41a53d43e44085627d`

```dockerfile
```

-	Layers:
	-	`sha256:608de47fe583d55de96c34e4f648a275957c4723931f32f5bf45243c183b05fb`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 239.9 KB (239903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cf620aebcdf5b9e70ca057c32bcd31da203ea2fc4f7048080488c8522073c0c`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:18200f03814c9cb448ed2604d3593447dda4056c967b2f12bcac3d1e22222d33
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
$ docker pull chronograf@sha256:cbb2398ca1e9c1e79905f76a6f508c0b84e124ed19d8bd1ef329113df6bd0554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84245436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef430dd9bd942ea971170a9ad41a7b86bf2b0bd54963f64e172414e8bbf7b6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1224e7e2d3fcfa467dc4f217326c057f4f2dd7300e13ef8f9e857ce39d3b4a1a`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 7.9 MB (7875383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156341f7966c50570025c0aa511f08d25d6323a659a42aed5dbf0d667f59476a`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 47.2 MB (47217593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc833227a91630f06fdbd4aa78c70728725f847e7108c30819c0dd7b1bcc2f1`  
		Last Modified: Tue, 12 Nov 2024 02:38:19 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942d7292f5707350b55e75b6962c10f687a2f79cd6897f52184d0d756f3640af`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59b128af6ad42b6a2e4237a81330a24126fa56928cb1282247f5a0b2e934cce`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:d283d9166d23e08f8f2ecab79a9506abca9aca59180582cf53a41af1716e8570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dff9e10e6a0907fdc037209f268bd74095409b257480933f04b1cad3729d68f`

```dockerfile
```

-	Layers:
	-	`sha256:3e81168bed413e125218f95a0a4120c7164a7f95a704ffc312fa47035416659c`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 2.7 MB (2706777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da14de2590a125267c353c750cc1c061c345a17e9a5da32b3651a9e5dc1c2ec`  
		Last Modified: Tue, 12 Nov 2024 02:38:19 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:45f678c553711d2db70d58535b9794b3ad28d4d84f59d79a55f54f272827789b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75517507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902c66527b2d96a1b1c3a0c88cbe54876f2dbd2a511a4c5fcb504a5a7838819d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6550685acd063dc6cce640c6f10c1dfac73cc458f5b8b19ec449579a08ab1401`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 6.5 MB (6497842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d9638c811aa475e3ef3dd738ebb9839a72c09623ca60283c170c2babda7f6`  
		Last Modified: Tue, 12 Nov 2024 16:06:27 GMT  
		Size: 44.3 MB (44276286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009a1e4b1ee7537b61421076ee24fd717c335f249c42420356c0539a1f6899b9`  
		Last Modified: Tue, 12 Nov 2024 16:06:25 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f869afcceefe33812d97f686e429f4d846795d1cd930495accf77f409f2506`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3c728782b2eeb8dd6001ebe7610861c011ebe762fcafbd576160449ed7bcb0`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:b310981b0390adbddba27b5ffa275d03002a50389474dc02ab36dd4e8c5b9ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2725282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621bb400573b68da87ad02e9d81f7ae8827c3ae22bd31fdb1d8e42dd93d4bd88`

```dockerfile
```

-	Layers:
	-	`sha256:a7b6c982a3a1c70e9c895470939fb5317eb615837e1c7b10cdac4960efaf1f79`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 2.7 MB (2709073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bda2b8c1e48a2737a6f3b881aea6e27ed53014051c50ff50e1613800ad657f8`  
		Last Modified: Tue, 12 Nov 2024 16:06:25 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:55b50dea2f2137ce54f443d25b2abfeae47947ee823b2f08388d6eda47d37d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81804433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22992893a7f71a7317d6d6a37c09a42bd342530c32f54b834b877cf5e2c5ab0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5311845117483a02d47c2a837750ed149b17f6ad45451557d3edf3b2361b65d1`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 7.7 MB (7652059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f1f751938fc31cf6a008145a362d6ef94697cef76dd2dcd3a8bb9c969ba5f5`  
		Last Modified: Tue, 12 Nov 2024 11:20:19 GMT  
		Size: 45.0 MB (44970549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa6316747afbf579f3ace66f98703019df3b8b3d7083660d7e299b89205fc7b`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ad95dbffe5e0b91bcdb9f70a444a19e3b49b1f65366caee2370468e451a8ff`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522a008c121d0b587cccc212b8a01b87d0893dd790681b545ce2777b6031c31f`  
		Last Modified: Tue, 12 Nov 2024 11:20:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:8005aae06ed87a042209bcd22fd86c390c027dfefd1ab385657eb9c4ff90b1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57bfeb1040a95763cafa6296c548fbc9a7c9d83b29c2a572fdd51e3e6aa28ce`

```dockerfile
```

-	Layers:
	-	`sha256:519a1a88095896e326f6589cb0448391ad985d186bae96a9b24df79476d03244`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 2.7 MB (2707049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6e694a5a62286326bdb76d6c68673eb2b6e170f2c7e26eb255c0224ddbc61be`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json
