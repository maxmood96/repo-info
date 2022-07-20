<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.21`](#telegraf121)
-	[`telegraf:1.21-alpine`](#telegraf121-alpine)
-	[`telegraf:1.21.4`](#telegraf1214)
-	[`telegraf:1.21.4-alpine`](#telegraf1214-alpine)
-	[`telegraf:1.22`](#telegraf122)
-	[`telegraf:1.22-alpine`](#telegraf122-alpine)
-	[`telegraf:1.22.4`](#telegraf1224)
-	[`telegraf:1.22.4-alpine`](#telegraf1224-alpine)
-	[`telegraf:1.23`](#telegraf123)
-	[`telegraf:1.23-alpine`](#telegraf123-alpine)
-	[`telegraf:1.23.2`](#telegraf1232)
-	[`telegraf:1.23.2-alpine`](#telegraf1232-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.21`

```console
$ docker pull telegraf@sha256:6da22989781e7dfadee6a4bac374092aa67cad90ebeeb3b19fcb99c57d2a9f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.21` - linux; amd64

```console
$ docker pull telegraf@sha256:abc655bff28b3fb2bafc0f59fe645a0aff8ade898b7e54d14e0ca9ba55820128
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127452803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73e8b75b206d9f34c358ae46070a87f473b06b456bc527940ac53c4c79e4920`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 01:19:57 GMT
ADD file:3451708ab45bc1bcfc1ebb2075d3af16767477cbeb79334959e0d1ff02b0864b in / 
# Tue, 12 Jul 2022 01:19:58 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:48:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 00:51:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 00:51:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 00:51:16 GMT
ENV TELEGRAF_VERSION=1.21.4
# Wed, 13 Jul 2022 00:51:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 00:51:20 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 00:51:20 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 00:51:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 00:51:20 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d836772a1c1f9c4b1f280fb2a98ace30a4c4c87370f89aa092b35dfd9556278a`  
		Last Modified: Tue, 12 Jul 2022 01:24:06 GMT  
		Size: 55.0 MB (54999406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9e63c657ad881997f5165c0826be395bfc064415876b9fbaae74bcb5dc721`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 5.2 MB (5156110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1989b6e74cfdda1591b9dd23be47c5caeb002b7a151379361ec0c3f0e6d0e52`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 10.9 MB (10876416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15796d428c46a6a6a6313c2bac0a095deacb13167f82adb559eb6176ec2af29c`  
		Last Modified: Wed, 13 Jul 2022 00:52:03 GMT  
		Size: 18.8 MB (18760391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0216c283a6188b969faf59c6e7426df41a6d4eb5c4fc0322b363da41ed51f5e7`  
		Last Modified: Wed, 13 Jul 2022 00:52:00 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015cf5e4faeee9efe7539480903d17d736153ef34652bea0eb251d254f3b128c`  
		Last Modified: Wed, 13 Jul 2022 00:52:07 GMT  
		Size: 37.7 MB (37657242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26d8a45764142b3d91a1a1c00ddcdcec85b9b8fa627255fd234033c62a854b2`  
		Last Modified: Wed, 13 Jul 2022 00:52:00 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.21` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7aeb562527627194875cc8174015a46da807d99652a116b6eb5265fdb334e3fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117733993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a61476058d27e6926859798baca591c1c4adacdb43d30c3ee193586263561f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 00:59:16 GMT
ADD file:72ef8362158fcd45f10c6fa2dc3ea411e81f700ecb92faf37cb6dc1887756f9d in / 
# Tue, 12 Jul 2022 00:59:17 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 03:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 03:28:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 21:46:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 21:46:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 21:46:33 GMT
ENV TELEGRAF_VERSION=1.21.4
# Wed, 13 Jul 2022 21:46:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 21:46:46 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 21:46:46 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 21:46:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 21:46:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a8a55ed160b9a554de2e46b828d606a0829d8d9f19c79bc47eddac683aeb2b91`  
		Last Modified: Tue, 12 Jul 2022 01:11:51 GMT  
		Size: 50.2 MB (50194881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5042ae471fd57ff8851607bf0b66366fbd0a499a0ce088f1fb39c5a1caf4123e`  
		Last Modified: Tue, 12 Jul 2022 03:50:27 GMT  
		Size: 4.9 MB (4924746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70da2acc639b7236796e6cb2a0b0e3a21e6f32f8a507bdbfb823a510caf8e75a`  
		Last Modified: Tue, 12 Jul 2022 03:50:29 GMT  
		Size: 10.2 MB (10218056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0992d5af0c071c385deec4002f52d299bee3cbcc3c6bc0ef2e42061a76a537c`  
		Last Modified: Wed, 13 Jul 2022 21:48:37 GMT  
		Size: 17.5 MB (17462343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51a28192fdc11036097b81d3334c36a8facd680b71c81d8d1c9c7260c1965a9`  
		Last Modified: Wed, 13 Jul 2022 21:48:24 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7110fd80ceec7547b7e85ad9e8a587f30110ed1ab000ab5bca3cebde4114f407`  
		Last Modified: Wed, 13 Jul 2022 21:48:49 GMT  
		Size: 34.9 MB (34930734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6874b20cf6ffee1b3bfbcf038d9d50919f3f306e77b1c5590beaa25d0e1c13`  
		Last Modified: Wed, 13 Jul 2022 21:48:24 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.21` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:878565c37526c7d74ff4ebaab57143ecfceeeb053856be0975239814e3c303c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (122030025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c14c096bd52fe450e3558bbd1645e4beabd402b6a67fc8222ce8ff6a98a52e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:18 GMT
ADD file:2dcc013bca5a420cad3b6a1ac61f52ea58a29ae05fe282078a744979c0e1a89e in / 
# Tue, 12 Jul 2022 00:40:19 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:33:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:33:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 01:28:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 01:28:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 01:28:43 GMT
ENV TELEGRAF_VERSION=1.21.4
# Wed, 13 Jul 2022 01:28:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 01:28:48 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 01:28:50 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 01:28:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 01:28:51 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cfc947b533a3ed8b8ce79820c7fe5e7634bf9c08479ed0aee1e74ee7b4f2b068`  
		Last Modified: Tue, 12 Jul 2022 00:45:41 GMT  
		Size: 53.7 MB (53683129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca36aa4204d2a708dcd1d41d1d4a128b095f8d88a2f9544f89799c36914e356`  
		Last Modified: Tue, 12 Jul 2022 02:42:29 GMT  
		Size: 5.1 MB (5142960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdcd2014de70fbce8c43a70cd1f42bceab4f1e35953db987fc318dbc0fb0d26`  
		Last Modified: Tue, 12 Jul 2022 02:42:30 GMT  
		Size: 10.7 MB (10657500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099450cf5212ff57fa7236e4391a4095fa42bc6d23fdb15869367ae44e396a37`  
		Last Modified: Wed, 13 Jul 2022 01:29:42 GMT  
		Size: 18.4 MB (18382881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19eef7412ec39d1a75650a00b44d7b79179cf36dd748bd466ec7bdad6841137`  
		Last Modified: Wed, 13 Jul 2022 01:29:39 GMT  
		Size: 2.9 KB (2869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232b45541d3e0015edca0f1b22e6132a33b83ecd67cad1eceea5ae37eded0395`  
		Last Modified: Wed, 13 Jul 2022 01:29:45 GMT  
		Size: 34.2 MB (34160343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be41b8e0bb8c359318a999f2aa8629adc8681faea2798d93793acd8c114e7202`  
		Last Modified: Wed, 13 Jul 2022 01:29:39 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.21-alpine`

```console
$ docker pull telegraf@sha256:9075e180705041df3bee8e648d870e569f50583bf390c17e9ab9ffad4aae0060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.21-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:2153f289617aec080afc5e5e6402068649ff0d4cf26ca4a4994b37a6f9f2b6c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43686262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23daa1ecb777459f77d7aab6bb64a46c89004f0dfad4663a9dade41a4fb49df7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:25:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 20 Jul 2022 02:25:58 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Wed, 20 Jul 2022 02:25:58 GMT
ENV TELEGRAF_VERSION=1.21.4
# Wed, 20 Jul 2022 02:26:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 20 Jul 2022 02:26:04 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 20 Jul 2022 02:26:04 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Wed, 20 Jul 2022 02:26:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Jul 2022 02:26:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1d6c3bdc90884e20be4b8964afbc50fc83dac03969c542117bb4c4e59802fb`  
		Last Modified: Wed, 20 Jul 2022 02:26:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7afda0100e244bcaa7520aff1df3205abf84be1593c127ee83151d1395be22`  
		Last Modified: Wed, 20 Jul 2022 02:26:49 GMT  
		Size: 3.4 MB (3372891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9555aad715806c0fea6ee0e9cf31acc2f7fb1c9067f0c5ef2ca4ff54b43f7838`  
		Last Modified: Wed, 20 Jul 2022 02:26:55 GMT  
		Size: 37.5 MB (37498245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272fc0e7895dc73648dc5d5d2a639de3f70ed4c044ad8e49ea25773172a8c329`  
		Last Modified: Wed, 20 Jul 2022 02:26:48 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.21.4`

```console
$ docker pull telegraf@sha256:6da22989781e7dfadee6a4bac374092aa67cad90ebeeb3b19fcb99c57d2a9f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.21.4` - linux; amd64

```console
$ docker pull telegraf@sha256:abc655bff28b3fb2bafc0f59fe645a0aff8ade898b7e54d14e0ca9ba55820128
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127452803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73e8b75b206d9f34c358ae46070a87f473b06b456bc527940ac53c4c79e4920`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 01:19:57 GMT
ADD file:3451708ab45bc1bcfc1ebb2075d3af16767477cbeb79334959e0d1ff02b0864b in / 
# Tue, 12 Jul 2022 01:19:58 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:48:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 00:51:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 00:51:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 00:51:16 GMT
ENV TELEGRAF_VERSION=1.21.4
# Wed, 13 Jul 2022 00:51:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 00:51:20 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 00:51:20 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 00:51:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 00:51:20 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d836772a1c1f9c4b1f280fb2a98ace30a4c4c87370f89aa092b35dfd9556278a`  
		Last Modified: Tue, 12 Jul 2022 01:24:06 GMT  
		Size: 55.0 MB (54999406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9e63c657ad881997f5165c0826be395bfc064415876b9fbaae74bcb5dc721`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 5.2 MB (5156110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1989b6e74cfdda1591b9dd23be47c5caeb002b7a151379361ec0c3f0e6d0e52`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 10.9 MB (10876416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15796d428c46a6a6a6313c2bac0a095deacb13167f82adb559eb6176ec2af29c`  
		Last Modified: Wed, 13 Jul 2022 00:52:03 GMT  
		Size: 18.8 MB (18760391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0216c283a6188b969faf59c6e7426df41a6d4eb5c4fc0322b363da41ed51f5e7`  
		Last Modified: Wed, 13 Jul 2022 00:52:00 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015cf5e4faeee9efe7539480903d17d736153ef34652bea0eb251d254f3b128c`  
		Last Modified: Wed, 13 Jul 2022 00:52:07 GMT  
		Size: 37.7 MB (37657242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26d8a45764142b3d91a1a1c00ddcdcec85b9b8fa627255fd234033c62a854b2`  
		Last Modified: Wed, 13 Jul 2022 00:52:00 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.21.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7aeb562527627194875cc8174015a46da807d99652a116b6eb5265fdb334e3fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117733993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a61476058d27e6926859798baca591c1c4adacdb43d30c3ee193586263561f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 00:59:16 GMT
ADD file:72ef8362158fcd45f10c6fa2dc3ea411e81f700ecb92faf37cb6dc1887756f9d in / 
# Tue, 12 Jul 2022 00:59:17 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 03:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 03:28:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 21:46:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 21:46:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 21:46:33 GMT
ENV TELEGRAF_VERSION=1.21.4
# Wed, 13 Jul 2022 21:46:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 21:46:46 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 21:46:46 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 21:46:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 21:46:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a8a55ed160b9a554de2e46b828d606a0829d8d9f19c79bc47eddac683aeb2b91`  
		Last Modified: Tue, 12 Jul 2022 01:11:51 GMT  
		Size: 50.2 MB (50194881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5042ae471fd57ff8851607bf0b66366fbd0a499a0ce088f1fb39c5a1caf4123e`  
		Last Modified: Tue, 12 Jul 2022 03:50:27 GMT  
		Size: 4.9 MB (4924746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70da2acc639b7236796e6cb2a0b0e3a21e6f32f8a507bdbfb823a510caf8e75a`  
		Last Modified: Tue, 12 Jul 2022 03:50:29 GMT  
		Size: 10.2 MB (10218056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0992d5af0c071c385deec4002f52d299bee3cbcc3c6bc0ef2e42061a76a537c`  
		Last Modified: Wed, 13 Jul 2022 21:48:37 GMT  
		Size: 17.5 MB (17462343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51a28192fdc11036097b81d3334c36a8facd680b71c81d8d1c9c7260c1965a9`  
		Last Modified: Wed, 13 Jul 2022 21:48:24 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7110fd80ceec7547b7e85ad9e8a587f30110ed1ab000ab5bca3cebde4114f407`  
		Last Modified: Wed, 13 Jul 2022 21:48:49 GMT  
		Size: 34.9 MB (34930734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6874b20cf6ffee1b3bfbcf038d9d50919f3f306e77b1c5590beaa25d0e1c13`  
		Last Modified: Wed, 13 Jul 2022 21:48:24 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.21.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:878565c37526c7d74ff4ebaab57143ecfceeeb053856be0975239814e3c303c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (122030025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c14c096bd52fe450e3558bbd1645e4beabd402b6a67fc8222ce8ff6a98a52e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:18 GMT
ADD file:2dcc013bca5a420cad3b6a1ac61f52ea58a29ae05fe282078a744979c0e1a89e in / 
# Tue, 12 Jul 2022 00:40:19 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:33:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:33:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 01:28:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 01:28:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 01:28:43 GMT
ENV TELEGRAF_VERSION=1.21.4
# Wed, 13 Jul 2022 01:28:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 01:28:48 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 01:28:50 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 01:28:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 01:28:51 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cfc947b533a3ed8b8ce79820c7fe5e7634bf9c08479ed0aee1e74ee7b4f2b068`  
		Last Modified: Tue, 12 Jul 2022 00:45:41 GMT  
		Size: 53.7 MB (53683129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca36aa4204d2a708dcd1d41d1d4a128b095f8d88a2f9544f89799c36914e356`  
		Last Modified: Tue, 12 Jul 2022 02:42:29 GMT  
		Size: 5.1 MB (5142960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdcd2014de70fbce8c43a70cd1f42bceab4f1e35953db987fc318dbc0fb0d26`  
		Last Modified: Tue, 12 Jul 2022 02:42:30 GMT  
		Size: 10.7 MB (10657500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099450cf5212ff57fa7236e4391a4095fa42bc6d23fdb15869367ae44e396a37`  
		Last Modified: Wed, 13 Jul 2022 01:29:42 GMT  
		Size: 18.4 MB (18382881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19eef7412ec39d1a75650a00b44d7b79179cf36dd748bd466ec7bdad6841137`  
		Last Modified: Wed, 13 Jul 2022 01:29:39 GMT  
		Size: 2.9 KB (2869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232b45541d3e0015edca0f1b22e6132a33b83ecd67cad1eceea5ae37eded0395`  
		Last Modified: Wed, 13 Jul 2022 01:29:45 GMT  
		Size: 34.2 MB (34160343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be41b8e0bb8c359318a999f2aa8629adc8681faea2798d93793acd8c114e7202`  
		Last Modified: Wed, 13 Jul 2022 01:29:39 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.21.4-alpine`

```console
$ docker pull telegraf@sha256:9075e180705041df3bee8e648d870e569f50583bf390c17e9ab9ffad4aae0060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.21.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:2153f289617aec080afc5e5e6402068649ff0d4cf26ca4a4994b37a6f9f2b6c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43686262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23daa1ecb777459f77d7aab6bb64a46c89004f0dfad4663a9dade41a4fb49df7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:25:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 20 Jul 2022 02:25:58 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Wed, 20 Jul 2022 02:25:58 GMT
ENV TELEGRAF_VERSION=1.21.4
# Wed, 20 Jul 2022 02:26:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 20 Jul 2022 02:26:04 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 20 Jul 2022 02:26:04 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Wed, 20 Jul 2022 02:26:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Jul 2022 02:26:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1d6c3bdc90884e20be4b8964afbc50fc83dac03969c542117bb4c4e59802fb`  
		Last Modified: Wed, 20 Jul 2022 02:26:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7afda0100e244bcaa7520aff1df3205abf84be1593c127ee83151d1395be22`  
		Last Modified: Wed, 20 Jul 2022 02:26:49 GMT  
		Size: 3.4 MB (3372891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9555aad715806c0fea6ee0e9cf31acc2f7fb1c9067f0c5ef2ca4ff54b43f7838`  
		Last Modified: Wed, 20 Jul 2022 02:26:55 GMT  
		Size: 37.5 MB (37498245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272fc0e7895dc73648dc5d5d2a639de3f70ed4c044ad8e49ea25773172a8c329`  
		Last Modified: Wed, 20 Jul 2022 02:26:48 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.22`

```console
$ docker pull telegraf@sha256:d799e8bcd02aeac5f75935051f4e97f54d0a7545934f7070937528a85d29e0af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.22` - linux; amd64

```console
$ docker pull telegraf@sha256:caeb90210a5767089204ad4fd70375f7c3f6bf20903fcd493d3f284dd4c54dfb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130294337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b8fe4e0e255647d55e5baae1dc63403d6e99dbc9accd20ea8e451e0e72a233`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 01:19:57 GMT
ADD file:3451708ab45bc1bcfc1ebb2075d3af16767477cbeb79334959e0d1ff02b0864b in / 
# Tue, 12 Jul 2022 01:19:58 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:48:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 00:51:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 00:51:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 00:51:26 GMT
ENV TELEGRAF_VERSION=1.22.4
# Wed, 13 Jul 2022 00:51:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 00:51:30 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 00:51:30 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 00:51:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 00:51:31 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d836772a1c1f9c4b1f280fb2a98ace30a4c4c87370f89aa092b35dfd9556278a`  
		Last Modified: Tue, 12 Jul 2022 01:24:06 GMT  
		Size: 55.0 MB (54999406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9e63c657ad881997f5165c0826be395bfc064415876b9fbaae74bcb5dc721`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 5.2 MB (5156110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1989b6e74cfdda1591b9dd23be47c5caeb002b7a151379361ec0c3f0e6d0e52`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 10.9 MB (10876416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15796d428c46a6a6a6313c2bac0a095deacb13167f82adb559eb6176ec2af29c`  
		Last Modified: Wed, 13 Jul 2022 00:52:03 GMT  
		Size: 18.8 MB (18760391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0216c283a6188b969faf59c6e7426df41a6d4eb5c4fc0322b363da41ed51f5e7`  
		Last Modified: Wed, 13 Jul 2022 00:52:00 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8fa7cc347bf576dcde2eae66363ce9b8ffc1fd0bcd93c04ce4c922d889fe73`  
		Last Modified: Wed, 13 Jul 2022 00:52:24 GMT  
		Size: 40.5 MB (40498775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc070eb0c4939ff9313ad28084042820ea485bba1a8b3db596e258aecd19dc0`  
		Last Modified: Wed, 13 Jul 2022 00:52:17 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.22` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:b9aa51211b3aaba6d1415a3a47cae18653f2e95280c7bfb543b1032e66333e94
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120725014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99a876aab2d80a35beafb8362d9d31ed7709185e7df47278c93ed8f6a38f858`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 00:59:16 GMT
ADD file:72ef8362158fcd45f10c6fa2dc3ea411e81f700ecb92faf37cb6dc1887756f9d in / 
# Tue, 12 Jul 2022 00:59:17 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 03:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 03:28:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 21:46:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 21:46:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 21:47:02 GMT
ENV TELEGRAF_VERSION=1.22.4
# Wed, 13 Jul 2022 21:47:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 21:47:14 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 21:47:15 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 21:47:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 21:47:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a8a55ed160b9a554de2e46b828d606a0829d8d9f19c79bc47eddac683aeb2b91`  
		Last Modified: Tue, 12 Jul 2022 01:11:51 GMT  
		Size: 50.2 MB (50194881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5042ae471fd57ff8851607bf0b66366fbd0a499a0ce088f1fb39c5a1caf4123e`  
		Last Modified: Tue, 12 Jul 2022 03:50:27 GMT  
		Size: 4.9 MB (4924746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70da2acc639b7236796e6cb2a0b0e3a21e6f32f8a507bdbfb823a510caf8e75a`  
		Last Modified: Tue, 12 Jul 2022 03:50:29 GMT  
		Size: 10.2 MB (10218056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0992d5af0c071c385deec4002f52d299bee3cbcc3c6bc0ef2e42061a76a537c`  
		Last Modified: Wed, 13 Jul 2022 21:48:37 GMT  
		Size: 17.5 MB (17462343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51a28192fdc11036097b81d3334c36a8facd680b71c81d8d1c9c7260c1965a9`  
		Last Modified: Wed, 13 Jul 2022 21:48:24 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781c40e268781685d933f18200fdc039a9421d61d7ea72d961706608ae4bcd4d`  
		Last Modified: Wed, 13 Jul 2022 21:49:29 GMT  
		Size: 37.9 MB (37921755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d953a38ca0c28b0527cfb4a2b8a2c9030c138321cbf58762a99e4806d59f48ef`  
		Last Modified: Wed, 13 Jul 2022 21:49:02 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.22` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:1ec84e2d3c1f10c28dfdd9a4a56db1a954358394e0a9723516c8f8cb9fbb424f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124680672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74456529cbef5137626f8b860cc6aed781189c7c1e11a5ad2b69ca0c4b182a73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:18 GMT
ADD file:2dcc013bca5a420cad3b6a1ac61f52ea58a29ae05fe282078a744979c0e1a89e in / 
# Tue, 12 Jul 2022 00:40:19 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:33:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:33:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 01:28:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 01:28:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 01:28:57 GMT
ENV TELEGRAF_VERSION=1.22.4
# Wed, 13 Jul 2022 01:29:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 01:29:01 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 01:29:03 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 01:29:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 01:29:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cfc947b533a3ed8b8ce79820c7fe5e7634bf9c08479ed0aee1e74ee7b4f2b068`  
		Last Modified: Tue, 12 Jul 2022 00:45:41 GMT  
		Size: 53.7 MB (53683129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca36aa4204d2a708dcd1d41d1d4a128b095f8d88a2f9544f89799c36914e356`  
		Last Modified: Tue, 12 Jul 2022 02:42:29 GMT  
		Size: 5.1 MB (5142960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdcd2014de70fbce8c43a70cd1f42bceab4f1e35953db987fc318dbc0fb0d26`  
		Last Modified: Tue, 12 Jul 2022 02:42:30 GMT  
		Size: 10.7 MB (10657500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099450cf5212ff57fa7236e4391a4095fa42bc6d23fdb15869367ae44e396a37`  
		Last Modified: Wed, 13 Jul 2022 01:29:42 GMT  
		Size: 18.4 MB (18382881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19eef7412ec39d1a75650a00b44d7b79179cf36dd748bd466ec7bdad6841137`  
		Last Modified: Wed, 13 Jul 2022 01:29:39 GMT  
		Size: 2.9 KB (2869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5ea551e83cd6a447c5b3eb89dae8b9b443cc295e3cf2fb4b4ad8938180be0d`  
		Last Modified: Wed, 13 Jul 2022 01:30:02 GMT  
		Size: 36.8 MB (36810991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324183b04dce314ed313d842c044ba60ad1248baa43fc0c0006a7aa765ad93b2`  
		Last Modified: Wed, 13 Jul 2022 01:29:56 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.22-alpine`

```console
$ docker pull telegraf@sha256:bf27934d3967ab34011854e1951b00cd30218ff49d5e30512dada3a568782606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.22-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c9c0e1f082fc573fb815361cce09bdd05f4756ba427d445b3a3a9a6c060239fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46542137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d178f642164168fecf5d636292cca6a61d896c8723830cf3717c3f3fd992c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:25:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 20 Jul 2022 02:25:58 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Wed, 20 Jul 2022 02:26:08 GMT
ENV TELEGRAF_VERSION=1.22.4
# Wed, 20 Jul 2022 02:26:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 20 Jul 2022 02:26:15 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 20 Jul 2022 02:26:15 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Wed, 20 Jul 2022 02:26:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Jul 2022 02:26:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1d6c3bdc90884e20be4b8964afbc50fc83dac03969c542117bb4c4e59802fb`  
		Last Modified: Wed, 20 Jul 2022 02:26:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7afda0100e244bcaa7520aff1df3205abf84be1593c127ee83151d1395be22`  
		Last Modified: Wed, 20 Jul 2022 02:26:49 GMT  
		Size: 3.4 MB (3372891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1744c6d7f1d3b0cfc79904e1d04f119570f1aa76386244b2a87426468fd4d500`  
		Last Modified: Wed, 20 Jul 2022 02:27:11 GMT  
		Size: 40.4 MB (40354121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702b42dd6a8e2c24a184819f51f5ba8fa12e92b225839733cc72571c871ba5a1`  
		Last Modified: Wed, 20 Jul 2022 02:27:05 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.22.4`

```console
$ docker pull telegraf@sha256:d799e8bcd02aeac5f75935051f4e97f54d0a7545934f7070937528a85d29e0af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.22.4` - linux; amd64

```console
$ docker pull telegraf@sha256:caeb90210a5767089204ad4fd70375f7c3f6bf20903fcd493d3f284dd4c54dfb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130294337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b8fe4e0e255647d55e5baae1dc63403d6e99dbc9accd20ea8e451e0e72a233`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 01:19:57 GMT
ADD file:3451708ab45bc1bcfc1ebb2075d3af16767477cbeb79334959e0d1ff02b0864b in / 
# Tue, 12 Jul 2022 01:19:58 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:48:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 00:51:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 00:51:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 00:51:26 GMT
ENV TELEGRAF_VERSION=1.22.4
# Wed, 13 Jul 2022 00:51:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 00:51:30 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 00:51:30 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 00:51:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 00:51:31 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d836772a1c1f9c4b1f280fb2a98ace30a4c4c87370f89aa092b35dfd9556278a`  
		Last Modified: Tue, 12 Jul 2022 01:24:06 GMT  
		Size: 55.0 MB (54999406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9e63c657ad881997f5165c0826be395bfc064415876b9fbaae74bcb5dc721`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 5.2 MB (5156110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1989b6e74cfdda1591b9dd23be47c5caeb002b7a151379361ec0c3f0e6d0e52`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 10.9 MB (10876416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15796d428c46a6a6a6313c2bac0a095deacb13167f82adb559eb6176ec2af29c`  
		Last Modified: Wed, 13 Jul 2022 00:52:03 GMT  
		Size: 18.8 MB (18760391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0216c283a6188b969faf59c6e7426df41a6d4eb5c4fc0322b363da41ed51f5e7`  
		Last Modified: Wed, 13 Jul 2022 00:52:00 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8fa7cc347bf576dcde2eae66363ce9b8ffc1fd0bcd93c04ce4c922d889fe73`  
		Last Modified: Wed, 13 Jul 2022 00:52:24 GMT  
		Size: 40.5 MB (40498775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc070eb0c4939ff9313ad28084042820ea485bba1a8b3db596e258aecd19dc0`  
		Last Modified: Wed, 13 Jul 2022 00:52:17 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.22.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:b9aa51211b3aaba6d1415a3a47cae18653f2e95280c7bfb543b1032e66333e94
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120725014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99a876aab2d80a35beafb8362d9d31ed7709185e7df47278c93ed8f6a38f858`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 00:59:16 GMT
ADD file:72ef8362158fcd45f10c6fa2dc3ea411e81f700ecb92faf37cb6dc1887756f9d in / 
# Tue, 12 Jul 2022 00:59:17 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 03:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 03:28:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 21:46:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 21:46:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 21:47:02 GMT
ENV TELEGRAF_VERSION=1.22.4
# Wed, 13 Jul 2022 21:47:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 21:47:14 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 21:47:15 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 21:47:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 21:47:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a8a55ed160b9a554de2e46b828d606a0829d8d9f19c79bc47eddac683aeb2b91`  
		Last Modified: Tue, 12 Jul 2022 01:11:51 GMT  
		Size: 50.2 MB (50194881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5042ae471fd57ff8851607bf0b66366fbd0a499a0ce088f1fb39c5a1caf4123e`  
		Last Modified: Tue, 12 Jul 2022 03:50:27 GMT  
		Size: 4.9 MB (4924746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70da2acc639b7236796e6cb2a0b0e3a21e6f32f8a507bdbfb823a510caf8e75a`  
		Last Modified: Tue, 12 Jul 2022 03:50:29 GMT  
		Size: 10.2 MB (10218056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0992d5af0c071c385deec4002f52d299bee3cbcc3c6bc0ef2e42061a76a537c`  
		Last Modified: Wed, 13 Jul 2022 21:48:37 GMT  
		Size: 17.5 MB (17462343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51a28192fdc11036097b81d3334c36a8facd680b71c81d8d1c9c7260c1965a9`  
		Last Modified: Wed, 13 Jul 2022 21:48:24 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781c40e268781685d933f18200fdc039a9421d61d7ea72d961706608ae4bcd4d`  
		Last Modified: Wed, 13 Jul 2022 21:49:29 GMT  
		Size: 37.9 MB (37921755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d953a38ca0c28b0527cfb4a2b8a2c9030c138321cbf58762a99e4806d59f48ef`  
		Last Modified: Wed, 13 Jul 2022 21:49:02 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.22.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:1ec84e2d3c1f10c28dfdd9a4a56db1a954358394e0a9723516c8f8cb9fbb424f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124680672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74456529cbef5137626f8b860cc6aed781189c7c1e11a5ad2b69ca0c4b182a73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:18 GMT
ADD file:2dcc013bca5a420cad3b6a1ac61f52ea58a29ae05fe282078a744979c0e1a89e in / 
# Tue, 12 Jul 2022 00:40:19 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:33:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:33:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 01:28:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 01:28:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 01:28:57 GMT
ENV TELEGRAF_VERSION=1.22.4
# Wed, 13 Jul 2022 01:29:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 01:29:01 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 01:29:03 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 01:29:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 01:29:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cfc947b533a3ed8b8ce79820c7fe5e7634bf9c08479ed0aee1e74ee7b4f2b068`  
		Last Modified: Tue, 12 Jul 2022 00:45:41 GMT  
		Size: 53.7 MB (53683129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca36aa4204d2a708dcd1d41d1d4a128b095f8d88a2f9544f89799c36914e356`  
		Last Modified: Tue, 12 Jul 2022 02:42:29 GMT  
		Size: 5.1 MB (5142960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdcd2014de70fbce8c43a70cd1f42bceab4f1e35953db987fc318dbc0fb0d26`  
		Last Modified: Tue, 12 Jul 2022 02:42:30 GMT  
		Size: 10.7 MB (10657500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099450cf5212ff57fa7236e4391a4095fa42bc6d23fdb15869367ae44e396a37`  
		Last Modified: Wed, 13 Jul 2022 01:29:42 GMT  
		Size: 18.4 MB (18382881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19eef7412ec39d1a75650a00b44d7b79179cf36dd748bd466ec7bdad6841137`  
		Last Modified: Wed, 13 Jul 2022 01:29:39 GMT  
		Size: 2.9 KB (2869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5ea551e83cd6a447c5b3eb89dae8b9b443cc295e3cf2fb4b4ad8938180be0d`  
		Last Modified: Wed, 13 Jul 2022 01:30:02 GMT  
		Size: 36.8 MB (36810991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324183b04dce314ed313d842c044ba60ad1248baa43fc0c0006a7aa765ad93b2`  
		Last Modified: Wed, 13 Jul 2022 01:29:56 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.22.4-alpine`

```console
$ docker pull telegraf@sha256:bf27934d3967ab34011854e1951b00cd30218ff49d5e30512dada3a568782606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.22.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c9c0e1f082fc573fb815361cce09bdd05f4756ba427d445b3a3a9a6c060239fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46542137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d178f642164168fecf5d636292cca6a61d896c8723830cf3717c3f3fd992c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:25:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 20 Jul 2022 02:25:58 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Wed, 20 Jul 2022 02:26:08 GMT
ENV TELEGRAF_VERSION=1.22.4
# Wed, 20 Jul 2022 02:26:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 20 Jul 2022 02:26:15 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 20 Jul 2022 02:26:15 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Wed, 20 Jul 2022 02:26:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Jul 2022 02:26:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1d6c3bdc90884e20be4b8964afbc50fc83dac03969c542117bb4c4e59802fb`  
		Last Modified: Wed, 20 Jul 2022 02:26:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7afda0100e244bcaa7520aff1df3205abf84be1593c127ee83151d1395be22`  
		Last Modified: Wed, 20 Jul 2022 02:26:49 GMT  
		Size: 3.4 MB (3372891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1744c6d7f1d3b0cfc79904e1d04f119570f1aa76386244b2a87426468fd4d500`  
		Last Modified: Wed, 20 Jul 2022 02:27:11 GMT  
		Size: 40.4 MB (40354121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702b42dd6a8e2c24a184819f51f5ba8fa12e92b225839733cc72571c871ba5a1`  
		Last Modified: Wed, 20 Jul 2022 02:27:05 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.23`

```console
$ docker pull telegraf@sha256:583de522849dd3335fc8365b28983b51e69a0a8e7851982ea337c68e892bb9c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.23` - linux; amd64

```console
$ docker pull telegraf@sha256:e3eef6a27482a8e8a1f1bd718e9b1cc819340e52f849a1dc93783757f6580ac6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131477605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11676beafdbe2c3cfaaa14432120397f0f43dcc9a5d01468334bf99352802c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 01:19:57 GMT
ADD file:3451708ab45bc1bcfc1ebb2075d3af16767477cbeb79334959e0d1ff02b0864b in / 
# Tue, 12 Jul 2022 01:19:58 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:48:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 00:51:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 00:51:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 00:51:35 GMT
ENV TELEGRAF_VERSION=1.23.2
# Wed, 13 Jul 2022 00:51:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 00:51:39 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 00:51:39 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 00:51:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 00:51:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d836772a1c1f9c4b1f280fb2a98ace30a4c4c87370f89aa092b35dfd9556278a`  
		Last Modified: Tue, 12 Jul 2022 01:24:06 GMT  
		Size: 55.0 MB (54999406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9e63c657ad881997f5165c0826be395bfc064415876b9fbaae74bcb5dc721`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 5.2 MB (5156110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1989b6e74cfdda1591b9dd23be47c5caeb002b7a151379361ec0c3f0e6d0e52`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 10.9 MB (10876416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15796d428c46a6a6a6313c2bac0a095deacb13167f82adb559eb6176ec2af29c`  
		Last Modified: Wed, 13 Jul 2022 00:52:03 GMT  
		Size: 18.8 MB (18760391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0216c283a6188b969faf59c6e7426df41a6d4eb5c4fc0322b363da41ed51f5e7`  
		Last Modified: Wed, 13 Jul 2022 00:52:00 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6c91432eb33f615f7769e025212187a24ea51091cbf45ed021029e16783d98`  
		Last Modified: Wed, 13 Jul 2022 00:52:42 GMT  
		Size: 41.7 MB (41682044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5858ef52fd16a141493f30423c6c6f8b8fa0eab849425e5c7911510465d72ebc`  
		Last Modified: Wed, 13 Jul 2022 00:52:35 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.23` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:13cf4e63816b971b2956ef710642f6c416a22fc644be0ab86f419cbf79c7914e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121775920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf31cbeb266a7ab780a82929973ebda033602028c0f875a512cb480fa0790237`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 00:59:16 GMT
ADD file:72ef8362158fcd45f10c6fa2dc3ea411e81f700ecb92faf37cb6dc1887756f9d in / 
# Tue, 12 Jul 2022 00:59:17 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 03:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 03:28:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 21:46:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 21:46:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 21:47:27 GMT
ENV TELEGRAF_VERSION=1.23.2
# Wed, 13 Jul 2022 21:47:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 21:47:39 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 21:47:40 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 21:47:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 21:47:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a8a55ed160b9a554de2e46b828d606a0829d8d9f19c79bc47eddac683aeb2b91`  
		Last Modified: Tue, 12 Jul 2022 01:11:51 GMT  
		Size: 50.2 MB (50194881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5042ae471fd57ff8851607bf0b66366fbd0a499a0ce088f1fb39c5a1caf4123e`  
		Last Modified: Tue, 12 Jul 2022 03:50:27 GMT  
		Size: 4.9 MB (4924746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70da2acc639b7236796e6cb2a0b0e3a21e6f32f8a507bdbfb823a510caf8e75a`  
		Last Modified: Tue, 12 Jul 2022 03:50:29 GMT  
		Size: 10.2 MB (10218056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0992d5af0c071c385deec4002f52d299bee3cbcc3c6bc0ef2e42061a76a537c`  
		Last Modified: Wed, 13 Jul 2022 21:48:37 GMT  
		Size: 17.5 MB (17462343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51a28192fdc11036097b81d3334c36a8facd680b71c81d8d1c9c7260c1965a9`  
		Last Modified: Wed, 13 Jul 2022 21:48:24 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf3ca93915b927d60ae79e264fdbcf2c79f75e0d6c4e722b14ff3d00ff57734`  
		Last Modified: Wed, 13 Jul 2022 21:50:09 GMT  
		Size: 39.0 MB (38972660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5990ca770cb06ccfc134f44fb0b9b3626585d4dda528c49f19092431216bd2a3`  
		Last Modified: Wed, 13 Jul 2022 21:49:41 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.23` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d2694ede98ea8d1b8005a72d3f657b5db8d80270579d70d21a1cb65e07291e4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125743953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb685a759d4f9ecd31e72ad90ae31d8823e84c34031d3a703af9b6c49fb0873`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:18 GMT
ADD file:2dcc013bca5a420cad3b6a1ac61f52ea58a29ae05fe282078a744979c0e1a89e in / 
# Tue, 12 Jul 2022 00:40:19 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:33:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:33:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 01:28:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 01:28:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 01:29:09 GMT
ENV TELEGRAF_VERSION=1.23.2
# Wed, 13 Jul 2022 01:29:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 01:29:15 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 01:29:16 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 01:29:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 01:29:17 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cfc947b533a3ed8b8ce79820c7fe5e7634bf9c08479ed0aee1e74ee7b4f2b068`  
		Last Modified: Tue, 12 Jul 2022 00:45:41 GMT  
		Size: 53.7 MB (53683129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca36aa4204d2a708dcd1d41d1d4a128b095f8d88a2f9544f89799c36914e356`  
		Last Modified: Tue, 12 Jul 2022 02:42:29 GMT  
		Size: 5.1 MB (5142960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdcd2014de70fbce8c43a70cd1f42bceab4f1e35953db987fc318dbc0fb0d26`  
		Last Modified: Tue, 12 Jul 2022 02:42:30 GMT  
		Size: 10.7 MB (10657500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099450cf5212ff57fa7236e4391a4095fa42bc6d23fdb15869367ae44e396a37`  
		Last Modified: Wed, 13 Jul 2022 01:29:42 GMT  
		Size: 18.4 MB (18382881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19eef7412ec39d1a75650a00b44d7b79179cf36dd748bd466ec7bdad6841137`  
		Last Modified: Wed, 13 Jul 2022 01:29:39 GMT  
		Size: 2.9 KB (2869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccef8ee42539528cbfc4baa7cb82663010375fa1deaf4abd07fb87fc5c9c3a14`  
		Last Modified: Wed, 13 Jul 2022 01:30:20 GMT  
		Size: 37.9 MB (37874271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9b7359533194b5c67c5d65cf220b089a93feb263208f0b0576bac0d45acb82`  
		Last Modified: Wed, 13 Jul 2022 01:30:14 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.23-alpine`

```console
$ docker pull telegraf@sha256:005ab6c1bac77aab1725395335ffb33eeec35e0f6db774554a0ce0d29cc8996c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.23-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:814678d57c5b75e0d38a9c9e0b16fe218681db3b90496d6272c019dede9e92ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47706813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5288c877257e0b347e8af5c2ce7cb2c41dfe81a1be9456e29aa9493acce1b69a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:25:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 20 Jul 2022 02:25:58 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Wed, 20 Jul 2022 02:26:20 GMT
ENV TELEGRAF_VERSION=1.23.2
# Wed, 20 Jul 2022 02:26:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 20 Jul 2022 02:26:28 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 20 Jul 2022 02:26:28 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Wed, 20 Jul 2022 02:26:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Jul 2022 02:26:28 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1d6c3bdc90884e20be4b8964afbc50fc83dac03969c542117bb4c4e59802fb`  
		Last Modified: Wed, 20 Jul 2022 02:26:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7afda0100e244bcaa7520aff1df3205abf84be1593c127ee83151d1395be22`  
		Last Modified: Wed, 20 Jul 2022 02:26:49 GMT  
		Size: 3.4 MB (3372891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971da97d895cca6554946fe061f528b7a23cef4eb70d22ee904fafe92648533c`  
		Last Modified: Wed, 20 Jul 2022 02:27:28 GMT  
		Size: 41.5 MB (41518796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3739c19c31dfe897e281af0e79cf4856473a21d54a2cb6cd62591ad0f0a1731a`  
		Last Modified: Wed, 20 Jul 2022 02:27:21 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.23.2`

```console
$ docker pull telegraf@sha256:583de522849dd3335fc8365b28983b51e69a0a8e7851982ea337c68e892bb9c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.23.2` - linux; amd64

```console
$ docker pull telegraf@sha256:e3eef6a27482a8e8a1f1bd718e9b1cc819340e52f849a1dc93783757f6580ac6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131477605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11676beafdbe2c3cfaaa14432120397f0f43dcc9a5d01468334bf99352802c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 01:19:57 GMT
ADD file:3451708ab45bc1bcfc1ebb2075d3af16767477cbeb79334959e0d1ff02b0864b in / 
# Tue, 12 Jul 2022 01:19:58 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:48:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 00:51:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 00:51:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 00:51:35 GMT
ENV TELEGRAF_VERSION=1.23.2
# Wed, 13 Jul 2022 00:51:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 00:51:39 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 00:51:39 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 00:51:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 00:51:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d836772a1c1f9c4b1f280fb2a98ace30a4c4c87370f89aa092b35dfd9556278a`  
		Last Modified: Tue, 12 Jul 2022 01:24:06 GMT  
		Size: 55.0 MB (54999406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9e63c657ad881997f5165c0826be395bfc064415876b9fbaae74bcb5dc721`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 5.2 MB (5156110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1989b6e74cfdda1591b9dd23be47c5caeb002b7a151379361ec0c3f0e6d0e52`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 10.9 MB (10876416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15796d428c46a6a6a6313c2bac0a095deacb13167f82adb559eb6176ec2af29c`  
		Last Modified: Wed, 13 Jul 2022 00:52:03 GMT  
		Size: 18.8 MB (18760391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0216c283a6188b969faf59c6e7426df41a6d4eb5c4fc0322b363da41ed51f5e7`  
		Last Modified: Wed, 13 Jul 2022 00:52:00 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6c91432eb33f615f7769e025212187a24ea51091cbf45ed021029e16783d98`  
		Last Modified: Wed, 13 Jul 2022 00:52:42 GMT  
		Size: 41.7 MB (41682044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5858ef52fd16a141493f30423c6c6f8b8fa0eab849425e5c7911510465d72ebc`  
		Last Modified: Wed, 13 Jul 2022 00:52:35 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.23.2` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:13cf4e63816b971b2956ef710642f6c416a22fc644be0ab86f419cbf79c7914e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121775920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf31cbeb266a7ab780a82929973ebda033602028c0f875a512cb480fa0790237`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 00:59:16 GMT
ADD file:72ef8362158fcd45f10c6fa2dc3ea411e81f700ecb92faf37cb6dc1887756f9d in / 
# Tue, 12 Jul 2022 00:59:17 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 03:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 03:28:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 21:46:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 21:46:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 21:47:27 GMT
ENV TELEGRAF_VERSION=1.23.2
# Wed, 13 Jul 2022 21:47:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 21:47:39 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 21:47:40 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 21:47:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 21:47:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a8a55ed160b9a554de2e46b828d606a0829d8d9f19c79bc47eddac683aeb2b91`  
		Last Modified: Tue, 12 Jul 2022 01:11:51 GMT  
		Size: 50.2 MB (50194881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5042ae471fd57ff8851607bf0b66366fbd0a499a0ce088f1fb39c5a1caf4123e`  
		Last Modified: Tue, 12 Jul 2022 03:50:27 GMT  
		Size: 4.9 MB (4924746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70da2acc639b7236796e6cb2a0b0e3a21e6f32f8a507bdbfb823a510caf8e75a`  
		Last Modified: Tue, 12 Jul 2022 03:50:29 GMT  
		Size: 10.2 MB (10218056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0992d5af0c071c385deec4002f52d299bee3cbcc3c6bc0ef2e42061a76a537c`  
		Last Modified: Wed, 13 Jul 2022 21:48:37 GMT  
		Size: 17.5 MB (17462343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51a28192fdc11036097b81d3334c36a8facd680b71c81d8d1c9c7260c1965a9`  
		Last Modified: Wed, 13 Jul 2022 21:48:24 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf3ca93915b927d60ae79e264fdbcf2c79f75e0d6c4e722b14ff3d00ff57734`  
		Last Modified: Wed, 13 Jul 2022 21:50:09 GMT  
		Size: 39.0 MB (38972660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5990ca770cb06ccfc134f44fb0b9b3626585d4dda528c49f19092431216bd2a3`  
		Last Modified: Wed, 13 Jul 2022 21:49:41 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.23.2` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d2694ede98ea8d1b8005a72d3f657b5db8d80270579d70d21a1cb65e07291e4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125743953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb685a759d4f9ecd31e72ad90ae31d8823e84c34031d3a703af9b6c49fb0873`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:18 GMT
ADD file:2dcc013bca5a420cad3b6a1ac61f52ea58a29ae05fe282078a744979c0e1a89e in / 
# Tue, 12 Jul 2022 00:40:19 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:33:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:33:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 01:28:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 01:28:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 01:29:09 GMT
ENV TELEGRAF_VERSION=1.23.2
# Wed, 13 Jul 2022 01:29:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 01:29:15 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 01:29:16 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 01:29:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 01:29:17 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cfc947b533a3ed8b8ce79820c7fe5e7634bf9c08479ed0aee1e74ee7b4f2b068`  
		Last Modified: Tue, 12 Jul 2022 00:45:41 GMT  
		Size: 53.7 MB (53683129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca36aa4204d2a708dcd1d41d1d4a128b095f8d88a2f9544f89799c36914e356`  
		Last Modified: Tue, 12 Jul 2022 02:42:29 GMT  
		Size: 5.1 MB (5142960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdcd2014de70fbce8c43a70cd1f42bceab4f1e35953db987fc318dbc0fb0d26`  
		Last Modified: Tue, 12 Jul 2022 02:42:30 GMT  
		Size: 10.7 MB (10657500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099450cf5212ff57fa7236e4391a4095fa42bc6d23fdb15869367ae44e396a37`  
		Last Modified: Wed, 13 Jul 2022 01:29:42 GMT  
		Size: 18.4 MB (18382881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19eef7412ec39d1a75650a00b44d7b79179cf36dd748bd466ec7bdad6841137`  
		Last Modified: Wed, 13 Jul 2022 01:29:39 GMT  
		Size: 2.9 KB (2869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccef8ee42539528cbfc4baa7cb82663010375fa1deaf4abd07fb87fc5c9c3a14`  
		Last Modified: Wed, 13 Jul 2022 01:30:20 GMT  
		Size: 37.9 MB (37874271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9b7359533194b5c67c5d65cf220b089a93feb263208f0b0576bac0d45acb82`  
		Last Modified: Wed, 13 Jul 2022 01:30:14 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.23.2-alpine`

```console
$ docker pull telegraf@sha256:005ab6c1bac77aab1725395335ffb33eeec35e0f6db774554a0ce0d29cc8996c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.23.2-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:814678d57c5b75e0d38a9c9e0b16fe218681db3b90496d6272c019dede9e92ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47706813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5288c877257e0b347e8af5c2ce7cb2c41dfe81a1be9456e29aa9493acce1b69a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:25:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 20 Jul 2022 02:25:58 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Wed, 20 Jul 2022 02:26:20 GMT
ENV TELEGRAF_VERSION=1.23.2
# Wed, 20 Jul 2022 02:26:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 20 Jul 2022 02:26:28 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 20 Jul 2022 02:26:28 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Wed, 20 Jul 2022 02:26:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Jul 2022 02:26:28 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1d6c3bdc90884e20be4b8964afbc50fc83dac03969c542117bb4c4e59802fb`  
		Last Modified: Wed, 20 Jul 2022 02:26:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7afda0100e244bcaa7520aff1df3205abf84be1593c127ee83151d1395be22`  
		Last Modified: Wed, 20 Jul 2022 02:26:49 GMT  
		Size: 3.4 MB (3372891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971da97d895cca6554946fe061f528b7a23cef4eb70d22ee904fafe92648533c`  
		Last Modified: Wed, 20 Jul 2022 02:27:28 GMT  
		Size: 41.5 MB (41518796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3739c19c31dfe897e281af0e79cf4856473a21d54a2cb6cd62591ad0f0a1731a`  
		Last Modified: Wed, 20 Jul 2022 02:27:21 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:005ab6c1bac77aab1725395335ffb33eeec35e0f6db774554a0ce0d29cc8996c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:814678d57c5b75e0d38a9c9e0b16fe218681db3b90496d6272c019dede9e92ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47706813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5288c877257e0b347e8af5c2ce7cb2c41dfe81a1be9456e29aa9493acce1b69a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:25:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 20 Jul 2022 02:25:58 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Wed, 20 Jul 2022 02:26:20 GMT
ENV TELEGRAF_VERSION=1.23.2
# Wed, 20 Jul 2022 02:26:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 20 Jul 2022 02:26:28 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 20 Jul 2022 02:26:28 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Wed, 20 Jul 2022 02:26:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Jul 2022 02:26:28 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1d6c3bdc90884e20be4b8964afbc50fc83dac03969c542117bb4c4e59802fb`  
		Last Modified: Wed, 20 Jul 2022 02:26:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7afda0100e244bcaa7520aff1df3205abf84be1593c127ee83151d1395be22`  
		Last Modified: Wed, 20 Jul 2022 02:26:49 GMT  
		Size: 3.4 MB (3372891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971da97d895cca6554946fe061f528b7a23cef4eb70d22ee904fafe92648533c`  
		Last Modified: Wed, 20 Jul 2022 02:27:28 GMT  
		Size: 41.5 MB (41518796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3739c19c31dfe897e281af0e79cf4856473a21d54a2cb6cd62591ad0f0a1731a`  
		Last Modified: Wed, 20 Jul 2022 02:27:21 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:583de522849dd3335fc8365b28983b51e69a0a8e7851982ea337c68e892bb9c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:e3eef6a27482a8e8a1f1bd718e9b1cc819340e52f849a1dc93783757f6580ac6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131477605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11676beafdbe2c3cfaaa14432120397f0f43dcc9a5d01468334bf99352802c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 01:19:57 GMT
ADD file:3451708ab45bc1bcfc1ebb2075d3af16767477cbeb79334959e0d1ff02b0864b in / 
# Tue, 12 Jul 2022 01:19:58 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:48:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 00:51:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 00:51:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 00:51:35 GMT
ENV TELEGRAF_VERSION=1.23.2
# Wed, 13 Jul 2022 00:51:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 00:51:39 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 00:51:39 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 00:51:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 00:51:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d836772a1c1f9c4b1f280fb2a98ace30a4c4c87370f89aa092b35dfd9556278a`  
		Last Modified: Tue, 12 Jul 2022 01:24:06 GMT  
		Size: 55.0 MB (54999406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9e63c657ad881997f5165c0826be395bfc064415876b9fbaae74bcb5dc721`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 5.2 MB (5156110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1989b6e74cfdda1591b9dd23be47c5caeb002b7a151379361ec0c3f0e6d0e52`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 10.9 MB (10876416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15796d428c46a6a6a6313c2bac0a095deacb13167f82adb559eb6176ec2af29c`  
		Last Modified: Wed, 13 Jul 2022 00:52:03 GMT  
		Size: 18.8 MB (18760391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0216c283a6188b969faf59c6e7426df41a6d4eb5c4fc0322b363da41ed51f5e7`  
		Last Modified: Wed, 13 Jul 2022 00:52:00 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6c91432eb33f615f7769e025212187a24ea51091cbf45ed021029e16783d98`  
		Last Modified: Wed, 13 Jul 2022 00:52:42 GMT  
		Size: 41.7 MB (41682044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5858ef52fd16a141493f30423c6c6f8b8fa0eab849425e5c7911510465d72ebc`  
		Last Modified: Wed, 13 Jul 2022 00:52:35 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:13cf4e63816b971b2956ef710642f6c416a22fc644be0ab86f419cbf79c7914e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121775920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf31cbeb266a7ab780a82929973ebda033602028c0f875a512cb480fa0790237`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 00:59:16 GMT
ADD file:72ef8362158fcd45f10c6fa2dc3ea411e81f700ecb92faf37cb6dc1887756f9d in / 
# Tue, 12 Jul 2022 00:59:17 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 03:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 03:28:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 21:46:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 21:46:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 21:47:27 GMT
ENV TELEGRAF_VERSION=1.23.2
# Wed, 13 Jul 2022 21:47:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 21:47:39 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 21:47:40 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 21:47:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 21:47:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a8a55ed160b9a554de2e46b828d606a0829d8d9f19c79bc47eddac683aeb2b91`  
		Last Modified: Tue, 12 Jul 2022 01:11:51 GMT  
		Size: 50.2 MB (50194881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5042ae471fd57ff8851607bf0b66366fbd0a499a0ce088f1fb39c5a1caf4123e`  
		Last Modified: Tue, 12 Jul 2022 03:50:27 GMT  
		Size: 4.9 MB (4924746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70da2acc639b7236796e6cb2a0b0e3a21e6f32f8a507bdbfb823a510caf8e75a`  
		Last Modified: Tue, 12 Jul 2022 03:50:29 GMT  
		Size: 10.2 MB (10218056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0992d5af0c071c385deec4002f52d299bee3cbcc3c6bc0ef2e42061a76a537c`  
		Last Modified: Wed, 13 Jul 2022 21:48:37 GMT  
		Size: 17.5 MB (17462343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51a28192fdc11036097b81d3334c36a8facd680b71c81d8d1c9c7260c1965a9`  
		Last Modified: Wed, 13 Jul 2022 21:48:24 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf3ca93915b927d60ae79e264fdbcf2c79f75e0d6c4e722b14ff3d00ff57734`  
		Last Modified: Wed, 13 Jul 2022 21:50:09 GMT  
		Size: 39.0 MB (38972660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5990ca770cb06ccfc134f44fb0b9b3626585d4dda528c49f19092431216bd2a3`  
		Last Modified: Wed, 13 Jul 2022 21:49:41 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d2694ede98ea8d1b8005a72d3f657b5db8d80270579d70d21a1cb65e07291e4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125743953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb685a759d4f9ecd31e72ad90ae31d8823e84c34031d3a703af9b6c49fb0873`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:18 GMT
ADD file:2dcc013bca5a420cad3b6a1ac61f52ea58a29ae05fe282078a744979c0e1a89e in / 
# Tue, 12 Jul 2022 00:40:19 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:33:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:33:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 01:28:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 01:28:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 01:29:09 GMT
ENV TELEGRAF_VERSION=1.23.2
# Wed, 13 Jul 2022 01:29:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 13 Jul 2022 01:29:15 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Jul 2022 01:29:16 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 13 Jul 2022 01:29:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 01:29:17 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cfc947b533a3ed8b8ce79820c7fe5e7634bf9c08479ed0aee1e74ee7b4f2b068`  
		Last Modified: Tue, 12 Jul 2022 00:45:41 GMT  
		Size: 53.7 MB (53683129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca36aa4204d2a708dcd1d41d1d4a128b095f8d88a2f9544f89799c36914e356`  
		Last Modified: Tue, 12 Jul 2022 02:42:29 GMT  
		Size: 5.1 MB (5142960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdcd2014de70fbce8c43a70cd1f42bceab4f1e35953db987fc318dbc0fb0d26`  
		Last Modified: Tue, 12 Jul 2022 02:42:30 GMT  
		Size: 10.7 MB (10657500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099450cf5212ff57fa7236e4391a4095fa42bc6d23fdb15869367ae44e396a37`  
		Last Modified: Wed, 13 Jul 2022 01:29:42 GMT  
		Size: 18.4 MB (18382881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19eef7412ec39d1a75650a00b44d7b79179cf36dd748bd466ec7bdad6841137`  
		Last Modified: Wed, 13 Jul 2022 01:29:39 GMT  
		Size: 2.9 KB (2869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccef8ee42539528cbfc4baa7cb82663010375fa1deaf4abd07fb87fc5c9c3a14`  
		Last Modified: Wed, 13 Jul 2022 01:30:20 GMT  
		Size: 37.9 MB (37874271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9b7359533194b5c67c5d65cf220b089a93feb263208f0b0576bac0d45acb82`  
		Last Modified: Wed, 13 Jul 2022 01:30:14 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
