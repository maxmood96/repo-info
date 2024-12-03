<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.30`](#telegraf130)
-	[`telegraf:1.30-alpine`](#telegraf130-alpine)
-	[`telegraf:1.30.3`](#telegraf1303)
-	[`telegraf:1.30.3-alpine`](#telegraf1303-alpine)
-	[`telegraf:1.31`](#telegraf131)
-	[`telegraf:1.31-alpine`](#telegraf131-alpine)
-	[`telegraf:1.31.3`](#telegraf1313)
-	[`telegraf:1.31.3-alpine`](#telegraf1313-alpine)
-	[`telegraf:1.32`](#telegraf132)
-	[`telegraf:1.32-alpine`](#telegraf132-alpine)
-	[`telegraf:1.32.3`](#telegraf1323)
-	[`telegraf:1.32.3-alpine`](#telegraf1323-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.30`

```console
$ docker pull telegraf@sha256:93d54db3edf69c944eb05b2a1319fbe773f62b51553168f8b82164400c2230b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30` - linux; amd64

```console
$ docker pull telegraf@sha256:e007590796dc930b341f36249052003a1804ef90074946d0db3a22b481fca162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154080006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9fed213aa114dc196fe4cef487e815d7a3e65231cfa5421833b041029e899c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a722c6247548023ea6714fa49f397254bae6cfb600793478c5c09e06b3751422`  
		Last Modified: Tue, 03 Dec 2024 03:24:44 GMT  
		Size: 18.9 MB (18948055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa30e447aaf0f8ce726e9002d01619bf8e1b5a0d5d21b553c8295e00e7a2e0b`  
		Last Modified: Tue, 03 Dec 2024 03:24:43 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1bee74c104df1b2215ee79657dc6e6ceb9d2d275dc5c8bf5a22cdc838b3a9c`  
		Last Modified: Tue, 03 Dec 2024 03:24:44 GMT  
		Size: 62.8 MB (62766455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cdc5aadbb5fdb82dc52bced521da5f9ad2cb6ee2c97b4033f59736b393fad6`  
		Last Modified: Tue, 03 Dec 2024 03:24:43 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:2539177a6701b257e61a9251ed9b25fa1c4fc4be27234978d1ea83376c152f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6423605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa6e04e33f091d130f9b42674b1f18c9024189a9a3d90e47b3a25b620178cb8`

```dockerfile
```

-	Layers:
	-	`sha256:ffd9351baaa984274bac98af252b8456f9c87ac6f192f3fd36d279138eadb9af`  
		Last Modified: Tue, 03 Dec 2024 03:24:43 GMT  
		Size: 6.4 MB (6409135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6faf3487ae90087f077bd90e5ca68428e24576953f45fcfdb0c8bce0680e6ef`  
		Last Modified: Tue, 03 Dec 2024 03:24:43 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:d11b10d7b351b4bd42182715e69cca4b25d230451fd8888ea26bd9caf485a5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143050971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6599186a260e8b0083de68faa2787bc6efa7b726fadb6a1ada72305ecb9ce0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c1519b04115013f7821f6b8398475148c7865994c7c5de2fb71d5916d5fb2e`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 17.7 MB (17725323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1859599b084be651ec09e42d0c7674081d74a573bd8eb676cc088609c1a1ed`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee6d626f779b08de0ab57eb59fa02c95c3a7616c6e4a97dd9bdea4bc37de78b`  
		Last Modified: Wed, 13 Nov 2024 10:41:23 GMT  
		Size: 58.2 MB (58212673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39963093867bf859f3e496714bb1d55f3c91fa4b77e31e2d63e9033f4f50bc68`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:ac428f9081d476de7e3f7d360bcf0711162cb812da72359c5c6e9b40603787b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6419578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb06f2040a83751ae0d83c311a5a898c4c8e9ffc624c2b6f805816ea90fdc85`

```dockerfile
```

-	Layers:
	-	`sha256:3f27beb76ecc69497466e4c9cf1043dcba85c26c48d6754df94ef9e1f864b97c`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 6.4 MB (6405022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7320041d6292fa415dec40ea266adf7ef5447eb76ee6bb2ea292cdb310e7e235`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:55017814475516fe305f3d8372c048d4fdd0aeff9afa66d1bb729b80da4f7d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147727540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d62098d8b7a1ba9b660092d18ab794fc260080c864c1bf5d7f13baada1efe01`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82c46aaa37285c7b036e2c06961935d109402757aac6158f08caf19093a766e`  
		Last Modified: Tue, 03 Dec 2024 14:46:53 GMT  
		Size: 18.9 MB (18870397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d3fbbd33a83aef503a229631a61792a552956e729abc4035ad057228a800ba`  
		Last Modified: Tue, 03 Dec 2024 14:46:53 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06c75b4d578764880c581532b28c9c137dc1f89229bafbfabba74ad6ee962cc`  
		Last Modified: Tue, 03 Dec 2024 14:46:55 GMT  
		Size: 57.1 MB (57123255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedc98988743526d425d922c90b18388518b53bf6332746c4b42b6bee7885639`  
		Last Modified: Tue, 03 Dec 2024 14:46:53 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:91e71e3dbea52899efd1804cab0e3a8eef75d784022dee246f2272316eb8cee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6423637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0126499f4c2b3c92989ae8317d5da53d94f8b88d0bfa1d6a3b3de433a5c06551`

```dockerfile
```

-	Layers:
	-	`sha256:337a82403340fc99ae8cdde130bb38a2fe22f9a325e2f9ff77ffdcfd8c7f3ffb`  
		Last Modified: Tue, 03 Dec 2024 14:46:53 GMT  
		Size: 6.4 MB (6409058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d03175b906400cea888b496101a28ce1813b5752c97f6c65e2aa8e526388f733`  
		Last Modified: Tue, 03 Dec 2024 14:46:53 GMT  
		Size: 14.6 KB (14579 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30-alpine`

```console
$ docker pull telegraf@sha256:48b16cd7118777f0f1bfbf1646e1361f86617940bf8be0f78a8f38b38f559d38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:d1fe88cff6f1f352b943b18a696b82f02f51b0c6cf6ef6f0f8ac06767c1aba32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68637840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5e575a5e5a70553ec5d58132072558a1f2a4f93eacf2c851b9e87044e8531d`
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
ENV TELEGRAF_VERSION=1.30.3
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
	-	`sha256:f26c83f64ca1456198e770c389b38e5bf8c9e65836f4618a54a974e411188638`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974bbb85e144ad54cca7dc47f8bb42c769d38b56729a078fe026f811498268fb`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 2.4 MB (2444834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45ebb412048f7665bc09f61be06e91c3bba493788205109742894989302ec21`  
		Last Modified: Tue, 12 Nov 2024 02:21:06 GMT  
		Size: 62.6 MB (62568494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70ab24ace3340ea55807f383962096485bd4b7d97294db29be4974593a11997`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4d1f2b2431200e7ea650df7ca3503ac7c776c116468c7d8b4c24cd3a1f22191e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1071366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308834af1822db8b6728b0a622602d025641dc2c956b8ba8ccbdb6b9575572c7`

```dockerfile
```

-	Layers:
	-	`sha256:a39b74605b0de8f0c7dffc4a9341b56a5e25959232ded52dda115dd0da436a6e`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 1.1 MB (1056405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fdfb4fd65fb42e643e34090b6fd02f342d53162daa4374e0ab66ebc5132de74`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:aa8942ae1c5553ceac2e04ea1f21939261f63205249a62e2b3c04e3fb7bc14d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63540183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a25b84a9e7b00a3db8f63063a3158b5d7fa3b6a45e1e7591e1b592c9ebfb4c`
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
ENV TELEGRAF_VERSION=1.30.3
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
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
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
	-	`sha256:5fda24d53e12767920ea59e84b53c365e01b3b29f4988df7f2e8a669b5411862`  
		Last Modified: Wed, 13 Nov 2024 00:44:20 GMT  
		Size: 56.9 MB (56921187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db666f85d9bf6e47b56332381281f973a63eb2e75f216da6c7de966ab6b3ccf`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8c63a415f442175dc0ac4d407d716e7e15c2839daedbba06a0cf1c5fbba42d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1066346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f023ae63c182c047e5e162572d71a566b408affba4667ae76c4458764d659e63`

```dockerfile
```

-	Layers:
	-	`sha256:ca8e82b4ad234fde2144ac752875f5f4e2624ca01398237dd917456fa3876a45`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 1.1 MB (1051275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e884945c1eedf9b90e6c05f951a12c4509d27fa03085eababc577b6919684f86`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30.3`

```console
$ docker pull telegraf@sha256:93d54db3edf69c944eb05b2a1319fbe773f62b51553168f8b82164400c2230b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30.3` - linux; amd64

```console
$ docker pull telegraf@sha256:e007590796dc930b341f36249052003a1804ef90074946d0db3a22b481fca162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154080006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9fed213aa114dc196fe4cef487e815d7a3e65231cfa5421833b041029e899c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a722c6247548023ea6714fa49f397254bae6cfb600793478c5c09e06b3751422`  
		Last Modified: Tue, 03 Dec 2024 03:24:44 GMT  
		Size: 18.9 MB (18948055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa30e447aaf0f8ce726e9002d01619bf8e1b5a0d5d21b553c8295e00e7a2e0b`  
		Last Modified: Tue, 03 Dec 2024 03:24:43 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1bee74c104df1b2215ee79657dc6e6ceb9d2d275dc5c8bf5a22cdc838b3a9c`  
		Last Modified: Tue, 03 Dec 2024 03:24:44 GMT  
		Size: 62.8 MB (62766455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cdc5aadbb5fdb82dc52bced521da5f9ad2cb6ee2c97b4033f59736b393fad6`  
		Last Modified: Tue, 03 Dec 2024 03:24:43 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:2539177a6701b257e61a9251ed9b25fa1c4fc4be27234978d1ea83376c152f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6423605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa6e04e33f091d130f9b42674b1f18c9024189a9a3d90e47b3a25b620178cb8`

```dockerfile
```

-	Layers:
	-	`sha256:ffd9351baaa984274bac98af252b8456f9c87ac6f192f3fd36d279138eadb9af`  
		Last Modified: Tue, 03 Dec 2024 03:24:43 GMT  
		Size: 6.4 MB (6409135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6faf3487ae90087f077bd90e5ca68428e24576953f45fcfdb0c8bce0680e6ef`  
		Last Modified: Tue, 03 Dec 2024 03:24:43 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:d11b10d7b351b4bd42182715e69cca4b25d230451fd8888ea26bd9caf485a5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143050971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6599186a260e8b0083de68faa2787bc6efa7b726fadb6a1ada72305ecb9ce0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c1519b04115013f7821f6b8398475148c7865994c7c5de2fb71d5916d5fb2e`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 17.7 MB (17725323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1859599b084be651ec09e42d0c7674081d74a573bd8eb676cc088609c1a1ed`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee6d626f779b08de0ab57eb59fa02c95c3a7616c6e4a97dd9bdea4bc37de78b`  
		Last Modified: Wed, 13 Nov 2024 10:41:23 GMT  
		Size: 58.2 MB (58212673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39963093867bf859f3e496714bb1d55f3c91fa4b77e31e2d63e9033f4f50bc68`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:ac428f9081d476de7e3f7d360bcf0711162cb812da72359c5c6e9b40603787b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6419578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb06f2040a83751ae0d83c311a5a898c4c8e9ffc624c2b6f805816ea90fdc85`

```dockerfile
```

-	Layers:
	-	`sha256:3f27beb76ecc69497466e4c9cf1043dcba85c26c48d6754df94ef9e1f864b97c`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 6.4 MB (6405022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7320041d6292fa415dec40ea266adf7ef5447eb76ee6bb2ea292cdb310e7e235`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:55017814475516fe305f3d8372c048d4fdd0aeff9afa66d1bb729b80da4f7d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147727540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d62098d8b7a1ba9b660092d18ab794fc260080c864c1bf5d7f13baada1efe01`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82c46aaa37285c7b036e2c06961935d109402757aac6158f08caf19093a766e`  
		Last Modified: Tue, 03 Dec 2024 14:46:53 GMT  
		Size: 18.9 MB (18870397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d3fbbd33a83aef503a229631a61792a552956e729abc4035ad057228a800ba`  
		Last Modified: Tue, 03 Dec 2024 14:46:53 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06c75b4d578764880c581532b28c9c137dc1f89229bafbfabba74ad6ee962cc`  
		Last Modified: Tue, 03 Dec 2024 14:46:55 GMT  
		Size: 57.1 MB (57123255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedc98988743526d425d922c90b18388518b53bf6332746c4b42b6bee7885639`  
		Last Modified: Tue, 03 Dec 2024 14:46:53 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:91e71e3dbea52899efd1804cab0e3a8eef75d784022dee246f2272316eb8cee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6423637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0126499f4c2b3c92989ae8317d5da53d94f8b88d0bfa1d6a3b3de433a5c06551`

```dockerfile
```

-	Layers:
	-	`sha256:337a82403340fc99ae8cdde130bb38a2fe22f9a325e2f9ff77ffdcfd8c7f3ffb`  
		Last Modified: Tue, 03 Dec 2024 14:46:53 GMT  
		Size: 6.4 MB (6409058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d03175b906400cea888b496101a28ce1813b5752c97f6c65e2aa8e526388f733`  
		Last Modified: Tue, 03 Dec 2024 14:46:53 GMT  
		Size: 14.6 KB (14579 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30.3-alpine`

```console
$ docker pull telegraf@sha256:48b16cd7118777f0f1bfbf1646e1361f86617940bf8be0f78a8f38b38f559d38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:d1fe88cff6f1f352b943b18a696b82f02f51b0c6cf6ef6f0f8ac06767c1aba32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68637840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5e575a5e5a70553ec5d58132072558a1f2a4f93eacf2c851b9e87044e8531d`
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
ENV TELEGRAF_VERSION=1.30.3
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
	-	`sha256:f26c83f64ca1456198e770c389b38e5bf8c9e65836f4618a54a974e411188638`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974bbb85e144ad54cca7dc47f8bb42c769d38b56729a078fe026f811498268fb`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 2.4 MB (2444834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45ebb412048f7665bc09f61be06e91c3bba493788205109742894989302ec21`  
		Last Modified: Tue, 12 Nov 2024 02:21:06 GMT  
		Size: 62.6 MB (62568494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70ab24ace3340ea55807f383962096485bd4b7d97294db29be4974593a11997`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4d1f2b2431200e7ea650df7ca3503ac7c776c116468c7d8b4c24cd3a1f22191e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1071366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308834af1822db8b6728b0a622602d025641dc2c956b8ba8ccbdb6b9575572c7`

```dockerfile
```

-	Layers:
	-	`sha256:a39b74605b0de8f0c7dffc4a9341b56a5e25959232ded52dda115dd0da436a6e`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 1.1 MB (1056405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fdfb4fd65fb42e643e34090b6fd02f342d53162daa4374e0ab66ebc5132de74`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:aa8942ae1c5553ceac2e04ea1f21939261f63205249a62e2b3c04e3fb7bc14d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63540183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a25b84a9e7b00a3db8f63063a3158b5d7fa3b6a45e1e7591e1b592c9ebfb4c`
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
ENV TELEGRAF_VERSION=1.30.3
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
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
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
	-	`sha256:5fda24d53e12767920ea59e84b53c365e01b3b29f4988df7f2e8a669b5411862`  
		Last Modified: Wed, 13 Nov 2024 00:44:20 GMT  
		Size: 56.9 MB (56921187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db666f85d9bf6e47b56332381281f973a63eb2e75f216da6c7de966ab6b3ccf`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8c63a415f442175dc0ac4d407d716e7e15c2839daedbba06a0cf1c5fbba42d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1066346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f023ae63c182c047e5e162572d71a566b408affba4667ae76c4458764d659e63`

```dockerfile
```

-	Layers:
	-	`sha256:ca8e82b4ad234fde2144ac752875f5f4e2624ca01398237dd917456fa3876a45`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 1.1 MB (1051275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e884945c1eedf9b90e6c05f951a12c4509d27fa03085eababc577b6919684f86`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31`

```console
$ docker pull telegraf@sha256:b44996b117f5d91c491d1e34120a2557cc860a8d5f6d2e1413e8a5694060bf84
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
$ docker pull telegraf@sha256:f90f820e1ac66dee3a2021b1af3a6cdbd3fdd2268e04853e25f25f9940d2b1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157598960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c01145e05d28a42e225f0631fa58d7335623f63c4b5f69dd9fc587717065761`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdde2d05cba99da2e74d73e991ecb82a79bfd76157e4a68b16c077db6065d39e`  
		Last Modified: Tue, 03 Dec 2024 03:24:44 GMT  
		Size: 18.9 MB (18948037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9ad3fec4223bc2bf574eb64f9553bb9fa2e114fe36f2f735f5033f493cf358`  
		Last Modified: Tue, 03 Dec 2024 03:24:44 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2313abe8bd5db514c7915eadb9f3d95df411eda1e8d64c6ab79259f85ce908`  
		Last Modified: Tue, 03 Dec 2024 03:24:45 GMT  
		Size: 66.3 MB (66285441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cf9fc86eed7a55414fd83276295772cf771b843c5a0ebc24141a5c5e6a3e81`  
		Last Modified: Tue, 03 Dec 2024 03:24:44 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:11294cbbbfb6477f27fc39bb164375f034e7aa4145103f960d1f196b0313ddab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6431813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff21b632f27ef2b0ef34dadea4d778750d9b22ce199adb24ed20fda027fe0e3`

```dockerfile
```

-	Layers:
	-	`sha256:e566cd69d2ab26fccface2dc7836f61e03df8b9af8d985c5eac4f4704a78d27d`  
		Last Modified: Tue, 03 Dec 2024 03:24:44 GMT  
		Size: 6.4 MB (6417343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0d300dd93561d3aef0afaf7f2b9b41345a42092f3c6b7acd7385f76b632599`  
		Last Modified: Tue, 03 Dec 2024 03:24:44 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:90babf59ae355dd9ca5289657c8387483c5284a406190467f8d608934b0855e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146510697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce88ea4a0c3e79d65dda7b627957b2a5b84b012a02b4e4bf50bac61256d2925`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c1519b04115013f7821f6b8398475148c7865994c7c5de2fb71d5916d5fb2e`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 17.7 MB (17725323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1859599b084be651ec09e42d0c7674081d74a573bd8eb676cc088609c1a1ed`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5aa14951461d4f24e8fe98880a1cdd3e533b827a78c21ab0b29e418320a334`  
		Last Modified: Wed, 13 Nov 2024 10:42:15 GMT  
		Size: 61.7 MB (61672399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9739370ed5c207a5b6b7db43b0f9c0842fbcd23b76c95fc4621def21308c0e3e`  
		Last Modified: Wed, 13 Nov 2024 10:42:13 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:05584c0701cf4027c88e039d7fe5bd76a64dd18dd3df21edfad122d5b705a046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6428583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5f21606923eb8970e4464c88e6c445a5b20b02e6f592a507b872e03d5c32a2`

```dockerfile
```

-	Layers:
	-	`sha256:8fe419709d841bd11cee70d38e46053dfdcc1a9f95dc2125218f9b4e238ab477`  
		Last Modified: Wed, 13 Nov 2024 10:42:14 GMT  
		Size: 6.4 MB (6414027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff47b9c83c808c9f089467e4bfe9feee8100d1a26f2a5ecbb7430b71c870435b`  
		Last Modified: Wed, 13 Nov 2024 10:42:13 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:deaf87dbc7e2d472c345cec503d2fbf7d7ec05cafd7eb51ac54c20afccc5cbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150982083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aba85cc9fe6bd0a267078be4269c47000f7931428a187f129c1d1d434d119ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82c46aaa37285c7b036e2c06961935d109402757aac6158f08caf19093a766e`  
		Last Modified: Tue, 03 Dec 2024 14:46:53 GMT  
		Size: 18.9 MB (18870397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d3fbbd33a83aef503a229631a61792a552956e729abc4035ad057228a800ba`  
		Last Modified: Tue, 03 Dec 2024 14:46:53 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf045ec18df6cebdfe41d6513c8d4e6c8c9d65f5238d6b4b8b50f594091c6ce`  
		Last Modified: Tue, 03 Dec 2024 14:47:32 GMT  
		Size: 60.4 MB (60377797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922b0d7a6e2a3d4266f6b78fae5b8470fd7d37f1be3a353c17fc489655657c9d`  
		Last Modified: Tue, 03 Dec 2024 14:47:30 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:30902abe5ff47d14c315a9e70f86b75fc71686e479497fdc67c7bb357602f5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6433438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cafe3e1588605acc5e3095d0dace1079639e838ce1dd0064f3a35c59577754`

```dockerfile
```

-	Layers:
	-	`sha256:f4610b4d5c643adc4b245cdd83c5754cf3a5459dad43d4d55165702f798a6f14`  
		Last Modified: Tue, 03 Dec 2024 14:47:30 GMT  
		Size: 6.4 MB (6418858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff519bb59412b621ab9db1a9d1d1e2165be045a8403b71d385abcc0d7f8f222b`  
		Last Modified: Tue, 03 Dec 2024 14:47:30 GMT  
		Size: 14.6 KB (14580 bytes)  
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
		Last Modified: Tue, 12 Nov 2024 02:21:17 GMT  
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
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
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
		Last Modified: Wed, 13 Nov 2024 00:44:56 GMT  
		Size: 15.1 KB (15070 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.3`

```console
$ docker pull telegraf@sha256:b44996b117f5d91c491d1e34120a2557cc860a8d5f6d2e1413e8a5694060bf84
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
$ docker pull telegraf@sha256:f90f820e1ac66dee3a2021b1af3a6cdbd3fdd2268e04853e25f25f9940d2b1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157598960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c01145e05d28a42e225f0631fa58d7335623f63c4b5f69dd9fc587717065761`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdde2d05cba99da2e74d73e991ecb82a79bfd76157e4a68b16c077db6065d39e`  
		Last Modified: Tue, 03 Dec 2024 03:24:44 GMT  
		Size: 18.9 MB (18948037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9ad3fec4223bc2bf574eb64f9553bb9fa2e114fe36f2f735f5033f493cf358`  
		Last Modified: Tue, 03 Dec 2024 03:24:44 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2313abe8bd5db514c7915eadb9f3d95df411eda1e8d64c6ab79259f85ce908`  
		Last Modified: Tue, 03 Dec 2024 03:24:45 GMT  
		Size: 66.3 MB (66285441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cf9fc86eed7a55414fd83276295772cf771b843c5a0ebc24141a5c5e6a3e81`  
		Last Modified: Tue, 03 Dec 2024 03:24:44 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:11294cbbbfb6477f27fc39bb164375f034e7aa4145103f960d1f196b0313ddab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6431813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff21b632f27ef2b0ef34dadea4d778750d9b22ce199adb24ed20fda027fe0e3`

```dockerfile
```

-	Layers:
	-	`sha256:e566cd69d2ab26fccface2dc7836f61e03df8b9af8d985c5eac4f4704a78d27d`  
		Last Modified: Tue, 03 Dec 2024 03:24:44 GMT  
		Size: 6.4 MB (6417343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0d300dd93561d3aef0afaf7f2b9b41345a42092f3c6b7acd7385f76b632599`  
		Last Modified: Tue, 03 Dec 2024 03:24:44 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:90babf59ae355dd9ca5289657c8387483c5284a406190467f8d608934b0855e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146510697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce88ea4a0c3e79d65dda7b627957b2a5b84b012a02b4e4bf50bac61256d2925`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c1519b04115013f7821f6b8398475148c7865994c7c5de2fb71d5916d5fb2e`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 17.7 MB (17725323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1859599b084be651ec09e42d0c7674081d74a573bd8eb676cc088609c1a1ed`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5aa14951461d4f24e8fe98880a1cdd3e533b827a78c21ab0b29e418320a334`  
		Last Modified: Wed, 13 Nov 2024 10:42:15 GMT  
		Size: 61.7 MB (61672399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9739370ed5c207a5b6b7db43b0f9c0842fbcd23b76c95fc4621def21308c0e3e`  
		Last Modified: Wed, 13 Nov 2024 10:42:13 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:05584c0701cf4027c88e039d7fe5bd76a64dd18dd3df21edfad122d5b705a046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6428583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5f21606923eb8970e4464c88e6c445a5b20b02e6f592a507b872e03d5c32a2`

```dockerfile
```

-	Layers:
	-	`sha256:8fe419709d841bd11cee70d38e46053dfdcc1a9f95dc2125218f9b4e238ab477`  
		Last Modified: Wed, 13 Nov 2024 10:42:14 GMT  
		Size: 6.4 MB (6414027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff47b9c83c808c9f089467e4bfe9feee8100d1a26f2a5ecbb7430b71c870435b`  
		Last Modified: Wed, 13 Nov 2024 10:42:13 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:deaf87dbc7e2d472c345cec503d2fbf7d7ec05cafd7eb51ac54c20afccc5cbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150982083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aba85cc9fe6bd0a267078be4269c47000f7931428a187f129c1d1d434d119ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82c46aaa37285c7b036e2c06961935d109402757aac6158f08caf19093a766e`  
		Last Modified: Tue, 03 Dec 2024 14:46:53 GMT  
		Size: 18.9 MB (18870397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d3fbbd33a83aef503a229631a61792a552956e729abc4035ad057228a800ba`  
		Last Modified: Tue, 03 Dec 2024 14:46:53 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf045ec18df6cebdfe41d6513c8d4e6c8c9d65f5238d6b4b8b50f594091c6ce`  
		Last Modified: Tue, 03 Dec 2024 14:47:32 GMT  
		Size: 60.4 MB (60377797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922b0d7a6e2a3d4266f6b78fae5b8470fd7d37f1be3a353c17fc489655657c9d`  
		Last Modified: Tue, 03 Dec 2024 14:47:30 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:30902abe5ff47d14c315a9e70f86b75fc71686e479497fdc67c7bb357602f5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6433438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cafe3e1588605acc5e3095d0dace1079639e838ce1dd0064f3a35c59577754`

```dockerfile
```

-	Layers:
	-	`sha256:f4610b4d5c643adc4b245cdd83c5754cf3a5459dad43d4d55165702f798a6f14`  
		Last Modified: Tue, 03 Dec 2024 14:47:30 GMT  
		Size: 6.4 MB (6418858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff519bb59412b621ab9db1a9d1d1e2165be045a8403b71d385abcc0d7f8f222b`  
		Last Modified: Tue, 03 Dec 2024 14:47:30 GMT  
		Size: 14.6 KB (14580 bytes)  
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
		Last Modified: Tue, 12 Nov 2024 02:21:17 GMT  
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
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
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
		Last Modified: Wed, 13 Nov 2024 00:44:56 GMT  
		Size: 15.1 KB (15070 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32`

```console
$ docker pull telegraf@sha256:d2e40d67f84dfd38c95efa7ee4dde2f1b31def5415741a06fe9d1cf1aa3de261
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
$ docker pull telegraf@sha256:90b5da625ef921f5089383356e1e85d1f070dd2dc85346c3df1b507db7606af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161334634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d5700fd4697294bdbe7fc69ffa77031da25a24380565c74b29b5a8a188fbe7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8584d808a3544732d2399a1cd75f7504a45963e284e8b36e35924d8f4c059036`  
		Last Modified: Tue, 03 Dec 2024 03:24:49 GMT  
		Size: 18.9 MB (18948077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca00c6f890e0c9fd8664ec62dd36ae0ba459bc85b6c8775a00b49a29684b62ea`  
		Last Modified: Tue, 03 Dec 2024 03:24:49 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f68c52fca4a74c9ca22ab6e9d2db88ae970c008321be4458589999d63145bd1`  
		Last Modified: Tue, 03 Dec 2024 03:24:50 GMT  
		Size: 70.0 MB (70021066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f81c5679d91f6eb7b6d208c827e7fd6c79872c309e3ff2b5bb1f22566e72c2`  
		Last Modified: Tue, 03 Dec 2024 03:24:49 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:36987cdbf8a516239f06a248d28c72ce71a808f720553e84d7307890df5e4b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6441755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ccf68973c8a0c34c264e6c78c790646c3f8b09d42432cd3df1abbf2c08b93e7`

```dockerfile
```

-	Layers:
	-	`sha256:da57eead985241ab767643723a8fbd672ef650bdf07a3c5b470e896d89bf4d9b`  
		Last Modified: Tue, 03 Dec 2024 03:24:49 GMT  
		Size: 6.4 MB (6426983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34c03b9eadb80e8f1b89585f3267fe9be38fa86e3aee39579d7e1e5aff80676a`  
		Last Modified: Tue, 03 Dec 2024 03:24:49 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:2652b91639669f475dcbafa85d5ceb407b4e5f5048ac1bae42fb5111a1574fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.5 MB (149521208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0e34e51635b65425f13e5466fd55a7e9b870199cf0af36b911845e252c33c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c1519b04115013f7821f6b8398475148c7865994c7c5de2fb71d5916d5fb2e`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 17.7 MB (17725323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1859599b084be651ec09e42d0c7674081d74a573bd8eb676cc088609c1a1ed`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bc73ed1aaf2e0fee0d7200d13d2f068a225cf6b26b40a5f955694865b8c8cc`  
		Last Modified: Mon, 18 Nov 2024 23:04:12 GMT  
		Size: 64.7 MB (64682909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c009391f91b8895de1428a5cfbe7014c5d0674f9bc7bcf35dafc55bfa9fcfc`  
		Last Modified: Mon, 18 Nov 2024 23:04:10 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:7c1f5dc1ef14ae1e81c1073d52d1f1c9cc0e5d2b5c8fc4859ddbd3eaad79def4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec659d8892cbf34142ad5feb5c816f440a4c1a82e16696794ec671aaa51eb3c`

```dockerfile
```

-	Layers:
	-	`sha256:d1c124d3335a2c3aa178c49bd4dfce25b32a69478154254a7d44c040a5323ed3`  
		Last Modified: Mon, 18 Nov 2024 23:04:10 GMT  
		Size: 6.4 MB (6423675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f10b0c590cdddd17bfac9a645ec5e1bc2dd583f281d32c22e76209aa449e28d3`  
		Last Modified: Mon, 18 Nov 2024 23:04:10 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a3afd005f87d33b98b787a8932115c1b7aa0beefd8922ce503f80cdf5ee8ced1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153755820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09598109a427b6a5744a2d2f90334637c62fd102979d2f18f6ed3739ff0086c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82c46aaa37285c7b036e2c06961935d109402757aac6158f08caf19093a766e`  
		Last Modified: Tue, 03 Dec 2024 14:46:53 GMT  
		Size: 18.9 MB (18870397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d3fbbd33a83aef503a229631a61792a552956e729abc4035ad057228a800ba`  
		Last Modified: Tue, 03 Dec 2024 14:46:53 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747970fe254af55439a1c6bee45d0cdcbb3d053f9dbce0692badbe834e4e6886`  
		Last Modified: Tue, 03 Dec 2024 14:48:00 GMT  
		Size: 63.2 MB (63151535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c631f472e2e393c43d10f2d3443c73ac4ba4b8d60ebc2afd3119529ad8df3c`  
		Last Modified: Tue, 03 Dec 2024 14:47:58 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:bb4bf15c88c876c665dd52a292d1bd8f14b92148599a40b0a6aa6184bf603a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6442607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edeb3689a88a844067983a54b05d5cde64b957db76bdbeba246e2ecfe45477c3`

```dockerfile
```

-	Layers:
	-	`sha256:48b49b0bd60e1ddc51791a79c3c7553d0db65f2a66269eaed02fbd0df8bde99f`  
		Last Modified: Tue, 03 Dec 2024 14:47:59 GMT  
		Size: 6.4 MB (6427713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072a807859c463f9746d15e79da2e694d6bf09cc982886018367a102cc3d507b`  
		Last Modified: Tue, 03 Dec 2024 14:47:58 GMT  
		Size: 14.9 KB (14894 bytes)  
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
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac69faebcdcde53563af6c2f2356011b54221d2d336fa20004d6e41cf7f676c`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 2.4 MB (2444821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d3519fedc4d5ee37ea7859c2cedc0f290e072022c6947c318979fd6eb71f55`  
		Last Modified: Mon, 18 Nov 2024 23:04:08 GMT  
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
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
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
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32.3`

```console
$ docker pull telegraf@sha256:d2e40d67f84dfd38c95efa7ee4dde2f1b31def5415741a06fe9d1cf1aa3de261
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
$ docker pull telegraf@sha256:90b5da625ef921f5089383356e1e85d1f070dd2dc85346c3df1b507db7606af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161334634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d5700fd4697294bdbe7fc69ffa77031da25a24380565c74b29b5a8a188fbe7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8584d808a3544732d2399a1cd75f7504a45963e284e8b36e35924d8f4c059036`  
		Last Modified: Tue, 03 Dec 2024 03:24:49 GMT  
		Size: 18.9 MB (18948077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca00c6f890e0c9fd8664ec62dd36ae0ba459bc85b6c8775a00b49a29684b62ea`  
		Last Modified: Tue, 03 Dec 2024 03:24:49 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f68c52fca4a74c9ca22ab6e9d2db88ae970c008321be4458589999d63145bd1`  
		Last Modified: Tue, 03 Dec 2024 03:24:50 GMT  
		Size: 70.0 MB (70021066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f81c5679d91f6eb7b6d208c827e7fd6c79872c309e3ff2b5bb1f22566e72c2`  
		Last Modified: Tue, 03 Dec 2024 03:24:49 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:36987cdbf8a516239f06a248d28c72ce71a808f720553e84d7307890df5e4b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6441755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ccf68973c8a0c34c264e6c78c790646c3f8b09d42432cd3df1abbf2c08b93e7`

```dockerfile
```

-	Layers:
	-	`sha256:da57eead985241ab767643723a8fbd672ef650bdf07a3c5b470e896d89bf4d9b`  
		Last Modified: Tue, 03 Dec 2024 03:24:49 GMT  
		Size: 6.4 MB (6426983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34c03b9eadb80e8f1b89585f3267fe9be38fa86e3aee39579d7e1e5aff80676a`  
		Last Modified: Tue, 03 Dec 2024 03:24:49 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:2652b91639669f475dcbafa85d5ceb407b4e5f5048ac1bae42fb5111a1574fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.5 MB (149521208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0e34e51635b65425f13e5466fd55a7e9b870199cf0af36b911845e252c33c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c1519b04115013f7821f6b8398475148c7865994c7c5de2fb71d5916d5fb2e`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 17.7 MB (17725323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1859599b084be651ec09e42d0c7674081d74a573bd8eb676cc088609c1a1ed`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bc73ed1aaf2e0fee0d7200d13d2f068a225cf6b26b40a5f955694865b8c8cc`  
		Last Modified: Mon, 18 Nov 2024 23:04:12 GMT  
		Size: 64.7 MB (64682909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c009391f91b8895de1428a5cfbe7014c5d0674f9bc7bcf35dafc55bfa9fcfc`  
		Last Modified: Mon, 18 Nov 2024 23:04:10 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:7c1f5dc1ef14ae1e81c1073d52d1f1c9cc0e5d2b5c8fc4859ddbd3eaad79def4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec659d8892cbf34142ad5feb5c816f440a4c1a82e16696794ec671aaa51eb3c`

```dockerfile
```

-	Layers:
	-	`sha256:d1c124d3335a2c3aa178c49bd4dfce25b32a69478154254a7d44c040a5323ed3`  
		Last Modified: Mon, 18 Nov 2024 23:04:10 GMT  
		Size: 6.4 MB (6423675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f10b0c590cdddd17bfac9a645ec5e1bc2dd583f281d32c22e76209aa449e28d3`  
		Last Modified: Mon, 18 Nov 2024 23:04:10 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a3afd005f87d33b98b787a8932115c1b7aa0beefd8922ce503f80cdf5ee8ced1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153755820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09598109a427b6a5744a2d2f90334637c62fd102979d2f18f6ed3739ff0086c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82c46aaa37285c7b036e2c06961935d109402757aac6158f08caf19093a766e`  
		Last Modified: Tue, 03 Dec 2024 14:46:53 GMT  
		Size: 18.9 MB (18870397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d3fbbd33a83aef503a229631a61792a552956e729abc4035ad057228a800ba`  
		Last Modified: Tue, 03 Dec 2024 14:46:53 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747970fe254af55439a1c6bee45d0cdcbb3d053f9dbce0692badbe834e4e6886`  
		Last Modified: Tue, 03 Dec 2024 14:48:00 GMT  
		Size: 63.2 MB (63151535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c631f472e2e393c43d10f2d3443c73ac4ba4b8d60ebc2afd3119529ad8df3c`  
		Last Modified: Tue, 03 Dec 2024 14:47:58 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:bb4bf15c88c876c665dd52a292d1bd8f14b92148599a40b0a6aa6184bf603a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6442607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edeb3689a88a844067983a54b05d5cde64b957db76bdbeba246e2ecfe45477c3`

```dockerfile
```

-	Layers:
	-	`sha256:48b49b0bd60e1ddc51791a79c3c7553d0db65f2a66269eaed02fbd0df8bde99f`  
		Last Modified: Tue, 03 Dec 2024 14:47:59 GMT  
		Size: 6.4 MB (6427713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072a807859c463f9746d15e79da2e694d6bf09cc982886018367a102cc3d507b`  
		Last Modified: Tue, 03 Dec 2024 14:47:58 GMT  
		Size: 14.9 KB (14894 bytes)  
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
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac69faebcdcde53563af6c2f2356011b54221d2d336fa20004d6e41cf7f676c`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 2.4 MB (2444821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d3519fedc4d5ee37ea7859c2cedc0f290e072022c6947c318979fd6eb71f55`  
		Last Modified: Mon, 18 Nov 2024 23:04:08 GMT  
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
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
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
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:4046c04762db9e28ad0fc5beebffaa0edf345ea2c7b8aa3ad5ba8db02f6f4c2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

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
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac69faebcdcde53563af6c2f2356011b54221d2d336fa20004d6e41cf7f676c`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 2.4 MB (2444821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d3519fedc4d5ee37ea7859c2cedc0f290e072022c6947c318979fd6eb71f55`  
		Last Modified: Mon, 18 Nov 2024 23:04:08 GMT  
		Size: 69.8 MB (69824563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6fc6e4c616b483bafdc6d886f7d5a5c2d59fcbff06d37f5eec6352e6f45818`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

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

### `telegraf:alpine` - linux; arm64 variant v8

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
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
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

### `telegraf:alpine` - unknown; unknown

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
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:d2e40d67f84dfd38c95efa7ee4dde2f1b31def5415741a06fe9d1cf1aa3de261
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
$ docker pull telegraf@sha256:90b5da625ef921f5089383356e1e85d1f070dd2dc85346c3df1b507db7606af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161334634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d5700fd4697294bdbe7fc69ffa77031da25a24380565c74b29b5a8a188fbe7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8584d808a3544732d2399a1cd75f7504a45963e284e8b36e35924d8f4c059036`  
		Last Modified: Tue, 03 Dec 2024 03:24:49 GMT  
		Size: 18.9 MB (18948077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca00c6f890e0c9fd8664ec62dd36ae0ba459bc85b6c8775a00b49a29684b62ea`  
		Last Modified: Tue, 03 Dec 2024 03:24:49 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f68c52fca4a74c9ca22ab6e9d2db88ae970c008321be4458589999d63145bd1`  
		Last Modified: Tue, 03 Dec 2024 03:24:50 GMT  
		Size: 70.0 MB (70021066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f81c5679d91f6eb7b6d208c827e7fd6c79872c309e3ff2b5bb1f22566e72c2`  
		Last Modified: Tue, 03 Dec 2024 03:24:49 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:36987cdbf8a516239f06a248d28c72ce71a808f720553e84d7307890df5e4b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6441755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ccf68973c8a0c34c264e6c78c790646c3f8b09d42432cd3df1abbf2c08b93e7`

```dockerfile
```

-	Layers:
	-	`sha256:da57eead985241ab767643723a8fbd672ef650bdf07a3c5b470e896d89bf4d9b`  
		Last Modified: Tue, 03 Dec 2024 03:24:49 GMT  
		Size: 6.4 MB (6426983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34c03b9eadb80e8f1b89585f3267fe9be38fa86e3aee39579d7e1e5aff80676a`  
		Last Modified: Tue, 03 Dec 2024 03:24:49 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:2652b91639669f475dcbafa85d5ceb407b4e5f5048ac1bae42fb5111a1574fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.5 MB (149521208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0e34e51635b65425f13e5466fd55a7e9b870199cf0af36b911845e252c33c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c1519b04115013f7821f6b8398475148c7865994c7c5de2fb71d5916d5fb2e`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 17.7 MB (17725323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1859599b084be651ec09e42d0c7674081d74a573bd8eb676cc088609c1a1ed`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bc73ed1aaf2e0fee0d7200d13d2f068a225cf6b26b40a5f955694865b8c8cc`  
		Last Modified: Mon, 18 Nov 2024 23:04:12 GMT  
		Size: 64.7 MB (64682909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c009391f91b8895de1428a5cfbe7014c5d0674f9bc7bcf35dafc55bfa9fcfc`  
		Last Modified: Mon, 18 Nov 2024 23:04:10 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:7c1f5dc1ef14ae1e81c1073d52d1f1c9cc0e5d2b5c8fc4859ddbd3eaad79def4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec659d8892cbf34142ad5feb5c816f440a4c1a82e16696794ec671aaa51eb3c`

```dockerfile
```

-	Layers:
	-	`sha256:d1c124d3335a2c3aa178c49bd4dfce25b32a69478154254a7d44c040a5323ed3`  
		Last Modified: Mon, 18 Nov 2024 23:04:10 GMT  
		Size: 6.4 MB (6423675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f10b0c590cdddd17bfac9a645ec5e1bc2dd583f281d32c22e76209aa449e28d3`  
		Last Modified: Mon, 18 Nov 2024 23:04:10 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a3afd005f87d33b98b787a8932115c1b7aa0beefd8922ce503f80cdf5ee8ced1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153755820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09598109a427b6a5744a2d2f90334637c62fd102979d2f18f6ed3739ff0086c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82c46aaa37285c7b036e2c06961935d109402757aac6158f08caf19093a766e`  
		Last Modified: Tue, 03 Dec 2024 14:46:53 GMT  
		Size: 18.9 MB (18870397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d3fbbd33a83aef503a229631a61792a552956e729abc4035ad057228a800ba`  
		Last Modified: Tue, 03 Dec 2024 14:46:53 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747970fe254af55439a1c6bee45d0cdcbb3d053f9dbce0692badbe834e4e6886`  
		Last Modified: Tue, 03 Dec 2024 14:48:00 GMT  
		Size: 63.2 MB (63151535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c631f472e2e393c43d10f2d3443c73ac4ba4b8d60ebc2afd3119529ad8df3c`  
		Last Modified: Tue, 03 Dec 2024 14:47:58 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:bb4bf15c88c876c665dd52a292d1bd8f14b92148599a40b0a6aa6184bf603a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6442607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edeb3689a88a844067983a54b05d5cde64b957db76bdbeba246e2ecfe45477c3`

```dockerfile
```

-	Layers:
	-	`sha256:48b49b0bd60e1ddc51791a79c3c7553d0db65f2a66269eaed02fbd0df8bde99f`  
		Last Modified: Tue, 03 Dec 2024 14:47:59 GMT  
		Size: 6.4 MB (6427713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072a807859c463f9746d15e79da2e694d6bf09cc982886018367a102cc3d507b`  
		Last Modified: Tue, 03 Dec 2024 14:47:58 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
