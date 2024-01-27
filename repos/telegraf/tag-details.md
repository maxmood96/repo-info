<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.27`](#telegraf127)
-	[`telegraf:1.27-alpine`](#telegraf127-alpine)
-	[`telegraf:1.27.4`](#telegraf1274)
-	[`telegraf:1.27.4-alpine`](#telegraf1274-alpine)
-	[`telegraf:1.28`](#telegraf128)
-	[`telegraf:1.28-alpine`](#telegraf128-alpine)
-	[`telegraf:1.28.5`](#telegraf1285)
-	[`telegraf:1.28.5-alpine`](#telegraf1285-alpine)
-	[`telegraf:1.29`](#telegraf129)
-	[`telegraf:1.29-alpine`](#telegraf129-alpine)
-	[`telegraf:1.29.2`](#telegraf1292)
-	[`telegraf:1.29.2-alpine`](#telegraf1292-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.27`

```console
$ docker pull telegraf@sha256:03f3123d2fb5146ad7194b1c8d97dd1e1ba68bafdef2e115906302afe19a59a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.27` - linux; amd64

```console
$ docker pull telegraf@sha256:07f698599a8fc788520db381080337534c78267db90c99fbbb121661c13557d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148088305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e846078b2120c1b9f3b7809eb78e79f61eddb0727262a997e3fc95a21df435`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:35:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:26:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:26:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 15:26:15 GMT
ENV TELEGRAF_VERSION=1.27.4
# Thu, 11 Jan 2024 15:26:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 15:26:22 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 15:26:22 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 15:26:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 15:26:22 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c74526957fc2157e8b0989072dc99b9582b398c12d1dcd40270fd76231bab0c`  
		Last Modified: Thu, 11 Jan 2024 04:44:35 GMT  
		Size: 24.0 MB (24046494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c05294ba0e56ba5bbc3718dec61a92f9d1433d187ac4a3c3cea2b58fd39b0d`  
		Last Modified: Thu, 11 Jan 2024 15:27:05 GMT  
		Size: 19.2 MB (19151386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ead2fc4375e772701e01ef14f0cb22b950d2d66691f8412a879def625a6e86e`  
		Last Modified: Thu, 11 Jan 2024 15:27:02 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d9f1cf2d8463140edbf22bd1ca9a6cf36c340e22b94a52e41834405f7d4bb8`  
		Last Modified: Thu, 11 Jan 2024 15:27:11 GMT  
		Size: 55.3 MB (55326776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b6b9e67dea38fddcbd8f0557010d745fd084e5564537c12efd1f26b1092ece`  
		Last Modified: Thu, 11 Jan 2024 15:27:02 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:bdbf338063a413799c03b135e9ff47e6db24ee76219005fc6e91b9fe94e8f10f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136544526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6547dc583eaa5e3ff719b4c6730c01ff0bd29193686d977c9631335d9d6a8aa0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:52 GMT
ADD file:781c48325e0a88993e9f749e0cd761de39d671e9a23223797cb25431ac40d39a in / 
# Thu, 11 Jan 2024 02:41:52 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:14:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 21:36:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 21:36:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 21:36:06 GMT
ENV TELEGRAF_VERSION=1.27.4
# Thu, 11 Jan 2024 21:36:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 21:36:17 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 21:36:18 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 21:36:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 21:36:18 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1d306580a85c9098725ffcffdc42e708e47695a4be4626d1dc152e55ec7f04c2`  
		Last Modified: Thu, 11 Jan 2024 02:48:11 GMT  
		Size: 45.2 MB (45156672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f838a77ac7b077a6478dbd3e8ae86811e8e8421b22a470d01688f320c26ea3`  
		Last Modified: Thu, 11 Jan 2024 03:28:50 GMT  
		Size: 21.9 MB (21949911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0269dbb76a185200cdcc88613c6b4567e60171be4b8b7ba0a7595a2835e6228f`  
		Last Modified: Thu, 11 Jan 2024 21:37:11 GMT  
		Size: 17.9 MB (17929961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1113a4af12ec76f8e7b77fafb8870cff6e2e0dfe90112ece75128dd0ebeee668`  
		Last Modified: Thu, 11 Jan 2024 21:37:06 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062bb1f2d78fe7fa523466942e000874a8570a1d6749c20192e9812cb263bcf5`  
		Last Modified: Thu, 11 Jan 2024 21:37:18 GMT  
		Size: 51.5 MB (51505825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be45e2afb8fc8f5a27b72a77cc864d3571f758c90d9a29fa39b958332f96c78a`  
		Last Modified: Thu, 11 Jan 2024 21:37:06 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:407f99b1caad28dd837742f6ad0caae12ff627879b6b22c28c9a378567a5ed8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142210634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36157564fd6804c512ab6e8de76a2dbed721c592ff3d9fd853e16bccefadf70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:46:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:46:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 15:46:33 GMT
ENV TELEGRAF_VERSION=1.27.4
# Thu, 11 Jan 2024 15:46:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 15:46:39 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 15:46:39 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 15:46:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 15:46:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f419b1a62fc83850ab3cb43274970bb20a18ae6e674535478a48f5bee11559b6`  
		Last Modified: Thu, 11 Jan 2024 09:34:07 GMT  
		Size: 23.6 MB (23582592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc6d96557ca39bf32423374ddf825dadcd91ffc484e19230e6f7bb5ef8ce4cd`  
		Last Modified: Thu, 11 Jan 2024 15:47:19 GMT  
		Size: 19.1 MB (19075022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fc85ea3b1e88d74db019f4f2cd5a63af935b115e231f8bfc1485e9bc814a95`  
		Last Modified: Thu, 11 Jan 2024 15:47:17 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66945c04f4ddb5f07d1b40ab39f79a87f62fff325cfe1c4d070d54e064d07dce`  
		Last Modified: Thu, 11 Jan 2024 15:47:22 GMT  
		Size: 50.0 MB (49958628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6520f70ba9da3ebbcad2a887334086b25497fe2a40bb589a8fd6b4129cdf8ab2`  
		Last Modified: Thu, 11 Jan 2024 15:47:16 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.27-alpine`

```console
$ docker pull telegraf@sha256:90628fc283952650d48052ee49024f4fc44cef176809b5c1a6f14a1e7ff43096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.27-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:feb1cc34bb4b9dfbd68131b7a2ab7623beaaf8ed29fde7682b1d9d621e9d8a9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61200515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6d36aec2bd3d065085dee9f3977c8fdfce3bd4878ea2edac98b3ebe355b9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:11:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:42:21 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 27 Jan 2024 05:42:21 GMT
ENV TELEGRAF_VERSION=1.27.4
# Sat, 27 Jan 2024 05:42:28 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 27 Jan 2024 05:42:28 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 27 Jan 2024 05:42:28 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 27 Jan 2024 05:42:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:42:28 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c0340c3b428b118deb541dd857e5413c0ea787e9ba56ae54589ea731c7730`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7f76cfdeef9f66d9fe75a233da721a0a053d88f490e69cd2640b17a3a4e99f`  
		Last Modified: Sat, 27 Jan 2024 05:43:11 GMT  
		Size: 2.6 MB (2645448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606821afbe463e87ab9d99dea66ab7a16e41bc5c351be47ab7142f32a6f05562`  
		Last Modified: Sat, 27 Jan 2024 05:43:23 GMT  
		Size: 55.2 MB (55151916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f57d9c7f0880931bb532ab2847499a03aa0c2739364d923fecbf610f76da17`  
		Last Modified: Sat, 27 Jan 2024 05:43:10 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:81a22be451ad61262e2e845b0e952b5ecab90dcda33d0132270c8d0ebad0948e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55802254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9748d607314d681a98f3b3bb2ce197b6590612c303c216d466e900d82b8ff2be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:38:30 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 09:29:37 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Fri, 01 Dec 2023 09:29:37 GMT
ENV TELEGRAF_VERSION=1.27.4
# Fri, 01 Dec 2023 09:29:45 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Fri, 01 Dec 2023 09:29:46 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 01 Dec 2023 09:29:46 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Fri, 01 Dec 2023 09:29:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 09:29:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f6ef2d119bdc2b844474b1941025c80c2a28072d415011a971ae3decceb4b8`  
		Last Modified: Fri, 01 Dec 2023 02:38:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca0a892394cd6b625d7d9cdb3d4bc69df64526779bd31ca9403a55bbbcca5c0`  
		Last Modified: Fri, 01 Dec 2023 09:30:27 GMT  
		Size: 2.7 MB (2673204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f41763daa90737683bffe594355f6ebc25c058ad7ca145f984dc1d8c142a6d`  
		Last Modified: Fri, 01 Dec 2023 09:30:32 GMT  
		Size: 49.8 MB (49795411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cea42bfc317e0b40fc34a99d9e45748b94b370205d160463aba9fbda67c27c7`  
		Last Modified: Fri, 01 Dec 2023 09:30:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.27.4`

```console
$ docker pull telegraf@sha256:03f3123d2fb5146ad7194b1c8d97dd1e1ba68bafdef2e115906302afe19a59a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.27.4` - linux; amd64

```console
$ docker pull telegraf@sha256:07f698599a8fc788520db381080337534c78267db90c99fbbb121661c13557d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148088305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e846078b2120c1b9f3b7809eb78e79f61eddb0727262a997e3fc95a21df435`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:35:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:26:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:26:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 15:26:15 GMT
ENV TELEGRAF_VERSION=1.27.4
# Thu, 11 Jan 2024 15:26:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 15:26:22 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 15:26:22 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 15:26:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 15:26:22 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c74526957fc2157e8b0989072dc99b9582b398c12d1dcd40270fd76231bab0c`  
		Last Modified: Thu, 11 Jan 2024 04:44:35 GMT  
		Size: 24.0 MB (24046494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c05294ba0e56ba5bbc3718dec61a92f9d1433d187ac4a3c3cea2b58fd39b0d`  
		Last Modified: Thu, 11 Jan 2024 15:27:05 GMT  
		Size: 19.2 MB (19151386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ead2fc4375e772701e01ef14f0cb22b950d2d66691f8412a879def625a6e86e`  
		Last Modified: Thu, 11 Jan 2024 15:27:02 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d9f1cf2d8463140edbf22bd1ca9a6cf36c340e22b94a52e41834405f7d4bb8`  
		Last Modified: Thu, 11 Jan 2024 15:27:11 GMT  
		Size: 55.3 MB (55326776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b6b9e67dea38fddcbd8f0557010d745fd084e5564537c12efd1f26b1092ece`  
		Last Modified: Thu, 11 Jan 2024 15:27:02 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:bdbf338063a413799c03b135e9ff47e6db24ee76219005fc6e91b9fe94e8f10f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136544526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6547dc583eaa5e3ff719b4c6730c01ff0bd29193686d977c9631335d9d6a8aa0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:52 GMT
ADD file:781c48325e0a88993e9f749e0cd761de39d671e9a23223797cb25431ac40d39a in / 
# Thu, 11 Jan 2024 02:41:52 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:14:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 21:36:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 21:36:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 21:36:06 GMT
ENV TELEGRAF_VERSION=1.27.4
# Thu, 11 Jan 2024 21:36:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 21:36:17 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 21:36:18 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 21:36:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 21:36:18 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1d306580a85c9098725ffcffdc42e708e47695a4be4626d1dc152e55ec7f04c2`  
		Last Modified: Thu, 11 Jan 2024 02:48:11 GMT  
		Size: 45.2 MB (45156672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f838a77ac7b077a6478dbd3e8ae86811e8e8421b22a470d01688f320c26ea3`  
		Last Modified: Thu, 11 Jan 2024 03:28:50 GMT  
		Size: 21.9 MB (21949911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0269dbb76a185200cdcc88613c6b4567e60171be4b8b7ba0a7595a2835e6228f`  
		Last Modified: Thu, 11 Jan 2024 21:37:11 GMT  
		Size: 17.9 MB (17929961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1113a4af12ec76f8e7b77fafb8870cff6e2e0dfe90112ece75128dd0ebeee668`  
		Last Modified: Thu, 11 Jan 2024 21:37:06 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062bb1f2d78fe7fa523466942e000874a8570a1d6749c20192e9812cb263bcf5`  
		Last Modified: Thu, 11 Jan 2024 21:37:18 GMT  
		Size: 51.5 MB (51505825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be45e2afb8fc8f5a27b72a77cc864d3571f758c90d9a29fa39b958332f96c78a`  
		Last Modified: Thu, 11 Jan 2024 21:37:06 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:407f99b1caad28dd837742f6ad0caae12ff627879b6b22c28c9a378567a5ed8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142210634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36157564fd6804c512ab6e8de76a2dbed721c592ff3d9fd853e16bccefadf70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:46:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:46:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 15:46:33 GMT
ENV TELEGRAF_VERSION=1.27.4
# Thu, 11 Jan 2024 15:46:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 15:46:39 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 15:46:39 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 15:46:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 15:46:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f419b1a62fc83850ab3cb43274970bb20a18ae6e674535478a48f5bee11559b6`  
		Last Modified: Thu, 11 Jan 2024 09:34:07 GMT  
		Size: 23.6 MB (23582592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc6d96557ca39bf32423374ddf825dadcd91ffc484e19230e6f7bb5ef8ce4cd`  
		Last Modified: Thu, 11 Jan 2024 15:47:19 GMT  
		Size: 19.1 MB (19075022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fc85ea3b1e88d74db019f4f2cd5a63af935b115e231f8bfc1485e9bc814a95`  
		Last Modified: Thu, 11 Jan 2024 15:47:17 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66945c04f4ddb5f07d1b40ab39f79a87f62fff325cfe1c4d070d54e064d07dce`  
		Last Modified: Thu, 11 Jan 2024 15:47:22 GMT  
		Size: 50.0 MB (49958628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6520f70ba9da3ebbcad2a887334086b25497fe2a40bb589a8fd6b4129cdf8ab2`  
		Last Modified: Thu, 11 Jan 2024 15:47:16 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.27.4-alpine`

```console
$ docker pull telegraf@sha256:90628fc283952650d48052ee49024f4fc44cef176809b5c1a6f14a1e7ff43096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.27.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:feb1cc34bb4b9dfbd68131b7a2ab7623beaaf8ed29fde7682b1d9d621e9d8a9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61200515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6d36aec2bd3d065085dee9f3977c8fdfce3bd4878ea2edac98b3ebe355b9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:11:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:42:21 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 27 Jan 2024 05:42:21 GMT
ENV TELEGRAF_VERSION=1.27.4
# Sat, 27 Jan 2024 05:42:28 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 27 Jan 2024 05:42:28 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 27 Jan 2024 05:42:28 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 27 Jan 2024 05:42:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:42:28 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c0340c3b428b118deb541dd857e5413c0ea787e9ba56ae54589ea731c7730`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7f76cfdeef9f66d9fe75a233da721a0a053d88f490e69cd2640b17a3a4e99f`  
		Last Modified: Sat, 27 Jan 2024 05:43:11 GMT  
		Size: 2.6 MB (2645448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606821afbe463e87ab9d99dea66ab7a16e41bc5c351be47ab7142f32a6f05562`  
		Last Modified: Sat, 27 Jan 2024 05:43:23 GMT  
		Size: 55.2 MB (55151916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f57d9c7f0880931bb532ab2847499a03aa0c2739364d923fecbf610f76da17`  
		Last Modified: Sat, 27 Jan 2024 05:43:10 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:81a22be451ad61262e2e845b0e952b5ecab90dcda33d0132270c8d0ebad0948e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55802254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9748d607314d681a98f3b3bb2ce197b6590612c303c216d466e900d82b8ff2be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:38:30 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 09:29:37 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Fri, 01 Dec 2023 09:29:37 GMT
ENV TELEGRAF_VERSION=1.27.4
# Fri, 01 Dec 2023 09:29:45 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Fri, 01 Dec 2023 09:29:46 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 01 Dec 2023 09:29:46 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Fri, 01 Dec 2023 09:29:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 09:29:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f6ef2d119bdc2b844474b1941025c80c2a28072d415011a971ae3decceb4b8`  
		Last Modified: Fri, 01 Dec 2023 02:38:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca0a892394cd6b625d7d9cdb3d4bc69df64526779bd31ca9403a55bbbcca5c0`  
		Last Modified: Fri, 01 Dec 2023 09:30:27 GMT  
		Size: 2.7 MB (2673204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f41763daa90737683bffe594355f6ebc25c058ad7ca145f984dc1d8c142a6d`  
		Last Modified: Fri, 01 Dec 2023 09:30:32 GMT  
		Size: 49.8 MB (49795411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cea42bfc317e0b40fc34a99d9e45748b94b370205d160463aba9fbda67c27c7`  
		Last Modified: Fri, 01 Dec 2023 09:30:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28`

```console
$ docker pull telegraf@sha256:2183389989f1e04f077447d711af2417a039308d33787d728c72a542a1284bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.28` - linux; amd64

```console
$ docker pull telegraf@sha256:5b6801424d78046b2964045f5b888e358ed7bc5ca669d9111afbdc6dde6f9c9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149850575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bd6c531b3e899f419b362c42cecf252b4415cfeeafb4a41436e731c2f59b39`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:35:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:26:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:26:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 15:26:28 GMT
ENV TELEGRAF_VERSION=1.28.5
# Thu, 11 Jan 2024 15:26:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 15:26:36 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 15:26:36 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 15:26:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 15:26:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c74526957fc2157e8b0989072dc99b9582b398c12d1dcd40270fd76231bab0c`  
		Last Modified: Thu, 11 Jan 2024 04:44:35 GMT  
		Size: 24.0 MB (24046494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c05294ba0e56ba5bbc3718dec61a92f9d1433d187ac4a3c3cea2b58fd39b0d`  
		Last Modified: Thu, 11 Jan 2024 15:27:05 GMT  
		Size: 19.2 MB (19151386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ead2fc4375e772701e01ef14f0cb22b950d2d66691f8412a879def625a6e86e`  
		Last Modified: Thu, 11 Jan 2024 15:27:02 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e3daddb350177ab4c699c18ffe9fd94e6638c3a365aaf73ee6e78c0eef41fcd`  
		Last Modified: Thu, 11 Jan 2024 15:27:31 GMT  
		Size: 57.1 MB (57089045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017d62ffbfb19d36d23e2fbe82afc582047e7262705f5b4a65596797f62e2f34`  
		Last Modified: Thu, 11 Jan 2024 15:27:22 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:8531ab4e81b2c31f2bc006b4cbde7f019b37765f9142b4a404250ef3ebb9876d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137593276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ce00085a87b7147754283534551bd22c7ac9ddeb09b933662dd32912afc6b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:52 GMT
ADD file:781c48325e0a88993e9f749e0cd761de39d671e9a23223797cb25431ac40d39a in / 
# Thu, 11 Jan 2024 02:41:52 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:14:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 21:36:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 21:36:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 21:36:22 GMT
ENV TELEGRAF_VERSION=1.28.5
# Thu, 11 Jan 2024 21:36:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 21:36:35 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 21:36:35 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 21:36:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 21:36:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1d306580a85c9098725ffcffdc42e708e47695a4be4626d1dc152e55ec7f04c2`  
		Last Modified: Thu, 11 Jan 2024 02:48:11 GMT  
		Size: 45.2 MB (45156672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f838a77ac7b077a6478dbd3e8ae86811e8e8421b22a470d01688f320c26ea3`  
		Last Modified: Thu, 11 Jan 2024 03:28:50 GMT  
		Size: 21.9 MB (21949911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0269dbb76a185200cdcc88613c6b4567e60171be4b8b7ba0a7595a2835e6228f`  
		Last Modified: Thu, 11 Jan 2024 21:37:11 GMT  
		Size: 17.9 MB (17929961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1113a4af12ec76f8e7b77fafb8870cff6e2e0dfe90112ece75128dd0ebeee668`  
		Last Modified: Thu, 11 Jan 2024 21:37:06 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7f024868e7cbecd113c0bca94fe667ff87b7fecd0d20666a264b0afc027741`  
		Last Modified: Thu, 11 Jan 2024 21:37:38 GMT  
		Size: 52.6 MB (52554574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7fa75745ad23ba3267cc899784bed9fbb00dd9817c670e2d95b388a534352b`  
		Last Modified: Thu, 11 Jan 2024 21:37:27 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:74f2ceaf55f8939badb9baa991689d333ef9fe248dea50c5fb7911cf97727a60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144002567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f074e59cf770eb8f6fda850caad59971e34f431b8ac288d56916385bf1a648`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:46:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:46:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 15:46:45 GMT
ENV TELEGRAF_VERSION=1.28.5
# Thu, 11 Jan 2024 15:46:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 15:46:52 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 15:46:52 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 15:46:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 15:46:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f419b1a62fc83850ab3cb43274970bb20a18ae6e674535478a48f5bee11559b6`  
		Last Modified: Thu, 11 Jan 2024 09:34:07 GMT  
		Size: 23.6 MB (23582592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc6d96557ca39bf32423374ddf825dadcd91ffc484e19230e6f7bb5ef8ce4cd`  
		Last Modified: Thu, 11 Jan 2024 15:47:19 GMT  
		Size: 19.1 MB (19075022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fc85ea3b1e88d74db019f4f2cd5a63af935b115e231f8bfc1485e9bc814a95`  
		Last Modified: Thu, 11 Jan 2024 15:47:17 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22471460e352619c229bf4ca264b2b59133ce0371a2fd341ca978e93e02be11e`  
		Last Modified: Thu, 11 Jan 2024 15:47:38 GMT  
		Size: 51.8 MB (51750561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b15bd802e9076de443adcaea72b2d0216811cce51ef4518083998a3a09c41c`  
		Last Modified: Thu, 11 Jan 2024 15:47:32 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28-alpine`

```console
$ docker pull telegraf@sha256:e1abb4a0c9189a73ceabfc7c66d71d01f3617d57faabd95b86037cd1036f8b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.28-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:3bb11df50410aeb8458d6a6b64f6b9751cbf6b4e16caec556f0811a90b705ab6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62961732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5d886307f1b4b075b4e863bfa404100eb7c953053b50333e6deaeff21ac680`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:11:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:42:21 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 27 Jan 2024 05:42:34 GMT
ENV TELEGRAF_VERSION=1.28.5
# Sat, 27 Jan 2024 05:42:41 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 27 Jan 2024 05:42:41 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 27 Jan 2024 05:42:41 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 27 Jan 2024 05:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:42:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c0340c3b428b118deb541dd857e5413c0ea787e9ba56ae54589ea731c7730`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7f76cfdeef9f66d9fe75a233da721a0a053d88f490e69cd2640b17a3a4e99f`  
		Last Modified: Sat, 27 Jan 2024 05:43:11 GMT  
		Size: 2.6 MB (2645448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e268102e23744f632353e792f109fb094fe94b23291aecb8132b4d213638c5`  
		Last Modified: Sat, 27 Jan 2024 05:43:41 GMT  
		Size: 56.9 MB (56913132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2008d4aa510f12b12224faadbabb4162029e5ad0c812da3178829a3364988b88`  
		Last Modified: Sat, 27 Jan 2024 05:43:33 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:9abd92c798e7a04f30103b1c909296a6f752b93258711d6736f41565a14e77f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57594128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c1be5420f2256037606879501b68b596b7270f939e5b0742cc880ce4da97cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:38:30 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 09:29:37 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Fri, 01 Dec 2023 09:29:51 GMT
ENV TELEGRAF_VERSION=1.28.5
# Fri, 01 Dec 2023 09:29:56 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Fri, 01 Dec 2023 09:29:57 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 01 Dec 2023 09:29:58 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Fri, 01 Dec 2023 09:29:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 09:29:58 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f6ef2d119bdc2b844474b1941025c80c2a28072d415011a971ae3decceb4b8`  
		Last Modified: Fri, 01 Dec 2023 02:38:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca0a892394cd6b625d7d9cdb3d4bc69df64526779bd31ca9403a55bbbcca5c0`  
		Last Modified: Fri, 01 Dec 2023 09:30:27 GMT  
		Size: 2.7 MB (2673204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0966c76ccd38be27a8bf79cd4f6906012dfd128984fa170f86fea2cd6155461`  
		Last Modified: Fri, 01 Dec 2023 09:30:47 GMT  
		Size: 51.6 MB (51587284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d86eebfd2c91e08ee20d44fef32c1ac56d89958f0c0ec81ddd495f2c2011698`  
		Last Modified: Fri, 01 Dec 2023 09:30:41 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28.5`

```console
$ docker pull telegraf@sha256:2183389989f1e04f077447d711af2417a039308d33787d728c72a542a1284bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.28.5` - linux; amd64

```console
$ docker pull telegraf@sha256:5b6801424d78046b2964045f5b888e358ed7bc5ca669d9111afbdc6dde6f9c9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149850575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bd6c531b3e899f419b362c42cecf252b4415cfeeafb4a41436e731c2f59b39`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:35:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:26:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:26:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 15:26:28 GMT
ENV TELEGRAF_VERSION=1.28.5
# Thu, 11 Jan 2024 15:26:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 15:26:36 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 15:26:36 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 15:26:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 15:26:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c74526957fc2157e8b0989072dc99b9582b398c12d1dcd40270fd76231bab0c`  
		Last Modified: Thu, 11 Jan 2024 04:44:35 GMT  
		Size: 24.0 MB (24046494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c05294ba0e56ba5bbc3718dec61a92f9d1433d187ac4a3c3cea2b58fd39b0d`  
		Last Modified: Thu, 11 Jan 2024 15:27:05 GMT  
		Size: 19.2 MB (19151386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ead2fc4375e772701e01ef14f0cb22b950d2d66691f8412a879def625a6e86e`  
		Last Modified: Thu, 11 Jan 2024 15:27:02 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e3daddb350177ab4c699c18ffe9fd94e6638c3a365aaf73ee6e78c0eef41fcd`  
		Last Modified: Thu, 11 Jan 2024 15:27:31 GMT  
		Size: 57.1 MB (57089045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017d62ffbfb19d36d23e2fbe82afc582047e7262705f5b4a65596797f62e2f34`  
		Last Modified: Thu, 11 Jan 2024 15:27:22 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28.5` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:8531ab4e81b2c31f2bc006b4cbde7f019b37765f9142b4a404250ef3ebb9876d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137593276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ce00085a87b7147754283534551bd22c7ac9ddeb09b933662dd32912afc6b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:52 GMT
ADD file:781c48325e0a88993e9f749e0cd761de39d671e9a23223797cb25431ac40d39a in / 
# Thu, 11 Jan 2024 02:41:52 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:14:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 21:36:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 21:36:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 21:36:22 GMT
ENV TELEGRAF_VERSION=1.28.5
# Thu, 11 Jan 2024 21:36:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 21:36:35 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 21:36:35 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 21:36:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 21:36:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1d306580a85c9098725ffcffdc42e708e47695a4be4626d1dc152e55ec7f04c2`  
		Last Modified: Thu, 11 Jan 2024 02:48:11 GMT  
		Size: 45.2 MB (45156672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f838a77ac7b077a6478dbd3e8ae86811e8e8421b22a470d01688f320c26ea3`  
		Last Modified: Thu, 11 Jan 2024 03:28:50 GMT  
		Size: 21.9 MB (21949911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0269dbb76a185200cdcc88613c6b4567e60171be4b8b7ba0a7595a2835e6228f`  
		Last Modified: Thu, 11 Jan 2024 21:37:11 GMT  
		Size: 17.9 MB (17929961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1113a4af12ec76f8e7b77fafb8870cff6e2e0dfe90112ece75128dd0ebeee668`  
		Last Modified: Thu, 11 Jan 2024 21:37:06 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7f024868e7cbecd113c0bca94fe667ff87b7fecd0d20666a264b0afc027741`  
		Last Modified: Thu, 11 Jan 2024 21:37:38 GMT  
		Size: 52.6 MB (52554574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7fa75745ad23ba3267cc899784bed9fbb00dd9817c670e2d95b388a534352b`  
		Last Modified: Thu, 11 Jan 2024 21:37:27 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28.5` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:74f2ceaf55f8939badb9baa991689d333ef9fe248dea50c5fb7911cf97727a60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144002567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f074e59cf770eb8f6fda850caad59971e34f431b8ac288d56916385bf1a648`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:46:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:46:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 15:46:45 GMT
ENV TELEGRAF_VERSION=1.28.5
# Thu, 11 Jan 2024 15:46:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 15:46:52 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 15:46:52 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 15:46:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 15:46:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f419b1a62fc83850ab3cb43274970bb20a18ae6e674535478a48f5bee11559b6`  
		Last Modified: Thu, 11 Jan 2024 09:34:07 GMT  
		Size: 23.6 MB (23582592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc6d96557ca39bf32423374ddf825dadcd91ffc484e19230e6f7bb5ef8ce4cd`  
		Last Modified: Thu, 11 Jan 2024 15:47:19 GMT  
		Size: 19.1 MB (19075022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fc85ea3b1e88d74db019f4f2cd5a63af935b115e231f8bfc1485e9bc814a95`  
		Last Modified: Thu, 11 Jan 2024 15:47:17 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22471460e352619c229bf4ca264b2b59133ce0371a2fd341ca978e93e02be11e`  
		Last Modified: Thu, 11 Jan 2024 15:47:38 GMT  
		Size: 51.8 MB (51750561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b15bd802e9076de443adcaea72b2d0216811cce51ef4518083998a3a09c41c`  
		Last Modified: Thu, 11 Jan 2024 15:47:32 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28.5-alpine`

```console
$ docker pull telegraf@sha256:e1abb4a0c9189a73ceabfc7c66d71d01f3617d57faabd95b86037cd1036f8b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.28.5-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:3bb11df50410aeb8458d6a6b64f6b9751cbf6b4e16caec556f0811a90b705ab6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62961732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5d886307f1b4b075b4e863bfa404100eb7c953053b50333e6deaeff21ac680`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:11:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:42:21 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 27 Jan 2024 05:42:34 GMT
ENV TELEGRAF_VERSION=1.28.5
# Sat, 27 Jan 2024 05:42:41 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 27 Jan 2024 05:42:41 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 27 Jan 2024 05:42:41 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 27 Jan 2024 05:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:42:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c0340c3b428b118deb541dd857e5413c0ea787e9ba56ae54589ea731c7730`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7f76cfdeef9f66d9fe75a233da721a0a053d88f490e69cd2640b17a3a4e99f`  
		Last Modified: Sat, 27 Jan 2024 05:43:11 GMT  
		Size: 2.6 MB (2645448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e268102e23744f632353e792f109fb094fe94b23291aecb8132b4d213638c5`  
		Last Modified: Sat, 27 Jan 2024 05:43:41 GMT  
		Size: 56.9 MB (56913132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2008d4aa510f12b12224faadbabb4162029e5ad0c812da3178829a3364988b88`  
		Last Modified: Sat, 27 Jan 2024 05:43:33 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28.5-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:9abd92c798e7a04f30103b1c909296a6f752b93258711d6736f41565a14e77f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57594128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c1be5420f2256037606879501b68b596b7270f939e5b0742cc880ce4da97cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:38:30 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 09:29:37 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Fri, 01 Dec 2023 09:29:51 GMT
ENV TELEGRAF_VERSION=1.28.5
# Fri, 01 Dec 2023 09:29:56 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Fri, 01 Dec 2023 09:29:57 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 01 Dec 2023 09:29:58 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Fri, 01 Dec 2023 09:29:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 09:29:58 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f6ef2d119bdc2b844474b1941025c80c2a28072d415011a971ae3decceb4b8`  
		Last Modified: Fri, 01 Dec 2023 02:38:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca0a892394cd6b625d7d9cdb3d4bc69df64526779bd31ca9403a55bbbcca5c0`  
		Last Modified: Fri, 01 Dec 2023 09:30:27 GMT  
		Size: 2.7 MB (2673204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0966c76ccd38be27a8bf79cd4f6906012dfd128984fa170f86fea2cd6155461`  
		Last Modified: Fri, 01 Dec 2023 09:30:47 GMT  
		Size: 51.6 MB (51587284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d86eebfd2c91e08ee20d44fef32c1ac56d89958f0c0ec81ddd495f2c2011698`  
		Last Modified: Fri, 01 Dec 2023 09:30:41 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.29`

```console
$ docker pull telegraf@sha256:c5803e78ebf632702d5021a2541a35faa5cdad9855bf0bfb9ee17edc4ce074b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.29` - linux; amd64

```console
$ docker pull telegraf@sha256:19d9cfd4d83f68e0fa5e5fc9f1a490d939cf7c2daf1a70f09981a5b25f78f569
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153428521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe63af8d08384cb910cb3920dd69712da3cf9c98dee890c2104bf6e736b479b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:35:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:26:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:26:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 15:26:41 GMT
ENV TELEGRAF_VERSION=1.29.2
# Thu, 11 Jan 2024 15:26:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 15:26:46 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 15:26:46 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 15:26:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 15:26:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c74526957fc2157e8b0989072dc99b9582b398c12d1dcd40270fd76231bab0c`  
		Last Modified: Thu, 11 Jan 2024 04:44:35 GMT  
		Size: 24.0 MB (24046494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c05294ba0e56ba5bbc3718dec61a92f9d1433d187ac4a3c3cea2b58fd39b0d`  
		Last Modified: Thu, 11 Jan 2024 15:27:05 GMT  
		Size: 19.2 MB (19151386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ead2fc4375e772701e01ef14f0cb22b950d2d66691f8412a879def625a6e86e`  
		Last Modified: Thu, 11 Jan 2024 15:27:02 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a172dbbd3e8f0faac5fa2e2778ab716cd4a5fb67d97a1b536515867b41fe30`  
		Last Modified: Thu, 11 Jan 2024 15:27:49 GMT  
		Size: 60.7 MB (60666992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f7cc3b97f480606ea1722661fe52fb03f5433089a65d9955c49d21f65c2b8b`  
		Last Modified: Thu, 11 Jan 2024 15:27:39 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:2208768cf97f0151b7f85333e3c7556a3215eb8069d4f1918dd66523c67cef3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141668246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a502fb29422d6629fce6e991c0886657ab727be144adbfa6e47a35acbe50af7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:52 GMT
ADD file:781c48325e0a88993e9f749e0cd761de39d671e9a23223797cb25431ac40d39a in / 
# Thu, 11 Jan 2024 02:41:52 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:14:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 21:36:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 21:36:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 21:36:39 GMT
ENV TELEGRAF_VERSION=1.29.2
# Thu, 11 Jan 2024 21:36:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 21:36:52 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 21:36:52 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 21:36:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 21:36:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1d306580a85c9098725ffcffdc42e708e47695a4be4626d1dc152e55ec7f04c2`  
		Last Modified: Thu, 11 Jan 2024 02:48:11 GMT  
		Size: 45.2 MB (45156672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f838a77ac7b077a6478dbd3e8ae86811e8e8421b22a470d01688f320c26ea3`  
		Last Modified: Thu, 11 Jan 2024 03:28:50 GMT  
		Size: 21.9 MB (21949911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0269dbb76a185200cdcc88613c6b4567e60171be4b8b7ba0a7595a2835e6228f`  
		Last Modified: Thu, 11 Jan 2024 21:37:11 GMT  
		Size: 17.9 MB (17929961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1113a4af12ec76f8e7b77fafb8870cff6e2e0dfe90112ece75128dd0ebeee668`  
		Last Modified: Thu, 11 Jan 2024 21:37:06 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936be5c98e79df8ac5094323864dbe43fbfb7cbdb13a455e61f1aca2fcde215d`  
		Last Modified: Thu, 11 Jan 2024 21:37:59 GMT  
		Size: 56.6 MB (56629547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99b077a4318e6b8d301652dfc32289571cca3a6cfe367e843b616d7f085717c`  
		Last Modified: Thu, 11 Jan 2024 21:37:47 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c3af56672cf63eedfd8dd9165d5436cbe76dea4d2595af54a74a9562c92479f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147312945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033cfcdb531b058325025c50ebb48eb2d54a5d39301d0b1c6ef58fead3801b4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:46:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:46:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 15:46:56 GMT
ENV TELEGRAF_VERSION=1.29.2
# Thu, 11 Jan 2024 15:47:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 15:47:01 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 15:47:01 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 15:47:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 15:47:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f419b1a62fc83850ab3cb43274970bb20a18ae6e674535478a48f5bee11559b6`  
		Last Modified: Thu, 11 Jan 2024 09:34:07 GMT  
		Size: 23.6 MB (23582592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc6d96557ca39bf32423374ddf825dadcd91ffc484e19230e6f7bb5ef8ce4cd`  
		Last Modified: Thu, 11 Jan 2024 15:47:19 GMT  
		Size: 19.1 MB (19075022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fc85ea3b1e88d74db019f4f2cd5a63af935b115e231f8bfc1485e9bc814a95`  
		Last Modified: Thu, 11 Jan 2024 15:47:17 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d60192dde374560408f7efbf20e383d4bcfc7385300b53ee6071d30a085cc6b`  
		Last Modified: Thu, 11 Jan 2024 15:47:55 GMT  
		Size: 55.1 MB (55060939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf94769e2bf93462f405f5ef3190c178463f0b24b329f0b69601dce2baeea856`  
		Last Modified: Thu, 11 Jan 2024 15:47:49 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.29-alpine`

```console
$ docker pull telegraf@sha256:3721bbad4cf9416ba5f7a4acfa879b62fa151809e5afc1335d0ceaec80072dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.29-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:71fa7922e7667c7d411abc96c4450ba77e909926a753bd18bbdb1057bf5f22be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66508114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d611373939167bd1bae368a08c5f889b569e9c3ce4f7461c35d560bdf8e958`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 05:42:48 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:42:49 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 27 Jan 2024 05:42:50 GMT
ENV TELEGRAF_VERSION=1.29.2
# Sat, 27 Jan 2024 05:42:56 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 27 Jan 2024 05:42:57 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 27 Jan 2024 05:42:57 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 27 Jan 2024 05:42:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:42:57 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c309218baf98379160fbb980c615eee5c06f955b9cb9d400f34fec882b8c51fe`  
		Last Modified: Sat, 27 Jan 2024 05:43:51 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108d05fcb7baa7ca2f29cf9ae4722b833c411ced538ff572420b87ef4179f038`  
		Last Modified: Sat, 27 Jan 2024 05:43:52 GMT  
		Size: 2.6 MB (2612631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66fbf2c40f5318c1996a423ae05c48d43c6fc70f535f668bc5a979343baf973`  
		Last Modified: Sat, 27 Jan 2024 05:44:01 GMT  
		Size: 60.5 MB (60486150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7d05221158c2cf3df39801d19c83fed89ba9055ec9855360d28621c218ad89`  
		Last Modified: Sat, 27 Jan 2024 05:43:51 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:da0a767e2566e846fa68cbdf2b1438370b1073ebd9a4382c1f9ad0f75cb9f8d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60925375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457fdeee8e6374c9f7a0805a3a58d4b3cf4b4d0d62eb0bbcf4a7df3dfc9be729`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Mon, 11 Dec 2023 20:07:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 11 Dec 2023 20:07:21 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 08 Jan 2024 22:13:19 GMT
ENV TELEGRAF_VERSION=1.29.2
# Mon, 08 Jan 2024 22:13:28 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 08 Jan 2024 22:13:29 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 08 Jan 2024 22:13:29 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 08 Jan 2024 22:13:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jan 2024 22:13:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f827e8bf907751a3e5b3169f3913e7b67c70b21c02477454501cd2043be3c67b`  
		Last Modified: Mon, 11 Dec 2023 20:08:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e495f22bdfc73e46af702cdb849f85f47df776e5075848c4a6ad77b02ec00f34`  
		Last Modified: Mon, 11 Dec 2023 20:08:05 GMT  
		Size: 2.7 MB (2694865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19281e235cd34cb27407d1ab33b1807ab6b87b6efbf03eaa58a4c3f79bf4132a`  
		Last Modified: Mon, 08 Jan 2024 22:14:14 GMT  
		Size: 54.9 MB (54882116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5bc6fc7ebd812348686f4ae5a38911cd1c10500ea3027f8f5cf869e6f4b80c`  
		Last Modified: Mon, 08 Jan 2024 22:14:07 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.29.2`

```console
$ docker pull telegraf@sha256:c5803e78ebf632702d5021a2541a35faa5cdad9855bf0bfb9ee17edc4ce074b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.29.2` - linux; amd64

```console
$ docker pull telegraf@sha256:19d9cfd4d83f68e0fa5e5fc9f1a490d939cf7c2daf1a70f09981a5b25f78f569
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153428521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe63af8d08384cb910cb3920dd69712da3cf9c98dee890c2104bf6e736b479b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:35:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:26:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:26:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 15:26:41 GMT
ENV TELEGRAF_VERSION=1.29.2
# Thu, 11 Jan 2024 15:26:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 15:26:46 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 15:26:46 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 15:26:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 15:26:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c74526957fc2157e8b0989072dc99b9582b398c12d1dcd40270fd76231bab0c`  
		Last Modified: Thu, 11 Jan 2024 04:44:35 GMT  
		Size: 24.0 MB (24046494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c05294ba0e56ba5bbc3718dec61a92f9d1433d187ac4a3c3cea2b58fd39b0d`  
		Last Modified: Thu, 11 Jan 2024 15:27:05 GMT  
		Size: 19.2 MB (19151386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ead2fc4375e772701e01ef14f0cb22b950d2d66691f8412a879def625a6e86e`  
		Last Modified: Thu, 11 Jan 2024 15:27:02 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a172dbbd3e8f0faac5fa2e2778ab716cd4a5fb67d97a1b536515867b41fe30`  
		Last Modified: Thu, 11 Jan 2024 15:27:49 GMT  
		Size: 60.7 MB (60666992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f7cc3b97f480606ea1722661fe52fb03f5433089a65d9955c49d21f65c2b8b`  
		Last Modified: Thu, 11 Jan 2024 15:27:39 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29.2` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:2208768cf97f0151b7f85333e3c7556a3215eb8069d4f1918dd66523c67cef3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141668246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a502fb29422d6629fce6e991c0886657ab727be144adbfa6e47a35acbe50af7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:52 GMT
ADD file:781c48325e0a88993e9f749e0cd761de39d671e9a23223797cb25431ac40d39a in / 
# Thu, 11 Jan 2024 02:41:52 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:14:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 21:36:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 21:36:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 21:36:39 GMT
ENV TELEGRAF_VERSION=1.29.2
# Thu, 11 Jan 2024 21:36:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 21:36:52 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 21:36:52 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 21:36:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 21:36:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1d306580a85c9098725ffcffdc42e708e47695a4be4626d1dc152e55ec7f04c2`  
		Last Modified: Thu, 11 Jan 2024 02:48:11 GMT  
		Size: 45.2 MB (45156672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f838a77ac7b077a6478dbd3e8ae86811e8e8421b22a470d01688f320c26ea3`  
		Last Modified: Thu, 11 Jan 2024 03:28:50 GMT  
		Size: 21.9 MB (21949911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0269dbb76a185200cdcc88613c6b4567e60171be4b8b7ba0a7595a2835e6228f`  
		Last Modified: Thu, 11 Jan 2024 21:37:11 GMT  
		Size: 17.9 MB (17929961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1113a4af12ec76f8e7b77fafb8870cff6e2e0dfe90112ece75128dd0ebeee668`  
		Last Modified: Thu, 11 Jan 2024 21:37:06 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936be5c98e79df8ac5094323864dbe43fbfb7cbdb13a455e61f1aca2fcde215d`  
		Last Modified: Thu, 11 Jan 2024 21:37:59 GMT  
		Size: 56.6 MB (56629547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99b077a4318e6b8d301652dfc32289571cca3a6cfe367e843b616d7f085717c`  
		Last Modified: Thu, 11 Jan 2024 21:37:47 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29.2` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c3af56672cf63eedfd8dd9165d5436cbe76dea4d2595af54a74a9562c92479f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147312945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033cfcdb531b058325025c50ebb48eb2d54a5d39301d0b1c6ef58fead3801b4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:46:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:46:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 15:46:56 GMT
ENV TELEGRAF_VERSION=1.29.2
# Thu, 11 Jan 2024 15:47:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 15:47:01 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 15:47:01 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 15:47:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 15:47:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f419b1a62fc83850ab3cb43274970bb20a18ae6e674535478a48f5bee11559b6`  
		Last Modified: Thu, 11 Jan 2024 09:34:07 GMT  
		Size: 23.6 MB (23582592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc6d96557ca39bf32423374ddf825dadcd91ffc484e19230e6f7bb5ef8ce4cd`  
		Last Modified: Thu, 11 Jan 2024 15:47:19 GMT  
		Size: 19.1 MB (19075022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fc85ea3b1e88d74db019f4f2cd5a63af935b115e231f8bfc1485e9bc814a95`  
		Last Modified: Thu, 11 Jan 2024 15:47:17 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d60192dde374560408f7efbf20e383d4bcfc7385300b53ee6071d30a085cc6b`  
		Last Modified: Thu, 11 Jan 2024 15:47:55 GMT  
		Size: 55.1 MB (55060939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf94769e2bf93462f405f5ef3190c178463f0b24b329f0b69601dce2baeea856`  
		Last Modified: Thu, 11 Jan 2024 15:47:49 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.29.2-alpine`

```console
$ docker pull telegraf@sha256:3721bbad4cf9416ba5f7a4acfa879b62fa151809e5afc1335d0ceaec80072dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.29.2-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:71fa7922e7667c7d411abc96c4450ba77e909926a753bd18bbdb1057bf5f22be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66508114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d611373939167bd1bae368a08c5f889b569e9c3ce4f7461c35d560bdf8e958`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 05:42:48 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:42:49 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 27 Jan 2024 05:42:50 GMT
ENV TELEGRAF_VERSION=1.29.2
# Sat, 27 Jan 2024 05:42:56 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 27 Jan 2024 05:42:57 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 27 Jan 2024 05:42:57 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 27 Jan 2024 05:42:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:42:57 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c309218baf98379160fbb980c615eee5c06f955b9cb9d400f34fec882b8c51fe`  
		Last Modified: Sat, 27 Jan 2024 05:43:51 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108d05fcb7baa7ca2f29cf9ae4722b833c411ced538ff572420b87ef4179f038`  
		Last Modified: Sat, 27 Jan 2024 05:43:52 GMT  
		Size: 2.6 MB (2612631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66fbf2c40f5318c1996a423ae05c48d43c6fc70f535f668bc5a979343baf973`  
		Last Modified: Sat, 27 Jan 2024 05:44:01 GMT  
		Size: 60.5 MB (60486150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7d05221158c2cf3df39801d19c83fed89ba9055ec9855360d28621c218ad89`  
		Last Modified: Sat, 27 Jan 2024 05:43:51 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29.2-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:da0a767e2566e846fa68cbdf2b1438370b1073ebd9a4382c1f9ad0f75cb9f8d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60925375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457fdeee8e6374c9f7a0805a3a58d4b3cf4b4d0d62eb0bbcf4a7df3dfc9be729`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Mon, 11 Dec 2023 20:07:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 11 Dec 2023 20:07:21 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 08 Jan 2024 22:13:19 GMT
ENV TELEGRAF_VERSION=1.29.2
# Mon, 08 Jan 2024 22:13:28 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 08 Jan 2024 22:13:29 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 08 Jan 2024 22:13:29 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 08 Jan 2024 22:13:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jan 2024 22:13:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f827e8bf907751a3e5b3169f3913e7b67c70b21c02477454501cd2043be3c67b`  
		Last Modified: Mon, 11 Dec 2023 20:08:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e495f22bdfc73e46af702cdb849f85f47df776e5075848c4a6ad77b02ec00f34`  
		Last Modified: Mon, 11 Dec 2023 20:08:05 GMT  
		Size: 2.7 MB (2694865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19281e235cd34cb27407d1ab33b1807ab6b87b6efbf03eaa58a4c3f79bf4132a`  
		Last Modified: Mon, 08 Jan 2024 22:14:14 GMT  
		Size: 54.9 MB (54882116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5bc6fc7ebd812348686f4ae5a38911cd1c10500ea3027f8f5cf869e6f4b80c`  
		Last Modified: Mon, 08 Jan 2024 22:14:07 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:3721bbad4cf9416ba5f7a4acfa879b62fa151809e5afc1335d0ceaec80072dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:71fa7922e7667c7d411abc96c4450ba77e909926a753bd18bbdb1057bf5f22be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66508114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d611373939167bd1bae368a08c5f889b569e9c3ce4f7461c35d560bdf8e958`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 05:42:48 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 05:42:49 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 27 Jan 2024 05:42:50 GMT
ENV TELEGRAF_VERSION=1.29.2
# Sat, 27 Jan 2024 05:42:56 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 27 Jan 2024 05:42:57 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 27 Jan 2024 05:42:57 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 27 Jan 2024 05:42:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 05:42:57 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c309218baf98379160fbb980c615eee5c06f955b9cb9d400f34fec882b8c51fe`  
		Last Modified: Sat, 27 Jan 2024 05:43:51 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108d05fcb7baa7ca2f29cf9ae4722b833c411ced538ff572420b87ef4179f038`  
		Last Modified: Sat, 27 Jan 2024 05:43:52 GMT  
		Size: 2.6 MB (2612631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66fbf2c40f5318c1996a423ae05c48d43c6fc70f535f668bc5a979343baf973`  
		Last Modified: Sat, 27 Jan 2024 05:44:01 GMT  
		Size: 60.5 MB (60486150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7d05221158c2cf3df39801d19c83fed89ba9055ec9855360d28621c218ad89`  
		Last Modified: Sat, 27 Jan 2024 05:43:51 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:da0a767e2566e846fa68cbdf2b1438370b1073ebd9a4382c1f9ad0f75cb9f8d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60925375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457fdeee8e6374c9f7a0805a3a58d4b3cf4b4d0d62eb0bbcf4a7df3dfc9be729`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Mon, 11 Dec 2023 20:07:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 11 Dec 2023 20:07:21 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 08 Jan 2024 22:13:19 GMT
ENV TELEGRAF_VERSION=1.29.2
# Mon, 08 Jan 2024 22:13:28 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 08 Jan 2024 22:13:29 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 08 Jan 2024 22:13:29 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 08 Jan 2024 22:13:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jan 2024 22:13:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f827e8bf907751a3e5b3169f3913e7b67c70b21c02477454501cd2043be3c67b`  
		Last Modified: Mon, 11 Dec 2023 20:08:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e495f22bdfc73e46af702cdb849f85f47df776e5075848c4a6ad77b02ec00f34`  
		Last Modified: Mon, 11 Dec 2023 20:08:05 GMT  
		Size: 2.7 MB (2694865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19281e235cd34cb27407d1ab33b1807ab6b87b6efbf03eaa58a4c3f79bf4132a`  
		Last Modified: Mon, 08 Jan 2024 22:14:14 GMT  
		Size: 54.9 MB (54882116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5bc6fc7ebd812348686f4ae5a38911cd1c10500ea3027f8f5cf869e6f4b80c`  
		Last Modified: Mon, 08 Jan 2024 22:14:07 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:c5803e78ebf632702d5021a2541a35faa5cdad9855bf0bfb9ee17edc4ce074b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:19d9cfd4d83f68e0fa5e5fc9f1a490d939cf7c2daf1a70f09981a5b25f78f569
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153428521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe63af8d08384cb910cb3920dd69712da3cf9c98dee890c2104bf6e736b479b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:35:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:26:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:26:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 15:26:41 GMT
ENV TELEGRAF_VERSION=1.29.2
# Thu, 11 Jan 2024 15:26:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 15:26:46 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 15:26:46 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 15:26:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 15:26:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c74526957fc2157e8b0989072dc99b9582b398c12d1dcd40270fd76231bab0c`  
		Last Modified: Thu, 11 Jan 2024 04:44:35 GMT  
		Size: 24.0 MB (24046494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c05294ba0e56ba5bbc3718dec61a92f9d1433d187ac4a3c3cea2b58fd39b0d`  
		Last Modified: Thu, 11 Jan 2024 15:27:05 GMT  
		Size: 19.2 MB (19151386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ead2fc4375e772701e01ef14f0cb22b950d2d66691f8412a879def625a6e86e`  
		Last Modified: Thu, 11 Jan 2024 15:27:02 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a172dbbd3e8f0faac5fa2e2778ab716cd4a5fb67d97a1b536515867b41fe30`  
		Last Modified: Thu, 11 Jan 2024 15:27:49 GMT  
		Size: 60.7 MB (60666992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f7cc3b97f480606ea1722661fe52fb03f5433089a65d9955c49d21f65c2b8b`  
		Last Modified: Thu, 11 Jan 2024 15:27:39 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:2208768cf97f0151b7f85333e3c7556a3215eb8069d4f1918dd66523c67cef3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141668246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a502fb29422d6629fce6e991c0886657ab727be144adbfa6e47a35acbe50af7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:52 GMT
ADD file:781c48325e0a88993e9f749e0cd761de39d671e9a23223797cb25431ac40d39a in / 
# Thu, 11 Jan 2024 02:41:52 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:14:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 21:36:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 21:36:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 21:36:39 GMT
ENV TELEGRAF_VERSION=1.29.2
# Thu, 11 Jan 2024 21:36:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 21:36:52 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 21:36:52 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 21:36:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 21:36:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1d306580a85c9098725ffcffdc42e708e47695a4be4626d1dc152e55ec7f04c2`  
		Last Modified: Thu, 11 Jan 2024 02:48:11 GMT  
		Size: 45.2 MB (45156672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f838a77ac7b077a6478dbd3e8ae86811e8e8421b22a470d01688f320c26ea3`  
		Last Modified: Thu, 11 Jan 2024 03:28:50 GMT  
		Size: 21.9 MB (21949911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0269dbb76a185200cdcc88613c6b4567e60171be4b8b7ba0a7595a2835e6228f`  
		Last Modified: Thu, 11 Jan 2024 21:37:11 GMT  
		Size: 17.9 MB (17929961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1113a4af12ec76f8e7b77fafb8870cff6e2e0dfe90112ece75128dd0ebeee668`  
		Last Modified: Thu, 11 Jan 2024 21:37:06 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936be5c98e79df8ac5094323864dbe43fbfb7cbdb13a455e61f1aca2fcde215d`  
		Last Modified: Thu, 11 Jan 2024 21:37:59 GMT  
		Size: 56.6 MB (56629547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99b077a4318e6b8d301652dfc32289571cca3a6cfe367e843b616d7f085717c`  
		Last Modified: Thu, 11 Jan 2024 21:37:47 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c3af56672cf63eedfd8dd9165d5436cbe76dea4d2595af54a74a9562c92479f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147312945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033cfcdb531b058325025c50ebb48eb2d54a5d39301d0b1c6ef58fead3801b4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:46:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 15:46:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 15:46:56 GMT
ENV TELEGRAF_VERSION=1.29.2
# Thu, 11 Jan 2024 15:47:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 11 Jan 2024 15:47:01 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 11 Jan 2024 15:47:01 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 11 Jan 2024 15:47:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 15:47:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f419b1a62fc83850ab3cb43274970bb20a18ae6e674535478a48f5bee11559b6`  
		Last Modified: Thu, 11 Jan 2024 09:34:07 GMT  
		Size: 23.6 MB (23582592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc6d96557ca39bf32423374ddf825dadcd91ffc484e19230e6f7bb5ef8ce4cd`  
		Last Modified: Thu, 11 Jan 2024 15:47:19 GMT  
		Size: 19.1 MB (19075022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fc85ea3b1e88d74db019f4f2cd5a63af935b115e231f8bfc1485e9bc814a95`  
		Last Modified: Thu, 11 Jan 2024 15:47:17 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d60192dde374560408f7efbf20e383d4bcfc7385300b53ee6071d30a085cc6b`  
		Last Modified: Thu, 11 Jan 2024 15:47:55 GMT  
		Size: 55.1 MB (55060939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf94769e2bf93462f405f5ef3190c178463f0b24b329f0b69601dce2baeea856`  
		Last Modified: Thu, 11 Jan 2024 15:47:49 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
