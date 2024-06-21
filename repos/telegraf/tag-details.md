<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.29`](#telegraf129)
-	[`telegraf:1.29-alpine`](#telegraf129-alpine)
-	[`telegraf:1.29.5`](#telegraf1295)
-	[`telegraf:1.29.5-alpine`](#telegraf1295-alpine)
-	[`telegraf:1.30`](#telegraf130)
-	[`telegraf:1.30-alpine`](#telegraf130-alpine)
-	[`telegraf:1.30.3`](#telegraf1303)
-	[`telegraf:1.30.3-alpine`](#telegraf1303-alpine)
-	[`telegraf:1.31`](#telegraf131)
-	[`telegraf:1.31-alpine`](#telegraf131-alpine)
-	[`telegraf:1.31.0`](#telegraf1310)
-	[`telegraf:1.31.0-alpine`](#telegraf1310-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.29`

```console
$ docker pull telegraf@sha256:579e8a76eb02820b87595a07f604b3cd389230ad1c6418ff092eb59be74a4f44
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
$ docker pull telegraf@sha256:187ea2739841f39fdb7baaa6b4a2b89b5ad8a5da53e4b1fb1116e0f250ecdfcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155219483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c163b7f1bd6a89904926f8bbe595c976c12efb38113963aa36266ced9c8979`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ea97d7bc5c5536e6d4af88b1476f960787cccfaf63226ac044b0bb1477650f`  
		Last Modified: Thu, 13 Jun 2024 18:23:56 GMT  
		Size: 18.9 MB (18947936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb32d413ed4b2f547df976de56111047f5447dca4fea708c3652b3a5b5ac2f9`  
		Last Modified: Thu, 13 Jun 2024 18:23:56 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1e50daab8faa3f23bb3972bf990bad99cfa76fb2a79fda2841578dd2f8d129`  
		Last Modified: Thu, 13 Jun 2024 18:23:56 GMT  
		Size: 62.6 MB (62642479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28418541aec0d5938439b801ee76259bf7f644b4904397b55cb1c81a17b3de61`  
		Last Modified: Thu, 13 Jun 2024 18:23:55 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:1c9c5df76e9d8e0bbf09b6278d641c655a830cd0b8b187ea5278083311114821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb9e7c43524cacf177d55051dc799057234d11f89f80a16f9b2d5a0b45854cb`

```dockerfile
```

-	Layers:
	-	`sha256:02c5a29ee85aa30b6eeb6b73fbc2c1380760d17790ac49120f630b31bc5cc887`  
		Last Modified: Thu, 13 Jun 2024 18:23:55 GMT  
		Size: 6.3 MB (6299204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:117e121c4aea2dc678e742d97068dfc00ef9d8979804b6d33abf34a44c08daaa`  
		Last Modified: Thu, 13 Jun 2024 18:23:55 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:a49dc38eb8958c1106febcda823f58362e6fef3e950be8b8337841a251609523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142841129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7ee56c3f7821983540ae2610a640783ad2cdaefcc5a439c8d80bfdf0052ecf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf146f17c4b04c5ca2c557cb73c9be1fed0cf0d0fe5bee8c1d74617db6314ba`  
		Last Modified: Fri, 14 Jun 2024 04:53:20 GMT  
		Size: 17.7 MB (17724928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d983f28198d5a99590d5f86f4724129c41da0416cc3f9923b2f2cea2c66d61d`  
		Last Modified: Fri, 14 Jun 2024 04:53:21 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f994768b9089dddd6b1014956dcc3bc029eec325e155c1aace0a1c1e135144d`  
		Last Modified: Fri, 14 Jun 2024 04:53:21 GMT  
		Size: 58.0 MB (57984972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6141bf20c52d02ee6bde18742f4b76a52cd7ff998a08c35fd760413dc867a5ae`  
		Last Modified: Fri, 14 Jun 2024 04:53:19 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:b416f1bbdc4c93c431d2c1ed95c39276b654626be7c9d6c5f225bbf3bdf1be7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6308962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f713ae5254de94e41b6c11c420657ad3c7556e11e8372f7010fdf986267194e5`

```dockerfile
```

-	Layers:
	-	`sha256:9ef52610fa65953bcc547240d770e238cc8631dd10278524e255cb2cce0531a3`  
		Last Modified: Fri, 14 Jun 2024 04:53:20 GMT  
		Size: 6.3 MB (6294558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a708e80f89e0c4e0e52e3042a9a56528fb617d6539d2f015d9d5e4b83936a9b`  
		Last Modified: Fri, 14 Jun 2024 04:53:19 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c2ee7d0d9d8ba2bb2f829ce592a4e35d4ec7bd0afe2b37e4e447b72c7553a069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149054142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c6dce5f595f611c647234c7d393aeec94d27f9494e7dce2f59e3ffda4df49a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2f02faf17c4ec382a59b54309f70d36d5833f9f68391665b51e0442d07e4e`  
		Last Modified: Fri, 14 Jun 2024 02:27:06 GMT  
		Size: 18.9 MB (18870625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49ec7ade1132963bc33d87cbdeb0aba5601c5bc17b10ad8b77f33b6a18cefdd`  
		Last Modified: Fri, 14 Jun 2024 02:27:05 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2409dbe5314e8ad8d9e2b74d16731c36428f2a839b06654418a5135db414bcd`  
		Last Modified: Fri, 14 Jun 2024 02:27:07 GMT  
		Size: 57.0 MB (56981137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6212067c302ad97a11d8d5596c57dd4c0b0f7d3b633828c193d6e05ab4557f38`  
		Last Modified: Fri, 14 Jun 2024 02:27:05 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:89f253fe90326df2a3be196be8a7ed1e88bb08d219f0e449c48dc66dd64f2419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33bca02a0e9861007496a1c3ed5051d09fccb61376665dd11fcc6a465876cbee`

```dockerfile
```

-	Layers:
	-	`sha256:ea5ebc77ae1e3678f7c57b96494000944c6b27a02cd37d7c5d462d89aa4c4643`  
		Last Modified: Fri, 14 Jun 2024 02:27:05 GMT  
		Size: 6.3 MB (6299842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99dbadd0eb54effd251c113c7e621beaacd2a3579e5c4e1b31d13fec3a41717a`  
		Last Modified: Fri, 14 Jun 2024 02:27:05 GMT  
		Size: 14.6 KB (14617 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.29-alpine`

```console
$ docker pull telegraf@sha256:a45a418654e7d83c676a6eaf8f4210a32b629b6a2da4257b89db761aee5e3183
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.29-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b4d98fbfaf3f1d7ff40ed85c70540146aa0fa4fbbf687468b22f6d1be26ee7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68518614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1564c81134cb93813370f8f75f08a8ff72d6fe556a6477f8f471a0656ba84285`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ec0c8543450ee946ac4c2c2f9aae3874329b9df256dec7a2a2a6d7f82239c0`  
		Last Modified: Thu, 20 Jun 2024 20:56:35 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8534341557b73ef6ba41ed2d84c14b991298e80406cf30c829ba55fe6dd531f`  
		Last Modified: Thu, 20 Jun 2024 20:56:36 GMT  
		Size: 2.5 MB (2452641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f5c878a1912d5951bb711c8ca6e5701e3a41e6303e969b9d649d6eb6cc5e46`  
		Last Modified: Thu, 20 Jun 2024 20:56:37 GMT  
		Size: 62.4 MB (62441523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19a98d885f59b7a00fd273e5d42a3adbcf0e25041776976d419d67ed1af9dca`  
		Last Modified: Thu, 20 Jun 2024 20:56:36 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4038f9156f61acbb53b9b11ee502dfe0b780778414853776fb72b398a3e2292f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1001195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f1c3562eeafe030c5c11fd3b202e29dcc941762f0295b8cf5d16e2dc380849`

```dockerfile
```

-	Layers:
	-	`sha256:f0cae03b640a9f603aae38824edacff44ff1270375fe427c4616ae3a52e9a999`  
		Last Modified: Thu, 20 Jun 2024 20:56:36 GMT  
		Size: 986.5 KB (986461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7d6dfd596bbf816398bc597d3fbf1e07a5b42d4be22a9ac110ab19f5dde9e84`  
		Last Modified: Thu, 20 Jun 2024 20:56:36 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:b7489cc89bfbb3afc64cc0793f8fbab9518ec171300f43ebc2a54910a1fe3230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63409663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b08dcf16d2d6c13b7f338d440e32ce6090f8dcb04751cfe89b432933d216749`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4d02fd6d451824a88c3da056c35af5ef536e8a634a98239ab90c650e0518e3`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75d4393617a41a89527ad46200950f81c7c7993bd950a78413ef7d03b012113`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 2.5 MB (2539706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c4e323f89c2384b089a00b5839fef87d6d056002482c0b5a22f16c82591b0`  
		Last Modified: Fri, 21 Jun 2024 07:01:18 GMT  
		Size: 56.8 MB (56780548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc69c6a8c13d94f9a7918c8e2e35a98316ac001c4dd518830eabf4be200e719`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:acd007149b6c53fcc9954bf1954aa3e170d017d3cc5262c637fb99e5c9c3ac49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **997.1 KB (997056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d60c41b16981197be52d5b58d9375d085534cfcd7d9011770d3c335620024f`

```dockerfile
```

-	Layers:
	-	`sha256:a420d692f20432c4fa2c0cc78f826bc1c840c30e2d680d3460871ae0ed0e9577`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 982.0 KB (982046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b72022ed01d76aa33626ce3346bb33bb260b2175e125d2f891ee54b12100c65c`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.29.5`

```console
$ docker pull telegraf@sha256:579e8a76eb02820b87595a07f604b3cd389230ad1c6418ff092eb59be74a4f44
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
$ docker pull telegraf@sha256:187ea2739841f39fdb7baaa6b4a2b89b5ad8a5da53e4b1fb1116e0f250ecdfcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155219483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c163b7f1bd6a89904926f8bbe595c976c12efb38113963aa36266ced9c8979`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ea97d7bc5c5536e6d4af88b1476f960787cccfaf63226ac044b0bb1477650f`  
		Last Modified: Thu, 13 Jun 2024 18:23:56 GMT  
		Size: 18.9 MB (18947936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb32d413ed4b2f547df976de56111047f5447dca4fea708c3652b3a5b5ac2f9`  
		Last Modified: Thu, 13 Jun 2024 18:23:56 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1e50daab8faa3f23bb3972bf990bad99cfa76fb2a79fda2841578dd2f8d129`  
		Last Modified: Thu, 13 Jun 2024 18:23:56 GMT  
		Size: 62.6 MB (62642479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28418541aec0d5938439b801ee76259bf7f644b4904397b55cb1c81a17b3de61`  
		Last Modified: Thu, 13 Jun 2024 18:23:55 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:1c9c5df76e9d8e0bbf09b6278d641c655a830cd0b8b187ea5278083311114821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb9e7c43524cacf177d55051dc799057234d11f89f80a16f9b2d5a0b45854cb`

```dockerfile
```

-	Layers:
	-	`sha256:02c5a29ee85aa30b6eeb6b73fbc2c1380760d17790ac49120f630b31bc5cc887`  
		Last Modified: Thu, 13 Jun 2024 18:23:55 GMT  
		Size: 6.3 MB (6299204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:117e121c4aea2dc678e742d97068dfc00ef9d8979804b6d33abf34a44c08daaa`  
		Last Modified: Thu, 13 Jun 2024 18:23:55 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29.5` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:a49dc38eb8958c1106febcda823f58362e6fef3e950be8b8337841a251609523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142841129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7ee56c3f7821983540ae2610a640783ad2cdaefcc5a439c8d80bfdf0052ecf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf146f17c4b04c5ca2c557cb73c9be1fed0cf0d0fe5bee8c1d74617db6314ba`  
		Last Modified: Fri, 14 Jun 2024 04:53:20 GMT  
		Size: 17.7 MB (17724928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d983f28198d5a99590d5f86f4724129c41da0416cc3f9923b2f2cea2c66d61d`  
		Last Modified: Fri, 14 Jun 2024 04:53:21 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f994768b9089dddd6b1014956dcc3bc029eec325e155c1aace0a1c1e135144d`  
		Last Modified: Fri, 14 Jun 2024 04:53:21 GMT  
		Size: 58.0 MB (57984972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6141bf20c52d02ee6bde18742f4b76a52cd7ff998a08c35fd760413dc867a5ae`  
		Last Modified: Fri, 14 Jun 2024 04:53:19 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:b416f1bbdc4c93c431d2c1ed95c39276b654626be7c9d6c5f225bbf3bdf1be7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6308962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f713ae5254de94e41b6c11c420657ad3c7556e11e8372f7010fdf986267194e5`

```dockerfile
```

-	Layers:
	-	`sha256:9ef52610fa65953bcc547240d770e238cc8631dd10278524e255cb2cce0531a3`  
		Last Modified: Fri, 14 Jun 2024 04:53:20 GMT  
		Size: 6.3 MB (6294558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a708e80f89e0c4e0e52e3042a9a56528fb617d6539d2f015d9d5e4b83936a9b`  
		Last Modified: Fri, 14 Jun 2024 04:53:19 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29.5` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c2ee7d0d9d8ba2bb2f829ce592a4e35d4ec7bd0afe2b37e4e447b72c7553a069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149054142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c6dce5f595f611c647234c7d393aeec94d27f9494e7dce2f59e3ffda4df49a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2f02faf17c4ec382a59b54309f70d36d5833f9f68391665b51e0442d07e4e`  
		Last Modified: Fri, 14 Jun 2024 02:27:06 GMT  
		Size: 18.9 MB (18870625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49ec7ade1132963bc33d87cbdeb0aba5601c5bc17b10ad8b77f33b6a18cefdd`  
		Last Modified: Fri, 14 Jun 2024 02:27:05 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2409dbe5314e8ad8d9e2b74d16731c36428f2a839b06654418a5135db414bcd`  
		Last Modified: Fri, 14 Jun 2024 02:27:07 GMT  
		Size: 57.0 MB (56981137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6212067c302ad97a11d8d5596c57dd4c0b0f7d3b633828c193d6e05ab4557f38`  
		Last Modified: Fri, 14 Jun 2024 02:27:05 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:89f253fe90326df2a3be196be8a7ed1e88bb08d219f0e449c48dc66dd64f2419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33bca02a0e9861007496a1c3ed5051d09fccb61376665dd11fcc6a465876cbee`

```dockerfile
```

-	Layers:
	-	`sha256:ea5ebc77ae1e3678f7c57b96494000944c6b27a02cd37d7c5d462d89aa4c4643`  
		Last Modified: Fri, 14 Jun 2024 02:27:05 GMT  
		Size: 6.3 MB (6299842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99dbadd0eb54effd251c113c7e621beaacd2a3579e5c4e1b31d13fec3a41717a`  
		Last Modified: Fri, 14 Jun 2024 02:27:05 GMT  
		Size: 14.6 KB (14617 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.29.5-alpine`

```console
$ docker pull telegraf@sha256:a45a418654e7d83c676a6eaf8f4210a32b629b6a2da4257b89db761aee5e3183
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.29.5-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b4d98fbfaf3f1d7ff40ed85c70540146aa0fa4fbbf687468b22f6d1be26ee7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68518614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1564c81134cb93813370f8f75f08a8ff72d6fe556a6477f8f471a0656ba84285`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ec0c8543450ee946ac4c2c2f9aae3874329b9df256dec7a2a2a6d7f82239c0`  
		Last Modified: Thu, 20 Jun 2024 20:56:35 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8534341557b73ef6ba41ed2d84c14b991298e80406cf30c829ba55fe6dd531f`  
		Last Modified: Thu, 20 Jun 2024 20:56:36 GMT  
		Size: 2.5 MB (2452641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f5c878a1912d5951bb711c8ca6e5701e3a41e6303e969b9d649d6eb6cc5e46`  
		Last Modified: Thu, 20 Jun 2024 20:56:37 GMT  
		Size: 62.4 MB (62441523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19a98d885f59b7a00fd273e5d42a3adbcf0e25041776976d419d67ed1af9dca`  
		Last Modified: Thu, 20 Jun 2024 20:56:36 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4038f9156f61acbb53b9b11ee502dfe0b780778414853776fb72b398a3e2292f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1001195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f1c3562eeafe030c5c11fd3b202e29dcc941762f0295b8cf5d16e2dc380849`

```dockerfile
```

-	Layers:
	-	`sha256:f0cae03b640a9f603aae38824edacff44ff1270375fe427c4616ae3a52e9a999`  
		Last Modified: Thu, 20 Jun 2024 20:56:36 GMT  
		Size: 986.5 KB (986461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7d6dfd596bbf816398bc597d3fbf1e07a5b42d4be22a9ac110ab19f5dde9e84`  
		Last Modified: Thu, 20 Jun 2024 20:56:36 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29.5-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:b7489cc89bfbb3afc64cc0793f8fbab9518ec171300f43ebc2a54910a1fe3230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63409663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b08dcf16d2d6c13b7f338d440e32ce6090f8dcb04751cfe89b432933d216749`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4d02fd6d451824a88c3da056c35af5ef536e8a634a98239ab90c650e0518e3`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75d4393617a41a89527ad46200950f81c7c7993bd950a78413ef7d03b012113`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 2.5 MB (2539706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c4e323f89c2384b089a00b5839fef87d6d056002482c0b5a22f16c82591b0`  
		Last Modified: Fri, 21 Jun 2024 07:01:18 GMT  
		Size: 56.8 MB (56780548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc69c6a8c13d94f9a7918c8e2e35a98316ac001c4dd518830eabf4be200e719`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:acd007149b6c53fcc9954bf1954aa3e170d017d3cc5262c637fb99e5c9c3ac49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **997.1 KB (997056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d60c41b16981197be52d5b58d9375d085534cfcd7d9011770d3c335620024f`

```dockerfile
```

-	Layers:
	-	`sha256:a420d692f20432c4fa2c0cc78f826bc1c840c30e2d680d3460871ae0ed0e9577`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 982.0 KB (982046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b72022ed01d76aa33626ce3346bb33bb260b2175e125d2f891ee54b12100c65c`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30`

```console
$ docker pull telegraf@sha256:6427d32d3604ddc52c318bf5338c785edbdac2b0dbfb362595e2ea6fd566b450
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
$ docker pull telegraf@sha256:cb5af77757ddc563b649128aa89133f7f019d4f4e916503ba0c592884b83f57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155343562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a3b6e06f66d4cbc6f4fbd071940e003895536a1ec10bbd7cb962af2b8d181c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5c16ef28714b1eb73768f679fde755bdc854512f8987b89dd8ee1d11966ff7`  
		Last Modified: Thu, 13 Jun 2024 18:24:03 GMT  
		Size: 18.9 MB (18948056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f59ce6cf45248b221b201ccc8a35d82650221b9133d90309832b80e5cb8de4`  
		Last Modified: Thu, 13 Jun 2024 18:24:02 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7afae8ec6a88c2f2b4f520d7850bffc187a5d74f00c7ec9171839241c224fa`  
		Last Modified: Thu, 13 Jun 2024 18:24:04 GMT  
		Size: 62.8 MB (62766454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aef803aabfc467d55871d503c09aa84ffc1257f26cc63c96af503806928a4f7`  
		Last Modified: Thu, 13 Jun 2024 18:24:02 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:7a39577f4c21f86312105d65bea4ad4e2946f74fdd9d487328d89ed398aea2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5597bfd476616fe101323db9981db93ed1628f28c71f1914579acf963d4204b`

```dockerfile
```

-	Layers:
	-	`sha256:0912c926fc32b6aa1768af96e0a6771f540a8174229f82df1f300d97a86f1aac`  
		Last Modified: Thu, 13 Jun 2024 18:24:02 GMT  
		Size: 6.3 MB (6299484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ea53bcdb7cf682786b4fd7ddef5eb2670c2f502698e0c9ca542781c92b056b9`  
		Last Modified: Thu, 13 Jun 2024 18:24:02 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:1cbc8686b85268acb8e13c03e6d9fa037a2310ef61cc82af412170f1d7dac374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143068927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3283597b18800eb70406a070f76960098a5e47112890c8133ccd8b7fc6205fd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf146f17c4b04c5ca2c557cb73c9be1fed0cf0d0fe5bee8c1d74617db6314ba`  
		Last Modified: Fri, 14 Jun 2024 04:53:20 GMT  
		Size: 17.7 MB (17724928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d983f28198d5a99590d5f86f4724129c41da0416cc3f9923b2f2cea2c66d61d`  
		Last Modified: Fri, 14 Jun 2024 04:53:21 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1348210ee98b1a808155e1e030b9b07efc4e4e6861068c583eba393f946e6b62`  
		Last Modified: Fri, 14 Jun 2024 04:54:14 GMT  
		Size: 58.2 MB (58212770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf88d2e096eee8af4fab613cde32239965a3e74923ea8ee446b90c42ccca457`  
		Last Modified: Fri, 14 Jun 2024 04:54:12 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:6ec9c0ddfb6a101ac4a62d74771434012aafae4eef7ac48f7e6c694504bba092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6309242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c62b3a920a440ee59420fdfbc0f42524ba636b983d2e126ba50bc259445eb8e`

```dockerfile
```

-	Layers:
	-	`sha256:6fdce2db9ae717b798bac25befef26ba671f2aca6ceb20011cced758a8822023`  
		Last Modified: Fri, 14 Jun 2024 04:54:12 GMT  
		Size: 6.3 MB (6294838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a667bc1bda5825d4701a5bb8dc5e78bd682c4d34d3efc4aae9858896b5e43a83`  
		Last Modified: Fri, 14 Jun 2024 04:54:12 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:439f0a21125c16dfcba443d1393c1f47534fa581e826ec33132939da96ff28c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149196298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cdbcbda9afaaaffc28b608b4070195adb03ba3e86bf9cd075a548e0468f64ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2f02faf17c4ec382a59b54309f70d36d5833f9f68391665b51e0442d07e4e`  
		Last Modified: Fri, 14 Jun 2024 02:27:06 GMT  
		Size: 18.9 MB (18870625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49ec7ade1132963bc33d87cbdeb0aba5601c5bc17b10ad8b77f33b6a18cefdd`  
		Last Modified: Fri, 14 Jun 2024 02:27:05 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327012ec83cacc2518a479fdd0b5ff37f0c2788f65b9c922fbc7171269390235`  
		Last Modified: Fri, 14 Jun 2024 02:27:43 GMT  
		Size: 57.1 MB (57123293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe4238db9aa776700adb9be6ea002118c1764c7dc361234897f9ea96be6219b`  
		Last Modified: Fri, 14 Jun 2024 02:27:41 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:cd0349b53618d93c52cf512195ccf65526939cd8651a9514d3216b6dee4a67c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587b39d0f24e5f0a18464e533ce674b011ff9bb5b8065e71be0d634655663332`

```dockerfile
```

-	Layers:
	-	`sha256:933d68535f76e6cd1549c571b510416434db3e31420ed12b1b52572c3fe851d6`  
		Last Modified: Fri, 14 Jun 2024 02:27:41 GMT  
		Size: 6.3 MB (6300122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7374e9139f95f6958ebe1110edb0a56300d04daddc028113c2ec9f1f3b1f855`  
		Last Modified: Fri, 14 Jun 2024 02:27:41 GMT  
		Size: 14.6 KB (14617 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30-alpine`

```console
$ docker pull telegraf@sha256:a2ed1c626f31e48a36261fb87b45435d08df5c8da8f8deef0aa567dd54e0fa8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7d9dd9a8d17927b5ab64f2b5ab5d753392bb6f602fa6926d9081256ad66894f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68645907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c78422aae7eb12bd23f41bce4cb35583613d09d7f9f20a343bd2110d44d1408`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854692264f8809cf92629e7525eb2598493eae4136d97f12ba8db44a2957cb6a`  
		Last Modified: Thu, 20 Jun 2024 20:56:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f81fa91f596181920960e72a6871a7fbfd31377b83e4d7ecdd55850dba219e7`  
		Last Modified: Thu, 20 Jun 2024 20:56:40 GMT  
		Size: 2.5 MB (2452628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5989c1129b25207a17de9c1e2b3b4d9bb5e4fa649a47321695b750cacd317a6b`  
		Last Modified: Thu, 20 Jun 2024 20:56:41 GMT  
		Size: 62.6 MB (62568829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8194eec5904ba428ad67b75aabc1dcc4ec6535ed0da6072bf4cbc796f12edf2f`  
		Last Modified: Thu, 20 Jun 2024 20:56:40 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:ec438523f550864f5f8cde1a61b9cb8dcafd1ce5b8e7039c9ca4358ff1d5688c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1001473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99b04efa643dcbf93abeb20c32c100ab442b5c97962b86919ffda7368edf4f1`

```dockerfile
```

-	Layers:
	-	`sha256:ed43db3ec20a6ba58ead7a069a1bf3aa51caa9afdd7e617641224fdd0c9864f6`  
		Last Modified: Thu, 20 Jun 2024 20:56:40 GMT  
		Size: 986.7 KB (986741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e2212a71037664885b4644cfe397c388c4704a4a706dcee39402e20ef0035c3`  
		Last Modified: Thu, 20 Jun 2024 20:56:40 GMT  
		Size: 14.7 KB (14732 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:669deff433f02f6cacdd048db7d127be4525d4dbe2db1a46f64ff6871a2341be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63550043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3dfe6b665f35c9e2fa07a7dba07cabfb44eec39975e2e76fb054559813bbea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4d02fd6d451824a88c3da056c35af5ef536e8a634a98239ab90c650e0518e3`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75d4393617a41a89527ad46200950f81c7c7993bd950a78413ef7d03b012113`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 2.5 MB (2539706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ee2de43b13169732d1745220365bd29615aa3000ad87986f795e3646215063`  
		Last Modified: Fri, 21 Jun 2024 07:01:54 GMT  
		Size: 56.9 MB (56920929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d390d8961f619b0803315f7c8b9d30e7635c6a23d4217bb5eff1f2c1bb2dabe`  
		Last Modified: Fri, 21 Jun 2024 07:01:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9a79b9bfee239c98abdfc6ec6c30c40e6a5e4a9db8fbbec7cf5c9f54d5673969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **997.3 KB (997336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e324cc8737b4f71db9beb447e8c7883604b95a87d1ab87f69850af44f2d0522`

```dockerfile
```

-	Layers:
	-	`sha256:e76a842a5de56bcea91c867461438062efcf970ccadae5ef1f9762f0e04de620`  
		Last Modified: Fri, 21 Jun 2024 07:01:52 GMT  
		Size: 982.3 KB (982326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f43f107321e13e25da1cbba39d7755e169259c65de055b3c2bdc12aa9b2cc261`  
		Last Modified: Fri, 21 Jun 2024 07:01:51 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30.3`

```console
$ docker pull telegraf@sha256:6427d32d3604ddc52c318bf5338c785edbdac2b0dbfb362595e2ea6fd566b450
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
$ docker pull telegraf@sha256:cb5af77757ddc563b649128aa89133f7f019d4f4e916503ba0c592884b83f57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155343562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a3b6e06f66d4cbc6f4fbd071940e003895536a1ec10bbd7cb962af2b8d181c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5c16ef28714b1eb73768f679fde755bdc854512f8987b89dd8ee1d11966ff7`  
		Last Modified: Thu, 13 Jun 2024 18:24:03 GMT  
		Size: 18.9 MB (18948056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f59ce6cf45248b221b201ccc8a35d82650221b9133d90309832b80e5cb8de4`  
		Last Modified: Thu, 13 Jun 2024 18:24:02 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7afae8ec6a88c2f2b4f520d7850bffc187a5d74f00c7ec9171839241c224fa`  
		Last Modified: Thu, 13 Jun 2024 18:24:04 GMT  
		Size: 62.8 MB (62766454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aef803aabfc467d55871d503c09aa84ffc1257f26cc63c96af503806928a4f7`  
		Last Modified: Thu, 13 Jun 2024 18:24:02 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:7a39577f4c21f86312105d65bea4ad4e2946f74fdd9d487328d89ed398aea2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5597bfd476616fe101323db9981db93ed1628f28c71f1914579acf963d4204b`

```dockerfile
```

-	Layers:
	-	`sha256:0912c926fc32b6aa1768af96e0a6771f540a8174229f82df1f300d97a86f1aac`  
		Last Modified: Thu, 13 Jun 2024 18:24:02 GMT  
		Size: 6.3 MB (6299484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ea53bcdb7cf682786b4fd7ddef5eb2670c2f502698e0c9ca542781c92b056b9`  
		Last Modified: Thu, 13 Jun 2024 18:24:02 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:1cbc8686b85268acb8e13c03e6d9fa037a2310ef61cc82af412170f1d7dac374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143068927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3283597b18800eb70406a070f76960098a5e47112890c8133ccd8b7fc6205fd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf146f17c4b04c5ca2c557cb73c9be1fed0cf0d0fe5bee8c1d74617db6314ba`  
		Last Modified: Fri, 14 Jun 2024 04:53:20 GMT  
		Size: 17.7 MB (17724928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d983f28198d5a99590d5f86f4724129c41da0416cc3f9923b2f2cea2c66d61d`  
		Last Modified: Fri, 14 Jun 2024 04:53:21 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1348210ee98b1a808155e1e030b9b07efc4e4e6861068c583eba393f946e6b62`  
		Last Modified: Fri, 14 Jun 2024 04:54:14 GMT  
		Size: 58.2 MB (58212770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf88d2e096eee8af4fab613cde32239965a3e74923ea8ee446b90c42ccca457`  
		Last Modified: Fri, 14 Jun 2024 04:54:12 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:6ec9c0ddfb6a101ac4a62d74771434012aafae4eef7ac48f7e6c694504bba092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6309242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c62b3a920a440ee59420fdfbc0f42524ba636b983d2e126ba50bc259445eb8e`

```dockerfile
```

-	Layers:
	-	`sha256:6fdce2db9ae717b798bac25befef26ba671f2aca6ceb20011cced758a8822023`  
		Last Modified: Fri, 14 Jun 2024 04:54:12 GMT  
		Size: 6.3 MB (6294838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a667bc1bda5825d4701a5bb8dc5e78bd682c4d34d3efc4aae9858896b5e43a83`  
		Last Modified: Fri, 14 Jun 2024 04:54:12 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:439f0a21125c16dfcba443d1393c1f47534fa581e826ec33132939da96ff28c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149196298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cdbcbda9afaaaffc28b608b4070195adb03ba3e86bf9cd075a548e0468f64ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2f02faf17c4ec382a59b54309f70d36d5833f9f68391665b51e0442d07e4e`  
		Last Modified: Fri, 14 Jun 2024 02:27:06 GMT  
		Size: 18.9 MB (18870625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49ec7ade1132963bc33d87cbdeb0aba5601c5bc17b10ad8b77f33b6a18cefdd`  
		Last Modified: Fri, 14 Jun 2024 02:27:05 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327012ec83cacc2518a479fdd0b5ff37f0c2788f65b9c922fbc7171269390235`  
		Last Modified: Fri, 14 Jun 2024 02:27:43 GMT  
		Size: 57.1 MB (57123293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe4238db9aa776700adb9be6ea002118c1764c7dc361234897f9ea96be6219b`  
		Last Modified: Fri, 14 Jun 2024 02:27:41 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:cd0349b53618d93c52cf512195ccf65526939cd8651a9514d3216b6dee4a67c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587b39d0f24e5f0a18464e533ce674b011ff9bb5b8065e71be0d634655663332`

```dockerfile
```

-	Layers:
	-	`sha256:933d68535f76e6cd1549c571b510416434db3e31420ed12b1b52572c3fe851d6`  
		Last Modified: Fri, 14 Jun 2024 02:27:41 GMT  
		Size: 6.3 MB (6300122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7374e9139f95f6958ebe1110edb0a56300d04daddc028113c2ec9f1f3b1f855`  
		Last Modified: Fri, 14 Jun 2024 02:27:41 GMT  
		Size: 14.6 KB (14617 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30.3-alpine`

```console
$ docker pull telegraf@sha256:a2ed1c626f31e48a36261fb87b45435d08df5c8da8f8deef0aa567dd54e0fa8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7d9dd9a8d17927b5ab64f2b5ab5d753392bb6f602fa6926d9081256ad66894f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68645907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c78422aae7eb12bd23f41bce4cb35583613d09d7f9f20a343bd2110d44d1408`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854692264f8809cf92629e7525eb2598493eae4136d97f12ba8db44a2957cb6a`  
		Last Modified: Thu, 20 Jun 2024 20:56:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f81fa91f596181920960e72a6871a7fbfd31377b83e4d7ecdd55850dba219e7`  
		Last Modified: Thu, 20 Jun 2024 20:56:40 GMT  
		Size: 2.5 MB (2452628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5989c1129b25207a17de9c1e2b3b4d9bb5e4fa649a47321695b750cacd317a6b`  
		Last Modified: Thu, 20 Jun 2024 20:56:41 GMT  
		Size: 62.6 MB (62568829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8194eec5904ba428ad67b75aabc1dcc4ec6535ed0da6072bf4cbc796f12edf2f`  
		Last Modified: Thu, 20 Jun 2024 20:56:40 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:ec438523f550864f5f8cde1a61b9cb8dcafd1ce5b8e7039c9ca4358ff1d5688c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1001473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99b04efa643dcbf93abeb20c32c100ab442b5c97962b86919ffda7368edf4f1`

```dockerfile
```

-	Layers:
	-	`sha256:ed43db3ec20a6ba58ead7a069a1bf3aa51caa9afdd7e617641224fdd0c9864f6`  
		Last Modified: Thu, 20 Jun 2024 20:56:40 GMT  
		Size: 986.7 KB (986741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e2212a71037664885b4644cfe397c388c4704a4a706dcee39402e20ef0035c3`  
		Last Modified: Thu, 20 Jun 2024 20:56:40 GMT  
		Size: 14.7 KB (14732 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:669deff433f02f6cacdd048db7d127be4525d4dbe2db1a46f64ff6871a2341be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63550043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3dfe6b665f35c9e2fa07a7dba07cabfb44eec39975e2e76fb054559813bbea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4d02fd6d451824a88c3da056c35af5ef536e8a634a98239ab90c650e0518e3`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75d4393617a41a89527ad46200950f81c7c7993bd950a78413ef7d03b012113`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 2.5 MB (2539706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ee2de43b13169732d1745220365bd29615aa3000ad87986f795e3646215063`  
		Last Modified: Fri, 21 Jun 2024 07:01:54 GMT  
		Size: 56.9 MB (56920929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d390d8961f619b0803315f7c8b9d30e7635c6a23d4217bb5eff1f2c1bb2dabe`  
		Last Modified: Fri, 21 Jun 2024 07:01:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9a79b9bfee239c98abdfc6ec6c30c40e6a5e4a9db8fbbec7cf5c9f54d5673969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **997.3 KB (997336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e324cc8737b4f71db9beb447e8c7883604b95a87d1ab87f69850af44f2d0522`

```dockerfile
```

-	Layers:
	-	`sha256:e76a842a5de56bcea91c867461438062efcf970ccadae5ef1f9762f0e04de620`  
		Last Modified: Fri, 21 Jun 2024 07:01:52 GMT  
		Size: 982.3 KB (982326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f43f107321e13e25da1cbba39d7755e169259c65de055b3c2bdc12aa9b2cc261`  
		Last Modified: Fri, 21 Jun 2024 07:01:51 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31`

```console
$ docker pull telegraf@sha256:a3fd9bde5d28301f27e87ec8ff8389365c788526cf22f19493ca6c02561be819
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
$ docker pull telegraf@sha256:cc725f0815864768711363bcb8f72fb318a49cd6de3c0a30c3982936e89e2498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157666348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055d4d585a8394cba8d922c1b699f701c593830a9370a4ed5973751dee41b7c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b544422e702f60545a013907e167d071d2df2aca46bb293ea989c838e92aecd`  
		Last Modified: Thu, 13 Jun 2024 18:24:19 GMT  
		Size: 18.9 MB (18947987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3f16a5f811a5ea914ed2e064204f1b421f30a6db4a39b5edeaf1befebe40c9`  
		Last Modified: Thu, 13 Jun 2024 18:24:18 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43743eef1327ea33746f5ad213f69f020857b4effec7f1d0d7ba4ad3efb5442`  
		Last Modified: Thu, 13 Jun 2024 18:24:20 GMT  
		Size: 65.1 MB (65089299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d7f0aa14b7b4cf144180fcd16a44609a3a4d3adb380ad3f58353e1e0a635cd`  
		Last Modified: Thu, 13 Jun 2024 18:24:18 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:3214527b87c92558d44dcc79d32163f091a81cec45b2ff78784483fa25075b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f9e71998a4c85358b2901fc1b239e33499bff7b8d87a14750da70064c7ba47`

```dockerfile
```

-	Layers:
	-	`sha256:47ff337fb7e0dd24bf9fd05d03b238350b3d716609f69394a3b3248a6ec4e230`  
		Last Modified: Thu, 13 Jun 2024 18:24:18 GMT  
		Size: 6.3 MB (6303812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efb5cc854a8efcf0f66f76afa2a727b3d1f508723b5585205a495a6b42b94818`  
		Last Modified: Thu, 13 Jun 2024 18:24:18 GMT  
		Size: 14.6 KB (14626 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:e99609f5a606a0f3c412163d1f900959cd349c1f68fbf8da070980fb3ba2aff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145377097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbabb35ec0f52e023d342d61fcebe0bbde8fbc373721f8e161dcb5529c3df094`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf146f17c4b04c5ca2c557cb73c9be1fed0cf0d0fe5bee8c1d74617db6314ba`  
		Last Modified: Fri, 14 Jun 2024 04:53:20 GMT  
		Size: 17.7 MB (17724928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d983f28198d5a99590d5f86f4724129c41da0416cc3f9923b2f2cea2c66d61d`  
		Last Modified: Fri, 14 Jun 2024 04:53:21 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1364f124231b8adbd533b6f309c5f7cffb7535269660e2e6cd4b4201f4147a4`  
		Last Modified: Fri, 14 Jun 2024 04:55:09 GMT  
		Size: 60.5 MB (60520942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae7c96b5fbf7fb8a68863e3bb2175922b1af8bac2682be3a4b416d0608b7115`  
		Last Modified: Fri, 14 Jun 2024 04:55:07 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:586e7c2d56daf592e9d9892b00e8c949ab2690b2f1c197f855e0a3460c75919a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2268fedd6b84dd4ce2d825386e483de4c35ccbdbe7f08021bb4532605702ef2a`

```dockerfile
```

-	Layers:
	-	`sha256:6f4834dfdeed043eb2eadc978b926df04a00af31bb23622bfc8b2ad21252b738`  
		Last Modified: Fri, 14 Jun 2024 04:55:07 GMT  
		Size: 6.3 MB (6299828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ed5b836e1b083802b9ac200d34a1fb213b398c6cee63de871b50d937657f3d`  
		Last Modified: Fri, 14 Jun 2024 04:55:07 GMT  
		Size: 14.7 KB (14714 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:cc68f549b7c4afb52c82937338c0cddf4c09141ba51200a93bc37719eeeedc48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151291070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf22d6bb19b4cc7029dd0330ad0aeabe0dc55f7ea2a392a3db16d196ba494f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2f02faf17c4ec382a59b54309f70d36d5833f9f68391665b51e0442d07e4e`  
		Last Modified: Fri, 14 Jun 2024 02:27:06 GMT  
		Size: 18.9 MB (18870625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49ec7ade1132963bc33d87cbdeb0aba5601c5bc17b10ad8b77f33b6a18cefdd`  
		Last Modified: Fri, 14 Jun 2024 02:27:05 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eac201c3c979f763764749fa3a02953658462d96cbea6aef28ebb0add7f1ade`  
		Last Modified: Fri, 14 Jun 2024 02:28:18 GMT  
		Size: 59.2 MB (59218065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f13455451fbd1dd0d3260d4cb103ab7c72ea1b928e911c0b979beea59e3dd1`  
		Last Modified: Fri, 14 Jun 2024 02:28:16 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:50632494559d86eac75ef9feac226e10281e640aaa348b2ec40d8083eb0f1220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6320698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f905f8db25306d4a35f65710fe5dc09d3e27c2982aee6e5823800bde7a96b8`

```dockerfile
```

-	Layers:
	-	`sha256:9bee7f9e0ee4210c7bc7ba5a7d5d53acc078cfbbba676e4936fdd86145fd5b7a`  
		Last Modified: Fri, 14 Jun 2024 02:28:17 GMT  
		Size: 6.3 MB (6305768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bda6498fa504623fae871fa8f4553f2f8137f985f6555067539db626456831c6`  
		Last Modified: Fri, 14 Jun 2024 02:28:16 GMT  
		Size: 14.9 KB (14930 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31-alpine`

```console
$ docker pull telegraf@sha256:936e30fd71b9a3c27d53ce9229953d025811bedcf57fb301e753d557c2e45437
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:9135d659bb330fc5958d2d5f6cb49f097f7aa4bd0ccf15765a7ad3a5e9d87dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70968917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6d9b40ffd3be9f391d78af6277cae1f42ace397007c6c60404a5f4cbceb3f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519e0b64014137e38d01158fb7fb21e423a93da332fd6b95b67ebbd67456db18`  
		Last Modified: Thu, 20 Jun 2024 20:56:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6c6387e3aceb95b9aa6f50902763954d64f353a43c87d05d4bec8c62f124d8`  
		Last Modified: Thu, 20 Jun 2024 20:56:47 GMT  
		Size: 2.5 MB (2452624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c945a75e8792b1293770eac0ad804c8058d7334b3b64106df49f1b1b1e317bf2`  
		Last Modified: Thu, 20 Jun 2024 20:56:48 GMT  
		Size: 64.9 MB (64891840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fbde9f849ec344671f835e8c6989b67db89802c51566272f609dcdca3fe92a`  
		Last Modified: Thu, 20 Jun 2024 20:56:47 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9db694bd013b8a7a1c54e5d9355148ae5c0696975514a36bff458fd414a7b1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1006105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c5b485b76a473b4d05aded093e6d20d775fd50c855274cb2477ed798f73a99`

```dockerfile
```

-	Layers:
	-	`sha256:4d1b403a4aef78f375e034aa5179812f92ccdfc7173056daaa98da078a2990a9`  
		Last Modified: Thu, 20 Jun 2024 20:56:47 GMT  
		Size: 991.1 KB (991069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95012819ef21cede26ace42a448c5d9b91240dbf5a6df58d02d40d9200362a41`  
		Last Modified: Thu, 20 Jun 2024 20:56:47 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4f1233944459215f7c7b3374f1e60a585af50d3738cc0d95eb54a60e9cd28ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65649250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c058664d0314985cc743c5e23605eb58d030b64b1d23b14c5228da8781cabf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4d02fd6d451824a88c3da056c35af5ef536e8a634a98239ab90c650e0518e3`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75d4393617a41a89527ad46200950f81c7c7993bd950a78413ef7d03b012113`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 2.5 MB (2539706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c049c93bb18ecfd2e4038ec248f1c54724ab954d9abb3fb4b1c6f919ad894c35`  
		Last Modified: Fri, 21 Jun 2024 07:02:25 GMT  
		Size: 59.0 MB (59020137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a21376323bf3755211bbbad2f03d5a2c4e633dffdee25251427c3316344992`  
		Last Modified: Fri, 21 Jun 2024 07:02:22 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:5e8aad1076c9e00e1944d5fa817289d7bb1d30bd5212bd1c09a9a44d7f8dbff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1003296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb32fe1022cc60f4eefad936aeda7da2996b2ceeddfd4cf172db84315565f55`

```dockerfile
```

-	Layers:
	-	`sha256:41745a7fa13c44c2bc34f51070e6df1487140c04b6db80fa6c06aacfdb047dac`  
		Last Modified: Fri, 21 Jun 2024 07:02:23 GMT  
		Size: 988.0 KB (987972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373261fcab240e364798582da667ac67257985292ae7d356280b55cf5fe93542`  
		Last Modified: Fri, 21 Jun 2024 07:02:22 GMT  
		Size: 15.3 KB (15324 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.0`

```console
$ docker pull telegraf@sha256:a3fd9bde5d28301f27e87ec8ff8389365c788526cf22f19493ca6c02561be819
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31.0` - linux; amd64

```console
$ docker pull telegraf@sha256:cc725f0815864768711363bcb8f72fb318a49cd6de3c0a30c3982936e89e2498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157666348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055d4d585a8394cba8d922c1b699f701c593830a9370a4ed5973751dee41b7c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b544422e702f60545a013907e167d071d2df2aca46bb293ea989c838e92aecd`  
		Last Modified: Thu, 13 Jun 2024 18:24:19 GMT  
		Size: 18.9 MB (18947987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3f16a5f811a5ea914ed2e064204f1b421f30a6db4a39b5edeaf1befebe40c9`  
		Last Modified: Thu, 13 Jun 2024 18:24:18 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43743eef1327ea33746f5ad213f69f020857b4effec7f1d0d7ba4ad3efb5442`  
		Last Modified: Thu, 13 Jun 2024 18:24:20 GMT  
		Size: 65.1 MB (65089299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d7f0aa14b7b4cf144180fcd16a44609a3a4d3adb380ad3f58353e1e0a635cd`  
		Last Modified: Thu, 13 Jun 2024 18:24:18 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.0` - unknown; unknown

```console
$ docker pull telegraf@sha256:3214527b87c92558d44dcc79d32163f091a81cec45b2ff78784483fa25075b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f9e71998a4c85358b2901fc1b239e33499bff7b8d87a14750da70064c7ba47`

```dockerfile
```

-	Layers:
	-	`sha256:47ff337fb7e0dd24bf9fd05d03b238350b3d716609f69394a3b3248a6ec4e230`  
		Last Modified: Thu, 13 Jun 2024 18:24:18 GMT  
		Size: 6.3 MB (6303812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efb5cc854a8efcf0f66f76afa2a727b3d1f508723b5585205a495a6b42b94818`  
		Last Modified: Thu, 13 Jun 2024 18:24:18 GMT  
		Size: 14.6 KB (14626 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.0` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:e99609f5a606a0f3c412163d1f900959cd349c1f68fbf8da070980fb3ba2aff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145377097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbabb35ec0f52e023d342d61fcebe0bbde8fbc373721f8e161dcb5529c3df094`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf146f17c4b04c5ca2c557cb73c9be1fed0cf0d0fe5bee8c1d74617db6314ba`  
		Last Modified: Fri, 14 Jun 2024 04:53:20 GMT  
		Size: 17.7 MB (17724928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d983f28198d5a99590d5f86f4724129c41da0416cc3f9923b2f2cea2c66d61d`  
		Last Modified: Fri, 14 Jun 2024 04:53:21 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1364f124231b8adbd533b6f309c5f7cffb7535269660e2e6cd4b4201f4147a4`  
		Last Modified: Fri, 14 Jun 2024 04:55:09 GMT  
		Size: 60.5 MB (60520942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae7c96b5fbf7fb8a68863e3bb2175922b1af8bac2682be3a4b416d0608b7115`  
		Last Modified: Fri, 14 Jun 2024 04:55:07 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.0` - unknown; unknown

```console
$ docker pull telegraf@sha256:586e7c2d56daf592e9d9892b00e8c949ab2690b2f1c197f855e0a3460c75919a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2268fedd6b84dd4ce2d825386e483de4c35ccbdbe7f08021bb4532605702ef2a`

```dockerfile
```

-	Layers:
	-	`sha256:6f4834dfdeed043eb2eadc978b926df04a00af31bb23622bfc8b2ad21252b738`  
		Last Modified: Fri, 14 Jun 2024 04:55:07 GMT  
		Size: 6.3 MB (6299828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ed5b836e1b083802b9ac200d34a1fb213b398c6cee63de871b50d937657f3d`  
		Last Modified: Fri, 14 Jun 2024 04:55:07 GMT  
		Size: 14.7 KB (14714 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.0` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:cc68f549b7c4afb52c82937338c0cddf4c09141ba51200a93bc37719eeeedc48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151291070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf22d6bb19b4cc7029dd0330ad0aeabe0dc55f7ea2a392a3db16d196ba494f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2f02faf17c4ec382a59b54309f70d36d5833f9f68391665b51e0442d07e4e`  
		Last Modified: Fri, 14 Jun 2024 02:27:06 GMT  
		Size: 18.9 MB (18870625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49ec7ade1132963bc33d87cbdeb0aba5601c5bc17b10ad8b77f33b6a18cefdd`  
		Last Modified: Fri, 14 Jun 2024 02:27:05 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eac201c3c979f763764749fa3a02953658462d96cbea6aef28ebb0add7f1ade`  
		Last Modified: Fri, 14 Jun 2024 02:28:18 GMT  
		Size: 59.2 MB (59218065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f13455451fbd1dd0d3260d4cb103ab7c72ea1b928e911c0b979beea59e3dd1`  
		Last Modified: Fri, 14 Jun 2024 02:28:16 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.0` - unknown; unknown

```console
$ docker pull telegraf@sha256:50632494559d86eac75ef9feac226e10281e640aaa348b2ec40d8083eb0f1220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6320698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f905f8db25306d4a35f65710fe5dc09d3e27c2982aee6e5823800bde7a96b8`

```dockerfile
```

-	Layers:
	-	`sha256:9bee7f9e0ee4210c7bc7ba5a7d5d53acc078cfbbba676e4936fdd86145fd5b7a`  
		Last Modified: Fri, 14 Jun 2024 02:28:17 GMT  
		Size: 6.3 MB (6305768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bda6498fa504623fae871fa8f4553f2f8137f985f6555067539db626456831c6`  
		Last Modified: Fri, 14 Jun 2024 02:28:16 GMT  
		Size: 14.9 KB (14930 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.0-alpine`

```console
$ docker pull telegraf@sha256:936e30fd71b9a3c27d53ce9229953d025811bedcf57fb301e753d557c2e45437
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31.0-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:9135d659bb330fc5958d2d5f6cb49f097f7aa4bd0ccf15765a7ad3a5e9d87dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70968917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6d9b40ffd3be9f391d78af6277cae1f42ace397007c6c60404a5f4cbceb3f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519e0b64014137e38d01158fb7fb21e423a93da332fd6b95b67ebbd67456db18`  
		Last Modified: Thu, 20 Jun 2024 20:56:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6c6387e3aceb95b9aa6f50902763954d64f353a43c87d05d4bec8c62f124d8`  
		Last Modified: Thu, 20 Jun 2024 20:56:47 GMT  
		Size: 2.5 MB (2452624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c945a75e8792b1293770eac0ad804c8058d7334b3b64106df49f1b1b1e317bf2`  
		Last Modified: Thu, 20 Jun 2024 20:56:48 GMT  
		Size: 64.9 MB (64891840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fbde9f849ec344671f835e8c6989b67db89802c51566272f609dcdca3fe92a`  
		Last Modified: Thu, 20 Jun 2024 20:56:47 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.0-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9db694bd013b8a7a1c54e5d9355148ae5c0696975514a36bff458fd414a7b1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1006105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c5b485b76a473b4d05aded093e6d20d775fd50c855274cb2477ed798f73a99`

```dockerfile
```

-	Layers:
	-	`sha256:4d1b403a4aef78f375e034aa5179812f92ccdfc7173056daaa98da078a2990a9`  
		Last Modified: Thu, 20 Jun 2024 20:56:47 GMT  
		Size: 991.1 KB (991069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95012819ef21cede26ace42a448c5d9b91240dbf5a6df58d02d40d9200362a41`  
		Last Modified: Thu, 20 Jun 2024 20:56:47 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.0-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4f1233944459215f7c7b3374f1e60a585af50d3738cc0d95eb54a60e9cd28ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65649250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c058664d0314985cc743c5e23605eb58d030b64b1d23b14c5228da8781cabf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4d02fd6d451824a88c3da056c35af5ef536e8a634a98239ab90c650e0518e3`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75d4393617a41a89527ad46200950f81c7c7993bd950a78413ef7d03b012113`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 2.5 MB (2539706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c049c93bb18ecfd2e4038ec248f1c54724ab954d9abb3fb4b1c6f919ad894c35`  
		Last Modified: Fri, 21 Jun 2024 07:02:25 GMT  
		Size: 59.0 MB (59020137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a21376323bf3755211bbbad2f03d5a2c4e633dffdee25251427c3316344992`  
		Last Modified: Fri, 21 Jun 2024 07:02:22 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.0-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:5e8aad1076c9e00e1944d5fa817289d7bb1d30bd5212bd1c09a9a44d7f8dbff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1003296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb32fe1022cc60f4eefad936aeda7da2996b2ceeddfd4cf172db84315565f55`

```dockerfile
```

-	Layers:
	-	`sha256:41745a7fa13c44c2bc34f51070e6df1487140c04b6db80fa6c06aacfdb047dac`  
		Last Modified: Fri, 21 Jun 2024 07:02:23 GMT  
		Size: 988.0 KB (987972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373261fcab240e364798582da667ac67257985292ae7d356280b55cf5fe93542`  
		Last Modified: Fri, 21 Jun 2024 07:02:22 GMT  
		Size: 15.3 KB (15324 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:936e30fd71b9a3c27d53ce9229953d025811bedcf57fb301e753d557c2e45437
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:9135d659bb330fc5958d2d5f6cb49f097f7aa4bd0ccf15765a7ad3a5e9d87dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70968917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6d9b40ffd3be9f391d78af6277cae1f42ace397007c6c60404a5f4cbceb3f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519e0b64014137e38d01158fb7fb21e423a93da332fd6b95b67ebbd67456db18`  
		Last Modified: Thu, 20 Jun 2024 20:56:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6c6387e3aceb95b9aa6f50902763954d64f353a43c87d05d4bec8c62f124d8`  
		Last Modified: Thu, 20 Jun 2024 20:56:47 GMT  
		Size: 2.5 MB (2452624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c945a75e8792b1293770eac0ad804c8058d7334b3b64106df49f1b1b1e317bf2`  
		Last Modified: Thu, 20 Jun 2024 20:56:48 GMT  
		Size: 64.9 MB (64891840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fbde9f849ec344671f835e8c6989b67db89802c51566272f609dcdca3fe92a`  
		Last Modified: Thu, 20 Jun 2024 20:56:47 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9db694bd013b8a7a1c54e5d9355148ae5c0696975514a36bff458fd414a7b1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1006105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c5b485b76a473b4d05aded093e6d20d775fd50c855274cb2477ed798f73a99`

```dockerfile
```

-	Layers:
	-	`sha256:4d1b403a4aef78f375e034aa5179812f92ccdfc7173056daaa98da078a2990a9`  
		Last Modified: Thu, 20 Jun 2024 20:56:47 GMT  
		Size: 991.1 KB (991069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95012819ef21cede26ace42a448c5d9b91240dbf5a6df58d02d40d9200362a41`  
		Last Modified: Thu, 20 Jun 2024 20:56:47 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4f1233944459215f7c7b3374f1e60a585af50d3738cc0d95eb54a60e9cd28ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65649250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c058664d0314985cc743c5e23605eb58d030b64b1d23b14c5228da8781cabf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4d02fd6d451824a88c3da056c35af5ef536e8a634a98239ab90c650e0518e3`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75d4393617a41a89527ad46200950f81c7c7993bd950a78413ef7d03b012113`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 2.5 MB (2539706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c049c93bb18ecfd2e4038ec248f1c54724ab954d9abb3fb4b1c6f919ad894c35`  
		Last Modified: Fri, 21 Jun 2024 07:02:25 GMT  
		Size: 59.0 MB (59020137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a21376323bf3755211bbbad2f03d5a2c4e633dffdee25251427c3316344992`  
		Last Modified: Fri, 21 Jun 2024 07:02:22 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:5e8aad1076c9e00e1944d5fa817289d7bb1d30bd5212bd1c09a9a44d7f8dbff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1003296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb32fe1022cc60f4eefad936aeda7da2996b2ceeddfd4cf172db84315565f55`

```dockerfile
```

-	Layers:
	-	`sha256:41745a7fa13c44c2bc34f51070e6df1487140c04b6db80fa6c06aacfdb047dac`  
		Last Modified: Fri, 21 Jun 2024 07:02:23 GMT  
		Size: 988.0 KB (987972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373261fcab240e364798582da667ac67257985292ae7d356280b55cf5fe93542`  
		Last Modified: Fri, 21 Jun 2024 07:02:22 GMT  
		Size: 15.3 KB (15324 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:a3fd9bde5d28301f27e87ec8ff8389365c788526cf22f19493ca6c02561be819
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
$ docker pull telegraf@sha256:cc725f0815864768711363bcb8f72fb318a49cd6de3c0a30c3982936e89e2498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157666348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055d4d585a8394cba8d922c1b699f701c593830a9370a4ed5973751dee41b7c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b544422e702f60545a013907e167d071d2df2aca46bb293ea989c838e92aecd`  
		Last Modified: Thu, 13 Jun 2024 18:24:19 GMT  
		Size: 18.9 MB (18947987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3f16a5f811a5ea914ed2e064204f1b421f30a6db4a39b5edeaf1befebe40c9`  
		Last Modified: Thu, 13 Jun 2024 18:24:18 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43743eef1327ea33746f5ad213f69f020857b4effec7f1d0d7ba4ad3efb5442`  
		Last Modified: Thu, 13 Jun 2024 18:24:20 GMT  
		Size: 65.1 MB (65089299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d7f0aa14b7b4cf144180fcd16a44609a3a4d3adb380ad3f58353e1e0a635cd`  
		Last Modified: Thu, 13 Jun 2024 18:24:18 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:3214527b87c92558d44dcc79d32163f091a81cec45b2ff78784483fa25075b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f9e71998a4c85358b2901fc1b239e33499bff7b8d87a14750da70064c7ba47`

```dockerfile
```

-	Layers:
	-	`sha256:47ff337fb7e0dd24bf9fd05d03b238350b3d716609f69394a3b3248a6ec4e230`  
		Last Modified: Thu, 13 Jun 2024 18:24:18 GMT  
		Size: 6.3 MB (6303812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efb5cc854a8efcf0f66f76afa2a727b3d1f508723b5585205a495a6b42b94818`  
		Last Modified: Thu, 13 Jun 2024 18:24:18 GMT  
		Size: 14.6 KB (14626 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:e99609f5a606a0f3c412163d1f900959cd349c1f68fbf8da070980fb3ba2aff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145377097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbabb35ec0f52e023d342d61fcebe0bbde8fbc373721f8e161dcb5529c3df094`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf146f17c4b04c5ca2c557cb73c9be1fed0cf0d0fe5bee8c1d74617db6314ba`  
		Last Modified: Fri, 14 Jun 2024 04:53:20 GMT  
		Size: 17.7 MB (17724928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d983f28198d5a99590d5f86f4724129c41da0416cc3f9923b2f2cea2c66d61d`  
		Last Modified: Fri, 14 Jun 2024 04:53:21 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1364f124231b8adbd533b6f309c5f7cffb7535269660e2e6cd4b4201f4147a4`  
		Last Modified: Fri, 14 Jun 2024 04:55:09 GMT  
		Size: 60.5 MB (60520942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae7c96b5fbf7fb8a68863e3bb2175922b1af8bac2682be3a4b416d0608b7115`  
		Last Modified: Fri, 14 Jun 2024 04:55:07 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:586e7c2d56daf592e9d9892b00e8c949ab2690b2f1c197f855e0a3460c75919a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2268fedd6b84dd4ce2d825386e483de4c35ccbdbe7f08021bb4532605702ef2a`

```dockerfile
```

-	Layers:
	-	`sha256:6f4834dfdeed043eb2eadc978b926df04a00af31bb23622bfc8b2ad21252b738`  
		Last Modified: Fri, 14 Jun 2024 04:55:07 GMT  
		Size: 6.3 MB (6299828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ed5b836e1b083802b9ac200d34a1fb213b398c6cee63de871b50d937657f3d`  
		Last Modified: Fri, 14 Jun 2024 04:55:07 GMT  
		Size: 14.7 KB (14714 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:cc68f549b7c4afb52c82937338c0cddf4c09141ba51200a93bc37719eeeedc48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151291070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf22d6bb19b4cc7029dd0330ad0aeabe0dc55f7ea2a392a3db16d196ba494f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2f02faf17c4ec382a59b54309f70d36d5833f9f68391665b51e0442d07e4e`  
		Last Modified: Fri, 14 Jun 2024 02:27:06 GMT  
		Size: 18.9 MB (18870625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49ec7ade1132963bc33d87cbdeb0aba5601c5bc17b10ad8b77f33b6a18cefdd`  
		Last Modified: Fri, 14 Jun 2024 02:27:05 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eac201c3c979f763764749fa3a02953658462d96cbea6aef28ebb0add7f1ade`  
		Last Modified: Fri, 14 Jun 2024 02:28:18 GMT  
		Size: 59.2 MB (59218065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f13455451fbd1dd0d3260d4cb103ab7c72ea1b928e911c0b979beea59e3dd1`  
		Last Modified: Fri, 14 Jun 2024 02:28:16 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:50632494559d86eac75ef9feac226e10281e640aaa348b2ec40d8083eb0f1220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6320698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f905f8db25306d4a35f65710fe5dc09d3e27c2982aee6e5823800bde7a96b8`

```dockerfile
```

-	Layers:
	-	`sha256:9bee7f9e0ee4210c7bc7ba5a7d5d53acc078cfbbba676e4936fdd86145fd5b7a`  
		Last Modified: Fri, 14 Jun 2024 02:28:17 GMT  
		Size: 6.3 MB (6305768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bda6498fa504623fae871fa8f4553f2f8137f985f6555067539db626456831c6`  
		Last Modified: Fri, 14 Jun 2024 02:28:16 GMT  
		Size: 14.9 KB (14930 bytes)  
		MIME: application/vnd.in-toto+json
