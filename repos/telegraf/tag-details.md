<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.33`](#telegraf133)
-	[`telegraf:1.33-alpine`](#telegraf133-alpine)
-	[`telegraf:1.33.3`](#telegraf1333)
-	[`telegraf:1.33.3-alpine`](#telegraf1333-alpine)
-	[`telegraf:1.34`](#telegraf134)
-	[`telegraf:1.34-alpine`](#telegraf134-alpine)
-	[`telegraf:1.34.4`](#telegraf1344)
-	[`telegraf:1.34.4-alpine`](#telegraf1344-alpine)
-	[`telegraf:1.35`](#telegraf135)
-	[`telegraf:1.35-alpine`](#telegraf135-alpine)
-	[`telegraf:1.35.1`](#telegraf1351)
-	[`telegraf:1.35.1-alpine`](#telegraf1351-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.33`

```console
$ docker pull telegraf@sha256:37b9ee7fc200d4dba38d7dfd73c015b5846c10498a7c84fb2f81dfdbbdd3aa50
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
$ docker pull telegraf@sha256:26bc2d77f0ed5a35a421c4679a98a4cd07b286b73a40451666daf3fe03966854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168774126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7f7ef123fa89471db256d369a0ab8742b9373c98f4abc84e724c99952a0d78`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.33.3
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa49f85ce7d96e3ae023554b728000bf96fcaa0f362ca69096b32a363db833b4`  
		Last Modified: Tue, 01 Jul 2025 03:26:38 GMT  
		Size: 18.9 MB (18946683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8388b9c176a70ce61976cadca6c35d3dd32399ff7607a202b5db6a927298aec7`  
		Last Modified: Tue, 01 Jul 2025 03:26:36 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5c9cde91a4e69c06eb035bc13e3c3cf7b1e76a9362961f0069ff7a0a1f0b33`  
		Last Modified: Tue, 01 Jul 2025 03:26:47 GMT  
		Size: 77.3 MB (77310060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df50e2b54983c8e6896815167ad509488027d8814151712e3b892f15b588d1c4`  
		Last Modified: Tue, 01 Jul 2025 03:26:36 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:de7007531c779807c01ac1ac3838dd1dec886b63f3ccba42107008fa656c61e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6631745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea19107bb14c4407477d4fdeff29a81ea74cc4f46be07eef4cd24d2f57e6e026`

```dockerfile
```

-	Layers:
	-	`sha256:54d022b2502af80d5ee72350760ce831e5b17ee6aeaaa3ee692af501b8cb23a7`  
		Last Modified: Tue, 01 Jul 2025 06:10:18 GMT  
		Size: 6.6 MB (6617275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:265fa4c8aec2a0190e360473f3f022eedebaeb302cc204cf8b9652034fddb4d0`  
		Last Modified: Tue, 01 Jul 2025 06:10:19 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:3c742b56d87c672ebce4b4a470f8ffee3dd2b51c5f80ec4ea7d54570aacfc3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154936282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74f991da17c4d150096928412eee2f0cba841910dfb6687137cd8bb573833e4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENV TELEGRAF_VERSION=1.33.3
