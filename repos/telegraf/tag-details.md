<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.28`](#telegraf128)
-	[`telegraf:1.28-alpine`](#telegraf128-alpine)
-	[`telegraf:1.28.5`](#telegraf1285)
-	[`telegraf:1.28.5-alpine`](#telegraf1285-alpine)
-	[`telegraf:1.29`](#telegraf129)
-	[`telegraf:1.29-alpine`](#telegraf129-alpine)
-	[`telegraf:1.29.5`](#telegraf1295)
-	[`telegraf:1.29.5-alpine`](#telegraf1295-alpine)
-	[`telegraf:1.30`](#telegraf130)
-	[`telegraf:1.30-alpine`](#telegraf130-alpine)
-	[`telegraf:1.30.2`](#telegraf1302)
-	[`telegraf:1.30.2-alpine`](#telegraf1302-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.28`

```console
$ docker pull telegraf@sha256:9a04f2ec80cb061b34abcaebdf8d01f35114881a18389083b9f53a159f6ec3d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.28` - linux; amd64

```console
$ docker pull telegraf@sha256:33240207fa1349593faf03d141fd3d5ced78058e260ad1137910855fbf08e41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.7 MB (149665884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ae6dbe0d4687a3288815c399089143b9445693611a2c97d35c477d00a07805`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.28.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ab38a549bb1db5dddef5e6e26db5ac78b77af2bd2d0f4821326424f22d298b`  
		Last Modified: Tue, 14 May 2024 03:58:09 GMT  
		Size: 18.9 MB (18947938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a62a8620030f619d3cf945301ace7afaf92ba97b679e0fa1c98a6d67f4cc70`  
		Last Modified: Tue, 14 May 2024 03:58:08 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144de80196570ca4e1874cedeca0a1c0d348354dc0ba4255755674be934dbef1`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 57.1 MB (57089059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce18a76b0cc2ba6e0991913425b60ed3e9d8d8be18c5913a21a4af61b729efa`  
		Last Modified: Tue, 14 May 2024 03:58:08 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.28` - unknown; unknown

```console
$ docker pull telegraf@sha256:01763d24133cfe3dbb2d21818ca3d27b2c61cec49902a6f7ae53ec962f4d87b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6301446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2e5ec9ba67cd179dbd09522cb0e79fc53553a496586b9cf602e5be38573484`

```dockerfile
```

-	Layers:
	-	`sha256:a78a4e9e03a62b77506390683e9ceae6f2507df0d2331a08c1910727e15ebc57`  
		Last Modified: Tue, 14 May 2024 03:58:09 GMT  
		Size: 6.3 MB (6286839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7805e2b09d44a8a006edffbf797e561d2058c05fbf1d2800ffccbc394d2a46b`  
		Last Modified: Tue, 14 May 2024 03:58:08 GMT  
		Size: 14.6 KB (14607 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.28` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:8be5cddb24e1ae646abe1da13b60083450492563ce1e9003861e0cc4a69fb451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 MB (137410650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca300782c19f49a01130197b126501bfe4ca058f37f0730f54bc451498d455e9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.28.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342c7577918dea746df9c5fbcb51b929d73f1915b3c0e7723a4aad3ca148c343`  
		Last Modified: Wed, 01 May 2024 22:11:44 GMT  
		Size: 17.7 MB (17724944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b7f4d906aeb5335da996f149e84e5db08b1905e7ceb937cca7a8c9ac360ede`  
		Last Modified: Wed, 01 May 2024 22:11:43 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d2819792e1f5dae390cd3b8397dde7d2326b4dff3dca1fc9f16878c3e20859`  
		Last Modified: Wed, 01 May 2024 22:11:46 GMT  
		Size: 52.6 MB (52554334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b625e284ea4a2d01f989692812ef596620a39cbee81472ae1bef2658cf763e0a`  
		Last Modified: Wed, 01 May 2024 22:11:43 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.28` - unknown; unknown

```console
$ docker pull telegraf@sha256:33ea9a28e68a4d8e64aa08aa5a62112d681bac8ce9b5747226eccc918e960fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6298179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61eeab43ea66c2a4dac5836b654b89ac2b5f4a908cd26555763ddf273e06c80d`

```dockerfile
```

-	Layers:
	-	`sha256:5cfdd5b2a67aff315db5710bcf1f576549576fbaff5e3acd0d1f0e51fee174b9`  
		Last Modified: Wed, 01 May 2024 22:11:44 GMT  
		Size: 6.3 MB (6283493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0aac1728dcf2de80829a4bda1e3d33e130db6ac79b8f8b10599aaddb1ef0566`  
		Last Modified: Wed, 01 May 2024 22:11:43 GMT  
		Size: 14.7 KB (14686 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.28` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:53307d2e4c066b6dede63c2972a308b9f9b0d1b1107965263568c9ae3fa6099c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143823194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad5d7c38f7b4b4a57d5aab4117cad34db8a6396cdc16cb56e666ef4fda0dceb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.28.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4668ee134c6d27b158f31b1c01b5e92a02ede4c76d4b570eb243b76e7b7567bb`  
		Last Modified: Wed, 01 May 2024 22:33:11 GMT  
		Size: 18.9 MB (18870222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c26c91634d198f308ee466c4f2be3a59218fcaea48af76c19274245b1725a7`  
		Last Modified: Wed, 01 May 2024 22:33:10 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66655e7e968f4303965c9041a6153b0b67dc27163ac99e94b61cb44d5834c9a`  
		Last Modified: Wed, 01 May 2024 22:33:12 GMT  
		Size: 51.8 MB (51750427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e532d5b9e98e3a37b1cc0fb852f725db11b0bdfa5f4d9061b809597c40e5a5cc`  
		Last Modified: Wed, 01 May 2024 22:33:10 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.28` - unknown; unknown

```console
$ docker pull telegraf@sha256:7c8b765831780ceb0518b17be95ed03fa2c21399556724961a45aa2a5836471e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6303365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ddfcf2407c453744ae94f32adde44875cbdbacf4c54566406df77e647641b2`

```dockerfile
```

-	Layers:
	-	`sha256:d3b6bd6c13bc9dc145844676689ce90b2ed45d3245fcd5c81b906fba6c55fca0`  
		Last Modified: Wed, 01 May 2024 22:33:11 GMT  
		Size: 6.3 MB (6288752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:069c30aaeb6f2134d59790bc0c2dbcbfb0d869f13e7f0cec58a2fd4f21e3aa14`  
		Last Modified: Wed, 01 May 2024 22:33:10 GMT  
		Size: 14.6 KB (14613 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.28-alpine`

```console
$ docker pull telegraf@sha256:8fd669183dc1c3318a5612082f7d657edf112848a5e70410c2021bbc63031e68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.28-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7cba338ca92016582121fde2c24898918febf9b3eef331c22c29e2f8ca5e5e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62942629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f059acd12fbc58dbbc090caa04773587136a367c7b9038c91d604fa0d589abdc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.28.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17fad2ec8d7d60600e220db6fb8a5e092ca32c368693c0658a03e82657f8f41`  
		Last Modified: Wed, 01 May 2024 21:52:37 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b6121a80388ea00a0dbc1c04c3650a718461a3474a433f5fb37884d4d7e77f`  
		Last Modified: Wed, 01 May 2024 21:52:37 GMT  
		Size: 2.6 MB (2618961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dca7bfce4c5b88479b37008b8413b1f013e39942858c4ce8075cd7e39128d15`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 56.9 MB (56914331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057993a88da0b4e296106809567dd40a6837a253e42133a2e5861393b8df00d4`  
		Last Modified: Wed, 01 May 2024 21:52:37 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.28-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:a6cd83c191df04acc472bac921a9bd5a195648f395d58b558f2398dbdfcdf787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1367687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a24b0ff68640e8c99a2abbf1cd5bc052692b1c93a9372dfbdbdf6727087c822`

```dockerfile
```

-	Layers:
	-	`sha256:623625e27493362e4a9a7bfb5662f501afd16533ce18b77a6c19fe101c1a8322`  
		Last Modified: Wed, 01 May 2024 21:52:37 GMT  
		Size: 1.4 MB (1352836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a1ceabb5a013e854d6cc531d83c7d0719cab24fbe7b9367f8a3fa5ff1de7add`  
		Last Modified: Wed, 01 May 2024 21:52:36 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.28-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:47131515785890df9e7611b8b18c91af39088507d7e90a40965d461d12762c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57639035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a758b54f0b137c4dd2c70a41ce6d228d3251e609289b5a868fd969bce41517db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.28.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddde0fe2ef8e41514be0d2d260ff46c7fa8adda5734b6aeb56e6ba0b174c9b1`  
		Last Modified: Wed, 01 May 2024 22:33:41 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfb31b2d6527f81d9d04ddd4779a6ecdac4257e8769d6d10af4516be1c7b4c2`  
		Last Modified: Wed, 01 May 2024 22:33:42 GMT  
		Size: 2.7 MB (2702917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8f68a26a0ad339eeb0d8c0bd2ecb4236e191446f574c1bd62d4a61902be54e`  
		Last Modified: Wed, 01 May 2024 22:33:43 GMT  
		Size: 51.6 MB (51587795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae51613913a2b1c01f5e6e504b461b87176212f06bda835aeaadd8c84925982f`  
		Last Modified: Wed, 01 May 2024 22:33:42 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.28-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e8dd4caf80fc50ab8f6a2b00d3480dab03f6c11296eb40ddf710f854ef045df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1364386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ada9c4e6609f50cdc288d4b6e180f9a36311d2fe6a9e5e9b2a6f6cbcf1be9c6`

```dockerfile
```

-	Layers:
	-	`sha256:ed5ed0ffd625ec269350925987b84eead74b7c903b47f9469183299084d1e2bf`  
		Last Modified: Wed, 01 May 2024 22:33:42 GMT  
		Size: 1.3 MB (1349696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:360a526294b33adab1b047d10b9f4917c63b5609857cbffd825795f383bd5e64`  
		Last Modified: Wed, 01 May 2024 22:33:42 GMT  
		Size: 14.7 KB (14690 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.28.5`

```console
$ docker pull telegraf@sha256:9a04f2ec80cb061b34abcaebdf8d01f35114881a18389083b9f53a159f6ec3d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.28.5` - linux; amd64

```console
$ docker pull telegraf@sha256:33240207fa1349593faf03d141fd3d5ced78058e260ad1137910855fbf08e41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.7 MB (149665884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ae6dbe0d4687a3288815c399089143b9445693611a2c97d35c477d00a07805`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.28.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ab38a549bb1db5dddef5e6e26db5ac78b77af2bd2d0f4821326424f22d298b`  
		Last Modified: Tue, 14 May 2024 03:58:09 GMT  
		Size: 18.9 MB (18947938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a62a8620030f619d3cf945301ace7afaf92ba97b679e0fa1c98a6d67f4cc70`  
		Last Modified: Tue, 14 May 2024 03:58:08 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144de80196570ca4e1874cedeca0a1c0d348354dc0ba4255755674be934dbef1`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 57.1 MB (57089059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce18a76b0cc2ba6e0991913425b60ed3e9d8d8be18c5913a21a4af61b729efa`  
		Last Modified: Tue, 14 May 2024 03:58:08 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.28.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:01763d24133cfe3dbb2d21818ca3d27b2c61cec49902a6f7ae53ec962f4d87b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6301446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2e5ec9ba67cd179dbd09522cb0e79fc53553a496586b9cf602e5be38573484`

```dockerfile
```

-	Layers:
	-	`sha256:a78a4e9e03a62b77506390683e9ceae6f2507df0d2331a08c1910727e15ebc57`  
		Last Modified: Tue, 14 May 2024 03:58:09 GMT  
		Size: 6.3 MB (6286839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7805e2b09d44a8a006edffbf797e561d2058c05fbf1d2800ffccbc394d2a46b`  
		Last Modified: Tue, 14 May 2024 03:58:08 GMT  
		Size: 14.6 KB (14607 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.28.5` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:8be5cddb24e1ae646abe1da13b60083450492563ce1e9003861e0cc4a69fb451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 MB (137410650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca300782c19f49a01130197b126501bfe4ca058f37f0730f54bc451498d455e9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.28.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342c7577918dea746df9c5fbcb51b929d73f1915b3c0e7723a4aad3ca148c343`  
		Last Modified: Wed, 01 May 2024 22:11:44 GMT  
		Size: 17.7 MB (17724944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b7f4d906aeb5335da996f149e84e5db08b1905e7ceb937cca7a8c9ac360ede`  
		Last Modified: Wed, 01 May 2024 22:11:43 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d2819792e1f5dae390cd3b8397dde7d2326b4dff3dca1fc9f16878c3e20859`  
		Last Modified: Wed, 01 May 2024 22:11:46 GMT  
		Size: 52.6 MB (52554334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b625e284ea4a2d01f989692812ef596620a39cbee81472ae1bef2658cf763e0a`  
		Last Modified: Wed, 01 May 2024 22:11:43 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.28.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:33ea9a28e68a4d8e64aa08aa5a62112d681bac8ce9b5747226eccc918e960fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6298179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61eeab43ea66c2a4dac5836b654b89ac2b5f4a908cd26555763ddf273e06c80d`

```dockerfile
```

-	Layers:
	-	`sha256:5cfdd5b2a67aff315db5710bcf1f576549576fbaff5e3acd0d1f0e51fee174b9`  
		Last Modified: Wed, 01 May 2024 22:11:44 GMT  
		Size: 6.3 MB (6283493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0aac1728dcf2de80829a4bda1e3d33e130db6ac79b8f8b10599aaddb1ef0566`  
		Last Modified: Wed, 01 May 2024 22:11:43 GMT  
		Size: 14.7 KB (14686 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.28.5` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:53307d2e4c066b6dede63c2972a308b9f9b0d1b1107965263568c9ae3fa6099c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143823194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad5d7c38f7b4b4a57d5aab4117cad34db8a6396cdc16cb56e666ef4fda0dceb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.28.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4668ee134c6d27b158f31b1c01b5e92a02ede4c76d4b570eb243b76e7b7567bb`  
		Last Modified: Wed, 01 May 2024 22:33:11 GMT  
		Size: 18.9 MB (18870222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c26c91634d198f308ee466c4f2be3a59218fcaea48af76c19274245b1725a7`  
		Last Modified: Wed, 01 May 2024 22:33:10 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66655e7e968f4303965c9041a6153b0b67dc27163ac99e94b61cb44d5834c9a`  
		Last Modified: Wed, 01 May 2024 22:33:12 GMT  
		Size: 51.8 MB (51750427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e532d5b9e98e3a37b1cc0fb852f725db11b0bdfa5f4d9061b809597c40e5a5cc`  
		Last Modified: Wed, 01 May 2024 22:33:10 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.28.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:7c8b765831780ceb0518b17be95ed03fa2c21399556724961a45aa2a5836471e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6303365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ddfcf2407c453744ae94f32adde44875cbdbacf4c54566406df77e647641b2`

```dockerfile
```

-	Layers:
	-	`sha256:d3b6bd6c13bc9dc145844676689ce90b2ed45d3245fcd5c81b906fba6c55fca0`  
		Last Modified: Wed, 01 May 2024 22:33:11 GMT  
		Size: 6.3 MB (6288752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:069c30aaeb6f2134d59790bc0c2dbcbfb0d869f13e7f0cec58a2fd4f21e3aa14`  
		Last Modified: Wed, 01 May 2024 22:33:10 GMT  
		Size: 14.6 KB (14613 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.28.5-alpine`

```console
$ docker pull telegraf@sha256:8fd669183dc1c3318a5612082f7d657edf112848a5e70410c2021bbc63031e68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.28.5-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7cba338ca92016582121fde2c24898918febf9b3eef331c22c29e2f8ca5e5e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62942629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f059acd12fbc58dbbc090caa04773587136a367c7b9038c91d604fa0d589abdc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.28.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17fad2ec8d7d60600e220db6fb8a5e092ca32c368693c0658a03e82657f8f41`  
		Last Modified: Wed, 01 May 2024 21:52:37 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b6121a80388ea00a0dbc1c04c3650a718461a3474a433f5fb37884d4d7e77f`  
		Last Modified: Wed, 01 May 2024 21:52:37 GMT  
		Size: 2.6 MB (2618961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dca7bfce4c5b88479b37008b8413b1f013e39942858c4ce8075cd7e39128d15`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 56.9 MB (56914331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057993a88da0b4e296106809567dd40a6837a253e42133a2e5861393b8df00d4`  
		Last Modified: Wed, 01 May 2024 21:52:37 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.28.5-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:a6cd83c191df04acc472bac921a9bd5a195648f395d58b558f2398dbdfcdf787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1367687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a24b0ff68640e8c99a2abbf1cd5bc052692b1c93a9372dfbdbdf6727087c822`

```dockerfile
```

-	Layers:
	-	`sha256:623625e27493362e4a9a7bfb5662f501afd16533ce18b77a6c19fe101c1a8322`  
		Last Modified: Wed, 01 May 2024 21:52:37 GMT  
		Size: 1.4 MB (1352836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a1ceabb5a013e854d6cc531d83c7d0719cab24fbe7b9367f8a3fa5ff1de7add`  
		Last Modified: Wed, 01 May 2024 21:52:36 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.28.5-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:47131515785890df9e7611b8b18c91af39088507d7e90a40965d461d12762c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57639035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a758b54f0b137c4dd2c70a41ce6d228d3251e609289b5a868fd969bce41517db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.28.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddde0fe2ef8e41514be0d2d260ff46c7fa8adda5734b6aeb56e6ba0b174c9b1`  
		Last Modified: Wed, 01 May 2024 22:33:41 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfb31b2d6527f81d9d04ddd4779a6ecdac4257e8769d6d10af4516be1c7b4c2`  
		Last Modified: Wed, 01 May 2024 22:33:42 GMT  
		Size: 2.7 MB (2702917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8f68a26a0ad339eeb0d8c0bd2ecb4236e191446f574c1bd62d4a61902be54e`  
		Last Modified: Wed, 01 May 2024 22:33:43 GMT  
		Size: 51.6 MB (51587795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae51613913a2b1c01f5e6e504b461b87176212f06bda835aeaadd8c84925982f`  
		Last Modified: Wed, 01 May 2024 22:33:42 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.28.5-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e8dd4caf80fc50ab8f6a2b00d3480dab03f6c11296eb40ddf710f854ef045df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1364386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ada9c4e6609f50cdc288d4b6e180f9a36311d2fe6a9e5e9b2a6f6cbcf1be9c6`

```dockerfile
```

-	Layers:
	-	`sha256:ed5ed0ffd625ec269350925987b84eead74b7c903b47f9469183299084d1e2bf`  
		Last Modified: Wed, 01 May 2024 22:33:42 GMT  
		Size: 1.3 MB (1349696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:360a526294b33adab1b047d10b9f4917c63b5609857cbffd825795f383bd5e64`  
		Last Modified: Wed, 01 May 2024 22:33:42 GMT  
		Size: 14.7 KB (14690 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.29`

```console
$ docker pull telegraf@sha256:f7c5e03d565b0ce5754f5011c314dff54d4b8f52a99477ba01ee04d3f774a57f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.29` - linux; amd64

```console
$ docker pull telegraf@sha256:03ff03f20ffeb13bd15052fea8393357d316c12f0d3d8dfd5cfd767817811fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155219398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34950cc48e4249d1efe53ad593d81506f149cfbc2db1f831a9b127a172c83f94`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb18af3a724e3cf224127a83533de2686c1a4f5f9842e943bd7a288c2e11631`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 18.9 MB (18947990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307ca8195c9db3477da4e9d4424c85f1f0f590a7b800e61035c7539f809135e7`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3d4602b080c2f585af7f5b3788a3cadc620a559332fdbdaa4904fa65849d9a`  
		Last Modified: Tue, 14 May 2024 03:58:11 GMT  
		Size: 62.6 MB (62642512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11091066be848f94bc4eeeabc2e81d0838e8efd324e1b578bd06b671d975f71`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:88010e4986fa4a60576e0697c79e5d6891cd9566683f5687b85b4a4e54b6ad8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595ada0f0c20a6d0f1b443672f95ac5a275cce2c9b987ba2560e1d448e760549`

```dockerfile
```

-	Layers:
	-	`sha256:18201db310e1d93bdab1da759dfe4e5d115c99221fc41df4e8b9ae643dbec959`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 6.3 MB (6299203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018ac014087ac4ae92459a75eca9fdbdf103dc0d7425f1eb3b8035bde38d8a28`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 14.6 KB (14607 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:1ba1b1f6dab3e9fd3b4b866694e0bb3cb32165b83cfe99f28bb36a20922950a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142841296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac07340d832f721358a552b37c19d2f5ca409ff0a5e931e924ef26e026e2049`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342c7577918dea746df9c5fbcb51b929d73f1915b3c0e7723a4aad3ca148c343`  
		Last Modified: Wed, 01 May 2024 22:11:44 GMT  
		Size: 17.7 MB (17724944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b7f4d906aeb5335da996f149e84e5db08b1905e7ceb937cca7a8c9ac360ede`  
		Last Modified: Wed, 01 May 2024 22:11:43 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500eef39529a52e4ac78761e2903513c87c7da1b4d78b7a417c832eda58e1a94`  
		Last Modified: Wed, 01 May 2024 22:12:38 GMT  
		Size: 58.0 MB (57984981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5d535b243ceda9cf756083c9b255293da60fc3487aa4b7ed49b6dac3f48a38`  
		Last Modified: Wed, 01 May 2024 22:12:36 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:713f4ebddb9a8b5768ec894a703376766b2759ced35bd50336109c62c59c9502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6308911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc094dc33a72c90ffcb2d100321275b03487b3c60074fb64f07c84042a5f434`

```dockerfile
```

-	Layers:
	-	`sha256:805012f53d872b64f6da953dc1ff412d9985cc963009559cdbfbc47a9b731a65`  
		Last Modified: Wed, 01 May 2024 22:12:36 GMT  
		Size: 6.3 MB (6294557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e8d298b2400b4b7c4a270ec79f8d94c97b1df8185efab67f9a1fbc70c6031f`  
		Last Modified: Wed, 01 May 2024 22:12:36 GMT  
		Size: 14.4 KB (14354 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a1ebb58d69ed9e256c9097e969bea3bc59f6e81406febdbac0882d3280436dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149053897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50d4f104dff51f840688163d12105b22775096df83f3a67693e6cbab8548787`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4668ee134c6d27b158f31b1c01b5e92a02ede4c76d4b570eb243b76e7b7567bb`  
		Last Modified: Wed, 01 May 2024 22:33:11 GMT  
		Size: 18.9 MB (18870222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c26c91634d198f308ee466c4f2be3a59218fcaea48af76c19274245b1725a7`  
		Last Modified: Wed, 01 May 2024 22:33:10 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d3eba0c019a8b7104a0fd9391ab3e1e9d62d1e4d1662b7078bb592847ea53a`  
		Last Modified: Wed, 01 May 2024 22:34:22 GMT  
		Size: 57.0 MB (56981131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186dafe70c25f7000da8dc51f42e15236a4e251b7f1dd44f6d2b55b717901462`  
		Last Modified: Wed, 01 May 2024 22:34:20 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:2af84ef18d84e114cad9a10fbeea5c4113075d3da694e9c68351ac2fa184b9e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba35d9077ae401b88972ce9fba278ff6c863e4f50332bfae12b9ad64a9eee774`

```dockerfile
```

-	Layers:
	-	`sha256:24e82876b4799e1332e0127d5d5c631c1bbd38f899762736e51a316ac62ad310`  
		Last Modified: Wed, 01 May 2024 22:34:20 GMT  
		Size: 6.3 MB (6299816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e48b1593fba9628f0cbd516132b53132d6d9bdae3f6ae5df2fbac99069e8335`  
		Last Modified: Wed, 01 May 2024 22:34:20 GMT  
		Size: 14.3 KB (14281 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.29-alpine`

```console
$ docker pull telegraf@sha256:0e4bd174d340f3058ff29f2197d89bd3c9eed5fb07e69da9c33046270d2c3adb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.29-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:29830a51d9174ec4932b0f32a44c2a5696271e572402a2b9308dbc0d876a3062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68485548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae49ea2b894a59d0baa970122b87381c7f5c647bd92a0d30eff9eda1bdc3c0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66916d60fd220360ccf9f8ce7c7629a0f7b9c16e56dc879ed453c020a7ff8c8`  
		Last Modified: Wed, 01 May 2024 21:52:33 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d681b89e78ca35ddd5dac78bea950a4dc933fb18f3662365cddc94efe62c17d`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 2.6 MB (2618968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e43ef88a1d8ac6699e940f1bb502a106c9c69dd61ec39064283029b3990893`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 62.5 MB (62457243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe64437110d2f0ec023235c3c2dbfa922dd2bc68f5b44c199bac1f117dbd382`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:31bd3022d8ca6189b92fdf28380fa9874d03bbd4ae130bfd243d7d94dabb0fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1380050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7b478da9edb82e9bba1762e22889f93d651c3b5c92bead224c6c8f9606f580`

```dockerfile
```

-	Layers:
	-	`sha256:808603a313dac867ddc4e10685e3da7916e6c936ac48e56a978a915db7b2e4a1`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 1.4 MB (1365200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c54cd2d4e7c728b5246c616629df51baac071e16bef995e8ee8a0cc4e6b02d`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 14.8 KB (14850 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:008197f6b39fe8b7e4e013e8574523e8cda2be226f7449cdc21ae45cc96e38c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62849729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bc39888daf763e890d415946b487839e389683b7796d00c03ac3ccc5748287`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddde0fe2ef8e41514be0d2d260ff46c7fa8adda5734b6aeb56e6ba0b174c9b1`  
		Last Modified: Wed, 01 May 2024 22:33:41 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfb31b2d6527f81d9d04ddd4779a6ecdac4257e8769d6d10af4516be1c7b4c2`  
		Last Modified: Wed, 01 May 2024 22:33:42 GMT  
		Size: 2.7 MB (2702917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3254b71ee2dea015969e2c70ba06e521a4b4a8e66936d7d30eb4ad716ec2d81`  
		Last Modified: Wed, 01 May 2024 22:34:57 GMT  
		Size: 56.8 MB (56798489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e47e8478949e8acbaeeb3374a1fe9cb324fe86a25bcdade81a0b694dfaee7b`  
		Last Modified: Wed, 01 May 2024 22:34:56 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c8c312ea591a35828406adca49789bc0c872ba3256226303d289ce0c5b62160e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1375450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d06fd9a6199d3e70d2c201f8e8db94b36694f4dbb05aa873ff0e720fa9f9d01`

```dockerfile
```

-	Layers:
	-	`sha256:79da5a86dca22346c1dfc562e88f1d5dd2c719a261768ce63c0b0f8b80686c3a`  
		Last Modified: Wed, 01 May 2024 22:34:56 GMT  
		Size: 1.4 MB (1360760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8470e678dcf0a7858cf8713ddcaf2a7e4da81c32b23a55f2aeed8b51301b287`  
		Last Modified: Wed, 01 May 2024 22:34:55 GMT  
		Size: 14.7 KB (14690 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.29.5`

```console
$ docker pull telegraf@sha256:f7c5e03d565b0ce5754f5011c314dff54d4b8f52a99477ba01ee04d3f774a57f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.29.5` - linux; amd64

```console
$ docker pull telegraf@sha256:03ff03f20ffeb13bd15052fea8393357d316c12f0d3d8dfd5cfd767817811fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155219398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34950cc48e4249d1efe53ad593d81506f149cfbc2db1f831a9b127a172c83f94`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb18af3a724e3cf224127a83533de2686c1a4f5f9842e943bd7a288c2e11631`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 18.9 MB (18947990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307ca8195c9db3477da4e9d4424c85f1f0f590a7b800e61035c7539f809135e7`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3d4602b080c2f585af7f5b3788a3cadc620a559332fdbdaa4904fa65849d9a`  
		Last Modified: Tue, 14 May 2024 03:58:11 GMT  
		Size: 62.6 MB (62642512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11091066be848f94bc4eeeabc2e81d0838e8efd324e1b578bd06b671d975f71`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:88010e4986fa4a60576e0697c79e5d6891cd9566683f5687b85b4a4e54b6ad8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595ada0f0c20a6d0f1b443672f95ac5a275cce2c9b987ba2560e1d448e760549`

```dockerfile
```

-	Layers:
	-	`sha256:18201db310e1d93bdab1da759dfe4e5d115c99221fc41df4e8b9ae643dbec959`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 6.3 MB (6299203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018ac014087ac4ae92459a75eca9fdbdf103dc0d7425f1eb3b8035bde38d8a28`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 14.6 KB (14607 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29.5` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:1ba1b1f6dab3e9fd3b4b866694e0bb3cb32165b83cfe99f28bb36a20922950a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142841296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac07340d832f721358a552b37c19d2f5ca409ff0a5e931e924ef26e026e2049`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342c7577918dea746df9c5fbcb51b929d73f1915b3c0e7723a4aad3ca148c343`  
		Last Modified: Wed, 01 May 2024 22:11:44 GMT  
		Size: 17.7 MB (17724944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b7f4d906aeb5335da996f149e84e5db08b1905e7ceb937cca7a8c9ac360ede`  
		Last Modified: Wed, 01 May 2024 22:11:43 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500eef39529a52e4ac78761e2903513c87c7da1b4d78b7a417c832eda58e1a94`  
		Last Modified: Wed, 01 May 2024 22:12:38 GMT  
		Size: 58.0 MB (57984981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5d535b243ceda9cf756083c9b255293da60fc3487aa4b7ed49b6dac3f48a38`  
		Last Modified: Wed, 01 May 2024 22:12:36 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:713f4ebddb9a8b5768ec894a703376766b2759ced35bd50336109c62c59c9502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6308911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc094dc33a72c90ffcb2d100321275b03487b3c60074fb64f07c84042a5f434`

```dockerfile
```

-	Layers:
	-	`sha256:805012f53d872b64f6da953dc1ff412d9985cc963009559cdbfbc47a9b731a65`  
		Last Modified: Wed, 01 May 2024 22:12:36 GMT  
		Size: 6.3 MB (6294557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e8d298b2400b4b7c4a270ec79f8d94c97b1df8185efab67f9a1fbc70c6031f`  
		Last Modified: Wed, 01 May 2024 22:12:36 GMT  
		Size: 14.4 KB (14354 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29.5` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a1ebb58d69ed9e256c9097e969bea3bc59f6e81406febdbac0882d3280436dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149053897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50d4f104dff51f840688163d12105b22775096df83f3a67693e6cbab8548787`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4668ee134c6d27b158f31b1c01b5e92a02ede4c76d4b570eb243b76e7b7567bb`  
		Last Modified: Wed, 01 May 2024 22:33:11 GMT  
		Size: 18.9 MB (18870222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c26c91634d198f308ee466c4f2be3a59218fcaea48af76c19274245b1725a7`  
		Last Modified: Wed, 01 May 2024 22:33:10 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d3eba0c019a8b7104a0fd9391ab3e1e9d62d1e4d1662b7078bb592847ea53a`  
		Last Modified: Wed, 01 May 2024 22:34:22 GMT  
		Size: 57.0 MB (56981131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186dafe70c25f7000da8dc51f42e15236a4e251b7f1dd44f6d2b55b717901462`  
		Last Modified: Wed, 01 May 2024 22:34:20 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:2af84ef18d84e114cad9a10fbeea5c4113075d3da694e9c68351ac2fa184b9e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba35d9077ae401b88972ce9fba278ff6c863e4f50332bfae12b9ad64a9eee774`

```dockerfile
```

-	Layers:
	-	`sha256:24e82876b4799e1332e0127d5d5c631c1bbd38f899762736e51a316ac62ad310`  
		Last Modified: Wed, 01 May 2024 22:34:20 GMT  
		Size: 6.3 MB (6299816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e48b1593fba9628f0cbd516132b53132d6d9bdae3f6ae5df2fbac99069e8335`  
		Last Modified: Wed, 01 May 2024 22:34:20 GMT  
		Size: 14.3 KB (14281 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.29.5-alpine`

```console
$ docker pull telegraf@sha256:0e4bd174d340f3058ff29f2197d89bd3c9eed5fb07e69da9c33046270d2c3adb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.29.5-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:29830a51d9174ec4932b0f32a44c2a5696271e572402a2b9308dbc0d876a3062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68485548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae49ea2b894a59d0baa970122b87381c7f5c647bd92a0d30eff9eda1bdc3c0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66916d60fd220360ccf9f8ce7c7629a0f7b9c16e56dc879ed453c020a7ff8c8`  
		Last Modified: Wed, 01 May 2024 21:52:33 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d681b89e78ca35ddd5dac78bea950a4dc933fb18f3662365cddc94efe62c17d`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 2.6 MB (2618968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e43ef88a1d8ac6699e940f1bb502a106c9c69dd61ec39064283029b3990893`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 62.5 MB (62457243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe64437110d2f0ec023235c3c2dbfa922dd2bc68f5b44c199bac1f117dbd382`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:31bd3022d8ca6189b92fdf28380fa9874d03bbd4ae130bfd243d7d94dabb0fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1380050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7b478da9edb82e9bba1762e22889f93d651c3b5c92bead224c6c8f9606f580`

```dockerfile
```

-	Layers:
	-	`sha256:808603a313dac867ddc4e10685e3da7916e6c936ac48e56a978a915db7b2e4a1`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 1.4 MB (1365200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c54cd2d4e7c728b5246c616629df51baac071e16bef995e8ee8a0cc4e6b02d`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 14.8 KB (14850 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29.5-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:008197f6b39fe8b7e4e013e8574523e8cda2be226f7449cdc21ae45cc96e38c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62849729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bc39888daf763e890d415946b487839e389683b7796d00c03ac3ccc5748287`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddde0fe2ef8e41514be0d2d260ff46c7fa8adda5734b6aeb56e6ba0b174c9b1`  
		Last Modified: Wed, 01 May 2024 22:33:41 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfb31b2d6527f81d9d04ddd4779a6ecdac4257e8769d6d10af4516be1c7b4c2`  
		Last Modified: Wed, 01 May 2024 22:33:42 GMT  
		Size: 2.7 MB (2702917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3254b71ee2dea015969e2c70ba06e521a4b4a8e66936d7d30eb4ad716ec2d81`  
		Last Modified: Wed, 01 May 2024 22:34:57 GMT  
		Size: 56.8 MB (56798489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e47e8478949e8acbaeeb3374a1fe9cb324fe86a25bcdade81a0b694dfaee7b`  
		Last Modified: Wed, 01 May 2024 22:34:56 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c8c312ea591a35828406adca49789bc0c872ba3256226303d289ce0c5b62160e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1375450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d06fd9a6199d3e70d2c201f8e8db94b36694f4dbb05aa873ff0e720fa9f9d01`

```dockerfile
```

-	Layers:
	-	`sha256:79da5a86dca22346c1dfc562e88f1d5dd2c719a261768ce63c0b0f8b80686c3a`  
		Last Modified: Wed, 01 May 2024 22:34:56 GMT  
		Size: 1.4 MB (1360760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8470e678dcf0a7858cf8713ddcaf2a7e4da81c32b23a55f2aeed8b51301b287`  
		Last Modified: Wed, 01 May 2024 22:34:55 GMT  
		Size: 14.7 KB (14690 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30`

```console
$ docker pull telegraf@sha256:062455b2e39324ec791168c4a82ef825936551c62b6e52e61f2ce0683f78b8a6
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
$ docker pull telegraf@sha256:e396e6b0fc235d80c69a2737e6d303c8178034c19d935fa4646cb143b99c22b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154599417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1463988fb9ac4d7f92622e154f20a430349ceb8e9d80ad5c6c7480e42586e3eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76047489d0b2ccdc4598bd413a2f7f8cddf3685229a8c8d2dfea4e28147e471`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 18.9 MB (18948018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c013e6ebce0fe5838f78b11b747a7ae2fffa092cdee0749609bfac6ae129058b`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049270f6c151d3bd1e976b0ca9a6d3aaabe9c2cb5ca253cb53edfb086182ecfb`  
		Last Modified: Tue, 14 May 2024 03:58:26 GMT  
		Size: 62.0 MB (62022501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1cf419edd6c5b8dc261f09c429795709ae8ec676035b9432f2635a6aa7a94a`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:82aaf3de49fedf1eb53867ae333b120a5baebce276115a08001a49cb66e0ec6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6312805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeeb6e6fe095a30e3ff49b6266c69beaa7f85fc9dd7290d1eef8c3bc33da59af`

```dockerfile
```

-	Layers:
	-	`sha256:b2533c5a707801d71bd284a7fabafe70b0371175da6b354e741a5f639fe0f9d7`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 6.3 MB (6297897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6d8718e9191bd392eb11b4485e6e87d2741437935af64356b66f9dd76f93338`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 14.9 KB (14908 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:b42974d2147951e1891eebf7cde1ed5597982d8bd389f5ed1f814683f546e655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142268061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1542ae530a1a2ff3497adb860e8cdf08ed73d23eb4e30c1208b72c73d5b8369`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342c7577918dea746df9c5fbcb51b929d73f1915b3c0e7723a4aad3ca148c343`  
		Last Modified: Wed, 01 May 2024 22:11:44 GMT  
		Size: 17.7 MB (17724944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b7f4d906aeb5335da996f149e84e5db08b1905e7ceb937cca7a8c9ac360ede`  
		Last Modified: Wed, 01 May 2024 22:11:43 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1702d62770944a6a6088dba2d4c1f99350f12e6de561f4a2c08d3e1aa5020d48`  
		Last Modified: Wed, 01 May 2024 22:13:32 GMT  
		Size: 57.4 MB (57411744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46965f9978bfadf9724ce2d3cae10baafa08d0de0b2ee52a4775ffa2f4eab101`  
		Last Modified: Wed, 01 May 2024 22:13:30 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:0fff7c5047b86c2c9bcbb6f021523fce3406e9ff778b675c6a8e01225a0a7330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6307923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df2fc033378f3acbac8f2ba1051996e57a489a90d9400aac223906579d204fd`

```dockerfile
```

-	Layers:
	-	`sha256:c5eed3c367c698de5243e012e512e93bcfb073261fb1c1f1360df30e47f9d627`  
		Last Modified: Wed, 01 May 2024 22:13:31 GMT  
		Size: 6.3 MB (6293259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b16eeec4048d39e68a41a306fd267533f6a0a2023c6016075e3b8a046c66407b`  
		Last Modified: Wed, 01 May 2024 22:13:30 GMT  
		Size: 14.7 KB (14664 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:77fc16f95036dec5f73c379d0c0b083133115e496bbb88a12c997eb1f812236c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148491545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ccc7cd3d68e411ff5e323927fa7376edd2b1648d5c01cde611bf7867da8b7b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4668ee134c6d27b158f31b1c01b5e92a02ede4c76d4b570eb243b76e7b7567bb`  
		Last Modified: Wed, 01 May 2024 22:33:11 GMT  
		Size: 18.9 MB (18870222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c26c91634d198f308ee466c4f2be3a59218fcaea48af76c19274245b1725a7`  
		Last Modified: Wed, 01 May 2024 22:33:10 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b65e3ef18a3b059c80d045b010aabe08d82d2c8504bb9b8d1e1cf28bea72b2`  
		Last Modified: Wed, 01 May 2024 22:35:35 GMT  
		Size: 56.4 MB (56418780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad2f9c46f3a11a31992befffc6b5533b6d86ea19882447a48448e2b936ba85`  
		Last Modified: Wed, 01 May 2024 22:35:33 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:336bbf80fe6a5d81fa90823a3663f5d4c6c6e5dfd4ff920a21fc0aa478942a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459f674c96e863832e3ed1390d07e3512fb7d49e6f01921a45497fba22864859`

```dockerfile
```

-	Layers:
	-	`sha256:ea9fc20d24af05be6bdcb3ece4c941918547a8353f7dc1d6e4b2554b0c58f7c8`  
		Last Modified: Wed, 01 May 2024 22:35:34 GMT  
		Size: 6.3 MB (6298512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43457d5c0f51f13681689d84eb3e643c3585306ba9c420ce87c401c054e78678`  
		Last Modified: Wed, 01 May 2024 22:35:33 GMT  
		Size: 14.6 KB (14584 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30-alpine`

```console
$ docker pull telegraf@sha256:f2808a1044967e05dc445dafb8961e16eeee4c7bcf3058e2869b8f3807645296
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:9146f72f04f7f6e2f66701330f8390aadd0054135f080b9b8fe2f3054cc9ac65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67866168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4874d28f9fa9094efdb1a230a3cdbe72ea46cb511aa94532136a5a213740cc07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9a15b3cf38e972d8a3f4e8af5d2c1f6e13775b0850fccf6e657d52cdfdf17e`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f738a4fef09827a9a9ed60b19f0fcaf16dea016921cf1151f7c2b01d0e4a6922`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 2.6 MB (2618975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7971ef61f150929f6915edddea3fef842e0ec742677d7b571e7300e51b251901`  
		Last Modified: Wed, 01 May 2024 21:52:50 GMT  
		Size: 61.8 MB (61837858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7efac562f2d6ac9cf8225ac8738a7a0f63124f076c0499b4cfad504f5031a40`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:99e30b4531b1bec3058b912cb6920a2da86af289603604078248f182ca7e8efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1379047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48e2e29db45e233fb3ffd2c72ea7265b6e213045042f81673e1230c1eeab98b`

```dockerfile
```

-	Layers:
	-	`sha256:378a3eceeef212f3b574308cb08aef9454ce753e285b8f15341c85bea781057e`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 1.4 MB (1363894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ead833acfae8cb7889259e87845134177e75b09e6a99570501e8990fd8d2f3f`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 15.2 KB (15153 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3e6ab2d201f1bd8b754506a5e5cffca613231e740330a47e8ddf52caf7958d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62286279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a2615c97a0324d780b97392e60d91a0884f585e24946cd8069771a14acfc2f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddde0fe2ef8e41514be0d2d260ff46c7fa8adda5734b6aeb56e6ba0b174c9b1`  
		Last Modified: Wed, 01 May 2024 22:33:41 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfb31b2d6527f81d9d04ddd4779a6ecdac4257e8769d6d10af4516be1c7b4c2`  
		Last Modified: Wed, 01 May 2024 22:33:42 GMT  
		Size: 2.7 MB (2702917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712cc35fce9c674cb0ce5c7facedc85de98ef7741faf3c67f91e62c822f5bfdb`  
		Last Modified: Wed, 01 May 2024 22:36:07 GMT  
		Size: 56.2 MB (56235042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fae45a5cce61f30b5c8c11bd26d498b5f5cd19a149af7762db218eb3a78571`  
		Last Modified: Wed, 01 May 2024 22:36:05 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:98fcd18a30d44deb01590a4573864149bb153d9f18908a73f874f1f2faebd6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1374451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ede174ca750f136c7744b8e5b405ba9d29463d422e9dfb5113d517b73a7bd5`

```dockerfile
```

-	Layers:
	-	`sha256:d9ee1f5137f9facdb00f08134b62e511a3fd511640332797e5ebca10b73644c1`  
		Last Modified: Wed, 01 May 2024 22:36:05 GMT  
		Size: 1.4 MB (1359456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9177c267b51bee1bfcdba7e7fc8571004c7ceb643d13703dbafd4c7d2f6721f4`  
		Last Modified: Wed, 01 May 2024 22:36:05 GMT  
		Size: 15.0 KB (14995 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30.2`

```console
$ docker pull telegraf@sha256:062455b2e39324ec791168c4a82ef825936551c62b6e52e61f2ce0683f78b8a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30.2` - linux; amd64

```console
$ docker pull telegraf@sha256:e396e6b0fc235d80c69a2737e6d303c8178034c19d935fa4646cb143b99c22b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154599417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1463988fb9ac4d7f92622e154f20a430349ceb8e9d80ad5c6c7480e42586e3eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76047489d0b2ccdc4598bd413a2f7f8cddf3685229a8c8d2dfea4e28147e471`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 18.9 MB (18948018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c013e6ebce0fe5838f78b11b747a7ae2fffa092cdee0749609bfac6ae129058b`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049270f6c151d3bd1e976b0ca9a6d3aaabe9c2cb5ca253cb53edfb086182ecfb`  
		Last Modified: Tue, 14 May 2024 03:58:26 GMT  
		Size: 62.0 MB (62022501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1cf419edd6c5b8dc261f09c429795709ae8ec676035b9432f2635a6aa7a94a`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:82aaf3de49fedf1eb53867ae333b120a5baebce276115a08001a49cb66e0ec6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6312805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeeb6e6fe095a30e3ff49b6266c69beaa7f85fc9dd7290d1eef8c3bc33da59af`

```dockerfile
```

-	Layers:
	-	`sha256:b2533c5a707801d71bd284a7fabafe70b0371175da6b354e741a5f639fe0f9d7`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 6.3 MB (6297897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6d8718e9191bd392eb11b4485e6e87d2741437935af64356b66f9dd76f93338`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 14.9 KB (14908 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.2` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:b42974d2147951e1891eebf7cde1ed5597982d8bd389f5ed1f814683f546e655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142268061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1542ae530a1a2ff3497adb860e8cdf08ed73d23eb4e30c1208b72c73d5b8369`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342c7577918dea746df9c5fbcb51b929d73f1915b3c0e7723a4aad3ca148c343`  
		Last Modified: Wed, 01 May 2024 22:11:44 GMT  
		Size: 17.7 MB (17724944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b7f4d906aeb5335da996f149e84e5db08b1905e7ceb937cca7a8c9ac360ede`  
		Last Modified: Wed, 01 May 2024 22:11:43 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1702d62770944a6a6088dba2d4c1f99350f12e6de561f4a2c08d3e1aa5020d48`  
		Last Modified: Wed, 01 May 2024 22:13:32 GMT  
		Size: 57.4 MB (57411744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46965f9978bfadf9724ce2d3cae10baafa08d0de0b2ee52a4775ffa2f4eab101`  
		Last Modified: Wed, 01 May 2024 22:13:30 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:0fff7c5047b86c2c9bcbb6f021523fce3406e9ff778b675c6a8e01225a0a7330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6307923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df2fc033378f3acbac8f2ba1051996e57a489a90d9400aac223906579d204fd`

```dockerfile
```

-	Layers:
	-	`sha256:c5eed3c367c698de5243e012e512e93bcfb073261fb1c1f1360df30e47f9d627`  
		Last Modified: Wed, 01 May 2024 22:13:31 GMT  
		Size: 6.3 MB (6293259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b16eeec4048d39e68a41a306fd267533f6a0a2023c6016075e3b8a046c66407b`  
		Last Modified: Wed, 01 May 2024 22:13:30 GMT  
		Size: 14.7 KB (14664 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.2` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:77fc16f95036dec5f73c379d0c0b083133115e496bbb88a12c997eb1f812236c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148491545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ccc7cd3d68e411ff5e323927fa7376edd2b1648d5c01cde611bf7867da8b7b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4668ee134c6d27b158f31b1c01b5e92a02ede4c76d4b570eb243b76e7b7567bb`  
		Last Modified: Wed, 01 May 2024 22:33:11 GMT  
		Size: 18.9 MB (18870222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c26c91634d198f308ee466c4f2be3a59218fcaea48af76c19274245b1725a7`  
		Last Modified: Wed, 01 May 2024 22:33:10 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b65e3ef18a3b059c80d045b010aabe08d82d2c8504bb9b8d1e1cf28bea72b2`  
		Last Modified: Wed, 01 May 2024 22:35:35 GMT  
		Size: 56.4 MB (56418780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad2f9c46f3a11a31992befffc6b5533b6d86ea19882447a48448e2b936ba85`  
		Last Modified: Wed, 01 May 2024 22:35:33 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:336bbf80fe6a5d81fa90823a3663f5d4c6c6e5dfd4ff920a21fc0aa478942a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459f674c96e863832e3ed1390d07e3512fb7d49e6f01921a45497fba22864859`

```dockerfile
```

-	Layers:
	-	`sha256:ea9fc20d24af05be6bdcb3ece4c941918547a8353f7dc1d6e4b2554b0c58f7c8`  
		Last Modified: Wed, 01 May 2024 22:35:34 GMT  
		Size: 6.3 MB (6298512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43457d5c0f51f13681689d84eb3e643c3585306ba9c420ce87c401c054e78678`  
		Last Modified: Wed, 01 May 2024 22:35:33 GMT  
		Size: 14.6 KB (14584 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30.2-alpine`

```console
$ docker pull telegraf@sha256:f2808a1044967e05dc445dafb8961e16eeee4c7bcf3058e2869b8f3807645296
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30.2-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:9146f72f04f7f6e2f66701330f8390aadd0054135f080b9b8fe2f3054cc9ac65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67866168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4874d28f9fa9094efdb1a230a3cdbe72ea46cb511aa94532136a5a213740cc07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9a15b3cf38e972d8a3f4e8af5d2c1f6e13775b0850fccf6e657d52cdfdf17e`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f738a4fef09827a9a9ed60b19f0fcaf16dea016921cf1151f7c2b01d0e4a6922`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 2.6 MB (2618975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7971ef61f150929f6915edddea3fef842e0ec742677d7b571e7300e51b251901`  
		Last Modified: Wed, 01 May 2024 21:52:50 GMT  
		Size: 61.8 MB (61837858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7efac562f2d6ac9cf8225ac8738a7a0f63124f076c0499b4cfad504f5031a40`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.2-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:99e30b4531b1bec3058b912cb6920a2da86af289603604078248f182ca7e8efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1379047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48e2e29db45e233fb3ffd2c72ea7265b6e213045042f81673e1230c1eeab98b`

```dockerfile
```

-	Layers:
	-	`sha256:378a3eceeef212f3b574308cb08aef9454ce753e285b8f15341c85bea781057e`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 1.4 MB (1363894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ead833acfae8cb7889259e87845134177e75b09e6a99570501e8990fd8d2f3f`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 15.2 KB (15153 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.2-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3e6ab2d201f1bd8b754506a5e5cffca613231e740330a47e8ddf52caf7958d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62286279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a2615c97a0324d780b97392e60d91a0884f585e24946cd8069771a14acfc2f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddde0fe2ef8e41514be0d2d260ff46c7fa8adda5734b6aeb56e6ba0b174c9b1`  
		Last Modified: Wed, 01 May 2024 22:33:41 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfb31b2d6527f81d9d04ddd4779a6ecdac4257e8769d6d10af4516be1c7b4c2`  
		Last Modified: Wed, 01 May 2024 22:33:42 GMT  
		Size: 2.7 MB (2702917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712cc35fce9c674cb0ce5c7facedc85de98ef7741faf3c67f91e62c822f5bfdb`  
		Last Modified: Wed, 01 May 2024 22:36:07 GMT  
		Size: 56.2 MB (56235042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fae45a5cce61f30b5c8c11bd26d498b5f5cd19a149af7762db218eb3a78571`  
		Last Modified: Wed, 01 May 2024 22:36:05 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.2-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:98fcd18a30d44deb01590a4573864149bb153d9f18908a73f874f1f2faebd6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1374451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ede174ca750f136c7744b8e5b405ba9d29463d422e9dfb5113d517b73a7bd5`

```dockerfile
```

-	Layers:
	-	`sha256:d9ee1f5137f9facdb00f08134b62e511a3fd511640332797e5ebca10b73644c1`  
		Last Modified: Wed, 01 May 2024 22:36:05 GMT  
		Size: 1.4 MB (1359456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9177c267b51bee1bfcdba7e7fc8571004c7ceb643d13703dbafd4c7d2f6721f4`  
		Last Modified: Wed, 01 May 2024 22:36:05 GMT  
		Size: 15.0 KB (14995 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:f2808a1044967e05dc445dafb8961e16eeee4c7bcf3058e2869b8f3807645296
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:9146f72f04f7f6e2f66701330f8390aadd0054135f080b9b8fe2f3054cc9ac65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67866168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4874d28f9fa9094efdb1a230a3cdbe72ea46cb511aa94532136a5a213740cc07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9a15b3cf38e972d8a3f4e8af5d2c1f6e13775b0850fccf6e657d52cdfdf17e`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f738a4fef09827a9a9ed60b19f0fcaf16dea016921cf1151f7c2b01d0e4a6922`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 2.6 MB (2618975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7971ef61f150929f6915edddea3fef842e0ec742677d7b571e7300e51b251901`  
		Last Modified: Wed, 01 May 2024 21:52:50 GMT  
		Size: 61.8 MB (61837858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7efac562f2d6ac9cf8225ac8738a7a0f63124f076c0499b4cfad504f5031a40`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:99e30b4531b1bec3058b912cb6920a2da86af289603604078248f182ca7e8efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1379047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48e2e29db45e233fb3ffd2c72ea7265b6e213045042f81673e1230c1eeab98b`

```dockerfile
```

-	Layers:
	-	`sha256:378a3eceeef212f3b574308cb08aef9454ce753e285b8f15341c85bea781057e`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 1.4 MB (1363894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ead833acfae8cb7889259e87845134177e75b09e6a99570501e8990fd8d2f3f`  
		Last Modified: Wed, 01 May 2024 21:52:48 GMT  
		Size: 15.2 KB (15153 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3e6ab2d201f1bd8b754506a5e5cffca613231e740330a47e8ddf52caf7958d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62286279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a2615c97a0324d780b97392e60d91a0884f585e24946cd8069771a14acfc2f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddde0fe2ef8e41514be0d2d260ff46c7fa8adda5734b6aeb56e6ba0b174c9b1`  
		Last Modified: Wed, 01 May 2024 22:33:41 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfb31b2d6527f81d9d04ddd4779a6ecdac4257e8769d6d10af4516be1c7b4c2`  
		Last Modified: Wed, 01 May 2024 22:33:42 GMT  
		Size: 2.7 MB (2702917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712cc35fce9c674cb0ce5c7facedc85de98ef7741faf3c67f91e62c822f5bfdb`  
		Last Modified: Wed, 01 May 2024 22:36:07 GMT  
		Size: 56.2 MB (56235042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fae45a5cce61f30b5c8c11bd26d498b5f5cd19a149af7762db218eb3a78571`  
		Last Modified: Wed, 01 May 2024 22:36:05 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:98fcd18a30d44deb01590a4573864149bb153d9f18908a73f874f1f2faebd6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1374451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ede174ca750f136c7744b8e5b405ba9d29463d422e9dfb5113d517b73a7bd5`

```dockerfile
```

-	Layers:
	-	`sha256:d9ee1f5137f9facdb00f08134b62e511a3fd511640332797e5ebca10b73644c1`  
		Last Modified: Wed, 01 May 2024 22:36:05 GMT  
		Size: 1.4 MB (1359456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9177c267b51bee1bfcdba7e7fc8571004c7ceb643d13703dbafd4c7d2f6721f4`  
		Last Modified: Wed, 01 May 2024 22:36:05 GMT  
		Size: 15.0 KB (14995 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:062455b2e39324ec791168c4a82ef825936551c62b6e52e61f2ce0683f78b8a6
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
$ docker pull telegraf@sha256:e396e6b0fc235d80c69a2737e6d303c8178034c19d935fa4646cb143b99c22b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154599417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1463988fb9ac4d7f92622e154f20a430349ceb8e9d80ad5c6c7480e42586e3eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76047489d0b2ccdc4598bd413a2f7f8cddf3685229a8c8d2dfea4e28147e471`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 18.9 MB (18948018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c013e6ebce0fe5838f78b11b747a7ae2fffa092cdee0749609bfac6ae129058b`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049270f6c151d3bd1e976b0ca9a6d3aaabe9c2cb5ca253cb53edfb086182ecfb`  
		Last Modified: Tue, 14 May 2024 03:58:26 GMT  
		Size: 62.0 MB (62022501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1cf419edd6c5b8dc261f09c429795709ae8ec676035b9432f2635a6aa7a94a`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:82aaf3de49fedf1eb53867ae333b120a5baebce276115a08001a49cb66e0ec6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6312805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeeb6e6fe095a30e3ff49b6266c69beaa7f85fc9dd7290d1eef8c3bc33da59af`

```dockerfile
```

-	Layers:
	-	`sha256:b2533c5a707801d71bd284a7fabafe70b0371175da6b354e741a5f639fe0f9d7`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 6.3 MB (6297897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6d8718e9191bd392eb11b4485e6e87d2741437935af64356b66f9dd76f93338`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 14.9 KB (14908 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:b42974d2147951e1891eebf7cde1ed5597982d8bd389f5ed1f814683f546e655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142268061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1542ae530a1a2ff3497adb860e8cdf08ed73d23eb4e30c1208b72c73d5b8369`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342c7577918dea746df9c5fbcb51b929d73f1915b3c0e7723a4aad3ca148c343`  
		Last Modified: Wed, 01 May 2024 22:11:44 GMT  
		Size: 17.7 MB (17724944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b7f4d906aeb5335da996f149e84e5db08b1905e7ceb937cca7a8c9ac360ede`  
		Last Modified: Wed, 01 May 2024 22:11:43 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1702d62770944a6a6088dba2d4c1f99350f12e6de561f4a2c08d3e1aa5020d48`  
		Last Modified: Wed, 01 May 2024 22:13:32 GMT  
		Size: 57.4 MB (57411744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46965f9978bfadf9724ce2d3cae10baafa08d0de0b2ee52a4775ffa2f4eab101`  
		Last Modified: Wed, 01 May 2024 22:13:30 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:0fff7c5047b86c2c9bcbb6f021523fce3406e9ff778b675c6a8e01225a0a7330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6307923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df2fc033378f3acbac8f2ba1051996e57a489a90d9400aac223906579d204fd`

```dockerfile
```

-	Layers:
	-	`sha256:c5eed3c367c698de5243e012e512e93bcfb073261fb1c1f1360df30e47f9d627`  
		Last Modified: Wed, 01 May 2024 22:13:31 GMT  
		Size: 6.3 MB (6293259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b16eeec4048d39e68a41a306fd267533f6a0a2023c6016075e3b8a046c66407b`  
		Last Modified: Wed, 01 May 2024 22:13:30 GMT  
		Size: 14.7 KB (14664 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:77fc16f95036dec5f73c379d0c0b083133115e496bbb88a12c997eb1f812236c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148491545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ccc7cd3d68e411ff5e323927fa7376edd2b1648d5c01cde611bf7867da8b7b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4668ee134c6d27b158f31b1c01b5e92a02ede4c76d4b570eb243b76e7b7567bb`  
		Last Modified: Wed, 01 May 2024 22:33:11 GMT  
		Size: 18.9 MB (18870222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c26c91634d198f308ee466c4f2be3a59218fcaea48af76c19274245b1725a7`  
		Last Modified: Wed, 01 May 2024 22:33:10 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b65e3ef18a3b059c80d045b010aabe08d82d2c8504bb9b8d1e1cf28bea72b2`  
		Last Modified: Wed, 01 May 2024 22:35:35 GMT  
		Size: 56.4 MB (56418780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad2f9c46f3a11a31992befffc6b5533b6d86ea19882447a48448e2b936ba85`  
		Last Modified: Wed, 01 May 2024 22:35:33 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:336bbf80fe6a5d81fa90823a3663f5d4c6c6e5dfd4ff920a21fc0aa478942a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459f674c96e863832e3ed1390d07e3512fb7d49e6f01921a45497fba22864859`

```dockerfile
```

-	Layers:
	-	`sha256:ea9fc20d24af05be6bdcb3ece4c941918547a8353f7dc1d6e4b2554b0c58f7c8`  
		Last Modified: Wed, 01 May 2024 22:35:34 GMT  
		Size: 6.3 MB (6298512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43457d5c0f51f13681689d84eb3e643c3585306ba9c420ce87c401c054e78678`  
		Last Modified: Wed, 01 May 2024 22:35:33 GMT  
		Size: 14.6 KB (14584 bytes)  
		MIME: application/vnd.in-toto+json
