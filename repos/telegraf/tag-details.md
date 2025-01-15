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
-	[`telegraf:1.33.1`](#telegraf1331)
-	[`telegraf:1.33.1-alpine`](#telegraf1331-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.31`

```console
$ docker pull telegraf@sha256:86d756d0cfc06b89cdfbaed8e2522e3c74b67a591f92c21a462d837a12e16f8b
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
$ docker pull telegraf@sha256:a397bfe1283345f30fb2e4180416b9332062470e2d957cff079050bafa53b4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157774349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7451db0554ed5fef32cdc89807aedfaafe56151c024df02f24dd9c4c66105695`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 20:33:03 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6451a409900f515eb8afecb4d2b9d437859ea666bc3fd5b769349f227e1a9b3`  
		Last Modified: Tue, 14 Jan 2025 20:50:12 GMT  
		Size: 18.9 MB (18947891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d20ef716e461c9fa3e7918407f16ce17c9f9710cab1161a154e8b50821a832`  
		Last Modified: Tue, 14 Jan 2025 20:35:34 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2d35c474eedb05b50fc3d3f76181e313d16e4c5444db8c649f5395af9f4f81`  
		Last Modified: Tue, 14 Jan 2025 03:24:03 GMT  
		Size: 66.3 MB (66285445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48821d19fdfec091fca9732b3ba4758fd1e80d38cf3c1199c9fab01c1ac12e4a`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:dbffdd0f28c27a8cbdf6bd2e2fbf8a48551827759352c050b33d956cc3a26688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6429049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207b8213be9cb2c88a1468ba829e5a1ffec175c7e94fda4d076572c10713c182`

```dockerfile
```

-	Layers:
	-	`sha256:de9f0c3eec9d974f71250141105982b693a91f2febdc02787640ce501d973967`  
		Last Modified: Tue, 14 Jan 2025 03:24:02 GMT  
		Size: 6.4 MB (6414580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2f9f7c99026dac2303b8a82b22efe5adf0c7580686fb51b5aa48c914ae6d42a`  
		Last Modified: Tue, 14 Jan 2025 03:24:02 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7ff0fbd66989213aa393376fb0fdefe0de69e20b164e3f88f0dbff993633a60e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145544445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d546b9c002da57b4c60ab4b5fc59369ae436a30e69bbf7513e7b1d73c496ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
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
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 20:44:11 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655f753857000d865814cd335d1b5bbde6d5763860fc3852ff72375ebf0d63eb`  
		Last Modified: Tue, 14 Jan 2025 17:59:40 GMT  
		Size: 17.7 MB (17725454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b904f7d9054ff68a043655602fd1acc5afc0ff9b27118fe50015641c990dd4`  
		Last Modified: Tue, 14 Jan 2025 21:38:36 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118072a03c656672df1ea738bb6ed4e2794b64a4c04185ed0f6c1da13b5a9305`  
		Last Modified: Tue, 14 Jan 2025 17:59:42 GMT  
		Size: 61.7 MB (61672309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ff036a008c545e31855bb2e65d283f7fe85bac031c4c4e83688059775684d7`  
		Last Modified: Wed, 15 Jan 2025 04:54:23 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:37fb02e402ee91b40d55c977f18a6db1ef1cf902330c6d5e12271f528598b1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1678d911c726c0cbf45fe72b1c19c430318279d62c28fcad8731f5caf5e59f11`

```dockerfile
```

-	Layers:
	-	`sha256:8fc86ae997f7978d6f3f84e3e699ac711cbb8652e671aeaabd568dacc276a52d`  
		Last Modified: Wed, 15 Jan 2025 04:54:23 GMT  
		Size: 6.4 MB (6409984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14078853615eecdd36326e073d2f1c18ecf2e885b036f9614fd3aaa699cae0b9`  
		Last Modified: Tue, 14 Jan 2025 17:59:39 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:b7d05b6b31be5ef14c1e56b48c6b7f71959e4a4d9ae795c205d20a1bb888f83b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151155985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69e251d8fd36880179f012156d103c51aaa2f07cf3b124f1acb5a3f795c263c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 20:33:16 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33795f8bcaccd45d2bfa5cf3246b685402b788022f2da882fe5e0d582f392da9`  
		Last Modified: Tue, 14 Jan 2025 20:44:04 GMT  
		Size: 18.9 MB (18870692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06a3eec8acfafd403112e32879e1f5cb55cf9494567e98f8c67e8bd16e7043`  
		Last Modified: Tue, 14 Jan 2025 20:40:47 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e65c62a6a4f2b03173b5531e48b9fcdb15e94cfa4e4df907b0b4b02e7bb3e33`  
		Last Modified: Wed, 15 Jan 2025 02:19:24 GMT  
		Size: 60.4 MB (60377779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebb35ddc124a8645631c28841e6a470f40139df321a0ae2b10b3bca20a90ddf`  
		Last Modified: Wed, 15 Jan 2025 01:46:38 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:a0e9664a88219fbeb07ce62cd19f2421bc121e244466d2c0c8d975ff35f3bc1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6430643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a99edb201e879f1f116a88f25c97517fcd24d5e6b85771335eb18169c175ac`

```dockerfile
```

-	Layers:
	-	`sha256:9662e55229c6a6a0f3d97480027d873894bf3a08578e95bd26186c72b076bf24`  
		Last Modified: Wed, 15 Jan 2025 02:25:47 GMT  
		Size: 6.4 MB (6416063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c8edb426cd9bb5b1086af41028dd873e7348e9ab2c5c923102424b0afd6928`  
		Last Modified: Tue, 14 Jan 2025 15:42:23 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31-alpine`

```console
$ docker pull telegraf@sha256:93e313e4f1683fa7aca89bad3aae490a3aa6b2272757ff9c9c15b9a6a51ad04c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:29e9b605caa346ae8c694414383b9cc2a2319f47d3a079afd2cc7dc80de32351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72154580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3953fb828c6e8d7a6f803e4b06e92f5e4e31165f3e38492988afe6a9f4dd6e5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Dec 2024 21:08:54 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468d1aecad0155c3d90e98277566dc27a141217f25ef85e8003fbc668659f2f2`  
		Last Modified: Wed, 08 Jan 2025 18:16:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82549f356bc75f4de167979912d7bebe8523c035eff811303e64fae27160d90c`  
		Last Modified: Tue, 14 Jan 2025 22:43:09 GMT  
		Size: 2.4 MB (2448110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffcdff2fd5699d6bc0e399178b4546e662761b1e15588eea68a161ae639e15e`  
		Last Modified: Wed, 08 Jan 2025 18:16:59 GMT  
		Size: 66.1 MB (66079603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05ed68a32610ae205abe1e20c7913b63467e67b954f7b240c0ec22c46748687`  
		Last Modified: Tue, 14 Jan 2025 20:49:00 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:63c5cdb72ba5b371e2d506be2ecac56565fbf891989936fe136f166cbb4f365f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1084258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13588094b5353fadc58d8e876f8ea23ece12a435cb31505cee6df8e14dcebe03`

```dockerfile
```

-	Layers:
	-	`sha256:e7dd33351529c9250deebb495f36b0bbd92be7df1d88d02034b260e8f5a63227`  
		Last Modified: Wed, 15 Jan 2025 00:49:49 GMT  
		Size: 1.1 MB (1069297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad63a6cbf6eeceb6367a166a67594bac4084a2f9d388bad707591dd37c6e593b`  
		Last Modified: Wed, 08 Jan 2025 18:16:57 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a2f2a638dbf972dd0171a0ecff843c0379f72a90083f1437db8b5e45f411fb10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66797096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196341707d85544215d87a51f3b1035c5b0086d99d01f6d22ab9b8e09ef7bf58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Dec 2024 21:08:54 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c7dafdb703875c4326b5e1c619a600f0cc7fe2b730986902401f7db9071f7`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b563c2c2e3fad2f23ba79a8de7332d3f0bd77ab6b2a39cbe7714e4393daf2f`  
		Last Modified: Tue, 14 Jan 2025 21:02:15 GMT  
		Size: 2.5 MB (2534054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52162d0ee6e9285992524e29892600906aa38022fcaf13a0bd96a6e887c4c81`  
		Last Modified: Wed, 15 Jan 2025 00:42:57 GMT  
		Size: 60.2 MB (60171665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcbf5b9147adc8d3381d8417765071dc1052e5cc541eb7f752b9ccc6b1aad78`  
		Last Modified: Thu, 09 Jan 2025 05:57:51 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:84b01ff4a3d1be79157b475296302dc73f0f30c59f22c4b3ca94c19083d19408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1080802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0ce3d34cb441e91bebd2907329b5ddd9fb710dd9465955373d995e7c437f78`

```dockerfile
```

-	Layers:
	-	`sha256:11cc2d4ac6cee0b48b626dd789fec7a50595c4d57bbdbae0b22bda5020c590b7`  
		Last Modified: Thu, 09 Jan 2025 05:57:51 GMT  
		Size: 1.1 MB (1065731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3e5eba2bb010278ea19a66f54b9e1415e64f43d8593426f1acd8d46e4ba8d20`  
		Last Modified: Thu, 09 Jan 2025 05:57:51 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.3`

```console
$ docker pull telegraf@sha256:86d756d0cfc06b89cdfbaed8e2522e3c74b67a591f92c21a462d837a12e16f8b
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
$ docker pull telegraf@sha256:a397bfe1283345f30fb2e4180416b9332062470e2d957cff079050bafa53b4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157774349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7451db0554ed5fef32cdc89807aedfaafe56151c024df02f24dd9c4c66105695`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 20:33:03 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6451a409900f515eb8afecb4d2b9d437859ea666bc3fd5b769349f227e1a9b3`  
		Last Modified: Tue, 14 Jan 2025 20:50:12 GMT  
		Size: 18.9 MB (18947891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d20ef716e461c9fa3e7918407f16ce17c9f9710cab1161a154e8b50821a832`  
		Last Modified: Tue, 14 Jan 2025 20:35:34 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2d35c474eedb05b50fc3d3f76181e313d16e4c5444db8c649f5395af9f4f81`  
		Last Modified: Tue, 14 Jan 2025 03:24:03 GMT  
		Size: 66.3 MB (66285445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48821d19fdfec091fca9732b3ba4758fd1e80d38cf3c1199c9fab01c1ac12e4a`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:dbffdd0f28c27a8cbdf6bd2e2fbf8a48551827759352c050b33d956cc3a26688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6429049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207b8213be9cb2c88a1468ba829e5a1ffec175c7e94fda4d076572c10713c182`

```dockerfile
```

-	Layers:
	-	`sha256:de9f0c3eec9d974f71250141105982b693a91f2febdc02787640ce501d973967`  
		Last Modified: Tue, 14 Jan 2025 03:24:02 GMT  
		Size: 6.4 MB (6414580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2f9f7c99026dac2303b8a82b22efe5adf0c7580686fb51b5aa48c914ae6d42a`  
		Last Modified: Tue, 14 Jan 2025 03:24:02 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7ff0fbd66989213aa393376fb0fdefe0de69e20b164e3f88f0dbff993633a60e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145544445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d546b9c002da57b4c60ab4b5fc59369ae436a30e69bbf7513e7b1d73c496ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
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
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 20:44:11 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655f753857000d865814cd335d1b5bbde6d5763860fc3852ff72375ebf0d63eb`  
		Last Modified: Tue, 14 Jan 2025 17:59:40 GMT  
		Size: 17.7 MB (17725454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b904f7d9054ff68a043655602fd1acc5afc0ff9b27118fe50015641c990dd4`  
		Last Modified: Tue, 14 Jan 2025 21:38:36 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118072a03c656672df1ea738bb6ed4e2794b64a4c04185ed0f6c1da13b5a9305`  
		Last Modified: Tue, 14 Jan 2025 17:59:42 GMT  
		Size: 61.7 MB (61672309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ff036a008c545e31855bb2e65d283f7fe85bac031c4c4e83688059775684d7`  
		Last Modified: Wed, 15 Jan 2025 04:54:23 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:37fb02e402ee91b40d55c977f18a6db1ef1cf902330c6d5e12271f528598b1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1678d911c726c0cbf45fe72b1c19c430318279d62c28fcad8731f5caf5e59f11`

```dockerfile
```

-	Layers:
	-	`sha256:8fc86ae997f7978d6f3f84e3e699ac711cbb8652e671aeaabd568dacc276a52d`  
		Last Modified: Wed, 15 Jan 2025 04:54:23 GMT  
		Size: 6.4 MB (6409984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14078853615eecdd36326e073d2f1c18ecf2e885b036f9614fd3aaa699cae0b9`  
		Last Modified: Tue, 14 Jan 2025 17:59:39 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:b7d05b6b31be5ef14c1e56b48c6b7f71959e4a4d9ae795c205d20a1bb888f83b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151155985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69e251d8fd36880179f012156d103c51aaa2f07cf3b124f1acb5a3f795c263c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 20:33:16 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33795f8bcaccd45d2bfa5cf3246b685402b788022f2da882fe5e0d582f392da9`  
		Last Modified: Tue, 14 Jan 2025 20:44:04 GMT  
		Size: 18.9 MB (18870692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06a3eec8acfafd403112e32879e1f5cb55cf9494567e98f8c67e8bd16e7043`  
		Last Modified: Tue, 14 Jan 2025 20:40:47 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e65c62a6a4f2b03173b5531e48b9fcdb15e94cfa4e4df907b0b4b02e7bb3e33`  
		Last Modified: Wed, 15 Jan 2025 02:19:24 GMT  
		Size: 60.4 MB (60377779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebb35ddc124a8645631c28841e6a470f40139df321a0ae2b10b3bca20a90ddf`  
		Last Modified: Wed, 15 Jan 2025 01:46:38 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:a0e9664a88219fbeb07ce62cd19f2421bc121e244466d2c0c8d975ff35f3bc1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6430643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a99edb201e879f1f116a88f25c97517fcd24d5e6b85771335eb18169c175ac`

```dockerfile
```

-	Layers:
	-	`sha256:9662e55229c6a6a0f3d97480027d873894bf3a08578e95bd26186c72b076bf24`  
		Last Modified: Wed, 15 Jan 2025 02:25:47 GMT  
		Size: 6.4 MB (6416063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c8edb426cd9bb5b1086af41028dd873e7348e9ab2c5c923102424b0afd6928`  
		Last Modified: Tue, 14 Jan 2025 15:42:23 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.3-alpine`

```console
$ docker pull telegraf@sha256:93e313e4f1683fa7aca89bad3aae490a3aa6b2272757ff9c9c15b9a6a51ad04c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:29e9b605caa346ae8c694414383b9cc2a2319f47d3a079afd2cc7dc80de32351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72154580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3953fb828c6e8d7a6f803e4b06e92f5e4e31165f3e38492988afe6a9f4dd6e5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Dec 2024 21:08:54 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468d1aecad0155c3d90e98277566dc27a141217f25ef85e8003fbc668659f2f2`  
		Last Modified: Wed, 08 Jan 2025 18:16:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82549f356bc75f4de167979912d7bebe8523c035eff811303e64fae27160d90c`  
		Last Modified: Tue, 14 Jan 2025 22:43:09 GMT  
		Size: 2.4 MB (2448110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffcdff2fd5699d6bc0e399178b4546e662761b1e15588eea68a161ae639e15e`  
		Last Modified: Wed, 08 Jan 2025 18:16:59 GMT  
		Size: 66.1 MB (66079603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05ed68a32610ae205abe1e20c7913b63467e67b954f7b240c0ec22c46748687`  
		Last Modified: Tue, 14 Jan 2025 20:49:00 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:63c5cdb72ba5b371e2d506be2ecac56565fbf891989936fe136f166cbb4f365f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1084258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13588094b5353fadc58d8e876f8ea23ece12a435cb31505cee6df8e14dcebe03`

```dockerfile
```

-	Layers:
	-	`sha256:e7dd33351529c9250deebb495f36b0bbd92be7df1d88d02034b260e8f5a63227`  
		Last Modified: Wed, 15 Jan 2025 00:49:49 GMT  
		Size: 1.1 MB (1069297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad63a6cbf6eeceb6367a166a67594bac4084a2f9d388bad707591dd37c6e593b`  
		Last Modified: Wed, 08 Jan 2025 18:16:57 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a2f2a638dbf972dd0171a0ecff843c0379f72a90083f1437db8b5e45f411fb10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66797096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196341707d85544215d87a51f3b1035c5b0086d99d01f6d22ab9b8e09ef7bf58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Dec 2024 21:08:54 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c7dafdb703875c4326b5e1c619a600f0cc7fe2b730986902401f7db9071f7`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b563c2c2e3fad2f23ba79a8de7332d3f0bd77ab6b2a39cbe7714e4393daf2f`  
		Last Modified: Tue, 14 Jan 2025 21:02:15 GMT  
		Size: 2.5 MB (2534054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52162d0ee6e9285992524e29892600906aa38022fcaf13a0bd96a6e887c4c81`  
		Last Modified: Wed, 15 Jan 2025 00:42:57 GMT  
		Size: 60.2 MB (60171665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcbf5b9147adc8d3381d8417765071dc1052e5cc541eb7f752b9ccc6b1aad78`  
		Last Modified: Thu, 09 Jan 2025 05:57:51 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:84b01ff4a3d1be79157b475296302dc73f0f30c59f22c4b3ca94c19083d19408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1080802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0ce3d34cb441e91bebd2907329b5ddd9fb710dd9465955373d995e7c437f78`

```dockerfile
```

-	Layers:
	-	`sha256:11cc2d4ac6cee0b48b626dd789fec7a50595c4d57bbdbae0b22bda5020c590b7`  
		Last Modified: Thu, 09 Jan 2025 05:57:51 GMT  
		Size: 1.1 MB (1065731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3e5eba2bb010278ea19a66f54b9e1415e64f43d8593426f1acd8d46e4ba8d20`  
		Last Modified: Thu, 09 Jan 2025 05:57:51 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32`

```console
$ docker pull telegraf@sha256:0ce6c553b4e37784d01cb70127acdd58f81da9615d611f8f886ef65f94785f29
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
$ docker pull telegraf@sha256:52f4613655e1f6634b6a25a35ca6dd74ae7546b7c8e533e3125783e3307f0fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161510041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f051d1b0852bda184830f0bd21fd89b55eba1ad6eb2e7379194952cff83b84`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 20:33:03 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab303d83e3b9fb141c228f738c9c3a96d55fb84b12642e0d8ee5243e3edd42f3`  
		Last Modified: Tue, 14 Jan 2025 20:34:23 GMT  
		Size: 18.9 MB (18947975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8693ba41d6abe8ff14c8ec7dc218bd34821bbc8d016f3e73d31a624c69f2960`  
		Last Modified: Tue, 14 Jan 2025 20:38:25 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88658b62c2fb61bdfc6966cc66381de4be194f9a42d485b7db107ae650b28020`  
		Last Modified: Tue, 14 Jan 2025 20:34:27 GMT  
		Size: 70.0 MB (70021052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49d1c971aba84d24dca09f90450a7a2c53a33eaa5f16e686e49b710da4bf6ee`  
		Last Modified: Tue, 14 Jan 2025 20:34:21 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:309dcc46985269333452d24e3ccf8379553fbcfe490130798ee6ba43ef5c081f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e6156bbd8cad07f8186294d79d8fe4212771f5d8db4d991efa2418d5783c87`

```dockerfile
```

-	Layers:
	-	`sha256:1fd6f4020df3bebe8dc7f631be1b5aee78016a3e40bdd242527179cd41a076ef`  
		Last Modified: Tue, 14 Jan 2025 03:24:32 GMT  
		Size: 6.4 MB (6424038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade60542fa0b7be2974b67fea666b08bf22a0c25c4716f052091c0881afab6a2`  
		Last Modified: Tue, 14 Jan 2025 03:24:31 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:342b633672b27da534717a26c687c0165032cf0c3b10530761fdac2dcadb0a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148555001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd58a4cceecbe1bfee5bdd7f990994c0d98023387f6e1a24335183c6af48d071`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
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
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 20:44:11 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655f753857000d865814cd335d1b5bbde6d5763860fc3852ff72375ebf0d63eb`  
		Last Modified: Tue, 14 Jan 2025 17:59:40 GMT  
		Size: 17.7 MB (17725454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b904f7d9054ff68a043655602fd1acc5afc0ff9b27118fe50015641c990dd4`  
		Last Modified: Tue, 14 Jan 2025 21:38:36 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6f90dc3f1069dd2f50d65681f06f13178a9e9696baee218e638376f7bf3e37`  
		Last Modified: Wed, 15 Jan 2025 04:54:44 GMT  
		Size: 64.7 MB (64682865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955c5ea9cae9c1a0b148caeb8e9f50d8e3b0609ff677c6703d2f1367eeaea7c6`  
		Last Modified: Wed, 15 Jan 2025 02:24:32 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:cd46471bd2f58db9ebee703d33268e719bafb45d4194b534bde17734c79a0a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6433997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9531d7fd42491b57b60949a8f0f8c154e5484c4b4fa4cc16ec62698126caf7e8`

```dockerfile
```

-	Layers:
	-	`sha256:417351c511eb52324e67e3696aeacb025189b3b352b740eff5fb530e06d85c0d`  
		Last Modified: Wed, 15 Jan 2025 02:24:36 GMT  
		Size: 6.4 MB (6419442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95713770d04c9210ec763e068fb436c3b7c37d0a5837d586aeb7d278d7f02dd1`  
		Last Modified: Tue, 14 Jan 2025 18:00:27 GMT  
		Size: 14.6 KB (14555 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2a4526438c6b1c8f00ba9234d619aa6ba81cd9eab4c370a479fee57060e24c58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153929717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eefb55db130daf89ee697ff7d38e2b2a33a0a7ff8e452c76e214e9730f5d5da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 20:33:16 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33795f8bcaccd45d2bfa5cf3246b685402b788022f2da882fe5e0d582f392da9`  
		Last Modified: Tue, 14 Jan 2025 20:44:04 GMT  
		Size: 18.9 MB (18870692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06a3eec8acfafd403112e32879e1f5cb55cf9494567e98f8c67e8bd16e7043`  
		Last Modified: Tue, 14 Jan 2025 20:40:47 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4216ebd57a5a2abf852d60cb9fb7bd8a8de833a6cf4956b58d654387523200b5`  
		Last Modified: Tue, 14 Jan 2025 15:42:58 GMT  
		Size: 63.2 MB (63151508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bd83dd815b3aafc81a0bfc2ebfd7ca00b8c151b783779faf66c8f913df7a0e`  
		Last Modified: Tue, 14 Jan 2025 21:06:26 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:bf86a806908c14e9508b457acc5189eb983bf7abdafd8983699ca620abaaa4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6439294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad4a52887263466cdc62530bbf48cae4ac6ddaad127c25ed988f141cabe1874`

```dockerfile
```

-	Layers:
	-	`sha256:5e140e9e3b7eafe95127c69b6a401e313cdb95a54ecd72aafbbe2caadc02861e`  
		Last Modified: Tue, 14 Jan 2025 15:42:56 GMT  
		Size: 6.4 MB (6424714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2251ac1ac4b50978c5ef7005ceb9f22c795b48f5ce2f9b18955099b5fac35d5f`  
		Last Modified: Tue, 14 Jan 2025 15:42:56 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32-alpine`

```console
$ docker pull telegraf@sha256:9b548aad77263ada594f2686b32b9de35f2b8c4a05aef09ef26e33e212d0d23f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:4d2659101482204300ca7e483cdb2e10fae827f8327176b5d0e0fe1d926332ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75899377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f84076c8c704db38f654f051504f2dae85c96f66f359e38c7de0337eac9adef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Dec 2024 21:08:54 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b890225f560541e48a5f0179cef47eed23912ee4d53196eca11fce0f695d65`  
		Last Modified: Wed, 08 Jan 2025 18:16:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1c5b2b7691b7ba253ab6932ac82877c22e9860136b5252c62649880a7864e8`  
		Last Modified: Tue, 14 Jan 2025 20:34:46 GMT  
		Size: 2.4 MB (2448063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3256316894cd81ef1d93e916036ac01554ca35d8079e17c8ffbd54bf14be84`  
		Last Modified: Wed, 08 Jan 2025 18:16:51 GMT  
		Size: 69.8 MB (69824447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2063fb4ac4811073d14df48a370dd28207788a97c61a24e09eec6d238d8f6b`  
		Last Modified: Tue, 14 Jan 2025 20:34:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:5d2ec22b94af0f3c69f6461632caaf2c3e6f59a839f6a55fb8ef548c503a0bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1093716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8607178d6f82b30fd68782fc0cd82482f97be156be1392157c1b5472c02b6a52`

```dockerfile
```

-	Layers:
	-	`sha256:2d0703d424793c953394f5d09d8259766068fdc907e8b2d612dcedd19d8296ea`  
		Last Modified: Wed, 08 Jan 2025 18:16:50 GMT  
		Size: 1.1 MB (1078755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c5cd16ba863559bfbaf01b9e10e431ac3712b992050ed3272da74ea08158e44`  
		Last Modified: Wed, 08 Jan 2025 18:16:50 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:1b8fad9e33d6d0928b8afb1842dac8888ca2905889ea4c100f63ab653bee0126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69569693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ab7ad56ea4dc6c682067b7865b4831ed13303cf0fb95dea4f010b8d02b3df0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Dec 2024 21:08:54 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c7dafdb703875c4326b5e1c619a600f0cc7fe2b730986902401f7db9071f7`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b563c2c2e3fad2f23ba79a8de7332d3f0bd77ab6b2a39cbe7714e4393daf2f`  
		Last Modified: Tue, 14 Jan 2025 21:02:15 GMT  
		Size: 2.5 MB (2534054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76be883812fa16c2b2933a2b42d8db4741fedab66eba8e95002375b5b5eee61f`  
		Last Modified: Tue, 14 Jan 2025 20:51:09 GMT  
		Size: 62.9 MB (62944261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b5c58f23b97b0b0fca27cba3dd58969fd67e429e26014cba326da3710862cb`  
		Last Modified: Thu, 09 Jan 2025 05:58:18 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:705d21521525581900da3ae17f2c687b61e507ac365954290403e054ef0519e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884104166e27ebead307e8a1419c8a0d4c930048342b11eb24a9650d44c42e61`

```dockerfile
```

-	Layers:
	-	`sha256:4cc452a64f0ae07c72130f895921ad75adb2a506f99af0509e1d566554a14089`  
		Last Modified: Thu, 09 Jan 2025 05:58:18 GMT  
		Size: 1.1 MB (1074382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa3ac68992776985fdccbfecafc86d547336f9b7ee0ceaeeac5929228d2307e3`  
		Last Modified: Thu, 09 Jan 2025 05:58:18 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32.3`

```console
$ docker pull telegraf@sha256:0ce6c553b4e37784d01cb70127acdd58f81da9615d611f8f886ef65f94785f29
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
$ docker pull telegraf@sha256:52f4613655e1f6634b6a25a35ca6dd74ae7546b7c8e533e3125783e3307f0fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161510041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f051d1b0852bda184830f0bd21fd89b55eba1ad6eb2e7379194952cff83b84`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 20:33:03 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab303d83e3b9fb141c228f738c9c3a96d55fb84b12642e0d8ee5243e3edd42f3`  
		Last Modified: Tue, 14 Jan 2025 20:34:23 GMT  
		Size: 18.9 MB (18947975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8693ba41d6abe8ff14c8ec7dc218bd34821bbc8d016f3e73d31a624c69f2960`  
		Last Modified: Tue, 14 Jan 2025 20:38:25 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88658b62c2fb61bdfc6966cc66381de4be194f9a42d485b7db107ae650b28020`  
		Last Modified: Tue, 14 Jan 2025 20:34:27 GMT  
		Size: 70.0 MB (70021052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49d1c971aba84d24dca09f90450a7a2c53a33eaa5f16e686e49b710da4bf6ee`  
		Last Modified: Tue, 14 Jan 2025 20:34:21 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:309dcc46985269333452d24e3ccf8379553fbcfe490130798ee6ba43ef5c081f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e6156bbd8cad07f8186294d79d8fe4212771f5d8db4d991efa2418d5783c87`

```dockerfile
```

-	Layers:
	-	`sha256:1fd6f4020df3bebe8dc7f631be1b5aee78016a3e40bdd242527179cd41a076ef`  
		Last Modified: Tue, 14 Jan 2025 03:24:32 GMT  
		Size: 6.4 MB (6424038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade60542fa0b7be2974b67fea666b08bf22a0c25c4716f052091c0881afab6a2`  
		Last Modified: Tue, 14 Jan 2025 03:24:31 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:342b633672b27da534717a26c687c0165032cf0c3b10530761fdac2dcadb0a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148555001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd58a4cceecbe1bfee5bdd7f990994c0d98023387f6e1a24335183c6af48d071`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
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
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 20:44:11 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655f753857000d865814cd335d1b5bbde6d5763860fc3852ff72375ebf0d63eb`  
		Last Modified: Tue, 14 Jan 2025 17:59:40 GMT  
		Size: 17.7 MB (17725454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b904f7d9054ff68a043655602fd1acc5afc0ff9b27118fe50015641c990dd4`  
		Last Modified: Tue, 14 Jan 2025 21:38:36 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6f90dc3f1069dd2f50d65681f06f13178a9e9696baee218e638376f7bf3e37`  
		Last Modified: Wed, 15 Jan 2025 04:54:44 GMT  
		Size: 64.7 MB (64682865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955c5ea9cae9c1a0b148caeb8e9f50d8e3b0609ff677c6703d2f1367eeaea7c6`  
		Last Modified: Wed, 15 Jan 2025 02:24:32 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:cd46471bd2f58db9ebee703d33268e719bafb45d4194b534bde17734c79a0a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6433997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9531d7fd42491b57b60949a8f0f8c154e5484c4b4fa4cc16ec62698126caf7e8`

```dockerfile
```

-	Layers:
	-	`sha256:417351c511eb52324e67e3696aeacb025189b3b352b740eff5fb530e06d85c0d`  
		Last Modified: Wed, 15 Jan 2025 02:24:36 GMT  
		Size: 6.4 MB (6419442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95713770d04c9210ec763e068fb436c3b7c37d0a5837d586aeb7d278d7f02dd1`  
		Last Modified: Tue, 14 Jan 2025 18:00:27 GMT  
		Size: 14.6 KB (14555 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2a4526438c6b1c8f00ba9234d619aa6ba81cd9eab4c370a479fee57060e24c58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153929717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eefb55db130daf89ee697ff7d38e2b2a33a0a7ff8e452c76e214e9730f5d5da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 20:33:16 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33795f8bcaccd45d2bfa5cf3246b685402b788022f2da882fe5e0d582f392da9`  
		Last Modified: Tue, 14 Jan 2025 20:44:04 GMT  
		Size: 18.9 MB (18870692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06a3eec8acfafd403112e32879e1f5cb55cf9494567e98f8c67e8bd16e7043`  
		Last Modified: Tue, 14 Jan 2025 20:40:47 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4216ebd57a5a2abf852d60cb9fb7bd8a8de833a6cf4956b58d654387523200b5`  
		Last Modified: Tue, 14 Jan 2025 15:42:58 GMT  
		Size: 63.2 MB (63151508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bd83dd815b3aafc81a0bfc2ebfd7ca00b8c151b783779faf66c8f913df7a0e`  
		Last Modified: Tue, 14 Jan 2025 21:06:26 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:bf86a806908c14e9508b457acc5189eb983bf7abdafd8983699ca620abaaa4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6439294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad4a52887263466cdc62530bbf48cae4ac6ddaad127c25ed988f141cabe1874`

```dockerfile
```

-	Layers:
	-	`sha256:5e140e9e3b7eafe95127c69b6a401e313cdb95a54ecd72aafbbe2caadc02861e`  
		Last Modified: Tue, 14 Jan 2025 15:42:56 GMT  
		Size: 6.4 MB (6424714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2251ac1ac4b50978c5ef7005ceb9f22c795b48f5ce2f9b18955099b5fac35d5f`  
		Last Modified: Tue, 14 Jan 2025 15:42:56 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32.3-alpine`

```console
$ docker pull telegraf@sha256:9b548aad77263ada594f2686b32b9de35f2b8c4a05aef09ef26e33e212d0d23f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:4d2659101482204300ca7e483cdb2e10fae827f8327176b5d0e0fe1d926332ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75899377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f84076c8c704db38f654f051504f2dae85c96f66f359e38c7de0337eac9adef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Dec 2024 21:08:54 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b890225f560541e48a5f0179cef47eed23912ee4d53196eca11fce0f695d65`  
		Last Modified: Wed, 08 Jan 2025 18:16:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1c5b2b7691b7ba253ab6932ac82877c22e9860136b5252c62649880a7864e8`  
		Last Modified: Tue, 14 Jan 2025 20:34:46 GMT  
		Size: 2.4 MB (2448063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3256316894cd81ef1d93e916036ac01554ca35d8079e17c8ffbd54bf14be84`  
		Last Modified: Wed, 08 Jan 2025 18:16:51 GMT  
		Size: 69.8 MB (69824447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2063fb4ac4811073d14df48a370dd28207788a97c61a24e09eec6d238d8f6b`  
		Last Modified: Tue, 14 Jan 2025 20:34:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:5d2ec22b94af0f3c69f6461632caaf2c3e6f59a839f6a55fb8ef548c503a0bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1093716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8607178d6f82b30fd68782fc0cd82482f97be156be1392157c1b5472c02b6a52`

```dockerfile
```

-	Layers:
	-	`sha256:2d0703d424793c953394f5d09d8259766068fdc907e8b2d612dcedd19d8296ea`  
		Last Modified: Wed, 08 Jan 2025 18:16:50 GMT  
		Size: 1.1 MB (1078755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c5cd16ba863559bfbaf01b9e10e431ac3712b992050ed3272da74ea08158e44`  
		Last Modified: Wed, 08 Jan 2025 18:16:50 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:1b8fad9e33d6d0928b8afb1842dac8888ca2905889ea4c100f63ab653bee0126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69569693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ab7ad56ea4dc6c682067b7865b4831ed13303cf0fb95dea4f010b8d02b3df0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Dec 2024 21:08:54 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c7dafdb703875c4326b5e1c619a600f0cc7fe2b730986902401f7db9071f7`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b563c2c2e3fad2f23ba79a8de7332d3f0bd77ab6b2a39cbe7714e4393daf2f`  
		Last Modified: Tue, 14 Jan 2025 21:02:15 GMT  
		Size: 2.5 MB (2534054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76be883812fa16c2b2933a2b42d8db4741fedab66eba8e95002375b5b5eee61f`  
		Last Modified: Tue, 14 Jan 2025 20:51:09 GMT  
		Size: 62.9 MB (62944261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b5c58f23b97b0b0fca27cba3dd58969fd67e429e26014cba326da3710862cb`  
		Last Modified: Thu, 09 Jan 2025 05:58:18 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:705d21521525581900da3ae17f2c687b61e507ac365954290403e054ef0519e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884104166e27ebead307e8a1419c8a0d4c930048342b11eb24a9650d44c42e61`

```dockerfile
```

-	Layers:
	-	`sha256:4cc452a64f0ae07c72130f895921ad75adb2a506f99af0509e1d566554a14089`  
		Last Modified: Thu, 09 Jan 2025 05:58:18 GMT  
		Size: 1.1 MB (1074382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa3ac68992776985fdccbfecafc86d547336f9b7ee0ceaeeac5929228d2307e3`  
		Last Modified: Thu, 09 Jan 2025 05:58:18 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33`

```console
$ docker pull telegraf@sha256:67761580048d0225b80189cd93029d5576779fb55681f73504e4199801d49324
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
$ docker pull telegraf@sha256:b4e7d1eb9f4710474c1e2f441b128050248b01c9709e05a5403b6adc5611e930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165724427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65f8a36bd73aa8a37ec1d2b158d29fcf2cc0f83573c1bc11f0c85215e1270bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.33.1
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
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 20:33:03 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e769155f8c228e7195ac76d14d49fc7ac87f7726cac2cbf61e930f28eae235f3`  
		Last Modified: Tue, 14 Jan 2025 20:33:25 GMT  
		Size: 18.9 MB (18947984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979b1b990bc7c07f284cffb80204001ee01cec2de81ad855d8b9c060c769da3d`  
		Last Modified: Tue, 14 Jan 2025 03:23:26 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a644d25c1fd4882d22828adeb34d1bb3125155eddb7112a1c33bd8b2389c4ae0`  
		Last Modified: Tue, 14 Jan 2025 20:33:48 GMT  
		Size: 74.2 MB (74235431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6038ddaa2c5af7e2b06edb6a99ca08cc87070f847fb5040cea3d687e499ec5b0`  
		Last Modified: Tue, 14 Jan 2025 20:33:12 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:ec137e9e679f32fbbe44c2e32bfcc8723f873ccb61756d9e94bf9bb772784fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6449224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be88a2aed43561201de06f563144a0f1a76039bd655e9fbbe46915861a5bc0d`

```dockerfile
```

-	Layers:
	-	`sha256:a1ce607cf5befceaf4d8dfc3da63dbc93b040de9cfd3f93083b8fe7853e790a3`  
		Last Modified: Tue, 14 Jan 2025 03:23:26 GMT  
		Size: 6.4 MB (6434452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ef9411cf75bb051d279a9ef0aa9dae9b96753965e03f239a21997d68402914f`  
		Last Modified: Tue, 14 Jan 2025 03:23:26 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:044f037465db31610863fddf48d531f1c164aa3b01d47bc8ce519792a7c953ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152380959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb5f5eed6e09b5f198be592f3abeb5ba98d5ed58aa210fd5a324d557c921992`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.33.1
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
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 20:44:11 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655f753857000d865814cd335d1b5bbde6d5763860fc3852ff72375ebf0d63eb`  
		Last Modified: Tue, 14 Jan 2025 17:59:40 GMT  
		Size: 17.7 MB (17725454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b904f7d9054ff68a043655602fd1acc5afc0ff9b27118fe50015641c990dd4`  
		Last Modified: Tue, 14 Jan 2025 21:38:36 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b123ff656fd5d9ca3182a8135c3befe3dd83738eddcdf00461bc4af05232b821`  
		Last Modified: Tue, 14 Jan 2025 22:36:03 GMT  
		Size: 68.5 MB (68508823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b5df2f480b6e8c372f60f92b7af2c255c87f40d921d8f1654bf9d4f64a0fd5`  
		Last Modified: Tue, 14 Jan 2025 21:38:47 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:5574cd0bfc4ecfb227e8e2eb6ad1b1f9ebb8bea7abf7af17523d4236c18c0df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6444730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c297fbddf0ab22cbefcf95b68423bdcabafb4ee28f73b43058e229432623971a`

```dockerfile
```

-	Layers:
	-	`sha256:5b0d3c961a1363515a133e93897c8d93db08fa3499d6e2f23343bb1760f19c0e`  
		Last Modified: Tue, 14 Jan 2025 18:01:16 GMT  
		Size: 6.4 MB (6429864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e79756e923c5ddbfabb40785313314ab3d9a6f2e781449b0cbf3fca7261a3e9d`  
		Last Modified: Tue, 14 Jan 2025 18:01:15 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:b7b7a2d134bc06447dcb786ab156de386501428f25a1847958302fea6f232447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157830866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13827bc555fff384f02371349823f49932949d52157d2cea61a91c63a0a7fcb1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.33.1
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
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 20:33:16 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33795f8bcaccd45d2bfa5cf3246b685402b788022f2da882fe5e0d582f392da9`  
		Last Modified: Tue, 14 Jan 2025 20:44:04 GMT  
		Size: 18.9 MB (18870692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06a3eec8acfafd403112e32879e1f5cb55cf9494567e98f8c67e8bd16e7043`  
		Last Modified: Tue, 14 Jan 2025 20:40:47 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6ceebed07ed12f9bb9d6c5bf6078c54950d717df7884f5f6e15b1391f25519`  
		Last Modified: Tue, 14 Jan 2025 15:43:30 GMT  
		Size: 67.1 MB (67052658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5366b624625c0a857050aba8b4e7932733a10f08e8372335a05fa107d54d32ed`  
		Last Modified: Tue, 14 Jan 2025 20:36:39 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:bee7d21c3b5ca6ad03f7eceb1018b0f671323458ede8e980caf1f4b8203920ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6450034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5810128f3c7c05b2d076420fefd5bc7da54c969b09e3905a95b90b1f4b35333f`

```dockerfile
```

-	Layers:
	-	`sha256:81499de1aa02b3aeafcd94bf13c54f784a65d97cafbfda84634c54762fe743f7`  
		Last Modified: Wed, 15 Jan 2025 00:05:34 GMT  
		Size: 6.4 MB (6435140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b04e82c3277e0399a29dd9860b09f4de85b67be6740df6b02126102b4c0b34a2`  
		Last Modified: Wed, 15 Jan 2025 00:05:33 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33-alpine`

```console
$ docker pull telegraf@sha256:031c67f0c987be80f944bf16074bb9e5113f3f8441b4e61f0d324068c4553db0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:ed89ccce0ba5c1e22561da653f45564ee14537b5e40640c01e5a5b989f5e063d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80114424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4665f1a5b74d710be9bf7784bc0e55687dd7fe20ee37aedc9ae513fea4930edb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.33.1
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059d2095d35a08d80370f68ac131ab5f15066f151e56c673974e6c2cacafbdd6`  
		Last Modified: Fri, 10 Jan 2025 23:28:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c3a5bdb69a75280aa2a7df2decfa66b3a427acaa1d3276cb536a580ee55953`  
		Last Modified: Tue, 14 Jan 2025 20:38:19 GMT  
		Size: 2.4 MB (2448123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b6b9ca35df170e1aa138604567e5f1042a9fde9419d5369ed572b434bac31f`  
		Last Modified: Tue, 14 Jan 2025 20:44:37 GMT  
		Size: 74.0 MB (74039433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d3acac1c57c8a349847c31d862fa454c71203826be9a72aa8a1a785415b383`  
		Last Modified: Tue, 14 Jan 2025 20:38:20 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:ecfe34882d56634706f0525a40dd6f3a0657f9301d4ad5d7cfa7727ac673e19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1104432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f42d85d471c7f797d96db61c6eea31257fdff9535faf5e765e8cdcc7b8dcde`

```dockerfile
```

-	Layers:
	-	`sha256:57d500fbfabaa368ee8dc850a5c910b4a17eaed2847a31fca088b8aa178d7565`  
		Last Modified: Fri, 10 Jan 2025 23:28:09 GMT  
		Size: 1.1 MB (1089169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068ffb81e2fd6d0dbca63501a54f965c7d7e9988d8ec00cfed296a2501c71038`  
		Last Modified: Fri, 10 Jan 2025 23:28:08 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e8173b35a1db201923d5ad91edf934b855f34c9c8e403eb2f7a88646ce3ceeac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73475479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602b685b59370c53c76f45edab5aca5aec1e73539e5c633e9dde043b10deb041`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.33.1
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c7dafdb703875c4326b5e1c619a600f0cc7fe2b730986902401f7db9071f7`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b563c2c2e3fad2f23ba79a8de7332d3f0bd77ab6b2a39cbe7714e4393daf2f`  
		Last Modified: Tue, 14 Jan 2025 21:02:15 GMT  
		Size: 2.5 MB (2534054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22843d819a8c6a0582f154a5307137db1f41b292018adeb28f7ee6740024e68b`  
		Last Modified: Wed, 15 Jan 2025 00:44:26 GMT  
		Size: 66.9 MB (66850048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6535fb7a213099119cdbfc118af1a690ffec6302dd9f9ff3f09c2fcf22f296`  
		Last Modified: Fri, 10 Jan 2025 23:28:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:cb7e04ffebce2efcdd7c4bde07494b51f1298bed28507c9a81c80c63a8bf7987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1100193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8cacf3c8c448cab071fb15327ded70625061b450270ff8224e8b0c9d3fc040`

```dockerfile
```

-	Layers:
	-	`sha256:69b595d9bf1e6717fa574fbbb066f6b0b3888da9bdf6cdb8e08a97c135351979`  
		Last Modified: Fri, 10 Jan 2025 23:28:35 GMT  
		Size: 1.1 MB (1084808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80da2d3dca9d5e86aaf7ddb8eab46a8bc8f382ef4cc59573c9ae048116f64274`  
		Last Modified: Fri, 10 Jan 2025 23:28:35 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33.1`

```console
$ docker pull telegraf@sha256:67761580048d0225b80189cd93029d5576779fb55681f73504e4199801d49324
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33.1` - linux; amd64

```console
$ docker pull telegraf@sha256:b4e7d1eb9f4710474c1e2f441b128050248b01c9709e05a5403b6adc5611e930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165724427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65f8a36bd73aa8a37ec1d2b158d29fcf2cc0f83573c1bc11f0c85215e1270bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.33.1
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
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 20:33:03 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e769155f8c228e7195ac76d14d49fc7ac87f7726cac2cbf61e930f28eae235f3`  
		Last Modified: Tue, 14 Jan 2025 20:33:25 GMT  
		Size: 18.9 MB (18947984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979b1b990bc7c07f284cffb80204001ee01cec2de81ad855d8b9c060c769da3d`  
		Last Modified: Tue, 14 Jan 2025 03:23:26 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a644d25c1fd4882d22828adeb34d1bb3125155eddb7112a1c33bd8b2389c4ae0`  
		Last Modified: Tue, 14 Jan 2025 20:33:48 GMT  
		Size: 74.2 MB (74235431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6038ddaa2c5af7e2b06edb6a99ca08cc87070f847fb5040cea3d687e499ec5b0`  
		Last Modified: Tue, 14 Jan 2025 20:33:12 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:ec137e9e679f32fbbe44c2e32bfcc8723f873ccb61756d9e94bf9bb772784fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6449224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be88a2aed43561201de06f563144a0f1a76039bd655e9fbbe46915861a5bc0d`

```dockerfile
```

-	Layers:
	-	`sha256:a1ce607cf5befceaf4d8dfc3da63dbc93b040de9cfd3f93083b8fe7853e790a3`  
		Last Modified: Tue, 14 Jan 2025 03:23:26 GMT  
		Size: 6.4 MB (6434452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ef9411cf75bb051d279a9ef0aa9dae9b96753965e03f239a21997d68402914f`  
		Last Modified: Tue, 14 Jan 2025 03:23:26 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.1` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:044f037465db31610863fddf48d531f1c164aa3b01d47bc8ce519792a7c953ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152380959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb5f5eed6e09b5f198be592f3abeb5ba98d5ed58aa210fd5a324d557c921992`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.33.1
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
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 20:44:11 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655f753857000d865814cd335d1b5bbde6d5763860fc3852ff72375ebf0d63eb`  
		Last Modified: Tue, 14 Jan 2025 17:59:40 GMT  
		Size: 17.7 MB (17725454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b904f7d9054ff68a043655602fd1acc5afc0ff9b27118fe50015641c990dd4`  
		Last Modified: Tue, 14 Jan 2025 21:38:36 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b123ff656fd5d9ca3182a8135c3befe3dd83738eddcdf00461bc4af05232b821`  
		Last Modified: Tue, 14 Jan 2025 22:36:03 GMT  
		Size: 68.5 MB (68508823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b5df2f480b6e8c372f60f92b7af2c255c87f40d921d8f1654bf9d4f64a0fd5`  
		Last Modified: Tue, 14 Jan 2025 21:38:47 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:5574cd0bfc4ecfb227e8e2eb6ad1b1f9ebb8bea7abf7af17523d4236c18c0df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6444730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c297fbddf0ab22cbefcf95b68423bdcabafb4ee28f73b43058e229432623971a`

```dockerfile
```

-	Layers:
	-	`sha256:5b0d3c961a1363515a133e93897c8d93db08fa3499d6e2f23343bb1760f19c0e`  
		Last Modified: Tue, 14 Jan 2025 18:01:16 GMT  
		Size: 6.4 MB (6429864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e79756e923c5ddbfabb40785313314ab3d9a6f2e781449b0cbf3fca7261a3e9d`  
		Last Modified: Tue, 14 Jan 2025 18:01:15 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.1` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:b7b7a2d134bc06447dcb786ab156de386501428f25a1847958302fea6f232447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157830866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13827bc555fff384f02371349823f49932949d52157d2cea61a91c63a0a7fcb1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.33.1
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
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 20:33:16 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33795f8bcaccd45d2bfa5cf3246b685402b788022f2da882fe5e0d582f392da9`  
		Last Modified: Tue, 14 Jan 2025 20:44:04 GMT  
		Size: 18.9 MB (18870692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06a3eec8acfafd403112e32879e1f5cb55cf9494567e98f8c67e8bd16e7043`  
		Last Modified: Tue, 14 Jan 2025 20:40:47 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6ceebed07ed12f9bb9d6c5bf6078c54950d717df7884f5f6e15b1391f25519`  
		Last Modified: Tue, 14 Jan 2025 15:43:30 GMT  
		Size: 67.1 MB (67052658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5366b624625c0a857050aba8b4e7932733a10f08e8372335a05fa107d54d32ed`  
		Last Modified: Tue, 14 Jan 2025 20:36:39 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:bee7d21c3b5ca6ad03f7eceb1018b0f671323458ede8e980caf1f4b8203920ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6450034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5810128f3c7c05b2d076420fefd5bc7da54c969b09e3905a95b90b1f4b35333f`

```dockerfile
```

-	Layers:
	-	`sha256:81499de1aa02b3aeafcd94bf13c54f784a65d97cafbfda84634c54762fe743f7`  
		Last Modified: Wed, 15 Jan 2025 00:05:34 GMT  
		Size: 6.4 MB (6435140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b04e82c3277e0399a29dd9860b09f4de85b67be6740df6b02126102b4c0b34a2`  
		Last Modified: Wed, 15 Jan 2025 00:05:33 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33.1-alpine`

```console
$ docker pull telegraf@sha256:031c67f0c987be80f944bf16074bb9e5113f3f8441b4e61f0d324068c4553db0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33.1-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:ed89ccce0ba5c1e22561da653f45564ee14537b5e40640c01e5a5b989f5e063d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80114424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4665f1a5b74d710be9bf7784bc0e55687dd7fe20ee37aedc9ae513fea4930edb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.33.1
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059d2095d35a08d80370f68ac131ab5f15066f151e56c673974e6c2cacafbdd6`  
		Last Modified: Fri, 10 Jan 2025 23:28:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c3a5bdb69a75280aa2a7df2decfa66b3a427acaa1d3276cb536a580ee55953`  
		Last Modified: Tue, 14 Jan 2025 20:38:19 GMT  
		Size: 2.4 MB (2448123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b6b9ca35df170e1aa138604567e5f1042a9fde9419d5369ed572b434bac31f`  
		Last Modified: Tue, 14 Jan 2025 20:44:37 GMT  
		Size: 74.0 MB (74039433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d3acac1c57c8a349847c31d862fa454c71203826be9a72aa8a1a785415b383`  
		Last Modified: Tue, 14 Jan 2025 20:38:20 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.1-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:ecfe34882d56634706f0525a40dd6f3a0657f9301d4ad5d7cfa7727ac673e19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1104432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f42d85d471c7f797d96db61c6eea31257fdff9535faf5e765e8cdcc7b8dcde`

```dockerfile
```

-	Layers:
	-	`sha256:57d500fbfabaa368ee8dc850a5c910b4a17eaed2847a31fca088b8aa178d7565`  
		Last Modified: Fri, 10 Jan 2025 23:28:09 GMT  
		Size: 1.1 MB (1089169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068ffb81e2fd6d0dbca63501a54f965c7d7e9988d8ec00cfed296a2501c71038`  
		Last Modified: Fri, 10 Jan 2025 23:28:08 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.1-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e8173b35a1db201923d5ad91edf934b855f34c9c8e403eb2f7a88646ce3ceeac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73475479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602b685b59370c53c76f45edab5aca5aec1e73539e5c633e9dde043b10deb041`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.33.1
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c7dafdb703875c4326b5e1c619a600f0cc7fe2b730986902401f7db9071f7`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b563c2c2e3fad2f23ba79a8de7332d3f0bd77ab6b2a39cbe7714e4393daf2f`  
		Last Modified: Tue, 14 Jan 2025 21:02:15 GMT  
		Size: 2.5 MB (2534054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22843d819a8c6a0582f154a5307137db1f41b292018adeb28f7ee6740024e68b`  
		Last Modified: Wed, 15 Jan 2025 00:44:26 GMT  
		Size: 66.9 MB (66850048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6535fb7a213099119cdbfc118af1a690ffec6302dd9f9ff3f09c2fcf22f296`  
		Last Modified: Fri, 10 Jan 2025 23:28:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.1-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:cb7e04ffebce2efcdd7c4bde07494b51f1298bed28507c9a81c80c63a8bf7987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1100193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8cacf3c8c448cab071fb15327ded70625061b450270ff8224e8b0c9d3fc040`

```dockerfile
```

-	Layers:
	-	`sha256:69b595d9bf1e6717fa574fbbb066f6b0b3888da9bdf6cdb8e08a97c135351979`  
		Last Modified: Fri, 10 Jan 2025 23:28:35 GMT  
		Size: 1.1 MB (1084808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80da2d3dca9d5e86aaf7ddb8eab46a8bc8f382ef4cc59573c9ae048116f64274`  
		Last Modified: Fri, 10 Jan 2025 23:28:35 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:031c67f0c987be80f944bf16074bb9e5113f3f8441b4e61f0d324068c4553db0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:ed89ccce0ba5c1e22561da653f45564ee14537b5e40640c01e5a5b989f5e063d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80114424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4665f1a5b74d710be9bf7784bc0e55687dd7fe20ee37aedc9ae513fea4930edb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.33.1
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059d2095d35a08d80370f68ac131ab5f15066f151e56c673974e6c2cacafbdd6`  
		Last Modified: Fri, 10 Jan 2025 23:28:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c3a5bdb69a75280aa2a7df2decfa66b3a427acaa1d3276cb536a580ee55953`  
		Last Modified: Tue, 14 Jan 2025 20:38:19 GMT  
		Size: 2.4 MB (2448123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b6b9ca35df170e1aa138604567e5f1042a9fde9419d5369ed572b434bac31f`  
		Last Modified: Tue, 14 Jan 2025 20:44:37 GMT  
		Size: 74.0 MB (74039433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d3acac1c57c8a349847c31d862fa454c71203826be9a72aa8a1a785415b383`  
		Last Modified: Tue, 14 Jan 2025 20:38:20 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:ecfe34882d56634706f0525a40dd6f3a0657f9301d4ad5d7cfa7727ac673e19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1104432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f42d85d471c7f797d96db61c6eea31257fdff9535faf5e765e8cdcc7b8dcde`

```dockerfile
```

-	Layers:
	-	`sha256:57d500fbfabaa368ee8dc850a5c910b4a17eaed2847a31fca088b8aa178d7565`  
		Last Modified: Fri, 10 Jan 2025 23:28:09 GMT  
		Size: 1.1 MB (1089169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068ffb81e2fd6d0dbca63501a54f965c7d7e9988d8ec00cfed296a2501c71038`  
		Last Modified: Fri, 10 Jan 2025 23:28:08 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e8173b35a1db201923d5ad91edf934b855f34c9c8e403eb2f7a88646ce3ceeac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73475479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602b685b59370c53c76f45edab5aca5aec1e73539e5c633e9dde043b10deb041`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.33.1
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c7dafdb703875c4326b5e1c619a600f0cc7fe2b730986902401f7db9071f7`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b563c2c2e3fad2f23ba79a8de7332d3f0bd77ab6b2a39cbe7714e4393daf2f`  
		Last Modified: Tue, 14 Jan 2025 21:02:15 GMT  
		Size: 2.5 MB (2534054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22843d819a8c6a0582f154a5307137db1f41b292018adeb28f7ee6740024e68b`  
		Last Modified: Wed, 15 Jan 2025 00:44:26 GMT  
		Size: 66.9 MB (66850048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6535fb7a213099119cdbfc118af1a690ffec6302dd9f9ff3f09c2fcf22f296`  
		Last Modified: Fri, 10 Jan 2025 23:28:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:cb7e04ffebce2efcdd7c4bde07494b51f1298bed28507c9a81c80c63a8bf7987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1100193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8cacf3c8c448cab071fb15327ded70625061b450270ff8224e8b0c9d3fc040`

```dockerfile
```

-	Layers:
	-	`sha256:69b595d9bf1e6717fa574fbbb066f6b0b3888da9bdf6cdb8e08a97c135351979`  
		Last Modified: Fri, 10 Jan 2025 23:28:35 GMT  
		Size: 1.1 MB (1084808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80da2d3dca9d5e86aaf7ddb8eab46a8bc8f382ef4cc59573c9ae048116f64274`  
		Last Modified: Fri, 10 Jan 2025 23:28:35 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:67761580048d0225b80189cd93029d5576779fb55681f73504e4199801d49324
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
$ docker pull telegraf@sha256:b4e7d1eb9f4710474c1e2f441b128050248b01c9709e05a5403b6adc5611e930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165724427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65f8a36bd73aa8a37ec1d2b158d29fcf2cc0f83573c1bc11f0c85215e1270bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.33.1
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
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 20:33:03 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e769155f8c228e7195ac76d14d49fc7ac87f7726cac2cbf61e930f28eae235f3`  
		Last Modified: Tue, 14 Jan 2025 20:33:25 GMT  
		Size: 18.9 MB (18947984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979b1b990bc7c07f284cffb80204001ee01cec2de81ad855d8b9c060c769da3d`  
		Last Modified: Tue, 14 Jan 2025 03:23:26 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a644d25c1fd4882d22828adeb34d1bb3125155eddb7112a1c33bd8b2389c4ae0`  
		Last Modified: Tue, 14 Jan 2025 20:33:48 GMT  
		Size: 74.2 MB (74235431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6038ddaa2c5af7e2b06edb6a99ca08cc87070f847fb5040cea3d687e499ec5b0`  
		Last Modified: Tue, 14 Jan 2025 20:33:12 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:ec137e9e679f32fbbe44c2e32bfcc8723f873ccb61756d9e94bf9bb772784fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6449224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be88a2aed43561201de06f563144a0f1a76039bd655e9fbbe46915861a5bc0d`

```dockerfile
```

-	Layers:
	-	`sha256:a1ce607cf5befceaf4d8dfc3da63dbc93b040de9cfd3f93083b8fe7853e790a3`  
		Last Modified: Tue, 14 Jan 2025 03:23:26 GMT  
		Size: 6.4 MB (6434452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ef9411cf75bb051d279a9ef0aa9dae9b96753965e03f239a21997d68402914f`  
		Last Modified: Tue, 14 Jan 2025 03:23:26 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:044f037465db31610863fddf48d531f1c164aa3b01d47bc8ce519792a7c953ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152380959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb5f5eed6e09b5f198be592f3abeb5ba98d5ed58aa210fd5a324d557c921992`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.33.1
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
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 20:44:11 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655f753857000d865814cd335d1b5bbde6d5763860fc3852ff72375ebf0d63eb`  
		Last Modified: Tue, 14 Jan 2025 17:59:40 GMT  
		Size: 17.7 MB (17725454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b904f7d9054ff68a043655602fd1acc5afc0ff9b27118fe50015641c990dd4`  
		Last Modified: Tue, 14 Jan 2025 21:38:36 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b123ff656fd5d9ca3182a8135c3befe3dd83738eddcdf00461bc4af05232b821`  
		Last Modified: Tue, 14 Jan 2025 22:36:03 GMT  
		Size: 68.5 MB (68508823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b5df2f480b6e8c372f60f92b7af2c255c87f40d921d8f1654bf9d4f64a0fd5`  
		Last Modified: Tue, 14 Jan 2025 21:38:47 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:5574cd0bfc4ecfb227e8e2eb6ad1b1f9ebb8bea7abf7af17523d4236c18c0df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6444730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c297fbddf0ab22cbefcf95b68423bdcabafb4ee28f73b43058e229432623971a`

```dockerfile
```

-	Layers:
	-	`sha256:5b0d3c961a1363515a133e93897c8d93db08fa3499d6e2f23343bb1760f19c0e`  
		Last Modified: Tue, 14 Jan 2025 18:01:16 GMT  
		Size: 6.4 MB (6429864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e79756e923c5ddbfabb40785313314ab3d9a6f2e781449b0cbf3fca7261a3e9d`  
		Last Modified: Tue, 14 Jan 2025 18:01:15 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:b7b7a2d134bc06447dcb786ab156de386501428f25a1847958302fea6f232447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157830866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13827bc555fff384f02371349823f49932949d52157d2cea61a91c63a0a7fcb1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.33.1
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
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 20:33:16 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33795f8bcaccd45d2bfa5cf3246b685402b788022f2da882fe5e0d582f392da9`  
		Last Modified: Tue, 14 Jan 2025 20:44:04 GMT  
		Size: 18.9 MB (18870692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06a3eec8acfafd403112e32879e1f5cb55cf9494567e98f8c67e8bd16e7043`  
		Last Modified: Tue, 14 Jan 2025 20:40:47 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6ceebed07ed12f9bb9d6c5bf6078c54950d717df7884f5f6e15b1391f25519`  
		Last Modified: Tue, 14 Jan 2025 15:43:30 GMT  
		Size: 67.1 MB (67052658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5366b624625c0a857050aba8b4e7932733a10f08e8372335a05fa107d54d32ed`  
		Last Modified: Tue, 14 Jan 2025 20:36:39 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:bee7d21c3b5ca6ad03f7eceb1018b0f671323458ede8e980caf1f4b8203920ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6450034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5810128f3c7c05b2d076420fefd5bc7da54c969b09e3905a95b90b1f4b35333f`

```dockerfile
```

-	Layers:
	-	`sha256:81499de1aa02b3aeafcd94bf13c54f784a65d97cafbfda84634c54762fe743f7`  
		Last Modified: Wed, 15 Jan 2025 00:05:34 GMT  
		Size: 6.4 MB (6435140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b04e82c3277e0399a29dd9860b09f4de85b67be6740df6b02126102b4c0b34a2`  
		Last Modified: Wed, 15 Jan 2025 00:05:33 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
