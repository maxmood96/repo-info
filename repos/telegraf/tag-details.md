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
-	[`telegraf:1.35.4`](#telegraf1354)
-	[`telegraf:1.35.4-alpine`](#telegraf1354-alpine)
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
$ docker pull telegraf@sha256:312e6c4df0a43cdde7d4ed0b3092a9218acff4bfd07216c64f555aa8f44f3bca
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
$ docker pull telegraf@sha256:29108ffecc690e6f401cd72f97644c8d10479c2670105104b9bb96e7d945a085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171035076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfd39d1b578d9f966fed67e3b1ce3c4ad94d6a3dbdaca3ef9185d4c434c2138`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
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
	-	`sha256:0413e7b2eb9ba4c821a81e0ff544fe1159f9844e3fd8cbd6511b6cf566951fc1`  
		Last Modified: Tue, 19 Aug 2025 16:43:16 GMT  
		Size: 18.9 MB (18946745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c04612bb27a46562400b3e8ec9fb02b17f87d0c90004a4307d17d467f54b93`  
		Last Modified: Tue, 19 Aug 2025 16:43:09 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee20cbf0bacc52406d309e74d8b6a3acfef762c1a5bf36d0963996cffe68a22`  
		Last Modified: Tue, 19 Aug 2025 16:43:19 GMT  
		Size: 79.6 MB (79570572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8023edc42cd5164dfe848a9d505431394d0221772402a722dd4c23c9d09fe6`  
		Last Modified: Tue, 19 Aug 2025 16:43:09 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:98468b2b79b42f22e53c382384ef8a16d22e25d6a757d3c6f8b261859c95b3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6653247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7aecaed26cf3b263f9df586abb492faa74769c0e83b9e0091fbf2648869e442`

```dockerfile
```

-	Layers:
	-	`sha256:80ecd638179d18e5ddcfc59632a9764f1ed8feaf7af880ee3659f3132b2bd7cc`  
		Last Modified: Tue, 19 Aug 2025 18:10:33 GMT  
		Size: 6.6 MB (6638475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d733296df4cd6d5ddc53d7fd601c3c0cadc2ea757a23ea3ee50bd6bb414c0eac`  
		Last Modified: Tue, 19 Aug 2025 18:10:34 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:91b8d30fa4be79a13d9f51dd4816ba0fc0a695a7d36b72af073c9749e63bf5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157156497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993e5a766b756ccfd7713920c7a9a1b14ab87dd3e0f341bb2ddfd1b604657562`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
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
	-	`sha256:637ea78bbab9b8889bcfddd80e42dd1798df1e3424c850924021be81254882cd`  
		Last Modified: Tue, 19 Aug 2025 16:42:43 GMT  
		Size: 73.3 MB (73290612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d2045f5208fe2cbc05be97c6a6f0cf96d5bd336067d64a1167223bf6c7d38`  
		Last Modified: Tue, 19 Aug 2025 16:42:20 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:bb8b802448d044c19b6bade15fe09c2513c1d83bca7e3ad2207f4ebd833bc6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6647946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d204ca9c7f06d1ca0dc1771646db5b6fe4d78803adaed77dfcc4a5a9690a82`

```dockerfile
```

-	Layers:
	-	`sha256:974c18a6fda81be68b50b13dea7c3313a417a56c1921c4d5e83409087c5a9a81`  
		Last Modified: Tue, 19 Aug 2025 18:10:39 GMT  
		Size: 6.6 MB (6633080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:196854c3e97335eeb6c8e0e3bad45237633e6e0cbeb761abb7a6f8208021332c`  
		Last Modified: Tue, 19 Aug 2025 18:10:40 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:91f320dc69e576a3849f1513847af69c36e87ad1758f061b42de29fa0c3b808e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162865925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57ffa7f02a5176dff9ce9b8b30822b9a1e1d404a29212bf5e58a849f0b89008`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
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
	-	`sha256:5b6fcb93b3bbaaadceefac094489cc08032e4998cd9d646bc073a8e79914bed3`  
		Last Modified: Tue, 19 Aug 2025 17:00:01 GMT  
		Size: 18.9 MB (18872021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b294ae850c792566c37c0813f26742c5fa1e40219f1c369e3dc8e5dd880ca6b1`  
		Last Modified: Tue, 19 Aug 2025 17:00:01 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec9a401f129ae26776c6c8671f757a150d7474312728cbe56970434da4fb965`  
		Last Modified: Tue, 19 Aug 2025 17:00:07 GMT  
		Size: 72.1 MB (72079198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e0899a04ff182a22c0ef9f5c60505f0df6bb571e18c428e27a14d0957fe89b`  
		Last Modified: Tue, 19 Aug 2025 17:00:02 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:79e8719d13bbf091734c90a5a6f1ba0e45885d85dc627a6e770208b0e21b3b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6654057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784c8c9310e95463557cffcedbb9541947006ff681d088b39873124a291e15a1`

```dockerfile
```

-	Layers:
	-	`sha256:f075f3fa43fb53b12af21fd40c7505e8c854b4b280854f3eeec2a16d0e46902b`  
		Last Modified: Tue, 19 Aug 2025 18:10:46 GMT  
		Size: 6.6 MB (6639163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d86b34105dafee1c434798390de08367794288d709eec75448c86ccf91d75fc`  
		Last Modified: Tue, 19 Aug 2025 18:10:47 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35-alpine`

```console
$ docker pull telegraf@sha256:c2f97b178be0d6da47934693aab5f12968d4c357067466b00750d7c883c7ca5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b9f1dad8bfc6e2e0a071ec3708f69b608314a1638df1a27dbee6c8d9c201157d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85721229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1898bfc2837a825d9ca57c11162f841378cca6e17895db8ff8007425b40ae030`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111a65e71ad846fe6bc5cf5d9981577f402356a07fa8643556a52a493832248d`  
		Last Modified: Tue, 19 Aug 2025 16:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cbaff1778259b3073527b025ae9ab08156e23a8b7f42fbbc0fafca178fc2a4`  
		Last Modified: Tue, 19 Aug 2025 16:43:11 GMT  
		Size: 2.6 MB (2552105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e527cfac45a96a64d7cc6821810e5660eec3f9f105ee9595ff5d0ef9ce3889e5`  
		Last Modified: Tue, 19 Aug 2025 16:43:18 GMT  
		Size: 79.4 MB (79368534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701fb22e4edb908e9c9db1946c3275c80eb50f1b6a4a0a263e2bcc780d2db6cb`  
		Last Modified: Tue, 19 Aug 2025 16:43:13 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d62ff060ab03e0e18dd18b68bef85d0e6253116947fe2889d8b0627c72be5d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1146960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00067d3ac59b152349cce2ee62d1d1fc80d424366cca0741b5130316ec1f36f0`

```dockerfile
```

-	Layers:
	-	`sha256:ae9d5119dea6d9d8dc370f0197b7815e7ea4eab7a50e3962df4ff7507b5ec15b`  
		Last Modified: Tue, 19 Aug 2025 18:10:39 GMT  
		Size: 1.1 MB (1131697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2678129d408de246508eace01dabc93d4762f22a4bce5468f32eb78e3c0d9cf4`  
		Last Modified: Tue, 19 Aug 2025 18:10:40 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:236e9d66b8103bd93e3872764468db2ac263c373b260498613a72d79b42e7f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78624875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f602f26ba2bca549d1b9b7ae0a9904b7bb21d6746ba5781c2e0a9a6e6aea23ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9ba851c3cc6f6a60e1f54d90b4a3e0088e3e71c1361234db72c0e681312948`  
		Last Modified: Tue, 19 Aug 2025 17:00:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4ac1b57267caa5ade49b9cf526c34877421ccf3ab657266741789a47db05a4`  
		Last Modified: Tue, 19 Aug 2025 17:00:42 GMT  
		Size: 2.6 MB (2616107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6254a8553d06cd74dd83678e67660d16a33aafe7a727405a4a8950db4c073a8`  
		Last Modified: Tue, 19 Aug 2025 17:00:55 GMT  
		Size: 71.9 MB (71877119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcbf034e9f0cedd31ed4f69e865f928e913e9e964d333ea83a0e38eab973e42`  
		Last Modified: Tue, 19 Aug 2025 17:00:42 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c7e18faf8edc102ce2aed72cca6a6ede5f0e92daa3e47336568447b0b82b2a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1142721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f034d01f06a7ef20999ff7fac16427ff60c143a68c0c7cd7ce2d43a9eeeffd`

```dockerfile
```

-	Layers:
	-	`sha256:b879ba997169df517ba2e5569a8fcd1783cfdde33a4b2a993479bdf25aeac651`  
		Last Modified: Tue, 19 Aug 2025 18:10:44 GMT  
		Size: 1.1 MB (1127336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c8fbc4be53f9d0b83f8a5baee19ef6ea265b37202aba06848c4f081543b0b3`  
		Last Modified: Tue, 19 Aug 2025 18:10:45 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4`

```console
$ docker pull telegraf@sha256:312e6c4df0a43cdde7d4ed0b3092a9218acff4bfd07216c64f555aa8f44f3bca
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
$ docker pull telegraf@sha256:29108ffecc690e6f401cd72f97644c8d10479c2670105104b9bb96e7d945a085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171035076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfd39d1b578d9f966fed67e3b1ce3c4ad94d6a3dbdaca3ef9185d4c434c2138`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
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
	-	`sha256:0413e7b2eb9ba4c821a81e0ff544fe1159f9844e3fd8cbd6511b6cf566951fc1`  
		Last Modified: Tue, 19 Aug 2025 16:43:16 GMT  
		Size: 18.9 MB (18946745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c04612bb27a46562400b3e8ec9fb02b17f87d0c90004a4307d17d467f54b93`  
		Last Modified: Tue, 19 Aug 2025 16:43:09 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee20cbf0bacc52406d309e74d8b6a3acfef762c1a5bf36d0963996cffe68a22`  
		Last Modified: Tue, 19 Aug 2025 16:43:19 GMT  
		Size: 79.6 MB (79570572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8023edc42cd5164dfe848a9d505431394d0221772402a722dd4c23c9d09fe6`  
		Last Modified: Tue, 19 Aug 2025 16:43:09 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:98468b2b79b42f22e53c382384ef8a16d22e25d6a757d3c6f8b261859c95b3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6653247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7aecaed26cf3b263f9df586abb492faa74769c0e83b9e0091fbf2648869e442`

```dockerfile
```

-	Layers:
	-	`sha256:80ecd638179d18e5ddcfc59632a9764f1ed8feaf7af880ee3659f3132b2bd7cc`  
		Last Modified: Tue, 19 Aug 2025 18:10:33 GMT  
		Size: 6.6 MB (6638475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d733296df4cd6d5ddc53d7fd601c3c0cadc2ea757a23ea3ee50bd6bb414c0eac`  
		Last Modified: Tue, 19 Aug 2025 18:10:34 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:91b8d30fa4be79a13d9f51dd4816ba0fc0a695a7d36b72af073c9749e63bf5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157156497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993e5a766b756ccfd7713920c7a9a1b14ab87dd3e0f341bb2ddfd1b604657562`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
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
	-	`sha256:637ea78bbab9b8889bcfddd80e42dd1798df1e3424c850924021be81254882cd`  
		Last Modified: Tue, 19 Aug 2025 16:42:43 GMT  
		Size: 73.3 MB (73290612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d2045f5208fe2cbc05be97c6a6f0cf96d5bd336067d64a1167223bf6c7d38`  
		Last Modified: Tue, 19 Aug 2025 16:42:20 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:bb8b802448d044c19b6bade15fe09c2513c1d83bca7e3ad2207f4ebd833bc6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6647946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d204ca9c7f06d1ca0dc1771646db5b6fe4d78803adaed77dfcc4a5a9690a82`

```dockerfile
```

-	Layers:
	-	`sha256:974c18a6fda81be68b50b13dea7c3313a417a56c1921c4d5e83409087c5a9a81`  
		Last Modified: Tue, 19 Aug 2025 18:10:39 GMT  
		Size: 6.6 MB (6633080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:196854c3e97335eeb6c8e0e3bad45237633e6e0cbeb761abb7a6f8208021332c`  
		Last Modified: Tue, 19 Aug 2025 18:10:40 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:91f320dc69e576a3849f1513847af69c36e87ad1758f061b42de29fa0c3b808e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162865925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57ffa7f02a5176dff9ce9b8b30822b9a1e1d404a29212bf5e58a849f0b89008`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
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
	-	`sha256:5b6fcb93b3bbaaadceefac094489cc08032e4998cd9d646bc073a8e79914bed3`  
		Last Modified: Tue, 19 Aug 2025 17:00:01 GMT  
		Size: 18.9 MB (18872021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b294ae850c792566c37c0813f26742c5fa1e40219f1c369e3dc8e5dd880ca6b1`  
		Last Modified: Tue, 19 Aug 2025 17:00:01 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec9a401f129ae26776c6c8671f757a150d7474312728cbe56970434da4fb965`  
		Last Modified: Tue, 19 Aug 2025 17:00:07 GMT  
		Size: 72.1 MB (72079198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e0899a04ff182a22c0ef9f5c60505f0df6bb571e18c428e27a14d0957fe89b`  
		Last Modified: Tue, 19 Aug 2025 17:00:02 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:79e8719d13bbf091734c90a5a6f1ba0e45885d85dc627a6e770208b0e21b3b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6654057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784c8c9310e95463557cffcedbb9541947006ff681d088b39873124a291e15a1`

```dockerfile
```

-	Layers:
	-	`sha256:f075f3fa43fb53b12af21fd40c7505e8c854b4b280854f3eeec2a16d0e46902b`  
		Last Modified: Tue, 19 Aug 2025 18:10:46 GMT  
		Size: 6.6 MB (6639163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d86b34105dafee1c434798390de08367794288d709eec75448c86ccf91d75fc`  
		Last Modified: Tue, 19 Aug 2025 18:10:47 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4-alpine`

```console
$ docker pull telegraf@sha256:c2f97b178be0d6da47934693aab5f12968d4c357067466b00750d7c883c7ca5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b9f1dad8bfc6e2e0a071ec3708f69b608314a1638df1a27dbee6c8d9c201157d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85721229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1898bfc2837a825d9ca57c11162f841378cca6e17895db8ff8007425b40ae030`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111a65e71ad846fe6bc5cf5d9981577f402356a07fa8643556a52a493832248d`  
		Last Modified: Tue, 19 Aug 2025 16:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cbaff1778259b3073527b025ae9ab08156e23a8b7f42fbbc0fafca178fc2a4`  
		Last Modified: Tue, 19 Aug 2025 16:43:11 GMT  
		Size: 2.6 MB (2552105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e527cfac45a96a64d7cc6821810e5660eec3f9f105ee9595ff5d0ef9ce3889e5`  
		Last Modified: Tue, 19 Aug 2025 16:43:18 GMT  
		Size: 79.4 MB (79368534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701fb22e4edb908e9c9db1946c3275c80eb50f1b6a4a0a263e2bcc780d2db6cb`  
		Last Modified: Tue, 19 Aug 2025 16:43:13 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d62ff060ab03e0e18dd18b68bef85d0e6253116947fe2889d8b0627c72be5d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1146960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00067d3ac59b152349cce2ee62d1d1fc80d424366cca0741b5130316ec1f36f0`

```dockerfile
```

-	Layers:
	-	`sha256:ae9d5119dea6d9d8dc370f0197b7815e7ea4eab7a50e3962df4ff7507b5ec15b`  
		Last Modified: Tue, 19 Aug 2025 18:10:39 GMT  
		Size: 1.1 MB (1131697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2678129d408de246508eace01dabc93d4762f22a4bce5468f32eb78e3c0d9cf4`  
		Last Modified: Tue, 19 Aug 2025 18:10:40 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:236e9d66b8103bd93e3872764468db2ac263c373b260498613a72d79b42e7f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78624875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f602f26ba2bca549d1b9b7ae0a9904b7bb21d6746ba5781c2e0a9a6e6aea23ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9ba851c3cc6f6a60e1f54d90b4a3e0088e3e71c1361234db72c0e681312948`  
		Last Modified: Tue, 19 Aug 2025 17:00:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4ac1b57267caa5ade49b9cf526c34877421ccf3ab657266741789a47db05a4`  
		Last Modified: Tue, 19 Aug 2025 17:00:42 GMT  
		Size: 2.6 MB (2616107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6254a8553d06cd74dd83678e67660d16a33aafe7a727405a4a8950db4c073a8`  
		Last Modified: Tue, 19 Aug 2025 17:00:55 GMT  
		Size: 71.9 MB (71877119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcbf034e9f0cedd31ed4f69e865f928e913e9e964d333ea83a0e38eab973e42`  
		Last Modified: Tue, 19 Aug 2025 17:00:42 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c7e18faf8edc102ce2aed72cca6a6ede5f0e92daa3e47336568447b0b82b2a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1142721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f034d01f06a7ef20999ff7fac16427ff60c143a68c0c7cd7ce2d43a9eeeffd`

```dockerfile
```

-	Layers:
	-	`sha256:b879ba997169df517ba2e5569a8fcd1783cfdde33a4b2a993479bdf25aeac651`  
		Last Modified: Tue, 19 Aug 2025 18:10:44 GMT  
		Size: 1.1 MB (1127336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c8fbc4be53f9d0b83f8a5baee19ef6ea265b37202aba06848c4f081543b0b3`  
		Last Modified: Tue, 19 Aug 2025 18:10:45 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:c2f97b178be0d6da47934693aab5f12968d4c357067466b00750d7c883c7ca5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b9f1dad8bfc6e2e0a071ec3708f69b608314a1638df1a27dbee6c8d9c201157d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85721229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1898bfc2837a825d9ca57c11162f841378cca6e17895db8ff8007425b40ae030`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111a65e71ad846fe6bc5cf5d9981577f402356a07fa8643556a52a493832248d`  
		Last Modified: Tue, 19 Aug 2025 16:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cbaff1778259b3073527b025ae9ab08156e23a8b7f42fbbc0fafca178fc2a4`  
		Last Modified: Tue, 19 Aug 2025 16:43:11 GMT  
		Size: 2.6 MB (2552105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e527cfac45a96a64d7cc6821810e5660eec3f9f105ee9595ff5d0ef9ce3889e5`  
		Last Modified: Tue, 19 Aug 2025 16:43:18 GMT  
		Size: 79.4 MB (79368534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701fb22e4edb908e9c9db1946c3275c80eb50f1b6a4a0a263e2bcc780d2db6cb`  
		Last Modified: Tue, 19 Aug 2025 16:43:13 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d62ff060ab03e0e18dd18b68bef85d0e6253116947fe2889d8b0627c72be5d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1146960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00067d3ac59b152349cce2ee62d1d1fc80d424366cca0741b5130316ec1f36f0`

```dockerfile
```

-	Layers:
	-	`sha256:ae9d5119dea6d9d8dc370f0197b7815e7ea4eab7a50e3962df4ff7507b5ec15b`  
		Last Modified: Tue, 19 Aug 2025 18:10:39 GMT  
		Size: 1.1 MB (1131697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2678129d408de246508eace01dabc93d4762f22a4bce5468f32eb78e3c0d9cf4`  
		Last Modified: Tue, 19 Aug 2025 18:10:40 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:236e9d66b8103bd93e3872764468db2ac263c373b260498613a72d79b42e7f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78624875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f602f26ba2bca549d1b9b7ae0a9904b7bb21d6746ba5781c2e0a9a6e6aea23ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9ba851c3cc6f6a60e1f54d90b4a3e0088e3e71c1361234db72c0e681312948`  
		Last Modified: Tue, 19 Aug 2025 17:00:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4ac1b57267caa5ade49b9cf526c34877421ccf3ab657266741789a47db05a4`  
		Last Modified: Tue, 19 Aug 2025 17:00:42 GMT  
		Size: 2.6 MB (2616107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6254a8553d06cd74dd83678e67660d16a33aafe7a727405a4a8950db4c073a8`  
		Last Modified: Tue, 19 Aug 2025 17:00:55 GMT  
		Size: 71.9 MB (71877119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcbf034e9f0cedd31ed4f69e865f928e913e9e964d333ea83a0e38eab973e42`  
		Last Modified: Tue, 19 Aug 2025 17:00:42 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c7e18faf8edc102ce2aed72cca6a6ede5f0e92daa3e47336568447b0b82b2a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1142721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f034d01f06a7ef20999ff7fac16427ff60c143a68c0c7cd7ce2d43a9eeeffd`

```dockerfile
```

-	Layers:
	-	`sha256:b879ba997169df517ba2e5569a8fcd1783cfdde33a4b2a993479bdf25aeac651`  
		Last Modified: Tue, 19 Aug 2025 18:10:44 GMT  
		Size: 1.1 MB (1127336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c8fbc4be53f9d0b83f8a5baee19ef6ea265b37202aba06848c4f081543b0b3`  
		Last Modified: Tue, 19 Aug 2025 18:10:45 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:312e6c4df0a43cdde7d4ed0b3092a9218acff4bfd07216c64f555aa8f44f3bca
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
$ docker pull telegraf@sha256:29108ffecc690e6f401cd72f97644c8d10479c2670105104b9bb96e7d945a085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171035076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfd39d1b578d9f966fed67e3b1ce3c4ad94d6a3dbdaca3ef9185d4c434c2138`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
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
	-	`sha256:0413e7b2eb9ba4c821a81e0ff544fe1159f9844e3fd8cbd6511b6cf566951fc1`  
		Last Modified: Tue, 19 Aug 2025 16:43:16 GMT  
		Size: 18.9 MB (18946745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c04612bb27a46562400b3e8ec9fb02b17f87d0c90004a4307d17d467f54b93`  
		Last Modified: Tue, 19 Aug 2025 16:43:09 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee20cbf0bacc52406d309e74d8b6a3acfef762c1a5bf36d0963996cffe68a22`  
		Last Modified: Tue, 19 Aug 2025 16:43:19 GMT  
		Size: 79.6 MB (79570572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8023edc42cd5164dfe848a9d505431394d0221772402a722dd4c23c9d09fe6`  
		Last Modified: Tue, 19 Aug 2025 16:43:09 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:98468b2b79b42f22e53c382384ef8a16d22e25d6a757d3c6f8b261859c95b3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6653247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7aecaed26cf3b263f9df586abb492faa74769c0e83b9e0091fbf2648869e442`

```dockerfile
```

-	Layers:
	-	`sha256:80ecd638179d18e5ddcfc59632a9764f1ed8feaf7af880ee3659f3132b2bd7cc`  
		Last Modified: Tue, 19 Aug 2025 18:10:33 GMT  
		Size: 6.6 MB (6638475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d733296df4cd6d5ddc53d7fd601c3c0cadc2ea757a23ea3ee50bd6bb414c0eac`  
		Last Modified: Tue, 19 Aug 2025 18:10:34 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:91b8d30fa4be79a13d9f51dd4816ba0fc0a695a7d36b72af073c9749e63bf5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157156497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993e5a766b756ccfd7713920c7a9a1b14ab87dd3e0f341bb2ddfd1b604657562`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
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
	-	`sha256:637ea78bbab9b8889bcfddd80e42dd1798df1e3424c850924021be81254882cd`  
		Last Modified: Tue, 19 Aug 2025 16:42:43 GMT  
		Size: 73.3 MB (73290612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d2045f5208fe2cbc05be97c6a6f0cf96d5bd336067d64a1167223bf6c7d38`  
		Last Modified: Tue, 19 Aug 2025 16:42:20 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:bb8b802448d044c19b6bade15fe09c2513c1d83bca7e3ad2207f4ebd833bc6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6647946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d204ca9c7f06d1ca0dc1771646db5b6fe4d78803adaed77dfcc4a5a9690a82`

```dockerfile
```

-	Layers:
	-	`sha256:974c18a6fda81be68b50b13dea7c3313a417a56c1921c4d5e83409087c5a9a81`  
		Last Modified: Tue, 19 Aug 2025 18:10:39 GMT  
		Size: 6.6 MB (6633080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:196854c3e97335eeb6c8e0e3bad45237633e6e0cbeb761abb7a6f8208021332c`  
		Last Modified: Tue, 19 Aug 2025 18:10:40 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:91f320dc69e576a3849f1513847af69c36e87ad1758f061b42de29fa0c3b808e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162865925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57ffa7f02a5176dff9ce9b8b30822b9a1e1d404a29212bf5e58a849f0b89008`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
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
	-	`sha256:5b6fcb93b3bbaaadceefac094489cc08032e4998cd9d646bc073a8e79914bed3`  
		Last Modified: Tue, 19 Aug 2025 17:00:01 GMT  
		Size: 18.9 MB (18872021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b294ae850c792566c37c0813f26742c5fa1e40219f1c369e3dc8e5dd880ca6b1`  
		Last Modified: Tue, 19 Aug 2025 17:00:01 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec9a401f129ae26776c6c8671f757a150d7474312728cbe56970434da4fb965`  
		Last Modified: Tue, 19 Aug 2025 17:00:07 GMT  
		Size: 72.1 MB (72079198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e0899a04ff182a22c0ef9f5c60505f0df6bb571e18c428e27a14d0957fe89b`  
		Last Modified: Tue, 19 Aug 2025 17:00:02 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:79e8719d13bbf091734c90a5a6f1ba0e45885d85dc627a6e770208b0e21b3b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6654057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784c8c9310e95463557cffcedbb9541947006ff681d088b39873124a291e15a1`

```dockerfile
```

-	Layers:
	-	`sha256:f075f3fa43fb53b12af21fd40c7505e8c854b4b280854f3eeec2a16d0e46902b`  
		Last Modified: Tue, 19 Aug 2025 18:10:46 GMT  
		Size: 6.6 MB (6639163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d86b34105dafee1c434798390de08367794288d709eec75448c86ccf91d75fc`  
		Last Modified: Tue, 19 Aug 2025 18:10:47 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
