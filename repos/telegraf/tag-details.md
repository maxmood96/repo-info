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
$ docker pull telegraf@sha256:94e0d68faa799eac894fb8aa6cb192ba715ebac10699ea3cc96feb800bc773b3
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
$ docker pull telegraf@sha256:1aec78acd484e3052a3b744aa4f506524919a9da02fc1433e8b4c0c4df5929c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143045409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e3cf41e7ffdc46a369d820c9892c0398ad9c39b7f4f3bbb63bf1661b4676b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2247d3273aa1d92c25210b647da389293f770c7463e0680590bba2707a00d4f`  
		Last Modified: Sat, 19 Oct 2024 07:17:52 GMT  
		Size: 17.7 MB (17724956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431a3580592e7869e0e9a687eeb734ecbf61aa4864384cb91bf7c24aee3a5b0a`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d2306cc2f9dc432bdab9577e71740b948af00d4db1eb08443a0547eca2e52a`  
		Last Modified: Sat, 19 Oct 2024 07:17:54 GMT  
		Size: 58.2 MB (58212698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb81901359f5d7c38fe327abcc66538f8e4bbe770e9fdbc72048a59bd935fc94`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:a04be35abee58909c3d42aced2d9147ca36e1a4e096534266a96b0d2acfcf695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6419536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade3393bc72761ef0b9812ba99ab201b31ea335dce0f4179478937d6a830cc27`

```dockerfile
```

-	Layers:
	-	`sha256:761d0fbf418de95f0bf4b3d8831e7c0247231173b138cb38369af68e028d09aa`  
		Last Modified: Sat, 19 Oct 2024 07:17:52 GMT  
		Size: 6.4 MB (6404950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb0764e2e8db77601eaa76a040320d4088bea4d5b360d5b3af5469ddfb0053ac`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 14.6 KB (14586 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e15f4ecf24e9acd0d799b33dfe2655209cce1a2329ef58b7ea340d6b47526440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149174941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ee0153e92a6e7016af48b545c85b7478ac2c16331e327c3b5ffc11460a7058`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c997025d65b9a3a17af2a5da355e59ddaef61afc5603e6e4f3d8c348d5dee2e2`  
		Last Modified: Sat, 19 Oct 2024 05:58:23 GMT  
		Size: 18.9 MB (18870445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3541e233720a537128c65519a803fff6e89bcae5e59f21c04e1e51e762996f72`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91266b6b4b069749e7b9cfe1bb730c4ecfdcfca9f33b816b9e2f0c17f10ea15`  
		Last Modified: Sat, 19 Oct 2024 05:58:24 GMT  
		Size: 57.1 MB (57123282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87c4bdfef8f024628957e3162ad4436c4d57fb0e5040c1e3a5970fbc4c23765`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:112ebaf7d621c726e72b5cb30a87e70283e1615524cf0c1ee94c1df9ba4a6b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc917b77a06f4ce84e84f3a352332a56c87ccbecb7fadb540e51ac5ca6f6cce`

```dockerfile
```

-	Layers:
	-	`sha256:8024b92a362069ab5c8cdbe2cdfe57d14579b8365e3e06d0e1968917732bd2a0`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 6.4 MB (6410234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54f4a4fa2a8c4f7d57746c6e9e061682eb70b2191cce975516f2585ac36a1024`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 14.6 KB (14610 bytes)  
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
$ docker pull telegraf@sha256:94e0d68faa799eac894fb8aa6cb192ba715ebac10699ea3cc96feb800bc773b3
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
$ docker pull telegraf@sha256:1aec78acd484e3052a3b744aa4f506524919a9da02fc1433e8b4c0c4df5929c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143045409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e3cf41e7ffdc46a369d820c9892c0398ad9c39b7f4f3bbb63bf1661b4676b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2247d3273aa1d92c25210b647da389293f770c7463e0680590bba2707a00d4f`  
		Last Modified: Sat, 19 Oct 2024 07:17:52 GMT  
		Size: 17.7 MB (17724956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431a3580592e7869e0e9a687eeb734ecbf61aa4864384cb91bf7c24aee3a5b0a`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d2306cc2f9dc432bdab9577e71740b948af00d4db1eb08443a0547eca2e52a`  
		Last Modified: Sat, 19 Oct 2024 07:17:54 GMT  
		Size: 58.2 MB (58212698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb81901359f5d7c38fe327abcc66538f8e4bbe770e9fdbc72048a59bd935fc94`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:a04be35abee58909c3d42aced2d9147ca36e1a4e096534266a96b0d2acfcf695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6419536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade3393bc72761ef0b9812ba99ab201b31ea335dce0f4179478937d6a830cc27`

```dockerfile
```

-	Layers:
	-	`sha256:761d0fbf418de95f0bf4b3d8831e7c0247231173b138cb38369af68e028d09aa`  
		Last Modified: Sat, 19 Oct 2024 07:17:52 GMT  
		Size: 6.4 MB (6404950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb0764e2e8db77601eaa76a040320d4088bea4d5b360d5b3af5469ddfb0053ac`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 14.6 KB (14586 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e15f4ecf24e9acd0d799b33dfe2655209cce1a2329ef58b7ea340d6b47526440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149174941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ee0153e92a6e7016af48b545c85b7478ac2c16331e327c3b5ffc11460a7058`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c997025d65b9a3a17af2a5da355e59ddaef61afc5603e6e4f3d8c348d5dee2e2`  
		Last Modified: Sat, 19 Oct 2024 05:58:23 GMT  
		Size: 18.9 MB (18870445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3541e233720a537128c65519a803fff6e89bcae5e59f21c04e1e51e762996f72`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91266b6b4b069749e7b9cfe1bb730c4ecfdcfca9f33b816b9e2f0c17f10ea15`  
		Last Modified: Sat, 19 Oct 2024 05:58:24 GMT  
		Size: 57.1 MB (57123282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87c4bdfef8f024628957e3162ad4436c4d57fb0e5040c1e3a5970fbc4c23765`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:112ebaf7d621c726e72b5cb30a87e70283e1615524cf0c1ee94c1df9ba4a6b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc917b77a06f4ce84e84f3a352332a56c87ccbecb7fadb540e51ac5ca6f6cce`

```dockerfile
```

-	Layers:
	-	`sha256:8024b92a362069ab5c8cdbe2cdfe57d14579b8365e3e06d0e1968917732bd2a0`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 6.4 MB (6410234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54f4a4fa2a8c4f7d57746c6e9e061682eb70b2191cce975516f2585ac36a1024`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 14.6 KB (14610 bytes)  
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
$ docker pull telegraf@sha256:9eb6c868bcc7ec550b7aa3c19eb7a5c0a0ba32aa3d56653a471fa353cf08df57
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
$ docker pull telegraf@sha256:a1f078b55f9f610ad5846395121f8d60f6c31fb7a8092e765f6d4db750c743a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146505020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc155a80eba3d2e0e66066a2ea4ba35e3f0bdebd523c802855c2681d88f4222`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2247d3273aa1d92c25210b647da389293f770c7463e0680590bba2707a00d4f`  
		Last Modified: Sat, 19 Oct 2024 07:17:52 GMT  
		Size: 17.7 MB (17724956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431a3580592e7869e0e9a687eeb734ecbf61aa4864384cb91bf7c24aee3a5b0a`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eacb03abf0c7c48a71fac48e96e9fb38faf180c40f09354e23071882ad24bb7`  
		Last Modified: Sat, 19 Oct 2024 07:18:47 GMT  
		Size: 61.7 MB (61672311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07573c18686fe6f8cdb08b70ad829f06e91f077d95acb7a82cadadcfd3e5ce9`  
		Last Modified: Sat, 19 Oct 2024 07:18:45 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:5d74cb512d2619f69c3f63bfe9e759d3081100e6e4c546343cc4ebaba8e757fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6428539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6beecdecb74e8d6019ebb06c9e34c2e00d6b4f356b6e908614a52c2ff5c2e86`

```dockerfile
```

-	Layers:
	-	`sha256:8e2bc141fe377ba66db0533d0c54136a71ec022c574f6540f4cf334d06ecec14`  
		Last Modified: Sat, 19 Oct 2024 07:18:46 GMT  
		Size: 6.4 MB (6413955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01b2b73c2f10326706992aae9c3de960b27cfb07a2f91ced75197a04ebbb769d`  
		Last Modified: Sat, 19 Oct 2024 07:18:45 GMT  
		Size: 14.6 KB (14584 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:7243bd28d2fc52162e63d17c1a3da13033a0581c9346803c5434c2c9b55b1a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152429478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ee2e306a81782ddda358f26d15807b7b9c15c9fe6b26691ad431801db79687`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c997025d65b9a3a17af2a5da355e59ddaef61afc5603e6e4f3d8c348d5dee2e2`  
		Last Modified: Sat, 19 Oct 2024 05:58:23 GMT  
		Size: 18.9 MB (18870445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3541e233720a537128c65519a803fff6e89bcae5e59f21c04e1e51e762996f72`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe15e9c7710d70a178beb6ed98ba9e666ffd3580ad8e46febf1b90bb762a4803`  
		Last Modified: Sat, 19 Oct 2024 05:59:10 GMT  
		Size: 60.4 MB (60377818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2322d8dc04ab6e646d0172e015614584248b876c90fa93dc2c397cc6a41405`  
		Last Modified: Sat, 19 Oct 2024 05:59:08 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:1f27329d7ea64281bf1adc2d1fc4f1aaef16af5304fc5d3fab12adbf0e651812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6434643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8451d90d88989cbf130586d38cf79ea9ecdac03bbf610b50dd9ae3fd99c3a7bf`

```dockerfile
```

-	Layers:
	-	`sha256:c0ce5698d7c8fa7a6dd546ca94f7a72c2388bf409df4b8e23aaa2a5631b78de6`  
		Last Modified: Sat, 19 Oct 2024 05:59:09 GMT  
		Size: 6.4 MB (6420034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:574153a67c23c0bfa30b4e1fd1c808e0a4921c304ced1ff0cddc66db662ef3ff`  
		Last Modified: Sat, 19 Oct 2024 05:59:08 GMT  
		Size: 14.6 KB (14609 bytes)  
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
$ docker pull telegraf@sha256:9eb6c868bcc7ec550b7aa3c19eb7a5c0a0ba32aa3d56653a471fa353cf08df57
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
$ docker pull telegraf@sha256:a1f078b55f9f610ad5846395121f8d60f6c31fb7a8092e765f6d4db750c743a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146505020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc155a80eba3d2e0e66066a2ea4ba35e3f0bdebd523c802855c2681d88f4222`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2247d3273aa1d92c25210b647da389293f770c7463e0680590bba2707a00d4f`  
		Last Modified: Sat, 19 Oct 2024 07:17:52 GMT  
		Size: 17.7 MB (17724956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431a3580592e7869e0e9a687eeb734ecbf61aa4864384cb91bf7c24aee3a5b0a`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eacb03abf0c7c48a71fac48e96e9fb38faf180c40f09354e23071882ad24bb7`  
		Last Modified: Sat, 19 Oct 2024 07:18:47 GMT  
		Size: 61.7 MB (61672311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07573c18686fe6f8cdb08b70ad829f06e91f077d95acb7a82cadadcfd3e5ce9`  
		Last Modified: Sat, 19 Oct 2024 07:18:45 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:5d74cb512d2619f69c3f63bfe9e759d3081100e6e4c546343cc4ebaba8e757fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6428539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6beecdecb74e8d6019ebb06c9e34c2e00d6b4f356b6e908614a52c2ff5c2e86`

```dockerfile
```

-	Layers:
	-	`sha256:8e2bc141fe377ba66db0533d0c54136a71ec022c574f6540f4cf334d06ecec14`  
		Last Modified: Sat, 19 Oct 2024 07:18:46 GMT  
		Size: 6.4 MB (6413955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01b2b73c2f10326706992aae9c3de960b27cfb07a2f91ced75197a04ebbb769d`  
		Last Modified: Sat, 19 Oct 2024 07:18:45 GMT  
		Size: 14.6 KB (14584 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:7243bd28d2fc52162e63d17c1a3da13033a0581c9346803c5434c2c9b55b1a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152429478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ee2e306a81782ddda358f26d15807b7b9c15c9fe6b26691ad431801db79687`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c997025d65b9a3a17af2a5da355e59ddaef61afc5603e6e4f3d8c348d5dee2e2`  
		Last Modified: Sat, 19 Oct 2024 05:58:23 GMT  
		Size: 18.9 MB (18870445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3541e233720a537128c65519a803fff6e89bcae5e59f21c04e1e51e762996f72`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe15e9c7710d70a178beb6ed98ba9e666ffd3580ad8e46febf1b90bb762a4803`  
		Last Modified: Sat, 19 Oct 2024 05:59:10 GMT  
		Size: 60.4 MB (60377818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2322d8dc04ab6e646d0172e015614584248b876c90fa93dc2c397cc6a41405`  
		Last Modified: Sat, 19 Oct 2024 05:59:08 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:1f27329d7ea64281bf1adc2d1fc4f1aaef16af5304fc5d3fab12adbf0e651812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6434643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8451d90d88989cbf130586d38cf79ea9ecdac03bbf610b50dd9ae3fd99c3a7bf`

```dockerfile
```

-	Layers:
	-	`sha256:c0ce5698d7c8fa7a6dd546ca94f7a72c2388bf409df4b8e23aaa2a5631b78de6`  
		Last Modified: Sat, 19 Oct 2024 05:59:09 GMT  
		Size: 6.4 MB (6420034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:574153a67c23c0bfa30b4e1fd1c808e0a4921c304ced1ff0cddc66db662ef3ff`  
		Last Modified: Sat, 19 Oct 2024 05:59:08 GMT  
		Size: 14.6 KB (14609 bytes)  
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
$ docker pull telegraf@sha256:e936a88678ebb732e87331b379d8e9ef6ff109ae8788b5ee9ee42fa997952f35
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
$ docker pull telegraf@sha256:8889195de0860f9ba3bd1d60f08ce1d51d4a03b33f03f0a82b50d861d41d7060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150492935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73516376c2e12f9c6861685c0f00740c92612a9a975227971b3fb820d4fe038`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2247d3273aa1d92c25210b647da389293f770c7463e0680590bba2707a00d4f`  
		Last Modified: Sat, 19 Oct 2024 07:17:52 GMT  
		Size: 17.7 MB (17724956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431a3580592e7869e0e9a687eeb734ecbf61aa4864384cb91bf7c24aee3a5b0a`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8b358a14a13e2f3c8bc662d86d0c8400edd9ec0748d9c7410bd7d4099d7b63`  
		Last Modified: Sat, 19 Oct 2024 07:19:40 GMT  
		Size: 65.7 MB (65660223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f379b324a2615b7d7ee7f25c755a7b219ff7961e9cc150b932b9c570aa0bcb10`  
		Last Modified: Sat, 19 Oct 2024 07:19:37 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:e8cda4ed6c7880693526a91c3539d43b80efd9b0e257468a2302f2392491dd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0283b6d5e93653256ed3a0fe39757b2d3f7d2bb14f424c98f79ef89faa50424f`

```dockerfile
```

-	Layers:
	-	`sha256:f98e131241ac341dbec655d0d731ff8a3bd8bedf9f228d6b4fba6bc09a9f0eba`  
		Last Modified: Sat, 19 Oct 2024 07:19:38 GMT  
		Size: 6.4 MB (6423677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f649043c97cf1464f256cc02da19c3e33e3b4144d1e59bbf8e025ff1ec5c69f6`  
		Last Modified: Sat, 19 Oct 2024 07:19:37 GMT  
		Size: 14.9 KB (14896 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6f539117e4e3f6a35a89f2f0dcda8168dee59184615d7f85cd804904e758d2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155956057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59e084ed05bbbfb6ecede5931d1866cd3bec38a5f64d158f1fcc80097e243e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c997025d65b9a3a17af2a5da355e59ddaef61afc5603e6e4f3d8c348d5dee2e2`  
		Last Modified: Sat, 19 Oct 2024 05:58:23 GMT  
		Size: 18.9 MB (18870445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3541e233720a537128c65519a803fff6e89bcae5e59f21c04e1e51e762996f72`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a168539fced4a13ac7b7038a0762bb103cd13433c435c2e39f0947c9e83f4b37`  
		Last Modified: Sat, 19 Oct 2024 05:59:48 GMT  
		Size: 63.9 MB (63904396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcb66cc4b191f0e022136e67e096613748738f167372068a005655154634c72`  
		Last Modified: Sat, 19 Oct 2024 05:59:45 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:ef6be82091e0dc83440dd6cecd5389dd4042af6d5068d317e589a29472bebc55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6443887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d333f2c095b4dcdee785bba674fe36fa15f38429ea1c8600daa58b62b0544bb0`

```dockerfile
```

-	Layers:
	-	`sha256:77b6430c26b2c64a088d675a53dd2fb40868e9fa40347f6210c4a052463ca758`  
		Last Modified: Sat, 19 Oct 2024 05:59:46 GMT  
		Size: 6.4 MB (6428963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:772d51ebd64dcc7649d8b400a769d6486cd37f9ee3510ec1dc1974435235f5ab`  
		Last Modified: Sat, 19 Oct 2024 05:59:45 GMT  
		Size: 14.9 KB (14924 bytes)  
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
$ docker pull telegraf@sha256:e936a88678ebb732e87331b379d8e9ef6ff109ae8788b5ee9ee42fa997952f35
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
$ docker pull telegraf@sha256:8889195de0860f9ba3bd1d60f08ce1d51d4a03b33f03f0a82b50d861d41d7060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150492935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73516376c2e12f9c6861685c0f00740c92612a9a975227971b3fb820d4fe038`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2247d3273aa1d92c25210b647da389293f770c7463e0680590bba2707a00d4f`  
		Last Modified: Sat, 19 Oct 2024 07:17:52 GMT  
		Size: 17.7 MB (17724956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431a3580592e7869e0e9a687eeb734ecbf61aa4864384cb91bf7c24aee3a5b0a`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8b358a14a13e2f3c8bc662d86d0c8400edd9ec0748d9c7410bd7d4099d7b63`  
		Last Modified: Sat, 19 Oct 2024 07:19:40 GMT  
		Size: 65.7 MB (65660223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f379b324a2615b7d7ee7f25c755a7b219ff7961e9cc150b932b9c570aa0bcb10`  
		Last Modified: Sat, 19 Oct 2024 07:19:37 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:e8cda4ed6c7880693526a91c3539d43b80efd9b0e257468a2302f2392491dd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0283b6d5e93653256ed3a0fe39757b2d3f7d2bb14f424c98f79ef89faa50424f`

```dockerfile
```

-	Layers:
	-	`sha256:f98e131241ac341dbec655d0d731ff8a3bd8bedf9f228d6b4fba6bc09a9f0eba`  
		Last Modified: Sat, 19 Oct 2024 07:19:38 GMT  
		Size: 6.4 MB (6423677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f649043c97cf1464f256cc02da19c3e33e3b4144d1e59bbf8e025ff1ec5c69f6`  
		Last Modified: Sat, 19 Oct 2024 07:19:37 GMT  
		Size: 14.9 KB (14896 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.1` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6f539117e4e3f6a35a89f2f0dcda8168dee59184615d7f85cd804904e758d2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155956057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59e084ed05bbbfb6ecede5931d1866cd3bec38a5f64d158f1fcc80097e243e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c997025d65b9a3a17af2a5da355e59ddaef61afc5603e6e4f3d8c348d5dee2e2`  
		Last Modified: Sat, 19 Oct 2024 05:58:23 GMT  
		Size: 18.9 MB (18870445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3541e233720a537128c65519a803fff6e89bcae5e59f21c04e1e51e762996f72`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a168539fced4a13ac7b7038a0762bb103cd13433c435c2e39f0947c9e83f4b37`  
		Last Modified: Sat, 19 Oct 2024 05:59:48 GMT  
		Size: 63.9 MB (63904396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcb66cc4b191f0e022136e67e096613748738f167372068a005655154634c72`  
		Last Modified: Sat, 19 Oct 2024 05:59:45 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:ef6be82091e0dc83440dd6cecd5389dd4042af6d5068d317e589a29472bebc55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6443887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d333f2c095b4dcdee785bba674fe36fa15f38429ea1c8600daa58b62b0544bb0`

```dockerfile
```

-	Layers:
	-	`sha256:77b6430c26b2c64a088d675a53dd2fb40868e9fa40347f6210c4a052463ca758`  
		Last Modified: Sat, 19 Oct 2024 05:59:46 GMT  
		Size: 6.4 MB (6428963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:772d51ebd64dcc7649d8b400a769d6486cd37f9ee3510ec1dc1974435235f5ab`  
		Last Modified: Sat, 19 Oct 2024 05:59:45 GMT  
		Size: 14.9 KB (14924 bytes)  
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
$ docker pull telegraf@sha256:e936a88678ebb732e87331b379d8e9ef6ff109ae8788b5ee9ee42fa997952f35
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
$ docker pull telegraf@sha256:8889195de0860f9ba3bd1d60f08ce1d51d4a03b33f03f0a82b50d861d41d7060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150492935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73516376c2e12f9c6861685c0f00740c92612a9a975227971b3fb820d4fe038`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2247d3273aa1d92c25210b647da389293f770c7463e0680590bba2707a00d4f`  
		Last Modified: Sat, 19 Oct 2024 07:17:52 GMT  
		Size: 17.7 MB (17724956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431a3580592e7869e0e9a687eeb734ecbf61aa4864384cb91bf7c24aee3a5b0a`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8b358a14a13e2f3c8bc662d86d0c8400edd9ec0748d9c7410bd7d4099d7b63`  
		Last Modified: Sat, 19 Oct 2024 07:19:40 GMT  
		Size: 65.7 MB (65660223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f379b324a2615b7d7ee7f25c755a7b219ff7961e9cc150b932b9c570aa0bcb10`  
		Last Modified: Sat, 19 Oct 2024 07:19:37 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:e8cda4ed6c7880693526a91c3539d43b80efd9b0e257468a2302f2392491dd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0283b6d5e93653256ed3a0fe39757b2d3f7d2bb14f424c98f79ef89faa50424f`

```dockerfile
```

-	Layers:
	-	`sha256:f98e131241ac341dbec655d0d731ff8a3bd8bedf9f228d6b4fba6bc09a9f0eba`  
		Last Modified: Sat, 19 Oct 2024 07:19:38 GMT  
		Size: 6.4 MB (6423677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f649043c97cf1464f256cc02da19c3e33e3b4144d1e59bbf8e025ff1ec5c69f6`  
		Last Modified: Sat, 19 Oct 2024 07:19:37 GMT  
		Size: 14.9 KB (14896 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6f539117e4e3f6a35a89f2f0dcda8168dee59184615d7f85cd804904e758d2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155956057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59e084ed05bbbfb6ecede5931d1866cd3bec38a5f64d158f1fcc80097e243e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c997025d65b9a3a17af2a5da355e59ddaef61afc5603e6e4f3d8c348d5dee2e2`  
		Last Modified: Sat, 19 Oct 2024 05:58:23 GMT  
		Size: 18.9 MB (18870445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3541e233720a537128c65519a803fff6e89bcae5e59f21c04e1e51e762996f72`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a168539fced4a13ac7b7038a0762bb103cd13433c435c2e39f0947c9e83f4b37`  
		Last Modified: Sat, 19 Oct 2024 05:59:48 GMT  
		Size: 63.9 MB (63904396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcb66cc4b191f0e022136e67e096613748738f167372068a005655154634c72`  
		Last Modified: Sat, 19 Oct 2024 05:59:45 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:ef6be82091e0dc83440dd6cecd5389dd4042af6d5068d317e589a29472bebc55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6443887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d333f2c095b4dcdee785bba674fe36fa15f38429ea1c8600daa58b62b0544bb0`

```dockerfile
```

-	Layers:
	-	`sha256:77b6430c26b2c64a088d675a53dd2fb40868e9fa40347f6210c4a052463ca758`  
		Last Modified: Sat, 19 Oct 2024 05:59:46 GMT  
		Size: 6.4 MB (6428963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:772d51ebd64dcc7649d8b400a769d6486cd37f9ee3510ec1dc1974435235f5ab`  
		Last Modified: Sat, 19 Oct 2024 05:59:45 GMT  
		Size: 14.9 KB (14924 bytes)  
		MIME: application/vnd.in-toto+json
