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
-	[`telegraf:1.18.2`](#telegraf1182)
-	[`telegraf:1.18.2-alpine`](#telegraf1182-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.16`

```console
$ docker pull telegraf@sha256:93f4c460d87bbd6acebdb6149a9015118154d83511ddccd6abd582a558da60a3
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
$ docker pull telegraf@sha256:0ccbc7039daf2927b4ca9ceebe2947a7f64f843114c131468467a5e20b188a03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104671697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4287e59e43b1b729d92f78aa8eaa25f771c688440dab55c6de6687783423b71b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 12 May 2021 00:50:48 GMT
ADD file:ff9983cd659b3fc32ddfbbdeda76a971afd7d399e6d8b98faea3a9ead0e598f6 in / 
# Wed, 12 May 2021 00:50:52 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:34:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 13 May 2021 00:40:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 13 May 2021 00:40:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 13 May 2021 00:40:19 GMT
ENV TELEGRAF_VERSION=1.16.3
# Thu, 13 May 2021 00:40:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 13 May 2021 00:40:26 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 13 May 2021 00:40:27 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 13 May 2021 00:40:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 May 2021 00:40:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c54d9402d498e45ed396b5b6fe836f55e4ccadbad745decda3e9f83d880bc677`  
		Last Modified: Wed, 12 May 2021 01:01:40 GMT  
		Size: 49.2 MB (49225351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91bbb3592d6685d1c683c8c20e60901274c636605800608685274c194d43d25`  
		Last Modified: Wed, 12 May 2021 01:48:24 GMT  
		Size: 7.7 MB (7695057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d8c28b9129321858810cff4cd78385949579ed18d991f98c77f912c7a754f8`  
		Last Modified: Wed, 12 May 2021 01:48:24 GMT  
		Size: 10.0 MB (9984343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c2afe1661b16b31414e984301464c54a688d670588da65e09acae49436f1c7`  
		Last Modified: Thu, 13 May 2021 00:41:27 GMT  
		Size: 17.3 MB (17269543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf8effe0189a9fabb276a8737e536476f360929816dd52b787ac4daba9033a9`  
		Last Modified: Thu, 13 May 2021 00:41:21 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f46fe8590c4d08f3ec5b1236f275fbd6039280d1cdd50accdf8aecf387804ee`  
		Last Modified: Thu, 13 May 2021 00:41:28 GMT  
		Size: 20.5 MB (20494321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5fcfbd4a652b1fea4fa3ebd30106da252697eab4003869f4ea4ffd36c6e922`  
		Last Modified: Thu, 13 May 2021 00:41:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.16-alpine`

```console
$ docker pull telegraf@sha256:74986f10bd8c816c25045b360d6dcdcbb539847ad2eb3a5bc57f7e5df2098db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.16-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:632276664eed5de425e15e07a8c855b47fa6fa7052be58fc853b3f1f43ca5d38
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28315966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee38dab3d69bb23a844bbaf3380490aa491faebfacb6a9b74ef5c49db4209654`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 15 Apr 2021 02:35:34 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Thu, 15 Apr 2021 02:35:35 GMT
ENV TELEGRAF_VERSION=1.16.3
# Thu, 15 Apr 2021 02:35:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 15 Apr 2021 02:35:43 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 15 Apr 2021 02:35:44 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 15 Apr 2021 02:35:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Apr 2021 02:35:45 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661683aad4bf8006657c2bf1c3d74bfd343aaa18c1d5a30eda2d437ea8149e2e`  
		Last Modified: Thu, 15 Apr 2021 02:37:00 GMT  
		Size: 3.3 MB (3300674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f169b5147d816d37a1fb74e47069d4702f512e8e2a9908fc1d27c70148008d5d`  
		Last Modified: Thu, 15 Apr 2021 02:37:04 GMT  
		Size: 22.2 MB (22214387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ac9ecc8e32fd45ac0347229d13646ddc5b2fdeef400dabf000cfcc0768233`  
		Last Modified: Thu, 15 Apr 2021 02:36:59 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.16.3`

```console
$ docker pull telegraf@sha256:93f4c460d87bbd6acebdb6149a9015118154d83511ddccd6abd582a558da60a3
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
$ docker pull telegraf@sha256:0ccbc7039daf2927b4ca9ceebe2947a7f64f843114c131468467a5e20b188a03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104671697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4287e59e43b1b729d92f78aa8eaa25f771c688440dab55c6de6687783423b71b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 12 May 2021 00:50:48 GMT
ADD file:ff9983cd659b3fc32ddfbbdeda76a971afd7d399e6d8b98faea3a9ead0e598f6 in / 
# Wed, 12 May 2021 00:50:52 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:34:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 13 May 2021 00:40:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 13 May 2021 00:40:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 13 May 2021 00:40:19 GMT
ENV TELEGRAF_VERSION=1.16.3
# Thu, 13 May 2021 00:40:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 13 May 2021 00:40:26 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 13 May 2021 00:40:27 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 13 May 2021 00:40:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 May 2021 00:40:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c54d9402d498e45ed396b5b6fe836f55e4ccadbad745decda3e9f83d880bc677`  
		Last Modified: Wed, 12 May 2021 01:01:40 GMT  
		Size: 49.2 MB (49225351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91bbb3592d6685d1c683c8c20e60901274c636605800608685274c194d43d25`  
		Last Modified: Wed, 12 May 2021 01:48:24 GMT  
		Size: 7.7 MB (7695057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d8c28b9129321858810cff4cd78385949579ed18d991f98c77f912c7a754f8`  
		Last Modified: Wed, 12 May 2021 01:48:24 GMT  
		Size: 10.0 MB (9984343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c2afe1661b16b31414e984301464c54a688d670588da65e09acae49436f1c7`  
		Last Modified: Thu, 13 May 2021 00:41:27 GMT  
		Size: 17.3 MB (17269543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf8effe0189a9fabb276a8737e536476f360929816dd52b787ac4daba9033a9`  
		Last Modified: Thu, 13 May 2021 00:41:21 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f46fe8590c4d08f3ec5b1236f275fbd6039280d1cdd50accdf8aecf387804ee`  
		Last Modified: Thu, 13 May 2021 00:41:28 GMT  
		Size: 20.5 MB (20494321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5fcfbd4a652b1fea4fa3ebd30106da252697eab4003869f4ea4ffd36c6e922`  
		Last Modified: Thu, 13 May 2021 00:41:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.16.3-alpine`

```console
$ docker pull telegraf@sha256:74986f10bd8c816c25045b360d6dcdcbb539847ad2eb3a5bc57f7e5df2098db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.16.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:632276664eed5de425e15e07a8c855b47fa6fa7052be58fc853b3f1f43ca5d38
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28315966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee38dab3d69bb23a844bbaf3380490aa491faebfacb6a9b74ef5c49db4209654`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 15 Apr 2021 02:35:34 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Thu, 15 Apr 2021 02:35:35 GMT
ENV TELEGRAF_VERSION=1.16.3
# Thu, 15 Apr 2021 02:35:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 15 Apr 2021 02:35:43 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 15 Apr 2021 02:35:44 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 15 Apr 2021 02:35:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Apr 2021 02:35:45 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661683aad4bf8006657c2bf1c3d74bfd343aaa18c1d5a30eda2d437ea8149e2e`  
		Last Modified: Thu, 15 Apr 2021 02:37:00 GMT  
		Size: 3.3 MB (3300674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f169b5147d816d37a1fb74e47069d4702f512e8e2a9908fc1d27c70148008d5d`  
		Last Modified: Thu, 15 Apr 2021 02:37:04 GMT  
		Size: 22.2 MB (22214387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ac9ecc8e32fd45ac0347229d13646ddc5b2fdeef400dabf000cfcc0768233`  
		Last Modified: Thu, 15 Apr 2021 02:36:59 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.17`

```console
$ docker pull telegraf@sha256:ca77ba11ef51104b79343fb989a117f44acc3b1c2a3c393b56f2da73421197a9
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
$ docker pull telegraf@sha256:7a4ddd3a6a57aafd9218a597512c7f3f661a4d3436ff84a7bc6cc6236f65091b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105229157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae02e1496282378ae7f6cd4d30124b7840c4022a5c9d781f1ba1d1dcc1361f58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 12 May 2021 00:50:48 GMT
ADD file:ff9983cd659b3fc32ddfbbdeda76a971afd7d399e6d8b98faea3a9ead0e598f6 in / 
# Wed, 12 May 2021 00:50:52 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:34:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 13 May 2021 00:40:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 13 May 2021 00:40:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 13 May 2021 00:40:41 GMT
ENV TELEGRAF_VERSION=1.17.3
# Thu, 13 May 2021 00:40:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 13 May 2021 00:40:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 13 May 2021 00:40:48 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 13 May 2021 00:40:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 May 2021 00:40:50 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c54d9402d498e45ed396b5b6fe836f55e4ccadbad745decda3e9f83d880bc677`  
		Last Modified: Wed, 12 May 2021 01:01:40 GMT  
		Size: 49.2 MB (49225351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91bbb3592d6685d1c683c8c20e60901274c636605800608685274c194d43d25`  
		Last Modified: Wed, 12 May 2021 01:48:24 GMT  
		Size: 7.7 MB (7695057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d8c28b9129321858810cff4cd78385949579ed18d991f98c77f912c7a754f8`  
		Last Modified: Wed, 12 May 2021 01:48:24 GMT  
		Size: 10.0 MB (9984343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c2afe1661b16b31414e984301464c54a688d670588da65e09acae49436f1c7`  
		Last Modified: Thu, 13 May 2021 00:41:27 GMT  
		Size: 17.3 MB (17269543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf8effe0189a9fabb276a8737e536476f360929816dd52b787ac4daba9033a9`  
		Last Modified: Thu, 13 May 2021 00:41:21 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb6c42128987e5ad02c5b9a783e7c1034636013cbea40bd2ffea99e616db2a0`  
		Last Modified: Thu, 13 May 2021 00:41:40 GMT  
		Size: 21.1 MB (21051781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0208003bfb3efd741ac782d0e8759350d1952cff542161180d77dcd8d05346`  
		Last Modified: Thu, 13 May 2021 00:41:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.17-alpine`

```console
$ docker pull telegraf@sha256:896a3e7a22bcff0969f454cd4b6376f4bd5585ae2d9205ebcb9ca0c90c6a946b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.17-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:771e1a4b1f8c3d4372e0a77e4f1dd4244d5d8fae811e71557e55bdefa75713b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28922500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466e80f78606722902c94806d368dcb7ef48aa4d14471c58a22959d6b977e165`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 15 Apr 2021 02:35:34 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Thu, 15 Apr 2021 02:35:53 GMT
ENV TELEGRAF_VERSION=1.17.3
# Thu, 15 Apr 2021 02:36:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 15 Apr 2021 02:36:05 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 15 Apr 2021 02:36:06 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 15 Apr 2021 02:36:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Apr 2021 02:36:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661683aad4bf8006657c2bf1c3d74bfd343aaa18c1d5a30eda2d437ea8149e2e`  
		Last Modified: Thu, 15 Apr 2021 02:37:00 GMT  
		Size: 3.3 MB (3300674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6276b38c606abd85c7ad60fa2b7708521d0c65481403e10222ec72b0bb52c8c`  
		Last Modified: Thu, 15 Apr 2021 02:37:24 GMT  
		Size: 22.8 MB (22820923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587929023026541619ae340883ecebb2d32f2ed0c06960d5ad5ef38269f09ab6`  
		Last Modified: Thu, 15 Apr 2021 02:37:16 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.17.3`

```console
$ docker pull telegraf@sha256:ca77ba11ef51104b79343fb989a117f44acc3b1c2a3c393b56f2da73421197a9
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
$ docker pull telegraf@sha256:7a4ddd3a6a57aafd9218a597512c7f3f661a4d3436ff84a7bc6cc6236f65091b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105229157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae02e1496282378ae7f6cd4d30124b7840c4022a5c9d781f1ba1d1dcc1361f58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 12 May 2021 00:50:48 GMT
ADD file:ff9983cd659b3fc32ddfbbdeda76a971afd7d399e6d8b98faea3a9ead0e598f6 in / 
# Wed, 12 May 2021 00:50:52 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:34:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 13 May 2021 00:40:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 13 May 2021 00:40:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 13 May 2021 00:40:41 GMT
ENV TELEGRAF_VERSION=1.17.3
# Thu, 13 May 2021 00:40:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 13 May 2021 00:40:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 13 May 2021 00:40:48 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 13 May 2021 00:40:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 May 2021 00:40:50 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c54d9402d498e45ed396b5b6fe836f55e4ccadbad745decda3e9f83d880bc677`  
		Last Modified: Wed, 12 May 2021 01:01:40 GMT  
		Size: 49.2 MB (49225351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91bbb3592d6685d1c683c8c20e60901274c636605800608685274c194d43d25`  
		Last Modified: Wed, 12 May 2021 01:48:24 GMT  
		Size: 7.7 MB (7695057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d8c28b9129321858810cff4cd78385949579ed18d991f98c77f912c7a754f8`  
		Last Modified: Wed, 12 May 2021 01:48:24 GMT  
		Size: 10.0 MB (9984343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c2afe1661b16b31414e984301464c54a688d670588da65e09acae49436f1c7`  
		Last Modified: Thu, 13 May 2021 00:41:27 GMT  
		Size: 17.3 MB (17269543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf8effe0189a9fabb276a8737e536476f360929816dd52b787ac4daba9033a9`  
		Last Modified: Thu, 13 May 2021 00:41:21 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb6c42128987e5ad02c5b9a783e7c1034636013cbea40bd2ffea99e616db2a0`  
		Last Modified: Thu, 13 May 2021 00:41:40 GMT  
		Size: 21.1 MB (21051781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0208003bfb3efd741ac782d0e8759350d1952cff542161180d77dcd8d05346`  
		Last Modified: Thu, 13 May 2021 00:41:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.17.3-alpine`

```console
$ docker pull telegraf@sha256:896a3e7a22bcff0969f454cd4b6376f4bd5585ae2d9205ebcb9ca0c90c6a946b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.17.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:771e1a4b1f8c3d4372e0a77e4f1dd4244d5d8fae811e71557e55bdefa75713b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28922500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466e80f78606722902c94806d368dcb7ef48aa4d14471c58a22959d6b977e165`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 15 Apr 2021 02:35:34 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Thu, 15 Apr 2021 02:35:53 GMT
ENV TELEGRAF_VERSION=1.17.3
# Thu, 15 Apr 2021 02:36:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 15 Apr 2021 02:36:05 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 15 Apr 2021 02:36:06 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 15 Apr 2021 02:36:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Apr 2021 02:36:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661683aad4bf8006657c2bf1c3d74bfd343aaa18c1d5a30eda2d437ea8149e2e`  
		Last Modified: Thu, 15 Apr 2021 02:37:00 GMT  
		Size: 3.3 MB (3300674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6276b38c606abd85c7ad60fa2b7708521d0c65481403e10222ec72b0bb52c8c`  
		Last Modified: Thu, 15 Apr 2021 02:37:24 GMT  
		Size: 22.8 MB (22820923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587929023026541619ae340883ecebb2d32f2ed0c06960d5ad5ef38269f09ab6`  
		Last Modified: Thu, 15 Apr 2021 02:37:16 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18`

```console
$ docker pull telegraf@sha256:64acb219a6a6b731b38753eb4c56a83a3a8cd4801bda21b3396ceae76b36114c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.18` - linux; amd64

```console
$ docker pull telegraf@sha256:5db5e69e7fbb7491b91ec62a00e6772ca7e87923673aee9ee0c2728e7b1003b6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111379545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09835a46c6a12928f91f8450f7aaba668b0210ca4b4efc2e9404ad9307d036c`
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
# Fri, 30 Apr 2021 19:21:14 GMT
ENV TELEGRAF_VERSION=1.18.2
# Fri, 30 Apr 2021 19:21:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 30 Apr 2021 19:21:18 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 30 Apr 2021 19:21:18 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 30 Apr 2021 19:21:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Apr 2021 19:21:19 GMT
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
	-	`sha256:316d5ebd8de05e0b312b2c71b38dda61a6f6e8029d6d4acbfd92f8d91218b5ab`  
		Last Modified: Fri, 30 Apr 2021 19:21:57 GMT  
		Size: 25.7 MB (25698930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcad41a00fc48214448443ec1057c5342b718a0b576d568de04527e394b3e42`  
		Last Modified: Fri, 30 Apr 2021 19:21:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.18` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:8d3a23b0eb4dfcd65c9bb883f70f7f275d721fee367f629dfbc5ec225bca045e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102321079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac137ce841b1ce992719ad0387d29033062862f3cb583e5a962433efae580846`
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
# Fri, 30 Apr 2021 20:36:22 GMT
ENV TELEGRAF_VERSION=1.18.2
# Fri, 30 Apr 2021 20:36:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 30 Apr 2021 20:36:32 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 30 Apr 2021 20:36:32 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 30 Apr 2021 20:36:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Apr 2021 20:36:34 GMT
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
	-	`sha256:2e07a6e9bfd266824d003e7e89c5669ac8582e681e7fe24fbe47a09de970a07b`  
		Last Modified: Fri, 30 Apr 2021 20:37:04 GMT  
		Size: 23.8 MB (23775227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858ffe0af88784089949a9655e123603eec3ca47aea8fad71de2090b9edaab4a`  
		Last Modified: Fri, 30 Apr 2021 20:36:56 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.18` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6b7dec78773d41eedbcaf33a6f3a700e0f006ba9210ae7aec2fdee4de4b5648c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107495557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48917cbf5d592ae6dfae0656501e41e0047103b7b1876a667d3f156f2142fa78`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 12 May 2021 00:50:48 GMT
ADD file:ff9983cd659b3fc32ddfbbdeda76a971afd7d399e6d8b98faea3a9ead0e598f6 in / 
# Wed, 12 May 2021 00:50:52 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:34:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 13 May 2021 00:40:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 13 May 2021 00:40:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 13 May 2021 00:40:57 GMT
ENV TELEGRAF_VERSION=1.18.2
# Thu, 13 May 2021 00:41:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 13 May 2021 00:41:04 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 13 May 2021 00:41:05 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 13 May 2021 00:41:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 May 2021 00:41:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c54d9402d498e45ed396b5b6fe836f55e4ccadbad745decda3e9f83d880bc677`  
		Last Modified: Wed, 12 May 2021 01:01:40 GMT  
		Size: 49.2 MB (49225351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91bbb3592d6685d1c683c8c20e60901274c636605800608685274c194d43d25`  
		Last Modified: Wed, 12 May 2021 01:48:24 GMT  
		Size: 7.7 MB (7695057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d8c28b9129321858810cff4cd78385949579ed18d991f98c77f912c7a754f8`  
		Last Modified: Wed, 12 May 2021 01:48:24 GMT  
		Size: 10.0 MB (9984343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c2afe1661b16b31414e984301464c54a688d670588da65e09acae49436f1c7`  
		Last Modified: Thu, 13 May 2021 00:41:27 GMT  
		Size: 17.3 MB (17269543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf8effe0189a9fabb276a8737e536476f360929816dd52b787ac4daba9033a9`  
		Last Modified: Thu, 13 May 2021 00:41:21 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c35990993f5e776c9d3526c5d51df7c5ab3436c32d463630b1075286ade1b1`  
		Last Modified: Thu, 13 May 2021 00:41:58 GMT  
		Size: 23.3 MB (23318181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a46636f0388d9ab8d6ba1fb8731367cdebe248479c81bd0180d7708411d36e`  
		Last Modified: Thu, 13 May 2021 00:41:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18-alpine`

```console
$ docker pull telegraf@sha256:573f8b440effe9c03e4e961b9caec14b720a7b09fb6d3d2f1a50e8c8ac3928c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.18-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:cd96ee08ef56cd196ee0ff0bd498b7ec471d15a778d1921a409cfdf3f4cb9010
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31653713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d424fa1659c5711d90313a78c69a40b42b00ce5220ff7160223b55a8a9bec5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 15 Apr 2021 02:35:34 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Fri, 30 Apr 2021 19:21:22 GMT
ENV TELEGRAF_VERSION=1.18.2
# Fri, 30 Apr 2021 19:21:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 30 Apr 2021 19:21:27 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 30 Apr 2021 19:21:28 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Fri, 30 Apr 2021 19:21:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Apr 2021 19:21:28 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661683aad4bf8006657c2bf1c3d74bfd343aaa18c1d5a30eda2d437ea8149e2e`  
		Last Modified: Thu, 15 Apr 2021 02:37:00 GMT  
		Size: 3.3 MB (3300674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e27e4b32eff8d1c800a97316997aed9ea46e709c8c56e1fb2934a3126aa3af5`  
		Last Modified: Fri, 30 Apr 2021 19:22:16 GMT  
		Size: 25.6 MB (25552134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6aa3f39cd1838267c46ab7c2f1986f4f0a966570ee29d7421a03414ec654aa`  
		Last Modified: Fri, 30 Apr 2021 19:22:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18.2`

```console
$ docker pull telegraf@sha256:64acb219a6a6b731b38753eb4c56a83a3a8cd4801bda21b3396ceae76b36114c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.18.2` - linux; amd64

```console
$ docker pull telegraf@sha256:5db5e69e7fbb7491b91ec62a00e6772ca7e87923673aee9ee0c2728e7b1003b6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111379545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09835a46c6a12928f91f8450f7aaba668b0210ca4b4efc2e9404ad9307d036c`
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
# Fri, 30 Apr 2021 19:21:14 GMT
ENV TELEGRAF_VERSION=1.18.2
# Fri, 30 Apr 2021 19:21:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 30 Apr 2021 19:21:18 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 30 Apr 2021 19:21:18 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 30 Apr 2021 19:21:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Apr 2021 19:21:19 GMT
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
	-	`sha256:316d5ebd8de05e0b312b2c71b38dda61a6f6e8029d6d4acbfd92f8d91218b5ab`  
		Last Modified: Fri, 30 Apr 2021 19:21:57 GMT  
		Size: 25.7 MB (25698930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcad41a00fc48214448443ec1057c5342b718a0b576d568de04527e394b3e42`  
		Last Modified: Fri, 30 Apr 2021 19:21:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.18.2` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:8d3a23b0eb4dfcd65c9bb883f70f7f275d721fee367f629dfbc5ec225bca045e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102321079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac137ce841b1ce992719ad0387d29033062862f3cb583e5a962433efae580846`
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
# Fri, 30 Apr 2021 20:36:22 GMT
ENV TELEGRAF_VERSION=1.18.2
# Fri, 30 Apr 2021 20:36:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 30 Apr 2021 20:36:32 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 30 Apr 2021 20:36:32 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 30 Apr 2021 20:36:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Apr 2021 20:36:34 GMT
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
	-	`sha256:2e07a6e9bfd266824d003e7e89c5669ac8582e681e7fe24fbe47a09de970a07b`  
		Last Modified: Fri, 30 Apr 2021 20:37:04 GMT  
		Size: 23.8 MB (23775227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858ffe0af88784089949a9655e123603eec3ca47aea8fad71de2090b9edaab4a`  
		Last Modified: Fri, 30 Apr 2021 20:36:56 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.18.2` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6b7dec78773d41eedbcaf33a6f3a700e0f006ba9210ae7aec2fdee4de4b5648c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107495557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48917cbf5d592ae6dfae0656501e41e0047103b7b1876a667d3f156f2142fa78`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 12 May 2021 00:50:48 GMT
ADD file:ff9983cd659b3fc32ddfbbdeda76a971afd7d399e6d8b98faea3a9ead0e598f6 in / 
# Wed, 12 May 2021 00:50:52 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:34:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 13 May 2021 00:40:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 13 May 2021 00:40:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 13 May 2021 00:40:57 GMT
ENV TELEGRAF_VERSION=1.18.2
# Thu, 13 May 2021 00:41:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 13 May 2021 00:41:04 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 13 May 2021 00:41:05 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 13 May 2021 00:41:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 May 2021 00:41:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c54d9402d498e45ed396b5b6fe836f55e4ccadbad745decda3e9f83d880bc677`  
		Last Modified: Wed, 12 May 2021 01:01:40 GMT  
		Size: 49.2 MB (49225351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91bbb3592d6685d1c683c8c20e60901274c636605800608685274c194d43d25`  
		Last Modified: Wed, 12 May 2021 01:48:24 GMT  
		Size: 7.7 MB (7695057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d8c28b9129321858810cff4cd78385949579ed18d991f98c77f912c7a754f8`  
		Last Modified: Wed, 12 May 2021 01:48:24 GMT  
		Size: 10.0 MB (9984343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c2afe1661b16b31414e984301464c54a688d670588da65e09acae49436f1c7`  
		Last Modified: Thu, 13 May 2021 00:41:27 GMT  
		Size: 17.3 MB (17269543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf8effe0189a9fabb276a8737e536476f360929816dd52b787ac4daba9033a9`  
		Last Modified: Thu, 13 May 2021 00:41:21 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c35990993f5e776c9d3526c5d51df7c5ab3436c32d463630b1075286ade1b1`  
		Last Modified: Thu, 13 May 2021 00:41:58 GMT  
		Size: 23.3 MB (23318181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a46636f0388d9ab8d6ba1fb8731367cdebe248479c81bd0180d7708411d36e`  
		Last Modified: Thu, 13 May 2021 00:41:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18.2-alpine`

```console
$ docker pull telegraf@sha256:573f8b440effe9c03e4e961b9caec14b720a7b09fb6d3d2f1a50e8c8ac3928c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.18.2-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:cd96ee08ef56cd196ee0ff0bd498b7ec471d15a778d1921a409cfdf3f4cb9010
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31653713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d424fa1659c5711d90313a78c69a40b42b00ce5220ff7160223b55a8a9bec5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 15 Apr 2021 02:35:34 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Fri, 30 Apr 2021 19:21:22 GMT
ENV TELEGRAF_VERSION=1.18.2
# Fri, 30 Apr 2021 19:21:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 30 Apr 2021 19:21:27 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 30 Apr 2021 19:21:28 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Fri, 30 Apr 2021 19:21:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Apr 2021 19:21:28 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661683aad4bf8006657c2bf1c3d74bfd343aaa18c1d5a30eda2d437ea8149e2e`  
		Last Modified: Thu, 15 Apr 2021 02:37:00 GMT  
		Size: 3.3 MB (3300674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e27e4b32eff8d1c800a97316997aed9ea46e709c8c56e1fb2934a3126aa3af5`  
		Last Modified: Fri, 30 Apr 2021 19:22:16 GMT  
		Size: 25.6 MB (25552134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6aa3f39cd1838267c46ab7c2f1986f4f0a966570ee29d7421a03414ec654aa`  
		Last Modified: Fri, 30 Apr 2021 19:22:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:573f8b440effe9c03e4e961b9caec14b720a7b09fb6d3d2f1a50e8c8ac3928c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:cd96ee08ef56cd196ee0ff0bd498b7ec471d15a778d1921a409cfdf3f4cb9010
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31653713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d424fa1659c5711d90313a78c69a40b42b00ce5220ff7160223b55a8a9bec5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 15 Apr 2021 02:35:34 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Fri, 30 Apr 2021 19:21:22 GMT
ENV TELEGRAF_VERSION=1.18.2
# Fri, 30 Apr 2021 19:21:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 30 Apr 2021 19:21:27 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 30 Apr 2021 19:21:28 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Fri, 30 Apr 2021 19:21:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Apr 2021 19:21:28 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661683aad4bf8006657c2bf1c3d74bfd343aaa18c1d5a30eda2d437ea8149e2e`  
		Last Modified: Thu, 15 Apr 2021 02:37:00 GMT  
		Size: 3.3 MB (3300674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e27e4b32eff8d1c800a97316997aed9ea46e709c8c56e1fb2934a3126aa3af5`  
		Last Modified: Fri, 30 Apr 2021 19:22:16 GMT  
		Size: 25.6 MB (25552134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6aa3f39cd1838267c46ab7c2f1986f4f0a966570ee29d7421a03414ec654aa`  
		Last Modified: Fri, 30 Apr 2021 19:22:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:64acb219a6a6b731b38753eb4c56a83a3a8cd4801bda21b3396ceae76b36114c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:5db5e69e7fbb7491b91ec62a00e6772ca7e87923673aee9ee0c2728e7b1003b6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111379545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09835a46c6a12928f91f8450f7aaba668b0210ca4b4efc2e9404ad9307d036c`
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
# Fri, 30 Apr 2021 19:21:14 GMT
ENV TELEGRAF_VERSION=1.18.2
# Fri, 30 Apr 2021 19:21:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 30 Apr 2021 19:21:18 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 30 Apr 2021 19:21:18 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 30 Apr 2021 19:21:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Apr 2021 19:21:19 GMT
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
	-	`sha256:316d5ebd8de05e0b312b2c71b38dda61a6f6e8029d6d4acbfd92f8d91218b5ab`  
		Last Modified: Fri, 30 Apr 2021 19:21:57 GMT  
		Size: 25.7 MB (25698930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcad41a00fc48214448443ec1057c5342b718a0b576d568de04527e394b3e42`  
		Last Modified: Fri, 30 Apr 2021 19:21:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:8d3a23b0eb4dfcd65c9bb883f70f7f275d721fee367f629dfbc5ec225bca045e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102321079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac137ce841b1ce992719ad0387d29033062862f3cb583e5a962433efae580846`
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
# Fri, 30 Apr 2021 20:36:22 GMT
ENV TELEGRAF_VERSION=1.18.2
# Fri, 30 Apr 2021 20:36:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 30 Apr 2021 20:36:32 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 30 Apr 2021 20:36:32 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Fri, 30 Apr 2021 20:36:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Apr 2021 20:36:34 GMT
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
	-	`sha256:2e07a6e9bfd266824d003e7e89c5669ac8582e681e7fe24fbe47a09de970a07b`  
		Last Modified: Fri, 30 Apr 2021 20:37:04 GMT  
		Size: 23.8 MB (23775227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858ffe0af88784089949a9655e123603eec3ca47aea8fad71de2090b9edaab4a`  
		Last Modified: Fri, 30 Apr 2021 20:36:56 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6b7dec78773d41eedbcaf33a6f3a700e0f006ba9210ae7aec2fdee4de4b5648c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107495557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48917cbf5d592ae6dfae0656501e41e0047103b7b1876a667d3f156f2142fa78`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 12 May 2021 00:50:48 GMT
ADD file:ff9983cd659b3fc32ddfbbdeda76a971afd7d399e6d8b98faea3a9ead0e598f6 in / 
# Wed, 12 May 2021 00:50:52 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:34:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 13 May 2021 00:40:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 13 May 2021 00:40:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 13 May 2021 00:40:57 GMT
ENV TELEGRAF_VERSION=1.18.2
# Thu, 13 May 2021 00:41:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 13 May 2021 00:41:04 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 13 May 2021 00:41:05 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 13 May 2021 00:41:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 May 2021 00:41:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c54d9402d498e45ed396b5b6fe836f55e4ccadbad745decda3e9f83d880bc677`  
		Last Modified: Wed, 12 May 2021 01:01:40 GMT  
		Size: 49.2 MB (49225351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91bbb3592d6685d1c683c8c20e60901274c636605800608685274c194d43d25`  
		Last Modified: Wed, 12 May 2021 01:48:24 GMT  
		Size: 7.7 MB (7695057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d8c28b9129321858810cff4cd78385949579ed18d991f98c77f912c7a754f8`  
		Last Modified: Wed, 12 May 2021 01:48:24 GMT  
		Size: 10.0 MB (9984343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c2afe1661b16b31414e984301464c54a688d670588da65e09acae49436f1c7`  
		Last Modified: Thu, 13 May 2021 00:41:27 GMT  
		Size: 17.3 MB (17269543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf8effe0189a9fabb276a8737e536476f360929816dd52b787ac4daba9033a9`  
		Last Modified: Thu, 13 May 2021 00:41:21 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c35990993f5e776c9d3526c5d51df7c5ab3436c32d463630b1075286ade1b1`  
		Last Modified: Thu, 13 May 2021 00:41:58 GMT  
		Size: 23.3 MB (23318181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a46636f0388d9ab8d6ba1fb8731367cdebe248479c81bd0180d7708411d36e`  
		Last Modified: Thu, 13 May 2021 00:41:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
