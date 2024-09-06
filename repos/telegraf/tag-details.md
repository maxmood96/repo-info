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
-	[`telegraf:1.31.3`](#telegraf1313)
-	[`telegraf:1.31.3-alpine`](#telegraf1313-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.29`

```console
$ docker pull telegraf@sha256:c3b08145370a7e8d0614ad8b883a14b7003bfa505be6d31023d75200e935e7d6
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
$ docker pull telegraf@sha256:f4d9d7ad23b2a77680b1c9fa1dd699ae20a246e1d06e204e2d4e5b26ca2e231f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155202665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9320b204c46151f087e6a621d8c18b800a630ae5fec4b4a69dde6d19358019c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e34bee3e9dfb94b241c408a3885bd2eaf9df612f399a4b9bbac9b02deb0b8f4`  
		Last Modified: Thu, 05 Sep 2024 00:10:16 GMT  
		Size: 18.9 MB (18947932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6db9612ba91c400649420e74ad64181e1f65efc1444cfd9135630bd185e706`  
		Last Modified: Thu, 05 Sep 2024 00:10:15 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d77d3df78f56e35bd17ff2ebdd3ecba0657670425b60d7fe68adfb66ab1011`  
		Last Modified: Thu, 05 Sep 2024 00:10:17 GMT  
		Size: 62.6 MB (62642471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f799bec7c14b00884f5bd359ff8d4ba4592c9378e64a8f78b1d0be34654c1f`  
		Last Modified: Thu, 05 Sep 2024 00:10:15 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:367cfdd57cf603f250a060884cdffdb8680bdcf9c697d532e4334e6601143951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbfef6ecba0d0da9ee1e8103c20e5d6822ba53da81cab92908315de9c547441`

```dockerfile
```

-	Layers:
	-	`sha256:671a31480b9a6e354c20be78c719a77652f04a1cf167495aa94643a61145c76b`  
		Last Modified: Thu, 05 Sep 2024 00:10:15 GMT  
		Size: 6.4 MB (6390702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71b9db3dbf3d83e659d7ec9954241c6a567e71b8540a000fed92d1754937575d`  
		Last Modified: Thu, 05 Sep 2024 00:10:15 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:fda34479267316b7859babd6795b31ecdbc219ad5c72a4cc12fb769afb6042fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142817975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed62ea938fef85e8ffbe7416493fd82d8df8ece2c2af789aa20e5d48fb312ca3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d3087a8c99ea87e011af172ffa23a565515328456f8ab3a8d3bbf65066c0c`  
		Last Modified: Wed, 04 Sep 2024 22:35:58 GMT  
		Size: 22.0 MB (21957240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2471024c37a9d8676e8df5926f303360da584aba5ac82efd6ccbca38498be25b`  
		Last Modified: Fri, 06 Sep 2024 04:13:38 GMT  
		Size: 17.7 MB (17724928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066224eb84e0d128bf5ea32e17bfb220f75986572b88390c53a8a0bc2b17ef56`  
		Last Modified: Fri, 06 Sep 2024 04:13:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c073b18dbb1239f1a640e1ac42eedbdb32372f82516b211a5d7d4f955e3db5b`  
		Last Modified: Fri, 06 Sep 2024 04:13:39 GMT  
		Size: 58.0 MB (57984965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12823ee9b84f1905d1702f0590a24fa7acd88e20db9aebb43b9130b9e52cfa7`  
		Last Modified: Fri, 06 Sep 2024 04:13:37 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:6132bc5fd4d122c2f18474bf3e3741812aead453c5627424c65489aef6f9997c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6399744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32cc264bb6a7929ad42d6723d14d8f17def6ba7b7d3573bfc32c706fa3f2891a`

```dockerfile
```

-	Layers:
	-	`sha256:11a013a307f5b8823389029589f76342135dd6ab964fc869db2928202a7139ec`  
		Last Modified: Fri, 06 Sep 2024 04:13:38 GMT  
		Size: 6.4 MB (6385341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2cdcf0d0836770b2ddd272769854024483463966b84dd137cd6b1504c22e329`  
		Last Modified: Fri, 06 Sep 2024 04:13:37 GMT  
		Size: 14.4 KB (14403 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:637e40bdad13e4b92b6076c478a385fce4fe8f2e51c3309e1602542aca5b1562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149034119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46014db129265e91cf094152775a99bab2c0b4841d13a9e2988ed28741fa650`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668d9f37d5cd85b4971a92ccf8bc4b94221b93af70278e14cb5467c3c57f2e40`  
		Last Modified: Thu, 05 Sep 2024 20:29:24 GMT  
		Size: 18.9 MB (18870684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebffecbaf4391db8de82e81b089f2632335d3b714f3ef8a2f0ffb1f4f9f21ff5`  
		Last Modified: Thu, 05 Sep 2024 20:29:23 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0651d0618a5f3bf91d614d1f5b2fbf2d804555ed5a36082992dc7eec00a5dce4`  
		Last Modified: Thu, 05 Sep 2024 20:29:25 GMT  
		Size: 57.0 MB (56981139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1181f1e2afd723fe10e2d13a167e4a3147f193dc0e24a2fc56df09492858b12`  
		Last Modified: Thu, 05 Sep 2024 20:29:23 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:6d4024db47d0d3bc909420db9cd6c74937374b29f1346f603690bf99d4c61653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff280020e08ccea79bc4fa3f9ddf71c3661b917376358950f59719afebd2b3c`

```dockerfile
```

-	Layers:
	-	`sha256:62243142ca6b86f9b95c53d4b70894d9682ba84111cbe4b5dc36329c6a64976e`  
		Last Modified: Thu, 05 Sep 2024 20:29:23 GMT  
		Size: 6.4 MB (6390625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3af1676347935c6678b82434e95e2643422bcbe31dc988b9fdb4473bbd7c0114`  
		Last Modified: Thu, 05 Sep 2024 20:29:23 GMT  
		Size: 14.6 KB (14617 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.29-alpine`

```console
$ docker pull telegraf@sha256:b1c2e442428e68f8879f094076237a8d71f9a7e1a569c992bf8c21069e443b18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.29-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:49f29125ad9233ff1bc5ea54024c4efd28e29a49e1b23b5e7108bb1130d32ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68516735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219c44bf7f97fbf6ec80259f34fc86d159a99275fe3aa51cccd8f6355de27764`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4132a9248b477c331526d071bc59ada3e5507ba7aa74b153a06aedf97735e3`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73efbc3eb4ae808763b36076a63493b677491ee7c62252fe659f77104dfbbd4`  
		Last Modified: Mon, 22 Jul 2024 23:04:26 GMT  
		Size: 2.5 MB (2451692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37a936729a8ef51dea490c7ccb55de9eda7ea83a4a113c02f3f1eb4385f720f`  
		Last Modified: Mon, 22 Jul 2024 23:04:26 GMT  
		Size: 62.4 MB (62441543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477c74b92f0f8849341c14b2292bc23755c4502d83f34369eb10f1f4550fec1d`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6f6e7b879e0e5bb41f6b43fb96aba99b8f3fe0398eb21426b85f02894332d281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1070504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4313fc3bf11bea29cee746e976c05d01de6caf9ca84c3f1e00a0e624887eb9`

```dockerfile
```

-	Layers:
	-	`sha256:200f9fb6ad3db368b251ba2339e4d956660225bc79c8a2208cea7e4984dafba9`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 1.1 MB (1055772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d263f2e91dc9c2336bd7ff18be122ca6af9fbae249c5b699921156bacccb2d`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 14.7 KB (14732 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5da5aa4566fb2bfd24bb52fff8400f836598193e97f0d3750c026498997cf86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63405473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c24924333978c8c70a609fc3c6223677e132506a48b6fc6a655714badb71f8b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da0d1ffb94d496286226e500ca461ae4c84a6368b8c23b64dfd72955579f654`  
		Last Modified: Wed, 24 Jul 2024 10:08:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c96666ef40bebea34c4984a3d34ddd3118468eb0087d117403688b0408735f6`  
		Last Modified: Wed, 24 Jul 2024 10:08:09 GMT  
		Size: 2.5 MB (2537424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0e59cfe1707ecb5ecfec7c63696c917ee3ed8bd002d14d40aa6866e4abce57`  
		Last Modified: Wed, 24 Jul 2024 10:08:11 GMT  
		Size: 56.8 MB (56780507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f633c760e44ef0d1301c842ab06c7fe9e073fd9e44e9448323f6d8cc98c7e728`  
		Last Modified: Wed, 24 Jul 2024 10:08:08 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:a19d2a7abcbe8fd4629bb91327edf9a69c41b23c49d1427b0ad8b3ec4b8fbabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1065651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b44f66460c3f5d9f8e20199bfda71fc87a3a256aa99f5146bd57fab863a8ab`

```dockerfile
```

-	Layers:
	-	`sha256:22c9cf8034785d65d1a08b743b8e27ce19acbec3f2b40a3fed684e6dc32fd0db`  
		Last Modified: Wed, 24 Jul 2024 10:08:09 GMT  
		Size: 1.1 MB (1050642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aad42f4d45df4450467ae8babb9e22d7018e72959826948ba41db26d5b13a00`  
		Last Modified: Wed, 24 Jul 2024 10:08:08 GMT  
		Size: 15.0 KB (15009 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.29.5`

```console
$ docker pull telegraf@sha256:c3b08145370a7e8d0614ad8b883a14b7003bfa505be6d31023d75200e935e7d6
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
$ docker pull telegraf@sha256:f4d9d7ad23b2a77680b1c9fa1dd699ae20a246e1d06e204e2d4e5b26ca2e231f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155202665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9320b204c46151f087e6a621d8c18b800a630ae5fec4b4a69dde6d19358019c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e34bee3e9dfb94b241c408a3885bd2eaf9df612f399a4b9bbac9b02deb0b8f4`  
		Last Modified: Thu, 05 Sep 2024 00:10:16 GMT  
		Size: 18.9 MB (18947932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6db9612ba91c400649420e74ad64181e1f65efc1444cfd9135630bd185e706`  
		Last Modified: Thu, 05 Sep 2024 00:10:15 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d77d3df78f56e35bd17ff2ebdd3ecba0657670425b60d7fe68adfb66ab1011`  
		Last Modified: Thu, 05 Sep 2024 00:10:17 GMT  
		Size: 62.6 MB (62642471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f799bec7c14b00884f5bd359ff8d4ba4592c9378e64a8f78b1d0be34654c1f`  
		Last Modified: Thu, 05 Sep 2024 00:10:15 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:367cfdd57cf603f250a060884cdffdb8680bdcf9c697d532e4334e6601143951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbfef6ecba0d0da9ee1e8103c20e5d6822ba53da81cab92908315de9c547441`

```dockerfile
```

-	Layers:
	-	`sha256:671a31480b9a6e354c20be78c719a77652f04a1cf167495aa94643a61145c76b`  
		Last Modified: Thu, 05 Sep 2024 00:10:15 GMT  
		Size: 6.4 MB (6390702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71b9db3dbf3d83e659d7ec9954241c6a567e71b8540a000fed92d1754937575d`  
		Last Modified: Thu, 05 Sep 2024 00:10:15 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29.5` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:fda34479267316b7859babd6795b31ecdbc219ad5c72a4cc12fb769afb6042fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142817975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed62ea938fef85e8ffbe7416493fd82d8df8ece2c2af789aa20e5d48fb312ca3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d3087a8c99ea87e011af172ffa23a565515328456f8ab3a8d3bbf65066c0c`  
		Last Modified: Wed, 04 Sep 2024 22:35:58 GMT  
		Size: 22.0 MB (21957240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2471024c37a9d8676e8df5926f303360da584aba5ac82efd6ccbca38498be25b`  
		Last Modified: Fri, 06 Sep 2024 04:13:38 GMT  
		Size: 17.7 MB (17724928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066224eb84e0d128bf5ea32e17bfb220f75986572b88390c53a8a0bc2b17ef56`  
		Last Modified: Fri, 06 Sep 2024 04:13:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c073b18dbb1239f1a640e1ac42eedbdb32372f82516b211a5d7d4f955e3db5b`  
		Last Modified: Fri, 06 Sep 2024 04:13:39 GMT  
		Size: 58.0 MB (57984965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12823ee9b84f1905d1702f0590a24fa7acd88e20db9aebb43b9130b9e52cfa7`  
		Last Modified: Fri, 06 Sep 2024 04:13:37 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:6132bc5fd4d122c2f18474bf3e3741812aead453c5627424c65489aef6f9997c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6399744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32cc264bb6a7929ad42d6723d14d8f17def6ba7b7d3573bfc32c706fa3f2891a`

```dockerfile
```

-	Layers:
	-	`sha256:11a013a307f5b8823389029589f76342135dd6ab964fc869db2928202a7139ec`  
		Last Modified: Fri, 06 Sep 2024 04:13:38 GMT  
		Size: 6.4 MB (6385341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2cdcf0d0836770b2ddd272769854024483463966b84dd137cd6b1504c22e329`  
		Last Modified: Fri, 06 Sep 2024 04:13:37 GMT  
		Size: 14.4 KB (14403 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29.5` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:637e40bdad13e4b92b6076c478a385fce4fe8f2e51c3309e1602542aca5b1562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149034119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46014db129265e91cf094152775a99bab2c0b4841d13a9e2988ed28741fa650`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668d9f37d5cd85b4971a92ccf8bc4b94221b93af70278e14cb5467c3c57f2e40`  
		Last Modified: Thu, 05 Sep 2024 20:29:24 GMT  
		Size: 18.9 MB (18870684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebffecbaf4391db8de82e81b089f2632335d3b714f3ef8a2f0ffb1f4f9f21ff5`  
		Last Modified: Thu, 05 Sep 2024 20:29:23 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0651d0618a5f3bf91d614d1f5b2fbf2d804555ed5a36082992dc7eec00a5dce4`  
		Last Modified: Thu, 05 Sep 2024 20:29:25 GMT  
		Size: 57.0 MB (56981139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1181f1e2afd723fe10e2d13a167e4a3147f193dc0e24a2fc56df09492858b12`  
		Last Modified: Thu, 05 Sep 2024 20:29:23 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:6d4024db47d0d3bc909420db9cd6c74937374b29f1346f603690bf99d4c61653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff280020e08ccea79bc4fa3f9ddf71c3661b917376358950f59719afebd2b3c`

```dockerfile
```

-	Layers:
	-	`sha256:62243142ca6b86f9b95c53d4b70894d9682ba84111cbe4b5dc36329c6a64976e`  
		Last Modified: Thu, 05 Sep 2024 20:29:23 GMT  
		Size: 6.4 MB (6390625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3af1676347935c6678b82434e95e2643422bcbe31dc988b9fdb4473bbd7c0114`  
		Last Modified: Thu, 05 Sep 2024 20:29:23 GMT  
		Size: 14.6 KB (14617 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.29.5-alpine`

```console
$ docker pull telegraf@sha256:b1c2e442428e68f8879f094076237a8d71f9a7e1a569c992bf8c21069e443b18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.29.5-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:49f29125ad9233ff1bc5ea54024c4efd28e29a49e1b23b5e7108bb1130d32ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68516735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219c44bf7f97fbf6ec80259f34fc86d159a99275fe3aa51cccd8f6355de27764`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4132a9248b477c331526d071bc59ada3e5507ba7aa74b153a06aedf97735e3`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73efbc3eb4ae808763b36076a63493b677491ee7c62252fe659f77104dfbbd4`  
		Last Modified: Mon, 22 Jul 2024 23:04:26 GMT  
		Size: 2.5 MB (2451692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37a936729a8ef51dea490c7ccb55de9eda7ea83a4a113c02f3f1eb4385f720f`  
		Last Modified: Mon, 22 Jul 2024 23:04:26 GMT  
		Size: 62.4 MB (62441543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477c74b92f0f8849341c14b2292bc23755c4502d83f34369eb10f1f4550fec1d`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6f6e7b879e0e5bb41f6b43fb96aba99b8f3fe0398eb21426b85f02894332d281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1070504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4313fc3bf11bea29cee746e976c05d01de6caf9ca84c3f1e00a0e624887eb9`

```dockerfile
```

-	Layers:
	-	`sha256:200f9fb6ad3db368b251ba2339e4d956660225bc79c8a2208cea7e4984dafba9`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 1.1 MB (1055772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d263f2e91dc9c2336bd7ff18be122ca6af9fbae249c5b699921156bacccb2d`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 14.7 KB (14732 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29.5-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5da5aa4566fb2bfd24bb52fff8400f836598193e97f0d3750c026498997cf86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63405473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c24924333978c8c70a609fc3c6223677e132506a48b6fc6a655714badb71f8b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da0d1ffb94d496286226e500ca461ae4c84a6368b8c23b64dfd72955579f654`  
		Last Modified: Wed, 24 Jul 2024 10:08:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c96666ef40bebea34c4984a3d34ddd3118468eb0087d117403688b0408735f6`  
		Last Modified: Wed, 24 Jul 2024 10:08:09 GMT  
		Size: 2.5 MB (2537424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0e59cfe1707ecb5ecfec7c63696c917ee3ed8bd002d14d40aa6866e4abce57`  
		Last Modified: Wed, 24 Jul 2024 10:08:11 GMT  
		Size: 56.8 MB (56780507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f633c760e44ef0d1301c842ab06c7fe9e073fd9e44e9448323f6d8cc98c7e728`  
		Last Modified: Wed, 24 Jul 2024 10:08:08 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:a19d2a7abcbe8fd4629bb91327edf9a69c41b23c49d1427b0ad8b3ec4b8fbabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1065651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b44f66460c3f5d9f8e20199bfda71fc87a3a256aa99f5146bd57fab863a8ab`

```dockerfile
```

-	Layers:
	-	`sha256:22c9cf8034785d65d1a08b743b8e27ce19acbec3f2b40a3fed684e6dc32fd0db`  
		Last Modified: Wed, 24 Jul 2024 10:08:09 GMT  
		Size: 1.1 MB (1050642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aad42f4d45df4450467ae8babb9e22d7018e72959826948ba41db26d5b13a00`  
		Last Modified: Wed, 24 Jul 2024 10:08:08 GMT  
		Size: 15.0 KB (15009 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30`

```console
$ docker pull telegraf@sha256:a53dc04d54bf1838844d0eed1bc19b34a7c443e2f57e54d01aceb96cfad5c0ab
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
$ docker pull telegraf@sha256:28e631482187445c106b9e96b694513c6a459a78de2dcc85fd62ff63b4636956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155326600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38102f5223dcd40ce6fb93fdfaf8b7175d44f79c6ae47fa4ff0bbf4395b83946`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5fe1e25e5e16980547caedd50c7b20e0880c649b6d158f7d363d5666239c14`  
		Last Modified: Thu, 05 Sep 2024 00:10:17 GMT  
		Size: 18.9 MB (18947882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e913cba1f618d3edc2997765c47e880d5e3161a45940d8a2fc7eb4bac4ce6e1`  
		Last Modified: Thu, 05 Sep 2024 00:10:16 GMT  
		Size: 1.8 KB (1777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58e0ee0c5c5c370a1ee674c2b05487a76cdc68cff92dcc545946d8c63a32737`  
		Last Modified: Thu, 05 Sep 2024 00:10:17 GMT  
		Size: 62.8 MB (62766460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3f2a38c68f78fb772cba68bbb7d8891d830c80e33fbb49f6db043dd90c11e4`  
		Last Modified: Thu, 05 Sep 2024 00:10:16 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:4cca2585ee2542c20d75f3a785dbe3b51d0917c059e27ca7ee6e463bc1d24c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71697ebfac21a5a2c1bb256b91e4372b28e5d06fe20c58bd8ff956cb97a5691a`

```dockerfile
```

-	Layers:
	-	`sha256:2f850e44431e313e6525b8c7d24a6bf79e8262ee2159c049a8711ab8649f9a5f`  
		Last Modified: Thu, 05 Sep 2024 00:10:17 GMT  
		Size: 6.4 MB (6391125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4488303cf8989475ee2b80cd4f3a03b6c91532802cc123291bda9e67d9bce17`  
		Last Modified: Thu, 05 Sep 2024 00:10:16 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:f05effb03b49c0c0d05ced52972a838f2e6c79989014d4772c4db262aa14dc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143045678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b500c038145ddaa133aa26d8e33e5f4186585dc5476bb6c8087849b951cf4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d3087a8c99ea87e011af172ffa23a565515328456f8ab3a8d3bbf65066c0c`  
		Last Modified: Wed, 04 Sep 2024 22:35:58 GMT  
		Size: 22.0 MB (21957240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2471024c37a9d8676e8df5926f303360da584aba5ac82efd6ccbca38498be25b`  
		Last Modified: Fri, 06 Sep 2024 04:13:38 GMT  
		Size: 17.7 MB (17724928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066224eb84e0d128bf5ea32e17bfb220f75986572b88390c53a8a0bc2b17ef56`  
		Last Modified: Fri, 06 Sep 2024 04:13:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52188c75f4a5687bd9bc4c34dc328205e1c5e274aeee1f895582b275d7dd663`  
		Last Modified: Fri, 06 Sep 2024 04:14:31 GMT  
		Size: 58.2 MB (58212668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22b854385bf50ed860f403d2065d5ee32b7fb2bee63b9d96372382798b4b497`  
		Last Modified: Fri, 06 Sep 2024 04:14:29 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:116892becfa0226a50610d19c0a2dae6d44ff8741c68c3017d44aadd0366d812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e86aab1758e57f673f61f0a07cce5e0a26fe422756d22c0285f507a553cf22e`

```dockerfile
```

-	Layers:
	-	`sha256:8af1be2a1e4aa6e2c5a54bdc6717126e9c42c3175cfe94bd3b3b148807ab836c`  
		Last Modified: Fri, 06 Sep 2024 04:14:29 GMT  
		Size: 6.4 MB (6385764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58de8733eb94a9f61f5f00158fe4d102257d16e65b63a816eb2487a879508feb`  
		Last Modified: Fri, 06 Sep 2024 04:14:29 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6eb5bf74b815483d6f01c55cc37fddbf7d0e41940f4483e7bd0f5cf205dcafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149176241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f91bf38277511d0cf3b2d595cf698b20124a79931d62d7fa83ed580f8bae3b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668d9f37d5cd85b4971a92ccf8bc4b94221b93af70278e14cb5467c3c57f2e40`  
		Last Modified: Thu, 05 Sep 2024 20:29:24 GMT  
		Size: 18.9 MB (18870684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebffecbaf4391db8de82e81b089f2632335d3b714f3ef8a2f0ffb1f4f9f21ff5`  
		Last Modified: Thu, 05 Sep 2024 20:29:23 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c37a04b72693a4ce19ead500adc2381a4198b28421553a250042421bf603f98`  
		Last Modified: Thu, 05 Sep 2024 20:30:01 GMT  
		Size: 57.1 MB (57123258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8eb953e2c6279ceeec759b9069371dd75db48647bf1c3559d33177bb76bdb6`  
		Last Modified: Thu, 05 Sep 2024 20:29:59 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:bdd62e59fd3da068bbc2c03ad04ac0a7971b209fd7fd2c018d75ce339a38a8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c739da24d2d085f98204025efe17872eca9a1b935e768e3f6062667af66cfe2`

```dockerfile
```

-	Layers:
	-	`sha256:255d533807c85ed4559e20f18e3fc88f7e84e44f46c7d4af075111b4d7fb28de`  
		Last Modified: Thu, 05 Sep 2024 20:30:00 GMT  
		Size: 6.4 MB (6391048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26e3bd966d1f21ca961d47a22790f1587b4551db54db930b48891b140552d337`  
		Last Modified: Thu, 05 Sep 2024 20:29:59 GMT  
		Size: 14.6 KB (14617 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30-alpine`

```console
$ docker pull telegraf@sha256:97bb530cc385132152f0f171db0514dd3b852d6f1529f135de0d1c3ed4a64805
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:fcfe5222366ad62f02e065f1a69e45bce3bdc64e7cc6bcc20dd5f5ea12eb3977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68644019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242ce2c4f74738cd111a37d48992142573863a657f5421e6429e62662fe350da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc469e64f8855e42c6d4c6f121d649ce80b1b57b520030009bdb799aaf7b6d3`  
		Last Modified: Mon, 22 Jul 2024 23:04:33 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd1dd2aea95e4d6aaeb5eadb1505da9fa8ba75ed038b99116d1289d3ee3607e`  
		Last Modified: Mon, 22 Jul 2024 23:04:33 GMT  
		Size: 2.5 MB (2451682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da5b95773c156c402ef1eaaf6796f414895775753500372be983f0dc9d1d0ad`  
		Last Modified: Mon, 22 Jul 2024 23:04:34 GMT  
		Size: 62.6 MB (62568841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32432b32d0336088c3d13e71d5f2557b2fec10426fcfbd387f37801d9a94865b`  
		Last Modified: Mon, 22 Jul 2024 23:04:33 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6e5a535211e37ba0525e30ae5b7005cffd5005998e7ce1cfaed15f200eeffd88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1070929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043244b274180f906f2a190fa8d7d09cbe1b5019f3de0040c8cfff6cf38cdc49`

```dockerfile
```

-	Layers:
	-	`sha256:47672bde33a0416036b3df7aa8668fc62f2d1b877370d59b5ca3a9e1118e1e0d`  
		Last Modified: Mon, 22 Jul 2024 23:04:33 GMT  
		Size: 1.1 MB (1056195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3753d4298e51b5ffd45bfc070c77a5b4f56235122d929b090b405de0e4fd9aa`  
		Last Modified: Mon, 22 Jul 2024 23:04:33 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:75a9c7f73eedd98dc2b6a64d5e280a846580396dbf9beb921d86e186cd328313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63545852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e783d7f3d1a9a6923de67a97257eb420d2f5a3363f798f2c3bb1eedff90488`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da0d1ffb94d496286226e500ca461ae4c84a6368b8c23b64dfd72955579f654`  
		Last Modified: Wed, 24 Jul 2024 10:08:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c96666ef40bebea34c4984a3d34ddd3118468eb0087d117403688b0408735f6`  
		Last Modified: Wed, 24 Jul 2024 10:08:09 GMT  
		Size: 2.5 MB (2537424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e8a5942cbf5e0ef4d4255f119ce9d09d2c12a398538968aa5e78e2776d217a`  
		Last Modified: Wed, 24 Jul 2024 10:09:20 GMT  
		Size: 56.9 MB (56920887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474ac264b7008a9fabe6524487bd7bf820471fcb7bb5c600987ec44467b4d449`  
		Last Modified: Wed, 24 Jul 2024 10:09:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:f9f7a61706ac67a335a92fa5448f8686290e0c1ce3689a186a08b620e16b3391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1066074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3486c7c0fa924d31507d7209b6055436fa9328a1f9bc101377f671ab00066071`

```dockerfile
```

-	Layers:
	-	`sha256:42bff7dffe23c1a81e044f9a8c3f5d35be7f93cba815e4da644691450f121e3a`  
		Last Modified: Wed, 24 Jul 2024 10:09:19 GMT  
		Size: 1.1 MB (1051065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d0280828ab5dc2c7606151e8005b003e9dd82e13f11311ad0775a53fc7161d`  
		Last Modified: Wed, 24 Jul 2024 10:09:18 GMT  
		Size: 15.0 KB (15009 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30.3`

```console
$ docker pull telegraf@sha256:a53dc04d54bf1838844d0eed1bc19b34a7c443e2f57e54d01aceb96cfad5c0ab
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
$ docker pull telegraf@sha256:28e631482187445c106b9e96b694513c6a459a78de2dcc85fd62ff63b4636956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155326600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38102f5223dcd40ce6fb93fdfaf8b7175d44f79c6ae47fa4ff0bbf4395b83946`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5fe1e25e5e16980547caedd50c7b20e0880c649b6d158f7d363d5666239c14`  
		Last Modified: Thu, 05 Sep 2024 00:10:17 GMT  
		Size: 18.9 MB (18947882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e913cba1f618d3edc2997765c47e880d5e3161a45940d8a2fc7eb4bac4ce6e1`  
		Last Modified: Thu, 05 Sep 2024 00:10:16 GMT  
		Size: 1.8 KB (1777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58e0ee0c5c5c370a1ee674c2b05487a76cdc68cff92dcc545946d8c63a32737`  
		Last Modified: Thu, 05 Sep 2024 00:10:17 GMT  
		Size: 62.8 MB (62766460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3f2a38c68f78fb772cba68bbb7d8891d830c80e33fbb49f6db043dd90c11e4`  
		Last Modified: Thu, 05 Sep 2024 00:10:16 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:4cca2585ee2542c20d75f3a785dbe3b51d0917c059e27ca7ee6e463bc1d24c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71697ebfac21a5a2c1bb256b91e4372b28e5d06fe20c58bd8ff956cb97a5691a`

```dockerfile
```

-	Layers:
	-	`sha256:2f850e44431e313e6525b8c7d24a6bf79e8262ee2159c049a8711ab8649f9a5f`  
		Last Modified: Thu, 05 Sep 2024 00:10:17 GMT  
		Size: 6.4 MB (6391125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4488303cf8989475ee2b80cd4f3a03b6c91532802cc123291bda9e67d9bce17`  
		Last Modified: Thu, 05 Sep 2024 00:10:16 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:f05effb03b49c0c0d05ced52972a838f2e6c79989014d4772c4db262aa14dc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143045678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b500c038145ddaa133aa26d8e33e5f4186585dc5476bb6c8087849b951cf4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d3087a8c99ea87e011af172ffa23a565515328456f8ab3a8d3bbf65066c0c`  
		Last Modified: Wed, 04 Sep 2024 22:35:58 GMT  
		Size: 22.0 MB (21957240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2471024c37a9d8676e8df5926f303360da584aba5ac82efd6ccbca38498be25b`  
		Last Modified: Fri, 06 Sep 2024 04:13:38 GMT  
		Size: 17.7 MB (17724928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066224eb84e0d128bf5ea32e17bfb220f75986572b88390c53a8a0bc2b17ef56`  
		Last Modified: Fri, 06 Sep 2024 04:13:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52188c75f4a5687bd9bc4c34dc328205e1c5e274aeee1f895582b275d7dd663`  
		Last Modified: Fri, 06 Sep 2024 04:14:31 GMT  
		Size: 58.2 MB (58212668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22b854385bf50ed860f403d2065d5ee32b7fb2bee63b9d96372382798b4b497`  
		Last Modified: Fri, 06 Sep 2024 04:14:29 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:116892becfa0226a50610d19c0a2dae6d44ff8741c68c3017d44aadd0366d812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e86aab1758e57f673f61f0a07cce5e0a26fe422756d22c0285f507a553cf22e`

```dockerfile
```

-	Layers:
	-	`sha256:8af1be2a1e4aa6e2c5a54bdc6717126e9c42c3175cfe94bd3b3b148807ab836c`  
		Last Modified: Fri, 06 Sep 2024 04:14:29 GMT  
		Size: 6.4 MB (6385764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58de8733eb94a9f61f5f00158fe4d102257d16e65b63a816eb2487a879508feb`  
		Last Modified: Fri, 06 Sep 2024 04:14:29 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6eb5bf74b815483d6f01c55cc37fddbf7d0e41940f4483e7bd0f5cf205dcafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149176241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f91bf38277511d0cf3b2d595cf698b20124a79931d62d7fa83ed580f8bae3b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668d9f37d5cd85b4971a92ccf8bc4b94221b93af70278e14cb5467c3c57f2e40`  
		Last Modified: Thu, 05 Sep 2024 20:29:24 GMT  
		Size: 18.9 MB (18870684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebffecbaf4391db8de82e81b089f2632335d3b714f3ef8a2f0ffb1f4f9f21ff5`  
		Last Modified: Thu, 05 Sep 2024 20:29:23 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c37a04b72693a4ce19ead500adc2381a4198b28421553a250042421bf603f98`  
		Last Modified: Thu, 05 Sep 2024 20:30:01 GMT  
		Size: 57.1 MB (57123258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8eb953e2c6279ceeec759b9069371dd75db48647bf1c3559d33177bb76bdb6`  
		Last Modified: Thu, 05 Sep 2024 20:29:59 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:bdd62e59fd3da068bbc2c03ad04ac0a7971b209fd7fd2c018d75ce339a38a8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c739da24d2d085f98204025efe17872eca9a1b935e768e3f6062667af66cfe2`

```dockerfile
```

-	Layers:
	-	`sha256:255d533807c85ed4559e20f18e3fc88f7e84e44f46c7d4af075111b4d7fb28de`  
		Last Modified: Thu, 05 Sep 2024 20:30:00 GMT  
		Size: 6.4 MB (6391048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26e3bd966d1f21ca961d47a22790f1587b4551db54db930b48891b140552d337`  
		Last Modified: Thu, 05 Sep 2024 20:29:59 GMT  
		Size: 14.6 KB (14617 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30.3-alpine`

```console
$ docker pull telegraf@sha256:97bb530cc385132152f0f171db0514dd3b852d6f1529f135de0d1c3ed4a64805
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:fcfe5222366ad62f02e065f1a69e45bce3bdc64e7cc6bcc20dd5f5ea12eb3977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68644019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242ce2c4f74738cd111a37d48992142573863a657f5421e6429e62662fe350da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc469e64f8855e42c6d4c6f121d649ce80b1b57b520030009bdb799aaf7b6d3`  
		Last Modified: Mon, 22 Jul 2024 23:04:33 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd1dd2aea95e4d6aaeb5eadb1505da9fa8ba75ed038b99116d1289d3ee3607e`  
		Last Modified: Mon, 22 Jul 2024 23:04:33 GMT  
		Size: 2.5 MB (2451682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da5b95773c156c402ef1eaaf6796f414895775753500372be983f0dc9d1d0ad`  
		Last Modified: Mon, 22 Jul 2024 23:04:34 GMT  
		Size: 62.6 MB (62568841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32432b32d0336088c3d13e71d5f2557b2fec10426fcfbd387f37801d9a94865b`  
		Last Modified: Mon, 22 Jul 2024 23:04:33 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6e5a535211e37ba0525e30ae5b7005cffd5005998e7ce1cfaed15f200eeffd88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1070929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043244b274180f906f2a190fa8d7d09cbe1b5019f3de0040c8cfff6cf38cdc49`

```dockerfile
```

-	Layers:
	-	`sha256:47672bde33a0416036b3df7aa8668fc62f2d1b877370d59b5ca3a9e1118e1e0d`  
		Last Modified: Mon, 22 Jul 2024 23:04:33 GMT  
		Size: 1.1 MB (1056195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3753d4298e51b5ffd45bfc070c77a5b4f56235122d929b090b405de0e4fd9aa`  
		Last Modified: Mon, 22 Jul 2024 23:04:33 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:75a9c7f73eedd98dc2b6a64d5e280a846580396dbf9beb921d86e186cd328313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63545852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e783d7f3d1a9a6923de67a97257eb420d2f5a3363f798f2c3bb1eedff90488`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da0d1ffb94d496286226e500ca461ae4c84a6368b8c23b64dfd72955579f654`  
		Last Modified: Wed, 24 Jul 2024 10:08:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c96666ef40bebea34c4984a3d34ddd3118468eb0087d117403688b0408735f6`  
		Last Modified: Wed, 24 Jul 2024 10:08:09 GMT  
		Size: 2.5 MB (2537424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e8a5942cbf5e0ef4d4255f119ce9d09d2c12a398538968aa5e78e2776d217a`  
		Last Modified: Wed, 24 Jul 2024 10:09:20 GMT  
		Size: 56.9 MB (56920887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474ac264b7008a9fabe6524487bd7bf820471fcb7bb5c600987ec44467b4d449`  
		Last Modified: Wed, 24 Jul 2024 10:09:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:f9f7a61706ac67a335a92fa5448f8686290e0c1ce3689a186a08b620e16b3391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1066074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3486c7c0fa924d31507d7209b6055436fa9328a1f9bc101377f671ab00066071`

```dockerfile
```

-	Layers:
	-	`sha256:42bff7dffe23c1a81e044f9a8c3f5d35be7f93cba815e4da644691450f121e3a`  
		Last Modified: Wed, 24 Jul 2024 10:09:19 GMT  
		Size: 1.1 MB (1051065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d0280828ab5dc2c7606151e8005b003e9dd82e13f11311ad0775a53fc7161d`  
		Last Modified: Wed, 24 Jul 2024 10:09:18 GMT  
		Size: 15.0 KB (15009 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31`

```console
$ docker pull telegraf@sha256:6b0d623c54754958fed356d2af239de21dcf7c95d63b76298d0cd70df79cc719
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
$ docker pull telegraf@sha256:848201b0601513122f567a6b690b5ef84abbb38e78ca461d1c1d3d7465691d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158845739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fffb7e682428f97779fdee3f4c44d062de6da9ba4a754a0f3b3f0ecaf87052e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1066a73fdebbd8509b0fbd880801443768b4750d690ca219c8b9d888d08cea7a`  
		Last Modified: Thu, 05 Sep 2024 00:10:35 GMT  
		Size: 18.9 MB (18948043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf0d785494ea7e25050b72827fc072abfd4b7fe79f6280ab96e14aeaca30db5`  
		Last Modified: Thu, 05 Sep 2024 00:10:34 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc9a8f028d52c0c5ddee1420162f92bd41b6727e097b984eb451eb214eee291`  
		Last Modified: Thu, 05 Sep 2024 00:10:37 GMT  
		Size: 66.3 MB (66285430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731f82814c1acde235e379eba61a89f2dc715b2532c9befd3bea6ec14a343d6d`  
		Last Modified: Thu, 05 Sep 2024 00:10:34 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:2a62640c6c53a3deea2ef3848d66f2e39ff8674da9e55d8b4114f7ddc9a1b3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6414261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918df84176f50aafdffbaf9d74b47b13d06f953baa2ee094940feaee085d7789`

```dockerfile
```

-	Layers:
	-	`sha256:bafe9f2fe594387d37cf2072bafcbf85f9eab2d608604404a7f9a040c6066f58`  
		Last Modified: Thu, 05 Sep 2024 00:10:34 GMT  
		Size: 6.4 MB (6399635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34649d9f158dee042fcbc66db861e7c1d57ff2b5b34bcc9de2c4ec8a174f94a9`  
		Last Modified: Thu, 05 Sep 2024 00:10:34 GMT  
		Size: 14.6 KB (14626 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:18ee367acddef6bc891ae4edf18785ecf75d7ce476c9c559baa36d06e58a27a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146505314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25293e4cc020419014b3b42171172513fa043eec52e3c0ffce53735e5225f25c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d3087a8c99ea87e011af172ffa23a565515328456f8ab3a8d3bbf65066c0c`  
		Last Modified: Wed, 04 Sep 2024 22:35:58 GMT  
		Size: 22.0 MB (21957240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2471024c37a9d8676e8df5926f303360da584aba5ac82efd6ccbca38498be25b`  
		Last Modified: Fri, 06 Sep 2024 04:13:38 GMT  
		Size: 17.7 MB (17724928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066224eb84e0d128bf5ea32e17bfb220f75986572b88390c53a8a0bc2b17ef56`  
		Last Modified: Fri, 06 Sep 2024 04:13:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3c9d6294e1c254e8a1d2a607df481760326190fff94300fa2b1d17f2335d13`  
		Last Modified: Fri, 06 Sep 2024 04:15:24 GMT  
		Size: 61.7 MB (61672302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7f4240d21c93e9e018996dd6319e9f18d5a6945d426d7995704ec1147b020f`  
		Last Modified: Fri, 06 Sep 2024 04:15:22 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:06658911b19998c722152953ae140cd59e9be6fd7d10efce48dc0be4c7549c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6409793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4730e2caa764a7456f82d7aaf02889c1fb114375c44898e0e7ebb1e8ccaa545`

```dockerfile
```

-	Layers:
	-	`sha256:d085dedcd5c89dd8eefb985468610d2107cd63b9aa471a307b8354cc6af69130`  
		Last Modified: Fri, 06 Sep 2024 04:15:22 GMT  
		Size: 6.4 MB (6395079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82367f0d56606fb3e59e30b9981ed3d4e28e4c5de2f50c2fd66323b3c0a6d2d6`  
		Last Modified: Fri, 06 Sep 2024 04:15:22 GMT  
		Size: 14.7 KB (14714 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8ab8223cf42035683913aac257a4a0bef2da657b9a1f9b6b82a25230789fe10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152430806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055cf6c735c777083bd2806758a5af6697ab8684839606797b01332fd990feaa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668d9f37d5cd85b4971a92ccf8bc4b94221b93af70278e14cb5467c3c57f2e40`  
		Last Modified: Thu, 05 Sep 2024 20:29:24 GMT  
		Size: 18.9 MB (18870684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebffecbaf4391db8de82e81b089f2632335d3b714f3ef8a2f0ffb1f4f9f21ff5`  
		Last Modified: Thu, 05 Sep 2024 20:29:23 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf67612c42ba4c3ddb2bead89893da493bfd4478ba8584c8aa801a1a03c15b2`  
		Last Modified: Thu, 05 Sep 2024 20:30:43 GMT  
		Size: 60.4 MB (60377823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2152361d4908d72b62e8f65c25d07c190373440ba8f6b1033bc179be36d61e`  
		Last Modified: Thu, 05 Sep 2024 20:30:40 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:c3bffc37d556833052d636c8f9bf84c7db5f8a05ed0fe726ad051efba5fa8c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6416093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d499c67e7614b99b5c1c3ba15e51faac1bb56afea1fe613917f87f83dedd605`

```dockerfile
```

-	Layers:
	-	`sha256:e93c666dc1eca05258ba8a07ca0a3c90bbe4ab804a34dff235618ba04df14762`  
		Last Modified: Thu, 05 Sep 2024 20:30:41 GMT  
		Size: 6.4 MB (6401162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638663a2967e62ad6afc5b5b1083c7444dd5337c26e7067446f380abd56b8279`  
		Last Modified: Thu, 05 Sep 2024 20:30:40 GMT  
		Size: 14.9 KB (14931 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31-alpine`

```console
$ docker pull telegraf@sha256:9f52c5e1ca21a0eae1d05d758904df4c8bc1aff7eca4f97f3134742347c45daa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:d5d40ac565ecd26025ac9dd3fab0b8b3805a30cb8a8081e63e181f1b5cbf5c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72153144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88347c5ad7332594511126fe4c31e0db9a6dbfe1788ee941a50201a690cef122`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
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
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d96f79ba57e9bfdec7d9011576873c104f3be71e5b9240a1a8a126194a5a353`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d395b78b6ead8e6044004820ae7bb2ff48550d479eb3e6484f3c4594e6fe2bde`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 2.5 MB (2451711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbac422ca05692ac2502b016ef8bcbcba0cd65cd1bf87743c4baf08df4cbade1`  
		Last Modified: Mon, 12 Aug 2024 16:56:25 GMT  
		Size: 66.1 MB (66077933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc81c539d4116f636265e92a3b4330bc0b8b967253c0253c1f4bdfe209f089`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6946f808a772b2069f9759e6c35ca0e87c5750c21a1e242fba4c701381f18101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1079739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becd149d7b4943a02c3280c8f2d1884e4431aa94421e18c6b8f607f918bff33e`

```dockerfile
```

-	Layers:
	-	`sha256:71031225d67afa7f4e6359dc25d8e3462d1a3a88782584d662b461ffea0c62fb`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 1.1 MB (1064703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e152629635514b1bf072f80775060dafa431cbea6e70f7207d5e73a26b779eb8`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:945cf4c3e4f70222f67e1430fce86cf2e8759a8a0f57587953e8793bb9051a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66796515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905ac98277de19213d3346e8a85b6402c0ce8eaccd17a0a2c5aa779d211304bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
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
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1de5eaf2a1972853375a025a0309628552446763159c73f9fb971eedad7e97c`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a243aa4517b40d42c094f617342384531a20fde653e4378bdd44eec4445eeaa6`  
		Last Modified: Mon, 12 Aug 2024 17:49:47 GMT  
		Size: 2.5 MB (2537428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a3518efde0102230b00c4ee09fbc1dfdb976577cf2a7d5b83a69e7b43522bd`  
		Last Modified: Mon, 12 Aug 2024 17:49:48 GMT  
		Size: 60.2 MB (60171546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5484c079133258c45d9ec7d30cc2226199c8e5aa7696769a347a3cf4e8049c`  
		Last Modified: Mon, 12 Aug 2024 17:49:46 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4f5a831694c31de36d0073720172bc80c502074299db482033b7cdf7db62f56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1076501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb9eb546251758114a08c15fe33944dbfe034e7e3dc03d31e8933901a115dcb`

```dockerfile
```

-	Layers:
	-	`sha256:c292ce24841951032243ce2c3c4e54e5460412a18a74a5c87892e3a25132dcdb`  
		Last Modified: Mon, 12 Aug 2024 17:49:46 GMT  
		Size: 1.1 MB (1061177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ef0ee15b6c05bd92cdff902bfc9dca23eb9922078481588bb06a55df4031c15`  
		Last Modified: Mon, 12 Aug 2024 17:49:46 GMT  
		Size: 15.3 KB (15324 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.3`

```console
$ docker pull telegraf@sha256:6b0d623c54754958fed356d2af239de21dcf7c95d63b76298d0cd70df79cc719
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
$ docker pull telegraf@sha256:848201b0601513122f567a6b690b5ef84abbb38e78ca461d1c1d3d7465691d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158845739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fffb7e682428f97779fdee3f4c44d062de6da9ba4a754a0f3b3f0ecaf87052e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1066a73fdebbd8509b0fbd880801443768b4750d690ca219c8b9d888d08cea7a`  
		Last Modified: Thu, 05 Sep 2024 00:10:35 GMT  
		Size: 18.9 MB (18948043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf0d785494ea7e25050b72827fc072abfd4b7fe79f6280ab96e14aeaca30db5`  
		Last Modified: Thu, 05 Sep 2024 00:10:34 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc9a8f028d52c0c5ddee1420162f92bd41b6727e097b984eb451eb214eee291`  
		Last Modified: Thu, 05 Sep 2024 00:10:37 GMT  
		Size: 66.3 MB (66285430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731f82814c1acde235e379eba61a89f2dc715b2532c9befd3bea6ec14a343d6d`  
		Last Modified: Thu, 05 Sep 2024 00:10:34 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:2a62640c6c53a3deea2ef3848d66f2e39ff8674da9e55d8b4114f7ddc9a1b3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6414261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918df84176f50aafdffbaf9d74b47b13d06f953baa2ee094940feaee085d7789`

```dockerfile
```

-	Layers:
	-	`sha256:bafe9f2fe594387d37cf2072bafcbf85f9eab2d608604404a7f9a040c6066f58`  
		Last Modified: Thu, 05 Sep 2024 00:10:34 GMT  
		Size: 6.4 MB (6399635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34649d9f158dee042fcbc66db861e7c1d57ff2b5b34bcc9de2c4ec8a174f94a9`  
		Last Modified: Thu, 05 Sep 2024 00:10:34 GMT  
		Size: 14.6 KB (14626 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:18ee367acddef6bc891ae4edf18785ecf75d7ce476c9c559baa36d06e58a27a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146505314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25293e4cc020419014b3b42171172513fa043eec52e3c0ffce53735e5225f25c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d3087a8c99ea87e011af172ffa23a565515328456f8ab3a8d3bbf65066c0c`  
		Last Modified: Wed, 04 Sep 2024 22:35:58 GMT  
		Size: 22.0 MB (21957240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2471024c37a9d8676e8df5926f303360da584aba5ac82efd6ccbca38498be25b`  
		Last Modified: Fri, 06 Sep 2024 04:13:38 GMT  
		Size: 17.7 MB (17724928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066224eb84e0d128bf5ea32e17bfb220f75986572b88390c53a8a0bc2b17ef56`  
		Last Modified: Fri, 06 Sep 2024 04:13:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3c9d6294e1c254e8a1d2a607df481760326190fff94300fa2b1d17f2335d13`  
		Last Modified: Fri, 06 Sep 2024 04:15:24 GMT  
		Size: 61.7 MB (61672302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7f4240d21c93e9e018996dd6319e9f18d5a6945d426d7995704ec1147b020f`  
		Last Modified: Fri, 06 Sep 2024 04:15:22 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:06658911b19998c722152953ae140cd59e9be6fd7d10efce48dc0be4c7549c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6409793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4730e2caa764a7456f82d7aaf02889c1fb114375c44898e0e7ebb1e8ccaa545`

```dockerfile
```

-	Layers:
	-	`sha256:d085dedcd5c89dd8eefb985468610d2107cd63b9aa471a307b8354cc6af69130`  
		Last Modified: Fri, 06 Sep 2024 04:15:22 GMT  
		Size: 6.4 MB (6395079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82367f0d56606fb3e59e30b9981ed3d4e28e4c5de2f50c2fd66323b3c0a6d2d6`  
		Last Modified: Fri, 06 Sep 2024 04:15:22 GMT  
		Size: 14.7 KB (14714 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8ab8223cf42035683913aac257a4a0bef2da657b9a1f9b6b82a25230789fe10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152430806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055cf6c735c777083bd2806758a5af6697ab8684839606797b01332fd990feaa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668d9f37d5cd85b4971a92ccf8bc4b94221b93af70278e14cb5467c3c57f2e40`  
		Last Modified: Thu, 05 Sep 2024 20:29:24 GMT  
		Size: 18.9 MB (18870684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebffecbaf4391db8de82e81b089f2632335d3b714f3ef8a2f0ffb1f4f9f21ff5`  
		Last Modified: Thu, 05 Sep 2024 20:29:23 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf67612c42ba4c3ddb2bead89893da493bfd4478ba8584c8aa801a1a03c15b2`  
		Last Modified: Thu, 05 Sep 2024 20:30:43 GMT  
		Size: 60.4 MB (60377823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2152361d4908d72b62e8f65c25d07c190373440ba8f6b1033bc179be36d61e`  
		Last Modified: Thu, 05 Sep 2024 20:30:40 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:c3bffc37d556833052d636c8f9bf84c7db5f8a05ed0fe726ad051efba5fa8c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6416093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d499c67e7614b99b5c1c3ba15e51faac1bb56afea1fe613917f87f83dedd605`

```dockerfile
```

-	Layers:
	-	`sha256:e93c666dc1eca05258ba8a07ca0a3c90bbe4ab804a34dff235618ba04df14762`  
		Last Modified: Thu, 05 Sep 2024 20:30:41 GMT  
		Size: 6.4 MB (6401162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638663a2967e62ad6afc5b5b1083c7444dd5337c26e7067446f380abd56b8279`  
		Last Modified: Thu, 05 Sep 2024 20:30:40 GMT  
		Size: 14.9 KB (14931 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.3-alpine`

```console
$ docker pull telegraf@sha256:9f52c5e1ca21a0eae1d05d758904df4c8bc1aff7eca4f97f3134742347c45daa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:d5d40ac565ecd26025ac9dd3fab0b8b3805a30cb8a8081e63e181f1b5cbf5c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72153144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88347c5ad7332594511126fe4c31e0db9a6dbfe1788ee941a50201a690cef122`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
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
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d96f79ba57e9bfdec7d9011576873c104f3be71e5b9240a1a8a126194a5a353`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d395b78b6ead8e6044004820ae7bb2ff48550d479eb3e6484f3c4594e6fe2bde`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 2.5 MB (2451711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbac422ca05692ac2502b016ef8bcbcba0cd65cd1bf87743c4baf08df4cbade1`  
		Last Modified: Mon, 12 Aug 2024 16:56:25 GMT  
		Size: 66.1 MB (66077933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc81c539d4116f636265e92a3b4330bc0b8b967253c0253c1f4bdfe209f089`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6946f808a772b2069f9759e6c35ca0e87c5750c21a1e242fba4c701381f18101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1079739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becd149d7b4943a02c3280c8f2d1884e4431aa94421e18c6b8f607f918bff33e`

```dockerfile
```

-	Layers:
	-	`sha256:71031225d67afa7f4e6359dc25d8e3462d1a3a88782584d662b461ffea0c62fb`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 1.1 MB (1064703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e152629635514b1bf072f80775060dafa431cbea6e70f7207d5e73a26b779eb8`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:945cf4c3e4f70222f67e1430fce86cf2e8759a8a0f57587953e8793bb9051a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66796515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905ac98277de19213d3346e8a85b6402c0ce8eaccd17a0a2c5aa779d211304bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
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
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1de5eaf2a1972853375a025a0309628552446763159c73f9fb971eedad7e97c`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a243aa4517b40d42c094f617342384531a20fde653e4378bdd44eec4445eeaa6`  
		Last Modified: Mon, 12 Aug 2024 17:49:47 GMT  
		Size: 2.5 MB (2537428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a3518efde0102230b00c4ee09fbc1dfdb976577cf2a7d5b83a69e7b43522bd`  
		Last Modified: Mon, 12 Aug 2024 17:49:48 GMT  
		Size: 60.2 MB (60171546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5484c079133258c45d9ec7d30cc2226199c8e5aa7696769a347a3cf4e8049c`  
		Last Modified: Mon, 12 Aug 2024 17:49:46 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4f5a831694c31de36d0073720172bc80c502074299db482033b7cdf7db62f56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1076501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb9eb546251758114a08c15fe33944dbfe034e7e3dc03d31e8933901a115dcb`

```dockerfile
```

-	Layers:
	-	`sha256:c292ce24841951032243ce2c3c4e54e5460412a18a74a5c87892e3a25132dcdb`  
		Last Modified: Mon, 12 Aug 2024 17:49:46 GMT  
		Size: 1.1 MB (1061177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ef0ee15b6c05bd92cdff902bfc9dca23eb9922078481588bb06a55df4031c15`  
		Last Modified: Mon, 12 Aug 2024 17:49:46 GMT  
		Size: 15.3 KB (15324 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:9f52c5e1ca21a0eae1d05d758904df4c8bc1aff7eca4f97f3134742347c45daa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:d5d40ac565ecd26025ac9dd3fab0b8b3805a30cb8a8081e63e181f1b5cbf5c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72153144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88347c5ad7332594511126fe4c31e0db9a6dbfe1788ee941a50201a690cef122`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
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
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d96f79ba57e9bfdec7d9011576873c104f3be71e5b9240a1a8a126194a5a353`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d395b78b6ead8e6044004820ae7bb2ff48550d479eb3e6484f3c4594e6fe2bde`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 2.5 MB (2451711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbac422ca05692ac2502b016ef8bcbcba0cd65cd1bf87743c4baf08df4cbade1`  
		Last Modified: Mon, 12 Aug 2024 16:56:25 GMT  
		Size: 66.1 MB (66077933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc81c539d4116f636265e92a3b4330bc0b8b967253c0253c1f4bdfe209f089`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6946f808a772b2069f9759e6c35ca0e87c5750c21a1e242fba4c701381f18101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1079739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becd149d7b4943a02c3280c8f2d1884e4431aa94421e18c6b8f607f918bff33e`

```dockerfile
```

-	Layers:
	-	`sha256:71031225d67afa7f4e6359dc25d8e3462d1a3a88782584d662b461ffea0c62fb`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 1.1 MB (1064703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e152629635514b1bf072f80775060dafa431cbea6e70f7207d5e73a26b779eb8`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:945cf4c3e4f70222f67e1430fce86cf2e8759a8a0f57587953e8793bb9051a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66796515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905ac98277de19213d3346e8a85b6402c0ce8eaccd17a0a2c5aa779d211304bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
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
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1de5eaf2a1972853375a025a0309628552446763159c73f9fb971eedad7e97c`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a243aa4517b40d42c094f617342384531a20fde653e4378bdd44eec4445eeaa6`  
		Last Modified: Mon, 12 Aug 2024 17:49:47 GMT  
		Size: 2.5 MB (2537428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a3518efde0102230b00c4ee09fbc1dfdb976577cf2a7d5b83a69e7b43522bd`  
		Last Modified: Mon, 12 Aug 2024 17:49:48 GMT  
		Size: 60.2 MB (60171546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5484c079133258c45d9ec7d30cc2226199c8e5aa7696769a347a3cf4e8049c`  
		Last Modified: Mon, 12 Aug 2024 17:49:46 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4f5a831694c31de36d0073720172bc80c502074299db482033b7cdf7db62f56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1076501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb9eb546251758114a08c15fe33944dbfe034e7e3dc03d31e8933901a115dcb`

```dockerfile
```

-	Layers:
	-	`sha256:c292ce24841951032243ce2c3c4e54e5460412a18a74a5c87892e3a25132dcdb`  
		Last Modified: Mon, 12 Aug 2024 17:49:46 GMT  
		Size: 1.1 MB (1061177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ef0ee15b6c05bd92cdff902bfc9dca23eb9922078481588bb06a55df4031c15`  
		Last Modified: Mon, 12 Aug 2024 17:49:46 GMT  
		Size: 15.3 KB (15324 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:6b0d623c54754958fed356d2af239de21dcf7c95d63b76298d0cd70df79cc719
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
$ docker pull telegraf@sha256:848201b0601513122f567a6b690b5ef84abbb38e78ca461d1c1d3d7465691d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158845739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fffb7e682428f97779fdee3f4c44d062de6da9ba4a754a0f3b3f0ecaf87052e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1066a73fdebbd8509b0fbd880801443768b4750d690ca219c8b9d888d08cea7a`  
		Last Modified: Thu, 05 Sep 2024 00:10:35 GMT  
		Size: 18.9 MB (18948043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf0d785494ea7e25050b72827fc072abfd4b7fe79f6280ab96e14aeaca30db5`  
		Last Modified: Thu, 05 Sep 2024 00:10:34 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc9a8f028d52c0c5ddee1420162f92bd41b6727e097b984eb451eb214eee291`  
		Last Modified: Thu, 05 Sep 2024 00:10:37 GMT  
		Size: 66.3 MB (66285430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731f82814c1acde235e379eba61a89f2dc715b2532c9befd3bea6ec14a343d6d`  
		Last Modified: Thu, 05 Sep 2024 00:10:34 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:2a62640c6c53a3deea2ef3848d66f2e39ff8674da9e55d8b4114f7ddc9a1b3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6414261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918df84176f50aafdffbaf9d74b47b13d06f953baa2ee094940feaee085d7789`

```dockerfile
```

-	Layers:
	-	`sha256:bafe9f2fe594387d37cf2072bafcbf85f9eab2d608604404a7f9a040c6066f58`  
		Last Modified: Thu, 05 Sep 2024 00:10:34 GMT  
		Size: 6.4 MB (6399635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34649d9f158dee042fcbc66db861e7c1d57ff2b5b34bcc9de2c4ec8a174f94a9`  
		Last Modified: Thu, 05 Sep 2024 00:10:34 GMT  
		Size: 14.6 KB (14626 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:18ee367acddef6bc891ae4edf18785ecf75d7ce476c9c559baa36d06e58a27a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146505314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25293e4cc020419014b3b42171172513fa043eec52e3c0ffce53735e5225f25c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d3087a8c99ea87e011af172ffa23a565515328456f8ab3a8d3bbf65066c0c`  
		Last Modified: Wed, 04 Sep 2024 22:35:58 GMT  
		Size: 22.0 MB (21957240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2471024c37a9d8676e8df5926f303360da584aba5ac82efd6ccbca38498be25b`  
		Last Modified: Fri, 06 Sep 2024 04:13:38 GMT  
		Size: 17.7 MB (17724928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066224eb84e0d128bf5ea32e17bfb220f75986572b88390c53a8a0bc2b17ef56`  
		Last Modified: Fri, 06 Sep 2024 04:13:37 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3c9d6294e1c254e8a1d2a607df481760326190fff94300fa2b1d17f2335d13`  
		Last Modified: Fri, 06 Sep 2024 04:15:24 GMT  
		Size: 61.7 MB (61672302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7f4240d21c93e9e018996dd6319e9f18d5a6945d426d7995704ec1147b020f`  
		Last Modified: Fri, 06 Sep 2024 04:15:22 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:06658911b19998c722152953ae140cd59e9be6fd7d10efce48dc0be4c7549c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6409793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4730e2caa764a7456f82d7aaf02889c1fb114375c44898e0e7ebb1e8ccaa545`

```dockerfile
```

-	Layers:
	-	`sha256:d085dedcd5c89dd8eefb985468610d2107cd63b9aa471a307b8354cc6af69130`  
		Last Modified: Fri, 06 Sep 2024 04:15:22 GMT  
		Size: 6.4 MB (6395079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82367f0d56606fb3e59e30b9981ed3d4e28e4c5de2f50c2fd66323b3c0a6d2d6`  
		Last Modified: Fri, 06 Sep 2024 04:15:22 GMT  
		Size: 14.7 KB (14714 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8ab8223cf42035683913aac257a4a0bef2da657b9a1f9b6b82a25230789fe10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152430806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055cf6c735c777083bd2806758a5af6697ab8684839606797b01332fd990feaa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668d9f37d5cd85b4971a92ccf8bc4b94221b93af70278e14cb5467c3c57f2e40`  
		Last Modified: Thu, 05 Sep 2024 20:29:24 GMT  
		Size: 18.9 MB (18870684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebffecbaf4391db8de82e81b089f2632335d3b714f3ef8a2f0ffb1f4f9f21ff5`  
		Last Modified: Thu, 05 Sep 2024 20:29:23 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf67612c42ba4c3ddb2bead89893da493bfd4478ba8584c8aa801a1a03c15b2`  
		Last Modified: Thu, 05 Sep 2024 20:30:43 GMT  
		Size: 60.4 MB (60377823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2152361d4908d72b62e8f65c25d07c190373440ba8f6b1033bc179be36d61e`  
		Last Modified: Thu, 05 Sep 2024 20:30:40 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:c3bffc37d556833052d636c8f9bf84c7db5f8a05ed0fe726ad051efba5fa8c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6416093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d499c67e7614b99b5c1c3ba15e51faac1bb56afea1fe613917f87f83dedd605`

```dockerfile
```

-	Layers:
	-	`sha256:e93c666dc1eca05258ba8a07ca0a3c90bbe4ab804a34dff235618ba04df14762`  
		Last Modified: Thu, 05 Sep 2024 20:30:41 GMT  
		Size: 6.4 MB (6401162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638663a2967e62ad6afc5b5b1083c7444dd5337c26e7067446f380abd56b8279`  
		Last Modified: Thu, 05 Sep 2024 20:30:40 GMT  
		Size: 14.9 KB (14931 bytes)  
		MIME: application/vnd.in-toto+json
