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
$ docker pull telegraf@sha256:c375eca95614fc37c5d5050e819ea0c25c783aa4c83711641705a86fda5465cc
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
$ docker pull telegraf@sha256:bf977925a84b7f98e4605d7d599606749eed32a91e9777e0690ef98487f6d7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155323242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0fb2e62534794b1bc57a4be101160e890f727edc597d1c9cea62ebbd2c6f26`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fd9ab95a299e2f6f7c355e9ee17457e44471949a3c32aea882ca04a8d7b3ea`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 18.9 MB (18947976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3290d3b71335295bbd0e92288cf85962dec0957fbf167ab8f7a2d5d494fb6e1f`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36defb8c859d8098307fb48dbb6a7f396a7c33414f9dfdda89126070ac15302`  
		Last Modified: Sat, 19 Oct 2024 02:07:42 GMT  
		Size: 62.8 MB (62766451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a68fa7e05f054136250d49c9966f9f5e643f5efc426fc8d04224f09ae5466d4`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:4e21cfca365eff6873070e1f4e975e6857641ae977191ddaefaa009c6a1c9767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18e2f2e15802d2dd8516e03942b710c1e43389174f6bd73c4a939a9ed3586fc`

```dockerfile
```

-	Layers:
	-	`sha256:0fd5ba346e15e3749f49cd9a066a2831f4d16817e58ee9f3bcc801a978c2fc6f`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 6.4 MB (6410311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f2f6ba96f8953e02b838e700f0b72baf59f4da6ad83b36835a884adf886b91`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:705311a50f9a30761a788f1546fdea1ddf58c41b17c16a8f8ac4408c5e7d4666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143045274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c883043f628c3162ccb04570dfdc61869fe7a4df8e0667d990c0908fdb37b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3332329de6b42a2c5f534a6f40381b05e4356eb62a42408f66b4d98e78cfee55`  
		Last Modified: Thu, 17 Oct 2024 03:36:59 GMT  
		Size: 22.0 MB (21957453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d145c46c1134675dd81d7f150a5956cd0534991b8712626affe84fdbc492d4e0`  
		Last Modified: Fri, 18 Oct 2024 02:16:51 GMT  
		Size: 17.7 MB (17724833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007f1d0a3dbb40db976a12849fd9dd9414e474b07b7a6ba8f34d999f06745782`  
		Last Modified: Fri, 18 Oct 2024 02:16:50 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27919f4eff19206d2867eb152d80675e1e96f96298430bbac8a606bbc6ccdf7f`  
		Last Modified: Fri, 18 Oct 2024 02:16:52 GMT  
		Size: 58.2 MB (58212642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96db75dfa54496515b7df7b37c3215fd68d87a44726399a492d427901b511c63`  
		Last Modified: Fri, 18 Oct 2024 02:16:50 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:8c0b387eda5bc20ac2815fc31bef948f24441299f33aef64f094ab1eebb159a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b054b2002254dad0809f0702822dc6cfaa128eba9ad4fe393955b181515e11`

```dockerfile
```

-	Layers:
	-	`sha256:a8bfb4e5dd41498e7d11822037111c9d20229f8530d6369d9a02538c01e6c9cf`  
		Last Modified: Fri, 18 Oct 2024 02:16:50 GMT  
		Size: 6.4 MB (6385777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b836c5cfaa5b87ba9cee01ec841b4a587409fd23dc1fb43292a2840b917e7cf`  
		Last Modified: Fri, 18 Oct 2024 02:16:49 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:62ba62ae11f26d2d714c53940bed354b47de3ed8e5d02d0647bb5c25c4a01957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149175467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fa4029b45082072f7344dd405682ebaabb4eff7fe739bbd2ad37c9b8298c87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437f71cf1903685ed3f6314161e121602758f809a760d2bd2293f7cd8ce1abe1`  
		Last Modified: Thu, 17 Oct 2024 04:36:08 GMT  
		Size: 23.6 MB (23594190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882a729e136449584637961d6c36466fd4de00cf1bd3c42a5b0ef2cc649a9935`  
		Last Modified: Thu, 17 Oct 2024 21:22:22 GMT  
		Size: 18.9 MB (18870637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc475b03394d09612cdb1d4d2c146bff32385599b122b5d5385fd6e1011322c`  
		Last Modified: Thu, 17 Oct 2024 21:22:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5507db310b3573c32a560401aea0a1d31d7b60f03e62c20b54c4f4b678f3f581`  
		Last Modified: Thu, 17 Oct 2024 21:22:23 GMT  
		Size: 57.1 MB (57123266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0219f174243de39061a288d3cfe721e3858e2f83d0cae165039788d355c5920`  
		Last Modified: Thu, 17 Oct 2024 21:22:21 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:d9dc46fff01ffb4b067646c77f9e6f1fb3b3a8f97d7605191caa6cbdb712eebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe4ed75850cb42d30dad78165f845052190d86f601609887300cf0e8036f5a7`

```dockerfile
```

-	Layers:
	-	`sha256:945507f71d2173dbd05cfe57723b05a99bc461c3fc87341e79fa7ba2960093b4`  
		Last Modified: Thu, 17 Oct 2024 21:22:21 GMT  
		Size: 6.4 MB (6391061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63cb1b298a12bc59b2606dcd5a8590e7d473500e3783415d0d92ac7505338970`  
		Last Modified: Thu, 17 Oct 2024 21:22:21 GMT  
		Size: 14.5 KB (14466 bytes)  
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
$ docker pull telegraf@sha256:c375eca95614fc37c5d5050e819ea0c25c783aa4c83711641705a86fda5465cc
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
$ docker pull telegraf@sha256:bf977925a84b7f98e4605d7d599606749eed32a91e9777e0690ef98487f6d7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155323242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0fb2e62534794b1bc57a4be101160e890f727edc597d1c9cea62ebbd2c6f26`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fd9ab95a299e2f6f7c355e9ee17457e44471949a3c32aea882ca04a8d7b3ea`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 18.9 MB (18947976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3290d3b71335295bbd0e92288cf85962dec0957fbf167ab8f7a2d5d494fb6e1f`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36defb8c859d8098307fb48dbb6a7f396a7c33414f9dfdda89126070ac15302`  
		Last Modified: Sat, 19 Oct 2024 02:07:42 GMT  
		Size: 62.8 MB (62766451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a68fa7e05f054136250d49c9966f9f5e643f5efc426fc8d04224f09ae5466d4`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:4e21cfca365eff6873070e1f4e975e6857641ae977191ddaefaa009c6a1c9767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18e2f2e15802d2dd8516e03942b710c1e43389174f6bd73c4a939a9ed3586fc`

```dockerfile
```

-	Layers:
	-	`sha256:0fd5ba346e15e3749f49cd9a066a2831f4d16817e58ee9f3bcc801a978c2fc6f`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 6.4 MB (6410311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f2f6ba96f8953e02b838e700f0b72baf59f4da6ad83b36835a884adf886b91`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:705311a50f9a30761a788f1546fdea1ddf58c41b17c16a8f8ac4408c5e7d4666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143045274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c883043f628c3162ccb04570dfdc61869fe7a4df8e0667d990c0908fdb37b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3332329de6b42a2c5f534a6f40381b05e4356eb62a42408f66b4d98e78cfee55`  
		Last Modified: Thu, 17 Oct 2024 03:36:59 GMT  
		Size: 22.0 MB (21957453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d145c46c1134675dd81d7f150a5956cd0534991b8712626affe84fdbc492d4e0`  
		Last Modified: Fri, 18 Oct 2024 02:16:51 GMT  
		Size: 17.7 MB (17724833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007f1d0a3dbb40db976a12849fd9dd9414e474b07b7a6ba8f34d999f06745782`  
		Last Modified: Fri, 18 Oct 2024 02:16:50 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27919f4eff19206d2867eb152d80675e1e96f96298430bbac8a606bbc6ccdf7f`  
		Last Modified: Fri, 18 Oct 2024 02:16:52 GMT  
		Size: 58.2 MB (58212642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96db75dfa54496515b7df7b37c3215fd68d87a44726399a492d427901b511c63`  
		Last Modified: Fri, 18 Oct 2024 02:16:50 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:8c0b387eda5bc20ac2815fc31bef948f24441299f33aef64f094ab1eebb159a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b054b2002254dad0809f0702822dc6cfaa128eba9ad4fe393955b181515e11`

```dockerfile
```

-	Layers:
	-	`sha256:a8bfb4e5dd41498e7d11822037111c9d20229f8530d6369d9a02538c01e6c9cf`  
		Last Modified: Fri, 18 Oct 2024 02:16:50 GMT  
		Size: 6.4 MB (6385777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b836c5cfaa5b87ba9cee01ec841b4a587409fd23dc1fb43292a2840b917e7cf`  
		Last Modified: Fri, 18 Oct 2024 02:16:49 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:62ba62ae11f26d2d714c53940bed354b47de3ed8e5d02d0647bb5c25c4a01957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149175467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fa4029b45082072f7344dd405682ebaabb4eff7fe739bbd2ad37c9b8298c87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437f71cf1903685ed3f6314161e121602758f809a760d2bd2293f7cd8ce1abe1`  
		Last Modified: Thu, 17 Oct 2024 04:36:08 GMT  
		Size: 23.6 MB (23594190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882a729e136449584637961d6c36466fd4de00cf1bd3c42a5b0ef2cc649a9935`  
		Last Modified: Thu, 17 Oct 2024 21:22:22 GMT  
		Size: 18.9 MB (18870637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc475b03394d09612cdb1d4d2c146bff32385599b122b5d5385fd6e1011322c`  
		Last Modified: Thu, 17 Oct 2024 21:22:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5507db310b3573c32a560401aea0a1d31d7b60f03e62c20b54c4f4b678f3f581`  
		Last Modified: Thu, 17 Oct 2024 21:22:23 GMT  
		Size: 57.1 MB (57123266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0219f174243de39061a288d3cfe721e3858e2f83d0cae165039788d355c5920`  
		Last Modified: Thu, 17 Oct 2024 21:22:21 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:d9dc46fff01ffb4b067646c77f9e6f1fb3b3a8f97d7605191caa6cbdb712eebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe4ed75850cb42d30dad78165f845052190d86f601609887300cf0e8036f5a7`

```dockerfile
```

-	Layers:
	-	`sha256:945507f71d2173dbd05cfe57723b05a99bc461c3fc87341e79fa7ba2960093b4`  
		Last Modified: Thu, 17 Oct 2024 21:22:21 GMT  
		Size: 6.4 MB (6391061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63cb1b298a12bc59b2606dcd5a8590e7d473500e3783415d0d92ac7505338970`  
		Last Modified: Thu, 17 Oct 2024 21:22:21 GMT  
		Size: 14.5 KB (14466 bytes)  
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
$ docker pull telegraf@sha256:ec649c45291b191b5adf2184cc220a959d717c543370f449f093f5b90ac873f6
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
$ docker pull telegraf@sha256:83e53ecd97b65f6d8d4f18013f7000b993f6a0cd72492342d658c30d0ac4c763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158842106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e271e3d0e6b30c363c253c7680f01d2c0ead77152a66b2514710977131d65bf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ab873cbb491a49b8a4a75e07ea55fc23d3399c631f175ce13170bc0ee349cf`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 18.9 MB (18947890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f902ac067d13046b5a1541aeb1fae200f0d8b60c236960a64b99b20cfca2be`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70413417887d0b875839282ba16b10d808cae57fc4bf880728bcda06fdd53cac`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 66.3 MB (66285412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14834176ab6052f8fd60a46aaf605bc092c99494e7cdeeba40d4930102e24dd4`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:32fde434eb50e158d51e2b541da2833042ba40900f6a41a06cdff8556bf86962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6432989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458ff9078bdb486654da434e6542cb71eba308c1e462a93b120b8f4f047756a7`

```dockerfile
```

-	Layers:
	-	`sha256:f915b8af518bdb66afa47c4bac0c041f9dd9397a1a50a9258a8949ee171e2185`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 6.4 MB (6418519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41146add8dc1189982c7e6e1ca74e3e28c2fa7f385822647db3c44f67df63893`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:703fb5bec942103f5ceb627d75ab07bf2c92fbafef1b40add7fb012bad1a3d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146504904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99abbad10b1dec621d16a28d5966da03ea048f86902d056fb77f1ea3675301fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3332329de6b42a2c5f534a6f40381b05e4356eb62a42408f66b4d98e78cfee55`  
		Last Modified: Thu, 17 Oct 2024 03:36:59 GMT  
		Size: 22.0 MB (21957453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d145c46c1134675dd81d7f150a5956cd0534991b8712626affe84fdbc492d4e0`  
		Last Modified: Fri, 18 Oct 2024 02:16:51 GMT  
		Size: 17.7 MB (17724833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007f1d0a3dbb40db976a12849fd9dd9414e474b07b7a6ba8f34d999f06745782`  
		Last Modified: Fri, 18 Oct 2024 02:16:50 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5606f144389f4b98272b9d0f5d075dfb0ca307c0dcd8a50379244cc1549166`  
		Last Modified: Fri, 18 Oct 2024 02:17:45 GMT  
		Size: 61.7 MB (61672273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d833bda4e771a6f12b2fd9251f0551507f0038f0a1cf1ee55d27206200f97c38`  
		Last Modified: Fri, 18 Oct 2024 02:17:43 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:bab8fa9ecb5d05faff6d106089af7d2703b736409f4f5d678c971985a48b3d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6409224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe8812e147716497a69e6531c84f64808885372048ad82707b2a1ec8adfea26`

```dockerfile
```

-	Layers:
	-	`sha256:1afc6997d0f9aca070d8730b3bef2ec07a48d3bf1e8052b34b4812e076d1201f`  
		Last Modified: Fri, 18 Oct 2024 02:17:43 GMT  
		Size: 6.4 MB (6394782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3ea2ede4c09ce92b36a5cc7efc75060c64ae9bce5bc01133e02e3dea678702`  
		Last Modified: Fri, 18 Oct 2024 02:17:43 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3a505958ebfbe16acba754c7ecca858e132944b8cae510b40d890b14557c5830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152429950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9179f612b110f399de7e6efa3001c6a300488260bf008f5de420f4cb67061215`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437f71cf1903685ed3f6314161e121602758f809a760d2bd2293f7cd8ce1abe1`  
		Last Modified: Thu, 17 Oct 2024 04:36:08 GMT  
		Size: 23.6 MB (23594190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882a729e136449584637961d6c36466fd4de00cf1bd3c42a5b0ef2cc649a9935`  
		Last Modified: Thu, 17 Oct 2024 21:22:22 GMT  
		Size: 18.9 MB (18870637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc475b03394d09612cdb1d4d2c146bff32385599b122b5d5385fd6e1011322c`  
		Last Modified: Thu, 17 Oct 2024 21:22:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43366acbc4b86d5842bff2615154aabc76b1dc82b70514b5c0f9fdbdbc4ae06f`  
		Last Modified: Thu, 17 Oct 2024 21:23:09 GMT  
		Size: 60.4 MB (60377749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a731e0806c3298b24ceab255f09ff2e3417b69e0db0d06b2cde4373d75a48d31`  
		Last Modified: Thu, 17 Oct 2024 21:23:07 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:8f1136f07bdb2dd09104677c02d056c403168a60a6d66614e0f219e21c080a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6415327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969483432fc409414014878a2369f2c7eef07fd3dd664b0e6dead0dc6d875704`

```dockerfile
```

-	Layers:
	-	`sha256:d044b823dd4a6b4af1fe428baaf026436636a7122c95611af58b9a4ee3dfbec7`  
		Last Modified: Thu, 17 Oct 2024 21:23:07 GMT  
		Size: 6.4 MB (6400861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ec7d0e401101c9001c1ade77d9396a4b9c8859b73e70a0d3768a2b107987dee`  
		Last Modified: Thu, 17 Oct 2024 21:23:07 GMT  
		Size: 14.5 KB (14466 bytes)  
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
$ docker pull telegraf@sha256:ec649c45291b191b5adf2184cc220a959d717c543370f449f093f5b90ac873f6
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
$ docker pull telegraf@sha256:83e53ecd97b65f6d8d4f18013f7000b993f6a0cd72492342d658c30d0ac4c763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158842106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e271e3d0e6b30c363c253c7680f01d2c0ead77152a66b2514710977131d65bf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ab873cbb491a49b8a4a75e07ea55fc23d3399c631f175ce13170bc0ee349cf`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 18.9 MB (18947890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f902ac067d13046b5a1541aeb1fae200f0d8b60c236960a64b99b20cfca2be`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70413417887d0b875839282ba16b10d808cae57fc4bf880728bcda06fdd53cac`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 66.3 MB (66285412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14834176ab6052f8fd60a46aaf605bc092c99494e7cdeeba40d4930102e24dd4`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:32fde434eb50e158d51e2b541da2833042ba40900f6a41a06cdff8556bf86962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6432989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458ff9078bdb486654da434e6542cb71eba308c1e462a93b120b8f4f047756a7`

```dockerfile
```

-	Layers:
	-	`sha256:f915b8af518bdb66afa47c4bac0c041f9dd9397a1a50a9258a8949ee171e2185`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 6.4 MB (6418519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41146add8dc1189982c7e6e1ca74e3e28c2fa7f385822647db3c44f67df63893`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:703fb5bec942103f5ceb627d75ab07bf2c92fbafef1b40add7fb012bad1a3d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146504904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99abbad10b1dec621d16a28d5966da03ea048f86902d056fb77f1ea3675301fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3332329de6b42a2c5f534a6f40381b05e4356eb62a42408f66b4d98e78cfee55`  
		Last Modified: Thu, 17 Oct 2024 03:36:59 GMT  
		Size: 22.0 MB (21957453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d145c46c1134675dd81d7f150a5956cd0534991b8712626affe84fdbc492d4e0`  
		Last Modified: Fri, 18 Oct 2024 02:16:51 GMT  
		Size: 17.7 MB (17724833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007f1d0a3dbb40db976a12849fd9dd9414e474b07b7a6ba8f34d999f06745782`  
		Last Modified: Fri, 18 Oct 2024 02:16:50 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5606f144389f4b98272b9d0f5d075dfb0ca307c0dcd8a50379244cc1549166`  
		Last Modified: Fri, 18 Oct 2024 02:17:45 GMT  
		Size: 61.7 MB (61672273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d833bda4e771a6f12b2fd9251f0551507f0038f0a1cf1ee55d27206200f97c38`  
		Last Modified: Fri, 18 Oct 2024 02:17:43 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:bab8fa9ecb5d05faff6d106089af7d2703b736409f4f5d678c971985a48b3d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6409224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe8812e147716497a69e6531c84f64808885372048ad82707b2a1ec8adfea26`

```dockerfile
```

-	Layers:
	-	`sha256:1afc6997d0f9aca070d8730b3bef2ec07a48d3bf1e8052b34b4812e076d1201f`  
		Last Modified: Fri, 18 Oct 2024 02:17:43 GMT  
		Size: 6.4 MB (6394782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3ea2ede4c09ce92b36a5cc7efc75060c64ae9bce5bc01133e02e3dea678702`  
		Last Modified: Fri, 18 Oct 2024 02:17:43 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3a505958ebfbe16acba754c7ecca858e132944b8cae510b40d890b14557c5830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152429950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9179f612b110f399de7e6efa3001c6a300488260bf008f5de420f4cb67061215`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437f71cf1903685ed3f6314161e121602758f809a760d2bd2293f7cd8ce1abe1`  
		Last Modified: Thu, 17 Oct 2024 04:36:08 GMT  
		Size: 23.6 MB (23594190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882a729e136449584637961d6c36466fd4de00cf1bd3c42a5b0ef2cc649a9935`  
		Last Modified: Thu, 17 Oct 2024 21:22:22 GMT  
		Size: 18.9 MB (18870637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc475b03394d09612cdb1d4d2c146bff32385599b122b5d5385fd6e1011322c`  
		Last Modified: Thu, 17 Oct 2024 21:22:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43366acbc4b86d5842bff2615154aabc76b1dc82b70514b5c0f9fdbdbc4ae06f`  
		Last Modified: Thu, 17 Oct 2024 21:23:09 GMT  
		Size: 60.4 MB (60377749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a731e0806c3298b24ceab255f09ff2e3417b69e0db0d06b2cde4373d75a48d31`  
		Last Modified: Thu, 17 Oct 2024 21:23:07 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:8f1136f07bdb2dd09104677c02d056c403168a60a6d66614e0f219e21c080a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6415327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969483432fc409414014878a2369f2c7eef07fd3dd664b0e6dead0dc6d875704`

```dockerfile
```

-	Layers:
	-	`sha256:d044b823dd4a6b4af1fe428baaf026436636a7122c95611af58b9a4ee3dfbec7`  
		Last Modified: Thu, 17 Oct 2024 21:23:07 GMT  
		Size: 6.4 MB (6400861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ec7d0e401101c9001c1ade77d9396a4b9c8859b73e70a0d3768a2b107987dee`  
		Last Modified: Thu, 17 Oct 2024 21:23:07 GMT  
		Size: 14.5 KB (14466 bytes)  
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
$ docker pull telegraf@sha256:49dbcf977fccc4eb1a0ece3d82b782fde035eaf9a9c50504f885cce42897cd8e
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
$ docker pull telegraf@sha256:f79645d0240b0e7e8d28ad7f6d0a7a21c408033ec1cc13fc7f475636f7d5bf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163445043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6a3bfbe4006c53d3dd7547eaba528445155ff825901c246ad6988318386fd4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbd1a615af2df22f2b15f5ad5cb2f173a13e164ce9f01bcd751a557d3e4acb2`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 18.9 MB (18947918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73752d9a19ef19ab378a03d151489ff46b7504b598354287b7af1a7026474f7`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7b40e7109ff62a6cd577ccb8c67c850ea2eabc0b6554dae89a3a5edf511803`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 70.9 MB (70888320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b47b69e9123c04c769e565d6cbe88d5e8d16926891d6c84f21eb573d9e7bdf`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:340795b11e4b687c0b80db6c7ac286e30165342ad8d22cfb3e3878a4c4043d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6443005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6111778aad66ee2131172053cd72afa9d883063ad67d709a6c00d6c691cbb76c`

```dockerfile
```

-	Layers:
	-	`sha256:39c9cc119205ae45e26963ea62bfa9636de7cf8ad630bc193c22cd6dec8a2900`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 6.4 MB (6428233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:243163876f5c67d58f3511c40b96decffae025e1deb3f824ad9c899ef0d70c42`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:eb1362b86487c58cc3eedcecc930c1d2ea707d1a54f23f2e86adde234de1fc3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150492868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9cfbd47e80505ab0beaf46701ea3812258575cadeab78102ef5f6d9b3334ca4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3332329de6b42a2c5f534a6f40381b05e4356eb62a42408f66b4d98e78cfee55`  
		Last Modified: Thu, 17 Oct 2024 03:36:59 GMT  
		Size: 22.0 MB (21957453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d145c46c1134675dd81d7f150a5956cd0534991b8712626affe84fdbc492d4e0`  
		Last Modified: Fri, 18 Oct 2024 02:16:51 GMT  
		Size: 17.7 MB (17724833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007f1d0a3dbb40db976a12849fd9dd9414e474b07b7a6ba8f34d999f06745782`  
		Last Modified: Fri, 18 Oct 2024 02:16:50 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69e3400482d857fc0fefdc3094f1780d3786c7bf40eb6d242715378395ddbf9`  
		Last Modified: Fri, 18 Oct 2024 02:18:42 GMT  
		Size: 65.7 MB (65660236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51dd83ebd073d1f6f0b7104313b22e4d288a94654f56d973e8eca63b665f5e1`  
		Last Modified: Fri, 18 Oct 2024 02:18:40 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:33cab6f8f48c594b57a6f17dd41e8e621373f2a6425a91a9c38f5ad1c447f774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6419256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1488cb71875a1522166dd1d8854f3b8d58d4f45b08fb3233ecc348d37994ed`

```dockerfile
```

-	Layers:
	-	`sha256:8d733c2db9cad610b0062cde762936efd02cbf1328906e4d9ba359e7abc3e052`  
		Last Modified: Fri, 18 Oct 2024 02:18:40 GMT  
		Size: 6.4 MB (6404504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:462a53325ce6a198b081809a76cbd910d4218603fb675e197ae7e1f3fb2d0d39`  
		Last Modified: Fri, 18 Oct 2024 02:18:40 GMT  
		Size: 14.8 KB (14752 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:bb4045f74b9acc3bc69b21af3f3e56c183b2d23aeabad3a23d03115d3d742228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155956546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99a4b0c4e80c0bbd5969e030260fd33530331849090df3ffdf2898ea6c625eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437f71cf1903685ed3f6314161e121602758f809a760d2bd2293f7cd8ce1abe1`  
		Last Modified: Thu, 17 Oct 2024 04:36:08 GMT  
		Size: 23.6 MB (23594190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882a729e136449584637961d6c36466fd4de00cf1bd3c42a5b0ef2cc649a9935`  
		Last Modified: Thu, 17 Oct 2024 21:22:22 GMT  
		Size: 18.9 MB (18870637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc475b03394d09612cdb1d4d2c146bff32385599b122b5d5385fd6e1011322c`  
		Last Modified: Thu, 17 Oct 2024 21:22:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d962aeb4af62e2815d8d098f34c65fdfb61d4d0ae402093d32d0e23cecba4e`  
		Last Modified: Thu, 17 Oct 2024 21:23:47 GMT  
		Size: 63.9 MB (63904347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eb623d0a674f3fb99e0c2851fd3509f2f430558ae529e97a20e207a1caa715`  
		Last Modified: Thu, 17 Oct 2024 21:23:45 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:0a4ca1cb89f457657faf440c2fcf2b12847d46f2eba5bec565f507a2c3ea6ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a351f1db952bb14500d8c1a31af9b318ba419c93a6f414068a2204f121e114`

```dockerfile
```

-	Layers:
	-	`sha256:4557c62bc087ec90e827f830c44e03677c3539d5cc8282a3b6d2f3b467e33e6a`  
		Last Modified: Thu, 17 Oct 2024 21:23:46 GMT  
		Size: 6.4 MB (6409790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bf8c96856c70b3c79754ffabccac33d2977d04279aa5bc4d399cb904fc71285`  
		Last Modified: Thu, 17 Oct 2024 21:23:45 GMT  
		Size: 14.8 KB (14780 bytes)  
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
$ docker pull telegraf@sha256:49dbcf977fccc4eb1a0ece3d82b782fde035eaf9a9c50504f885cce42897cd8e
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
$ docker pull telegraf@sha256:f79645d0240b0e7e8d28ad7f6d0a7a21c408033ec1cc13fc7f475636f7d5bf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163445043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6a3bfbe4006c53d3dd7547eaba528445155ff825901c246ad6988318386fd4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbd1a615af2df22f2b15f5ad5cb2f173a13e164ce9f01bcd751a557d3e4acb2`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 18.9 MB (18947918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73752d9a19ef19ab378a03d151489ff46b7504b598354287b7af1a7026474f7`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7b40e7109ff62a6cd577ccb8c67c850ea2eabc0b6554dae89a3a5edf511803`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 70.9 MB (70888320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b47b69e9123c04c769e565d6cbe88d5e8d16926891d6c84f21eb573d9e7bdf`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:340795b11e4b687c0b80db6c7ac286e30165342ad8d22cfb3e3878a4c4043d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6443005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6111778aad66ee2131172053cd72afa9d883063ad67d709a6c00d6c691cbb76c`

```dockerfile
```

-	Layers:
	-	`sha256:39c9cc119205ae45e26963ea62bfa9636de7cf8ad630bc193c22cd6dec8a2900`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 6.4 MB (6428233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:243163876f5c67d58f3511c40b96decffae025e1deb3f824ad9c899ef0d70c42`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.1` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:eb1362b86487c58cc3eedcecc930c1d2ea707d1a54f23f2e86adde234de1fc3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150492868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9cfbd47e80505ab0beaf46701ea3812258575cadeab78102ef5f6d9b3334ca4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3332329de6b42a2c5f534a6f40381b05e4356eb62a42408f66b4d98e78cfee55`  
		Last Modified: Thu, 17 Oct 2024 03:36:59 GMT  
		Size: 22.0 MB (21957453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d145c46c1134675dd81d7f150a5956cd0534991b8712626affe84fdbc492d4e0`  
		Last Modified: Fri, 18 Oct 2024 02:16:51 GMT  
		Size: 17.7 MB (17724833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007f1d0a3dbb40db976a12849fd9dd9414e474b07b7a6ba8f34d999f06745782`  
		Last Modified: Fri, 18 Oct 2024 02:16:50 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69e3400482d857fc0fefdc3094f1780d3786c7bf40eb6d242715378395ddbf9`  
		Last Modified: Fri, 18 Oct 2024 02:18:42 GMT  
		Size: 65.7 MB (65660236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51dd83ebd073d1f6f0b7104313b22e4d288a94654f56d973e8eca63b665f5e1`  
		Last Modified: Fri, 18 Oct 2024 02:18:40 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:33cab6f8f48c594b57a6f17dd41e8e621373f2a6425a91a9c38f5ad1c447f774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6419256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1488cb71875a1522166dd1d8854f3b8d58d4f45b08fb3233ecc348d37994ed`

```dockerfile
```

-	Layers:
	-	`sha256:8d733c2db9cad610b0062cde762936efd02cbf1328906e4d9ba359e7abc3e052`  
		Last Modified: Fri, 18 Oct 2024 02:18:40 GMT  
		Size: 6.4 MB (6404504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:462a53325ce6a198b081809a76cbd910d4218603fb675e197ae7e1f3fb2d0d39`  
		Last Modified: Fri, 18 Oct 2024 02:18:40 GMT  
		Size: 14.8 KB (14752 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.1` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:bb4045f74b9acc3bc69b21af3f3e56c183b2d23aeabad3a23d03115d3d742228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155956546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99a4b0c4e80c0bbd5969e030260fd33530331849090df3ffdf2898ea6c625eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437f71cf1903685ed3f6314161e121602758f809a760d2bd2293f7cd8ce1abe1`  
		Last Modified: Thu, 17 Oct 2024 04:36:08 GMT  
		Size: 23.6 MB (23594190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882a729e136449584637961d6c36466fd4de00cf1bd3c42a5b0ef2cc649a9935`  
		Last Modified: Thu, 17 Oct 2024 21:22:22 GMT  
		Size: 18.9 MB (18870637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc475b03394d09612cdb1d4d2c146bff32385599b122b5d5385fd6e1011322c`  
		Last Modified: Thu, 17 Oct 2024 21:22:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d962aeb4af62e2815d8d098f34c65fdfb61d4d0ae402093d32d0e23cecba4e`  
		Last Modified: Thu, 17 Oct 2024 21:23:47 GMT  
		Size: 63.9 MB (63904347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eb623d0a674f3fb99e0c2851fd3509f2f430558ae529e97a20e207a1caa715`  
		Last Modified: Thu, 17 Oct 2024 21:23:45 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:0a4ca1cb89f457657faf440c2fcf2b12847d46f2eba5bec565f507a2c3ea6ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a351f1db952bb14500d8c1a31af9b318ba419c93a6f414068a2204f121e114`

```dockerfile
```

-	Layers:
	-	`sha256:4557c62bc087ec90e827f830c44e03677c3539d5cc8282a3b6d2f3b467e33e6a`  
		Last Modified: Thu, 17 Oct 2024 21:23:46 GMT  
		Size: 6.4 MB (6409790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bf8c96856c70b3c79754ffabccac33d2977d04279aa5bc4d399cb904fc71285`  
		Last Modified: Thu, 17 Oct 2024 21:23:45 GMT  
		Size: 14.8 KB (14780 bytes)  
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
$ docker pull telegraf@sha256:49dbcf977fccc4eb1a0ece3d82b782fde035eaf9a9c50504f885cce42897cd8e
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
$ docker pull telegraf@sha256:f79645d0240b0e7e8d28ad7f6d0a7a21c408033ec1cc13fc7f475636f7d5bf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163445043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6a3bfbe4006c53d3dd7547eaba528445155ff825901c246ad6988318386fd4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbd1a615af2df22f2b15f5ad5cb2f173a13e164ce9f01bcd751a557d3e4acb2`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 18.9 MB (18947918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73752d9a19ef19ab378a03d151489ff46b7504b598354287b7af1a7026474f7`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7b40e7109ff62a6cd577ccb8c67c850ea2eabc0b6554dae89a3a5edf511803`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 70.9 MB (70888320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b47b69e9123c04c769e565d6cbe88d5e8d16926891d6c84f21eb573d9e7bdf`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:340795b11e4b687c0b80db6c7ac286e30165342ad8d22cfb3e3878a4c4043d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6443005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6111778aad66ee2131172053cd72afa9d883063ad67d709a6c00d6c691cbb76c`

```dockerfile
```

-	Layers:
	-	`sha256:39c9cc119205ae45e26963ea62bfa9636de7cf8ad630bc193c22cd6dec8a2900`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 6.4 MB (6428233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:243163876f5c67d58f3511c40b96decffae025e1deb3f824ad9c899ef0d70c42`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:eb1362b86487c58cc3eedcecc930c1d2ea707d1a54f23f2e86adde234de1fc3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150492868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9cfbd47e80505ab0beaf46701ea3812258575cadeab78102ef5f6d9b3334ca4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3332329de6b42a2c5f534a6f40381b05e4356eb62a42408f66b4d98e78cfee55`  
		Last Modified: Thu, 17 Oct 2024 03:36:59 GMT  
		Size: 22.0 MB (21957453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d145c46c1134675dd81d7f150a5956cd0534991b8712626affe84fdbc492d4e0`  
		Last Modified: Fri, 18 Oct 2024 02:16:51 GMT  
		Size: 17.7 MB (17724833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007f1d0a3dbb40db976a12849fd9dd9414e474b07b7a6ba8f34d999f06745782`  
		Last Modified: Fri, 18 Oct 2024 02:16:50 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69e3400482d857fc0fefdc3094f1780d3786c7bf40eb6d242715378395ddbf9`  
		Last Modified: Fri, 18 Oct 2024 02:18:42 GMT  
		Size: 65.7 MB (65660236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51dd83ebd073d1f6f0b7104313b22e4d288a94654f56d973e8eca63b665f5e1`  
		Last Modified: Fri, 18 Oct 2024 02:18:40 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:33cab6f8f48c594b57a6f17dd41e8e621373f2a6425a91a9c38f5ad1c447f774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6419256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1488cb71875a1522166dd1d8854f3b8d58d4f45b08fb3233ecc348d37994ed`

```dockerfile
```

-	Layers:
	-	`sha256:8d733c2db9cad610b0062cde762936efd02cbf1328906e4d9ba359e7abc3e052`  
		Last Modified: Fri, 18 Oct 2024 02:18:40 GMT  
		Size: 6.4 MB (6404504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:462a53325ce6a198b081809a76cbd910d4218603fb675e197ae7e1f3fb2d0d39`  
		Last Modified: Fri, 18 Oct 2024 02:18:40 GMT  
		Size: 14.8 KB (14752 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:bb4045f74b9acc3bc69b21af3f3e56c183b2d23aeabad3a23d03115d3d742228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155956546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99a4b0c4e80c0bbd5969e030260fd33530331849090df3ffdf2898ea6c625eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Oct 2024 21:02:29 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437f71cf1903685ed3f6314161e121602758f809a760d2bd2293f7cd8ce1abe1`  
		Last Modified: Thu, 17 Oct 2024 04:36:08 GMT  
		Size: 23.6 MB (23594190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882a729e136449584637961d6c36466fd4de00cf1bd3c42a5b0ef2cc649a9935`  
		Last Modified: Thu, 17 Oct 2024 21:22:22 GMT  
		Size: 18.9 MB (18870637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc475b03394d09612cdb1d4d2c146bff32385599b122b5d5385fd6e1011322c`  
		Last Modified: Thu, 17 Oct 2024 21:22:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d962aeb4af62e2815d8d098f34c65fdfb61d4d0ae402093d32d0e23cecba4e`  
		Last Modified: Thu, 17 Oct 2024 21:23:47 GMT  
		Size: 63.9 MB (63904347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eb623d0a674f3fb99e0c2851fd3509f2f430558ae529e97a20e207a1caa715`  
		Last Modified: Thu, 17 Oct 2024 21:23:45 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:0a4ca1cb89f457657faf440c2fcf2b12847d46f2eba5bec565f507a2c3ea6ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a351f1db952bb14500d8c1a31af9b318ba419c93a6f414068a2204f121e114`

```dockerfile
```

-	Layers:
	-	`sha256:4557c62bc087ec90e827f830c44e03677c3539d5cc8282a3b6d2f3b467e33e6a`  
		Last Modified: Thu, 17 Oct 2024 21:23:46 GMT  
		Size: 6.4 MB (6409790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bf8c96856c70b3c79754ffabccac33d2977d04279aa5bc4d399cb904fc71285`  
		Last Modified: Thu, 17 Oct 2024 21:23:45 GMT  
		Size: 14.8 KB (14780 bytes)  
		MIME: application/vnd.in-toto+json
