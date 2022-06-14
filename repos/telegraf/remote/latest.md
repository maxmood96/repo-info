## `telegraf:latest`

```console
$ docker pull telegraf@sha256:98bbc52e40092dc35e86daa635f4b402128fa0409f216fc74435b3a2a7c4be9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:cc0bbf7c36f4451ea5e3669777ef4a1f3e5af540ab1ebec4b4c283be2c8a4d87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130433911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a0f86dd96e38670e17db6c08d89344f528ff3a1b35c7459a196b8a2f52b400`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 28 May 2022 01:20:12 GMT
ADD file:dd3d4b31d7f1d4062ad0eb2d85dba064cea067b1eb4a8b89a0b593ea90001cdf in / 
# Sat, 28 May 2022 01:20:12 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:40:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:40:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 May 2022 01:20:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Sun, 29 May 2022 01:20:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 13 Jun 2022 22:14:45 GMT
ENV TELEGRAF_VERSION=1.23.0
# Mon, 13 Jun 2022 22:14:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 13 Jun 2022 22:14:51 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 13 Jun 2022 22:14:51 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Mon, 13 Jun 2022 22:14:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Jun 2022 22:14:51 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e756f3fdd6a378aa16205b0f75d178b7532b110e86be7659004fc6a21183226c`  
		Last Modified: Sat, 28 May 2022 01:24:51 GMT  
		Size: 55.0 MB (55009253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf168a6748997eb97b48cc86234b7ff7d8bc907645b9be99013158b3f146b272`  
		Last Modified: Sat, 28 May 2022 02:49:08 GMT  
		Size: 5.2 MB (5156036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e604223835ccf02d097187b5a58ca73e8598cadbb16a36202ca1943e97f56f1f`  
		Last Modified: Sat, 28 May 2022 02:49:08 GMT  
		Size: 10.9 MB (10875008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5402678d70402b800956345b27ae92b4c3c278d30adaec57e35773bd283289`  
		Last Modified: Sun, 29 May 2022 01:21:02 GMT  
		Size: 18.8 MB (18760140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef8afd41bbd350473f4945ad525683699b8d4a0863ae5739473f6541c19db4f`  
		Last Modified: Sun, 29 May 2022 01:20:59 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae7a8f7b782ade36dd96d466617efa7db9b5fad18508cc7e2e9d8be74b6964c`  
		Last Modified: Mon, 13 Jun 2022 22:15:28 GMT  
		Size: 40.6 MB (40630232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036c886461614e933f99414ef9c8fb0389342e5740de8ec089b88b6972cc3fab`  
		Last Modified: Mon, 13 Jun 2022 22:15:22 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:2c9af8c312e61be3372b1d3dbe74150f973f6da8bcbbdccdff58bcaf9e1cd8c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120861561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a476e408a9b6464ed662869fed7e1df60b45bd8a2644eadf243aabe6b633225d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 28 May 2022 00:59:10 GMT
ADD file:faa82773e36b14c218e792730b0264c016864613a8d43cfaa33864075b0ef169 in / 
# Sat, 28 May 2022 00:59:11 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:42:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:42:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 May 2022 22:31:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Sun, 29 May 2022 22:31:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 13 Jun 2022 23:04:41 GMT
ENV TELEGRAF_VERSION=1.23.0
# Mon, 13 Jun 2022 23:04:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 13 Jun 2022 23:04:53 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 13 Jun 2022 23:04:54 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Mon, 13 Jun 2022 23:04:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Jun 2022 23:04:55 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8c8b1770c0de8d780b721bb37e9a8b6e5071a83530a584b1aed8ddc9aa12dd00`  
		Last Modified: Sat, 28 May 2022 01:14:50 GMT  
		Size: 50.2 MB (50199379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7380c9813fdc7aac45d249b456f89965b8eee97a56d8cc8d01bf2c09bd344e`  
		Last Modified: Sat, 28 May 2022 03:08:58 GMT  
		Size: 4.9 MB (4924792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed7ad25f71b787f363a804d83f044bdccc37536ae3e8856aecb500db41357a0`  
		Last Modified: Sat, 28 May 2022 03:08:59 GMT  
		Size: 10.2 MB (10217910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8721a75b16929fea3f06dcf4b0cc04cd8ea9fc1a81bfeefc91ddcb23cae0c6de`  
		Last Modified: Sun, 29 May 2022 22:33:25 GMT  
		Size: 17.5 MB (17462491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f06223ee9d1c344b9394a168ec62e31b26924d7380ea1240380495d65380237`  
		Last Modified: Sun, 29 May 2022 22:33:12 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5226a1165fdccc8e2a1b0c13f168e886ab067d835c786b5a78553e098da3e0`  
		Last Modified: Mon, 13 Jun 2022 23:06:10 GMT  
		Size: 38.1 MB (38053751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f87ca34d3fee066c74942e826a2df2be5f8d936c5d30f594ee55f391a67837`  
		Last Modified: Mon, 13 Jun 2022 23:05:44 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5f3c558e723efc691b029093fda4a9d9c93ca732086b59a789f5c77daff70a38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124641786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04cc53d2d5f5c5436f340862d32bd9f93d4d86ebb32420f5aaa9b31ffd7a1864`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 28 May 2022 00:40:23 GMT
ADD file:a78273677555ebe8bac187f491203093eec62fa1c4f65f00ba2cf0cc2230992f in / 
# Sat, 28 May 2022 00:40:24 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 11:05:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 May 2022 01:36:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Sun, 29 May 2022 01:36:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 13 Jun 2022 23:33:32 GMT
ENV TELEGRAF_VERSION=1.23.0
# Mon, 13 Jun 2022 23:33:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 13 Jun 2022 23:33:37 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 13 Jun 2022 23:33:38 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Mon, 13 Jun 2022 23:33:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Jun 2022 23:33:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d794814721d57f8aaec06ab3652e90212cc3beccf5ff5c87f6ecf8375784bcc8`  
		Last Modified: Sat, 28 May 2022 00:47:04 GMT  
		Size: 53.7 MB (53696947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf62ee63325dbbad699d6845f68c2391db3bf158f60373849c2d1cb6bb479788`  
		Last Modified: Sat, 28 May 2022 11:17:05 GMT  
		Size: 4.9 MB (4938744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e37b4c58dd1db7ead6f3c2cdf757f490b4e29c958d2a70559c313e9a03a5ef`  
		Last Modified: Sat, 28 May 2022 11:17:06 GMT  
		Size: 10.7 MB (10657073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2835e11a747e0b80fc4af45f154b30f61be8fed23dc39b6ad5fa3b6e6703518`  
		Last Modified: Sun, 29 May 2022 01:37:35 GMT  
		Size: 18.4 MB (18382788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea17ce5ec891b229898ee80d0c706660093b31d42d92b3e6d9922eda755a463`  
		Last Modified: Sun, 29 May 2022 01:37:31 GMT  
		Size: 2.9 KB (2868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be352536d14a0ee0f721ef767bc115df4b986e74f6a8c8950c859c8b7b3b68c0`  
		Last Modified: Mon, 13 Jun 2022 23:34:09 GMT  
		Size: 37.0 MB (36963021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462cea9ca7e4bafeb5ca67e59805836f3e4d1368290a1eac33943ef8a664f0fd`  
		Last Modified: Mon, 13 Jun 2022 23:34:04 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
