<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.32`](#telegraf132)
-	[`telegraf:1.32-alpine`](#telegraf132-alpine)
-	[`telegraf:1.32.3`](#telegraf1323)
-	[`telegraf:1.32.3-alpine`](#telegraf1323-alpine)
-	[`telegraf:1.33`](#telegraf133)
-	[`telegraf:1.33-alpine`](#telegraf133-alpine)
-	[`telegraf:1.33.3`](#telegraf1333)
-	[`telegraf:1.33.3-alpine`](#telegraf1333-alpine)
-	[`telegraf:1.34`](#telegraf134)
-	[`telegraf:1.34-alpine`](#telegraf134-alpine)
-	[`telegraf:1.34.0`](#telegraf1340)
-	[`telegraf:1.34.0-alpine`](#telegraf1340-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.32`

```console
$ docker pull telegraf@sha256:781d56e8ef2218f02d10545d526eb2341555adfd7ed9cda73c681155d735591d
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
$ docker pull telegraf@sha256:7e9c741c66e6c36a994bf59d20925a49c8fac4b4e659c0c26c8041957e9c1c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161506224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c680864557b2b3972e26ee25fe9d70fea1d337c7cf919f763a276c784b5e658`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cdbcd7a3b8e2113a68c04122c987b8e1356fbd1c5409cd84925418c4f71d81`  
		Last Modified: Tue, 25 Feb 2025 03:20:28 GMT  
		Size: 18.9 MB (18948113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39d45b98f2b3b33c43cced7e334f1a56d5e404525bcbd2a1c732d4ae1f23bc6`  
		Last Modified: Tue, 25 Feb 2025 03:20:27 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f69f009be6ba57b0997fba811ee12b698781b508b0773400015f58bac34cfae`  
		Last Modified: Tue, 25 Feb 2025 03:20:28 GMT  
		Size: 70.0 MB (70021086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9d26b56568dacd6cc96c42fbac1cb9c41aa17a7ef42e1cdf49e745176cdbd5`  
		Last Modified: Tue, 25 Feb 2025 03:20:27 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:02895093f637d5ffd45efa1963c19d8b79f6ec285c72d25e9e7f9ee78ef17d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6c15195292a90b4d03d2c962f3efafa5167ba6c5f56590dd4737eee60043f8`

```dockerfile
```

-	Layers:
	-	`sha256:7fcf577b99b4b64e23f663e9857c02482d2ab6329156a1033c1aa6712462e6f7`  
		Last Modified: Tue, 25 Feb 2025 03:20:28 GMT  
		Size: 6.4 MB (6424056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:283a7c01142a53fab5d8530d286b6e63807cc81f62005a56c12785b20c9a459c`  
		Last Modified: Tue, 25 Feb 2025 03:20:27 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:72d2157e20a796f9a5a7bcf70e76d2c475d5cd823be6699eff3a76fd03d7a749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148551078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b53e03051ca4cb2862def088af59a6e12b9beacef4dbbd4323216bc5f750b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b7bc1cadeb470200dfcf00359923782434145f653ef282933b6bfd1a14f8e1`  
		Last Modified: Tue, 25 Feb 2025 16:11:10 GMT  
		Size: 17.7 MB (17725528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3040f99c6489531530751f75cd87bb9c15b4a08bca39de42e280315706371487`  
		Last Modified: Tue, 25 Feb 2025 16:11:09 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a9bb98830ddd37b5d7310e0823febe76f8d4543dbc389e9482fbdb15252567`  
		Last Modified: Tue, 25 Feb 2025 16:12:04 GMT  
		Size: 64.7 MB (64682888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e683b8fdc05bfa49cc6f7297f4dd387281d5cf60dd582008d590f57fda5369`  
		Last Modified: Tue, 25 Feb 2025 16:12:02 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:3c902db54348fbfd405ccfca671a5ec0331b25b1466801c21420ba6af6c94f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6434016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4aef02ec57fc092aa024f35889eee14868d1fde9dc3a6edf6c4f43e2f3dea7e`

```dockerfile
```

-	Layers:
	-	`sha256:d89f2a401cf395b696c4591c15bc239ddc8dc85e0acdef5be42f4110c597ad93`  
		Last Modified: Tue, 25 Feb 2025 16:12:03 GMT  
		Size: 6.4 MB (6419460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8ba20a15b182362f5b640d2b58f183c7586f3388a86bc292f1d7ced6623367f`  
		Last Modified: Tue, 25 Feb 2025 16:12:02 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:10f79bfc29b90f9bfa20b20252338902675f158075a57625112eed368e77323d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153930870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba76c99baa6a64bb8deb694c2806f1f50f80dae8a00233eb692d3643ebe629bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bcf63b4ff6fa63b5e72af00ad5db4255c5aaa3771526590165a03d9354c295`  
		Last Modified: Tue, 25 Feb 2025 14:22:58 GMT  
		Size: 18.9 MB (18870670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5919f122039cdb24f3f65e32f513ff925f97caf4c5d1490e990644265653e9ca`  
		Last Modified: Tue, 25 Feb 2025 14:22:57 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e1dde60f84109d9aa4424ce096926d2e011808f5511d784fafd83ee8186569`  
		Last Modified: Tue, 25 Feb 2025 15:16:22 GMT  
		Size: 63.2 MB (63151521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9861bd5922e4910e94dd2097a9cac2d3cb44c9ce84c59e3ee175d981bcd28a9d`  
		Last Modified: Tue, 25 Feb 2025 15:16:20 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:5839e2b27cb5ddec947647d643d0b5194360ff72c7dc61aad1431add47deb6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6439312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c951dfa4ab0be13726c33c5181764d614b577df0d33f951f58cba681d0afff84`

```dockerfile
```

-	Layers:
	-	`sha256:5f0cba28eb8113c861a8e29b1383035a798efdd0ce1d088c16f097a324461139`  
		Last Modified: Tue, 25 Feb 2025 15:16:20 GMT  
		Size: 6.4 MB (6424732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d8f9f467cdd7eccd760d37c69341d913b8b6acd9d35f14cde3146ea9fed6868`  
		Last Modified: Tue, 25 Feb 2025 15:16:19 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32-alpine`

```console
$ docker pull telegraf@sha256:9613ea0126325721f7087013726dadd23bf0aff8caed38d9337c449cdb66f05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:3ad9fa3557eec07393d93ba99a10a803a1d358c08aee5b31f11927ed45248331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75899910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87127c7ae451c11d56da2e3bbdb0133e4fc5465199f4a064700dc7bc1b95f94d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb2f8452f18fa5ca6d6eab55873b03df9cb04ec2a5cbef0b0347252dd1f1b98`  
		Last Modified: Fri, 14 Feb 2025 19:27:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1849576e5bfb8707e5b6da1ed76fc1b4642590a5cd627cc954d4458c972b87`  
		Last Modified: Fri, 14 Feb 2025 19:27:08 GMT  
		Size: 2.4 MB (2447977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8976f17c93a72e5f006514ed0e2d593d5fa816d872152c28e428bea70d7a275`  
		Last Modified: Fri, 14 Feb 2025 19:27:10 GMT  
		Size: 69.8 MB (69824429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0c5ba34859540677e65faaa6f81da813c58e83b5870ad2c8611227ad0b1a0`  
		Last Modified: Fri, 14 Feb 2025 19:27:08 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6a788cf31b15ae6004a2eb7b8e1abe4b99d5f46318fabad2c75620283de0f097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1093716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9834368eb385832d1124281f968481309de1c0912c4bea4bad334e1ee56503`

```dockerfile
```

-	Layers:
	-	`sha256:36d17874c7c519d61791ce6538dcf5b70d8d316102b689fadc4fcbf715597e97`  
		Last Modified: Fri, 14 Feb 2025 19:27:08 GMT  
		Size: 1.1 MB (1078755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53875bd2d4d184394b04b7247846ef535add592138dcbbc0131261f51dd4b97`  
		Last Modified: Fri, 14 Feb 2025 19:27:07 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5c131e9d3dfd41b67fbe1efc79eade66effd3013805af278d26b9581ac0535eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69569876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7adaf8892bce40df4e537a256a91cdc51bfcdaf585b04cdc584cdded2e35ab2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61a5f488a07a5f9b377e1e8af47680d864b0a298fd6acfe930441fecb3ecf84`  
		Last Modified: Fri, 14 Feb 2025 23:51:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a777ce7d187cf232aae59fd07445827d4a146c69dd2ff0adb80ede2329896`  
		Last Modified: Sat, 15 Feb 2025 06:30:24 GMT  
		Size: 2.5 MB (2533889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd034834e7dc25546d11a5edde9078270a777c1002a13613255b26db02298a6`  
		Last Modified: Sat, 15 Feb 2025 06:30:57 GMT  
		Size: 62.9 MB (62944215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d8419ba9fcec72ee59593f2912c265a2f2650c283c863e9e30235da563b5f`  
		Last Modified: Sat, 15 Feb 2025 06:30:55 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e951a2565274dbce09494aac2324db6c6f4fe6b0940ca7528fc4c98c8023c85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33f51f8d0f3468d4c73164109a47998bc26ee6bb0739487e7e5c768a16499b1`

```dockerfile
```

-	Layers:
	-	`sha256:bb8efb89840ee2ef6a38b956f3d6cbdbf3e368f97c83314121ef06c9cc5b3a98`  
		Last Modified: Sat, 15 Feb 2025 06:30:55 GMT  
		Size: 1.1 MB (1074382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c6663ca7744f97d48d6c22ad8f29c6a45701e956bceefa937ea8e5eeab84f7b`  
		Last Modified: Sat, 15 Feb 2025 06:30:55 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32.3`

```console
$ docker pull telegraf@sha256:781d56e8ef2218f02d10545d526eb2341555adfd7ed9cda73c681155d735591d
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
$ docker pull telegraf@sha256:7e9c741c66e6c36a994bf59d20925a49c8fac4b4e659c0c26c8041957e9c1c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161506224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c680864557b2b3972e26ee25fe9d70fea1d337c7cf919f763a276c784b5e658`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cdbcd7a3b8e2113a68c04122c987b8e1356fbd1c5409cd84925418c4f71d81`  
		Last Modified: Tue, 25 Feb 2025 03:20:28 GMT  
		Size: 18.9 MB (18948113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39d45b98f2b3b33c43cced7e334f1a56d5e404525bcbd2a1c732d4ae1f23bc6`  
		Last Modified: Tue, 25 Feb 2025 03:20:27 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f69f009be6ba57b0997fba811ee12b698781b508b0773400015f58bac34cfae`  
		Last Modified: Tue, 25 Feb 2025 03:20:28 GMT  
		Size: 70.0 MB (70021086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9d26b56568dacd6cc96c42fbac1cb9c41aa17a7ef42e1cdf49e745176cdbd5`  
		Last Modified: Tue, 25 Feb 2025 03:20:27 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:02895093f637d5ffd45efa1963c19d8b79f6ec285c72d25e9e7f9ee78ef17d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6c15195292a90b4d03d2c962f3efafa5167ba6c5f56590dd4737eee60043f8`

```dockerfile
```

-	Layers:
	-	`sha256:7fcf577b99b4b64e23f663e9857c02482d2ab6329156a1033c1aa6712462e6f7`  
		Last Modified: Tue, 25 Feb 2025 03:20:28 GMT  
		Size: 6.4 MB (6424056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:283a7c01142a53fab5d8530d286b6e63807cc81f62005a56c12785b20c9a459c`  
		Last Modified: Tue, 25 Feb 2025 03:20:27 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:72d2157e20a796f9a5a7bcf70e76d2c475d5cd823be6699eff3a76fd03d7a749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148551078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b53e03051ca4cb2862def088af59a6e12b9beacef4dbbd4323216bc5f750b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b7bc1cadeb470200dfcf00359923782434145f653ef282933b6bfd1a14f8e1`  
		Last Modified: Tue, 25 Feb 2025 16:11:10 GMT  
		Size: 17.7 MB (17725528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3040f99c6489531530751f75cd87bb9c15b4a08bca39de42e280315706371487`  
		Last Modified: Tue, 25 Feb 2025 16:11:09 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a9bb98830ddd37b5d7310e0823febe76f8d4543dbc389e9482fbdb15252567`  
		Last Modified: Tue, 25 Feb 2025 16:12:04 GMT  
		Size: 64.7 MB (64682888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e683b8fdc05bfa49cc6f7297f4dd387281d5cf60dd582008d590f57fda5369`  
		Last Modified: Tue, 25 Feb 2025 16:12:02 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:3c902db54348fbfd405ccfca671a5ec0331b25b1466801c21420ba6af6c94f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6434016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4aef02ec57fc092aa024f35889eee14868d1fde9dc3a6edf6c4f43e2f3dea7e`

```dockerfile
```

-	Layers:
	-	`sha256:d89f2a401cf395b696c4591c15bc239ddc8dc85e0acdef5be42f4110c597ad93`  
		Last Modified: Tue, 25 Feb 2025 16:12:03 GMT  
		Size: 6.4 MB (6419460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8ba20a15b182362f5b640d2b58f183c7586f3388a86bc292f1d7ced6623367f`  
		Last Modified: Tue, 25 Feb 2025 16:12:02 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:10f79bfc29b90f9bfa20b20252338902675f158075a57625112eed368e77323d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153930870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba76c99baa6a64bb8deb694c2806f1f50f80dae8a00233eb692d3643ebe629bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bcf63b4ff6fa63b5e72af00ad5db4255c5aaa3771526590165a03d9354c295`  
		Last Modified: Tue, 25 Feb 2025 14:22:58 GMT  
		Size: 18.9 MB (18870670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5919f122039cdb24f3f65e32f513ff925f97caf4c5d1490e990644265653e9ca`  
		Last Modified: Tue, 25 Feb 2025 14:22:57 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e1dde60f84109d9aa4424ce096926d2e011808f5511d784fafd83ee8186569`  
		Last Modified: Tue, 25 Feb 2025 15:16:22 GMT  
		Size: 63.2 MB (63151521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9861bd5922e4910e94dd2097a9cac2d3cb44c9ce84c59e3ee175d981bcd28a9d`  
		Last Modified: Tue, 25 Feb 2025 15:16:20 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:5839e2b27cb5ddec947647d643d0b5194360ff72c7dc61aad1431add47deb6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6439312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c951dfa4ab0be13726c33c5181764d614b577df0d33f951f58cba681d0afff84`

```dockerfile
```

-	Layers:
	-	`sha256:5f0cba28eb8113c861a8e29b1383035a798efdd0ce1d088c16f097a324461139`  
		Last Modified: Tue, 25 Feb 2025 15:16:20 GMT  
		Size: 6.4 MB (6424732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d8f9f467cdd7eccd760d37c69341d913b8b6acd9d35f14cde3146ea9fed6868`  
		Last Modified: Tue, 25 Feb 2025 15:16:19 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32.3-alpine`

```console
$ docker pull telegraf@sha256:9613ea0126325721f7087013726dadd23bf0aff8caed38d9337c449cdb66f05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:3ad9fa3557eec07393d93ba99a10a803a1d358c08aee5b31f11927ed45248331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75899910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87127c7ae451c11d56da2e3bbdb0133e4fc5465199f4a064700dc7bc1b95f94d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb2f8452f18fa5ca6d6eab55873b03df9cb04ec2a5cbef0b0347252dd1f1b98`  
		Last Modified: Fri, 14 Feb 2025 19:27:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1849576e5bfb8707e5b6da1ed76fc1b4642590a5cd627cc954d4458c972b87`  
		Last Modified: Fri, 14 Feb 2025 19:27:08 GMT  
		Size: 2.4 MB (2447977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8976f17c93a72e5f006514ed0e2d593d5fa816d872152c28e428bea70d7a275`  
		Last Modified: Fri, 14 Feb 2025 19:27:10 GMT  
		Size: 69.8 MB (69824429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0c5ba34859540677e65faaa6f81da813c58e83b5870ad2c8611227ad0b1a0`  
		Last Modified: Fri, 14 Feb 2025 19:27:08 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6a788cf31b15ae6004a2eb7b8e1abe4b99d5f46318fabad2c75620283de0f097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1093716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9834368eb385832d1124281f968481309de1c0912c4bea4bad334e1ee56503`

```dockerfile
```

-	Layers:
	-	`sha256:36d17874c7c519d61791ce6538dcf5b70d8d316102b689fadc4fcbf715597e97`  
		Last Modified: Fri, 14 Feb 2025 19:27:08 GMT  
		Size: 1.1 MB (1078755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53875bd2d4d184394b04b7247846ef535add592138dcbbc0131261f51dd4b97`  
		Last Modified: Fri, 14 Feb 2025 19:27:07 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5c131e9d3dfd41b67fbe1efc79eade66effd3013805af278d26b9581ac0535eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69569876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7adaf8892bce40df4e537a256a91cdc51bfcdaf585b04cdc584cdded2e35ab2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61a5f488a07a5f9b377e1e8af47680d864b0a298fd6acfe930441fecb3ecf84`  
		Last Modified: Fri, 14 Feb 2025 23:51:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a777ce7d187cf232aae59fd07445827d4a146c69dd2ff0adb80ede2329896`  
		Last Modified: Sat, 15 Feb 2025 06:30:24 GMT  
		Size: 2.5 MB (2533889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd034834e7dc25546d11a5edde9078270a777c1002a13613255b26db02298a6`  
		Last Modified: Sat, 15 Feb 2025 06:30:57 GMT  
		Size: 62.9 MB (62944215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d8419ba9fcec72ee59593f2912c265a2f2650c283c863e9e30235da563b5f`  
		Last Modified: Sat, 15 Feb 2025 06:30:55 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e951a2565274dbce09494aac2324db6c6f4fe6b0940ca7528fc4c98c8023c85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33f51f8d0f3468d4c73164109a47998bc26ee6bb0739487e7e5c768a16499b1`

```dockerfile
```

-	Layers:
	-	`sha256:bb8efb89840ee2ef6a38b956f3d6cbdbf3e368f97c83314121ef06c9cc5b3a98`  
		Last Modified: Sat, 15 Feb 2025 06:30:55 GMT  
		Size: 1.1 MB (1074382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c6663ca7744f97d48d6c22ad8f29c6a45701e956bceefa937ea8e5eeab84f7b`  
		Last Modified: Sat, 15 Feb 2025 06:30:55 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33`

```console
$ docker pull telegraf@sha256:c8dfb65adbfbd9bb3b911f8fb8a85140c72a22e602104d9dbd970d350450ee3b
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
$ docker pull telegraf@sha256:f35103d787b9fa0672f45756bf60f4e5826bb76c7ec1e18440d73d92d3091540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168795051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7497718ee4e266c68ff7b9a793da3b6eabf63961e3552429d7deab401b6f55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Tue, 25 Feb 2025 19:20:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e79a86ea52306a9d84647da7fc1e0d035ce2d06beb89e92efbbf45bea00ce3`  
		Last Modified: Tue, 25 Feb 2025 23:27:42 GMT  
		Size: 18.9 MB (18948056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f2201cb606567ba4abddee6420ff339f502222976b582bb82ddfc6905f9f9b`  
		Last Modified: Tue, 25 Feb 2025 23:27:42 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d732aebd54f1edc5efef6869e6184f714ef16ebbc12045d81c632abd5de0032a`  
		Last Modified: Tue, 25 Feb 2025 23:27:44 GMT  
		Size: 77.3 MB (77309955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb2df4207ca81e6d28ad25c7e9c9dfd9494fbe7b457df3483dbbe24d9fd4cd3`  
		Last Modified: Tue, 25 Feb 2025 23:27:42 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:15417c9f8231c8a547d60d3b24ff5d65213b9a66d20258a59d4da5db12b9e47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6454849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bf4b1443a51ef69c19bfdd861c1f733f1b97b81531b0ddf14d997eb1555ec0`

```dockerfile
```

-	Layers:
	-	`sha256:84686085ed4f018a12fe1ebe7f08170aa05a329d9ab1689b0606bb3a828788c2`  
		Last Modified: Tue, 25 Feb 2025 23:27:42 GMT  
		Size: 6.4 MB (6440077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e30e010b7a4bbc1116f3a047c8905f90940610150fac82758a7deb02ec80a4ea`  
		Last Modified: Tue, 25 Feb 2025 23:27:42 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:f35303945f1d2ae0fdd2b442655cd606fe2f8dd5f32e652ffb2fbcd549bc795a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154944053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f7aadd15cafaf1fc05df7e2d14cc47868e9ba8591e5c4a4ccb691ded06aef8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Tue, 25 Feb 2025 19:20:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b7bc1cadeb470200dfcf00359923782434145f653ef282933b6bfd1a14f8e1`  
		Last Modified: Tue, 25 Feb 2025 16:11:10 GMT  
		Size: 17.7 MB (17725528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3040f99c6489531530751f75cd87bb9c15b4a08bca39de42e280315706371487`  
		Last Modified: Tue, 25 Feb 2025 16:11:09 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5fa8d37d57b797cfd5febd0696f499b062a2abe42931e1c281787ac4e92e77`  
		Last Modified: Wed, 26 Feb 2025 03:45:42 GMT  
		Size: 71.1 MB (71075866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c12d6acf19d7766b58466c1e8af0a3583c7ef40db8fa6d2d321debfceaa93e`  
		Last Modified: Wed, 26 Feb 2025 03:45:40 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:cd4881a2af76f56611fcdc717770c10dfc2c3b1c0bb8aa51f9199b444a1edf5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6450355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225244887d5d4f45d29f7695221b3e624855a0260bbf4cc0df7db458bdc32a1a`

```dockerfile
```

-	Layers:
	-	`sha256:e46b39bbd40f35d8d4467b17da843343deb51976c0361d46f91c78be70e55d4a`  
		Last Modified: Wed, 26 Feb 2025 03:45:40 GMT  
		Size: 6.4 MB (6435489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f96b9ab1263b74a458fbf865446e43e73d3111864acc2681a200031fcb3b3e5`  
		Last Modified: Wed, 26 Feb 2025 03:45:39 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4dc19ed2f25e8998e98d60ce1f20349a03b7231222b3d9465ccf11edb31b9a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160379072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415aef95178dafe87ec0b3724b189d5412c3205692239f460ca57c64df8f30a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Tue, 25 Feb 2025 19:20:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bcf63b4ff6fa63b5e72af00ad5db4255c5aaa3771526590165a03d9354c295`  
		Last Modified: Tue, 25 Feb 2025 14:22:58 GMT  
		Size: 18.9 MB (18870670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5919f122039cdb24f3f65e32f513ff925f97caf4c5d1490e990644265653e9ca`  
		Last Modified: Tue, 25 Feb 2025 14:22:57 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833d4b908494fa6e4d36c02ca7f63611fdf724ba1b033e6082b95275e37b138e`  
		Last Modified: Wed, 26 Feb 2025 00:00:47 GMT  
		Size: 69.6 MB (69599724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad74673ccf1bc53f01f6329eb514e252a6a749aecedd0b590ecc7e4f6194871`  
		Last Modified: Wed, 26 Feb 2025 00:00:43 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:2be48907660010e73fe7d1f0baa614487c1b3b38aaff681d4b4b11b7355f7fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6455659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce6177c55209963087e477c84eb2aae16bc1755fa7e23a186ef281081730db7`

```dockerfile
```

-	Layers:
	-	`sha256:13ff4276376b551ab842fd4934f1cf13dee981f42938023a30b2ce71cd8a2560`  
		Last Modified: Wed, 26 Feb 2025 00:00:44 GMT  
		Size: 6.4 MB (6440765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62827200218aadcf3b902882a3bcd719e09264ce9217fb5ed837a8068048e305`  
		Last Modified: Wed, 26 Feb 2025 00:00:43 GMT  
		Size: 14.9 KB (14894 bytes)  
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
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38049afbf35aebc48750aa922431b39f2fc798c04bdbe76bd6ae3b281fed2ba5`  
		Last Modified: Tue, 25 Feb 2025 23:27:37 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073bd82841c579643840dc44375728fdc6290a0b75a5c7c7a9f475e2fd33df5c`  
		Last Modified: Tue, 25 Feb 2025 23:27:37 GMT  
		Size: 2.4 MB (2448010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804d0c3c2f1304b11b15aa3615c2ae951b7aa267345cd8caebf2534c09f432c4`  
		Last Modified: Tue, 25 Feb 2025 23:27:38 GMT  
		Size: 77.1 MB (77105828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecb0ae4356bd231d8a07dbc4b04fad1e156e8bcf1f303290303cee493817e28`  
		Last Modified: Tue, 25 Feb 2025 23:27:37 GMT  
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
		Last Modified: Tue, 25 Feb 2025 23:27:37 GMT  
		Size: 1.1 MB (1094776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b15e5bf904084afce0335a323cb7a49eb0e277254fb8c1ce8618e0518df0650`  
		Last Modified: Tue, 25 Feb 2025 23:27:36 GMT  
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
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61a5f488a07a5f9b377e1e8af47680d864b0a298fd6acfe930441fecb3ecf84`  
		Last Modified: Fri, 14 Feb 2025 23:51:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a777ce7d187cf232aae59fd07445827d4a146c69dd2ff0adb80ede2329896`  
		Last Modified: Sat, 15 Feb 2025 06:30:24 GMT  
		Size: 2.5 MB (2533889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb755c12ce2b641e186784c9d65629a9e336edd2adbfc1769a50ca60cc9d39c7`  
		Last Modified: Wed, 26 Feb 2025 00:01:21 GMT  
		Size: 69.4 MB (69395470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cb2567b59e86792e2fb28a415d81a683488ae3254f26baf29d93ab79827052`  
		Last Modified: Wed, 26 Feb 2025 00:01:19 GMT  
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
		Last Modified: Wed, 26 Feb 2025 00:01:19 GMT  
		Size: 1.1 MB (1090415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5040171f06da0c2a54629d1c7e68fd289af078d85e7686d7a27924345d07e654`  
		Last Modified: Wed, 26 Feb 2025 00:01:19 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33.3`

```console
$ docker pull telegraf@sha256:c8dfb65adbfbd9bb3b911f8fb8a85140c72a22e602104d9dbd970d350450ee3b
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
$ docker pull telegraf@sha256:f35103d787b9fa0672f45756bf60f4e5826bb76c7ec1e18440d73d92d3091540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168795051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7497718ee4e266c68ff7b9a793da3b6eabf63961e3552429d7deab401b6f55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Tue, 25 Feb 2025 19:20:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e79a86ea52306a9d84647da7fc1e0d035ce2d06beb89e92efbbf45bea00ce3`  
		Last Modified: Tue, 25 Feb 2025 23:27:42 GMT  
		Size: 18.9 MB (18948056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f2201cb606567ba4abddee6420ff339f502222976b582bb82ddfc6905f9f9b`  
		Last Modified: Tue, 25 Feb 2025 23:27:42 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d732aebd54f1edc5efef6869e6184f714ef16ebbc12045d81c632abd5de0032a`  
		Last Modified: Tue, 25 Feb 2025 23:27:44 GMT  
		Size: 77.3 MB (77309955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb2df4207ca81e6d28ad25c7e9c9dfd9494fbe7b457df3483dbbe24d9fd4cd3`  
		Last Modified: Tue, 25 Feb 2025 23:27:42 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:15417c9f8231c8a547d60d3b24ff5d65213b9a66d20258a59d4da5db12b9e47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6454849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bf4b1443a51ef69c19bfdd861c1f733f1b97b81531b0ddf14d997eb1555ec0`

```dockerfile
```

-	Layers:
	-	`sha256:84686085ed4f018a12fe1ebe7f08170aa05a329d9ab1689b0606bb3a828788c2`  
		Last Modified: Tue, 25 Feb 2025 23:27:42 GMT  
		Size: 6.4 MB (6440077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e30e010b7a4bbc1116f3a047c8905f90940610150fac82758a7deb02ec80a4ea`  
		Last Modified: Tue, 25 Feb 2025 23:27:42 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:f35303945f1d2ae0fdd2b442655cd606fe2f8dd5f32e652ffb2fbcd549bc795a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154944053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f7aadd15cafaf1fc05df7e2d14cc47868e9ba8591e5c4a4ccb691ded06aef8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Tue, 25 Feb 2025 19:20:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b7bc1cadeb470200dfcf00359923782434145f653ef282933b6bfd1a14f8e1`  
		Last Modified: Tue, 25 Feb 2025 16:11:10 GMT  
		Size: 17.7 MB (17725528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3040f99c6489531530751f75cd87bb9c15b4a08bca39de42e280315706371487`  
		Last Modified: Tue, 25 Feb 2025 16:11:09 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5fa8d37d57b797cfd5febd0696f499b062a2abe42931e1c281787ac4e92e77`  
		Last Modified: Wed, 26 Feb 2025 03:45:42 GMT  
		Size: 71.1 MB (71075866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c12d6acf19d7766b58466c1e8af0a3583c7ef40db8fa6d2d321debfceaa93e`  
		Last Modified: Wed, 26 Feb 2025 03:45:40 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:cd4881a2af76f56611fcdc717770c10dfc2c3b1c0bb8aa51f9199b444a1edf5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6450355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225244887d5d4f45d29f7695221b3e624855a0260bbf4cc0df7db458bdc32a1a`

```dockerfile
```

-	Layers:
	-	`sha256:e46b39bbd40f35d8d4467b17da843343deb51976c0361d46f91c78be70e55d4a`  
		Last Modified: Wed, 26 Feb 2025 03:45:40 GMT  
		Size: 6.4 MB (6435489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f96b9ab1263b74a458fbf865446e43e73d3111864acc2681a200031fcb3b3e5`  
		Last Modified: Wed, 26 Feb 2025 03:45:39 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4dc19ed2f25e8998e98d60ce1f20349a03b7231222b3d9465ccf11edb31b9a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160379072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415aef95178dafe87ec0b3724b189d5412c3205692239f460ca57c64df8f30a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Tue, 25 Feb 2025 19:20:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bcf63b4ff6fa63b5e72af00ad5db4255c5aaa3771526590165a03d9354c295`  
		Last Modified: Tue, 25 Feb 2025 14:22:58 GMT  
		Size: 18.9 MB (18870670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5919f122039cdb24f3f65e32f513ff925f97caf4c5d1490e990644265653e9ca`  
		Last Modified: Tue, 25 Feb 2025 14:22:57 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833d4b908494fa6e4d36c02ca7f63611fdf724ba1b033e6082b95275e37b138e`  
		Last Modified: Wed, 26 Feb 2025 00:00:47 GMT  
		Size: 69.6 MB (69599724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad74673ccf1bc53f01f6329eb514e252a6a749aecedd0b590ecc7e4f6194871`  
		Last Modified: Wed, 26 Feb 2025 00:00:43 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:2be48907660010e73fe7d1f0baa614487c1b3b38aaff681d4b4b11b7355f7fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6455659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce6177c55209963087e477c84eb2aae16bc1755fa7e23a186ef281081730db7`

```dockerfile
```

-	Layers:
	-	`sha256:13ff4276376b551ab842fd4934f1cf13dee981f42938023a30b2ce71cd8a2560`  
		Last Modified: Wed, 26 Feb 2025 00:00:44 GMT  
		Size: 6.4 MB (6440765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62827200218aadcf3b902882a3bcd719e09264ce9217fb5ed837a8068048e305`  
		Last Modified: Wed, 26 Feb 2025 00:00:43 GMT  
		Size: 14.9 KB (14894 bytes)  
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
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38049afbf35aebc48750aa922431b39f2fc798c04bdbe76bd6ae3b281fed2ba5`  
		Last Modified: Tue, 25 Feb 2025 23:27:37 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073bd82841c579643840dc44375728fdc6290a0b75a5c7c7a9f475e2fd33df5c`  
		Last Modified: Tue, 25 Feb 2025 23:27:37 GMT  
		Size: 2.4 MB (2448010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804d0c3c2f1304b11b15aa3615c2ae951b7aa267345cd8caebf2534c09f432c4`  
		Last Modified: Tue, 25 Feb 2025 23:27:38 GMT  
		Size: 77.1 MB (77105828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecb0ae4356bd231d8a07dbc4b04fad1e156e8bcf1f303290303cee493817e28`  
		Last Modified: Tue, 25 Feb 2025 23:27:37 GMT  
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
		Last Modified: Tue, 25 Feb 2025 23:27:37 GMT  
		Size: 1.1 MB (1094776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b15e5bf904084afce0335a323cb7a49eb0e277254fb8c1ce8618e0518df0650`  
		Last Modified: Tue, 25 Feb 2025 23:27:36 GMT  
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
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61a5f488a07a5f9b377e1e8af47680d864b0a298fd6acfe930441fecb3ecf84`  
		Last Modified: Fri, 14 Feb 2025 23:51:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a777ce7d187cf232aae59fd07445827d4a146c69dd2ff0adb80ede2329896`  
		Last Modified: Sat, 15 Feb 2025 06:30:24 GMT  
		Size: 2.5 MB (2533889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb755c12ce2b641e186784c9d65629a9e336edd2adbfc1769a50ca60cc9d39c7`  
		Last Modified: Wed, 26 Feb 2025 00:01:21 GMT  
		Size: 69.4 MB (69395470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cb2567b59e86792e2fb28a415d81a683488ae3254f26baf29d93ab79827052`  
		Last Modified: Wed, 26 Feb 2025 00:01:19 GMT  
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
		Last Modified: Wed, 26 Feb 2025 00:01:19 GMT  
		Size: 1.1 MB (1090415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5040171f06da0c2a54629d1c7e68fd289af078d85e7686d7a27924345d07e654`  
		Last Modified: Wed, 26 Feb 2025 00:01:19 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34`

```console
$ docker pull telegraf@sha256:5c1ae2187f43d6039196a12b7dd9960b2dbd80d996036894d0da3e4ca692885d
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
$ docker pull telegraf@sha256:cb299a37099f8f95b141ea396908c5b16bd52e38729155ba59ea6359a3bc89c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169126885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5f4bc952b642a35b619e206e213610d0a3bce93b450dc2721c23bbf1999d72`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENV TELEGRAF_VERSION=1.34.0
# Mon, 10 Mar 2025 21:51:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Mar 2025 21:51:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69e4b7262125d8685828f509e3e3c515efe312fad22f714266b281e478c7c91`  
		Last Modified: Mon, 10 Mar 2025 23:11:08 GMT  
		Size: 18.9 MB (18947976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb4eab3359f09de90e8408a05d256043914eab395db866aae36fb223310e160`  
		Last Modified: Mon, 10 Mar 2025 23:11:07 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f985cea1a4bb53787e358aa13c7ae12c14d50925d92e8510649b8a01faae7221`  
		Last Modified: Mon, 10 Mar 2025 23:11:10 GMT  
		Size: 77.6 MB (77641870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ae58584ec414068223a394c3539b5e89ad93f923aed38584cddeaae7289e19`  
		Last Modified: Mon, 10 Mar 2025 23:11:07 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:ee51d7a840ee7a74ea1ea05ac739e886a802548f7414487391a12937791a0671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6459443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee22901449a88ceefc6e46f53b36fdc80776c5790e3bc9301e122d75732c6024`

```dockerfile
```

-	Layers:
	-	`sha256:fc6eb5d591df55cf03a92bb16b33704a917b52ab69bf8284809f5e75297b1983`  
		Last Modified: Mon, 10 Mar 2025 23:11:08 GMT  
		Size: 6.4 MB (6444671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b21ef6d9228a75be92ecdd1d98fda168fdb33fb34bfc7654b3c701fec23a196b`  
		Last Modified: Mon, 10 Mar 2025 23:11:07 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:6f06caf71de92725a9e971fc9ff82e6f7919c76d33ad43be8af62a3c99e12ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155247864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee00484a53b75ca25dd0a4508f1bf82df345e4b3546be3e174f841096c95c04`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENV TELEGRAF_VERSION=1.34.0
# Mon, 10 Mar 2025 21:51:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Mar 2025 21:51:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b7bc1cadeb470200dfcf00359923782434145f653ef282933b6bfd1a14f8e1`  
		Last Modified: Tue, 25 Feb 2025 16:11:10 GMT  
		Size: 17.7 MB (17725528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3040f99c6489531530751f75cd87bb9c15b4a08bca39de42e280315706371487`  
		Last Modified: Tue, 25 Feb 2025 16:11:09 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e0c411d25868143a86b3e9c07847948da1a6c91d61b5a97ff12a6d6d171467`  
		Last Modified: Mon, 10 Mar 2025 23:10:30 GMT  
		Size: 71.4 MB (71379675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e730494c4399b5e22144e2bb2178332f2fa433aecaab3821295752164bd83176`  
		Last Modified: Mon, 10 Mar 2025 23:10:27 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:6d40e7d92e06774d26e00050985b466f1917012576cc91e7237b04e723b22967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6454949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0239cc8a4bffd542a3cc9ec391aecdb98e65e18afbf37fc069c5ae898f549ac0`

```dockerfile
```

-	Layers:
	-	`sha256:1d15c754a5d42d55283cb1d3bcbe56bf61b881d25066fe7fba8353f7b5ed0a8a`  
		Last Modified: Mon, 10 Mar 2025 23:10:28 GMT  
		Size: 6.4 MB (6440083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce92eb1382e9d9764d43c95d5c2c182af347791cbeed2ddc606ad84858c11102`  
		Last Modified: Mon, 10 Mar 2025 23:10:27 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:9758ef94a906d1c9d9430eb7afd7ff2ba74659e628292ddfb5b0c0cd7caca8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160673152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a2aa193dac21d389b4003208f7487c835ada8f825e442860234c82cd83fc73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENV TELEGRAF_VERSION=1.34.0
# Mon, 10 Mar 2025 21:51:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Mar 2025 21:51:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3c814be53f34ab64fcffafa3cce7c0113e3307f946247a7db09eb0a5ca0b4e`  
		Last Modified: Mon, 10 Mar 2025 23:10:28 GMT  
		Size: 18.9 MB (18870942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c837fce1617eb619a65ab4ad1862ce7eb84fca2ed2dfe2547bba688e94e69ff9`  
		Last Modified: Mon, 10 Mar 2025 23:10:26 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ab3d010401bb84dc9b8828047533299db58996caf5dba011bda609de1c63d0`  
		Last Modified: Mon, 10 Mar 2025 23:10:29 GMT  
		Size: 69.9 MB (69893520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5359e3548b02051e7d46bf4cf58bc6700caedfc4507619114a3ffc13a584c346`  
		Last Modified: Mon, 10 Mar 2025 23:10:27 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:2b47a480857e23e1aa81670b8f9817e7be30891862ab62f0bafb5b0dcfcb2d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6460252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a181ff33b151c62a03b1c16adf16db4e231e85017faa61d74c6193e723d0a86`

```dockerfile
```

-	Layers:
	-	`sha256:eee69b6677f78e6997ec2eecb9b1bc6c5e4b5d411545c07cdb44668c2fbd9ade`  
		Last Modified: Mon, 10 Mar 2025 23:10:27 GMT  
		Size: 6.4 MB (6445359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfb7865e46688a1f92abb77a79a51a3aa59c7520661b162d6967ed8e5896e83c`  
		Last Modified: Mon, 10 Mar 2025 23:10:26 GMT  
		Size: 14.9 KB (14893 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34-alpine`

```console
$ docker pull telegraf@sha256:c6fbec5afe347a6cf6753fa34701e5ddc4c360a605e45686b445521905a138ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:940cee6ce1142dce08812a3862cc4c5745e9497e2eb407cd6645c53b5e44a4cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83517659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54ec71e13f4738a55e28e1ef085d9bb497098bc269cb3645c2b5db7ca374ab5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENV TELEGRAF_VERSION=1.34.0
# Mon, 10 Mar 2025 21:51:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Mar 2025 21:51:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1019a8e545d1b563b6c9aa75a0304412ae8778e307a3a85df8a782599a39586`  
		Last Modified: Mon, 10 Mar 2025 23:10:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01e0f49d959a083d8e673e69502a774a3330febfbd8af17a94de1addd138b96`  
		Last Modified: Mon, 10 Mar 2025 23:10:57 GMT  
		Size: 2.4 MB (2448015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c98ddf18fb95a841228184ec2f11b22e6044f2b0a3243edb31f4d35bd20568d`  
		Last Modified: Mon, 10 Mar 2025 23:11:01 GMT  
		Size: 77.4 MB (77442139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1542b15ab2c9e33cf73b29c6e07c36a36116ace9c60b6e0a9cc60e04976f40`  
		Last Modified: Mon, 10 Mar 2025 23:10:57 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:1fd1309ae2efab92cae2434af6d2c58541bf04916ab4507699125a2214ed7b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1114633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53be4a655a24ecb1dba3f27582591f7b2af503ce37909e52f351daefffc9d704`

```dockerfile
```

-	Layers:
	-	`sha256:e1c19eec0f7bb8613936d0202d7f5a327bb6088f92d22423d3c2d5ff3e1153b5`  
		Last Modified: Mon, 10 Mar 2025 23:10:57 GMT  
		Size: 1.1 MB (1099370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7d6816b7155ce85b4fd3d7090122a729edcf997dfd5811a0da6f9efb5eb842`  
		Last Modified: Mon, 10 Mar 2025 23:10:57 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:66f341f3d9c3a9ed063f589d97031bfcbb352b0b7bbcacc1566df33672e8d468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76308949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf5fed543e27d83c18311052a57b5fb1d3326d209325a28a1f9c6b4233bc6ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENV TELEGRAF_VERSION=1.34.0
# Mon, 10 Mar 2025 21:51:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Mar 2025 21:51:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762a8644aed736cbf4c123385c72d805586043830867b764844d918e74198748`  
		Last Modified: Mon, 10 Mar 2025 23:11:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eb2ac6e1bddedd29dec17c8c60b881e71180e9057717b8bedd88a5ddf29dff`  
		Last Modified: Mon, 10 Mar 2025 23:11:02 GMT  
		Size: 2.5 MB (2533888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20701fd7f7a969a1bb9baed0533147a4628e6b1e40e06cc6766a8c24bbb4d7ed`  
		Last Modified: Mon, 10 Mar 2025 23:11:04 GMT  
		Size: 69.7 MB (69683288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8a78f405bde17beaef6b5427477777ec46ef79f448a34a5696059ea9640d53`  
		Last Modified: Mon, 10 Mar 2025 23:11:01 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d28fc275fc1644b0c1ced6d75ab3a8cc29421bcdc61078be517d7f594dd623f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1110394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b056bb10daf2d2da12f3331ed098a4815715ac4bd65fbae4b8dcd59ee35d37`

```dockerfile
```

-	Layers:
	-	`sha256:c4e80edcb5ee8ddfb281a98ae137fdbbfd549dd05f4446a03756b9153a9cd647`  
		Last Modified: Mon, 10 Mar 2025 23:11:02 GMT  
		Size: 1.1 MB (1095009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e30c7e59efcf50a5d390853fa8e19f748b27cede182f74e6748210d6a8f5d49`  
		Last Modified: Mon, 10 Mar 2025 23:11:01 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34.0`

```console
$ docker pull telegraf@sha256:5c1ae2187f43d6039196a12b7dd9960b2dbd80d996036894d0da3e4ca692885d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34.0` - linux; amd64

```console
$ docker pull telegraf@sha256:cb299a37099f8f95b141ea396908c5b16bd52e38729155ba59ea6359a3bc89c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169126885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5f4bc952b642a35b619e206e213610d0a3bce93b450dc2721c23bbf1999d72`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENV TELEGRAF_VERSION=1.34.0
# Mon, 10 Mar 2025 21:51:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Mar 2025 21:51:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69e4b7262125d8685828f509e3e3c515efe312fad22f714266b281e478c7c91`  
		Last Modified: Mon, 10 Mar 2025 23:11:08 GMT  
		Size: 18.9 MB (18947976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb4eab3359f09de90e8408a05d256043914eab395db866aae36fb223310e160`  
		Last Modified: Mon, 10 Mar 2025 23:11:07 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f985cea1a4bb53787e358aa13c7ae12c14d50925d92e8510649b8a01faae7221`  
		Last Modified: Mon, 10 Mar 2025 23:11:10 GMT  
		Size: 77.6 MB (77641870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ae58584ec414068223a394c3539b5e89ad93f923aed38584cddeaae7289e19`  
		Last Modified: Mon, 10 Mar 2025 23:11:07 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.0` - unknown; unknown

```console
$ docker pull telegraf@sha256:ee51d7a840ee7a74ea1ea05ac739e886a802548f7414487391a12937791a0671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6459443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee22901449a88ceefc6e46f53b36fdc80776c5790e3bc9301e122d75732c6024`

```dockerfile
```

-	Layers:
	-	`sha256:fc6eb5d591df55cf03a92bb16b33704a917b52ab69bf8284809f5e75297b1983`  
		Last Modified: Mon, 10 Mar 2025 23:11:08 GMT  
		Size: 6.4 MB (6444671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b21ef6d9228a75be92ecdd1d98fda168fdb33fb34bfc7654b3c701fec23a196b`  
		Last Modified: Mon, 10 Mar 2025 23:11:07 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.0` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:6f06caf71de92725a9e971fc9ff82e6f7919c76d33ad43be8af62a3c99e12ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155247864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee00484a53b75ca25dd0a4508f1bf82df345e4b3546be3e174f841096c95c04`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENV TELEGRAF_VERSION=1.34.0
# Mon, 10 Mar 2025 21:51:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Mar 2025 21:51:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b7bc1cadeb470200dfcf00359923782434145f653ef282933b6bfd1a14f8e1`  
		Last Modified: Tue, 25 Feb 2025 16:11:10 GMT  
		Size: 17.7 MB (17725528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3040f99c6489531530751f75cd87bb9c15b4a08bca39de42e280315706371487`  
		Last Modified: Tue, 25 Feb 2025 16:11:09 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e0c411d25868143a86b3e9c07847948da1a6c91d61b5a97ff12a6d6d171467`  
		Last Modified: Mon, 10 Mar 2025 23:10:30 GMT  
		Size: 71.4 MB (71379675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e730494c4399b5e22144e2bb2178332f2fa433aecaab3821295752164bd83176`  
		Last Modified: Mon, 10 Mar 2025 23:10:27 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.0` - unknown; unknown

```console
$ docker pull telegraf@sha256:6d40e7d92e06774d26e00050985b466f1917012576cc91e7237b04e723b22967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6454949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0239cc8a4bffd542a3cc9ec391aecdb98e65e18afbf37fc069c5ae898f549ac0`

```dockerfile
```

-	Layers:
	-	`sha256:1d15c754a5d42d55283cb1d3bcbe56bf61b881d25066fe7fba8353f7b5ed0a8a`  
		Last Modified: Mon, 10 Mar 2025 23:10:28 GMT  
		Size: 6.4 MB (6440083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce92eb1382e9d9764d43c95d5c2c182af347791cbeed2ddc606ad84858c11102`  
		Last Modified: Mon, 10 Mar 2025 23:10:27 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.0` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:9758ef94a906d1c9d9430eb7afd7ff2ba74659e628292ddfb5b0c0cd7caca8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160673152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a2aa193dac21d389b4003208f7487c835ada8f825e442860234c82cd83fc73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENV TELEGRAF_VERSION=1.34.0
# Mon, 10 Mar 2025 21:51:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Mar 2025 21:51:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3c814be53f34ab64fcffafa3cce7c0113e3307f946247a7db09eb0a5ca0b4e`  
		Last Modified: Mon, 10 Mar 2025 23:10:28 GMT  
		Size: 18.9 MB (18870942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c837fce1617eb619a65ab4ad1862ce7eb84fca2ed2dfe2547bba688e94e69ff9`  
		Last Modified: Mon, 10 Mar 2025 23:10:26 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ab3d010401bb84dc9b8828047533299db58996caf5dba011bda609de1c63d0`  
		Last Modified: Mon, 10 Mar 2025 23:10:29 GMT  
		Size: 69.9 MB (69893520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5359e3548b02051e7d46bf4cf58bc6700caedfc4507619114a3ffc13a584c346`  
		Last Modified: Mon, 10 Mar 2025 23:10:27 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.0` - unknown; unknown

```console
$ docker pull telegraf@sha256:2b47a480857e23e1aa81670b8f9817e7be30891862ab62f0bafb5b0dcfcb2d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6460252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a181ff33b151c62a03b1c16adf16db4e231e85017faa61d74c6193e723d0a86`

```dockerfile
```

-	Layers:
	-	`sha256:eee69b6677f78e6997ec2eecb9b1bc6c5e4b5d411545c07cdb44668c2fbd9ade`  
		Last Modified: Mon, 10 Mar 2025 23:10:27 GMT  
		Size: 6.4 MB (6445359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfb7865e46688a1f92abb77a79a51a3aa59c7520661b162d6967ed8e5896e83c`  
		Last Modified: Mon, 10 Mar 2025 23:10:26 GMT  
		Size: 14.9 KB (14893 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34.0-alpine`

```console
$ docker pull telegraf@sha256:c6fbec5afe347a6cf6753fa34701e5ddc4c360a605e45686b445521905a138ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34.0-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:940cee6ce1142dce08812a3862cc4c5745e9497e2eb407cd6645c53b5e44a4cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83517659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54ec71e13f4738a55e28e1ef085d9bb497098bc269cb3645c2b5db7ca374ab5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENV TELEGRAF_VERSION=1.34.0
# Mon, 10 Mar 2025 21:51:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Mar 2025 21:51:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1019a8e545d1b563b6c9aa75a0304412ae8778e307a3a85df8a782599a39586`  
		Last Modified: Mon, 10 Mar 2025 23:10:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01e0f49d959a083d8e673e69502a774a3330febfbd8af17a94de1addd138b96`  
		Last Modified: Mon, 10 Mar 2025 23:10:57 GMT  
		Size: 2.4 MB (2448015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c98ddf18fb95a841228184ec2f11b22e6044f2b0a3243edb31f4d35bd20568d`  
		Last Modified: Mon, 10 Mar 2025 23:11:01 GMT  
		Size: 77.4 MB (77442139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1542b15ab2c9e33cf73b29c6e07c36a36116ace9c60b6e0a9cc60e04976f40`  
		Last Modified: Mon, 10 Mar 2025 23:10:57 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.0-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:1fd1309ae2efab92cae2434af6d2c58541bf04916ab4507699125a2214ed7b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1114633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53be4a655a24ecb1dba3f27582591f7b2af503ce37909e52f351daefffc9d704`

```dockerfile
```

-	Layers:
	-	`sha256:e1c19eec0f7bb8613936d0202d7f5a327bb6088f92d22423d3c2d5ff3e1153b5`  
		Last Modified: Mon, 10 Mar 2025 23:10:57 GMT  
		Size: 1.1 MB (1099370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7d6816b7155ce85b4fd3d7090122a729edcf997dfd5811a0da6f9efb5eb842`  
		Last Modified: Mon, 10 Mar 2025 23:10:57 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.0-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:66f341f3d9c3a9ed063f589d97031bfcbb352b0b7bbcacc1566df33672e8d468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76308949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf5fed543e27d83c18311052a57b5fb1d3326d209325a28a1f9c6b4233bc6ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENV TELEGRAF_VERSION=1.34.0
# Mon, 10 Mar 2025 21:51:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Mar 2025 21:51:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762a8644aed736cbf4c123385c72d805586043830867b764844d918e74198748`  
		Last Modified: Mon, 10 Mar 2025 23:11:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eb2ac6e1bddedd29dec17c8c60b881e71180e9057717b8bedd88a5ddf29dff`  
		Last Modified: Mon, 10 Mar 2025 23:11:02 GMT  
		Size: 2.5 MB (2533888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20701fd7f7a969a1bb9baed0533147a4628e6b1e40e06cc6766a8c24bbb4d7ed`  
		Last Modified: Mon, 10 Mar 2025 23:11:04 GMT  
		Size: 69.7 MB (69683288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8a78f405bde17beaef6b5427477777ec46ef79f448a34a5696059ea9640d53`  
		Last Modified: Mon, 10 Mar 2025 23:11:01 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.0-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d28fc275fc1644b0c1ced6d75ab3a8cc29421bcdc61078be517d7f594dd623f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1110394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b056bb10daf2d2da12f3331ed098a4815715ac4bd65fbae4b8dcd59ee35d37`

```dockerfile
```

-	Layers:
	-	`sha256:c4e80edcb5ee8ddfb281a98ae137fdbbfd549dd05f4446a03756b9153a9cd647`  
		Last Modified: Mon, 10 Mar 2025 23:11:02 GMT  
		Size: 1.1 MB (1095009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e30c7e59efcf50a5d390853fa8e19f748b27cede182f74e6748210d6a8f5d49`  
		Last Modified: Mon, 10 Mar 2025 23:11:01 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:c6fbec5afe347a6cf6753fa34701e5ddc4c360a605e45686b445521905a138ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:940cee6ce1142dce08812a3862cc4c5745e9497e2eb407cd6645c53b5e44a4cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83517659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54ec71e13f4738a55e28e1ef085d9bb497098bc269cb3645c2b5db7ca374ab5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENV TELEGRAF_VERSION=1.34.0
# Mon, 10 Mar 2025 21:51:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Mar 2025 21:51:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1019a8e545d1b563b6c9aa75a0304412ae8778e307a3a85df8a782599a39586`  
		Last Modified: Mon, 10 Mar 2025 23:10:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01e0f49d959a083d8e673e69502a774a3330febfbd8af17a94de1addd138b96`  
		Last Modified: Mon, 10 Mar 2025 23:10:57 GMT  
		Size: 2.4 MB (2448015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c98ddf18fb95a841228184ec2f11b22e6044f2b0a3243edb31f4d35bd20568d`  
		Last Modified: Mon, 10 Mar 2025 23:11:01 GMT  
		Size: 77.4 MB (77442139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1542b15ab2c9e33cf73b29c6e07c36a36116ace9c60b6e0a9cc60e04976f40`  
		Last Modified: Mon, 10 Mar 2025 23:10:57 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:1fd1309ae2efab92cae2434af6d2c58541bf04916ab4507699125a2214ed7b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1114633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53be4a655a24ecb1dba3f27582591f7b2af503ce37909e52f351daefffc9d704`

```dockerfile
```

-	Layers:
	-	`sha256:e1c19eec0f7bb8613936d0202d7f5a327bb6088f92d22423d3c2d5ff3e1153b5`  
		Last Modified: Mon, 10 Mar 2025 23:10:57 GMT  
		Size: 1.1 MB (1099370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7d6816b7155ce85b4fd3d7090122a729edcf997dfd5811a0da6f9efb5eb842`  
		Last Modified: Mon, 10 Mar 2025 23:10:57 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:66f341f3d9c3a9ed063f589d97031bfcbb352b0b7bbcacc1566df33672e8d468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76308949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf5fed543e27d83c18311052a57b5fb1d3326d209325a28a1f9c6b4233bc6ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENV TELEGRAF_VERSION=1.34.0
# Mon, 10 Mar 2025 21:51:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Mar 2025 21:51:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762a8644aed736cbf4c123385c72d805586043830867b764844d918e74198748`  
		Last Modified: Mon, 10 Mar 2025 23:11:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eb2ac6e1bddedd29dec17c8c60b881e71180e9057717b8bedd88a5ddf29dff`  
		Last Modified: Mon, 10 Mar 2025 23:11:02 GMT  
		Size: 2.5 MB (2533888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20701fd7f7a969a1bb9baed0533147a4628e6b1e40e06cc6766a8c24bbb4d7ed`  
		Last Modified: Mon, 10 Mar 2025 23:11:04 GMT  
		Size: 69.7 MB (69683288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8a78f405bde17beaef6b5427477777ec46ef79f448a34a5696059ea9640d53`  
		Last Modified: Mon, 10 Mar 2025 23:11:01 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d28fc275fc1644b0c1ced6d75ab3a8cc29421bcdc61078be517d7f594dd623f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1110394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b056bb10daf2d2da12f3331ed098a4815715ac4bd65fbae4b8dcd59ee35d37`

```dockerfile
```

-	Layers:
	-	`sha256:c4e80edcb5ee8ddfb281a98ae137fdbbfd549dd05f4446a03756b9153a9cd647`  
		Last Modified: Mon, 10 Mar 2025 23:11:02 GMT  
		Size: 1.1 MB (1095009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e30c7e59efcf50a5d390853fa8e19f748b27cede182f74e6748210d6a8f5d49`  
		Last Modified: Mon, 10 Mar 2025 23:11:01 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:5c1ae2187f43d6039196a12b7dd9960b2dbd80d996036894d0da3e4ca692885d
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
$ docker pull telegraf@sha256:cb299a37099f8f95b141ea396908c5b16bd52e38729155ba59ea6359a3bc89c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169126885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5f4bc952b642a35b619e206e213610d0a3bce93b450dc2721c23bbf1999d72`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENV TELEGRAF_VERSION=1.34.0
# Mon, 10 Mar 2025 21:51:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Mar 2025 21:51:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69e4b7262125d8685828f509e3e3c515efe312fad22f714266b281e478c7c91`  
		Last Modified: Mon, 10 Mar 2025 23:11:08 GMT  
		Size: 18.9 MB (18947976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb4eab3359f09de90e8408a05d256043914eab395db866aae36fb223310e160`  
		Last Modified: Mon, 10 Mar 2025 23:11:07 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f985cea1a4bb53787e358aa13c7ae12c14d50925d92e8510649b8a01faae7221`  
		Last Modified: Mon, 10 Mar 2025 23:11:10 GMT  
		Size: 77.6 MB (77641870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ae58584ec414068223a394c3539b5e89ad93f923aed38584cddeaae7289e19`  
		Last Modified: Mon, 10 Mar 2025 23:11:07 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:ee51d7a840ee7a74ea1ea05ac739e886a802548f7414487391a12937791a0671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6459443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee22901449a88ceefc6e46f53b36fdc80776c5790e3bc9301e122d75732c6024`

```dockerfile
```

-	Layers:
	-	`sha256:fc6eb5d591df55cf03a92bb16b33704a917b52ab69bf8284809f5e75297b1983`  
		Last Modified: Mon, 10 Mar 2025 23:11:08 GMT  
		Size: 6.4 MB (6444671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b21ef6d9228a75be92ecdd1d98fda168fdb33fb34bfc7654b3c701fec23a196b`  
		Last Modified: Mon, 10 Mar 2025 23:11:07 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:6f06caf71de92725a9e971fc9ff82e6f7919c76d33ad43be8af62a3c99e12ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155247864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee00484a53b75ca25dd0a4508f1bf82df345e4b3546be3e174f841096c95c04`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENV TELEGRAF_VERSION=1.34.0
# Mon, 10 Mar 2025 21:51:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Mar 2025 21:51:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b7bc1cadeb470200dfcf00359923782434145f653ef282933b6bfd1a14f8e1`  
		Last Modified: Tue, 25 Feb 2025 16:11:10 GMT  
		Size: 17.7 MB (17725528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3040f99c6489531530751f75cd87bb9c15b4a08bca39de42e280315706371487`  
		Last Modified: Tue, 25 Feb 2025 16:11:09 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e0c411d25868143a86b3e9c07847948da1a6c91d61b5a97ff12a6d6d171467`  
		Last Modified: Mon, 10 Mar 2025 23:10:30 GMT  
		Size: 71.4 MB (71379675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e730494c4399b5e22144e2bb2178332f2fa433aecaab3821295752164bd83176`  
		Last Modified: Mon, 10 Mar 2025 23:10:27 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:6d40e7d92e06774d26e00050985b466f1917012576cc91e7237b04e723b22967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6454949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0239cc8a4bffd542a3cc9ec391aecdb98e65e18afbf37fc069c5ae898f549ac0`

```dockerfile
```

-	Layers:
	-	`sha256:1d15c754a5d42d55283cb1d3bcbe56bf61b881d25066fe7fba8353f7b5ed0a8a`  
		Last Modified: Mon, 10 Mar 2025 23:10:28 GMT  
		Size: 6.4 MB (6440083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce92eb1382e9d9764d43c95d5c2c182af347791cbeed2ddc606ad84858c11102`  
		Last Modified: Mon, 10 Mar 2025 23:10:27 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:9758ef94a906d1c9d9430eb7afd7ff2ba74659e628292ddfb5b0c0cd7caca8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160673152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a2aa193dac21d389b4003208f7487c835ada8f825e442860234c82cd83fc73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENV TELEGRAF_VERSION=1.34.0
# Mon, 10 Mar 2025 21:51:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Mar 2025 21:51:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3c814be53f34ab64fcffafa3cce7c0113e3307f946247a7db09eb0a5ca0b4e`  
		Last Modified: Mon, 10 Mar 2025 23:10:28 GMT  
		Size: 18.9 MB (18870942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c837fce1617eb619a65ab4ad1862ce7eb84fca2ed2dfe2547bba688e94e69ff9`  
		Last Modified: Mon, 10 Mar 2025 23:10:26 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ab3d010401bb84dc9b8828047533299db58996caf5dba011bda609de1c63d0`  
		Last Modified: Mon, 10 Mar 2025 23:10:29 GMT  
		Size: 69.9 MB (69893520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5359e3548b02051e7d46bf4cf58bc6700caedfc4507619114a3ffc13a584c346`  
		Last Modified: Mon, 10 Mar 2025 23:10:27 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:2b47a480857e23e1aa81670b8f9817e7be30891862ab62f0bafb5b0dcfcb2d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6460252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a181ff33b151c62a03b1c16adf16db4e231e85017faa61d74c6193e723d0a86`

```dockerfile
```

-	Layers:
	-	`sha256:eee69b6677f78e6997ec2eecb9b1bc6c5e4b5d411545c07cdb44668c2fbd9ade`  
		Last Modified: Mon, 10 Mar 2025 23:10:27 GMT  
		Size: 6.4 MB (6445359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfb7865e46688a1f92abb77a79a51a3aa59c7520661b162d6967ed8e5896e83c`  
		Last Modified: Mon, 10 Mar 2025 23:10:26 GMT  
		Size: 14.9 KB (14893 bytes)  
		MIME: application/vnd.in-toto+json
