<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `influxdb`

-	[`influxdb:1.7`](#influxdb17)
-	[`influxdb:1.7.10`](#influxdb1710)
-	[`influxdb:1.7.10-alpine`](#influxdb1710-alpine)
-	[`influxdb:1.7.10-data`](#influxdb1710-data)
-	[`influxdb:1.7.10-data-alpine`](#influxdb1710-data-alpine)
-	[`influxdb:1.7.10-meta`](#influxdb1710-meta)
-	[`influxdb:1.7.10-meta-alpine`](#influxdb1710-meta-alpine)
-	[`influxdb:1.7-alpine`](#influxdb17-alpine)
-	[`influxdb:1.7-data`](#influxdb17-data)
-	[`influxdb:1.7-data-alpine`](#influxdb17-data-alpine)
-	[`influxdb:1.7-meta`](#influxdb17-meta)
-	[`influxdb:1.7-meta-alpine`](#influxdb17-meta-alpine)
-	[`influxdb:1.8`](#influxdb18)
-	[`influxdb:1.8.3`](#influxdb183)
-	[`influxdb:1.8.3-alpine`](#influxdb183-alpine)
-	[`influxdb:1.8.3-data`](#influxdb183-data)
-	[`influxdb:1.8.3-data-alpine`](#influxdb183-data-alpine)
-	[`influxdb:1.8.3-meta`](#influxdb183-meta)
-	[`influxdb:1.8.3-meta-alpine`](#influxdb183-meta-alpine)
-	[`influxdb:1.8-alpine`](#influxdb18-alpine)
-	[`influxdb:1.8-data`](#influxdb18-data)
-	[`influxdb:1.8-data-alpine`](#influxdb18-data-alpine)
-	[`influxdb:1.8-meta`](#influxdb18-meta)
-	[`influxdb:1.8-meta-alpine`](#influxdb18-meta-alpine)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:data`](#influxdbdata)
-	[`influxdb:data-alpine`](#influxdbdata-alpine)
-	[`influxdb:latest`](#influxdblatest)
-	[`influxdb:meta`](#influxdbmeta)
-	[`influxdb:meta-alpine`](#influxdbmeta-alpine)

## `influxdb:1.7`

```console
$ docker pull influxdb@sha256:481709b32cca5001a6d03022b3a11e152fd4faa3038e5c0b92bb6de59dbbd868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7` - linux; amd64

```console
$ docker pull influxdb@sha256:9528d0edc8376afac61a3fcdb47a30fc330d3db4dd93c07b8dfb5fa581af2c8e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124559925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4847a02aa97bd6cd5abe05edb6d456a6668c2af75c2f93106c4bfa55cacb6dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:23:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 23:23:15 GMT
ENV INFLUXDB_VERSION=1.7.10
# Tue, 13 Oct 2020 23:23:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 13 Oct 2020 23:23:24 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 13 Oct 2020 23:23:24 GMT
EXPOSE 8086
# Tue, 13 Oct 2020 23:23:24 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Oct 2020 23:23:24 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 13 Oct 2020 23:23:25 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Oct 2020 23:23:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 23:23:25 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8559aa5ebb59d52475c0142459015fb9be267e1a497d8664f3fc8a35445173`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 10.8 MB (10751068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32bfbbc3bad880f731e2f37903c9e359e180a5e74a703293a9441260cf3551`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 4.3 MB (4340586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2107148596b1d475384d38442e52f5aee3e9ab070498ad61d7ae6fde1b136793`  
		Last Modified: Tue, 13 Oct 2020 23:25:21 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1023ead1ba8bc4990854d90d2975b90840d82c3ffee7edc7cb4559698fa615f0`  
		Last Modified: Tue, 13 Oct 2020 23:25:32 GMT  
		Size: 64.1 MB (64096951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7ed721dfe8f88157ab5d22ce022239f72540b01a4cf780f66f69b3c951d318`  
		Last Modified: Tue, 13 Oct 2020 23:25:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a6b9fcb73acca81cce16e43d168ec87e3b4a2aa54994f3d20ed01e0e3c0f65`  
		Last Modified: Tue, 13 Oct 2020 23:25:21 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957523d8a7eb7fc38a615d154527125745e23df9cadf90b8d0f3dc94b8a5f955`  
		Last Modified: Tue, 13 Oct 2020 23:25:21 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:e725b94dc6d57c7c9535dd0072b1c7264eb74ab28bd65f9351fc41d99ca2c350
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116115179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ef11492c1bc2e2cbed5beccd6c8ab86548a8450ae3ccbf5c860502005ed658`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Oct 2020 01:04:04 GMT
ADD file:fb1dab6b0ac08f52870fca9435eedd2f707a3b8a5d28e5d1c2ff88e096f695ec in / 
# Tue, 13 Oct 2020 01:04:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:47:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 01:48:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 21:40:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 21:41:01 GMT
ENV INFLUXDB_VERSION=1.7.10
# Tue, 13 Oct 2020 21:41:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 13 Oct 2020 21:42:17 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 13 Oct 2020 21:42:29 GMT
EXPOSE 8086
# Tue, 13 Oct 2020 21:42:38 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Oct 2020 21:42:56 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 13 Oct 2020 21:43:14 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Oct 2020 21:43:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 21:43:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1b636fdf37230c276ff1507a9f2b0067182f369cd669d1852bf5b9f5ba3a43bf`  
		Last Modified: Tue, 13 Oct 2020 01:12:25 GMT  
		Size: 42.1 MB (42111286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be3bc01c2e26b6c110cf55ed7833949511463f13387c8e708aec5a5c076fd83`  
		Last Modified: Tue, 13 Oct 2020 02:00:39 GMT  
		Size: 9.4 MB (9443957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1b23b3e38f06003a13d520ed3ec7eee0eafb5efe4a72d5508b3c2b2a7e3393`  
		Last Modified: Tue, 13 Oct 2020 02:00:37 GMT  
		Size: 3.9 MB (3919858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb874e260368d0b929e2dc1424843a22bfb4638e7a33c29465a3e302861bea9`  
		Last Modified: Tue, 13 Oct 2020 21:46:53 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e4058f9c04349cf276590988ddbf52ed2352705e36d50499d10dff7a1ba669`  
		Last Modified: Tue, 13 Oct 2020 21:47:08 GMT  
		Size: 60.6 MB (60635510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd17ac8c4dda0b25b2fc7ddd6d936626d4152eb07e62ff409c322fa472a23c61`  
		Last Modified: Tue, 13 Oct 2020 21:46:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f2c20aa2e94e3d5ad835fd5c3429605ada75e0ca7b7f3e27347238134a42c4`  
		Last Modified: Tue, 13 Oct 2020 21:46:53 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf0e3a6aefa482ebe761205beb51e4444ea7b884a4a3c3d1b4a07d51f1d267d`  
		Last Modified: Tue, 13 Oct 2020 21:46:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:40cc00db8c752687737fe56e8822818ffdb971047d0759c792ee4bb196daa6f4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117100322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349127fdf56db524b01e41c7d61af7bf4313e4ead5a551ba009b32995a87cd2c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Oct 2020 01:43:49 GMT
ADD file:2752d391988f4ad7e086be863c36a83a3226e31e44ea816ca4c89d6a410727b1 in / 
# Tue, 13 Oct 2020 01:43:51 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:40:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:40:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 14 Oct 2020 00:42:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 14 Oct 2020 00:42:19 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 14 Oct 2020 00:42:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 14 Oct 2020 00:42:32 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 14 Oct 2020 00:42:33 GMT
EXPOSE 8086
# Wed, 14 Oct 2020 00:42:34 GMT
VOLUME [/var/lib/influxdb]
# Wed, 14 Oct 2020 00:42:35 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 14 Oct 2020 00:42:36 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 14 Oct 2020 00:42:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Oct 2020 00:42:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:19e4d0e7f8f2c5cb8a0a8d0e741e9e387c34bd673da69cdcc8e758a5c4dbc106`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 43.2 MB (43171543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b66c8297162aeeca035e2cf9e752a4f0e5b411d1c90d7314aba56e52741b6cf`  
		Last Modified: Tue, 13 Oct 2020 02:50:51 GMT  
		Size: 9.7 MB (9701174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558b5390d6e12ba26207e779d409c31a61c54713a327bb04565a18f2432bb25d`  
		Last Modified: Tue, 13 Oct 2020 02:50:50 GMT  
		Size: 4.1 MB (4095275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fa64acfa2daa89a185c25af4ca9c3567e8f967ad4a9658356d2f87c180554a`  
		Last Modified: Wed, 14 Oct 2020 00:43:12 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef53185202787c0c9e31fd5e4db328f5dcd4be177023754ba4bcaad44731519b`  
		Last Modified: Wed, 14 Oct 2020 00:43:27 GMT  
		Size: 60.1 MB (60127754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bd3fd493b3afbfa9d379fd55bb6211cfde6d941349bbcc5e7e2e9b410a9c1f`  
		Last Modified: Wed, 14 Oct 2020 00:43:12 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5386856533d5dfa1fe945be41009fe094d8e44f28cd2155e8c129b6b20bb9d8f`  
		Last Modified: Wed, 14 Oct 2020 00:43:12 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ecb10e8c8a64645407d7420d12234e6e7d28f030ebc0864d923a78821b9723`  
		Last Modified: Wed, 14 Oct 2020 00:43:12 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10`

```console
$ docker pull influxdb@sha256:481709b32cca5001a6d03022b3a11e152fd4faa3038e5c0b92bb6de59dbbd868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7.10` - linux; amd64

```console
$ docker pull influxdb@sha256:9528d0edc8376afac61a3fcdb47a30fc330d3db4dd93c07b8dfb5fa581af2c8e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124559925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4847a02aa97bd6cd5abe05edb6d456a6668c2af75c2f93106c4bfa55cacb6dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:23:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 23:23:15 GMT
ENV INFLUXDB_VERSION=1.7.10
# Tue, 13 Oct 2020 23:23:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 13 Oct 2020 23:23:24 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 13 Oct 2020 23:23:24 GMT
EXPOSE 8086
# Tue, 13 Oct 2020 23:23:24 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Oct 2020 23:23:24 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 13 Oct 2020 23:23:25 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Oct 2020 23:23:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 23:23:25 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8559aa5ebb59d52475c0142459015fb9be267e1a497d8664f3fc8a35445173`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 10.8 MB (10751068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32bfbbc3bad880f731e2f37903c9e359e180a5e74a703293a9441260cf3551`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 4.3 MB (4340586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2107148596b1d475384d38442e52f5aee3e9ab070498ad61d7ae6fde1b136793`  
		Last Modified: Tue, 13 Oct 2020 23:25:21 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1023ead1ba8bc4990854d90d2975b90840d82c3ffee7edc7cb4559698fa615f0`  
		Last Modified: Tue, 13 Oct 2020 23:25:32 GMT  
		Size: 64.1 MB (64096951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7ed721dfe8f88157ab5d22ce022239f72540b01a4cf780f66f69b3c951d318`  
		Last Modified: Tue, 13 Oct 2020 23:25:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a6b9fcb73acca81cce16e43d168ec87e3b4a2aa54994f3d20ed01e0e3c0f65`  
		Last Modified: Tue, 13 Oct 2020 23:25:21 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957523d8a7eb7fc38a615d154527125745e23df9cadf90b8d0f3dc94b8a5f955`  
		Last Modified: Tue, 13 Oct 2020 23:25:21 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:e725b94dc6d57c7c9535dd0072b1c7264eb74ab28bd65f9351fc41d99ca2c350
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116115179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ef11492c1bc2e2cbed5beccd6c8ab86548a8450ae3ccbf5c860502005ed658`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Oct 2020 01:04:04 GMT
ADD file:fb1dab6b0ac08f52870fca9435eedd2f707a3b8a5d28e5d1c2ff88e096f695ec in / 
# Tue, 13 Oct 2020 01:04:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:47:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 01:48:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 21:40:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 21:41:01 GMT
ENV INFLUXDB_VERSION=1.7.10
# Tue, 13 Oct 2020 21:41:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 13 Oct 2020 21:42:17 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 13 Oct 2020 21:42:29 GMT
EXPOSE 8086
# Tue, 13 Oct 2020 21:42:38 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Oct 2020 21:42:56 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 13 Oct 2020 21:43:14 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Oct 2020 21:43:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 21:43:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1b636fdf37230c276ff1507a9f2b0067182f369cd669d1852bf5b9f5ba3a43bf`  
		Last Modified: Tue, 13 Oct 2020 01:12:25 GMT  
		Size: 42.1 MB (42111286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be3bc01c2e26b6c110cf55ed7833949511463f13387c8e708aec5a5c076fd83`  
		Last Modified: Tue, 13 Oct 2020 02:00:39 GMT  
		Size: 9.4 MB (9443957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1b23b3e38f06003a13d520ed3ec7eee0eafb5efe4a72d5508b3c2b2a7e3393`  
		Last Modified: Tue, 13 Oct 2020 02:00:37 GMT  
		Size: 3.9 MB (3919858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb874e260368d0b929e2dc1424843a22bfb4638e7a33c29465a3e302861bea9`  
		Last Modified: Tue, 13 Oct 2020 21:46:53 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e4058f9c04349cf276590988ddbf52ed2352705e36d50499d10dff7a1ba669`  
		Last Modified: Tue, 13 Oct 2020 21:47:08 GMT  
		Size: 60.6 MB (60635510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd17ac8c4dda0b25b2fc7ddd6d936626d4152eb07e62ff409c322fa472a23c61`  
		Last Modified: Tue, 13 Oct 2020 21:46:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f2c20aa2e94e3d5ad835fd5c3429605ada75e0ca7b7f3e27347238134a42c4`  
		Last Modified: Tue, 13 Oct 2020 21:46:53 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf0e3a6aefa482ebe761205beb51e4444ea7b884a4a3c3d1b4a07d51f1d267d`  
		Last Modified: Tue, 13 Oct 2020 21:46:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:40cc00db8c752687737fe56e8822818ffdb971047d0759c792ee4bb196daa6f4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117100322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349127fdf56db524b01e41c7d61af7bf4313e4ead5a551ba009b32995a87cd2c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Oct 2020 01:43:49 GMT
ADD file:2752d391988f4ad7e086be863c36a83a3226e31e44ea816ca4c89d6a410727b1 in / 
# Tue, 13 Oct 2020 01:43:51 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:40:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:40:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 14 Oct 2020 00:42:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 14 Oct 2020 00:42:19 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 14 Oct 2020 00:42:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 14 Oct 2020 00:42:32 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 14 Oct 2020 00:42:33 GMT
EXPOSE 8086
# Wed, 14 Oct 2020 00:42:34 GMT
VOLUME [/var/lib/influxdb]
# Wed, 14 Oct 2020 00:42:35 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 14 Oct 2020 00:42:36 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 14 Oct 2020 00:42:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Oct 2020 00:42:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:19e4d0e7f8f2c5cb8a0a8d0e741e9e387c34bd673da69cdcc8e758a5c4dbc106`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 43.2 MB (43171543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b66c8297162aeeca035e2cf9e752a4f0e5b411d1c90d7314aba56e52741b6cf`  
		Last Modified: Tue, 13 Oct 2020 02:50:51 GMT  
		Size: 9.7 MB (9701174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558b5390d6e12ba26207e779d409c31a61c54713a327bb04565a18f2432bb25d`  
		Last Modified: Tue, 13 Oct 2020 02:50:50 GMT  
		Size: 4.1 MB (4095275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fa64acfa2daa89a185c25af4ca9c3567e8f967ad4a9658356d2f87c180554a`  
		Last Modified: Wed, 14 Oct 2020 00:43:12 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef53185202787c0c9e31fd5e4db328f5dcd4be177023754ba4bcaad44731519b`  
		Last Modified: Wed, 14 Oct 2020 00:43:27 GMT  
		Size: 60.1 MB (60127754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bd3fd493b3afbfa9d379fd55bb6211cfde6d941349bbcc5e7e2e9b410a9c1f`  
		Last Modified: Wed, 14 Oct 2020 00:43:12 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5386856533d5dfa1fe945be41009fe094d8e44f28cd2155e8c129b6b20bb9d8f`  
		Last Modified: Wed, 14 Oct 2020 00:43:12 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ecb10e8c8a64645407d7420d12234e6e7d28f030ebc0864d923a78821b9723`  
		Last Modified: Wed, 14 Oct 2020 00:43:12 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-alpine`

```console
$ docker pull influxdb@sha256:9c65e7bf946ddc2a627e50201e385ead0631f95cb080c6b36aadbe636c602802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:9fbf261a26a34a469631767ca8264ee0de84228f14934baffe404d44db761729
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68067483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7be02aaf243e5281c1833da3bac8a49205220413cf3f7bea1463259ac0abcd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:58:25 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 01 Sep 2020 00:58:25 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 02 Sep 2020 00:11:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 02 Sep 2020 00:11:44 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 02 Sep 2020 00:11:44 GMT
EXPOSE 8086
# Wed, 02 Sep 2020 00:11:45 GMT
VOLUME [/var/lib/influxdb]
# Wed, 02 Sep 2020 00:11:45 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 02 Sep 2020 00:11:45 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 02 Sep 2020 00:11:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Sep 2020 00:11:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7279b9f70b385667a52ff20142c09fd4fe94f3c717683fe273d3af53528ada`  
		Last Modified: Tue, 01 Sep 2020 01:01:22 GMT  
		Size: 1.4 MB (1427184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9023e716c8a4c5d917ba76a2e97b02719b195d01082d3c2ead8b84eecf1abe9`  
		Last Modified: Wed, 02 Sep 2020 00:14:00 GMT  
		Size: 63.8 MB (63840890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92913e1dce15864d871000ff0248a79ea63aa9b42b3ad53f5b03c78956fc3710`  
		Last Modified: Wed, 02 Sep 2020 00:13:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16f9e04304e1949c2639cb2d4a6cd228209aaa2b7defc3ad0246a8d68ecdd4c`  
		Last Modified: Wed, 02 Sep 2020 00:13:51 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05a057cd8848b21c64c7338ee4ecce50673c9de07ec50e49edd1da24e49627b`  
		Last Modified: Wed, 02 Sep 2020 00:13:50 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-data`

```console
$ docker pull influxdb@sha256:e7cb137708d17aae6b8077b6188d4c5303fcfcdc2d86ae591f6351efedf16326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:59b79eb93d8b91cc1338db149abd08d3266da7d452ff8312f2d74bb51102ca97
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148375342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af69a565dc6e3f5da575a8945f56c8d22bf68226b0b64f2a6a2225e6e9efdb43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:23:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 23:23:34 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Tue, 13 Oct 2020 23:23:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Tue, 13 Oct 2020 23:23:45 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 13 Oct 2020 23:23:45 GMT
EXPOSE 8086
# Tue, 13 Oct 2020 23:23:45 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Oct 2020 23:23:46 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 13 Oct 2020 23:23:46 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Oct 2020 23:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 23:23:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8559aa5ebb59d52475c0142459015fb9be267e1a497d8664f3fc8a35445173`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 10.8 MB (10751068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32bfbbc3bad880f731e2f37903c9e359e180a5e74a703293a9441260cf3551`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 4.3 MB (4340586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2107148596b1d475384d38442e52f5aee3e9ab070498ad61d7ae6fde1b136793`  
		Last Modified: Tue, 13 Oct 2020 23:25:21 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e81b574818d67b816c571e0c9e2dff41a1cc2d0ce05aa601e1f091b34e97a4`  
		Last Modified: Tue, 13 Oct 2020 23:26:14 GMT  
		Size: 87.9 MB (87912310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f80967cb2ff583960abcb9b9a3bff69993c4b80707fcb0678ca326c59c5230`  
		Last Modified: Tue, 13 Oct 2020 23:25:59 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee7464ca939335def1fa3b300e13d14e39d6aa610757b71846fed3dabe6514e`  
		Last Modified: Tue, 13 Oct 2020 23:25:59 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74908c1f8cdaf665939940a23ba6be1cab31b573b94344801e6dd8f3a4ac1ea2`  
		Last Modified: Tue, 13 Oct 2020 23:25:59 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-data-alpine`

```console
$ docker pull influxdb@sha256:5431b628835fdf7987a4a2d407c4591b16613f03967c5c54008850a4768d2c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5b8b7162256351382fbb7ece4db132eb47721ea99b7280a5f97671270fc9ac02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91830740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ead97b0073c7307f1b8d5b2660d65c129140a0a0c1c66b7927d4d08e97895f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:58:25 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 01 Sep 2020 00:58:41 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 02 Sep 2020 00:12:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 02 Sep 2020 00:12:12 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 02 Sep 2020 00:12:12 GMT
EXPOSE 8086
# Wed, 02 Sep 2020 00:12:13 GMT
VOLUME [/var/lib/influxdb]
# Wed, 02 Sep 2020 00:12:13 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 02 Sep 2020 00:12:13 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 02 Sep 2020 00:12:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Sep 2020 00:12:13 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7279b9f70b385667a52ff20142c09fd4fe94f3c717683fe273d3af53528ada`  
		Last Modified: Tue, 01 Sep 2020 01:01:22 GMT  
		Size: 1.4 MB (1427184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69cc6b83e5605951bf483536e45fd29fa2f129c438b27a792f30dfbc5f7ebeb8`  
		Last Modified: Wed, 02 Sep 2020 00:14:35 GMT  
		Size: 87.6 MB (87604090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b03a6b82a698bc8f2db18e933750c58085cc252740c4d5f82bb852df790cba3`  
		Last Modified: Wed, 02 Sep 2020 00:14:22 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7185a2356ab4745253c91a431f6bb343ff44088060bbff830cdc9efbedddd879`  
		Last Modified: Wed, 02 Sep 2020 00:14:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d479801efe2743cdae9a377a8f9b294c6f0f956f10a08c6da1f74d71d6d69cf`  
		Last Modified: Wed, 02 Sep 2020 00:14:22 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-meta`

```console
$ docker pull influxdb@sha256:1dfde1c7d4959453bb12818cbe81194403f9f27c85a9b6a753b9a9aeabb1001e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:a665256ae495d71dae29a3f0103713928da6e1b9db7f81eb97f12c193127d1e3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83594492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd83a5ec4004b99fb778ecb90345ea5d48a19d947780428d36c16d50904f0d3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:23:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 23:23:34 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Tue, 13 Oct 2020 23:23:58 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Tue, 13 Oct 2020 23:23:58 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 13 Oct 2020 23:23:58 GMT
EXPOSE 8091
# Tue, 13 Oct 2020 23:23:59 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Oct 2020 23:23:59 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 13 Oct 2020 23:23:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 23:23:59 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8559aa5ebb59d52475c0142459015fb9be267e1a497d8664f3fc8a35445173`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 10.8 MB (10751068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32bfbbc3bad880f731e2f37903c9e359e180a5e74a703293a9441260cf3551`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 4.3 MB (4340586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2107148596b1d475384d38442e52f5aee3e9ab070498ad61d7ae6fde1b136793`  
		Last Modified: Tue, 13 Oct 2020 23:25:21 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261235e55734407be4a1196fc171fba46c097fa6ec481c30603821d8b3e70e3f`  
		Last Modified: Tue, 13 Oct 2020 23:26:26 GMT  
		Size: 23.1 MB (23132663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ae0993153169c462e604ad5b13d113d9637424d878289ccc19172f5473a1ce`  
		Last Modified: Tue, 13 Oct 2020 23:26:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e5fdf301b3895d14ed1da7b20133cd8004f58a8e871d10131953d66847ecc1`  
		Last Modified: Tue, 13 Oct 2020 23:26:22 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-meta-alpine`

```console
$ docker pull influxdb@sha256:abd6a0c5e71d742cd66274f5b0d6d95cc3eed64d4f83238ce3c616a795d36240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:c59e639516bdde5c0f1aa33a144117d8984775cafa6d9e57b00ce9b2ba47a2fb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27228222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbff5e0053b6fd6fb76731aa0897a46ddce122de9ab89771f5acbadf586c373f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:58:25 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 01 Sep 2020 00:58:41 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 02 Sep 2020 00:12:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 02 Sep 2020 00:12:30 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 02 Sep 2020 00:12:30 GMT
EXPOSE 8091
# Wed, 02 Sep 2020 00:12:31 GMT
VOLUME [/var/lib/influxdb]
# Wed, 02 Sep 2020 00:12:31 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 02 Sep 2020 00:12:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Sep 2020 00:12:31 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7279b9f70b385667a52ff20142c09fd4fe94f3c717683fe273d3af53528ada`  
		Last Modified: Tue, 01 Sep 2020 01:01:22 GMT  
		Size: 1.4 MB (1427184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e926a4ac2f6d229659017939bcd27c30a101cef5a8b6b8c89b54a13f355e616`  
		Last Modified: Wed, 02 Sep 2020 00:14:49 GMT  
		Size: 23.0 MB (23002776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:035a9b83b307a36d60c4477f29cc9ce7340803852e96e904bc2d08c8b5a94539`  
		Last Modified: Wed, 02 Sep 2020 00:14:45 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878762750ff031c08c7c13438015dd9e46b2cf8fc464bbefc21a493ca46f8559`  
		Last Modified: Wed, 02 Sep 2020 00:14:45 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-alpine`

```console
$ docker pull influxdb@sha256:9c65e7bf946ddc2a627e50201e385ead0631f95cb080c6b36aadbe636c602802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:9fbf261a26a34a469631767ca8264ee0de84228f14934baffe404d44db761729
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68067483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7be02aaf243e5281c1833da3bac8a49205220413cf3f7bea1463259ac0abcd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:58:25 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 01 Sep 2020 00:58:25 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 02 Sep 2020 00:11:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 02 Sep 2020 00:11:44 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 02 Sep 2020 00:11:44 GMT
EXPOSE 8086
# Wed, 02 Sep 2020 00:11:45 GMT
VOLUME [/var/lib/influxdb]
# Wed, 02 Sep 2020 00:11:45 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 02 Sep 2020 00:11:45 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 02 Sep 2020 00:11:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Sep 2020 00:11:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7279b9f70b385667a52ff20142c09fd4fe94f3c717683fe273d3af53528ada`  
		Last Modified: Tue, 01 Sep 2020 01:01:22 GMT  
		Size: 1.4 MB (1427184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9023e716c8a4c5d917ba76a2e97b02719b195d01082d3c2ead8b84eecf1abe9`  
		Last Modified: Wed, 02 Sep 2020 00:14:00 GMT  
		Size: 63.8 MB (63840890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92913e1dce15864d871000ff0248a79ea63aa9b42b3ad53f5b03c78956fc3710`  
		Last Modified: Wed, 02 Sep 2020 00:13:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16f9e04304e1949c2639cb2d4a6cd228209aaa2b7defc3ad0246a8d68ecdd4c`  
		Last Modified: Wed, 02 Sep 2020 00:13:51 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05a057cd8848b21c64c7338ee4ecce50673c9de07ec50e49edd1da24e49627b`  
		Last Modified: Wed, 02 Sep 2020 00:13:50 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-data`

```console
$ docker pull influxdb@sha256:e7cb137708d17aae6b8077b6188d4c5303fcfcdc2d86ae591f6351efedf16326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:59b79eb93d8b91cc1338db149abd08d3266da7d452ff8312f2d74bb51102ca97
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148375342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af69a565dc6e3f5da575a8945f56c8d22bf68226b0b64f2a6a2225e6e9efdb43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:23:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 23:23:34 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Tue, 13 Oct 2020 23:23:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Tue, 13 Oct 2020 23:23:45 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 13 Oct 2020 23:23:45 GMT
EXPOSE 8086
# Tue, 13 Oct 2020 23:23:45 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Oct 2020 23:23:46 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 13 Oct 2020 23:23:46 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Oct 2020 23:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 23:23:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8559aa5ebb59d52475c0142459015fb9be267e1a497d8664f3fc8a35445173`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 10.8 MB (10751068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32bfbbc3bad880f731e2f37903c9e359e180a5e74a703293a9441260cf3551`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 4.3 MB (4340586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2107148596b1d475384d38442e52f5aee3e9ab070498ad61d7ae6fde1b136793`  
		Last Modified: Tue, 13 Oct 2020 23:25:21 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e81b574818d67b816c571e0c9e2dff41a1cc2d0ce05aa601e1f091b34e97a4`  
		Last Modified: Tue, 13 Oct 2020 23:26:14 GMT  
		Size: 87.9 MB (87912310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f80967cb2ff583960abcb9b9a3bff69993c4b80707fcb0678ca326c59c5230`  
		Last Modified: Tue, 13 Oct 2020 23:25:59 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee7464ca939335def1fa3b300e13d14e39d6aa610757b71846fed3dabe6514e`  
		Last Modified: Tue, 13 Oct 2020 23:25:59 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74908c1f8cdaf665939940a23ba6be1cab31b573b94344801e6dd8f3a4ac1ea2`  
		Last Modified: Tue, 13 Oct 2020 23:25:59 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-data-alpine`

```console
$ docker pull influxdb@sha256:5431b628835fdf7987a4a2d407c4591b16613f03967c5c54008850a4768d2c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5b8b7162256351382fbb7ece4db132eb47721ea99b7280a5f97671270fc9ac02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91830740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ead97b0073c7307f1b8d5b2660d65c129140a0a0c1c66b7927d4d08e97895f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:58:25 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 01 Sep 2020 00:58:41 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 02 Sep 2020 00:12:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 02 Sep 2020 00:12:12 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 02 Sep 2020 00:12:12 GMT
EXPOSE 8086
# Wed, 02 Sep 2020 00:12:13 GMT
VOLUME [/var/lib/influxdb]
# Wed, 02 Sep 2020 00:12:13 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 02 Sep 2020 00:12:13 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 02 Sep 2020 00:12:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Sep 2020 00:12:13 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7279b9f70b385667a52ff20142c09fd4fe94f3c717683fe273d3af53528ada`  
		Last Modified: Tue, 01 Sep 2020 01:01:22 GMT  
		Size: 1.4 MB (1427184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69cc6b83e5605951bf483536e45fd29fa2f129c438b27a792f30dfbc5f7ebeb8`  
		Last Modified: Wed, 02 Sep 2020 00:14:35 GMT  
		Size: 87.6 MB (87604090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b03a6b82a698bc8f2db18e933750c58085cc252740c4d5f82bb852df790cba3`  
		Last Modified: Wed, 02 Sep 2020 00:14:22 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7185a2356ab4745253c91a431f6bb343ff44088060bbff830cdc9efbedddd879`  
		Last Modified: Wed, 02 Sep 2020 00:14:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d479801efe2743cdae9a377a8f9b294c6f0f956f10a08c6da1f74d71d6d69cf`  
		Last Modified: Wed, 02 Sep 2020 00:14:22 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-meta`

```console
$ docker pull influxdb@sha256:1dfde1c7d4959453bb12818cbe81194403f9f27c85a9b6a753b9a9aeabb1001e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:a665256ae495d71dae29a3f0103713928da6e1b9db7f81eb97f12c193127d1e3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83594492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd83a5ec4004b99fb778ecb90345ea5d48a19d947780428d36c16d50904f0d3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:23:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 23:23:34 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Tue, 13 Oct 2020 23:23:58 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Tue, 13 Oct 2020 23:23:58 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 13 Oct 2020 23:23:58 GMT
EXPOSE 8091
# Tue, 13 Oct 2020 23:23:59 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Oct 2020 23:23:59 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 13 Oct 2020 23:23:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 23:23:59 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8559aa5ebb59d52475c0142459015fb9be267e1a497d8664f3fc8a35445173`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 10.8 MB (10751068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32bfbbc3bad880f731e2f37903c9e359e180a5e74a703293a9441260cf3551`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 4.3 MB (4340586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2107148596b1d475384d38442e52f5aee3e9ab070498ad61d7ae6fde1b136793`  
		Last Modified: Tue, 13 Oct 2020 23:25:21 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261235e55734407be4a1196fc171fba46c097fa6ec481c30603821d8b3e70e3f`  
		Last Modified: Tue, 13 Oct 2020 23:26:26 GMT  
		Size: 23.1 MB (23132663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ae0993153169c462e604ad5b13d113d9637424d878289ccc19172f5473a1ce`  
		Last Modified: Tue, 13 Oct 2020 23:26:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e5fdf301b3895d14ed1da7b20133cd8004f58a8e871d10131953d66847ecc1`  
		Last Modified: Tue, 13 Oct 2020 23:26:22 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-meta-alpine`

```console
$ docker pull influxdb@sha256:abd6a0c5e71d742cd66274f5b0d6d95cc3eed64d4f83238ce3c616a795d36240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:c59e639516bdde5c0f1aa33a144117d8984775cafa6d9e57b00ce9b2ba47a2fb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27228222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbff5e0053b6fd6fb76731aa0897a46ddce122de9ab89771f5acbadf586c373f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:58:25 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 01 Sep 2020 00:58:41 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 02 Sep 2020 00:12:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 02 Sep 2020 00:12:30 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 02 Sep 2020 00:12:30 GMT
EXPOSE 8091
# Wed, 02 Sep 2020 00:12:31 GMT
VOLUME [/var/lib/influxdb]
# Wed, 02 Sep 2020 00:12:31 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 02 Sep 2020 00:12:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Sep 2020 00:12:31 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7279b9f70b385667a52ff20142c09fd4fe94f3c717683fe273d3af53528ada`  
		Last Modified: Tue, 01 Sep 2020 01:01:22 GMT  
		Size: 1.4 MB (1427184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e926a4ac2f6d229659017939bcd27c30a101cef5a8b6b8c89b54a13f355e616`  
		Last Modified: Wed, 02 Sep 2020 00:14:49 GMT  
		Size: 23.0 MB (23002776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:035a9b83b307a36d60c4477f29cc9ce7340803852e96e904bc2d08c8b5a94539`  
		Last Modified: Wed, 02 Sep 2020 00:14:45 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878762750ff031c08c7c13438015dd9e46b2cf8fc464bbefc21a493ca46f8559`  
		Last Modified: Wed, 02 Sep 2020 00:14:45 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8`

```console
$ docker pull influxdb@sha256:08d4559f382b6f1705231a453b7a7e59f9387b8b37e825b8d4f815dfcfdd9b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8` - linux; amd64

```console
$ docker pull influxdb@sha256:37ff13ea47fe65b16a72fc8d9aee4b4264b92c75ccff9f71404b70e3273eee10
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125428830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15aefdd926b54caa10fd9ae20bd9b1ab433bbfe4667c5f454ebf18ca3205485`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:23:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 23:24:07 GMT
ENV INFLUXDB_VERSION=1.8.3
# Tue, 13 Oct 2020 23:24:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 13 Oct 2020 23:24:19 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 13 Oct 2020 23:24:19 GMT
EXPOSE 8086
# Tue, 13 Oct 2020 23:24:19 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Oct 2020 23:24:19 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 13 Oct 2020 23:24:19 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Oct 2020 23:24:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 23:24:20 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8559aa5ebb59d52475c0142459015fb9be267e1a497d8664f3fc8a35445173`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 10.8 MB (10751068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32bfbbc3bad880f731e2f37903c9e359e180a5e74a703293a9441260cf3551`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 4.3 MB (4340586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2107148596b1d475384d38442e52f5aee3e9ab070498ad61d7ae6fde1b136793`  
		Last Modified: Tue, 13 Oct 2020 23:25:21 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4f998976a3a5232dc08310c34df7de51f438fcc4a717b758e24892fd20eb8c`  
		Last Modified: Tue, 13 Oct 2020 23:26:51 GMT  
		Size: 65.0 MB (64965855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b778e6196d24c69572771ae8a1d22fdfea3b452392e52b6fb3055b8e9cee304`  
		Last Modified: Tue, 13 Oct 2020 23:26:39 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32f0180a33f89b5be800465c10f37708ac00097a6c7046643d3949cb2af2936`  
		Last Modified: Tue, 13 Oct 2020 23:26:39 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b93617d02165b55ad2247c22dd670b57119d174f992d6469a39e13735acda8`  
		Last Modified: Tue, 13 Oct 2020 23:26:40 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:b4529fd53e9022bd1e83aaf04c6c6a1ebfffdfa112c31367d69da1354983a24b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116537009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f4765754f02a4b84f105115a677b529bd9d35f5eb995f3d35cbd8f51b4ebfa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Oct 2020 01:04:04 GMT
ADD file:fb1dab6b0ac08f52870fca9435eedd2f707a3b8a5d28e5d1c2ff88e096f695ec in / 
# Tue, 13 Oct 2020 01:04:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:47:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 01:48:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 21:40:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 21:44:10 GMT
ENV INFLUXDB_VERSION=1.8.3
# Tue, 13 Oct 2020 21:44:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 13 Oct 2020 21:45:14 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 13 Oct 2020 21:45:22 GMT
EXPOSE 8086
# Tue, 13 Oct 2020 21:45:30 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Oct 2020 21:45:50 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 13 Oct 2020 21:46:06 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Oct 2020 21:46:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 21:46:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1b636fdf37230c276ff1507a9f2b0067182f369cd669d1852bf5b9f5ba3a43bf`  
		Last Modified: Tue, 13 Oct 2020 01:12:25 GMT  
		Size: 42.1 MB (42111286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be3bc01c2e26b6c110cf55ed7833949511463f13387c8e708aec5a5c076fd83`  
		Last Modified: Tue, 13 Oct 2020 02:00:39 GMT  
		Size: 9.4 MB (9443957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1b23b3e38f06003a13d520ed3ec7eee0eafb5efe4a72d5508b3c2b2a7e3393`  
		Last Modified: Tue, 13 Oct 2020 02:00:37 GMT  
		Size: 3.9 MB (3919858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb874e260368d0b929e2dc1424843a22bfb4638e7a33c29465a3e302861bea9`  
		Last Modified: Tue, 13 Oct 2020 21:46:53 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5082600dc00e64d1fdd3972c115c7da5a31f896bfe7d6a92370e4b2e053bb97c`  
		Last Modified: Tue, 13 Oct 2020 21:47:36 GMT  
		Size: 61.1 MB (61057337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab7c7405a3b6e60e26ed4c3bb319a44aa2428d37b2aa99d0c0302d76581bcbd`  
		Last Modified: Tue, 13 Oct 2020 21:47:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b1bc5c7dce8ca2188feee6a4ebe41d36ba1dd2e11f34ebba3547c16cacc1e1`  
		Last Modified: Tue, 13 Oct 2020 21:47:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec56dafd95671f23eb4dd60ee9246171bdecdc16b8957ed3690cfd442c018e9c`  
		Last Modified: Tue, 13 Oct 2020 21:47:20 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:acea47f4730023b7f66495c1a78d67fceb7a37d4fcfbb966fe81e2d0c5cab9b2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117599345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93492a0189b98fcf8a0c1c11117a459fd60fc5d9e40b13e9e376460be0d2320c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Oct 2020 01:43:49 GMT
ADD file:2752d391988f4ad7e086be863c36a83a3226e31e44ea816ca4c89d6a410727b1 in / 
# Tue, 13 Oct 2020 01:43:51 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:40:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:40:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 14 Oct 2020 00:42:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 14 Oct 2020 00:42:45 GMT
ENV INFLUXDB_VERSION=1.8.3
# Wed, 14 Oct 2020 00:42:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 14 Oct 2020 00:42:56 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 14 Oct 2020 00:42:56 GMT
EXPOSE 8086
# Wed, 14 Oct 2020 00:42:57 GMT
VOLUME [/var/lib/influxdb]
# Wed, 14 Oct 2020 00:42:58 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 14 Oct 2020 00:42:58 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 14 Oct 2020 00:42:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Oct 2020 00:43:00 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:19e4d0e7f8f2c5cb8a0a8d0e741e9e387c34bd673da69cdcc8e758a5c4dbc106`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 43.2 MB (43171543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b66c8297162aeeca035e2cf9e752a4f0e5b411d1c90d7314aba56e52741b6cf`  
		Last Modified: Tue, 13 Oct 2020 02:50:51 GMT  
		Size: 9.7 MB (9701174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558b5390d6e12ba26207e779d409c31a61c54713a327bb04565a18f2432bb25d`  
		Last Modified: Tue, 13 Oct 2020 02:50:50 GMT  
		Size: 4.1 MB (4095275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fa64acfa2daa89a185c25af4ca9c3567e8f967ad4a9658356d2f87c180554a`  
		Last Modified: Wed, 14 Oct 2020 00:43:12 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711e58d7c899353413ed9a7a69e2f44ebe1f0f54455551b95d74c80878825276`  
		Last Modified: Wed, 14 Oct 2020 00:43:55 GMT  
		Size: 60.6 MB (60626781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ed2cc3695654d0c61dc8145e897ad7ed1d12a8b21dd3a809d90cfa6c6a20c5`  
		Last Modified: Wed, 14 Oct 2020 00:43:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fe23bddda38f9bad90dd8c5f6f1b88bf2638cda45be2e4d844c811367a4e6c`  
		Last Modified: Wed, 14 Oct 2020 00:43:41 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1bb09f7551524e946c5408e31f4c233b5ec8241f767714fd6110bd3d5bcbdf`  
		Last Modified: Wed, 14 Oct 2020 00:43:41 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3`

```console
$ docker pull influxdb@sha256:08d4559f382b6f1705231a453b7a7e59f9387b8b37e825b8d4f815dfcfdd9b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8.3` - linux; amd64

```console
$ docker pull influxdb@sha256:37ff13ea47fe65b16a72fc8d9aee4b4264b92c75ccff9f71404b70e3273eee10
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125428830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15aefdd926b54caa10fd9ae20bd9b1ab433bbfe4667c5f454ebf18ca3205485`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:23:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 23:24:07 GMT
ENV INFLUXDB_VERSION=1.8.3
# Tue, 13 Oct 2020 23:24:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 13 Oct 2020 23:24:19 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 13 Oct 2020 23:24:19 GMT
EXPOSE 8086
# Tue, 13 Oct 2020 23:24:19 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Oct 2020 23:24:19 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 13 Oct 2020 23:24:19 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Oct 2020 23:24:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 23:24:20 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8559aa5ebb59d52475c0142459015fb9be267e1a497d8664f3fc8a35445173`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 10.8 MB (10751068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32bfbbc3bad880f731e2f37903c9e359e180a5e74a703293a9441260cf3551`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 4.3 MB (4340586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2107148596b1d475384d38442e52f5aee3e9ab070498ad61d7ae6fde1b136793`  
		Last Modified: Tue, 13 Oct 2020 23:25:21 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4f998976a3a5232dc08310c34df7de51f438fcc4a717b758e24892fd20eb8c`  
		Last Modified: Tue, 13 Oct 2020 23:26:51 GMT  
		Size: 65.0 MB (64965855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b778e6196d24c69572771ae8a1d22fdfea3b452392e52b6fb3055b8e9cee304`  
		Last Modified: Tue, 13 Oct 2020 23:26:39 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32f0180a33f89b5be800465c10f37708ac00097a6c7046643d3949cb2af2936`  
		Last Modified: Tue, 13 Oct 2020 23:26:39 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b93617d02165b55ad2247c22dd670b57119d174f992d6469a39e13735acda8`  
		Last Modified: Tue, 13 Oct 2020 23:26:40 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.3` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:b4529fd53e9022bd1e83aaf04c6c6a1ebfffdfa112c31367d69da1354983a24b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116537009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f4765754f02a4b84f105115a677b529bd9d35f5eb995f3d35cbd8f51b4ebfa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Oct 2020 01:04:04 GMT
ADD file:fb1dab6b0ac08f52870fca9435eedd2f707a3b8a5d28e5d1c2ff88e096f695ec in / 
# Tue, 13 Oct 2020 01:04:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:47:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 01:48:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 21:40:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 21:44:10 GMT
ENV INFLUXDB_VERSION=1.8.3
# Tue, 13 Oct 2020 21:44:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 13 Oct 2020 21:45:14 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 13 Oct 2020 21:45:22 GMT
EXPOSE 8086
# Tue, 13 Oct 2020 21:45:30 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Oct 2020 21:45:50 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 13 Oct 2020 21:46:06 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Oct 2020 21:46:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 21:46:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1b636fdf37230c276ff1507a9f2b0067182f369cd669d1852bf5b9f5ba3a43bf`  
		Last Modified: Tue, 13 Oct 2020 01:12:25 GMT  
		Size: 42.1 MB (42111286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be3bc01c2e26b6c110cf55ed7833949511463f13387c8e708aec5a5c076fd83`  
		Last Modified: Tue, 13 Oct 2020 02:00:39 GMT  
		Size: 9.4 MB (9443957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1b23b3e38f06003a13d520ed3ec7eee0eafb5efe4a72d5508b3c2b2a7e3393`  
		Last Modified: Tue, 13 Oct 2020 02:00:37 GMT  
		Size: 3.9 MB (3919858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb874e260368d0b929e2dc1424843a22bfb4638e7a33c29465a3e302861bea9`  
		Last Modified: Tue, 13 Oct 2020 21:46:53 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5082600dc00e64d1fdd3972c115c7da5a31f896bfe7d6a92370e4b2e053bb97c`  
		Last Modified: Tue, 13 Oct 2020 21:47:36 GMT  
		Size: 61.1 MB (61057337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab7c7405a3b6e60e26ed4c3bb319a44aa2428d37b2aa99d0c0302d76581bcbd`  
		Last Modified: Tue, 13 Oct 2020 21:47:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b1bc5c7dce8ca2188feee6a4ebe41d36ba1dd2e11f34ebba3547c16cacc1e1`  
		Last Modified: Tue, 13 Oct 2020 21:47:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec56dafd95671f23eb4dd60ee9246171bdecdc16b8957ed3690cfd442c018e9c`  
		Last Modified: Tue, 13 Oct 2020 21:47:20 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.3` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:acea47f4730023b7f66495c1a78d67fceb7a37d4fcfbb966fe81e2d0c5cab9b2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117599345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93492a0189b98fcf8a0c1c11117a459fd60fc5d9e40b13e9e376460be0d2320c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Oct 2020 01:43:49 GMT
ADD file:2752d391988f4ad7e086be863c36a83a3226e31e44ea816ca4c89d6a410727b1 in / 
# Tue, 13 Oct 2020 01:43:51 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:40:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:40:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 14 Oct 2020 00:42:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 14 Oct 2020 00:42:45 GMT
ENV INFLUXDB_VERSION=1.8.3
# Wed, 14 Oct 2020 00:42:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 14 Oct 2020 00:42:56 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 14 Oct 2020 00:42:56 GMT
EXPOSE 8086
# Wed, 14 Oct 2020 00:42:57 GMT
VOLUME [/var/lib/influxdb]
# Wed, 14 Oct 2020 00:42:58 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 14 Oct 2020 00:42:58 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 14 Oct 2020 00:42:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Oct 2020 00:43:00 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:19e4d0e7f8f2c5cb8a0a8d0e741e9e387c34bd673da69cdcc8e758a5c4dbc106`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 43.2 MB (43171543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b66c8297162aeeca035e2cf9e752a4f0e5b411d1c90d7314aba56e52741b6cf`  
		Last Modified: Tue, 13 Oct 2020 02:50:51 GMT  
		Size: 9.7 MB (9701174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558b5390d6e12ba26207e779d409c31a61c54713a327bb04565a18f2432bb25d`  
		Last Modified: Tue, 13 Oct 2020 02:50:50 GMT  
		Size: 4.1 MB (4095275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fa64acfa2daa89a185c25af4ca9c3567e8f967ad4a9658356d2f87c180554a`  
		Last Modified: Wed, 14 Oct 2020 00:43:12 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711e58d7c899353413ed9a7a69e2f44ebe1f0f54455551b95d74c80878825276`  
		Last Modified: Wed, 14 Oct 2020 00:43:55 GMT  
		Size: 60.6 MB (60626781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ed2cc3695654d0c61dc8145e897ad7ed1d12a8b21dd3a809d90cfa6c6a20c5`  
		Last Modified: Wed, 14 Oct 2020 00:43:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fe23bddda38f9bad90dd8c5f6f1b88bf2638cda45be2e4d844c811367a4e6c`  
		Last Modified: Wed, 14 Oct 2020 00:43:41 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1bb09f7551524e946c5408e31f4c233b5ec8241f767714fd6110bd3d5bcbdf`  
		Last Modified: Wed, 14 Oct 2020 00:43:41 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-alpine`

```console
$ docker pull influxdb@sha256:6164ccc357644e45c9f5109930b5f2129779cd35dcffcc159d9087d5c0bc0b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e5ec65e5f17945cb07d31bcfada571a99409c7d6e1569a7a6fd00614fc87443e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68933395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c05a8368bb8ae92a31b3134560aa1e4a9240fed013cd3557bf44d5f36733194`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:58:25 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 02 Oct 2020 01:35:01 GMT
ENV INFLUXDB_VERSION=1.8.3
# Fri, 02 Oct 2020 01:35:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 02 Oct 2020 01:35:13 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 02 Oct 2020 01:35:14 GMT
EXPOSE 8086
# Fri, 02 Oct 2020 01:35:14 GMT
VOLUME [/var/lib/influxdb]
# Fri, 02 Oct 2020 01:35:14 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 02 Oct 2020 01:35:15 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 02 Oct 2020 01:35:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:35:15 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7279b9f70b385667a52ff20142c09fd4fe94f3c717683fe273d3af53528ada`  
		Last Modified: Tue, 01 Sep 2020 01:01:22 GMT  
		Size: 1.4 MB (1427184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac8d40395bf69bf20882c2380b63e8b58c5a6a0c33db4f615c71cf297aa0040`  
		Last Modified: Fri, 02 Oct 2020 01:37:20 GMT  
		Size: 64.7 MB (64706805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a84861fe0f5c1b40110a3e1acc2f5ec6e450eaf4df4fef054661eb1b446db9`  
		Last Modified: Fri, 02 Oct 2020 01:37:10 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126c200711ccb87277a552ef28d8dea7f62aba0c01a7b24964aa0204d88883b3`  
		Last Modified: Fri, 02 Oct 2020 01:37:10 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cec4b06914a90ed7b99e6e168e85bd05aeb96402a628fe40c54b88c82a19fcf`  
		Last Modified: Fri, 02 Oct 2020 01:37:11 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-data`

```console
$ docker pull influxdb@sha256:4e731f442b48686a25850c1c17bba29ddf5dafe2e4a333a124a5b8eb92f78c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-data` - linux; amd64

```console
$ docker pull influxdb@sha256:e7bf385eed0ed6747f02f3a773bf560e3672befc07323e657ccb1cfb66214cef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126259083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33314d1a32c565f73f6d46b81b6214d0095d21cc53fdfc55936e52c181ef584f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:23:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 23:24:28 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Tue, 13 Oct 2020 23:24:38 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Tue, 13 Oct 2020 23:24:38 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 13 Oct 2020 23:24:38 GMT
EXPOSE 8086
# Tue, 13 Oct 2020 23:24:39 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Oct 2020 23:24:39 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 13 Oct 2020 23:24:39 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Oct 2020 23:24:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 23:24:39 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8559aa5ebb59d52475c0142459015fb9be267e1a497d8664f3fc8a35445173`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 10.8 MB (10751068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32bfbbc3bad880f731e2f37903c9e359e180a5e74a703293a9441260cf3551`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 4.3 MB (4340586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2107148596b1d475384d38442e52f5aee3e9ab070498ad61d7ae6fde1b136793`  
		Last Modified: Tue, 13 Oct 2020 23:25:21 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78899c7499770b74c69453d21d81f6b7335dd14c106ed2111e295e5ae7c8dcf`  
		Last Modified: Tue, 13 Oct 2020 23:27:10 GMT  
		Size: 65.8 MB (65796049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38b5a149abfbcd0fb90d7aba7731a818ec848e88f6bbcd380ef8ff6798f72a8`  
		Last Modified: Tue, 13 Oct 2020 23:26:58 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60172c342366dbbe1e4ffb11db1683bd49fbfe5a0ca467148a63947269be76e9`  
		Last Modified: Tue, 13 Oct 2020 23:26:58 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040c38124b3a8ab9a7916bf9b961dcc6ff9b790549d1137d4b1f3ca2f84dea76`  
		Last Modified: Tue, 13 Oct 2020 23:26:58 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-data-alpine`

```console
$ docker pull influxdb@sha256:2a40c2dcc051f1fa3ff879b6a3ad180ba3ceb5663d19fb705077e110a3157c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:6ab1bc2ac832e74bc9a8f8cdaa1ec926f128f9295f310d4bac50b4040fa41faf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69767912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9005367a7013a0c821114e5c246af4c958b406b70964740c7a75ac7db455626e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:58:25 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 02 Oct 2020 01:35:42 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Fri, 02 Oct 2020 01:35:54 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 02 Oct 2020 01:35:54 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 02 Oct 2020 01:35:54 GMT
EXPOSE 8086
# Fri, 02 Oct 2020 01:35:55 GMT
VOLUME [/var/lib/influxdb]
# Fri, 02 Oct 2020 01:35:55 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 02 Oct 2020 01:35:56 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 02 Oct 2020 01:35:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:35:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7279b9f70b385667a52ff20142c09fd4fe94f3c717683fe273d3af53528ada`  
		Last Modified: Tue, 01 Sep 2020 01:01:22 GMT  
		Size: 1.4 MB (1427184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6c9cc6d742b38a644e52f5315dd19a00f1e35914458395b2727a6ec49e6907`  
		Last Modified: Fri, 02 Oct 2020 01:38:00 GMT  
		Size: 65.5 MB (65541265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df65ca50a156e83f23ce08b536c7a5be6fbc1c7d22d97f1eb19134cca6a85c9b`  
		Last Modified: Fri, 02 Oct 2020 01:37:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b53dc52b55c114635baf6e8ae10d60c5b67ee15e6e8b826c19a067ca7cdb83a`  
		Last Modified: Fri, 02 Oct 2020 01:37:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b9c39533c0948f67ff7de863ebab65b8de2fcfb1dc5cad22b67cb5744b971d`  
		Last Modified: Fri, 02 Oct 2020 01:37:48 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-meta`

```console
$ docker pull influxdb@sha256:e0c3128a5a4f13e9e2c0458d9ce3e214a352a578670c45d2ca10b7ad3a79d4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:832644b195462477c771dd131795f0f94a2da2acb68f51ede21169812fe476c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83327105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c949da4bdef3d8b30689c39a4cddf7e49d661dc36006f132dfd9dd6bac8bd5e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:23:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 23:24:28 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Tue, 13 Oct 2020 23:24:54 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Tue, 13 Oct 2020 23:24:54 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 13 Oct 2020 23:24:55 GMT
EXPOSE 8091
# Tue, 13 Oct 2020 23:24:55 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Oct 2020 23:24:55 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 13 Oct 2020 23:24:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 23:24:56 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8559aa5ebb59d52475c0142459015fb9be267e1a497d8664f3fc8a35445173`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 10.8 MB (10751068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32bfbbc3bad880f731e2f37903c9e359e180a5e74a703293a9441260cf3551`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 4.3 MB (4340586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2107148596b1d475384d38442e52f5aee3e9ab070498ad61d7ae6fde1b136793`  
		Last Modified: Tue, 13 Oct 2020 23:25:21 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1244f0c82926c52dada51c72c56ebf7f2292e8b86dd9f146657b9ea24545c4`  
		Last Modified: Tue, 13 Oct 2020 23:27:31 GMT  
		Size: 22.9 MB (22865278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf7761c34341104f351f1ea9bd2f6bb719fea42c9d8d4b6137ec36c9137968b`  
		Last Modified: Tue, 13 Oct 2020 23:27:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbbe52edc408b0748ba9cea8fc3096730a300bc0bba111918c4294e9bb200e8`  
		Last Modified: Tue, 13 Oct 2020 23:27:28 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-meta-alpine`

```console
$ docker pull influxdb@sha256:9e0398d5a404e926ef1f323f82d42e720bfc95be0c5e75daf996443b50838832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:52448fe88e33f95fc4d67a497594a79ea2429b45c060b2f47e611b6b56d04c4a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26960924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c880c97715d917f46ea45279fdc97bbe1f1d6ea0813a489d350f849ddd19ec6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:58:25 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 02 Oct 2020 01:35:42 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Fri, 02 Oct 2020 01:36:21 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 02 Oct 2020 01:36:21 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 02 Oct 2020 01:36:22 GMT
EXPOSE 8091
# Fri, 02 Oct 2020 01:36:22 GMT
VOLUME [/var/lib/influxdb]
# Fri, 02 Oct 2020 01:36:22 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 02 Oct 2020 01:36:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:36:23 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7279b9f70b385667a52ff20142c09fd4fe94f3c717683fe273d3af53528ada`  
		Last Modified: Tue, 01 Sep 2020 01:01:22 GMT  
		Size: 1.4 MB (1427184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ff1317902374e623809ca4662f3268f4baa22b0d30e4291d0d1c65c46b1e4`  
		Last Modified: Fri, 02 Oct 2020 01:38:26 GMT  
		Size: 22.7 MB (22735479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bffba48663473be34d6a2866430290d0d1f1f764ef58a22eb8015cc23a072b2`  
		Last Modified: Fri, 02 Oct 2020 01:38:18 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f34efd91799ade0c6963a123abc31838782ce898b2435a8ccd21d00447a4c34`  
		Last Modified: Fri, 02 Oct 2020 01:38:18 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-alpine`

```console
$ docker pull influxdb@sha256:6164ccc357644e45c9f5109930b5f2129779cd35dcffcc159d9087d5c0bc0b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e5ec65e5f17945cb07d31bcfada571a99409c7d6e1569a7a6fd00614fc87443e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68933395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c05a8368bb8ae92a31b3134560aa1e4a9240fed013cd3557bf44d5f36733194`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:58:25 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 02 Oct 2020 01:35:01 GMT
ENV INFLUXDB_VERSION=1.8.3
# Fri, 02 Oct 2020 01:35:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 02 Oct 2020 01:35:13 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 02 Oct 2020 01:35:14 GMT
EXPOSE 8086
# Fri, 02 Oct 2020 01:35:14 GMT
VOLUME [/var/lib/influxdb]
# Fri, 02 Oct 2020 01:35:14 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 02 Oct 2020 01:35:15 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 02 Oct 2020 01:35:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:35:15 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7279b9f70b385667a52ff20142c09fd4fe94f3c717683fe273d3af53528ada`  
		Last Modified: Tue, 01 Sep 2020 01:01:22 GMT  
		Size: 1.4 MB (1427184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac8d40395bf69bf20882c2380b63e8b58c5a6a0c33db4f615c71cf297aa0040`  
		Last Modified: Fri, 02 Oct 2020 01:37:20 GMT  
		Size: 64.7 MB (64706805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a84861fe0f5c1b40110a3e1acc2f5ec6e450eaf4df4fef054661eb1b446db9`  
		Last Modified: Fri, 02 Oct 2020 01:37:10 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126c200711ccb87277a552ef28d8dea7f62aba0c01a7b24964aa0204d88883b3`  
		Last Modified: Fri, 02 Oct 2020 01:37:10 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cec4b06914a90ed7b99e6e168e85bd05aeb96402a628fe40c54b88c82a19fcf`  
		Last Modified: Fri, 02 Oct 2020 01:37:11 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data`

```console
$ docker pull influxdb@sha256:4e731f442b48686a25850c1c17bba29ddf5dafe2e4a333a124a5b8eb92f78c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:e7bf385eed0ed6747f02f3a773bf560e3672befc07323e657ccb1cfb66214cef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126259083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33314d1a32c565f73f6d46b81b6214d0095d21cc53fdfc55936e52c181ef584f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:23:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 23:24:28 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Tue, 13 Oct 2020 23:24:38 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Tue, 13 Oct 2020 23:24:38 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 13 Oct 2020 23:24:38 GMT
EXPOSE 8086
# Tue, 13 Oct 2020 23:24:39 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Oct 2020 23:24:39 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 13 Oct 2020 23:24:39 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Oct 2020 23:24:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 23:24:39 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8559aa5ebb59d52475c0142459015fb9be267e1a497d8664f3fc8a35445173`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 10.8 MB (10751068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32bfbbc3bad880f731e2f37903c9e359e180a5e74a703293a9441260cf3551`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 4.3 MB (4340586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2107148596b1d475384d38442e52f5aee3e9ab070498ad61d7ae6fde1b136793`  
		Last Modified: Tue, 13 Oct 2020 23:25:21 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78899c7499770b74c69453d21d81f6b7335dd14c106ed2111e295e5ae7c8dcf`  
		Last Modified: Tue, 13 Oct 2020 23:27:10 GMT  
		Size: 65.8 MB (65796049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38b5a149abfbcd0fb90d7aba7731a818ec848e88f6bbcd380ef8ff6798f72a8`  
		Last Modified: Tue, 13 Oct 2020 23:26:58 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60172c342366dbbe1e4ffb11db1683bd49fbfe5a0ca467148a63947269be76e9`  
		Last Modified: Tue, 13 Oct 2020 23:26:58 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040c38124b3a8ab9a7916bf9b961dcc6ff9b790549d1137d4b1f3ca2f84dea76`  
		Last Modified: Tue, 13 Oct 2020 23:26:58 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data-alpine`

```console
$ docker pull influxdb@sha256:2a40c2dcc051f1fa3ff879b6a3ad180ba3ceb5663d19fb705077e110a3157c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:6ab1bc2ac832e74bc9a8f8cdaa1ec926f128f9295f310d4bac50b4040fa41faf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69767912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9005367a7013a0c821114e5c246af4c958b406b70964740c7a75ac7db455626e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:58:25 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 02 Oct 2020 01:35:42 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Fri, 02 Oct 2020 01:35:54 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 02 Oct 2020 01:35:54 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 02 Oct 2020 01:35:54 GMT
EXPOSE 8086
# Fri, 02 Oct 2020 01:35:55 GMT
VOLUME [/var/lib/influxdb]
# Fri, 02 Oct 2020 01:35:55 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 02 Oct 2020 01:35:56 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 02 Oct 2020 01:35:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:35:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7279b9f70b385667a52ff20142c09fd4fe94f3c717683fe273d3af53528ada`  
		Last Modified: Tue, 01 Sep 2020 01:01:22 GMT  
		Size: 1.4 MB (1427184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6c9cc6d742b38a644e52f5315dd19a00f1e35914458395b2727a6ec49e6907`  
		Last Modified: Fri, 02 Oct 2020 01:38:00 GMT  
		Size: 65.5 MB (65541265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df65ca50a156e83f23ce08b536c7a5be6fbc1c7d22d97f1eb19134cca6a85c9b`  
		Last Modified: Fri, 02 Oct 2020 01:37:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b53dc52b55c114635baf6e8ae10d60c5b67ee15e6e8b826c19a067ca7cdb83a`  
		Last Modified: Fri, 02 Oct 2020 01:37:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b9c39533c0948f67ff7de863ebab65b8de2fcfb1dc5cad22b67cb5744b971d`  
		Last Modified: Fri, 02 Oct 2020 01:37:48 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-meta`

```console
$ docker pull influxdb@sha256:e0c3128a5a4f13e9e2c0458d9ce3e214a352a578670c45d2ca10b7ad3a79d4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:832644b195462477c771dd131795f0f94a2da2acb68f51ede21169812fe476c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83327105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c949da4bdef3d8b30689c39a4cddf7e49d661dc36006f132dfd9dd6bac8bd5e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:23:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 23:24:28 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Tue, 13 Oct 2020 23:24:54 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Tue, 13 Oct 2020 23:24:54 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 13 Oct 2020 23:24:55 GMT
EXPOSE 8091
# Tue, 13 Oct 2020 23:24:55 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Oct 2020 23:24:55 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 13 Oct 2020 23:24:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 23:24:56 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8559aa5ebb59d52475c0142459015fb9be267e1a497d8664f3fc8a35445173`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 10.8 MB (10751068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32bfbbc3bad880f731e2f37903c9e359e180a5e74a703293a9441260cf3551`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 4.3 MB (4340586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2107148596b1d475384d38442e52f5aee3e9ab070498ad61d7ae6fde1b136793`  
		Last Modified: Tue, 13 Oct 2020 23:25:21 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1244f0c82926c52dada51c72c56ebf7f2292e8b86dd9f146657b9ea24545c4`  
		Last Modified: Tue, 13 Oct 2020 23:27:31 GMT  
		Size: 22.9 MB (22865278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf7761c34341104f351f1ea9bd2f6bb719fea42c9d8d4b6137ec36c9137968b`  
		Last Modified: Tue, 13 Oct 2020 23:27:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbbe52edc408b0748ba9cea8fc3096730a300bc0bba111918c4294e9bb200e8`  
		Last Modified: Tue, 13 Oct 2020 23:27:28 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-meta-alpine`

```console
$ docker pull influxdb@sha256:9e0398d5a404e926ef1f323f82d42e720bfc95be0c5e75daf996443b50838832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:52448fe88e33f95fc4d67a497594a79ea2429b45c060b2f47e611b6b56d04c4a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26960924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c880c97715d917f46ea45279fdc97bbe1f1d6ea0813a489d350f849ddd19ec6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:58:25 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 02 Oct 2020 01:35:42 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Fri, 02 Oct 2020 01:36:21 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 02 Oct 2020 01:36:21 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 02 Oct 2020 01:36:22 GMT
EXPOSE 8091
# Fri, 02 Oct 2020 01:36:22 GMT
VOLUME [/var/lib/influxdb]
# Fri, 02 Oct 2020 01:36:22 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 02 Oct 2020 01:36:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:36:23 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7279b9f70b385667a52ff20142c09fd4fe94f3c717683fe273d3af53528ada`  
		Last Modified: Tue, 01 Sep 2020 01:01:22 GMT  
		Size: 1.4 MB (1427184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ff1317902374e623809ca4662f3268f4baa22b0d30e4291d0d1c65c46b1e4`  
		Last Modified: Fri, 02 Oct 2020 01:38:26 GMT  
		Size: 22.7 MB (22735479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bffba48663473be34d6a2866430290d0d1f1f764ef58a22eb8015cc23a072b2`  
		Last Modified: Fri, 02 Oct 2020 01:38:18 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f34efd91799ade0c6963a123abc31838782ce898b2435a8ccd21d00447a4c34`  
		Last Modified: Fri, 02 Oct 2020 01:38:18 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:6164ccc357644e45c9f5109930b5f2129779cd35dcffcc159d9087d5c0bc0b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e5ec65e5f17945cb07d31bcfada571a99409c7d6e1569a7a6fd00614fc87443e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68933395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c05a8368bb8ae92a31b3134560aa1e4a9240fed013cd3557bf44d5f36733194`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:58:25 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 02 Oct 2020 01:35:01 GMT
ENV INFLUXDB_VERSION=1.8.3
# Fri, 02 Oct 2020 01:35:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 02 Oct 2020 01:35:13 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 02 Oct 2020 01:35:14 GMT
EXPOSE 8086
# Fri, 02 Oct 2020 01:35:14 GMT
VOLUME [/var/lib/influxdb]
# Fri, 02 Oct 2020 01:35:14 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 02 Oct 2020 01:35:15 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 02 Oct 2020 01:35:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:35:15 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7279b9f70b385667a52ff20142c09fd4fe94f3c717683fe273d3af53528ada`  
		Last Modified: Tue, 01 Sep 2020 01:01:22 GMT  
		Size: 1.4 MB (1427184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac8d40395bf69bf20882c2380b63e8b58c5a6a0c33db4f615c71cf297aa0040`  
		Last Modified: Fri, 02 Oct 2020 01:37:20 GMT  
		Size: 64.7 MB (64706805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a84861fe0f5c1b40110a3e1acc2f5ec6e450eaf4df4fef054661eb1b446db9`  
		Last Modified: Fri, 02 Oct 2020 01:37:10 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126c200711ccb87277a552ef28d8dea7f62aba0c01a7b24964aa0204d88883b3`  
		Last Modified: Fri, 02 Oct 2020 01:37:10 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cec4b06914a90ed7b99e6e168e85bd05aeb96402a628fe40c54b88c82a19fcf`  
		Last Modified: Fri, 02 Oct 2020 01:37:11 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data`

```console
$ docker pull influxdb@sha256:4e731f442b48686a25850c1c17bba29ddf5dafe2e4a333a124a5b8eb92f78c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:e7bf385eed0ed6747f02f3a773bf560e3672befc07323e657ccb1cfb66214cef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126259083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33314d1a32c565f73f6d46b81b6214d0095d21cc53fdfc55936e52c181ef584f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:23:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 23:24:28 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Tue, 13 Oct 2020 23:24:38 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Tue, 13 Oct 2020 23:24:38 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 13 Oct 2020 23:24:38 GMT
EXPOSE 8086
# Tue, 13 Oct 2020 23:24:39 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Oct 2020 23:24:39 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 13 Oct 2020 23:24:39 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Oct 2020 23:24:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 23:24:39 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8559aa5ebb59d52475c0142459015fb9be267e1a497d8664f3fc8a35445173`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 10.8 MB (10751068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32bfbbc3bad880f731e2f37903c9e359e180a5e74a703293a9441260cf3551`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 4.3 MB (4340586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2107148596b1d475384d38442e52f5aee3e9ab070498ad61d7ae6fde1b136793`  
		Last Modified: Tue, 13 Oct 2020 23:25:21 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78899c7499770b74c69453d21d81f6b7335dd14c106ed2111e295e5ae7c8dcf`  
		Last Modified: Tue, 13 Oct 2020 23:27:10 GMT  
		Size: 65.8 MB (65796049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38b5a149abfbcd0fb90d7aba7731a818ec848e88f6bbcd380ef8ff6798f72a8`  
		Last Modified: Tue, 13 Oct 2020 23:26:58 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60172c342366dbbe1e4ffb11db1683bd49fbfe5a0ca467148a63947269be76e9`  
		Last Modified: Tue, 13 Oct 2020 23:26:58 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040c38124b3a8ab9a7916bf9b961dcc6ff9b790549d1137d4b1f3ca2f84dea76`  
		Last Modified: Tue, 13 Oct 2020 23:26:58 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:2a40c2dcc051f1fa3ff879b6a3ad180ba3ceb5663d19fb705077e110a3157c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:6ab1bc2ac832e74bc9a8f8cdaa1ec926f128f9295f310d4bac50b4040fa41faf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69767912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9005367a7013a0c821114e5c246af4c958b406b70964740c7a75ac7db455626e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:58:25 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 02 Oct 2020 01:35:42 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Fri, 02 Oct 2020 01:35:54 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 02 Oct 2020 01:35:54 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 02 Oct 2020 01:35:54 GMT
EXPOSE 8086
# Fri, 02 Oct 2020 01:35:55 GMT
VOLUME [/var/lib/influxdb]
# Fri, 02 Oct 2020 01:35:55 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 02 Oct 2020 01:35:56 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 02 Oct 2020 01:35:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:35:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7279b9f70b385667a52ff20142c09fd4fe94f3c717683fe273d3af53528ada`  
		Last Modified: Tue, 01 Sep 2020 01:01:22 GMT  
		Size: 1.4 MB (1427184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6c9cc6d742b38a644e52f5315dd19a00f1e35914458395b2727a6ec49e6907`  
		Last Modified: Fri, 02 Oct 2020 01:38:00 GMT  
		Size: 65.5 MB (65541265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df65ca50a156e83f23ce08b536c7a5be6fbc1c7d22d97f1eb19134cca6a85c9b`  
		Last Modified: Fri, 02 Oct 2020 01:37:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b53dc52b55c114635baf6e8ae10d60c5b67ee15e6e8b826c19a067ca7cdb83a`  
		Last Modified: Fri, 02 Oct 2020 01:37:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b9c39533c0948f67ff7de863ebab65b8de2fcfb1dc5cad22b67cb5744b971d`  
		Last Modified: Fri, 02 Oct 2020 01:37:48 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:08d4559f382b6f1705231a453b7a7e59f9387b8b37e825b8d4f815dfcfdd9b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:37ff13ea47fe65b16a72fc8d9aee4b4264b92c75ccff9f71404b70e3273eee10
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125428830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15aefdd926b54caa10fd9ae20bd9b1ab433bbfe4667c5f454ebf18ca3205485`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:23:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 23:24:07 GMT
ENV INFLUXDB_VERSION=1.8.3
# Tue, 13 Oct 2020 23:24:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 13 Oct 2020 23:24:19 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 13 Oct 2020 23:24:19 GMT
EXPOSE 8086
# Tue, 13 Oct 2020 23:24:19 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Oct 2020 23:24:19 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 13 Oct 2020 23:24:19 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Oct 2020 23:24:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 23:24:20 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8559aa5ebb59d52475c0142459015fb9be267e1a497d8664f3fc8a35445173`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 10.8 MB (10751068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32bfbbc3bad880f731e2f37903c9e359e180a5e74a703293a9441260cf3551`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 4.3 MB (4340586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2107148596b1d475384d38442e52f5aee3e9ab070498ad61d7ae6fde1b136793`  
		Last Modified: Tue, 13 Oct 2020 23:25:21 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4f998976a3a5232dc08310c34df7de51f438fcc4a717b758e24892fd20eb8c`  
		Last Modified: Tue, 13 Oct 2020 23:26:51 GMT  
		Size: 65.0 MB (64965855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b778e6196d24c69572771ae8a1d22fdfea3b452392e52b6fb3055b8e9cee304`  
		Last Modified: Tue, 13 Oct 2020 23:26:39 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32f0180a33f89b5be800465c10f37708ac00097a6c7046643d3949cb2af2936`  
		Last Modified: Tue, 13 Oct 2020 23:26:39 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b93617d02165b55ad2247c22dd670b57119d174f992d6469a39e13735acda8`  
		Last Modified: Tue, 13 Oct 2020 23:26:40 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:b4529fd53e9022bd1e83aaf04c6c6a1ebfffdfa112c31367d69da1354983a24b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116537009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f4765754f02a4b84f105115a677b529bd9d35f5eb995f3d35cbd8f51b4ebfa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Oct 2020 01:04:04 GMT
ADD file:fb1dab6b0ac08f52870fca9435eedd2f707a3b8a5d28e5d1c2ff88e096f695ec in / 
# Tue, 13 Oct 2020 01:04:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:47:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 01:48:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 21:40:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 21:44:10 GMT
ENV INFLUXDB_VERSION=1.8.3
# Tue, 13 Oct 2020 21:44:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 13 Oct 2020 21:45:14 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 13 Oct 2020 21:45:22 GMT
EXPOSE 8086
# Tue, 13 Oct 2020 21:45:30 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Oct 2020 21:45:50 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 13 Oct 2020 21:46:06 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 13 Oct 2020 21:46:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 21:46:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1b636fdf37230c276ff1507a9f2b0067182f369cd669d1852bf5b9f5ba3a43bf`  
		Last Modified: Tue, 13 Oct 2020 01:12:25 GMT  
		Size: 42.1 MB (42111286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be3bc01c2e26b6c110cf55ed7833949511463f13387c8e708aec5a5c076fd83`  
		Last Modified: Tue, 13 Oct 2020 02:00:39 GMT  
		Size: 9.4 MB (9443957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1b23b3e38f06003a13d520ed3ec7eee0eafb5efe4a72d5508b3c2b2a7e3393`  
		Last Modified: Tue, 13 Oct 2020 02:00:37 GMT  
		Size: 3.9 MB (3919858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb874e260368d0b929e2dc1424843a22bfb4638e7a33c29465a3e302861bea9`  
		Last Modified: Tue, 13 Oct 2020 21:46:53 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5082600dc00e64d1fdd3972c115c7da5a31f896bfe7d6a92370e4b2e053bb97c`  
		Last Modified: Tue, 13 Oct 2020 21:47:36 GMT  
		Size: 61.1 MB (61057337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab7c7405a3b6e60e26ed4c3bb319a44aa2428d37b2aa99d0c0302d76581bcbd`  
		Last Modified: Tue, 13 Oct 2020 21:47:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b1bc5c7dce8ca2188feee6a4ebe41d36ba1dd2e11f34ebba3547c16cacc1e1`  
		Last Modified: Tue, 13 Oct 2020 21:47:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec56dafd95671f23eb4dd60ee9246171bdecdc16b8957ed3690cfd442c018e9c`  
		Last Modified: Tue, 13 Oct 2020 21:47:20 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:acea47f4730023b7f66495c1a78d67fceb7a37d4fcfbb966fe81e2d0c5cab9b2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117599345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93492a0189b98fcf8a0c1c11117a459fd60fc5d9e40b13e9e376460be0d2320c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Oct 2020 01:43:49 GMT
ADD file:2752d391988f4ad7e086be863c36a83a3226e31e44ea816ca4c89d6a410727b1 in / 
# Tue, 13 Oct 2020 01:43:51 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:40:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:40:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 14 Oct 2020 00:42:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 14 Oct 2020 00:42:45 GMT
ENV INFLUXDB_VERSION=1.8.3
# Wed, 14 Oct 2020 00:42:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 14 Oct 2020 00:42:56 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 14 Oct 2020 00:42:56 GMT
EXPOSE 8086
# Wed, 14 Oct 2020 00:42:57 GMT
VOLUME [/var/lib/influxdb]
# Wed, 14 Oct 2020 00:42:58 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 14 Oct 2020 00:42:58 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 14 Oct 2020 00:42:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Oct 2020 00:43:00 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:19e4d0e7f8f2c5cb8a0a8d0e741e9e387c34bd673da69cdcc8e758a5c4dbc106`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 43.2 MB (43171543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b66c8297162aeeca035e2cf9e752a4f0e5b411d1c90d7314aba56e52741b6cf`  
		Last Modified: Tue, 13 Oct 2020 02:50:51 GMT  
		Size: 9.7 MB (9701174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558b5390d6e12ba26207e779d409c31a61c54713a327bb04565a18f2432bb25d`  
		Last Modified: Tue, 13 Oct 2020 02:50:50 GMT  
		Size: 4.1 MB (4095275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fa64acfa2daa89a185c25af4ca9c3567e8f967ad4a9658356d2f87c180554a`  
		Last Modified: Wed, 14 Oct 2020 00:43:12 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711e58d7c899353413ed9a7a69e2f44ebe1f0f54455551b95d74c80878825276`  
		Last Modified: Wed, 14 Oct 2020 00:43:55 GMT  
		Size: 60.6 MB (60626781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ed2cc3695654d0c61dc8145e897ad7ed1d12a8b21dd3a809d90cfa6c6a20c5`  
		Last Modified: Wed, 14 Oct 2020 00:43:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fe23bddda38f9bad90dd8c5f6f1b88bf2638cda45be2e4d844c811367a4e6c`  
		Last Modified: Wed, 14 Oct 2020 00:43:41 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1bb09f7551524e946c5408e31f4c233b5ec8241f767714fd6110bd3d5bcbdf`  
		Last Modified: Wed, 14 Oct 2020 00:43:41 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:e0c3128a5a4f13e9e2c0458d9ce3e214a352a578670c45d2ca10b7ad3a79d4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:832644b195462477c771dd131795f0f94a2da2acb68f51ede21169812fe476c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83327105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c949da4bdef3d8b30689c39a4cddf7e49d661dc36006f132dfd9dd6bac8bd5e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:23:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 23:24:28 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Tue, 13 Oct 2020 23:24:54 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Tue, 13 Oct 2020 23:24:54 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 13 Oct 2020 23:24:55 GMT
EXPOSE 8091
# Tue, 13 Oct 2020 23:24:55 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Oct 2020 23:24:55 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 13 Oct 2020 23:24:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 23:24:56 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8559aa5ebb59d52475c0142459015fb9be267e1a497d8664f3fc8a35445173`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 10.8 MB (10751068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32bfbbc3bad880f731e2f37903c9e359e180a5e74a703293a9441260cf3551`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 4.3 MB (4340586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2107148596b1d475384d38442e52f5aee3e9ab070498ad61d7ae6fde1b136793`  
		Last Modified: Tue, 13 Oct 2020 23:25:21 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1244f0c82926c52dada51c72c56ebf7f2292e8b86dd9f146657b9ea24545c4`  
		Last Modified: Tue, 13 Oct 2020 23:27:31 GMT  
		Size: 22.9 MB (22865278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf7761c34341104f351f1ea9bd2f6bb719fea42c9d8d4b6137ec36c9137968b`  
		Last Modified: Tue, 13 Oct 2020 23:27:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbbe52edc408b0748ba9cea8fc3096730a300bc0bba111918c4294e9bb200e8`  
		Last Modified: Tue, 13 Oct 2020 23:27:28 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta-alpine`

```console
$ docker pull influxdb@sha256:9e0398d5a404e926ef1f323f82d42e720bfc95be0c5e75daf996443b50838832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:52448fe88e33f95fc4d67a497594a79ea2429b45c060b2f47e611b6b56d04c4a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26960924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c880c97715d917f46ea45279fdc97bbe1f1d6ea0813a489d350f849ddd19ec6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:58:25 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 02 Oct 2020 01:35:42 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Fri, 02 Oct 2020 01:36:21 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 02 Oct 2020 01:36:21 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 02 Oct 2020 01:36:22 GMT
EXPOSE 8091
# Fri, 02 Oct 2020 01:36:22 GMT
VOLUME [/var/lib/influxdb]
# Fri, 02 Oct 2020 01:36:22 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 02 Oct 2020 01:36:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:36:23 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7279b9f70b385667a52ff20142c09fd4fe94f3c717683fe273d3af53528ada`  
		Last Modified: Tue, 01 Sep 2020 01:01:22 GMT  
		Size: 1.4 MB (1427184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443ff1317902374e623809ca4662f3268f4baa22b0d30e4291d0d1c65c46b1e4`  
		Last Modified: Fri, 02 Oct 2020 01:38:26 GMT  
		Size: 22.7 MB (22735479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bffba48663473be34d6a2866430290d0d1f1f764ef58a22eb8015cc23a072b2`  
		Last Modified: Fri, 02 Oct 2020 01:38:18 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f34efd91799ade0c6963a123abc31838782ce898b2435a8ccd21d00447a4c34`  
		Last Modified: Fri, 02 Oct 2020 01:38:18 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
