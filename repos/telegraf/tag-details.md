<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.22`](#telegraf122)
-	[`telegraf:1.22-alpine`](#telegraf122-alpine)
-	[`telegraf:1.22.4`](#telegraf1224)
-	[`telegraf:1.22.4-alpine`](#telegraf1224-alpine)
-	[`telegraf:1.23`](#telegraf123)
-	[`telegraf:1.23-alpine`](#telegraf123-alpine)
-	[`telegraf:1.23.4`](#telegraf1234)
-	[`telegraf:1.23.4-alpine`](#telegraf1234-alpine)
-	[`telegraf:1.24`](#telegraf124)
-	[`telegraf:1.24-alpine`](#telegraf124-alpine)
-	[`telegraf:1.24.2`](#telegraf1242)
-	[`telegraf:1.24.2-alpine`](#telegraf1242-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.22`

```console
$ docker pull telegraf@sha256:9b89f91918d2621227dd777ee8c779cf729b8341dd264d1981460298010abbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.22` - linux; amd64

```console
$ docker pull telegraf@sha256:14ed0456a29f4629bdb65bcbbc502b1c3888309580239b7b011ddf5440aa1385
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130348164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702613c5fe3808339f71fc74b89ec3ee892bd2a259bfc8328179caf965ca151e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:54:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:55:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 23:03:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 23:03:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 23:03:01 GMT
ENV TELEGRAF_VERSION=1.22.4
# Wed, 05 Oct 2022 23:03:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Oct 2022 23:03:05 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Oct 2022 23:03:05 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 05 Oct 2022 23:03:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 23:03:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47db815c6a4547dc224b75222193cb1851cf529d2cbdf26f854b9bbf97099b98`  
		Last Modified: Wed, 05 Oct 2022 01:19:13 GMT  
		Size: 5.2 MB (5163279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf48494000001a037b72870d2a6a2536f9da8bc5d1ceddd72d79f4a51fe7a60e`  
		Last Modified: Wed, 05 Oct 2022 01:19:13 GMT  
		Size: 10.9 MB (10876505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863a7459c8fe546ab3b805bc6fb6f6e8b01bcf7411513f42699201aacfc4bb9c`  
		Last Modified: Wed, 05 Oct 2022 23:03:48 GMT  
		Size: 18.8 MB (18760121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e28af260775d457e7415a6995724f47b2d5a7b97a31a0c7d14f0c8a2ff1c257`  
		Last Modified: Wed, 05 Oct 2022 23:03:45 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9146fe0c9fd9b9d8b457f3554cae96baa2d6cbf0ad3d99bc1835bb254fe41216`  
		Last Modified: Wed, 05 Oct 2022 23:03:52 GMT  
		Size: 40.5 MB (40498770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0395d410b9a8faccee2d45a42d52d389c3c21bfc5a6ce1420e02dd4bf85d3c2`  
		Last Modified: Wed, 05 Oct 2022 23:03:45 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.22` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7fca9ab66c5208114cf5dca4677a6317bd8bc512c1f0c56ec225b316cc25b328
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120745599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33cf883d2dd481f15e853bd3ebb68795fd39d2c2cbe61e2809c996d53fdd2159`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:28 GMT
ADD file:47a3f2948af18c39686ca59a88a439c25edaf286064d3a2ccc5dab47fee2fc52 in / 
# Tue, 04 Oct 2022 23:58:29 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:32:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:32:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 06 Oct 2022 16:07:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 16:07:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 06 Oct 2022 16:07:06 GMT
ENV TELEGRAF_VERSION=1.22.4
# Thu, 06 Oct 2022 16:07:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 06 Oct 2022 16:07:17 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 06 Oct 2022 16:07:17 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 06 Oct 2022 16:07:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 16:07:17 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e19342fb46cabf6147aec1d1c6af1f3a82736530cf3b067835fc8a09da092ce3`  
		Last Modified: Wed, 05 Oct 2022 00:04:36 GMT  
		Size: 50.2 MB (50209087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49f93f990f17337480b5bdf526a6bb48d1ae63bd17f54be17cd2f6ebba4de7d`  
		Last Modified: Wed, 05 Oct 2022 00:53:28 GMT  
		Size: 4.9 MB (4931366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3989be0d7ed2f72fae0310039043f6ba76c24a45f9ec9689697ebd932845cc8`  
		Last Modified: Wed, 05 Oct 2022 00:53:28 GMT  
		Size: 10.2 MB (10217872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef23f3c089cb85cd0436535aeb8422fbfd379b3a897532a89f1c2fea29728e03`  
		Last Modified: Thu, 06 Oct 2022 16:08:13 GMT  
		Size: 17.5 MB (17462363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a05f53155f290b1fb830a5da47f116e34fb30b79dcd539c2e8d735f10fd13ac`  
		Last Modified: Thu, 06 Oct 2022 16:08:09 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27acb15d391b96b5edf8a1eb28de712b835e2454d552437d8ee221055389a907`  
		Last Modified: Thu, 06 Oct 2022 16:08:17 GMT  
		Size: 37.9 MB (37921670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fd35fe581c13d9a8f10c1a1501eb79da9c044ffd293523007b154990f934b2`  
		Last Modified: Thu, 06 Oct 2022 16:08:09 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.22` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:7368fb640e7026c37e2feff72e99760dad5e0528537f9d4067fe59c2c2a6dacc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124499335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e5416cd3492886a1d4f4fd04c3c26245d6a6e992e9bdf89aea51bce2600e5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:23:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:23:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 17:52:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:52:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 17:52:25 GMT
ENV TELEGRAF_VERSION=1.22.4
# Wed, 05 Oct 2022 17:52:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Oct 2022 17:52:31 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Oct 2022 17:52:32 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 05 Oct 2022 17:52:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 17:52:33 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37c953a37e989b49a533e8d08c80d87ce66fadee48160f9a4d8cd2dd5b0ec87`  
		Last Modified: Wed, 05 Oct 2022 00:37:21 GMT  
		Size: 4.9 MB (4944361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98802a15fc60bda24c79203236f930586f1dba6218aa2b4c121cf0dbf5627b38`  
		Last Modified: Wed, 05 Oct 2022 00:37:22 GMT  
		Size: 10.7 MB (10657400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22398aa42c1b74e8b8aa86450b2606b08a367992108afd66f03799f1393932ef`  
		Last Modified: Wed, 05 Oct 2022 17:53:26 GMT  
		Size: 18.4 MB (18382830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50578a1c2d11fdb0e84248fb7effbf5bc328dc0f95e2f855be12c15e333f02af`  
		Last Modified: Wed, 05 Oct 2022 17:53:23 GMT  
		Size: 2.9 KB (2860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae60bb815624a8c7921142b8df92aa0c60b1f1d1d90f656989004d5aa9eb9f2c`  
		Last Modified: Wed, 05 Oct 2022 17:53:29 GMT  
		Size: 36.8 MB (36810915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94e7fa739c81d7c9a53200c1044af7d8e6905cc14fefd9a9b212574c1e202a3`  
		Last Modified: Wed, 05 Oct 2022 17:53:23 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.22-alpine`

```console
$ docker pull telegraf@sha256:549a57354a32ba18667288c8702ad772adb0b10bd8e507b5d1ba4392dbee222d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.22-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b1b6c79dbb71113360ed5fbc53a02fb13c9a3318fdb9aa7777fc988ab183018e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46468343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8eee01edb344ccc13e8d13755cfe7660345a4436513ed82df112f946dfd9823`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:59:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 07 Oct 2022 04:19:22 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Fri, 07 Oct 2022 04:19:22 GMT
ENV TELEGRAF_VERSION=1.22.4
# Fri, 07 Oct 2022 04:19:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Fri, 07 Oct 2022 04:19:30 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 07 Oct 2022 04:19:30 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Fri, 07 Oct 2022 04:19:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 04:19:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d30442cf8411e7f53657b11f2e08ef81065f359c49d13af3d255eb9ce50bd8`  
		Last Modified: Thu, 06 Oct 2022 23:00:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df12bedc10645580477742185fbda69b5e253e91012a2898380cae67461d4c7`  
		Last Modified: Fri, 07 Oct 2022 04:20:16 GMT  
		Size: 3.3 MB (3310249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2bc112f0c4083a93e263b2af0c68bd4c6e11c6c9c9bd74a1b36480e896283d0`  
		Last Modified: Fri, 07 Oct 2022 04:20:22 GMT  
		Size: 40.4 MB (40351559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33be33203f6ee4e7fd60d2a7b01562a12ce8331579c432b159ee415110e1dbe1`  
		Last Modified: Fri, 07 Oct 2022 04:20:16 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.22.4`

```console
$ docker pull telegraf@sha256:9b89f91918d2621227dd777ee8c779cf729b8341dd264d1981460298010abbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.22.4` - linux; amd64

```console
$ docker pull telegraf@sha256:14ed0456a29f4629bdb65bcbbc502b1c3888309580239b7b011ddf5440aa1385
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130348164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702613c5fe3808339f71fc74b89ec3ee892bd2a259bfc8328179caf965ca151e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:54:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:55:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 23:03:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 23:03:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 23:03:01 GMT
ENV TELEGRAF_VERSION=1.22.4
# Wed, 05 Oct 2022 23:03:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Oct 2022 23:03:05 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Oct 2022 23:03:05 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 05 Oct 2022 23:03:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 23:03:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47db815c6a4547dc224b75222193cb1851cf529d2cbdf26f854b9bbf97099b98`  
		Last Modified: Wed, 05 Oct 2022 01:19:13 GMT  
		Size: 5.2 MB (5163279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf48494000001a037b72870d2a6a2536f9da8bc5d1ceddd72d79f4a51fe7a60e`  
		Last Modified: Wed, 05 Oct 2022 01:19:13 GMT  
		Size: 10.9 MB (10876505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863a7459c8fe546ab3b805bc6fb6f6e8b01bcf7411513f42699201aacfc4bb9c`  
		Last Modified: Wed, 05 Oct 2022 23:03:48 GMT  
		Size: 18.8 MB (18760121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e28af260775d457e7415a6995724f47b2d5a7b97a31a0c7d14f0c8a2ff1c257`  
		Last Modified: Wed, 05 Oct 2022 23:03:45 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9146fe0c9fd9b9d8b457f3554cae96baa2d6cbf0ad3d99bc1835bb254fe41216`  
		Last Modified: Wed, 05 Oct 2022 23:03:52 GMT  
		Size: 40.5 MB (40498770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0395d410b9a8faccee2d45a42d52d389c3c21bfc5a6ce1420e02dd4bf85d3c2`  
		Last Modified: Wed, 05 Oct 2022 23:03:45 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.22.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7fca9ab66c5208114cf5dca4677a6317bd8bc512c1f0c56ec225b316cc25b328
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120745599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33cf883d2dd481f15e853bd3ebb68795fd39d2c2cbe61e2809c996d53fdd2159`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:28 GMT
ADD file:47a3f2948af18c39686ca59a88a439c25edaf286064d3a2ccc5dab47fee2fc52 in / 
# Tue, 04 Oct 2022 23:58:29 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:32:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:32:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 06 Oct 2022 16:07:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 16:07:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 06 Oct 2022 16:07:06 GMT
ENV TELEGRAF_VERSION=1.22.4
# Thu, 06 Oct 2022 16:07:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 06 Oct 2022 16:07:17 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 06 Oct 2022 16:07:17 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 06 Oct 2022 16:07:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 16:07:17 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e19342fb46cabf6147aec1d1c6af1f3a82736530cf3b067835fc8a09da092ce3`  
		Last Modified: Wed, 05 Oct 2022 00:04:36 GMT  
		Size: 50.2 MB (50209087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49f93f990f17337480b5bdf526a6bb48d1ae63bd17f54be17cd2f6ebba4de7d`  
		Last Modified: Wed, 05 Oct 2022 00:53:28 GMT  
		Size: 4.9 MB (4931366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3989be0d7ed2f72fae0310039043f6ba76c24a45f9ec9689697ebd932845cc8`  
		Last Modified: Wed, 05 Oct 2022 00:53:28 GMT  
		Size: 10.2 MB (10217872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef23f3c089cb85cd0436535aeb8422fbfd379b3a897532a89f1c2fea29728e03`  
		Last Modified: Thu, 06 Oct 2022 16:08:13 GMT  
		Size: 17.5 MB (17462363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a05f53155f290b1fb830a5da47f116e34fb30b79dcd539c2e8d735f10fd13ac`  
		Last Modified: Thu, 06 Oct 2022 16:08:09 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27acb15d391b96b5edf8a1eb28de712b835e2454d552437d8ee221055389a907`  
		Last Modified: Thu, 06 Oct 2022 16:08:17 GMT  
		Size: 37.9 MB (37921670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fd35fe581c13d9a8f10c1a1501eb79da9c044ffd293523007b154990f934b2`  
		Last Modified: Thu, 06 Oct 2022 16:08:09 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.22.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:7368fb640e7026c37e2feff72e99760dad5e0528537f9d4067fe59c2c2a6dacc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124499335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e5416cd3492886a1d4f4fd04c3c26245d6a6e992e9bdf89aea51bce2600e5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:23:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:23:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 17:52:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:52:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 17:52:25 GMT
ENV TELEGRAF_VERSION=1.22.4
# Wed, 05 Oct 2022 17:52:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Oct 2022 17:52:31 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Oct 2022 17:52:32 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 05 Oct 2022 17:52:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 17:52:33 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37c953a37e989b49a533e8d08c80d87ce66fadee48160f9a4d8cd2dd5b0ec87`  
		Last Modified: Wed, 05 Oct 2022 00:37:21 GMT  
		Size: 4.9 MB (4944361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98802a15fc60bda24c79203236f930586f1dba6218aa2b4c121cf0dbf5627b38`  
		Last Modified: Wed, 05 Oct 2022 00:37:22 GMT  
		Size: 10.7 MB (10657400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22398aa42c1b74e8b8aa86450b2606b08a367992108afd66f03799f1393932ef`  
		Last Modified: Wed, 05 Oct 2022 17:53:26 GMT  
		Size: 18.4 MB (18382830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50578a1c2d11fdb0e84248fb7effbf5bc328dc0f95e2f855be12c15e333f02af`  
		Last Modified: Wed, 05 Oct 2022 17:53:23 GMT  
		Size: 2.9 KB (2860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae60bb815624a8c7921142b8df92aa0c60b1f1d1d90f656989004d5aa9eb9f2c`  
		Last Modified: Wed, 05 Oct 2022 17:53:29 GMT  
		Size: 36.8 MB (36810915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94e7fa739c81d7c9a53200c1044af7d8e6905cc14fefd9a9b212574c1e202a3`  
		Last Modified: Wed, 05 Oct 2022 17:53:23 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.22.4-alpine`

```console
$ docker pull telegraf@sha256:549a57354a32ba18667288c8702ad772adb0b10bd8e507b5d1ba4392dbee222d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.22.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b1b6c79dbb71113360ed5fbc53a02fb13c9a3318fdb9aa7777fc988ab183018e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46468343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8eee01edb344ccc13e8d13755cfe7660345a4436513ed82df112f946dfd9823`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:59:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 07 Oct 2022 04:19:22 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Fri, 07 Oct 2022 04:19:22 GMT
ENV TELEGRAF_VERSION=1.22.4
# Fri, 07 Oct 2022 04:19:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Fri, 07 Oct 2022 04:19:30 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 07 Oct 2022 04:19:30 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Fri, 07 Oct 2022 04:19:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 04:19:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d30442cf8411e7f53657b11f2e08ef81065f359c49d13af3d255eb9ce50bd8`  
		Last Modified: Thu, 06 Oct 2022 23:00:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df12bedc10645580477742185fbda69b5e253e91012a2898380cae67461d4c7`  
		Last Modified: Fri, 07 Oct 2022 04:20:16 GMT  
		Size: 3.3 MB (3310249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2bc112f0c4083a93e263b2af0c68bd4c6e11c6c9c9bd74a1b36480e896283d0`  
		Last Modified: Fri, 07 Oct 2022 04:20:22 GMT  
		Size: 40.4 MB (40351559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33be33203f6ee4e7fd60d2a7b01562a12ce8331579c432b159ee415110e1dbe1`  
		Last Modified: Fri, 07 Oct 2022 04:20:16 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.23`

```console
$ docker pull telegraf@sha256:6f2a8fdf5d1571495357831e94f95ccfa2a73214b77a4168c346aeb488f05331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.23` - linux; amd64

```console
$ docker pull telegraf@sha256:328c9997a632a8527095a4e9dcc984fe59ef79f8c5c9425c7ec9d2828d20c9fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131698596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d8d04e0298d2914efe05319ddd9a660d5b9fa3c634cef047ca7cf1cb3f0a82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:54:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:55:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 23:03:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 23:03:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 23:03:10 GMT
ENV TELEGRAF_VERSION=1.23.4
# Wed, 05 Oct 2022 23:03:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Oct 2022 23:03:14 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Oct 2022 23:03:14 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 05 Oct 2022 23:03:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 23:03:14 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47db815c6a4547dc224b75222193cb1851cf529d2cbdf26f854b9bbf97099b98`  
		Last Modified: Wed, 05 Oct 2022 01:19:13 GMT  
		Size: 5.2 MB (5163279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf48494000001a037b72870d2a6a2536f9da8bc5d1ceddd72d79f4a51fe7a60e`  
		Last Modified: Wed, 05 Oct 2022 01:19:13 GMT  
		Size: 10.9 MB (10876505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863a7459c8fe546ab3b805bc6fb6f6e8b01bcf7411513f42699201aacfc4bb9c`  
		Last Modified: Wed, 05 Oct 2022 23:03:48 GMT  
		Size: 18.8 MB (18760121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e28af260775d457e7415a6995724f47b2d5a7b97a31a0c7d14f0c8a2ff1c257`  
		Last Modified: Wed, 05 Oct 2022 23:03:45 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264ff58a5b4e3bf99903e079a463770cf11ceb7382bf83079f15587468b358ea`  
		Last Modified: Wed, 05 Oct 2022 23:04:13 GMT  
		Size: 41.8 MB (41849205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9005b6d6aa1756fc24a3678ff55054a75a3bdf4e8a209b030febe3925bf2cb1`  
		Last Modified: Wed, 05 Oct 2022 23:04:06 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.23` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:eb0795397aa082da4dce7ac9d0d6b7670327a6314efd62855e2ee3b026a7da79
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121930485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aeca7023955d184a2d2e51baa3f7b951753f98371f12df46586c20ce873952d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:28 GMT
ADD file:47a3f2948af18c39686ca59a88a439c25edaf286064d3a2ccc5dab47fee2fc52 in / 
# Tue, 04 Oct 2022 23:58:29 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:32:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:32:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 06 Oct 2022 16:07:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 16:07:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 06 Oct 2022 16:07:24 GMT
ENV TELEGRAF_VERSION=1.23.4
# Thu, 06 Oct 2022 16:07:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 06 Oct 2022 16:07:30 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 06 Oct 2022 16:07:30 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 06 Oct 2022 16:07:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 16:07:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e19342fb46cabf6147aec1d1c6af1f3a82736530cf3b067835fc8a09da092ce3`  
		Last Modified: Wed, 05 Oct 2022 00:04:36 GMT  
		Size: 50.2 MB (50209087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49f93f990f17337480b5bdf526a6bb48d1ae63bd17f54be17cd2f6ebba4de7d`  
		Last Modified: Wed, 05 Oct 2022 00:53:28 GMT  
		Size: 4.9 MB (4931366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3989be0d7ed2f72fae0310039043f6ba76c24a45f9ec9689697ebd932845cc8`  
		Last Modified: Wed, 05 Oct 2022 00:53:28 GMT  
		Size: 10.2 MB (10217872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef23f3c089cb85cd0436535aeb8422fbfd379b3a897532a89f1c2fea29728e03`  
		Last Modified: Thu, 06 Oct 2022 16:08:13 GMT  
		Size: 17.5 MB (17462363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a05f53155f290b1fb830a5da47f116e34fb30b79dcd539c2e8d735f10fd13ac`  
		Last Modified: Thu, 06 Oct 2022 16:08:09 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6162765b3cba24225be965855e89cba4121b8aeb1dc6bee23e637820cf698522`  
		Last Modified: Thu, 06 Oct 2022 16:08:35 GMT  
		Size: 39.1 MB (39106556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3fab56c33152b67d36793d7a153cb14d96626226b7063d1ea7d04877b0a5e9`  
		Last Modified: Thu, 06 Oct 2022 16:08:28 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.23` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ccf728ced8a278a6164dc68e6c294e0569c32e73ae3b70c0dbf8aa79c2bf83e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125718691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae84ce737718980b147e07299ce4fb4e7f0e8a65151663b3ce8836ef3597c2c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:23:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:23:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 17:52:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:52:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 17:52:39 GMT
ENV TELEGRAF_VERSION=1.23.4
# Wed, 05 Oct 2022 17:52:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Oct 2022 17:52:44 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Oct 2022 17:52:45 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 05 Oct 2022 17:52:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 17:52:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37c953a37e989b49a533e8d08c80d87ce66fadee48160f9a4d8cd2dd5b0ec87`  
		Last Modified: Wed, 05 Oct 2022 00:37:21 GMT  
		Size: 4.9 MB (4944361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98802a15fc60bda24c79203236f930586f1dba6218aa2b4c121cf0dbf5627b38`  
		Last Modified: Wed, 05 Oct 2022 00:37:22 GMT  
		Size: 10.7 MB (10657400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22398aa42c1b74e8b8aa86450b2606b08a367992108afd66f03799f1393932ef`  
		Last Modified: Wed, 05 Oct 2022 17:53:26 GMT  
		Size: 18.4 MB (18382830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50578a1c2d11fdb0e84248fb7effbf5bc328dc0f95e2f855be12c15e333f02af`  
		Last Modified: Wed, 05 Oct 2022 17:53:23 GMT  
		Size: 2.9 KB (2860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff5bfe8ebabd5dfb65d9ad72b152a0d492efdc3ffb8e8ccc68b3286dbf40203`  
		Last Modified: Wed, 05 Oct 2022 17:53:47 GMT  
		Size: 38.0 MB (38030270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed18acdae117334f1123e5e940de0871656bdd4b584d7d84ceb8f5b361ff1a81`  
		Last Modified: Wed, 05 Oct 2022 17:53:41 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.23-alpine`

```console
$ docker pull telegraf@sha256:87b29b7c8aae95f9e15997f22345e1362782a272367ccc85a1bf72bcd6df2024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.23-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e787b6410ecaee448c2977e59106ead6332b224434cba4539953c0dc62653073
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47802182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d584753fb1df1c0c599592b09d5cfd38c7e4126928f24d269d32899520f6703f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:59:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 07 Oct 2022 04:19:22 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Fri, 07 Oct 2022 04:19:34 GMT
ENV TELEGRAF_VERSION=1.23.4
# Fri, 07 Oct 2022 04:19:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Fri, 07 Oct 2022 04:19:42 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 07 Oct 2022 04:19:42 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Fri, 07 Oct 2022 04:19:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 04:19:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d30442cf8411e7f53657b11f2e08ef81065f359c49d13af3d255eb9ce50bd8`  
		Last Modified: Thu, 06 Oct 2022 23:00:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df12bedc10645580477742185fbda69b5e253e91012a2898380cae67461d4c7`  
		Last Modified: Fri, 07 Oct 2022 04:20:16 GMT  
		Size: 3.3 MB (3310249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab3ed1eda323e4516c1db369a4bec5a7121760376690f8a0618a54e5344d482`  
		Last Modified: Fri, 07 Oct 2022 04:20:39 GMT  
		Size: 41.7 MB (41685397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22fa5ffc4562276d4547aa68fae5cb82114d48d8638f7c7d7e10e6873318475`  
		Last Modified: Fri, 07 Oct 2022 04:20:32 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.23.4`

```console
$ docker pull telegraf@sha256:6f2a8fdf5d1571495357831e94f95ccfa2a73214b77a4168c346aeb488f05331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.23.4` - linux; amd64

```console
$ docker pull telegraf@sha256:328c9997a632a8527095a4e9dcc984fe59ef79f8c5c9425c7ec9d2828d20c9fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131698596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d8d04e0298d2914efe05319ddd9a660d5b9fa3c634cef047ca7cf1cb3f0a82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:54:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:55:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 23:03:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 23:03:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 23:03:10 GMT
ENV TELEGRAF_VERSION=1.23.4
# Wed, 05 Oct 2022 23:03:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Oct 2022 23:03:14 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Oct 2022 23:03:14 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 05 Oct 2022 23:03:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 23:03:14 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47db815c6a4547dc224b75222193cb1851cf529d2cbdf26f854b9bbf97099b98`  
		Last Modified: Wed, 05 Oct 2022 01:19:13 GMT  
		Size: 5.2 MB (5163279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf48494000001a037b72870d2a6a2536f9da8bc5d1ceddd72d79f4a51fe7a60e`  
		Last Modified: Wed, 05 Oct 2022 01:19:13 GMT  
		Size: 10.9 MB (10876505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863a7459c8fe546ab3b805bc6fb6f6e8b01bcf7411513f42699201aacfc4bb9c`  
		Last Modified: Wed, 05 Oct 2022 23:03:48 GMT  
		Size: 18.8 MB (18760121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e28af260775d457e7415a6995724f47b2d5a7b97a31a0c7d14f0c8a2ff1c257`  
		Last Modified: Wed, 05 Oct 2022 23:03:45 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264ff58a5b4e3bf99903e079a463770cf11ceb7382bf83079f15587468b358ea`  
		Last Modified: Wed, 05 Oct 2022 23:04:13 GMT  
		Size: 41.8 MB (41849205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9005b6d6aa1756fc24a3678ff55054a75a3bdf4e8a209b030febe3925bf2cb1`  
		Last Modified: Wed, 05 Oct 2022 23:04:06 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.23.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:eb0795397aa082da4dce7ac9d0d6b7670327a6314efd62855e2ee3b026a7da79
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121930485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aeca7023955d184a2d2e51baa3f7b951753f98371f12df46586c20ce873952d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:28 GMT
ADD file:47a3f2948af18c39686ca59a88a439c25edaf286064d3a2ccc5dab47fee2fc52 in / 
# Tue, 04 Oct 2022 23:58:29 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:32:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:32:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 06 Oct 2022 16:07:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 16:07:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 06 Oct 2022 16:07:24 GMT
ENV TELEGRAF_VERSION=1.23.4
# Thu, 06 Oct 2022 16:07:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 06 Oct 2022 16:07:30 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 06 Oct 2022 16:07:30 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 06 Oct 2022 16:07:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 16:07:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e19342fb46cabf6147aec1d1c6af1f3a82736530cf3b067835fc8a09da092ce3`  
		Last Modified: Wed, 05 Oct 2022 00:04:36 GMT  
		Size: 50.2 MB (50209087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49f93f990f17337480b5bdf526a6bb48d1ae63bd17f54be17cd2f6ebba4de7d`  
		Last Modified: Wed, 05 Oct 2022 00:53:28 GMT  
		Size: 4.9 MB (4931366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3989be0d7ed2f72fae0310039043f6ba76c24a45f9ec9689697ebd932845cc8`  
		Last Modified: Wed, 05 Oct 2022 00:53:28 GMT  
		Size: 10.2 MB (10217872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef23f3c089cb85cd0436535aeb8422fbfd379b3a897532a89f1c2fea29728e03`  
		Last Modified: Thu, 06 Oct 2022 16:08:13 GMT  
		Size: 17.5 MB (17462363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a05f53155f290b1fb830a5da47f116e34fb30b79dcd539c2e8d735f10fd13ac`  
		Last Modified: Thu, 06 Oct 2022 16:08:09 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6162765b3cba24225be965855e89cba4121b8aeb1dc6bee23e637820cf698522`  
		Last Modified: Thu, 06 Oct 2022 16:08:35 GMT  
		Size: 39.1 MB (39106556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3fab56c33152b67d36793d7a153cb14d96626226b7063d1ea7d04877b0a5e9`  
		Last Modified: Thu, 06 Oct 2022 16:08:28 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.23.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ccf728ced8a278a6164dc68e6c294e0569c32e73ae3b70c0dbf8aa79c2bf83e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125718691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae84ce737718980b147e07299ce4fb4e7f0e8a65151663b3ce8836ef3597c2c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:23:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:23:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 17:52:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:52:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 17:52:39 GMT
ENV TELEGRAF_VERSION=1.23.4
# Wed, 05 Oct 2022 17:52:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Oct 2022 17:52:44 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Oct 2022 17:52:45 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 05 Oct 2022 17:52:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 17:52:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37c953a37e989b49a533e8d08c80d87ce66fadee48160f9a4d8cd2dd5b0ec87`  
		Last Modified: Wed, 05 Oct 2022 00:37:21 GMT  
		Size: 4.9 MB (4944361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98802a15fc60bda24c79203236f930586f1dba6218aa2b4c121cf0dbf5627b38`  
		Last Modified: Wed, 05 Oct 2022 00:37:22 GMT  
		Size: 10.7 MB (10657400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22398aa42c1b74e8b8aa86450b2606b08a367992108afd66f03799f1393932ef`  
		Last Modified: Wed, 05 Oct 2022 17:53:26 GMT  
		Size: 18.4 MB (18382830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50578a1c2d11fdb0e84248fb7effbf5bc328dc0f95e2f855be12c15e333f02af`  
		Last Modified: Wed, 05 Oct 2022 17:53:23 GMT  
		Size: 2.9 KB (2860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff5bfe8ebabd5dfb65d9ad72b152a0d492efdc3ffb8e8ccc68b3286dbf40203`  
		Last Modified: Wed, 05 Oct 2022 17:53:47 GMT  
		Size: 38.0 MB (38030270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed18acdae117334f1123e5e940de0871656bdd4b584d7d84ceb8f5b361ff1a81`  
		Last Modified: Wed, 05 Oct 2022 17:53:41 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.23.4-alpine`

```console
$ docker pull telegraf@sha256:87b29b7c8aae95f9e15997f22345e1362782a272367ccc85a1bf72bcd6df2024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.23.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e787b6410ecaee448c2977e59106ead6332b224434cba4539953c0dc62653073
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47802182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d584753fb1df1c0c599592b09d5cfd38c7e4126928f24d269d32899520f6703f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:59:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 07 Oct 2022 04:19:22 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Fri, 07 Oct 2022 04:19:34 GMT
ENV TELEGRAF_VERSION=1.23.4
# Fri, 07 Oct 2022 04:19:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Fri, 07 Oct 2022 04:19:42 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 07 Oct 2022 04:19:42 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Fri, 07 Oct 2022 04:19:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 04:19:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d30442cf8411e7f53657b11f2e08ef81065f359c49d13af3d255eb9ce50bd8`  
		Last Modified: Thu, 06 Oct 2022 23:00:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df12bedc10645580477742185fbda69b5e253e91012a2898380cae67461d4c7`  
		Last Modified: Fri, 07 Oct 2022 04:20:16 GMT  
		Size: 3.3 MB (3310249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab3ed1eda323e4516c1db369a4bec5a7121760376690f8a0618a54e5344d482`  
		Last Modified: Fri, 07 Oct 2022 04:20:39 GMT  
		Size: 41.7 MB (41685397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22fa5ffc4562276d4547aa68fae5cb82114d48d8638f7c7d7e10e6873318475`  
		Last Modified: Fri, 07 Oct 2022 04:20:32 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.24`

```console
$ docker pull telegraf@sha256:c041b149b338b1edeac1d9cfdaed9531842621e20d3863e04034fb8bfa897f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.24` - linux; amd64

```console
$ docker pull telegraf@sha256:2d544a60af363eb9710022f41d4109e836a9c82951225073dd6d07d9f243a8a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133856512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548e4f33b1dc8068c849c0c96e5918539c9ba1647f647c89c0ca3fca68cece74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:54:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:55:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 23:03:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 23:03:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 23:03:19 GMT
ENV TELEGRAF_VERSION=1.24.2
# Wed, 05 Oct 2022 23:03:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Oct 2022 23:03:23 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Oct 2022 23:03:23 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 05 Oct 2022 23:03:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 23:03:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47db815c6a4547dc224b75222193cb1851cf529d2cbdf26f854b9bbf97099b98`  
		Last Modified: Wed, 05 Oct 2022 01:19:13 GMT  
		Size: 5.2 MB (5163279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf48494000001a037b72870d2a6a2536f9da8bc5d1ceddd72d79f4a51fe7a60e`  
		Last Modified: Wed, 05 Oct 2022 01:19:13 GMT  
		Size: 10.9 MB (10876505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863a7459c8fe546ab3b805bc6fb6f6e8b01bcf7411513f42699201aacfc4bb9c`  
		Last Modified: Wed, 05 Oct 2022 23:03:48 GMT  
		Size: 18.8 MB (18760121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e28af260775d457e7415a6995724f47b2d5a7b97a31a0c7d14f0c8a2ff1c257`  
		Last Modified: Wed, 05 Oct 2022 23:03:45 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f15f27d873fce4dbd5165fb753fc5b702a3ffcff509b667742a60950fcc8261`  
		Last Modified: Wed, 05 Oct 2022 23:04:31 GMT  
		Size: 44.0 MB (44007118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b89a3dd513bbc50e6ff4df223ff078d1bacaad986a61fb7b6d91a14f74ad95a`  
		Last Modified: Wed, 05 Oct 2022 23:04:24 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.24` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7da547f0b06db7b505c678289103bf96bef2dcbb9606fee01663470b490d0c2e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123881365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c29fad03d96db8d2b5cd496a1dc6ff839d055f6dd82fc3cd603a3f6d5e46f96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:28 GMT
ADD file:47a3f2948af18c39686ca59a88a439c25edaf286064d3a2ccc5dab47fee2fc52 in / 
# Tue, 04 Oct 2022 23:58:29 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:32:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:32:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 06 Oct 2022 16:07:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 16:07:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 06 Oct 2022 16:07:35 GMT
ENV TELEGRAF_VERSION=1.24.2
# Thu, 06 Oct 2022 16:07:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 06 Oct 2022 16:07:41 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 06 Oct 2022 16:07:41 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 06 Oct 2022 16:07:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 16:07:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e19342fb46cabf6147aec1d1c6af1f3a82736530cf3b067835fc8a09da092ce3`  
		Last Modified: Wed, 05 Oct 2022 00:04:36 GMT  
		Size: 50.2 MB (50209087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49f93f990f17337480b5bdf526a6bb48d1ae63bd17f54be17cd2f6ebba4de7d`  
		Last Modified: Wed, 05 Oct 2022 00:53:28 GMT  
		Size: 4.9 MB (4931366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3989be0d7ed2f72fae0310039043f6ba76c24a45f9ec9689697ebd932845cc8`  
		Last Modified: Wed, 05 Oct 2022 00:53:28 GMT  
		Size: 10.2 MB (10217872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef23f3c089cb85cd0436535aeb8422fbfd379b3a897532a89f1c2fea29728e03`  
		Last Modified: Thu, 06 Oct 2022 16:08:13 GMT  
		Size: 17.5 MB (17462363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a05f53155f290b1fb830a5da47f116e34fb30b79dcd539c2e8d735f10fd13ac`  
		Last Modified: Thu, 06 Oct 2022 16:08:09 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0c43f9c460c0df3bccd6147aec132029dfcb6c97462b59494d46b61d2fa73b`  
		Last Modified: Thu, 06 Oct 2022 16:08:55 GMT  
		Size: 41.1 MB (41057433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c573a3fdf94f1a4476208d9bdcf1c919fbae54e198fa626b45e7afa62cf99a8`  
		Last Modified: Thu, 06 Oct 2022 16:08:48 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.24` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ec9785ee6a1f0f6c15aff3757860c2ceadab3d1e16105f1ed6eae6ef8126ad46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127582555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aab2522ba7f26a4e559c798050d9111fd3a140acd7d2c89a49e93f9e001d6cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:23:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:23:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 17:52:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:52:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 17:52:52 GMT
ENV TELEGRAF_VERSION=1.24.2
# Wed, 05 Oct 2022 17:52:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Oct 2022 17:52:57 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Oct 2022 17:52:59 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 05 Oct 2022 17:52:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 17:53:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37c953a37e989b49a533e8d08c80d87ce66fadee48160f9a4d8cd2dd5b0ec87`  
		Last Modified: Wed, 05 Oct 2022 00:37:21 GMT  
		Size: 4.9 MB (4944361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98802a15fc60bda24c79203236f930586f1dba6218aa2b4c121cf0dbf5627b38`  
		Last Modified: Wed, 05 Oct 2022 00:37:22 GMT  
		Size: 10.7 MB (10657400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22398aa42c1b74e8b8aa86450b2606b08a367992108afd66f03799f1393932ef`  
		Last Modified: Wed, 05 Oct 2022 17:53:26 GMT  
		Size: 18.4 MB (18382830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50578a1c2d11fdb0e84248fb7effbf5bc328dc0f95e2f855be12c15e333f02af`  
		Last Modified: Wed, 05 Oct 2022 17:53:23 GMT  
		Size: 2.9 KB (2860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9174328e2187fa4664cf5c87ea2fd53c187664bc4b6f8cc249146ebb422c1b7`  
		Last Modified: Wed, 05 Oct 2022 17:54:04 GMT  
		Size: 39.9 MB (39894136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0757b0a107178edfae558b254d8f2be8c846b0971b0ba21a1c042a31e5384ee7`  
		Last Modified: Wed, 05 Oct 2022 17:53:58 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.24-alpine`

```console
$ docker pull telegraf@sha256:79f31359c2dc968fa6ec9a310f639366349b70d7696b13d7d1b1ae6ac833203e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.24-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:df8365931560dcbc7b4932c4d54a16a1e18b0fa20905cc84e4bf900a1784314b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49964024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfccdc00226cd049281da9cf00567b42c20337b80abb08a317213fceaed6cbde`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:59:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 07 Oct 2022 04:19:22 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Fri, 07 Oct 2022 04:19:46 GMT
ENV TELEGRAF_VERSION=1.24.2
# Fri, 07 Oct 2022 04:19:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Fri, 07 Oct 2022 04:19:54 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 07 Oct 2022 04:19:54 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Fri, 07 Oct 2022 04:19:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 04:19:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d30442cf8411e7f53657b11f2e08ef81065f359c49d13af3d255eb9ce50bd8`  
		Last Modified: Thu, 06 Oct 2022 23:00:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df12bedc10645580477742185fbda69b5e253e91012a2898380cae67461d4c7`  
		Last Modified: Fri, 07 Oct 2022 04:20:16 GMT  
		Size: 3.3 MB (3310249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8149f95e616abc317967fe87a6cf8d29f0a9861a63850406e57a7b64d8bead`  
		Last Modified: Fri, 07 Oct 2022 04:20:57 GMT  
		Size: 43.8 MB (43847240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4311e5314ed466b831892d8dede2255f089777346f1d5ef0db5a5427a0152f03`  
		Last Modified: Fri, 07 Oct 2022 04:20:49 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.24.2`

```console
$ docker pull telegraf@sha256:c041b149b338b1edeac1d9cfdaed9531842621e20d3863e04034fb8bfa897f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.24.2` - linux; amd64

```console
$ docker pull telegraf@sha256:2d544a60af363eb9710022f41d4109e836a9c82951225073dd6d07d9f243a8a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133856512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548e4f33b1dc8068c849c0c96e5918539c9ba1647f647c89c0ca3fca68cece74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:54:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:55:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 23:03:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 23:03:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 23:03:19 GMT
ENV TELEGRAF_VERSION=1.24.2
# Wed, 05 Oct 2022 23:03:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Oct 2022 23:03:23 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Oct 2022 23:03:23 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 05 Oct 2022 23:03:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 23:03:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47db815c6a4547dc224b75222193cb1851cf529d2cbdf26f854b9bbf97099b98`  
		Last Modified: Wed, 05 Oct 2022 01:19:13 GMT  
		Size: 5.2 MB (5163279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf48494000001a037b72870d2a6a2536f9da8bc5d1ceddd72d79f4a51fe7a60e`  
		Last Modified: Wed, 05 Oct 2022 01:19:13 GMT  
		Size: 10.9 MB (10876505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863a7459c8fe546ab3b805bc6fb6f6e8b01bcf7411513f42699201aacfc4bb9c`  
		Last Modified: Wed, 05 Oct 2022 23:03:48 GMT  
		Size: 18.8 MB (18760121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e28af260775d457e7415a6995724f47b2d5a7b97a31a0c7d14f0c8a2ff1c257`  
		Last Modified: Wed, 05 Oct 2022 23:03:45 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f15f27d873fce4dbd5165fb753fc5b702a3ffcff509b667742a60950fcc8261`  
		Last Modified: Wed, 05 Oct 2022 23:04:31 GMT  
		Size: 44.0 MB (44007118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b89a3dd513bbc50e6ff4df223ff078d1bacaad986a61fb7b6d91a14f74ad95a`  
		Last Modified: Wed, 05 Oct 2022 23:04:24 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.24.2` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7da547f0b06db7b505c678289103bf96bef2dcbb9606fee01663470b490d0c2e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123881365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c29fad03d96db8d2b5cd496a1dc6ff839d055f6dd82fc3cd603a3f6d5e46f96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:28 GMT
ADD file:47a3f2948af18c39686ca59a88a439c25edaf286064d3a2ccc5dab47fee2fc52 in / 
# Tue, 04 Oct 2022 23:58:29 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:32:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:32:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 06 Oct 2022 16:07:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 16:07:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 06 Oct 2022 16:07:35 GMT
ENV TELEGRAF_VERSION=1.24.2
# Thu, 06 Oct 2022 16:07:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 06 Oct 2022 16:07:41 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 06 Oct 2022 16:07:41 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 06 Oct 2022 16:07:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 16:07:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e19342fb46cabf6147aec1d1c6af1f3a82736530cf3b067835fc8a09da092ce3`  
		Last Modified: Wed, 05 Oct 2022 00:04:36 GMT  
		Size: 50.2 MB (50209087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49f93f990f17337480b5bdf526a6bb48d1ae63bd17f54be17cd2f6ebba4de7d`  
		Last Modified: Wed, 05 Oct 2022 00:53:28 GMT  
		Size: 4.9 MB (4931366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3989be0d7ed2f72fae0310039043f6ba76c24a45f9ec9689697ebd932845cc8`  
		Last Modified: Wed, 05 Oct 2022 00:53:28 GMT  
		Size: 10.2 MB (10217872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef23f3c089cb85cd0436535aeb8422fbfd379b3a897532a89f1c2fea29728e03`  
		Last Modified: Thu, 06 Oct 2022 16:08:13 GMT  
		Size: 17.5 MB (17462363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a05f53155f290b1fb830a5da47f116e34fb30b79dcd539c2e8d735f10fd13ac`  
		Last Modified: Thu, 06 Oct 2022 16:08:09 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0c43f9c460c0df3bccd6147aec132029dfcb6c97462b59494d46b61d2fa73b`  
		Last Modified: Thu, 06 Oct 2022 16:08:55 GMT  
		Size: 41.1 MB (41057433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c573a3fdf94f1a4476208d9bdcf1c919fbae54e198fa626b45e7afa62cf99a8`  
		Last Modified: Thu, 06 Oct 2022 16:08:48 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.24.2` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ec9785ee6a1f0f6c15aff3757860c2ceadab3d1e16105f1ed6eae6ef8126ad46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127582555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aab2522ba7f26a4e559c798050d9111fd3a140acd7d2c89a49e93f9e001d6cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:23:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:23:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 17:52:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:52:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 17:52:52 GMT
ENV TELEGRAF_VERSION=1.24.2
# Wed, 05 Oct 2022 17:52:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Oct 2022 17:52:57 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Oct 2022 17:52:59 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 05 Oct 2022 17:52:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 17:53:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37c953a37e989b49a533e8d08c80d87ce66fadee48160f9a4d8cd2dd5b0ec87`  
		Last Modified: Wed, 05 Oct 2022 00:37:21 GMT  
		Size: 4.9 MB (4944361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98802a15fc60bda24c79203236f930586f1dba6218aa2b4c121cf0dbf5627b38`  
		Last Modified: Wed, 05 Oct 2022 00:37:22 GMT  
		Size: 10.7 MB (10657400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22398aa42c1b74e8b8aa86450b2606b08a367992108afd66f03799f1393932ef`  
		Last Modified: Wed, 05 Oct 2022 17:53:26 GMT  
		Size: 18.4 MB (18382830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50578a1c2d11fdb0e84248fb7effbf5bc328dc0f95e2f855be12c15e333f02af`  
		Last Modified: Wed, 05 Oct 2022 17:53:23 GMT  
		Size: 2.9 KB (2860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9174328e2187fa4664cf5c87ea2fd53c187664bc4b6f8cc249146ebb422c1b7`  
		Last Modified: Wed, 05 Oct 2022 17:54:04 GMT  
		Size: 39.9 MB (39894136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0757b0a107178edfae558b254d8f2be8c846b0971b0ba21a1c042a31e5384ee7`  
		Last Modified: Wed, 05 Oct 2022 17:53:58 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.24.2-alpine`

```console
$ docker pull telegraf@sha256:79f31359c2dc968fa6ec9a310f639366349b70d7696b13d7d1b1ae6ac833203e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.24.2-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:df8365931560dcbc7b4932c4d54a16a1e18b0fa20905cc84e4bf900a1784314b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49964024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfccdc00226cd049281da9cf00567b42c20337b80abb08a317213fceaed6cbde`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:59:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 07 Oct 2022 04:19:22 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Fri, 07 Oct 2022 04:19:46 GMT
ENV TELEGRAF_VERSION=1.24.2
# Fri, 07 Oct 2022 04:19:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Fri, 07 Oct 2022 04:19:54 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 07 Oct 2022 04:19:54 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Fri, 07 Oct 2022 04:19:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 04:19:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d30442cf8411e7f53657b11f2e08ef81065f359c49d13af3d255eb9ce50bd8`  
		Last Modified: Thu, 06 Oct 2022 23:00:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df12bedc10645580477742185fbda69b5e253e91012a2898380cae67461d4c7`  
		Last Modified: Fri, 07 Oct 2022 04:20:16 GMT  
		Size: 3.3 MB (3310249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8149f95e616abc317967fe87a6cf8d29f0a9861a63850406e57a7b64d8bead`  
		Last Modified: Fri, 07 Oct 2022 04:20:57 GMT  
		Size: 43.8 MB (43847240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4311e5314ed466b831892d8dede2255f089777346f1d5ef0db5a5427a0152f03`  
		Last Modified: Fri, 07 Oct 2022 04:20:49 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:79f31359c2dc968fa6ec9a310f639366349b70d7696b13d7d1b1ae6ac833203e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:df8365931560dcbc7b4932c4d54a16a1e18b0fa20905cc84e4bf900a1784314b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49964024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfccdc00226cd049281da9cf00567b42c20337b80abb08a317213fceaed6cbde`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:59:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 07 Oct 2022 04:19:22 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Fri, 07 Oct 2022 04:19:46 GMT
ENV TELEGRAF_VERSION=1.24.2
# Fri, 07 Oct 2022 04:19:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Fri, 07 Oct 2022 04:19:54 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 07 Oct 2022 04:19:54 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Fri, 07 Oct 2022 04:19:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 04:19:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d30442cf8411e7f53657b11f2e08ef81065f359c49d13af3d255eb9ce50bd8`  
		Last Modified: Thu, 06 Oct 2022 23:00:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df12bedc10645580477742185fbda69b5e253e91012a2898380cae67461d4c7`  
		Last Modified: Fri, 07 Oct 2022 04:20:16 GMT  
		Size: 3.3 MB (3310249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8149f95e616abc317967fe87a6cf8d29f0a9861a63850406e57a7b64d8bead`  
		Last Modified: Fri, 07 Oct 2022 04:20:57 GMT  
		Size: 43.8 MB (43847240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4311e5314ed466b831892d8dede2255f089777346f1d5ef0db5a5427a0152f03`  
		Last Modified: Fri, 07 Oct 2022 04:20:49 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:c041b149b338b1edeac1d9cfdaed9531842621e20d3863e04034fb8bfa897f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:2d544a60af363eb9710022f41d4109e836a9c82951225073dd6d07d9f243a8a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133856512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548e4f33b1dc8068c849c0c96e5918539c9ba1647f647c89c0ca3fca68cece74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:54:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:55:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 23:03:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 23:03:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 23:03:19 GMT
ENV TELEGRAF_VERSION=1.24.2
# Wed, 05 Oct 2022 23:03:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Oct 2022 23:03:23 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Oct 2022 23:03:23 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 05 Oct 2022 23:03:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 23:03:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47db815c6a4547dc224b75222193cb1851cf529d2cbdf26f854b9bbf97099b98`  
		Last Modified: Wed, 05 Oct 2022 01:19:13 GMT  
		Size: 5.2 MB (5163279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf48494000001a037b72870d2a6a2536f9da8bc5d1ceddd72d79f4a51fe7a60e`  
		Last Modified: Wed, 05 Oct 2022 01:19:13 GMT  
		Size: 10.9 MB (10876505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863a7459c8fe546ab3b805bc6fb6f6e8b01bcf7411513f42699201aacfc4bb9c`  
		Last Modified: Wed, 05 Oct 2022 23:03:48 GMT  
		Size: 18.8 MB (18760121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e28af260775d457e7415a6995724f47b2d5a7b97a31a0c7d14f0c8a2ff1c257`  
		Last Modified: Wed, 05 Oct 2022 23:03:45 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f15f27d873fce4dbd5165fb753fc5b702a3ffcff509b667742a60950fcc8261`  
		Last Modified: Wed, 05 Oct 2022 23:04:31 GMT  
		Size: 44.0 MB (44007118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b89a3dd513bbc50e6ff4df223ff078d1bacaad986a61fb7b6d91a14f74ad95a`  
		Last Modified: Wed, 05 Oct 2022 23:04:24 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7da547f0b06db7b505c678289103bf96bef2dcbb9606fee01663470b490d0c2e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123881365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c29fad03d96db8d2b5cd496a1dc6ff839d055f6dd82fc3cd603a3f6d5e46f96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:28 GMT
ADD file:47a3f2948af18c39686ca59a88a439c25edaf286064d3a2ccc5dab47fee2fc52 in / 
# Tue, 04 Oct 2022 23:58:29 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:32:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:32:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 06 Oct 2022 16:07:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 16:07:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 06 Oct 2022 16:07:35 GMT
ENV TELEGRAF_VERSION=1.24.2
# Thu, 06 Oct 2022 16:07:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 06 Oct 2022 16:07:41 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 06 Oct 2022 16:07:41 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 06 Oct 2022 16:07:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 16:07:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e19342fb46cabf6147aec1d1c6af1f3a82736530cf3b067835fc8a09da092ce3`  
		Last Modified: Wed, 05 Oct 2022 00:04:36 GMT  
		Size: 50.2 MB (50209087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49f93f990f17337480b5bdf526a6bb48d1ae63bd17f54be17cd2f6ebba4de7d`  
		Last Modified: Wed, 05 Oct 2022 00:53:28 GMT  
		Size: 4.9 MB (4931366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3989be0d7ed2f72fae0310039043f6ba76c24a45f9ec9689697ebd932845cc8`  
		Last Modified: Wed, 05 Oct 2022 00:53:28 GMT  
		Size: 10.2 MB (10217872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef23f3c089cb85cd0436535aeb8422fbfd379b3a897532a89f1c2fea29728e03`  
		Last Modified: Thu, 06 Oct 2022 16:08:13 GMT  
		Size: 17.5 MB (17462363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a05f53155f290b1fb830a5da47f116e34fb30b79dcd539c2e8d735f10fd13ac`  
		Last Modified: Thu, 06 Oct 2022 16:08:09 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0c43f9c460c0df3bccd6147aec132029dfcb6c97462b59494d46b61d2fa73b`  
		Last Modified: Thu, 06 Oct 2022 16:08:55 GMT  
		Size: 41.1 MB (41057433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c573a3fdf94f1a4476208d9bdcf1c919fbae54e198fa626b45e7afa62cf99a8`  
		Last Modified: Thu, 06 Oct 2022 16:08:48 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ec9785ee6a1f0f6c15aff3757860c2ceadab3d1e16105f1ed6eae6ef8126ad46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127582555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aab2522ba7f26a4e559c798050d9111fd3a140acd7d2c89a49e93f9e001d6cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:23:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:23:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 17:52:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:52:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 17:52:52 GMT
ENV TELEGRAF_VERSION=1.24.2
# Wed, 05 Oct 2022 17:52:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Oct 2022 17:52:57 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Oct 2022 17:52:59 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 05 Oct 2022 17:52:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 17:53:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37c953a37e989b49a533e8d08c80d87ce66fadee48160f9a4d8cd2dd5b0ec87`  
		Last Modified: Wed, 05 Oct 2022 00:37:21 GMT  
		Size: 4.9 MB (4944361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98802a15fc60bda24c79203236f930586f1dba6218aa2b4c121cf0dbf5627b38`  
		Last Modified: Wed, 05 Oct 2022 00:37:22 GMT  
		Size: 10.7 MB (10657400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22398aa42c1b74e8b8aa86450b2606b08a367992108afd66f03799f1393932ef`  
		Last Modified: Wed, 05 Oct 2022 17:53:26 GMT  
		Size: 18.4 MB (18382830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50578a1c2d11fdb0e84248fb7effbf5bc328dc0f95e2f855be12c15e333f02af`  
		Last Modified: Wed, 05 Oct 2022 17:53:23 GMT  
		Size: 2.9 KB (2860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9174328e2187fa4664cf5c87ea2fd53c187664bc4b6f8cc249146ebb422c1b7`  
		Last Modified: Wed, 05 Oct 2022 17:54:04 GMT  
		Size: 39.9 MB (39894136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0757b0a107178edfae558b254d8f2be8c846b0971b0ba21a1c042a31e5384ee7`  
		Last Modified: Wed, 05 Oct 2022 17:53:58 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
