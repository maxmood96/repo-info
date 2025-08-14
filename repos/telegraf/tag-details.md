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
-	[`telegraf:1.35.3`](#telegraf1353)
-	[`telegraf:1.35.3-alpine`](#telegraf1353-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.33`

```console
$ docker pull telegraf@sha256:eedd6e957a54a2fac2962e9d0b888befccaf75a4dcfc0023f94ecdcf36239d66
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
$ docker pull telegraf@sha256:3499ea2051c9363fb198fca9ac55f63ea896d0ab063553905c313caf6e81e29e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168774064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29070b2729a392c6a83f21296178c1a032032e32ce939e62a705803d3dd48595`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.33.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8cb4e2e5841c27b179f01f4757c942a605a7d3847b3e9e1e06391e38b75a2c`  
		Last Modified: Tue, 12 Aug 2025 22:22:46 GMT  
		Size: 18.9 MB (18946278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f3bb332def2e1f53b8a6a5cbce44c70830b405fd853307cef83226176cbf5d`  
		Last Modified: Tue, 12 Aug 2025 22:22:36 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9547e30ea3874ffb5d00d9632c88c28960ce3bcdcc6995eedbad3287afd4625f`  
		Last Modified: Wed, 13 Aug 2025 00:12:37 GMT  
		Size: 77.3 MB (77310039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb949b15494f635413421f2a3f9a20d37d1cfbb060f60389d9b74cf93b7339e3`  
		Last Modified: Tue, 12 Aug 2025 22:22:39 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:4b40856a54ec3c8180acebdd11768dac7eaaf2280a55c13206af1b2758de31eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6631745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9913c42e7806979394f198ecf8c57b0df0fb07543d29a199bd9c1bf83cf4ca7b`

```dockerfile
```

-	Layers:
	-	`sha256:13923ced312959d3ce06ac8981a76c984e71b64bb56bda0d2750df99fce185ce`  
		Last Modified: Wed, 13 Aug 2025 00:10:40 GMT  
		Size: 6.6 MB (6617275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:222c234e3158764a214d8c6e537bafcc29b45b8c88fbd95ac259c90943ce23ae`  
		Last Modified: Wed, 13 Aug 2025 00:10:41 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:a00c76a46c09d6601be61b6bc46f4e918c8b6fd4e0224c5f53d0378502ea1cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154941769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b92177ab797c0aeb46483b4c7d1cb1d182a2dc084366d8d92e4dc43e301bf4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.33.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a06e9cd35e09740ec78f63d1179c1e1528d9cfd9686a0094a4655ebe70922c99`  
		Last Modified: Tue, 12 Aug 2025 20:46:18 GMT  
		Size: 44.2 MB (44209044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4756b55428372e77ee6ab2b6c5a35bda8bf113537f0ebde9510c43737f4249c`  
		Last Modified: Wed, 13 Aug 2025 00:15:08 GMT  
		Size: 21.9 MB (21929365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681fdff4dcb6359e721989060c3743deca10d1e73cef0d9b907513c9b4f320f4`  
		Last Modified: Wed, 13 Aug 2025 11:56:52 GMT  
		Size: 17.7 MB (17725068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797481eb709a7b6a93b1cc1814d1f5184123c7245ebd3cdd2c05ae8ebfff5d30`  
		Last Modified: Wed, 13 Aug 2025 11:14:56 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9cfc32b6df135dc46836b79233122ff79e0a72e3d3ff6bffbf88145883cd47`  
		Last Modified: Wed, 13 Aug 2025 11:56:57 GMT  
		Size: 71.1 MB (71075882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cbd6443edff4656b60aa2f8fb4dd7b0e30172738491105a56934bee7ff32c7`  
		Last Modified: Wed, 13 Aug 2025 11:56:59 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:2fe29771c663be3705758bc8b38cdfd2c0de4ba7ddcc565230aebdece6aa392e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3928b7a74653f1f99e039b9d3937d17cc97670b3c0ae43fb34416431758a60`

```dockerfile
```

-	Layers:
	-	`sha256:2e59a61a6466f494ce95211088e31e2d243daa5b456c4c5f741c6bdb63195d6f`  
		Last Modified: Wed, 13 Aug 2025 12:10:22 GMT  
		Size: 6.6 MB (6612679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f4887eeb735bc6487dce103a7d3d27297535077395395cd343a11be8195495`  
		Last Modified: Wed, 13 Aug 2025 12:10:23 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c2cc76c44fc3b69ddccc7df309af4f348520310d8e89c663a15ab6d7a9f3f70e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160386487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb2f49c952f18abb6367ec2a745207a6564204cfe796bc76907c16a97738b0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.33.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cff9c97e1a1ee42786188e1d1b57f6a2035d65b648178ac0262d0eba0c5c86d`  
		Last Modified: Wed, 13 Aug 2025 07:22:32 GMT  
		Size: 23.6 MB (23569847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b99cb526a2d2c2edce8225080365ce7d0a1289117aacac869f1c80eaed39a8`  
		Last Modified: Wed, 13 Aug 2025 18:10:42 GMT  
		Size: 18.9 MB (18872091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eece436e998d9c9c646d86bd4bacd2c6a80585a2eb2f8903fd22301a267692`  
		Last Modified: Wed, 13 Aug 2025 18:10:43 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada187ba803b9362c33fa5dfaa14bb82415864c787f6d4c92d92bd41b5a57cce`  
		Last Modified: Wed, 13 Aug 2025 18:15:41 GMT  
		Size: 69.6 MB (69599692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608bf763638f1151d07e3daf7a9dab826543fc82e31967d6f169c465e5163e72`  
		Last Modified: Wed, 13 Aug 2025 18:11:47 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:b67c11d338ee1caf8d0634220bf6bd56cc17135ed50ac169eea4853743f7aa46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbccdbbdc57f3f5b4db41e20e300e47df79b1a5c5a932594b908735a6066f721`

```dockerfile
```

-	Layers:
	-	`sha256:4a3aafa987377471c056efa04cc42cda6e82aa5dd78c4761b94f89651f7e1efd`  
		Last Modified: Wed, 13 Aug 2025 18:10:29 GMT  
		Size: 6.6 MB (6617951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afebf805cf7515da10bb3df2314a1d9e5eb707f0274e41afc0b73b96ac691361`  
		Last Modified: Wed, 13 Aug 2025 18:10:30 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33-alpine`

```console
$ docker pull telegraf@sha256:3ea0664bed1cacec5e6b463882dc43da9b33c9742d436ace35f157843aca9e40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:5be81b98ae6e3f3cb2e8bc6fd7ce30259795d16b2dde9de10af41a71f46ad022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83166797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827e2d9cb045d209bfbd704d40d29683968cf7a07dff33260a102b9541a6b907`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 08 Jul 2025 13:49:16 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENV TELEGRAF_VERSION=1.33.3
# Tue, 08 Jul 2025 13:49:16 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 08 Jul 2025 13:49:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a11f81e59a8f62537e7c6c6c6897c48e654167182797b719d2af1ad8b6cc14c`  
		Last Modified: Tue, 15 Jul 2025 19:30:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17baa4c72e8aeba0a94141eded59b380bc55475cd912e9344a0b9a35bccdeea`  
		Last Modified: Tue, 15 Jul 2025 19:30:07 GMT  
		Size: 2.4 MB (2439854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5781548725adc99168b12daed77bdc3a1dd984f692670c9d2462fd81ab4c61b7`  
		Last Modified: Tue, 15 Jul 2025 19:30:11 GMT  
		Size: 77.1 MB (77105860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e5e12654a500db3bbbbe8fdda6046f993256ad78f631ff3a59208a8392fd36`  
		Last Modified: Tue, 15 Jul 2025 19:29:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4373f8979063df550f4ed737990ec44af2145bcafad4c9870b35230aa7e97369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1108965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4ada5317f660878c67206e24a58fcebc29b80123bd3dc0b38764b1b4210bd0`

```dockerfile
```

-	Layers:
	-	`sha256:8c5ca65359616874ea3cd631e843c2c739800e3c52e89ff404aacb1a2391a2ac`  
		Last Modified: Tue, 15 Jul 2025 21:10:18 GMT  
		Size: 1.1 MB (1094004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:917c5ce556ffb7b80029ea0a0bf5c3f787b523e829ba4d8948b8ac2a9fbc52ec`  
		Last Modified: Tue, 15 Jul 2025 21:10:19 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:bf8a64d7da2ce6eacb9eee7bbdceb8b423c754c5f7173722fffda2db5f8989cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76005041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65abf29e620ff2969e8280b95c3689a9717ae8951aa9516d4cd7c463b59eb0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 08 Jul 2025 13:49:16 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENV TELEGRAF_VERSION=1.33.3
# Tue, 08 Jul 2025 13:49:16 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 08 Jul 2025 13:49:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa97d491d631a48e4505bc7c819c75f4b17b81cb0aa363976f80703a1234abb`  
		Last Modified: Wed, 16 Jul 2025 05:48:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e3d554c3bbc91882bf606a734d925d5ed86684e95c17dc1c4086533c11d92d`  
		Last Modified: Wed, 16 Jul 2025 05:48:12 GMT  
		Size: 2.5 MB (2521335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a9510cfc3a20aa58a318111518fbd3b23506ad1775b1ccd7530405f07b3f4c`  
		Last Modified: Wed, 16 Jul 2025 05:48:16 GMT  
		Size: 69.4 MB (69394730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268a91db8f1a8d2e1b87d2a29b2718d2314b327ce085ef24009c233906ecfa96`  
		Last Modified: Wed, 16 Jul 2025 05:48:11 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6f5fd109f87debcc9b851fa8b20b9e3c33eb2abcc8267777dfc524a0edd3cf59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1104701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc0f0c80cbe8fdf3612f6585d89f0cc4c099a662e16bf9e79b8b74a6d83333f1`

```dockerfile
```

-	Layers:
	-	`sha256:c2db24f0f00f677e7cec8f0d78ddbb336f3dbc822b7d2f404038336cbf6432cb`  
		Last Modified: Wed, 16 Jul 2025 09:10:20 GMT  
		Size: 1.1 MB (1089631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c3e669e261b86dc9fdb4fd46b866c066096f659998590d6882ddb6f38f0c21a`  
		Last Modified: Wed, 16 Jul 2025 09:10:21 GMT  
		Size: 15.1 KB (15070 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33.3`

```console
$ docker pull telegraf@sha256:eedd6e957a54a2fac2962e9d0b888befccaf75a4dcfc0023f94ecdcf36239d66
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
$ docker pull telegraf@sha256:3499ea2051c9363fb198fca9ac55f63ea896d0ab063553905c313caf6e81e29e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168774064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29070b2729a392c6a83f21296178c1a032032e32ce939e62a705803d3dd48595`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.33.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8cb4e2e5841c27b179f01f4757c942a605a7d3847b3e9e1e06391e38b75a2c`  
		Last Modified: Tue, 12 Aug 2025 22:22:46 GMT  
		Size: 18.9 MB (18946278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f3bb332def2e1f53b8a6a5cbce44c70830b405fd853307cef83226176cbf5d`  
		Last Modified: Tue, 12 Aug 2025 22:22:36 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9547e30ea3874ffb5d00d9632c88c28960ce3bcdcc6995eedbad3287afd4625f`  
		Last Modified: Wed, 13 Aug 2025 00:12:37 GMT  
		Size: 77.3 MB (77310039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb949b15494f635413421f2a3f9a20d37d1cfbb060f60389d9b74cf93b7339e3`  
		Last Modified: Tue, 12 Aug 2025 22:22:39 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:4b40856a54ec3c8180acebdd11768dac7eaaf2280a55c13206af1b2758de31eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6631745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9913c42e7806979394f198ecf8c57b0df0fb07543d29a199bd9c1bf83cf4ca7b`

```dockerfile
```

-	Layers:
	-	`sha256:13923ced312959d3ce06ac8981a76c984e71b64bb56bda0d2750df99fce185ce`  
		Last Modified: Wed, 13 Aug 2025 00:10:40 GMT  
		Size: 6.6 MB (6617275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:222c234e3158764a214d8c6e537bafcc29b45b8c88fbd95ac259c90943ce23ae`  
		Last Modified: Wed, 13 Aug 2025 00:10:41 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:a00c76a46c09d6601be61b6bc46f4e918c8b6fd4e0224c5f53d0378502ea1cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154941769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b92177ab797c0aeb46483b4c7d1cb1d182a2dc084366d8d92e4dc43e301bf4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.33.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a06e9cd35e09740ec78f63d1179c1e1528d9cfd9686a0094a4655ebe70922c99`  
		Last Modified: Tue, 12 Aug 2025 20:46:18 GMT  
		Size: 44.2 MB (44209044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4756b55428372e77ee6ab2b6c5a35bda8bf113537f0ebde9510c43737f4249c`  
		Last Modified: Wed, 13 Aug 2025 00:15:08 GMT  
		Size: 21.9 MB (21929365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681fdff4dcb6359e721989060c3743deca10d1e73cef0d9b907513c9b4f320f4`  
		Last Modified: Wed, 13 Aug 2025 11:56:52 GMT  
		Size: 17.7 MB (17725068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797481eb709a7b6a93b1cc1814d1f5184123c7245ebd3cdd2c05ae8ebfff5d30`  
		Last Modified: Wed, 13 Aug 2025 11:14:56 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9cfc32b6df135dc46836b79233122ff79e0a72e3d3ff6bffbf88145883cd47`  
		Last Modified: Wed, 13 Aug 2025 11:56:57 GMT  
		Size: 71.1 MB (71075882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cbd6443edff4656b60aa2f8fb4dd7b0e30172738491105a56934bee7ff32c7`  
		Last Modified: Wed, 13 Aug 2025 11:56:59 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:2fe29771c663be3705758bc8b38cdfd2c0de4ba7ddcc565230aebdece6aa392e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3928b7a74653f1f99e039b9d3937d17cc97670b3c0ae43fb34416431758a60`

```dockerfile
```

-	Layers:
	-	`sha256:2e59a61a6466f494ce95211088e31e2d243daa5b456c4c5f741c6bdb63195d6f`  
		Last Modified: Wed, 13 Aug 2025 12:10:22 GMT  
		Size: 6.6 MB (6612679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f4887eeb735bc6487dce103a7d3d27297535077395395cd343a11be8195495`  
		Last Modified: Wed, 13 Aug 2025 12:10:23 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c2cc76c44fc3b69ddccc7df309af4f348520310d8e89c663a15ab6d7a9f3f70e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160386487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb2f49c952f18abb6367ec2a745207a6564204cfe796bc76907c16a97738b0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.33.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cff9c97e1a1ee42786188e1d1b57f6a2035d65b648178ac0262d0eba0c5c86d`  
		Last Modified: Wed, 13 Aug 2025 07:22:32 GMT  
		Size: 23.6 MB (23569847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b99cb526a2d2c2edce8225080365ce7d0a1289117aacac869f1c80eaed39a8`  
		Last Modified: Wed, 13 Aug 2025 18:10:42 GMT  
		Size: 18.9 MB (18872091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eece436e998d9c9c646d86bd4bacd2c6a80585a2eb2f8903fd22301a267692`  
		Last Modified: Wed, 13 Aug 2025 18:10:43 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada187ba803b9362c33fa5dfaa14bb82415864c787f6d4c92d92bd41b5a57cce`  
		Last Modified: Wed, 13 Aug 2025 18:15:41 GMT  
		Size: 69.6 MB (69599692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608bf763638f1151d07e3daf7a9dab826543fc82e31967d6f169c465e5163e72`  
		Last Modified: Wed, 13 Aug 2025 18:11:47 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:b67c11d338ee1caf8d0634220bf6bd56cc17135ed50ac169eea4853743f7aa46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbccdbbdc57f3f5b4db41e20e300e47df79b1a5c5a932594b908735a6066f721`

```dockerfile
```

-	Layers:
	-	`sha256:4a3aafa987377471c056efa04cc42cda6e82aa5dd78c4761b94f89651f7e1efd`  
		Last Modified: Wed, 13 Aug 2025 18:10:29 GMT  
		Size: 6.6 MB (6617951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afebf805cf7515da10bb3df2314a1d9e5eb707f0274e41afc0b73b96ac691361`  
		Last Modified: Wed, 13 Aug 2025 18:10:30 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33.3-alpine`

```console
$ docker pull telegraf@sha256:3ea0664bed1cacec5e6b463882dc43da9b33c9742d436ace35f157843aca9e40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:5be81b98ae6e3f3cb2e8bc6fd7ce30259795d16b2dde9de10af41a71f46ad022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83166797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827e2d9cb045d209bfbd704d40d29683968cf7a07dff33260a102b9541a6b907`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 08 Jul 2025 13:49:16 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENV TELEGRAF_VERSION=1.33.3
# Tue, 08 Jul 2025 13:49:16 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 08 Jul 2025 13:49:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a11f81e59a8f62537e7c6c6c6897c48e654167182797b719d2af1ad8b6cc14c`  
		Last Modified: Tue, 15 Jul 2025 19:30:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17baa4c72e8aeba0a94141eded59b380bc55475cd912e9344a0b9a35bccdeea`  
		Last Modified: Tue, 15 Jul 2025 19:30:07 GMT  
		Size: 2.4 MB (2439854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5781548725adc99168b12daed77bdc3a1dd984f692670c9d2462fd81ab4c61b7`  
		Last Modified: Tue, 15 Jul 2025 19:30:11 GMT  
		Size: 77.1 MB (77105860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e5e12654a500db3bbbbe8fdda6046f993256ad78f631ff3a59208a8392fd36`  
		Last Modified: Tue, 15 Jul 2025 19:29:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4373f8979063df550f4ed737990ec44af2145bcafad4c9870b35230aa7e97369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1108965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4ada5317f660878c67206e24a58fcebc29b80123bd3dc0b38764b1b4210bd0`

```dockerfile
```

-	Layers:
	-	`sha256:8c5ca65359616874ea3cd631e843c2c739800e3c52e89ff404aacb1a2391a2ac`  
		Last Modified: Tue, 15 Jul 2025 21:10:18 GMT  
		Size: 1.1 MB (1094004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:917c5ce556ffb7b80029ea0a0bf5c3f787b523e829ba4d8948b8ac2a9fbc52ec`  
		Last Modified: Tue, 15 Jul 2025 21:10:19 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:bf8a64d7da2ce6eacb9eee7bbdceb8b423c754c5f7173722fffda2db5f8989cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76005041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65abf29e620ff2969e8280b95c3689a9717ae8951aa9516d4cd7c463b59eb0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 08 Jul 2025 13:49:16 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENV TELEGRAF_VERSION=1.33.3
# Tue, 08 Jul 2025 13:49:16 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 08 Jul 2025 13:49:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa97d491d631a48e4505bc7c819c75f4b17b81cb0aa363976f80703a1234abb`  
		Last Modified: Wed, 16 Jul 2025 05:48:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e3d554c3bbc91882bf606a734d925d5ed86684e95c17dc1c4086533c11d92d`  
		Last Modified: Wed, 16 Jul 2025 05:48:12 GMT  
		Size: 2.5 MB (2521335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a9510cfc3a20aa58a318111518fbd3b23506ad1775b1ccd7530405f07b3f4c`  
		Last Modified: Wed, 16 Jul 2025 05:48:16 GMT  
		Size: 69.4 MB (69394730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268a91db8f1a8d2e1b87d2a29b2718d2314b327ce085ef24009c233906ecfa96`  
		Last Modified: Wed, 16 Jul 2025 05:48:11 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6f5fd109f87debcc9b851fa8b20b9e3c33eb2abcc8267777dfc524a0edd3cf59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1104701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc0f0c80cbe8fdf3612f6585d89f0cc4c099a662e16bf9e79b8b74a6d83333f1`

```dockerfile
```

-	Layers:
	-	`sha256:c2db24f0f00f677e7cec8f0d78ddbb336f3dbc822b7d2f404038336cbf6432cb`  
		Last Modified: Wed, 16 Jul 2025 09:10:20 GMT  
		Size: 1.1 MB (1089631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c3e669e261b86dc9fdb4fd46b866c066096f659998590d6882ddb6f38f0c21a`  
		Last Modified: Wed, 16 Jul 2025 09:10:21 GMT  
		Size: 15.1 KB (15070 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34`

```console
$ docker pull telegraf@sha256:94e486bda487f8b8808a69ffd6837ca07aed87b28fe37298bbd0b5b22d2ba122
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
$ docker pull telegraf@sha256:6f63bdd8d8c3dec24e45366a158ba66d9208f75a3b49f52918c621d79b37f359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168910509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b04fc9ddcb97ff42077df31b0f6c185c9cb5fb2ecb6362216a496b68f33194d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bfaf0ca5bf58aaad6b75b80e5178a2140915933368b4bbda2842cfdbc5cfc3`  
		Last Modified: Tue, 12 Aug 2025 22:22:45 GMT  
		Size: 18.9 MB (18946634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5718a6d64d08d71aa41004bdc51a44152716d1d9cabbf5d855c006e3f771e5`  
		Last Modified: Tue, 12 Aug 2025 22:22:43 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5609a4ac164f17a1bdb412533bb5dacc7c836550daf0264d445d94ede2c455a9`  
		Last Modified: Tue, 12 Aug 2025 22:22:48 GMT  
		Size: 77.4 MB (77446113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464468d425e892719a75b3b4a8d1d2145a24d572c731cac29a26c36057c327f6`  
		Last Modified: Tue, 12 Aug 2025 22:22:43 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:4eb7db99e8b6eca26600d98b79e87fbfb259235eceac171b6c08b27a4e7a946a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6637917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fa06cbecfd7d6862c3d27ee564bbe438fa53e209c477af6b29471fb0076071`

```dockerfile
```

-	Layers:
	-	`sha256:d04587dfd71632d5c70f1e923cc066ab6fad8726a58e2f34e51e6657d3ea6ca8`  
		Last Modified: Wed, 13 Aug 2025 00:10:47 GMT  
		Size: 6.6 MB (6623447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efdd6fa20b3559577ecf7bca3b1478c4eaa5bc570c6d92b012a10018b622fcb1`  
		Last Modified: Wed, 13 Aug 2025 00:10:47 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:8525316727352245d3e5c7b722d16fcfeac7a1c9f37f55d3258ab536a4b76aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155392990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363a69bc528d9f8df25f08b20a9d4a874e27c0eeb23abe95db677a6d945eb752`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a06e9cd35e09740ec78f63d1179c1e1528d9cfd9686a0094a4655ebe70922c99`  
		Last Modified: Tue, 12 Aug 2025 20:46:18 GMT  
		Size: 44.2 MB (44209044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4756b55428372e77ee6ab2b6c5a35bda8bf113537f0ebde9510c43737f4249c`  
		Last Modified: Wed, 13 Aug 2025 00:15:08 GMT  
		Size: 21.9 MB (21929365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681fdff4dcb6359e721989060c3743deca10d1e73cef0d9b907513c9b4f320f4`  
		Last Modified: Wed, 13 Aug 2025 11:56:52 GMT  
		Size: 17.7 MB (17725068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797481eb709a7b6a93b1cc1814d1f5184123c7245ebd3cdd2c05ae8ebfff5d30`  
		Last Modified: Wed, 13 Aug 2025 11:14:56 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a08bafc8ea855b686695373cd2ea652e75ae58fdeed4ee6df05c6b7380360e`  
		Last Modified: Wed, 13 Aug 2025 12:15:52 GMT  
		Size: 71.5 MB (71527106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c1aad3aa39a8d033772df4776a79fcc3de3886a1bd13a25ab54727f3e1d885`  
		Last Modified: Wed, 13 Aug 2025 11:06:10 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:4d6e2026da42431b3027f14c66d6e44d30dee182d36c98b6a15872f0ea224fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c3f6ef1be33945a02effc04f83e3d6d64732b22fd6cde04ef785b8321ed813`

```dockerfile
```

-	Layers:
	-	`sha256:179a955cff8279332f7d7c0162d2d9fa481d454ad5eff5ac0b2014cd9701e918`  
		Last Modified: Wed, 13 Aug 2025 12:10:31 GMT  
		Size: 6.6 MB (6618042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a2f1d89afc20cb5b6f51a0748d3d72ae276415c6e4ef4b25317c4b3ed1c7a7e`  
		Last Modified: Wed, 13 Aug 2025 12:10:32 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d2471e2b808cd1ef46b20165ed47e6ab653f6b712313ec2b1b9d9a5ee9718a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160987850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb226dfa14bc321e3d183105223f17181e816fa53cfb3a9076958a2c110f8170`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cff9c97e1a1ee42786188e1d1b57f6a2035d65b648178ac0262d0eba0c5c86d`  
		Last Modified: Wed, 13 Aug 2025 07:22:32 GMT  
		Size: 23.6 MB (23569847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b99cb526a2d2c2edce8225080365ce7d0a1289117aacac869f1c80eaed39a8`  
		Last Modified: Wed, 13 Aug 2025 18:10:42 GMT  
		Size: 18.9 MB (18872091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eece436e998d9c9c646d86bd4bacd2c6a80585a2eb2f8903fd22301a267692`  
		Last Modified: Wed, 13 Aug 2025 18:10:43 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0acbcba6fbec2a91154c5131fa3dbc7af14befb4f6d0ced01191ce26978359`  
		Last Modified: Wed, 13 Aug 2025 18:15:52 GMT  
		Size: 70.2 MB (70201054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a89fc224e3e6e4a8817723f3b1ebe7e7f2a57d611f2f59384f73176ea7ccbe0`  
		Last Modified: Wed, 13 Aug 2025 18:11:47 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:e1673c2273664b06cb20efc0bcbd6f2b90b1686a82683b0d62c2bcd057661e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6638702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c9ef5ebb465f38d37b70ae220be240a04db341035610acc0fb0689316e48d4`

```dockerfile
```

-	Layers:
	-	`sha256:c448c01b96a365ad9c4dd1868cb3ee348ff5d1c17ece168b6b8fc657959e5831`  
		Last Modified: Wed, 13 Aug 2025 18:10:37 GMT  
		Size: 6.6 MB (6624123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be78c797231e62bda19d641d8c0538d73fcfe8cc3e05eb244f9500ee35504844`  
		Last Modified: Wed, 13 Aug 2025 18:10:38 GMT  
		Size: 14.6 KB (14579 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34-alpine`

```console
$ docker pull telegraf@sha256:9be449277b6e16b04c256e629f93828212eb22ab7078d8cfc31eabb8f235958e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e362bcc7d4ae010b3a0c3e4d8b1f9bf282889ad6f7ea994b2b3880e48c475013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83297830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95af6019e0f47aab1b15987c237287a5ef2e1b0b0ba2212a018af58df10444b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 08 Jul 2025 13:49:16 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 08 Jul 2025 13:49:16 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 08 Jul 2025 13:49:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0189be59b6d310438ecb57749d0b53be563f40ffe1756830daa09c83bef8415`  
		Last Modified: Tue, 15 Jul 2025 19:29:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849892cdebd263b6f41ddad1e9e9871a82acbc1ec12f6f6b59662c23a53ecbf1`  
		Last Modified: Tue, 15 Jul 2025 19:29:47 GMT  
		Size: 2.4 MB (2439839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316eafe4c20455456d584383463ddea70937a57b18aec6228e29596ee9de83a7`  
		Last Modified: Tue, 15 Jul 2025 19:30:07 GMT  
		Size: 77.2 MB (77236907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f076fa9b0654a47181d7442facaee6b922f57fa5852d7fc10dd0be83c120b346`  
		Last Modified: Tue, 15 Jul 2025 19:29:47 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e15eb7de3d16b848ef39912698dda6c995896e073b4008ad9600961cdb860db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1115137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f198cead148de598872801d73980fdb724789579180ff32cfe6f04947dad89a`

```dockerfile
```

-	Layers:
	-	`sha256:d3ea611838b71a81e7a7367547df6df24cef1c638e19546e4dc7e33cc7a068de`  
		Last Modified: Tue, 15 Jul 2025 21:10:26 GMT  
		Size: 1.1 MB (1100176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:625f67f8eb83f5062222a4600b78ea3fe502964fed0a9a5926fb7bc39e252874`  
		Last Modified: Tue, 15 Jul 2025 21:10:27 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5b64250fc700aeebd3f26215ece94e7341b6e7d58d45d99523b55053d6f91eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76607035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc67083c4f61db20b3105fe2cd30bcf445b17a5158845f1d0d70dce9347dbc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 08 Jul 2025 13:49:16 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 08 Jul 2025 13:49:16 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 08 Jul 2025 13:49:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa97d491d631a48e4505bc7c819c75f4b17b81cb0aa363976f80703a1234abb`  
		Last Modified: Wed, 16 Jul 2025 05:48:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e3d554c3bbc91882bf606a734d925d5ed86684e95c17dc1c4086533c11d92d`  
		Last Modified: Wed, 16 Jul 2025 05:48:12 GMT  
		Size: 2.5 MB (2521335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d0fd404ed95c46e6aea3a067faf07519cbf026660c39be7025cd50716ea7f2`  
		Last Modified: Wed, 16 Jul 2025 05:53:22 GMT  
		Size: 70.0 MB (69996726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8c75c3500cb4a7e076b1b9b4f29b7e03521b0ece8f93dd40ebd6daf77abb00`  
		Last Modified: Wed, 16 Jul 2025 05:53:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e3e029dcd13960995bf695390d4a2863fbd47f5a8130d6e768e12b90244327da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1110874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7223847de5ba827672f9a137203b3140516fd02c91cd068c3052bca535e9171`

```dockerfile
```

-	Layers:
	-	`sha256:011b777430464b8e65f955ffc476335083996826eff86889230201ccf2006966`  
		Last Modified: Wed, 16 Jul 2025 09:10:27 GMT  
		Size: 1.1 MB (1095803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de9bd2eeda1dc84918e31e2ed46ae9d5f948064f10caa04e320d93e42d3e633e`  
		Last Modified: Wed, 16 Jul 2025 09:10:28 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34.4`

```console
$ docker pull telegraf@sha256:94e486bda487f8b8808a69ffd6837ca07aed87b28fe37298bbd0b5b22d2ba122
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
$ docker pull telegraf@sha256:6f63bdd8d8c3dec24e45366a158ba66d9208f75a3b49f52918c621d79b37f359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168910509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b04fc9ddcb97ff42077df31b0f6c185c9cb5fb2ecb6362216a496b68f33194d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bfaf0ca5bf58aaad6b75b80e5178a2140915933368b4bbda2842cfdbc5cfc3`  
		Last Modified: Tue, 12 Aug 2025 22:22:45 GMT  
		Size: 18.9 MB (18946634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5718a6d64d08d71aa41004bdc51a44152716d1d9cabbf5d855c006e3f771e5`  
		Last Modified: Tue, 12 Aug 2025 22:22:43 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5609a4ac164f17a1bdb412533bb5dacc7c836550daf0264d445d94ede2c455a9`  
		Last Modified: Tue, 12 Aug 2025 22:22:48 GMT  
		Size: 77.4 MB (77446113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464468d425e892719a75b3b4a8d1d2145a24d572c731cac29a26c36057c327f6`  
		Last Modified: Tue, 12 Aug 2025 22:22:43 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:4eb7db99e8b6eca26600d98b79e87fbfb259235eceac171b6c08b27a4e7a946a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6637917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fa06cbecfd7d6862c3d27ee564bbe438fa53e209c477af6b29471fb0076071`

```dockerfile
```

-	Layers:
	-	`sha256:d04587dfd71632d5c70f1e923cc066ab6fad8726a58e2f34e51e6657d3ea6ca8`  
		Last Modified: Wed, 13 Aug 2025 00:10:47 GMT  
		Size: 6.6 MB (6623447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efdd6fa20b3559577ecf7bca3b1478c4eaa5bc570c6d92b012a10018b622fcb1`  
		Last Modified: Wed, 13 Aug 2025 00:10:47 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:8525316727352245d3e5c7b722d16fcfeac7a1c9f37f55d3258ab536a4b76aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155392990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363a69bc528d9f8df25f08b20a9d4a874e27c0eeb23abe95db677a6d945eb752`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a06e9cd35e09740ec78f63d1179c1e1528d9cfd9686a0094a4655ebe70922c99`  
		Last Modified: Tue, 12 Aug 2025 20:46:18 GMT  
		Size: 44.2 MB (44209044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4756b55428372e77ee6ab2b6c5a35bda8bf113537f0ebde9510c43737f4249c`  
		Last Modified: Wed, 13 Aug 2025 00:15:08 GMT  
		Size: 21.9 MB (21929365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681fdff4dcb6359e721989060c3743deca10d1e73cef0d9b907513c9b4f320f4`  
		Last Modified: Wed, 13 Aug 2025 11:56:52 GMT  
		Size: 17.7 MB (17725068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797481eb709a7b6a93b1cc1814d1f5184123c7245ebd3cdd2c05ae8ebfff5d30`  
		Last Modified: Wed, 13 Aug 2025 11:14:56 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a08bafc8ea855b686695373cd2ea652e75ae58fdeed4ee6df05c6b7380360e`  
		Last Modified: Wed, 13 Aug 2025 12:15:52 GMT  
		Size: 71.5 MB (71527106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c1aad3aa39a8d033772df4776a79fcc3de3886a1bd13a25ab54727f3e1d885`  
		Last Modified: Wed, 13 Aug 2025 11:06:10 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:4d6e2026da42431b3027f14c66d6e44d30dee182d36c98b6a15872f0ea224fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c3f6ef1be33945a02effc04f83e3d6d64732b22fd6cde04ef785b8321ed813`

```dockerfile
```

-	Layers:
	-	`sha256:179a955cff8279332f7d7c0162d2d9fa481d454ad5eff5ac0b2014cd9701e918`  
		Last Modified: Wed, 13 Aug 2025 12:10:31 GMT  
		Size: 6.6 MB (6618042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a2f1d89afc20cb5b6f51a0748d3d72ae276415c6e4ef4b25317c4b3ed1c7a7e`  
		Last Modified: Wed, 13 Aug 2025 12:10:32 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d2471e2b808cd1ef46b20165ed47e6ab653f6b712313ec2b1b9d9a5ee9718a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160987850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb226dfa14bc321e3d183105223f17181e816fa53cfb3a9076958a2c110f8170`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cff9c97e1a1ee42786188e1d1b57f6a2035d65b648178ac0262d0eba0c5c86d`  
		Last Modified: Wed, 13 Aug 2025 07:22:32 GMT  
		Size: 23.6 MB (23569847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b99cb526a2d2c2edce8225080365ce7d0a1289117aacac869f1c80eaed39a8`  
		Last Modified: Wed, 13 Aug 2025 18:10:42 GMT  
		Size: 18.9 MB (18872091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eece436e998d9c9c646d86bd4bacd2c6a80585a2eb2f8903fd22301a267692`  
		Last Modified: Wed, 13 Aug 2025 18:10:43 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0acbcba6fbec2a91154c5131fa3dbc7af14befb4f6d0ced01191ce26978359`  
		Last Modified: Wed, 13 Aug 2025 18:15:52 GMT  
		Size: 70.2 MB (70201054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a89fc224e3e6e4a8817723f3b1ebe7e7f2a57d611f2f59384f73176ea7ccbe0`  
		Last Modified: Wed, 13 Aug 2025 18:11:47 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:e1673c2273664b06cb20efc0bcbd6f2b90b1686a82683b0d62c2bcd057661e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6638702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c9ef5ebb465f38d37b70ae220be240a04db341035610acc0fb0689316e48d4`

```dockerfile
```

-	Layers:
	-	`sha256:c448c01b96a365ad9c4dd1868cb3ee348ff5d1c17ece168b6b8fc657959e5831`  
		Last Modified: Wed, 13 Aug 2025 18:10:37 GMT  
		Size: 6.6 MB (6624123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be78c797231e62bda19d641d8c0538d73fcfe8cc3e05eb244f9500ee35504844`  
		Last Modified: Wed, 13 Aug 2025 18:10:38 GMT  
		Size: 14.6 KB (14579 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34.4-alpine`

```console
$ docker pull telegraf@sha256:9be449277b6e16b04c256e629f93828212eb22ab7078d8cfc31eabb8f235958e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e362bcc7d4ae010b3a0c3e4d8b1f9bf282889ad6f7ea994b2b3880e48c475013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83297830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95af6019e0f47aab1b15987c237287a5ef2e1b0b0ba2212a018af58df10444b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 08 Jul 2025 13:49:16 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 08 Jul 2025 13:49:16 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 08 Jul 2025 13:49:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0189be59b6d310438ecb57749d0b53be563f40ffe1756830daa09c83bef8415`  
		Last Modified: Tue, 15 Jul 2025 19:29:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849892cdebd263b6f41ddad1e9e9871a82acbc1ec12f6f6b59662c23a53ecbf1`  
		Last Modified: Tue, 15 Jul 2025 19:29:47 GMT  
		Size: 2.4 MB (2439839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316eafe4c20455456d584383463ddea70937a57b18aec6228e29596ee9de83a7`  
		Last Modified: Tue, 15 Jul 2025 19:30:07 GMT  
		Size: 77.2 MB (77236907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f076fa9b0654a47181d7442facaee6b922f57fa5852d7fc10dd0be83c120b346`  
		Last Modified: Tue, 15 Jul 2025 19:29:47 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e15eb7de3d16b848ef39912698dda6c995896e073b4008ad9600961cdb860db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1115137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f198cead148de598872801d73980fdb724789579180ff32cfe6f04947dad89a`

```dockerfile
```

-	Layers:
	-	`sha256:d3ea611838b71a81e7a7367547df6df24cef1c638e19546e4dc7e33cc7a068de`  
		Last Modified: Tue, 15 Jul 2025 21:10:26 GMT  
		Size: 1.1 MB (1100176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:625f67f8eb83f5062222a4600b78ea3fe502964fed0a9a5926fb7bc39e252874`  
		Last Modified: Tue, 15 Jul 2025 21:10:27 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5b64250fc700aeebd3f26215ece94e7341b6e7d58d45d99523b55053d6f91eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76607035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc67083c4f61db20b3105fe2cd30bcf445b17a5158845f1d0d70dce9347dbc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 08 Jul 2025 13:49:16 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 08 Jul 2025 13:49:16 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 08 Jul 2025 13:49:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa97d491d631a48e4505bc7c819c75f4b17b81cb0aa363976f80703a1234abb`  
		Last Modified: Wed, 16 Jul 2025 05:48:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e3d554c3bbc91882bf606a734d925d5ed86684e95c17dc1c4086533c11d92d`  
		Last Modified: Wed, 16 Jul 2025 05:48:12 GMT  
		Size: 2.5 MB (2521335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d0fd404ed95c46e6aea3a067faf07519cbf026660c39be7025cd50716ea7f2`  
		Last Modified: Wed, 16 Jul 2025 05:53:22 GMT  
		Size: 70.0 MB (69996726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8c75c3500cb4a7e076b1b9b4f29b7e03521b0ece8f93dd40ebd6daf77abb00`  
		Last Modified: Wed, 16 Jul 2025 05:53:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e3e029dcd13960995bf695390d4a2863fbd47f5a8130d6e768e12b90244327da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1110874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7223847de5ba827672f9a137203b3140516fd02c91cd068c3052bca535e9171`

```dockerfile
```

-	Layers:
	-	`sha256:011b777430464b8e65f955ffc476335083996826eff86889230201ccf2006966`  
		Last Modified: Wed, 16 Jul 2025 09:10:27 GMT  
		Size: 1.1 MB (1095803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de9bd2eeda1dc84918e31e2ed46ae9d5f948064f10caa04e320d93e42d3e633e`  
		Last Modified: Wed, 16 Jul 2025 09:10:28 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35`

```console
$ docker pull telegraf@sha256:d55e33e698ae0e9d9bc0dfad33d100e7f2137ae53b65e4c8c090a79e0ee417ea
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
$ docker pull telegraf@sha256:d15a39d5d2b009728da553971935d0dac3811cfd9aa1c48d528eecbcf4b31bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.0 MB (170018463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eda2b8a73b1e01c0cf9efed0956db0475f3cd4d84469c2aea8d4182b7a7a750`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.35.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591ff18e55078b509b99ab7e3c869fc2f6ddc8d8930ed3358ae877682363fc00`  
		Last Modified: Tue, 12 Aug 2025 22:22:50 GMT  
		Size: 18.9 MB (18946345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19bb8c35abeeae86a2ada31b18685fd2cfcbf8fb5efc1fead517cffbb9cdf5c`  
		Last Modified: Tue, 12 Aug 2025 22:22:45 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7914e4fc6ae203ffe3e14eb402bb182f3bef3c806609359537faabb8938a2cc`  
		Last Modified: Tue, 12 Aug 2025 22:22:59 GMT  
		Size: 78.6 MB (78554361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35d9b51e6adbcc3a5dfdad293751b9af99909590f8ce37abce14c3be6558155`  
		Last Modified: Tue, 12 Aug 2025 22:22:47 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:6972ff8ec88a9249009bad5607cd05dafad830ecc9eb6a4b0236b865b233b2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6653160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de2e9d695e11a49c24bb75bc80fdbbe8296cd831bb220cc4be0e22935b0173b`

```dockerfile
```

-	Layers:
	-	`sha256:c492104500241dee5012e5aca9f3e7331ab282a43112b11bdbaee3108ecd9a0b`  
		Last Modified: Wed, 13 Aug 2025 00:10:53 GMT  
		Size: 6.6 MB (6638389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18c6a63414e56a2b879172f184f72bd9e7739a13795abd6cff7f8413d2fc900f`  
		Last Modified: Wed, 13 Aug 2025 00:10:54 GMT  
		Size: 14.8 KB (14771 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7e92274870845922c540933cac3ad588773324cd4dc9c24d710261dd3f5aeb0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156438798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6749fc9a90145eed636cfde43a431bb8ba2b5bcfd84b242ec1408c0d62ade75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.35.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a06e9cd35e09740ec78f63d1179c1e1528d9cfd9686a0094a4655ebe70922c99`  
		Last Modified: Tue, 12 Aug 2025 20:46:18 GMT  
		Size: 44.2 MB (44209044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4756b55428372e77ee6ab2b6c5a35bda8bf113537f0ebde9510c43737f4249c`  
		Last Modified: Wed, 13 Aug 2025 00:15:08 GMT  
		Size: 21.9 MB (21929365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681fdff4dcb6359e721989060c3743deca10d1e73cef0d9b907513c9b4f320f4`  
		Last Modified: Wed, 13 Aug 2025 11:56:52 GMT  
		Size: 17.7 MB (17725068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797481eb709a7b6a93b1cc1814d1f5184123c7245ebd3cdd2c05ae8ebfff5d30`  
		Last Modified: Wed, 13 Aug 2025 11:14:56 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f5973b04d4b80272b9a2f9c407ca321a873af327991f0e4aa1d17801deecd9`  
		Last Modified: Wed, 13 Aug 2025 11:07:01 GMT  
		Size: 72.6 MB (72572912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025c8f783802ef0617664dc4bcf86fcbe3490c943c930783ba4073bd7aeabe24`  
		Last Modified: Wed, 13 Aug 2025 11:06:58 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:f540acfe4ac4a1172bf8673094fd5d9a950d2e25a5cc595adb11ecb413ca92d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6647858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe1fab520699fec52069bb2da5e714552df2a91169116fb422752ee4c5d1e46`

```dockerfile
```

-	Layers:
	-	`sha256:b61f5a4f6e86fcf15d13171ee53d3cae4989c08fe5331e0a91f9a7c64737406f`  
		Last Modified: Wed, 13 Aug 2025 12:10:37 GMT  
		Size: 6.6 MB (6632992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6647686ae7885822c11bab2fad634a369381d65a2393bb4cbad3b2b609cbaa83`  
		Last Modified: Wed, 13 Aug 2025 12:10:38 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:904db379b4746d9df9946af2aad4eb087d0a7851d0cf82e97a05452594e3446c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (162014796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27bd61c58d5ec833e9e3fff27a5890cadd06457cf3026cc4491ab9aa971f22f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.35.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cff9c97e1a1ee42786188e1d1b57f6a2035d65b648178ac0262d0eba0c5c86d`  
		Last Modified: Wed, 13 Aug 2025 07:22:32 GMT  
		Size: 23.6 MB (23569847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b99cb526a2d2c2edce8225080365ce7d0a1289117aacac869f1c80eaed39a8`  
		Last Modified: Wed, 13 Aug 2025 18:10:42 GMT  
		Size: 18.9 MB (18872091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eece436e998d9c9c646d86bd4bacd2c6a80585a2eb2f8903fd22301a267692`  
		Last Modified: Wed, 13 Aug 2025 18:10:43 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f18cd58ac9516b123490b510c54b973bf1ed4d3d12e186b330ccc1f553f215b`  
		Last Modified: Wed, 13 Aug 2025 18:01:56 GMT  
		Size: 71.2 MB (71228002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fabf6fbd3169c71d4799024af77b9aaaf483781078168c3ad82816993090cf3`  
		Last Modified: Wed, 13 Aug 2025 18:01:53 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:49f46c47b0e01182228c8a81eae2cf320a5e5514302879d6b2cc71a010df89f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6653971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b737d49f451e3279ac7337c8af00fb52f5bfd995cb92aed8203528b0d690f39`

```dockerfile
```

-	Layers:
	-	`sha256:b329a08f9f729de3d5dc78c5dbcdc375e08637204261d377168b97e990fb032b`  
		Last Modified: Wed, 13 Aug 2025 18:10:45 GMT  
		Size: 6.6 MB (6639077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98919b9c7706f83ae440ca2aa5285c51487d704a3dff97ad0c9920b0ddc4c2ae`  
		Last Modified: Wed, 13 Aug 2025 18:10:46 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35-alpine`

```console
$ docker pull telegraf@sha256:ef81917ebf37c5e115aa9850acfe6e259cd930a52d9ab631369860f5ad5f714a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:a6d691e966af30894110ca0c541de511c5673b1cea36531539efd075371dad5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84702775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f994615c47582f57294a82c6e40c34ecea33872a4a6bbe47ecda10ef51f28d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.35.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441bfd7cbe6dcce1d3a679483905055d08ac53a62c4b46f7400e56b6033c9fe1`  
		Last Modified: Mon, 28 Jul 2025 20:40:02 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61074257c6ed478d2d729dd4dbb47516bc6c05ae4aaa0a04c6a3760a44dbf9dd`  
		Last Modified: Mon, 28 Jul 2025 20:40:03 GMT  
		Size: 2.6 MB (2552151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e736009a88223d0f0a222e07fd4258d31efc4501ef0908c5913528d7c6d1b74`  
		Last Modified: Mon, 28 Jul 2025 20:40:07 GMT  
		Size: 78.4 MB (78350036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efff3a00ac272dc1ba9246539f23fb935a05ea610519bf545ac53ebb641ed40`  
		Last Modified: Mon, 28 Jul 2025 20:40:02 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8180485c3053244cf019026be34b55ef471f76d951ea3848a556e4c77fd7d26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1146874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ac32bf4bbdfe9dd36a984077c3aaa1b1a3996f894c989113cff87cc2595835`

```dockerfile
```

-	Layers:
	-	`sha256:97e004a361da778aa37b4a3cf769dfaf18eea20a989ee4881806bd6da90237a4`  
		Last Modified: Mon, 28 Jul 2025 21:10:34 GMT  
		Size: 1.1 MB (1131611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c5b7c0959010e9a80cb17b1a324f0e072bf2830d9a94d74f694bcdf97e6f136`  
		Last Modified: Mon, 28 Jul 2025 21:10:35 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:beeb9a84badaee837038459bc3704b40bd7c7ca7e0549ed46536c3baac5ffd30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77773286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647f62df4ae4764d5521c03f468d882504f8ba21e446a90c9dddf3523ad15d78`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.35.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b1f86b4ba4441253e81263e61cb7f6f39394b74b0581bb5e17c44991e92d47`  
		Last Modified: Mon, 28 Jul 2025 21:02:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0a4824ddd6c41e298e5d586333adbb184c26b05b1ab9c1a4634f3201984f82`  
		Last Modified: Mon, 28 Jul 2025 21:02:44 GMT  
		Size: 2.6 MB (2616106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78acedd717276dc34c4db9cd0bca200c6e7d1b09113bbcea9701b87c2c80d90e`  
		Last Modified: Mon, 28 Jul 2025 21:02:58 GMT  
		Size: 71.0 MB (71025532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f530a71952f68dd125e267b32fe83d1a3cf0b84804a3e2c732d979b8d3ff76`  
		Last Modified: Mon, 28 Jul 2025 21:02:43 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d1e66627b765593009da0e1edcf5ce02c9f08a36204e5c2d5faa9a9e9f030dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1142635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1826a2c722e7ec911dc76c2fe2a2151f317a92825e69ff411129c279ca35d79e`

```dockerfile
```

-	Layers:
	-	`sha256:4c9bba698c7676088571f6e1a62024585a0e6c02e55c656d4736299d8b1f3128`  
		Last Modified: Mon, 28 Jul 2025 21:10:39 GMT  
		Size: 1.1 MB (1127250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446732bee9b46b11f5aaecad242187051df8c0d5027d5b0f987fe99aadd5e27c`  
		Last Modified: Mon, 28 Jul 2025 21:10:39 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.3`

```console
$ docker pull telegraf@sha256:d55e33e698ae0e9d9bc0dfad33d100e7f2137ae53b65e4c8c090a79e0ee417ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.3` - linux; amd64

```console
$ docker pull telegraf@sha256:d15a39d5d2b009728da553971935d0dac3811cfd9aa1c48d528eecbcf4b31bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.0 MB (170018463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eda2b8a73b1e01c0cf9efed0956db0475f3cd4d84469c2aea8d4182b7a7a750`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.35.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591ff18e55078b509b99ab7e3c869fc2f6ddc8d8930ed3358ae877682363fc00`  
		Last Modified: Tue, 12 Aug 2025 22:22:50 GMT  
		Size: 18.9 MB (18946345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19bb8c35abeeae86a2ada31b18685fd2cfcbf8fb5efc1fead517cffbb9cdf5c`  
		Last Modified: Tue, 12 Aug 2025 22:22:45 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7914e4fc6ae203ffe3e14eb402bb182f3bef3c806609359537faabb8938a2cc`  
		Last Modified: Tue, 12 Aug 2025 22:22:59 GMT  
		Size: 78.6 MB (78554361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35d9b51e6adbcc3a5dfdad293751b9af99909590f8ce37abce14c3be6558155`  
		Last Modified: Tue, 12 Aug 2025 22:22:47 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:6972ff8ec88a9249009bad5607cd05dafad830ecc9eb6a4b0236b865b233b2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6653160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de2e9d695e11a49c24bb75bc80fdbbe8296cd831bb220cc4be0e22935b0173b`

```dockerfile
```

-	Layers:
	-	`sha256:c492104500241dee5012e5aca9f3e7331ab282a43112b11bdbaee3108ecd9a0b`  
		Last Modified: Wed, 13 Aug 2025 00:10:53 GMT  
		Size: 6.6 MB (6638389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18c6a63414e56a2b879172f184f72bd9e7739a13795abd6cff7f8413d2fc900f`  
		Last Modified: Wed, 13 Aug 2025 00:10:54 GMT  
		Size: 14.8 KB (14771 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7e92274870845922c540933cac3ad588773324cd4dc9c24d710261dd3f5aeb0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156438798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6749fc9a90145eed636cfde43a431bb8ba2b5bcfd84b242ec1408c0d62ade75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.35.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a06e9cd35e09740ec78f63d1179c1e1528d9cfd9686a0094a4655ebe70922c99`  
		Last Modified: Tue, 12 Aug 2025 20:46:18 GMT  
		Size: 44.2 MB (44209044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4756b55428372e77ee6ab2b6c5a35bda8bf113537f0ebde9510c43737f4249c`  
		Last Modified: Wed, 13 Aug 2025 00:15:08 GMT  
		Size: 21.9 MB (21929365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681fdff4dcb6359e721989060c3743deca10d1e73cef0d9b907513c9b4f320f4`  
		Last Modified: Wed, 13 Aug 2025 11:56:52 GMT  
		Size: 17.7 MB (17725068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797481eb709a7b6a93b1cc1814d1f5184123c7245ebd3cdd2c05ae8ebfff5d30`  
		Last Modified: Wed, 13 Aug 2025 11:14:56 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f5973b04d4b80272b9a2f9c407ca321a873af327991f0e4aa1d17801deecd9`  
		Last Modified: Wed, 13 Aug 2025 11:07:01 GMT  
		Size: 72.6 MB (72572912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025c8f783802ef0617664dc4bcf86fcbe3490c943c930783ba4073bd7aeabe24`  
		Last Modified: Wed, 13 Aug 2025 11:06:58 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:f540acfe4ac4a1172bf8673094fd5d9a950d2e25a5cc595adb11ecb413ca92d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6647858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe1fab520699fec52069bb2da5e714552df2a91169116fb422752ee4c5d1e46`

```dockerfile
```

-	Layers:
	-	`sha256:b61f5a4f6e86fcf15d13171ee53d3cae4989c08fe5331e0a91f9a7c64737406f`  
		Last Modified: Wed, 13 Aug 2025 12:10:37 GMT  
		Size: 6.6 MB (6632992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6647686ae7885822c11bab2fad634a369381d65a2393bb4cbad3b2b609cbaa83`  
		Last Modified: Wed, 13 Aug 2025 12:10:38 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:904db379b4746d9df9946af2aad4eb087d0a7851d0cf82e97a05452594e3446c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (162014796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27bd61c58d5ec833e9e3fff27a5890cadd06457cf3026cc4491ab9aa971f22f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.35.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cff9c97e1a1ee42786188e1d1b57f6a2035d65b648178ac0262d0eba0c5c86d`  
		Last Modified: Wed, 13 Aug 2025 07:22:32 GMT  
		Size: 23.6 MB (23569847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b99cb526a2d2c2edce8225080365ce7d0a1289117aacac869f1c80eaed39a8`  
		Last Modified: Wed, 13 Aug 2025 18:10:42 GMT  
		Size: 18.9 MB (18872091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eece436e998d9c9c646d86bd4bacd2c6a80585a2eb2f8903fd22301a267692`  
		Last Modified: Wed, 13 Aug 2025 18:10:43 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f18cd58ac9516b123490b510c54b973bf1ed4d3d12e186b330ccc1f553f215b`  
		Last Modified: Wed, 13 Aug 2025 18:01:56 GMT  
		Size: 71.2 MB (71228002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fabf6fbd3169c71d4799024af77b9aaaf483781078168c3ad82816993090cf3`  
		Last Modified: Wed, 13 Aug 2025 18:01:53 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:49f46c47b0e01182228c8a81eae2cf320a5e5514302879d6b2cc71a010df89f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6653971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b737d49f451e3279ac7337c8af00fb52f5bfd995cb92aed8203528b0d690f39`

```dockerfile
```

-	Layers:
	-	`sha256:b329a08f9f729de3d5dc78c5dbcdc375e08637204261d377168b97e990fb032b`  
		Last Modified: Wed, 13 Aug 2025 18:10:45 GMT  
		Size: 6.6 MB (6639077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98919b9c7706f83ae440ca2aa5285c51487d704a3dff97ad0c9920b0ddc4c2ae`  
		Last Modified: Wed, 13 Aug 2025 18:10:46 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.3-alpine`

```console
$ docker pull telegraf@sha256:ef81917ebf37c5e115aa9850acfe6e259cd930a52d9ab631369860f5ad5f714a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:a6d691e966af30894110ca0c541de511c5673b1cea36531539efd075371dad5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84702775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f994615c47582f57294a82c6e40c34ecea33872a4a6bbe47ecda10ef51f28d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.35.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441bfd7cbe6dcce1d3a679483905055d08ac53a62c4b46f7400e56b6033c9fe1`  
		Last Modified: Mon, 28 Jul 2025 20:40:02 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61074257c6ed478d2d729dd4dbb47516bc6c05ae4aaa0a04c6a3760a44dbf9dd`  
		Last Modified: Mon, 28 Jul 2025 20:40:03 GMT  
		Size: 2.6 MB (2552151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e736009a88223d0f0a222e07fd4258d31efc4501ef0908c5913528d7c6d1b74`  
		Last Modified: Mon, 28 Jul 2025 20:40:07 GMT  
		Size: 78.4 MB (78350036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efff3a00ac272dc1ba9246539f23fb935a05ea610519bf545ac53ebb641ed40`  
		Last Modified: Mon, 28 Jul 2025 20:40:02 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8180485c3053244cf019026be34b55ef471f76d951ea3848a556e4c77fd7d26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1146874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ac32bf4bbdfe9dd36a984077c3aaa1b1a3996f894c989113cff87cc2595835`

```dockerfile
```

-	Layers:
	-	`sha256:97e004a361da778aa37b4a3cf769dfaf18eea20a989ee4881806bd6da90237a4`  
		Last Modified: Mon, 28 Jul 2025 21:10:34 GMT  
		Size: 1.1 MB (1131611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c5b7c0959010e9a80cb17b1a324f0e072bf2830d9a94d74f694bcdf97e6f136`  
		Last Modified: Mon, 28 Jul 2025 21:10:35 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:beeb9a84badaee837038459bc3704b40bd7c7ca7e0549ed46536c3baac5ffd30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77773286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647f62df4ae4764d5521c03f468d882504f8ba21e446a90c9dddf3523ad15d78`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.35.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b1f86b4ba4441253e81263e61cb7f6f39394b74b0581bb5e17c44991e92d47`  
		Last Modified: Mon, 28 Jul 2025 21:02:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0a4824ddd6c41e298e5d586333adbb184c26b05b1ab9c1a4634f3201984f82`  
		Last Modified: Mon, 28 Jul 2025 21:02:44 GMT  
		Size: 2.6 MB (2616106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78acedd717276dc34c4db9cd0bca200c6e7d1b09113bbcea9701b87c2c80d90e`  
		Last Modified: Mon, 28 Jul 2025 21:02:58 GMT  
		Size: 71.0 MB (71025532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f530a71952f68dd125e267b32fe83d1a3cf0b84804a3e2c732d979b8d3ff76`  
		Last Modified: Mon, 28 Jul 2025 21:02:43 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d1e66627b765593009da0e1edcf5ce02c9f08a36204e5c2d5faa9a9e9f030dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1142635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1826a2c722e7ec911dc76c2fe2a2151f317a92825e69ff411129c279ca35d79e`

```dockerfile
```

-	Layers:
	-	`sha256:4c9bba698c7676088571f6e1a62024585a0e6c02e55c656d4736299d8b1f3128`  
		Last Modified: Mon, 28 Jul 2025 21:10:39 GMT  
		Size: 1.1 MB (1127250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446732bee9b46b11f5aaecad242187051df8c0d5027d5b0f987fe99aadd5e27c`  
		Last Modified: Mon, 28 Jul 2025 21:10:39 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:ef81917ebf37c5e115aa9850acfe6e259cd930a52d9ab631369860f5ad5f714a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:a6d691e966af30894110ca0c541de511c5673b1cea36531539efd075371dad5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84702775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f994615c47582f57294a82c6e40c34ecea33872a4a6bbe47ecda10ef51f28d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.35.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441bfd7cbe6dcce1d3a679483905055d08ac53a62c4b46f7400e56b6033c9fe1`  
		Last Modified: Mon, 28 Jul 2025 20:40:02 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61074257c6ed478d2d729dd4dbb47516bc6c05ae4aaa0a04c6a3760a44dbf9dd`  
		Last Modified: Mon, 28 Jul 2025 20:40:03 GMT  
		Size: 2.6 MB (2552151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e736009a88223d0f0a222e07fd4258d31efc4501ef0908c5913528d7c6d1b74`  
		Last Modified: Mon, 28 Jul 2025 20:40:07 GMT  
		Size: 78.4 MB (78350036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efff3a00ac272dc1ba9246539f23fb935a05ea610519bf545ac53ebb641ed40`  
		Last Modified: Mon, 28 Jul 2025 20:40:02 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8180485c3053244cf019026be34b55ef471f76d951ea3848a556e4c77fd7d26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1146874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ac32bf4bbdfe9dd36a984077c3aaa1b1a3996f894c989113cff87cc2595835`

```dockerfile
```

-	Layers:
	-	`sha256:97e004a361da778aa37b4a3cf769dfaf18eea20a989ee4881806bd6da90237a4`  
		Last Modified: Mon, 28 Jul 2025 21:10:34 GMT  
		Size: 1.1 MB (1131611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c5b7c0959010e9a80cb17b1a324f0e072bf2830d9a94d74f694bcdf97e6f136`  
		Last Modified: Mon, 28 Jul 2025 21:10:35 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:beeb9a84badaee837038459bc3704b40bd7c7ca7e0549ed46536c3baac5ffd30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77773286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647f62df4ae4764d5521c03f468d882504f8ba21e446a90c9dddf3523ad15d78`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.35.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b1f86b4ba4441253e81263e61cb7f6f39394b74b0581bb5e17c44991e92d47`  
		Last Modified: Mon, 28 Jul 2025 21:02:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0a4824ddd6c41e298e5d586333adbb184c26b05b1ab9c1a4634f3201984f82`  
		Last Modified: Mon, 28 Jul 2025 21:02:44 GMT  
		Size: 2.6 MB (2616106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78acedd717276dc34c4db9cd0bca200c6e7d1b09113bbcea9701b87c2c80d90e`  
		Last Modified: Mon, 28 Jul 2025 21:02:58 GMT  
		Size: 71.0 MB (71025532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f530a71952f68dd125e267b32fe83d1a3cf0b84804a3e2c732d979b8d3ff76`  
		Last Modified: Mon, 28 Jul 2025 21:02:43 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d1e66627b765593009da0e1edcf5ce02c9f08a36204e5c2d5faa9a9e9f030dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1142635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1826a2c722e7ec911dc76c2fe2a2151f317a92825e69ff411129c279ca35d79e`

```dockerfile
```

-	Layers:
	-	`sha256:4c9bba698c7676088571f6e1a62024585a0e6c02e55c656d4736299d8b1f3128`  
		Last Modified: Mon, 28 Jul 2025 21:10:39 GMT  
		Size: 1.1 MB (1127250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446732bee9b46b11f5aaecad242187051df8c0d5027d5b0f987fe99aadd5e27c`  
		Last Modified: Mon, 28 Jul 2025 21:10:39 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:d55e33e698ae0e9d9bc0dfad33d100e7f2137ae53b65e4c8c090a79e0ee417ea
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
$ docker pull telegraf@sha256:d15a39d5d2b009728da553971935d0dac3811cfd9aa1c48d528eecbcf4b31bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.0 MB (170018463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eda2b8a73b1e01c0cf9efed0956db0475f3cd4d84469c2aea8d4182b7a7a750`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.35.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591ff18e55078b509b99ab7e3c869fc2f6ddc8d8930ed3358ae877682363fc00`  
		Last Modified: Tue, 12 Aug 2025 22:22:50 GMT  
		Size: 18.9 MB (18946345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19bb8c35abeeae86a2ada31b18685fd2cfcbf8fb5efc1fead517cffbb9cdf5c`  
		Last Modified: Tue, 12 Aug 2025 22:22:45 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7914e4fc6ae203ffe3e14eb402bb182f3bef3c806609359537faabb8938a2cc`  
		Last Modified: Tue, 12 Aug 2025 22:22:59 GMT  
		Size: 78.6 MB (78554361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35d9b51e6adbcc3a5dfdad293751b9af99909590f8ce37abce14c3be6558155`  
		Last Modified: Tue, 12 Aug 2025 22:22:47 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:6972ff8ec88a9249009bad5607cd05dafad830ecc9eb6a4b0236b865b233b2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6653160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de2e9d695e11a49c24bb75bc80fdbbe8296cd831bb220cc4be0e22935b0173b`

```dockerfile
```

-	Layers:
	-	`sha256:c492104500241dee5012e5aca9f3e7331ab282a43112b11bdbaee3108ecd9a0b`  
		Last Modified: Wed, 13 Aug 2025 00:10:53 GMT  
		Size: 6.6 MB (6638389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18c6a63414e56a2b879172f184f72bd9e7739a13795abd6cff7f8413d2fc900f`  
		Last Modified: Wed, 13 Aug 2025 00:10:54 GMT  
		Size: 14.8 KB (14771 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7e92274870845922c540933cac3ad588773324cd4dc9c24d710261dd3f5aeb0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156438798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6749fc9a90145eed636cfde43a431bb8ba2b5bcfd84b242ec1408c0d62ade75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.35.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a06e9cd35e09740ec78f63d1179c1e1528d9cfd9686a0094a4655ebe70922c99`  
		Last Modified: Tue, 12 Aug 2025 20:46:18 GMT  
		Size: 44.2 MB (44209044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4756b55428372e77ee6ab2b6c5a35bda8bf113537f0ebde9510c43737f4249c`  
		Last Modified: Wed, 13 Aug 2025 00:15:08 GMT  
		Size: 21.9 MB (21929365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681fdff4dcb6359e721989060c3743deca10d1e73cef0d9b907513c9b4f320f4`  
		Last Modified: Wed, 13 Aug 2025 11:56:52 GMT  
		Size: 17.7 MB (17725068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797481eb709a7b6a93b1cc1814d1f5184123c7245ebd3cdd2c05ae8ebfff5d30`  
		Last Modified: Wed, 13 Aug 2025 11:14:56 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f5973b04d4b80272b9a2f9c407ca321a873af327991f0e4aa1d17801deecd9`  
		Last Modified: Wed, 13 Aug 2025 11:07:01 GMT  
		Size: 72.6 MB (72572912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025c8f783802ef0617664dc4bcf86fcbe3490c943c930783ba4073bd7aeabe24`  
		Last Modified: Wed, 13 Aug 2025 11:06:58 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:f540acfe4ac4a1172bf8673094fd5d9a950d2e25a5cc595adb11ecb413ca92d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6647858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe1fab520699fec52069bb2da5e714552df2a91169116fb422752ee4c5d1e46`

```dockerfile
```

-	Layers:
	-	`sha256:b61f5a4f6e86fcf15d13171ee53d3cae4989c08fe5331e0a91f9a7c64737406f`  
		Last Modified: Wed, 13 Aug 2025 12:10:37 GMT  
		Size: 6.6 MB (6632992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6647686ae7885822c11bab2fad634a369381d65a2393bb4cbad3b2b609cbaa83`  
		Last Modified: Wed, 13 Aug 2025 12:10:38 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:904db379b4746d9df9946af2aad4eb087d0a7851d0cf82e97a05452594e3446c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (162014796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27bd61c58d5ec833e9e3fff27a5890cadd06457cf3026cc4491ab9aa971f22f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.35.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cff9c97e1a1ee42786188e1d1b57f6a2035d65b648178ac0262d0eba0c5c86d`  
		Last Modified: Wed, 13 Aug 2025 07:22:32 GMT  
		Size: 23.6 MB (23569847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b99cb526a2d2c2edce8225080365ce7d0a1289117aacac869f1c80eaed39a8`  
		Last Modified: Wed, 13 Aug 2025 18:10:42 GMT  
		Size: 18.9 MB (18872091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eece436e998d9c9c646d86bd4bacd2c6a80585a2eb2f8903fd22301a267692`  
		Last Modified: Wed, 13 Aug 2025 18:10:43 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f18cd58ac9516b123490b510c54b973bf1ed4d3d12e186b330ccc1f553f215b`  
		Last Modified: Wed, 13 Aug 2025 18:01:56 GMT  
		Size: 71.2 MB (71228002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fabf6fbd3169c71d4799024af77b9aaaf483781078168c3ad82816993090cf3`  
		Last Modified: Wed, 13 Aug 2025 18:01:53 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:49f46c47b0e01182228c8a81eae2cf320a5e5514302879d6b2cc71a010df89f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6653971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b737d49f451e3279ac7337c8af00fb52f5bfd995cb92aed8203528b0d690f39`

```dockerfile
```

-	Layers:
	-	`sha256:b329a08f9f729de3d5dc78c5dbcdc375e08637204261d377168b97e990fb032b`  
		Last Modified: Wed, 13 Aug 2025 18:10:45 GMT  
		Size: 6.6 MB (6639077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98919b9c7706f83ae440ca2aa5285c51487d704a3dff97ad0c9920b0ddc4c2ae`  
		Last Modified: Wed, 13 Aug 2025 18:10:46 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
