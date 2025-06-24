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
$ docker pull telegraf@sha256:84acff3e5f3c9eaa6aa427dc91e107ef79febbf6f7bf63d73cd0186fc86b5ccd
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
$ docker pull telegraf@sha256:31f04b5bd7a9b52c1c7ed16c1fde1a9e0c55de21a4b698e78e461b6c3536525f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168769106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9530fab264191c66fff3474ea32fa3ed2b3945802874ec605996e47caa3e4f00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b298ca43a16d856bafb09f79aff018680e44c902b9708a120f7829f3c1d0dbb`  
		Last Modified: Wed, 11 Jun 2025 00:08:27 GMT  
		Size: 18.9 MB (18946697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991765328cd2f8ad40e27cf9dbd225ecc0f3c9afa68ddcfdd75a24789f2b3739`  
		Last Modified: Wed, 11 Jun 2025 00:08:27 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2be4752f1a044b68ceaa2469afcb2138347dfc0b3eb60bc5889bd27ef67e888`  
		Last Modified: Wed, 11 Jun 2025 00:08:33 GMT  
		Size: 77.3 MB (77310034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330451eebea036dd4e233644fa4c486f5c5e8f8aa590d6166f27e7e4cff03bfe`  
		Last Modified: Wed, 11 Jun 2025 00:08:27 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:e3bb1033a183cadbde3fe90d6acb3a9c3b33d780be0cbf4dd2b11bc78c0ed25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6630389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a75c3779898f3376f57bc2a33ea2644ebf2055fb3d9aa3f4ba5b4f872d04d0`

```dockerfile
```

-	Layers:
	-	`sha256:3a9d1303c720f8af87c451eeb42dbc40d69141d8e9d3b0f4f0d1421aea289107`  
		Last Modified: Wed, 11 Jun 2025 03:10:26 GMT  
		Size: 6.6 MB (6615919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca2e45fffe3567a53a43e524a534127c04c8d6ee07db7f0a6fdc33840e143d89`  
		Last Modified: Wed, 11 Jun 2025 03:10:27 GMT  
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
$ docker pull telegraf@sha256:84acff3e5f3c9eaa6aa427dc91e107ef79febbf6f7bf63d73cd0186fc86b5ccd
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
$ docker pull telegraf@sha256:31f04b5bd7a9b52c1c7ed16c1fde1a9e0c55de21a4b698e78e461b6c3536525f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168769106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9530fab264191c66fff3474ea32fa3ed2b3945802874ec605996e47caa3e4f00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b298ca43a16d856bafb09f79aff018680e44c902b9708a120f7829f3c1d0dbb`  
		Last Modified: Wed, 11 Jun 2025 00:08:27 GMT  
		Size: 18.9 MB (18946697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991765328cd2f8ad40e27cf9dbd225ecc0f3c9afa68ddcfdd75a24789f2b3739`  
		Last Modified: Wed, 11 Jun 2025 00:08:27 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2be4752f1a044b68ceaa2469afcb2138347dfc0b3eb60bc5889bd27ef67e888`  
		Last Modified: Wed, 11 Jun 2025 00:08:33 GMT  
		Size: 77.3 MB (77310034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330451eebea036dd4e233644fa4c486f5c5e8f8aa590d6166f27e7e4cff03bfe`  
		Last Modified: Wed, 11 Jun 2025 00:08:27 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:e3bb1033a183cadbde3fe90d6acb3a9c3b33d780be0cbf4dd2b11bc78c0ed25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6630389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a75c3779898f3376f57bc2a33ea2644ebf2055fb3d9aa3f4ba5b4f872d04d0`

```dockerfile
```

-	Layers:
	-	`sha256:3a9d1303c720f8af87c451eeb42dbc40d69141d8e9d3b0f4f0d1421aea289107`  
		Last Modified: Wed, 11 Jun 2025 03:10:26 GMT  
		Size: 6.6 MB (6615919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca2e45fffe3567a53a43e524a534127c04c8d6ee07db7f0a6fdc33840e143d89`  
		Last Modified: Wed, 11 Jun 2025 03:10:27 GMT  
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
$ docker pull telegraf@sha256:c3ffe02a814fba78c0d811a2b75b7d64b9ef56750030b671cb1355d581a2123d
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
$ docker pull telegraf@sha256:ebd28432537368a021adcc509c8a6865d9648e151197989650f44157c6d186e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168905204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3bc7a126664f73f1e4eb09ff001d6b13da6a6b4db7558ff986c91bf4bf481a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6cdba89edb802101d9452e5b48ea25d788b3543709fa1a041282fba5a5ccce`  
		Last Modified: Wed, 11 Jun 2025 00:09:19 GMT  
		Size: 18.9 MB (18946707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895e212150671b2b85274d553a8a027a50da75030d9cbceaae5b0840540818e0`  
		Last Modified: Wed, 11 Jun 2025 00:09:16 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a558a1e264c2c2ae93b2c8ae67ab46627d1956677835a8e07b14eec7bd17f2`  
		Last Modified: Wed, 11 Jun 2025 00:09:23 GMT  
		Size: 77.4 MB (77446110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdb13042e44da2a35770f9a09b5af6ba80dc8021dd33a9c0bb451495aa65ed`  
		Last Modified: Wed, 11 Jun 2025 00:09:17 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:2355bb40d3c9aba6f6c7f62a82db3587a9a0a6ce5109bd54f7ecc7d91c58df33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6637165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de931ac1ae971b8e670ec7250be10c64ba6e3fae129979fcf79be28a91c97cf`

```dockerfile
```

-	Layers:
	-	`sha256:e823304da466e14b1e19c8d1b5bcb0417a0a9934ba871d79aa4189eec311ea5c`  
		Last Modified: Wed, 11 Jun 2025 03:10:31 GMT  
		Size: 6.6 MB (6622393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3eb8e114251127b53c591c87df8551d4e69bfd4c018042ecafb5dfce64f918d`  
		Last Modified: Wed, 11 Jun 2025 03:10:32 GMT  
		Size: 14.8 KB (14772 bytes)  
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
$ docker pull telegraf@sha256:c3ffe02a814fba78c0d811a2b75b7d64b9ef56750030b671cb1355d581a2123d
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
$ docker pull telegraf@sha256:ebd28432537368a021adcc509c8a6865d9648e151197989650f44157c6d186e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168905204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3bc7a126664f73f1e4eb09ff001d6b13da6a6b4db7558ff986c91bf4bf481a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6cdba89edb802101d9452e5b48ea25d788b3543709fa1a041282fba5a5ccce`  
		Last Modified: Wed, 11 Jun 2025 00:09:19 GMT  
		Size: 18.9 MB (18946707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895e212150671b2b85274d553a8a027a50da75030d9cbceaae5b0840540818e0`  
		Last Modified: Wed, 11 Jun 2025 00:09:16 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a558a1e264c2c2ae93b2c8ae67ab46627d1956677835a8e07b14eec7bd17f2`  
		Last Modified: Wed, 11 Jun 2025 00:09:23 GMT  
		Size: 77.4 MB (77446110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdb13042e44da2a35770f9a09b5af6ba80dc8021dd33a9c0bb451495aa65ed`  
		Last Modified: Wed, 11 Jun 2025 00:09:17 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:2355bb40d3c9aba6f6c7f62a82db3587a9a0a6ce5109bd54f7ecc7d91c58df33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6637165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de931ac1ae971b8e670ec7250be10c64ba6e3fae129979fcf79be28a91c97cf`

```dockerfile
```

-	Layers:
	-	`sha256:e823304da466e14b1e19c8d1b5bcb0417a0a9934ba871d79aa4189eec311ea5c`  
		Last Modified: Wed, 11 Jun 2025 03:10:31 GMT  
		Size: 6.6 MB (6622393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3eb8e114251127b53c591c87df8551d4e69bfd4c018042ecafb5dfce64f918d`  
		Last Modified: Wed, 11 Jun 2025 03:10:32 GMT  
		Size: 14.8 KB (14772 bytes)  
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
$ docker pull telegraf@sha256:1b4dbebb724c61726c1c44edc15067a176020c35207620e06212c2e72339435e
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
$ docker pull telegraf@sha256:25cf4d910e75c1631c60242fd0fb777697de7287538a6390f22f5ec3f28b3479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169929889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7745ba6757add3cd32dbe5b328c7d6e30a54721b41f87744ada181c4dfe6a0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04f894c9e9144c5a44b547f93fa55733fc6b7d2ddc31d5b9c13ff2307a74fb7`  
		Last Modified: Mon, 23 Jun 2025 21:51:45 GMT  
		Size: 18.9 MB (18946572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998a701658913f63bea75a9c425ccf195a5ab83307bdfb9c2b391e2b8af81642`  
		Last Modified: Mon, 23 Jun 2025 21:51:42 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697f8bb75caf60e34009e2b31b54126f6ba87c97ab1a061ca78d41d41ca67a86`  
		Last Modified: Tue, 24 Jun 2025 00:10:41 GMT  
		Size: 78.5 MB (78470943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a89198acf78f2e74f68400a5555343b3301e654b6eb77b85f9670d463fac329`  
		Last Modified: Mon, 23 Jun 2025 21:51:42 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:bbeb16248fca8e87a79da0088556d9f67d89591bde1f3f5398ec33426f995c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07064035e41321f35dca453d90152bfd2bd683036ae7f0fd1e7975bd50f84c70`

```dockerfile
```

-	Layers:
	-	`sha256:836585210c55cda93ccb51298f721a3d39e79b9c3a16e1ed5030c7e28e184432`  
		Last Modified: Tue, 24 Jun 2025 00:10:30 GMT  
		Size: 6.6 MB (6637089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bcc5c93c20fc60dcaf0b42c95872afc8a517d122dcfc8d8ea437cbd2e4bc0d8`  
		Last Modified: Tue, 24 Jun 2025 00:10:31 GMT  
		Size: 14.8 KB (14772 bytes)  
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
$ docker pull telegraf@sha256:1b4dbebb724c61726c1c44edc15067a176020c35207620e06212c2e72339435e
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
$ docker pull telegraf@sha256:25cf4d910e75c1631c60242fd0fb777697de7287538a6390f22f5ec3f28b3479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169929889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7745ba6757add3cd32dbe5b328c7d6e30a54721b41f87744ada181c4dfe6a0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04f894c9e9144c5a44b547f93fa55733fc6b7d2ddc31d5b9c13ff2307a74fb7`  
		Last Modified: Mon, 23 Jun 2025 21:51:45 GMT  
		Size: 18.9 MB (18946572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998a701658913f63bea75a9c425ccf195a5ab83307bdfb9c2b391e2b8af81642`  
		Last Modified: Mon, 23 Jun 2025 21:51:42 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697f8bb75caf60e34009e2b31b54126f6ba87c97ab1a061ca78d41d41ca67a86`  
		Last Modified: Tue, 24 Jun 2025 00:10:41 GMT  
		Size: 78.5 MB (78470943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a89198acf78f2e74f68400a5555343b3301e654b6eb77b85f9670d463fac329`  
		Last Modified: Mon, 23 Jun 2025 21:51:42 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:bbeb16248fca8e87a79da0088556d9f67d89591bde1f3f5398ec33426f995c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07064035e41321f35dca453d90152bfd2bd683036ae7f0fd1e7975bd50f84c70`

```dockerfile
```

-	Layers:
	-	`sha256:836585210c55cda93ccb51298f721a3d39e79b9c3a16e1ed5030c7e28e184432`  
		Last Modified: Tue, 24 Jun 2025 00:10:30 GMT  
		Size: 6.6 MB (6637089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bcc5c93c20fc60dcaf0b42c95872afc8a517d122dcfc8d8ea437cbd2e4bc0d8`  
		Last Modified: Tue, 24 Jun 2025 00:10:31 GMT  
		Size: 14.8 KB (14772 bytes)  
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
$ docker pull telegraf@sha256:1b4dbebb724c61726c1c44edc15067a176020c35207620e06212c2e72339435e
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
$ docker pull telegraf@sha256:25cf4d910e75c1631c60242fd0fb777697de7287538a6390f22f5ec3f28b3479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169929889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7745ba6757add3cd32dbe5b328c7d6e30a54721b41f87744ada181c4dfe6a0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04f894c9e9144c5a44b547f93fa55733fc6b7d2ddc31d5b9c13ff2307a74fb7`  
		Last Modified: Mon, 23 Jun 2025 21:51:45 GMT  
		Size: 18.9 MB (18946572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998a701658913f63bea75a9c425ccf195a5ab83307bdfb9c2b391e2b8af81642`  
		Last Modified: Mon, 23 Jun 2025 21:51:42 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697f8bb75caf60e34009e2b31b54126f6ba87c97ab1a061ca78d41d41ca67a86`  
		Last Modified: Tue, 24 Jun 2025 00:10:41 GMT  
		Size: 78.5 MB (78470943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a89198acf78f2e74f68400a5555343b3301e654b6eb77b85f9670d463fac329`  
		Last Modified: Mon, 23 Jun 2025 21:51:42 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:bbeb16248fca8e87a79da0088556d9f67d89591bde1f3f5398ec33426f995c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07064035e41321f35dca453d90152bfd2bd683036ae7f0fd1e7975bd50f84c70`

```dockerfile
```

-	Layers:
	-	`sha256:836585210c55cda93ccb51298f721a3d39e79b9c3a16e1ed5030c7e28e184432`  
		Last Modified: Tue, 24 Jun 2025 00:10:30 GMT  
		Size: 6.6 MB (6637089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bcc5c93c20fc60dcaf0b42c95872afc8a517d122dcfc8d8ea437cbd2e4bc0d8`  
		Last Modified: Tue, 24 Jun 2025 00:10:31 GMT  
		Size: 14.8 KB (14772 bytes)  
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
