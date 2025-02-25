<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.31`](#telegraf131)
-	[`telegraf:1.31-alpine`](#telegraf131-alpine)
-	[`telegraf:1.31.3`](#telegraf1313)
-	[`telegraf:1.31.3-alpine`](#telegraf1313-alpine)
-	[`telegraf:1.32`](#telegraf132)
-	[`telegraf:1.32-alpine`](#telegraf132-alpine)
-	[`telegraf:1.32.3`](#telegraf1323)
-	[`telegraf:1.32.3-alpine`](#telegraf1323-alpine)
-	[`telegraf:1.33`](#telegraf133)
-	[`telegraf:1.33-alpine`](#telegraf133-alpine)
-	[`telegraf:1.33.2`](#telegraf1332)
-	[`telegraf:1.33.2-alpine`](#telegraf1332-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.31`

```console
$ docker pull telegraf@sha256:32f4abf572bae2f2dad76ab936cc414be82a4580235d26fd6689ffe10382b6f5
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
$ docker pull telegraf@sha256:0eeaeb4a4f78f8c4da5513a806dd205534b0ab5b4d1311eb0afd21abbd05a6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157770556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b55bd17bf050bf59ab1c75cba03b2e1d3619be307620cad27ac97d16f6b20b`
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
ENV TELEGRAF_VERSION=1.31.3
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
	-	`sha256:9832afa111a21d269cc1c747ea12a4925ba66b7425d4a94246a3fde96dfb0447`  
		Last Modified: Tue, 25 Feb 2025 03:19:23 GMT  
		Size: 18.9 MB (18948048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c522c5ac56efbb4dbd9e3edd214e9e8de30022aca87ad7d326e6a2ddb9ddf3d2`  
		Last Modified: Tue, 25 Feb 2025 03:19:23 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bf82cb8cfceb0c3cf08bfd032f6427823eda2ad9f7c777157fa2d49c3a8f11`  
		Last Modified: Tue, 25 Feb 2025 03:19:24 GMT  
		Size: 66.3 MB (66285481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d618f08d2bb07dd9d987ff08f91b88389de51ba6f97f1563dff2df03eb5e11`  
		Last Modified: Tue, 25 Feb 2025 03:19:23 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:fe1356fb19923867b5c0be1dfc81936a87df9f84a969c2460b5c1fa136c62dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6429067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863104ff91124a44eb979699332459be520189ae7535b3e7ca75157b64d94654`

```dockerfile
```

-	Layers:
	-	`sha256:26c44c12cdf6e39917ece99b81257dc1cfa10968593c81a81a74fed3cd3dc82b`  
		Last Modified: Tue, 25 Feb 2025 03:19:23 GMT  
		Size: 6.4 MB (6414598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638c3b2840ff6399c1a379dcc0f907a0134db3bafb8c0ffbb6831b6fb096c2fd`  
		Last Modified: Tue, 25 Feb 2025 03:19:23 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:80bf9a6198cdddd3e341bb1d843b04d263bcd1c39d3ebe8b2fd4348671a65598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145544334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ecf0158ea08df57a4b96312128c56f68db6f9d82ae9f446054f86bbcf0b80b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.31.3
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 10 Jan 2025 18:06:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 01:37:07 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 10:41:49 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52d37da5ea34f101d528e16df8870c72e9bd46b0b2a815871f8b2cad7f226a6`  
		Last Modified: Tue, 04 Feb 2025 18:30:30 GMT  
		Size: 17.7 MB (17725432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7eff7fe833c3fbd6d3c6ddd5c4675fe3df5730fd39b06790f9bf9180f68be3`  
		Last Modified: Tue, 04 Feb 2025 18:30:29 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6e79ba0bf8c0c7e2cec56f584f900184f5281a417f6fe872a33864e846e3e8`  
		Last Modified: Tue, 04 Feb 2025 18:30:32 GMT  
		Size: 61.7 MB (61672360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c309b3a1ce3a10fa77348b583e640083dedac36625f96116e074ff34a55644cf`  
		Last Modified: Tue, 04 Feb 2025 18:30:29 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:60c769fdd167e9ad1a361c0e433ebd9430ae5b3ba1fcbc011ef1b089694bc18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2bcc9ce0c93896239fdf9c842b6754dcc946e4eaddacfdf6fba32ea89c7d09`

```dockerfile
```

-	Layers:
	-	`sha256:d5b7a63d54c86b99c07cd11af6d6be02cecd8da3ac90e710e6ec39a4503f448e`  
		Last Modified: Tue, 04 Feb 2025 18:30:30 GMT  
		Size: 6.4 MB (6409984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c1bf88c1303dab963aa25f03aa55530abbf185f9914e6df4f1c3f3e12cab9f5`  
		Last Modified: Tue, 04 Feb 2025 18:30:29 GMT  
		Size: 14.6 KB (14555 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e888fc6f3fc4c771d839a0de18228e8bd5aedb034eb02178a5b3945efa938fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151157125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6d79e11560bb8ce52b1b7369ebf8f8bc0815f71b969b9e50736a558fe0ef8e`
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
ENV TELEGRAF_VERSION=1.31.3
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
	-	`sha256:5941052af88faff1a01d30d2145d0fbb8c19a83177f658e79d3f44523ac1e6fc`  
		Last Modified: Tue, 25 Feb 2025 14:22:59 GMT  
		Size: 60.4 MB (60377776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c953bc49454fef3ae77e742e22ac2502b204c047470cd5c9d6fcaa2a88bf45c`  
		Last Modified: Tue, 25 Feb 2025 14:22:57 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:6162cabd20957615b30f0f6bbeb9b8ccc055cd5e172ce05711e7f9f9ee470156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6430661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffac3aae2a5edbd0afe16c5ca3f5a66041809c60d2fb508513c13a92ddd8fe0d`

```dockerfile
```

-	Layers:
	-	`sha256:88f9421372d938abe4d58d452efe0455fe06ab0f0d96e118daec92c35dbc1a30`  
		Last Modified: Tue, 25 Feb 2025 14:22:58 GMT  
		Size: 6.4 MB (6416081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dcd409444bcce065f6f20ad68ada707e41cb42c544052712eaf22c6d68c1fca`  
		Last Modified: Tue, 25 Feb 2025 14:22:57 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31-alpine`

```console
$ docker pull telegraf@sha256:bf274ea9fbf49a62ed19478ea0badb0f040ee9db09725a94175fa5ffecd8b7ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:ba2879ac96fd18bebe4c194335b874fed284a3bcb26c1f976728d5c1917e2b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72155101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a170b8100d371adf3369933695bec97d426d1c68052e5f5ac7095c027d584b0a`
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
ENV TELEGRAF_VERSION=1.31.3
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
	-	`sha256:386a218cdb719a9576158ee1a7a44f91e4ca831aacaa99c77c4cc08a97a91d3a`  
		Last Modified: Fri, 14 Feb 2025 19:26:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b02cf70d3e15fbc1e627a366bd4ee04f1b87dbe5474dc9a33dac6af3e60913`  
		Last Modified: Fri, 14 Feb 2025 19:26:50 GMT  
		Size: 2.4 MB (2447985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52362ba785f3e9dfe7a835dee1206078f01677109c3321961083785dea5f380e`  
		Last Modified: Fri, 14 Feb 2025 19:26:50 GMT  
		Size: 66.1 MB (66079612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87823eebe559f47748506cb625ba45bf8ee21e45497482b145807fca62e0581`  
		Last Modified: Fri, 14 Feb 2025 19:26:50 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:561b5d3febe7ec49a6880f52c60a2e962e776f7d72e07eebbcf1795998814a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1084257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad041b757f4bde1051df284acc5642c2038bf93f83c50dfc4abb7394b82bd12e`

```dockerfile
```

-	Layers:
	-	`sha256:8ebe564a6114bab7156f964582817a92044c1b8b0e2f863a4e8cbd765438bf86`  
		Last Modified: Fri, 14 Feb 2025 19:26:50 GMT  
		Size: 1.1 MB (1069297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef8b23e8f8443f2c3d9bfc51273e7f15ea22ae1e25202b2be769cdfec542efa9`  
		Last Modified: Fri, 14 Feb 2025 19:26:50 GMT  
		Size: 15.0 KB (14960 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a1eee96d7b4b95b7a2482715cde7f5efffef624e8e6f3b493c4c7e1eaba38615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66797318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b0ae86f166140f943f2e6470e5c7a00960ffee837b0747f31248e30a071d09`
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
ENV TELEGRAF_VERSION=1.31.3
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
	-	`sha256:ba9ab4ab3455972429abe5f16a52674c53b992437c904a1c16a75642e09aa089`  
		Last Modified: Sat, 15 Feb 2025 06:30:26 GMT  
		Size: 60.2 MB (60171658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33c14aabdf5557104adea5cdd7a2d77cea7e032d61a3cc12d11c6c65c3dc2b6`  
		Last Modified: Sat, 15 Feb 2025 06:30:24 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9f18e6537bdfe5df0c24f59d2f397a224f2f2f525b91c0c8e72adb9ebbb8465c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1080802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ddc32d0be2006d802595fdcd620b167bedf1af82ee142557f25ab9cd6f139e`

```dockerfile
```

-	Layers:
	-	`sha256:0ff35a494c1c5958a815f9e1e9b468fd4246630f76ccaa6c412c62af92d7a192`  
		Last Modified: Sat, 15 Feb 2025 06:30:24 GMT  
		Size: 1.1 MB (1065731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:105383f7c1f88fb4340b53e6324cd3c18bd5b55146d306b8c63f5734df3d8835`  
		Last Modified: Sat, 15 Feb 2025 06:30:24 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.3`

```console
$ docker pull telegraf@sha256:32f4abf572bae2f2dad76ab936cc414be82a4580235d26fd6689ffe10382b6f5
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
$ docker pull telegraf@sha256:0eeaeb4a4f78f8c4da5513a806dd205534b0ab5b4d1311eb0afd21abbd05a6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157770556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b55bd17bf050bf59ab1c75cba03b2e1d3619be307620cad27ac97d16f6b20b`
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
ENV TELEGRAF_VERSION=1.31.3
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
	-	`sha256:9832afa111a21d269cc1c747ea12a4925ba66b7425d4a94246a3fde96dfb0447`  
		Last Modified: Tue, 25 Feb 2025 03:19:23 GMT  
		Size: 18.9 MB (18948048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c522c5ac56efbb4dbd9e3edd214e9e8de30022aca87ad7d326e6a2ddb9ddf3d2`  
		Last Modified: Tue, 25 Feb 2025 03:19:23 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bf82cb8cfceb0c3cf08bfd032f6427823eda2ad9f7c777157fa2d49c3a8f11`  
		Last Modified: Tue, 25 Feb 2025 03:19:24 GMT  
		Size: 66.3 MB (66285481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d618f08d2bb07dd9d987ff08f91b88389de51ba6f97f1563dff2df03eb5e11`  
		Last Modified: Tue, 25 Feb 2025 03:19:23 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:fe1356fb19923867b5c0be1dfc81936a87df9f84a969c2460b5c1fa136c62dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6429067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863104ff91124a44eb979699332459be520189ae7535b3e7ca75157b64d94654`

```dockerfile
```

-	Layers:
	-	`sha256:26c44c12cdf6e39917ece99b81257dc1cfa10968593c81a81a74fed3cd3dc82b`  
		Last Modified: Tue, 25 Feb 2025 03:19:23 GMT  
		Size: 6.4 MB (6414598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638c3b2840ff6399c1a379dcc0f907a0134db3bafb8c0ffbb6831b6fb096c2fd`  
		Last Modified: Tue, 25 Feb 2025 03:19:23 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:80bf9a6198cdddd3e341bb1d843b04d263bcd1c39d3ebe8b2fd4348671a65598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145544334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ecf0158ea08df57a4b96312128c56f68db6f9d82ae9f446054f86bbcf0b80b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.31.3
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 10 Jan 2025 18:06:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 01:37:07 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 10:41:49 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52d37da5ea34f101d528e16df8870c72e9bd46b0b2a815871f8b2cad7f226a6`  
		Last Modified: Tue, 04 Feb 2025 18:30:30 GMT  
		Size: 17.7 MB (17725432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7eff7fe833c3fbd6d3c6ddd5c4675fe3df5730fd39b06790f9bf9180f68be3`  
		Last Modified: Tue, 04 Feb 2025 18:30:29 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6e79ba0bf8c0c7e2cec56f584f900184f5281a417f6fe872a33864e846e3e8`  
		Last Modified: Tue, 04 Feb 2025 18:30:32 GMT  
		Size: 61.7 MB (61672360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c309b3a1ce3a10fa77348b583e640083dedac36625f96116e074ff34a55644cf`  
		Last Modified: Tue, 04 Feb 2025 18:30:29 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:60c769fdd167e9ad1a361c0e433ebd9430ae5b3ba1fcbc011ef1b089694bc18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2bcc9ce0c93896239fdf9c842b6754dcc946e4eaddacfdf6fba32ea89c7d09`

```dockerfile
```

-	Layers:
	-	`sha256:d5b7a63d54c86b99c07cd11af6d6be02cecd8da3ac90e710e6ec39a4503f448e`  
		Last Modified: Tue, 04 Feb 2025 18:30:30 GMT  
		Size: 6.4 MB (6409984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c1bf88c1303dab963aa25f03aa55530abbf185f9914e6df4f1c3f3e12cab9f5`  
		Last Modified: Tue, 04 Feb 2025 18:30:29 GMT  
		Size: 14.6 KB (14555 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e888fc6f3fc4c771d839a0de18228e8bd5aedb034eb02178a5b3945efa938fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151157125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6d79e11560bb8ce52b1b7369ebf8f8bc0815f71b969b9e50736a558fe0ef8e`
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
ENV TELEGRAF_VERSION=1.31.3
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
	-	`sha256:5941052af88faff1a01d30d2145d0fbb8c19a83177f658e79d3f44523ac1e6fc`  
		Last Modified: Tue, 25 Feb 2025 14:22:59 GMT  
		Size: 60.4 MB (60377776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c953bc49454fef3ae77e742e22ac2502b204c047470cd5c9d6fcaa2a88bf45c`  
		Last Modified: Tue, 25 Feb 2025 14:22:57 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:6162cabd20957615b30f0f6bbeb9b8ccc055cd5e172ce05711e7f9f9ee470156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6430661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffac3aae2a5edbd0afe16c5ca3f5a66041809c60d2fb508513c13a92ddd8fe0d`

```dockerfile
```

-	Layers:
	-	`sha256:88f9421372d938abe4d58d452efe0455fe06ab0f0d96e118daec92c35dbc1a30`  
		Last Modified: Tue, 25 Feb 2025 14:22:58 GMT  
		Size: 6.4 MB (6416081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dcd409444bcce065f6f20ad68ada707e41cb42c544052712eaf22c6d68c1fca`  
		Last Modified: Tue, 25 Feb 2025 14:22:57 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.3-alpine`

```console
$ docker pull telegraf@sha256:bf274ea9fbf49a62ed19478ea0badb0f040ee9db09725a94175fa5ffecd8b7ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:ba2879ac96fd18bebe4c194335b874fed284a3bcb26c1f976728d5c1917e2b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72155101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a170b8100d371adf3369933695bec97d426d1c68052e5f5ac7095c027d584b0a`
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
ENV TELEGRAF_VERSION=1.31.3
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
	-	`sha256:386a218cdb719a9576158ee1a7a44f91e4ca831aacaa99c77c4cc08a97a91d3a`  
		Last Modified: Fri, 14 Feb 2025 19:26:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b02cf70d3e15fbc1e627a366bd4ee04f1b87dbe5474dc9a33dac6af3e60913`  
		Last Modified: Fri, 14 Feb 2025 19:26:50 GMT  
		Size: 2.4 MB (2447985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52362ba785f3e9dfe7a835dee1206078f01677109c3321961083785dea5f380e`  
		Last Modified: Fri, 14 Feb 2025 19:26:50 GMT  
		Size: 66.1 MB (66079612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87823eebe559f47748506cb625ba45bf8ee21e45497482b145807fca62e0581`  
		Last Modified: Fri, 14 Feb 2025 19:26:50 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:561b5d3febe7ec49a6880f52c60a2e962e776f7d72e07eebbcf1795998814a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1084257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad041b757f4bde1051df284acc5642c2038bf93f83c50dfc4abb7394b82bd12e`

```dockerfile
```

-	Layers:
	-	`sha256:8ebe564a6114bab7156f964582817a92044c1b8b0e2f863a4e8cbd765438bf86`  
		Last Modified: Fri, 14 Feb 2025 19:26:50 GMT  
		Size: 1.1 MB (1069297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef8b23e8f8443f2c3d9bfc51273e7f15ea22ae1e25202b2be769cdfec542efa9`  
		Last Modified: Fri, 14 Feb 2025 19:26:50 GMT  
		Size: 15.0 KB (14960 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a1eee96d7b4b95b7a2482715cde7f5efffef624e8e6f3b493c4c7e1eaba38615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66797318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b0ae86f166140f943f2e6470e5c7a00960ffee837b0747f31248e30a071d09`
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
ENV TELEGRAF_VERSION=1.31.3
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
	-	`sha256:ba9ab4ab3455972429abe5f16a52674c53b992437c904a1c16a75642e09aa089`  
		Last Modified: Sat, 15 Feb 2025 06:30:26 GMT  
		Size: 60.2 MB (60171658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33c14aabdf5557104adea5cdd7a2d77cea7e032d61a3cc12d11c6c65c3dc2b6`  
		Last Modified: Sat, 15 Feb 2025 06:30:24 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9f18e6537bdfe5df0c24f59d2f397a224f2f2f525b91c0c8e72adb9ebbb8465c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1080802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ddc32d0be2006d802595fdcd620b167bedf1af82ee142557f25ab9cd6f139e`

```dockerfile
```

-	Layers:
	-	`sha256:0ff35a494c1c5958a815f9e1e9b468fd4246630f76ccaa6c412c62af92d7a192`  
		Last Modified: Sat, 15 Feb 2025 06:30:24 GMT  
		Size: 1.1 MB (1065731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:105383f7c1f88fb4340b53e6324cd3c18bd5b55146d306b8c63f5734df3d8835`  
		Last Modified: Sat, 15 Feb 2025 06:30:24 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32`

```console
$ docker pull telegraf@sha256:d109c8601be71d7dcc439c484544328e3e74fb1ec9a7160909d0bc93ae662836
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
$ docker pull telegraf@sha256:4aa84f86799a612db75d3238a9fe03cf86ca334ac4bfecd47d7d4113edbb10cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148554837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de54822187119f8a56a513bdafd4c66a8f88e580de699da405f0e98f133d2d55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.32.3
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 10 Jan 2025 18:06:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 01:37:07 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 10:41:49 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52d37da5ea34f101d528e16df8870c72e9bd46b0b2a815871f8b2cad7f226a6`  
		Last Modified: Tue, 04 Feb 2025 18:30:30 GMT  
		Size: 17.7 MB (17725432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7eff7fe833c3fbd6d3c6ddd5c4675fe3df5730fd39b06790f9bf9180f68be3`  
		Last Modified: Tue, 04 Feb 2025 18:30:29 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf70aefe3719702dbd94833da29fa795c128b685bea70616300426d56cb18f4`  
		Last Modified: Tue, 04 Feb 2025 18:31:20 GMT  
		Size: 64.7 MB (64682863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9e3b3c168fcca5e8fc731ec7c740b6f5a0fa7ee9f1fcb5904a4901eed55a3c`  
		Last Modified: Tue, 04 Feb 2025 18:31:18 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:6d1af87fc2809f5fe0a5c1610c5e6c8e4308d2cf7e2ae11544f397d587c37c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6433998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820e6ad1d63c5560122353558ae33228893101b690e76cf80d3ba43536646f62`

```dockerfile
```

-	Layers:
	-	`sha256:0b5d792333488891b03f0b784574869a10312353e0eb76f11967acd86eb8e20a`  
		Last Modified: Tue, 04 Feb 2025 18:31:19 GMT  
		Size: 6.4 MB (6419442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02091922e33ce14e5262a735256017abd5bf12ed099ce7c9bb931eed9529bdde`  
		Last Modified: Tue, 04 Feb 2025 18:31:18 GMT  
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
$ docker pull telegraf@sha256:d109c8601be71d7dcc439c484544328e3e74fb1ec9a7160909d0bc93ae662836
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
$ docker pull telegraf@sha256:4aa84f86799a612db75d3238a9fe03cf86ca334ac4bfecd47d7d4113edbb10cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148554837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de54822187119f8a56a513bdafd4c66a8f88e580de699da405f0e98f133d2d55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.32.3
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 10 Jan 2025 18:06:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 01:37:07 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 10:41:49 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52d37da5ea34f101d528e16df8870c72e9bd46b0b2a815871f8b2cad7f226a6`  
		Last Modified: Tue, 04 Feb 2025 18:30:30 GMT  
		Size: 17.7 MB (17725432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7eff7fe833c3fbd6d3c6ddd5c4675fe3df5730fd39b06790f9bf9180f68be3`  
		Last Modified: Tue, 04 Feb 2025 18:30:29 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf70aefe3719702dbd94833da29fa795c128b685bea70616300426d56cb18f4`  
		Last Modified: Tue, 04 Feb 2025 18:31:20 GMT  
		Size: 64.7 MB (64682863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9e3b3c168fcca5e8fc731ec7c740b6f5a0fa7ee9f1fcb5904a4901eed55a3c`  
		Last Modified: Tue, 04 Feb 2025 18:31:18 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:6d1af87fc2809f5fe0a5c1610c5e6c8e4308d2cf7e2ae11544f397d587c37c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6433998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820e6ad1d63c5560122353558ae33228893101b690e76cf80d3ba43536646f62`

```dockerfile
```

-	Layers:
	-	`sha256:0b5d792333488891b03f0b784574869a10312353e0eb76f11967acd86eb8e20a`  
		Last Modified: Tue, 04 Feb 2025 18:31:19 GMT  
		Size: 6.4 MB (6419442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02091922e33ce14e5262a735256017abd5bf12ed099ce7c9bb931eed9529bdde`  
		Last Modified: Tue, 04 Feb 2025 18:31:18 GMT  
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
$ docker pull telegraf@sha256:087783af38ad58b701da6c2a53fd5319f0d299702a115f7604ad7a5badaf929a
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
$ docker pull telegraf@sha256:0e20b846d9899ae9b86688ab34e6d3e836319fe78f596145f84f3a1afd84493a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167818964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e77c194d1304c21f28786a430d64b5dbe1565f4a5792397e387353fc91c3f0`
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
ENV TELEGRAF_VERSION=1.33.2
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
	-	`sha256:25c658cdde06a1e65ba1002194efed4848e35e244409acc7c78e8d97bebf7786`  
		Last Modified: Tue, 25 Feb 2025 03:19:40 GMT  
		Size: 18.9 MB (18948049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa4b4f5cf5b6e6b5b8ae49862efd932205ab78607f281fc3831bf9a7f763352`  
		Last Modified: Tue, 25 Feb 2025 03:19:39 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6d24e2103cf750df19a4c11f9a8702f311cbf91cfa860d6dcf72b0533b14ef`  
		Last Modified: Tue, 25 Feb 2025 03:19:42 GMT  
		Size: 76.3 MB (76333879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3c2c4ed2937ed31f842f4519a3f724492b8b379a9bb7822b44fa1ac6c0f02c`  
		Last Modified: Tue, 25 Feb 2025 03:19:39 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:0e9854eb40d6cbf9a7fa892556d5beaaecefd1593bee1e0821437dd553cae3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6453920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796b73d5653c4020e8556be51509120215cb3c8dbb2af2dd4e03d8ca48f5e832`

```dockerfile
```

-	Layers:
	-	`sha256:0e03a257cfbc0c29d4649a2a13e2b3978a231681694a4792e24a6428ded91791`  
		Last Modified: Tue, 25 Feb 2025 03:19:39 GMT  
		Size: 6.4 MB (6439148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed0280b00b4bbc5082a718e72f7e6536118286d27b9737c472b2004e70236399`  
		Last Modified: Tue, 25 Feb 2025 03:19:39 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:631c670d815298bf1f01e9fc14a70a9c7bd7df381413c2f6f8cf9703f88c6acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154403882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b7d15c4334993a82be810f026fa39135482da26066349e5f69993fa3cb98a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
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
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 01:37:07 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 10:41:49 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52d37da5ea34f101d528e16df8870c72e9bd46b0b2a815871f8b2cad7f226a6`  
		Last Modified: Tue, 04 Feb 2025 18:30:30 GMT  
		Size: 17.7 MB (17725432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7eff7fe833c3fbd6d3c6ddd5c4675fe3df5730fd39b06790f9bf9180f68be3`  
		Last Modified: Tue, 04 Feb 2025 18:30:29 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad85eae4eeefe28382b2b6ac022363abf12720aad417db847747f7cedc24e4f`  
		Last Modified: Tue, 11 Feb 2025 01:30:27 GMT  
		Size: 70.5 MB (70531910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf78465c33b061c5ae7946dbbaa605f1f867b1eb067fa2855063e286ac831242`  
		Last Modified: Tue, 11 Feb 2025 01:30:24 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:93190e99f59af7e4b86571b6be0b588840260f7a057d24c488ebe065c5db4eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6449408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87aed9440d4d8fa5f34ec0f4f034d2ada4b4415c95fce9276d64b5270762d6db`

```dockerfile
```

-	Layers:
	-	`sha256:bea2ca2705b89231972f0f25adccd1a433f3d0bfd15e8e4e3fd71d4068b5d196`  
		Last Modified: Tue, 11 Feb 2025 01:30:25 GMT  
		Size: 6.4 MB (6434542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2665fc8fe71fcacebb712ffb1f8fa69073fee2a894fa79dcd10281dff936e306`  
		Last Modified: Tue, 11 Feb 2025 01:30:25 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a52f579be8879ab811a43023136bc80273b068ac5d2428c1bcca5b6c1a5ec1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159823353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0482f0c34431d6c2adf636e0bd282ee7d8a092e21958e1fbe916a1991e994`
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
ENV TELEGRAF_VERSION=1.33.2
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
	-	`sha256:89c98c553b9355d2ae2a9b13642e4537218cc56887c0fb73e5bacf3150a83e86`  
		Last Modified: Tue, 25 Feb 2025 14:23:34 GMT  
		Size: 69.0 MB (69044004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3de81cdd34603beef4431e7737c1077c744885449f1935092b907a3b285c090`  
		Last Modified: Tue, 25 Feb 2025 14:23:32 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:1ee5c1d2c42525a7aa170adec5fff57bbfdeb0a967a5fd31bd8033769f6bd28a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6454730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28ab34ce15bf6f1bd512ff4c5399e6f1c0a0f69eb405d7cc1f470ec437383d2`

```dockerfile
```

-	Layers:
	-	`sha256:c7f2bc34f6d09f29b4ca841a71d0c558ef7158682ba7670f2b44aaa23bfd0cc1`  
		Last Modified: Tue, 25 Feb 2025 14:23:32 GMT  
		Size: 6.4 MB (6439836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e72e238be180e670a58d0e1608bf092cf8a0e862a96f6f2db23a274efb90b97f`  
		Last Modified: Tue, 25 Feb 2025 14:23:31 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33-alpine`

```console
$ docker pull telegraf@sha256:69fa36580c611f3035ab7925194cd62b53651cc0d7795219ce9345560ec29d77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e001ac229a01e097b80d6d23a6182691a7c1cad10869f684597ee609e33a6b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82201285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb39c98bfad6a37dc90ba4085099a0f6f9c513aae8bba47efbe7a3f442ae89d`
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
ENV TELEGRAF_VERSION=1.33.2
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
	-	`sha256:c2c0bed9355d3eb54aa1208d3a20257a76f64080773dc86dcb02a82c6e8f82c6`  
		Last Modified: Fri, 14 Feb 2025 19:26:55 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325236e58b26876274c2856b683e82eaf5bdecf70373559cbcbe456230a5f053`  
		Last Modified: Fri, 14 Feb 2025 19:26:56 GMT  
		Size: 2.4 MB (2447975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6031a4ba8445bd07a336bf1dd87e8fc25a2b331379934204cd688e656b4a9a`  
		Last Modified: Fri, 14 Feb 2025 19:26:57 GMT  
		Size: 76.1 MB (76125805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8e7ad7c1c42825ed080658aaa640df496aa868c7efb879c706b8147cff5710`  
		Last Modified: Fri, 14 Feb 2025 19:26:56 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:16d454cb57b400e67295e59abd73a643329b519fce6d55bd24dfb96cecd5c9c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1109110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a241722ce577a08c5d381c1f78d5c1ae86f867161c20c23e86808423352077`

```dockerfile
```

-	Layers:
	-	`sha256:ad0137f95a7afc49f37e4adc720387b76f20227bbe6621e5ca331fb943377567`  
		Last Modified: Fri, 14 Feb 2025 19:26:55 GMT  
		Size: 1.1 MB (1093847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1528d844dfa92117a2ea7bf3a4ca3e75062348016828dcd367bba63a3e5e5ca1`  
		Last Modified: Fri, 14 Feb 2025 19:26:55 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6a65d050e306d9717bcc023d72592dca9d57822fa5cd6d6df109ed7238a19b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75469195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85926df0ec4603baa1eeb2e3715a4f2d8cd29fd6277a4dfbb38e415734fc306e`
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
ENV TELEGRAF_VERSION=1.33.2
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
	-	`sha256:f7bf10fc8b7214ca8fef9f7bb41b2d0347463acd22e2fbceedb7a5e8b8e8e343`  
		Last Modified: Sat, 15 Feb 2025 06:31:28 GMT  
		Size: 68.8 MB (68843532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd185c393dc552246958fc560ea1cc609f26d253c54abd6599bd16f158f4f22`  
		Last Modified: Sat, 15 Feb 2025 06:31:26 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:22d9a2b1dd0ae592bf224ebe3d2a54de598ef6648a29a48cd1b3a5177a39526c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1104870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1272b930dbce6f617c202d1a5ae455db4b97a9bb21c3d063c046406fa09f81`

```dockerfile
```

-	Layers:
	-	`sha256:c69531efe7feb8f84aa571217dd572369b538232ce2942a97f0c8ef8c8008b18`  
		Last Modified: Sat, 15 Feb 2025 06:31:26 GMT  
		Size: 1.1 MB (1089486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15a68ad0bcd8f5bb69ea8993a1c6674fdac750648cae385ff459a274cb622b9a`  
		Last Modified: Sat, 15 Feb 2025 06:31:25 GMT  
		Size: 15.4 KB (15384 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33.2`

```console
$ docker pull telegraf@sha256:087783af38ad58b701da6c2a53fd5319f0d299702a115f7604ad7a5badaf929a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33.2` - linux; amd64

```console
$ docker pull telegraf@sha256:0e20b846d9899ae9b86688ab34e6d3e836319fe78f596145f84f3a1afd84493a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167818964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e77c194d1304c21f28786a430d64b5dbe1565f4a5792397e387353fc91c3f0`
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
ENV TELEGRAF_VERSION=1.33.2
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
	-	`sha256:25c658cdde06a1e65ba1002194efed4848e35e244409acc7c78e8d97bebf7786`  
		Last Modified: Tue, 25 Feb 2025 03:19:40 GMT  
		Size: 18.9 MB (18948049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa4b4f5cf5b6e6b5b8ae49862efd932205ab78607f281fc3831bf9a7f763352`  
		Last Modified: Tue, 25 Feb 2025 03:19:39 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6d24e2103cf750df19a4c11f9a8702f311cbf91cfa860d6dcf72b0533b14ef`  
		Last Modified: Tue, 25 Feb 2025 03:19:42 GMT  
		Size: 76.3 MB (76333879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3c2c4ed2937ed31f842f4519a3f724492b8b379a9bb7822b44fa1ac6c0f02c`  
		Last Modified: Tue, 25 Feb 2025 03:19:39 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:0e9854eb40d6cbf9a7fa892556d5beaaecefd1593bee1e0821437dd553cae3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6453920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796b73d5653c4020e8556be51509120215cb3c8dbb2af2dd4e03d8ca48f5e832`

```dockerfile
```

-	Layers:
	-	`sha256:0e03a257cfbc0c29d4649a2a13e2b3978a231681694a4792e24a6428ded91791`  
		Last Modified: Tue, 25 Feb 2025 03:19:39 GMT  
		Size: 6.4 MB (6439148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed0280b00b4bbc5082a718e72f7e6536118286d27b9737c472b2004e70236399`  
		Last Modified: Tue, 25 Feb 2025 03:19:39 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.2` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:631c670d815298bf1f01e9fc14a70a9c7bd7df381413c2f6f8cf9703f88c6acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154403882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b7d15c4334993a82be810f026fa39135482da26066349e5f69993fa3cb98a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
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
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 01:37:07 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 10:41:49 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52d37da5ea34f101d528e16df8870c72e9bd46b0b2a815871f8b2cad7f226a6`  
		Last Modified: Tue, 04 Feb 2025 18:30:30 GMT  
		Size: 17.7 MB (17725432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7eff7fe833c3fbd6d3c6ddd5c4675fe3df5730fd39b06790f9bf9180f68be3`  
		Last Modified: Tue, 04 Feb 2025 18:30:29 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad85eae4eeefe28382b2b6ac022363abf12720aad417db847747f7cedc24e4f`  
		Last Modified: Tue, 11 Feb 2025 01:30:27 GMT  
		Size: 70.5 MB (70531910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf78465c33b061c5ae7946dbbaa605f1f867b1eb067fa2855063e286ac831242`  
		Last Modified: Tue, 11 Feb 2025 01:30:24 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:93190e99f59af7e4b86571b6be0b588840260f7a057d24c488ebe065c5db4eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6449408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87aed9440d4d8fa5f34ec0f4f034d2ada4b4415c95fce9276d64b5270762d6db`

```dockerfile
```

-	Layers:
	-	`sha256:bea2ca2705b89231972f0f25adccd1a433f3d0bfd15e8e4e3fd71d4068b5d196`  
		Last Modified: Tue, 11 Feb 2025 01:30:25 GMT  
		Size: 6.4 MB (6434542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2665fc8fe71fcacebb712ffb1f8fa69073fee2a894fa79dcd10281dff936e306`  
		Last Modified: Tue, 11 Feb 2025 01:30:25 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.2` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a52f579be8879ab811a43023136bc80273b068ac5d2428c1bcca5b6c1a5ec1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159823353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0482f0c34431d6c2adf636e0bd282ee7d8a092e21958e1fbe916a1991e994`
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
ENV TELEGRAF_VERSION=1.33.2
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
	-	`sha256:89c98c553b9355d2ae2a9b13642e4537218cc56887c0fb73e5bacf3150a83e86`  
		Last Modified: Tue, 25 Feb 2025 14:23:34 GMT  
		Size: 69.0 MB (69044004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3de81cdd34603beef4431e7737c1077c744885449f1935092b907a3b285c090`  
		Last Modified: Tue, 25 Feb 2025 14:23:32 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:1ee5c1d2c42525a7aa170adec5fff57bbfdeb0a967a5fd31bd8033769f6bd28a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6454730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28ab34ce15bf6f1bd512ff4c5399e6f1c0a0f69eb405d7cc1f470ec437383d2`

```dockerfile
```

-	Layers:
	-	`sha256:c7f2bc34f6d09f29b4ca841a71d0c558ef7158682ba7670f2b44aaa23bfd0cc1`  
		Last Modified: Tue, 25 Feb 2025 14:23:32 GMT  
		Size: 6.4 MB (6439836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e72e238be180e670a58d0e1608bf092cf8a0e862a96f6f2db23a274efb90b97f`  
		Last Modified: Tue, 25 Feb 2025 14:23:31 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33.2-alpine`

```console
$ docker pull telegraf@sha256:69fa36580c611f3035ab7925194cd62b53651cc0d7795219ce9345560ec29d77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33.2-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e001ac229a01e097b80d6d23a6182691a7c1cad10869f684597ee609e33a6b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82201285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb39c98bfad6a37dc90ba4085099a0f6f9c513aae8bba47efbe7a3f442ae89d`
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
ENV TELEGRAF_VERSION=1.33.2
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
	-	`sha256:c2c0bed9355d3eb54aa1208d3a20257a76f64080773dc86dcb02a82c6e8f82c6`  
		Last Modified: Fri, 14 Feb 2025 19:26:55 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325236e58b26876274c2856b683e82eaf5bdecf70373559cbcbe456230a5f053`  
		Last Modified: Fri, 14 Feb 2025 19:26:56 GMT  
		Size: 2.4 MB (2447975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6031a4ba8445bd07a336bf1dd87e8fc25a2b331379934204cd688e656b4a9a`  
		Last Modified: Fri, 14 Feb 2025 19:26:57 GMT  
		Size: 76.1 MB (76125805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8e7ad7c1c42825ed080658aaa640df496aa868c7efb879c706b8147cff5710`  
		Last Modified: Fri, 14 Feb 2025 19:26:56 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.2-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:16d454cb57b400e67295e59abd73a643329b519fce6d55bd24dfb96cecd5c9c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1109110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a241722ce577a08c5d381c1f78d5c1ae86f867161c20c23e86808423352077`

```dockerfile
```

-	Layers:
	-	`sha256:ad0137f95a7afc49f37e4adc720387b76f20227bbe6621e5ca331fb943377567`  
		Last Modified: Fri, 14 Feb 2025 19:26:55 GMT  
		Size: 1.1 MB (1093847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1528d844dfa92117a2ea7bf3a4ca3e75062348016828dcd367bba63a3e5e5ca1`  
		Last Modified: Fri, 14 Feb 2025 19:26:55 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.2-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6a65d050e306d9717bcc023d72592dca9d57822fa5cd6d6df109ed7238a19b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75469195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85926df0ec4603baa1eeb2e3715a4f2d8cd29fd6277a4dfbb38e415734fc306e`
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
ENV TELEGRAF_VERSION=1.33.2
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
	-	`sha256:f7bf10fc8b7214ca8fef9f7bb41b2d0347463acd22e2fbceedb7a5e8b8e8e343`  
		Last Modified: Sat, 15 Feb 2025 06:31:28 GMT  
		Size: 68.8 MB (68843532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd185c393dc552246958fc560ea1cc609f26d253c54abd6599bd16f158f4f22`  
		Last Modified: Sat, 15 Feb 2025 06:31:26 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.2-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:22d9a2b1dd0ae592bf224ebe3d2a54de598ef6648a29a48cd1b3a5177a39526c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1104870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1272b930dbce6f617c202d1a5ae455db4b97a9bb21c3d063c046406fa09f81`

```dockerfile
```

-	Layers:
	-	`sha256:c69531efe7feb8f84aa571217dd572369b538232ce2942a97f0c8ef8c8008b18`  
		Last Modified: Sat, 15 Feb 2025 06:31:26 GMT  
		Size: 1.1 MB (1089486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15a68ad0bcd8f5bb69ea8993a1c6674fdac750648cae385ff459a274cb622b9a`  
		Last Modified: Sat, 15 Feb 2025 06:31:25 GMT  
		Size: 15.4 KB (15384 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:69fa36580c611f3035ab7925194cd62b53651cc0d7795219ce9345560ec29d77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e001ac229a01e097b80d6d23a6182691a7c1cad10869f684597ee609e33a6b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82201285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb39c98bfad6a37dc90ba4085099a0f6f9c513aae8bba47efbe7a3f442ae89d`
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
ENV TELEGRAF_VERSION=1.33.2
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
	-	`sha256:c2c0bed9355d3eb54aa1208d3a20257a76f64080773dc86dcb02a82c6e8f82c6`  
		Last Modified: Fri, 14 Feb 2025 19:26:55 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325236e58b26876274c2856b683e82eaf5bdecf70373559cbcbe456230a5f053`  
		Last Modified: Fri, 14 Feb 2025 19:26:56 GMT  
		Size: 2.4 MB (2447975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6031a4ba8445bd07a336bf1dd87e8fc25a2b331379934204cd688e656b4a9a`  
		Last Modified: Fri, 14 Feb 2025 19:26:57 GMT  
		Size: 76.1 MB (76125805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8e7ad7c1c42825ed080658aaa640df496aa868c7efb879c706b8147cff5710`  
		Last Modified: Fri, 14 Feb 2025 19:26:56 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:16d454cb57b400e67295e59abd73a643329b519fce6d55bd24dfb96cecd5c9c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1109110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a241722ce577a08c5d381c1f78d5c1ae86f867161c20c23e86808423352077`

```dockerfile
```

-	Layers:
	-	`sha256:ad0137f95a7afc49f37e4adc720387b76f20227bbe6621e5ca331fb943377567`  
		Last Modified: Fri, 14 Feb 2025 19:26:55 GMT  
		Size: 1.1 MB (1093847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1528d844dfa92117a2ea7bf3a4ca3e75062348016828dcd367bba63a3e5e5ca1`  
		Last Modified: Fri, 14 Feb 2025 19:26:55 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6a65d050e306d9717bcc023d72592dca9d57822fa5cd6d6df109ed7238a19b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75469195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85926df0ec4603baa1eeb2e3715a4f2d8cd29fd6277a4dfbb38e415734fc306e`
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
ENV TELEGRAF_VERSION=1.33.2
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
	-	`sha256:f7bf10fc8b7214ca8fef9f7bb41b2d0347463acd22e2fbceedb7a5e8b8e8e343`  
		Last Modified: Sat, 15 Feb 2025 06:31:28 GMT  
		Size: 68.8 MB (68843532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd185c393dc552246958fc560ea1cc609f26d253c54abd6599bd16f158f4f22`  
		Last Modified: Sat, 15 Feb 2025 06:31:26 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:22d9a2b1dd0ae592bf224ebe3d2a54de598ef6648a29a48cd1b3a5177a39526c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1104870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1272b930dbce6f617c202d1a5ae455db4b97a9bb21c3d063c046406fa09f81`

```dockerfile
```

-	Layers:
	-	`sha256:c69531efe7feb8f84aa571217dd572369b538232ce2942a97f0c8ef8c8008b18`  
		Last Modified: Sat, 15 Feb 2025 06:31:26 GMT  
		Size: 1.1 MB (1089486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15a68ad0bcd8f5bb69ea8993a1c6674fdac750648cae385ff459a274cb622b9a`  
		Last Modified: Sat, 15 Feb 2025 06:31:25 GMT  
		Size: 15.4 KB (15384 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:087783af38ad58b701da6c2a53fd5319f0d299702a115f7604ad7a5badaf929a
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
$ docker pull telegraf@sha256:0e20b846d9899ae9b86688ab34e6d3e836319fe78f596145f84f3a1afd84493a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167818964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e77c194d1304c21f28786a430d64b5dbe1565f4a5792397e387353fc91c3f0`
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
ENV TELEGRAF_VERSION=1.33.2
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
	-	`sha256:25c658cdde06a1e65ba1002194efed4848e35e244409acc7c78e8d97bebf7786`  
		Last Modified: Tue, 25 Feb 2025 03:19:40 GMT  
		Size: 18.9 MB (18948049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa4b4f5cf5b6e6b5b8ae49862efd932205ab78607f281fc3831bf9a7f763352`  
		Last Modified: Tue, 25 Feb 2025 03:19:39 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6d24e2103cf750df19a4c11f9a8702f311cbf91cfa860d6dcf72b0533b14ef`  
		Last Modified: Tue, 25 Feb 2025 03:19:42 GMT  
		Size: 76.3 MB (76333879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3c2c4ed2937ed31f842f4519a3f724492b8b379a9bb7822b44fa1ac6c0f02c`  
		Last Modified: Tue, 25 Feb 2025 03:19:39 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:0e9854eb40d6cbf9a7fa892556d5beaaecefd1593bee1e0821437dd553cae3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6453920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796b73d5653c4020e8556be51509120215cb3c8dbb2af2dd4e03d8ca48f5e832`

```dockerfile
```

-	Layers:
	-	`sha256:0e03a257cfbc0c29d4649a2a13e2b3978a231681694a4792e24a6428ded91791`  
		Last Modified: Tue, 25 Feb 2025 03:19:39 GMT  
		Size: 6.4 MB (6439148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed0280b00b4bbc5082a718e72f7e6536118286d27b9737c472b2004e70236399`  
		Last Modified: Tue, 25 Feb 2025 03:19:39 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:631c670d815298bf1f01e9fc14a70a9c7bd7df381413c2f6f8cf9703f88c6acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154403882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b7d15c4334993a82be810f026fa39135482da26066349e5f69993fa3cb98a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
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
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 01:37:07 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 10:41:49 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52d37da5ea34f101d528e16df8870c72e9bd46b0b2a815871f8b2cad7f226a6`  
		Last Modified: Tue, 04 Feb 2025 18:30:30 GMT  
		Size: 17.7 MB (17725432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7eff7fe833c3fbd6d3c6ddd5c4675fe3df5730fd39b06790f9bf9180f68be3`  
		Last Modified: Tue, 04 Feb 2025 18:30:29 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad85eae4eeefe28382b2b6ac022363abf12720aad417db847747f7cedc24e4f`  
		Last Modified: Tue, 11 Feb 2025 01:30:27 GMT  
		Size: 70.5 MB (70531910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf78465c33b061c5ae7946dbbaa605f1f867b1eb067fa2855063e286ac831242`  
		Last Modified: Tue, 11 Feb 2025 01:30:24 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:93190e99f59af7e4b86571b6be0b588840260f7a057d24c488ebe065c5db4eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6449408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87aed9440d4d8fa5f34ec0f4f034d2ada4b4415c95fce9276d64b5270762d6db`

```dockerfile
```

-	Layers:
	-	`sha256:bea2ca2705b89231972f0f25adccd1a433f3d0bfd15e8e4e3fd71d4068b5d196`  
		Last Modified: Tue, 11 Feb 2025 01:30:25 GMT  
		Size: 6.4 MB (6434542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2665fc8fe71fcacebb712ffb1f8fa69073fee2a894fa79dcd10281dff936e306`  
		Last Modified: Tue, 11 Feb 2025 01:30:25 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a52f579be8879ab811a43023136bc80273b068ac5d2428c1bcca5b6c1a5ec1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159823353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0482f0c34431d6c2adf636e0bd282ee7d8a092e21958e1fbe916a1991e994`
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
ENV TELEGRAF_VERSION=1.33.2
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
	-	`sha256:89c98c553b9355d2ae2a9b13642e4537218cc56887c0fb73e5bacf3150a83e86`  
		Last Modified: Tue, 25 Feb 2025 14:23:34 GMT  
		Size: 69.0 MB (69044004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3de81cdd34603beef4431e7737c1077c744885449f1935092b907a3b285c090`  
		Last Modified: Tue, 25 Feb 2025 14:23:32 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:1ee5c1d2c42525a7aa170adec5fff57bbfdeb0a967a5fd31bd8033769f6bd28a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6454730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28ab34ce15bf6f1bd512ff4c5399e6f1c0a0f69eb405d7cc1f470ec437383d2`

```dockerfile
```

-	Layers:
	-	`sha256:c7f2bc34f6d09f29b4ca841a71d0c558ef7158682ba7670f2b44aaa23bfd0cc1`  
		Last Modified: Tue, 25 Feb 2025 14:23:32 GMT  
		Size: 6.4 MB (6439836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e72e238be180e670a58d0e1608bf092cf8a0e862a96f6f2db23a274efb90b97f`  
		Last Modified: Tue, 25 Feb 2025 14:23:31 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
