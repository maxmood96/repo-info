<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.16`](#telegraf116)
-	[`telegraf:1.16-alpine`](#telegraf116-alpine)
-	[`telegraf:1.16.3`](#telegraf1163)
-	[`telegraf:1.16.3-alpine`](#telegraf1163-alpine)
-	[`telegraf:1.17`](#telegraf117)
-	[`telegraf:1.17-alpine`](#telegraf117-alpine)
-	[`telegraf:1.17.3`](#telegraf1173)
-	[`telegraf:1.17.3-alpine`](#telegraf1173-alpine)
-	[`telegraf:1.18`](#telegraf118)
-	[`telegraf:1.18-alpine`](#telegraf118-alpine)
-	[`telegraf:1.18.1`](#telegraf1181)
-	[`telegraf:1.18.1-alpine`](#telegraf1181-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.16`

```console
$ docker pull telegraf@sha256:151c16d8ab8ecaa58e5f446725a4258f3d82008ce67a4f1f4b71a478c76c23b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.16` - linux; amd64

```console
$ docker pull telegraf@sha256:747186f4fd16e35ca60a1f679fc8f3595a2556c1218b076ec10535956cd2b75c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (108037825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5930e85bf27218a27f1a5dedf0aed73bf4cbf4011bf20f56506777d2fb96b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:08 GMT
ADD file:e18bc3e10e7c743f18bb8be65ec94a62c03764af7dbdb4957f9a600237730212 in / 
# Sat, 10 Apr 2021 01:20:09 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:54:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:54:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 11 Apr 2021 00:20:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sun, 11 Apr 2021 00:20:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 11 Apr 2021 00:20:06 GMT
ENV TELEGRAF_VERSION=1.16.3
# Sun, 11 Apr 2021 00:20:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sun, 11 Apr 2021 00:20:10 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sun, 11 Apr 2021 00:20:10 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sun, 11 Apr 2021 00:20:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 11 Apr 2021 00:20:10 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bd8f6a7501ccbe80b95c82519ed6fd4f7236a41e0ae59ba4a8df76af24629efc`  
		Last Modified: Sat, 10 Apr 2021 01:24:48 GMT  
		Size: 50.4 MB (50432971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44718e6d535d365250316b02459f98a1b0fa490158cc53057d18858507504d60`  
		Last Modified: Sat, 10 Apr 2021 02:01:57 GMT  
		Size: 7.8 MB (7832944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe9738af0cb2184ee8f3fb3dcb130455385aa428a27d14e1e07a5587ff16e64`  
		Last Modified: Sat, 10 Apr 2021 02:01:59 GMT  
		Size: 10.0 MB (9997183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b311f6d4be86d05278922f0a954851900a506a94ba9617ed7bc61f75a838316`  
		Last Modified: Sun, 11 Apr 2021 00:20:58 GMT  
		Size: 17.4 MB (17414435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ba220c8e4ca9f44f0b52538b1d8a42113d7f0f68ce1cad4bd6731a5c69b925`  
		Last Modified: Sun, 11 Apr 2021 00:20:54 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739cc1a3f530c177cd807ffeb6c3d3715bab42a90b55082ab61dd8cd45cca74c`  
		Last Modified: Sun, 11 Apr 2021 00:20:59 GMT  
		Size: 22.4 MB (22357210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8425f0a578b35b3c18efaeea56ecc2bb124e32426444d3290a588ba720caf796`  
		Last Modified: Sun, 11 Apr 2021 00:20:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.16` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:53a66274aa39f6ea1e60c040b18791e4dabb997c9ae9a7bd5ebfefed5cbfbc03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99435950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6479561384fa8e0b14b9e3c510a88dd82e3df72de163c4ea73c59188734ac83`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 00:59:18 GMT
ADD file:bd2081229497eea2b33310cb1582b965581ca78b00b87cc8e42bdc8b9f350678 in / 
# Sat, 10 Apr 2021 00:59:20 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 06:05:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 06:05:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 11 Apr 2021 00:01:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sun, 11 Apr 2021 00:01:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 11 Apr 2021 00:01:41 GMT
ENV TELEGRAF_VERSION=1.16.3
# Sun, 11 Apr 2021 00:01:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sun, 11 Apr 2021 00:01:48 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sun, 11 Apr 2021 00:01:49 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sun, 11 Apr 2021 00:01:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 11 Apr 2021 00:01:51 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:de0ca59eb81518ffd92fbcd386251018f950dc16b1bd8ad2e642184db76be2a1`  
		Last Modified: Sat, 10 Apr 2021 01:07:26 GMT  
		Size: 45.9 MB (45915598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed23bfa8aaeab64a1ca00d3bead680f790be28326d14305705b2ee5227b4f2b7`  
		Last Modified: Sat, 10 Apr 2021 06:19:54 GMT  
		Size: 7.1 MB (7124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a12824e68a5072613049fad15fc8f0d209526ddd9d85787cc60d1b0d5073c0`  
		Last Modified: Sat, 10 Apr 2021 06:19:55 GMT  
		Size: 9.3 MB (9343784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9b5a49c2322e06d3fc820c5ff14f870c596c995b7507088b36bc3a1672b6ab`  
		Last Modified: Sun, 11 Apr 2021 00:03:02 GMT  
		Size: 16.2 MB (16159209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0870eb6e6fcdd0fb000437fe01af38c3221a86734c678514de094444ed63fed0`  
		Last Modified: Sun, 11 Apr 2021 00:02:52 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd17b5824801ff34b468c7e614a9074be4040aa78c8f2a624378314139b0a8eb`  
		Last Modified: Sun, 11 Apr 2021 00:02:59 GMT  
		Size: 20.9 MB (20890096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9920e572a5bd2104a6b860a0383323e6f93d8f3fbd096e9ce379ead4320ec86`  
		Last Modified: Sun, 11 Apr 2021 00:02:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.16` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e127f0205614d683033525960ce8edd2f1cf2bfc4e19cf471e2887bfacc67450
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104672284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e43bd33c93eec8c8028564355048e6d4b087510629966c7d13e694a661d50e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 00:40:59 GMT
ADD file:320ad0e2a3d6c676ddb8ce5646b5a94d18d82a8868955da3a9379a261dfe1ffe in / 
# Sat, 10 Apr 2021 00:41:01 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:46:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:46:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 23:33:45 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 23:33:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 23:33:49 GMT
ENV TELEGRAF_VERSION=1.16.3
# Sat, 10 Apr 2021 23:33:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 10 Apr 2021 23:33:55 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 10 Apr 2021 23:33:56 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sat, 10 Apr 2021 23:33:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 23:33:58 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01cf0f0da10ede0eec0fc1c5fbfdeb63a447dfcc0a3c4419c0a4c3f0a2826636`  
		Last Modified: Sat, 10 Apr 2021 00:47:28 GMT  
		Size: 49.2 MB (49225782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c667eb56cd05909001c1c50e81cbc75e290fd8e353f974bab4246a0d4fc484ca`  
		Last Modified: Sat, 10 Apr 2021 02:01:00 GMT  
		Size: 7.7 MB (7695101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ca15a4cef673e0e1a7bc3e659f4653df9bce82b945e367475e436852cc7880`  
		Last Modified: Sat, 10 Apr 2021 02:00:59 GMT  
		Size: 10.0 MB (9984406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7440732130595d801c674589c3625a20f8ba2557fc88cacd7025e2a93db2eb4`  
		Last Modified: Sat, 10 Apr 2021 23:34:56 GMT  
		Size: 17.3 MB (17269572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e708bbd80f49e36ab315d2c12f23cc9b58cc5db46272609d4162cf97e2e4177e`  
		Last Modified: Sat, 10 Apr 2021 23:34:50 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c50938f9bcc8b4b2fbcdfc9a3843c8b1e378ef7c96bf966303b7b251ee5a0d`  
		Last Modified: Sat, 10 Apr 2021 23:34:56 GMT  
		Size: 20.5 MB (20494341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cf6b6246e7dd2be2907917b14d5ea71805d31e73ce9044ee2025df2eb96ea4`  
		Last Modified: Sat, 10 Apr 2021 23:34:50 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.16-alpine`

```console
$ docker pull telegraf@sha256:bafffff80f705dc77b3ddffdc085018edc8ca29fe6036b8dc55ce2cbdeac20c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.16-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:4b97547cb91d8b2f9d9b84ed744303e723033bb267e43334385e41451b1ef9bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28315034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ae49b672a1396eee003f7937a976d58212ca2aec493fefa226f012b0bc9fd0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:46:56 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Wed, 31 Mar 2021 22:46:56 GMT
ENV TELEGRAF_VERSION=1.16.3
# Wed, 31 Mar 2021 22:47:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 31 Mar 2021 22:47:04 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 31 Mar 2021 22:47:05 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Wed, 31 Mar 2021 22:47:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:47:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3d7ca742af0ce468e2012708013276fbd53bc83cbfbc6067bee7576dfc77fd`  
		Last Modified: Wed, 31 Mar 2021 22:48:32 GMT  
		Size: 3.3 MB (3300612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b24b2ef2e945c093a864cee98065bb150dcf6fb3f625d1b8a0e5747387e6113`  
		Last Modified: Wed, 31 Mar 2021 22:48:38 GMT  
		Size: 22.2 MB (22214370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e62aa81482401d0acc5589d9a8cb6d47c2eaa7eeb1c6e43750365771c0c8fb5`  
		Last Modified: Wed, 31 Mar 2021 22:48:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.16.3`

```console
$ docker pull telegraf@sha256:151c16d8ab8ecaa58e5f446725a4258f3d82008ce67a4f1f4b71a478c76c23b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.16.3` - linux; amd64

```console
$ docker pull telegraf@sha256:747186f4fd16e35ca60a1f679fc8f3595a2556c1218b076ec10535956cd2b75c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (108037825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5930e85bf27218a27f1a5dedf0aed73bf4cbf4011bf20f56506777d2fb96b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:08 GMT
ADD file:e18bc3e10e7c743f18bb8be65ec94a62c03764af7dbdb4957f9a600237730212 in / 
# Sat, 10 Apr 2021 01:20:09 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:54:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:54:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 11 Apr 2021 00:20:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sun, 11 Apr 2021 00:20:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 11 Apr 2021 00:20:06 GMT
ENV TELEGRAF_VERSION=1.16.3
# Sun, 11 Apr 2021 00:20:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sun, 11 Apr 2021 00:20:10 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sun, 11 Apr 2021 00:20:10 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sun, 11 Apr 2021 00:20:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 11 Apr 2021 00:20:10 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bd8f6a7501ccbe80b95c82519ed6fd4f7236a41e0ae59ba4a8df76af24629efc`  
		Last Modified: Sat, 10 Apr 2021 01:24:48 GMT  
		Size: 50.4 MB (50432971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44718e6d535d365250316b02459f98a1b0fa490158cc53057d18858507504d60`  
		Last Modified: Sat, 10 Apr 2021 02:01:57 GMT  
		Size: 7.8 MB (7832944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe9738af0cb2184ee8f3fb3dcb130455385aa428a27d14e1e07a5587ff16e64`  
		Last Modified: Sat, 10 Apr 2021 02:01:59 GMT  
		Size: 10.0 MB (9997183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b311f6d4be86d05278922f0a954851900a506a94ba9617ed7bc61f75a838316`  
		Last Modified: Sun, 11 Apr 2021 00:20:58 GMT  
		Size: 17.4 MB (17414435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ba220c8e4ca9f44f0b52538b1d8a42113d7f0f68ce1cad4bd6731a5c69b925`  
		Last Modified: Sun, 11 Apr 2021 00:20:54 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739cc1a3f530c177cd807ffeb6c3d3715bab42a90b55082ab61dd8cd45cca74c`  
		Last Modified: Sun, 11 Apr 2021 00:20:59 GMT  
		Size: 22.4 MB (22357210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8425f0a578b35b3c18efaeea56ecc2bb124e32426444d3290a588ba720caf796`  
		Last Modified: Sun, 11 Apr 2021 00:20:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.16.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:53a66274aa39f6ea1e60c040b18791e4dabb997c9ae9a7bd5ebfefed5cbfbc03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99435950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6479561384fa8e0b14b9e3c510a88dd82e3df72de163c4ea73c59188734ac83`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 00:59:18 GMT
ADD file:bd2081229497eea2b33310cb1582b965581ca78b00b87cc8e42bdc8b9f350678 in / 
# Sat, 10 Apr 2021 00:59:20 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 06:05:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 06:05:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 11 Apr 2021 00:01:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sun, 11 Apr 2021 00:01:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 11 Apr 2021 00:01:41 GMT
ENV TELEGRAF_VERSION=1.16.3
# Sun, 11 Apr 2021 00:01:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sun, 11 Apr 2021 00:01:48 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sun, 11 Apr 2021 00:01:49 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sun, 11 Apr 2021 00:01:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 11 Apr 2021 00:01:51 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:de0ca59eb81518ffd92fbcd386251018f950dc16b1bd8ad2e642184db76be2a1`  
		Last Modified: Sat, 10 Apr 2021 01:07:26 GMT  
		Size: 45.9 MB (45915598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed23bfa8aaeab64a1ca00d3bead680f790be28326d14305705b2ee5227b4f2b7`  
		Last Modified: Sat, 10 Apr 2021 06:19:54 GMT  
		Size: 7.1 MB (7124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a12824e68a5072613049fad15fc8f0d209526ddd9d85787cc60d1b0d5073c0`  
		Last Modified: Sat, 10 Apr 2021 06:19:55 GMT  
		Size: 9.3 MB (9343784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9b5a49c2322e06d3fc820c5ff14f870c596c995b7507088b36bc3a1672b6ab`  
		Last Modified: Sun, 11 Apr 2021 00:03:02 GMT  
		Size: 16.2 MB (16159209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0870eb6e6fcdd0fb000437fe01af38c3221a86734c678514de094444ed63fed0`  
		Last Modified: Sun, 11 Apr 2021 00:02:52 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd17b5824801ff34b468c7e614a9074be4040aa78c8f2a624378314139b0a8eb`  
		Last Modified: Sun, 11 Apr 2021 00:02:59 GMT  
		Size: 20.9 MB (20890096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9920e572a5bd2104a6b860a0383323e6f93d8f3fbd096e9ce379ead4320ec86`  
		Last Modified: Sun, 11 Apr 2021 00:02:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.16.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e127f0205614d683033525960ce8edd2f1cf2bfc4e19cf471e2887bfacc67450
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104672284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e43bd33c93eec8c8028564355048e6d4b087510629966c7d13e694a661d50e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 00:40:59 GMT
ADD file:320ad0e2a3d6c676ddb8ce5646b5a94d18d82a8868955da3a9379a261dfe1ffe in / 
# Sat, 10 Apr 2021 00:41:01 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:46:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:46:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 23:33:45 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 23:33:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 23:33:49 GMT
ENV TELEGRAF_VERSION=1.16.3
# Sat, 10 Apr 2021 23:33:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 10 Apr 2021 23:33:55 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 10 Apr 2021 23:33:56 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sat, 10 Apr 2021 23:33:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 23:33:58 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01cf0f0da10ede0eec0fc1c5fbfdeb63a447dfcc0a3c4419c0a4c3f0a2826636`  
		Last Modified: Sat, 10 Apr 2021 00:47:28 GMT  
		Size: 49.2 MB (49225782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c667eb56cd05909001c1c50e81cbc75e290fd8e353f974bab4246a0d4fc484ca`  
		Last Modified: Sat, 10 Apr 2021 02:01:00 GMT  
		Size: 7.7 MB (7695101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ca15a4cef673e0e1a7bc3e659f4653df9bce82b945e367475e436852cc7880`  
		Last Modified: Sat, 10 Apr 2021 02:00:59 GMT  
		Size: 10.0 MB (9984406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7440732130595d801c674589c3625a20f8ba2557fc88cacd7025e2a93db2eb4`  
		Last Modified: Sat, 10 Apr 2021 23:34:56 GMT  
		Size: 17.3 MB (17269572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e708bbd80f49e36ab315d2c12f23cc9b58cc5db46272609d4162cf97e2e4177e`  
		Last Modified: Sat, 10 Apr 2021 23:34:50 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c50938f9bcc8b4b2fbcdfc9a3843c8b1e378ef7c96bf966303b7b251ee5a0d`  
		Last Modified: Sat, 10 Apr 2021 23:34:56 GMT  
		Size: 20.5 MB (20494341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cf6b6246e7dd2be2907917b14d5ea71805d31e73ce9044ee2025df2eb96ea4`  
		Last Modified: Sat, 10 Apr 2021 23:34:50 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.16.3-alpine`

```console
$ docker pull telegraf@sha256:bafffff80f705dc77b3ddffdc085018edc8ca29fe6036b8dc55ce2cbdeac20c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.16.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:4b97547cb91d8b2f9d9b84ed744303e723033bb267e43334385e41451b1ef9bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28315034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ae49b672a1396eee003f7937a976d58212ca2aec493fefa226f012b0bc9fd0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:46:56 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Wed, 31 Mar 2021 22:46:56 GMT
ENV TELEGRAF_VERSION=1.16.3
# Wed, 31 Mar 2021 22:47:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 31 Mar 2021 22:47:04 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 31 Mar 2021 22:47:05 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Wed, 31 Mar 2021 22:47:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:47:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3d7ca742af0ce468e2012708013276fbd53bc83cbfbc6067bee7576dfc77fd`  
		Last Modified: Wed, 31 Mar 2021 22:48:32 GMT  
		Size: 3.3 MB (3300612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b24b2ef2e945c093a864cee98065bb150dcf6fb3f625d1b8a0e5747387e6113`  
		Last Modified: Wed, 31 Mar 2021 22:48:38 GMT  
		Size: 22.2 MB (22214370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e62aa81482401d0acc5589d9a8cb6d47c2eaa7eeb1c6e43750365771c0c8fb5`  
		Last Modified: Wed, 31 Mar 2021 22:48:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.17`

```console
$ docker pull telegraf@sha256:b92576d12d0281b833551d32b44a0c3d8f27a5b9c58318ecc2cb05e9e2eeda37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.17` - linux; amd64

```console
$ docker pull telegraf@sha256:7d2f9caf80589c24bf6a53d3781f9e841c4a27513371452765e2dda4d7dcfb42
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108639487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227b692bf4082154544e6256333bd9a979136de4dc76fa95a55b83e9d219522f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:08 GMT
ADD file:e18bc3e10e7c743f18bb8be65ec94a62c03764af7dbdb4957f9a600237730212 in / 
# Sat, 10 Apr 2021 01:20:09 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:54:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:54:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 11 Apr 2021 00:20:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sun, 11 Apr 2021 00:20:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 11 Apr 2021 00:20:16 GMT
ENV TELEGRAF_VERSION=1.17.3
# Sun, 11 Apr 2021 00:20:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sun, 11 Apr 2021 00:20:21 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sun, 11 Apr 2021 00:20:21 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sun, 11 Apr 2021 00:20:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 11 Apr 2021 00:20:21 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bd8f6a7501ccbe80b95c82519ed6fd4f7236a41e0ae59ba4a8df76af24629efc`  
		Last Modified: Sat, 10 Apr 2021 01:24:48 GMT  
		Size: 50.4 MB (50432971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44718e6d535d365250316b02459f98a1b0fa490158cc53057d18858507504d60`  
		Last Modified: Sat, 10 Apr 2021 02:01:57 GMT  
		Size: 7.8 MB (7832944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe9738af0cb2184ee8f3fb3dcb130455385aa428a27d14e1e07a5587ff16e64`  
		Last Modified: Sat, 10 Apr 2021 02:01:59 GMT  
		Size: 10.0 MB (9997183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b311f6d4be86d05278922f0a954851900a506a94ba9617ed7bc61f75a838316`  
		Last Modified: Sun, 11 Apr 2021 00:20:58 GMT  
		Size: 17.4 MB (17414435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ba220c8e4ca9f44f0b52538b1d8a42113d7f0f68ce1cad4bd6731a5c69b925`  
		Last Modified: Sun, 11 Apr 2021 00:20:54 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44849540cd0d7632667a0bb80be262400ea812d02a89dc8e2d04adb86cb985c`  
		Last Modified: Sun, 11 Apr 2021 00:21:17 GMT  
		Size: 23.0 MB (22958873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91dd9636c593c74c191b597cdf0c1b60b8320eea98208c8b4cacfd97b7acc1d8`  
		Last Modified: Sun, 11 Apr 2021 00:21:10 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.17` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:8b4b952357210ad2184f3452d12575eed481c5881fd00715ac51bd34450a8a0f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (100004462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5c01eae6fbe4b2e3d81c244b1787c8a83ab2e70cadf29a574bf03deaa59590`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 00:59:18 GMT
ADD file:bd2081229497eea2b33310cb1582b965581ca78b00b87cc8e42bdc8b9f350678 in / 
# Sat, 10 Apr 2021 00:59:20 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 06:05:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 06:05:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 11 Apr 2021 00:01:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sun, 11 Apr 2021 00:01:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 11 Apr 2021 00:02:00 GMT
ENV TELEGRAF_VERSION=1.17.3
# Sun, 11 Apr 2021 00:02:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sun, 11 Apr 2021 00:02:08 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sun, 11 Apr 2021 00:02:09 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sun, 11 Apr 2021 00:02:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 11 Apr 2021 00:02:11 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:de0ca59eb81518ffd92fbcd386251018f950dc16b1bd8ad2e642184db76be2a1`  
		Last Modified: Sat, 10 Apr 2021 01:07:26 GMT  
		Size: 45.9 MB (45915598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed23bfa8aaeab64a1ca00d3bead680f790be28326d14305705b2ee5227b4f2b7`  
		Last Modified: Sat, 10 Apr 2021 06:19:54 GMT  
		Size: 7.1 MB (7124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a12824e68a5072613049fad15fc8f0d209526ddd9d85787cc60d1b0d5073c0`  
		Last Modified: Sat, 10 Apr 2021 06:19:55 GMT  
		Size: 9.3 MB (9343784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9b5a49c2322e06d3fc820c5ff14f870c596c995b7507088b36bc3a1672b6ab`  
		Last Modified: Sun, 11 Apr 2021 00:03:02 GMT  
		Size: 16.2 MB (16159209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0870eb6e6fcdd0fb000437fe01af38c3221a86734c678514de094444ed63fed0`  
		Last Modified: Sun, 11 Apr 2021 00:02:52 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222dca62499f92461027a24a33ecfc1d7276ee05443a804eeca8d25509266293`  
		Last Modified: Sun, 11 Apr 2021 00:03:16 GMT  
		Size: 21.5 MB (21458608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57683c38379e2ce60baf111b9ebce05d778db3eed573b6b904748a1084b22317`  
		Last Modified: Sun, 11 Apr 2021 00:03:09 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.17` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6908f849fbb72b3572b6f69ad86c356baae97317361776ced8aced4d2a1054bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105229671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b46549f79d777d2d986afdec193808da89920dea0e135c7c3cd5bc542be06e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 00:40:59 GMT
ADD file:320ad0e2a3d6c676ddb8ce5646b5a94d18d82a8868955da3a9379a261dfe1ffe in / 
# Sat, 10 Apr 2021 00:41:01 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:46:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:46:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 23:33:45 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 23:33:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 23:34:07 GMT
ENV TELEGRAF_VERSION=1.17.3
# Sat, 10 Apr 2021 23:34:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 10 Apr 2021 23:34:13 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 10 Apr 2021 23:34:14 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sat, 10 Apr 2021 23:34:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 23:34:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01cf0f0da10ede0eec0fc1c5fbfdeb63a447dfcc0a3c4419c0a4c3f0a2826636`  
		Last Modified: Sat, 10 Apr 2021 00:47:28 GMT  
		Size: 49.2 MB (49225782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c667eb56cd05909001c1c50e81cbc75e290fd8e353f974bab4246a0d4fc484ca`  
		Last Modified: Sat, 10 Apr 2021 02:01:00 GMT  
		Size: 7.7 MB (7695101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ca15a4cef673e0e1a7bc3e659f4653df9bce82b945e367475e436852cc7880`  
		Last Modified: Sat, 10 Apr 2021 02:00:59 GMT  
		Size: 10.0 MB (9984406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7440732130595d801c674589c3625a20f8ba2557fc88cacd7025e2a93db2eb4`  
		Last Modified: Sat, 10 Apr 2021 23:34:56 GMT  
		Size: 17.3 MB (17269572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e708bbd80f49e36ab315d2c12f23cc9b58cc5db46272609d4162cf97e2e4177e`  
		Last Modified: Sat, 10 Apr 2021 23:34:50 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c7a1fb66fd93ba4a7f85ca802d23e66cd308a5d35d3dfbc749f9663eb16893`  
		Last Modified: Sat, 10 Apr 2021 23:35:09 GMT  
		Size: 21.1 MB (21051729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cd3aca40189890aa3b8eba90ba93142c3c3368917c63bf6d957d3669dd6d78`  
		Last Modified: Sat, 10 Apr 2021 23:35:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.17-alpine`

```console
$ docker pull telegraf@sha256:e5cc20de430b19e5cf2531e8898e06211294064ac9d7a8a69d7e73ec3827f343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.17-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:0c45633c35118bbe3cb87ffaa0c9dec06416ee4ff41b7a8d35ffbe2bf335ef69
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28921560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108daa767dcdeb9e7c67fcef201a04fe0b608f3ad13b6063543e075e1bef514e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:46:56 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Wed, 31 Mar 2021 22:47:22 GMT
ENV TELEGRAF_VERSION=1.17.3
# Wed, 31 Mar 2021 22:47:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 31 Mar 2021 22:47:29 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 31 Mar 2021 22:47:30 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Wed, 31 Mar 2021 22:47:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:47:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3d7ca742af0ce468e2012708013276fbd53bc83cbfbc6067bee7576dfc77fd`  
		Last Modified: Wed, 31 Mar 2021 22:48:32 GMT  
		Size: 3.3 MB (3300612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d91d88132675be9b65b0d93277ac84b4b02ebaec36a901faf284f9926353be`  
		Last Modified: Wed, 31 Mar 2021 22:49:10 GMT  
		Size: 22.8 MB (22820900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5acc6235f76ad9d31e59cbea5a553dd404f4856299d178c28db76f1f66c3b3`  
		Last Modified: Wed, 31 Mar 2021 22:49:05 GMT  
		Size: 181.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.17.3`

```console
$ docker pull telegraf@sha256:b92576d12d0281b833551d32b44a0c3d8f27a5b9c58318ecc2cb05e9e2eeda37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.17.3` - linux; amd64

```console
$ docker pull telegraf@sha256:7d2f9caf80589c24bf6a53d3781f9e841c4a27513371452765e2dda4d7dcfb42
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108639487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227b692bf4082154544e6256333bd9a979136de4dc76fa95a55b83e9d219522f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:08 GMT
ADD file:e18bc3e10e7c743f18bb8be65ec94a62c03764af7dbdb4957f9a600237730212 in / 
# Sat, 10 Apr 2021 01:20:09 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:54:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:54:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 11 Apr 2021 00:20:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sun, 11 Apr 2021 00:20:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 11 Apr 2021 00:20:16 GMT
ENV TELEGRAF_VERSION=1.17.3
# Sun, 11 Apr 2021 00:20:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sun, 11 Apr 2021 00:20:21 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sun, 11 Apr 2021 00:20:21 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sun, 11 Apr 2021 00:20:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 11 Apr 2021 00:20:21 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bd8f6a7501ccbe80b95c82519ed6fd4f7236a41e0ae59ba4a8df76af24629efc`  
		Last Modified: Sat, 10 Apr 2021 01:24:48 GMT  
		Size: 50.4 MB (50432971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44718e6d535d365250316b02459f98a1b0fa490158cc53057d18858507504d60`  
		Last Modified: Sat, 10 Apr 2021 02:01:57 GMT  
		Size: 7.8 MB (7832944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe9738af0cb2184ee8f3fb3dcb130455385aa428a27d14e1e07a5587ff16e64`  
		Last Modified: Sat, 10 Apr 2021 02:01:59 GMT  
		Size: 10.0 MB (9997183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b311f6d4be86d05278922f0a954851900a506a94ba9617ed7bc61f75a838316`  
		Last Modified: Sun, 11 Apr 2021 00:20:58 GMT  
		Size: 17.4 MB (17414435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ba220c8e4ca9f44f0b52538b1d8a42113d7f0f68ce1cad4bd6731a5c69b925`  
		Last Modified: Sun, 11 Apr 2021 00:20:54 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44849540cd0d7632667a0bb80be262400ea812d02a89dc8e2d04adb86cb985c`  
		Last Modified: Sun, 11 Apr 2021 00:21:17 GMT  
		Size: 23.0 MB (22958873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91dd9636c593c74c191b597cdf0c1b60b8320eea98208c8b4cacfd97b7acc1d8`  
		Last Modified: Sun, 11 Apr 2021 00:21:10 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.17.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:8b4b952357210ad2184f3452d12575eed481c5881fd00715ac51bd34450a8a0f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (100004462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5c01eae6fbe4b2e3d81c244b1787c8a83ab2e70cadf29a574bf03deaa59590`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 00:59:18 GMT
ADD file:bd2081229497eea2b33310cb1582b965581ca78b00b87cc8e42bdc8b9f350678 in / 
# Sat, 10 Apr 2021 00:59:20 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 06:05:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 06:05:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 11 Apr 2021 00:01:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sun, 11 Apr 2021 00:01:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 11 Apr 2021 00:02:00 GMT
ENV TELEGRAF_VERSION=1.17.3
# Sun, 11 Apr 2021 00:02:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sun, 11 Apr 2021 00:02:08 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sun, 11 Apr 2021 00:02:09 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sun, 11 Apr 2021 00:02:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 11 Apr 2021 00:02:11 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:de0ca59eb81518ffd92fbcd386251018f950dc16b1bd8ad2e642184db76be2a1`  
		Last Modified: Sat, 10 Apr 2021 01:07:26 GMT  
		Size: 45.9 MB (45915598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed23bfa8aaeab64a1ca00d3bead680f790be28326d14305705b2ee5227b4f2b7`  
		Last Modified: Sat, 10 Apr 2021 06:19:54 GMT  
		Size: 7.1 MB (7124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a12824e68a5072613049fad15fc8f0d209526ddd9d85787cc60d1b0d5073c0`  
		Last Modified: Sat, 10 Apr 2021 06:19:55 GMT  
		Size: 9.3 MB (9343784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9b5a49c2322e06d3fc820c5ff14f870c596c995b7507088b36bc3a1672b6ab`  
		Last Modified: Sun, 11 Apr 2021 00:03:02 GMT  
		Size: 16.2 MB (16159209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0870eb6e6fcdd0fb000437fe01af38c3221a86734c678514de094444ed63fed0`  
		Last Modified: Sun, 11 Apr 2021 00:02:52 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222dca62499f92461027a24a33ecfc1d7276ee05443a804eeca8d25509266293`  
		Last Modified: Sun, 11 Apr 2021 00:03:16 GMT  
		Size: 21.5 MB (21458608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57683c38379e2ce60baf111b9ebce05d778db3eed573b6b904748a1084b22317`  
		Last Modified: Sun, 11 Apr 2021 00:03:09 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.17.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6908f849fbb72b3572b6f69ad86c356baae97317361776ced8aced4d2a1054bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105229671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b46549f79d777d2d986afdec193808da89920dea0e135c7c3cd5bc542be06e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 00:40:59 GMT
ADD file:320ad0e2a3d6c676ddb8ce5646b5a94d18d82a8868955da3a9379a261dfe1ffe in / 
# Sat, 10 Apr 2021 00:41:01 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:46:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:46:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 23:33:45 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 23:33:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 23:34:07 GMT
ENV TELEGRAF_VERSION=1.17.3
# Sat, 10 Apr 2021 23:34:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 10 Apr 2021 23:34:13 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 10 Apr 2021 23:34:14 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sat, 10 Apr 2021 23:34:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 23:34:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01cf0f0da10ede0eec0fc1c5fbfdeb63a447dfcc0a3c4419c0a4c3f0a2826636`  
		Last Modified: Sat, 10 Apr 2021 00:47:28 GMT  
		Size: 49.2 MB (49225782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c667eb56cd05909001c1c50e81cbc75e290fd8e353f974bab4246a0d4fc484ca`  
		Last Modified: Sat, 10 Apr 2021 02:01:00 GMT  
		Size: 7.7 MB (7695101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ca15a4cef673e0e1a7bc3e659f4653df9bce82b945e367475e436852cc7880`  
		Last Modified: Sat, 10 Apr 2021 02:00:59 GMT  
		Size: 10.0 MB (9984406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7440732130595d801c674589c3625a20f8ba2557fc88cacd7025e2a93db2eb4`  
		Last Modified: Sat, 10 Apr 2021 23:34:56 GMT  
		Size: 17.3 MB (17269572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e708bbd80f49e36ab315d2c12f23cc9b58cc5db46272609d4162cf97e2e4177e`  
		Last Modified: Sat, 10 Apr 2021 23:34:50 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c7a1fb66fd93ba4a7f85ca802d23e66cd308a5d35d3dfbc749f9663eb16893`  
		Last Modified: Sat, 10 Apr 2021 23:35:09 GMT  
		Size: 21.1 MB (21051729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cd3aca40189890aa3b8eba90ba93142c3c3368917c63bf6d957d3669dd6d78`  
		Last Modified: Sat, 10 Apr 2021 23:35:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.17.3-alpine`

```console
$ docker pull telegraf@sha256:e5cc20de430b19e5cf2531e8898e06211294064ac9d7a8a69d7e73ec3827f343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.17.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:0c45633c35118bbe3cb87ffaa0c9dec06416ee4ff41b7a8d35ffbe2bf335ef69
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28921560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108daa767dcdeb9e7c67fcef201a04fe0b608f3ad13b6063543e075e1bef514e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:46:56 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Wed, 31 Mar 2021 22:47:22 GMT
ENV TELEGRAF_VERSION=1.17.3
# Wed, 31 Mar 2021 22:47:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 31 Mar 2021 22:47:29 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 31 Mar 2021 22:47:30 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Wed, 31 Mar 2021 22:47:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:47:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3d7ca742af0ce468e2012708013276fbd53bc83cbfbc6067bee7576dfc77fd`  
		Last Modified: Wed, 31 Mar 2021 22:48:32 GMT  
		Size: 3.3 MB (3300612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d91d88132675be9b65b0d93277ac84b4b02ebaec36a901faf284f9926353be`  
		Last Modified: Wed, 31 Mar 2021 22:49:10 GMT  
		Size: 22.8 MB (22820900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5acc6235f76ad9d31e59cbea5a553dd404f4856299d178c28db76f1f66c3b3`  
		Last Modified: Wed, 31 Mar 2021 22:49:05 GMT  
		Size: 181.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18`

```console
$ docker pull telegraf@sha256:e46f7d19a612529019555da42e4e1e49e0b638c375098adb8cac06ca38ae8cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.18` - linux; amd64

```console
$ docker pull telegraf@sha256:5a2001b9883029c19046e762f53336d3e612c394c7eb3ddadf1948e2978458a4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111375761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750c89a1a1933b3bb67614adb8af362e39be15da61411aac3827ce78bb80a34c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:08 GMT
ADD file:e18bc3e10e7c743f18bb8be65ec94a62c03764af7dbdb4957f9a600237730212 in / 
# Sat, 10 Apr 2021 01:20:09 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:54:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:54:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 11 Apr 2021 00:20:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sun, 11 Apr 2021 00:20:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 11 Apr 2021 00:20:27 GMT
ENV TELEGRAF_VERSION=1.18.1
# Sun, 11 Apr 2021 00:20:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sun, 11 Apr 2021 00:20:31 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sun, 11 Apr 2021 00:20:31 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sun, 11 Apr 2021 00:20:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 11 Apr 2021 00:20:31 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bd8f6a7501ccbe80b95c82519ed6fd4f7236a41e0ae59ba4a8df76af24629efc`  
		Last Modified: Sat, 10 Apr 2021 01:24:48 GMT  
		Size: 50.4 MB (50432971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44718e6d535d365250316b02459f98a1b0fa490158cc53057d18858507504d60`  
		Last Modified: Sat, 10 Apr 2021 02:01:57 GMT  
		Size: 7.8 MB (7832944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe9738af0cb2184ee8f3fb3dcb130455385aa428a27d14e1e07a5587ff16e64`  
		Last Modified: Sat, 10 Apr 2021 02:01:59 GMT  
		Size: 10.0 MB (9997183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b311f6d4be86d05278922f0a954851900a506a94ba9617ed7bc61f75a838316`  
		Last Modified: Sun, 11 Apr 2021 00:20:58 GMT  
		Size: 17.4 MB (17414435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ba220c8e4ca9f44f0b52538b1d8a42113d7f0f68ce1cad4bd6731a5c69b925`  
		Last Modified: Sun, 11 Apr 2021 00:20:54 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb53c97f11558e14932c2af2f429a79d3906f2e0dbc8d55679be97b8109dff22`  
		Last Modified: Sun, 11 Apr 2021 00:21:33 GMT  
		Size: 25.7 MB (25695146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11dca13555d95d5ae82a20d57c0ee01aea42d334386b2e83dca5edc563cc8fb`  
		Last Modified: Sun, 11 Apr 2021 00:21:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.18` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:73f5987acb4f1005af0e3ef841c62f41d7d95c3342036fdaab20feef5583bb5a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102319486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b416b2a1fac33be9675028a4f2b990b12e35db8b37f27892c0dc9c310c54c518`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 00:59:18 GMT
ADD file:bd2081229497eea2b33310cb1582b965581ca78b00b87cc8e42bdc8b9f350678 in / 
# Sat, 10 Apr 2021 00:59:20 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 06:05:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 06:05:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 11 Apr 2021 00:01:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sun, 11 Apr 2021 00:01:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 11 Apr 2021 00:02:20 GMT
ENV TELEGRAF_VERSION=1.18.1
# Sun, 11 Apr 2021 00:02:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sun, 11 Apr 2021 00:02:32 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sun, 11 Apr 2021 00:02:34 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sun, 11 Apr 2021 00:02:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 11 Apr 2021 00:02:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:de0ca59eb81518ffd92fbcd386251018f950dc16b1bd8ad2e642184db76be2a1`  
		Last Modified: Sat, 10 Apr 2021 01:07:26 GMT  
		Size: 45.9 MB (45915598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed23bfa8aaeab64a1ca00d3bead680f790be28326d14305705b2ee5227b4f2b7`  
		Last Modified: Sat, 10 Apr 2021 06:19:54 GMT  
		Size: 7.1 MB (7124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a12824e68a5072613049fad15fc8f0d209526ddd9d85787cc60d1b0d5073c0`  
		Last Modified: Sat, 10 Apr 2021 06:19:55 GMT  
		Size: 9.3 MB (9343784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9b5a49c2322e06d3fc820c5ff14f870c596c995b7507088b36bc3a1672b6ab`  
		Last Modified: Sun, 11 Apr 2021 00:03:02 GMT  
		Size: 16.2 MB (16159209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0870eb6e6fcdd0fb000437fe01af38c3221a86734c678514de094444ed63fed0`  
		Last Modified: Sun, 11 Apr 2021 00:02:52 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ccd84c6386d4b15034b660cc35cf0ff47e996ff02f88f3fea216ba7eb366cf`  
		Last Modified: Sun, 11 Apr 2021 00:03:33 GMT  
		Size: 23.8 MB (23773632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d36aef8d3f194528ec12de46552a8081e9dbfd29b44fd5bd8621e0f751e16a2`  
		Last Modified: Sun, 11 Apr 2021 00:03:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.18` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d2993805d79dbda776e228e166e1e0996fc1909485c475fd9b14092331a00640
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107497126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17eee52a225a86b5debbf77dba3f4f045b6bc5c04652cf5a53a34ee28f2a8bbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 00:40:59 GMT
ADD file:320ad0e2a3d6c676ddb8ce5646b5a94d18d82a8868955da3a9379a261dfe1ffe in / 
# Sat, 10 Apr 2021 00:41:01 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:46:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:46:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 23:33:45 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 23:33:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 23:34:23 GMT
ENV TELEGRAF_VERSION=1.18.1
# Sat, 10 Apr 2021 23:34:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 10 Apr 2021 23:34:30 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 10 Apr 2021 23:34:31 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sat, 10 Apr 2021 23:34:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 23:34:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01cf0f0da10ede0eec0fc1c5fbfdeb63a447dfcc0a3c4419c0a4c3f0a2826636`  
		Last Modified: Sat, 10 Apr 2021 00:47:28 GMT  
		Size: 49.2 MB (49225782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c667eb56cd05909001c1c50e81cbc75e290fd8e353f974bab4246a0d4fc484ca`  
		Last Modified: Sat, 10 Apr 2021 02:01:00 GMT  
		Size: 7.7 MB (7695101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ca15a4cef673e0e1a7bc3e659f4653df9bce82b945e367475e436852cc7880`  
		Last Modified: Sat, 10 Apr 2021 02:00:59 GMT  
		Size: 10.0 MB (9984406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7440732130595d801c674589c3625a20f8ba2557fc88cacd7025e2a93db2eb4`  
		Last Modified: Sat, 10 Apr 2021 23:34:56 GMT  
		Size: 17.3 MB (17269572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e708bbd80f49e36ab315d2c12f23cc9b58cc5db46272609d4162cf97e2e4177e`  
		Last Modified: Sat, 10 Apr 2021 23:34:50 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d53490cc5f8b6df0efc9ba02c0b5740cc6a052412b3e3a9a1815b7345c87d9f`  
		Last Modified: Sat, 10 Apr 2021 23:35:22 GMT  
		Size: 23.3 MB (23319184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9eb3e242371a26184d3ada2abbb6fd2633c984de35083eedaa4bbbac94b93fa`  
		Last Modified: Sat, 10 Apr 2021 23:35:17 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18-alpine`

```console
$ docker pull telegraf@sha256:0fd73530266c0dfe568869fc4cbf6470ab8ffc265a3980a252dc66842c2dc1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.18-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:0e343a4cc8ae1f599dc3ab9c83f2145f4f97e706a6093143a1228001743cfb00
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31653260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a741054359e030f59cb7176234ac27a83b3959c658ee042f4aa33b1d73828766`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:46:56 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Thu, 08 Apr 2021 22:21:21 GMT
ENV TELEGRAF_VERSION=1.18.1
# Thu, 08 Apr 2021 22:21:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 08 Apr 2021 22:21:25 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 08 Apr 2021 22:21:25 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 08 Apr 2021 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Apr 2021 22:21:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3d7ca742af0ce468e2012708013276fbd53bc83cbfbc6067bee7576dfc77fd`  
		Last Modified: Wed, 31 Mar 2021 22:48:32 GMT  
		Size: 3.3 MB (3300612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4feec04eb0a5472aa868a7b838780f6895ff1330e612274e04bf7bb3f81043f1`  
		Last Modified: Thu, 08 Apr 2021 22:22:41 GMT  
		Size: 25.6 MB (25552599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8f28895c4eba8dc353ce86fb39f4c86bf48d11e0594562d1cae1b6a4cde3de`  
		Last Modified: Thu, 08 Apr 2021 22:22:35 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18.1`

```console
$ docker pull telegraf@sha256:e46f7d19a612529019555da42e4e1e49e0b638c375098adb8cac06ca38ae8cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.18.1` - linux; amd64

```console
$ docker pull telegraf@sha256:5a2001b9883029c19046e762f53336d3e612c394c7eb3ddadf1948e2978458a4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111375761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750c89a1a1933b3bb67614adb8af362e39be15da61411aac3827ce78bb80a34c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:08 GMT
ADD file:e18bc3e10e7c743f18bb8be65ec94a62c03764af7dbdb4957f9a600237730212 in / 
# Sat, 10 Apr 2021 01:20:09 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:54:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:54:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 11 Apr 2021 00:20:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sun, 11 Apr 2021 00:20:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 11 Apr 2021 00:20:27 GMT
ENV TELEGRAF_VERSION=1.18.1
# Sun, 11 Apr 2021 00:20:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sun, 11 Apr 2021 00:20:31 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sun, 11 Apr 2021 00:20:31 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sun, 11 Apr 2021 00:20:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 11 Apr 2021 00:20:31 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bd8f6a7501ccbe80b95c82519ed6fd4f7236a41e0ae59ba4a8df76af24629efc`  
		Last Modified: Sat, 10 Apr 2021 01:24:48 GMT  
		Size: 50.4 MB (50432971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44718e6d535d365250316b02459f98a1b0fa490158cc53057d18858507504d60`  
		Last Modified: Sat, 10 Apr 2021 02:01:57 GMT  
		Size: 7.8 MB (7832944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe9738af0cb2184ee8f3fb3dcb130455385aa428a27d14e1e07a5587ff16e64`  
		Last Modified: Sat, 10 Apr 2021 02:01:59 GMT  
		Size: 10.0 MB (9997183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b311f6d4be86d05278922f0a954851900a506a94ba9617ed7bc61f75a838316`  
		Last Modified: Sun, 11 Apr 2021 00:20:58 GMT  
		Size: 17.4 MB (17414435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ba220c8e4ca9f44f0b52538b1d8a42113d7f0f68ce1cad4bd6731a5c69b925`  
		Last Modified: Sun, 11 Apr 2021 00:20:54 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb53c97f11558e14932c2af2f429a79d3906f2e0dbc8d55679be97b8109dff22`  
		Last Modified: Sun, 11 Apr 2021 00:21:33 GMT  
		Size: 25.7 MB (25695146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11dca13555d95d5ae82a20d57c0ee01aea42d334386b2e83dca5edc563cc8fb`  
		Last Modified: Sun, 11 Apr 2021 00:21:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.18.1` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:73f5987acb4f1005af0e3ef841c62f41d7d95c3342036fdaab20feef5583bb5a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102319486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b416b2a1fac33be9675028a4f2b990b12e35db8b37f27892c0dc9c310c54c518`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 00:59:18 GMT
ADD file:bd2081229497eea2b33310cb1582b965581ca78b00b87cc8e42bdc8b9f350678 in / 
# Sat, 10 Apr 2021 00:59:20 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 06:05:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 06:05:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 11 Apr 2021 00:01:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sun, 11 Apr 2021 00:01:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 11 Apr 2021 00:02:20 GMT
ENV TELEGRAF_VERSION=1.18.1
# Sun, 11 Apr 2021 00:02:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sun, 11 Apr 2021 00:02:32 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sun, 11 Apr 2021 00:02:34 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sun, 11 Apr 2021 00:02:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 11 Apr 2021 00:02:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:de0ca59eb81518ffd92fbcd386251018f950dc16b1bd8ad2e642184db76be2a1`  
		Last Modified: Sat, 10 Apr 2021 01:07:26 GMT  
		Size: 45.9 MB (45915598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed23bfa8aaeab64a1ca00d3bead680f790be28326d14305705b2ee5227b4f2b7`  
		Last Modified: Sat, 10 Apr 2021 06:19:54 GMT  
		Size: 7.1 MB (7124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a12824e68a5072613049fad15fc8f0d209526ddd9d85787cc60d1b0d5073c0`  
		Last Modified: Sat, 10 Apr 2021 06:19:55 GMT  
		Size: 9.3 MB (9343784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9b5a49c2322e06d3fc820c5ff14f870c596c995b7507088b36bc3a1672b6ab`  
		Last Modified: Sun, 11 Apr 2021 00:03:02 GMT  
		Size: 16.2 MB (16159209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0870eb6e6fcdd0fb000437fe01af38c3221a86734c678514de094444ed63fed0`  
		Last Modified: Sun, 11 Apr 2021 00:02:52 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ccd84c6386d4b15034b660cc35cf0ff47e996ff02f88f3fea216ba7eb366cf`  
		Last Modified: Sun, 11 Apr 2021 00:03:33 GMT  
		Size: 23.8 MB (23773632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d36aef8d3f194528ec12de46552a8081e9dbfd29b44fd5bd8621e0f751e16a2`  
		Last Modified: Sun, 11 Apr 2021 00:03:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.18.1` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d2993805d79dbda776e228e166e1e0996fc1909485c475fd9b14092331a00640
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107497126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17eee52a225a86b5debbf77dba3f4f045b6bc5c04652cf5a53a34ee28f2a8bbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 00:40:59 GMT
ADD file:320ad0e2a3d6c676ddb8ce5646b5a94d18d82a8868955da3a9379a261dfe1ffe in / 
# Sat, 10 Apr 2021 00:41:01 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:46:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:46:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 23:33:45 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 23:33:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 23:34:23 GMT
ENV TELEGRAF_VERSION=1.18.1
# Sat, 10 Apr 2021 23:34:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 10 Apr 2021 23:34:30 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 10 Apr 2021 23:34:31 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sat, 10 Apr 2021 23:34:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 23:34:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01cf0f0da10ede0eec0fc1c5fbfdeb63a447dfcc0a3c4419c0a4c3f0a2826636`  
		Last Modified: Sat, 10 Apr 2021 00:47:28 GMT  
		Size: 49.2 MB (49225782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c667eb56cd05909001c1c50e81cbc75e290fd8e353f974bab4246a0d4fc484ca`  
		Last Modified: Sat, 10 Apr 2021 02:01:00 GMT  
		Size: 7.7 MB (7695101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ca15a4cef673e0e1a7bc3e659f4653df9bce82b945e367475e436852cc7880`  
		Last Modified: Sat, 10 Apr 2021 02:00:59 GMT  
		Size: 10.0 MB (9984406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7440732130595d801c674589c3625a20f8ba2557fc88cacd7025e2a93db2eb4`  
		Last Modified: Sat, 10 Apr 2021 23:34:56 GMT  
		Size: 17.3 MB (17269572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e708bbd80f49e36ab315d2c12f23cc9b58cc5db46272609d4162cf97e2e4177e`  
		Last Modified: Sat, 10 Apr 2021 23:34:50 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d53490cc5f8b6df0efc9ba02c0b5740cc6a052412b3e3a9a1815b7345c87d9f`  
		Last Modified: Sat, 10 Apr 2021 23:35:22 GMT  
		Size: 23.3 MB (23319184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9eb3e242371a26184d3ada2abbb6fd2633c984de35083eedaa4bbbac94b93fa`  
		Last Modified: Sat, 10 Apr 2021 23:35:17 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18.1-alpine`

```console
$ docker pull telegraf@sha256:0fd73530266c0dfe568869fc4cbf6470ab8ffc265a3980a252dc66842c2dc1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.18.1-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:0e343a4cc8ae1f599dc3ab9c83f2145f4f97e706a6093143a1228001743cfb00
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31653260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a741054359e030f59cb7176234ac27a83b3959c658ee042f4aa33b1d73828766`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:46:56 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Thu, 08 Apr 2021 22:21:21 GMT
ENV TELEGRAF_VERSION=1.18.1
# Thu, 08 Apr 2021 22:21:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 08 Apr 2021 22:21:25 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 08 Apr 2021 22:21:25 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 08 Apr 2021 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Apr 2021 22:21:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3d7ca742af0ce468e2012708013276fbd53bc83cbfbc6067bee7576dfc77fd`  
		Last Modified: Wed, 31 Mar 2021 22:48:32 GMT  
		Size: 3.3 MB (3300612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4feec04eb0a5472aa868a7b838780f6895ff1330e612274e04bf7bb3f81043f1`  
		Last Modified: Thu, 08 Apr 2021 22:22:41 GMT  
		Size: 25.6 MB (25552599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8f28895c4eba8dc353ce86fb39f4c86bf48d11e0594562d1cae1b6a4cde3de`  
		Last Modified: Thu, 08 Apr 2021 22:22:35 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:0fd73530266c0dfe568869fc4cbf6470ab8ffc265a3980a252dc66842c2dc1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:0e343a4cc8ae1f599dc3ab9c83f2145f4f97e706a6093143a1228001743cfb00
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31653260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a741054359e030f59cb7176234ac27a83b3959c658ee042f4aa33b1d73828766`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:46:56 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Thu, 08 Apr 2021 22:21:21 GMT
ENV TELEGRAF_VERSION=1.18.1
# Thu, 08 Apr 2021 22:21:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 08 Apr 2021 22:21:25 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 08 Apr 2021 22:21:25 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 08 Apr 2021 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Apr 2021 22:21:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3d7ca742af0ce468e2012708013276fbd53bc83cbfbc6067bee7576dfc77fd`  
		Last Modified: Wed, 31 Mar 2021 22:48:32 GMT  
		Size: 3.3 MB (3300612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4feec04eb0a5472aa868a7b838780f6895ff1330e612274e04bf7bb3f81043f1`  
		Last Modified: Thu, 08 Apr 2021 22:22:41 GMT  
		Size: 25.6 MB (25552599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8f28895c4eba8dc353ce86fb39f4c86bf48d11e0594562d1cae1b6a4cde3de`  
		Last Modified: Thu, 08 Apr 2021 22:22:35 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:e46f7d19a612529019555da42e4e1e49e0b638c375098adb8cac06ca38ae8cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:5a2001b9883029c19046e762f53336d3e612c394c7eb3ddadf1948e2978458a4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111375761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750c89a1a1933b3bb67614adb8af362e39be15da61411aac3827ce78bb80a34c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:08 GMT
ADD file:e18bc3e10e7c743f18bb8be65ec94a62c03764af7dbdb4957f9a600237730212 in / 
# Sat, 10 Apr 2021 01:20:09 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:54:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:54:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 11 Apr 2021 00:20:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sun, 11 Apr 2021 00:20:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 11 Apr 2021 00:20:27 GMT
ENV TELEGRAF_VERSION=1.18.1
# Sun, 11 Apr 2021 00:20:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sun, 11 Apr 2021 00:20:31 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sun, 11 Apr 2021 00:20:31 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sun, 11 Apr 2021 00:20:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 11 Apr 2021 00:20:31 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bd8f6a7501ccbe80b95c82519ed6fd4f7236a41e0ae59ba4a8df76af24629efc`  
		Last Modified: Sat, 10 Apr 2021 01:24:48 GMT  
		Size: 50.4 MB (50432971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44718e6d535d365250316b02459f98a1b0fa490158cc53057d18858507504d60`  
		Last Modified: Sat, 10 Apr 2021 02:01:57 GMT  
		Size: 7.8 MB (7832944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe9738af0cb2184ee8f3fb3dcb130455385aa428a27d14e1e07a5587ff16e64`  
		Last Modified: Sat, 10 Apr 2021 02:01:59 GMT  
		Size: 10.0 MB (9997183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b311f6d4be86d05278922f0a954851900a506a94ba9617ed7bc61f75a838316`  
		Last Modified: Sun, 11 Apr 2021 00:20:58 GMT  
		Size: 17.4 MB (17414435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ba220c8e4ca9f44f0b52538b1d8a42113d7f0f68ce1cad4bd6731a5c69b925`  
		Last Modified: Sun, 11 Apr 2021 00:20:54 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb53c97f11558e14932c2af2f429a79d3906f2e0dbc8d55679be97b8109dff22`  
		Last Modified: Sun, 11 Apr 2021 00:21:33 GMT  
		Size: 25.7 MB (25695146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11dca13555d95d5ae82a20d57c0ee01aea42d334386b2e83dca5edc563cc8fb`  
		Last Modified: Sun, 11 Apr 2021 00:21:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:73f5987acb4f1005af0e3ef841c62f41d7d95c3342036fdaab20feef5583bb5a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102319486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b416b2a1fac33be9675028a4f2b990b12e35db8b37f27892c0dc9c310c54c518`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 00:59:18 GMT
ADD file:bd2081229497eea2b33310cb1582b965581ca78b00b87cc8e42bdc8b9f350678 in / 
# Sat, 10 Apr 2021 00:59:20 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 06:05:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 06:05:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 11 Apr 2021 00:01:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sun, 11 Apr 2021 00:01:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 11 Apr 2021 00:02:20 GMT
ENV TELEGRAF_VERSION=1.18.1
# Sun, 11 Apr 2021 00:02:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sun, 11 Apr 2021 00:02:32 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sun, 11 Apr 2021 00:02:34 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sun, 11 Apr 2021 00:02:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 11 Apr 2021 00:02:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:de0ca59eb81518ffd92fbcd386251018f950dc16b1bd8ad2e642184db76be2a1`  
		Last Modified: Sat, 10 Apr 2021 01:07:26 GMT  
		Size: 45.9 MB (45915598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed23bfa8aaeab64a1ca00d3bead680f790be28326d14305705b2ee5227b4f2b7`  
		Last Modified: Sat, 10 Apr 2021 06:19:54 GMT  
		Size: 7.1 MB (7124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a12824e68a5072613049fad15fc8f0d209526ddd9d85787cc60d1b0d5073c0`  
		Last Modified: Sat, 10 Apr 2021 06:19:55 GMT  
		Size: 9.3 MB (9343784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9b5a49c2322e06d3fc820c5ff14f870c596c995b7507088b36bc3a1672b6ab`  
		Last Modified: Sun, 11 Apr 2021 00:03:02 GMT  
		Size: 16.2 MB (16159209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0870eb6e6fcdd0fb000437fe01af38c3221a86734c678514de094444ed63fed0`  
		Last Modified: Sun, 11 Apr 2021 00:02:52 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ccd84c6386d4b15034b660cc35cf0ff47e996ff02f88f3fea216ba7eb366cf`  
		Last Modified: Sun, 11 Apr 2021 00:03:33 GMT  
		Size: 23.8 MB (23773632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d36aef8d3f194528ec12de46552a8081e9dbfd29b44fd5bd8621e0f751e16a2`  
		Last Modified: Sun, 11 Apr 2021 00:03:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d2993805d79dbda776e228e166e1e0996fc1909485c475fd9b14092331a00640
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107497126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17eee52a225a86b5debbf77dba3f4f045b6bc5c04652cf5a53a34ee28f2a8bbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 10 Apr 2021 00:40:59 GMT
ADD file:320ad0e2a3d6c676ddb8ce5646b5a94d18d82a8868955da3a9379a261dfe1ffe in / 
# Sat, 10 Apr 2021 00:41:01 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:46:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:46:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 23:33:45 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 23:33:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 23:34:23 GMT
ENV TELEGRAF_VERSION=1.18.1
# Sat, 10 Apr 2021 23:34:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 10 Apr 2021 23:34:30 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 10 Apr 2021 23:34:31 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Sat, 10 Apr 2021 23:34:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 23:34:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01cf0f0da10ede0eec0fc1c5fbfdeb63a447dfcc0a3c4419c0a4c3f0a2826636`  
		Last Modified: Sat, 10 Apr 2021 00:47:28 GMT  
		Size: 49.2 MB (49225782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c667eb56cd05909001c1c50e81cbc75e290fd8e353f974bab4246a0d4fc484ca`  
		Last Modified: Sat, 10 Apr 2021 02:01:00 GMT  
		Size: 7.7 MB (7695101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ca15a4cef673e0e1a7bc3e659f4653df9bce82b945e367475e436852cc7880`  
		Last Modified: Sat, 10 Apr 2021 02:00:59 GMT  
		Size: 10.0 MB (9984406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7440732130595d801c674589c3625a20f8ba2557fc88cacd7025e2a93db2eb4`  
		Last Modified: Sat, 10 Apr 2021 23:34:56 GMT  
		Size: 17.3 MB (17269572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e708bbd80f49e36ab315d2c12f23cc9b58cc5db46272609d4162cf97e2e4177e`  
		Last Modified: Sat, 10 Apr 2021 23:34:50 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d53490cc5f8b6df0efc9ba02c0b5740cc6a052412b3e3a9a1815b7345c87d9f`  
		Last Modified: Sat, 10 Apr 2021 23:35:22 GMT  
		Size: 23.3 MB (23319184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9eb3e242371a26184d3ada2abbb6fd2633c984de35083eedaa4bbbac94b93fa`  
		Last Modified: Sat, 10 Apr 2021 23:35:17 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
