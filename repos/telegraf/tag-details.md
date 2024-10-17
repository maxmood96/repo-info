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
$ docker pull telegraf@sha256:d61889bcbaf3ffb5d40434e08a1f35caa7c76aa98e242aa2b7747c31b0f4220d
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
$ docker pull telegraf@sha256:96f9a55cacd0dc8e847e4fe7074bd01caac2f340f10a23c76aef0ab31f15d7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155324847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b071ff1cdeb279e68f2ebcece63664bcdf5da3e9becfd58a458d5b934e6a06d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5f3b3f727e71a2c8e2d282f958aa488342e7a0edc7c26d994f1dbbb88c88d`  
		Last Modified: Thu, 17 Oct 2024 01:09:47 GMT  
		Size: 24.1 MB (24053088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9000e1067b38ce9eead338a45b20246f31badb1b692623262aeec57c1c5171`  
		Last Modified: Thu, 17 Oct 2024 02:58:37 GMT  
		Size: 18.9 MB (18947890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec3af90ab09cd596dcf44fda648026a8e2a0fc543e431d41e9a9ab1fbeabd7f`  
		Last Modified: Thu, 17 Oct 2024 02:58:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13354cb61b8a605b0a43c14a2e4c2e624de5964c533f1f51edb1184184cc857`  
		Last Modified: Thu, 17 Oct 2024 02:58:38 GMT  
		Size: 62.8 MB (62766453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a802126f6b225f2c4ebd9216350310e8c015a3656240049acb81b1231e61d29`  
		Last Modified: Thu, 17 Oct 2024 02:58:35 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:d73610f879c318b37c88a18db321af2b6b4a6bf10e1bdfb9048e1c39fc6366c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9cdc51c4a040761c3aa9a420a5e054ce5e84c88ec4495c5a461d4c0f8c1806`

```dockerfile
```

-	Layers:
	-	`sha256:a1d2599f8ed1989b68a65e5164aab8c8c7701cfffc86e1c569d981d5ec75f348`  
		Last Modified: Thu, 17 Oct 2024 02:58:37 GMT  
		Size: 6.4 MB (6391138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8161253d365cb1e7ba4182b7f4edf9b1489d1a4b9757fd48d4244781b8e352d`  
		Last Modified: Thu, 17 Oct 2024 02:58:37 GMT  
		Size: 14.4 KB (14362 bytes)  
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
$ docker pull telegraf@sha256:d61889bcbaf3ffb5d40434e08a1f35caa7c76aa98e242aa2b7747c31b0f4220d
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
$ docker pull telegraf@sha256:96f9a55cacd0dc8e847e4fe7074bd01caac2f340f10a23c76aef0ab31f15d7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155324847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b071ff1cdeb279e68f2ebcece63664bcdf5da3e9becfd58a458d5b934e6a06d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5f3b3f727e71a2c8e2d282f958aa488342e7a0edc7c26d994f1dbbb88c88d`  
		Last Modified: Thu, 17 Oct 2024 01:09:47 GMT  
		Size: 24.1 MB (24053088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9000e1067b38ce9eead338a45b20246f31badb1b692623262aeec57c1c5171`  
		Last Modified: Thu, 17 Oct 2024 02:58:37 GMT  
		Size: 18.9 MB (18947890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec3af90ab09cd596dcf44fda648026a8e2a0fc543e431d41e9a9ab1fbeabd7f`  
		Last Modified: Thu, 17 Oct 2024 02:58:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13354cb61b8a605b0a43c14a2e4c2e624de5964c533f1f51edb1184184cc857`  
		Last Modified: Thu, 17 Oct 2024 02:58:38 GMT  
		Size: 62.8 MB (62766453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a802126f6b225f2c4ebd9216350310e8c015a3656240049acb81b1231e61d29`  
		Last Modified: Thu, 17 Oct 2024 02:58:35 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:d73610f879c318b37c88a18db321af2b6b4a6bf10e1bdfb9048e1c39fc6366c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9cdc51c4a040761c3aa9a420a5e054ce5e84c88ec4495c5a461d4c0f8c1806`

```dockerfile
```

-	Layers:
	-	`sha256:a1d2599f8ed1989b68a65e5164aab8c8c7701cfffc86e1c569d981d5ec75f348`  
		Last Modified: Thu, 17 Oct 2024 02:58:37 GMT  
		Size: 6.4 MB (6391138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8161253d365cb1e7ba4182b7f4edf9b1489d1a4b9757fd48d4244781b8e352d`  
		Last Modified: Thu, 17 Oct 2024 02:58:37 GMT  
		Size: 14.4 KB (14362 bytes)  
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
$ docker pull telegraf@sha256:11f59d4dd4d7e804bb23f670f7866a40d3204673e44f1e850a5f18f775ca433d
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
$ docker pull telegraf@sha256:d49b0a59288a495d0543afadcd0d6ca17d422174731da98167ef0bc525bac069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158843879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9b2c81bfba827921bf2a8f58fc9ca49c899f9ef4065ca4d68587345be3c993`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5f3b3f727e71a2c8e2d282f958aa488342e7a0edc7c26d994f1dbbb88c88d`  
		Last Modified: Thu, 17 Oct 2024 01:09:47 GMT  
		Size: 24.1 MB (24053088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f8d5c28c5b58b00ce262bb73a621a7af0b4b09fe89bc22e4df30ef2b6971fd`  
		Last Modified: Thu, 17 Oct 2024 02:58:36 GMT  
		Size: 18.9 MB (18947926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfa986252c82e40ce1fee86c5280aa85b37dab922ffc9bef9aac548dd60d49c`  
		Last Modified: Thu, 17 Oct 2024 02:58:35 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc152baccadedea7cc53100685dbc71611d4c76524e720cb8fcda6266d7ae04`  
		Last Modified: Thu, 17 Oct 2024 02:58:36 GMT  
		Size: 66.3 MB (66285437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a802126f6b225f2c4ebd9216350310e8c015a3656240049acb81b1231e61d29`  
		Last Modified: Thu, 17 Oct 2024 02:58:35 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:f8ead2c0517da1bf91fc238d53925a8cbbe5b3d56c790b30fdde84989a3f560f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6413708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a6179f191a709e8ac92eae29b91d3971f57796682623ffab0bef0ff644c22a`

```dockerfile
```

-	Layers:
	-	`sha256:2dc34580a414327d0c7e4e696cd94d97720ef1ff772807af7874a88a6b2e849e`  
		Last Modified: Thu, 17 Oct 2024 02:58:35 GMT  
		Size: 6.4 MB (6399346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39bbe8612c8eb95108af2790e8c28986a9811ca672d4358f2f33424804ca8419`  
		Last Modified: Thu, 17 Oct 2024 02:58:35 GMT  
		Size: 14.4 KB (14362 bytes)  
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
$ docker pull telegraf@sha256:11f59d4dd4d7e804bb23f670f7866a40d3204673e44f1e850a5f18f775ca433d
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
$ docker pull telegraf@sha256:d49b0a59288a495d0543afadcd0d6ca17d422174731da98167ef0bc525bac069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158843879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9b2c81bfba827921bf2a8f58fc9ca49c899f9ef4065ca4d68587345be3c993`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5f3b3f727e71a2c8e2d282f958aa488342e7a0edc7c26d994f1dbbb88c88d`  
		Last Modified: Thu, 17 Oct 2024 01:09:47 GMT  
		Size: 24.1 MB (24053088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f8d5c28c5b58b00ce262bb73a621a7af0b4b09fe89bc22e4df30ef2b6971fd`  
		Last Modified: Thu, 17 Oct 2024 02:58:36 GMT  
		Size: 18.9 MB (18947926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfa986252c82e40ce1fee86c5280aa85b37dab922ffc9bef9aac548dd60d49c`  
		Last Modified: Thu, 17 Oct 2024 02:58:35 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc152baccadedea7cc53100685dbc71611d4c76524e720cb8fcda6266d7ae04`  
		Last Modified: Thu, 17 Oct 2024 02:58:36 GMT  
		Size: 66.3 MB (66285437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a802126f6b225f2c4ebd9216350310e8c015a3656240049acb81b1231e61d29`  
		Last Modified: Thu, 17 Oct 2024 02:58:35 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:f8ead2c0517da1bf91fc238d53925a8cbbe5b3d56c790b30fdde84989a3f560f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6413708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a6179f191a709e8ac92eae29b91d3971f57796682623ffab0bef0ff644c22a`

```dockerfile
```

-	Layers:
	-	`sha256:2dc34580a414327d0c7e4e696cd94d97720ef1ff772807af7874a88a6b2e849e`  
		Last Modified: Thu, 17 Oct 2024 02:58:35 GMT  
		Size: 6.4 MB (6399346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39bbe8612c8eb95108af2790e8c28986a9811ca672d4358f2f33424804ca8419`  
		Last Modified: Thu, 17 Oct 2024 02:58:35 GMT  
		Size: 14.4 KB (14362 bytes)  
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
$ docker pull telegraf@sha256:2f2c21a89ce365592f632a54485356595c4682ec922233bb2f767483dbd563a9
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
$ docker pull telegraf@sha256:3b3abd4176dca9247884528f17685574790ab4fd99b0bc1bb29a9a5efbc9e331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163446937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03348efb2f9d2c24d73f18736357bd4bc474398e4c89bafc9a848c691e1ba9c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.32.1
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5f3b3f727e71a2c8e2d282f958aa488342e7a0edc7c26d994f1dbbb88c88d`  
		Last Modified: Thu, 17 Oct 2024 01:09:47 GMT  
		Size: 24.1 MB (24053088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274f45dbd2303b270389edf8469e71178eac546f608941b5bc390f8414c889fd`  
		Last Modified: Thu, 17 Oct 2024 03:05:53 GMT  
		Size: 18.9 MB (18948094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e5cae3fe8eade46cb0b644340961b2617eb3aea96fce1e19365f6b27c935cc`  
		Last Modified: Thu, 17 Oct 2024 03:05:53 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385cedbd42c81165c28f33c1694685bde47eff35a718bc85a6efcec3ca11cd7a`  
		Last Modified: Thu, 17 Oct 2024 03:05:54 GMT  
		Size: 70.9 MB (70888335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ae196631a8ff9947aa7b9a0669a2f2ae1a84a0b4c0935425ba1c5b1c07d9d6`  
		Last Modified: Thu, 17 Oct 2024 03:05:53 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:a9b32569a210391f0379aea7701fcbd882e5b19c58332adc1ff71cd52510147f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6423724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35aca53424ae89d48ba9494ccdd5119104867ba6107569d43da8e7402bd8a879`

```dockerfile
```

-	Layers:
	-	`sha256:5afae7cc38ab2c8bc8004393911f550158b1c5d3fb4e7b1e33689e532b2e4464`  
		Last Modified: Thu, 17 Oct 2024 03:05:53 GMT  
		Size: 6.4 MB (6409060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b761ae4a40f9498ba4aeb30b5bc93ef2650fc8ac52dbe3aa3f971a2f64dc348`  
		Last Modified: Thu, 17 Oct 2024 03:05:53 GMT  
		Size: 14.7 KB (14664 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:9cbca0cfd64cd1a6144e0a1e252194f8ad2fbd065540e535f6d394af31621e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150492986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3647e6b71f1d9384641a6031b272bbba91953fa3a537daaf825db7bdc4a660f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:34 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Fri, 27 Sep 2024 05:13:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:30:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.32.1
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
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
	-	`sha256:ea021eb4372c3142f230f2f4a6c977cfe739e21df24606b4502bb04a8f16986a`  
		Last Modified: Mon, 07 Oct 2024 22:58:06 GMT  
		Size: 65.7 MB (65660224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cce45fb22c766229d0969fcc373404da1624ab9cce152341e05468145f9f31`  
		Last Modified: Mon, 07 Oct 2024 22:58:04 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:cec6e99f3c9467ab8f78344b676ba9417458031cac1b4c607576c095daa9e761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6419223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ef0b0277f327dba42fcab490c374524ea8b87b96c2bec775e4623be9e45708`

```dockerfile
```

-	Layers:
	-	`sha256:3ae3b56884f6a6ad5a269c8763d0054409564862b12c8e8bc1019c5211ccb041`  
		Last Modified: Mon, 07 Oct 2024 22:58:05 GMT  
		Size: 6.4 MB (6404504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9c300aa23788cd7b61e66e86fab7258485e625aaaa81477b828887c48daf43e`  
		Last Modified: Mon, 07 Oct 2024 22:58:04 GMT  
		Size: 14.7 KB (14719 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:de3002720d690288cfd9c267363e6cea0125d89dc654b209eefcdc6c8a54ca0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155956418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f47c14910d3a2bce369697bc755caf4de74cc54c4cd827a460ba1244365bf5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.32.1
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
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
	-	`sha256:12082b1f66bc73173ffea4689d2e359ce4c59a5717287ad6c70347c93333ddd7`  
		Last Modified: Mon, 07 Oct 2024 22:59:11 GMT  
		Size: 18.9 MB (18870729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbbf742a49eec6df68547fc74dc476b2c43c77f5fc9608dedd2fe4693eff571`  
		Last Modified: Mon, 07 Oct 2024 22:59:10 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9124130d2039ac838ab4f40df83d17a37f7742553fc12be0caa7752d49a049e1`  
		Last Modified: Mon, 07 Oct 2024 22:59:12 GMT  
		Size: 63.9 MB (63904363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdad22eb148f11fd30e8c995d325faf370dffdd3093cdbbea2123831cbc8bcdb`  
		Last Modified: Mon, 07 Oct 2024 22:59:10 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:54c20b7e3c7477637ac860139006e761134b003f1f18761c1bbe35e50c266f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac014f8cf26740177667e55340b1776c8accd1810947182df1e7d226906e1ca0`

```dockerfile
```

-	Layers:
	-	`sha256:bb057f766d5e849f9def1b70beaafec54e13bfaf037b414a52be1e59cb93655a`  
		Last Modified: Mon, 07 Oct 2024 22:59:10 GMT  
		Size: 6.4 MB (6409790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d214d7897de3512e2415be0ed8a39987f0dc4c49252d657277ba31b8cf2ee4b6`  
		Last Modified: Mon, 07 Oct 2024 22:59:10 GMT  
		Size: 14.7 KB (14747 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32-alpine`

```console
$ docker pull telegraf@sha256:ea445ca906fe3838112f715ba22ae2bd4b3196a376bc57605b1f6974c40eb746
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:67fd793729e6554260cd3a2a960e39d9bb60ef81a5f19fb904254efe7b3da457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76755070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6177944eb8a7320fbb91455e6ad406b4ec49e104642c3ec4f05000a7d2eedc87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.32.1
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d65e7a3eeaf684e364810ae9efdd667c7e11c502aaa6b0003b5ba4fd263338`  
		Last Modified: Mon, 07 Oct 2024 22:57:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ca4141e20e3b014ca06a700477b4d7a4a4cd0ed66175af6a40dbaa8029bc4f`  
		Last Modified: Mon, 07 Oct 2024 22:57:53 GMT  
		Size: 2.4 MB (2444827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151894639f1b131c655d70eff374cb45299d6492db60a56b6d817e317dc5cf4f`  
		Last Modified: Mon, 07 Oct 2024 22:57:54 GMT  
		Size: 70.7 MB (70685831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c04e97fa83cb52b1ad239e4ee1d61b58058bf3d8e0c9c10b209d9a88c4407a9`  
		Last Modified: Mon, 07 Oct 2024 22:57:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:035e245bf268d29fa02569921d324ca449c50ebf4c42090ae819866e3a3c42e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4e0805ae239bcf10f2d9188e777b17945d68e96bf48bb8a04062c07a07d006`

```dockerfile
```

-	Layers:
	-	`sha256:c44853d716312a3ec67529e37a4503da3fe831d02d30ada179485cc37507cf23`  
		Last Modified: Mon, 07 Oct 2024 22:57:53 GMT  
		Size: 1.1 MB (1074128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6b69d6f872644b28ca7eb7419f0c0acbf2880556a84b50a93274337376f945`  
		Last Modified: Mon, 07 Oct 2024 22:57:53 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8fe27027e99482d119cc663eefa868da195f525f68233bccf40580a4b7dfdbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70326293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1142994c468336adb9af3255ec7d656e26e4fda2cfad1301fed80b0db226981e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.32.1
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeafef20316ff1ee5e72a732d82fcc3771b00ac02739e7f40d837b55ef5d930f`  
		Last Modified: Mon, 07 Oct 2024 22:59:49 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b311cd7a8d103bf8024568f1367d531dce0f0f38a1a666a4d176c00c1e8d888`  
		Last Modified: Mon, 07 Oct 2024 22:59:50 GMT  
		Size: 2.5 MB (2530621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3899e78eb85fe9ee13d8731160354f9d4f14070d45af427e51155c9d2a6a0a2`  
		Last Modified: Mon, 07 Oct 2024 22:59:51 GMT  
		Size: 63.7 MB (63707421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df1cf1029241c1b3d0b6565615c47c2be59d3a4fbc3235b9a037fe387bf99a2`  
		Last Modified: Mon, 07 Oct 2024 22:59:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:1451ec2fb0edb36168b8c1590ae6087e87713c9b8c7fa3964f418312ad70513e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1084962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f05436b77aaa4677f89ca4e69a3e013c3e1808eecd4386290eb75ca2318977`

```dockerfile
```

-	Layers:
	-	`sha256:a8d30224c926f97d91fa3911173de7cfc7e3b7d22ddf121842d47ae0353f7b6f`  
		Last Modified: Mon, 07 Oct 2024 22:59:50 GMT  
		Size: 1.1 MB (1069805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8bb6f07593e8ecf2315de80bed38cde5508df800621fc1bf7c70ebfb8f224e3`  
		Last Modified: Mon, 07 Oct 2024 22:59:49 GMT  
		Size: 15.2 KB (15157 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32.1`

```console
$ docker pull telegraf@sha256:2f2c21a89ce365592f632a54485356595c4682ec922233bb2f767483dbd563a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32.1` - linux; amd64

```console
$ docker pull telegraf@sha256:3b3abd4176dca9247884528f17685574790ab4fd99b0bc1bb29a9a5efbc9e331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163446937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03348efb2f9d2c24d73f18736357bd4bc474398e4c89bafc9a848c691e1ba9c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.32.1
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5f3b3f727e71a2c8e2d282f958aa488342e7a0edc7c26d994f1dbbb88c88d`  
		Last Modified: Thu, 17 Oct 2024 01:09:47 GMT  
		Size: 24.1 MB (24053088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274f45dbd2303b270389edf8469e71178eac546f608941b5bc390f8414c889fd`  
		Last Modified: Thu, 17 Oct 2024 03:05:53 GMT  
		Size: 18.9 MB (18948094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e5cae3fe8eade46cb0b644340961b2617eb3aea96fce1e19365f6b27c935cc`  
		Last Modified: Thu, 17 Oct 2024 03:05:53 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385cedbd42c81165c28f33c1694685bde47eff35a718bc85a6efcec3ca11cd7a`  
		Last Modified: Thu, 17 Oct 2024 03:05:54 GMT  
		Size: 70.9 MB (70888335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ae196631a8ff9947aa7b9a0669a2f2ae1a84a0b4c0935425ba1c5b1c07d9d6`  
		Last Modified: Thu, 17 Oct 2024 03:05:53 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:a9b32569a210391f0379aea7701fcbd882e5b19c58332adc1ff71cd52510147f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6423724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35aca53424ae89d48ba9494ccdd5119104867ba6107569d43da8e7402bd8a879`

```dockerfile
```

-	Layers:
	-	`sha256:5afae7cc38ab2c8bc8004393911f550158b1c5d3fb4e7b1e33689e532b2e4464`  
		Last Modified: Thu, 17 Oct 2024 03:05:53 GMT  
		Size: 6.4 MB (6409060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b761ae4a40f9498ba4aeb30b5bc93ef2650fc8ac52dbe3aa3f971a2f64dc348`  
		Last Modified: Thu, 17 Oct 2024 03:05:53 GMT  
		Size: 14.7 KB (14664 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.1` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:9cbca0cfd64cd1a6144e0a1e252194f8ad2fbd065540e535f6d394af31621e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150492986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3647e6b71f1d9384641a6031b272bbba91953fa3a537daaf825db7bdc4a660f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:34 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Fri, 27 Sep 2024 05:13:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:30:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.32.1
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
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
	-	`sha256:ea021eb4372c3142f230f2f4a6c977cfe739e21df24606b4502bb04a8f16986a`  
		Last Modified: Mon, 07 Oct 2024 22:58:06 GMT  
		Size: 65.7 MB (65660224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cce45fb22c766229d0969fcc373404da1624ab9cce152341e05468145f9f31`  
		Last Modified: Mon, 07 Oct 2024 22:58:04 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:cec6e99f3c9467ab8f78344b676ba9417458031cac1b4c607576c095daa9e761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6419223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ef0b0277f327dba42fcab490c374524ea8b87b96c2bec775e4623be9e45708`

```dockerfile
```

-	Layers:
	-	`sha256:3ae3b56884f6a6ad5a269c8763d0054409564862b12c8e8bc1019c5211ccb041`  
		Last Modified: Mon, 07 Oct 2024 22:58:05 GMT  
		Size: 6.4 MB (6404504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9c300aa23788cd7b61e66e86fab7258485e625aaaa81477b828887c48daf43e`  
		Last Modified: Mon, 07 Oct 2024 22:58:04 GMT  
		Size: 14.7 KB (14719 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.1` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:de3002720d690288cfd9c267363e6cea0125d89dc654b209eefcdc6c8a54ca0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155956418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f47c14910d3a2bce369697bc755caf4de74cc54c4cd827a460ba1244365bf5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.32.1
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
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
	-	`sha256:12082b1f66bc73173ffea4689d2e359ce4c59a5717287ad6c70347c93333ddd7`  
		Last Modified: Mon, 07 Oct 2024 22:59:11 GMT  
		Size: 18.9 MB (18870729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbbf742a49eec6df68547fc74dc476b2c43c77f5fc9608dedd2fe4693eff571`  
		Last Modified: Mon, 07 Oct 2024 22:59:10 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9124130d2039ac838ab4f40df83d17a37f7742553fc12be0caa7752d49a049e1`  
		Last Modified: Mon, 07 Oct 2024 22:59:12 GMT  
		Size: 63.9 MB (63904363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdad22eb148f11fd30e8c995d325faf370dffdd3093cdbbea2123831cbc8bcdb`  
		Last Modified: Mon, 07 Oct 2024 22:59:10 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:54c20b7e3c7477637ac860139006e761134b003f1f18761c1bbe35e50c266f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac014f8cf26740177667e55340b1776c8accd1810947182df1e7d226906e1ca0`

```dockerfile
```

-	Layers:
	-	`sha256:bb057f766d5e849f9def1b70beaafec54e13bfaf037b414a52be1e59cb93655a`  
		Last Modified: Mon, 07 Oct 2024 22:59:10 GMT  
		Size: 6.4 MB (6409790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d214d7897de3512e2415be0ed8a39987f0dc4c49252d657277ba31b8cf2ee4b6`  
		Last Modified: Mon, 07 Oct 2024 22:59:10 GMT  
		Size: 14.7 KB (14747 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32.1-alpine`

```console
$ docker pull telegraf@sha256:ea445ca906fe3838112f715ba22ae2bd4b3196a376bc57605b1f6974c40eb746
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32.1-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:67fd793729e6554260cd3a2a960e39d9bb60ef81a5f19fb904254efe7b3da457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76755070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6177944eb8a7320fbb91455e6ad406b4ec49e104642c3ec4f05000a7d2eedc87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.32.1
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d65e7a3eeaf684e364810ae9efdd667c7e11c502aaa6b0003b5ba4fd263338`  
		Last Modified: Mon, 07 Oct 2024 22:57:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ca4141e20e3b014ca06a700477b4d7a4a4cd0ed66175af6a40dbaa8029bc4f`  
		Last Modified: Mon, 07 Oct 2024 22:57:53 GMT  
		Size: 2.4 MB (2444827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151894639f1b131c655d70eff374cb45299d6492db60a56b6d817e317dc5cf4f`  
		Last Modified: Mon, 07 Oct 2024 22:57:54 GMT  
		Size: 70.7 MB (70685831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c04e97fa83cb52b1ad239e4ee1d61b58058bf3d8e0c9c10b209d9a88c4407a9`  
		Last Modified: Mon, 07 Oct 2024 22:57:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.1-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:035e245bf268d29fa02569921d324ca449c50ebf4c42090ae819866e3a3c42e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4e0805ae239bcf10f2d9188e777b17945d68e96bf48bb8a04062c07a07d006`

```dockerfile
```

-	Layers:
	-	`sha256:c44853d716312a3ec67529e37a4503da3fe831d02d30ada179485cc37507cf23`  
		Last Modified: Mon, 07 Oct 2024 22:57:53 GMT  
		Size: 1.1 MB (1074128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6b69d6f872644b28ca7eb7419f0c0acbf2880556a84b50a93274337376f945`  
		Last Modified: Mon, 07 Oct 2024 22:57:53 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.1-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8fe27027e99482d119cc663eefa868da195f525f68233bccf40580a4b7dfdbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70326293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1142994c468336adb9af3255ec7d656e26e4fda2cfad1301fed80b0db226981e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.32.1
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeafef20316ff1ee5e72a732d82fcc3771b00ac02739e7f40d837b55ef5d930f`  
		Last Modified: Mon, 07 Oct 2024 22:59:49 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b311cd7a8d103bf8024568f1367d531dce0f0f38a1a666a4d176c00c1e8d888`  
		Last Modified: Mon, 07 Oct 2024 22:59:50 GMT  
		Size: 2.5 MB (2530621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3899e78eb85fe9ee13d8731160354f9d4f14070d45af427e51155c9d2a6a0a2`  
		Last Modified: Mon, 07 Oct 2024 22:59:51 GMT  
		Size: 63.7 MB (63707421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df1cf1029241c1b3d0b6565615c47c2be59d3a4fbc3235b9a037fe387bf99a2`  
		Last Modified: Mon, 07 Oct 2024 22:59:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.1-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:1451ec2fb0edb36168b8c1590ae6087e87713c9b8c7fa3964f418312ad70513e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1084962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f05436b77aaa4677f89ca4e69a3e013c3e1808eecd4386290eb75ca2318977`

```dockerfile
```

-	Layers:
	-	`sha256:a8d30224c926f97d91fa3911173de7cfc7e3b7d22ddf121842d47ae0353f7b6f`  
		Last Modified: Mon, 07 Oct 2024 22:59:50 GMT  
		Size: 1.1 MB (1069805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8bb6f07593e8ecf2315de80bed38cde5508df800621fc1bf7c70ebfb8f224e3`  
		Last Modified: Mon, 07 Oct 2024 22:59:49 GMT  
		Size: 15.2 KB (15157 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:ea445ca906fe3838112f715ba22ae2bd4b3196a376bc57605b1f6974c40eb746
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:67fd793729e6554260cd3a2a960e39d9bb60ef81a5f19fb904254efe7b3da457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76755070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6177944eb8a7320fbb91455e6ad406b4ec49e104642c3ec4f05000a7d2eedc87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.32.1
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d65e7a3eeaf684e364810ae9efdd667c7e11c502aaa6b0003b5ba4fd263338`  
		Last Modified: Mon, 07 Oct 2024 22:57:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ca4141e20e3b014ca06a700477b4d7a4a4cd0ed66175af6a40dbaa8029bc4f`  
		Last Modified: Mon, 07 Oct 2024 22:57:53 GMT  
		Size: 2.4 MB (2444827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151894639f1b131c655d70eff374cb45299d6492db60a56b6d817e317dc5cf4f`  
		Last Modified: Mon, 07 Oct 2024 22:57:54 GMT  
		Size: 70.7 MB (70685831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c04e97fa83cb52b1ad239e4ee1d61b58058bf3d8e0c9c10b209d9a88c4407a9`  
		Last Modified: Mon, 07 Oct 2024 22:57:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:035e245bf268d29fa02569921d324ca449c50ebf4c42090ae819866e3a3c42e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4e0805ae239bcf10f2d9188e777b17945d68e96bf48bb8a04062c07a07d006`

```dockerfile
```

-	Layers:
	-	`sha256:c44853d716312a3ec67529e37a4503da3fe831d02d30ada179485cc37507cf23`  
		Last Modified: Mon, 07 Oct 2024 22:57:53 GMT  
		Size: 1.1 MB (1074128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6b69d6f872644b28ca7eb7419f0c0acbf2880556a84b50a93274337376f945`  
		Last Modified: Mon, 07 Oct 2024 22:57:53 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8fe27027e99482d119cc663eefa868da195f525f68233bccf40580a4b7dfdbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70326293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1142994c468336adb9af3255ec7d656e26e4fda2cfad1301fed80b0db226981e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.32.1
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeafef20316ff1ee5e72a732d82fcc3771b00ac02739e7f40d837b55ef5d930f`  
		Last Modified: Mon, 07 Oct 2024 22:59:49 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b311cd7a8d103bf8024568f1367d531dce0f0f38a1a666a4d176c00c1e8d888`  
		Last Modified: Mon, 07 Oct 2024 22:59:50 GMT  
		Size: 2.5 MB (2530621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3899e78eb85fe9ee13d8731160354f9d4f14070d45af427e51155c9d2a6a0a2`  
		Last Modified: Mon, 07 Oct 2024 22:59:51 GMT  
		Size: 63.7 MB (63707421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df1cf1029241c1b3d0b6565615c47c2be59d3a4fbc3235b9a037fe387bf99a2`  
		Last Modified: Mon, 07 Oct 2024 22:59:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:1451ec2fb0edb36168b8c1590ae6087e87713c9b8c7fa3964f418312ad70513e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1084962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f05436b77aaa4677f89ca4e69a3e013c3e1808eecd4386290eb75ca2318977`

```dockerfile
```

-	Layers:
	-	`sha256:a8d30224c926f97d91fa3911173de7cfc7e3b7d22ddf121842d47ae0353f7b6f`  
		Last Modified: Mon, 07 Oct 2024 22:59:50 GMT  
		Size: 1.1 MB (1069805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8bb6f07593e8ecf2315de80bed38cde5508df800621fc1bf7c70ebfb8f224e3`  
		Last Modified: Mon, 07 Oct 2024 22:59:49 GMT  
		Size: 15.2 KB (15157 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:2f2c21a89ce365592f632a54485356595c4682ec922233bb2f767483dbd563a9
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
$ docker pull telegraf@sha256:3b3abd4176dca9247884528f17685574790ab4fd99b0bc1bb29a9a5efbc9e331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163446937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03348efb2f9d2c24d73f18736357bd4bc474398e4c89bafc9a848c691e1ba9c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.32.1
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5f3b3f727e71a2c8e2d282f958aa488342e7a0edc7c26d994f1dbbb88c88d`  
		Last Modified: Thu, 17 Oct 2024 01:09:47 GMT  
		Size: 24.1 MB (24053088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274f45dbd2303b270389edf8469e71178eac546f608941b5bc390f8414c889fd`  
		Last Modified: Thu, 17 Oct 2024 03:05:53 GMT  
		Size: 18.9 MB (18948094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e5cae3fe8eade46cb0b644340961b2617eb3aea96fce1e19365f6b27c935cc`  
		Last Modified: Thu, 17 Oct 2024 03:05:53 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385cedbd42c81165c28f33c1694685bde47eff35a718bc85a6efcec3ca11cd7a`  
		Last Modified: Thu, 17 Oct 2024 03:05:54 GMT  
		Size: 70.9 MB (70888335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ae196631a8ff9947aa7b9a0669a2f2ae1a84a0b4c0935425ba1c5b1c07d9d6`  
		Last Modified: Thu, 17 Oct 2024 03:05:53 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:a9b32569a210391f0379aea7701fcbd882e5b19c58332adc1ff71cd52510147f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6423724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35aca53424ae89d48ba9494ccdd5119104867ba6107569d43da8e7402bd8a879`

```dockerfile
```

-	Layers:
	-	`sha256:5afae7cc38ab2c8bc8004393911f550158b1c5d3fb4e7b1e33689e532b2e4464`  
		Last Modified: Thu, 17 Oct 2024 03:05:53 GMT  
		Size: 6.4 MB (6409060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b761ae4a40f9498ba4aeb30b5bc93ef2650fc8ac52dbe3aa3f971a2f64dc348`  
		Last Modified: Thu, 17 Oct 2024 03:05:53 GMT  
		Size: 14.7 KB (14664 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:9cbca0cfd64cd1a6144e0a1e252194f8ad2fbd065540e535f6d394af31621e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150492986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3647e6b71f1d9384641a6031b272bbba91953fa3a537daaf825db7bdc4a660f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:34 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Fri, 27 Sep 2024 05:13:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:30:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.32.1
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
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
	-	`sha256:ea021eb4372c3142f230f2f4a6c977cfe739e21df24606b4502bb04a8f16986a`  
		Last Modified: Mon, 07 Oct 2024 22:58:06 GMT  
		Size: 65.7 MB (65660224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cce45fb22c766229d0969fcc373404da1624ab9cce152341e05468145f9f31`  
		Last Modified: Mon, 07 Oct 2024 22:58:04 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:cec6e99f3c9467ab8f78344b676ba9417458031cac1b4c607576c095daa9e761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6419223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ef0b0277f327dba42fcab490c374524ea8b87b96c2bec775e4623be9e45708`

```dockerfile
```

-	Layers:
	-	`sha256:3ae3b56884f6a6ad5a269c8763d0054409564862b12c8e8bc1019c5211ccb041`  
		Last Modified: Mon, 07 Oct 2024 22:58:05 GMT  
		Size: 6.4 MB (6404504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9c300aa23788cd7b61e66e86fab7258485e625aaaa81477b828887c48daf43e`  
		Last Modified: Mon, 07 Oct 2024 22:58:04 GMT  
		Size: 14.7 KB (14719 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:de3002720d690288cfd9c267363e6cea0125d89dc654b209eefcdc6c8a54ca0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155956418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f47c14910d3a2bce369697bc755caf4de74cc54c4cd827a460ba1244365bf5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.32.1
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
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
	-	`sha256:12082b1f66bc73173ffea4689d2e359ce4c59a5717287ad6c70347c93333ddd7`  
		Last Modified: Mon, 07 Oct 2024 22:59:11 GMT  
		Size: 18.9 MB (18870729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbbf742a49eec6df68547fc74dc476b2c43c77f5fc9608dedd2fe4693eff571`  
		Last Modified: Mon, 07 Oct 2024 22:59:10 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9124130d2039ac838ab4f40df83d17a37f7742553fc12be0caa7752d49a049e1`  
		Last Modified: Mon, 07 Oct 2024 22:59:12 GMT  
		Size: 63.9 MB (63904363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdad22eb148f11fd30e8c995d325faf370dffdd3093cdbbea2123831cbc8bcdb`  
		Last Modified: Mon, 07 Oct 2024 22:59:10 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:54c20b7e3c7477637ac860139006e761134b003f1f18761c1bbe35e50c266f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac014f8cf26740177667e55340b1776c8accd1810947182df1e7d226906e1ca0`

```dockerfile
```

-	Layers:
	-	`sha256:bb057f766d5e849f9def1b70beaafec54e13bfaf037b414a52be1e59cb93655a`  
		Last Modified: Mon, 07 Oct 2024 22:59:10 GMT  
		Size: 6.4 MB (6409790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d214d7897de3512e2415be0ed8a39987f0dc4c49252d657277ba31b8cf2ee4b6`  
		Last Modified: Mon, 07 Oct 2024 22:59:10 GMT  
		Size: 14.7 KB (14747 bytes)  
		MIME: application/vnd.in-toto+json
