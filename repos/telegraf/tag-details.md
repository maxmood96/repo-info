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
-	[`telegraf:1.33.0`](#telegraf1330)
-	[`telegraf:1.33.0-alpine`](#telegraf1330-alpine)
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
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e62e07b295392732a3ab8803f6f9f85e134cddb8627a947923c37ef5505bf`  
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
$ docker pull telegraf@sha256:de67a108f127bbfd06b21b18fe8bba745b71b0e1e4f743a5e06ca45a705f42a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:997da12fb34bf904334e39d911327f45ef79d2a498bc71c547e8d5d70e1e0f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72149519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d731e4354684f4ef6b4d3e92a4e45008a4deb236170c5f0a349ee3416002dde`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f10048322eb86f2be1b7699a5c82453c4c117017d59212b59520756810207c`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf3378dfe0cc506adaa827bc20236dda2e82ec4b94cb866c503da70171e15c9`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 2.4 MB (2444831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d9dde8a359ac2194bdd2c1b777d7406616290d0020cc51a94a759f0ff42479`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 66.1 MB (66080176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86878befd798f41f972e38cf31f2ad1250c4660288a9574685a05d438f0c41ec`  
		Last Modified: Tue, 12 Nov 2024 02:21:17 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:0f5d76963c8dedbac66a6c0c7490a05a1a2e628a1a60395bab2df9c350343fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1079572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0749f1205673d1a6b749b89096eae616216f940a6b4a468d12e7e2d5c950bdd9`

```dockerfile
```

-	Layers:
	-	`sha256:f6021eb66e288afca40a3de988cb4b331eab3569a6cf828c4b2c64257f06557f`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 1.1 MB (1064613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc8d6cf96bf0c4c71fd14e16c3f7a3b4c0a73536343040b53c476c22e16d1203`  
		Size: 15.0 KB (14959 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c721817221b9cc330049e20dc9cf632918644881181202c11ab1ef5669e0f054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66790689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ecbb2893d24b9033fa9dbf9bf0c0fc5ead7044e742fc8801c1163854e6bc85`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de63ce930d0f77f6402e61ee732ad4f784c59fd26df033bb1b7d6a0b87a2f4`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848dadffeaafa841326acf8c33573919df8ff222e2680607f7d10bb804a23d6c`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 2.5 MB (2530663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c165eccfb6fb22936f132b38db1bea94249c4f9025902071816f681d45278592`  
		Last Modified: Wed, 13 Nov 2024 00:44:58 GMT  
		Size: 60.2 MB (60171693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f25aa3692cb281849fa0eba2cb21828fd6ad1c13fa61aaec973cde6d98d95d`  
		Last Modified: Wed, 13 Nov 2024 00:44:56 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:3c1199bc5e2229bba0fa164cb749ad110ae8ccfaebe006a2f0b23f770c5e1823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1076145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89563d9bd0aa15d8dc6e06421e37cb9040f7ff3e1cee8e2ed0852ff7977231ce`

```dockerfile
```

-	Layers:
	-	`sha256:e91298accb6ca3e23bd891af5501a0f171f772039e4cfdcea12b9c71bbac032a`  
		Last Modified: Wed, 13 Nov 2024 00:44:56 GMT  
		Size: 1.1 MB (1061075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f3921a2b1ca085f8a80fe529e5b99ce2fe7915122f7539650b0150864970c`  
		Size: 15.1 KB (15070 bytes)  
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
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e62e07b295392732a3ab8803f6f9f85e134cddb8627a947923c37ef5505bf`  
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
$ docker pull telegraf@sha256:de67a108f127bbfd06b21b18fe8bba745b71b0e1e4f743a5e06ca45a705f42a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:997da12fb34bf904334e39d911327f45ef79d2a498bc71c547e8d5d70e1e0f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72149519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d731e4354684f4ef6b4d3e92a4e45008a4deb236170c5f0a349ee3416002dde`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f10048322eb86f2be1b7699a5c82453c4c117017d59212b59520756810207c`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf3378dfe0cc506adaa827bc20236dda2e82ec4b94cb866c503da70171e15c9`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 2.4 MB (2444831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d9dde8a359ac2194bdd2c1b777d7406616290d0020cc51a94a759f0ff42479`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 66.1 MB (66080176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86878befd798f41f972e38cf31f2ad1250c4660288a9574685a05d438f0c41ec`  
		Last Modified: Tue, 12 Nov 2024 02:21:17 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:0f5d76963c8dedbac66a6c0c7490a05a1a2e628a1a60395bab2df9c350343fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1079572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0749f1205673d1a6b749b89096eae616216f940a6b4a468d12e7e2d5c950bdd9`

```dockerfile
```

-	Layers:
	-	`sha256:f6021eb66e288afca40a3de988cb4b331eab3569a6cf828c4b2c64257f06557f`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 1.1 MB (1064613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc8d6cf96bf0c4c71fd14e16c3f7a3b4c0a73536343040b53c476c22e16d1203`  
		Size: 15.0 KB (14959 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c721817221b9cc330049e20dc9cf632918644881181202c11ab1ef5669e0f054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66790689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ecbb2893d24b9033fa9dbf9bf0c0fc5ead7044e742fc8801c1163854e6bc85`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de63ce930d0f77f6402e61ee732ad4f784c59fd26df033bb1b7d6a0b87a2f4`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848dadffeaafa841326acf8c33573919df8ff222e2680607f7d10bb804a23d6c`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 2.5 MB (2530663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c165eccfb6fb22936f132b38db1bea94249c4f9025902071816f681d45278592`  
		Last Modified: Wed, 13 Nov 2024 00:44:58 GMT  
		Size: 60.2 MB (60171693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f25aa3692cb281849fa0eba2cb21828fd6ad1c13fa61aaec973cde6d98d95d`  
		Last Modified: Wed, 13 Nov 2024 00:44:56 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:3c1199bc5e2229bba0fa164cb749ad110ae8ccfaebe006a2f0b23f770c5e1823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1076145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89563d9bd0aa15d8dc6e06421e37cb9040f7ff3e1cee8e2ed0852ff7977231ce`

```dockerfile
```

-	Layers:
	-	`sha256:e91298accb6ca3e23bd891af5501a0f171f772039e4cfdcea12b9c71bbac032a`  
		Last Modified: Wed, 13 Nov 2024 00:44:56 GMT  
		Size: 1.1 MB (1061075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f3921a2b1ca085f8a80fe529e5b99ce2fe7915122f7539650b0150864970c`  
		Size: 15.1 KB (15070 bytes)  
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
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e62e07b295392732a3ab8803f6f9f85e134cddb8627a947923c37ef5505bf`  
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
$ docker pull telegraf@sha256:4046c04762db9e28ad0fc5beebffaa0edf345ea2c7b8aa3ad5ba8db02f6f4c2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:60e401f12742cafbfa564bb7f31d6e5c35daba0b50e0b5264c0cddac21e0efcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75893896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445d094c3c199fa803bcab90c7ffcc6166fa97f07846d2d88d6b0e3bd5ad333c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 18 Nov 2024 20:48:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caee9ab776a1c2beeb238e0643dbf6f3b7c0a83fd9aa339dc798e2b5272a39f5`  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac69faebcdcde53563af6c2f2356011b54221d2d336fa20004d6e41cf7f676c`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 2.4 MB (2444821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d3519fedc4d5ee37ea7859c2cedc0f290e072022c6947c318979fd6eb71f55`  
		Size: 69.8 MB (69824563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6fc6e4c616b483bafdc6d886f7d5a5c2d59fcbff06d37f5eec6352e6f45818`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:281e39380036537235243436889bf410fd2908fd811d92157772d744f55dba4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c515de8cd05e47bd266f48c2b5b5034383aebbc3b2dfc9e9eb1ba756e4d1da`

```dockerfile
```

-	Layers:
	-	`sha256:b6d2654f5db4cef75f0d0dfbaf9b3095359625a64b11278eaa23d00004cd15d9`  
		Last Modified: Mon, 18 Nov 2024 23:04:07 GMT  
		Size: 1.1 MB (1074253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34df0a4ca1bb919a775b446cf53aed82c5c950fb10f80c1950f2a1e0e6e2abdb`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8c583f2ca801c3c4e1d85d418904406884f11a8faf69abff30fcb998be6ae7d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69563728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a3b7bca19af75445ee828d6ae44a4aca6001ccfbc285e03a0bb04d3c59c691`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 18 Nov 2024 20:48:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2136f9e7feb99945e2787587daa3284c73e45adf2e22f99ad169fe2df7417c`  
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261692eb4698b8fef35728a5f463bc73da3690cc00050ff8eae9c2e6b6f2056c`  
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 2.5 MB (2530622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c097c44c7b51c633d2ea3c42c293141f0aebe80769accd240ba2787ecffc3221`  
		Last Modified: Mon, 18 Nov 2024 23:53:12 GMT  
		Size: 62.9 MB (62944775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cacd0e5e7d2ccf9cf75159eb73e57bd71b2d79b7099539c28a3e36b072c5b7d`  
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c85b59700690d98745cb96f176ac655994b903886cfa983cccbd3eff660a8254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1085315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680778e461d1fab783a7e89f344f6d64cda902be5c72231d3124ae143f05dc76`

```dockerfile
```

-	Layers:
	-	`sha256:61652ab748fb8c98a72a67271f2195ea9bfe2fbdcb40aefb9c49c77d57f46c33`  
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 1.1 MB (1069930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ec49b11d7c57d08dc2c42d71b46d3a5df4d2f3c151e691be742b9ffbc606c06`  
		Size: 15.4 KB (15385 bytes)  
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
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e62e07b295392732a3ab8803f6f9f85e134cddb8627a947923c37ef5505bf`  
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
$ docker pull telegraf@sha256:4046c04762db9e28ad0fc5beebffaa0edf345ea2c7b8aa3ad5ba8db02f6f4c2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:60e401f12742cafbfa564bb7f31d6e5c35daba0b50e0b5264c0cddac21e0efcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75893896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445d094c3c199fa803bcab90c7ffcc6166fa97f07846d2d88d6b0e3bd5ad333c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 18 Nov 2024 20:48:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caee9ab776a1c2beeb238e0643dbf6f3b7c0a83fd9aa339dc798e2b5272a39f5`  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac69faebcdcde53563af6c2f2356011b54221d2d336fa20004d6e41cf7f676c`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 2.4 MB (2444821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d3519fedc4d5ee37ea7859c2cedc0f290e072022c6947c318979fd6eb71f55`  
		Size: 69.8 MB (69824563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6fc6e4c616b483bafdc6d886f7d5a5c2d59fcbff06d37f5eec6352e6f45818`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:281e39380036537235243436889bf410fd2908fd811d92157772d744f55dba4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c515de8cd05e47bd266f48c2b5b5034383aebbc3b2dfc9e9eb1ba756e4d1da`

```dockerfile
```

-	Layers:
	-	`sha256:b6d2654f5db4cef75f0d0dfbaf9b3095359625a64b11278eaa23d00004cd15d9`  
		Last Modified: Mon, 18 Nov 2024 23:04:07 GMT  
		Size: 1.1 MB (1074253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34df0a4ca1bb919a775b446cf53aed82c5c950fb10f80c1950f2a1e0e6e2abdb`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8c583f2ca801c3c4e1d85d418904406884f11a8faf69abff30fcb998be6ae7d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69563728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a3b7bca19af75445ee828d6ae44a4aca6001ccfbc285e03a0bb04d3c59c691`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 18 Nov 2024 20:48:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2136f9e7feb99945e2787587daa3284c73e45adf2e22f99ad169fe2df7417c`  
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261692eb4698b8fef35728a5f463bc73da3690cc00050ff8eae9c2e6b6f2056c`  
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 2.5 MB (2530622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c097c44c7b51c633d2ea3c42c293141f0aebe80769accd240ba2787ecffc3221`  
		Last Modified: Mon, 18 Nov 2024 23:53:12 GMT  
		Size: 62.9 MB (62944775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cacd0e5e7d2ccf9cf75159eb73e57bd71b2d79b7099539c28a3e36b072c5b7d`  
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c85b59700690d98745cb96f176ac655994b903886cfa983cccbd3eff660a8254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1085315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680778e461d1fab783a7e89f344f6d64cda902be5c72231d3124ae143f05dc76`

```dockerfile
```

-	Layers:
	-	`sha256:61652ab748fb8c98a72a67271f2195ea9bfe2fbdcb40aefb9c49c77d57f46c33`  
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 1.1 MB (1069930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ec49b11d7c57d08dc2c42d71b46d3a5df4d2f3c151e691be742b9ffbc606c06`  
		Size: 15.4 KB (15385 bytes)  
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
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e62e07b295392732a3ab8803f6f9f85e134cddb8627a947923c37ef5505bf`  
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
		Size: 6.4 MB (6435198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:499f40d6cd20f0c782c5d0afcb503cf45cc0c00d4d8266e044b49b5b9ee38cd7`  
		Last Modified: Wed, 25 Dec 2024 10:32:05 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33-alpine`

```console
$ docker pull telegraf@sha256:5abe5982e729899f64303232d10cc164360e8b48cfc83019a60976ac75c4e736
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:56afc6f08c2533886c59d0eaf48f7cac46b4033c184f679f6e7320dd436544b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78895357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4403577c5afdca639d437c201a9aef292a5c8933ac4d890ba63c10b4e4d33f75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3946b3ae4514a58a37deccd6f84334267981743132330e6969cde8ba7d51511e`  
		Last Modified: Tue, 10 Dec 2024 01:29:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d223af490ee78c955b2175e1febe79c8cd6081622ce206ed5c8ffb586e54a`  
		Last Modified: Tue, 10 Dec 2024 01:29:12 GMT  
		Size: 2.4 MB (2444832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c5a91a122385f5fad17011d530eb32627133b82b9397a561f515f3db6f5483`  
		Last Modified: Tue, 10 Dec 2024 01:29:13 GMT  
		Size: 72.8 MB (72826013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6824f28cce7261bf9b8fc7fcbe15409b8d00440edc41b67fd641af40d213f112`  
		Last Modified: Tue, 10 Dec 2024 01:29:12 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:2883f62bcc05b5fb1fb8d695b8ea9f4cfc3d8c57b0f5651156f0c2535cdeb318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1099566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096aa8c212da9dbf8160d81904149a293cd310ee73bc195696f9c926acdd5f5a`

```dockerfile
```

-	Layers:
	-	`sha256:8bdf0771a78b5d9029133efb52d2404092cc534da014190eed53c59a7154085c`  
		Last Modified: Tue, 10 Dec 2024 01:29:12 GMT  
		Size: 1.1 MB (1084303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1cd315410a7184b1a5f15718af4ba6c614d910bad4091474080465a1498c2a9`  
		Last Modified: Tue, 10 Dec 2024 01:29:12 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d073cdd4111aaf73bdc7fd904a294751e08009bdfd5effa6b3775fbcef49df88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72355005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0555ad8ac2c3623881a9086dfd629f446e24f470745fefbcf1fa44c225c51e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2136f9e7feb99945e2787587daa3284c73e45adf2e22f99ad169fe2df7417c`  
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e247ff053d226fd37126c7ecceffb98b618b9eec2760612a700803ed29229f1d`  
		Size: 2.5 MB (2530641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b8407cde6b289ef88c65d4c870f030de85057927bf7f73ccf2183e846830ea`  
		Last Modified: Tue, 10 Dec 2024 02:39:24 GMT  
		Size: 65.7 MB (65736032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a988d5dfd388833596c99e986e35557c873170cd19d2815675410dd36e887136`  
		Last Modified: Tue, 10 Dec 2024 02:39:22 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d6078b18266041b3760f8e5a1c1c3a6f3664a054a103eb7a6a1d086def4319c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1095365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e814c053d793117985578032ae7827f13d9d382c0fd5c4352e551c1e03396569`

```dockerfile
```

-	Layers:
	-	`sha256:c86c350c09cca7742e805c276c6e397619a6c9f9ff31559f406484121eebfe60`  
		Last Modified: Tue, 10 Dec 2024 02:39:22 GMT  
		Size: 1.1 MB (1079980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49f0629751754940eca02cef6f395593841af6903e63c2b86b1f429f69e58c7f`  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33.0`

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

### `telegraf:1.33.0` - linux; amd64

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

### `telegraf:1.33.0` - unknown; unknown

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
		Size: 6.4 MB (6434510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf3b44288d65b3aaa02eb85b924a4dd8fe35501e0fedb30953f9cf9a083146e1`  
		Last Modified: Tue, 24 Dec 2024 23:21:55 GMT  
		Size: 14.8 KB (14771 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.0` - linux; arm variant v7

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
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e62e07b295392732a3ab8803f6f9f85e134cddb8627a947923c37ef5505bf`  
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

### `telegraf:1.33.0` - unknown; unknown

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
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.0` - linux; arm64 variant v8

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

### `telegraf:1.33.0` - unknown; unknown

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
		Size: 6.4 MB (6435198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:499f40d6cd20f0c782c5d0afcb503cf45cc0c00d4d8266e044b49b5b9ee38cd7`  
		Last Modified: Wed, 25 Dec 2024 10:32:05 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33.0-alpine`

```console
$ docker pull telegraf@sha256:5abe5982e729899f64303232d10cc164360e8b48cfc83019a60976ac75c4e736
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33.0-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:56afc6f08c2533886c59d0eaf48f7cac46b4033c184f679f6e7320dd436544b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78895357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4403577c5afdca639d437c201a9aef292a5c8933ac4d890ba63c10b4e4d33f75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3946b3ae4514a58a37deccd6f84334267981743132330e6969cde8ba7d51511e`  
		Last Modified: Tue, 10 Dec 2024 01:29:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d223af490ee78c955b2175e1febe79c8cd6081622ce206ed5c8ffb586e54a`  
		Last Modified: Tue, 10 Dec 2024 01:29:12 GMT  
		Size: 2.4 MB (2444832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c5a91a122385f5fad17011d530eb32627133b82b9397a561f515f3db6f5483`  
		Last Modified: Tue, 10 Dec 2024 01:29:13 GMT  
		Size: 72.8 MB (72826013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6824f28cce7261bf9b8fc7fcbe15409b8d00440edc41b67fd641af40d213f112`  
		Last Modified: Tue, 10 Dec 2024 01:29:12 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.0-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:2883f62bcc05b5fb1fb8d695b8ea9f4cfc3d8c57b0f5651156f0c2535cdeb318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1099566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096aa8c212da9dbf8160d81904149a293cd310ee73bc195696f9c926acdd5f5a`

```dockerfile
```

-	Layers:
	-	`sha256:8bdf0771a78b5d9029133efb52d2404092cc534da014190eed53c59a7154085c`  
		Last Modified: Tue, 10 Dec 2024 01:29:12 GMT  
		Size: 1.1 MB (1084303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1cd315410a7184b1a5f15718af4ba6c614d910bad4091474080465a1498c2a9`  
		Last Modified: Tue, 10 Dec 2024 01:29:12 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.0-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d073cdd4111aaf73bdc7fd904a294751e08009bdfd5effa6b3775fbcef49df88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72355005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0555ad8ac2c3623881a9086dfd629f446e24f470745fefbcf1fa44c225c51e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2136f9e7feb99945e2787587daa3284c73e45adf2e22f99ad169fe2df7417c`  
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e247ff053d226fd37126c7ecceffb98b618b9eec2760612a700803ed29229f1d`  
		Size: 2.5 MB (2530641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b8407cde6b289ef88c65d4c870f030de85057927bf7f73ccf2183e846830ea`  
		Last Modified: Tue, 10 Dec 2024 02:39:24 GMT  
		Size: 65.7 MB (65736032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a988d5dfd388833596c99e986e35557c873170cd19d2815675410dd36e887136`  
		Last Modified: Tue, 10 Dec 2024 02:39:22 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.0-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d6078b18266041b3760f8e5a1c1c3a6f3664a054a103eb7a6a1d086def4319c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1095365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e814c053d793117985578032ae7827f13d9d382c0fd5c4352e551c1e03396569`

```dockerfile
```

-	Layers:
	-	`sha256:c86c350c09cca7742e805c276c6e397619a6c9f9ff31559f406484121eebfe60`  
		Last Modified: Tue, 10 Dec 2024 02:39:22 GMT  
		Size: 1.1 MB (1079980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49f0629751754940eca02cef6f395593841af6903e63c2b86b1f429f69e58c7f`  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:5abe5982e729899f64303232d10cc164360e8b48cfc83019a60976ac75c4e736
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:56afc6f08c2533886c59d0eaf48f7cac46b4033c184f679f6e7320dd436544b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78895357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4403577c5afdca639d437c201a9aef292a5c8933ac4d890ba63c10b4e4d33f75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3946b3ae4514a58a37deccd6f84334267981743132330e6969cde8ba7d51511e`  
		Last Modified: Tue, 10 Dec 2024 01:29:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d223af490ee78c955b2175e1febe79c8cd6081622ce206ed5c8ffb586e54a`  
		Last Modified: Tue, 10 Dec 2024 01:29:12 GMT  
		Size: 2.4 MB (2444832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c5a91a122385f5fad17011d530eb32627133b82b9397a561f515f3db6f5483`  
		Last Modified: Tue, 10 Dec 2024 01:29:13 GMT  
		Size: 72.8 MB (72826013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6824f28cce7261bf9b8fc7fcbe15409b8d00440edc41b67fd641af40d213f112`  
		Last Modified: Tue, 10 Dec 2024 01:29:12 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:2883f62bcc05b5fb1fb8d695b8ea9f4cfc3d8c57b0f5651156f0c2535cdeb318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1099566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096aa8c212da9dbf8160d81904149a293cd310ee73bc195696f9c926acdd5f5a`

```dockerfile
```

-	Layers:
	-	`sha256:8bdf0771a78b5d9029133efb52d2404092cc534da014190eed53c59a7154085c`  
		Last Modified: Tue, 10 Dec 2024 01:29:12 GMT  
		Size: 1.1 MB (1084303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1cd315410a7184b1a5f15718af4ba6c614d910bad4091474080465a1498c2a9`  
		Last Modified: Tue, 10 Dec 2024 01:29:12 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d073cdd4111aaf73bdc7fd904a294751e08009bdfd5effa6b3775fbcef49df88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72355005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0555ad8ac2c3623881a9086dfd629f446e24f470745fefbcf1fa44c225c51e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2136f9e7feb99945e2787587daa3284c73e45adf2e22f99ad169fe2df7417c`  
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e247ff053d226fd37126c7ecceffb98b618b9eec2760612a700803ed29229f1d`  
		Size: 2.5 MB (2530641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b8407cde6b289ef88c65d4c870f030de85057927bf7f73ccf2183e846830ea`  
		Last Modified: Tue, 10 Dec 2024 02:39:24 GMT  
		Size: 65.7 MB (65736032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a988d5dfd388833596c99e986e35557c873170cd19d2815675410dd36e887136`  
		Last Modified: Tue, 10 Dec 2024 02:39:22 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d6078b18266041b3760f8e5a1c1c3a6f3664a054a103eb7a6a1d086def4319c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1095365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e814c053d793117985578032ae7827f13d9d382c0fd5c4352e551c1e03396569`

```dockerfile
```

-	Layers:
	-	`sha256:c86c350c09cca7742e805c276c6e397619a6c9f9ff31559f406484121eebfe60`  
		Last Modified: Tue, 10 Dec 2024 02:39:22 GMT  
		Size: 1.1 MB (1079980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49f0629751754940eca02cef6f395593841af6903e63c2b86b1f429f69e58c7f`  
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
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e62e07b295392732a3ab8803f6f9f85e134cddb8627a947923c37ef5505bf`  
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
		Size: 6.4 MB (6435198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:499f40d6cd20f0c782c5d0afcb503cf45cc0c00d4d8266e044b49b5b9ee38cd7`  
		Last Modified: Wed, 25 Dec 2024 10:32:05 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
