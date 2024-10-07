<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.30`](#telegraf130)
-	[`telegraf:1.30-alpine`](#telegraf130-alpine)
-	[`telegraf:1.30.3`](#telegraf1303)
-	[`telegraf:1.30.3-alpine`](#telegraf1303-alpine)
-	[`telegraf:1.31`](#telegraf131)
-	[`telegraf:1.31-alpine`](#telegraf131-alpine)
-	[`telegraf:1.31.3`](#telegraf1313)
-	[`telegraf:1.31.3-alpine`](#telegraf1313-alpine)
-	[`telegraf:1.32`](#telegraf132)
-	[`telegraf:1.32-alpine`](#telegraf132-alpine)
-	[`telegraf:1.32.1`](#telegraf1321)
-	[`telegraf:1.32.1-alpine`](#telegraf1321-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.30`

```console
$ docker pull telegraf@sha256:f9b07f91ee00779f552a87b92ebd41124a91fd7de2d9d87a5d734d7ee4d18fd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30` - linux; amd64

```console
$ docker pull telegraf@sha256:789c8f2b68ce3116613d7578051629460280362589579124e242480055177eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155324989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d601c47b2cc76418082ed9e1affc1bb9da207e1883af6e28333a3996d8ae6e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Sep 2024 19:33:37 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 19:33:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1433b93c8b559e6f077106926b0a6a9a32dbc73b562f117de1450b76442d61dd`  
		Last Modified: Fri, 27 Sep 2024 06:15:45 GMT  
		Size: 18.9 MB (18947989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d1da800c36d534d38e317ac23a00e45efe8edf5ce1ce05541b3a10aa10a772`  
		Last Modified: Fri, 27 Sep 2024 06:15:44 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c60714d315d09052b5efd4905d4776944d649cfc4ac92af354c042710e42e6`  
		Last Modified: Fri, 27 Sep 2024 06:15:45 GMT  
		Size: 62.8 MB (62766489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9319cb924fe464a782425551f8838b2cf1392fc1f24681f0013c70256e9471`  
		Last Modified: Fri, 27 Sep 2024 06:15:44 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:d496142000a76541ec49dd4526bf55a28231609800d7f43851e2966109bd58f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9849fcce6e1935186295ed9fcfc984fad7b4dab472485640cd5adfaed5657b`

```dockerfile
```

-	Layers:
	-	`sha256:e82d0c6fc341cc9b98329f2add557eb87e5698af3368864437b173693ef83437`  
		Last Modified: Fri, 27 Sep 2024 06:15:44 GMT  
		Size: 6.4 MB (6391138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43b5c9037050ada1a77a95ea12c85f8e38a1f8131007b72093265a5fdd0481bd`  
		Last Modified: Fri, 27 Sep 2024 06:15:44 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:4782dee2276712745401413352f156c2ee3ef3a9f5e9c0010dcca8db1fa062d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143045412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7de357d252cdbab2eccea80863477b9b488d48742248f9aea323dfeeef722ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Sep 2024 19:33:37 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 19:33:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6b3cf1834faf48a7863802a88d183d7c882c279894a2875ceab123807eb3e0`  
		Last Modified: Sat, 28 Sep 2024 04:09:58 GMT  
		Size: 17.7 MB (17724904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc1bcf3dddedf4b1504712d28eec4c85ca3531dfc940b394aca29a5c91d734b`  
		Last Modified: Sat, 28 Sep 2024 04:09:57 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c071b30591b99ff308ecb3f8c9af9945b98a2fecdfccc306d3fe8a9133b2f9d6`  
		Last Modified: Sat, 28 Sep 2024 04:09:59 GMT  
		Size: 58.2 MB (58212651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6891cc87680d8207ea4a4bf1672a7b98fec600b3180a095ba1528c896a3409`  
		Last Modified: Sat, 28 Sep 2024 04:09:57 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:14ffdda7a0c9ac41b76b2b2ce2f6a28b573a6186ef01d128343b3e85671b3784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6633aff21924d548a9e76f784a15e669b05d662d6726ea8c82b8abeebdd79cce`

```dockerfile
```

-	Layers:
	-	`sha256:bd8390032549e060ea8748bcd26893f05b488c5b1937e50e7b3e2365259316e2`  
		Last Modified: Sat, 28 Sep 2024 04:09:58 GMT  
		Size: 6.4 MB (6385777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:715e45f33d8a5fb1478e7199d42ed7d29194faf16895275144ad54cb919f7384`  
		Last Modified: Sat, 28 Sep 2024 04:09:57 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:bfb7889d7f35a96a3c9591b5a59fd4f45462c5e7dbb7a23fe3cd1243d85aae5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149175253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ee5f497b0fb4089aa43beda3236ef8916bfe185483666906fdef28340099be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Sep 2024 19:33:37 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 19:33:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a5e311e8602fb4adc997da60dc66e9b3fdbb48311a540c7c6f3e63afef030b`  
		Last Modified: Fri, 27 Sep 2024 23:54:12 GMT  
		Size: 18.9 MB (18870648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb152dfb28ebda156d29a36e88b6e3501988064995d55089c376c3012aac1ed6`  
		Last Modified: Fri, 27 Sep 2024 23:54:11 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b91b648b2cc734f3ceef33b217323c31801d76e48bc1dfa57975c9f39090f31`  
		Last Modified: Fri, 27 Sep 2024 23:54:13 GMT  
		Size: 57.1 MB (57123272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79e50083399a6467b414ad030bcd64149249787406a956a634718e68e909843`  
		Last Modified: Fri, 27 Sep 2024 23:54:11 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:314831f63854fd73fc65d2520279f84e92a32dab1fc92b60e40fba6aa8fe7439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4262b38530bf18496b005006c3d62d0f494a7f21342f524df0d44df2dbc2b9cf`

```dockerfile
```

-	Layers:
	-	`sha256:eaef863517add38947256743ed1d7e9f73a34e2b3aa3a0a822cec3e559b28ca6`  
		Last Modified: Fri, 27 Sep 2024 23:54:12 GMT  
		Size: 6.4 MB (6391061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c683f482f406c0d3e40351632136d0c37825bab9abb12f240a8ac499e0996cbc`  
		Last Modified: Fri, 27 Sep 2024 23:54:11 GMT  
		Size: 14.6 KB (14617 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30-alpine`

```console
$ docker pull telegraf@sha256:e9e93edb70da8d8b89af431a98e510ab8efe719b2e0581a7360fcdf78f0e2a95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f204a64e42da80d96c8ed82613253bf3649d7aadccefc5a667e47d6e40e834ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68637698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18bb0214a0965f70002d5358dcf43d85e106e0f5acfe0ed9f1abe26b0353932`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["/bin/sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e0021259f7a43d4a51ff9aee4e5370c38c6b29f581a2f3917b9425788389e7`  
		Last Modified: Fri, 06 Sep 2024 23:24:59 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb5673a8ee4bb44fb3c81f4d9550f573a638290e03cbd4e6a25c15da651174e`  
		Last Modified: Fri, 06 Sep 2024 23:25:00 GMT  
		Size: 2.4 MB (2444799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319f92d6bf7f9fb73eb304cbfc559e1f53f37ddc6ea75f43f4fba540bdd48aab`  
		Last Modified: Fri, 06 Sep 2024 23:25:01 GMT  
		Size: 62.6 MB (62568484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6290f46669fa74c561f37b059bef89d7c0978262b2b174c9d679e178dc69c189`  
		Last Modified: Fri, 06 Sep 2024 23:25:00 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:a6cd90301c5006163e8c49e4bcf59e680ed27cae2ffc1807bd78d70aabf61002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1070927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfc7684017c3e8e8a41cd89bda48b33a054c47f2f180d2a7538cf7454ba3808`

```dockerfile
```

-	Layers:
	-	`sha256:af0f2bf20de1328a4327eebc5922312f834863b7cc0fccd141b387059835f300`  
		Last Modified: Fri, 06 Sep 2024 23:25:00 GMT  
		Size: 1.1 MB (1056193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c94f580866058dbce4eef3bfe30f18fc33f9a5459a6f1a6b7ccc3fac94acf2`  
		Last Modified: Fri, 06 Sep 2024 23:24:59 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c0a48224b1fac0a7ec76fb965f8a0f14197c2fd0dc9a5cc76f59b14068b83426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63540080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fbdb969ae579454f2552dc7a5db01e6ab557c9e18b798ebd0c97fa73920a14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["/bin/sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4b70a44519145916f8803166c99c3ba52ea4bf109ad21b6d3e97aaa6f17a6`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db919974f422fe094695197712c3932f2f53b2941206fb854ced215414963d4e`  
		Last Modified: Sat, 07 Sep 2024 11:57:52 GMT  
		Size: 2.5 MB (2530619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e67708f7300292967538b2b447a952fac80c63223b66037df5292b0016fd615`  
		Last Modified: Sat, 07 Sep 2024 11:58:25 GMT  
		Size: 56.9 MB (56921208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3ef821c8bb10a4ff3a2638095a296ec255014d4d1f8f8b12812d0d9ca47f94`  
		Last Modified: Sat, 07 Sep 2024 11:58:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:1cd8d33254705beda1e543deb90bb1799f7824469384d41fdb60a7719500a1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1066073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e7f4271336d69ddbcfa834f69bfeec190b89141fa1ea109903385a650720e6`

```dockerfile
```

-	Layers:
	-	`sha256:92ba2e90787eb65a0a0c9642a8aadc906d692a37b3885951db68885164430250`  
		Last Modified: Sat, 07 Sep 2024 11:58:24 GMT  
		Size: 1.1 MB (1051063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42fdfcd789dcecad4489fca68e75e1d75529cc853d3067b6e41f78c5fa5efc96`  
		Last Modified: Sat, 07 Sep 2024 11:58:23 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30.3`

```console
$ docker pull telegraf@sha256:f9b07f91ee00779f552a87b92ebd41124a91fd7de2d9d87a5d734d7ee4d18fd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30.3` - linux; amd64

```console
$ docker pull telegraf@sha256:789c8f2b68ce3116613d7578051629460280362589579124e242480055177eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155324989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d601c47b2cc76418082ed9e1affc1bb9da207e1883af6e28333a3996d8ae6e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Sep 2024 19:33:37 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 19:33:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1433b93c8b559e6f077106926b0a6a9a32dbc73b562f117de1450b76442d61dd`  
		Last Modified: Fri, 27 Sep 2024 06:15:45 GMT  
		Size: 18.9 MB (18947989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d1da800c36d534d38e317ac23a00e45efe8edf5ce1ce05541b3a10aa10a772`  
		Last Modified: Fri, 27 Sep 2024 06:15:44 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c60714d315d09052b5efd4905d4776944d649cfc4ac92af354c042710e42e6`  
		Last Modified: Fri, 27 Sep 2024 06:15:45 GMT  
		Size: 62.8 MB (62766489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9319cb924fe464a782425551f8838b2cf1392fc1f24681f0013c70256e9471`  
		Last Modified: Fri, 27 Sep 2024 06:15:44 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:d496142000a76541ec49dd4526bf55a28231609800d7f43851e2966109bd58f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9849fcce6e1935186295ed9fcfc984fad7b4dab472485640cd5adfaed5657b`

```dockerfile
```

-	Layers:
	-	`sha256:e82d0c6fc341cc9b98329f2add557eb87e5698af3368864437b173693ef83437`  
		Last Modified: Fri, 27 Sep 2024 06:15:44 GMT  
		Size: 6.4 MB (6391138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43b5c9037050ada1a77a95ea12c85f8e38a1f8131007b72093265a5fdd0481bd`  
		Last Modified: Fri, 27 Sep 2024 06:15:44 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:4782dee2276712745401413352f156c2ee3ef3a9f5e9c0010dcca8db1fa062d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143045412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7de357d252cdbab2eccea80863477b9b488d48742248f9aea323dfeeef722ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Sep 2024 19:33:37 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 19:33:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6b3cf1834faf48a7863802a88d183d7c882c279894a2875ceab123807eb3e0`  
		Last Modified: Sat, 28 Sep 2024 04:09:58 GMT  
		Size: 17.7 MB (17724904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc1bcf3dddedf4b1504712d28eec4c85ca3531dfc940b394aca29a5c91d734b`  
		Last Modified: Sat, 28 Sep 2024 04:09:57 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c071b30591b99ff308ecb3f8c9af9945b98a2fecdfccc306d3fe8a9133b2f9d6`  
		Last Modified: Sat, 28 Sep 2024 04:09:59 GMT  
		Size: 58.2 MB (58212651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6891cc87680d8207ea4a4bf1672a7b98fec600b3180a095ba1528c896a3409`  
		Last Modified: Sat, 28 Sep 2024 04:09:57 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:14ffdda7a0c9ac41b76b2b2ce2f6a28b573a6186ef01d128343b3e85671b3784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6633aff21924d548a9e76f784a15e669b05d662d6726ea8c82b8abeebdd79cce`

```dockerfile
```

-	Layers:
	-	`sha256:bd8390032549e060ea8748bcd26893f05b488c5b1937e50e7b3e2365259316e2`  
		Last Modified: Sat, 28 Sep 2024 04:09:58 GMT  
		Size: 6.4 MB (6385777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:715e45f33d8a5fb1478e7199d42ed7d29194faf16895275144ad54cb919f7384`  
		Last Modified: Sat, 28 Sep 2024 04:09:57 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:bfb7889d7f35a96a3c9591b5a59fd4f45462c5e7dbb7a23fe3cd1243d85aae5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149175253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ee5f497b0fb4089aa43beda3236ef8916bfe185483666906fdef28340099be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Sep 2024 19:33:37 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 19:33:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a5e311e8602fb4adc997da60dc66e9b3fdbb48311a540c7c6f3e63afef030b`  
		Last Modified: Fri, 27 Sep 2024 23:54:12 GMT  
		Size: 18.9 MB (18870648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb152dfb28ebda156d29a36e88b6e3501988064995d55089c376c3012aac1ed6`  
		Last Modified: Fri, 27 Sep 2024 23:54:11 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b91b648b2cc734f3ceef33b217323c31801d76e48bc1dfa57975c9f39090f31`  
		Last Modified: Fri, 27 Sep 2024 23:54:13 GMT  
		Size: 57.1 MB (57123272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79e50083399a6467b414ad030bcd64149249787406a956a634718e68e909843`  
		Last Modified: Fri, 27 Sep 2024 23:54:11 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:314831f63854fd73fc65d2520279f84e92a32dab1fc92b60e40fba6aa8fe7439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4262b38530bf18496b005006c3d62d0f494a7f21342f524df0d44df2dbc2b9cf`

```dockerfile
```

-	Layers:
	-	`sha256:eaef863517add38947256743ed1d7e9f73a34e2b3aa3a0a822cec3e559b28ca6`  
		Last Modified: Fri, 27 Sep 2024 23:54:12 GMT  
		Size: 6.4 MB (6391061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c683f482f406c0d3e40351632136d0c37825bab9abb12f240a8ac499e0996cbc`  
		Last Modified: Fri, 27 Sep 2024 23:54:11 GMT  
		Size: 14.6 KB (14617 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30.3-alpine`

```console
$ docker pull telegraf@sha256:e9e93edb70da8d8b89af431a98e510ab8efe719b2e0581a7360fcdf78f0e2a95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f204a64e42da80d96c8ed82613253bf3649d7aadccefc5a667e47d6e40e834ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68637698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18bb0214a0965f70002d5358dcf43d85e106e0f5acfe0ed9f1abe26b0353932`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["/bin/sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e0021259f7a43d4a51ff9aee4e5370c38c6b29f581a2f3917b9425788389e7`  
		Last Modified: Fri, 06 Sep 2024 23:24:59 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb5673a8ee4bb44fb3c81f4d9550f573a638290e03cbd4e6a25c15da651174e`  
		Last Modified: Fri, 06 Sep 2024 23:25:00 GMT  
		Size: 2.4 MB (2444799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319f92d6bf7f9fb73eb304cbfc559e1f53f37ddc6ea75f43f4fba540bdd48aab`  
		Last Modified: Fri, 06 Sep 2024 23:25:01 GMT  
		Size: 62.6 MB (62568484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6290f46669fa74c561f37b059bef89d7c0978262b2b174c9d679e178dc69c189`  
		Last Modified: Fri, 06 Sep 2024 23:25:00 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:a6cd90301c5006163e8c49e4bcf59e680ed27cae2ffc1807bd78d70aabf61002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1070927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfc7684017c3e8e8a41cd89bda48b33a054c47f2f180d2a7538cf7454ba3808`

```dockerfile
```

-	Layers:
	-	`sha256:af0f2bf20de1328a4327eebc5922312f834863b7cc0fccd141b387059835f300`  
		Last Modified: Fri, 06 Sep 2024 23:25:00 GMT  
		Size: 1.1 MB (1056193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c94f580866058dbce4eef3bfe30f18fc33f9a5459a6f1a6b7ccc3fac94acf2`  
		Last Modified: Fri, 06 Sep 2024 23:24:59 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c0a48224b1fac0a7ec76fb965f8a0f14197c2fd0dc9a5cc76f59b14068b83426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63540080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fbdb969ae579454f2552dc7a5db01e6ab557c9e18b798ebd0c97fa73920a14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["/bin/sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4b70a44519145916f8803166c99c3ba52ea4bf109ad21b6d3e97aaa6f17a6`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db919974f422fe094695197712c3932f2f53b2941206fb854ced215414963d4e`  
		Last Modified: Sat, 07 Sep 2024 11:57:52 GMT  
		Size: 2.5 MB (2530619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e67708f7300292967538b2b447a952fac80c63223b66037df5292b0016fd615`  
		Last Modified: Sat, 07 Sep 2024 11:58:25 GMT  
		Size: 56.9 MB (56921208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3ef821c8bb10a4ff3a2638095a296ec255014d4d1f8f8b12812d0d9ca47f94`  
		Last Modified: Sat, 07 Sep 2024 11:58:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:1cd8d33254705beda1e543deb90bb1799f7824469384d41fdb60a7719500a1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1066073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e7f4271336d69ddbcfa834f69bfeec190b89141fa1ea109903385a650720e6`

```dockerfile
```

-	Layers:
	-	`sha256:92ba2e90787eb65a0a0c9642a8aadc906d692a37b3885951db68885164430250`  
		Last Modified: Sat, 07 Sep 2024 11:58:24 GMT  
		Size: 1.1 MB (1051063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42fdfcd789dcecad4489fca68e75e1d75529cc853d3067b6e41f78c5fa5efc96`  
		Last Modified: Sat, 07 Sep 2024 11:58:23 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31`

```console
$ docker pull telegraf@sha256:dd6c94fcad6201c5a1dad17fcf673d55f5b908879b5c28445bb3c95069ba7389
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
$ docker pull telegraf@sha256:cb426a07c5bd674a9fd0ff12e6f7d706c745295817196337797e9f72fa88028a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158843851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9430a17d41e9eaf0dee1cb5e96ed74d912706a7884a86e64872edcf556980c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Sep 2024 19:33:37 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 19:33:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8894bc810747ca113f515ee951e4d935c0966f21346e46d1e43f5a462d130f8c`  
		Last Modified: Fri, 27 Sep 2024 06:16:05 GMT  
		Size: 18.9 MB (18947913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1be4d32b5f8f6c760c7ac538b92d96e5aceb20ceb2933855b8494b983ae6df`  
		Last Modified: Fri, 27 Sep 2024 06:16:04 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14bd6c1e8afec7a29e4a712e5191ed735a290425816687e7d1c87538da83148`  
		Last Modified: Fri, 27 Sep 2024 06:16:06 GMT  
		Size: 66.3 MB (66285439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6cd8d8edc92129583645483a2d73228939df1f0f7ad14319f2ae60f0053e75`  
		Last Modified: Fri, 27 Sep 2024 06:16:04 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:fe33004f717e662d0569f9320d3f91447a9821fc32af072c3ca8ceb0ad8d9aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6413670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d916eac86eb0b070c4eb1b820fe9b7d727389430903a64c140fdfb830ad4663`

```dockerfile
```

-	Layers:
	-	`sha256:48a464fdce5c2141198a4671f9fc140fa86995f75fc727a9850b69cd80e44208`  
		Last Modified: Fri, 27 Sep 2024 06:16:05 GMT  
		Size: 6.4 MB (6399346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89760ecfc7ce1304cec7904434ec4daef1d249f2fd946a781dd30693a034a621`  
		Last Modified: Fri, 27 Sep 2024 06:16:04 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:c9c3796d337b23652196defde5f5847846378261eac321f9ad1f42d263551532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146505025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c2c81f5fd206d9289934f6835516f0e375ccb7489062532c5e05937b01fa10`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Sep 2024 19:33:37 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 19:33:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6b3cf1834faf48a7863802a88d183d7c882c279894a2875ceab123807eb3e0`  
		Last Modified: Sat, 28 Sep 2024 04:09:58 GMT  
		Size: 17.7 MB (17724904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc1bcf3dddedf4b1504712d28eec4c85ca3531dfc940b394aca29a5c91d734b`  
		Last Modified: Sat, 28 Sep 2024 04:09:57 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d6f2d4a6d7875efcc53cf4c8d8b8478576c9eca4f49dc7fdf6f72dbea57049`  
		Last Modified: Sat, 28 Sep 2024 04:10:55 GMT  
		Size: 61.7 MB (61672264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55cb566960c6e38751dcbb12811f18bcfbf7114dd337e9bb7ef0d93f7a772bd`  
		Last Modified: Sat, 28 Sep 2024 04:10:53 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:8980f51e85b0d982a9f034d58a942c2ae28147eef656bc9b2e7850dcacce0b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6409186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bfad38d0326407cf7ddd13a9a22a059bd383e0156ce5b3a79fe8c41ea6af74`

```dockerfile
```

-	Layers:
	-	`sha256:d475520f06ca2a0082d04f9bf11a97a54a896320b574b78fdc3d1bcbd77a0e88`  
		Last Modified: Sat, 28 Sep 2024 04:10:53 GMT  
		Size: 6.4 MB (6394782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79f09ced08e765f48a8a25489a4c5841ab1f7b71ab96ea60a281486efa9231a8`  
		Last Modified: Sat, 28 Sep 2024 04:10:53 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0a5afe7ab9edbf3168b2c2a2dee20bda842312faddd0323167d8f13ad2e5c23d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152429723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8642587799295c253e4747b1cce9c1d9cb0983a14f47143577cac2a1ec71e96b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Sep 2024 19:33:37 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 19:33:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a5e311e8602fb4adc997da60dc66e9b3fdbb48311a540c7c6f3e63afef030b`  
		Last Modified: Fri, 27 Sep 2024 23:54:12 GMT  
		Size: 18.9 MB (18870648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb152dfb28ebda156d29a36e88b6e3501988064995d55089c376c3012aac1ed6`  
		Last Modified: Fri, 27 Sep 2024 23:54:11 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e442da107b337392c4df5b1dd4149374b0bdab4bb78808eb10bb3b3036d8ee21`  
		Last Modified: Fri, 27 Sep 2024 23:54:49 GMT  
		Size: 60.4 MB (60377739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c79b650ba333513e63633930dbbec61bca52873ad3de66ea5d760e5694f621d`  
		Last Modified: Fri, 27 Sep 2024 23:54:47 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:9e11e39d8e983e1e6ad25c42f11c98ad0aa4ddd7ff664d291df20fb307a45841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6415478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8757f1035dc788b4caf16f7f2673bdb91fce16471ab7a84f77f550120aec83c0`

```dockerfile
```

-	Layers:
	-	`sha256:25df675be8f95b40d3f7f1794e4513b7dc9f04adb5847ff78a8eb0bbb8f7fdc3`  
		Last Modified: Fri, 27 Sep 2024 23:54:48 GMT  
		Size: 6.4 MB (6400861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:033bbdd4f9de790e54c90a84dde815185c8ad00927de4f9eb440dba320939413`  
		Last Modified: Fri, 27 Sep 2024 23:54:47 GMT  
		Size: 14.6 KB (14617 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31-alpine`

```console
$ docker pull telegraf@sha256:b78b498e94d710030a84f1234c84ba2c53236bfbf46b06e7a6e37c8047f00ad3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:16daff872dcd602d6682904d3ede0c72ce5296b7b176dc5d31da0594813da9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72149456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3ad30f110753f70688097d344cf3b2e396a418439ae0e756693b15ef5c7696`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["/bin/sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62ec09d7a341b60e44a50a82c0a1fa1d180945697b2e6eee3ae259dbbaa85c7`  
		Last Modified: Fri, 06 Sep 2024 23:24:59 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce20c423b4b23f77e61da05477f8377a20c7d6f77d9ea27949653e40b2f6d2f`  
		Last Modified: Fri, 06 Sep 2024 23:24:59 GMT  
		Size: 2.4 MB (2444795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97c7b2edb13f5c70d230dbf4d5540df9f5e1c5ff16b3a7cd159b226b61d28f8`  
		Last Modified: Fri, 06 Sep 2024 23:25:00 GMT  
		Size: 66.1 MB (66080247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2900ca1a68499f072eed9cf13c8da01fafc0480017ceca8f6f36f00833e7ccd6`  
		Last Modified: Fri, 06 Sep 2024 23:24:59 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:56fc016a4c5dd60a703f51fa0c2f889b875482d3f68e77b31dc6c0a565035d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1079739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8381e7f1304c5dc7aead6fb12c8a29867621c096c8e9cde32e857dcf487eda96`

```dockerfile
```

-	Layers:
	-	`sha256:637befdbe25763e391c62a9e81b52c013b29ed34065dbd32a7ddf6681653fe72`  
		Last Modified: Fri, 06 Sep 2024 23:24:59 GMT  
		Size: 1.1 MB (1064703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:762b6501521af904ee02e2ea20c76821fcb1f85eae2d72d83df75be293e56069`  
		Last Modified: Fri, 06 Sep 2024 23:24:59 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8dd771749c30e38181cac4642625aa4d7f0a4272df725474207d3110a2539358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66790555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a462c147bb1486aedd0d407163105d2f371aecebd49fe99214e233fc9fde86b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["/bin/sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4b70a44519145916f8803166c99c3ba52ea4bf109ad21b6d3e97aaa6f17a6`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db919974f422fe094695197712c3932f2f53b2941206fb854ced215414963d4e`  
		Last Modified: Sat, 07 Sep 2024 11:57:52 GMT  
		Size: 2.5 MB (2530619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f98bba1c3177a002078eeb4b0b81b0bad71f6a7b6f2e65a5f400ec0727bd27`  
		Last Modified: Sat, 07 Sep 2024 11:58:56 GMT  
		Size: 60.2 MB (60171685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b28765732beff23a54f0e5e9188027832ff4570934fa1e9190ea84f8ff7130f`  
		Last Modified: Sat, 07 Sep 2024 11:58:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:fb4962af6a600ab02dbe30fa3f394caf2fbb4d1545fb7b01aae8c5d83f781b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1076499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d5eac083ed899eb1035be4249c6626c1896fab526fb80739cafa1bd8d5dd1b`

```dockerfile
```

-	Layers:
	-	`sha256:e93bab49c2bd0b672f9c423d312dead46e29d3a014fc4f7a95b4d0e7cae1c494`  
		Last Modified: Sat, 07 Sep 2024 11:58:55 GMT  
		Size: 1.1 MB (1061177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69032c1d7d91b916842cad44ce3d2280efde144eb3bc798db4bd6e3e233a31ce`  
		Last Modified: Sat, 07 Sep 2024 11:58:55 GMT  
		Size: 15.3 KB (15322 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.3`

```console
$ docker pull telegraf@sha256:dd6c94fcad6201c5a1dad17fcf673d55f5b908879b5c28445bb3c95069ba7389
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
$ docker pull telegraf@sha256:cb426a07c5bd674a9fd0ff12e6f7d706c745295817196337797e9f72fa88028a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158843851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9430a17d41e9eaf0dee1cb5e96ed74d912706a7884a86e64872edcf556980c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Sep 2024 19:33:37 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 19:33:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8894bc810747ca113f515ee951e4d935c0966f21346e46d1e43f5a462d130f8c`  
		Last Modified: Fri, 27 Sep 2024 06:16:05 GMT  
		Size: 18.9 MB (18947913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1be4d32b5f8f6c760c7ac538b92d96e5aceb20ceb2933855b8494b983ae6df`  
		Last Modified: Fri, 27 Sep 2024 06:16:04 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14bd6c1e8afec7a29e4a712e5191ed735a290425816687e7d1c87538da83148`  
		Last Modified: Fri, 27 Sep 2024 06:16:06 GMT  
		Size: 66.3 MB (66285439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6cd8d8edc92129583645483a2d73228939df1f0f7ad14319f2ae60f0053e75`  
		Last Modified: Fri, 27 Sep 2024 06:16:04 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:fe33004f717e662d0569f9320d3f91447a9821fc32af072c3ca8ceb0ad8d9aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6413670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d916eac86eb0b070c4eb1b820fe9b7d727389430903a64c140fdfb830ad4663`

```dockerfile
```

-	Layers:
	-	`sha256:48a464fdce5c2141198a4671f9fc140fa86995f75fc727a9850b69cd80e44208`  
		Last Modified: Fri, 27 Sep 2024 06:16:05 GMT  
		Size: 6.4 MB (6399346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89760ecfc7ce1304cec7904434ec4daef1d249f2fd946a781dd30693a034a621`  
		Last Modified: Fri, 27 Sep 2024 06:16:04 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:c9c3796d337b23652196defde5f5847846378261eac321f9ad1f42d263551532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146505025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c2c81f5fd206d9289934f6835516f0e375ccb7489062532c5e05937b01fa10`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Sep 2024 19:33:37 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 19:33:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6b3cf1834faf48a7863802a88d183d7c882c279894a2875ceab123807eb3e0`  
		Last Modified: Sat, 28 Sep 2024 04:09:58 GMT  
		Size: 17.7 MB (17724904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc1bcf3dddedf4b1504712d28eec4c85ca3531dfc940b394aca29a5c91d734b`  
		Last Modified: Sat, 28 Sep 2024 04:09:57 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d6f2d4a6d7875efcc53cf4c8d8b8478576c9eca4f49dc7fdf6f72dbea57049`  
		Last Modified: Sat, 28 Sep 2024 04:10:55 GMT  
		Size: 61.7 MB (61672264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55cb566960c6e38751dcbb12811f18bcfbf7114dd337e9bb7ef0d93f7a772bd`  
		Last Modified: Sat, 28 Sep 2024 04:10:53 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:8980f51e85b0d982a9f034d58a942c2ae28147eef656bc9b2e7850dcacce0b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6409186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bfad38d0326407cf7ddd13a9a22a059bd383e0156ce5b3a79fe8c41ea6af74`

```dockerfile
```

-	Layers:
	-	`sha256:d475520f06ca2a0082d04f9bf11a97a54a896320b574b78fdc3d1bcbd77a0e88`  
		Last Modified: Sat, 28 Sep 2024 04:10:53 GMT  
		Size: 6.4 MB (6394782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79f09ced08e765f48a8a25489a4c5841ab1f7b71ab96ea60a281486efa9231a8`  
		Last Modified: Sat, 28 Sep 2024 04:10:53 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0a5afe7ab9edbf3168b2c2a2dee20bda842312faddd0323167d8f13ad2e5c23d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152429723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8642587799295c253e4747b1cce9c1d9cb0983a14f47143577cac2a1ec71e96b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Sep 2024 19:33:37 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 19:33:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a5e311e8602fb4adc997da60dc66e9b3fdbb48311a540c7c6f3e63afef030b`  
		Last Modified: Fri, 27 Sep 2024 23:54:12 GMT  
		Size: 18.9 MB (18870648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb152dfb28ebda156d29a36e88b6e3501988064995d55089c376c3012aac1ed6`  
		Last Modified: Fri, 27 Sep 2024 23:54:11 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e442da107b337392c4df5b1dd4149374b0bdab4bb78808eb10bb3b3036d8ee21`  
		Last Modified: Fri, 27 Sep 2024 23:54:49 GMT  
		Size: 60.4 MB (60377739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c79b650ba333513e63633930dbbec61bca52873ad3de66ea5d760e5694f621d`  
		Last Modified: Fri, 27 Sep 2024 23:54:47 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:9e11e39d8e983e1e6ad25c42f11c98ad0aa4ddd7ff664d291df20fb307a45841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6415478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8757f1035dc788b4caf16f7f2673bdb91fce16471ab7a84f77f550120aec83c0`

```dockerfile
```

-	Layers:
	-	`sha256:25df675be8f95b40d3f7f1794e4513b7dc9f04adb5847ff78a8eb0bbb8f7fdc3`  
		Last Modified: Fri, 27 Sep 2024 23:54:48 GMT  
		Size: 6.4 MB (6400861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:033bbdd4f9de790e54c90a84dde815185c8ad00927de4f9eb440dba320939413`  
		Last Modified: Fri, 27 Sep 2024 23:54:47 GMT  
		Size: 14.6 KB (14617 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.3-alpine`

```console
$ docker pull telegraf@sha256:b78b498e94d710030a84f1234c84ba2c53236bfbf46b06e7a6e37c8047f00ad3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:16daff872dcd602d6682904d3ede0c72ce5296b7b176dc5d31da0594813da9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72149456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3ad30f110753f70688097d344cf3b2e396a418439ae0e756693b15ef5c7696`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["/bin/sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62ec09d7a341b60e44a50a82c0a1fa1d180945697b2e6eee3ae259dbbaa85c7`  
		Last Modified: Fri, 06 Sep 2024 23:24:59 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce20c423b4b23f77e61da05477f8377a20c7d6f77d9ea27949653e40b2f6d2f`  
		Last Modified: Fri, 06 Sep 2024 23:24:59 GMT  
		Size: 2.4 MB (2444795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97c7b2edb13f5c70d230dbf4d5540df9f5e1c5ff16b3a7cd159b226b61d28f8`  
		Last Modified: Fri, 06 Sep 2024 23:25:00 GMT  
		Size: 66.1 MB (66080247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2900ca1a68499f072eed9cf13c8da01fafc0480017ceca8f6f36f00833e7ccd6`  
		Last Modified: Fri, 06 Sep 2024 23:24:59 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:56fc016a4c5dd60a703f51fa0c2f889b875482d3f68e77b31dc6c0a565035d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1079739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8381e7f1304c5dc7aead6fb12c8a29867621c096c8e9cde32e857dcf487eda96`

```dockerfile
```

-	Layers:
	-	`sha256:637befdbe25763e391c62a9e81b52c013b29ed34065dbd32a7ddf6681653fe72`  
		Last Modified: Fri, 06 Sep 2024 23:24:59 GMT  
		Size: 1.1 MB (1064703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:762b6501521af904ee02e2ea20c76821fcb1f85eae2d72d83df75be293e56069`  
		Last Modified: Fri, 06 Sep 2024 23:24:59 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8dd771749c30e38181cac4642625aa4d7f0a4272df725474207d3110a2539358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66790555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a462c147bb1486aedd0d407163105d2f371aecebd49fe99214e233fc9fde86b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["/bin/sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4b70a44519145916f8803166c99c3ba52ea4bf109ad21b6d3e97aaa6f17a6`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db919974f422fe094695197712c3932f2f53b2941206fb854ced215414963d4e`  
		Last Modified: Sat, 07 Sep 2024 11:57:52 GMT  
		Size: 2.5 MB (2530619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f98bba1c3177a002078eeb4b0b81b0bad71f6a7b6f2e65a5f400ec0727bd27`  
		Last Modified: Sat, 07 Sep 2024 11:58:56 GMT  
		Size: 60.2 MB (60171685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b28765732beff23a54f0e5e9188027832ff4570934fa1e9190ea84f8ff7130f`  
		Last Modified: Sat, 07 Sep 2024 11:58:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:fb4962af6a600ab02dbe30fa3f394caf2fbb4d1545fb7b01aae8c5d83f781b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1076499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d5eac083ed899eb1035be4249c6626c1896fab526fb80739cafa1bd8d5dd1b`

```dockerfile
```

-	Layers:
	-	`sha256:e93bab49c2bd0b672f9c423d312dead46e29d3a014fc4f7a95b4d0e7cae1c494`  
		Last Modified: Sat, 07 Sep 2024 11:58:55 GMT  
		Size: 1.1 MB (1061177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69032c1d7d91b916842cad44ce3d2280efde144eb3bc798db4bd6e3e233a31ce`  
		Last Modified: Sat, 07 Sep 2024 11:58:55 GMT  
		Size: 15.3 KB (15322 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32`

```console
$ docker pull telegraf@sha256:b415e563e59e725ebaaf564413583c3339cf98be03f49b68d26ccfcaaad26713
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
$ docker pull telegraf@sha256:6bdf0c400821df1cdc0588f235dec2c2d1aa6937faee52b6a3debf2514e80714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163158564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf8546f179ecfeaf19db55c84cfbca7a2484d7573683a1af8808f8564395760`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Sep 2024 19:33:37 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 19:33:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.32.0
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a09ad81b3e57520b06fb56e67b0a0ee7cc0cb05a47c4fef65d4dd1f80309c4`  
		Last Modified: Fri, 27 Sep 2024 06:16:16 GMT  
		Size: 18.9 MB (18947911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c474793bbad3ff20d3097566b4aa09c6b2cd661efbb9d300a3b65f99061bf1`  
		Last Modified: Fri, 27 Sep 2024 06:16:15 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e744105db1a075e56811824edb76c452d77f03d830029ef21466c66cc9a3499`  
		Last Modified: Fri, 27 Sep 2024 06:16:17 GMT  
		Size: 70.6 MB (70600144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca64fec051937c1363352bb5de026e3c33dd4f69ab9e18c4fa94acafc2761f4b`  
		Last Modified: Fri, 27 Sep 2024 06:16:16 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:5340560842cb469f0ed04e1472969f02bee4ecedf5018f93d4c166b6528de61d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6423738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74dce79bf05646939438da6c8d2cdde5d61efa16ad1e691aebbb0fe21ef15b0`

```dockerfile
```

-	Layers:
	-	`sha256:844c5bab82ebce7f86e2ad4368161c3987614cac30a3651a9f68e25cfe683ac9`  
		Last Modified: Fri, 27 Sep 2024 06:16:16 GMT  
		Size: 6.4 MB (6409112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8af7817d96f257a8a0f171b2a02048e7481eb7792e1401e57dc4a67aa2b8888`  
		Last Modified: Fri, 27 Sep 2024 06:16:16 GMT  
		Size: 14.6 KB (14626 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:2ce3c2c334c5b71485023327cb1cf59ab35876847550ffb3d800340cba695883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150243306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a4fd81df29a137c52c81d7bbd3ff8fd1d7c4e12f32c255a66965a116aa944f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Sep 2024 19:33:37 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 19:33:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.32.0
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6b3cf1834faf48a7863802a88d183d7c882c279894a2875ceab123807eb3e0`  
		Last Modified: Sat, 28 Sep 2024 04:09:58 GMT  
		Size: 17.7 MB (17724904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc1bcf3dddedf4b1504712d28eec4c85ca3531dfc940b394aca29a5c91d734b`  
		Last Modified: Sat, 28 Sep 2024 04:09:57 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481f33f96fd0f8e52639b1118d9409547fed783c886aed8a88b997ade1a976fd`  
		Last Modified: Sat, 28 Sep 2024 04:11:51 GMT  
		Size: 65.4 MB (65410544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b450e7f94991a6ecc6bfd585254b9edfff166588f20d2339f4592a93fd5369cd`  
		Last Modified: Sat, 28 Sep 2024 04:11:49 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:ab0b8d848ac8fe1371b224ceb41529b9f4efbb537cd053d34e0467a8a538cb24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6419269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a50eceea3be53e9f648962f05e126c4296bd595fe65c2cd36f55f8ff7f2f27b`

```dockerfile
```

-	Layers:
	-	`sha256:7f783ba9dfeeddb2d67ac091e80f5d96b1b2a1781b9bfaa74524072843862fb8`  
		Last Modified: Sat, 28 Sep 2024 04:11:49 GMT  
		Size: 6.4 MB (6404556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e10290387388b2a2b2410d631b4a34a0374f7459b7f3d9b658925e7a4fb2d0`  
		Last Modified: Sat, 28 Sep 2024 04:11:49 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ff4d838ffb6141c3bc4598a438862eb4797ef1c85d132bb648ac0b6d4ceb2065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155704659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f98e54b8308fd957c2c466ce21fddd19dc7d689598b5f2e92810a1af6abd74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Sep 2024 19:33:37 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 19:33:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.32.0
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a5e311e8602fb4adc997da60dc66e9b3fdbb48311a540c7c6f3e63afef030b`  
		Last Modified: Fri, 27 Sep 2024 23:54:12 GMT  
		Size: 18.9 MB (18870648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb152dfb28ebda156d29a36e88b6e3501988064995d55089c376c3012aac1ed6`  
		Last Modified: Fri, 27 Sep 2024 23:54:11 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b8ffc5c29e81b17d840627fa8ea4a3d92b1e775ee95e9f43b12c6f8f46670b`  
		Last Modified: Fri, 27 Sep 2024 23:55:29 GMT  
		Size: 63.7 MB (63652673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9f8084122f8a636b02d5159268441a258c5624d1f430db92ff3c49df041c8d`  
		Last Modified: Fri, 27 Sep 2024 23:55:27 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:d6e11b8ec47af61358dc35c5b477f70e08df06f541579699bd4a706bb9710830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d2db25ffb51ac50947296593a4d047e90ee45de00ee5527a55da1ae63ce88c`

```dockerfile
```

-	Layers:
	-	`sha256:846bd798a45e40a162050bd8179bf159aa6d58b6c832b9b03cd6315c33e49114`  
		Last Modified: Fri, 27 Sep 2024 23:55:28 GMT  
		Size: 6.4 MB (6409842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15f97a9668b94231a528776e30a250d933be05374b9b26f42e816afcca5c5963`  
		Last Modified: Fri, 27 Sep 2024 23:55:27 GMT  
		Size: 14.9 KB (14931 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32-alpine`

```console
$ docker pull telegraf@sha256:fdf6d4bcdcfad281ac758edc437c63f8269b76029a32577228e92276e5816dae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:4b5bf7ee33971b587f6a56098b0a9dae5f433538e9b37fed00e380dda6771b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76465975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1158ceb0ee52558da6454d482326523f1d3a27a725f7649606f8786464192595`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.32.0
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8407248640ce51895daeb226fca47e0d9a489324a81cd5f7b29b3b3c858ea96`  
		Last Modified: Mon, 09 Sep 2024 21:00:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd456413a5ad81c1400225c0d58e2579dba79235bfe0e5be3f57d5ba75758e47`  
		Last Modified: Mon, 09 Sep 2024 21:00:51 GMT  
		Size: 2.4 MB (2444815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a4d1e24eb773b01d5bf5198476daa9da3e007efac326a4e0cd5e5b2e4f5e68`  
		Last Modified: Mon, 09 Sep 2024 21:00:53 GMT  
		Size: 70.4 MB (70396747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8662223dfa2a764e67ee8c53547c560fe46f82c85abfe6640b17bcacbd3bdd5f`  
		Last Modified: Mon, 09 Sep 2024 21:00:51 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:ce43df1cc0e45b4c4b4bb3c0ef2fc3f77bb38a18ffb48b08454e6e1e13774c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd59cb9fd39a2192d59fc30b317b541408ed82e0bcda8ebac7334cf82bd331fc`

```dockerfile
```

-	Layers:
	-	`sha256:a6cc0dfd496f8b51fbaf36e103bc5aeef5640e837bc3ecc19254e5dc6bd6280b`  
		Last Modified: Mon, 09 Sep 2024 21:00:51 GMT  
		Size: 1.1 MB (1074167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60f8df29aefc9a5cc62c9603f14a009df07208d6d1fbe234591b7be8123a66d6`  
		Last Modified: Mon, 09 Sep 2024 21:00:51 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:914be2639aa0528293e87d9a1c89521b7905b61ce05490ebf8ee06f19db00d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70064723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c452efd6c8109dea34cd886fc2f889130c7c09ea2c3bc1e7933990f91769caf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.32.0
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4b70a44519145916f8803166c99c3ba52ea4bf109ad21b6d3e97aaa6f17a6`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db919974f422fe094695197712c3932f2f53b2941206fb854ced215414963d4e`  
		Last Modified: Sat, 07 Sep 2024 11:57:52 GMT  
		Size: 2.5 MB (2530619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ce795c4e61b36d98415cebcbe5ae217a9496aae4855bbdac71015f558f269`  
		Last Modified: Tue, 10 Sep 2024 02:53:26 GMT  
		Size: 63.4 MB (63445850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d975a327eb6969aeeadae546b8e0124f9f6188afda9328174f97ff8c8320e9`  
		Last Modified: Tue, 10 Sep 2024 02:53:23 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:f97b4d7add54399904e669c2fe70978f48ce0aa3a4e637a0dd3da66268825798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1085168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b890cc6a9b66b7d8466df8cc5762b9fc42610dee02244681bee6c9d59ef30cb`

```dockerfile
```

-	Layers:
	-	`sha256:4af855bef43bba7766793187024c913cbd20e9e80becc1947b04811f3c6bcf5f`  
		Last Modified: Tue, 10 Sep 2024 02:53:24 GMT  
		Size: 1.1 MB (1069844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aced2b9a2b37dffba4ff1522bd3a9d2f4ed17da031b16267e646d868280c25a`  
		Last Modified: Tue, 10 Sep 2024 02:53:23 GMT  
		Size: 15.3 KB (15324 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32.1`

**does not exist** (yet?)

## `telegraf:1.32.1-alpine`

**does not exist** (yet?)

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:fdf6d4bcdcfad281ac758edc437c63f8269b76029a32577228e92276e5816dae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:4b5bf7ee33971b587f6a56098b0a9dae5f433538e9b37fed00e380dda6771b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76465975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1158ceb0ee52558da6454d482326523f1d3a27a725f7649606f8786464192595`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.32.0
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8407248640ce51895daeb226fca47e0d9a489324a81cd5f7b29b3b3c858ea96`  
		Last Modified: Mon, 09 Sep 2024 21:00:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd456413a5ad81c1400225c0d58e2579dba79235bfe0e5be3f57d5ba75758e47`  
		Last Modified: Mon, 09 Sep 2024 21:00:51 GMT  
		Size: 2.4 MB (2444815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a4d1e24eb773b01d5bf5198476daa9da3e007efac326a4e0cd5e5b2e4f5e68`  
		Last Modified: Mon, 09 Sep 2024 21:00:53 GMT  
		Size: 70.4 MB (70396747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8662223dfa2a764e67ee8c53547c560fe46f82c85abfe6640b17bcacbd3bdd5f`  
		Last Modified: Mon, 09 Sep 2024 21:00:51 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:ce43df1cc0e45b4c4b4bb3c0ef2fc3f77bb38a18ffb48b08454e6e1e13774c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd59cb9fd39a2192d59fc30b317b541408ed82e0bcda8ebac7334cf82bd331fc`

```dockerfile
```

-	Layers:
	-	`sha256:a6cc0dfd496f8b51fbaf36e103bc5aeef5640e837bc3ecc19254e5dc6bd6280b`  
		Last Modified: Mon, 09 Sep 2024 21:00:51 GMT  
		Size: 1.1 MB (1074167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60f8df29aefc9a5cc62c9603f14a009df07208d6d1fbe234591b7be8123a66d6`  
		Last Modified: Mon, 09 Sep 2024 21:00:51 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:914be2639aa0528293e87d9a1c89521b7905b61ce05490ebf8ee06f19db00d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70064723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c452efd6c8109dea34cd886fc2f889130c7c09ea2c3bc1e7933990f91769caf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.32.0
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4b70a44519145916f8803166c99c3ba52ea4bf109ad21b6d3e97aaa6f17a6`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db919974f422fe094695197712c3932f2f53b2941206fb854ced215414963d4e`  
		Last Modified: Sat, 07 Sep 2024 11:57:52 GMT  
		Size: 2.5 MB (2530619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ce795c4e61b36d98415cebcbe5ae217a9496aae4855bbdac71015f558f269`  
		Last Modified: Tue, 10 Sep 2024 02:53:26 GMT  
		Size: 63.4 MB (63445850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d975a327eb6969aeeadae546b8e0124f9f6188afda9328174f97ff8c8320e9`  
		Last Modified: Tue, 10 Sep 2024 02:53:23 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:f97b4d7add54399904e669c2fe70978f48ce0aa3a4e637a0dd3da66268825798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1085168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b890cc6a9b66b7d8466df8cc5762b9fc42610dee02244681bee6c9d59ef30cb`

```dockerfile
```

-	Layers:
	-	`sha256:4af855bef43bba7766793187024c913cbd20e9e80becc1947b04811f3c6bcf5f`  
		Last Modified: Tue, 10 Sep 2024 02:53:24 GMT  
		Size: 1.1 MB (1069844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aced2b9a2b37dffba4ff1522bd3a9d2f4ed17da031b16267e646d868280c25a`  
		Last Modified: Tue, 10 Sep 2024 02:53:23 GMT  
		Size: 15.3 KB (15324 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:b415e563e59e725ebaaf564413583c3339cf98be03f49b68d26ccfcaaad26713
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
$ docker pull telegraf@sha256:6bdf0c400821df1cdc0588f235dec2c2d1aa6937faee52b6a3debf2514e80714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163158564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf8546f179ecfeaf19db55c84cfbca7a2484d7573683a1af8808f8564395760`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Sep 2024 19:33:37 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 19:33:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.32.0
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a09ad81b3e57520b06fb56e67b0a0ee7cc0cb05a47c4fef65d4dd1f80309c4`  
		Last Modified: Fri, 27 Sep 2024 06:16:16 GMT  
		Size: 18.9 MB (18947911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c474793bbad3ff20d3097566b4aa09c6b2cd661efbb9d300a3b65f99061bf1`  
		Last Modified: Fri, 27 Sep 2024 06:16:15 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e744105db1a075e56811824edb76c452d77f03d830029ef21466c66cc9a3499`  
		Last Modified: Fri, 27 Sep 2024 06:16:17 GMT  
		Size: 70.6 MB (70600144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca64fec051937c1363352bb5de026e3c33dd4f69ab9e18c4fa94acafc2761f4b`  
		Last Modified: Fri, 27 Sep 2024 06:16:16 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:5340560842cb469f0ed04e1472969f02bee4ecedf5018f93d4c166b6528de61d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6423738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74dce79bf05646939438da6c8d2cdde5d61efa16ad1e691aebbb0fe21ef15b0`

```dockerfile
```

-	Layers:
	-	`sha256:844c5bab82ebce7f86e2ad4368161c3987614cac30a3651a9f68e25cfe683ac9`  
		Last Modified: Fri, 27 Sep 2024 06:16:16 GMT  
		Size: 6.4 MB (6409112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8af7817d96f257a8a0f171b2a02048e7481eb7792e1401e57dc4a67aa2b8888`  
		Last Modified: Fri, 27 Sep 2024 06:16:16 GMT  
		Size: 14.6 KB (14626 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:2ce3c2c334c5b71485023327cb1cf59ab35876847550ffb3d800340cba695883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150243306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a4fd81df29a137c52c81d7bbd3ff8fd1d7c4e12f32c255a66965a116aa944f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Sep 2024 19:33:37 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 19:33:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.32.0
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6b3cf1834faf48a7863802a88d183d7c882c279894a2875ceab123807eb3e0`  
		Last Modified: Sat, 28 Sep 2024 04:09:58 GMT  
		Size: 17.7 MB (17724904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc1bcf3dddedf4b1504712d28eec4c85ca3531dfc940b394aca29a5c91d734b`  
		Last Modified: Sat, 28 Sep 2024 04:09:57 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481f33f96fd0f8e52639b1118d9409547fed783c886aed8a88b997ade1a976fd`  
		Last Modified: Sat, 28 Sep 2024 04:11:51 GMT  
		Size: 65.4 MB (65410544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b450e7f94991a6ecc6bfd585254b9edfff166588f20d2339f4592a93fd5369cd`  
		Last Modified: Sat, 28 Sep 2024 04:11:49 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:ab0b8d848ac8fe1371b224ceb41529b9f4efbb537cd053d34e0467a8a538cb24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6419269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a50eceea3be53e9f648962f05e126c4296bd595fe65c2cd36f55f8ff7f2f27b`

```dockerfile
```

-	Layers:
	-	`sha256:7f783ba9dfeeddb2d67ac091e80f5d96b1b2a1781b9bfaa74524072843862fb8`  
		Last Modified: Sat, 28 Sep 2024 04:11:49 GMT  
		Size: 6.4 MB (6404556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e10290387388b2a2b2410d631b4a34a0374f7459b7f3d9b658925e7a4fb2d0`  
		Last Modified: Sat, 28 Sep 2024 04:11:49 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ff4d838ffb6141c3bc4598a438862eb4797ef1c85d132bb648ac0b6d4ceb2065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155704659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f98e54b8308fd957c2c466ce21fddd19dc7d689598b5f2e92810a1af6abd74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 09 Sep 2024 19:33:37 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 19:33:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.32.0
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a5e311e8602fb4adc997da60dc66e9b3fdbb48311a540c7c6f3e63afef030b`  
		Last Modified: Fri, 27 Sep 2024 23:54:12 GMT  
		Size: 18.9 MB (18870648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb152dfb28ebda156d29a36e88b6e3501988064995d55089c376c3012aac1ed6`  
		Last Modified: Fri, 27 Sep 2024 23:54:11 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b8ffc5c29e81b17d840627fa8ea4a3d92b1e775ee95e9f43b12c6f8f46670b`  
		Last Modified: Fri, 27 Sep 2024 23:55:29 GMT  
		Size: 63.7 MB (63652673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9f8084122f8a636b02d5159268441a258c5624d1f430db92ff3c49df041c8d`  
		Last Modified: Fri, 27 Sep 2024 23:55:27 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:d6e11b8ec47af61358dc35c5b477f70e08df06f541579699bd4a706bb9710830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d2db25ffb51ac50947296593a4d047e90ee45de00ee5527a55da1ae63ce88c`

```dockerfile
```

-	Layers:
	-	`sha256:846bd798a45e40a162050bd8179bf159aa6d58b6c832b9b03cd6315c33e49114`  
		Last Modified: Fri, 27 Sep 2024 23:55:28 GMT  
		Size: 6.4 MB (6409842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15f97a9668b94231a528776e30a250d933be05374b9b26f42e816afcca5c5963`  
		Last Modified: Fri, 27 Sep 2024 23:55:27 GMT  
		Size: 14.9 KB (14931 bytes)  
		MIME: application/vnd.in-toto+json
