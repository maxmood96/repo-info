## `telegraf:latest`

```console
$ docker pull telegraf@sha256:64d741a8de5ea0c7a8c14fbe333a0ad0caee0f1e6558ae2b7ddfe562b566e043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:c51ddc799f5cc2aa2e277077213c1308cc10f8453847ef6b2e9f55468aa69ffa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147932304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc86af7fa20ff0b2bfdd505cd3524ff2ec49f336e97e0b1a06054cd5b1d81c2c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:29 GMT
ADD file:cc1376ecb3d9e93e4160573c110da753ffeb2efe2223351f1fbf483d89f1a756 in / 
# Thu, 27 Jul 2023 23:24:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:00:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 03:25:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 03:25:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 01 Aug 2023 03:25:20 GMT
ENV TELEGRAF_VERSION=1.27.3
# Tue, 01 Aug 2023 03:25:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 01 Aug 2023 03:25:24 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 01 Aug 2023 03:25:24 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Tue, 01 Aug 2023 03:25:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Aug 2023 03:25:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:785ef8b9b236a5f027f33cae77513051704c0538bff455ff5548105c954c3b1c`  
		Last Modified: Thu, 27 Jul 2023 23:29:02 GMT  
		Size: 49.6 MB (49557354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6dad8f55ae6c733e986316bd08205c8b2c41640bf8d08ff6e9bbcb6884304f`  
		Last Modified: Fri, 28 Jul 2023 03:07:18 GMT  
		Size: 24.0 MB (24030539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17262727d08ee9eb6ad9c8f2b4820dbc1540bf19e2af0459f4e911912573dddf`  
		Last Modified: Tue, 01 Aug 2023 03:26:00 GMT  
		Size: 19.1 MB (19143504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6389cbe011833bd5e7734655ba1af8ce0d49b52cf7cffacdab75948c7531c4`  
		Last Modified: Tue, 01 Aug 2023 03:25:57 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165f6d642f9c36a2dd66e2de8327a38c5d9a06aab8d113a81ae20b90d82852a1`  
		Last Modified: Tue, 01 Aug 2023 03:26:05 GMT  
		Size: 55.2 MB (55198753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e550770b61c6a9450b22d04a5aa3287735810f680a6f78e933b7851589c59bb`  
		Last Modified: Tue, 01 Aug 2023 03:25:57 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:11161e8d3ba4ec2ec3e84c9b4f467817b4de2aa736e811d5de71954c8284cfaf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136542782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f4e91ebe11cc5a5d61fc52e54fe58933a5a966c8b71903d77c5a0ed527834d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 16 Aug 2023 00:16:59 GMT
ADD file:03964ab92340a6f07fac7e332ca5f5401b3a35aa1e4a5c0b2484a71ff345bc29 in / 
# Wed, 16 Aug 2023 00:16:59 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 05:28:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 21:46:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 21:46:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 16 Aug 2023 21:46:09 GMT
ENV TELEGRAF_VERSION=1.27.3
# Wed, 16 Aug 2023 21:46:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 16 Aug 2023 21:46:16 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 16 Aug 2023 21:46:16 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 16 Aug 2023 21:46:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Aug 2023 21:46:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:22c91d9cbb3cbc0e4a05c1bfc86da0b5a439ded4f68eb2fbc055ba6b85ca1d90`  
		Last Modified: Wed, 16 Aug 2023 00:21:04 GMT  
		Size: 45.2 MB (45232937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24238a7fc18d7c6089f4f19e3e3d866f42674716043768c48cf6cabb7c8855b0`  
		Last Modified: Wed, 16 Aug 2023 05:47:31 GMT  
		Size: 21.9 MB (21936925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4136b5069a32b3e75c4401bafaaebbd14020c9c796608200fbb58b7f8e501fad`  
		Last Modified: Wed, 16 Aug 2023 21:47:05 GMT  
		Size: 18.0 MB (17989197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3b4492a7ea907433ba641a18fbfee37063deaa9b261a9256cfad10885e0ff2`  
		Last Modified: Wed, 16 Aug 2023 21:47:01 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb731d500e6ac848e2a1c77ccff128ea3d600ac93c0873ab57c5cb74207adf6c`  
		Last Modified: Wed, 16 Aug 2023 21:47:10 GMT  
		Size: 51.4 MB (51381575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacffefe40b87b80d9919717a65643aa681470667079aaf67e95c5db58cebf33`  
		Last Modified: Wed, 16 Aug 2023 21:47:01 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:bb8fe3ebf848636359b3788172b7a3b1370bf8ac7812c416ae9601a31599c391
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142083353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0c63bd03757347602fffd84065b9bb5b18902d631a1dd672a147cfeab0cb69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:49 GMT
ADD file:ca43018e3d97d44b49e60fe002bb20834a74cc1163d7e95ad50d549f072de158 in / 
# Tue, 15 Aug 2023 23:39:49 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 23:00:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 23:00:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 16 Aug 2023 23:00:01 GMT
ENV TELEGRAF_VERSION=1.27.3
# Wed, 16 Aug 2023 23:00:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 16 Aug 2023 23:00:06 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 16 Aug 2023 23:00:06 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 16 Aug 2023 23:00:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Aug 2023 23:00:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a014e5e7d08c37cf1703b97e701ccdc850e4a18d0ee679f03aa875dcd520aa85`  
		Last Modified: Tue, 15 Aug 2023 23:42:59 GMT  
		Size: 49.6 MB (49591310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715cea74ecbb15cb82efef1e77dd60c31d90b01d1286d6f39b4562afaebe75f3`  
		Last Modified: Wed, 16 Aug 2023 01:38:30 GMT  
		Size: 23.6 MB (23570046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58121fe4abd88f975020d3205911dfdcbf27a7bd72628f083186bfc6fbb9cf2`  
		Last Modified: Wed, 16 Aug 2023 23:00:51 GMT  
		Size: 19.1 MB (19077113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6997a7c465673ef3826712aff5a6ad2532f97774caea70aed6ea6f23e22575fb`  
		Last Modified: Wed, 16 Aug 2023 23:00:48 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b854c4748f18f843da8a7f9a7d932a5ed445cf1c2b97bf8159228aa35cf5816`  
		Last Modified: Wed, 16 Aug 2023 23:00:54 GMT  
		Size: 49.8 MB (49842741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc00fa1181a674ddb859e618bf3414abf6a32bf60ab4e854e0f206dd3c40bf9`  
		Last Modified: Wed, 16 Aug 2023 23:00:48 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
