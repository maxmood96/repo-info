<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.14`](#telegraf114)
-	[`telegraf:1.14.5`](#telegraf1145)
-	[`telegraf:1.14.5-alpine`](#telegraf1145-alpine)
-	[`telegraf:1.14-alpine`](#telegraf114-alpine)
-	[`telegraf:1.15`](#telegraf115)
-	[`telegraf:1.15.4`](#telegraf1154)
-	[`telegraf:1.15.4-alpine`](#telegraf1154-alpine)
-	[`telegraf:1.15-alpine`](#telegraf115-alpine)
-	[`telegraf:1.16`](#telegraf116)
-	[`telegraf:1.16.3`](#telegraf1163)
-	[`telegraf:1.16.3-alpine`](#telegraf1163-alpine)
-	[`telegraf:1.16-alpine`](#telegraf116-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.14`

```console
$ docker pull telegraf@sha256:363b4a37abac9ce1557669bc81ce91725703572335a7cfb4065e21e958cfe3dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.14` - linux; amd64

```console
$ docker pull telegraf@sha256:cfbd1c4c626629fb2b1c0f4ecf3ac7029e59dba66a27c91c3b1b4c1f6554a52a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97854813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f42d640f74c4366256809a97bb5e41c97ac7e6ff9565c08114e22af3af93f7dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:10 GMT
ADD file:373a8875589f170b51fa677a3bf736feeb46ea278c553950a3eb3169a2056c12 in / 
# Tue, 17 Nov 2020 20:24:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:43:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:43:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 03:13:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:13:43 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 19 Nov 2020 03:13:44 GMT
ENV TELEGRAF_VERSION=1.14.5
# Thu, 19 Nov 2020 03:13:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 19 Nov 2020 03:13:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 19 Nov 2020 03:13:47 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 19 Nov 2020 03:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 03:13:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7919f5b7d60254cafc73c0d097b8ccffb72e0b6472957ece4dd5b378c5ca7cc1`  
		Last Modified: Tue, 17 Nov 2020 20:30:26 GMT  
		Size: 45.4 MB (45377037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e107167dcc5392ce7b34cb6af6bcfe1cf99f76f9e632d6c321526666558ab50`  
		Last Modified: Wed, 18 Nov 2020 00:54:39 GMT  
		Size: 10.8 MB (10752152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a456bba435b99e4c17dd5da957e63bef2c43ae5291b055ce82bd26d9153259`  
		Last Modified: Wed, 18 Nov 2020 00:54:37 GMT  
		Size: 4.3 MB (4340590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9103b78915378c325516cb0ad63e73184031ba4cadb498ff4f5e87dbe6b6a4f`  
		Last Modified: Thu, 19 Nov 2020 03:14:45 GMT  
		Size: 16.0 MB (15964674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e83c4647348e7a0a848581ac3edbe3719be570ef526e25788ee84698484f8b5`  
		Last Modified: Thu, 19 Nov 2020 03:14:41 GMT  
		Size: 2.8 KB (2775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f898dd887e22a58e16eccfa0374ca9ae37dfdacb240fb88735a6a60bcee8f5e2`  
		Last Modified: Thu, 19 Nov 2020 03:14:46 GMT  
		Size: 21.4 MB (21417401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7533bf9064dd592b0f339c3116e46e5f58775628cd0e1db6850fcb61a478e9`  
		Last Modified: Thu, 19 Nov 2020 03:14:41 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.14` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:5b4dfd7865adc53da3d67bcdcf56e8969b91b6df68014d0b687cedc5a847321c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90450946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175b0145db9c43660f059e9761fc43c22811e986f307df1cbc6c8420c5089081`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:26:47 GMT
ADD file:58b80132bbfb3cae1eb2a9345e362cce1e39de41055fdcef8e5a8a8a447f69b0 in / 
# Tue, 17 Nov 2020 20:26:50 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:57:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:57:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 19:38:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 19:38:23 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 18 Nov 2020 19:38:24 GMT
ENV TELEGRAF_VERSION=1.14.5
# Wed, 18 Nov 2020 19:38:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 18 Nov 2020 19:38:30 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 18 Nov 2020 19:38:31 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 18 Nov 2020 19:38:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 19:38:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cfc77fa15d772230821249f78cfbb69a8fc6596f6867601b9dad16aedb424325`  
		Last Modified: Tue, 17 Nov 2020 20:35:24 GMT  
		Size: 42.1 MB (42117734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1d24dbd0f85452f20a934ea14ebc3dadfdd8493317dfe8f7f2aa1772937953`  
		Last Modified: Tue, 17 Nov 2020 22:12:47 GMT  
		Size: 9.4 MB (9444101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90255e5a0a934b36df89ac1c1842d07d8d7ed4b3531898af64fdab8372662e3e`  
		Last Modified: Tue, 17 Nov 2020 22:12:46 GMT  
		Size: 3.9 MB (3919908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a1c69817fec36edf16d90f052013b725587c9d6eb80809c0e9ea0497c22675`  
		Last Modified: Wed, 18 Nov 2020 19:39:46 GMT  
		Size: 14.8 MB (14835898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e328aac09d7d6b0404e18b7f4aa5c05c23d1c6fb12bc557eb00def267392b3b`  
		Last Modified: Wed, 18 Nov 2020 19:39:40 GMT  
		Size: 2.8 KB (2801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b638034d8df9f44bb2827e1460c5af82323e4a3bcb9f0ac8044ffcbfe081930a`  
		Last Modified: Wed, 18 Nov 2020 19:39:47 GMT  
		Size: 20.1 MB (20130319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b8d3de7dee4e3382bc0c06124c06ccc75700422e976788be0c9b03521016a4`  
		Last Modified: Wed, 18 Nov 2020 19:39:40 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.14` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5f0b9419970af8edaea679d12e62b45bc5d9922b895032455e5638644bdb98f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92221122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0eecf3079e64d13c03efc4ef038c58a0ce116cd67c7fe178b7d607cd2eaebb1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:27:33 GMT
ADD file:d2e307c3e54ad69dff47f6bdacca7c8ee0957a09346bb21baec02b9de1a657e1 in / 
# Tue, 17 Nov 2020 20:27:37 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:28:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:28:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 21:21:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 21:21:54 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 18 Nov 2020 21:21:55 GMT
ENV TELEGRAF_VERSION=1.14.5
# Wed, 18 Nov 2020 21:22:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 18 Nov 2020 21:22:02 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 18 Nov 2020 21:22:03 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 18 Nov 2020 21:22:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 21:22:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f99bf631c0ebddf9e32516b47bf6e198efc42d06c3eb86d6f5f5739757b5839c`  
		Last Modified: Tue, 17 Nov 2020 20:34:17 GMT  
		Size: 43.2 MB (43176009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a9b3adbe4ac4ca73818d8b79e94d2ff2b6ceafc1225d7c036ec4d384f0804a`  
		Last Modified: Tue, 17 Nov 2020 22:40:38 GMT  
		Size: 9.7 MB (9702292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052ba804da6ef34fd9dddf0ca298b1e0551ac8cf3ea14fc371fa1fa51cbd7f7c`  
		Last Modified: Tue, 17 Nov 2020 22:40:36 GMT  
		Size: 4.1 MB (4095219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3dc0ade15aa05f463feb656ab64ad3e79b136185db227c81c2d8cda6bd3220`  
		Last Modified: Wed, 18 Nov 2020 21:23:20 GMT  
		Size: 15.5 MB (15522941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b0c19f82f08e1df3f56b76b8da55fedd41f8f608ee5c76df938a005849d695`  
		Last Modified: Wed, 18 Nov 2020 21:23:15 GMT  
		Size: 2.8 KB (2806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa777f07087f83cd8716ad940b8ef1806eff4bd8e528964bfe83cf37d8dccd5`  
		Last Modified: Wed, 18 Nov 2020 21:23:21 GMT  
		Size: 19.7 MB (19721673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f3eff71cad396bba47c2274345ee65914f86c4b2b4ac8ae1c54315ce9553f`  
		Last Modified: Wed, 18 Nov 2020 21:23:16 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.14.5`

```console
$ docker pull telegraf@sha256:363b4a37abac9ce1557669bc81ce91725703572335a7cfb4065e21e958cfe3dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.14.5` - linux; amd64

```console
$ docker pull telegraf@sha256:cfbd1c4c626629fb2b1c0f4ecf3ac7029e59dba66a27c91c3b1b4c1f6554a52a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97854813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f42d640f74c4366256809a97bb5e41c97ac7e6ff9565c08114e22af3af93f7dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:10 GMT
ADD file:373a8875589f170b51fa677a3bf736feeb46ea278c553950a3eb3169a2056c12 in / 
# Tue, 17 Nov 2020 20:24:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:43:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:43:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 03:13:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:13:43 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 19 Nov 2020 03:13:44 GMT
ENV TELEGRAF_VERSION=1.14.5
# Thu, 19 Nov 2020 03:13:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 19 Nov 2020 03:13:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 19 Nov 2020 03:13:47 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 19 Nov 2020 03:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 03:13:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7919f5b7d60254cafc73c0d097b8ccffb72e0b6472957ece4dd5b378c5ca7cc1`  
		Last Modified: Tue, 17 Nov 2020 20:30:26 GMT  
		Size: 45.4 MB (45377037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e107167dcc5392ce7b34cb6af6bcfe1cf99f76f9e632d6c321526666558ab50`  
		Last Modified: Wed, 18 Nov 2020 00:54:39 GMT  
		Size: 10.8 MB (10752152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a456bba435b99e4c17dd5da957e63bef2c43ae5291b055ce82bd26d9153259`  
		Last Modified: Wed, 18 Nov 2020 00:54:37 GMT  
		Size: 4.3 MB (4340590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9103b78915378c325516cb0ad63e73184031ba4cadb498ff4f5e87dbe6b6a4f`  
		Last Modified: Thu, 19 Nov 2020 03:14:45 GMT  
		Size: 16.0 MB (15964674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e83c4647348e7a0a848581ac3edbe3719be570ef526e25788ee84698484f8b5`  
		Last Modified: Thu, 19 Nov 2020 03:14:41 GMT  
		Size: 2.8 KB (2775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f898dd887e22a58e16eccfa0374ca9ae37dfdacb240fb88735a6a60bcee8f5e2`  
		Last Modified: Thu, 19 Nov 2020 03:14:46 GMT  
		Size: 21.4 MB (21417401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7533bf9064dd592b0f339c3116e46e5f58775628cd0e1db6850fcb61a478e9`  
		Last Modified: Thu, 19 Nov 2020 03:14:41 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.14.5` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:5b4dfd7865adc53da3d67bcdcf56e8969b91b6df68014d0b687cedc5a847321c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90450946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175b0145db9c43660f059e9761fc43c22811e986f307df1cbc6c8420c5089081`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:26:47 GMT
ADD file:58b80132bbfb3cae1eb2a9345e362cce1e39de41055fdcef8e5a8a8a447f69b0 in / 
# Tue, 17 Nov 2020 20:26:50 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:57:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:57:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 19:38:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 19:38:23 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 18 Nov 2020 19:38:24 GMT
ENV TELEGRAF_VERSION=1.14.5
# Wed, 18 Nov 2020 19:38:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 18 Nov 2020 19:38:30 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 18 Nov 2020 19:38:31 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 18 Nov 2020 19:38:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 19:38:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cfc77fa15d772230821249f78cfbb69a8fc6596f6867601b9dad16aedb424325`  
		Last Modified: Tue, 17 Nov 2020 20:35:24 GMT  
		Size: 42.1 MB (42117734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1d24dbd0f85452f20a934ea14ebc3dadfdd8493317dfe8f7f2aa1772937953`  
		Last Modified: Tue, 17 Nov 2020 22:12:47 GMT  
		Size: 9.4 MB (9444101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90255e5a0a934b36df89ac1c1842d07d8d7ed4b3531898af64fdab8372662e3e`  
		Last Modified: Tue, 17 Nov 2020 22:12:46 GMT  
		Size: 3.9 MB (3919908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a1c69817fec36edf16d90f052013b725587c9d6eb80809c0e9ea0497c22675`  
		Last Modified: Wed, 18 Nov 2020 19:39:46 GMT  
		Size: 14.8 MB (14835898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e328aac09d7d6b0404e18b7f4aa5c05c23d1c6fb12bc557eb00def267392b3b`  
		Last Modified: Wed, 18 Nov 2020 19:39:40 GMT  
		Size: 2.8 KB (2801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b638034d8df9f44bb2827e1460c5af82323e4a3bcb9f0ac8044ffcbfe081930a`  
		Last Modified: Wed, 18 Nov 2020 19:39:47 GMT  
		Size: 20.1 MB (20130319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b8d3de7dee4e3382bc0c06124c06ccc75700422e976788be0c9b03521016a4`  
		Last Modified: Wed, 18 Nov 2020 19:39:40 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.14.5` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5f0b9419970af8edaea679d12e62b45bc5d9922b895032455e5638644bdb98f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92221122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0eecf3079e64d13c03efc4ef038c58a0ce116cd67c7fe178b7d607cd2eaebb1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:27:33 GMT
ADD file:d2e307c3e54ad69dff47f6bdacca7c8ee0957a09346bb21baec02b9de1a657e1 in / 
# Tue, 17 Nov 2020 20:27:37 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:28:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:28:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 21:21:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 21:21:54 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 18 Nov 2020 21:21:55 GMT
ENV TELEGRAF_VERSION=1.14.5
# Wed, 18 Nov 2020 21:22:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 18 Nov 2020 21:22:02 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 18 Nov 2020 21:22:03 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 18 Nov 2020 21:22:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 21:22:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f99bf631c0ebddf9e32516b47bf6e198efc42d06c3eb86d6f5f5739757b5839c`  
		Last Modified: Tue, 17 Nov 2020 20:34:17 GMT  
		Size: 43.2 MB (43176009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a9b3adbe4ac4ca73818d8b79e94d2ff2b6ceafc1225d7c036ec4d384f0804a`  
		Last Modified: Tue, 17 Nov 2020 22:40:38 GMT  
		Size: 9.7 MB (9702292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052ba804da6ef34fd9dddf0ca298b1e0551ac8cf3ea14fc371fa1fa51cbd7f7c`  
		Last Modified: Tue, 17 Nov 2020 22:40:36 GMT  
		Size: 4.1 MB (4095219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3dc0ade15aa05f463feb656ab64ad3e79b136185db227c81c2d8cda6bd3220`  
		Last Modified: Wed, 18 Nov 2020 21:23:20 GMT  
		Size: 15.5 MB (15522941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b0c19f82f08e1df3f56b76b8da55fedd41f8f608ee5c76df938a005849d695`  
		Last Modified: Wed, 18 Nov 2020 21:23:15 GMT  
		Size: 2.8 KB (2806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa777f07087f83cd8716ad940b8ef1806eff4bd8e528964bfe83cf37d8dccd5`  
		Last Modified: Wed, 18 Nov 2020 21:23:21 GMT  
		Size: 19.7 MB (19721673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f3eff71cad396bba47c2274345ee65914f86c4b2b4ac8ae1c54315ce9553f`  
		Last Modified: Wed, 18 Nov 2020 21:23:16 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.14.5-alpine`

```console
$ docker pull telegraf@sha256:4fa201b3bf74d87188868e5bbb1022201b7ea591f60cd350375355cd0844361a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.14.5-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7d3ff248fe489e3d707209d545f49fae89e17fbcfd70b55b36b8877ba9edc0bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27450323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d91dd2738db3d8f0db3bcf1acec51579f6a5079b5a9ec4ef88e092bfed41a63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 13:50:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Fri, 11 Dec 2020 13:50:54 GMT
ENV TELEGRAF_VERSION=1.14.5
# Fri, 11 Dec 2020 13:51:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/telegraf.conf /etc/telegraf/ &&     chmod +x /usr/src/telegraf*/* &&     cp -a /usr/src/telegraf*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 13:51:00 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 11 Dec 2020 13:51:01 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Fri, 11 Dec 2020 13:51:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 13:51:02 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9624996f533f5dfa6054365968149298c1183a1202c16061de0fc5093ad633f`  
		Last Modified: Fri, 11 Dec 2020 02:53:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b41f8dcfdf530094e6b347e5cf020edc7a260ea9df8825794acfa748a91e65`  
		Last Modified: Fri, 11 Dec 2020 13:52:15 GMT  
		Size: 3.3 MB (3298137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4a03cfdd927f9446e6d273be41fd583d1bb30e073e17541e7fbcb2c597028a`  
		Last Modified: Fri, 11 Dec 2020 13:52:20 GMT  
		Size: 21.4 MB (21354904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f373630002a5237dd92fc516bd8442c9fc2313b2fd363a9a6b3c0534043604e`  
		Last Modified: Fri, 11 Dec 2020 13:52:12 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.14-alpine`

```console
$ docker pull telegraf@sha256:4fa201b3bf74d87188868e5bbb1022201b7ea591f60cd350375355cd0844361a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.14-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7d3ff248fe489e3d707209d545f49fae89e17fbcfd70b55b36b8877ba9edc0bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27450323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d91dd2738db3d8f0db3bcf1acec51579f6a5079b5a9ec4ef88e092bfed41a63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 13:50:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Fri, 11 Dec 2020 13:50:54 GMT
ENV TELEGRAF_VERSION=1.14.5
# Fri, 11 Dec 2020 13:51:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/telegraf.conf /etc/telegraf/ &&     chmod +x /usr/src/telegraf*/* &&     cp -a /usr/src/telegraf*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 13:51:00 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 11 Dec 2020 13:51:01 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Fri, 11 Dec 2020 13:51:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 13:51:02 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9624996f533f5dfa6054365968149298c1183a1202c16061de0fc5093ad633f`  
		Last Modified: Fri, 11 Dec 2020 02:53:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b41f8dcfdf530094e6b347e5cf020edc7a260ea9df8825794acfa748a91e65`  
		Last Modified: Fri, 11 Dec 2020 13:52:15 GMT  
		Size: 3.3 MB (3298137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4a03cfdd927f9446e6d273be41fd583d1bb30e073e17541e7fbcb2c597028a`  
		Last Modified: Fri, 11 Dec 2020 13:52:20 GMT  
		Size: 21.4 MB (21354904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f373630002a5237dd92fc516bd8442c9fc2313b2fd363a9a6b3c0534043604e`  
		Last Modified: Fri, 11 Dec 2020 13:52:12 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.15`

```console
$ docker pull telegraf@sha256:705deccf058c000c3c9c75bdbc67f78b44d0b253bbd39a512033c1c5c8badda0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.15` - linux; amd64

```console
$ docker pull telegraf@sha256:8bc5d10ef214377197d32c1a6a8be9c37ba2a81c7c735bc169ede270360f5f44
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107290293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810c267fbd8146ab6f0a9cbf816a028cf4994c1c150d264e73556e17d0ff0312`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 03:14:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:14:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 19 Nov 2020 03:14:07 GMT
ENV TELEGRAF_VERSION=1.15.4
# Thu, 19 Nov 2020 03:14:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 19 Nov 2020 03:14:10 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 19 Nov 2020 03:14:10 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 19 Nov 2020 03:14:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 03:14:11 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d6c1e41df7f683e348f4b1ba7a31ed110ef5a195b6f91f2e610375f357e311`  
		Last Modified: Thu, 19 Nov 2020 03:14:56 GMT  
		Size: 17.4 MB (17411982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5874855598e2eb7e4fbe8ccd121456de452ff75cda1db9cab5ea26f3e678dcd4`  
		Last Modified: Thu, 19 Nov 2020 03:14:53 GMT  
		Size: 2.9 KB (2871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c520ebcbdd026b7f9c9009219afa6acbe0fe84bc8a40fde879c1c0d84b537c58`  
		Last Modified: Thu, 19 Nov 2020 03:14:58 GMT  
		Size: 21.7 MB (21669580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c549c892aa3296a1247dfb6dc6172ff0e5a8f1093543cda8aa8056ebd4b32c`  
		Last Modified: Thu, 19 Nov 2020 03:14:53 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.15` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:30d1b36628865dd9ef9b169517c4d111718d31bce328497d609a25ba65d6ec33
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98879096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af582cdc8ca2bdff46f35a9a6874a2bb3bf3a850126aa7829d174fdb104e8ff1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:30 GMT
ADD file:81141d8fa450e1e5af67bb3757057f3fc34d3ed35cfd0caedb0aab64c5da9aaf in / 
# Tue, 17 Nov 2020 20:20:33 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:41:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:41:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 19:38:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 19:39:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 18 Nov 2020 19:39:02 GMT
ENV TELEGRAF_VERSION=1.15.4
# Wed, 18 Nov 2020 19:39:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 18 Nov 2020 19:39:09 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 18 Nov 2020 19:39:10 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 18 Nov 2020 19:39:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 19:39:11 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ebde10b2510128140d24e66909ceb0c80e00656af313829f82d31ae8cf08bcf8`  
		Last Modified: Tue, 17 Nov 2020 20:31:13 GMT  
		Size: 45.9 MB (45868212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05478d2a9ec4daaef33a6c87d057451c262677d02e4d9c61125bbb68bc56a601`  
		Last Modified: Tue, 17 Nov 2020 22:07:16 GMT  
		Size: 7.1 MB (7098267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c5f002cc82f5d62a78100714f451edb33a717fbf6795e309e0b1768712c093`  
		Last Modified: Tue, 17 Nov 2020 22:07:17 GMT  
		Size: 9.3 MB (9343289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedbca3e3ea6de7e47e218c7cc3f7dd619016a54ad5397be38d69b8f560828b6`  
		Last Modified: Wed, 18 Nov 2020 19:40:02 GMT  
		Size: 16.2 MB (16158373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8d00c099ae0c3d9472ea97c1bdc0ccad68561b54b5dec86934b2b7f36225d3`  
		Last Modified: Wed, 18 Nov 2020 19:39:55 GMT  
		Size: 2.9 KB (2908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90887e362f5ed4a3a3a769f0803a7bd2ffb54f9bf8ac01cb2442476a365d198b`  
		Last Modified: Wed, 18 Nov 2020 19:40:02 GMT  
		Size: 20.4 MB (20407862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcb5e4fcfffa383d9c24595525f9ca768ae4232ed8b7186b9e59bbe0e753bb3`  
		Last Modified: Wed, 18 Nov 2020 19:39:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.15` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:628852ea14e89bf9d3add7ed9163ac384c629d4a4dde7233fa6f87ef518c3142
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104136718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d9a54fc372097355d69fc8cc21390d37d8efad229da1f1f5473f3bd9ff89b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:04 GMT
ADD file:28343d2066831f0ffb2002914f158698f92b4af6dc16ac22e3d8e9c388c688bb in / 
# Tue, 17 Nov 2020 20:23:05 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:20:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:21:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 21:22:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 21:22:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 18 Nov 2020 21:22:37 GMT
ENV TELEGRAF_VERSION=1.15.4
# Wed, 18 Nov 2020 21:22:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 18 Nov 2020 21:22:44 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 18 Nov 2020 21:22:44 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 18 Nov 2020 21:22:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 21:22:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:22518ad4a7da48a5acd01946dad2fbee99e4fca910d23b78cd7e4a16c3bd1e5b`  
		Last Modified: Tue, 17 Nov 2020 20:31:35 GMT  
		Size: 49.2 MB (49179215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ed68dbf09ea059b44b3e1013706c78f868e5f07beb5f16780ca8f52aa9594a`  
		Last Modified: Tue, 17 Nov 2020 22:36:39 GMT  
		Size: 7.7 MB (7681805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eeb09cb5ac2e2a9553920a21389f08df1b6b08c816ae4b8e60866d84119492`  
		Last Modified: Tue, 17 Nov 2020 22:36:38 GMT  
		Size: 10.0 MB (9984036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99defcf10d427cd7311f65426b31bac5899cb371b55378040043b62925f1c8f8`  
		Last Modified: Wed, 18 Nov 2020 21:23:35 GMT  
		Size: 17.3 MB (17270083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b6c4c6331458eec5a72832999c71509dc81df2c6861aa17b679db9c437ef23`  
		Last Modified: Wed, 18 Nov 2020 21:23:29 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a6a290779ef76d535c44ddf9af25e98f9dadc59a316af25da718750348255`  
		Last Modified: Wed, 18 Nov 2020 21:23:35 GMT  
		Size: 20.0 MB (20018495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3fb7b8973bb452974e5e375352a3635b98f227053dffcdc643687c5f54b6e1`  
		Last Modified: Wed, 18 Nov 2020 21:23:29 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.15.4`

```console
$ docker pull telegraf@sha256:705deccf058c000c3c9c75bdbc67f78b44d0b253bbd39a512033c1c5c8badda0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.15.4` - linux; amd64

```console
$ docker pull telegraf@sha256:8bc5d10ef214377197d32c1a6a8be9c37ba2a81c7c735bc169ede270360f5f44
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107290293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810c267fbd8146ab6f0a9cbf816a028cf4994c1c150d264e73556e17d0ff0312`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 03:14:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:14:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 19 Nov 2020 03:14:07 GMT
ENV TELEGRAF_VERSION=1.15.4
# Thu, 19 Nov 2020 03:14:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 19 Nov 2020 03:14:10 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 19 Nov 2020 03:14:10 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Thu, 19 Nov 2020 03:14:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 03:14:11 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d6c1e41df7f683e348f4b1ba7a31ed110ef5a195b6f91f2e610375f357e311`  
		Last Modified: Thu, 19 Nov 2020 03:14:56 GMT  
		Size: 17.4 MB (17411982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5874855598e2eb7e4fbe8ccd121456de452ff75cda1db9cab5ea26f3e678dcd4`  
		Last Modified: Thu, 19 Nov 2020 03:14:53 GMT  
		Size: 2.9 KB (2871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c520ebcbdd026b7f9c9009219afa6acbe0fe84bc8a40fde879c1c0d84b537c58`  
		Last Modified: Thu, 19 Nov 2020 03:14:58 GMT  
		Size: 21.7 MB (21669580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c549c892aa3296a1247dfb6dc6172ff0e5a8f1093543cda8aa8056ebd4b32c`  
		Last Modified: Thu, 19 Nov 2020 03:14:53 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.15.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:30d1b36628865dd9ef9b169517c4d111718d31bce328497d609a25ba65d6ec33
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98879096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af582cdc8ca2bdff46f35a9a6874a2bb3bf3a850126aa7829d174fdb104e8ff1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:30 GMT
ADD file:81141d8fa450e1e5af67bb3757057f3fc34d3ed35cfd0caedb0aab64c5da9aaf in / 
# Tue, 17 Nov 2020 20:20:33 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:41:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:41:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 19:38:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 19:39:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 18 Nov 2020 19:39:02 GMT
ENV TELEGRAF_VERSION=1.15.4
# Wed, 18 Nov 2020 19:39:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 18 Nov 2020 19:39:09 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 18 Nov 2020 19:39:10 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 18 Nov 2020 19:39:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 19:39:11 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ebde10b2510128140d24e66909ceb0c80e00656af313829f82d31ae8cf08bcf8`  
		Last Modified: Tue, 17 Nov 2020 20:31:13 GMT  
		Size: 45.9 MB (45868212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05478d2a9ec4daaef33a6c87d057451c262677d02e4d9c61125bbb68bc56a601`  
		Last Modified: Tue, 17 Nov 2020 22:07:16 GMT  
		Size: 7.1 MB (7098267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c5f002cc82f5d62a78100714f451edb33a717fbf6795e309e0b1768712c093`  
		Last Modified: Tue, 17 Nov 2020 22:07:17 GMT  
		Size: 9.3 MB (9343289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedbca3e3ea6de7e47e218c7cc3f7dd619016a54ad5397be38d69b8f560828b6`  
		Last Modified: Wed, 18 Nov 2020 19:40:02 GMT  
		Size: 16.2 MB (16158373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8d00c099ae0c3d9472ea97c1bdc0ccad68561b54b5dec86934b2b7f36225d3`  
		Last Modified: Wed, 18 Nov 2020 19:39:55 GMT  
		Size: 2.9 KB (2908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90887e362f5ed4a3a3a769f0803a7bd2ffb54f9bf8ac01cb2442476a365d198b`  
		Last Modified: Wed, 18 Nov 2020 19:40:02 GMT  
		Size: 20.4 MB (20407862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcb5e4fcfffa383d9c24595525f9ca768ae4232ed8b7186b9e59bbe0e753bb3`  
		Last Modified: Wed, 18 Nov 2020 19:39:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.15.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:628852ea14e89bf9d3add7ed9163ac384c629d4a4dde7233fa6f87ef518c3142
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104136718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d9a54fc372097355d69fc8cc21390d37d8efad229da1f1f5473f3bd9ff89b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:04 GMT
ADD file:28343d2066831f0ffb2002914f158698f92b4af6dc16ac22e3d8e9c388c688bb in / 
# Tue, 17 Nov 2020 20:23:05 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:20:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:21:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 21:22:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 21:22:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 18 Nov 2020 21:22:37 GMT
ENV TELEGRAF_VERSION=1.15.4
# Wed, 18 Nov 2020 21:22:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 18 Nov 2020 21:22:44 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 18 Nov 2020 21:22:44 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 18 Nov 2020 21:22:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 21:22:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:22518ad4a7da48a5acd01946dad2fbee99e4fca910d23b78cd7e4a16c3bd1e5b`  
		Last Modified: Tue, 17 Nov 2020 20:31:35 GMT  
		Size: 49.2 MB (49179215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ed68dbf09ea059b44b3e1013706c78f868e5f07beb5f16780ca8f52aa9594a`  
		Last Modified: Tue, 17 Nov 2020 22:36:39 GMT  
		Size: 7.7 MB (7681805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eeb09cb5ac2e2a9553920a21389f08df1b6b08c816ae4b8e60866d84119492`  
		Last Modified: Tue, 17 Nov 2020 22:36:38 GMT  
		Size: 10.0 MB (9984036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99defcf10d427cd7311f65426b31bac5899cb371b55378040043b62925f1c8f8`  
		Last Modified: Wed, 18 Nov 2020 21:23:35 GMT  
		Size: 17.3 MB (17270083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b6c4c6331458eec5a72832999c71509dc81df2c6861aa17b679db9c437ef23`  
		Last Modified: Wed, 18 Nov 2020 21:23:29 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a6a290779ef76d535c44ddf9af25e98f9dadc59a316af25da718750348255`  
		Last Modified: Wed, 18 Nov 2020 21:23:35 GMT  
		Size: 20.0 MB (20018495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3fb7b8973bb452974e5e375352a3635b98f227053dffcdc643687c5f54b6e1`  
		Last Modified: Wed, 18 Nov 2020 21:23:29 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.15.4-alpine`

```console
$ docker pull telegraf@sha256:c1af1ca08d3434d11b19adf5a8d1b532e9e80f35c07f7257b0b303d810cf8086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.15.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:6e3c66e0026c02ace09109ae08ea2f23d113397b8932bf6465514dff3d8b2bdf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27635081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501750be137651726c5bbb556fccf2c4af9fb91b690a78613fb72ab280b57671`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 13:50:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Fri, 11 Dec 2020 13:51:12 GMT
ENV TELEGRAF_VERSION=1.15.4
# Fri, 11 Dec 2020 13:51:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 13:51:20 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 11 Dec 2020 13:51:20 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Fri, 11 Dec 2020 13:51:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 13:51:21 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9624996f533f5dfa6054365968149298c1183a1202c16061de0fc5093ad633f`  
		Last Modified: Fri, 11 Dec 2020 02:53:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b41f8dcfdf530094e6b347e5cf020edc7a260ea9df8825794acfa748a91e65`  
		Last Modified: Fri, 11 Dec 2020 13:52:15 GMT  
		Size: 3.3 MB (3298137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d911c0065ae204caa62fdbf9a5c142b30e43579d56fe854a48faa1a48b5c2349`  
		Last Modified: Fri, 11 Dec 2020 13:52:33 GMT  
		Size: 21.5 MB (21539664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43903febd2e3c4774e49a8e72adc6c91207b15177d1a94751655583351273b14`  
		Last Modified: Fri, 11 Dec 2020 13:52:28 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.15-alpine`

```console
$ docker pull telegraf@sha256:c1af1ca08d3434d11b19adf5a8d1b532e9e80f35c07f7257b0b303d810cf8086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.15-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:6e3c66e0026c02ace09109ae08ea2f23d113397b8932bf6465514dff3d8b2bdf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27635081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501750be137651726c5bbb556fccf2c4af9fb91b690a78613fb72ab280b57671`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 13:50:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Fri, 11 Dec 2020 13:51:12 GMT
ENV TELEGRAF_VERSION=1.15.4
# Fri, 11 Dec 2020 13:51:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 13:51:20 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 11 Dec 2020 13:51:20 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Fri, 11 Dec 2020 13:51:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 13:51:21 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9624996f533f5dfa6054365968149298c1183a1202c16061de0fc5093ad633f`  
		Last Modified: Fri, 11 Dec 2020 02:53:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b41f8dcfdf530094e6b347e5cf020edc7a260ea9df8825794acfa748a91e65`  
		Last Modified: Fri, 11 Dec 2020 13:52:15 GMT  
		Size: 3.3 MB (3298137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d911c0065ae204caa62fdbf9a5c142b30e43579d56fe854a48faa1a48b5c2349`  
		Last Modified: Fri, 11 Dec 2020 13:52:33 GMT  
		Size: 21.5 MB (21539664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43903febd2e3c4774e49a8e72adc6c91207b15177d1a94751655583351273b14`  
		Last Modified: Fri, 11 Dec 2020 13:52:28 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.16`

```console
$ docker pull telegraf@sha256:62bc07d7c66986ab958102681ac04461a22552d8adeed9d30bbaeb2a52c9a39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.16` - linux; amd64

```console
$ docker pull telegraf@sha256:9a88a346264a395fd90bdfe189a992b86e2486f4c856702ec709235c9183a092
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (107977914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e51f853103711ee113b533a133cfb254baaecd036ad82911e9a7a4897720b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 03:14:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:14:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 02 Dec 2020 01:11:55 GMT
ENV TELEGRAF_VERSION=1.16.3
# Wed, 02 Dec 2020 01:11:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 02 Dec 2020 01:11:59 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 02 Dec 2020 01:11:59 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 02 Dec 2020 01:11:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Dec 2020 01:11:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d6c1e41df7f683e348f4b1ba7a31ed110ef5a195b6f91f2e610375f357e311`  
		Last Modified: Thu, 19 Nov 2020 03:14:56 GMT  
		Size: 17.4 MB (17411982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5874855598e2eb7e4fbe8ccd121456de452ff75cda1db9cab5ea26f3e678dcd4`  
		Last Modified: Thu, 19 Nov 2020 03:14:53 GMT  
		Size: 2.9 KB (2871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9de99deafd4ddd3deaa1b973987abac8be49fd6207975222f60a369c0e47e14`  
		Last Modified: Wed, 02 Dec 2020 01:12:28 GMT  
		Size: 22.4 MB (22357201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc3d2dab14a20122865a86abb6b866863d0804197693fe1d2c9e8b860c829ab`  
		Last Modified: Wed, 02 Dec 2020 01:12:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.16` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:0f3b0234b891b24d1561f69bc29b0b43c1fff71a28da71d74263cdee7b7ff8f1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99361237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ae66be788718bbf1dce5d0c0a2e10a58df79d215e21d9463c304d82a88ccac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:30 GMT
ADD file:81141d8fa450e1e5af67bb3757057f3fc34d3ed35cfd0caedb0aab64c5da9aaf in / 
# Tue, 17 Nov 2020 20:20:33 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:41:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:41:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 19:38:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 19:39:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 02 Dec 2020 00:17:13 GMT
ENV TELEGRAF_VERSION=1.16.3
# Wed, 02 Dec 2020 00:17:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 02 Dec 2020 00:17:37 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 02 Dec 2020 00:17:38 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 02 Dec 2020 00:17:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Dec 2020 00:17:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ebde10b2510128140d24e66909ceb0c80e00656af313829f82d31ae8cf08bcf8`  
		Last Modified: Tue, 17 Nov 2020 20:31:13 GMT  
		Size: 45.9 MB (45868212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05478d2a9ec4daaef33a6c87d057451c262677d02e4d9c61125bbb68bc56a601`  
		Last Modified: Tue, 17 Nov 2020 22:07:16 GMT  
		Size: 7.1 MB (7098267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c5f002cc82f5d62a78100714f451edb33a717fbf6795e309e0b1768712c093`  
		Last Modified: Tue, 17 Nov 2020 22:07:17 GMT  
		Size: 9.3 MB (9343289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedbca3e3ea6de7e47e218c7cc3f7dd619016a54ad5397be38d69b8f560828b6`  
		Last Modified: Wed, 18 Nov 2020 19:40:02 GMT  
		Size: 16.2 MB (16158373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8d00c099ae0c3d9472ea97c1bdc0ccad68561b54b5dec86934b2b7f36225d3`  
		Last Modified: Wed, 18 Nov 2020 19:39:55 GMT  
		Size: 2.9 KB (2908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9fbb4f02db132292979e8cae047e1e4830ad318b4f0a4b0099ab924ea9842d`  
		Last Modified: Wed, 02 Dec 2020 00:18:12 GMT  
		Size: 20.9 MB (20890005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b702ff2f86e5fe3b43cbca0c66790a3b11e526bff2694082029e8bfa6418d43`  
		Last Modified: Wed, 02 Dec 2020 00:18:05 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.16` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:33a9e80d4f624cd0aa81ec7a1ce8fa9c04dd7fc5fa5b4e1a28640535bd038924
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104612560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7157905813f13c2e68a89f73a475c60d1d5bc84caa26427aa0926e4d354477`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:04 GMT
ADD file:28343d2066831f0ffb2002914f158698f92b4af6dc16ac22e3d8e9c388c688bb in / 
# Tue, 17 Nov 2020 20:23:05 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:20:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:21:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 21:22:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 21:22:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 02 Dec 2020 01:15:21 GMT
ENV TELEGRAF_VERSION=1.16.3
# Wed, 02 Dec 2020 01:15:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 02 Dec 2020 01:15:31 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 02 Dec 2020 01:15:32 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 02 Dec 2020 01:15:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Dec 2020 01:15:34 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:22518ad4a7da48a5acd01946dad2fbee99e4fca910d23b78cd7e4a16c3bd1e5b`  
		Last Modified: Tue, 17 Nov 2020 20:31:35 GMT  
		Size: 49.2 MB (49179215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ed68dbf09ea059b44b3e1013706c78f868e5f07beb5f16780ca8f52aa9594a`  
		Last Modified: Tue, 17 Nov 2020 22:36:39 GMT  
		Size: 7.7 MB (7681805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eeb09cb5ac2e2a9553920a21389f08df1b6b08c816ae4b8e60866d84119492`  
		Last Modified: Tue, 17 Nov 2020 22:36:38 GMT  
		Size: 10.0 MB (9984036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99defcf10d427cd7311f65426b31bac5899cb371b55378040043b62925f1c8f8`  
		Last Modified: Wed, 18 Nov 2020 21:23:35 GMT  
		Size: 17.3 MB (17270083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b6c4c6331458eec5a72832999c71509dc81df2c6861aa17b679db9c437ef23`  
		Last Modified: Wed, 18 Nov 2020 21:23:29 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86194ef779d93ab0ff3e9ff6b9526d5784cfc24400529988501184e30ea6cf81`  
		Last Modified: Wed, 02 Dec 2020 01:15:56 GMT  
		Size: 20.5 MB (20494336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89120b5b686173ad49d3a9d60dfcba92803f324b6751abc30cdea9ccb930001`  
		Last Modified: Wed, 02 Dec 2020 01:15:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.16.3`

```console
$ docker pull telegraf@sha256:62bc07d7c66986ab958102681ac04461a22552d8adeed9d30bbaeb2a52c9a39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.16.3` - linux; amd64

```console
$ docker pull telegraf@sha256:9a88a346264a395fd90bdfe189a992b86e2486f4c856702ec709235c9183a092
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (107977914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e51f853103711ee113b533a133cfb254baaecd036ad82911e9a7a4897720b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 03:14:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:14:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 02 Dec 2020 01:11:55 GMT
ENV TELEGRAF_VERSION=1.16.3
# Wed, 02 Dec 2020 01:11:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 02 Dec 2020 01:11:59 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 02 Dec 2020 01:11:59 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 02 Dec 2020 01:11:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Dec 2020 01:11:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d6c1e41df7f683e348f4b1ba7a31ed110ef5a195b6f91f2e610375f357e311`  
		Last Modified: Thu, 19 Nov 2020 03:14:56 GMT  
		Size: 17.4 MB (17411982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5874855598e2eb7e4fbe8ccd121456de452ff75cda1db9cab5ea26f3e678dcd4`  
		Last Modified: Thu, 19 Nov 2020 03:14:53 GMT  
		Size: 2.9 KB (2871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9de99deafd4ddd3deaa1b973987abac8be49fd6207975222f60a369c0e47e14`  
		Last Modified: Wed, 02 Dec 2020 01:12:28 GMT  
		Size: 22.4 MB (22357201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc3d2dab14a20122865a86abb6b866863d0804197693fe1d2c9e8b860c829ab`  
		Last Modified: Wed, 02 Dec 2020 01:12:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.16.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:0f3b0234b891b24d1561f69bc29b0b43c1fff71a28da71d74263cdee7b7ff8f1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99361237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ae66be788718bbf1dce5d0c0a2e10a58df79d215e21d9463c304d82a88ccac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:30 GMT
ADD file:81141d8fa450e1e5af67bb3757057f3fc34d3ed35cfd0caedb0aab64c5da9aaf in / 
# Tue, 17 Nov 2020 20:20:33 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:41:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:41:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 19:38:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 19:39:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 02 Dec 2020 00:17:13 GMT
ENV TELEGRAF_VERSION=1.16.3
# Wed, 02 Dec 2020 00:17:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 02 Dec 2020 00:17:37 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 02 Dec 2020 00:17:38 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 02 Dec 2020 00:17:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Dec 2020 00:17:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ebde10b2510128140d24e66909ceb0c80e00656af313829f82d31ae8cf08bcf8`  
		Last Modified: Tue, 17 Nov 2020 20:31:13 GMT  
		Size: 45.9 MB (45868212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05478d2a9ec4daaef33a6c87d057451c262677d02e4d9c61125bbb68bc56a601`  
		Last Modified: Tue, 17 Nov 2020 22:07:16 GMT  
		Size: 7.1 MB (7098267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c5f002cc82f5d62a78100714f451edb33a717fbf6795e309e0b1768712c093`  
		Last Modified: Tue, 17 Nov 2020 22:07:17 GMT  
		Size: 9.3 MB (9343289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedbca3e3ea6de7e47e218c7cc3f7dd619016a54ad5397be38d69b8f560828b6`  
		Last Modified: Wed, 18 Nov 2020 19:40:02 GMT  
		Size: 16.2 MB (16158373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8d00c099ae0c3d9472ea97c1bdc0ccad68561b54b5dec86934b2b7f36225d3`  
		Last Modified: Wed, 18 Nov 2020 19:39:55 GMT  
		Size: 2.9 KB (2908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9fbb4f02db132292979e8cae047e1e4830ad318b4f0a4b0099ab924ea9842d`  
		Last Modified: Wed, 02 Dec 2020 00:18:12 GMT  
		Size: 20.9 MB (20890005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b702ff2f86e5fe3b43cbca0c66790a3b11e526bff2694082029e8bfa6418d43`  
		Last Modified: Wed, 02 Dec 2020 00:18:05 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.16.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:33a9e80d4f624cd0aa81ec7a1ce8fa9c04dd7fc5fa5b4e1a28640535bd038924
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104612560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7157905813f13c2e68a89f73a475c60d1d5bc84caa26427aa0926e4d354477`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:04 GMT
ADD file:28343d2066831f0ffb2002914f158698f92b4af6dc16ac22e3d8e9c388c688bb in / 
# Tue, 17 Nov 2020 20:23:05 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:20:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:21:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 21:22:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 21:22:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 02 Dec 2020 01:15:21 GMT
ENV TELEGRAF_VERSION=1.16.3
# Wed, 02 Dec 2020 01:15:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 02 Dec 2020 01:15:31 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 02 Dec 2020 01:15:32 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 02 Dec 2020 01:15:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Dec 2020 01:15:34 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:22518ad4a7da48a5acd01946dad2fbee99e4fca910d23b78cd7e4a16c3bd1e5b`  
		Last Modified: Tue, 17 Nov 2020 20:31:35 GMT  
		Size: 49.2 MB (49179215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ed68dbf09ea059b44b3e1013706c78f868e5f07beb5f16780ca8f52aa9594a`  
		Last Modified: Tue, 17 Nov 2020 22:36:39 GMT  
		Size: 7.7 MB (7681805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eeb09cb5ac2e2a9553920a21389f08df1b6b08c816ae4b8e60866d84119492`  
		Last Modified: Tue, 17 Nov 2020 22:36:38 GMT  
		Size: 10.0 MB (9984036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99defcf10d427cd7311f65426b31bac5899cb371b55378040043b62925f1c8f8`  
		Last Modified: Wed, 18 Nov 2020 21:23:35 GMT  
		Size: 17.3 MB (17270083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b6c4c6331458eec5a72832999c71509dc81df2c6861aa17b679db9c437ef23`  
		Last Modified: Wed, 18 Nov 2020 21:23:29 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86194ef779d93ab0ff3e9ff6b9526d5784cfc24400529988501184e30ea6cf81`  
		Last Modified: Wed, 02 Dec 2020 01:15:56 GMT  
		Size: 20.5 MB (20494336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89120b5b686173ad49d3a9d60dfcba92803f324b6751abc30cdea9ccb930001`  
		Last Modified: Wed, 02 Dec 2020 01:15:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.16.3-alpine`

```console
$ docker pull telegraf@sha256:5b2a4fc9aab295dcc27291d4db05cd16cdd28fbc881be8b85b8885c0fb64f5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.16.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c425554204a9b21fc6cb3fa7a94df957bc9848d1273cf4fb49085ba3c7b66d28
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28309665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07361a0446436294df5d9740e3d0857f35e024360be73443fa852e9ae47df900`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 13:50:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Fri, 11 Dec 2020 13:51:33 GMT
ENV TELEGRAF_VERSION=1.16.3
# Fri, 11 Dec 2020 13:51:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 13:51:40 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 11 Dec 2020 13:51:41 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Fri, 11 Dec 2020 13:51:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 13:51:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9624996f533f5dfa6054365968149298c1183a1202c16061de0fc5093ad633f`  
		Last Modified: Fri, 11 Dec 2020 02:53:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b41f8dcfdf530094e6b347e5cf020edc7a260ea9df8825794acfa748a91e65`  
		Last Modified: Fri, 11 Dec 2020 13:52:15 GMT  
		Size: 3.3 MB (3298137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06fc4e567d60ba73099d32627ff03e8a60d57bd6c0ddd212906a047cd1ee9bd`  
		Last Modified: Fri, 11 Dec 2020 13:52:45 GMT  
		Size: 22.2 MB (22214246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77890822bfb88a1afb68d31aacad1c5721e0d38aa270fb077cba65e4a6c58861`  
		Last Modified: Fri, 11 Dec 2020 13:52:40 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.16-alpine`

```console
$ docker pull telegraf@sha256:5b2a4fc9aab295dcc27291d4db05cd16cdd28fbc881be8b85b8885c0fb64f5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.16-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c425554204a9b21fc6cb3fa7a94df957bc9848d1273cf4fb49085ba3c7b66d28
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28309665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07361a0446436294df5d9740e3d0857f35e024360be73443fa852e9ae47df900`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 13:50:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Fri, 11 Dec 2020 13:51:33 GMT
ENV TELEGRAF_VERSION=1.16.3
# Fri, 11 Dec 2020 13:51:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 13:51:40 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 11 Dec 2020 13:51:41 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Fri, 11 Dec 2020 13:51:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 13:51:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9624996f533f5dfa6054365968149298c1183a1202c16061de0fc5093ad633f`  
		Last Modified: Fri, 11 Dec 2020 02:53:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b41f8dcfdf530094e6b347e5cf020edc7a260ea9df8825794acfa748a91e65`  
		Last Modified: Fri, 11 Dec 2020 13:52:15 GMT  
		Size: 3.3 MB (3298137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06fc4e567d60ba73099d32627ff03e8a60d57bd6c0ddd212906a047cd1ee9bd`  
		Last Modified: Fri, 11 Dec 2020 13:52:45 GMT  
		Size: 22.2 MB (22214246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77890822bfb88a1afb68d31aacad1c5721e0d38aa270fb077cba65e4a6c58861`  
		Last Modified: Fri, 11 Dec 2020 13:52:40 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:5b2a4fc9aab295dcc27291d4db05cd16cdd28fbc881be8b85b8885c0fb64f5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c425554204a9b21fc6cb3fa7a94df957bc9848d1273cf4fb49085ba3c7b66d28
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28309665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07361a0446436294df5d9740e3d0857f35e024360be73443fa852e9ae47df900`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 13:50:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Fri, 11 Dec 2020 13:51:33 GMT
ENV TELEGRAF_VERSION=1.16.3
# Fri, 11 Dec 2020 13:51:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 13:51:40 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 11 Dec 2020 13:51:41 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Fri, 11 Dec 2020 13:51:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 13:51:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9624996f533f5dfa6054365968149298c1183a1202c16061de0fc5093ad633f`  
		Last Modified: Fri, 11 Dec 2020 02:53:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b41f8dcfdf530094e6b347e5cf020edc7a260ea9df8825794acfa748a91e65`  
		Last Modified: Fri, 11 Dec 2020 13:52:15 GMT  
		Size: 3.3 MB (3298137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06fc4e567d60ba73099d32627ff03e8a60d57bd6c0ddd212906a047cd1ee9bd`  
		Last Modified: Fri, 11 Dec 2020 13:52:45 GMT  
		Size: 22.2 MB (22214246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77890822bfb88a1afb68d31aacad1c5721e0d38aa270fb077cba65e4a6c58861`  
		Last Modified: Fri, 11 Dec 2020 13:52:40 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:62bc07d7c66986ab958102681ac04461a22552d8adeed9d30bbaeb2a52c9a39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:9a88a346264a395fd90bdfe189a992b86e2486f4c856702ec709235c9183a092
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (107977914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e51f853103711ee113b533a133cfb254baaecd036ad82911e9a7a4897720b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 03:14:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:14:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 02 Dec 2020 01:11:55 GMT
ENV TELEGRAF_VERSION=1.16.3
# Wed, 02 Dec 2020 01:11:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 02 Dec 2020 01:11:59 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 02 Dec 2020 01:11:59 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 02 Dec 2020 01:11:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Dec 2020 01:11:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d6c1e41df7f683e348f4b1ba7a31ed110ef5a195b6f91f2e610375f357e311`  
		Last Modified: Thu, 19 Nov 2020 03:14:56 GMT  
		Size: 17.4 MB (17411982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5874855598e2eb7e4fbe8ccd121456de452ff75cda1db9cab5ea26f3e678dcd4`  
		Last Modified: Thu, 19 Nov 2020 03:14:53 GMT  
		Size: 2.9 KB (2871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9de99deafd4ddd3deaa1b973987abac8be49fd6207975222f60a369c0e47e14`  
		Last Modified: Wed, 02 Dec 2020 01:12:28 GMT  
		Size: 22.4 MB (22357201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc3d2dab14a20122865a86abb6b866863d0804197693fe1d2c9e8b860c829ab`  
		Last Modified: Wed, 02 Dec 2020 01:12:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:0f3b0234b891b24d1561f69bc29b0b43c1fff71a28da71d74263cdee7b7ff8f1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99361237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ae66be788718bbf1dce5d0c0a2e10a58df79d215e21d9463c304d82a88ccac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:30 GMT
ADD file:81141d8fa450e1e5af67bb3757057f3fc34d3ed35cfd0caedb0aab64c5da9aaf in / 
# Tue, 17 Nov 2020 20:20:33 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:41:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:41:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 19:38:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 19:39:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 02 Dec 2020 00:17:13 GMT
ENV TELEGRAF_VERSION=1.16.3
# Wed, 02 Dec 2020 00:17:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 02 Dec 2020 00:17:37 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 02 Dec 2020 00:17:38 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 02 Dec 2020 00:17:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Dec 2020 00:17:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ebde10b2510128140d24e66909ceb0c80e00656af313829f82d31ae8cf08bcf8`  
		Last Modified: Tue, 17 Nov 2020 20:31:13 GMT  
		Size: 45.9 MB (45868212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05478d2a9ec4daaef33a6c87d057451c262677d02e4d9c61125bbb68bc56a601`  
		Last Modified: Tue, 17 Nov 2020 22:07:16 GMT  
		Size: 7.1 MB (7098267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c5f002cc82f5d62a78100714f451edb33a717fbf6795e309e0b1768712c093`  
		Last Modified: Tue, 17 Nov 2020 22:07:17 GMT  
		Size: 9.3 MB (9343289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedbca3e3ea6de7e47e218c7cc3f7dd619016a54ad5397be38d69b8f560828b6`  
		Last Modified: Wed, 18 Nov 2020 19:40:02 GMT  
		Size: 16.2 MB (16158373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8d00c099ae0c3d9472ea97c1bdc0ccad68561b54b5dec86934b2b7f36225d3`  
		Last Modified: Wed, 18 Nov 2020 19:39:55 GMT  
		Size: 2.9 KB (2908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9fbb4f02db132292979e8cae047e1e4830ad318b4f0a4b0099ab924ea9842d`  
		Last Modified: Wed, 02 Dec 2020 00:18:12 GMT  
		Size: 20.9 MB (20890005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b702ff2f86e5fe3b43cbca0c66790a3b11e526bff2694082029e8bfa6418d43`  
		Last Modified: Wed, 02 Dec 2020 00:18:05 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:33a9e80d4f624cd0aa81ec7a1ce8fa9c04dd7fc5fa5b4e1a28640535bd038924
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104612560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7157905813f13c2e68a89f73a475c60d1d5bc84caa26427aa0926e4d354477`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:04 GMT
ADD file:28343d2066831f0ffb2002914f158698f92b4af6dc16ac22e3d8e9c388c688bb in / 
# Tue, 17 Nov 2020 20:23:05 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:20:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:21:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 21:22:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 21:22:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 02 Dec 2020 01:15:21 GMT
ENV TELEGRAF_VERSION=1.16.3
# Wed, 02 Dec 2020 01:15:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 02 Dec 2020 01:15:31 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 02 Dec 2020 01:15:32 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 02 Dec 2020 01:15:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Dec 2020 01:15:34 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:22518ad4a7da48a5acd01946dad2fbee99e4fca910d23b78cd7e4a16c3bd1e5b`  
		Last Modified: Tue, 17 Nov 2020 20:31:35 GMT  
		Size: 49.2 MB (49179215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ed68dbf09ea059b44b3e1013706c78f868e5f07beb5f16780ca8f52aa9594a`  
		Last Modified: Tue, 17 Nov 2020 22:36:39 GMT  
		Size: 7.7 MB (7681805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eeb09cb5ac2e2a9553920a21389f08df1b6b08c816ae4b8e60866d84119492`  
		Last Modified: Tue, 17 Nov 2020 22:36:38 GMT  
		Size: 10.0 MB (9984036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99defcf10d427cd7311f65426b31bac5899cb371b55378040043b62925f1c8f8`  
		Last Modified: Wed, 18 Nov 2020 21:23:35 GMT  
		Size: 17.3 MB (17270083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b6c4c6331458eec5a72832999c71509dc81df2c6861aa17b679db9c437ef23`  
		Last Modified: Wed, 18 Nov 2020 21:23:29 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86194ef779d93ab0ff3e9ff6b9526d5784cfc24400529988501184e30ea6cf81`  
		Last Modified: Wed, 02 Dec 2020 01:15:56 GMT  
		Size: 20.5 MB (20494336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89120b5b686173ad49d3a9d60dfcba92803f324b6751abc30cdea9ccb930001`  
		Last Modified: Wed, 02 Dec 2020 01:15:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
