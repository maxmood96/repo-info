<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.18`](#telegraf118)
-	[`telegraf:1.18-alpine`](#telegraf118-alpine)
-	[`telegraf:1.18.3`](#telegraf1183)
-	[`telegraf:1.18.3-alpine`](#telegraf1183-alpine)
-	[`telegraf:1.19`](#telegraf119)
-	[`telegraf:1.19-alpine`](#telegraf119-alpine)
-	[`telegraf:1.19.3`](#telegraf1193)
-	[`telegraf:1.19.3-alpine`](#telegraf1193-alpine)
-	[`telegraf:1.20`](#telegraf120)
-	[`telegraf:1.20-alpine`](#telegraf120-alpine)
-	[`telegraf:1.20.4`](#telegraf1204)
-	[`telegraf:1.20.4-alpine`](#telegraf1204-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.18`

```console
$ docker pull telegraf@sha256:dba6fde3609fd3f124bc74b4ba591855260a8ff3336a372c1fcdcf9aac9f8ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.18` - linux; amd64

```console
$ docker pull telegraf@sha256:91a1840e4c0aa0e96ec8d2684b9eea409f0b2c79c0a5f574b0f6d01438047dea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115494381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a2a930efa3a704ef8231ef72a923d38e51651a57775ad6f7b8afa4946c7cfa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:31 GMT
ADD file:f077e1a42fb919be2af67820782ceee3b46ffd13d7ab6949bea9921217d12813 in / 
# Thu, 02 Dec 2021 02:48:32 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:41:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:41:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Dec 2021 04:32:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 04:32:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 04:32:19 GMT
ENV TELEGRAF_VERSION=1.18.3
# Fri, 03 Dec 2021 04:32:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 03 Dec 2021 04:32:24 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 03 Dec 2021 04:32:24 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 03 Dec 2021 04:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 04:32:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c4cc477c22ba7abce860198107408434dd7bd73ddbaf82f1e69ab941b9979405`  
		Last Modified: Thu, 02 Dec 2021 02:54:07 GMT  
		Size: 50.4 MB (50437113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077c54d048f1f1a1f28079caa54bf5d99803f937ffe5c1dc6e207698f70b4e74`  
		Last Modified: Thu, 02 Dec 2021 03:50:46 GMT  
		Size: 7.8 MB (7833819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368544993b2deeeffdd19463cdf92ec4e39f83073de5de316f9f5c725ab403f`  
		Last Modified: Thu, 02 Dec 2021 03:50:46 GMT  
		Size: 10.0 MB (9997240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d19fc3bb1a1152e2be5e863a11ffafd241f042019bc0191614d8552ef25b3fd`  
		Last Modified: Fri, 03 Dec 2021 04:33:13 GMT  
		Size: 17.4 MB (17415385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ada106a1ddfa307bb6f3b252de34b237c4dd398272b5c71c9ae6d8fa1e56abf`  
		Last Modified: Fri, 03 Dec 2021 04:33:10 GMT  
		Size: 2.9 KB (2906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca85ede0b8912b4a206440adda30884162bf1e62bbfd011c23257344633b648b`  
		Last Modified: Fri, 03 Dec 2021 04:33:16 GMT  
		Size: 29.8 MB (29807687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697f9ba09b3a69f48faf8a9cee0e2c572ed5f5bbcdb2389de9ea4b22898d2231`  
		Last Modified: Fri, 03 Dec 2021 04:33:10 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.18` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:ff53ff60cf0e6c120f9ce7089ec72f59b5da6e5b8b8283d8031b9c238368cb19
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106106749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c399799cf4c8d99ffbe2aec8bfc3a39e8a0746fb51218cd5585e336c68358cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:12 GMT
ADD file:d71807613acdf86685f6d640a90e27b7b63cfe0f13d88668ee943aca089d8876 in / 
# Wed, 17 Nov 2021 02:00:13 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 02:45:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 19 Nov 2021 06:57:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 19 Nov 2021 06:57:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 19 Nov 2021 06:57:40 GMT
ENV TELEGRAF_VERSION=1.18.3
# Fri, 19 Nov 2021 06:57:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 19 Nov 2021 06:57:50 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 19 Nov 2021 06:57:51 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 19 Nov 2021 06:57:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Nov 2021 06:57:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:10acd81022d17f452439d0385615fa066b8f0ddcf3c1a803872eec5bdc6acf64`  
		Last Modified: Wed, 17 Nov 2021 02:16:00 GMT  
		Size: 45.9 MB (45918099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a9604eb6c465f658d6422593d504030155029fe0c4302451d4369030c29144`  
		Last Modified: Wed, 17 Nov 2021 03:07:14 GMT  
		Size: 7.1 MB (7125194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043b954c4f0757e89df96897cea2cf1f93c6275466008e4ba7a4b1089c7dd3d`  
		Last Modified: Wed, 17 Nov 2021 03:07:15 GMT  
		Size: 9.3 MB (9343839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f948c503612d7c3256c810d1947e6739199bedadaa86c607aaf0a20748fd2e28`  
		Last Modified: Fri, 19 Nov 2021 06:59:38 GMT  
		Size: 16.2 MB (16161406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a5c71a30ea8197d13500f671181ef00e946261de58f9df4450d46f71292b94`  
		Last Modified: Fri, 19 Nov 2021 06:59:26 GMT  
		Size: 2.9 KB (2907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64204edbae5b69711bed83dc2a6461cad0472198a5d4ecc22850d64c18caa37`  
		Last Modified: Fri, 19 Nov 2021 06:59:45 GMT  
		Size: 27.6 MB (27555073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38a4bdeb238c2a32f1581645af485da48e802d9a0e8bd387f6a3139698faf68`  
		Last Modified: Fri, 19 Nov 2021 06:59:27 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.18` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3874d1ad563ef679e5339c2bd39691e8b86857a669726b53ec6438a33ab2ea05
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110720669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9289cb5d8fe4f7f7bd96b1bf89d1ec9f5ea02e80bb75b3133fdc437fc1f53227`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:20 GMT
ADD file:82c1819d8416d9d44564980e25e98a081f813bc2ee8ad2789114fe37e802848f in / 
# Thu, 02 Dec 2021 08:08:20 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:54:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:54:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Dec 2021 05:04:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 05:04:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 05:04:12 GMT
ENV TELEGRAF_VERSION=1.18.3
# Fri, 03 Dec 2021 05:04:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 03 Dec 2021 05:04:17 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 03 Dec 2021 05:04:19 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 03 Dec 2021 05:04:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 05:04:20 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:39e4f823356a9e2dbba530f9d363b4d76beaff75a13bad788d38eebeae67e5b0`  
		Last Modified: Thu, 02 Dec 2021 08:41:08 GMT  
		Size: 49.2 MB (49223045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df66cf961d4016eccee4ce9bc5dc18dcd99e9f9963e66c4980a66e6492a421b2`  
		Last Modified: Thu, 02 Dec 2021 10:03:39 GMT  
		Size: 7.7 MB (7695103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6c547e43b8b6afdfae413ba7a49c1120d0534fff63c4a242ef611d562a678c`  
		Last Modified: Thu, 02 Dec 2021 10:03:39 GMT  
		Size: 9.8 MB (9767269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad6f83cdf6241198d4e908c6f92b100cf9cc4dc5242b4d38550ca7639929981`  
		Last Modified: Fri, 03 Dec 2021 05:05:12 GMT  
		Size: 17.1 MB (17058986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5a73aa06cee308b9f2e886dd606487821f89cfcd4179ad928c98be2967203d`  
		Last Modified: Fri, 03 Dec 2021 05:05:09 GMT  
		Size: 2.9 KB (2877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44808f889762521d80f10db87b488c928479a2112a4c4ccac59bb1d89c051520`  
		Last Modified: Fri, 03 Dec 2021 05:05:14 GMT  
		Size: 27.0 MB (26973158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32251faceb0b2811f3d13d5f452b63693ac3ad584b293f3c45483b38b52d899b`  
		Last Modified: Fri, 03 Dec 2021 05:05:09 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18-alpine`

```console
$ docker pull telegraf@sha256:6aa02585a82331defaba9fa2d482579de674adda7a608a3f4a449089fd03c22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.18-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7036acf1cb6af49f02c4109ce8bb3a5938a17a9563ba3bd2ac8805ff7590e37c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35862269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b2815ff14c8ac1315ff16b32175e996f8f78d14d9e50860c8830372a871e52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Nov 2021 07:20:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Sat, 13 Nov 2021 07:20:28 GMT
ENV TELEGRAF_VERSION=1.18.3
# Sat, 13 Nov 2021 07:20:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 13 Nov 2021 07:20:44 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 13 Nov 2021 07:20:44 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Sat, 13 Nov 2021 07:20:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Nov 2021 07:20:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ae06dab0a6b50d3f23d332a8c326fd227bd58abc651b7033038337f97e077f`  
		Last Modified: Sat, 13 Nov 2021 07:21:57 GMT  
		Size: 3.4 MB (3371612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4b4cb0834236816551000b761fd652c542d20937310c681a0bd1a8c9e0c82c`  
		Last Modified: Sat, 13 Nov 2021 07:22:03 GMT  
		Size: 29.7 MB (29667313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ef8c5df072c949c20c7b8fc003a502452dce57577a3c495f513cf155ad4357`  
		Last Modified: Sat, 13 Nov 2021 07:21:56 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18.3`

```console
$ docker pull telegraf@sha256:dba6fde3609fd3f124bc74b4ba591855260a8ff3336a372c1fcdcf9aac9f8ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.18.3` - linux; amd64

```console
$ docker pull telegraf@sha256:91a1840e4c0aa0e96ec8d2684b9eea409f0b2c79c0a5f574b0f6d01438047dea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115494381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a2a930efa3a704ef8231ef72a923d38e51651a57775ad6f7b8afa4946c7cfa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:31 GMT
ADD file:f077e1a42fb919be2af67820782ceee3b46ffd13d7ab6949bea9921217d12813 in / 
# Thu, 02 Dec 2021 02:48:32 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:41:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:41:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Dec 2021 04:32:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 04:32:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 04:32:19 GMT
ENV TELEGRAF_VERSION=1.18.3
# Fri, 03 Dec 2021 04:32:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 03 Dec 2021 04:32:24 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 03 Dec 2021 04:32:24 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 03 Dec 2021 04:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 04:32:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c4cc477c22ba7abce860198107408434dd7bd73ddbaf82f1e69ab941b9979405`  
		Last Modified: Thu, 02 Dec 2021 02:54:07 GMT  
		Size: 50.4 MB (50437113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077c54d048f1f1a1f28079caa54bf5d99803f937ffe5c1dc6e207698f70b4e74`  
		Last Modified: Thu, 02 Dec 2021 03:50:46 GMT  
		Size: 7.8 MB (7833819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368544993b2deeeffdd19463cdf92ec4e39f83073de5de316f9f5c725ab403f`  
		Last Modified: Thu, 02 Dec 2021 03:50:46 GMT  
		Size: 10.0 MB (9997240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d19fc3bb1a1152e2be5e863a11ffafd241f042019bc0191614d8552ef25b3fd`  
		Last Modified: Fri, 03 Dec 2021 04:33:13 GMT  
		Size: 17.4 MB (17415385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ada106a1ddfa307bb6f3b252de34b237c4dd398272b5c71c9ae6d8fa1e56abf`  
		Last Modified: Fri, 03 Dec 2021 04:33:10 GMT  
		Size: 2.9 KB (2906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca85ede0b8912b4a206440adda30884162bf1e62bbfd011c23257344633b648b`  
		Last Modified: Fri, 03 Dec 2021 04:33:16 GMT  
		Size: 29.8 MB (29807687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697f9ba09b3a69f48faf8a9cee0e2c572ed5f5bbcdb2389de9ea4b22898d2231`  
		Last Modified: Fri, 03 Dec 2021 04:33:10 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.18.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:ff53ff60cf0e6c120f9ce7089ec72f59b5da6e5b8b8283d8031b9c238368cb19
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106106749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c399799cf4c8d99ffbe2aec8bfc3a39e8a0746fb51218cd5585e336c68358cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:12 GMT
ADD file:d71807613acdf86685f6d640a90e27b7b63cfe0f13d88668ee943aca089d8876 in / 
# Wed, 17 Nov 2021 02:00:13 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 02:45:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 19 Nov 2021 06:57:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 19 Nov 2021 06:57:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 19 Nov 2021 06:57:40 GMT
ENV TELEGRAF_VERSION=1.18.3
# Fri, 19 Nov 2021 06:57:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 19 Nov 2021 06:57:50 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 19 Nov 2021 06:57:51 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 19 Nov 2021 06:57:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Nov 2021 06:57:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:10acd81022d17f452439d0385615fa066b8f0ddcf3c1a803872eec5bdc6acf64`  
		Last Modified: Wed, 17 Nov 2021 02:16:00 GMT  
		Size: 45.9 MB (45918099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a9604eb6c465f658d6422593d504030155029fe0c4302451d4369030c29144`  
		Last Modified: Wed, 17 Nov 2021 03:07:14 GMT  
		Size: 7.1 MB (7125194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043b954c4f0757e89df96897cea2cf1f93c6275466008e4ba7a4b1089c7dd3d`  
		Last Modified: Wed, 17 Nov 2021 03:07:15 GMT  
		Size: 9.3 MB (9343839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f948c503612d7c3256c810d1947e6739199bedadaa86c607aaf0a20748fd2e28`  
		Last Modified: Fri, 19 Nov 2021 06:59:38 GMT  
		Size: 16.2 MB (16161406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a5c71a30ea8197d13500f671181ef00e946261de58f9df4450d46f71292b94`  
		Last Modified: Fri, 19 Nov 2021 06:59:26 GMT  
		Size: 2.9 KB (2907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64204edbae5b69711bed83dc2a6461cad0472198a5d4ecc22850d64c18caa37`  
		Last Modified: Fri, 19 Nov 2021 06:59:45 GMT  
		Size: 27.6 MB (27555073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38a4bdeb238c2a32f1581645af485da48e802d9a0e8bd387f6a3139698faf68`  
		Last Modified: Fri, 19 Nov 2021 06:59:27 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.18.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3874d1ad563ef679e5339c2bd39691e8b86857a669726b53ec6438a33ab2ea05
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110720669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9289cb5d8fe4f7f7bd96b1bf89d1ec9f5ea02e80bb75b3133fdc437fc1f53227`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:20 GMT
ADD file:82c1819d8416d9d44564980e25e98a081f813bc2ee8ad2789114fe37e802848f in / 
# Thu, 02 Dec 2021 08:08:20 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:54:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:54:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Dec 2021 05:04:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 05:04:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 05:04:12 GMT
ENV TELEGRAF_VERSION=1.18.3
# Fri, 03 Dec 2021 05:04:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 03 Dec 2021 05:04:17 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 03 Dec 2021 05:04:19 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 03 Dec 2021 05:04:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 05:04:20 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:39e4f823356a9e2dbba530f9d363b4d76beaff75a13bad788d38eebeae67e5b0`  
		Last Modified: Thu, 02 Dec 2021 08:41:08 GMT  
		Size: 49.2 MB (49223045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df66cf961d4016eccee4ce9bc5dc18dcd99e9f9963e66c4980a66e6492a421b2`  
		Last Modified: Thu, 02 Dec 2021 10:03:39 GMT  
		Size: 7.7 MB (7695103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6c547e43b8b6afdfae413ba7a49c1120d0534fff63c4a242ef611d562a678c`  
		Last Modified: Thu, 02 Dec 2021 10:03:39 GMT  
		Size: 9.8 MB (9767269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad6f83cdf6241198d4e908c6f92b100cf9cc4dc5242b4d38550ca7639929981`  
		Last Modified: Fri, 03 Dec 2021 05:05:12 GMT  
		Size: 17.1 MB (17058986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5a73aa06cee308b9f2e886dd606487821f89cfcd4179ad928c98be2967203d`  
		Last Modified: Fri, 03 Dec 2021 05:05:09 GMT  
		Size: 2.9 KB (2877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44808f889762521d80f10db87b488c928479a2112a4c4ccac59bb1d89c051520`  
		Last Modified: Fri, 03 Dec 2021 05:05:14 GMT  
		Size: 27.0 MB (26973158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32251faceb0b2811f3d13d5f452b63693ac3ad584b293f3c45483b38b52d899b`  
		Last Modified: Fri, 03 Dec 2021 05:05:09 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.18.3-alpine`

```console
$ docker pull telegraf@sha256:6aa02585a82331defaba9fa2d482579de674adda7a608a3f4a449089fd03c22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.18.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7036acf1cb6af49f02c4109ce8bb3a5938a17a9563ba3bd2ac8805ff7590e37c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35862269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b2815ff14c8ac1315ff16b32175e996f8f78d14d9e50860c8830372a871e52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Nov 2021 07:20:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Sat, 13 Nov 2021 07:20:28 GMT
ENV TELEGRAF_VERSION=1.18.3
# Sat, 13 Nov 2021 07:20:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 13 Nov 2021 07:20:44 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 13 Nov 2021 07:20:44 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Sat, 13 Nov 2021 07:20:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Nov 2021 07:20:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ae06dab0a6b50d3f23d332a8c326fd227bd58abc651b7033038337f97e077f`  
		Last Modified: Sat, 13 Nov 2021 07:21:57 GMT  
		Size: 3.4 MB (3371612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4b4cb0834236816551000b761fd652c542d20937310c681a0bd1a8c9e0c82c`  
		Last Modified: Sat, 13 Nov 2021 07:22:03 GMT  
		Size: 29.7 MB (29667313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ef8c5df072c949c20c7b8fc003a502452dce57577a3c495f513cf155ad4357`  
		Last Modified: Sat, 13 Nov 2021 07:21:56 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.19`

```console
$ docker pull telegraf@sha256:cc406578b19f31160767c10bfd06b1c189d53e072af57a628f879e75efadb33d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.19` - linux; amd64

```console
$ docker pull telegraf@sha256:01cd6c6915a16c4cbc868f2bb9c0961191df78f5396dfbe47ff84fbbafd45b27
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119874505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe01dc17288bc8b76c1a5cca7af4fa19a773ea0a049d414afa5c64ed1506509`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:31 GMT
ADD file:f077e1a42fb919be2af67820782ceee3b46ffd13d7ab6949bea9921217d12813 in / 
# Thu, 02 Dec 2021 02:48:32 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:41:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:41:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Dec 2021 04:32:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 04:32:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 04:32:29 GMT
ENV TELEGRAF_VERSION=1.19.3
# Fri, 03 Dec 2021 04:32:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 03 Dec 2021 04:32:35 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 03 Dec 2021 04:32:35 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 03 Dec 2021 04:32:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 04:32:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c4cc477c22ba7abce860198107408434dd7bd73ddbaf82f1e69ab941b9979405`  
		Last Modified: Thu, 02 Dec 2021 02:54:07 GMT  
		Size: 50.4 MB (50437113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077c54d048f1f1a1f28079caa54bf5d99803f937ffe5c1dc6e207698f70b4e74`  
		Last Modified: Thu, 02 Dec 2021 03:50:46 GMT  
		Size: 7.8 MB (7833819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368544993b2deeeffdd19463cdf92ec4e39f83073de5de316f9f5c725ab403f`  
		Last Modified: Thu, 02 Dec 2021 03:50:46 GMT  
		Size: 10.0 MB (9997240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d19fc3bb1a1152e2be5e863a11ffafd241f042019bc0191614d8552ef25b3fd`  
		Last Modified: Fri, 03 Dec 2021 04:33:13 GMT  
		Size: 17.4 MB (17415385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ada106a1ddfa307bb6f3b252de34b237c4dd398272b5c71c9ae6d8fa1e56abf`  
		Last Modified: Fri, 03 Dec 2021 04:33:10 GMT  
		Size: 2.9 KB (2906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c668f307c54ff5b2162cce4dbc304e3d2f48f88bbffefc1c4534e07cd82b81`  
		Last Modified: Fri, 03 Dec 2021 04:33:35 GMT  
		Size: 34.2 MB (34187811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc9e6e7e41ded48bd52e3fb816c55df760d51735b3745769ee473cd0e32a1b8`  
		Last Modified: Fri, 03 Dec 2021 04:33:27 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.19` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:90228f52b34d3d3d3d5f6368a124f711677fe674d856568bfefb542006f1aaf9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110246198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba66f1c126cb23803294193a275666e29e27d85a8e520387ab137bce65e1857`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:12 GMT
ADD file:d71807613acdf86685f6d640a90e27b7b63cfe0f13d88668ee943aca089d8876 in / 
# Wed, 17 Nov 2021 02:00:13 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 02:45:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 19 Nov 2021 06:57:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 19 Nov 2021 06:57:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 19 Nov 2021 06:58:03 GMT
ENV TELEGRAF_VERSION=1.19.3
# Fri, 19 Nov 2021 06:58:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 19 Nov 2021 06:58:15 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 19 Nov 2021 06:58:16 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 19 Nov 2021 06:58:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Nov 2021 06:58:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:10acd81022d17f452439d0385615fa066b8f0ddcf3c1a803872eec5bdc6acf64`  
		Last Modified: Wed, 17 Nov 2021 02:16:00 GMT  
		Size: 45.9 MB (45918099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a9604eb6c465f658d6422593d504030155029fe0c4302451d4369030c29144`  
		Last Modified: Wed, 17 Nov 2021 03:07:14 GMT  
		Size: 7.1 MB (7125194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043b954c4f0757e89df96897cea2cf1f93c6275466008e4ba7a4b1089c7dd3d`  
		Last Modified: Wed, 17 Nov 2021 03:07:15 GMT  
		Size: 9.3 MB (9343839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f948c503612d7c3256c810d1947e6739199bedadaa86c607aaf0a20748fd2e28`  
		Last Modified: Fri, 19 Nov 2021 06:59:38 GMT  
		Size: 16.2 MB (16161406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a5c71a30ea8197d13500f671181ef00e946261de58f9df4450d46f71292b94`  
		Last Modified: Fri, 19 Nov 2021 06:59:26 GMT  
		Size: 2.9 KB (2907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbbb4e17729f251dc3f9513f36c054c2d6ac052717167eec8a88b6bc04e2702`  
		Last Modified: Fri, 19 Nov 2021 07:00:19 GMT  
		Size: 31.7 MB (31694521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c903f87cb7852570162bd2bb538accf97ea40954a82b515c40d947c9d306c3b2`  
		Last Modified: Fri, 19 Nov 2021 06:59:57 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.19` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:215857f883e1df3d8c112471caa472bc213c5c369498809124131c655929bd31
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114714046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09eacedbde5f9a93956881ac8df56359ab4d629effe4fea02de5acf1bdf7be82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:20 GMT
ADD file:82c1819d8416d9d44564980e25e98a081f813bc2ee8ad2789114fe37e802848f in / 
# Thu, 02 Dec 2021 08:08:20 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:54:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:54:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Dec 2021 05:04:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 05:04:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 05:04:27 GMT
ENV TELEGRAF_VERSION=1.19.3
# Fri, 03 Dec 2021 05:04:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 03 Dec 2021 05:04:32 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 03 Dec 2021 05:04:33 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 03 Dec 2021 05:04:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 05:04:34 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:39e4f823356a9e2dbba530f9d363b4d76beaff75a13bad788d38eebeae67e5b0`  
		Last Modified: Thu, 02 Dec 2021 08:41:08 GMT  
		Size: 49.2 MB (49223045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df66cf961d4016eccee4ce9bc5dc18dcd99e9f9963e66c4980a66e6492a421b2`  
		Last Modified: Thu, 02 Dec 2021 10:03:39 GMT  
		Size: 7.7 MB (7695103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6c547e43b8b6afdfae413ba7a49c1120d0534fff63c4a242ef611d562a678c`  
		Last Modified: Thu, 02 Dec 2021 10:03:39 GMT  
		Size: 9.8 MB (9767269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad6f83cdf6241198d4e908c6f92b100cf9cc4dc5242b4d38550ca7639929981`  
		Last Modified: Fri, 03 Dec 2021 05:05:12 GMT  
		Size: 17.1 MB (17058986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5a73aa06cee308b9f2e886dd606487821f89cfcd4179ad928c98be2967203d`  
		Last Modified: Fri, 03 Dec 2021 05:05:09 GMT  
		Size: 2.9 KB (2877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e603812d6b94f46c6224abdccbdaff25d2713289fbb1bbb6b934db50bf83bf`  
		Last Modified: Fri, 03 Dec 2021 05:05:30 GMT  
		Size: 31.0 MB (30966536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5114bc5c46d3e1283ccbe04ee39854b4247c8371980d2572baa46f5a344582`  
		Last Modified: Fri, 03 Dec 2021 05:05:25 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.19-alpine`

```console
$ docker pull telegraf@sha256:9e391c4169ccb91b1001061dae70fac58ab82165f4079e7ec039e9d84a4b5ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.19-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:627ea1f7f074a431873307fdba4c402fd567078bcc892dd9db37c5b26628f8c0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40241320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b97513bb4d721e5e1acbe529575e7db4451fc351934ce3ddee001d8183371b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Nov 2021 07:20:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Sat, 13 Nov 2021 07:20:51 GMT
ENV TELEGRAF_VERSION=1.19.3
# Sat, 13 Nov 2021 07:21:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 13 Nov 2021 07:21:05 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 13 Nov 2021 07:21:05 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Sat, 13 Nov 2021 07:21:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Nov 2021 07:21:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ae06dab0a6b50d3f23d332a8c326fd227bd58abc651b7033038337f97e077f`  
		Last Modified: Sat, 13 Nov 2021 07:21:57 GMT  
		Size: 3.4 MB (3371612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269b03bad908f1f612f0e6e5f1618e234a49ac3fcf23cd4f579ae4e09117ac49`  
		Last Modified: Sat, 13 Nov 2021 07:22:22 GMT  
		Size: 34.0 MB (34046365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63e1ff47e2021e70246af4383776e6845936e12e0337f4540c023f664bbe5bd`  
		Last Modified: Sat, 13 Nov 2021 07:22:14 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.19.3`

```console
$ docker pull telegraf@sha256:cc406578b19f31160767c10bfd06b1c189d53e072af57a628f879e75efadb33d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.19.3` - linux; amd64

```console
$ docker pull telegraf@sha256:01cd6c6915a16c4cbc868f2bb9c0961191df78f5396dfbe47ff84fbbafd45b27
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119874505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe01dc17288bc8b76c1a5cca7af4fa19a773ea0a049d414afa5c64ed1506509`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:31 GMT
ADD file:f077e1a42fb919be2af67820782ceee3b46ffd13d7ab6949bea9921217d12813 in / 
# Thu, 02 Dec 2021 02:48:32 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:41:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:41:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Dec 2021 04:32:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 04:32:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 04:32:29 GMT
ENV TELEGRAF_VERSION=1.19.3
# Fri, 03 Dec 2021 04:32:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 03 Dec 2021 04:32:35 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 03 Dec 2021 04:32:35 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 03 Dec 2021 04:32:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 04:32:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c4cc477c22ba7abce860198107408434dd7bd73ddbaf82f1e69ab941b9979405`  
		Last Modified: Thu, 02 Dec 2021 02:54:07 GMT  
		Size: 50.4 MB (50437113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077c54d048f1f1a1f28079caa54bf5d99803f937ffe5c1dc6e207698f70b4e74`  
		Last Modified: Thu, 02 Dec 2021 03:50:46 GMT  
		Size: 7.8 MB (7833819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368544993b2deeeffdd19463cdf92ec4e39f83073de5de316f9f5c725ab403f`  
		Last Modified: Thu, 02 Dec 2021 03:50:46 GMT  
		Size: 10.0 MB (9997240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d19fc3bb1a1152e2be5e863a11ffafd241f042019bc0191614d8552ef25b3fd`  
		Last Modified: Fri, 03 Dec 2021 04:33:13 GMT  
		Size: 17.4 MB (17415385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ada106a1ddfa307bb6f3b252de34b237c4dd398272b5c71c9ae6d8fa1e56abf`  
		Last Modified: Fri, 03 Dec 2021 04:33:10 GMT  
		Size: 2.9 KB (2906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c668f307c54ff5b2162cce4dbc304e3d2f48f88bbffefc1c4534e07cd82b81`  
		Last Modified: Fri, 03 Dec 2021 04:33:35 GMT  
		Size: 34.2 MB (34187811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc9e6e7e41ded48bd52e3fb816c55df760d51735b3745769ee473cd0e32a1b8`  
		Last Modified: Fri, 03 Dec 2021 04:33:27 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.19.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:90228f52b34d3d3d3d5f6368a124f711677fe674d856568bfefb542006f1aaf9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110246198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba66f1c126cb23803294193a275666e29e27d85a8e520387ab137bce65e1857`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:12 GMT
ADD file:d71807613acdf86685f6d640a90e27b7b63cfe0f13d88668ee943aca089d8876 in / 
# Wed, 17 Nov 2021 02:00:13 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 02:45:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 19 Nov 2021 06:57:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 19 Nov 2021 06:57:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 19 Nov 2021 06:58:03 GMT
ENV TELEGRAF_VERSION=1.19.3
# Fri, 19 Nov 2021 06:58:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 19 Nov 2021 06:58:15 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 19 Nov 2021 06:58:16 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 19 Nov 2021 06:58:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Nov 2021 06:58:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:10acd81022d17f452439d0385615fa066b8f0ddcf3c1a803872eec5bdc6acf64`  
		Last Modified: Wed, 17 Nov 2021 02:16:00 GMT  
		Size: 45.9 MB (45918099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a9604eb6c465f658d6422593d504030155029fe0c4302451d4369030c29144`  
		Last Modified: Wed, 17 Nov 2021 03:07:14 GMT  
		Size: 7.1 MB (7125194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043b954c4f0757e89df96897cea2cf1f93c6275466008e4ba7a4b1089c7dd3d`  
		Last Modified: Wed, 17 Nov 2021 03:07:15 GMT  
		Size: 9.3 MB (9343839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f948c503612d7c3256c810d1947e6739199bedadaa86c607aaf0a20748fd2e28`  
		Last Modified: Fri, 19 Nov 2021 06:59:38 GMT  
		Size: 16.2 MB (16161406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a5c71a30ea8197d13500f671181ef00e946261de58f9df4450d46f71292b94`  
		Last Modified: Fri, 19 Nov 2021 06:59:26 GMT  
		Size: 2.9 KB (2907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbbb4e17729f251dc3f9513f36c054c2d6ac052717167eec8a88b6bc04e2702`  
		Last Modified: Fri, 19 Nov 2021 07:00:19 GMT  
		Size: 31.7 MB (31694521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c903f87cb7852570162bd2bb538accf97ea40954a82b515c40d947c9d306c3b2`  
		Last Modified: Fri, 19 Nov 2021 06:59:57 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.19.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:215857f883e1df3d8c112471caa472bc213c5c369498809124131c655929bd31
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114714046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09eacedbde5f9a93956881ac8df56359ab4d629effe4fea02de5acf1bdf7be82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:20 GMT
ADD file:82c1819d8416d9d44564980e25e98a081f813bc2ee8ad2789114fe37e802848f in / 
# Thu, 02 Dec 2021 08:08:20 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:54:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:54:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Dec 2021 05:04:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 05:04:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 05:04:27 GMT
ENV TELEGRAF_VERSION=1.19.3
# Fri, 03 Dec 2021 05:04:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 03 Dec 2021 05:04:32 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 03 Dec 2021 05:04:33 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 03 Dec 2021 05:04:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 05:04:34 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:39e4f823356a9e2dbba530f9d363b4d76beaff75a13bad788d38eebeae67e5b0`  
		Last Modified: Thu, 02 Dec 2021 08:41:08 GMT  
		Size: 49.2 MB (49223045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df66cf961d4016eccee4ce9bc5dc18dcd99e9f9963e66c4980a66e6492a421b2`  
		Last Modified: Thu, 02 Dec 2021 10:03:39 GMT  
		Size: 7.7 MB (7695103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6c547e43b8b6afdfae413ba7a49c1120d0534fff63c4a242ef611d562a678c`  
		Last Modified: Thu, 02 Dec 2021 10:03:39 GMT  
		Size: 9.8 MB (9767269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad6f83cdf6241198d4e908c6f92b100cf9cc4dc5242b4d38550ca7639929981`  
		Last Modified: Fri, 03 Dec 2021 05:05:12 GMT  
		Size: 17.1 MB (17058986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5a73aa06cee308b9f2e886dd606487821f89cfcd4179ad928c98be2967203d`  
		Last Modified: Fri, 03 Dec 2021 05:05:09 GMT  
		Size: 2.9 KB (2877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e603812d6b94f46c6224abdccbdaff25d2713289fbb1bbb6b934db50bf83bf`  
		Last Modified: Fri, 03 Dec 2021 05:05:30 GMT  
		Size: 31.0 MB (30966536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5114bc5c46d3e1283ccbe04ee39854b4247c8371980d2572baa46f5a344582`  
		Last Modified: Fri, 03 Dec 2021 05:05:25 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.19.3-alpine`

```console
$ docker pull telegraf@sha256:9e391c4169ccb91b1001061dae70fac58ab82165f4079e7ec039e9d84a4b5ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.19.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:627ea1f7f074a431873307fdba4c402fd567078bcc892dd9db37c5b26628f8c0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40241320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b97513bb4d721e5e1acbe529575e7db4451fc351934ce3ddee001d8183371b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Nov 2021 07:20:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Sat, 13 Nov 2021 07:20:51 GMT
ENV TELEGRAF_VERSION=1.19.3
# Sat, 13 Nov 2021 07:21:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 13 Nov 2021 07:21:05 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 13 Nov 2021 07:21:05 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Sat, 13 Nov 2021 07:21:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Nov 2021 07:21:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ae06dab0a6b50d3f23d332a8c326fd227bd58abc651b7033038337f97e077f`  
		Last Modified: Sat, 13 Nov 2021 07:21:57 GMT  
		Size: 3.4 MB (3371612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269b03bad908f1f612f0e6e5f1618e234a49ac3fcf23cd4f579ae4e09117ac49`  
		Last Modified: Sat, 13 Nov 2021 07:22:22 GMT  
		Size: 34.0 MB (34046365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63e1ff47e2021e70246af4383776e6845936e12e0337f4540c023f664bbe5bd`  
		Last Modified: Sat, 13 Nov 2021 07:22:14 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.20`

```console
$ docker pull telegraf@sha256:f6ae081705426f48e69db8ecfdd1d7c635584167656997a2dbff834dc20affd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.20` - linux; amd64

```console
$ docker pull telegraf@sha256:0f62fa65be36a4e2f8f111eefd6eaf8c25a6f8341ce7cc709af738d77c63d101
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121320348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cb255a1ae30a1dffa7eb1f466180c8e05a03959c83eaa91dc1dcd43c59bb7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:31 GMT
ADD file:f077e1a42fb919be2af67820782ceee3b46ffd13d7ab6949bea9921217d12813 in / 
# Thu, 02 Dec 2021 02:48:32 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:41:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:41:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Dec 2021 04:32:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 04:32:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 04:32:40 GMT
ENV TELEGRAF_VERSION=1.20.4
# Fri, 03 Dec 2021 04:32:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 03 Dec 2021 04:32:46 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 03 Dec 2021 04:32:46 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 03 Dec 2021 04:32:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 04:32:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c4cc477c22ba7abce860198107408434dd7bd73ddbaf82f1e69ab941b9979405`  
		Last Modified: Thu, 02 Dec 2021 02:54:07 GMT  
		Size: 50.4 MB (50437113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077c54d048f1f1a1f28079caa54bf5d99803f937ffe5c1dc6e207698f70b4e74`  
		Last Modified: Thu, 02 Dec 2021 03:50:46 GMT  
		Size: 7.8 MB (7833819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368544993b2deeeffdd19463cdf92ec4e39f83073de5de316f9f5c725ab403f`  
		Last Modified: Thu, 02 Dec 2021 03:50:46 GMT  
		Size: 10.0 MB (9997240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d19fc3bb1a1152e2be5e863a11ffafd241f042019bc0191614d8552ef25b3fd`  
		Last Modified: Fri, 03 Dec 2021 04:33:13 GMT  
		Size: 17.4 MB (17415385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ada106a1ddfa307bb6f3b252de34b237c4dd398272b5c71c9ae6d8fa1e56abf`  
		Last Modified: Fri, 03 Dec 2021 04:33:10 GMT  
		Size: 2.9 KB (2906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e06a28ac32f4bab638d1a5b479c51e66f381e120475b90158a7b841bb753760`  
		Last Modified: Fri, 03 Dec 2021 04:33:52 GMT  
		Size: 35.6 MB (35633654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac2e943959b3f8077504e390f9aa41fb3f518b5e350f9bd9b9c5b966e9b53a5`  
		Last Modified: Fri, 03 Dec 2021 04:33:46 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.20` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:e4a4ef230593b0769880e26fff66572c65d7a0e7491338df7003cb40ac15cf4c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111646832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8105647936f3c9d10ae2b7e04016e7bb25cfd49f9de8ac2d0826a65e820d4d33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:12 GMT
ADD file:d71807613acdf86685f6d640a90e27b7b63cfe0f13d88668ee943aca089d8876 in / 
# Wed, 17 Nov 2021 02:00:13 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 02:45:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 19 Nov 2021 06:57:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 19 Nov 2021 06:57:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 19 Nov 2021 06:58:28 GMT
ENV TELEGRAF_VERSION=1.20.4
# Fri, 19 Nov 2021 06:58:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 19 Nov 2021 06:58:40 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 19 Nov 2021 06:58:41 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 19 Nov 2021 06:58:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Nov 2021 06:58:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:10acd81022d17f452439d0385615fa066b8f0ddcf3c1a803872eec5bdc6acf64`  
		Last Modified: Wed, 17 Nov 2021 02:16:00 GMT  
		Size: 45.9 MB (45918099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a9604eb6c465f658d6422593d504030155029fe0c4302451d4369030c29144`  
		Last Modified: Wed, 17 Nov 2021 03:07:14 GMT  
		Size: 7.1 MB (7125194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043b954c4f0757e89df96897cea2cf1f93c6275466008e4ba7a4b1089c7dd3d`  
		Last Modified: Wed, 17 Nov 2021 03:07:15 GMT  
		Size: 9.3 MB (9343839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f948c503612d7c3256c810d1947e6739199bedadaa86c607aaf0a20748fd2e28`  
		Last Modified: Fri, 19 Nov 2021 06:59:38 GMT  
		Size: 16.2 MB (16161406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a5c71a30ea8197d13500f671181ef00e946261de58f9df4450d46f71292b94`  
		Last Modified: Fri, 19 Nov 2021 06:59:26 GMT  
		Size: 2.9 KB (2907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6de908f25ea6225c51944cf17448323ed01586e8bd396cd2c6a31833d0b640e`  
		Last Modified: Fri, 19 Nov 2021 07:00:54 GMT  
		Size: 33.1 MB (33095155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9a22e1550f034287182d426f2f591e940c8361d8454a1d210292b6edd4ee36`  
		Last Modified: Fri, 19 Nov 2021 07:00:31 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.20` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2dcae3326239817abaaef855729f6c2efd680750e6365bda41f177c82668bf43
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116117152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dd3855686dc7b618e54c8a05c5c3cc2143e329f8b115c2f78786cb41af9795`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:20 GMT
ADD file:82c1819d8416d9d44564980e25e98a081f813bc2ee8ad2789114fe37e802848f in / 
# Thu, 02 Dec 2021 08:08:20 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:54:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:54:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Dec 2021 05:04:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 05:04:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 05:04:40 GMT
ENV TELEGRAF_VERSION=1.20.4
# Fri, 03 Dec 2021 05:04:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 03 Dec 2021 05:04:45 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 03 Dec 2021 05:04:46 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 03 Dec 2021 05:04:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 05:04:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:39e4f823356a9e2dbba530f9d363b4d76beaff75a13bad788d38eebeae67e5b0`  
		Last Modified: Thu, 02 Dec 2021 08:41:08 GMT  
		Size: 49.2 MB (49223045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df66cf961d4016eccee4ce9bc5dc18dcd99e9f9963e66c4980a66e6492a421b2`  
		Last Modified: Thu, 02 Dec 2021 10:03:39 GMT  
		Size: 7.7 MB (7695103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6c547e43b8b6afdfae413ba7a49c1120d0534fff63c4a242ef611d562a678c`  
		Last Modified: Thu, 02 Dec 2021 10:03:39 GMT  
		Size: 9.8 MB (9767269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad6f83cdf6241198d4e908c6f92b100cf9cc4dc5242b4d38550ca7639929981`  
		Last Modified: Fri, 03 Dec 2021 05:05:12 GMT  
		Size: 17.1 MB (17058986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5a73aa06cee308b9f2e886dd606487821f89cfcd4179ad928c98be2967203d`  
		Last Modified: Fri, 03 Dec 2021 05:05:09 GMT  
		Size: 2.9 KB (2877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a457da2a301b2827e99ea10f9db7e47ac26dbd996e3fa821834baa4101c0b0`  
		Last Modified: Fri, 03 Dec 2021 05:05:47 GMT  
		Size: 32.4 MB (32369641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1549001848a878902d2bd1aa11a741ac52eccef7d8455b81def886c9933fec6`  
		Last Modified: Fri, 03 Dec 2021 05:05:41 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.20-alpine`

```console
$ docker pull telegraf@sha256:ec38849bc5fe65c4f7d176d6d9e8d30b95962bc9a1c01e3dfb59b2696fa13b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.20-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:0484a9bf34a2451e0f136e6774708aa14ad4260c3f50a23fd75382007610db80
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41665045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2594c1dd130583f16f66043a73bf0aa9023c6b1fc72a610bcf384ac22bb271b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Nov 2021 07:20:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Thu, 18 Nov 2021 00:40:52 GMT
ENV TELEGRAF_VERSION=1.20.4
# Thu, 18 Nov 2021 00:41:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Thu, 18 Nov 2021 00:41:01 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 18 Nov 2021 00:41:02 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Thu, 18 Nov 2021 00:41:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Nov 2021 00:41:02 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ae06dab0a6b50d3f23d332a8c326fd227bd58abc651b7033038337f97e077f`  
		Last Modified: Sat, 13 Nov 2021 07:21:57 GMT  
		Size: 3.4 MB (3371612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fbec476f43d42da124ae1c41b556588430df5cca52f8ae134f26f63e42d163`  
		Last Modified: Thu, 18 Nov 2021 00:42:24 GMT  
		Size: 35.5 MB (35470091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accdd69badfcb3fe5f971ffa73e6fd222a08e30312cce915a79e1f3e3419e7da`  
		Last Modified: Thu, 18 Nov 2021 00:42:18 GMT  
		Size: 206.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.20.4`

```console
$ docker pull telegraf@sha256:f6ae081705426f48e69db8ecfdd1d7c635584167656997a2dbff834dc20affd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.20.4` - linux; amd64

```console
$ docker pull telegraf@sha256:0f62fa65be36a4e2f8f111eefd6eaf8c25a6f8341ce7cc709af738d77c63d101
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121320348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cb255a1ae30a1dffa7eb1f466180c8e05a03959c83eaa91dc1dcd43c59bb7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:31 GMT
ADD file:f077e1a42fb919be2af67820782ceee3b46ffd13d7ab6949bea9921217d12813 in / 
# Thu, 02 Dec 2021 02:48:32 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:41:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:41:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Dec 2021 04:32:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 04:32:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 04:32:40 GMT
ENV TELEGRAF_VERSION=1.20.4
# Fri, 03 Dec 2021 04:32:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 03 Dec 2021 04:32:46 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 03 Dec 2021 04:32:46 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 03 Dec 2021 04:32:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 04:32:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c4cc477c22ba7abce860198107408434dd7bd73ddbaf82f1e69ab941b9979405`  
		Last Modified: Thu, 02 Dec 2021 02:54:07 GMT  
		Size: 50.4 MB (50437113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077c54d048f1f1a1f28079caa54bf5d99803f937ffe5c1dc6e207698f70b4e74`  
		Last Modified: Thu, 02 Dec 2021 03:50:46 GMT  
		Size: 7.8 MB (7833819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368544993b2deeeffdd19463cdf92ec4e39f83073de5de316f9f5c725ab403f`  
		Last Modified: Thu, 02 Dec 2021 03:50:46 GMT  
		Size: 10.0 MB (9997240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d19fc3bb1a1152e2be5e863a11ffafd241f042019bc0191614d8552ef25b3fd`  
		Last Modified: Fri, 03 Dec 2021 04:33:13 GMT  
		Size: 17.4 MB (17415385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ada106a1ddfa307bb6f3b252de34b237c4dd398272b5c71c9ae6d8fa1e56abf`  
		Last Modified: Fri, 03 Dec 2021 04:33:10 GMT  
		Size: 2.9 KB (2906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e06a28ac32f4bab638d1a5b479c51e66f381e120475b90158a7b841bb753760`  
		Last Modified: Fri, 03 Dec 2021 04:33:52 GMT  
		Size: 35.6 MB (35633654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac2e943959b3f8077504e390f9aa41fb3f518b5e350f9bd9b9c5b966e9b53a5`  
		Last Modified: Fri, 03 Dec 2021 04:33:46 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.20.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:e4a4ef230593b0769880e26fff66572c65d7a0e7491338df7003cb40ac15cf4c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111646832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8105647936f3c9d10ae2b7e04016e7bb25cfd49f9de8ac2d0826a65e820d4d33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:12 GMT
ADD file:d71807613acdf86685f6d640a90e27b7b63cfe0f13d88668ee943aca089d8876 in / 
# Wed, 17 Nov 2021 02:00:13 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 02:45:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 19 Nov 2021 06:57:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 19 Nov 2021 06:57:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 19 Nov 2021 06:58:28 GMT
ENV TELEGRAF_VERSION=1.20.4
# Fri, 19 Nov 2021 06:58:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 19 Nov 2021 06:58:40 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 19 Nov 2021 06:58:41 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 19 Nov 2021 06:58:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Nov 2021 06:58:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:10acd81022d17f452439d0385615fa066b8f0ddcf3c1a803872eec5bdc6acf64`  
		Last Modified: Wed, 17 Nov 2021 02:16:00 GMT  
		Size: 45.9 MB (45918099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a9604eb6c465f658d6422593d504030155029fe0c4302451d4369030c29144`  
		Last Modified: Wed, 17 Nov 2021 03:07:14 GMT  
		Size: 7.1 MB (7125194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043b954c4f0757e89df96897cea2cf1f93c6275466008e4ba7a4b1089c7dd3d`  
		Last Modified: Wed, 17 Nov 2021 03:07:15 GMT  
		Size: 9.3 MB (9343839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f948c503612d7c3256c810d1947e6739199bedadaa86c607aaf0a20748fd2e28`  
		Last Modified: Fri, 19 Nov 2021 06:59:38 GMT  
		Size: 16.2 MB (16161406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a5c71a30ea8197d13500f671181ef00e946261de58f9df4450d46f71292b94`  
		Last Modified: Fri, 19 Nov 2021 06:59:26 GMT  
		Size: 2.9 KB (2907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6de908f25ea6225c51944cf17448323ed01586e8bd396cd2c6a31833d0b640e`  
		Last Modified: Fri, 19 Nov 2021 07:00:54 GMT  
		Size: 33.1 MB (33095155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9a22e1550f034287182d426f2f591e940c8361d8454a1d210292b6edd4ee36`  
		Last Modified: Fri, 19 Nov 2021 07:00:31 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.20.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2dcae3326239817abaaef855729f6c2efd680750e6365bda41f177c82668bf43
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116117152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dd3855686dc7b618e54c8a05c5c3cc2143e329f8b115c2f78786cb41af9795`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:20 GMT
ADD file:82c1819d8416d9d44564980e25e98a081f813bc2ee8ad2789114fe37e802848f in / 
# Thu, 02 Dec 2021 08:08:20 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:54:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:54:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Dec 2021 05:04:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 05:04:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 05:04:40 GMT
ENV TELEGRAF_VERSION=1.20.4
# Fri, 03 Dec 2021 05:04:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 03 Dec 2021 05:04:45 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 03 Dec 2021 05:04:46 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 03 Dec 2021 05:04:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 05:04:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:39e4f823356a9e2dbba530f9d363b4d76beaff75a13bad788d38eebeae67e5b0`  
		Last Modified: Thu, 02 Dec 2021 08:41:08 GMT  
		Size: 49.2 MB (49223045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df66cf961d4016eccee4ce9bc5dc18dcd99e9f9963e66c4980a66e6492a421b2`  
		Last Modified: Thu, 02 Dec 2021 10:03:39 GMT  
		Size: 7.7 MB (7695103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6c547e43b8b6afdfae413ba7a49c1120d0534fff63c4a242ef611d562a678c`  
		Last Modified: Thu, 02 Dec 2021 10:03:39 GMT  
		Size: 9.8 MB (9767269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad6f83cdf6241198d4e908c6f92b100cf9cc4dc5242b4d38550ca7639929981`  
		Last Modified: Fri, 03 Dec 2021 05:05:12 GMT  
		Size: 17.1 MB (17058986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5a73aa06cee308b9f2e886dd606487821f89cfcd4179ad928c98be2967203d`  
		Last Modified: Fri, 03 Dec 2021 05:05:09 GMT  
		Size: 2.9 KB (2877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a457da2a301b2827e99ea10f9db7e47ac26dbd996e3fa821834baa4101c0b0`  
		Last Modified: Fri, 03 Dec 2021 05:05:47 GMT  
		Size: 32.4 MB (32369641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1549001848a878902d2bd1aa11a741ac52eccef7d8455b81def886c9933fec6`  
		Last Modified: Fri, 03 Dec 2021 05:05:41 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.20.4-alpine`

```console
$ docker pull telegraf@sha256:ec38849bc5fe65c4f7d176d6d9e8d30b95962bc9a1c01e3dfb59b2696fa13b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.20.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:0484a9bf34a2451e0f136e6774708aa14ad4260c3f50a23fd75382007610db80
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41665045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2594c1dd130583f16f66043a73bf0aa9023c6b1fc72a610bcf384ac22bb271b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Nov 2021 07:20:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Thu, 18 Nov 2021 00:40:52 GMT
ENV TELEGRAF_VERSION=1.20.4
# Thu, 18 Nov 2021 00:41:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Thu, 18 Nov 2021 00:41:01 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 18 Nov 2021 00:41:02 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Thu, 18 Nov 2021 00:41:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Nov 2021 00:41:02 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ae06dab0a6b50d3f23d332a8c326fd227bd58abc651b7033038337f97e077f`  
		Last Modified: Sat, 13 Nov 2021 07:21:57 GMT  
		Size: 3.4 MB (3371612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fbec476f43d42da124ae1c41b556588430df5cca52f8ae134f26f63e42d163`  
		Last Modified: Thu, 18 Nov 2021 00:42:24 GMT  
		Size: 35.5 MB (35470091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accdd69badfcb3fe5f971ffa73e6fd222a08e30312cce915a79e1f3e3419e7da`  
		Last Modified: Thu, 18 Nov 2021 00:42:18 GMT  
		Size: 206.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:ec38849bc5fe65c4f7d176d6d9e8d30b95962bc9a1c01e3dfb59b2696fa13b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:0484a9bf34a2451e0f136e6774708aa14ad4260c3f50a23fd75382007610db80
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41665045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2594c1dd130583f16f66043a73bf0aa9023c6b1fc72a610bcf384ac22bb271b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Nov 2021 07:20:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Thu, 18 Nov 2021 00:40:52 GMT
ENV TELEGRAF_VERSION=1.20.4
# Thu, 18 Nov 2021 00:41:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Thu, 18 Nov 2021 00:41:01 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 18 Nov 2021 00:41:02 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Thu, 18 Nov 2021 00:41:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Nov 2021 00:41:02 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ae06dab0a6b50d3f23d332a8c326fd227bd58abc651b7033038337f97e077f`  
		Last Modified: Sat, 13 Nov 2021 07:21:57 GMT  
		Size: 3.4 MB (3371612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fbec476f43d42da124ae1c41b556588430df5cca52f8ae134f26f63e42d163`  
		Last Modified: Thu, 18 Nov 2021 00:42:24 GMT  
		Size: 35.5 MB (35470091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accdd69badfcb3fe5f971ffa73e6fd222a08e30312cce915a79e1f3e3419e7da`  
		Last Modified: Thu, 18 Nov 2021 00:42:18 GMT  
		Size: 206.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:f6ae081705426f48e69db8ecfdd1d7c635584167656997a2dbff834dc20affd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:0f62fa65be36a4e2f8f111eefd6eaf8c25a6f8341ce7cc709af738d77c63d101
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121320348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cb255a1ae30a1dffa7eb1f466180c8e05a03959c83eaa91dc1dcd43c59bb7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:31 GMT
ADD file:f077e1a42fb919be2af67820782ceee3b46ffd13d7ab6949bea9921217d12813 in / 
# Thu, 02 Dec 2021 02:48:32 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:41:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:41:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Dec 2021 04:32:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 04:32:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 04:32:40 GMT
ENV TELEGRAF_VERSION=1.20.4
# Fri, 03 Dec 2021 04:32:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 03 Dec 2021 04:32:46 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 03 Dec 2021 04:32:46 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 03 Dec 2021 04:32:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 04:32:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c4cc477c22ba7abce860198107408434dd7bd73ddbaf82f1e69ab941b9979405`  
		Last Modified: Thu, 02 Dec 2021 02:54:07 GMT  
		Size: 50.4 MB (50437113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077c54d048f1f1a1f28079caa54bf5d99803f937ffe5c1dc6e207698f70b4e74`  
		Last Modified: Thu, 02 Dec 2021 03:50:46 GMT  
		Size: 7.8 MB (7833819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368544993b2deeeffdd19463cdf92ec4e39f83073de5de316f9f5c725ab403f`  
		Last Modified: Thu, 02 Dec 2021 03:50:46 GMT  
		Size: 10.0 MB (9997240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d19fc3bb1a1152e2be5e863a11ffafd241f042019bc0191614d8552ef25b3fd`  
		Last Modified: Fri, 03 Dec 2021 04:33:13 GMT  
		Size: 17.4 MB (17415385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ada106a1ddfa307bb6f3b252de34b237c4dd398272b5c71c9ae6d8fa1e56abf`  
		Last Modified: Fri, 03 Dec 2021 04:33:10 GMT  
		Size: 2.9 KB (2906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e06a28ac32f4bab638d1a5b479c51e66f381e120475b90158a7b841bb753760`  
		Last Modified: Fri, 03 Dec 2021 04:33:52 GMT  
		Size: 35.6 MB (35633654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac2e943959b3f8077504e390f9aa41fb3f518b5e350f9bd9b9c5b966e9b53a5`  
		Last Modified: Fri, 03 Dec 2021 04:33:46 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:e4a4ef230593b0769880e26fff66572c65d7a0e7491338df7003cb40ac15cf4c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111646832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8105647936f3c9d10ae2b7e04016e7bb25cfd49f9de8ac2d0826a65e820d4d33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:12 GMT
ADD file:d71807613acdf86685f6d640a90e27b7b63cfe0f13d88668ee943aca089d8876 in / 
# Wed, 17 Nov 2021 02:00:13 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 02:45:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 19 Nov 2021 06:57:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 19 Nov 2021 06:57:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 19 Nov 2021 06:58:28 GMT
ENV TELEGRAF_VERSION=1.20.4
# Fri, 19 Nov 2021 06:58:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 19 Nov 2021 06:58:40 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 19 Nov 2021 06:58:41 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 19 Nov 2021 06:58:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Nov 2021 06:58:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:10acd81022d17f452439d0385615fa066b8f0ddcf3c1a803872eec5bdc6acf64`  
		Last Modified: Wed, 17 Nov 2021 02:16:00 GMT  
		Size: 45.9 MB (45918099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a9604eb6c465f658d6422593d504030155029fe0c4302451d4369030c29144`  
		Last Modified: Wed, 17 Nov 2021 03:07:14 GMT  
		Size: 7.1 MB (7125194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043b954c4f0757e89df96897cea2cf1f93c6275466008e4ba7a4b1089c7dd3d`  
		Last Modified: Wed, 17 Nov 2021 03:07:15 GMT  
		Size: 9.3 MB (9343839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f948c503612d7c3256c810d1947e6739199bedadaa86c607aaf0a20748fd2e28`  
		Last Modified: Fri, 19 Nov 2021 06:59:38 GMT  
		Size: 16.2 MB (16161406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a5c71a30ea8197d13500f671181ef00e946261de58f9df4450d46f71292b94`  
		Last Modified: Fri, 19 Nov 2021 06:59:26 GMT  
		Size: 2.9 KB (2907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6de908f25ea6225c51944cf17448323ed01586e8bd396cd2c6a31833d0b640e`  
		Last Modified: Fri, 19 Nov 2021 07:00:54 GMT  
		Size: 33.1 MB (33095155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9a22e1550f034287182d426f2f591e940c8361d8454a1d210292b6edd4ee36`  
		Last Modified: Fri, 19 Nov 2021 07:00:31 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2dcae3326239817abaaef855729f6c2efd680750e6365bda41f177c82668bf43
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116117152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dd3855686dc7b618e54c8a05c5c3cc2143e329f8b115c2f78786cb41af9795`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:20 GMT
ADD file:82c1819d8416d9d44564980e25e98a081f813bc2ee8ad2789114fe37e802848f in / 
# Thu, 02 Dec 2021 08:08:20 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:54:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:54:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Dec 2021 05:04:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 05:04:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 05:04:40 GMT
ENV TELEGRAF_VERSION=1.20.4
# Fri, 03 Dec 2021 05:04:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 03 Dec 2021 05:04:45 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 03 Dec 2021 05:04:46 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 03 Dec 2021 05:04:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 05:04:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:39e4f823356a9e2dbba530f9d363b4d76beaff75a13bad788d38eebeae67e5b0`  
		Last Modified: Thu, 02 Dec 2021 08:41:08 GMT  
		Size: 49.2 MB (49223045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df66cf961d4016eccee4ce9bc5dc18dcd99e9f9963e66c4980a66e6492a421b2`  
		Last Modified: Thu, 02 Dec 2021 10:03:39 GMT  
		Size: 7.7 MB (7695103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6c547e43b8b6afdfae413ba7a49c1120d0534fff63c4a242ef611d562a678c`  
		Last Modified: Thu, 02 Dec 2021 10:03:39 GMT  
		Size: 9.8 MB (9767269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad6f83cdf6241198d4e908c6f92b100cf9cc4dc5242b4d38550ca7639929981`  
		Last Modified: Fri, 03 Dec 2021 05:05:12 GMT  
		Size: 17.1 MB (17058986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5a73aa06cee308b9f2e886dd606487821f89cfcd4179ad928c98be2967203d`  
		Last Modified: Fri, 03 Dec 2021 05:05:09 GMT  
		Size: 2.9 KB (2877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a457da2a301b2827e99ea10f9db7e47ac26dbd996e3fa821834baa4101c0b0`  
		Last Modified: Fri, 03 Dec 2021 05:05:47 GMT  
		Size: 32.4 MB (32369641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1549001848a878902d2bd1aa11a741ac52eccef7d8455b81def886c9933fec6`  
		Last Modified: Fri, 03 Dec 2021 05:05:41 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
