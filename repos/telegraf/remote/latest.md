## `telegraf:latest`

```console
$ docker pull telegraf@sha256:77cb9fcdaab2804f2d4625c9c7ee5ebe04399daf761990c7a35a66ab60ce5ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:bd842af6baa31b90cf8890a22a4f191e59658fdbe3ca55283e39e800bdb47e63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149867936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ff75561f721a1f0489a4b4919748228e699f5d478a894cf1e4b21b41c8d9aa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:37 GMT
ADD file:3e9b6405f11dd24ce62105c033f1d8b931d9409298553f63b03af1b6dd1dda35 in / 
# Wed, 01 Nov 2023 00:20:38 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:52:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 18:14:22 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 18:14:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 16 Nov 2023 02:43:43 GMT
ENV TELEGRAF_VERSION=1.28.5
# Thu, 16 Nov 2023 02:43:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 16 Nov 2023 02:43:48 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 16 Nov 2023 02:43:48 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 16 Nov 2023 02:43:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Nov 2023 02:43:48 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8457fd5474e70835e4482983a5662355d892d5f6f0f90a27a8e9f009997e8196`  
		Last Modified: Wed, 01 Nov 2023 00:25:05 GMT  
		Size: 49.6 MB (49582024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13baa2029dde87a21b87127168a0fb50a007c07da6b5adc8864e1fe1376c86ff`  
		Last Modified: Wed, 01 Nov 2023 01:02:01 GMT  
		Size: 24.0 MB (24049147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb5cbba93e421136061ff7a287eca07e2c44834e732791ce0db133784207ea7`  
		Last Modified: Wed, 01 Nov 2023 18:15:20 GMT  
		Size: 19.1 MB (19145622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2a9cce78837515beeedadd4ef39d88e074358603c1c6360199c5bbb54a9356`  
		Last Modified: Wed, 01 Nov 2023 18:15:17 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5df87cbe58e2f321baefcefa53328afc16f2a3624f32639d6a5d2e92e6edfb`  
		Last Modified: Thu, 16 Nov 2023 02:44:25 GMT  
		Size: 57.1 MB (57088996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a9e7f2d627f724d801ee6f4db15a7bf79b50751908fd91baf419be07ce569d`  
		Last Modified: Thu, 16 Nov 2023 02:44:16 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:0aa63390591606635689d97a35c6f20f8209c7d9bfb61f0041fc4dc508a45719
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137660588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17dfc697d38f21247fc0140502c56cfd31b791e58adb3755bcbb2706c00235ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:42 GMT
ADD file:3b2b4eda35d794b39d6b5567e81651625af51da3deb3f63b3ffdffa07720646e in / 
# Wed, 01 Nov 2023 00:57:42 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:30:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 16:53:02 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 16:53:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 14 Nov 2023 02:19:51 GMT
ENV TELEGRAF_VERSION=1.28.4
# Tue, 14 Nov 2023 02:20:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 14 Nov 2023 02:20:01 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 14 Nov 2023 02:20:01 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Tue, 14 Nov 2023 02:20:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 02:20:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9bf855396a6f46c1cbac4e188af10f2c38474f989707b0b1b406b48c4b7284ef`  
		Last Modified: Wed, 01 Nov 2023 01:01:41 GMT  
		Size: 45.2 MB (45179410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6e59eca644b227cb755978679a3031e7b3f9a5c707057c293f2ba8732d8ef2`  
		Last Modified: Wed, 01 Nov 2023 02:41:40 GMT  
		Size: 22.0 MB (21951880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce8fce53d3efe8a2a390487834b7740bd7e15c9881525b32ef88c1042a1f6dd`  
		Last Modified: Wed, 01 Nov 2023 16:54:00 GMT  
		Size: 18.0 MB (17991623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c85606ced42864565ce1f0bdc077764bb9239e718d2786f778966cd9f1ff659`  
		Last Modified: Wed, 01 Nov 2023 16:53:56 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037fb71aab0611522ab940b632a52f81b5d8ab2f6c82436ce9cd3505d936a84a`  
		Last Modified: Tue, 14 Nov 2023 02:20:24 GMT  
		Size: 52.5 MB (52535528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cabbb138608cabfcb3a7280e5e7beeca35abc909ba6458634d7fb9354e06a6`  
		Last Modified: Tue, 14 Nov 2023 02:20:15 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3ce0c05f1d48927e505a728656240203562c788695de4208ec2bafd821223292
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144029023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00ea23f8e53b1a4eca352a524eac13c13a2909941763c24b9c5a9f4fba7a67d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:32 GMT
ADD file:c934ceb4c53a1cce6779198f1ea73d5c8aad9a035e750b343d49826120ecd0eb in / 
# Wed, 01 Nov 2023 00:39:33 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:04:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:12:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:12:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 16 Nov 2023 06:27:51 GMT
ENV TELEGRAF_VERSION=1.28.5
# Thu, 16 Nov 2023 06:27:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 16 Nov 2023 06:27:58 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 16 Nov 2023 06:27:58 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 16 Nov 2023 06:27:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Nov 2023 06:27:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8024d4fb53b2455f66d49b7ee72eb3cad5074043578238b796a9879955946a88`  
		Last Modified: Wed, 01 Nov 2023 00:42:44 GMT  
		Size: 49.6 MB (49612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d826ee8aa65e56e167f0e27fa65cfc065687a7ac6c360787d5940d8b51f0cf1`  
		Last Modified: Wed, 01 Nov 2023 02:13:39 GMT  
		Size: 23.6 MB (23584896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2794f9c6546f6aa0a9a29e1eab9226f3bc5b9ba469b98cd8850edb9209ee4be2`  
		Last Modified: Wed, 01 Nov 2023 14:13:11 GMT  
		Size: 19.1 MB (19078763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916aaf6834f48574720db24d78a45050d28210cadfdba1f7e5b8952d05bae145`  
		Last Modified: Wed, 01 Nov 2023 14:13:09 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07024b08becf8847f660ae75d143d2fe35d91c39badd9d9b86f7265dcfd95448`  
		Last Modified: Thu, 16 Nov 2023 06:28:31 GMT  
		Size: 51.8 MB (51750552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96d863c4ecdbb740edfbdb9fd4febbab0aeffb60a313f568caa30aca4ab7302`  
		Last Modified: Thu, 16 Nov 2023 06:28:25 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