# Mon, 19 May 2025 18:42:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 19 May 2025 18:42:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 May 2025 18:42:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6449907dadb3e534574a2fbaebc996906a8ec5bbb4a2b536a5bf81fd8b82f603`  
		Last Modified: Wed, 11 Jun 2025 15:11:55 GMT  
		Size: 17.7 MB (17725142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c3e4d696d461ef5c8e795643cada7a24e540bd4fdb43157a6c36d759d3fd3c`  
		Last Modified: Wed, 11 Jun 2025 15:16:19 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d25512b818d59b8d7ba2866ce11d7f0a883f9b77a0888cd47e5ad9541436a7`  
		Last Modified: Wed, 11 Jun 2025 15:12:55 GMT  
		Size: 71.1 MB (71075883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1040e0469192003ad90b6b7aa5503182b0d082519648fddc6c701b47cc0299f8`  
		Last Modified: Wed, 11 Jun 2025 15:12:40 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:08c9ac1dd78abedbebbd8e0f272e91f3e7623f670de46e02a57f7a8fefadba4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6625879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593e38febe4e9f87749e92229b876b0ec315e363912e4ab46a2b36ed35e30065`

```dockerfile
```

-	Layers:
	-	`sha256:06abd92659b28020cfa09b385bc7c18353f04424c9ceca65824ca0deb4975315`  
		Last Modified: Wed, 11 Jun 2025 18:10:32 GMT  
		Size: 6.6 MB (6611323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b51bbd3bb6dabb620dbc81def3d58561d85f1dc488191140045e94d704c6ee6`  
		Last Modified: Wed, 11 Jun 2025 18:10:33 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:70e56ad4d4fef71193c864b8e9c13d81df0a489398f3f26cfa0ccad45435d23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160364466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a549cc27b351f7eb624ae07dd22c4a773250ed2337fb071e94805f7287336763`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENV TELEGRAF_VERSION=1.33.3
# Mon, 19 May 2025 18:42:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 19 May 2025 18:42:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 May 2025 18:42:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9272eaa397ad42bf538f779ac47a75a0363f21b2774ded24e4b752d3a03e881`  
		Last Modified: Wed, 11 Jun 2025 13:17:08 GMT  
		Size: 18.9 MB (18871981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccb41b0f7395aa22520b1994b648327f4c2304d74d5be89decbe523899b0d37`  
		Last Modified: Wed, 11 Jun 2025 13:17:08 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7305d4da183f6c3024cc7cc5dae3ae46822cb305da53dc4be1a150b89d9ffa`  
		Last Modified: Wed, 11 Jun 2025 12:37:25 GMT  
		Size: 69.6 MB (69599670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ac083f7ba053bafd75b3f278e9b7148a395de31dbc8bae6f116c6971a0f85b`  
		Last Modified: Wed, 11 Jun 2025 12:37:13 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:bb40c491e6818072878e3a21f4c650526921db2388c560eb49fa10ed89fcded7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6631175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b46f64c71af0e79988785cf63ed8f277bd4322500897c5cd188780ab7a0091e`

```dockerfile
```

-	Layers:
	-	`sha256:0a9864674f487b75713802df1bfe395efdfaa19e67d6cf8b0f894ea7d7054844`  
		Last Modified: Wed, 11 Jun 2025 15:10:34 GMT  
		Size: 6.6 MB (6616595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:200e089989a59bdcfc6b6c3bad03d01e4a7d5b152c89efc8b9e84e25687cb397`  
		Last Modified: Wed, 11 Jun 2025 15:10:35 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33-alpine`

```console
$ docker pull telegraf@sha256:bc804829ecc8a436fe7852c14d8e8189f7cbe84a9971410504ad0298ac395c25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:307dff9d25edf62e990b02f7427799852b411acf9defbe0a746da41334fc2280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a2f2610a65d4727686a80d149dec5e8eabc84964f8672c121ae59bf5129b0f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Tue, 25 Feb 2025 19:20:46 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 25 Feb 2025 19:20:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2025 19:20:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38049afbf35aebc48750aa922431b39f2fc798c04bdbe76bd6ae3b281fed2ba5`  
		Last Modified: Thu, 08 May 2025 19:55:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073bd82841c579643840dc44375728fdc6290a0b75a5c7c7a9f475e2fd33df5c`  
		Last Modified: Thu, 08 May 2025 19:55:07 GMT  
		Size: 2.4 MB (2448010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804d0c3c2f1304b11b15aa3615c2ae951b7aa267345cd8caebf2534c09f432c4`  
		Last Modified: Thu, 08 May 2025 19:55:11 GMT  
		Size: 77.1 MB (77105828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecb0ae4356bd231d8a07dbc4b04fad1e156e8bcf1f303290303cee493817e28`  
		Last Modified: Thu, 08 May 2025 19:55:07 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c7da2eb2660beb59ed82ea1425fe6e4bb730c61f69a7197c2ed08ebc3cdc021d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1110039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028284213fd46027a1ced219a906753338d9c763850718d8f063be618ea2b50f`

```dockerfile
```

-	Layers:
	-	`sha256:f43b03bb1a8042cca6df1e56fbc4d2705ce1afa316953c6a42fa05d0dd301ff3`  
		Last Modified: Thu, 12 Jun 2025 00:45:00 GMT  
		Size: 1.1 MB (1094776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b15e5bf904084afce0335a323cb7a49eb0e277254fb8c1ce8618e0518df0650`  
		Last Modified: Thu, 12 Jun 2025 00:45:01 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a43e4a027c5584945633041b846be6f9fcf9a440ba9dc357ce3b5ce86c7dd4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76021133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8591b770895f10d03fe40dc2f2b0cd25b81c7f2ead94a86a0521e60712ee2ed6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Tue, 25 Feb 2025 19:20:46 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 25 Feb 2025 19:20:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2025 19:20:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61a5f488a07a5f9b377e1e8af47680d864b0a298fd6acfe930441fecb3ecf84`  
		Last Modified: Sat, 15 Feb 2025 03:20:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a777ce7d187cf232aae59fd07445827d4a146c69dd2ff0adb80ede2329896`  
		Last Modified: Sat, 15 Feb 2025 10:11:16 GMT  
		Size: 2.5 MB (2533889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb755c12ce2b641e186784c9d65629a9e336edd2adbfc1769a50ca60cc9d39c7`  
		Last Modified: Fri, 09 May 2025 09:47:20 GMT  
		Size: 69.4 MB (69395470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cb2567b59e86792e2fb28a415d81a683488ae3254f26baf29d93ab79827052`  
		Last Modified: Fri, 09 May 2025 09:47:16 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8859417a657434c92362fd7628b01aa683b21e0131e15a12d1b8db1e6adc949b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1105800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2279b435bd3fccc85c118d273f224fa5d354af37b7f133bebe2b97de2e263235`

```dockerfile
```

-	Layers:
	-	`sha256:75cfdceac3bea7f46c668c49082e6a34da449c79fac4278cdb6a9095936d12b0`  
		Last Modified: Fri, 20 Jun 2025 11:37:43 GMT  
		Size: 1.1 MB (1090415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5040171f06da0c2a54629d1c7e68fd289af078d85e7686d7a27924345d07e654`  
		Last Modified: Fri, 20 Jun 2025 11:37:44 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33.3`

```console
$ docker pull telegraf@sha256:37b9ee7fc200d4dba38d7dfd73c015b5846c10498a7c84fb2f81dfdbbdd3aa50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33.3` - linux; amd64

```console
$ docker pull telegraf@sha256:26bc2d77f0ed5a35a421c4679a98a4cd07b286b73a40451666daf3fe03966854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168774126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7f7ef123fa89471db256d369a0ab8742b9373c98f4abc84e724c99952a0d78`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.33.3
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa49f85ce7d96e3ae023554b728000bf96fcaa0f362ca69096b32a363db833b4`  
		Last Modified: Tue, 01 Jul 2025 03:26:38 GMT  
		Size: 18.9 MB (18946683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8388b9c176a70ce61976cadca6c35d3dd32399ff7607a202b5db6a927298aec7`  
		Last Modified: Tue, 01 Jul 2025 03:26:36 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5c9cde91a4e69c06eb035bc13e3c3cf7b1e76a9362961f0069ff7a0a1f0b33`  
		Last Modified: Tue, 01 Jul 2025 03:26:47 GMT  
		Size: 77.3 MB (77310060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df50e2b54983c8e6896815167ad509488027d8814151712e3b892f15b588d1c4`  
		Last Modified: Tue, 01 Jul 2025 03:26:36 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:de7007531c779807c01ac1ac3838dd1dec886b63f3ccba42107008fa656c61e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6631745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea19107bb14c4407477d4fdeff29a81ea74cc4f46be07eef4cd24d2f57e6e026`

```dockerfile
```

-	Layers:
	-	`sha256:54d022b2502af80d5ee72350760ce831e5b17ee6aeaaa3ee692af501b8cb23a7`  
		Last Modified: Tue, 01 Jul 2025 06:10:18 GMT  
		Size: 6.6 MB (6617275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:265fa4c8aec2a0190e360473f3f022eedebaeb302cc204cf8b9652034fddb4d0`  
		Last Modified: Tue, 01 Jul 2025 06:10:19 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:3c742b56d87c672ebce4b4a470f8ffee3dd2b51c5f80ec4ea7d54570aacfc3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154936282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74f991da17c4d150096928412eee2f0cba841910dfb6687137cd8bb573833e4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENV TELEGRAF_VERSION=1.33.3
# Mon, 19 May 2025 18:42:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 19 May 2025 18:42:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 May 2025 18:42:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6449907dadb3e534574a2fbaebc996906a8ec5bbb4a2b536a5bf81fd8b82f603`  
		Last Modified: Wed, 11 Jun 2025 15:11:55 GMT  
		Size: 17.7 MB (17725142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c3e4d696d461ef5c8e795643cada7a24e540bd4fdb43157a6c36d759d3fd3c`  
		Last Modified: Wed, 11 Jun 2025 15:16:19 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d25512b818d59b8d7ba2866ce11d7f0a883f9b77a0888cd47e5ad9541436a7`  
		Last Modified: Wed, 11 Jun 2025 15:12:55 GMT  
		Size: 71.1 MB (71075883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1040e0469192003ad90b6b7aa5503182b0d082519648fddc6c701b47cc0299f8`  
		Last Modified: Wed, 11 Jun 2025 15:12:40 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:08c9ac1dd78abedbebbd8e0f272e91f3e7623f670de46e02a57f7a8fefadba4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6625879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593e38febe4e9f87749e92229b876b0ec315e363912e4ab46a2b36ed35e30065`

```dockerfile
```

-	Layers:
	-	`sha256:06abd92659b28020cfa09b385bc7c18353f04424c9ceca65824ca0deb4975315`  
		Last Modified: Wed, 11 Jun 2025 18:10:32 GMT  
		Size: 6.6 MB (6611323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b51bbd3bb6dabb620dbc81def3d58561d85f1dc488191140045e94d704c6ee6`  
		Last Modified: Wed, 11 Jun 2025 18:10:33 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:70e56ad4d4fef71193c864b8e9c13d81df0a489398f3f26cfa0ccad45435d23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160364466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a549cc27b351f7eb624ae07dd22c4a773250ed2337fb071e94805f7287336763`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENV TELEGRAF_VERSION=1.33.3
# Mon, 19 May 2025 18:42:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 19 May 2025 18:42:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 May 2025 18:42:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9272eaa397ad42bf538f779ac47a75a0363f21b2774ded24e4b752d3a03e881`  
		Last Modified: Wed, 11 Jun 2025 13:17:08 GMT  
		Size: 18.9 MB (18871981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccb41b0f7395aa22520b1994b648327f4c2304d74d5be89decbe523899b0d37`  
		Last Modified: Wed, 11 Jun 2025 13:17:08 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7305d4da183f6c3024cc7cc5dae3ae46822cb305da53dc4be1a150b89d9ffa`  
		Last Modified: Wed, 11 Jun 2025 12:37:25 GMT  
		Size: 69.6 MB (69599670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ac083f7ba053bafd75b3f278e9b7148a395de31dbc8bae6f116c6971a0f85b`  
		Last Modified: Wed, 11 Jun 2025 12:37:13 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:bb40c491e6818072878e3a21f4c650526921db2388c560eb49fa10ed89fcded7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6631175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b46f64c71af0e79988785cf63ed8f277bd4322500897c5cd188780ab7a0091e`

```dockerfile
```

-	Layers:
	-	`sha256:0a9864674f487b75713802df1bfe395efdfaa19e67d6cf8b0f894ea7d7054844`  
		Last Modified: Wed, 11 Jun 2025 15:10:34 GMT  
		Size: 6.6 MB (6616595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:200e089989a59bdcfc6b6c3bad03d01e4a7d5b152c89efc8b9e84e25687cb397`  
		Last Modified: Wed, 11 Jun 2025 15:10:35 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33.3-alpine`

```console
$ docker pull telegraf@sha256:bc804829ecc8a436fe7852c14d8e8189f7cbe84a9971410504ad0298ac395c25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:307dff9d25edf62e990b02f7427799852b411acf9defbe0a746da41334fc2280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a2f2610a65d4727686a80d149dec5e8eabc84964f8672c121ae59bf5129b0f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Tue, 25 Feb 2025 19:20:46 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 25 Feb 2025 19:20:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2025 19:20:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38049afbf35aebc48750aa922431b39f2fc798c04bdbe76bd6ae3b281fed2ba5`  
		Last Modified: Thu, 08 May 2025 19:55:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073bd82841c579643840dc44375728fdc6290a0b75a5c7c7a9f475e2fd33df5c`  
		Last Modified: Thu, 08 May 2025 19:55:07 GMT  
		Size: 2.4 MB (2448010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804d0c3c2f1304b11b15aa3615c2ae951b7aa267345cd8caebf2534c09f432c4`  
		Last Modified: Thu, 08 May 2025 19:55:11 GMT  
		Size: 77.1 MB (77105828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecb0ae4356bd231d8a07dbc4b04fad1e156e8bcf1f303290303cee493817e28`  
		Last Modified: Thu, 08 May 2025 19:55:07 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c7da2eb2660beb59ed82ea1425fe6e4bb730c61f69a7197c2ed08ebc3cdc021d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1110039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028284213fd46027a1ced219a906753338d9c763850718d8f063be618ea2b50f`

```dockerfile
```

-	Layers:
	-	`sha256:f43b03bb1a8042cca6df1e56fbc4d2705ce1afa316953c6a42fa05d0dd301ff3`  
		Last Modified: Thu, 12 Jun 2025 00:45:00 GMT  
		Size: 1.1 MB (1094776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b15e5bf904084afce0335a323cb7a49eb0e277254fb8c1ce8618e0518df0650`  
		Last Modified: Thu, 12 Jun 2025 00:45:01 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a43e4a027c5584945633041b846be6f9fcf9a440ba9dc357ce3b5ce86c7dd4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76021133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8591b770895f10d03fe40dc2f2b0cd25b81c7f2ead94a86a0521e60712ee2ed6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Tue, 25 Feb 2025 19:20:46 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 25 Feb 2025 19:20:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2025 19:20:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61a5f488a07a5f9b377e1e8af47680d864b0a298fd6acfe930441fecb3ecf84`  
		Last Modified: Sat, 15 Feb 2025 03:20:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a777ce7d187cf232aae59fd07445827d4a146c69dd2ff0adb80ede2329896`  
		Last Modified: Sat, 15 Feb 2025 10:11:16 GMT  
		Size: 2.5 MB (2533889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb755c12ce2b641e186784c9d65629a9e336edd2adbfc1769a50ca60cc9d39c7`  
		Last Modified: Fri, 09 May 2025 09:47:20 GMT  
		Size: 69.4 MB (69395470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cb2567b59e86792e2fb28a415d81a683488ae3254f26baf29d93ab79827052`  
		Last Modified: Fri, 09 May 2025 09:47:16 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8859417a657434c92362fd7628b01aa683b21e0131e15a12d1b8db1e6adc949b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1105800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2279b435bd3fccc85c118d273f224fa5d354af37b7f133bebe2b97de2e263235`

```dockerfile
```

-	Layers:
	-	`sha256:75cfdceac3bea7f46c668c49082e6a34da449c79fac4278cdb6a9095936d12b0`  
		Last Modified: Fri, 20 Jun 2025 11:37:43 GMT  
		Size: 1.1 MB (1090415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5040171f06da0c2a54629d1c7e68fd289af078d85e7686d7a27924345d07e654`  
		Last Modified: Fri, 20 Jun 2025 11:37:44 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34`

```console
$ docker pull telegraf@sha256:9a01311eebad9720791ce968d3fa09c45f0c59dbb1f4a51e9bc9584be251fa0b
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
$ docker pull telegraf@sha256:b289ce50bd342db98198d5d69fff811f572a60afc298236b6ef519f225f46957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168910150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb24cda65638a71b5b18742e6e8c1113d75769b0660cb8db2d31acb5e9c8dfdc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c519c8dc0dae14ac0088efeb396c71954b827de10c5ca28d3d81ea4e688f193`  
		Last Modified: Tue, 01 Jul 2025 03:26:38 GMT  
		Size: 18.9 MB (18946679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae95b6f9c0a60cff96bbf3ab8070eb12f2aa41a80526aef3fc5ab6f2a26a73`  
		Last Modified: Tue, 01 Jul 2025 03:26:37 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc12a7f7e5ff648931583e2992f8c5d083136e89a91416cea614d684999bcfb`  
		Last Modified: Tue, 01 Jul 2025 03:26:46 GMT  
		Size: 77.4 MB (77446090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f35801655e1016773672ec32ecce5256761d2e7741c3d8006d31498f7fc728`  
		Last Modified: Tue, 01 Jul 2025 03:26:37 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:590a2e3d2ced54578ee0c47ae29249ea7ab0fc3160c806bb8e3203a912ee8a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6637917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a41c8d2d66fdcf95cc07041497d56f70b465681aeaa6fbe0b8dd11681e118e`

```dockerfile
```

-	Layers:
	-	`sha256:cd9595d93751dcf604506929bdc4761bec2e40b8583a8c930f46e3185e4d5fc3`  
		Last Modified: Tue, 01 Jul 2025 06:10:27 GMT  
		Size: 6.6 MB (6623447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fca6943adb03f60ab21e0d0eee60d13f1d89184ae3ee74a7601cb026b87be2b9`  
		Last Modified: Tue, 01 Jul 2025 06:10:28 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:45a545ff4f6d0db7989a64f567ac0bfae4b1d3ad11f411b7ce643a0f3fa3c16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155387450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70560a278fe67b2f30daf455b8dc48ccd1e3b7498d8f440e540896c3f21e355c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 19 May 2025 18:42:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 19 May 2025 18:42:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 May 2025 18:42:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6449907dadb3e534574a2fbaebc996906a8ec5bbb4a2b536a5bf81fd8b82f603`  
		Last Modified: Wed, 11 Jun 2025 15:11:55 GMT  
		Size: 17.7 MB (17725142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c3e4d696d461ef5c8e795643cada7a24e540bd4fdb43157a6c36d759d3fd3c`  
		Last Modified: Wed, 11 Jun 2025 15:16:19 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbeab7d12ce9af659e4c6c8bcf27f5a095d49ec6ea905d27bc9bc70b67188ff`  
		Last Modified: Wed, 11 Jun 2025 15:13:49 GMT  
		Size: 71.5 MB (71527051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75afb621067d3aca1fb3068d9c0faca23b02a460f8ce95b4626e00bc1ce3851`  
		Last Modified: Wed, 11 Jun 2025 15:13:42 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:76533e7f474714a10368c3dc1e583acc804f54eeaa8aaf89c49460944a8823ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6631862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897a304a0208b547c19dbdfee6f3223502d60248a364361898b2f510a726d930`

```dockerfile
```

-	Layers:
	-	`sha256:9d4ac8ab7f1732a34cdc9e52a2f2ad9a9264198e7b74b317b1b53b4dc69f75b2`  
		Last Modified: Wed, 11 Jun 2025 18:10:37 GMT  
		Size: 6.6 MB (6616996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2673c739a5f7ed41061943161355314134adf0e74fccca9d131ef11bd7d34a96`  
		Last Modified: Wed, 11 Jun 2025 18:10:37 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3a1f60e51ea97c496f5ea0c422bbf0ea9488196eb3b2cd891438dab7406c4262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160965879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab90a828e1f1ee9dc0996d31486e861ef885129a6e638b08cbf953abd4c67509`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 19 May 2025 18:42:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 19 May 2025 18:42:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 May 2025 18:42:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9272eaa397ad42bf538f779ac47a75a0363f21b2774ded24e4b752d3a03e881`  
		Last Modified: Wed, 11 Jun 2025 13:17:08 GMT  
		Size: 18.9 MB (18871981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccb41b0f7395aa22520b1994b648327f4c2304d74d5be89decbe523899b0d37`  
		Last Modified: Wed, 11 Jun 2025 13:17:08 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71173eb69366a18934cb3088146a58f342006f927eb37ce7fba709252097f37a`  
		Last Modified: Wed, 11 Jun 2025 12:38:00 GMT  
		Size: 70.2 MB (70201085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d285f40ad4fc9c546f4493177288b453d263bc20c74f73a8db5b133ebea8cf8`  
		Last Modified: Wed, 11 Jun 2025 12:37:49 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:afdd727513593d03843c3b0ac81aac39fa8de875c45d4bafc54a8f83e0134ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6637975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611c479730fe5c6729c335881927d24ec76c6763bda0e9e1903f6e2c8dbb3435`

```dockerfile
```

-	Layers:
	-	`sha256:cd4eb9f0e39784767a8a995114016e1104b89fa9bd859f260751e6bf608b967d`  
		Last Modified: Wed, 11 Jun 2025 15:10:40 GMT  
		Size: 6.6 MB (6623081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e3c09ab286a564ec4e97994fe5af62a4ad98164d1541b378e5afdbab64cd43`  
		Last Modified: Wed, 11 Jun 2025 15:10:41 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34-alpine`

```console
$ docker pull telegraf@sha256:a18f6f4cd256131c9e3a0d22e4304421cc00992be16006a5a75feceee2af46de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:740b2f1b261acc9297fe0fad68322986532e7d9bdb59efa024c326b0c38478e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83313296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15721c8d81b3cd80a5f811e26c92fa62fb87187ac61a35cf76873182df727264`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 18:42:44 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 18:42:44 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 19 May 2025 18:42:44 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 19 May 2025 18:42:44 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 19 May 2025 18:42:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 May 2025 18:42:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f57d20f08c7b0bb65b5c15fd14d45946ee7d539fcb8ae5359f25a0c3d3dbbb2`  
		Last Modified: Mon, 19 May 2025 23:23:46 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49332a9ec0e4b728abc3baa00c33325c8e4317934105b9b29856ef462d67997e`  
		Last Modified: Mon, 19 May 2025 23:23:48 GMT  
		Size: 2.4 MB (2449565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942c6f48c3f6d0c87a2466b4cae308941b96a2471a83c1acc8efd9eb66e16be5`  
		Last Modified: Mon, 19 May 2025 23:24:16 GMT  
		Size: 77.2 MB (77236229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36fbb2315acfc4c17771e64880965d7ac100ba7672c86442dd8506dbc582e3b`  
		Last Modified: Mon, 19 May 2025 23:23:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9fd553c4e7501ca191957f61e73914e12f00188bc0a68b0d939c887b279132ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1120283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c698c74b911b99cb88e7165329c616f4eddba4e174592a5b3feea0a43f495237`

```dockerfile
```

-	Layers:
	-	`sha256:688b30db849dc63e5498ae60f5a848aef1b2ac6b3a8fab1188c5606a8961dcd2`  
		Last Modified: Tue, 20 May 2025 00:10:39 GMT  
		Size: 1.1 MB (1105020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07f9bd1a56b1c7d53eb673689b4807defee430946ba107ccce59198fc99366d0`  
		Last Modified: Tue, 20 May 2025 00:10:39 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2484dc4338c0457edc8113483b73c4ce24495ae42218965d2c8a8bf5b3a393a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76624559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8402837ffbf45f344926767a4dab161df89f01d38240cc91765c3eebb1ed054`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 18:42:44 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 18:42:44 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 19 May 2025 18:42:44 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 19 May 2025 18:42:44 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 19 May 2025 18:42:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 May 2025 18:42:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434c8ed1b411bf87e31d51dcd5e11ad29b842c6ac23d29867f58c9b6657217f9`  
		Last Modified: Thu, 08 May 2025 17:16:04 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d509229eaab440944eafb92883af0415ca875e0db2665add61e48bfe43f6b4dd`  
		Last Modified: Thu, 08 May 2025 17:16:06 GMT  
		Size: 2.5 MB (2535687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7e6b0206db92121e0ec2f3f0386fdc698c9aa77ba1f54311c0d9ec732fc0b4`  
		Last Modified: Mon, 19 May 2025 23:26:51 GMT  
		Size: 70.0 MB (69997100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1839913b9686d60eed2b62fdacc02a73939156dae285739545e8c36b7fead2c5`  
		Last Modified: Mon, 19 May 2025 23:26:29 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:7debbe2f2bc26448edf87702c6731f5e6f8758c641c7cb927b9b1dd99e67402d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1116043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200827bbd04899d006cf9bea00f3d17163175a4fe376916a7240c36424cd6f65`

```dockerfile
```

-	Layers:
	-	`sha256:50c1484435b4113b054fa68bfb4926ffdb3b5317e27513dc7cf5d1f36918d45c`  
		Last Modified: Tue, 20 May 2025 00:10:42 GMT  
		Size: 1.1 MB (1100659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28b81d01ec345366ab824ec82d1893cdcde1b84d143e40d37c8bd76fc3cd8290`  
		Last Modified: Tue, 20 May 2025 00:10:43 GMT  
		Size: 15.4 KB (15384 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34.4`

```console
$ docker pull telegraf@sha256:9a01311eebad9720791ce968d3fa09c45f0c59dbb1f4a51e9bc9584be251fa0b
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
$ docker pull telegraf@sha256:b289ce50bd342db98198d5d69fff811f572a60afc298236b6ef519f225f46957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168910150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb24cda65638a71b5b18742e6e8c1113d75769b0660cb8db2d31acb5e9c8dfdc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c519c8dc0dae14ac0088efeb396c71954b827de10c5ca28d3d81ea4e688f193`  
		Last Modified: Tue, 01 Jul 2025 03:26:38 GMT  
		Size: 18.9 MB (18946679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae95b6f9c0a60cff96bbf3ab8070eb12f2aa41a80526aef3fc5ab6f2a26a73`  
		Last Modified: Tue, 01 Jul 2025 03:26:37 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc12a7f7e5ff648931583e2992f8c5d083136e89a91416cea614d684999bcfb`  
		Last Modified: Tue, 01 Jul 2025 03:26:46 GMT  
		Size: 77.4 MB (77446090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f35801655e1016773672ec32ecce5256761d2e7741c3d8006d31498f7fc728`  
		Last Modified: Tue, 01 Jul 2025 03:26:37 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:590a2e3d2ced54578ee0c47ae29249ea7ab0fc3160c806bb8e3203a912ee8a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6637917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a41c8d2d66fdcf95cc07041497d56f70b465681aeaa6fbe0b8dd11681e118e`

```dockerfile
```

-	Layers:
	-	`sha256:cd9595d93751dcf604506929bdc4761bec2e40b8583a8c930f46e3185e4d5fc3`  
		Last Modified: Tue, 01 Jul 2025 06:10:27 GMT  
		Size: 6.6 MB (6623447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fca6943adb03f60ab21e0d0eee60d13f1d89184ae3ee74a7601cb026b87be2b9`  
		Last Modified: Tue, 01 Jul 2025 06:10:28 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:45a545ff4f6d0db7989a64f567ac0bfae4b1d3ad11f411b7ce643a0f3fa3c16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155387450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70560a278fe67b2f30daf455b8dc48ccd1e3b7498d8f440e540896c3f21e355c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 19 May 2025 18:42:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 19 May 2025 18:42:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 May 2025 18:42:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6449907dadb3e534574a2fbaebc996906a8ec5bbb4a2b536a5bf81fd8b82f603`  
		Last Modified: Wed, 11 Jun 2025 15:11:55 GMT  
		Size: 17.7 MB (17725142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c3e4d696d461ef5c8e795643cada7a24e540bd4fdb43157a6c36d759d3fd3c`  
		Last Modified: Wed, 11 Jun 2025 15:16:19 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbeab7d12ce9af659e4c6c8bcf27f5a095d49ec6ea905d27bc9bc70b67188ff`  
		Last Modified: Wed, 11 Jun 2025 15:13:49 GMT  
		Size: 71.5 MB (71527051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75afb621067d3aca1fb3068d9c0faca23b02a460f8ce95b4626e00bc1ce3851`  
		Last Modified: Wed, 11 Jun 2025 15:13:42 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:76533e7f474714a10368c3dc1e583acc804f54eeaa8aaf89c49460944a8823ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6631862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897a304a0208b547c19dbdfee6f3223502d60248a364361898b2f510a726d930`

```dockerfile
```

-	Layers:
	-	`sha256:9d4ac8ab7f1732a34cdc9e52a2f2ad9a9264198e7b74b317b1b53b4dc69f75b2`  
		Last Modified: Wed, 11 Jun 2025 18:10:37 GMT  
		Size: 6.6 MB (6616996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2673c739a5f7ed41061943161355314134adf0e74fccca9d131ef11bd7d34a96`  
		Last Modified: Wed, 11 Jun 2025 18:10:37 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3a1f60e51ea97c496f5ea0c422bbf0ea9488196eb3b2cd891438dab7406c4262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160965879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab90a828e1f1ee9dc0996d31486e861ef885129a6e638b08cbf953abd4c67509`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 19 May 2025 18:42:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 19 May 2025 18:42:44 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 19 May 2025 18:42:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 May 2025 18:42:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9272eaa397ad42bf538f779ac47a75a0363f21b2774ded24e4b752d3a03e881`  
		Last Modified: Wed, 11 Jun 2025 13:17:08 GMT  
		Size: 18.9 MB (18871981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccb41b0f7395aa22520b1994b648327f4c2304d74d5be89decbe523899b0d37`  
		Last Modified: Wed, 11 Jun 2025 13:17:08 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71173eb69366a18934cb3088146a58f342006f927eb37ce7fba709252097f37a`  
		Last Modified: Wed, 11 Jun 2025 12:38:00 GMT  
		Size: 70.2 MB (70201085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d285f40ad4fc9c546f4493177288b453d263bc20c74f73a8db5b133ebea8cf8`  
		Last Modified: Wed, 11 Jun 2025 12:37:49 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:afdd727513593d03843c3b0ac81aac39fa8de875c45d4bafc54a8f83e0134ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6637975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611c479730fe5c6729c335881927d24ec76c6763bda0e9e1903f6e2c8dbb3435`

```dockerfile
```

-	Layers:
	-	`sha256:cd4eb9f0e39784767a8a995114016e1104b89fa9bd859f260751e6bf608b967d`  
		Last Modified: Wed, 11 Jun 2025 15:10:40 GMT  
		Size: 6.6 MB (6623081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e3c09ab286a564ec4e97994fe5af62a4ad98164d1541b378e5afdbab64cd43`  
		Last Modified: Wed, 11 Jun 2025 15:10:41 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34.4-alpine`

```console
$ docker pull telegraf@sha256:a18f6f4cd256131c9e3a0d22e4304421cc00992be16006a5a75feceee2af46de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:740b2f1b261acc9297fe0fad68322986532e7d9bdb59efa024c326b0c38478e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83313296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15721c8d81b3cd80a5f811e26c92fa62fb87187ac61a35cf76873182df727264`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 18:42:44 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 18:42:44 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 19 May 2025 18:42:44 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 19 May 2025 18:42:44 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 19 May 2025 18:42:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 May 2025 18:42:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f57d20f08c7b0bb65b5c15fd14d45946ee7d539fcb8ae5359f25a0c3d3dbbb2`  
		Last Modified: Mon, 19 May 2025 23:23:46 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49332a9ec0e4b728abc3baa00c33325c8e4317934105b9b29856ef462d67997e`  
		Last Modified: Mon, 19 May 2025 23:23:48 GMT  
		Size: 2.4 MB (2449565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942c6f48c3f6d0c87a2466b4cae308941b96a2471a83c1acc8efd9eb66e16be5`  
		Last Modified: Mon, 19 May 2025 23:24:16 GMT  
		Size: 77.2 MB (77236229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36fbb2315acfc4c17771e64880965d7ac100ba7672c86442dd8506dbc582e3b`  
		Last Modified: Mon, 19 May 2025 23:23:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9fd553c4e7501ca191957f61e73914e12f00188bc0a68b0d939c887b279132ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1120283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c698c74b911b99cb88e7165329c616f4eddba4e174592a5b3feea0a43f495237`

```dockerfile
```

-	Layers:
	-	`sha256:688b30db849dc63e5498ae60f5a848aef1b2ac6b3a8fab1188c5606a8961dcd2`  
		Last Modified: Tue, 20 May 2025 00:10:39 GMT  
		Size: 1.1 MB (1105020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07f9bd1a56b1c7d53eb673689b4807defee430946ba107ccce59198fc99366d0`  
		Last Modified: Tue, 20 May 2025 00:10:39 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2484dc4338c0457edc8113483b73c4ce24495ae42218965d2c8a8bf5b3a393a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76624559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8402837ffbf45f344926767a4dab161df89f01d38240cc91765c3eebb1ed054`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 18:42:44 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 18:42:44 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 19 May 2025 18:42:44 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 19 May 2025 18:42:44 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 19 May 2025 18:42:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 19 May 2025 18:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 May 2025 18:42:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434c8ed1b411bf87e31d51dcd5e11ad29b842c6ac23d29867f58c9b6657217f9`  
		Last Modified: Thu, 08 May 2025 17:16:04 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d509229eaab440944eafb92883af0415ca875e0db2665add61e48bfe43f6b4dd`  
		Last Modified: Thu, 08 May 2025 17:16:06 GMT  
		Size: 2.5 MB (2535687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7e6b0206db92121e0ec2f3f0386fdc698c9aa77ba1f54311c0d9ec732fc0b4`  
		Last Modified: Mon, 19 May 2025 23:26:51 GMT  
		Size: 70.0 MB (69997100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1839913b9686d60eed2b62fdacc02a73939156dae285739545e8c36b7fead2c5`  
		Last Modified: Mon, 19 May 2025 23:26:29 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:7debbe2f2bc26448edf87702c6731f5e6f8758c641c7cb927b9b1dd99e67402d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1116043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200827bbd04899d006cf9bea00f3d17163175a4fe376916a7240c36424cd6f65`

```dockerfile
```

-	Layers:
	-	`sha256:50c1484435b4113b054fa68bfb4926ffdb3b5317e27513dc7cf5d1f36918d45c`  
		Last Modified: Tue, 20 May 2025 00:10:42 GMT  
		Size: 1.1 MB (1100659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28b81d01ec345366ab824ec82d1893cdcde1b84d143e40d37c8bd76fc3cd8290`  
		Last Modified: Tue, 20 May 2025 00:10:43 GMT  
		Size: 15.4 KB (15384 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35`

```console
$ docker pull telegraf@sha256:23956c30b100ab67163c9ad4168c5f6a7921d68eb667b8338f99504121ee9226
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
$ docker pull telegraf@sha256:794857af3bfca93a8bb37c9d014da9aa4d42f867c217f9ab42a9b18e2251cda0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169934969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56407da986d0a6d13a51524f13c4a663499105dc0b5397b17afe4807fe3d9654`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72864e4928e35ff6c6b6e3e7aa816ee1b5f3fb618baaf2008ac865a34795926b`  
		Last Modified: Tue, 01 Jul 2025 03:26:38 GMT  
		Size: 18.9 MB (18946627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4eb62bea469c40ed112705779da59c026d8820bb81decb16912a5f7ca62cb6`  
		Last Modified: Tue, 01 Jul 2025 03:26:37 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de9ae5617fe32c7cbe7ffd1f1a3e43b37dffdb8bc7f6656e5e05f84b893a070`  
		Last Modified: Tue, 01 Jul 2025 03:26:46 GMT  
		Size: 78.5 MB (78470962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e475bea97f877cf09cd3ae2a132fb274e947e03baea4764b26d24b139526d1`  
		Last Modified: Tue, 01 Jul 2025 03:26:37 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:c25bb14a0abf2568f1b674b6cd3e8e1dcb0c4ee042356d740dadef6906e97d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6653216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80bd367ebb493ba94afbe5ac1ad1f798b550a32c3a4a0b156c35fdc26adf678`

```dockerfile
```

-	Layers:
	-	`sha256:fae96db7acc750044041ca25da5ce670b8f940272ed9f65b07dfdae55fb281e7`  
		Last Modified: Tue, 01 Jul 2025 06:10:33 GMT  
		Size: 6.6 MB (6638445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b00ccb6d978f64a7ed3887955d927efbbfea90c8d8a664c8865dafa16db3460a`  
		Last Modified: Tue, 01 Jul 2025 06:10:34 GMT  
		Size: 14.8 KB (14771 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:234efe5eca43c454934e2ab1443c098888827e15935897ddf5591b415b6822d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156370914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1668d1e3bbea6c1e6c184f99a888bc2e379791ddd259275c5c2504b3f23e4c27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6449907dadb3e534574a2fbaebc996906a8ec5bbb4a2b536a5bf81fd8b82f603`  
		Last Modified: Wed, 11 Jun 2025 15:11:55 GMT  
		Size: 17.7 MB (17725142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9378665d1fbace5ff58281c8769d5dd7956ae34dd48f5981527d5a253dc35f35`  
		Last Modified: Tue, 17 Jun 2025 22:02:03 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eeb49456c542ce43f24e8fe7a7b61aa78e8c5125a9b22659ee1d54a727a32bd`  
		Last Modified: Mon, 23 Jun 2025 21:51:28 GMT  
		Size: 72.5 MB (72510527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf28e68a60f2fe7286b78b3f256881fca4a85d6f547c8ccf235ec90abe89252`  
		Last Modified: Mon, 23 Jun 2025 21:51:09 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:d9058e4d487567b1b879300724f7c0b4f974a336c228ebd46288a7ea0f4b4c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6646557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9dd0fa53f237d51a161e634a1fca2cc256807bea0853ad0ed5ac32326aad5ae`

```dockerfile
```

-	Layers:
	-	`sha256:041b7a1c87fa324981c03e424373940afbcb8646e951d117c217d7a0c8e6caef`  
		Last Modified: Tue, 24 Jun 2025 00:10:37 GMT  
		Size: 6.6 MB (6631692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab0e104532ca127ca2198d21eb07e54f1f2981be5ad22e1d91a71218f5b4578`  
		Last Modified: Tue, 24 Jun 2025 00:10:37 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:07c7b62be9ff3af75017a2ec363c86c8f532566666984ec7fe3e9b5d725bf02e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161914465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1e713e42839bebab87906ae3f79b1436f086b39a2128676ead6bf9e8958234`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f54a5ba270c8c951d04c03b722b8248bd8f3e41dc8c3ab443d6aedcae4165f7`  
		Last Modified: Tue, 17 Jun 2025 22:07:58 GMT  
		Size: 18.9 MB (18872028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99487c7a328ad568d7b219d1ba0ac111561192b88793fd96629fa10378b2712b`  
		Last Modified: Tue, 17 Jun 2025 22:05:52 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1e599e5d86c57376b30aa8f44334f650e9144a7fa02612ea4f92f62cf9ae12`  
		Last Modified: Mon, 23 Jun 2025 21:51:20 GMT  
		Size: 71.1 MB (71149623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34431be71109f4ab0dae3e9e3138dbc83aa025cc99e6a77b8f79ba679a5e452`  
		Last Modified: Mon, 23 Jun 2025 21:51:05 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:f2e7923997956104d616cc6492446b03d043ecc1cc2c49259535fb5368a079c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6652671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bfd7e3c2de91c77e6ab9a7ea0f55c3a2ab4df0548cd0b06ead4f2473362318`

```dockerfile
```

-	Layers:
	-	`sha256:a50db35ca596919f9dbd929efc85dbee4d4333c84158f8495ffa05494acccbd9`  
		Last Modified: Tue, 24 Jun 2025 00:10:43 GMT  
		Size: 6.6 MB (6637777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26123943db9a6853d77aadaecb866e8273c121d5a8814e9eb0dc363e0bf63a45`  
		Last Modified: Tue, 24 Jun 2025 00:10:44 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35-alpine`

```console
$ docker pull telegraf@sha256:f406ae5d669a91f2ce4fd0ae8ea479dd883760e55e40deb31360af30ce777c36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:cd14989da5f4e656684bb024661121cf3d08384be2d4d7eda874bf67edbc50f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84344218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc73b7fce6be7ee8c60c2571ca2f0d58b10b2e1380e91d2e4a93f98016a2b86c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee991574603a73eca8e68ff1f93028fe15568de3293092a342b5020029662067`  
		Last Modified: Mon, 23 Jun 2025 21:51:41 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c77cb1b97f9f14b94bdfe648376a558faa016e53b6deb7e8e90e8d460f54b04`  
		Last Modified: Mon, 23 Jun 2025 21:51:43 GMT  
		Size: 2.4 MB (2449551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e12d4cbe4a7d022a9ee2c91373f0ac0621cdcf154e117e2f0fb0cf70399840`  
		Last Modified: Tue, 24 Jun 2025 00:10:42 GMT  
		Size: 78.3 MB (78267164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f3072feb5e6191df7b1f32cd9ea1f0e569746d701d5fe9fe64335860a56b5e`  
		Last Modified: Mon, 23 Jun 2025 21:51:42 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:71eb3f2817776bd497c8f93b2cc3d9c019c972ed1e9ba71f6abc9a0bf73465ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1134979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354824fbcfa95a60aca28551df8c584c7332e3ad5450ea756829fae1aef0c1cb`

```dockerfile
```

-	Layers:
	-	`sha256:af130bbf4ebb03f1b987341ccd534b47c03dbf6a40c99468ba959bda0a21225c`  
		Last Modified: Tue, 24 Jun 2025 00:10:36 GMT  
		Size: 1.1 MB (1119716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4010b35a1602a9a5bac65a732114ff3d5ee6affbeff1132977e9716140a0dede`  
		Last Modified: Tue, 24 Jun 2025 00:10:37 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f28cc18f47c24f8101102c68e367abcd563f3402f40a838674b8cd7fd12caf6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77574890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3add096e9525224ff50f71eb7792f15f87c8846da6e43528f379ff2b92a79ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f510c09f9a01186dd4c2402783364f8758f93441babfacf9dc0d91b8374bf15`  
		Last Modified: Tue, 17 Jun 2025 22:02:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4dbe240912179424627f553a57e7c9e83f060e9540143c361167cd424a6c0f`  
		Last Modified: Tue, 17 Jun 2025 22:02:44 GMT  
		Size: 2.5 MB (2535676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2b6be6e5df7035cf56d5242963ca8469ba453beacccbc58bb15f4909457df`  
		Last Modified: Tue, 24 Jun 2025 00:16:20 GMT  
		Size: 70.9 MB (70947442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312a578c0513a5e4fa436defe8a9ae03df9967fe84a5e423147efca200ddd609`  
		Last Modified: Mon, 23 Jun 2025 21:57:25 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:55a184c46a7912642cece1eca42ab1803758cd7feb68eda94da149d8a0765444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1130740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce60141c4c1529bd0d9437ea6587b150e2115d71476c53426a66aa1f5bff9aea`

```dockerfile
```

-	Layers:
	-	`sha256:9aac6915cad74a23c2b3a7a2d1a58233ec1de79df0d6cc31cba9d8d8122fd9a3`  
		Last Modified: Tue, 24 Jun 2025 00:10:50 GMT  
		Size: 1.1 MB (1115355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0900df99b9669bfeeb42ed8cdc2479b6c35cac5a9ea3a2172351db506ee859a`  
		Last Modified: Tue, 24 Jun 2025 00:10:51 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.1`

```console
$ docker pull telegraf@sha256:23956c30b100ab67163c9ad4168c5f6a7921d68eb667b8338f99504121ee9226
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.1` - linux; amd64

```console
$ docker pull telegraf@sha256:794857af3bfca93a8bb37c9d014da9aa4d42f867c217f9ab42a9b18e2251cda0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169934969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56407da986d0a6d13a51524f13c4a663499105dc0b5397b17afe4807fe3d9654`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72864e4928e35ff6c6b6e3e7aa816ee1b5f3fb618baaf2008ac865a34795926b`  
		Last Modified: Tue, 01 Jul 2025 03:26:38 GMT  
		Size: 18.9 MB (18946627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4eb62bea469c40ed112705779da59c026d8820bb81decb16912a5f7ca62cb6`  
		Last Modified: Tue, 01 Jul 2025 03:26:37 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de9ae5617fe32c7cbe7ffd1f1a3e43b37dffdb8bc7f6656e5e05f84b893a070`  
		Last Modified: Tue, 01 Jul 2025 03:26:46 GMT  
		Size: 78.5 MB (78470962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e475bea97f877cf09cd3ae2a132fb274e947e03baea4764b26d24b139526d1`  
		Last Modified: Tue, 01 Jul 2025 03:26:37 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:c25bb14a0abf2568f1b674b6cd3e8e1dcb0c4ee042356d740dadef6906e97d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6653216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80bd367ebb493ba94afbe5ac1ad1f798b550a32c3a4a0b156c35fdc26adf678`

```dockerfile
```

-	Layers:
	-	`sha256:fae96db7acc750044041ca25da5ce670b8f940272ed9f65b07dfdae55fb281e7`  
		Last Modified: Tue, 01 Jul 2025 06:10:33 GMT  
		Size: 6.6 MB (6638445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b00ccb6d978f64a7ed3887955d927efbbfea90c8d8a664c8865dafa16db3460a`  
		Last Modified: Tue, 01 Jul 2025 06:10:34 GMT  
		Size: 14.8 KB (14771 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.1` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:234efe5eca43c454934e2ab1443c098888827e15935897ddf5591b415b6822d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156370914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1668d1e3bbea6c1e6c184f99a888bc2e379791ddd259275c5c2504b3f23e4c27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6449907dadb3e534574a2fbaebc996906a8ec5bbb4a2b536a5bf81fd8b82f603`  
		Last Modified: Wed, 11 Jun 2025 15:11:55 GMT  
		Size: 17.7 MB (17725142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9378665d1fbace5ff58281c8769d5dd7956ae34dd48f5981527d5a253dc35f35`  
		Last Modified: Tue, 17 Jun 2025 22:02:03 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eeb49456c542ce43f24e8fe7a7b61aa78e8c5125a9b22659ee1d54a727a32bd`  
		Last Modified: Mon, 23 Jun 2025 21:51:28 GMT  
		Size: 72.5 MB (72510527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf28e68a60f2fe7286b78b3f256881fca4a85d6f547c8ccf235ec90abe89252`  
		Last Modified: Mon, 23 Jun 2025 21:51:09 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:d9058e4d487567b1b879300724f7c0b4f974a336c228ebd46288a7ea0f4b4c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6646557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9dd0fa53f237d51a161e634a1fca2cc256807bea0853ad0ed5ac32326aad5ae`

```dockerfile
```

-	Layers:
	-	`sha256:041b7a1c87fa324981c03e424373940afbcb8646e951d117c217d7a0c8e6caef`  
		Last Modified: Tue, 24 Jun 2025 00:10:37 GMT  
		Size: 6.6 MB (6631692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab0e104532ca127ca2198d21eb07e54f1f2981be5ad22e1d91a71218f5b4578`  
		Last Modified: Tue, 24 Jun 2025 00:10:37 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.1` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:07c7b62be9ff3af75017a2ec363c86c8f532566666984ec7fe3e9b5d725bf02e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161914465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1e713e42839bebab87906ae3f79b1436f086b39a2128676ead6bf9e8958234`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f54a5ba270c8c951d04c03b722b8248bd8f3e41dc8c3ab443d6aedcae4165f7`  
		Last Modified: Tue, 17 Jun 2025 22:07:58 GMT  
		Size: 18.9 MB (18872028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99487c7a328ad568d7b219d1ba0ac111561192b88793fd96629fa10378b2712b`  
		Last Modified: Tue, 17 Jun 2025 22:05:52 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1e599e5d86c57376b30aa8f44334f650e9144a7fa02612ea4f92f62cf9ae12`  
		Last Modified: Mon, 23 Jun 2025 21:51:20 GMT  
		Size: 71.1 MB (71149623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34431be71109f4ab0dae3e9e3138dbc83aa025cc99e6a77b8f79ba679a5e452`  
		Last Modified: Mon, 23 Jun 2025 21:51:05 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:f2e7923997956104d616cc6492446b03d043ecc1cc2c49259535fb5368a079c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6652671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bfd7e3c2de91c77e6ab9a7ea0f55c3a2ab4df0548cd0b06ead4f2473362318`

```dockerfile
```

-	Layers:
	-	`sha256:a50db35ca596919f9dbd929efc85dbee4d4333c84158f8495ffa05494acccbd9`  
		Last Modified: Tue, 24 Jun 2025 00:10:43 GMT  
		Size: 6.6 MB (6637777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26123943db9a6853d77aadaecb866e8273c121d5a8814e9eb0dc363e0bf63a45`  
		Last Modified: Tue, 24 Jun 2025 00:10:44 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.1-alpine`

```console
$ docker pull telegraf@sha256:f406ae5d669a91f2ce4fd0ae8ea479dd883760e55e40deb31360af30ce777c36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.1-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:cd14989da5f4e656684bb024661121cf3d08384be2d4d7eda874bf67edbc50f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84344218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc73b7fce6be7ee8c60c2571ca2f0d58b10b2e1380e91d2e4a93f98016a2b86c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee991574603a73eca8e68ff1f93028fe15568de3293092a342b5020029662067`  
		Last Modified: Mon, 23 Jun 2025 21:51:41 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c77cb1b97f9f14b94bdfe648376a558faa016e53b6deb7e8e90e8d460f54b04`  
		Last Modified: Mon, 23 Jun 2025 21:51:43 GMT  
		Size: 2.4 MB (2449551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e12d4cbe4a7d022a9ee2c91373f0ac0621cdcf154e117e2f0fb0cf70399840`  
		Last Modified: Tue, 24 Jun 2025 00:10:42 GMT  
		Size: 78.3 MB (78267164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f3072feb5e6191df7b1f32cd9ea1f0e569746d701d5fe9fe64335860a56b5e`  
		Last Modified: Mon, 23 Jun 2025 21:51:42 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.1-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:71eb3f2817776bd497c8f93b2cc3d9c019c972ed1e9ba71f6abc9a0bf73465ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1134979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354824fbcfa95a60aca28551df8c584c7332e3ad5450ea756829fae1aef0c1cb`

```dockerfile
```

-	Layers:
	-	`sha256:af130bbf4ebb03f1b987341ccd534b47c03dbf6a40c99468ba959bda0a21225c`  
		Last Modified: Tue, 24 Jun 2025 00:10:36 GMT  
		Size: 1.1 MB (1119716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4010b35a1602a9a5bac65a732114ff3d5ee6affbeff1132977e9716140a0dede`  
		Last Modified: Tue, 24 Jun 2025 00:10:37 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.1-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f28cc18f47c24f8101102c68e367abcd563f3402f40a838674b8cd7fd12caf6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77574890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3add096e9525224ff50f71eb7792f15f87c8846da6e43528f379ff2b92a79ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f510c09f9a01186dd4c2402783364f8758f93441babfacf9dc0d91b8374bf15`  
		Last Modified: Tue, 17 Jun 2025 22:02:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4dbe240912179424627f553a57e7c9e83f060e9540143c361167cd424a6c0f`  
		Last Modified: Tue, 17 Jun 2025 22:02:44 GMT  
		Size: 2.5 MB (2535676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2b6be6e5df7035cf56d5242963ca8469ba453beacccbc58bb15f4909457df`  
		Last Modified: Tue, 24 Jun 2025 00:16:20 GMT  
		Size: 70.9 MB (70947442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312a578c0513a5e4fa436defe8a9ae03df9967fe84a5e423147efca200ddd609`  
		Last Modified: Mon, 23 Jun 2025 21:57:25 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.1-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:55a184c46a7912642cece1eca42ab1803758cd7feb68eda94da149d8a0765444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1130740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce60141c4c1529bd0d9437ea6587b150e2115d71476c53426a66aa1f5bff9aea`

```dockerfile
```

-	Layers:
	-	`sha256:9aac6915cad74a23c2b3a7a2d1a58233ec1de79df0d6cc31cba9d8d8122fd9a3`  
		Last Modified: Tue, 24 Jun 2025 00:10:50 GMT  
		Size: 1.1 MB (1115355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0900df99b9669bfeeb42ed8cdc2479b6c35cac5a9ea3a2172351db506ee859a`  
		Last Modified: Tue, 24 Jun 2025 00:10:51 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:f406ae5d669a91f2ce4fd0ae8ea479dd883760e55e40deb31360af30ce777c36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:cd14989da5f4e656684bb024661121cf3d08384be2d4d7eda874bf67edbc50f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84344218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc73b7fce6be7ee8c60c2571ca2f0d58b10b2e1380e91d2e4a93f98016a2b86c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee991574603a73eca8e68ff1f93028fe15568de3293092a342b5020029662067`  
		Last Modified: Mon, 23 Jun 2025 21:51:41 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c77cb1b97f9f14b94bdfe648376a558faa016e53b6deb7e8e90e8d460f54b04`  
		Last Modified: Mon, 23 Jun 2025 21:51:43 GMT  
		Size: 2.4 MB (2449551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e12d4cbe4a7d022a9ee2c91373f0ac0621cdcf154e117e2f0fb0cf70399840`  
		Last Modified: Tue, 24 Jun 2025 00:10:42 GMT  
		Size: 78.3 MB (78267164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f3072feb5e6191df7b1f32cd9ea1f0e569746d701d5fe9fe64335860a56b5e`  
		Last Modified: Mon, 23 Jun 2025 21:51:42 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:71eb3f2817776bd497c8f93b2cc3d9c019c972ed1e9ba71f6abc9a0bf73465ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1134979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354824fbcfa95a60aca28551df8c584c7332e3ad5450ea756829fae1aef0c1cb`

```dockerfile
```

-	Layers:
	-	`sha256:af130bbf4ebb03f1b987341ccd534b47c03dbf6a40c99468ba959bda0a21225c`  
		Last Modified: Tue, 24 Jun 2025 00:10:36 GMT  
		Size: 1.1 MB (1119716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4010b35a1602a9a5bac65a732114ff3d5ee6affbeff1132977e9716140a0dede`  
		Last Modified: Tue, 24 Jun 2025 00:10:37 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f28cc18f47c24f8101102c68e367abcd563f3402f40a838674b8cd7fd12caf6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77574890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3add096e9525224ff50f71eb7792f15f87c8846da6e43528f379ff2b92a79ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f510c09f9a01186dd4c2402783364f8758f93441babfacf9dc0d91b8374bf15`  
		Last Modified: Tue, 17 Jun 2025 22:02:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4dbe240912179424627f553a57e7c9e83f060e9540143c361167cd424a6c0f`  
		Last Modified: Tue, 17 Jun 2025 22:02:44 GMT  
		Size: 2.5 MB (2535676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2b6be6e5df7035cf56d5242963ca8469ba453beacccbc58bb15f4909457df`  
		Last Modified: Tue, 24 Jun 2025 00:16:20 GMT  
		Size: 70.9 MB (70947442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312a578c0513a5e4fa436defe8a9ae03df9967fe84a5e423147efca200ddd609`  
		Last Modified: Mon, 23 Jun 2025 21:57:25 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:55a184c46a7912642cece1eca42ab1803758cd7feb68eda94da149d8a0765444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1130740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce60141c4c1529bd0d9437ea6587b150e2115d71476c53426a66aa1f5bff9aea`

```dockerfile
```

-	Layers:
	-	`sha256:9aac6915cad74a23c2b3a7a2d1a58233ec1de79df0d6cc31cba9d8d8122fd9a3`  
		Last Modified: Tue, 24 Jun 2025 00:10:50 GMT  
		Size: 1.1 MB (1115355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0900df99b9669bfeeb42ed8cdc2479b6c35cac5a9ea3a2172351db506ee859a`  
		Last Modified: Tue, 24 Jun 2025 00:10:51 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:23956c30b100ab67163c9ad4168c5f6a7921d68eb667b8338f99504121ee9226
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
$ docker pull telegraf@sha256:794857af3bfca93a8bb37c9d014da9aa4d42f867c217f9ab42a9b18e2251cda0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169934969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56407da986d0a6d13a51524f13c4a663499105dc0b5397b17afe4807fe3d9654`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72864e4928e35ff6c6b6e3e7aa816ee1b5f3fb618baaf2008ac865a34795926b`  
		Last Modified: Tue, 01 Jul 2025 03:26:38 GMT  
		Size: 18.9 MB (18946627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4eb62bea469c40ed112705779da59c026d8820bb81decb16912a5f7ca62cb6`  
		Last Modified: Tue, 01 Jul 2025 03:26:37 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de9ae5617fe32c7cbe7ffd1f1a3e43b37dffdb8bc7f6656e5e05f84b893a070`  
		Last Modified: Tue, 01 Jul 2025 03:26:46 GMT  
		Size: 78.5 MB (78470962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e475bea97f877cf09cd3ae2a132fb274e947e03baea4764b26d24b139526d1`  
		Last Modified: Tue, 01 Jul 2025 03:26:37 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:c25bb14a0abf2568f1b674b6cd3e8e1dcb0c4ee042356d740dadef6906e97d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6653216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80bd367ebb493ba94afbe5ac1ad1f798b550a32c3a4a0b156c35fdc26adf678`

```dockerfile
```

-	Layers:
	-	`sha256:fae96db7acc750044041ca25da5ce670b8f940272ed9f65b07dfdae55fb281e7`  
		Last Modified: Tue, 01 Jul 2025 06:10:33 GMT  
		Size: 6.6 MB (6638445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b00ccb6d978f64a7ed3887955d927efbbfea90c8d8a664c8865dafa16db3460a`  
		Last Modified: Tue, 01 Jul 2025 06:10:34 GMT  
		Size: 14.8 KB (14771 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:234efe5eca43c454934e2ab1443c098888827e15935897ddf5591b415b6822d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156370914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1668d1e3bbea6c1e6c184f99a888bc2e379791ddd259275c5c2504b3f23e4c27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6449907dadb3e534574a2fbaebc996906a8ec5bbb4a2b536a5bf81fd8b82f603`  
		Last Modified: Wed, 11 Jun 2025 15:11:55 GMT  
		Size: 17.7 MB (17725142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9378665d1fbace5ff58281c8769d5dd7956ae34dd48f5981527d5a253dc35f35`  
		Last Modified: Tue, 17 Jun 2025 22:02:03 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eeb49456c542ce43f24e8fe7a7b61aa78e8c5125a9b22659ee1d54a727a32bd`  
		Last Modified: Mon, 23 Jun 2025 21:51:28 GMT  
		Size: 72.5 MB (72510527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf28e68a60f2fe7286b78b3f256881fca4a85d6f547c8ccf235ec90abe89252`  
		Last Modified: Mon, 23 Jun 2025 21:51:09 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:d9058e4d487567b1b879300724f7c0b4f974a336c228ebd46288a7ea0f4b4c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6646557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9dd0fa53f237d51a161e634a1fca2cc256807bea0853ad0ed5ac32326aad5ae`

```dockerfile
```

-	Layers:
	-	`sha256:041b7a1c87fa324981c03e424373940afbcb8646e951d117c217d7a0c8e6caef`  
		Last Modified: Tue, 24 Jun 2025 00:10:37 GMT  
		Size: 6.6 MB (6631692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab0e104532ca127ca2198d21eb07e54f1f2981be5ad22e1d91a71218f5b4578`  
		Last Modified: Tue, 24 Jun 2025 00:10:37 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:07c7b62be9ff3af75017a2ec363c86c8f532566666984ec7fe3e9b5d725bf02e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161914465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1e713e42839bebab87906ae3f79b1436f086b39a2128676ead6bf9e8958234`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f54a5ba270c8c951d04c03b722b8248bd8f3e41dc8c3ab443d6aedcae4165f7`  
		Last Modified: Tue, 17 Jun 2025 22:07:58 GMT  
		Size: 18.9 MB (18872028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99487c7a328ad568d7b219d1ba0ac111561192b88793fd96629fa10378b2712b`  
		Last Modified: Tue, 17 Jun 2025 22:05:52 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1e599e5d86c57376b30aa8f44334f650e9144a7fa02612ea4f92f62cf9ae12`  
		Last Modified: Mon, 23 Jun 2025 21:51:20 GMT  
		Size: 71.1 MB (71149623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34431be71109f4ab0dae3e9e3138dbc83aa025cc99e6a77b8f79ba679a5e452`  
		Last Modified: Mon, 23 Jun 2025 21:51:05 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:f2e7923997956104d616cc6492446b03d043ecc1cc2c49259535fb5368a079c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6652671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bfd7e3c2de91c77e6ab9a7ea0f55c3a2ab4df0548cd0b06ead4f2473362318`

```dockerfile
```

-	Layers:
	-	`sha256:a50db35ca596919f9dbd929efc85dbee4d4333c84158f8495ffa05494acccbd9`  
		Last Modified: Tue, 24 Jun 2025 00:10:43 GMT  
		Size: 6.6 MB (6637777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26123943db9a6853d77aadaecb866e8273c121d5a8814e9eb0dc363e0bf63a45`  
		Last Modified: Tue, 24 Jun 2025 00:10:44 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
