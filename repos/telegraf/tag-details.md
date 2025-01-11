<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.31`](#telegraf131)
-	[`telegraf:1.31-alpine`](#telegraf131-alpine)
-	[`telegraf:1.31.3`](#telegraf1313)
-	[`telegraf:1.31.3-alpine`](#telegraf1313-alpine)
-	[`telegraf:1.32`](#telegraf132)
-	[`telegraf:1.32-alpine`](#telegraf132-alpine)
-	[`telegraf:1.32.3`](#telegraf1323)
-	[`telegraf:1.32.3-alpine`](#telegraf1323-alpine)
-	[`telegraf:1.33`](#telegraf133)
-	[`telegraf:1.33-alpine`](#telegraf133-alpine)
-	[`telegraf:1.33.1`](#telegraf1331)
-	[`telegraf:1.33.1-alpine`](#telegraf1331-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.31`

```console
$ docker pull telegraf@sha256:c8eaf59a982f8e2eb84e54cb79b5796d7892504fd72d28e5aeadbb0f441db9be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31` - linux; amd64

```console
$ docker pull telegraf@sha256:e1b4c27833c2938876d621ea0069e17e7ff542f39c8719049f114eb36d601690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157598652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65877181256104db196dbf2fbce4bd042775a05503958112d1f092d9844803c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 24 Dec 2024 22:15:27 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653d1814857109e9b1cc1ccde62f5dee03564dbdcc5e5a4323744c7efc7867d4`  
		Last Modified: Tue, 24 Dec 2024 23:21:45 GMT  
		Size: 18.9 MB (18947948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7013bc6bb2b583d21f8dd226e302c37be6487b23e2b9668b59f5c19eeb5123be`  
		Last Modified: Tue, 24 Dec 2024 23:21:45 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4aa26cc3a71162b582402bea52bc061f590c468760f14b168820af735b34f65`  
		Last Modified: Tue, 24 Dec 2024 23:21:46 GMT  
		Size: 66.3 MB (66285426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bd192a99a12ce5d7c0574cda4d2371ebdc880ba7733e9f6f1e44ddc0700329`  
		Last Modified: Tue, 24 Dec 2024 23:21:45 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:90f509c60fc9ef670eb7f18cda300b0e816df719511041ba70567e2955ddb0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6429050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f922e94cb926848dfb26885c71ba4f8e863405b7417f91766495902405fcb4b`

```dockerfile
```

-	Layers:
	-	`sha256:1efaeab6a7d06f5435c93afc5c07e21bb5252c268dda51ebad00c89cca1d6bb1`  
		Last Modified: Tue, 24 Dec 2024 23:21:45 GMT  
		Size: 6.4 MB (6414580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4979f533aefffdb2b92f65ffa57ff8467abe8253130d5b3f74c71297bbe5bd4d`  
		Last Modified: Tue, 24 Dec 2024 23:21:45 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:cfab64194abc56e4a43df781504ecea0dd24b54d4dcfb8c77085c6062504bebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145367038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30470f6665cb7ebbbecc83ee45d72dda5008901be15ff7020f02825f85426acc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e62e07b295392732a3ab8803f6f9f85e134cddb8627a947923c37ef5505bf`  
		Last Modified: Wed, 25 Dec 2024 14:45:59 GMT  
		Size: 17.7 MB (17725151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67efe14fd8e7b3fd44fa9953a8500f10f373138d7814b70a767fc4a549e5710c`  
		Last Modified: Wed, 25 Dec 2024 14:45:58 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e399030c1bb7d48c9f1cd87dff7fcdadd478e6ea695c85d0c17e077e4590db`  
		Last Modified: Wed, 25 Dec 2024 14:46:01 GMT  
		Size: 61.7 MB (61672296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a50bc08465ea1237bc77c0cd9dd135f94308e6f663e8627e1600ebd0e00b9e2`  
		Last Modified: Wed, 25 Dec 2024 14:45:59 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:23e3de2db369b05ab135f183eed1f838afe25bd32ea2a73d947aadd55e46f889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91594284d07e71874a61c7bb63d4259dc978e516d2acc54905991a31ef5d8ab`

```dockerfile
```

-	Layers:
	-	`sha256:c867478f32bbd1de150d2a0188c4dee9ad754b3bd5578426aa07f972e8d66249`  
		Last Modified: Wed, 25 Dec 2024 14:45:59 GMT  
		Size: 6.4 MB (6409984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:738df23a5f47d64cad27872d34512400df61f5fa88d33d7f81d6a5f15d6e1754`  
		Last Modified: Wed, 25 Dec 2024 14:45:59 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2d5563ee576dfe73e22f222d076345922a37df335a748325151ff00dd15af71b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150982220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4760e2195758a6cf61f756ee292291ce90854841ed92384c7162966ba010f3ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d3b15c5dbf0a57dd889770a634184ac5a00d1c9e6442d3466c4f5bf2ae386e`  
		Last Modified: Wed, 25 Dec 2024 10:31:02 GMT  
		Size: 18.9 MB (18870819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3234f16fbfb2639349fbdd74cc1ab1c092b1088fddfd3665b73f1bd1e9907`  
		Last Modified: Wed, 25 Dec 2024 10:31:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2037bb26edb96295a374e2228609b967ab72b11431e5c4cc1d659e2f5dd1d2b9`  
		Last Modified: Wed, 25 Dec 2024 10:31:03 GMT  
		Size: 60.4 MB (60377738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f8cd26bab6a25f164bbb4d50bca5bfbc4951b8d8ed9b974c8b2d13afe5f7e7`  
		Last Modified: Wed, 25 Dec 2024 10:31:00 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:19b597ca238143eced3ff7ea85aae5ecbf366e67ce47b74892bb0800adf6098e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6430641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6978ea0583a7ae6f3691bc5aceedb9fe21d7fb9de8831cff9e17d515e5397d6`

```dockerfile
```

-	Layers:
	-	`sha256:bae485db739c54fb3d4e97bd428eff5a4f002391564e3e1960d94959c2abf923`  
		Last Modified: Wed, 25 Dec 2024 10:31:01 GMT  
		Size: 6.4 MB (6416063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64df1019e57de44a14e4b76bd166051c09d68ced9ffe3dd0eb736672c25943e6`  
		Last Modified: Wed, 25 Dec 2024 10:31:00 GMT  
		Size: 14.6 KB (14578 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31-alpine`

```console
$ docker pull telegraf@sha256:93e313e4f1683fa7aca89bad3aae490a3aa6b2272757ff9c9c15b9a6a51ad04c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:29e9b605caa346ae8c694414383b9cc2a2319f47d3a079afd2cc7dc80de32351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72154580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3953fb828c6e8d7a6f803e4b06e92f5e4e31165f3e38492988afe6a9f4dd6e5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Dec 2024 21:08:54 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468d1aecad0155c3d90e98277566dc27a141217f25ef85e8003fbc668659f2f2`  
		Last Modified: Wed, 08 Jan 2025 18:16:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82549f356bc75f4de167979912d7bebe8523c035eff811303e64fae27160d90c`  
		Last Modified: Wed, 08 Jan 2025 18:16:57 GMT  
		Size: 2.4 MB (2448110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffcdff2fd5699d6bc0e399178b4546e662761b1e15588eea68a161ae639e15e`  
		Last Modified: Wed, 08 Jan 2025 18:16:59 GMT  
		Size: 66.1 MB (66079603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05ed68a32610ae205abe1e20c7913b63467e67b954f7b240c0ec22c46748687`  
		Last Modified: Wed, 08 Jan 2025 18:16:57 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:63c5cdb72ba5b371e2d506be2ecac56565fbf891989936fe136f166cbb4f365f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1084258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13588094b5353fadc58d8e876f8ea23ece12a435cb31505cee6df8e14dcebe03`

```dockerfile
```

-	Layers:
	-	`sha256:e7dd33351529c9250deebb495f36b0bbd92be7df1d88d02034b260e8f5a63227`  
		Last Modified: Wed, 08 Jan 2025 18:16:57 GMT  
		Size: 1.1 MB (1069297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad63a6cbf6eeceb6367a166a67594bac4084a2f9d388bad707591dd37c6e593b`  
		Last Modified: Wed, 08 Jan 2025 18:16:57 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a2f2a638dbf972dd0171a0ecff843c0379f72a90083f1437db8b5e45f411fb10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66797096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196341707d85544215d87a51f3b1035c5b0086d99d01f6d22ab9b8e09ef7bf58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Dec 2024 21:08:54 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c7dafdb703875c4326b5e1c619a600f0cc7fe2b730986902401f7db9071f7`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b563c2c2e3fad2f23ba79a8de7332d3f0bd77ab6b2a39cbe7714e4393daf2f`  
		Last Modified: Thu, 09 Jan 2025 05:57:51 GMT  
		Size: 2.5 MB (2534054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52162d0ee6e9285992524e29892600906aa38022fcaf13a0bd96a6e887c4c81`  
		Last Modified: Thu, 09 Jan 2025 05:57:52 GMT  
		Size: 60.2 MB (60171665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcbf5b9147adc8d3381d8417765071dc1052e5cc541eb7f752b9ccc6b1aad78`  
		Last Modified: Thu, 09 Jan 2025 05:57:51 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:84b01ff4a3d1be79157b475296302dc73f0f30c59f22c4b3ca94c19083d19408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1080802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0ce3d34cb441e91bebd2907329b5ddd9fb710dd9465955373d995e7c437f78`

```dockerfile
```

-	Layers:
	-	`sha256:11cc2d4ac6cee0b48b626dd789fec7a50595c4d57bbdbae0b22bda5020c590b7`  
		Last Modified: Thu, 09 Jan 2025 05:57:51 GMT  
		Size: 1.1 MB (1065731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3e5eba2bb010278ea19a66f54b9e1415e64f43d8593426f1acd8d46e4ba8d20`  
		Last Modified: Thu, 09 Jan 2025 05:57:51 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.3`

```console
$ docker pull telegraf@sha256:c8eaf59a982f8e2eb84e54cb79b5796d7892504fd72d28e5aeadbb0f441db9be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31.3` - linux; amd64

```console
$ docker pull telegraf@sha256:e1b4c27833c2938876d621ea0069e17e7ff542f39c8719049f114eb36d601690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157598652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65877181256104db196dbf2fbce4bd042775a05503958112d1f092d9844803c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 24 Dec 2024 22:15:27 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653d1814857109e9b1cc1ccde62f5dee03564dbdcc5e5a4323744c7efc7867d4`  
		Last Modified: Tue, 24 Dec 2024 23:21:45 GMT  
		Size: 18.9 MB (18947948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7013bc6bb2b583d21f8dd226e302c37be6487b23e2b9668b59f5c19eeb5123be`  
		Last Modified: Tue, 24 Dec 2024 23:21:45 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4aa26cc3a71162b582402bea52bc061f590c468760f14b168820af735b34f65`  
		Last Modified: Tue, 24 Dec 2024 23:21:46 GMT  
		Size: 66.3 MB (66285426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bd192a99a12ce5d7c0574cda4d2371ebdc880ba7733e9f6f1e44ddc0700329`  
		Last Modified: Tue, 24 Dec 2024 23:21:45 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:90f509c60fc9ef670eb7f18cda300b0e816df719511041ba70567e2955ddb0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6429050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f922e94cb926848dfb26885c71ba4f8e863405b7417f91766495902405fcb4b`

```dockerfile
```

-	Layers:
	-	`sha256:1efaeab6a7d06f5435c93afc5c07e21bb5252c268dda51ebad00c89cca1d6bb1`  
		Last Modified: Tue, 24 Dec 2024 23:21:45 GMT  
		Size: 6.4 MB (6414580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4979f533aefffdb2b92f65ffa57ff8467abe8253130d5b3f74c71297bbe5bd4d`  
		Last Modified: Tue, 24 Dec 2024 23:21:45 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:cfab64194abc56e4a43df781504ecea0dd24b54d4dcfb8c77085c6062504bebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145367038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30470f6665cb7ebbbecc83ee45d72dda5008901be15ff7020f02825f85426acc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e62e07b295392732a3ab8803f6f9f85e134cddb8627a947923c37ef5505bf`  
		Last Modified: Wed, 25 Dec 2024 14:45:59 GMT  
		Size: 17.7 MB (17725151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67efe14fd8e7b3fd44fa9953a8500f10f373138d7814b70a767fc4a549e5710c`  
		Last Modified: Wed, 25 Dec 2024 14:45:58 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e399030c1bb7d48c9f1cd87dff7fcdadd478e6ea695c85d0c17e077e4590db`  
		Last Modified: Wed, 25 Dec 2024 14:46:01 GMT  
		Size: 61.7 MB (61672296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a50bc08465ea1237bc77c0cd9dd135f94308e6f663e8627e1600ebd0e00b9e2`  
		Last Modified: Wed, 25 Dec 2024 14:45:59 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:23e3de2db369b05ab135f183eed1f838afe25bd32ea2a73d947aadd55e46f889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91594284d07e71874a61c7bb63d4259dc978e516d2acc54905991a31ef5d8ab`

```dockerfile
```

-	Layers:
	-	`sha256:c867478f32bbd1de150d2a0188c4dee9ad754b3bd5578426aa07f972e8d66249`  
		Last Modified: Wed, 25 Dec 2024 14:45:59 GMT  
		Size: 6.4 MB (6409984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:738df23a5f47d64cad27872d34512400df61f5fa88d33d7f81d6a5f15d6e1754`  
		Last Modified: Wed, 25 Dec 2024 14:45:59 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2d5563ee576dfe73e22f222d076345922a37df335a748325151ff00dd15af71b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150982220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4760e2195758a6cf61f756ee292291ce90854841ed92384c7162966ba010f3ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d3b15c5dbf0a57dd889770a634184ac5a00d1c9e6442d3466c4f5bf2ae386e`  
		Last Modified: Wed, 25 Dec 2024 10:31:02 GMT  
		Size: 18.9 MB (18870819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3234f16fbfb2639349fbdd74cc1ab1c092b1088fddfd3665b73f1bd1e9907`  
		Last Modified: Wed, 25 Dec 2024 10:31:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2037bb26edb96295a374e2228609b967ab72b11431e5c4cc1d659e2f5dd1d2b9`  
		Last Modified: Wed, 25 Dec 2024 10:31:03 GMT  
		Size: 60.4 MB (60377738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f8cd26bab6a25f164bbb4d50bca5bfbc4951b8d8ed9b974c8b2d13afe5f7e7`  
		Last Modified: Wed, 25 Dec 2024 10:31:00 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:19b597ca238143eced3ff7ea85aae5ecbf366e67ce47b74892bb0800adf6098e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6430641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6978ea0583a7ae6f3691bc5aceedb9fe21d7fb9de8831cff9e17d515e5397d6`

```dockerfile
```

-	Layers:
	-	`sha256:bae485db739c54fb3d4e97bd428eff5a4f002391564e3e1960d94959c2abf923`  
		Last Modified: Wed, 25 Dec 2024 10:31:01 GMT  
		Size: 6.4 MB (6416063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64df1019e57de44a14e4b76bd166051c09d68ced9ffe3dd0eb736672c25943e6`  
		Last Modified: Wed, 25 Dec 2024 10:31:00 GMT  
		Size: 14.6 KB (14578 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.3-alpine`

```console
$ docker pull telegraf@sha256:93e313e4f1683fa7aca89bad3aae490a3aa6b2272757ff9c9c15b9a6a51ad04c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:29e9b605caa346ae8c694414383b9cc2a2319f47d3a079afd2cc7dc80de32351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72154580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3953fb828c6e8d7a6f803e4b06e92f5e4e31165f3e38492988afe6a9f4dd6e5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Dec 2024 21:08:54 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468d1aecad0155c3d90e98277566dc27a141217f25ef85e8003fbc668659f2f2`  
		Last Modified: Wed, 08 Jan 2025 18:16:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82549f356bc75f4de167979912d7bebe8523c035eff811303e64fae27160d90c`  
		Last Modified: Wed, 08 Jan 2025 18:16:57 GMT  
		Size: 2.4 MB (2448110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffcdff2fd5699d6bc0e399178b4546e662761b1e15588eea68a161ae639e15e`  
		Last Modified: Wed, 08 Jan 2025 18:16:59 GMT  
		Size: 66.1 MB (66079603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05ed68a32610ae205abe1e20c7913b63467e67b954f7b240c0ec22c46748687`  
		Last Modified: Wed, 08 Jan 2025 18:16:57 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:63c5cdb72ba5b371e2d506be2ecac56565fbf891989936fe136f166cbb4f365f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1084258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13588094b5353fadc58d8e876f8ea23ece12a435cb31505cee6df8e14dcebe03`

```dockerfile
```

-	Layers:
	-	`sha256:e7dd33351529c9250deebb495f36b0bbd92be7df1d88d02034b260e8f5a63227`  
		Last Modified: Wed, 08 Jan 2025 18:16:57 GMT  
		Size: 1.1 MB (1069297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad63a6cbf6eeceb6367a166a67594bac4084a2f9d388bad707591dd37c6e593b`  
		Last Modified: Wed, 08 Jan 2025 18:16:57 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a2f2a638dbf972dd0171a0ecff843c0379f72a90083f1437db8b5e45f411fb10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66797096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196341707d85544215d87a51f3b1035c5b0086d99d01f6d22ab9b8e09ef7bf58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Dec 2024 21:08:54 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c7dafdb703875c4326b5e1c619a600f0cc7fe2b730986902401f7db9071f7`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b563c2c2e3fad2f23ba79a8de7332d3f0bd77ab6b2a39cbe7714e4393daf2f`  
		Last Modified: Thu, 09 Jan 2025 05:57:51 GMT  
		Size: 2.5 MB (2534054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52162d0ee6e9285992524e29892600906aa38022fcaf13a0bd96a6e887c4c81`  
		Last Modified: Thu, 09 Jan 2025 05:57:52 GMT  
		Size: 60.2 MB (60171665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcbf5b9147adc8d3381d8417765071dc1052e5cc541eb7f752b9ccc6b1aad78`  
		Last Modified: Thu, 09 Jan 2025 05:57:51 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:84b01ff4a3d1be79157b475296302dc73f0f30c59f22c4b3ca94c19083d19408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1080802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0ce3d34cb441e91bebd2907329b5ddd9fb710dd9465955373d995e7c437f78`

```dockerfile
```

-	Layers:
	-	`sha256:11cc2d4ac6cee0b48b626dd789fec7a50595c4d57bbdbae0b22bda5020c590b7`  
		Last Modified: Thu, 09 Jan 2025 05:57:51 GMT  
		Size: 1.1 MB (1065731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3e5eba2bb010278ea19a66f54b9e1415e64f43d8593426f1acd8d46e4ba8d20`  
		Last Modified: Thu, 09 Jan 2025 05:57:51 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32`

```console
$ docker pull telegraf@sha256:72ab42cc5200229fd1030f8837ff53f6f8c9831545e4030cb29d5b52e1e0de4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32` - linux; amd64

```console
$ docker pull telegraf@sha256:1c699e31c715350963e403cd6356da85ab91b1c937d3c831aa4bd6e70313253a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161334379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828289431ddc4e681b822e6c8e0ef745f212eeb904bb15746d1b398328d17962`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 24 Dec 2024 22:15:27 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf9288c04ef24a7a430826d2712c6a1761c179fc3b6dbf5acf1ad36d273a876`  
		Last Modified: Tue, 24 Dec 2024 23:21:58 GMT  
		Size: 18.9 MB (18948047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e8f8dd3c6ff997428abcc0c5ef24b4cc837a7cb71ad3213c4b183ddd7c8854`  
		Last Modified: Tue, 24 Dec 2024 23:21:57 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea77c07f598b14468c1ba2c5e54a934536fb24bb377f4591c0800440419e2716`  
		Last Modified: Tue, 24 Dec 2024 23:21:59 GMT  
		Size: 70.0 MB (70021040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a753ec2d17b79aa749029f878c004c958c8cf5d0f081dc0eb7490fcc3a1b522`  
		Last Modified: Tue, 24 Dec 2024 23:21:57 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:b1f3acef162db07de427a2b2b1ef1cd2ef963487268b436311b1018f7876d66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008abdf936f164e96b1d7c025136870fc4026862ed5bd9d209886083730235e4`

```dockerfile
```

-	Layers:
	-	`sha256:10765a469d4af148f22b987be1341b3d216826e041f0f2b588c5690595ba3e0c`  
		Last Modified: Tue, 24 Dec 2024 23:21:57 GMT  
		Size: 6.4 MB (6424038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:355c30f5c76ac417ed215cab5f9d679b3fee52b4bcfe9fddcb0d2951f67f545e`  
		Last Modified: Tue, 24 Dec 2024 23:21:57 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:df5fdd9acfcb006f199c957b5f0ae2c6ec8458446970bb45a66d9522d2d8fe7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148377605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b29a3b632b699a709ba87e71e8c83dbff987163c5afdf8e8b0a42240a4201f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e62e07b295392732a3ab8803f6f9f85e134cddb8627a947923c37ef5505bf`  
		Last Modified: Wed, 25 Dec 2024 14:45:59 GMT  
		Size: 17.7 MB (17725151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67efe14fd8e7b3fd44fa9953a8500f10f373138d7814b70a767fc4a549e5710c`  
		Last Modified: Wed, 25 Dec 2024 14:45:58 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db4bf8d7a8a2f36733cba2acdc44164532a8cccec6f0129b2c25c0309fb790d`  
		Last Modified: Wed, 25 Dec 2024 14:46:48 GMT  
		Size: 64.7 MB (64682865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdc8c04aa92897ed6278be817bd6e4c4249416482569ee8b1fffaea738ae076`  
		Last Modified: Wed, 25 Dec 2024 14:46:46 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:0a2ef12c2575e2c23d8d0d5a7f209d9733690b6ee21390863dcbb1aecf647202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6433997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39954d9cf54e2cbf060d3c96a45ddaba8568527c5825fe3648d998f82134fc08`

```dockerfile
```

-	Layers:
	-	`sha256:e8ff97327cccbfe9a3cdea32fdc70cadd4e20a727be58092407e293ae07e77b4`  
		Last Modified: Wed, 25 Dec 2024 14:46:46 GMT  
		Size: 6.4 MB (6419442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82eabf027297ba47ee74afba017166b7da5465c6a7e03a6e79ffb8060f2c88ff`  
		Last Modified: Wed, 25 Dec 2024 14:46:46 GMT  
		Size: 14.6 KB (14555 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3befe804c430be9a86b392a67f2695eec6fb81f78b1e559e098bb9d89da7f3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153756008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d604928c1d25ec51748106457692ebbfb6f3ca7986bcab16815650bfff64c981`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d3b15c5dbf0a57dd889770a634184ac5a00d1c9e6442d3466c4f5bf2ae386e`  
		Last Modified: Wed, 25 Dec 2024 10:31:02 GMT  
		Size: 18.9 MB (18870819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3234f16fbfb2639349fbdd74cc1ab1c092b1088fddfd3665b73f1bd1e9907`  
		Last Modified: Wed, 25 Dec 2024 10:31:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7927f6daa63bf08ee5eb2b48e0598f433de2dd35e152ee55722bd4a0936a03d8`  
		Last Modified: Wed, 25 Dec 2024 10:31:35 GMT  
		Size: 63.2 MB (63151528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0908b81a77fb29f19f2d7f7bcd531cc0b1d44203059d96018abf2a6389ba00`  
		Last Modified: Wed, 25 Dec 2024 10:31:33 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:5c99fd6f3b89fd6f071b47240fbc43f9d1ce7214dffacc5e9887c985c6aba9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6439294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa723a96d68e3ca0e489b1e6723b7442704afeaded6049cc81e5de476479b95`

```dockerfile
```

-	Layers:
	-	`sha256:63ef022e0e70766df723d6350a80df3919634bec852f1baefcb185efb1d6eb3a`  
		Last Modified: Wed, 25 Dec 2024 10:31:34 GMT  
		Size: 6.4 MB (6424714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26bde39422c3f620abd52ccc830647bcecf3f4fe56d00558d585076e6a72b354`  
		Last Modified: Wed, 25 Dec 2024 10:31:33 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32-alpine`

```console
$ docker pull telegraf@sha256:9b548aad77263ada594f2686b32b9de35f2b8c4a05aef09ef26e33e212d0d23f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:4d2659101482204300ca7e483cdb2e10fae827f8327176b5d0e0fe1d926332ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75899377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f84076c8c704db38f654f051504f2dae85c96f66f359e38c7de0337eac9adef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Dec 2024 21:08:54 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b890225f560541e48a5f0179cef47eed23912ee4d53196eca11fce0f695d65`  
		Last Modified: Wed, 08 Jan 2025 18:16:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1c5b2b7691b7ba253ab6932ac82877c22e9860136b5252c62649880a7864e8`  
		Last Modified: Wed, 08 Jan 2025 18:16:50 GMT  
		Size: 2.4 MB (2448063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3256316894cd81ef1d93e916036ac01554ca35d8079e17c8ffbd54bf14be84`  
		Last Modified: Wed, 08 Jan 2025 18:16:51 GMT  
		Size: 69.8 MB (69824447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2063fb4ac4811073d14df48a370dd28207788a97c61a24e09eec6d238d8f6b`  
		Last Modified: Wed, 08 Jan 2025 18:16:50 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:5d2ec22b94af0f3c69f6461632caaf2c3e6f59a839f6a55fb8ef548c503a0bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1093716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8607178d6f82b30fd68782fc0cd82482f97be156be1392157c1b5472c02b6a52`

```dockerfile
```

-	Layers:
	-	`sha256:2d0703d424793c953394f5d09d8259766068fdc907e8b2d612dcedd19d8296ea`  
		Last Modified: Wed, 08 Jan 2025 18:16:50 GMT  
		Size: 1.1 MB (1078755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c5cd16ba863559bfbaf01b9e10e431ac3712b992050ed3272da74ea08158e44`  
		Last Modified: Wed, 08 Jan 2025 18:16:50 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:1b8fad9e33d6d0928b8afb1842dac8888ca2905889ea4c100f63ab653bee0126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69569693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ab7ad56ea4dc6c682067b7865b4831ed13303cf0fb95dea4f010b8d02b3df0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Dec 2024 21:08:54 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c7dafdb703875c4326b5e1c619a600f0cc7fe2b730986902401f7db9071f7`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b563c2c2e3fad2f23ba79a8de7332d3f0bd77ab6b2a39cbe7714e4393daf2f`  
		Last Modified: Thu, 09 Jan 2025 05:57:51 GMT  
		Size: 2.5 MB (2534054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76be883812fa16c2b2933a2b42d8db4741fedab66eba8e95002375b5b5eee61f`  
		Last Modified: Thu, 09 Jan 2025 05:58:20 GMT  
		Size: 62.9 MB (62944261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b5c58f23b97b0b0fca27cba3dd58969fd67e429e26014cba326da3710862cb`  
		Last Modified: Thu, 09 Jan 2025 05:58:18 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:705d21521525581900da3ae17f2c687b61e507ac365954290403e054ef0519e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884104166e27ebead307e8a1419c8a0d4c930048342b11eb24a9650d44c42e61`

```dockerfile
```

-	Layers:
	-	`sha256:4cc452a64f0ae07c72130f895921ad75adb2a506f99af0509e1d566554a14089`  
		Last Modified: Thu, 09 Jan 2025 05:58:18 GMT  
		Size: 1.1 MB (1074382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa3ac68992776985fdccbfecafc86d547336f9b7ee0ceaeeac5929228d2307e3`  
		Last Modified: Thu, 09 Jan 2025 05:58:18 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32.3`

```console
$ docker pull telegraf@sha256:72ab42cc5200229fd1030f8837ff53f6f8c9831545e4030cb29d5b52e1e0de4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32.3` - linux; amd64

```console
$ docker pull telegraf@sha256:1c699e31c715350963e403cd6356da85ab91b1c937d3c831aa4bd6e70313253a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161334379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828289431ddc4e681b822e6c8e0ef745f212eeb904bb15746d1b398328d17962`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 24 Dec 2024 22:15:27 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf9288c04ef24a7a430826d2712c6a1761c179fc3b6dbf5acf1ad36d273a876`  
		Last Modified: Tue, 24 Dec 2024 23:21:58 GMT  
		Size: 18.9 MB (18948047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e8f8dd3c6ff997428abcc0c5ef24b4cc837a7cb71ad3213c4b183ddd7c8854`  
		Last Modified: Tue, 24 Dec 2024 23:21:57 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea77c07f598b14468c1ba2c5e54a934536fb24bb377f4591c0800440419e2716`  
		Last Modified: Tue, 24 Dec 2024 23:21:59 GMT  
		Size: 70.0 MB (70021040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a753ec2d17b79aa749029f878c004c958c8cf5d0f081dc0eb7490fcc3a1b522`  
		Last Modified: Tue, 24 Dec 2024 23:21:57 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:b1f3acef162db07de427a2b2b1ef1cd2ef963487268b436311b1018f7876d66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008abdf936f164e96b1d7c025136870fc4026862ed5bd9d209886083730235e4`

```dockerfile
```

-	Layers:
	-	`sha256:10765a469d4af148f22b987be1341b3d216826e041f0f2b588c5690595ba3e0c`  
		Last Modified: Tue, 24 Dec 2024 23:21:57 GMT  
		Size: 6.4 MB (6424038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:355c30f5c76ac417ed215cab5f9d679b3fee52b4bcfe9fddcb0d2951f67f545e`  
		Last Modified: Tue, 24 Dec 2024 23:21:57 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:df5fdd9acfcb006f199c957b5f0ae2c6ec8458446970bb45a66d9522d2d8fe7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148377605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b29a3b632b699a709ba87e71e8c83dbff987163c5afdf8e8b0a42240a4201f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e62e07b295392732a3ab8803f6f9f85e134cddb8627a947923c37ef5505bf`  
		Last Modified: Wed, 25 Dec 2024 14:45:59 GMT  
		Size: 17.7 MB (17725151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67efe14fd8e7b3fd44fa9953a8500f10f373138d7814b70a767fc4a549e5710c`  
		Last Modified: Wed, 25 Dec 2024 14:45:58 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db4bf8d7a8a2f36733cba2acdc44164532a8cccec6f0129b2c25c0309fb790d`  
		Last Modified: Wed, 25 Dec 2024 14:46:48 GMT  
		Size: 64.7 MB (64682865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdc8c04aa92897ed6278be817bd6e4c4249416482569ee8b1fffaea738ae076`  
		Last Modified: Wed, 25 Dec 2024 14:46:46 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:0a2ef12c2575e2c23d8d0d5a7f209d9733690b6ee21390863dcbb1aecf647202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6433997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39954d9cf54e2cbf060d3c96a45ddaba8568527c5825fe3648d998f82134fc08`

```dockerfile
```

-	Layers:
	-	`sha256:e8ff97327cccbfe9a3cdea32fdc70cadd4e20a727be58092407e293ae07e77b4`  
		Last Modified: Wed, 25 Dec 2024 14:46:46 GMT  
		Size: 6.4 MB (6419442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82eabf027297ba47ee74afba017166b7da5465c6a7e03a6e79ffb8060f2c88ff`  
		Last Modified: Wed, 25 Dec 2024 14:46:46 GMT  
		Size: 14.6 KB (14555 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3befe804c430be9a86b392a67f2695eec6fb81f78b1e559e098bb9d89da7f3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153756008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d604928c1d25ec51748106457692ebbfb6f3ca7986bcab16815650bfff64c981`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d3b15c5dbf0a57dd889770a634184ac5a00d1c9e6442d3466c4f5bf2ae386e`  
		Last Modified: Wed, 25 Dec 2024 10:31:02 GMT  
		Size: 18.9 MB (18870819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3234f16fbfb2639349fbdd74cc1ab1c092b1088fddfd3665b73f1bd1e9907`  
		Last Modified: Wed, 25 Dec 2024 10:31:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7927f6daa63bf08ee5eb2b48e0598f433de2dd35e152ee55722bd4a0936a03d8`  
		Last Modified: Wed, 25 Dec 2024 10:31:35 GMT  
		Size: 63.2 MB (63151528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0908b81a77fb29f19f2d7f7bcd531cc0b1d44203059d96018abf2a6389ba00`  
		Last Modified: Wed, 25 Dec 2024 10:31:33 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:5c99fd6f3b89fd6f071b47240fbc43f9d1ce7214dffacc5e9887c985c6aba9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6439294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa723a96d68e3ca0e489b1e6723b7442704afeaded6049cc81e5de476479b95`

```dockerfile
```

-	Layers:
	-	`sha256:63ef022e0e70766df723d6350a80df3919634bec852f1baefcb185efb1d6eb3a`  
		Last Modified: Wed, 25 Dec 2024 10:31:34 GMT  
		Size: 6.4 MB (6424714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26bde39422c3f620abd52ccc830647bcecf3f4fe56d00558d585076e6a72b354`  
		Last Modified: Wed, 25 Dec 2024 10:31:33 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32.3-alpine`

```console
$ docker pull telegraf@sha256:9b548aad77263ada594f2686b32b9de35f2b8c4a05aef09ef26e33e212d0d23f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:4d2659101482204300ca7e483cdb2e10fae827f8327176b5d0e0fe1d926332ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75899377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f84076c8c704db38f654f051504f2dae85c96f66f359e38c7de0337eac9adef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Dec 2024 21:08:54 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b890225f560541e48a5f0179cef47eed23912ee4d53196eca11fce0f695d65`  
		Last Modified: Wed, 08 Jan 2025 18:16:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1c5b2b7691b7ba253ab6932ac82877c22e9860136b5252c62649880a7864e8`  
		Last Modified: Wed, 08 Jan 2025 18:16:50 GMT  
		Size: 2.4 MB (2448063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3256316894cd81ef1d93e916036ac01554ca35d8079e17c8ffbd54bf14be84`  
		Last Modified: Wed, 08 Jan 2025 18:16:51 GMT  
		Size: 69.8 MB (69824447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2063fb4ac4811073d14df48a370dd28207788a97c61a24e09eec6d238d8f6b`  
		Last Modified: Wed, 08 Jan 2025 18:16:50 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:5d2ec22b94af0f3c69f6461632caaf2c3e6f59a839f6a55fb8ef548c503a0bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1093716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8607178d6f82b30fd68782fc0cd82482f97be156be1392157c1b5472c02b6a52`

```dockerfile
```

-	Layers:
	-	`sha256:2d0703d424793c953394f5d09d8259766068fdc907e8b2d612dcedd19d8296ea`  
		Last Modified: Wed, 08 Jan 2025 18:16:50 GMT  
		Size: 1.1 MB (1078755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c5cd16ba863559bfbaf01b9e10e431ac3712b992050ed3272da74ea08158e44`  
		Last Modified: Wed, 08 Jan 2025 18:16:50 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:1b8fad9e33d6d0928b8afb1842dac8888ca2905889ea4c100f63ab653bee0126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69569693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ab7ad56ea4dc6c682067b7865b4831ed13303cf0fb95dea4f010b8d02b3df0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Dec 2024 21:08:54 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c7dafdb703875c4326b5e1c619a600f0cc7fe2b730986902401f7db9071f7`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b563c2c2e3fad2f23ba79a8de7332d3f0bd77ab6b2a39cbe7714e4393daf2f`  
		Last Modified: Thu, 09 Jan 2025 05:57:51 GMT  
		Size: 2.5 MB (2534054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76be883812fa16c2b2933a2b42d8db4741fedab66eba8e95002375b5b5eee61f`  
		Last Modified: Thu, 09 Jan 2025 05:58:20 GMT  
		Size: 62.9 MB (62944261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b5c58f23b97b0b0fca27cba3dd58969fd67e429e26014cba326da3710862cb`  
		Last Modified: Thu, 09 Jan 2025 05:58:18 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:705d21521525581900da3ae17f2c687b61e507ac365954290403e054ef0519e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884104166e27ebead307e8a1419c8a0d4c930048342b11eb24a9650d44c42e61`

```dockerfile
```

-	Layers:
	-	`sha256:4cc452a64f0ae07c72130f895921ad75adb2a506f99af0509e1d566554a14089`  
		Last Modified: Thu, 09 Jan 2025 05:58:18 GMT  
		Size: 1.1 MB (1074382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa3ac68992776985fdccbfecafc86d547336f9b7ee0ceaeeac5929228d2307e3`  
		Last Modified: Thu, 09 Jan 2025 05:58:18 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33`

```console
$ docker pull telegraf@sha256:747cdcd15fce7acf93692d9394c31b0e2c812a9f2a770f8003428f4e6e81f5de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33` - linux; amd64

```console
$ docker pull telegraf@sha256:9914ddd25d014cfef42b29945643e111fe3359f28f647fc1711006d4728b71e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164337675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666974c79fea63bdc95ee71d3f0483a8511bf35cf445db664a708b90f4f91e5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.33.0
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 24 Dec 2024 22:15:27 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea042f7af0af45684f2e467cf4fea905b33fe8e68a6e9a84e891b6f1cd7e2a`  
		Last Modified: Tue, 24 Dec 2024 23:21:55 GMT  
		Size: 18.9 MB (18948122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a427735e269b8580bb01a6e38c28818f6d413680eb67a6b53428b16fd3a4214`  
		Last Modified: Tue, 24 Dec 2024 23:21:55 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9ef2be3db327b2e0f248bf12aceeee49ca9bb66920dc92fdc55a3271f1237b`  
		Last Modified: Tue, 24 Dec 2024 23:21:56 GMT  
		Size: 73.0 MB (73024260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57122ef5ca9aae1841b94746d3812a9bb324aaf6881d9325c380226116decea9`  
		Last Modified: Tue, 24 Dec 2024 23:21:55 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:fbb59d4694532e273ff8131b9be52fdeb9d0e9424586ee820560e7b54db991c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6449281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563413b89b3d2b9d8cc291785563055af2fbbe9a18b66fce72417fd65b6d1609`

```dockerfile
```

-	Layers:
	-	`sha256:b468749829f434f99736649248b915c3549244b4ada16935516312d384e119c7`  
		Last Modified: Tue, 24 Dec 2024 23:21:55 GMT  
		Size: 6.4 MB (6434510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf3b44288d65b3aaa02eb85b924a4dd8fe35501e0fedb30953f9cf9a083146e1`  
		Last Modified: Tue, 24 Dec 2024 23:21:55 GMT  
		Size: 14.8 KB (14771 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:54f6540d6b761ebfd6b1bdc7f54ad3ad661fa9956d71107759ae28048b1ae542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151149573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8468b0a22a43c945e99ffae03cd269af33f60005a68a7226dbae76b8df54e52a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.33.0
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e62e07b295392732a3ab8803f6f9f85e134cddb8627a947923c37ef5505bf`  
		Last Modified: Wed, 25 Dec 2024 14:45:59 GMT  
		Size: 17.7 MB (17725151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67efe14fd8e7b3fd44fa9953a8500f10f373138d7814b70a767fc4a549e5710c`  
		Last Modified: Wed, 25 Dec 2024 14:45:58 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751472ed4a2c5b1f6ebe55129295353248c908fb6c202328ff755c6139721f5c`  
		Last Modified: Wed, 25 Dec 2024 14:47:36 GMT  
		Size: 67.5 MB (67454831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffb69c71c1cf50e7e4f24d008213a7b3d2280404af9b99ad6dc16094471e207`  
		Last Modified: Wed, 25 Dec 2024 14:47:34 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:f8ff144a4b5f7c47e3e4b5e07cfe66d11933e420a648b0bf3c27668aa9eb3b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6444788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d873727328901f6f5b2dd5598fd0c6b7c45824620ebba8eeb7c36f4868c61456`

```dockerfile
```

-	Layers:
	-	`sha256:23077ff3fc4a8943349d9ce971610083f0da557e0e9de176535df07a79b81711`  
		Last Modified: Wed, 25 Dec 2024 14:47:35 GMT  
		Size: 6.4 MB (6429922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9df9d718116b30474c44ca5feaaf40c75698b56ecdd9c0450ee17f5e05581876`  
		Last Modified: Wed, 25 Dec 2024 14:47:34 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4fe318b15308bb9b06809a8b64d9bf2cf3a37fd75ea809ed4deb1a1bfbb06a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156540489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99892fec240dd9d3cc50d0b3353c25650a22cf18bff4e40f5cf436c526b06d7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.33.0
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d3b15c5dbf0a57dd889770a634184ac5a00d1c9e6442d3466c4f5bf2ae386e`  
		Last Modified: Wed, 25 Dec 2024 10:31:02 GMT  
		Size: 18.9 MB (18870819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3234f16fbfb2639349fbdd74cc1ab1c092b1088fddfd3665b73f1bd1e9907`  
		Last Modified: Wed, 25 Dec 2024 10:31:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ad396c371f5045a691bb4ca0fc7ff833bc83cf1b3f3988c9eec6d26920b2f6`  
		Last Modified: Wed, 25 Dec 2024 10:32:07 GMT  
		Size: 65.9 MB (65936010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6b4ef88184633c184d048ee22af2f8d6a9ef022bae0cb88252fba140933dff`  
		Last Modified: Wed, 25 Dec 2024 10:32:05 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:0608eb7d8f742cf1ed007d367045a3ff2e8e0ba9151cd5f0d8b6c6ccb0a4cf96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6450092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b355ac88b5f308193f97c5f4e1194a44e5bbaece3ea6982a5cd57388bc93fd4`

```dockerfile
```

-	Layers:
	-	`sha256:6afa6886767bc4751c0c497e395c22b26799bf23ebe64d4822a3ab42e217f90c`  
		Last Modified: Wed, 25 Dec 2024 10:32:05 GMT  
		Size: 6.4 MB (6435198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:499f40d6cd20f0c782c5d0afcb503cf45cc0c00d4d8266e044b49b5b9ee38cd7`  
		Last Modified: Wed, 25 Dec 2024 10:32:05 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33-alpine`

```console
$ docker pull telegraf@sha256:5bc167fe0428bbeae504ebdb155228e4e986b45cf8314940079297c24639521e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:6b55ae43e78fa52721721d4cacc4278cf1493e63ee00088c4ee55d73c154da79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78901278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f14e0815236cb3b9882bcc7282d66050b5639852e0ef3d05575ef1e07fc9ea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Dec 2024 21:08:54 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.33.0
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ea7f6f2a1796ddac83d592e16f4eb5611bbeac0d9115f9bd4a6453682bf724`  
		Last Modified: Wed, 08 Jan 2025 18:16:53 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5631a08a093df13a9447f6ef014aa76a5db6ebfb4c50aff97e194f1224722bc`  
		Last Modified: Wed, 08 Jan 2025 18:16:53 GMT  
		Size: 2.4 MB (2448041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070502ebc74c8daf64e907663c9f38c8482a311f9bc45cfdcf63785d2e0c318e`  
		Last Modified: Wed, 08 Jan 2025 18:16:54 GMT  
		Size: 72.8 MB (72826369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dccf6145737d25fb5d97be45b4cd34c6d33af030a504d0d11843ef0802e8194`  
		Last Modified: Wed, 08 Jan 2025 18:16:53 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:f4d7085f2117321d61b8cb839e3b5c8992778a264e1f6ef2a29351a6547ee333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1104490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24343a090dafe8ad0b568c07e17cba3712632b57d62c19ec481b0996c299653a`

```dockerfile
```

-	Layers:
	-	`sha256:563cb094caccc39f217f18eda2f2b6151fd9748fff0806df1f1e6e79cc869b99`  
		Last Modified: Wed, 08 Jan 2025 18:16:53 GMT  
		Size: 1.1 MB (1089227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28874a39f7583f7276a588708a66236c36abbc733228024c79a2f03defa7e9c1`  
		Last Modified: Wed, 08 Jan 2025 18:16:53 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:93759d09b6aa1cc96cf9186b6497ab2fa066f95299494bf35f6a5469a9598d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72361745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa90c4fa33497fff698ca808a9361e9dfc16a86738de9d5ed7c4ec1bf09e7268`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Dec 2024 21:08:54 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.33.0
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c7dafdb703875c4326b5e1c619a600f0cc7fe2b730986902401f7db9071f7`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b563c2c2e3fad2f23ba79a8de7332d3f0bd77ab6b2a39cbe7714e4393daf2f`  
		Last Modified: Thu, 09 Jan 2025 05:57:51 GMT  
		Size: 2.5 MB (2534054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f811a4403bdaa00e9c7fcb3f145261a55121621f80a120e66993b86023f34233`  
		Last Modified: Thu, 09 Jan 2025 05:58:47 GMT  
		Size: 65.7 MB (65736313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2ab404301aa25896aadf246daac92e9882acbccb23570d0a25271c5a4c228e`  
		Last Modified: Thu, 09 Jan 2025 05:58:45 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:82f7ee4a06ea418ec6b2bf025032ccb20c9d57431c71fee9167b337e21ac2fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1100251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50bcd6c524e3a8594e4b45587c60104ff1894e0d4844399bb4b8b0bf10ed369c`

```dockerfile
```

-	Layers:
	-	`sha256:584ce19804b176b17eece225809e8d5bb82a7decaac8777ddc4df496d71b0085`  
		Last Modified: Thu, 09 Jan 2025 05:58:46 GMT  
		Size: 1.1 MB (1084866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2baa213db2a6e9378b75753f4c1efe8b62157f40b299c36fa7da1d4b5a6bdd1`  
		Last Modified: Thu, 09 Jan 2025 05:58:45 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33.1`

```console
$ docker pull telegraf@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `telegraf:1.33.1-alpine`

```console
$ docker pull telegraf@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:5bc167fe0428bbeae504ebdb155228e4e986b45cf8314940079297c24639521e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:6b55ae43e78fa52721721d4cacc4278cf1493e63ee00088c4ee55d73c154da79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78901278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f14e0815236cb3b9882bcc7282d66050b5639852e0ef3d05575ef1e07fc9ea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Dec 2024 21:08:54 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.33.0
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ea7f6f2a1796ddac83d592e16f4eb5611bbeac0d9115f9bd4a6453682bf724`  
		Last Modified: Wed, 08 Jan 2025 18:16:53 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5631a08a093df13a9447f6ef014aa76a5db6ebfb4c50aff97e194f1224722bc`  
		Last Modified: Wed, 08 Jan 2025 18:16:53 GMT  
		Size: 2.4 MB (2448041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070502ebc74c8daf64e907663c9f38c8482a311f9bc45cfdcf63785d2e0c318e`  
		Last Modified: Wed, 08 Jan 2025 18:16:54 GMT  
		Size: 72.8 MB (72826369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dccf6145737d25fb5d97be45b4cd34c6d33af030a504d0d11843ef0802e8194`  
		Last Modified: Wed, 08 Jan 2025 18:16:53 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:f4d7085f2117321d61b8cb839e3b5c8992778a264e1f6ef2a29351a6547ee333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1104490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24343a090dafe8ad0b568c07e17cba3712632b57d62c19ec481b0996c299653a`

```dockerfile
```

-	Layers:
	-	`sha256:563cb094caccc39f217f18eda2f2b6151fd9748fff0806df1f1e6e79cc869b99`  
		Last Modified: Wed, 08 Jan 2025 18:16:53 GMT  
		Size: 1.1 MB (1089227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28874a39f7583f7276a588708a66236c36abbc733228024c79a2f03defa7e9c1`  
		Last Modified: Wed, 08 Jan 2025 18:16:53 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:93759d09b6aa1cc96cf9186b6497ab2fa066f95299494bf35f6a5469a9598d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72361745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa90c4fa33497fff698ca808a9361e9dfc16a86738de9d5ed7c4ec1bf09e7268`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Dec 2024 21:08:54 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.33.0
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c7dafdb703875c4326b5e1c619a600f0cc7fe2b730986902401f7db9071f7`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b563c2c2e3fad2f23ba79a8de7332d3f0bd77ab6b2a39cbe7714e4393daf2f`  
		Last Modified: Thu, 09 Jan 2025 05:57:51 GMT  
		Size: 2.5 MB (2534054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f811a4403bdaa00e9c7fcb3f145261a55121621f80a120e66993b86023f34233`  
		Last Modified: Thu, 09 Jan 2025 05:58:47 GMT  
		Size: 65.7 MB (65736313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2ab404301aa25896aadf246daac92e9882acbccb23570d0a25271c5a4c228e`  
		Last Modified: Thu, 09 Jan 2025 05:58:45 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:82f7ee4a06ea418ec6b2bf025032ccb20c9d57431c71fee9167b337e21ac2fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1100251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50bcd6c524e3a8594e4b45587c60104ff1894e0d4844399bb4b8b0bf10ed369c`

```dockerfile
```

-	Layers:
	-	`sha256:584ce19804b176b17eece225809e8d5bb82a7decaac8777ddc4df496d71b0085`  
		Last Modified: Thu, 09 Jan 2025 05:58:46 GMT  
		Size: 1.1 MB (1084866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2baa213db2a6e9378b75753f4c1efe8b62157f40b299c36fa7da1d4b5a6bdd1`  
		Last Modified: Thu, 09 Jan 2025 05:58:45 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:747cdcd15fce7acf93692d9394c31b0e2c812a9f2a770f8003428f4e6e81f5de
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
$ docker pull telegraf@sha256:9914ddd25d014cfef42b29945643e111fe3359f28f647fc1711006d4728b71e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164337675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666974c79fea63bdc95ee71d3f0483a8511bf35cf445db664a708b90f4f91e5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.33.0
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 24 Dec 2024 22:15:27 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea042f7af0af45684f2e467cf4fea905b33fe8e68a6e9a84e891b6f1cd7e2a`  
		Last Modified: Tue, 24 Dec 2024 23:21:55 GMT  
		Size: 18.9 MB (18948122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a427735e269b8580bb01a6e38c28818f6d413680eb67a6b53428b16fd3a4214`  
		Last Modified: Tue, 24 Dec 2024 23:21:55 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9ef2be3db327b2e0f248bf12aceeee49ca9bb66920dc92fdc55a3271f1237b`  
		Last Modified: Tue, 24 Dec 2024 23:21:56 GMT  
		Size: 73.0 MB (73024260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57122ef5ca9aae1841b94746d3812a9bb324aaf6881d9325c380226116decea9`  
		Last Modified: Tue, 24 Dec 2024 23:21:55 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:fbb59d4694532e273ff8131b9be52fdeb9d0e9424586ee820560e7b54db991c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6449281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563413b89b3d2b9d8cc291785563055af2fbbe9a18b66fce72417fd65b6d1609`

```dockerfile
```

-	Layers:
	-	`sha256:b468749829f434f99736649248b915c3549244b4ada16935516312d384e119c7`  
		Last Modified: Tue, 24 Dec 2024 23:21:55 GMT  
		Size: 6.4 MB (6434510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf3b44288d65b3aaa02eb85b924a4dd8fe35501e0fedb30953f9cf9a083146e1`  
		Last Modified: Tue, 24 Dec 2024 23:21:55 GMT  
		Size: 14.8 KB (14771 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:54f6540d6b761ebfd6b1bdc7f54ad3ad661fa9956d71107759ae28048b1ae542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151149573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8468b0a22a43c945e99ffae03cd269af33f60005a68a7226dbae76b8df54e52a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.33.0
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e62e07b295392732a3ab8803f6f9f85e134cddb8627a947923c37ef5505bf`  
		Last Modified: Wed, 25 Dec 2024 14:45:59 GMT  
		Size: 17.7 MB (17725151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67efe14fd8e7b3fd44fa9953a8500f10f373138d7814b70a767fc4a549e5710c`  
		Last Modified: Wed, 25 Dec 2024 14:45:58 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751472ed4a2c5b1f6ebe55129295353248c908fb6c202328ff755c6139721f5c`  
		Last Modified: Wed, 25 Dec 2024 14:47:36 GMT  
		Size: 67.5 MB (67454831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffb69c71c1cf50e7e4f24d008213a7b3d2280404af9b99ad6dc16094471e207`  
		Last Modified: Wed, 25 Dec 2024 14:47:34 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:f8ff144a4b5f7c47e3e4b5e07cfe66d11933e420a648b0bf3c27668aa9eb3b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6444788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d873727328901f6f5b2dd5598fd0c6b7c45824620ebba8eeb7c36f4868c61456`

```dockerfile
```

-	Layers:
	-	`sha256:23077ff3fc4a8943349d9ce971610083f0da557e0e9de176535df07a79b81711`  
		Last Modified: Wed, 25 Dec 2024 14:47:35 GMT  
		Size: 6.4 MB (6429922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9df9d718116b30474c44ca5feaaf40c75698b56ecdd9c0450ee17f5e05581876`  
		Last Modified: Wed, 25 Dec 2024 14:47:34 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4fe318b15308bb9b06809a8b64d9bf2cf3a37fd75ea809ed4deb1a1bfbb06a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156540489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99892fec240dd9d3cc50d0b3353c25650a22cf18bff4e40f5cf436c526b06d7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.33.0
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d3b15c5dbf0a57dd889770a634184ac5a00d1c9e6442d3466c4f5bf2ae386e`  
		Last Modified: Wed, 25 Dec 2024 10:31:02 GMT  
		Size: 18.9 MB (18870819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3234f16fbfb2639349fbdd74cc1ab1c092b1088fddfd3665b73f1bd1e9907`  
		Last Modified: Wed, 25 Dec 2024 10:31:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ad396c371f5045a691bb4ca0fc7ff833bc83cf1b3f3988c9eec6d26920b2f6`  
		Last Modified: Wed, 25 Dec 2024 10:32:07 GMT  
		Size: 65.9 MB (65936010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6b4ef88184633c184d048ee22af2f8d6a9ef022bae0cb88252fba140933dff`  
		Last Modified: Wed, 25 Dec 2024 10:32:05 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:0608eb7d8f742cf1ed007d367045a3ff2e8e0ba9151cd5f0d8b6c6ccb0a4cf96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6450092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b355ac88b5f308193f97c5f4e1194a44e5bbaece3ea6982a5cd57388bc93fd4`

```dockerfile
```

-	Layers:
	-	`sha256:6afa6886767bc4751c0c497e395c22b26799bf23ebe64d4822a3ab42e217f90c`  
		Last Modified: Wed, 25 Dec 2024 10:32:05 GMT  
		Size: 6.4 MB (6435198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:499f40d6cd20f0c782c5d0afcb503cf45cc0c00d4d8266e044b49b5b9ee38cd7`  
		Last Modified: Wed, 25 Dec 2024 10:32:05 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
