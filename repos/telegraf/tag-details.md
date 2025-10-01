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
$ docker pull telegraf@sha256:ecb51879e1c72489bb3758411ad64320a390d8a03dcdbcc9bfaaa6d72ad2627a
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
$ docker pull telegraf@sha256:c8f235994359365f738e3d0a800c20c7aac263cef5b59dda64d2b946f8267791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168899640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa093a5ee1d003efd400d3ab488885ae83bf2a3ab240299a334ffc1422cf18bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704693836433c5fc060b14707abb300b9669d85e84b8629466ad2f5239f96544`  
		Last Modified: Tue, 30 Sep 2025 03:32:02 GMT  
		Size: 18.9 MB (18942900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10f91eb1a6da86001f0ef64968c93a7bbe1370eb2102039f22d275fa6f87ae6`  
		Last Modified: Tue, 30 Sep 2025 03:32:00 GMT  
		Size: 3.4 KB (3442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730b4ddbfe8952a6be9adf1ffdd98dd2afa0704442d14bb968bd58a3aad82e59`  
		Last Modified: Tue, 30 Sep 2025 03:32:12 GMT  
		Size: 77.4 MB (77446241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0610bd2a869ce63aa8ef14a6cf233bbb6a5d0d64620ad444b078947b65008b2`  
		Last Modified: Tue, 30 Sep 2025 03:32:00 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:88d4246f92c70beb7bd701c55188bffaff340b9547b931196f6e2542929569b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a6495939f37b373b36168cd4521f2bd139dd73f34d26e9d3ee7e2f0d55693d`

```dockerfile
```

-	Layers:
	-	`sha256:f34d30ad1bb78fb744341c06ca2b67c8f8b6426ddaaf39f1f62c3918bf7bf5ec`  
		Last Modified: Tue, 30 Sep 2025 21:10:19 GMT  
		Size: 6.6 MB (6630220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14384be44a90e8a65430d9c0fc183ba0de11f240b3c1da6311538bf310cea1c1`  
		Last Modified: Tue, 30 Sep 2025 21:10:19 GMT  
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
$ docker pull telegraf@sha256:416c5bd2bbfdb5f32fb499cd0fc89ecca7bfd389a3493500b3c38dedd77ea428
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:a89bc7ffdbef167a327b58ace97578a6a9e9e276d11154170d67070da85b375e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83297852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4db5e150e9290289636cf093450917d430adf382e5080ff52d44c2798ff08a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
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
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d610c1d9a5e45a7a26b07fdf443b5eefeffe225cf7319bb5d2a09f64d9580ac`  
		Last Modified: Mon, 29 Sep 2025 22:00:33 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508a19720aac03e7d12041162a7c63361474a3ad3b3444b3591721fc4daacc93`  
		Last Modified: Mon, 29 Sep 2025 22:00:36 GMT  
		Size: 2.4 MB (2439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed6b57f80c90e4701bd23dff2c08c21829e429fbe924997bf3200d9951ceef8`  
		Last Modified: Tue, 30 Sep 2025 00:13:07 GMT  
		Size: 77.2 MB (77236902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d48b8ba599e1cdca477a3f87208239039469f1865d2887461c85413d5351de`  
		Last Modified: Mon, 29 Sep 2025 22:00:50 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9bec9ecc3ca56738c5844f6746e8e5d50a20bf56a778813814541ca567f099d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1115136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4868df07db4d82c66d9c0af956b3722684c09ec3105d059d66507700277f91e5`

```dockerfile
```

-	Layers:
	-	`sha256:a210f259ca6f0690a3d798095ef3ba253ad25686c5d60a99905327f1856c5178`  
		Last Modified: Tue, 30 Sep 2025 00:10:23 GMT  
		Size: 1.1 MB (1100176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e97176ca55880ed9fde28f2d7786ef35acb158f396a3a53ef48ccaa2795ec33`  
		Last Modified: Tue, 30 Sep 2025 00:10:24 GMT  
		Size: 15.0 KB (14960 bytes)  
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
$ docker pull telegraf@sha256:cda342c630af551b162dc9d9fb6b460e9996725593d9874f05913193d0642fa8
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
$ docker pull telegraf@sha256:07b18889de77916e91f89ab129ccf8b7695bc430c1d5374d824c33143b84f27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168899719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2357a0788fbb3e93b066057b3dd3b20f78081345e2c8b2f22e5ec9213d33b492`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e939fd554de58bcaac4d28ca00ddb5de8f4459df3c5cea76d0be9bb768cc6dec`  
		Last Modified: Mon, 29 Sep 2025 21:48:24 GMT  
		Size: 18.9 MB (18942854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efac14c456ae320dc857040cd81a6eada97f1fd3876863de73d38aed7883b43e`  
		Last Modified: Mon, 29 Sep 2025 21:48:20 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c288f50a94d04ac661ee78e356470a98f2a3f44f6b5db8de36367d4d1126279a`  
		Last Modified: Mon, 29 Sep 2025 21:48:35 GMT  
		Size: 77.4 MB (77446194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1807a9b66143f6c1ad21aca084d9b87b9bb4776df23442449b6cafb89cdac0e9`  
		Last Modified: Mon, 29 Sep 2025 21:48:21 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:1fc3a850f3ea660ede89b67c8d540818d15ccd6504bf2b056c45e43b63d3b6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3f4534f2c86238ceada9a423c7dff2b5d630a46e93effad190018648a552ba`

```dockerfile
```

-	Layers:
	-	`sha256:d1e278a76fc12119d6a761348a2e66fc28904ddc2a6f053d4579c3876c94ef37`  
		Last Modified: Tue, 30 Sep 2025 00:10:21 GMT  
		Size: 6.6 MB (6630220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4a85b9e188109f2573bfcd59b34dd63367f7906830aacc1e8dc9f61203527c7`  
		Last Modified: Tue, 30 Sep 2025 00:10:22 GMT  
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
$ docker pull telegraf@sha256:416c5bd2bbfdb5f32fb499cd0fc89ecca7bfd389a3493500b3c38dedd77ea428
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:a89bc7ffdbef167a327b58ace97578a6a9e9e276d11154170d67070da85b375e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83297852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4db5e150e9290289636cf093450917d430adf382e5080ff52d44c2798ff08a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
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
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d610c1d9a5e45a7a26b07fdf443b5eefeffe225cf7319bb5d2a09f64d9580ac`  
		Last Modified: Mon, 29 Sep 2025 22:00:33 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508a19720aac03e7d12041162a7c63361474a3ad3b3444b3591721fc4daacc93`  
		Last Modified: Mon, 29 Sep 2025 22:00:36 GMT  
		Size: 2.4 MB (2439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed6b57f80c90e4701bd23dff2c08c21829e429fbe924997bf3200d9951ceef8`  
		Last Modified: Tue, 30 Sep 2025 00:13:07 GMT  
		Size: 77.2 MB (77236902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d48b8ba599e1cdca477a3f87208239039469f1865d2887461c85413d5351de`  
		Last Modified: Mon, 29 Sep 2025 22:00:50 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9bec9ecc3ca56738c5844f6746e8e5d50a20bf56a778813814541ca567f099d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1115136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4868df07db4d82c66d9c0af956b3722684c09ec3105d059d66507700277f91e5`

```dockerfile
```

-	Layers:
	-	`sha256:a210f259ca6f0690a3d798095ef3ba253ad25686c5d60a99905327f1856c5178`  
		Last Modified: Tue, 30 Sep 2025 00:10:23 GMT  
		Size: 1.1 MB (1100176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e97176ca55880ed9fde28f2d7786ef35acb158f396a3a53ef48ccaa2795ec33`  
		Last Modified: Tue, 30 Sep 2025 00:10:24 GMT  
		Size: 15.0 KB (14960 bytes)  
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
$ docker pull telegraf@sha256:4ce17d86058f6e5032936319ddccb562c80cc77c4975fb8ce07d8f3424ab5dae
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
$ docker pull telegraf@sha256:ef6946d7c6284727f7651678cf407bb6b6ad9d784ecfcb17ca066b7bda7121e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171024116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b89732389e6ab347c66a997bef286367b1ad52ef8ae10b54324b01d96aa5c41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905a538f3072339dd80ad1dcd9203d1de20aad468fdfd7531aef312af27fa1b4`  
		Last Modified: Tue, 30 Sep 2025 03:32:28 GMT  
		Size: 18.9 MB (18942952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba6a09d6603897420ff6f2c67250dfed683b097e71ae77c3147d734ae961555`  
		Last Modified: Tue, 30 Sep 2025 03:32:24 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa53f0d38866b96f79c95b59950fd004fce4f75f5b676b5cbe7e310b296e6211`  
		Last Modified: Tue, 30 Sep 2025 03:32:38 GMT  
		Size: 79.6 MB (79570668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec016cf57451412d011eae5c04f1ebe52e9b0205f57b08bcc502bc909bb166a7`  
		Last Modified: Tue, 30 Sep 2025 03:32:24 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:9a5f40cbcc5fbbf45374164037be274a961f515996f7788e2f83dfb6d3fd6b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6659415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb52bdea623aa2fead3af1ec3f2d7b5f744b0fc9978e353dcf9a0e7fee6fb444`

```dockerfile
```

-	Layers:
	-	`sha256:a4576b8a7d546d86c785525ddb5c77629660f6e2507634960a75182dc0ca0174`  
		Last Modified: Tue, 30 Sep 2025 21:10:27 GMT  
		Size: 6.6 MB (6644946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:249199bf90aedf7d9fd21123765c62dffee7881bc6d01102a654f756d92484e0`  
		Last Modified: Tue, 30 Sep 2025 21:10:28 GMT  
		Size: 14.5 KB (14469 bytes)  
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
$ docker pull telegraf@sha256:79c210c753acc507409c498f9065f7b790d1cd232caae3f4264c2ef44585e596
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c366265ce878c9599b4aa58cdf539ecea3bf67782021fecd5f2e85ee0436a618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85721200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f0203159b23744b2665b74836a487193df1dd0bf6260320841f84b2338b629`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c541f94d6a93453872065bc238d1ec99c7499f029c11f038bcfa7d24e4cce6`  
		Last Modified: Mon, 29 Sep 2025 21:50:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaae0607e1fa6c8525a473e315d9cac5aba7bfc33892b0297ee59aa9a6203d12`  
		Last Modified: Mon, 29 Sep 2025 21:50:05 GMT  
		Size: 2.6 MB (2552125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e170152b00900e68f5f25c33c37fa7a843d69b9df891271bcb9b9541b0f285`  
		Last Modified: Mon, 29 Sep 2025 21:50:16 GMT  
		Size: 79.4 MB (79368489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6ac488b3539456cb82aa7308743e86fe1c639b8a32f972a290e2ec7ffa28ed`  
		Last Modified: Mon, 29 Sep 2025 21:50:05 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:2f29504fd8b7523ed2299c9433e6631e1c3cd5a94450cf6798303689eb83f53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1146356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c5dc401cc5c0cf45c0ae4b79bbcdeaa5d7d368bbfc3fb07cba14d48a73913f`

```dockerfile
```

-	Layers:
	-	`sha256:d31efd39957cae8129617b6628fd369dcb6d17b85dd5f3f36f5d3556a3e68398`  
		Last Modified: Tue, 30 Sep 2025 00:10:41 GMT  
		Size: 1.1 MB (1131395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eefc1ac59c8f2d1c8bfb63ecdd04ef3925885acf53133853d4735da2c1a7af0`  
		Last Modified: Tue, 30 Sep 2025 00:10:41 GMT  
		Size: 15.0 KB (14961 bytes)  
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
$ docker pull telegraf@sha256:ba18057364e4d41a9651ebbc880a2732b3eee50c2a93ffcc71f10fb8840a9d9d
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
$ docker pull telegraf@sha256:cea5d08bf3381da63ca094c669ec8a8b9ae883646f95f8dbd631d387dabbeac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171024205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac05e712d6ddbad963bf6a60cc1e8b790e83f220f3aef0538c6328d905ab479`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e939fd554de58bcaac4d28ca00ddb5de8f4459df3c5cea76d0be9bb768cc6dec`  
		Last Modified: Mon, 29 Sep 2025 21:48:24 GMT  
		Size: 18.9 MB (18942854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efac14c456ae320dc857040cd81a6eada97f1fd3876863de73d38aed7883b43e`  
		Last Modified: Mon, 29 Sep 2025 21:48:20 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8658a5ce9063c5c5ecb4030afa8cd248978a5d9b7def7918afdbd7552d2c564b`  
		Last Modified: Mon, 29 Sep 2025 21:49:17 GMT  
		Size: 79.6 MB (79570681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab0f3da3d72bfafb62fee0529a959d5e21737d8703642c6fee9b851e8dcefab`  
		Last Modified: Mon, 29 Sep 2025 21:49:10 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:fa8c8067b7b611f43f8891e52ae0f125639dc3fea5bd20b390c5d4e5dec03055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6659416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41748e6b691f590d2f506ab79a6791a82348f9fe0de92fba2c1b80bb177136e`

```dockerfile
```

-	Layers:
	-	`sha256:986dc6b84b984f0a021e6e345154ea3eed6fbf58b29944c0607767866f291103`  
		Last Modified: Tue, 30 Sep 2025 00:10:34 GMT  
		Size: 6.6 MB (6644946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dd930d9d4116259e7d4610592825bc0a516c2a8eeddc2dbbfd06b9485cf6cc3`  
		Last Modified: Tue, 30 Sep 2025 00:10:35 GMT  
		Size: 14.5 KB (14470 bytes)  
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
$ docker pull telegraf@sha256:79c210c753acc507409c498f9065f7b790d1cd232caae3f4264c2ef44585e596
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c366265ce878c9599b4aa58cdf539ecea3bf67782021fecd5f2e85ee0436a618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85721200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f0203159b23744b2665b74836a487193df1dd0bf6260320841f84b2338b629`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c541f94d6a93453872065bc238d1ec99c7499f029c11f038bcfa7d24e4cce6`  
		Last Modified: Mon, 29 Sep 2025 21:50:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaae0607e1fa6c8525a473e315d9cac5aba7bfc33892b0297ee59aa9a6203d12`  
		Last Modified: Mon, 29 Sep 2025 21:50:05 GMT  
		Size: 2.6 MB (2552125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e170152b00900e68f5f25c33c37fa7a843d69b9df891271bcb9b9541b0f285`  
		Last Modified: Mon, 29 Sep 2025 21:50:16 GMT  
		Size: 79.4 MB (79368489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6ac488b3539456cb82aa7308743e86fe1c639b8a32f972a290e2ec7ffa28ed`  
		Last Modified: Mon, 29 Sep 2025 21:50:05 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:2f29504fd8b7523ed2299c9433e6631e1c3cd5a94450cf6798303689eb83f53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1146356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c5dc401cc5c0cf45c0ae4b79bbcdeaa5d7d368bbfc3fb07cba14d48a73913f`

```dockerfile
```

-	Layers:
	-	`sha256:d31efd39957cae8129617b6628fd369dcb6d17b85dd5f3f36f5d3556a3e68398`  
		Last Modified: Tue, 30 Sep 2025 00:10:41 GMT  
		Size: 1.1 MB (1131395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eefc1ac59c8f2d1c8bfb63ecdd04ef3925885acf53133853d4735da2c1a7af0`  
		Last Modified: Tue, 30 Sep 2025 00:10:41 GMT  
		Size: 15.0 KB (14961 bytes)  
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
$ docker pull telegraf@sha256:f1b19855570be26a9fb3d35cee7790ba57f73387f69be1b9ecd2d97bbc72e437
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
$ docker pull telegraf@sha256:ec8ee87b8be2c670115ff1254f6a228c063488cb93ecce79f015e3f86297c732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171667859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e538c6c58ae8f1a857814625d53e4f4f768e84c10f1fdeaf17b87fe2a12e8f66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a64992b4a12cf46a1c333ddf70c3e1f104aada157bc49d0631c9dc0602d0a0`  
		Last Modified: Tue, 30 Sep 2025 21:16:05 GMT  
		Size: 18.9 MB (18942836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464069bfa65a76b221fe94d5910c40e27cad4e9ac5c384caf7efacb22d7fdeb7`  
		Last Modified: Tue, 30 Sep 2025 04:03:58 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c8b3704935fcab33fd2329cb47373fc10d2fdc75dff89f73b393fc975ea4a6`  
		Last Modified: Tue, 30 Sep 2025 21:16:10 GMT  
		Size: 80.2 MB (80214516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3cd8d77696a4ab053da7a9b245d403d5ca9eb44eb44ace76a85e306cd714f1`  
		Last Modified: Tue, 30 Sep 2025 04:03:57 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:d3332118cc2ce3f9ffaa1274bae1dcefcf610cb2cd205205490bb96d1bdd843a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85d71734bd0510616dfc7dc4e1da63fe87c43553d6ef96f40b12af4f71eb4e6`

```dockerfile
```

-	Layers:
	-	`sha256:85e5a6a527f19517ef9674c580040ef0023db1fe3b3e824626338cc6850be99c`  
		Last Modified: Tue, 30 Sep 2025 21:10:34 GMT  
		Size: 6.7 MB (6651978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5ac0e3774170443b87f9ff22ee0074a70fdba5500e675aebf41a1700df27699`  
		Last Modified: Tue, 30 Sep 2025 21:10:35 GMT  
		Size: 14.8 KB (14772 bytes)  
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
$ docker pull telegraf@sha256:ea80726b07338a48e44c6fb8a3a3223d7ef818f5490a090eb3aada106a8f150f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:4fbed4e06e5df544ed529383ec35e53bae0f341e54f63fb31d8ac963eeb81e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86359024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ed2baf78c6fdeb2376ecd9f4e5cdbf40f7a8d8a317ddc70d238162ff0856cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7b1d485f9659a78600f888324852b1f5a26b04a2c0c0f330a612bb8fdba2ca`  
		Last Modified: Mon, 29 Sep 2025 21:50:28 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81390e055f00a320259d4d1b3d76cd52aa054e49e8b77a0e2cf92d880f9c8a30`  
		Last Modified: Mon, 29 Sep 2025 21:50:29 GMT  
		Size: 2.6 MB (2552110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb256e183b2e4e5ed2d9dd2497551fc87241a7ac9c0a1a45d36fb9786bad3f2`  
		Last Modified: Mon, 29 Sep 2025 21:50:33 GMT  
		Size: 80.0 MB (80006327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2270c8c1f9cdd658e2720692e195609df809cb96c0787ecdca0fef2453ba9933`  
		Last Modified: Mon, 29 Sep 2025 21:50:28 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:456bd4ad67a437a52e7e6bd403a025e5b00cd41e442dfdb7a405847c320be693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1153690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4ffce3790929d52a085a6730bf36c216aa61c0bd96483a876a8855dc087d64`

```dockerfile
```

-	Layers:
	-	`sha256:916ab854da1fc6926d8d213652218cd590767a08a4cb159d6be59e4647a5a831`  
		Last Modified: Tue, 30 Sep 2025 00:10:54 GMT  
		Size: 1.1 MB (1138427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbde52daa903888bd5b2d7d01c85d8b3d6af175fc7b562e4915222eb79c2ab1a`  
		Last Modified: Tue, 30 Sep 2025 00:10:55 GMT  
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
$ docker pull telegraf@sha256:eebf1f376c354fc9491bfd7f4715f471072c79c6e8e78ec9b67f831b1b984232
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.2` - linux; amd64

```console
$ docker pull telegraf@sha256:e9c5c8047d591a2eadef96d5d537e764845ee7793bcd1d2671734230073c1aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171668031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a6ddbb25b6e0e7a2c467b01ef8eaad1ea24c24afecc4e175add14e3c106f93`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b0b371baff5a92fcc4cff34c1943477157122a17cc504aa39afe355be62d52`  
		Last Modified: Mon, 29 Sep 2025 21:51:09 GMT  
		Size: 18.9 MB (18942885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49235a08758f6b0f5453a5f1de9aefa77e9fa9cb6d985aa4c1302546bc3b1ea0`  
		Last Modified: Mon, 29 Sep 2025 21:51:04 GMT  
		Size: 3.4 KB (3442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553326328f7b4ffc5cfaab954a4bfd5831063d8ffa16b918db209f41ba5c926e`  
		Last Modified: Mon, 29 Sep 2025 21:51:15 GMT  
		Size: 80.2 MB (80214474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545d43f9992d57bbaade53f5589e67aa467591b3668f70416be82c33664848b6`  
		Last Modified: Mon, 29 Sep 2025 21:51:04 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:50c99492a64009b77fc8f105f4596e915aa904dd16b13bba200aee890d61f6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d773dd7401ac17a45adc905ad8211778461cc101df9c0608cd07aacc3e944498`

```dockerfile
```

-	Layers:
	-	`sha256:fa813155f7cd0836958d0a5066edf7bb667207fc6bf5ddf40da23ebe74e633ce`  
		Last Modified: Tue, 30 Sep 2025 00:10:52 GMT  
		Size: 6.7 MB (6651978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cf5214c4c16f0e1fde24a3855652fdeb4e8fa080c24588b9ded4d8edbe3b7aa`  
		Last Modified: Tue, 30 Sep 2025 00:10:53 GMT  
		Size: 14.8 KB (14771 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull telegraf@sha256:ea80726b07338a48e44c6fb8a3a3223d7ef818f5490a090eb3aada106a8f150f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.2-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:4fbed4e06e5df544ed529383ec35e53bae0f341e54f63fb31d8ac963eeb81e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86359024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ed2baf78c6fdeb2376ecd9f4e5cdbf40f7a8d8a317ddc70d238162ff0856cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7b1d485f9659a78600f888324852b1f5a26b04a2c0c0f330a612bb8fdba2ca`  
		Last Modified: Mon, 29 Sep 2025 21:50:28 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81390e055f00a320259d4d1b3d76cd52aa054e49e8b77a0e2cf92d880f9c8a30`  
		Last Modified: Mon, 29 Sep 2025 21:50:29 GMT  
		Size: 2.6 MB (2552110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb256e183b2e4e5ed2d9dd2497551fc87241a7ac9c0a1a45d36fb9786bad3f2`  
		Last Modified: Mon, 29 Sep 2025 21:50:33 GMT  
		Size: 80.0 MB (80006327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2270c8c1f9cdd658e2720692e195609df809cb96c0787ecdca0fef2453ba9933`  
		Last Modified: Mon, 29 Sep 2025 21:50:28 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.2-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:456bd4ad67a437a52e7e6bd403a025e5b00cd41e442dfdb7a405847c320be693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1153690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4ffce3790929d52a085a6730bf36c216aa61c0bd96483a876a8855dc087d64`

```dockerfile
```

-	Layers:
	-	`sha256:916ab854da1fc6926d8d213652218cd590767a08a4cb159d6be59e4647a5a831`  
		Last Modified: Tue, 30 Sep 2025 00:10:54 GMT  
		Size: 1.1 MB (1138427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbde52daa903888bd5b2d7d01c85d8b3d6af175fc7b562e4915222eb79c2ab1a`  
		Last Modified: Tue, 30 Sep 2025 00:10:55 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull telegraf@sha256:ea80726b07338a48e44c6fb8a3a3223d7ef818f5490a090eb3aada106a8f150f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:4fbed4e06e5df544ed529383ec35e53bae0f341e54f63fb31d8ac963eeb81e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86359024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ed2baf78c6fdeb2376ecd9f4e5cdbf40f7a8d8a317ddc70d238162ff0856cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7b1d485f9659a78600f888324852b1f5a26b04a2c0c0f330a612bb8fdba2ca`  
		Last Modified: Mon, 29 Sep 2025 21:50:28 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81390e055f00a320259d4d1b3d76cd52aa054e49e8b77a0e2cf92d880f9c8a30`  
		Last Modified: Mon, 29 Sep 2025 21:50:29 GMT  
		Size: 2.6 MB (2552110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb256e183b2e4e5ed2d9dd2497551fc87241a7ac9c0a1a45d36fb9786bad3f2`  
		Last Modified: Mon, 29 Sep 2025 21:50:33 GMT  
		Size: 80.0 MB (80006327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2270c8c1f9cdd658e2720692e195609df809cb96c0787ecdca0fef2453ba9933`  
		Last Modified: Mon, 29 Sep 2025 21:50:28 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:456bd4ad67a437a52e7e6bd403a025e5b00cd41e442dfdb7a405847c320be693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1153690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4ffce3790929d52a085a6730bf36c216aa61c0bd96483a876a8855dc087d64`

```dockerfile
```

-	Layers:
	-	`sha256:916ab854da1fc6926d8d213652218cd590767a08a4cb159d6be59e4647a5a831`  
		Last Modified: Tue, 30 Sep 2025 00:10:54 GMT  
		Size: 1.1 MB (1138427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbde52daa903888bd5b2d7d01c85d8b3d6af175fc7b562e4915222eb79c2ab1a`  
		Last Modified: Tue, 30 Sep 2025 00:10:55 GMT  
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
$ docker pull telegraf@sha256:eebf1f376c354fc9491bfd7f4715f471072c79c6e8e78ec9b67f831b1b984232
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
$ docker pull telegraf@sha256:e9c5c8047d591a2eadef96d5d537e764845ee7793bcd1d2671734230073c1aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171668031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a6ddbb25b6e0e7a2c467b01ef8eaad1ea24c24afecc4e175add14e3c106f93`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b0b371baff5a92fcc4cff34c1943477157122a17cc504aa39afe355be62d52`  
		Last Modified: Mon, 29 Sep 2025 21:51:09 GMT  
		Size: 18.9 MB (18942885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49235a08758f6b0f5453a5f1de9aefa77e9fa9cb6d985aa4c1302546bc3b1ea0`  
		Last Modified: Mon, 29 Sep 2025 21:51:04 GMT  
		Size: 3.4 KB (3442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553326328f7b4ffc5cfaab954a4bfd5831063d8ffa16b918db209f41ba5c926e`  
		Last Modified: Mon, 29 Sep 2025 21:51:15 GMT  
		Size: 80.2 MB (80214474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545d43f9992d57bbaade53f5589e67aa467591b3668f70416be82c33664848b6`  
		Last Modified: Mon, 29 Sep 2025 21:51:04 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:50c99492a64009b77fc8f105f4596e915aa904dd16b13bba200aee890d61f6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d773dd7401ac17a45adc905ad8211778461cc101df9c0608cd07aacc3e944498`

```dockerfile
```

-	Layers:
	-	`sha256:fa813155f7cd0836958d0a5066edf7bb667207fc6bf5ddf40da23ebe74e633ce`  
		Last Modified: Tue, 30 Sep 2025 00:10:52 GMT  
		Size: 6.7 MB (6651978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cf5214c4c16f0e1fde24a3855652fdeb4e8fa080c24588b9ded4d8edbe3b7aa`  
		Last Modified: Tue, 30 Sep 2025 00:10:53 GMT  
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
