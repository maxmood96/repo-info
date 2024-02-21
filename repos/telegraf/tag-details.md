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
-	[`telegraf:1.29.5`](#telegraf1295)
-	[`telegraf:1.29.5-alpine`](#telegraf1295-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.27`

```console
$ docker pull telegraf@sha256:0d8b264261d70d6fc48fa9b5383ceb77c4ff40022fefad5b75fa0e6ae2da9cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.27` - linux; amd64

```console
$ docker pull telegraf@sha256:7f81f710bdca41aaf67cfe5e99517d1074f612b82f6eb42ead35770900d1144d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148079676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bed9297f3354b2d5b788ccfd4cef061d4d5b7091e7d1a10a0d95e9b39f96414`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 13:04:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 13:04:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 13:04:52 GMT
ENV TELEGRAF_VERSION=1.27.4
# Tue, 13 Feb 2024 13:04:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 13 Feb 2024 13:04:56 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 21 Feb 2024 01:01:14 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Wed, 21 Feb 2024 01:01:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Feb 2024 01:01:14 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c71dd3592ae7480fef8cfd38fa2eb3e6694745fd687b9ced3e1602331c069f`  
		Last Modified: Tue, 13 Feb 2024 13:05:35 GMT  
		Size: 19.2 MB (19151417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9140cc5510d63237e7fcacc3cfbcb2a1338e9934d7705922cc175a91aac1416b`  
		Last Modified: Tue, 13 Feb 2024 13:05:32 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f217903a7604c9572a8dc3484d9c9eb66419f6f92089cf5d25e192bb5f7e2b85`  
		Last Modified: Tue, 13 Feb 2024 13:05:41 GMT  
		Size: 55.3 MB (55326880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2f786989da2d6753df9ba5c1cd0daa9f669d1065c0a133e546bfaca39aae7c`  
		Last Modified: Wed, 21 Feb 2024 01:01:59 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:50dbbde34ce95ac0d227c2e88b52684e2ee8692787275f2bb238233d5bb2f6e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136542242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c60b79fc30b0ac22bf4c810ebb250b406bb7ec6cb85ccc242a3190fe9b3ab6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 01:19:48 GMT
ADD file:9b07e306d84beed6568160f3e02cfd7537add7bed5debf00f251fee99a50ee80 in / 
# Tue, 13 Feb 2024 01:19:49 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 17:14:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 17:14:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 17:14:43 GMT
ENV TELEGRAF_VERSION=1.27.4
# Tue, 13 Feb 2024 17:14:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 13 Feb 2024 17:14:54 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 20 Feb 2024 23:57:44 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Tue, 20 Feb 2024 23:57:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Feb 2024 23:57:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:84ee7bddcb1a35ae933efe6113f47b4047fb90d2a626c4a8a93e3548fa8b61d5`  
		Last Modified: Tue, 13 Feb 2024 01:26:22 GMT  
		Size: 45.2 MB (45153612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e6fa0e83f7c31cdfb8e77c4a8229243dc182cac7b985200c404bddc6e2bc9d`  
		Last Modified: Tue, 13 Feb 2024 04:26:58 GMT  
		Size: 22.0 MB (21950325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106e9dcbc36f8610a588868a2b26cfca072a98e44b65004999cb2045135307fe`  
		Last Modified: Tue, 13 Feb 2024 17:15:49 GMT  
		Size: 17.9 MB (17930146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b35263345c17ee21c6873626e4bbeb503ca2b1144bb1f0e4fe80793280e5d6a`  
		Last Modified: Tue, 13 Feb 2024 17:15:43 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a3ca16728e87223655c8ae7ecbe04ceaca0b4c24b769885fdc7a87bd6a669d`  
		Last Modified: Tue, 13 Feb 2024 17:15:55 GMT  
		Size: 51.5 MB (51505963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8371101632acae24f2dddf8c77b303bb03451562225aa0d2a310c11b3be349ac`  
		Last Modified: Tue, 20 Feb 2024 23:58:08 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a1295fc74a5780d4d4d59d103cf264e0ba56fada4dffa44a89764c23f0ed3802
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142210160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ce5f1a5242f0e7e79be74a5ec85c094a2f13cb0d104f944f62694d2fd9846b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:48:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:48:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 11:48:15 GMT
ENV TELEGRAF_VERSION=1.27.4
# Tue, 13 Feb 2024 11:48:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 13 Feb 2024 11:48:19 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 20 Feb 2024 23:59:37 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Tue, 20 Feb 2024 23:59:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Feb 2024 23:59:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f707ba957ebc9b527b04c0819aa8bf91e3c23b713922f22fccfc74fbc74dbc`  
		Last Modified: Tue, 13 Feb 2024 11:48:55 GMT  
		Size: 19.1 MB (19075452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b98e47593d4c2d0e4d705e1cca72b55387a78f74f3b309b5d257f89bae5d3`  
		Last Modified: Tue, 13 Feb 2024 11:48:54 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283cdc695371f65473db8c74fa9514c3198d7956340fc305f0a5261b6c4d59d3`  
		Last Modified: Tue, 13 Feb 2024 11:48:59 GMT  
		Size: 50.0 MB (49958779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823a7bc4832dea3a6288604a76b18f1341bce36a99a13740ac95814dacf1aa12`  
		Last Modified: Wed, 21 Feb 2024 00:00:27 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.27-alpine`

```console
$ docker pull telegraf@sha256:d9a8491c49df156b82fb2added01f556f96d9776fd706bc9a3a63b18e5d87c24
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
$ docker pull telegraf@sha256:15ff38873c847f4a3c57e1aeb389383169fc01c0e090eb5c6d2597c86309fb91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55803326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5d49dd54b3ca9f513e983a7bc179e8e5b1f3c8347ae698f35c0517b7e313a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:14:32 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 09:10:37 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 27 Jan 2024 09:10:37 GMT
ENV TELEGRAF_VERSION=1.27.4
# Sat, 27 Jan 2024 09:10:44 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 27 Jan 2024 09:10:45 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 27 Jan 2024 09:10:45 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 27 Jan 2024 09:10:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 09:10:45 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b10b365dc27fbcb456614696265123cb9aa34afefec8863e4cc7c7c90a506f5`  
		Last Modified: Sat, 27 Jan 2024 04:14:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7525fc3259afa1a7bfbf09f186ed24e031f2229e1c7c98b4eb70cf0551c6bb7`  
		Last Modified: Sat, 27 Jan 2024 09:11:24 GMT  
		Size: 2.7 MB (2673745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8027cdb7aad7f3a557a83756f94597106717434616c9193e77818741239da48`  
		Last Modified: Sat, 27 Jan 2024 09:11:30 GMT  
		Size: 49.8 MB (49795616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981c3ea8d91c7061286b36f594cc0bfed86c2317e645a2414846ed459795fcc5`  
		Last Modified: Sat, 27 Jan 2024 09:11:24 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.27.4`

```console
$ docker pull telegraf@sha256:0d8b264261d70d6fc48fa9b5383ceb77c4ff40022fefad5b75fa0e6ae2da9cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.27.4` - linux; amd64

```console
$ docker pull telegraf@sha256:7f81f710bdca41aaf67cfe5e99517d1074f612b82f6eb42ead35770900d1144d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148079676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bed9297f3354b2d5b788ccfd4cef061d4d5b7091e7d1a10a0d95e9b39f96414`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 13:04:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 13:04:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 13:04:52 GMT
ENV TELEGRAF_VERSION=1.27.4
# Tue, 13 Feb 2024 13:04:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 13 Feb 2024 13:04:56 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 21 Feb 2024 01:01:14 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Wed, 21 Feb 2024 01:01:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Feb 2024 01:01:14 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c71dd3592ae7480fef8cfd38fa2eb3e6694745fd687b9ced3e1602331c069f`  
		Last Modified: Tue, 13 Feb 2024 13:05:35 GMT  
		Size: 19.2 MB (19151417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9140cc5510d63237e7fcacc3cfbcb2a1338e9934d7705922cc175a91aac1416b`  
		Last Modified: Tue, 13 Feb 2024 13:05:32 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f217903a7604c9572a8dc3484d9c9eb66419f6f92089cf5d25e192bb5f7e2b85`  
		Last Modified: Tue, 13 Feb 2024 13:05:41 GMT  
		Size: 55.3 MB (55326880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2f786989da2d6753df9ba5c1cd0daa9f669d1065c0a133e546bfaca39aae7c`  
		Last Modified: Wed, 21 Feb 2024 01:01:59 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:50dbbde34ce95ac0d227c2e88b52684e2ee8692787275f2bb238233d5bb2f6e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136542242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c60b79fc30b0ac22bf4c810ebb250b406bb7ec6cb85ccc242a3190fe9b3ab6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 01:19:48 GMT
ADD file:9b07e306d84beed6568160f3e02cfd7537add7bed5debf00f251fee99a50ee80 in / 
# Tue, 13 Feb 2024 01:19:49 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 17:14:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 17:14:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 17:14:43 GMT
ENV TELEGRAF_VERSION=1.27.4
# Tue, 13 Feb 2024 17:14:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 13 Feb 2024 17:14:54 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 20 Feb 2024 23:57:44 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Tue, 20 Feb 2024 23:57:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Feb 2024 23:57:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:84ee7bddcb1a35ae933efe6113f47b4047fb90d2a626c4a8a93e3548fa8b61d5`  
		Last Modified: Tue, 13 Feb 2024 01:26:22 GMT  
		Size: 45.2 MB (45153612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e6fa0e83f7c31cdfb8e77c4a8229243dc182cac7b985200c404bddc6e2bc9d`  
		Last Modified: Tue, 13 Feb 2024 04:26:58 GMT  
		Size: 22.0 MB (21950325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106e9dcbc36f8610a588868a2b26cfca072a98e44b65004999cb2045135307fe`  
		Last Modified: Tue, 13 Feb 2024 17:15:49 GMT  
		Size: 17.9 MB (17930146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b35263345c17ee21c6873626e4bbeb503ca2b1144bb1f0e4fe80793280e5d6a`  
		Last Modified: Tue, 13 Feb 2024 17:15:43 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a3ca16728e87223655c8ae7ecbe04ceaca0b4c24b769885fdc7a87bd6a669d`  
		Last Modified: Tue, 13 Feb 2024 17:15:55 GMT  
		Size: 51.5 MB (51505963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8371101632acae24f2dddf8c77b303bb03451562225aa0d2a310c11b3be349ac`  
		Last Modified: Tue, 20 Feb 2024 23:58:08 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a1295fc74a5780d4d4d59d103cf264e0ba56fada4dffa44a89764c23f0ed3802
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142210160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ce5f1a5242f0e7e79be74a5ec85c094a2f13cb0d104f944f62694d2fd9846b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:48:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:48:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 11:48:15 GMT
ENV TELEGRAF_VERSION=1.27.4
# Tue, 13 Feb 2024 11:48:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 13 Feb 2024 11:48:19 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 20 Feb 2024 23:59:37 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Tue, 20 Feb 2024 23:59:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Feb 2024 23:59:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f707ba957ebc9b527b04c0819aa8bf91e3c23b713922f22fccfc74fbc74dbc`  
		Last Modified: Tue, 13 Feb 2024 11:48:55 GMT  
		Size: 19.1 MB (19075452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b98e47593d4c2d0e4d705e1cca72b55387a78f74f3b309b5d257f89bae5d3`  
		Last Modified: Tue, 13 Feb 2024 11:48:54 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283cdc695371f65473db8c74fa9514c3198d7956340fc305f0a5261b6c4d59d3`  
		Last Modified: Tue, 13 Feb 2024 11:48:59 GMT  
		Size: 50.0 MB (49958779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823a7bc4832dea3a6288604a76b18f1341bce36a99a13740ac95814dacf1aa12`  
		Last Modified: Wed, 21 Feb 2024 00:00:27 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.27.4-alpine`

```console
$ docker pull telegraf@sha256:d9a8491c49df156b82fb2added01f556f96d9776fd706bc9a3a63b18e5d87c24
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
$ docker pull telegraf@sha256:15ff38873c847f4a3c57e1aeb389383169fc01c0e090eb5c6d2597c86309fb91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55803326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5d49dd54b3ca9f513e983a7bc179e8e5b1f3c8347ae698f35c0517b7e313a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:14:32 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 09:10:37 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 27 Jan 2024 09:10:37 GMT
ENV TELEGRAF_VERSION=1.27.4
# Sat, 27 Jan 2024 09:10:44 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 27 Jan 2024 09:10:45 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 27 Jan 2024 09:10:45 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 27 Jan 2024 09:10:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 09:10:45 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b10b365dc27fbcb456614696265123cb9aa34afefec8863e4cc7c7c90a506f5`  
		Last Modified: Sat, 27 Jan 2024 04:14:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7525fc3259afa1a7bfbf09f186ed24e031f2229e1c7c98b4eb70cf0551c6bb7`  
		Last Modified: Sat, 27 Jan 2024 09:11:24 GMT  
		Size: 2.7 MB (2673745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8027cdb7aad7f3a557a83756f94597106717434616c9193e77818741239da48`  
		Last Modified: Sat, 27 Jan 2024 09:11:30 GMT  
		Size: 49.8 MB (49795616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981c3ea8d91c7061286b36f594cc0bfed86c2317e645a2414846ed459795fcc5`  
		Last Modified: Sat, 27 Jan 2024 09:11:24 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28`

```console
$ docker pull telegraf@sha256:b469486a955942e9279316622db7ee6c05789e94f1940e33635b550a63c3d051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.28` - linux; amd64

```console
$ docker pull telegraf@sha256:c7697144301ec25111b7d6a15ac9e059599eba1fcb77d944947aa45ceb1a026b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149841988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b577e470e325d26c8ddb594aec70a1d20ed4b61143fa3451491ef4115c58b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 13:04:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 13:04:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 13:05:02 GMT
ENV TELEGRAF_VERSION=1.28.5
# Tue, 13 Feb 2024 13:05:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 13 Feb 2024 13:05:07 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 21 Feb 2024 01:01:19 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Wed, 21 Feb 2024 01:01:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Feb 2024 01:01:20 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c71dd3592ae7480fef8cfd38fa2eb3e6694745fd687b9ced3e1602331c069f`  
		Last Modified: Tue, 13 Feb 2024 13:05:35 GMT  
		Size: 19.2 MB (19151417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9140cc5510d63237e7fcacc3cfbcb2a1338e9934d7705922cc175a91aac1416b`  
		Last Modified: Tue, 13 Feb 2024 13:05:32 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0b556cb70f6cda82f9226616ee41c5e21e01c5d30d1d25eddcaf7095b5354c`  
		Last Modified: Tue, 13 Feb 2024 13:06:00 GMT  
		Size: 57.1 MB (57089192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b97ca0e44263ef107969d9d7b700bafba51eb9a45be2bad6cc55ba25581c239`  
		Last Modified: Wed, 21 Feb 2024 01:02:08 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:c53423eea3b7923d3aaa128fc378216b3749edbc7261e76f850b2c28f2a80015
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137590970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3bf8c87bd29e0a824b3201f5320803497bdec285cf540df10b1fa59213537d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 01:19:48 GMT
ADD file:9b07e306d84beed6568160f3e02cfd7537add7bed5debf00f251fee99a50ee80 in / 
# Tue, 13 Feb 2024 01:19:49 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 17:14:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 17:14:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 17:14:59 GMT
ENV TELEGRAF_VERSION=1.28.5
# Tue, 13 Feb 2024 17:15:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 13 Feb 2024 17:15:11 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 20 Feb 2024 23:57:46 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Tue, 20 Feb 2024 23:57:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Feb 2024 23:57:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:84ee7bddcb1a35ae933efe6113f47b4047fb90d2a626c4a8a93e3548fa8b61d5`  
		Last Modified: Tue, 13 Feb 2024 01:26:22 GMT  
		Size: 45.2 MB (45153612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e6fa0e83f7c31cdfb8e77c4a8229243dc182cac7b985200c404bddc6e2bc9d`  
		Last Modified: Tue, 13 Feb 2024 04:26:58 GMT  
		Size: 22.0 MB (21950325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106e9dcbc36f8610a588868a2b26cfca072a98e44b65004999cb2045135307fe`  
		Last Modified: Tue, 13 Feb 2024 17:15:49 GMT  
		Size: 17.9 MB (17930146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b35263345c17ee21c6873626e4bbeb503ca2b1144bb1f0e4fe80793280e5d6a`  
		Last Modified: Tue, 13 Feb 2024 17:15:43 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a21f2b057aecd2b020491add1f2018afbf110e4b34ff9bac71a236a2c1cb9f`  
		Last Modified: Tue, 13 Feb 2024 17:16:16 GMT  
		Size: 52.6 MB (52554692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77cdb6c7b8a824c443acc0442cff6f3f0fe69a89b8bedf0b9416c1eb87af322`  
		Last Modified: Tue, 20 Feb 2024 23:58:15 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:b625409296376f55a7e9c796a411c997dd34dbecc869121ed777806c9e9b737d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144002074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedf4afef846196d285a034f56e63eaecfefd7047fa55aa1c618886903ef3e69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:48:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:48:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 11:48:25 GMT
ENV TELEGRAF_VERSION=1.28.5
# Tue, 13 Feb 2024 11:48:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 13 Feb 2024 11:48:29 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 20 Feb 2024 23:59:40 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Tue, 20 Feb 2024 23:59:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Feb 2024 23:59:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f707ba957ebc9b527b04c0819aa8bf91e3c23b713922f22fccfc74fbc74dbc`  
		Last Modified: Tue, 13 Feb 2024 11:48:55 GMT  
		Size: 19.1 MB (19075452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b98e47593d4c2d0e4d705e1cca72b55387a78f74f3b309b5d257f89bae5d3`  
		Last Modified: Tue, 13 Feb 2024 11:48:54 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b88fb02f553bf494bf6d3d4bf3179dfcf4d29653864f7a1e80e7def907809f8`  
		Last Modified: Tue, 13 Feb 2024 11:49:13 GMT  
		Size: 51.8 MB (51750693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e607cc1a0a2e47463a9d637e49ad5546044faec3b4859c1ae8cce014f61883`  
		Last Modified: Wed, 21 Feb 2024 00:00:36 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28-alpine`

```console
$ docker pull telegraf@sha256:6d91203705ccf1f896a9f4cac75b428cf39995a2f33365addf441f05f5db43c1
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
$ docker pull telegraf@sha256:34a1bc8756c13764ff2bf49d09c5075c2dd1fabe7dcf10ce4803851e5be207f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57595261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f23e3ce2ba33c73069b57ffe4060888a6c6c82cf6b0e797e65b00f9a382e12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:14:32 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 09:10:37 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 27 Jan 2024 09:10:48 GMT
ENV TELEGRAF_VERSION=1.28.5
# Sat, 27 Jan 2024 09:10:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 27 Jan 2024 09:10:55 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 27 Jan 2024 09:10:55 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 27 Jan 2024 09:10:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 09:10:55 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b10b365dc27fbcb456614696265123cb9aa34afefec8863e4cc7c7c90a506f5`  
		Last Modified: Sat, 27 Jan 2024 04:14:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7525fc3259afa1a7bfbf09f186ed24e031f2229e1c7c98b4eb70cf0551c6bb7`  
		Last Modified: Sat, 27 Jan 2024 09:11:24 GMT  
		Size: 2.7 MB (2673745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e607b726aaafc6a7fe5e1c80c11d0333c64a2489025dae25d530cbcbecd2001c`  
		Last Modified: Sat, 27 Jan 2024 09:11:44 GMT  
		Size: 51.6 MB (51587551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b61c9edef3f53da5024b99f28e35e828a3f526834dd7801c33c5e1ee9f6df7`  
		Last Modified: Sat, 27 Jan 2024 09:11:38 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28.5`

```console
$ docker pull telegraf@sha256:b469486a955942e9279316622db7ee6c05789e94f1940e33635b550a63c3d051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.28.5` - linux; amd64

```console
$ docker pull telegraf@sha256:c7697144301ec25111b7d6a15ac9e059599eba1fcb77d944947aa45ceb1a026b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149841988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b577e470e325d26c8ddb594aec70a1d20ed4b61143fa3451491ef4115c58b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 13:04:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 13:04:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 13:05:02 GMT
ENV TELEGRAF_VERSION=1.28.5
# Tue, 13 Feb 2024 13:05:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 13 Feb 2024 13:05:07 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 21 Feb 2024 01:01:19 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Wed, 21 Feb 2024 01:01:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Feb 2024 01:01:20 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c71dd3592ae7480fef8cfd38fa2eb3e6694745fd687b9ced3e1602331c069f`  
		Last Modified: Tue, 13 Feb 2024 13:05:35 GMT  
		Size: 19.2 MB (19151417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9140cc5510d63237e7fcacc3cfbcb2a1338e9934d7705922cc175a91aac1416b`  
		Last Modified: Tue, 13 Feb 2024 13:05:32 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0b556cb70f6cda82f9226616ee41c5e21e01c5d30d1d25eddcaf7095b5354c`  
		Last Modified: Tue, 13 Feb 2024 13:06:00 GMT  
		Size: 57.1 MB (57089192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b97ca0e44263ef107969d9d7b700bafba51eb9a45be2bad6cc55ba25581c239`  
		Last Modified: Wed, 21 Feb 2024 01:02:08 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28.5` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:c53423eea3b7923d3aaa128fc378216b3749edbc7261e76f850b2c28f2a80015
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137590970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3bf8c87bd29e0a824b3201f5320803497bdec285cf540df10b1fa59213537d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 01:19:48 GMT
ADD file:9b07e306d84beed6568160f3e02cfd7537add7bed5debf00f251fee99a50ee80 in / 
# Tue, 13 Feb 2024 01:19:49 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 17:14:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 17:14:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 17:14:59 GMT
ENV TELEGRAF_VERSION=1.28.5
# Tue, 13 Feb 2024 17:15:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 13 Feb 2024 17:15:11 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 20 Feb 2024 23:57:46 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Tue, 20 Feb 2024 23:57:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Feb 2024 23:57:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:84ee7bddcb1a35ae933efe6113f47b4047fb90d2a626c4a8a93e3548fa8b61d5`  
		Last Modified: Tue, 13 Feb 2024 01:26:22 GMT  
		Size: 45.2 MB (45153612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e6fa0e83f7c31cdfb8e77c4a8229243dc182cac7b985200c404bddc6e2bc9d`  
		Last Modified: Tue, 13 Feb 2024 04:26:58 GMT  
		Size: 22.0 MB (21950325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106e9dcbc36f8610a588868a2b26cfca072a98e44b65004999cb2045135307fe`  
		Last Modified: Tue, 13 Feb 2024 17:15:49 GMT  
		Size: 17.9 MB (17930146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b35263345c17ee21c6873626e4bbeb503ca2b1144bb1f0e4fe80793280e5d6a`  
		Last Modified: Tue, 13 Feb 2024 17:15:43 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a21f2b057aecd2b020491add1f2018afbf110e4b34ff9bac71a236a2c1cb9f`  
		Last Modified: Tue, 13 Feb 2024 17:16:16 GMT  
		Size: 52.6 MB (52554692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77cdb6c7b8a824c443acc0442cff6f3f0fe69a89b8bedf0b9416c1eb87af322`  
		Last Modified: Tue, 20 Feb 2024 23:58:15 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28.5` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:b625409296376f55a7e9c796a411c997dd34dbecc869121ed777806c9e9b737d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144002074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedf4afef846196d285a034f56e63eaecfefd7047fa55aa1c618886903ef3e69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:48:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:48:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 11:48:25 GMT
ENV TELEGRAF_VERSION=1.28.5
# Tue, 13 Feb 2024 11:48:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 13 Feb 2024 11:48:29 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 20 Feb 2024 23:59:40 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Tue, 20 Feb 2024 23:59:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Feb 2024 23:59:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f707ba957ebc9b527b04c0819aa8bf91e3c23b713922f22fccfc74fbc74dbc`  
		Last Modified: Tue, 13 Feb 2024 11:48:55 GMT  
		Size: 19.1 MB (19075452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b98e47593d4c2d0e4d705e1cca72b55387a78f74f3b309b5d257f89bae5d3`  
		Last Modified: Tue, 13 Feb 2024 11:48:54 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b88fb02f553bf494bf6d3d4bf3179dfcf4d29653864f7a1e80e7def907809f8`  
		Last Modified: Tue, 13 Feb 2024 11:49:13 GMT  
		Size: 51.8 MB (51750693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e607cc1a0a2e47463a9d637e49ad5546044faec3b4859c1ae8cce014f61883`  
		Last Modified: Wed, 21 Feb 2024 00:00:36 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28.5-alpine`

```console
$ docker pull telegraf@sha256:6d91203705ccf1f896a9f4cac75b428cf39995a2f33365addf441f05f5db43c1
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
$ docker pull telegraf@sha256:34a1bc8756c13764ff2bf49d09c5075c2dd1fabe7dcf10ce4803851e5be207f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57595261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f23e3ce2ba33c73069b57ffe4060888a6c6c82cf6b0e797e65b00f9a382e12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:14:32 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 09:10:37 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 27 Jan 2024 09:10:48 GMT
ENV TELEGRAF_VERSION=1.28.5
# Sat, 27 Jan 2024 09:10:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 27 Jan 2024 09:10:55 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 27 Jan 2024 09:10:55 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 27 Jan 2024 09:10:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 09:10:55 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b10b365dc27fbcb456614696265123cb9aa34afefec8863e4cc7c7c90a506f5`  
		Last Modified: Sat, 27 Jan 2024 04:14:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7525fc3259afa1a7bfbf09f186ed24e031f2229e1c7c98b4eb70cf0551c6bb7`  
		Last Modified: Sat, 27 Jan 2024 09:11:24 GMT  
		Size: 2.7 MB (2673745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e607b726aaafc6a7fe5e1c80c11d0333c64a2489025dae25d530cbcbecd2001c`  
		Last Modified: Sat, 27 Jan 2024 09:11:44 GMT  
		Size: 51.6 MB (51587551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b61c9edef3f53da5024b99f28e35e828a3f526834dd7801c33c5e1ee9f6df7`  
		Last Modified: Sat, 27 Jan 2024 09:11:38 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.29`

```console
$ docker pull telegraf@sha256:2fd5f3358069034d274aa57a29c8474be5c8676efb4b85e68f92656b8371ac55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.29` - linux; amd64

```console
$ docker pull telegraf@sha256:3e706b0a8cedf798e9d74df3c832f4d824c191f1131dbe7e1909d04cfbf1b2db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155395449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8ee7cd75cb69f398bf3692221e349008a2971824ddb87f1c1c479ac9daa746`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 13:04:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 13:04:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 21 Feb 2024 01:01:25 GMT
ENV TELEGRAF_VERSION=1.29.5
# Wed, 21 Feb 2024 01:01:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 21 Feb 2024 01:01:33 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 21 Feb 2024 01:01:33 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Wed, 21 Feb 2024 01:01:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Feb 2024 01:01:33 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c71dd3592ae7480fef8cfd38fa2eb3e6694745fd687b9ced3e1602331c069f`  
		Last Modified: Tue, 13 Feb 2024 13:05:35 GMT  
		Size: 19.2 MB (19151417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9140cc5510d63237e7fcacc3cfbcb2a1338e9934d7705922cc175a91aac1416b`  
		Last Modified: Tue, 13 Feb 2024 13:05:32 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89ce8fb65aae3fd93b55ab75f9c43271c520cf9ba95758eae349dfce869c86`  
		Last Modified: Wed, 21 Feb 2024 01:02:27 GMT  
		Size: 62.6 MB (62642654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb88e6dae44ed9e41aaf13a5845bb0b6b25bf8e797daa1cd8c9f91598e249189`  
		Last Modified: Wed, 21 Feb 2024 01:02:17 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:fa26457e159021168abf90dbb9dfa25d5680049ec9b7763c5feec791f48571ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143021747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227b8072a76068cc2c6f14084e596de16753489812f40444281d2348f80cc7d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 01:19:48 GMT
ADD file:9b07e306d84beed6568160f3e02cfd7537add7bed5debf00f251fee99a50ee80 in / 
# Tue, 13 Feb 2024 01:19:49 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 17:14:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 17:14:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Feb 2024 23:57:47 GMT
ENV TELEGRAF_VERSION=1.29.5
# Tue, 20 Feb 2024 23:57:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 20 Feb 2024 23:57:56 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 20 Feb 2024 23:57:56 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Tue, 20 Feb 2024 23:57:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Feb 2024 23:57:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:84ee7bddcb1a35ae933efe6113f47b4047fb90d2a626c4a8a93e3548fa8b61d5`  
		Last Modified: Tue, 13 Feb 2024 01:26:22 GMT  
		Size: 45.2 MB (45153612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e6fa0e83f7c31cdfb8e77c4a8229243dc182cac7b985200c404bddc6e2bc9d`  
		Last Modified: Tue, 13 Feb 2024 04:26:58 GMT  
		Size: 22.0 MB (21950325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106e9dcbc36f8610a588868a2b26cfca072a98e44b65004999cb2045135307fe`  
		Last Modified: Tue, 13 Feb 2024 17:15:49 GMT  
		Size: 17.9 MB (17930146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b35263345c17ee21c6873626e4bbeb503ca2b1144bb1f0e4fe80793280e5d6a`  
		Last Modified: Tue, 13 Feb 2024 17:15:43 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a9f9f01d23827be5ef9877365c2b47f0dbec32f4f624e6f2387bc517f131a1`  
		Last Modified: Tue, 20 Feb 2024 23:58:33 GMT  
		Size: 58.0 MB (57985468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0e5af7d2cfd3b96c45b47fec5bd10b77c0136894d50ed3166362a27b2164b9`  
		Last Modified: Tue, 20 Feb 2024 23:58:23 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:54ed536a202622a895b48e851f2db633c78158b16046d6c131b5d1232bb25f46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149232743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59af7f0359edeaafdf894c3ba6c50377831f11669572000ac55246af705f634c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:48:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:48:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Feb 2024 23:59:44 GMT
ENV TELEGRAF_VERSION=1.29.5
# Tue, 20 Feb 2024 23:59:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 20 Feb 2024 23:59:51 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 20 Feb 2024 23:59:52 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Tue, 20 Feb 2024 23:59:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Feb 2024 23:59:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f707ba957ebc9b527b04c0819aa8bf91e3c23b713922f22fccfc74fbc74dbc`  
		Last Modified: Tue, 13 Feb 2024 11:48:55 GMT  
		Size: 19.1 MB (19075452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b98e47593d4c2d0e4d705e1cca72b55387a78f74f3b309b5d257f89bae5d3`  
		Last Modified: Tue, 13 Feb 2024 11:48:54 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4577f5f103558520eeea25ac0c7ffb9e50e2ef8f2335ce9dd14d056777bb7d63`  
		Last Modified: Wed, 21 Feb 2024 00:00:53 GMT  
		Size: 57.0 MB (56981362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6848b742fc81707b93888173092491bbd01e2f96f2fd3b6ab7c2f9f2101893a`  
		Last Modified: Wed, 21 Feb 2024 00:00:46 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.29-alpine`

```console
$ docker pull telegraf@sha256:bd9362d41a1f0f458953a9ab52741910d6912b6fb66a6461522fd2b296e288a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.29-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:af482c44667cb35b04d8b112201ef0e7b19681217d17bec949f9be0e17ddfe90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68479481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d671e9ee238abb8a943cb32e33ac45d8a61fe4a445f3766530ee7809bfe3249`
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
# Wed, 21 Feb 2024 01:01:37 GMT
ENV TELEGRAF_VERSION=1.29.5
# Wed, 21 Feb 2024 01:01:44 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 21 Feb 2024 01:01:45 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 21 Feb 2024 01:01:45 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Wed, 21 Feb 2024 01:01:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Feb 2024 01:01:45 GMT
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
	-	`sha256:7e811d8e3e3815f63b4fd50b30dc5295ad61234afa740cec0b8a1845ebae0500`  
		Last Modified: Wed, 21 Feb 2024 01:02:48 GMT  
		Size: 62.5 MB (62457515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8818279db78b202c9552dc700adf5e1f46b83ba0c3fa9b08148c0a53aff70015`  
		Last Modified: Wed, 21 Feb 2024 01:02:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:382b02d956bc0603bcb21ab98fbfcf5c5d560f2711e808d5d7e1b7065b984505
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62842139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c046f383fed3d7b139aa736c2e53e3bf2249ab9c343373d6c6142c8d4086a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:11:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 09:11:02 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Tue, 20 Feb 2024 23:59:54 GMT
ENV TELEGRAF_VERSION=1.29.5
# Wed, 21 Feb 2024 00:00:02 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 21 Feb 2024 00:00:03 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 21 Feb 2024 00:00:04 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Wed, 21 Feb 2024 00:00:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Feb 2024 00:00:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249c196897ea35a6f5c9da9f4bc3bffb5a6ca121c481649ba32589b229cacd53`  
		Last Modified: Sat, 27 Jan 2024 09:11:52 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ee6d9a8d80680b38cbdcf1c127883344c6c09e71f8dd4b1e6396e3343e6ebc`  
		Last Modified: Sat, 27 Jan 2024 09:11:53 GMT  
		Size: 2.7 MB (2695269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54722726c2b9c0f43f804cfc9dc5bec0fb83619f441cf11b87ddd8461df9d7e`  
		Last Modified: Wed, 21 Feb 2024 00:01:11 GMT  
		Size: 56.8 MB (56798548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f695568a8ddca75c420c530e3a2c2d6bf1701d13d140e8c63256558be4d37789`  
		Last Modified: Wed, 21 Feb 2024 00:01:04 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.29.5`

```console
$ docker pull telegraf@sha256:2fd5f3358069034d274aa57a29c8474be5c8676efb4b85e68f92656b8371ac55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.29.5` - linux; amd64

```console
$ docker pull telegraf@sha256:3e706b0a8cedf798e9d74df3c832f4d824c191f1131dbe7e1909d04cfbf1b2db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155395449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8ee7cd75cb69f398bf3692221e349008a2971824ddb87f1c1c479ac9daa746`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 13:04:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 13:04:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 21 Feb 2024 01:01:25 GMT
ENV TELEGRAF_VERSION=1.29.5
# Wed, 21 Feb 2024 01:01:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 21 Feb 2024 01:01:33 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 21 Feb 2024 01:01:33 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Wed, 21 Feb 2024 01:01:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Feb 2024 01:01:33 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c71dd3592ae7480fef8cfd38fa2eb3e6694745fd687b9ced3e1602331c069f`  
		Last Modified: Tue, 13 Feb 2024 13:05:35 GMT  
		Size: 19.2 MB (19151417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9140cc5510d63237e7fcacc3cfbcb2a1338e9934d7705922cc175a91aac1416b`  
		Last Modified: Tue, 13 Feb 2024 13:05:32 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89ce8fb65aae3fd93b55ab75f9c43271c520cf9ba95758eae349dfce869c86`  
		Last Modified: Wed, 21 Feb 2024 01:02:27 GMT  
		Size: 62.6 MB (62642654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb88e6dae44ed9e41aaf13a5845bb0b6b25bf8e797daa1cd8c9f91598e249189`  
		Last Modified: Wed, 21 Feb 2024 01:02:17 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29.5` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:fa26457e159021168abf90dbb9dfa25d5680049ec9b7763c5feec791f48571ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143021747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227b8072a76068cc2c6f14084e596de16753489812f40444281d2348f80cc7d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 01:19:48 GMT
ADD file:9b07e306d84beed6568160f3e02cfd7537add7bed5debf00f251fee99a50ee80 in / 
# Tue, 13 Feb 2024 01:19:49 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 17:14:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 17:14:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Feb 2024 23:57:47 GMT
ENV TELEGRAF_VERSION=1.29.5
# Tue, 20 Feb 2024 23:57:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 20 Feb 2024 23:57:56 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 20 Feb 2024 23:57:56 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Tue, 20 Feb 2024 23:57:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Feb 2024 23:57:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:84ee7bddcb1a35ae933efe6113f47b4047fb90d2a626c4a8a93e3548fa8b61d5`  
		Last Modified: Tue, 13 Feb 2024 01:26:22 GMT  
		Size: 45.2 MB (45153612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e6fa0e83f7c31cdfb8e77c4a8229243dc182cac7b985200c404bddc6e2bc9d`  
		Last Modified: Tue, 13 Feb 2024 04:26:58 GMT  
		Size: 22.0 MB (21950325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106e9dcbc36f8610a588868a2b26cfca072a98e44b65004999cb2045135307fe`  
		Last Modified: Tue, 13 Feb 2024 17:15:49 GMT  
		Size: 17.9 MB (17930146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b35263345c17ee21c6873626e4bbeb503ca2b1144bb1f0e4fe80793280e5d6a`  
		Last Modified: Tue, 13 Feb 2024 17:15:43 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a9f9f01d23827be5ef9877365c2b47f0dbec32f4f624e6f2387bc517f131a1`  
		Last Modified: Tue, 20 Feb 2024 23:58:33 GMT  
		Size: 58.0 MB (57985468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0e5af7d2cfd3b96c45b47fec5bd10b77c0136894d50ed3166362a27b2164b9`  
		Last Modified: Tue, 20 Feb 2024 23:58:23 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29.5` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:54ed536a202622a895b48e851f2db633c78158b16046d6c131b5d1232bb25f46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149232743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59af7f0359edeaafdf894c3ba6c50377831f11669572000ac55246af705f634c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:48:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:48:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Feb 2024 23:59:44 GMT
ENV TELEGRAF_VERSION=1.29.5
# Tue, 20 Feb 2024 23:59:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 20 Feb 2024 23:59:51 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 20 Feb 2024 23:59:52 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Tue, 20 Feb 2024 23:59:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Feb 2024 23:59:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f707ba957ebc9b527b04c0819aa8bf91e3c23b713922f22fccfc74fbc74dbc`  
		Last Modified: Tue, 13 Feb 2024 11:48:55 GMT  
		Size: 19.1 MB (19075452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b98e47593d4c2d0e4d705e1cca72b55387a78f74f3b309b5d257f89bae5d3`  
		Last Modified: Tue, 13 Feb 2024 11:48:54 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4577f5f103558520eeea25ac0c7ffb9e50e2ef8f2335ce9dd14d056777bb7d63`  
		Last Modified: Wed, 21 Feb 2024 00:00:53 GMT  
		Size: 57.0 MB (56981362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6848b742fc81707b93888173092491bbd01e2f96f2fd3b6ab7c2f9f2101893a`  
		Last Modified: Wed, 21 Feb 2024 00:00:46 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.29.5-alpine`

```console
$ docker pull telegraf@sha256:bd9362d41a1f0f458953a9ab52741910d6912b6fb66a6461522fd2b296e288a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.29.5-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:af482c44667cb35b04d8b112201ef0e7b19681217d17bec949f9be0e17ddfe90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68479481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d671e9ee238abb8a943cb32e33ac45d8a61fe4a445f3766530ee7809bfe3249`
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
# Wed, 21 Feb 2024 01:01:37 GMT
ENV TELEGRAF_VERSION=1.29.5
# Wed, 21 Feb 2024 01:01:44 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 21 Feb 2024 01:01:45 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 21 Feb 2024 01:01:45 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Wed, 21 Feb 2024 01:01:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Feb 2024 01:01:45 GMT
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
	-	`sha256:7e811d8e3e3815f63b4fd50b30dc5295ad61234afa740cec0b8a1845ebae0500`  
		Last Modified: Wed, 21 Feb 2024 01:02:48 GMT  
		Size: 62.5 MB (62457515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8818279db78b202c9552dc700adf5e1f46b83ba0c3fa9b08148c0a53aff70015`  
		Last Modified: Wed, 21 Feb 2024 01:02:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29.5-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:382b02d956bc0603bcb21ab98fbfcf5c5d560f2711e808d5d7e1b7065b984505
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62842139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c046f383fed3d7b139aa736c2e53e3bf2249ab9c343373d6c6142c8d4086a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:11:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 09:11:02 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Tue, 20 Feb 2024 23:59:54 GMT
ENV TELEGRAF_VERSION=1.29.5
# Wed, 21 Feb 2024 00:00:02 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 21 Feb 2024 00:00:03 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 21 Feb 2024 00:00:04 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Wed, 21 Feb 2024 00:00:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Feb 2024 00:00:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249c196897ea35a6f5c9da9f4bc3bffb5a6ca121c481649ba32589b229cacd53`  
		Last Modified: Sat, 27 Jan 2024 09:11:52 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ee6d9a8d80680b38cbdcf1c127883344c6c09e71f8dd4b1e6396e3343e6ebc`  
		Last Modified: Sat, 27 Jan 2024 09:11:53 GMT  
		Size: 2.7 MB (2695269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54722726c2b9c0f43f804cfc9dc5bec0fb83619f441cf11b87ddd8461df9d7e`  
		Last Modified: Wed, 21 Feb 2024 00:01:11 GMT  
		Size: 56.8 MB (56798548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f695568a8ddca75c420c530e3a2c2d6bf1701d13d140e8c63256558be4d37789`  
		Last Modified: Wed, 21 Feb 2024 00:01:04 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:bd9362d41a1f0f458953a9ab52741910d6912b6fb66a6461522fd2b296e288a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:af482c44667cb35b04d8b112201ef0e7b19681217d17bec949f9be0e17ddfe90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68479481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d671e9ee238abb8a943cb32e33ac45d8a61fe4a445f3766530ee7809bfe3249`
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
# Wed, 21 Feb 2024 01:01:37 GMT
ENV TELEGRAF_VERSION=1.29.5
# Wed, 21 Feb 2024 01:01:44 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 21 Feb 2024 01:01:45 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 21 Feb 2024 01:01:45 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Wed, 21 Feb 2024 01:01:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Feb 2024 01:01:45 GMT
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
	-	`sha256:7e811d8e3e3815f63b4fd50b30dc5295ad61234afa740cec0b8a1845ebae0500`  
		Last Modified: Wed, 21 Feb 2024 01:02:48 GMT  
		Size: 62.5 MB (62457515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8818279db78b202c9552dc700adf5e1f46b83ba0c3fa9b08148c0a53aff70015`  
		Last Modified: Wed, 21 Feb 2024 01:02:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:382b02d956bc0603bcb21ab98fbfcf5c5d560f2711e808d5d7e1b7065b984505
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62842139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c046f383fed3d7b139aa736c2e53e3bf2249ab9c343373d6c6142c8d4086a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:11:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 09:11:02 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Tue, 20 Feb 2024 23:59:54 GMT
ENV TELEGRAF_VERSION=1.29.5
# Wed, 21 Feb 2024 00:00:02 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 21 Feb 2024 00:00:03 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 21 Feb 2024 00:00:04 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Wed, 21 Feb 2024 00:00:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Feb 2024 00:00:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249c196897ea35a6f5c9da9f4bc3bffb5a6ca121c481649ba32589b229cacd53`  
		Last Modified: Sat, 27 Jan 2024 09:11:52 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ee6d9a8d80680b38cbdcf1c127883344c6c09e71f8dd4b1e6396e3343e6ebc`  
		Last Modified: Sat, 27 Jan 2024 09:11:53 GMT  
		Size: 2.7 MB (2695269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54722726c2b9c0f43f804cfc9dc5bec0fb83619f441cf11b87ddd8461df9d7e`  
		Last Modified: Wed, 21 Feb 2024 00:01:11 GMT  
		Size: 56.8 MB (56798548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f695568a8ddca75c420c530e3a2c2d6bf1701d13d140e8c63256558be4d37789`  
		Last Modified: Wed, 21 Feb 2024 00:01:04 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:2fd5f3358069034d274aa57a29c8474be5c8676efb4b85e68f92656b8371ac55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:3e706b0a8cedf798e9d74df3c832f4d824c191f1131dbe7e1909d04cfbf1b2db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155395449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8ee7cd75cb69f398bf3692221e349008a2971824ddb87f1c1c479ac9daa746`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 13:04:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 13:04:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 21 Feb 2024 01:01:25 GMT
ENV TELEGRAF_VERSION=1.29.5
# Wed, 21 Feb 2024 01:01:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 21 Feb 2024 01:01:33 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 21 Feb 2024 01:01:33 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Wed, 21 Feb 2024 01:01:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Feb 2024 01:01:33 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c71dd3592ae7480fef8cfd38fa2eb3e6694745fd687b9ced3e1602331c069f`  
		Last Modified: Tue, 13 Feb 2024 13:05:35 GMT  
		Size: 19.2 MB (19151417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9140cc5510d63237e7fcacc3cfbcb2a1338e9934d7705922cc175a91aac1416b`  
		Last Modified: Tue, 13 Feb 2024 13:05:32 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89ce8fb65aae3fd93b55ab75f9c43271c520cf9ba95758eae349dfce869c86`  
		Last Modified: Wed, 21 Feb 2024 01:02:27 GMT  
		Size: 62.6 MB (62642654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb88e6dae44ed9e41aaf13a5845bb0b6b25bf8e797daa1cd8c9f91598e249189`  
		Last Modified: Wed, 21 Feb 2024 01:02:17 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:fa26457e159021168abf90dbb9dfa25d5680049ec9b7763c5feec791f48571ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143021747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227b8072a76068cc2c6f14084e596de16753489812f40444281d2348f80cc7d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 01:19:48 GMT
ADD file:9b07e306d84beed6568160f3e02cfd7537add7bed5debf00f251fee99a50ee80 in / 
# Tue, 13 Feb 2024 01:19:49 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 17:14:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 17:14:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Feb 2024 23:57:47 GMT
ENV TELEGRAF_VERSION=1.29.5
# Tue, 20 Feb 2024 23:57:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 20 Feb 2024 23:57:56 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 20 Feb 2024 23:57:56 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Tue, 20 Feb 2024 23:57:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Feb 2024 23:57:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:84ee7bddcb1a35ae933efe6113f47b4047fb90d2a626c4a8a93e3548fa8b61d5`  
		Last Modified: Tue, 13 Feb 2024 01:26:22 GMT  
		Size: 45.2 MB (45153612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e6fa0e83f7c31cdfb8e77c4a8229243dc182cac7b985200c404bddc6e2bc9d`  
		Last Modified: Tue, 13 Feb 2024 04:26:58 GMT  
		Size: 22.0 MB (21950325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106e9dcbc36f8610a588868a2b26cfca072a98e44b65004999cb2045135307fe`  
		Last Modified: Tue, 13 Feb 2024 17:15:49 GMT  
		Size: 17.9 MB (17930146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b35263345c17ee21c6873626e4bbeb503ca2b1144bb1f0e4fe80793280e5d6a`  
		Last Modified: Tue, 13 Feb 2024 17:15:43 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a9f9f01d23827be5ef9877365c2b47f0dbec32f4f624e6f2387bc517f131a1`  
		Last Modified: Tue, 20 Feb 2024 23:58:33 GMT  
		Size: 58.0 MB (57985468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0e5af7d2cfd3b96c45b47fec5bd10b77c0136894d50ed3166362a27b2164b9`  
		Last Modified: Tue, 20 Feb 2024 23:58:23 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:54ed536a202622a895b48e851f2db633c78158b16046d6c131b5d1232bb25f46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149232743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59af7f0359edeaafdf894c3ba6c50377831f11669572000ac55246af705f634c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:48:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:48:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Feb 2024 23:59:44 GMT
ENV TELEGRAF_VERSION=1.29.5
# Tue, 20 Feb 2024 23:59:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 20 Feb 2024 23:59:51 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 20 Feb 2024 23:59:52 GMT
COPY file:6eb4fc66e5cdfa4523c9e77df0aa1dcdbdacec6af2b86aafe777a8ad509e3ff8 in /entrypoint.sh 
# Tue, 20 Feb 2024 23:59:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Feb 2024 23:59:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f707ba957ebc9b527b04c0819aa8bf91e3c23b713922f22fccfc74fbc74dbc`  
		Last Modified: Tue, 13 Feb 2024 11:48:55 GMT  
		Size: 19.1 MB (19075452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b98e47593d4c2d0e4d705e1cca72b55387a78f74f3b309b5d257f89bae5d3`  
		Last Modified: Tue, 13 Feb 2024 11:48:54 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4577f5f103558520eeea25ac0c7ffb9e50e2ef8f2335ce9dd14d056777bb7d63`  
		Last Modified: Wed, 21 Feb 2024 00:00:53 GMT  
		Size: 57.0 MB (56981362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6848b742fc81707b93888173092491bbd01e2f96f2fd3b6ab7c2f9f2101893a`  
		Last Modified: Wed, 21 Feb 2024 00:00:46 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
