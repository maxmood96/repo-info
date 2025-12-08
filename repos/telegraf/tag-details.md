<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.35`](#telegraf135)
-	[`telegraf:1.35-alpine`](#telegraf135-alpine)
-	[`telegraf:1.35.4`](#telegraf1354)
-	[`telegraf:1.35.4-alpine`](#telegraf1354-alpine)
-	[`telegraf:1.36`](#telegraf136)
-	[`telegraf:1.36-alpine`](#telegraf136-alpine)
-	[`telegraf:1.36.4`](#telegraf1364)
-	[`telegraf:1.36.4-alpine`](#telegraf1364-alpine)
-	[`telegraf:1.37`](#telegraf137)
-	[`telegraf:1.37-alpine`](#telegraf137-alpine)
-	[`telegraf:1.37.0`](#telegraf1370)
-	[`telegraf:1.37.0-alpine`](#telegraf1370-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.35`

```console
$ docker pull telegraf@sha256:8d2193e9ffb654e19abf2cfcd7fba1697bef812a775455142aedc1bf2c3844e5
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
$ docker pull telegraf@sha256:50d80d075e876d4029cbeb15dd9400cdcd623a551eb4c0af409ee49e41512568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171027782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269d0176b0dcbe5112803f8fb2cfa4fc1a2779f75c6e98b5491ba845f4beef79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 07:03:26 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 18 Nov 2025 07:03:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 07:03:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 07:03:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 07:03:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5f053ec8926ee0eac7cd01f85cba4936db5cd004807d520797258a293de2f2`  
		Last Modified: Tue, 18 Nov 2025 07:03:58 GMT  
		Size: 18.9 MB (18942918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ff3b5a7e3a3189d28a02bb5802edb06a68bdac6958aeb327cfc4effb36ef3a`  
		Last Modified: Tue, 18 Nov 2025 07:03:53 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0b4568a334886380c1ddbd41e3887ea7712558d19dbb287eea69a5f4365c3d`  
		Last Modified: Tue, 18 Nov 2025 07:04:10 GMT  
		Size: 79.6 MB (79570680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2257ba4d71f440352eb07b501c4a467afa432a68db3be6645e936e89c774c86a`  
		Last Modified: Tue, 18 Nov 2025 07:03:53 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:f04995bce32c7a9e3ce63a62cf9d78782b454d9d4434349a2d7a6125d0234c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6659372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7723b8e0c4f8908d64b757e580e2751a5bb3a752d899dcafcea1bbdca98bf3`

```dockerfile
```

-	Layers:
	-	`sha256:83c52b6bdfc78cd3f0899c7dae78bdce7b69082a8c964b3cfe507aad63bb4e77`  
		Last Modified: Tue, 18 Nov 2025 10:11:48 GMT  
		Size: 6.6 MB (6644946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:076b5f3088b7bf663c9684ffa83eca3bce17623e586c2d25f01ad3c992461a60`  
		Last Modified: Tue, 18 Nov 2025 10:11:49 GMT  
		Size: 14.4 KB (14426 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:085c84f62156cb279c05694ab3fff24b0b96e867bb0bccf168b5df902fca48cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157148107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba8fb66d8290d9df131d773ae56b0501594cf65c3b99ee84da29aabba70f1c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:50:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:50:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 05:50:48 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 18 Nov 2025 05:50:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 05:50:48 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 05:50:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:50:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:50:48 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de283c9f1014e51262a382731c3a4d3224f79d2e1126367dc0e017820fffaf2e`  
		Last Modified: Tue, 18 Nov 2025 05:51:41 GMT  
		Size: 17.7 MB (17722470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485d468a03d1b31f40e39d9a9e76bb739e0d6324bbcd67bf402772634bc52cf6`  
		Last Modified: Tue, 18 Nov 2025 05:51:37 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce9268d0540926055eaad7328348ac9eb9a4654604d3fc39e18a52fba8efa7f`  
		Last Modified: Tue, 18 Nov 2025 05:51:44 GMT  
		Size: 73.3 MB (73290755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3643944f07ce119cabd447b7de7e0d3ae7c66a6037416cc78d81600e7451b4d2`  
		Last Modified: Tue, 18 Nov 2025 05:51:37 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:59d0ea717bd2e426860e10efd2aed8913fcf01fe8d0b187ec5effbb938a1e0a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6654060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031a0d2e2aead9d0e7578dd55e2835c67aff52bf96f18c39b0699d881808f48c`

```dockerfile
```

-	Layers:
	-	`sha256:65cf11ea9b8b0e52ce561982f3da8f2e05588e198dc9c9199314005242d00415`  
		Last Modified: Tue, 18 Nov 2025 07:11:29 GMT  
		Size: 6.6 MB (6639543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cbcf987f70cc3bf95749837eb6ba218afc958afec6d13cc1635b4c9e5354076`  
		Last Modified: Tue, 18 Nov 2025 07:11:30 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d49e01013420e1cbf4604bdc135eae846aeeb4877608b1fc706c9006704abb21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162925404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdaea9b88101ace62d615d5484fe1167abf09e31fc3430aee424eba12b2bf0a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:11:11 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:11:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 06:11:15 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 18 Nov 2025 06:11:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 06:11:15 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 06:11:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:11:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:11:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cb45c5599c9c6c086d5acafe91bc81ccd2c81008c1431729fe3d7c4c2c396a`  
		Last Modified: Tue, 18 Nov 2025 06:11:42 GMT  
		Size: 18.9 MB (18884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e7d413ad7172c971c72728951997295238b5fd79fe9aac465d1ebfa4685864`  
		Last Modified: Tue, 18 Nov 2025 06:11:40 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceaed55b3c4269b53c03d0d9eb44a1794778c3939aabee1a482fad11b1868cfa`  
		Last Modified: Tue, 18 Nov 2025 06:11:44 GMT  
		Size: 72.1 MB (72079330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8ca2b75a13023f96ad260241723dfb32f25d44a5eaa96b4a8a4fa5275b5c5a`  
		Last Modified: Tue, 18 Nov 2025 06:11:40 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:95d17338946d671cc48b3151c4c7c52cb48a25733feac71f0c1521ddb2c5486e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa75bc84ec0235e4602f212226c6727855805215aff014548ea81eedc4b63d76`

```dockerfile
```

-	Layers:
	-	`sha256:2efd56c35f67dcb6dda051c71f4a3686a2219c1783ccb721f783e661655d0dba`  
		Last Modified: Tue, 18 Nov 2025 10:11:58 GMT  
		Size: 6.6 MB (6645622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebdc0095e31df8d53bf59c363739d44995c8058df0ffb8a0386b385f287bf3ca`  
		Last Modified: Tue, 18 Nov 2025 10:11:59 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35-alpine`

```console
$ docker pull telegraf@sha256:07f7dcf2b3827f051657569751cb64d5faff3e5a72a868693ffb9120e8235879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:218877c5f874e303ce9eff463bd641cd6524d5cb4bf594a918719ce7cb049492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85735517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c39d7be492e6591caa8ad4bed3b416b8e1b0012dabf4da111f2a659a79b3111`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccca5a3c76061483f8823e5d77dd23416fdb6c1db125a11118301458c29897c`  
		Last Modified: Mon, 08 Dec 2025 00:08:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2332823178d0061e80a1f95c48765dbaf18df2dd31878bac57f31fc7e9a9feeb`  
		Last Modified: Mon, 08 Dec 2025 00:08:07 GMT  
		Size: 2.6 MB (2563472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251b8f38f4c764d714567e5ca660283254c5c1f76d6a3eb579385593c3db441f`  
		Last Modified: Mon, 08 Dec 2025 01:56:53 GMT  
		Size: 79.4 MB (79368696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2523c7a219f6fba7e1e9fd8f9a81fbc8fb21f84c41aa6b03e5f001f54fa7d4f`  
		Last Modified: Mon, 08 Dec 2025 00:08:07 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d5f21a0772915320f389bebe6d06e7068c9cfb1211b785a9b3f6333c50c294c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1148969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc15951201cadcadb797550a067ab3695eb31ecadbb317a8dbb86766c39fb43f`

```dockerfile
```

-	Layers:
	-	`sha256:f609b510765575f46fd07751df9253b9e0bef412ef4d52e9f96a165469460ed0`  
		Last Modified: Wed, 08 Oct 2025 23:21:28 GMT  
		Size: 1.1 MB (1134008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b8d9f56ca4b6828b99375d962b74da6a704fd9f3bb65cb4e937fc29576512b`  
		Last Modified: Wed, 08 Oct 2025 23:21:27 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2dc98b18a3b682b4d47915f648c59570b29ce00624355c476e03ec8b7437e844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78643760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a73c4abccf0bdf3e9ed8b9eb7c3415a9215de1a7580eefdf2b21df5e598d2ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb651d889db2dee7911408fa57f1d7539c6e6d834e35cef0953d16bae75bf92b`  
		Last Modified: Mon, 08 Dec 2025 11:40:45 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d79a0d11e911af062cf834a3903c2474ae8e732b43633aba958f2e6ad1016b9`  
		Last Modified: Mon, 08 Dec 2025 11:40:46 GMT  
		Size: 2.6 MB (2627489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564facf9ae36962cd5148a9e7a58a23d64ee343b817bdf79fbe0febc06402a3c`  
		Last Modified: Mon, 08 Dec 2025 11:40:48 GMT  
		Size: 71.9 MB (71877304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1f7ca04417cf2ffd90adfbbaee47bb81f8f7ebd0b7537bfd13f76b41d9bf2c`  
		Last Modified: Mon, 08 Dec 2025 11:40:45 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4753dbe48b97e81e45692abc4a4cc8c2bea6375210f9d3db090253c6327d3b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1144706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ef814572f43a3f8c71c902f5ec20cd44a4e27fb3aa10c609a6532bf95e196a`

```dockerfile
```

-	Layers:
	-	`sha256:eb88913d7607490638a82238d8cb692ac25949af926c0aae25a744e853aec341`  
		Last Modified: Wed, 08 Oct 2025 22:09:56 GMT  
		Size: 1.1 MB (1129635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a5c5dcdefea06875f2d3c71b915b1573aa37fde54d0649aa9189ca1bc85d5a`  
		Last Modified: Wed, 08 Oct 2025 22:09:56 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4`

```console
$ docker pull telegraf@sha256:8d2193e9ffb654e19abf2cfcd7fba1697bef812a775455142aedc1bf2c3844e5
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
$ docker pull telegraf@sha256:50d80d075e876d4029cbeb15dd9400cdcd623a551eb4c0af409ee49e41512568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171027782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269d0176b0dcbe5112803f8fb2cfa4fc1a2779f75c6e98b5491ba845f4beef79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 07:03:26 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 18 Nov 2025 07:03:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 07:03:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 07:03:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 07:03:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5f053ec8926ee0eac7cd01f85cba4936db5cd004807d520797258a293de2f2`  
		Last Modified: Tue, 18 Nov 2025 07:03:58 GMT  
		Size: 18.9 MB (18942918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ff3b5a7e3a3189d28a02bb5802edb06a68bdac6958aeb327cfc4effb36ef3a`  
		Last Modified: Tue, 18 Nov 2025 07:03:53 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0b4568a334886380c1ddbd41e3887ea7712558d19dbb287eea69a5f4365c3d`  
		Last Modified: Tue, 18 Nov 2025 07:04:10 GMT  
		Size: 79.6 MB (79570680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2257ba4d71f440352eb07b501c4a467afa432a68db3be6645e936e89c774c86a`  
		Last Modified: Tue, 18 Nov 2025 07:03:53 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:f04995bce32c7a9e3ce63a62cf9d78782b454d9d4434349a2d7a6125d0234c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6659372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7723b8e0c4f8908d64b757e580e2751a5bb3a752d899dcafcea1bbdca98bf3`

```dockerfile
```

-	Layers:
	-	`sha256:83c52b6bdfc78cd3f0899c7dae78bdce7b69082a8c964b3cfe507aad63bb4e77`  
		Last Modified: Tue, 18 Nov 2025 10:11:48 GMT  
		Size: 6.6 MB (6644946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:076b5f3088b7bf663c9684ffa83eca3bce17623e586c2d25f01ad3c992461a60`  
		Last Modified: Tue, 18 Nov 2025 10:11:49 GMT  
		Size: 14.4 KB (14426 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:085c84f62156cb279c05694ab3fff24b0b96e867bb0bccf168b5df902fca48cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157148107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba8fb66d8290d9df131d773ae56b0501594cf65c3b99ee84da29aabba70f1c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:50:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:50:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 05:50:48 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 18 Nov 2025 05:50:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 05:50:48 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 05:50:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:50:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:50:48 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de283c9f1014e51262a382731c3a4d3224f79d2e1126367dc0e017820fffaf2e`  
		Last Modified: Tue, 18 Nov 2025 05:51:41 GMT  
		Size: 17.7 MB (17722470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485d468a03d1b31f40e39d9a9e76bb739e0d6324bbcd67bf402772634bc52cf6`  
		Last Modified: Tue, 18 Nov 2025 05:51:37 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce9268d0540926055eaad7328348ac9eb9a4654604d3fc39e18a52fba8efa7f`  
		Last Modified: Tue, 18 Nov 2025 05:51:44 GMT  
		Size: 73.3 MB (73290755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3643944f07ce119cabd447b7de7e0d3ae7c66a6037416cc78d81600e7451b4d2`  
		Last Modified: Tue, 18 Nov 2025 05:51:37 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:59d0ea717bd2e426860e10efd2aed8913fcf01fe8d0b187ec5effbb938a1e0a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6654060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031a0d2e2aead9d0e7578dd55e2835c67aff52bf96f18c39b0699d881808f48c`

```dockerfile
```

-	Layers:
	-	`sha256:65cf11ea9b8b0e52ce561982f3da8f2e05588e198dc9c9199314005242d00415`  
		Last Modified: Tue, 18 Nov 2025 07:11:29 GMT  
		Size: 6.6 MB (6639543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cbcf987f70cc3bf95749837eb6ba218afc958afec6d13cc1635b4c9e5354076`  
		Last Modified: Tue, 18 Nov 2025 07:11:30 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d49e01013420e1cbf4604bdc135eae846aeeb4877608b1fc706c9006704abb21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162925404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdaea9b88101ace62d615d5484fe1167abf09e31fc3430aee424eba12b2bf0a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:11:11 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:11:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 06:11:15 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 18 Nov 2025 06:11:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 06:11:15 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 06:11:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:11:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:11:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cb45c5599c9c6c086d5acafe91bc81ccd2c81008c1431729fe3d7c4c2c396a`  
		Last Modified: Tue, 18 Nov 2025 06:11:42 GMT  
		Size: 18.9 MB (18884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e7d413ad7172c971c72728951997295238b5fd79fe9aac465d1ebfa4685864`  
		Last Modified: Tue, 18 Nov 2025 06:11:40 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceaed55b3c4269b53c03d0d9eb44a1794778c3939aabee1a482fad11b1868cfa`  
		Last Modified: Tue, 18 Nov 2025 06:11:44 GMT  
		Size: 72.1 MB (72079330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8ca2b75a13023f96ad260241723dfb32f25d44a5eaa96b4a8a4fa5275b5c5a`  
		Last Modified: Tue, 18 Nov 2025 06:11:40 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:95d17338946d671cc48b3151c4c7c52cb48a25733feac71f0c1521ddb2c5486e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa75bc84ec0235e4602f212226c6727855805215aff014548ea81eedc4b63d76`

```dockerfile
```

-	Layers:
	-	`sha256:2efd56c35f67dcb6dda051c71f4a3686a2219c1783ccb721f783e661655d0dba`  
		Last Modified: Tue, 18 Nov 2025 10:11:58 GMT  
		Size: 6.6 MB (6645622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebdc0095e31df8d53bf59c363739d44995c8058df0ffb8a0386b385f287bf3ca`  
		Last Modified: Tue, 18 Nov 2025 10:11:59 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4-alpine`

```console
$ docker pull telegraf@sha256:07f7dcf2b3827f051657569751cb64d5faff3e5a72a868693ffb9120e8235879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:218877c5f874e303ce9eff463bd641cd6524d5cb4bf594a918719ce7cb049492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85735517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c39d7be492e6591caa8ad4bed3b416b8e1b0012dabf4da111f2a659a79b3111`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccca5a3c76061483f8823e5d77dd23416fdb6c1db125a11118301458c29897c`  
		Last Modified: Mon, 08 Dec 2025 00:08:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2332823178d0061e80a1f95c48765dbaf18df2dd31878bac57f31fc7e9a9feeb`  
		Last Modified: Mon, 08 Dec 2025 00:08:07 GMT  
		Size: 2.6 MB (2563472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251b8f38f4c764d714567e5ca660283254c5c1f76d6a3eb579385593c3db441f`  
		Last Modified: Mon, 08 Dec 2025 01:56:53 GMT  
		Size: 79.4 MB (79368696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2523c7a219f6fba7e1e9fd8f9a81fbc8fb21f84c41aa6b03e5f001f54fa7d4f`  
		Last Modified: Mon, 08 Dec 2025 00:08:07 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d5f21a0772915320f389bebe6d06e7068c9cfb1211b785a9b3f6333c50c294c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1148969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc15951201cadcadb797550a067ab3695eb31ecadbb317a8dbb86766c39fb43f`

```dockerfile
```

-	Layers:
	-	`sha256:f609b510765575f46fd07751df9253b9e0bef412ef4d52e9f96a165469460ed0`  
		Last Modified: Wed, 08 Oct 2025 23:21:28 GMT  
		Size: 1.1 MB (1134008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b8d9f56ca4b6828b99375d962b74da6a704fd9f3bb65cb4e937fc29576512b`  
		Last Modified: Wed, 08 Oct 2025 23:21:27 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2dc98b18a3b682b4d47915f648c59570b29ce00624355c476e03ec8b7437e844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78643760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a73c4abccf0bdf3e9ed8b9eb7c3415a9215de1a7580eefdf2b21df5e598d2ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb651d889db2dee7911408fa57f1d7539c6e6d834e35cef0953d16bae75bf92b`  
		Last Modified: Mon, 08 Dec 2025 11:40:45 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d79a0d11e911af062cf834a3903c2474ae8e732b43633aba958f2e6ad1016b9`  
		Last Modified: Mon, 08 Dec 2025 11:40:46 GMT  
		Size: 2.6 MB (2627489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564facf9ae36962cd5148a9e7a58a23d64ee343b817bdf79fbe0febc06402a3c`  
		Last Modified: Mon, 08 Dec 2025 11:40:48 GMT  
		Size: 71.9 MB (71877304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1f7ca04417cf2ffd90adfbbaee47bb81f8f7ebd0b7537bfd13f76b41d9bf2c`  
		Last Modified: Mon, 08 Dec 2025 11:40:45 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4753dbe48b97e81e45692abc4a4cc8c2bea6375210f9d3db090253c6327d3b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1144706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ef814572f43a3f8c71c902f5ec20cd44a4e27fb3aa10c609a6532bf95e196a`

```dockerfile
```

-	Layers:
	-	`sha256:eb88913d7607490638a82238d8cb692ac25949af926c0aae25a744e853aec341`  
		Last Modified: Wed, 08 Oct 2025 22:09:56 GMT  
		Size: 1.1 MB (1129635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a5c5dcdefea06875f2d3c71b915b1573aa37fde54d0649aa9189ca1bc85d5a`  
		Last Modified: Wed, 08 Oct 2025 22:09:56 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36`

```console
$ docker pull telegraf@sha256:5f5a18511b2f75c2773394bdeb70e8df735e788d834280842c72a3afbd2ea033
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
$ docker pull telegraf@sha256:44d0c1e880333cbca36d5b04a4265d9c25439e803c2923a717bded1458e19f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171930379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5307a413c6ef9a168da7c4f02d3f56425b7fd46b5145c996d0031e38265629aa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 07:03:38 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 18 Nov 2025 07:03:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 07:03:38 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 07:03:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 07:03:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:38 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b9d0400de861bd9fd471e8915c53d25ae95fa8c9b6faada96c93bab8b33eed`  
		Last Modified: Tue, 18 Nov 2025 07:04:09 GMT  
		Size: 18.9 MB (18942686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df33929b66e536ddcd331e714db06615e3bf1fe0594621b9374104e65ead7a73`  
		Last Modified: Tue, 18 Nov 2025 07:04:08 GMT  
		Size: 3.4 KB (3439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbc395ec01246ec776b36853ed74cc7d2dd1834ea59a5068252608594b3d9d1`  
		Last Modified: Tue, 18 Nov 2025 07:04:20 GMT  
		Size: 80.5 MB (80473522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8190af7a955eec0bae4f8ce8953bec2ff6a32ec8c7ed0c8b48052e3a76e00f49`  
		Last Modified: Tue, 18 Nov 2025 07:04:08 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:ddcad4cd4a6a685b92715342d7ac637974a093d277294b771f8ee9c8a430b5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6668277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707c51fd65ac0bbfad0eb314e65218461c473227a398cd1889ba5a280fa66d3f`

```dockerfile
```

-	Layers:
	-	`sha256:3b071af06ce227d07aa190f6ba4c86e0fc3c38a6675e09e4eca6c95610757f4a`  
		Last Modified: Tue, 18 Nov 2025 10:12:03 GMT  
		Size: 6.7 MB (6653548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5b21e929a204e5831fffeb8099afef4de813a34f4ce9b4384b56106cdb01f8`  
		Last Modified: Tue, 18 Nov 2025 10:12:04 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:9e27fd79374ef186b5d218b2212ec8dd5a5bf2f35c0e230050ae58d39001d59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157820958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571a4938a7b9caba0eb38582091907a2decabe3a31f8521e304f22cd94c33381`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:51:02 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:51:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 05:51:07 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 18 Nov 2025 05:51:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 05:51:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 05:51:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:51:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:51:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7105ead932b30517c12cb3bb6c17914e08db14c4798aa43c1aabb7010f5b45`  
		Last Modified: Tue, 18 Nov 2025 05:51:34 GMT  
		Size: 17.7 MB (17722488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dad9c2caee4b2dfe72a6a3ee58e157e80aa18ffca53632e15785e1953b9820`  
		Last Modified: Tue, 18 Nov 2025 05:51:32 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1136d33da7add9039d86ae1587988fa40135f4f5f757372d3d2a520807c59c32`  
		Last Modified: Tue, 18 Nov 2025 05:51:38 GMT  
		Size: 74.0 MB (73963585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae494612a17424b8bd1b0160c8fd5b5a1872657894a7818a842ffb572ae117bd`  
		Last Modified: Tue, 18 Nov 2025 05:51:32 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:e821deda4c002d2fd49eea100765b9b6d299c29542e13500d933d740c4a09129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44916c788a82e02df905fbb56a10119301ff779a62445d3ed4b42cbb0856590c`

```dockerfile
```

-	Layers:
	-	`sha256:573ae69a018ad83aa850ca735d385a4afb4fb6d6a759b0dbb4a3274fece4504e`  
		Last Modified: Tue, 18 Nov 2025 07:11:37 GMT  
		Size: 6.6 MB (6648153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5434d141d8bb9751ddda08d6f97f2a72be54fbd6157fce1cc08774b249bf72c`  
		Last Modified: Tue, 18 Nov 2025 07:11:38 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6ebda6a65fc5573ee696a0481c69dea9fc68c5d44366c080c956d5f8d76dac33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162645599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2bc6ef617e6cb4888c328d42a5b672a883bb04a0b45f52c49e4ab141e20b89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:11:16 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:11:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 06:11:20 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 18 Nov 2025 06:11:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 06:11:20 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 06:11:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:11:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:11:21 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8759b8978ec0d34561d784757fa6476dd7b42d741d4ffb7e39e1daee465b081`  
		Last Modified: Tue, 18 Nov 2025 06:11:48 GMT  
		Size: 18.9 MB (18883787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebe79faffe81a3dbc810b07a1ada318d395cd3fcaebe00c730fd4a21d186023`  
		Last Modified: Tue, 18 Nov 2025 06:11:46 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cf27dce91cceef13a63c40febe7e615e985dca81383f71c4fd78b072a624d2`  
		Last Modified: Tue, 18 Nov 2025 06:11:52 GMT  
		Size: 71.8 MB (71800292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fa4e01808b562f04159fa0c2c7b0698fda75af81de83e130cde4c067acf1d6`  
		Last Modified: Tue, 18 Nov 2025 06:11:46 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:77b326c80f4525a0546588711843437362ba80969941a6e7bae25cd2bf8052c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6669087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6375a82c70a4059eea635d4a2cf4735e30ac32695885063af0269ff03b67a7`

```dockerfile
```

-	Layers:
	-	`sha256:649f319c614cbafcd450d7b6dd2b09969455c7794bbd7bae9ef2921e053f5cb0`  
		Last Modified: Tue, 18 Nov 2025 10:12:13 GMT  
		Size: 6.7 MB (6654236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65d6fb8cc8da981ec451c3345291491d558fa3707cb025e7272cd4ac5242892f`  
		Last Modified: Tue, 18 Nov 2025 10:12:14 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36-alpine`

```console
$ docker pull telegraf@sha256:46cabb477e6e31268bad42966facd2d52c22561d3cfc8d4b0c112b5728ba2c19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:48407b552b16c564ccc47bae44b45ab122d4f48a5bd67d75735d24f586e3f124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86642882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0280f08a3c4aeff01bdbeb32bbf32ce8225d3a92ce6199bdfdfabb565fdee4f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 18:59:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:00:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:00:08 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:00:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:00:08 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb344b979ef9e3d6ea2f360ff66a3139d4cfcd9b863983621de8eefe5cd84aa6`  
		Last Modified: Mon, 17 Nov 2025 19:00:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5696b9b7585c20f57f20c3c7c460662abb184e8eab21a8d4cafd61afc3077a9f`  
		Last Modified: Mon, 17 Nov 2025 19:00:32 GMT  
		Size: 2.6 MB (2563494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff853a04372dd9d1360ee371deb684033ada876ca3c1a38e2d67fe3c5f992aba`  
		Last Modified: Mon, 17 Nov 2025 19:12:22 GMT  
		Size: 80.3 MB (80276038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21db64bfe323b246d3e17e70370a071cbe6e04b604f006cafc7c552ae2a84a58`  
		Last Modified: Mon, 17 Nov 2025 19:00:32 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c9db14f5b6e1db85cf120f8325e5c21fb4b6bc3952dec26a4da8e31845827cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d50f7a3066665cbeb8c985217e41c9d2c2f556ea806eb93be6998e153351815`

```dockerfile
```

-	Layers:
	-	`sha256:d104164b2bcc3c30f646afbdfb9f7942e9d74e4e2e583067261c32c2602a9f20`  
		Last Modified: Mon, 17 Nov 2025 19:10:34 GMT  
		Size: 1.1 MB (1142610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4946291a4533c865cd6bb8bff0320c5aa46fefdae9cb144749cee928ced7711d`  
		Last Modified: Mon, 17 Nov 2025 19:10:35 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4d49d49f81612798363550052fd65d73706db1548e68e0f38576322706f00ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78365616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e73a3d881177da588f763fcd0ab17af8d7f22d8dbad194af635b0bae1274cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 19:02:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:02:18 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:02:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:02:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:02:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e686dad26a4c7f703dc366e1e60b14ae44807c190f97f04760640bb32361676`  
		Last Modified: Mon, 17 Nov 2025 19:02:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d3b38a4228f7da2c38dea9114166ad90b746642df4747865aa32a613fe8247`  
		Last Modified: Mon, 17 Nov 2025 19:02:48 GMT  
		Size: 2.6 MB (2627506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bca33979b5e4d10e8626da8ae6b21afab00ccbeef50beaf1bcd0ad868b8ce7`  
		Last Modified: Mon, 17 Nov 2025 19:02:55 GMT  
		Size: 71.6 MB (71599144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bfa9ad7ce4e4f025b9cfab73b412dc8c04760d6c3ace7fa607998ad9813725`  
		Last Modified: Mon, 17 Nov 2025 19:02:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:b73f976d36f57759d14866b99041351f2aeb2a0facca4b270cf46c7645d8b4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1153591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85106f70e2bf1311bea0e40536625bd137213ea7b96647b802c77c659d7b1b43`

```dockerfile
```

-	Layers:
	-	`sha256:0e40d6658c33f56500ab6ae63559dc1c965812fc29e9404fd354af08b46bc679`  
		Last Modified: Mon, 17 Nov 2025 19:10:39 GMT  
		Size: 1.1 MB (1138249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b269496aa7a00647a4b8e38da5384d0924c563e868cab39620498cdc13c489`  
		Last Modified: Mon, 17 Nov 2025 19:10:40 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4`

```console
$ docker pull telegraf@sha256:5f5a18511b2f75c2773394bdeb70e8df735e788d834280842c72a3afbd2ea033
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.4` - linux; amd64

```console
$ docker pull telegraf@sha256:44d0c1e880333cbca36d5b04a4265d9c25439e803c2923a717bded1458e19f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171930379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5307a413c6ef9a168da7c4f02d3f56425b7fd46b5145c996d0031e38265629aa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:03:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 07:03:38 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 18 Nov 2025 07:03:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 07:03:38 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 07:03:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 07:03:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 07:03:38 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b9d0400de861bd9fd471e8915c53d25ae95fa8c9b6faada96c93bab8b33eed`  
		Last Modified: Tue, 18 Nov 2025 07:04:09 GMT  
		Size: 18.9 MB (18942686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df33929b66e536ddcd331e714db06615e3bf1fe0594621b9374104e65ead7a73`  
		Last Modified: Tue, 18 Nov 2025 07:04:08 GMT  
		Size: 3.4 KB (3439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbc395ec01246ec776b36853ed74cc7d2dd1834ea59a5068252608594b3d9d1`  
		Last Modified: Tue, 18 Nov 2025 07:04:20 GMT  
		Size: 80.5 MB (80473522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8190af7a955eec0bae4f8ce8953bec2ff6a32ec8c7ed0c8b48052e3a76e00f49`  
		Last Modified: Tue, 18 Nov 2025 07:04:08 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:ddcad4cd4a6a685b92715342d7ac637974a093d277294b771f8ee9c8a430b5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6668277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707c51fd65ac0bbfad0eb314e65218461c473227a398cd1889ba5a280fa66d3f`

```dockerfile
```

-	Layers:
	-	`sha256:3b071af06ce227d07aa190f6ba4c86e0fc3c38a6675e09e4eca6c95610757f4a`  
		Last Modified: Tue, 18 Nov 2025 10:12:03 GMT  
		Size: 6.7 MB (6653548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5b21e929a204e5831fffeb8099afef4de813a34f4ce9b4384b56106cdb01f8`  
		Last Modified: Tue, 18 Nov 2025 10:12:04 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:9e27fd79374ef186b5d218b2212ec8dd5a5bf2f35c0e230050ae58d39001d59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157820958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571a4938a7b9caba0eb38582091907a2decabe3a31f8521e304f22cd94c33381`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:51:02 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:51:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 05:51:07 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 18 Nov 2025 05:51:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 05:51:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 05:51:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:51:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:51:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7105ead932b30517c12cb3bb6c17914e08db14c4798aa43c1aabb7010f5b45`  
		Last Modified: Tue, 18 Nov 2025 05:51:34 GMT  
		Size: 17.7 MB (17722488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dad9c2caee4b2dfe72a6a3ee58e157e80aa18ffca53632e15785e1953b9820`  
		Last Modified: Tue, 18 Nov 2025 05:51:32 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1136d33da7add9039d86ae1587988fa40135f4f5f757372d3d2a520807c59c32`  
		Last Modified: Tue, 18 Nov 2025 05:51:38 GMT  
		Size: 74.0 MB (73963585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae494612a17424b8bd1b0160c8fd5b5a1872657894a7818a842ffb572ae117bd`  
		Last Modified: Tue, 18 Nov 2025 05:51:32 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:e821deda4c002d2fd49eea100765b9b6d299c29542e13500d933d740c4a09129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44916c788a82e02df905fbb56a10119301ff779a62445d3ed4b42cbb0856590c`

```dockerfile
```

-	Layers:
	-	`sha256:573ae69a018ad83aa850ca735d385a4afb4fb6d6a759b0dbb4a3274fece4504e`  
		Last Modified: Tue, 18 Nov 2025 07:11:37 GMT  
		Size: 6.6 MB (6648153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5434d141d8bb9751ddda08d6f97f2a72be54fbd6157fce1cc08774b249bf72c`  
		Last Modified: Tue, 18 Nov 2025 07:11:38 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6ebda6a65fc5573ee696a0481c69dea9fc68c5d44366c080c956d5f8d76dac33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162645599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2bc6ef617e6cb4888c328d42a5b672a883bb04a0b45f52c49e4ab141e20b89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:11:16 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:11:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 06:11:20 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 18 Nov 2025 06:11:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Nov 2025 06:11:20 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 18 Nov 2025 06:11:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:11:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:11:21 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8759b8978ec0d34561d784757fa6476dd7b42d741d4ffb7e39e1daee465b081`  
		Last Modified: Tue, 18 Nov 2025 06:11:48 GMT  
		Size: 18.9 MB (18883787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebe79faffe81a3dbc810b07a1ada318d395cd3fcaebe00c730fd4a21d186023`  
		Last Modified: Tue, 18 Nov 2025 06:11:46 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cf27dce91cceef13a63c40febe7e615e985dca81383f71c4fd78b072a624d2`  
		Last Modified: Tue, 18 Nov 2025 06:11:52 GMT  
		Size: 71.8 MB (71800292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fa4e01808b562f04159fa0c2c7b0698fda75af81de83e130cde4c067acf1d6`  
		Last Modified: Tue, 18 Nov 2025 06:11:46 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:77b326c80f4525a0546588711843437362ba80969941a6e7bae25cd2bf8052c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6669087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6375a82c70a4059eea635d4a2cf4735e30ac32695885063af0269ff03b67a7`

```dockerfile
```

-	Layers:
	-	`sha256:649f319c614cbafcd450d7b6dd2b09969455c7794bbd7bae9ef2921e053f5cb0`  
		Last Modified: Tue, 18 Nov 2025 10:12:13 GMT  
		Size: 6.7 MB (6654236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65d6fb8cc8da981ec451c3345291491d558fa3707cb025e7272cd4ac5242892f`  
		Last Modified: Tue, 18 Nov 2025 10:12:14 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4-alpine`

```console
$ docker pull telegraf@sha256:46cabb477e6e31268bad42966facd2d52c22561d3cfc8d4b0c112b5728ba2c19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:48407b552b16c564ccc47bae44b45ab122d4f48a5bd67d75735d24f586e3f124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86642882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0280f08a3c4aeff01bdbeb32bbf32ce8225d3a92ce6199bdfdfabb565fdee4f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 18:59:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:00:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:00:08 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:00:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:00:08 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb344b979ef9e3d6ea2f360ff66a3139d4cfcd9b863983621de8eefe5cd84aa6`  
		Last Modified: Mon, 17 Nov 2025 19:00:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5696b9b7585c20f57f20c3c7c460662abb184e8eab21a8d4cafd61afc3077a9f`  
		Last Modified: Mon, 17 Nov 2025 19:00:32 GMT  
		Size: 2.6 MB (2563494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff853a04372dd9d1360ee371deb684033ada876ca3c1a38e2d67fe3c5f992aba`  
		Last Modified: Mon, 17 Nov 2025 19:12:22 GMT  
		Size: 80.3 MB (80276038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21db64bfe323b246d3e17e70370a071cbe6e04b604f006cafc7c552ae2a84a58`  
		Last Modified: Mon, 17 Nov 2025 19:00:32 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c9db14f5b6e1db85cf120f8325e5c21fb4b6bc3952dec26a4da8e31845827cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d50f7a3066665cbeb8c985217e41c9d2c2f556ea806eb93be6998e153351815`

```dockerfile
```

-	Layers:
	-	`sha256:d104164b2bcc3c30f646afbdfb9f7942e9d74e4e2e583067261c32c2602a9f20`  
		Last Modified: Mon, 17 Nov 2025 19:10:34 GMT  
		Size: 1.1 MB (1142610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4946291a4533c865cd6bb8bff0320c5aa46fefdae9cb144749cee928ced7711d`  
		Last Modified: Mon, 17 Nov 2025 19:10:35 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4d49d49f81612798363550052fd65d73706db1548e68e0f38576322706f00ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78365616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e73a3d881177da588f763fcd0ab17af8d7f22d8dbad194af635b0bae1274cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 19:02:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:02:18 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:02:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:02:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:02:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e686dad26a4c7f703dc366e1e60b14ae44807c190f97f04760640bb32361676`  
		Last Modified: Mon, 17 Nov 2025 19:02:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d3b38a4228f7da2c38dea9114166ad90b746642df4747865aa32a613fe8247`  
		Last Modified: Mon, 17 Nov 2025 19:02:48 GMT  
		Size: 2.6 MB (2627506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bca33979b5e4d10e8626da8ae6b21afab00ccbeef50beaf1bcd0ad868b8ce7`  
		Last Modified: Mon, 17 Nov 2025 19:02:55 GMT  
		Size: 71.6 MB (71599144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bfa9ad7ce4e4f025b9cfab73b412dc8c04760d6c3ace7fa607998ad9813725`  
		Last Modified: Mon, 17 Nov 2025 19:02:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:b73f976d36f57759d14866b99041351f2aeb2a0facca4b270cf46c7645d8b4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1153591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85106f70e2bf1311bea0e40536625bd137213ea7b96647b802c77c659d7b1b43`

```dockerfile
```

-	Layers:
	-	`sha256:0e40d6658c33f56500ab6ae63559dc1c965812fc29e9404fd354af08b46bc679`  
		Last Modified: Mon, 17 Nov 2025 19:10:39 GMT  
		Size: 1.1 MB (1138249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b269496aa7a00647a4b8e38da5384d0924c563e868cab39620498cdc13c489`  
		Last Modified: Mon, 17 Nov 2025 19:10:40 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37`

```console
$ docker pull telegraf@sha256:5455056dddebfa85d7bc8fe724278bd1847e856eb610a0fd2cad829f1afb2838
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37` - linux; amd64

```console
$ docker pull telegraf@sha256:14182b461ba97401a23631904ecc8ce7d4a388b1005a95a91dc090d972d83427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172205272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ae40de51ebdb9c5a0de896ad61df0c8a8ff35da610de7bb7d79434e76c9d80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:15:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:15:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 21:16:02 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:16:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Dec 2025 21:16:02 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:16:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:16:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:16:02 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3955c1c7e9186ca7bc0e6b217dc58cb859974a31b211d9ee7c66cb3852c4de40`  
		Last Modified: Mon, 08 Dec 2025 21:16:30 GMT  
		Size: 18.9 MB (18942891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea07bea6c4d7b93f73b8efab6d6919fad6cbcafccdf6914e6e889faa645e2744`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 3.4 KB (3449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691acc2c25c38154f83c6dcb07a9f84167e31889f80361c6b198b94d2d7c201e`  
		Last Modified: Mon, 08 Dec 2025 21:16:38 GMT  
		Size: 80.7 MB (80748200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33376e647ead58704e9fd8ee985b8f803cfd401900f089e25cb87896ba4985bd`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:5622219565f39096961784d31e044c8cc4efe6dba0a4d483fb7e6137617fbbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6679126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30b3a77d69d09cec4c6fcf9d64ee32de7360028ec0371e16c152ad5cd34b5fc`

```dockerfile
```

-	Layers:
	-	`sha256:96f17ec2f1cd92f64ec27f849115c114bfdb6fb6a9673f9c05db99c5ce9f1caa`  
		Last Modified: Mon, 08 Dec 2025 22:10:31 GMT  
		Size: 6.7 MB (6664397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50832b27b515571cc652e8d8b5b018fdc6b72e290a124102005d08833ff64b1b`  
		Last Modified: Mon, 08 Dec 2025 22:10:32 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:c23fbb7392e98dceb10d548d2c667b7e6c78a9d695d5bac0293d60e36de3e513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158440177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb53ab8a14948a52176935ddb53585573f0680f536757440d114e3fff7fc7d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:14:47 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:14:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 21:14:54 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:14:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Dec 2025 21:14:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:14:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:14:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:14:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17a08dfa69d8ea4e22baa8dc6670d74f3393f85a4b481ff079651c1a1212d96`  
		Last Modified: Mon, 08 Dec 2025 21:15:21 GMT  
		Size: 17.7 MB (17722482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889819377807975d7dc9d21289246cc30df973dba3e5abde28b40968a45b6fb2`  
		Last Modified: Mon, 08 Dec 2025 21:15:19 GMT  
		Size: 3.5 KB (3454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4260d0aa9dcde0e457ba2df5abb42f635a157e8603996cfa34d843ea9dbccd83`  
		Last Modified: Mon, 08 Dec 2025 21:15:36 GMT  
		Size: 74.6 MB (74582804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95c55b9f9b296a78c3075c04cef854755a94ab309f3e43951a10ce3019e0440`  
		Last Modified: Mon, 08 Dec 2025 21:15:20 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:0064ac2489bb0a9d84883effe97fb927693f3146382010e1462202bdf1d5759f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8825565d8ad43bb8bfd021103a694b9138178e324adeea9c2ea585fc922e27e`

```dockerfile
```

-	Layers:
	-	`sha256:2851b9a398db71ff6720c8a7f2517dc3cef2aca78b1f2ad266885a972f0b90de`  
		Last Modified: Mon, 08 Dec 2025 22:10:38 GMT  
		Size: 6.7 MB (6659002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00a822f8e172bd707d3b440c51b5b536acc3c22247e132f3fa466f069f4e9c99`  
		Last Modified: Mon, 08 Dec 2025 22:10:39 GMT  
		Size: 14.8 KB (14826 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:11b23df6f74f8b39ffc8c0df9258f4b4d6aebb4e1d6ff3f46b156da0801acb2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162859621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbb8f084f2788441c7235812ffa98d6c92378cf68c50e1ffe6d30d843dde2d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:14:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:14:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 21:14:53 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:14:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Dec 2025 21:14:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:14:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:14:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:14:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e886215090eba2379645b59d5ea77586aec42fe7f5f8191a814687af5b35a83`  
		Last Modified: Mon, 08 Dec 2025 21:15:27 GMT  
		Size: 18.9 MB (18884530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd780df0c406cf70d83e3bee3770d1fef950cbedb50e2eb4e4f52b3b8192524`  
		Last Modified: Mon, 08 Dec 2025 21:15:19 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e79997b3be7f3731b6ea1ec5a68d53816fa82b35a088caca4ce42021c4e7499`  
		Last Modified: Mon, 08 Dec 2025 21:15:28 GMT  
		Size: 72.0 MB (72013557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec078996978b3045acb60aa5d6f4ce8d586c40a69e44c096f2af1d023dfa4e9`  
		Last Modified: Mon, 08 Dec 2025 21:15:19 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:d983eaf8761c6c0c47692f24beb3663531f9edce27b91320263fe2bedda23d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6679936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d149aad78becbc65b063b18d56d9417c3a8b1823d01a8e9538d2bcad42402dd8`

```dockerfile
```

-	Layers:
	-	`sha256:9c63a57edc0ea0221917161838d74d3cde5194efc5166ef3086cc4e666dd2a54`  
		Last Modified: Mon, 08 Dec 2025 22:10:45 GMT  
		Size: 6.7 MB (6665085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13983d5fc1624bdf36b6c803cea632a7ac27e1ef203af03ec652dbbb82bd95b9`  
		Last Modified: Mon, 08 Dec 2025 22:10:46 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37-alpine`

```console
$ docker pull telegraf@sha256:9a4fc91b4abbeda71ed1b20eaf171fe050aa2ad2b21eb14ff703fc855c907c2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c42df5ee945977249706b33cc61cc8078d2413faf02d3f9360e2d79f4cef23a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86908207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad33aa6db544c71a9cb9ed7c3c8f1a9dbddd2a11da136741157e75b24c7e575`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 21:15:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Dec 2025 21:15:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Dec 2025 21:16:01 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:16:01 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Dec 2025 21:16:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:16:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:16:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:16:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a611c78d9bf6367a5ff1c0af825e87a9c688c32c6bd466b0152c8e55057d0ef8`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6c6b437b30b508582494bc3659651fc006e6b317cb913bcfecb0c9cc43f903`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 2.6 MB (2563450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae2bab86b5942106a04676b4bf7c91a0d29d2292a13f02bf6d4f36ddf622483`  
		Last Modified: Mon, 08 Dec 2025 21:16:44 GMT  
		Size: 80.5 MB (80541409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41706228cbe6d20f21947a6628baaf8686a316dde23a1af93d00244f957b3106`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:22ea74f5e3a9e94dc1875a8b87f5cff2f305ab5255ca166688adef8cf7484649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6e2eabd715b17c5f68e5cdc67087023aeba7abc6487fba2e80f4ad65d55876`

```dockerfile
```

-	Layers:
	-	`sha256:6de4f753fda5fa2690b93557578e653e46294dd08d956c09b311ec9ebb6cfd38`  
		Last Modified: Mon, 08 Dec 2025 22:10:36 GMT  
		Size: 1.2 MB (1153459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97258d9d1ffd16f77651af3edcb551aad12dda21350c060371c7ebe7215d0e5b`  
		Last Modified: Mon, 08 Dec 2025 22:10:37 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6af586afcd09465b767fad06b4d75c562f9bf300cf196c9a2c00327d04f850dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78572340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4aff5bfdfec17e65cca78f8663b7051e50a8911fdfca5c4c3446a87f2a59a5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 21:14:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Dec 2025 21:14:24 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Dec 2025 21:14:32 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:14:32 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Dec 2025 21:14:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:14:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:14:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:14:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b37a1a2b9598ec2c2a9163b74e038910a5495a3e5f255f76b1d3e83be45d64f`  
		Last Modified: Mon, 08 Dec 2025 21:14:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582eb84a33ab2260528ae7b8b512ca3a9d38048483a4ce48ba5fcfc4d779a551`  
		Last Modified: Mon, 08 Dec 2025 21:14:53 GMT  
		Size: 2.6 MB (2627517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41c305c71f628d11404eb52f4f468848edb0489ef820a2b9eb32aff5b996015`  
		Last Modified: Mon, 08 Dec 2025 21:15:02 GMT  
		Size: 71.8 MB (71805856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff24d143605b201c9e6d56010a5fb6bd81d9f301639b34dd6ab94ff439f83b6`  
		Last Modified: Mon, 08 Dec 2025 21:14:53 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:230c5af04901994545279302b5df587e34bf258e19ab60e53cb069a9ba652f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22eafb95136ea3bf17561283dc6499af8c5feec12c67e57764c559e5a6597629`

```dockerfile
```

-	Layers:
	-	`sha256:57b8b1fcfb80ab3ba810659ce21ac5f533de482bb3d1da675785fe5db4ef76b8`  
		Last Modified: Mon, 08 Dec 2025 22:10:41 GMT  
		Size: 1.1 MB (1149098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dcc52c65be07218d787c7581acb9d9ce226c1501d5d81dac46405ac0fd75f63`  
		Last Modified: Mon, 08 Dec 2025 22:10:42 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.0`

```console
$ docker pull telegraf@sha256:5455056dddebfa85d7bc8fe724278bd1847e856eb610a0fd2cad829f1afb2838
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37.0` - linux; amd64

```console
$ docker pull telegraf@sha256:14182b461ba97401a23631904ecc8ce7d4a388b1005a95a91dc090d972d83427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172205272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ae40de51ebdb9c5a0de896ad61df0c8a8ff35da610de7bb7d79434e76c9d80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:15:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:15:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 21:16:02 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:16:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Dec 2025 21:16:02 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:16:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:16:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:16:02 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3955c1c7e9186ca7bc0e6b217dc58cb859974a31b211d9ee7c66cb3852c4de40`  
		Last Modified: Mon, 08 Dec 2025 21:16:30 GMT  
		Size: 18.9 MB (18942891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea07bea6c4d7b93f73b8efab6d6919fad6cbcafccdf6914e6e889faa645e2744`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 3.4 KB (3449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691acc2c25c38154f83c6dcb07a9f84167e31889f80361c6b198b94d2d7c201e`  
		Last Modified: Mon, 08 Dec 2025 21:16:38 GMT  
		Size: 80.7 MB (80748200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33376e647ead58704e9fd8ee985b8f803cfd401900f089e25cb87896ba4985bd`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.0` - unknown; unknown

```console
$ docker pull telegraf@sha256:5622219565f39096961784d31e044c8cc4efe6dba0a4d483fb7e6137617fbbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6679126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30b3a77d69d09cec4c6fcf9d64ee32de7360028ec0371e16c152ad5cd34b5fc`

```dockerfile
```

-	Layers:
	-	`sha256:96f17ec2f1cd92f64ec27f849115c114bfdb6fb6a9673f9c05db99c5ce9f1caa`  
		Last Modified: Mon, 08 Dec 2025 22:10:31 GMT  
		Size: 6.7 MB (6664397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50832b27b515571cc652e8d8b5b018fdc6b72e290a124102005d08833ff64b1b`  
		Last Modified: Mon, 08 Dec 2025 22:10:32 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.0` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:c23fbb7392e98dceb10d548d2c667b7e6c78a9d695d5bac0293d60e36de3e513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158440177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb53ab8a14948a52176935ddb53585573f0680f536757440d114e3fff7fc7d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:14:47 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:14:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 21:14:54 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:14:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Dec 2025 21:14:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:14:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:14:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:14:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17a08dfa69d8ea4e22baa8dc6670d74f3393f85a4b481ff079651c1a1212d96`  
		Last Modified: Mon, 08 Dec 2025 21:15:21 GMT  
		Size: 17.7 MB (17722482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889819377807975d7dc9d21289246cc30df973dba3e5abde28b40968a45b6fb2`  
		Last Modified: Mon, 08 Dec 2025 21:15:19 GMT  
		Size: 3.5 KB (3454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4260d0aa9dcde0e457ba2df5abb42f635a157e8603996cfa34d843ea9dbccd83`  
		Last Modified: Mon, 08 Dec 2025 21:15:36 GMT  
		Size: 74.6 MB (74582804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95c55b9f9b296a78c3075c04cef854755a94ab309f3e43951a10ce3019e0440`  
		Last Modified: Mon, 08 Dec 2025 21:15:20 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.0` - unknown; unknown

```console
$ docker pull telegraf@sha256:0064ac2489bb0a9d84883effe97fb927693f3146382010e1462202bdf1d5759f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8825565d8ad43bb8bfd021103a694b9138178e324adeea9c2ea585fc922e27e`

```dockerfile
```

-	Layers:
	-	`sha256:2851b9a398db71ff6720c8a7f2517dc3cef2aca78b1f2ad266885a972f0b90de`  
		Last Modified: Mon, 08 Dec 2025 22:10:38 GMT  
		Size: 6.7 MB (6659002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00a822f8e172bd707d3b440c51b5b536acc3c22247e132f3fa466f069f4e9c99`  
		Last Modified: Mon, 08 Dec 2025 22:10:39 GMT  
		Size: 14.8 KB (14826 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.0` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:11b23df6f74f8b39ffc8c0df9258f4b4d6aebb4e1d6ff3f46b156da0801acb2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162859621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbb8f084f2788441c7235812ffa98d6c92378cf68c50e1ffe6d30d843dde2d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:14:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:14:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 21:14:53 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:14:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Dec 2025 21:14:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:14:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:14:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:14:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e886215090eba2379645b59d5ea77586aec42fe7f5f8191a814687af5b35a83`  
		Last Modified: Mon, 08 Dec 2025 21:15:27 GMT  
		Size: 18.9 MB (18884530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd780df0c406cf70d83e3bee3770d1fef950cbedb50e2eb4e4f52b3b8192524`  
		Last Modified: Mon, 08 Dec 2025 21:15:19 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e79997b3be7f3731b6ea1ec5a68d53816fa82b35a088caca4ce42021c4e7499`  
		Last Modified: Mon, 08 Dec 2025 21:15:28 GMT  
		Size: 72.0 MB (72013557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec078996978b3045acb60aa5d6f4ce8d586c40a69e44c096f2af1d023dfa4e9`  
		Last Modified: Mon, 08 Dec 2025 21:15:19 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.0` - unknown; unknown

```console
$ docker pull telegraf@sha256:d983eaf8761c6c0c47692f24beb3663531f9edce27b91320263fe2bedda23d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6679936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d149aad78becbc65b063b18d56d9417c3a8b1823d01a8e9538d2bcad42402dd8`

```dockerfile
```

-	Layers:
	-	`sha256:9c63a57edc0ea0221917161838d74d3cde5194efc5166ef3086cc4e666dd2a54`  
		Last Modified: Mon, 08 Dec 2025 22:10:45 GMT  
		Size: 6.7 MB (6665085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13983d5fc1624bdf36b6c803cea632a7ac27e1ef203af03ec652dbbb82bd95b9`  
		Last Modified: Mon, 08 Dec 2025 22:10:46 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.0-alpine`

```console
$ docker pull telegraf@sha256:9a4fc91b4abbeda71ed1b20eaf171fe050aa2ad2b21eb14ff703fc855c907c2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37.0-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c42df5ee945977249706b33cc61cc8078d2413faf02d3f9360e2d79f4cef23a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86908207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad33aa6db544c71a9cb9ed7c3c8f1a9dbddd2a11da136741157e75b24c7e575`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 21:15:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Dec 2025 21:15:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Dec 2025 21:16:01 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:16:01 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Dec 2025 21:16:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:16:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:16:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:16:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a611c78d9bf6367a5ff1c0af825e87a9c688c32c6bd466b0152c8e55057d0ef8`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6c6b437b30b508582494bc3659651fc006e6b317cb913bcfecb0c9cc43f903`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 2.6 MB (2563450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae2bab86b5942106a04676b4bf7c91a0d29d2292a13f02bf6d4f36ddf622483`  
		Last Modified: Mon, 08 Dec 2025 21:16:44 GMT  
		Size: 80.5 MB (80541409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41706228cbe6d20f21947a6628baaf8686a316dde23a1af93d00244f957b3106`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.0-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:22ea74f5e3a9e94dc1875a8b87f5cff2f305ab5255ca166688adef8cf7484649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6e2eabd715b17c5f68e5cdc67087023aeba7abc6487fba2e80f4ad65d55876`

```dockerfile
```

-	Layers:
	-	`sha256:6de4f753fda5fa2690b93557578e653e46294dd08d956c09b311ec9ebb6cfd38`  
		Last Modified: Mon, 08 Dec 2025 22:10:36 GMT  
		Size: 1.2 MB (1153459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97258d9d1ffd16f77651af3edcb551aad12dda21350c060371c7ebe7215d0e5b`  
		Last Modified: Mon, 08 Dec 2025 22:10:37 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.0-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6af586afcd09465b767fad06b4d75c562f9bf300cf196c9a2c00327d04f850dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78572340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4aff5bfdfec17e65cca78f8663b7051e50a8911fdfca5c4c3446a87f2a59a5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 21:14:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Dec 2025 21:14:24 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Dec 2025 21:14:32 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:14:32 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Dec 2025 21:14:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:14:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:14:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:14:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b37a1a2b9598ec2c2a9163b74e038910a5495a3e5f255f76b1d3e83be45d64f`  
		Last Modified: Mon, 08 Dec 2025 21:14:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582eb84a33ab2260528ae7b8b512ca3a9d38048483a4ce48ba5fcfc4d779a551`  
		Last Modified: Mon, 08 Dec 2025 21:14:53 GMT  
		Size: 2.6 MB (2627517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41c305c71f628d11404eb52f4f468848edb0489ef820a2b9eb32aff5b996015`  
		Last Modified: Mon, 08 Dec 2025 21:15:02 GMT  
		Size: 71.8 MB (71805856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff24d143605b201c9e6d56010a5fb6bd81d9f301639b34dd6ab94ff439f83b6`  
		Last Modified: Mon, 08 Dec 2025 21:14:53 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.0-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:230c5af04901994545279302b5df587e34bf258e19ab60e53cb069a9ba652f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22eafb95136ea3bf17561283dc6499af8c5feec12c67e57764c559e5a6597629`

```dockerfile
```

-	Layers:
	-	`sha256:57b8b1fcfb80ab3ba810659ce21ac5f533de482bb3d1da675785fe5db4ef76b8`  
		Last Modified: Mon, 08 Dec 2025 22:10:41 GMT  
		Size: 1.1 MB (1149098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dcc52c65be07218d787c7581acb9d9ce226c1501d5d81dac46405ac0fd75f63`  
		Last Modified: Mon, 08 Dec 2025 22:10:42 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:9a4fc91b4abbeda71ed1b20eaf171fe050aa2ad2b21eb14ff703fc855c907c2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c42df5ee945977249706b33cc61cc8078d2413faf02d3f9360e2d79f4cef23a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86908207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad33aa6db544c71a9cb9ed7c3c8f1a9dbddd2a11da136741157e75b24c7e575`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 21:15:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Dec 2025 21:15:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Dec 2025 21:16:01 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:16:01 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Dec 2025 21:16:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:16:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:16:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:16:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a611c78d9bf6367a5ff1c0af825e87a9c688c32c6bd466b0152c8e55057d0ef8`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6c6b437b30b508582494bc3659651fc006e6b317cb913bcfecb0c9cc43f903`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 2.6 MB (2563450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae2bab86b5942106a04676b4bf7c91a0d29d2292a13f02bf6d4f36ddf622483`  
		Last Modified: Mon, 08 Dec 2025 21:16:44 GMT  
		Size: 80.5 MB (80541409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41706228cbe6d20f21947a6628baaf8686a316dde23a1af93d00244f957b3106`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:22ea74f5e3a9e94dc1875a8b87f5cff2f305ab5255ca166688adef8cf7484649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6e2eabd715b17c5f68e5cdc67087023aeba7abc6487fba2e80f4ad65d55876`

```dockerfile
```

-	Layers:
	-	`sha256:6de4f753fda5fa2690b93557578e653e46294dd08d956c09b311ec9ebb6cfd38`  
		Last Modified: Mon, 08 Dec 2025 22:10:36 GMT  
		Size: 1.2 MB (1153459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97258d9d1ffd16f77651af3edcb551aad12dda21350c060371c7ebe7215d0e5b`  
		Last Modified: Mon, 08 Dec 2025 22:10:37 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6af586afcd09465b767fad06b4d75c562f9bf300cf196c9a2c00327d04f850dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78572340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4aff5bfdfec17e65cca78f8663b7051e50a8911fdfca5c4c3446a87f2a59a5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 21:14:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Dec 2025 21:14:24 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Dec 2025 21:14:32 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:14:32 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Dec 2025 21:14:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:14:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:14:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:14:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b37a1a2b9598ec2c2a9163b74e038910a5495a3e5f255f76b1d3e83be45d64f`  
		Last Modified: Mon, 08 Dec 2025 21:14:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582eb84a33ab2260528ae7b8b512ca3a9d38048483a4ce48ba5fcfc4d779a551`  
		Last Modified: Mon, 08 Dec 2025 21:14:53 GMT  
		Size: 2.6 MB (2627517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41c305c71f628d11404eb52f4f468848edb0489ef820a2b9eb32aff5b996015`  
		Last Modified: Mon, 08 Dec 2025 21:15:02 GMT  
		Size: 71.8 MB (71805856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff24d143605b201c9e6d56010a5fb6bd81d9f301639b34dd6ab94ff439f83b6`  
		Last Modified: Mon, 08 Dec 2025 21:14:53 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:230c5af04901994545279302b5df587e34bf258e19ab60e53cb069a9ba652f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22eafb95136ea3bf17561283dc6499af8c5feec12c67e57764c559e5a6597629`

```dockerfile
```

-	Layers:
	-	`sha256:57b8b1fcfb80ab3ba810659ce21ac5f533de482bb3d1da675785fe5db4ef76b8`  
		Last Modified: Mon, 08 Dec 2025 22:10:41 GMT  
		Size: 1.1 MB (1149098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dcc52c65be07218d787c7581acb9d9ce226c1501d5d81dac46405ac0fd75f63`  
		Last Modified: Mon, 08 Dec 2025 22:10:42 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:5455056dddebfa85d7bc8fe724278bd1847e856eb610a0fd2cad829f1afb2838
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
$ docker pull telegraf@sha256:14182b461ba97401a23631904ecc8ce7d4a388b1005a95a91dc090d972d83427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172205272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ae40de51ebdb9c5a0de896ad61df0c8a8ff35da610de7bb7d79434e76c9d80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:15:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:15:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 21:16:02 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:16:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Dec 2025 21:16:02 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:16:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:16:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:16:02 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3955c1c7e9186ca7bc0e6b217dc58cb859974a31b211d9ee7c66cb3852c4de40`  
		Last Modified: Mon, 08 Dec 2025 21:16:30 GMT  
		Size: 18.9 MB (18942891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea07bea6c4d7b93f73b8efab6d6919fad6cbcafccdf6914e6e889faa645e2744`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 3.4 KB (3449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691acc2c25c38154f83c6dcb07a9f84167e31889f80361c6b198b94d2d7c201e`  
		Last Modified: Mon, 08 Dec 2025 21:16:38 GMT  
		Size: 80.7 MB (80748200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33376e647ead58704e9fd8ee985b8f803cfd401900f089e25cb87896ba4985bd`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:5622219565f39096961784d31e044c8cc4efe6dba0a4d483fb7e6137617fbbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6679126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30b3a77d69d09cec4c6fcf9d64ee32de7360028ec0371e16c152ad5cd34b5fc`

```dockerfile
```

-	Layers:
	-	`sha256:96f17ec2f1cd92f64ec27f849115c114bfdb6fb6a9673f9c05db99c5ce9f1caa`  
		Last Modified: Mon, 08 Dec 2025 22:10:31 GMT  
		Size: 6.7 MB (6664397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50832b27b515571cc652e8d8b5b018fdc6b72e290a124102005d08833ff64b1b`  
		Last Modified: Mon, 08 Dec 2025 22:10:32 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:c23fbb7392e98dceb10d548d2c667b7e6c78a9d695d5bac0293d60e36de3e513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158440177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb53ab8a14948a52176935ddb53585573f0680f536757440d114e3fff7fc7d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:14:47 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:14:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 21:14:54 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:14:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Dec 2025 21:14:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:14:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:14:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:14:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17a08dfa69d8ea4e22baa8dc6670d74f3393f85a4b481ff079651c1a1212d96`  
		Last Modified: Mon, 08 Dec 2025 21:15:21 GMT  
		Size: 17.7 MB (17722482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889819377807975d7dc9d21289246cc30df973dba3e5abde28b40968a45b6fb2`  
		Last Modified: Mon, 08 Dec 2025 21:15:19 GMT  
		Size: 3.5 KB (3454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4260d0aa9dcde0e457ba2df5abb42f635a157e8603996cfa34d843ea9dbccd83`  
		Last Modified: Mon, 08 Dec 2025 21:15:36 GMT  
		Size: 74.6 MB (74582804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95c55b9f9b296a78c3075c04cef854755a94ab309f3e43951a10ce3019e0440`  
		Last Modified: Mon, 08 Dec 2025 21:15:20 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:0064ac2489bb0a9d84883effe97fb927693f3146382010e1462202bdf1d5759f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8825565d8ad43bb8bfd021103a694b9138178e324adeea9c2ea585fc922e27e`

```dockerfile
```

-	Layers:
	-	`sha256:2851b9a398db71ff6720c8a7f2517dc3cef2aca78b1f2ad266885a972f0b90de`  
		Last Modified: Mon, 08 Dec 2025 22:10:38 GMT  
		Size: 6.7 MB (6659002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00a822f8e172bd707d3b440c51b5b536acc3c22247e132f3fa466f069f4e9c99`  
		Last Modified: Mon, 08 Dec 2025 22:10:39 GMT  
		Size: 14.8 KB (14826 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:11b23df6f74f8b39ffc8c0df9258f4b4d6aebb4e1d6ff3f46b156da0801acb2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162859621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbb8f084f2788441c7235812ffa98d6c92378cf68c50e1ffe6d30d843dde2d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:14:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:14:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Dec 2025 21:14:53 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:14:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Dec 2025 21:14:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:14:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:14:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:14:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e886215090eba2379645b59d5ea77586aec42fe7f5f8191a814687af5b35a83`  
		Last Modified: Mon, 08 Dec 2025 21:15:27 GMT  
		Size: 18.9 MB (18884530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd780df0c406cf70d83e3bee3770d1fef950cbedb50e2eb4e4f52b3b8192524`  
		Last Modified: Mon, 08 Dec 2025 21:15:19 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e79997b3be7f3731b6ea1ec5a68d53816fa82b35a088caca4ce42021c4e7499`  
		Last Modified: Mon, 08 Dec 2025 21:15:28 GMT  
		Size: 72.0 MB (72013557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec078996978b3045acb60aa5d6f4ce8d586c40a69e44c096f2af1d023dfa4e9`  
		Last Modified: Mon, 08 Dec 2025 21:15:19 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:d983eaf8761c6c0c47692f24beb3663531f9edce27b91320263fe2bedda23d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6679936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d149aad78becbc65b063b18d56d9417c3a8b1823d01a8e9538d2bcad42402dd8`

```dockerfile
```

-	Layers:
	-	`sha256:9c63a57edc0ea0221917161838d74d3cde5194efc5166ef3086cc4e666dd2a54`  
		Last Modified: Mon, 08 Dec 2025 22:10:45 GMT  
		Size: 6.7 MB (6665085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13983d5fc1624bdf36b6c803cea632a7ac27e1ef203af03ec652dbbb82bd95b9`  
		Last Modified: Mon, 08 Dec 2025 22:10:46 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
