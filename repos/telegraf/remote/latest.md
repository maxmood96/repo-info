## `telegraf:latest`

```console
$ docker pull telegraf@sha256:c041b149b338b1edeac1d9cfdaed9531842621e20d3863e04034fb8bfa897f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:2d544a60af363eb9710022f41d4109e836a9c82951225073dd6d07d9f243a8a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133856512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548e4f33b1dc8068c849c0c96e5918539c9ba1647f647c89c0ca3fca68cece74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:54:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:55:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 23:03:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 23:03:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 23:03:19 GMT
ENV TELEGRAF_VERSION=1.24.2
# Wed, 05 Oct 2022 23:03:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Oct 2022 23:03:23 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Oct 2022 23:03:23 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 05 Oct 2022 23:03:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 23:03:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47db815c6a4547dc224b75222193cb1851cf529d2cbdf26f854b9bbf97099b98`  
		Last Modified: Wed, 05 Oct 2022 01:19:13 GMT  
		Size: 5.2 MB (5163279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf48494000001a037b72870d2a6a2536f9da8bc5d1ceddd72d79f4a51fe7a60e`  
		Last Modified: Wed, 05 Oct 2022 01:19:13 GMT  
		Size: 10.9 MB (10876505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863a7459c8fe546ab3b805bc6fb6f6e8b01bcf7411513f42699201aacfc4bb9c`  
		Last Modified: Wed, 05 Oct 2022 23:03:48 GMT  
		Size: 18.8 MB (18760121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e28af260775d457e7415a6995724f47b2d5a7b97a31a0c7d14f0c8a2ff1c257`  
		Last Modified: Wed, 05 Oct 2022 23:03:45 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f15f27d873fce4dbd5165fb753fc5b702a3ffcff509b667742a60950fcc8261`  
		Last Modified: Wed, 05 Oct 2022 23:04:31 GMT  
		Size: 44.0 MB (44007118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b89a3dd513bbc50e6ff4df223ff078d1bacaad986a61fb7b6d91a14f74ad95a`  
		Last Modified: Wed, 05 Oct 2022 23:04:24 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7da547f0b06db7b505c678289103bf96bef2dcbb9606fee01663470b490d0c2e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123881365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c29fad03d96db8d2b5cd496a1dc6ff839d055f6dd82fc3cd603a3f6d5e46f96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:28 GMT
ADD file:47a3f2948af18c39686ca59a88a439c25edaf286064d3a2ccc5dab47fee2fc52 in / 
# Tue, 04 Oct 2022 23:58:29 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:32:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:32:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 06 Oct 2022 16:07:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 16:07:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 06 Oct 2022 16:07:35 GMT
ENV TELEGRAF_VERSION=1.24.2
# Thu, 06 Oct 2022 16:07:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 06 Oct 2022 16:07:41 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 06 Oct 2022 16:07:41 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 06 Oct 2022 16:07:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 16:07:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e19342fb46cabf6147aec1d1c6af1f3a82736530cf3b067835fc8a09da092ce3`  
		Last Modified: Wed, 05 Oct 2022 00:04:36 GMT  
		Size: 50.2 MB (50209087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49f93f990f17337480b5bdf526a6bb48d1ae63bd17f54be17cd2f6ebba4de7d`  
		Last Modified: Wed, 05 Oct 2022 00:53:28 GMT  
		Size: 4.9 MB (4931366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3989be0d7ed2f72fae0310039043f6ba76c24a45f9ec9689697ebd932845cc8`  
		Last Modified: Wed, 05 Oct 2022 00:53:28 GMT  
		Size: 10.2 MB (10217872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef23f3c089cb85cd0436535aeb8422fbfd379b3a897532a89f1c2fea29728e03`  
		Last Modified: Thu, 06 Oct 2022 16:08:13 GMT  
		Size: 17.5 MB (17462363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a05f53155f290b1fb830a5da47f116e34fb30b79dcd539c2e8d735f10fd13ac`  
		Last Modified: Thu, 06 Oct 2022 16:08:09 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0c43f9c460c0df3bccd6147aec132029dfcb6c97462b59494d46b61d2fa73b`  
		Last Modified: Thu, 06 Oct 2022 16:08:55 GMT  
		Size: 41.1 MB (41057433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c573a3fdf94f1a4476208d9bdcf1c919fbae54e198fa626b45e7afa62cf99a8`  
		Last Modified: Thu, 06 Oct 2022 16:08:48 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ec9785ee6a1f0f6c15aff3757860c2ceadab3d1e16105f1ed6eae6ef8126ad46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127582555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aab2522ba7f26a4e559c798050d9111fd3a140acd7d2c89a49e93f9e001d6cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:23:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:23:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 17:52:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:52:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 17:52:52 GMT
ENV TELEGRAF_VERSION=1.24.2
# Wed, 05 Oct 2022 17:52:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Oct 2022 17:52:57 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Oct 2022 17:52:59 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 05 Oct 2022 17:52:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 17:53:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37c953a37e989b49a533e8d08c80d87ce66fadee48160f9a4d8cd2dd5b0ec87`  
		Last Modified: Wed, 05 Oct 2022 00:37:21 GMT  
		Size: 4.9 MB (4944361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98802a15fc60bda24c79203236f930586f1dba6218aa2b4c121cf0dbf5627b38`  
		Last Modified: Wed, 05 Oct 2022 00:37:22 GMT  
		Size: 10.7 MB (10657400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22398aa42c1b74e8b8aa86450b2606b08a367992108afd66f03799f1393932ef`  
		Last Modified: Wed, 05 Oct 2022 17:53:26 GMT  
		Size: 18.4 MB (18382830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50578a1c2d11fdb0e84248fb7effbf5bc328dc0f95e2f855be12c15e333f02af`  
		Last Modified: Wed, 05 Oct 2022 17:53:23 GMT  
		Size: 2.9 KB (2860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9174328e2187fa4664cf5c87ea2fd53c187664bc4b6f8cc249146ebb422c1b7`  
		Last Modified: Wed, 05 Oct 2022 17:54:04 GMT  
		Size: 39.9 MB (39894136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0757b0a107178edfae558b254d8f2be8c846b0971b0ba21a1c042a31e5384ee7`  
		Last Modified: Wed, 05 Oct 2022 17:53:58 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
