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
-	[`telegraf:1.36.2`](#telegraf1362)
-	[`telegraf:1.36.2-alpine`](#telegraf1362-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.34`

```console
$ docker pull telegraf@sha256:ef3cbfe3b0f53a7ddef29153ab3c33056c0434824702f023147768089457fbfa
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
$ docker pull telegraf@sha256:634b237ed27cfc0ea2dd24470648c529b7e06665f5a67d23a8d0c1a8767d5920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168898019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc441610f3d1f8dd48ce1aaf251f9b85ed88ad267c3dfd60efc6f7402b41d508`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713c0828c39ab022dbf13ba47edb1968e8b2e5c9c0479f3035c18c3e3f69f08f`  
		Last Modified: Tue, 09 Sep 2025 00:10:19 GMT  
		Size: 18.9 MB (18942765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbd87b60718d74054de983d4a9266a059766adfe7c598cc2a2cee738db0bc1d`  
		Last Modified: Mon, 08 Sep 2025 22:38:30 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08dbc3b287c8de62508162e19edf850157fe47256d1503e33a8969d4667dae8`  
		Last Modified: Tue, 09 Sep 2025 00:10:24 GMT  
		Size: 77.4 MB (77446240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967cfee02b473da3c46b4b284d322cd048f4cccb968bb8f6c355518fb48806e5`  
		Last Modified: Mon, 08 Sep 2025 22:38:33 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:f8670880cdbc5dcc824a09b211a2d4471d052052a628023793f56e94ce61f2ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7441e4e50d74d617cdbe8008ad27242adbc44da8d6016e29960d83f3033159de`

```dockerfile
```

-	Layers:
	-	`sha256:6ea4aab32c3dbd6ef0d220d3fb13bcec687b8dc7ac2fb7d33a5fded4862a5f32`  
		Last Modified: Tue, 09 Sep 2025 00:10:18 GMT  
		Size: 6.6 MB (6630220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5bfa398a00445bf8f2faa865d20821cdc8f16fd531314e5df0fb31f967dc03f`  
		Last Modified: Tue, 09 Sep 2025 00:10:19 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:9d9d4f2947c8ab25939c6ca256af1d814a96a21d71372e810bb931afd7db7653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155380920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2635428f4c648840b8c7b89ed96a6fdc1b7de543f2aeff551f695707e1e8ee0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dc4168cb25b55b5cbdedf9511df1cbef908c557840783f9965c3305c8054a6`  
		Last Modified: Mon, 29 Sep 2025 20:04:10 GMT  
		Size: 17.7 MB (17722606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8a3e6793d72d75d4183a83070b45281e8de226228b46b444efb02e7c60e165`  
		Last Modified: Mon, 29 Sep 2025 20:04:09 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ead00392bd1cc6baf443d6408d8ebcfd858091ab848602b80b1b11e44c3b0b`  
		Last Modified: Mon, 29 Sep 2025 20:04:17 GMT  
		Size: 71.5 MB (71527163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ef56a806e829ef311f10de4da8b569268c908102514b3e35457f044698c698`  
		Last Modified: Mon, 29 Sep 2025 20:04:10 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:d4d42bef08a02e20d9c36f6418252c88afe37b2e30c123d2dd366b0e3b538d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6639375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90061ac69b5ef77f5ecb4429fa082c8625ce4a3f22a287c37a8528f6ccd5cdf`

```dockerfile
```

-	Layers:
	-	`sha256:2c9a3024e95aec894d5085e5f069e0be5d2177d119ca8fe64b86e0e5c32f53f2`  
		Last Modified: Mon, 29 Sep 2025 21:10:27 GMT  
		Size: 6.6 MB (6624815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43e4192dfc43d9048e982f3f7950ccf52ef694ed6e4d6676a305cb5fc966523e`  
		Last Modified: Mon, 29 Sep 2025 21:10:28 GMT  
		Size: 14.6 KB (14560 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:32e9e2c23d646ff4133f4bd502fe0241c225d5c9d58853cea02f557f31501be5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161042843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6416ce1b0a7bb22055250d3a4a78ebb753e91f5b7fcfd2ba6b0180f2b60383`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdde913dd621c27e9627581215b4387d186667594d8aecc71c6b3a8699c20d83`  
		Last Modified: Mon, 29 Sep 2025 20:04:08 GMT  
		Size: 18.9 MB (18883763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbe511718c3c1d68ef005e3a700e57399725439222c2ec04dc8d46a0f7fe3f7`  
		Last Modified: Mon, 29 Sep 2025 20:04:02 GMT  
		Size: 3.5 KB (3456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1471c87465f1dcc03bae6cc61a806144639c828392a7c47b188f865472fdffd`  
		Last Modified: Mon, 29 Sep 2025 20:04:20 GMT  
		Size: 70.2 MB (70201192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507567145ad35414d4efc60d280f7d67f078ec7ede54219be90c02da5a2e4dd1`  
		Last Modified: Mon, 29 Sep 2025 20:04:01 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:6347bb6d5213deaef866818588000eafa809b1fed32a42c7c2f474a3e1aa8691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6645474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d93051a7c760ff8e4b46497af7da17b2521a186b83582a6cee7109eb9b97122`

```dockerfile
```

-	Layers:
	-	`sha256:a50b8585f99a7c768692105c4ea1cd7cd9c87c4327686a896319aaca3a117089`  
		Last Modified: Mon, 29 Sep 2025 21:10:34 GMT  
		Size: 6.6 MB (6630896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d5a3ddf938ad49178d83f42068d5286dcaa4c5cde85169b6bc7c685515926c4`  
		Last Modified: Mon, 29 Sep 2025 21:10:34 GMT  
		Size: 14.6 KB (14578 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34-alpine`

```console
$ docker pull telegraf@sha256:60feffd065518dbb2af2ba2be980bfeafdbc0397bdaca6540ed28cdb48e7aad6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e362bcc7d4ae010b3a0c3e4d8b1f9bf282889ad6f7ea994b2b3880e48c475013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83297830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95af6019e0f47aab1b15987c237287a5ef2e1b0b0ba2212a018af58df10444b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 08 Jul 2025 13:49:16 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 08 Jul 2025 13:49:16 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 08 Jul 2025 13:49:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0189be59b6d310438ecb57749d0b53be563f40ffe1756830daa09c83bef8415`  
		Last Modified: Tue, 15 Jul 2025 19:29:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849892cdebd263b6f41ddad1e9e9871a82acbc1ec12f6f6b59662c23a53ecbf1`  
		Last Modified: Tue, 15 Jul 2025 19:29:47 GMT  
		Size: 2.4 MB (2439839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316eafe4c20455456d584383463ddea70937a57b18aec6228e29596ee9de83a7`  
		Last Modified: Tue, 15 Jul 2025 19:30:07 GMT  
		Size: 77.2 MB (77236907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f076fa9b0654a47181d7442facaee6b922f57fa5852d7fc10dd0be83c120b346`  
		Last Modified: Tue, 15 Jul 2025 19:29:47 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e15eb7de3d16b848ef39912698dda6c995896e073b4008ad9600961cdb860db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1115137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f198cead148de598872801d73980fdb724789579180ff32cfe6f04947dad89a`

```dockerfile
```

-	Layers:
	-	`sha256:d3ea611838b71a81e7a7367547df6df24cef1c638e19546e4dc7e33cc7a068de`  
		Last Modified: Tue, 15 Jul 2025 21:10:26 GMT  
		Size: 1.1 MB (1100176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:625f67f8eb83f5062222a4600b78ea3fe502964fed0a9a5926fb7bc39e252874`  
		Last Modified: Tue, 15 Jul 2025 21:10:27 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:929b86ff77a4b3b4ce0d0a3651b6d0971edbe6d13b96082c2478205825e009c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76607081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5638f2b8b3d1b76640983e5e573cdc0dd73f27bdfb4227d103277315a2236da3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
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
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676d46f929b931c62f68a368a8f43b98e689e279ca1c994051b2338ef8c0c1e8`  
		Last Modified: Mon, 29 Sep 2025 20:04:02 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7e353cf49957f5803095c086bcc71a9404f7e7e425dd3c5b44b7fafc0c9fe3`  
		Last Modified: Mon, 29 Sep 2025 20:04:02 GMT  
		Size: 2.5 MB (2521354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c2dcf306fa478d1f4401cdf5531714b34092907a23b91e8d48e1d3b9fb0a79`  
		Last Modified: Mon, 29 Sep 2025 20:04:19 GMT  
		Size: 70.0 MB (69996753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c8250da1742232fd5d28b1c29dad86d9d5ccf47b55dbb92c91f115715e89d`  
		Last Modified: Mon, 29 Sep 2025 20:04:01 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:ec11b896824420b4eb9715f078172eacca870342f72cffc98b5ee3cdd9dcf1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1110874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b990b6f6c5a467bd88b2e54eb910843400050fb4756cdc48bfc62024076c9fc`

```dockerfile
```

-	Layers:
	-	`sha256:7dbeb4d539515b8c1fb84fd7375abd9645c150a4f1c27d09678cac55e13fd79b`  
		Last Modified: Mon, 29 Sep 2025 21:10:30 GMT  
		Size: 1.1 MB (1095803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e868aeb3ff4724c9f41bfaf7a150bde62fff8ac74545ce14e69e3e8fd32cc7d2`  
		Last Modified: Mon, 29 Sep 2025 21:10:31 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34.4`

```console
$ docker pull telegraf@sha256:ef3cbfe3b0f53a7ddef29153ab3c33056c0434824702f023147768089457fbfa
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
$ docker pull telegraf@sha256:634b237ed27cfc0ea2dd24470648c529b7e06665f5a67d23a8d0c1a8767d5920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168898019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc441610f3d1f8dd48ce1aaf251f9b85ed88ad267c3dfd60efc6f7402b41d508`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713c0828c39ab022dbf13ba47edb1968e8b2e5c9c0479f3035c18c3e3f69f08f`  
		Last Modified: Tue, 09 Sep 2025 00:10:19 GMT  
		Size: 18.9 MB (18942765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbd87b60718d74054de983d4a9266a059766adfe7c598cc2a2cee738db0bc1d`  
		Last Modified: Mon, 08 Sep 2025 22:38:30 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08dbc3b287c8de62508162e19edf850157fe47256d1503e33a8969d4667dae8`  
		Last Modified: Tue, 09 Sep 2025 00:10:24 GMT  
		Size: 77.4 MB (77446240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967cfee02b473da3c46b4b284d322cd048f4cccb968bb8f6c355518fb48806e5`  
		Last Modified: Mon, 08 Sep 2025 22:38:33 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:f8670880cdbc5dcc824a09b211a2d4471d052052a628023793f56e94ce61f2ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7441e4e50d74d617cdbe8008ad27242adbc44da8d6016e29960d83f3033159de`

```dockerfile
```

-	Layers:
	-	`sha256:6ea4aab32c3dbd6ef0d220d3fb13bcec687b8dc7ac2fb7d33a5fded4862a5f32`  
		Last Modified: Tue, 09 Sep 2025 00:10:18 GMT  
		Size: 6.6 MB (6630220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5bfa398a00445bf8f2faa865d20821cdc8f16fd531314e5df0fb31f967dc03f`  
		Last Modified: Tue, 09 Sep 2025 00:10:19 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:9d9d4f2947c8ab25939c6ca256af1d814a96a21d71372e810bb931afd7db7653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155380920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2635428f4c648840b8c7b89ed96a6fdc1b7de543f2aeff551f695707e1e8ee0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dc4168cb25b55b5cbdedf9511df1cbef908c557840783f9965c3305c8054a6`  
		Last Modified: Mon, 29 Sep 2025 20:04:10 GMT  
		Size: 17.7 MB (17722606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8a3e6793d72d75d4183a83070b45281e8de226228b46b444efb02e7c60e165`  
		Last Modified: Mon, 29 Sep 2025 20:04:09 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ead00392bd1cc6baf443d6408d8ebcfd858091ab848602b80b1b11e44c3b0b`  
		Last Modified: Mon, 29 Sep 2025 20:04:17 GMT  
		Size: 71.5 MB (71527163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ef56a806e829ef311f10de4da8b569268c908102514b3e35457f044698c698`  
		Last Modified: Mon, 29 Sep 2025 20:04:10 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:d4d42bef08a02e20d9c36f6418252c88afe37b2e30c123d2dd366b0e3b538d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6639375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90061ac69b5ef77f5ecb4429fa082c8625ce4a3f22a287c37a8528f6ccd5cdf`

```dockerfile
```

-	Layers:
	-	`sha256:2c9a3024e95aec894d5085e5f069e0be5d2177d119ca8fe64b86e0e5c32f53f2`  
		Last Modified: Mon, 29 Sep 2025 21:10:27 GMT  
		Size: 6.6 MB (6624815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43e4192dfc43d9048e982f3f7950ccf52ef694ed6e4d6676a305cb5fc966523e`  
		Last Modified: Mon, 29 Sep 2025 21:10:28 GMT  
		Size: 14.6 KB (14560 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:32e9e2c23d646ff4133f4bd502fe0241c225d5c9d58853cea02f557f31501be5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161042843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6416ce1b0a7bb22055250d3a4a78ebb753e91f5b7fcfd2ba6b0180f2b60383`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdde913dd621c27e9627581215b4387d186667594d8aecc71c6b3a8699c20d83`  
		Last Modified: Mon, 29 Sep 2025 20:04:08 GMT  
		Size: 18.9 MB (18883763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbe511718c3c1d68ef005e3a700e57399725439222c2ec04dc8d46a0f7fe3f7`  
		Last Modified: Mon, 29 Sep 2025 20:04:02 GMT  
		Size: 3.5 KB (3456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1471c87465f1dcc03bae6cc61a806144639c828392a7c47b188f865472fdffd`  
		Last Modified: Mon, 29 Sep 2025 20:04:20 GMT  
		Size: 70.2 MB (70201192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507567145ad35414d4efc60d280f7d67f078ec7ede54219be90c02da5a2e4dd1`  
		Last Modified: Mon, 29 Sep 2025 20:04:01 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:6347bb6d5213deaef866818588000eafa809b1fed32a42c7c2f474a3e1aa8691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6645474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d93051a7c760ff8e4b46497af7da17b2521a186b83582a6cee7109eb9b97122`

```dockerfile
```

-	Layers:
	-	`sha256:a50b8585f99a7c768692105c4ea1cd7cd9c87c4327686a896319aaca3a117089`  
		Last Modified: Mon, 29 Sep 2025 21:10:34 GMT  
		Size: 6.6 MB (6630896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d5a3ddf938ad49178d83f42068d5286dcaa4c5cde85169b6bc7c685515926c4`  
		Last Modified: Mon, 29 Sep 2025 21:10:34 GMT  
		Size: 14.6 KB (14578 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34.4-alpine`

```console
$ docker pull telegraf@sha256:60feffd065518dbb2af2ba2be980bfeafdbc0397bdaca6540ed28cdb48e7aad6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e362bcc7d4ae010b3a0c3e4d8b1f9bf282889ad6f7ea994b2b3880e48c475013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83297830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95af6019e0f47aab1b15987c237287a5ef2e1b0b0ba2212a018af58df10444b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 08 Jul 2025 13:49:16 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 08 Jul 2025 13:49:16 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 08 Jul 2025 13:49:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0189be59b6d310438ecb57749d0b53be563f40ffe1756830daa09c83bef8415`  
		Last Modified: Tue, 15 Jul 2025 19:29:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849892cdebd263b6f41ddad1e9e9871a82acbc1ec12f6f6b59662c23a53ecbf1`  
		Last Modified: Tue, 15 Jul 2025 19:29:47 GMT  
		Size: 2.4 MB (2439839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316eafe4c20455456d584383463ddea70937a57b18aec6228e29596ee9de83a7`  
		Last Modified: Tue, 15 Jul 2025 19:30:07 GMT  
		Size: 77.2 MB (77236907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f076fa9b0654a47181d7442facaee6b922f57fa5852d7fc10dd0be83c120b346`  
		Last Modified: Tue, 15 Jul 2025 19:29:47 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e15eb7de3d16b848ef39912698dda6c995896e073b4008ad9600961cdb860db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1115137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f198cead148de598872801d73980fdb724789579180ff32cfe6f04947dad89a`

```dockerfile
```

-	Layers:
	-	`sha256:d3ea611838b71a81e7a7367547df6df24cef1c638e19546e4dc7e33cc7a068de`  
		Last Modified: Tue, 15 Jul 2025 21:10:26 GMT  
		Size: 1.1 MB (1100176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:625f67f8eb83f5062222a4600b78ea3fe502964fed0a9a5926fb7bc39e252874`  
		Last Modified: Tue, 15 Jul 2025 21:10:27 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:929b86ff77a4b3b4ce0d0a3651b6d0971edbe6d13b96082c2478205825e009c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76607081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5638f2b8b3d1b76640983e5e573cdc0dd73f27bdfb4227d103277315a2236da3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
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
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676d46f929b931c62f68a368a8f43b98e689e279ca1c994051b2338ef8c0c1e8`  
		Last Modified: Mon, 29 Sep 2025 20:04:02 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7e353cf49957f5803095c086bcc71a9404f7e7e425dd3c5b44b7fafc0c9fe3`  
		Last Modified: Mon, 29 Sep 2025 20:04:02 GMT  
		Size: 2.5 MB (2521354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c2dcf306fa478d1f4401cdf5531714b34092907a23b91e8d48e1d3b9fb0a79`  
		Last Modified: Mon, 29 Sep 2025 20:04:19 GMT  
		Size: 70.0 MB (69996753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c8250da1742232fd5d28b1c29dad86d9d5ccf47b55dbb92c91f115715e89d`  
		Last Modified: Mon, 29 Sep 2025 20:04:01 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:ec11b896824420b4eb9715f078172eacca870342f72cffc98b5ee3cdd9dcf1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1110874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b990b6f6c5a467bd88b2e54eb910843400050fb4756cdc48bfc62024076c9fc`

```dockerfile
```

-	Layers:
	-	`sha256:7dbeb4d539515b8c1fb84fd7375abd9645c150a4f1c27d09678cac55e13fd79b`  
		Last Modified: Mon, 29 Sep 2025 21:10:30 GMT  
		Size: 1.1 MB (1095803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e868aeb3ff4724c9f41bfaf7a150bde62fff8ac74545ce14e69e3e8fd32cc7d2`  
		Last Modified: Mon, 29 Sep 2025 21:10:31 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35`

```console
$ docker pull telegraf@sha256:089ea91776a2be3c8173f70dc18c9b10390dacaa4e5493debcd713f543dac16c
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
$ docker pull telegraf@sha256:36d255dd9ae95d3e27b946eb1fe0b49fc2af2345008072da50014e4bcda242ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171022468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0dc6c618d32f6cde59aec8a49d929007d42b66db90f523a03c87efb89da0ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f0e44eea62b373168e2637ef3acd7d9c0cdc1f54e46dbba237c53ffe1a6677`  
		Last Modified: Mon, 08 Sep 2025 23:07:11 GMT  
		Size: 18.9 MB (18942775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b8e00afe64f97c33175f8fd3049909003fc239302631480338eada1d36e866`  
		Last Modified: Mon, 08 Sep 2025 22:38:28 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e040dee2cd7e3fe769dbf2c2d7354e6001775cbf76d3ecaba320d245a47391`  
		Last Modified: Mon, 08 Sep 2025 23:07:23 GMT  
		Size: 79.6 MB (79570693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d38927b48db8048f0c4e35f6b04babcf2270a93ac7b3123fa1e51a3049676e`  
		Last Modified: Mon, 08 Sep 2025 22:38:32 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:9b16d545ae6013b56868cd457f45e3f0307b650a64427869a8ce59884cd01193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfa191c748905e60046920fe24441aacd2d46d7291b6276e72faa1e69a835fe`

```dockerfile
```

-	Layers:
	-	`sha256:986b097123cd85a28ac5c30b5895d3005769d9941e963c1b1ee283e5d579f842`  
		Last Modified: Tue, 09 Sep 2025 00:10:26 GMT  
		Size: 6.6 MB (6645248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3460e2249de1c5dc714828e70f912f1132d32b07cab2fd1c11853efa3ace949b`  
		Last Modified: Tue, 09 Sep 2025 00:10:27 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:6dee59d6ff5e21136ffca76eac77449683df014eab9aa3cab2aa4b4dc7238952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157144464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2c4fce79643f5d2c55fe148018dea02aa8a4d9a949b8a353f989947f454ee2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b69b4e6862d27a9410f082f3b8a07f3bac8d26902a3499beeb2cc3a116ea3af`  
		Last Modified: Mon, 29 Sep 2025 20:05:09 GMT  
		Size: 17.7 MB (17722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7608f70d7a008d211059ab5971134d36b83b88c3ce73d5ac9f53d10d5d2d7a2d`  
		Last Modified: Mon, 29 Sep 2025 20:05:06 GMT  
		Size: 3.4 KB (3439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9453de39ae0f2cce4c257ca22c19ab8d51888b10267d8144c139de70c039886`  
		Last Modified: Mon, 29 Sep 2025 21:17:06 GMT  
		Size: 73.3 MB (73290729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feae187d06675c3afedbd2b180fd04c608ae0ac53ef990ced23fe0980f52e8f1`  
		Last Modified: Mon, 29 Sep 2025 20:05:06 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:cf06fd49f0c4c20700db7f75b469f1870e29cc846062e47363229f8ffc66490c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6654103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417f6952143821be528bcdd5c7ad2a4248d7e9adca7b70742b10ac151dc0aab4`

```dockerfile
```

-	Layers:
	-	`sha256:c11e4e5764a3c1b548098a3e03cb143fbf5352630f3eea92d6208b226d670942`  
		Last Modified: Mon, 29 Sep 2025 21:10:46 GMT  
		Size: 6.6 MB (6639543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:098baf02df52d0311fb868a529fdfa1304001a53d2f523c1917b2fd3cf5d3390`  
		Last Modified: Mon, 29 Sep 2025 21:10:47 GMT  
		Size: 14.6 KB (14560 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:03e93a2fe86cd0360ab6e1b003b70804beb887c710085c97417ed0c5e3387890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162921403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e222dd26c4186173c08c817617f8a6c88be2ac2b8496dc49bcb524f38c533ea8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fec91e847cd476ea430df3e65ea423e3641f54e46d22d9289932ef6b4df1af`  
		Last Modified: Mon, 29 Sep 2025 20:04:35 GMT  
		Size: 18.9 MB (18884229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673f00c58d54cb4f5a9f22af62013d9350fc003573e785c76f6b1e4f50ac2505`  
		Last Modified: Mon, 29 Sep 2025 20:04:33 GMT  
		Size: 3.5 KB (3453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e818dff6ededa710dd3d1e6ee35effa8b11d6aed378856767dbbc814dff78e16`  
		Last Modified: Mon, 29 Sep 2025 20:04:46 GMT  
		Size: 72.1 MB (72079291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe4eefaa7dada4e206c13378f291c068a881e7802265605b46757ef2442fc6a`  
		Last Modified: Mon, 29 Sep 2025 20:04:31 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:88b30d8ee9fef452ce89fe8479781674534a1ef30e8b02e19e3a3850b082d535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea3e1e9c5c7cbdf5c7475fe343b333943b7a9f162c801340909fea9b23535b4`

```dockerfile
```

-	Layers:
	-	`sha256:01569e591efda49b41604f0a88c5530a03e9594365d57c7e2c67f019c094355f`  
		Last Modified: Mon, 29 Sep 2025 21:10:54 GMT  
		Size: 6.6 MB (6645622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed4799f5077dfc1ffc9a827bca4507da7d2d3017682d21224f420943c240e949`  
		Last Modified: Mon, 29 Sep 2025 21:10:55 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35-alpine`

```console
$ docker pull telegraf@sha256:392f91d8f25afefda481c24d1b58e7ecb793fbdd4f5768ad1f77b14eab6ad871
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b9f1dad8bfc6e2e0a071ec3708f69b608314a1638df1a27dbee6c8d9c201157d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85721229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1898bfc2837a825d9ca57c11162f841378cca6e17895db8ff8007425b40ae030`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111a65e71ad846fe6bc5cf5d9981577f402356a07fa8643556a52a493832248d`  
		Last Modified: Tue, 19 Aug 2025 16:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cbaff1778259b3073527b025ae9ab08156e23a8b7f42fbbc0fafca178fc2a4`  
		Last Modified: Tue, 19 Aug 2025 16:43:11 GMT  
		Size: 2.6 MB (2552105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e527cfac45a96a64d7cc6821810e5660eec3f9f105ee9595ff5d0ef9ce3889e5`  
		Last Modified: Tue, 19 Aug 2025 16:43:18 GMT  
		Size: 79.4 MB (79368534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701fb22e4edb908e9c9db1946c3275c80eb50f1b6a4a0a263e2bcc780d2db6cb`  
		Last Modified: Tue, 19 Aug 2025 16:43:13 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d62ff060ab03e0e18dd18b68bef85d0e6253116947fe2889d8b0627c72be5d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1146960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00067d3ac59b152349cce2ee62d1d1fc80d424366cca0741b5130316ec1f36f0`

```dockerfile
```

-	Layers:
	-	`sha256:ae9d5119dea6d9d8dc370f0197b7815e7ea4eab7a50e3962df4ff7507b5ec15b`  
		Last Modified: Tue, 19 Aug 2025 18:10:39 GMT  
		Size: 1.1 MB (1131697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2678129d408de246508eace01dabc93d4762f22a4bce5468f32eb78e3c0d9cf4`  
		Last Modified: Tue, 19 Aug 2025 18:10:40 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:efe8805729f22ff921c2d40f617ec08d6e6ab248a971b532e3936f3f425c860d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78624887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d2a1ad93836ad2ccc3e2dafa19541125e7faa1621d23baedd6682a3806c7cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e08e8bbbfa51f82a9c53e3b3c881588fc27adc2ce6f93bb9e94dadf8554096`  
		Last Modified: Mon, 29 Sep 2025 20:04:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69556eba8836e94327a9e1bd227870982172ace6763bcee7453f5e92fc3aab34`  
		Last Modified: Mon, 29 Sep 2025 20:04:22 GMT  
		Size: 2.6 MB (2616103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2f7af0b25a30bc3499f49baf594c9fff529854b75e52781fba082bc15aec6b`  
		Last Modified: Mon, 29 Sep 2025 20:04:28 GMT  
		Size: 71.9 MB (71877135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3c3cec64506711e37ae0bba8f2871d671b5642e508160aa37c1467e93a039a`  
		Last Modified: Mon, 29 Sep 2025 20:04:22 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4f0d90a1f69783989fc907fbca1ff98e8c49b06b4f9999429d8e867de46ff7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1142093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce49bc2eb5ea014ba3ff1a39577bad4c7cec3ae8874519fe150a5cdfddc8d8f`

```dockerfile
```

-	Layers:
	-	`sha256:f5b4eb8725f9f168d1df38e3615374f105f7246ad471e43a764bd95940f1f7a2`  
		Last Modified: Mon, 29 Sep 2025 21:10:51 GMT  
		Size: 1.1 MB (1127022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25c94fdf46808cbfedf139b211b89b177e6b56e2210ad42c97ccb86dadcca49`  
		Last Modified: Mon, 29 Sep 2025 21:10:52 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4`

```console
$ docker pull telegraf@sha256:089ea91776a2be3c8173f70dc18c9b10390dacaa4e5493debcd713f543dac16c
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
$ docker pull telegraf@sha256:36d255dd9ae95d3e27b946eb1fe0b49fc2af2345008072da50014e4bcda242ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171022468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0dc6c618d32f6cde59aec8a49d929007d42b66db90f523a03c87efb89da0ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f0e44eea62b373168e2637ef3acd7d9c0cdc1f54e46dbba237c53ffe1a6677`  
		Last Modified: Mon, 08 Sep 2025 23:07:11 GMT  
		Size: 18.9 MB (18942775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b8e00afe64f97c33175f8fd3049909003fc239302631480338eada1d36e866`  
		Last Modified: Mon, 08 Sep 2025 22:38:28 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e040dee2cd7e3fe769dbf2c2d7354e6001775cbf76d3ecaba320d245a47391`  
		Last Modified: Mon, 08 Sep 2025 23:07:23 GMT  
		Size: 79.6 MB (79570693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d38927b48db8048f0c4e35f6b04babcf2270a93ac7b3123fa1e51a3049676e`  
		Last Modified: Mon, 08 Sep 2025 22:38:32 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:9b16d545ae6013b56868cd457f45e3f0307b650a64427869a8ce59884cd01193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfa191c748905e60046920fe24441aacd2d46d7291b6276e72faa1e69a835fe`

```dockerfile
```

-	Layers:
	-	`sha256:986b097123cd85a28ac5c30b5895d3005769d9941e963c1b1ee283e5d579f842`  
		Last Modified: Tue, 09 Sep 2025 00:10:26 GMT  
		Size: 6.6 MB (6645248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3460e2249de1c5dc714828e70f912f1132d32b07cab2fd1c11853efa3ace949b`  
		Last Modified: Tue, 09 Sep 2025 00:10:27 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:6dee59d6ff5e21136ffca76eac77449683df014eab9aa3cab2aa4b4dc7238952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157144464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2c4fce79643f5d2c55fe148018dea02aa8a4d9a949b8a353f989947f454ee2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b69b4e6862d27a9410f082f3b8a07f3bac8d26902a3499beeb2cc3a116ea3af`  
		Last Modified: Mon, 29 Sep 2025 20:05:09 GMT  
		Size: 17.7 MB (17722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7608f70d7a008d211059ab5971134d36b83b88c3ce73d5ac9f53d10d5d2d7a2d`  
		Last Modified: Mon, 29 Sep 2025 20:05:06 GMT  
		Size: 3.4 KB (3439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9453de39ae0f2cce4c257ca22c19ab8d51888b10267d8144c139de70c039886`  
		Last Modified: Mon, 29 Sep 2025 21:17:06 GMT  
		Size: 73.3 MB (73290729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feae187d06675c3afedbd2b180fd04c608ae0ac53ef990ced23fe0980f52e8f1`  
		Last Modified: Mon, 29 Sep 2025 20:05:06 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:cf06fd49f0c4c20700db7f75b469f1870e29cc846062e47363229f8ffc66490c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6654103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417f6952143821be528bcdd5c7ad2a4248d7e9adca7b70742b10ac151dc0aab4`

```dockerfile
```

-	Layers:
	-	`sha256:c11e4e5764a3c1b548098a3e03cb143fbf5352630f3eea92d6208b226d670942`  
		Last Modified: Mon, 29 Sep 2025 21:10:46 GMT  
		Size: 6.6 MB (6639543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:098baf02df52d0311fb868a529fdfa1304001a53d2f523c1917b2fd3cf5d3390`  
		Last Modified: Mon, 29 Sep 2025 21:10:47 GMT  
		Size: 14.6 KB (14560 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:03e93a2fe86cd0360ab6e1b003b70804beb887c710085c97417ed0c5e3387890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162921403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e222dd26c4186173c08c817617f8a6c88be2ac2b8496dc49bcb524f38c533ea8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fec91e847cd476ea430df3e65ea423e3641f54e46d22d9289932ef6b4df1af`  
		Last Modified: Mon, 29 Sep 2025 20:04:35 GMT  
		Size: 18.9 MB (18884229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673f00c58d54cb4f5a9f22af62013d9350fc003573e785c76f6b1e4f50ac2505`  
		Last Modified: Mon, 29 Sep 2025 20:04:33 GMT  
		Size: 3.5 KB (3453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e818dff6ededa710dd3d1e6ee35effa8b11d6aed378856767dbbc814dff78e16`  
		Last Modified: Mon, 29 Sep 2025 20:04:46 GMT  
		Size: 72.1 MB (72079291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe4eefaa7dada4e206c13378f291c068a881e7802265605b46757ef2442fc6a`  
		Last Modified: Mon, 29 Sep 2025 20:04:31 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:88b30d8ee9fef452ce89fe8479781674534a1ef30e8b02e19e3a3850b082d535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea3e1e9c5c7cbdf5c7475fe343b333943b7a9f162c801340909fea9b23535b4`

```dockerfile
```

-	Layers:
	-	`sha256:01569e591efda49b41604f0a88c5530a03e9594365d57c7e2c67f019c094355f`  
		Last Modified: Mon, 29 Sep 2025 21:10:54 GMT  
		Size: 6.6 MB (6645622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed4799f5077dfc1ffc9a827bca4507da7d2d3017682d21224f420943c240e949`  
		Last Modified: Mon, 29 Sep 2025 21:10:55 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4-alpine`

```console
$ docker pull telegraf@sha256:392f91d8f25afefda481c24d1b58e7ecb793fbdd4f5768ad1f77b14eab6ad871
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b9f1dad8bfc6e2e0a071ec3708f69b608314a1638df1a27dbee6c8d9c201157d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85721229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1898bfc2837a825d9ca57c11162f841378cca6e17895db8ff8007425b40ae030`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111a65e71ad846fe6bc5cf5d9981577f402356a07fa8643556a52a493832248d`  
		Last Modified: Tue, 19 Aug 2025 16:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cbaff1778259b3073527b025ae9ab08156e23a8b7f42fbbc0fafca178fc2a4`  
		Last Modified: Tue, 19 Aug 2025 16:43:11 GMT  
		Size: 2.6 MB (2552105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e527cfac45a96a64d7cc6821810e5660eec3f9f105ee9595ff5d0ef9ce3889e5`  
		Last Modified: Tue, 19 Aug 2025 16:43:18 GMT  
		Size: 79.4 MB (79368534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701fb22e4edb908e9c9db1946c3275c80eb50f1b6a4a0a263e2bcc780d2db6cb`  
		Last Modified: Tue, 19 Aug 2025 16:43:13 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d62ff060ab03e0e18dd18b68bef85d0e6253116947fe2889d8b0627c72be5d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1146960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00067d3ac59b152349cce2ee62d1d1fc80d424366cca0741b5130316ec1f36f0`

```dockerfile
```

-	Layers:
	-	`sha256:ae9d5119dea6d9d8dc370f0197b7815e7ea4eab7a50e3962df4ff7507b5ec15b`  
		Last Modified: Tue, 19 Aug 2025 18:10:39 GMT  
		Size: 1.1 MB (1131697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2678129d408de246508eace01dabc93d4762f22a4bce5468f32eb78e3c0d9cf4`  
		Last Modified: Tue, 19 Aug 2025 18:10:40 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:efe8805729f22ff921c2d40f617ec08d6e6ab248a971b532e3936f3f425c860d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78624887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d2a1ad93836ad2ccc3e2dafa19541125e7faa1621d23baedd6682a3806c7cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e08e8bbbfa51f82a9c53e3b3c881588fc27adc2ce6f93bb9e94dadf8554096`  
		Last Modified: Mon, 29 Sep 2025 20:04:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69556eba8836e94327a9e1bd227870982172ace6763bcee7453f5e92fc3aab34`  
		Last Modified: Mon, 29 Sep 2025 20:04:22 GMT  
		Size: 2.6 MB (2616103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2f7af0b25a30bc3499f49baf594c9fff529854b75e52781fba082bc15aec6b`  
		Last Modified: Mon, 29 Sep 2025 20:04:28 GMT  
		Size: 71.9 MB (71877135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3c3cec64506711e37ae0bba8f2871d671b5642e508160aa37c1467e93a039a`  
		Last Modified: Mon, 29 Sep 2025 20:04:22 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4f0d90a1f69783989fc907fbca1ff98e8c49b06b4f9999429d8e867de46ff7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1142093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce49bc2eb5ea014ba3ff1a39577bad4c7cec3ae8874519fe150a5cdfddc8d8f`

```dockerfile
```

-	Layers:
	-	`sha256:f5b4eb8725f9f168d1df38e3615374f105f7246ad471e43a764bd95940f1f7a2`  
		Last Modified: Mon, 29 Sep 2025 21:10:51 GMT  
		Size: 1.1 MB (1127022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25c94fdf46808cbfedf139b211b89b177e6b56e2210ad42c97ccb86dadcca49`  
		Last Modified: Mon, 29 Sep 2025 21:10:52 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36`

```console
$ docker pull telegraf@sha256:cf14507fc088bba807d9b4ab2597fb40f74f62f9c645a84ecb0e99869e67ee0c
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
$ docker pull telegraf@sha256:09efd7277e074e14f58b6aa50cd107c8abbe6898aa2c2b9029b647bf3fc60fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171241057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:360e8b4feb461261003f6e94145404dea824e7d2d377a10f73c907879a6d8e09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
ENV TELEGRAF_VERSION=1.36.1
# Tue, 09 Sep 2025 01:37:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Sep 2025 01:37:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 01:37:08 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d1a0f1ddd0803d51fc5f5e8d035ed9a04f06bd2551fff5d94ae9d975432043`  
		Last Modified: Tue, 09 Sep 2025 18:16:58 GMT  
		Size: 18.9 MB (18942917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34061fc6be711b5b2ce5fc1c01a7957a0185335d4f3a072ca25ff5d71720d1c0`  
		Last Modified: Tue, 09 Sep 2025 18:16:57 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35e6b83a3d36081bbc656e054ae64c8f27682b2e806fa1017ce19ca3d4cd491`  
		Last Modified: Tue, 09 Sep 2025 18:17:07 GMT  
		Size: 79.8 MB (79789123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a12c0b1ff0f0351a224730958090f2affd58e5f8240144929ba6a35ead76df`  
		Last Modified: Tue, 09 Sep 2025 18:16:57 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:7771fe69ee44718411df1cdca9e3a15916321f1f1c63238642f96214060bc016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6661775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7fb2ab2239ee79cb670069fc8c329b36181567c19380d1a18c50f8badbced1`

```dockerfile
```

-	Layers:
	-	`sha256:a9aeb94991521f1fa2b26acae8b4ad303da7a09962a20ec3aaf10189f2426ed7`  
		Last Modified: Tue, 09 Sep 2025 21:10:29 GMT  
		Size: 6.6 MB (6647004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec01a023330011a1460d6bbff15171bbc3c3dae60bf4545430b933e395e2130d`  
		Last Modified: Tue, 09 Sep 2025 21:10:30 GMT  
		Size: 14.8 KB (14771 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:47b7cf4918ba95e369b819d425d382bafeb3891f85d0b200739f2263c9e2a04f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157635396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f38dac53bd952e7345f4da097568b7ce44e564f68b60cfe64c96c86c1e9ace1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.36.2
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dc4168cb25b55b5cbdedf9511df1cbef908c557840783f9965c3305c8054a6`  
		Last Modified: Mon, 29 Sep 2025 20:04:10 GMT  
		Size: 17.7 MB (17722606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8a3e6793d72d75d4183a83070b45281e8de226228b46b444efb02e7c60e165`  
		Last Modified: Mon, 29 Sep 2025 20:04:09 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcc5c2a03ead4e05a39572278e5fc3e0971bbdad892d18dbecc793ab09e3df1`  
		Last Modified: Mon, 29 Sep 2025 20:04:38 GMT  
		Size: 73.8 MB (73781640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546c32e0fd3be9b4ace9f1a772d18bc3deeb968927a39f17baebfb2f8497ced0`  
		Last Modified: Mon, 29 Sep 2025 20:04:32 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:5a678d2ca71996bed4a0eac1c6bf23e40de9a7bc1ca2afacc654135478624df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6661453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18df71b3865865e04ed03947cd0add0fa78eac0af1a584e6e20309b78cdd8995`

```dockerfile
```

-	Layers:
	-	`sha256:b6f3539c45f9147b7e9b404ed5508c4539d5b84fe061da2c2377b554482defa8`  
		Last Modified: Mon, 29 Sep 2025 21:11:10 GMT  
		Size: 6.6 MB (6646583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d661fc2bdbd8be2674af91da8a1777c5c4e9084b90b2d80aeb12322339ad456e`  
		Last Modified: Mon, 29 Sep 2025 21:11:11 GMT  
		Size: 14.9 KB (14870 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5008708de5ea25fb22009e01875963707a3ea95f72430173a21dda0bebb559e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162400874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cab57a13f6a864f609b2e9b039d2bf69374f8014daa50e63aff12f25622bc97`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.36.2
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed67e27f81fe86d6b042c6a6b65e21ad8b606b040ff540bf83e62f61ca44f97`  
		Last Modified: Mon, 29 Sep 2025 20:09:13 GMT  
		Size: 18.9 MB (18884201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c011997a0b2aeaae8fe9b40ac5ff95e698b3bddfa9302d53ffcf72e33386e58f`  
		Last Modified: Mon, 29 Sep 2025 20:09:12 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc86dff5cbd5a940b8dd231af96ff7e0ca52d7a881185f1f89415984bd8b422`  
		Last Modified: Mon, 29 Sep 2025 20:09:17 GMT  
		Size: 71.6 MB (71558800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0ee1630ffd40588db8f671a7f705d33f26ac046579135282119b89b025a933`  
		Last Modified: Mon, 29 Sep 2025 20:09:13 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:9e9ae8848ca744f5cf3c89bb0cbf2aed72e6df137daa73cc9c503548c0ffb7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6667560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0bf7181961c80924da12c1c78eebf6791cb3b50a7382594ec6efbabcc6f198e`

```dockerfile
```

-	Layers:
	-	`sha256:2bc796c7f2841ce6c35b8f6e261f1accb7c8f0e539ea3264db317bd0a042c156`  
		Last Modified: Mon, 29 Sep 2025 21:11:16 GMT  
		Size: 6.7 MB (6652666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a6d1548f9bdad55b659b7e51c03f2d6f72570d137b8645225a5b6abd039a6fd`  
		Last Modified: Mon, 29 Sep 2025 21:11:17 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36-alpine`

```console
$ docker pull telegraf@sha256:dcfbbeff303b6f86f8b7b473f92f7976fa99687b215d19482cd43fcf92dc11e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:4baf3d0febd72178f98f5f91d3b3610c4ee3928800e5b760f41e78bc0d5ecab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85939075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea7730189c7e10c6b12a83f37f295d23aa5670f46cf0043841c3bfed8babcf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 01:37:08 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
ENV TELEGRAF_VERSION=1.36.1
# Tue, 09 Sep 2025 01:37:08 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Sep 2025 01:37:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 01:37:08 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a2890272a02dda8552f8b5a7284009a0ab2fa049a7b64209625a9bb6271dfd`  
		Last Modified: Tue, 09 Sep 2025 18:16:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9357318f01d6bb7addaaae6f3179c368231969b186628d4c7806adf18ee2cc03`  
		Last Modified: Tue, 09 Sep 2025 18:16:58 GMT  
		Size: 2.6 MB (2552109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902c19770a605c522bb610c30eafa11d02d2b97df29bcfeac8da080e0a22790c`  
		Last Modified: Tue, 09 Sep 2025 18:17:10 GMT  
		Size: 79.6 MB (79586378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3862474385352367a328b157091e0d84f94392f45d799cb6bc4cf0155a489b4e`  
		Last Modified: Tue, 09 Sep 2025 18:16:58 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:acb4525ea924ad37eac15b6875795915046178da610141ba2445a9d0741d4a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1148716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badb9b5302d0ee7eb2f67f824289edfd801a726106421ba49ce8964c9a324162`

```dockerfile
```

-	Layers:
	-	`sha256:b056972c63283a0cfa5392eb3c7c3918e1a687245ba26a90cd1b98d9178beaba`  
		Last Modified: Tue, 09 Sep 2025 21:10:36 GMT  
		Size: 1.1 MB (1133453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:742d9947d617762d40197f2a1821f53753272d8c379848aecb7e8b46428b4c09`  
		Last Modified: Tue, 09 Sep 2025 21:10:37 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8e76a566c829fa70a3c0ddb789baae7ecf3b82b6365cda75fc649935c3a3ff4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78103825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f5a3f9b7faa0af5a9bfb182cfed63d2927a01b1650ee53070aee91e6d25a64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.36.2
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478342f3673521ce474529789681e0a1b13cfad57c81eb3f3ef521a7fdeaf83d`  
		Last Modified: Mon, 29 Sep 2025 20:04:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd33640a76eefaa3b65db81ca4f6c4860eb0e4b5abd4019fdf0d7e0c685a9689`  
		Last Modified: Mon, 29 Sep 2025 20:04:12 GMT  
		Size: 2.6 MB (2616107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e3bc9fdd7eb4d762c1c7e6bfc0a0f19abe5617c73b3afdedb870d2158eae02`  
		Last Modified: Mon, 29 Sep 2025 20:04:22 GMT  
		Size: 71.4 MB (71356070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64df0f28a68d54b5492b00273c7e26626b204b866bf3ed18cb4c5f5a281a5825`  
		Last Modified: Mon, 29 Sep 2025 20:04:08 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:70ce115fd0ab7907a509734b83b729101b64319e1a782e115b96adcb3acfc151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1149451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d083ca1f53da5b3e3db8e63032173d0dd27c8a140c7fb1ff9a152688f2846f71`

```dockerfile
```

-	Layers:
	-	`sha256:08cd96849dc563c9588374bc84324df94c28e852cbcee02f9c60cc59fe685e20`  
		Last Modified: Mon, 29 Sep 2025 21:11:10 GMT  
		Size: 1.1 MB (1134066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f47d66aa3bc216f253542b9e87847540adf890bd032a1cb2303abd547996428`  
		Last Modified: Mon, 29 Sep 2025 21:11:11 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.2`

```console
$ docker pull telegraf@sha256:1cdf94248c85f530ca6889c0228693578eadc2cfddd3af56791404618d6fd492
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.2` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:47b7cf4918ba95e369b819d425d382bafeb3891f85d0b200739f2263c9e2a04f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157635396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f38dac53bd952e7345f4da097568b7ce44e564f68b60cfe64c96c86c1e9ace1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.36.2
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dc4168cb25b55b5cbdedf9511df1cbef908c557840783f9965c3305c8054a6`  
		Last Modified: Mon, 29 Sep 2025 20:04:10 GMT  
		Size: 17.7 MB (17722606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8a3e6793d72d75d4183a83070b45281e8de226228b46b444efb02e7c60e165`  
		Last Modified: Mon, 29 Sep 2025 20:04:09 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcc5c2a03ead4e05a39572278e5fc3e0971bbdad892d18dbecc793ab09e3df1`  
		Last Modified: Mon, 29 Sep 2025 20:04:38 GMT  
		Size: 73.8 MB (73781640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546c32e0fd3be9b4ace9f1a772d18bc3deeb968927a39f17baebfb2f8497ced0`  
		Last Modified: Mon, 29 Sep 2025 20:04:32 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:5a678d2ca71996bed4a0eac1c6bf23e40de9a7bc1ca2afacc654135478624df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6661453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18df71b3865865e04ed03947cd0add0fa78eac0af1a584e6e20309b78cdd8995`

```dockerfile
```

-	Layers:
	-	`sha256:b6f3539c45f9147b7e9b404ed5508c4539d5b84fe061da2c2377b554482defa8`  
		Last Modified: Mon, 29 Sep 2025 21:11:10 GMT  
		Size: 6.6 MB (6646583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d661fc2bdbd8be2674af91da8a1777c5c4e9084b90b2d80aeb12322339ad456e`  
		Last Modified: Mon, 29 Sep 2025 21:11:11 GMT  
		Size: 14.9 KB (14870 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.2` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5008708de5ea25fb22009e01875963707a3ea95f72430173a21dda0bebb559e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162400874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cab57a13f6a864f609b2e9b039d2bf69374f8014daa50e63aff12f25622bc97`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.36.2
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed67e27f81fe86d6b042c6a6b65e21ad8b606b040ff540bf83e62f61ca44f97`  
		Last Modified: Mon, 29 Sep 2025 20:09:13 GMT  
		Size: 18.9 MB (18884201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c011997a0b2aeaae8fe9b40ac5ff95e698b3bddfa9302d53ffcf72e33386e58f`  
		Last Modified: Mon, 29 Sep 2025 20:09:12 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc86dff5cbd5a940b8dd231af96ff7e0ca52d7a881185f1f89415984bd8b422`  
		Last Modified: Mon, 29 Sep 2025 20:09:17 GMT  
		Size: 71.6 MB (71558800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0ee1630ffd40588db8f671a7f705d33f26ac046579135282119b89b025a933`  
		Last Modified: Mon, 29 Sep 2025 20:09:13 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:9e9ae8848ca744f5cf3c89bb0cbf2aed72e6df137daa73cc9c503548c0ffb7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6667560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0bf7181961c80924da12c1c78eebf6791cb3b50a7382594ec6efbabcc6f198e`

```dockerfile
```

-	Layers:
	-	`sha256:2bc796c7f2841ce6c35b8f6e261f1accb7c8f0e539ea3264db317bd0a042c156`  
		Last Modified: Mon, 29 Sep 2025 21:11:16 GMT  
		Size: 6.7 MB (6652666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a6d1548f9bdad55b659b7e51c03f2d6f72570d137b8645225a5b6abd039a6fd`  
		Last Modified: Mon, 29 Sep 2025 21:11:17 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.2-alpine`

```console
$ docker pull telegraf@sha256:8b414da2669fa0c018ca08bf80b78e9baf8af8a775c717e46ea8ae301e5d0214
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.2-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8e76a566c829fa70a3c0ddb789baae7ecf3b82b6365cda75fc649935c3a3ff4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78103825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f5a3f9b7faa0af5a9bfb182cfed63d2927a01b1650ee53070aee91e6d25a64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.36.2
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478342f3673521ce474529789681e0a1b13cfad57c81eb3f3ef521a7fdeaf83d`  
		Last Modified: Mon, 29 Sep 2025 20:04:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd33640a76eefaa3b65db81ca4f6c4860eb0e4b5abd4019fdf0d7e0c685a9689`  
		Last Modified: Mon, 29 Sep 2025 20:04:12 GMT  
		Size: 2.6 MB (2616107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e3bc9fdd7eb4d762c1c7e6bfc0a0f19abe5617c73b3afdedb870d2158eae02`  
		Last Modified: Mon, 29 Sep 2025 20:04:22 GMT  
		Size: 71.4 MB (71356070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64df0f28a68d54b5492b00273c7e26626b204b866bf3ed18cb4c5f5a281a5825`  
		Last Modified: Mon, 29 Sep 2025 20:04:08 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.2-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:70ce115fd0ab7907a509734b83b729101b64319e1a782e115b96adcb3acfc151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1149451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d083ca1f53da5b3e3db8e63032173d0dd27c8a140c7fb1ff9a152688f2846f71`

```dockerfile
```

-	Layers:
	-	`sha256:08cd96849dc563c9588374bc84324df94c28e852cbcee02f9c60cc59fe685e20`  
		Last Modified: Mon, 29 Sep 2025 21:11:10 GMT  
		Size: 1.1 MB (1134066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f47d66aa3bc216f253542b9e87847540adf890bd032a1cb2303abd547996428`  
		Last Modified: Mon, 29 Sep 2025 21:11:11 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:dcfbbeff303b6f86f8b7b473f92f7976fa99687b215d19482cd43fcf92dc11e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:4baf3d0febd72178f98f5f91d3b3610c4ee3928800e5b760f41e78bc0d5ecab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85939075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea7730189c7e10c6b12a83f37f295d23aa5670f46cf0043841c3bfed8babcf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 01:37:08 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
ENV TELEGRAF_VERSION=1.36.1
# Tue, 09 Sep 2025 01:37:08 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Sep 2025 01:37:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 01:37:08 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a2890272a02dda8552f8b5a7284009a0ab2fa049a7b64209625a9bb6271dfd`  
		Last Modified: Tue, 09 Sep 2025 18:16:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9357318f01d6bb7addaaae6f3179c368231969b186628d4c7806adf18ee2cc03`  
		Last Modified: Tue, 09 Sep 2025 18:16:58 GMT  
		Size: 2.6 MB (2552109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902c19770a605c522bb610c30eafa11d02d2b97df29bcfeac8da080e0a22790c`  
		Last Modified: Tue, 09 Sep 2025 18:17:10 GMT  
		Size: 79.6 MB (79586378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3862474385352367a328b157091e0d84f94392f45d799cb6bc4cf0155a489b4e`  
		Last Modified: Tue, 09 Sep 2025 18:16:58 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:acb4525ea924ad37eac15b6875795915046178da610141ba2445a9d0741d4a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1148716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badb9b5302d0ee7eb2f67f824289edfd801a726106421ba49ce8964c9a324162`

```dockerfile
```

-	Layers:
	-	`sha256:b056972c63283a0cfa5392eb3c7c3918e1a687245ba26a90cd1b98d9178beaba`  
		Last Modified: Tue, 09 Sep 2025 21:10:36 GMT  
		Size: 1.1 MB (1133453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:742d9947d617762d40197f2a1821f53753272d8c379848aecb7e8b46428b4c09`  
		Last Modified: Tue, 09 Sep 2025 21:10:37 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8e76a566c829fa70a3c0ddb789baae7ecf3b82b6365cda75fc649935c3a3ff4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78103825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f5a3f9b7faa0af5a9bfb182cfed63d2927a01b1650ee53070aee91e6d25a64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.36.2
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478342f3673521ce474529789681e0a1b13cfad57c81eb3f3ef521a7fdeaf83d`  
		Last Modified: Mon, 29 Sep 2025 20:04:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd33640a76eefaa3b65db81ca4f6c4860eb0e4b5abd4019fdf0d7e0c685a9689`  
		Last Modified: Mon, 29 Sep 2025 20:04:12 GMT  
		Size: 2.6 MB (2616107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e3bc9fdd7eb4d762c1c7e6bfc0a0f19abe5617c73b3afdedb870d2158eae02`  
		Last Modified: Mon, 29 Sep 2025 20:04:22 GMT  
		Size: 71.4 MB (71356070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64df0f28a68d54b5492b00273c7e26626b204b866bf3ed18cb4c5f5a281a5825`  
		Last Modified: Mon, 29 Sep 2025 20:04:08 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:70ce115fd0ab7907a509734b83b729101b64319e1a782e115b96adcb3acfc151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1149451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d083ca1f53da5b3e3db8e63032173d0dd27c8a140c7fb1ff9a152688f2846f71`

```dockerfile
```

-	Layers:
	-	`sha256:08cd96849dc563c9588374bc84324df94c28e852cbcee02f9c60cc59fe685e20`  
		Last Modified: Mon, 29 Sep 2025 21:11:10 GMT  
		Size: 1.1 MB (1134066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f47d66aa3bc216f253542b9e87847540adf890bd032a1cb2303abd547996428`  
		Last Modified: Mon, 29 Sep 2025 21:11:11 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:cf14507fc088bba807d9b4ab2597fb40f74f62f9c645a84ecb0e99869e67ee0c
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
$ docker pull telegraf@sha256:09efd7277e074e14f58b6aa50cd107c8abbe6898aa2c2b9029b647bf3fc60fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171241057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:360e8b4feb461261003f6e94145404dea824e7d2d377a10f73c907879a6d8e09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
ENV TELEGRAF_VERSION=1.36.1
# Tue, 09 Sep 2025 01:37:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Sep 2025 01:37:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 01:37:08 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d1a0f1ddd0803d51fc5f5e8d035ed9a04f06bd2551fff5d94ae9d975432043`  
		Last Modified: Tue, 09 Sep 2025 18:16:58 GMT  
		Size: 18.9 MB (18942917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34061fc6be711b5b2ce5fc1c01a7957a0185335d4f3a072ca25ff5d71720d1c0`  
		Last Modified: Tue, 09 Sep 2025 18:16:57 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35e6b83a3d36081bbc656e054ae64c8f27682b2e806fa1017ce19ca3d4cd491`  
		Last Modified: Tue, 09 Sep 2025 18:17:07 GMT  
		Size: 79.8 MB (79789123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a12c0b1ff0f0351a224730958090f2affd58e5f8240144929ba6a35ead76df`  
		Last Modified: Tue, 09 Sep 2025 18:16:57 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:7771fe69ee44718411df1cdca9e3a15916321f1f1c63238642f96214060bc016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6661775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7fb2ab2239ee79cb670069fc8c329b36181567c19380d1a18c50f8badbced1`

```dockerfile
```

-	Layers:
	-	`sha256:a9aeb94991521f1fa2b26acae8b4ad303da7a09962a20ec3aaf10189f2426ed7`  
		Last Modified: Tue, 09 Sep 2025 21:10:29 GMT  
		Size: 6.6 MB (6647004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec01a023330011a1460d6bbff15171bbc3c3dae60bf4545430b933e395e2130d`  
		Last Modified: Tue, 09 Sep 2025 21:10:30 GMT  
		Size: 14.8 KB (14771 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:47b7cf4918ba95e369b819d425d382bafeb3891f85d0b200739f2263c9e2a04f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157635396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f38dac53bd952e7345f4da097568b7ce44e564f68b60cfe64c96c86c1e9ace1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.36.2
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dc4168cb25b55b5cbdedf9511df1cbef908c557840783f9965c3305c8054a6`  
		Last Modified: Mon, 29 Sep 2025 20:04:10 GMT  
		Size: 17.7 MB (17722606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8a3e6793d72d75d4183a83070b45281e8de226228b46b444efb02e7c60e165`  
		Last Modified: Mon, 29 Sep 2025 20:04:09 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcc5c2a03ead4e05a39572278e5fc3e0971bbdad892d18dbecc793ab09e3df1`  
		Last Modified: Mon, 29 Sep 2025 20:04:38 GMT  
		Size: 73.8 MB (73781640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546c32e0fd3be9b4ace9f1a772d18bc3deeb968927a39f17baebfb2f8497ced0`  
		Last Modified: Mon, 29 Sep 2025 20:04:32 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:5a678d2ca71996bed4a0eac1c6bf23e40de9a7bc1ca2afacc654135478624df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6661453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18df71b3865865e04ed03947cd0add0fa78eac0af1a584e6e20309b78cdd8995`

```dockerfile
```

-	Layers:
	-	`sha256:b6f3539c45f9147b7e9b404ed5508c4539d5b84fe061da2c2377b554482defa8`  
		Last Modified: Mon, 29 Sep 2025 21:11:10 GMT  
		Size: 6.6 MB (6646583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d661fc2bdbd8be2674af91da8a1777c5c4e9084b90b2d80aeb12322339ad456e`  
		Last Modified: Mon, 29 Sep 2025 21:11:11 GMT  
		Size: 14.9 KB (14870 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5008708de5ea25fb22009e01875963707a3ea95f72430173a21dda0bebb559e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162400874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cab57a13f6a864f609b2e9b039d2bf69374f8014daa50e63aff12f25622bc97`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.36.2
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed67e27f81fe86d6b042c6a6b65e21ad8b606b040ff540bf83e62f61ca44f97`  
		Last Modified: Mon, 29 Sep 2025 20:09:13 GMT  
		Size: 18.9 MB (18884201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c011997a0b2aeaae8fe9b40ac5ff95e698b3bddfa9302d53ffcf72e33386e58f`  
		Last Modified: Mon, 29 Sep 2025 20:09:12 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc86dff5cbd5a940b8dd231af96ff7e0ca52d7a881185f1f89415984bd8b422`  
		Last Modified: Mon, 29 Sep 2025 20:09:17 GMT  
		Size: 71.6 MB (71558800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0ee1630ffd40588db8f671a7f705d33f26ac046579135282119b89b025a933`  
		Last Modified: Mon, 29 Sep 2025 20:09:13 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:9e9ae8848ca744f5cf3c89bb0cbf2aed72e6df137daa73cc9c503548c0ffb7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6667560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0bf7181961c80924da12c1c78eebf6791cb3b50a7382594ec6efbabcc6f198e`

```dockerfile
```

-	Layers:
	-	`sha256:2bc796c7f2841ce6c35b8f6e261f1accb7c8f0e539ea3264db317bd0a042c156`  
		Last Modified: Mon, 29 Sep 2025 21:11:16 GMT  
		Size: 6.7 MB (6652666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a6d1548f9bdad55b659b7e51c03f2d6f72570d137b8645225a5b6abd039a6fd`  
		Last Modified: Mon, 29 Sep 2025 21:11:17 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
