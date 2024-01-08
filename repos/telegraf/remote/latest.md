## `telegraf:latest`

```console
$ docker pull telegraf@sha256:1f3e0122ec5ee9aaf54a2fffa006b2ec36baa23ea2de306524469fafe0c0b79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:11f314c297db353e2b6d97f8192661ccd99c5abfa1d3c6b8909deeaf60a818ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153428070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6577f3f1ef1abad7ca4a8b6d6a8a23150a581d6ae61229c3138194edb0710702`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:15 GMT
ADD file:7d8adf68670e8dc2af6b8603870ea610fc65ecbb08799f2ca6a3134f5d47d289 in / 
# Tue, 19 Dec 2023 01:20:16 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:32:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 21:34:42 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 21:34:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 08 Jan 2024 22:20:21 GMT
ENV TELEGRAF_VERSION=1.29.2
# Mon, 08 Jan 2024 22:20:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 08 Jan 2024 22:20:27 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 08 Jan 2024 22:20:27 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Mon, 08 Jan 2024 22:20:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jan 2024 22:20:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bc0734b949dcdcabe5bfdf0c8b9f44491e0fce04cb10c9c6e76282b9f6abdf01`  
		Last Modified: Tue, 19 Dec 2023 01:24:35 GMT  
		Size: 49.6 MB (49561579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5de22c0f5cd2ea2bb6c0524478db95bff5a294c99419ccd4a9d3ccc9873bad9`  
		Last Modified: Tue, 19 Dec 2023 04:41:08 GMT  
		Size: 24.0 MB (24046123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbaf5cb3dfa1ae286cd0c0705da0a90d7bc2d008273e345163fc1f48b4a16c6b`  
		Last Modified: Tue, 19 Dec 2023 21:35:31 GMT  
		Size: 19.2 MB (19151193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3227bbd870b97c29728fa20623f1ec917c3b0ed9037db5a8118319744f7c72`  
		Last Modified: Tue, 19 Dec 2023 21:35:28 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b9f2ec268f26c2d92cd50b2fa81909ca2e745f7a4c97a28d4345316f025bf15`  
		Last Modified: Mon, 08 Jan 2024 22:21:05 GMT  
		Size: 60.7 MB (60667018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:551e8d2b2ef192cfba0137ec71d0efe9795b6585db55110b4bbcaadf30f919bc`  
		Last Modified: Mon, 08 Jan 2024 22:20:55 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:dacfb50414307bf205c9609e5f0188adfb10a63de36fe257e6c3be863236dc46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141667425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:967f37ee06bdfa7a66205833fe3667ca274da13a5675503b86c64518ccede064`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 19 Dec 2023 02:07:39 GMT
ADD file:1633615de1824a95e35747f0133e90ab5ddc138574a83fb9c4f337cf45762574 in / 
# Tue, 19 Dec 2023 02:07:39 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:54:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 16:57:02 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 16:57:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 08 Jan 2024 22:10:53 GMT
ENV TELEGRAF_VERSION=1.29.2
# Mon, 08 Jan 2024 22:11:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 08 Jan 2024 22:11:06 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 08 Jan 2024 22:11:06 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Mon, 08 Jan 2024 22:11:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jan 2024 22:11:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:89cc9e7932dc0f797e6c3fc84b4c6868fedaca1b174b38a51e152a23a643be7a`  
		Last Modified: Tue, 19 Dec 2023 02:11:28 GMT  
		Size: 45.2 MB (45156699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1cce8fac77d35b90037c77fcb46603ed4cdc1388009887c5132cbdf3531132`  
		Last Modified: Tue, 19 Dec 2023 08:06:19 GMT  
		Size: 21.9 MB (21949134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c670d64c592d7ac7b9d213141415567dd40e2c0bb79d392857566e0093248844`  
		Last Modified: Tue, 19 Dec 2023 16:57:51 GMT  
		Size: 17.9 MB (17929935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b4b5c3ab72a46c46f32a4312b8ff1c1a9ebd9add0e439694d4258c850152cd`  
		Last Modified: Tue, 19 Dec 2023 16:57:47 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b4f9b7cf6dfa1b413d6f4e8792c293d0e84338490e5a4af7e67ef4bd558e5c`  
		Last Modified: Mon, 08 Jan 2024 22:11:32 GMT  
		Size: 56.6 MB (56629511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc08e168516e8b0561645104e38530d79e09ed178038498a563e836a1f23b95`  
		Last Modified: Mon, 08 Jan 2024 22:11:21 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:cf55c3a5e4616fc5edbed948f2c4b85f78aa75b1212e004767d48e088ebf9304
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147312865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e5c10027627afa76adf9a9230c19f6c0ae2ab66e24f8e0145ac491d43c27b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:02 GMT
ADD file:412f80f75ed3e520f767e70b6b27fc81807f62fc5c6e5adf756507e33af9fa6b in / 
# Tue, 19 Dec 2023 01:41:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 19:18:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 19:18:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 08 Jan 2024 22:13:10 GMT
ENV TELEGRAF_VERSION=1.29.2
# Mon, 08 Jan 2024 22:13:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 08 Jan 2024 22:13:17 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 08 Jan 2024 22:13:17 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Mon, 08 Jan 2024 22:13:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jan 2024 22:13:17 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b66b4ecd3ecfb67b3b7a2a44b0199cbdfc94965c8bd3fefab75cd2e612799740`  
		Last Modified: Tue, 19 Dec 2023 01:44:14 GMT  
		Size: 49.6 MB (49592259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c641d36985b2db859fc64c43a6dbf7c25cdf73e5d16d107fab1d95a840bb4e1`  
		Last Modified: Tue, 19 Dec 2023 11:42:17 GMT  
		Size: 23.6 MB (23582271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b31b6acda26269588812123f55f30787af039fc3803ac5f4a5fb9bc8e5292d1`  
		Last Modified: Tue, 19 Dec 2023 19:19:15 GMT  
		Size: 19.1 MB (19075170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a389000b0ac1cc7647d736c638c3db0dafad765cb5e95f2afb13a62cd32dd`  
		Last Modified: Tue, 19 Dec 2023 19:19:13 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af608d3f6b67a288f51795208fc5310297ded2b8133806f2485b4a1b3a70b968`  
		Last Modified: Mon, 08 Jan 2024 22:13:56 GMT  
		Size: 55.1 MB (55061003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3c2d4929536fccea59c968dee70c4301f70ce9cba1cfbaef55a706e66ece2a`  
		Last Modified: Mon, 08 Jan 2024 22:13:48 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
