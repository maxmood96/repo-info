<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `influxdb`

-	[`influxdb:1.7`](#influxdb17)
-	[`influxdb:1.7-alpine`](#influxdb17-alpine)
-	[`influxdb:1.7-data`](#influxdb17-data)
-	[`influxdb:1.7-data-alpine`](#influxdb17-data-alpine)
-	[`influxdb:1.7-meta`](#influxdb17-meta)
-	[`influxdb:1.7-meta-alpine`](#influxdb17-meta-alpine)
-	[`influxdb:1.7.11`](#influxdb1711)
-	[`influxdb:1.7.11-alpine`](#influxdb1711-alpine)
-	[`influxdb:1.7.11-data`](#influxdb1711-data)
-	[`influxdb:1.7.11-data-alpine`](#influxdb1711-data-alpine)
-	[`influxdb:1.7.11-meta`](#influxdb1711-meta)
-	[`influxdb:1.7.11-meta-alpine`](#influxdb1711-meta-alpine)
-	[`influxdb:1.8`](#influxdb18)
-	[`influxdb:1.8-alpine`](#influxdb18-alpine)
-	[`influxdb:1.8-data`](#influxdb18-data)
-	[`influxdb:1.8-data-alpine`](#influxdb18-data-alpine)
-	[`influxdb:1.8-meta`](#influxdb18-meta)
-	[`influxdb:1.8-meta-alpine`](#influxdb18-meta-alpine)
-	[`influxdb:1.8.3-data`](#influxdb183-data)
-	[`influxdb:1.8.3-data-alpine`](#influxdb183-data-alpine)
-	[`influxdb:1.8.3-meta`](#influxdb183-meta)
-	[`influxdb:1.8.3-meta-alpine`](#influxdb183-meta-alpine)
-	[`influxdb:1.8.4`](#influxdb184)
-	[`influxdb:1.8.4-alpine`](#influxdb184-alpine)
-	[`influxdb:2.0`](#influxdb20)
-	[`influxdb:2.0-alpine`](#influxdb20-alpine)
-	[`influxdb:2.0.4`](#influxdb204)
-	[`influxdb:2.0.4-alpine`](#influxdb204-alpine)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:data`](#influxdbdata)
-	[`influxdb:data-alpine`](#influxdbdata-alpine)
-	[`influxdb:latest`](#influxdblatest)
-	[`influxdb:meta`](#influxdbmeta)
-	[`influxdb:meta-alpine`](#influxdbmeta-alpine)

## `influxdb:1.7`

```console
$ docker pull influxdb@sha256:5580120fd73fb9730224d50df5045abeb03aecff94be99c3436de1b40ecdd500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7` - linux; amd64

```console
$ docker pull influxdb@sha256:085e385bfa2ba565ab08f8cd2f0da84dd82aa4e17005474bb4d4a9742bc041c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122298781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12bc503b20833ec67f59ab266430f7271bfee129944caf515bd6fb8eb793e9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:08:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:08:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:08:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 22:08:33 GMT
ENV INFLUXDB_VERSION=1.7.11
# Wed, 31 Mar 2021 22:08:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 31 Mar 2021 22:08:37 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:08:37 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:08:37 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:08:38 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:08:38 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:08:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:08:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61ad49fa9961d6dfe53dc067fd690133f205498e8045e8f7ef6b9da0d42bd2`  
		Last Modified: Tue, 30 Mar 2021 23:17:25 GMT  
		Size: 11.3 MB (11286658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af62e04c0f85ed10801df4314d8cb9ba5e6c391f6a3c1db1080a0a78c8d4ed9d`  
		Last Modified: Tue, 30 Mar 2021 23:17:23 GMT  
		Size: 4.3 MB (4342466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ea2dd79e17761ed8d11e98f7420d9d909dcbc0ca1fe34ad492f5e495302a6`  
		Last Modified: Wed, 31 Mar 2021 22:12:05 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fe229f55c75d04148fec1b8ac835e71155fe2dd3019e89468cc5c509734f16`  
		Last Modified: Wed, 31 Mar 2021 22:12:12 GMT  
		Size: 61.3 MB (61285139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204ed1cc6a5bbd44e2efb4760a49c1f3e644d002db5219bc8d9c1b888b70109d`  
		Last Modified: Wed, 31 Mar 2021 22:12:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae808837ffae9d3b8c309d57301206b3429931fa761ee683970fe9e090a2df0`  
		Last Modified: Wed, 31 Mar 2021 22:12:04 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25d02fd28797c972a922f5db2d046c09dbc6633cba6cbe79aebc8cbec7f3118`  
		Last Modified: Wed, 31 Mar 2021 22:12:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:49d9e0cae396c3fafa0b6aa9c243467e9ce60ccb6d2c4eada9a7e934b41b4cea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113454707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4950472e9271c1fb2903a7c06a5534a838e7b50c0c5bcf21ba521f197e58a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 23:11:31 GMT
ADD file:65b5cf73b0b90f1f459a64d5706f2420deed7cdc5a9e13abacf5bcb05cc3138d in / 
# Tue, 30 Mar 2021 23:11:34 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:29:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 01:29:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:23:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 22:23:48 GMT
ENV INFLUXDB_VERSION=1.7.11
# Wed, 31 Mar 2021 22:23:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 31 Mar 2021 22:24:01 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:24:02 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:24:03 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:24:06 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:24:07 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:24:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:24:09 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:80ad3ae4821828f32ce9b3e0f76c3c8f157a7f111e64ffad3ba40287904dfc63`  
		Last Modified: Tue, 30 Mar 2021 23:18:47 GMT  
		Size: 42.1 MB (42120250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b448d9cdc0300784b14c4a254300d86c316aca568d8b068cdc585ff456ccca`  
		Last Modified: Wed, 31 Mar 2021 01:39:43 GMT  
		Size: 9.9 MB (9939722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3845e857248fe8de10609204e4eb4db8efcbb33c6a2f9e10b7d3efe4c3c625be`  
		Last Modified: Wed, 31 Mar 2021 01:39:41 GMT  
		Size: 3.9 MB (3921214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a177cdea9c8b927ab242f3d48404d79f201eae96cb5226a0939a0177356b64`  
		Last Modified: Wed, 31 Mar 2021 22:24:56 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e299c4e7f28f26deb843476cfbfb80a68e59de79da7c44abb9f852f548587b`  
		Last Modified: Wed, 31 Mar 2021 22:25:15 GMT  
		Size: 57.5 MB (57468950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de7fed255648802072e4472c84624c39f8c3c0fdc51fb4759055d012419e239`  
		Last Modified: Wed, 31 Mar 2021 22:24:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b2e89c38a1ae59f304ae4045b3f0df5b3034cbb876c30d5afb7f22c1f678cb`  
		Last Modified: Wed, 31 Mar 2021 22:24:56 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d35dca3fb12085be2e54a9f52f1edab20f89e77ceeffaea6828d0573952dbe`  
		Last Modified: Wed, 31 Mar 2021 22:24:56 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:fd1c2692d3deac68fbece7af5d753d7549547679cfce3b28f97a19a1020ec3f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114684365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f3cacb0410ac244ddeb9903901043b6799c98429d7ca95f128a6d540327c92`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:45 GMT
ADD file:0546f28e5d1be54699d1e0756275203da731735b3212f2ff1a87cd7f8dcc9049 in / 
# Tue, 30 Mar 2021 21:49:50 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 00:22:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 17:12:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 17:12:07 GMT
ENV INFLUXDB_VERSION=1.7.11
# Wed, 31 Mar 2021 17:12:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 31 Mar 2021 17:12:18 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 17:12:19 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 17:12:20 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 17:12:21 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 31 Mar 2021 17:12:22 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 17:12:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 17:12:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9317dc7ea567b49ade0ea730b5530d1363b065549e8b75a198e0b60bdde1f1d7`  
		Last Modified: Tue, 30 Mar 2021 21:56:46 GMT  
		Size: 43.2 MB (43177588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaf1b7b1bdfdc23af33da7d1fc9670524e63a8408bb04de9aebdf95979c5635`  
		Last Modified: Wed, 31 Mar 2021 00:33:12 GMT  
		Size: 10.2 MB (10201033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4446041554682b465ef9a0e853a5067e7d794fa1c840946d140beab2ddeb51`  
		Last Modified: Wed, 31 Mar 2021 00:33:09 GMT  
		Size: 4.1 MB (4096741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf88a824acc9fb8f6c222255ac308ae4dfd9c222a1ee0f5fcaed4052bffdc2c`  
		Last Modified: Wed, 31 Mar 2021 17:13:54 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66330e82421685243f1c9c216071cf6568161133c0644aaa2b4649fdebbbce8a`  
		Last Modified: Wed, 31 Mar 2021 17:14:02 GMT  
		Size: 57.2 MB (57204433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9792ecea67c37f0d03c6e735fda5a7d9a5ceabd9fa10d35d923eca3e677602d4`  
		Last Modified: Wed, 31 Mar 2021 17:13:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac9e14cd87085573645cfa79b670384878e25407ac5f6142396c51f46001ecf`  
		Last Modified: Wed, 31 Mar 2021 17:13:50 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6bfe85754d6fd61c49da9c76d167de65c5bb11e9b2b44cc13297f28e83e49d`  
		Last Modified: Wed, 31 Mar 2021 17:13:54 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-alpine`

```console
$ docker pull influxdb@sha256:14f4a7c83857b98a3f5402d8dea9a5564111ebd2d6b9a3e165152e62d6836e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:08732827457617517197f74bc65fa519e47cfd8c47fcdc39fe36606cca631f7c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65267191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099d42999ea27b9d0b279171f9b7ac536b5fa2ebce78475c87ba5f6e5f6a9722`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:08:44 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 31 Mar 2021 22:08:44 GMT
ENV INFLUXDB_VERSION=1.7.11
# Wed, 31 Mar 2021 22:08:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 31 Mar 2021 22:08:52 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:08:52 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:08:53 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:08:53 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:08:53 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:08:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:08:53 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f9e539bb1e7629825670530d6a7fea3f07e8044425ad739925c87c1c5ea1cc`  
		Last Modified: Wed, 31 Mar 2021 22:12:25 GMT  
		Size: 1.4 MB (1430776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df027f94023cc7e7d827fdc9dc559016431cccc18b46c2b5ec3bf3ad3025b40`  
		Last Modified: Wed, 31 Mar 2021 22:12:33 GMT  
		Size: 61.0 MB (61034808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b12a3946b3154d850e27b95f9db09516f61a3411aa78ad2970fbcb9cf64c67`  
		Last Modified: Wed, 31 Mar 2021 22:12:25 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7188cf87728f0d8de2c9759dff4d6f1b35685198b881ad83aebee559d3fe8c76`  
		Last Modified: Wed, 31 Mar 2021 22:12:24 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63842ef6831999dd7be9273c3e6aee0aeefe6a88ca33ee0a3aa0b52e4020974`  
		Last Modified: Wed, 31 Mar 2021 22:12:24 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-data`

```console
$ docker pull influxdb@sha256:d507cb256a6a6b8ca17ffabe20986e5382ded1dd9a532f402d4218eff561d780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:c3341b412977924bdc8484f185046542ab731e235748c95bfa8e878f3d717958
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (148962754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d426c4f0f5b924c2547e987e355eb133777d6308e22baf3b45bd12736dd1cfe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:08:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:08:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:08:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 22:08:57 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Wed, 31 Mar 2021 22:09:05 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 31 Mar 2021 22:09:06 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:09:06 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:09:06 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:09:06 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:09:06 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:09:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:09:07 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61ad49fa9961d6dfe53dc067fd690133f205498e8045e8f7ef6b9da0d42bd2`  
		Last Modified: Tue, 30 Mar 2021 23:17:25 GMT  
		Size: 11.3 MB (11286658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af62e04c0f85ed10801df4314d8cb9ba5e6c391f6a3c1db1080a0a78c8d4ed9d`  
		Last Modified: Tue, 30 Mar 2021 23:17:23 GMT  
		Size: 4.3 MB (4342466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ea2dd79e17761ed8d11e98f7420d9d909dcbc0ca1fe34ad492f5e495302a6`  
		Last Modified: Wed, 31 Mar 2021 22:12:05 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb8919f186b5a8340d78d89d2083bfcd6dd2e0107e8ab48802da21a7fbba6e1`  
		Last Modified: Wed, 31 Mar 2021 22:12:56 GMT  
		Size: 87.9 MB (87949054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175bae23aeb0fea9576ffe885c43c49f5838be31217c29159a990ce9478774ac`  
		Last Modified: Wed, 31 Mar 2021 22:12:44 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10c5997fe7fb0b6ac832345928733a2b85d87c9598189239cff7139e4041bee`  
		Last Modified: Wed, 31 Mar 2021 22:12:44 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d76baf07fe872379eb4b03f31ab336216d5febd316f61b2fc3251292bd8bca`  
		Last Modified: Wed, 31 Mar 2021 22:12:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-data-alpine`

```console
$ docker pull influxdb@sha256:abe0e9f69df0e94ba5c4f0f924f82782513a320d058de5da04d595c1e47f4f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:0babcaeb252ea080270753d6e921a4962fff72fceeb268d97fc82d92a1a766fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91871270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7cd3686c8a7ec423f870ddfc41eaeedbfc665c7a6ec3ae588af83ab66be7932`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:08:44 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 31 Mar 2021 22:09:10 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Wed, 31 Mar 2021 22:09:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 31 Mar 2021 22:09:20 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:09:20 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:09:21 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:09:21 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:09:21 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:09:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:09:21 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f9e539bb1e7629825670530d6a7fea3f07e8044425ad739925c87c1c5ea1cc`  
		Last Modified: Wed, 31 Mar 2021 22:12:25 GMT  
		Size: 1.4 MB (1430776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8074b4c793b1fc0dc52a235b578beb8276324c843e948dd001ade08f066614d`  
		Last Modified: Wed, 31 Mar 2021 22:13:21 GMT  
		Size: 87.6 MB (87638832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb6605109dc0463b08970c58ecba64249d63b77887a6fc484f5fdf51ae9d841`  
		Last Modified: Wed, 31 Mar 2021 22:13:10 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c8c9359c2fdc210c0edd9f0cde9a59b5e93d0b9e68e9be299383bf0a20c27e`  
		Last Modified: Wed, 31 Mar 2021 22:13:10 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12161952457fe52630344ae9061a2af64b1e21e17b891ab2164e95fa9173de4`  
		Last Modified: Wed, 31 Mar 2021 22:13:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-meta`

```console
$ docker pull influxdb@sha256:e14c106ff385882d294e3de7b3b4b6d1ccc711874e42987a0c355033a7540b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:98bca5c69869c7e38a944b7a4946c004ec6ebbdde41ceb6d84f4b203254f8a78
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84146142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839200c33d3be5eec372d3ccdb6cbe5901764ffda491d43b430cb6020e81de40`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:08:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:08:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:08:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 22:08:57 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Wed, 31 Mar 2021 22:09:29 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 31 Mar 2021 22:09:30 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 31 Mar 2021 22:09:30 GMT
EXPOSE 8091
# Wed, 31 Mar 2021 22:09:30 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:09:30 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:09:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:09:30 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61ad49fa9961d6dfe53dc067fd690133f205498e8045e8f7ef6b9da0d42bd2`  
		Last Modified: Tue, 30 Mar 2021 23:17:25 GMT  
		Size: 11.3 MB (11286658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af62e04c0f85ed10801df4314d8cb9ba5e6c391f6a3c1db1080a0a78c8d4ed9d`  
		Last Modified: Tue, 30 Mar 2021 23:17:23 GMT  
		Size: 4.3 MB (4342466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ea2dd79e17761ed8d11e98f7420d9d909dcbc0ca1fe34ad492f5e495302a6`  
		Last Modified: Wed, 31 Mar 2021 22:12:05 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cdef65d59a05bbbc1936a8bd8dd1a2df472e8c0611364d14ed8ab0a9f975f0`  
		Last Modified: Wed, 31 Mar 2021 22:13:38 GMT  
		Size: 23.1 MB (23133649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7c04f53ef80f9803f0ec13b925ebb42d81e93f88d161612e70476f82ecfbb1`  
		Last Modified: Wed, 31 Mar 2021 22:13:34 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9093f77d368c10feaa32a0429c2f5406ae03e15113d81c81339986052126b0e0`  
		Last Modified: Wed, 31 Mar 2021 22:13:35 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-meta-alpine`

```console
$ docker pull influxdb@sha256:b9c02b15a4ebfc411c7900a5271d81904c7eb2393dfc065a46021c45730af4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:1d0f01a617b837387e825db777a30cef1275da776cbf23e89d8653582dfd49d5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27234205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892428501a1c824208618881e321792e21ed6ae902fa27e272a5329f33e178c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:08:44 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 31 Mar 2021 22:09:10 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Wed, 31 Mar 2021 22:09:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 31 Mar 2021 22:09:38 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 31 Mar 2021 22:09:39 GMT
EXPOSE 8091
# Wed, 31 Mar 2021 22:09:39 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:09:39 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:09:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:09:39 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f9e539bb1e7629825670530d6a7fea3f07e8044425ad739925c87c1c5ea1cc`  
		Last Modified: Wed, 31 Mar 2021 22:12:25 GMT  
		Size: 1.4 MB (1430776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a157febdb22e8a46d480f9e82ebef69aa9e959265c0292473e355b10748e6335`  
		Last Modified: Wed, 31 Mar 2021 22:13:52 GMT  
		Size: 23.0 MB (23002968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee362e5190b6f898d3de8ff583eea76456081adc7a12d191ec93286eaa46f82b`  
		Last Modified: Wed, 31 Mar 2021 22:13:49 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fec40d69538b961e54ea88c7abe6da519a52675fbda2b07563f8d0fbcf0d91a`  
		Last Modified: Wed, 31 Mar 2021 22:13:49 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.11`

```console
$ docker pull influxdb@sha256:5580120fd73fb9730224d50df5045abeb03aecff94be99c3436de1b40ecdd500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7.11` - linux; amd64

```console
$ docker pull influxdb@sha256:085e385bfa2ba565ab08f8cd2f0da84dd82aa4e17005474bb4d4a9742bc041c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122298781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12bc503b20833ec67f59ab266430f7271bfee129944caf515bd6fb8eb793e9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:08:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:08:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:08:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 22:08:33 GMT
ENV INFLUXDB_VERSION=1.7.11
# Wed, 31 Mar 2021 22:08:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 31 Mar 2021 22:08:37 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:08:37 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:08:37 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:08:38 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:08:38 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:08:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:08:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61ad49fa9961d6dfe53dc067fd690133f205498e8045e8f7ef6b9da0d42bd2`  
		Last Modified: Tue, 30 Mar 2021 23:17:25 GMT  
		Size: 11.3 MB (11286658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af62e04c0f85ed10801df4314d8cb9ba5e6c391f6a3c1db1080a0a78c8d4ed9d`  
		Last Modified: Tue, 30 Mar 2021 23:17:23 GMT  
		Size: 4.3 MB (4342466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ea2dd79e17761ed8d11e98f7420d9d909dcbc0ca1fe34ad492f5e495302a6`  
		Last Modified: Wed, 31 Mar 2021 22:12:05 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fe229f55c75d04148fec1b8ac835e71155fe2dd3019e89468cc5c509734f16`  
		Last Modified: Wed, 31 Mar 2021 22:12:12 GMT  
		Size: 61.3 MB (61285139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204ed1cc6a5bbd44e2efb4760a49c1f3e644d002db5219bc8d9c1b888b70109d`  
		Last Modified: Wed, 31 Mar 2021 22:12:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae808837ffae9d3b8c309d57301206b3429931fa761ee683970fe9e090a2df0`  
		Last Modified: Wed, 31 Mar 2021 22:12:04 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25d02fd28797c972a922f5db2d046c09dbc6633cba6cbe79aebc8cbec7f3118`  
		Last Modified: Wed, 31 Mar 2021 22:12:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.11` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:49d9e0cae396c3fafa0b6aa9c243467e9ce60ccb6d2c4eada9a7e934b41b4cea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113454707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4950472e9271c1fb2903a7c06a5534a838e7b50c0c5bcf21ba521f197e58a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 23:11:31 GMT
ADD file:65b5cf73b0b90f1f459a64d5706f2420deed7cdc5a9e13abacf5bcb05cc3138d in / 
# Tue, 30 Mar 2021 23:11:34 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:29:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 01:29:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:23:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 22:23:48 GMT
ENV INFLUXDB_VERSION=1.7.11
# Wed, 31 Mar 2021 22:23:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 31 Mar 2021 22:24:01 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:24:02 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:24:03 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:24:06 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:24:07 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:24:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:24:09 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:80ad3ae4821828f32ce9b3e0f76c3c8f157a7f111e64ffad3ba40287904dfc63`  
		Last Modified: Tue, 30 Mar 2021 23:18:47 GMT  
		Size: 42.1 MB (42120250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b448d9cdc0300784b14c4a254300d86c316aca568d8b068cdc585ff456ccca`  
		Last Modified: Wed, 31 Mar 2021 01:39:43 GMT  
		Size: 9.9 MB (9939722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3845e857248fe8de10609204e4eb4db8efcbb33c6a2f9e10b7d3efe4c3c625be`  
		Last Modified: Wed, 31 Mar 2021 01:39:41 GMT  
		Size: 3.9 MB (3921214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a177cdea9c8b927ab242f3d48404d79f201eae96cb5226a0939a0177356b64`  
		Last Modified: Wed, 31 Mar 2021 22:24:56 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e299c4e7f28f26deb843476cfbfb80a68e59de79da7c44abb9f852f548587b`  
		Last Modified: Wed, 31 Mar 2021 22:25:15 GMT  
		Size: 57.5 MB (57468950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de7fed255648802072e4472c84624c39f8c3c0fdc51fb4759055d012419e239`  
		Last Modified: Wed, 31 Mar 2021 22:24:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b2e89c38a1ae59f304ae4045b3f0df5b3034cbb876c30d5afb7f22c1f678cb`  
		Last Modified: Wed, 31 Mar 2021 22:24:56 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d35dca3fb12085be2e54a9f52f1edab20f89e77ceeffaea6828d0573952dbe`  
		Last Modified: Wed, 31 Mar 2021 22:24:56 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:fd1c2692d3deac68fbece7af5d753d7549547679cfce3b28f97a19a1020ec3f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114684365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f3cacb0410ac244ddeb9903901043b6799c98429d7ca95f128a6d540327c92`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:45 GMT
ADD file:0546f28e5d1be54699d1e0756275203da731735b3212f2ff1a87cd7f8dcc9049 in / 
# Tue, 30 Mar 2021 21:49:50 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 00:22:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 17:12:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 17:12:07 GMT
ENV INFLUXDB_VERSION=1.7.11
# Wed, 31 Mar 2021 17:12:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 31 Mar 2021 17:12:18 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 17:12:19 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 17:12:20 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 17:12:21 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 31 Mar 2021 17:12:22 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 17:12:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 17:12:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9317dc7ea567b49ade0ea730b5530d1363b065549e8b75a198e0b60bdde1f1d7`  
		Last Modified: Tue, 30 Mar 2021 21:56:46 GMT  
		Size: 43.2 MB (43177588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaf1b7b1bdfdc23af33da7d1fc9670524e63a8408bb04de9aebdf95979c5635`  
		Last Modified: Wed, 31 Mar 2021 00:33:12 GMT  
		Size: 10.2 MB (10201033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4446041554682b465ef9a0e853a5067e7d794fa1c840946d140beab2ddeb51`  
		Last Modified: Wed, 31 Mar 2021 00:33:09 GMT  
		Size: 4.1 MB (4096741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf88a824acc9fb8f6c222255ac308ae4dfd9c222a1ee0f5fcaed4052bffdc2c`  
		Last Modified: Wed, 31 Mar 2021 17:13:54 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66330e82421685243f1c9c216071cf6568161133c0644aaa2b4649fdebbbce8a`  
		Last Modified: Wed, 31 Mar 2021 17:14:02 GMT  
		Size: 57.2 MB (57204433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9792ecea67c37f0d03c6e735fda5a7d9a5ceabd9fa10d35d923eca3e677602d4`  
		Last Modified: Wed, 31 Mar 2021 17:13:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac9e14cd87085573645cfa79b670384878e25407ac5f6142396c51f46001ecf`  
		Last Modified: Wed, 31 Mar 2021 17:13:50 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6bfe85754d6fd61c49da9c76d167de65c5bb11e9b2b44cc13297f28e83e49d`  
		Last Modified: Wed, 31 Mar 2021 17:13:54 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.11-alpine`

```console
$ docker pull influxdb@sha256:14f4a7c83857b98a3f5402d8dea9a5564111ebd2d6b9a3e165152e62d6836e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.11-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:08732827457617517197f74bc65fa519e47cfd8c47fcdc39fe36606cca631f7c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65267191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099d42999ea27b9d0b279171f9b7ac536b5fa2ebce78475c87ba5f6e5f6a9722`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:08:44 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 31 Mar 2021 22:08:44 GMT
ENV INFLUXDB_VERSION=1.7.11
# Wed, 31 Mar 2021 22:08:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 31 Mar 2021 22:08:52 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:08:52 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:08:53 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:08:53 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:08:53 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:08:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:08:53 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f9e539bb1e7629825670530d6a7fea3f07e8044425ad739925c87c1c5ea1cc`  
		Last Modified: Wed, 31 Mar 2021 22:12:25 GMT  
		Size: 1.4 MB (1430776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df027f94023cc7e7d827fdc9dc559016431cccc18b46c2b5ec3bf3ad3025b40`  
		Last Modified: Wed, 31 Mar 2021 22:12:33 GMT  
		Size: 61.0 MB (61034808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b12a3946b3154d850e27b95f9db09516f61a3411aa78ad2970fbcb9cf64c67`  
		Last Modified: Wed, 31 Mar 2021 22:12:25 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7188cf87728f0d8de2c9759dff4d6f1b35685198b881ad83aebee559d3fe8c76`  
		Last Modified: Wed, 31 Mar 2021 22:12:24 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63842ef6831999dd7be9273c3e6aee0aeefe6a88ca33ee0a3aa0b52e4020974`  
		Last Modified: Wed, 31 Mar 2021 22:12:24 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.11-data`

```console
$ docker pull influxdb@sha256:d507cb256a6a6b8ca17ffabe20986e5382ded1dd9a532f402d4218eff561d780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:c3341b412977924bdc8484f185046542ab731e235748c95bfa8e878f3d717958
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (148962754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d426c4f0f5b924c2547e987e355eb133777d6308e22baf3b45bd12736dd1cfe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:08:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:08:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:08:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 22:08:57 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Wed, 31 Mar 2021 22:09:05 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 31 Mar 2021 22:09:06 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:09:06 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:09:06 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:09:06 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:09:06 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:09:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:09:07 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61ad49fa9961d6dfe53dc067fd690133f205498e8045e8f7ef6b9da0d42bd2`  
		Last Modified: Tue, 30 Mar 2021 23:17:25 GMT  
		Size: 11.3 MB (11286658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af62e04c0f85ed10801df4314d8cb9ba5e6c391f6a3c1db1080a0a78c8d4ed9d`  
		Last Modified: Tue, 30 Mar 2021 23:17:23 GMT  
		Size: 4.3 MB (4342466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ea2dd79e17761ed8d11e98f7420d9d909dcbc0ca1fe34ad492f5e495302a6`  
		Last Modified: Wed, 31 Mar 2021 22:12:05 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb8919f186b5a8340d78d89d2083bfcd6dd2e0107e8ab48802da21a7fbba6e1`  
		Last Modified: Wed, 31 Mar 2021 22:12:56 GMT  
		Size: 87.9 MB (87949054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175bae23aeb0fea9576ffe885c43c49f5838be31217c29159a990ce9478774ac`  
		Last Modified: Wed, 31 Mar 2021 22:12:44 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10c5997fe7fb0b6ac832345928733a2b85d87c9598189239cff7139e4041bee`  
		Last Modified: Wed, 31 Mar 2021 22:12:44 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d76baf07fe872379eb4b03f31ab336216d5febd316f61b2fc3251292bd8bca`  
		Last Modified: Wed, 31 Mar 2021 22:12:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.11-data-alpine`

```console
$ docker pull influxdb@sha256:abe0e9f69df0e94ba5c4f0f924f82782513a320d058de5da04d595c1e47f4f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:0babcaeb252ea080270753d6e921a4962fff72fceeb268d97fc82d92a1a766fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91871270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7cd3686c8a7ec423f870ddfc41eaeedbfc665c7a6ec3ae588af83ab66be7932`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:08:44 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 31 Mar 2021 22:09:10 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Wed, 31 Mar 2021 22:09:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 31 Mar 2021 22:09:20 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:09:20 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:09:21 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:09:21 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:09:21 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:09:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:09:21 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f9e539bb1e7629825670530d6a7fea3f07e8044425ad739925c87c1c5ea1cc`  
		Last Modified: Wed, 31 Mar 2021 22:12:25 GMT  
		Size: 1.4 MB (1430776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8074b4c793b1fc0dc52a235b578beb8276324c843e948dd001ade08f066614d`  
		Last Modified: Wed, 31 Mar 2021 22:13:21 GMT  
		Size: 87.6 MB (87638832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb6605109dc0463b08970c58ecba64249d63b77887a6fc484f5fdf51ae9d841`  
		Last Modified: Wed, 31 Mar 2021 22:13:10 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c8c9359c2fdc210c0edd9f0cde9a59b5e93d0b9e68e9be299383bf0a20c27e`  
		Last Modified: Wed, 31 Mar 2021 22:13:10 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12161952457fe52630344ae9061a2af64b1e21e17b891ab2164e95fa9173de4`  
		Last Modified: Wed, 31 Mar 2021 22:13:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.11-meta`

```console
$ docker pull influxdb@sha256:e14c106ff385882d294e3de7b3b4b6d1ccc711874e42987a0c355033a7540b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:98bca5c69869c7e38a944b7a4946c004ec6ebbdde41ceb6d84f4b203254f8a78
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84146142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839200c33d3be5eec372d3ccdb6cbe5901764ffda491d43b430cb6020e81de40`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:08:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:08:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:08:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 22:08:57 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Wed, 31 Mar 2021 22:09:29 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 31 Mar 2021 22:09:30 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 31 Mar 2021 22:09:30 GMT
EXPOSE 8091
# Wed, 31 Mar 2021 22:09:30 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:09:30 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:09:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:09:30 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61ad49fa9961d6dfe53dc067fd690133f205498e8045e8f7ef6b9da0d42bd2`  
		Last Modified: Tue, 30 Mar 2021 23:17:25 GMT  
		Size: 11.3 MB (11286658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af62e04c0f85ed10801df4314d8cb9ba5e6c391f6a3c1db1080a0a78c8d4ed9d`  
		Last Modified: Tue, 30 Mar 2021 23:17:23 GMT  
		Size: 4.3 MB (4342466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ea2dd79e17761ed8d11e98f7420d9d909dcbc0ca1fe34ad492f5e495302a6`  
		Last Modified: Wed, 31 Mar 2021 22:12:05 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cdef65d59a05bbbc1936a8bd8dd1a2df472e8c0611364d14ed8ab0a9f975f0`  
		Last Modified: Wed, 31 Mar 2021 22:13:38 GMT  
		Size: 23.1 MB (23133649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7c04f53ef80f9803f0ec13b925ebb42d81e93f88d161612e70476f82ecfbb1`  
		Last Modified: Wed, 31 Mar 2021 22:13:34 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9093f77d368c10feaa32a0429c2f5406ae03e15113d81c81339986052126b0e0`  
		Last Modified: Wed, 31 Mar 2021 22:13:35 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.11-meta-alpine`

```console
$ docker pull influxdb@sha256:b9c02b15a4ebfc411c7900a5271d81904c7eb2393dfc065a46021c45730af4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:1d0f01a617b837387e825db777a30cef1275da776cbf23e89d8653582dfd49d5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27234205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892428501a1c824208618881e321792e21ed6ae902fa27e272a5329f33e178c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:08:44 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 31 Mar 2021 22:09:10 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Wed, 31 Mar 2021 22:09:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 31 Mar 2021 22:09:38 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 31 Mar 2021 22:09:39 GMT
EXPOSE 8091
# Wed, 31 Mar 2021 22:09:39 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:09:39 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:09:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:09:39 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f9e539bb1e7629825670530d6a7fea3f07e8044425ad739925c87c1c5ea1cc`  
		Last Modified: Wed, 31 Mar 2021 22:12:25 GMT  
		Size: 1.4 MB (1430776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a157febdb22e8a46d480f9e82ebef69aa9e959265c0292473e355b10748e6335`  
		Last Modified: Wed, 31 Mar 2021 22:13:52 GMT  
		Size: 23.0 MB (23002968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee362e5190b6f898d3de8ff583eea76456081adc7a12d191ec93286eaa46f82b`  
		Last Modified: Wed, 31 Mar 2021 22:13:49 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fec40d69538b961e54ea88c7abe6da519a52675fbda2b07563f8d0fbcf0d91a`  
		Last Modified: Wed, 31 Mar 2021 22:13:49 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8`

```console
$ docker pull influxdb@sha256:2fad3a39ce1bcfe2653bebab8a364382c91b72ac23ca7c3eb902f8243dc147b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8` - linux; amd64

```console
$ docker pull influxdb@sha256:1e56e8397d8a4dfb0976c4e838d13752bad8c6d12c703cbc602d6f62b66d3cbe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125980433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32270dcd881f7082ff2c40edee89c96e4a588745100b56814f1827370be7346d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:08:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:08:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:08:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 22:09:43 GMT
ENV INFLUXDB_VERSION=1.8.4
# Wed, 31 Mar 2021 22:09:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 31 Mar 2021 22:09:48 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:09:49 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:09:49 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:09:49 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:09:49 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:09:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:09:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61ad49fa9961d6dfe53dc067fd690133f205498e8045e8f7ef6b9da0d42bd2`  
		Last Modified: Tue, 30 Mar 2021 23:17:25 GMT  
		Size: 11.3 MB (11286658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af62e04c0f85ed10801df4314d8cb9ba5e6c391f6a3c1db1080a0a78c8d4ed9d`  
		Last Modified: Tue, 30 Mar 2021 23:17:23 GMT  
		Size: 4.3 MB (4342466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ea2dd79e17761ed8d11e98f7420d9d909dcbc0ca1fe34ad492f5e495302a6`  
		Last Modified: Wed, 31 Mar 2021 22:12:05 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9b858efb0b11f8f11c90b664ca3a7908f7eb9bf558303496e14edd293e9185`  
		Last Modified: Wed, 31 Mar 2021 22:14:14 GMT  
		Size: 65.0 MB (64966792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25ac85aa53d757d16652d2d471e78dc9620da1f878ef9847c9f90fb98b6caad`  
		Last Modified: Wed, 31 Mar 2021 22:14:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d214a7ad757b11f3bfdbaa89e9d074c4a7fd5ff316182c6accca8749fe5351`  
		Last Modified: Wed, 31 Mar 2021 22:14:06 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a797563c924c918d19c78efa451650fbfef9533776ce3ca21f8d7815d6f0cd4c`  
		Last Modified: Wed, 31 Mar 2021 22:14:06 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:4441068a546cda688fedd1f8746b60d2f8da5aa0fb3c161de2ef2859414e8b3e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117045739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366e5c0bc8282c0853c96618002003a4f872a516d1ad403216a291e944df890f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 23:11:31 GMT
ADD file:65b5cf73b0b90f1f459a64d5706f2420deed7cdc5a9e13abacf5bcb05cc3138d in / 
# Tue, 30 Mar 2021 23:11:34 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:29:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 01:29:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:23:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 22:24:20 GMT
ENV INFLUXDB_VERSION=1.8.4
# Wed, 31 Mar 2021 22:24:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 31 Mar 2021 22:24:36 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:24:37 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:24:38 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:24:39 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:24:39 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:24:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:80ad3ae4821828f32ce9b3e0f76c3c8f157a7f111e64ffad3ba40287904dfc63`  
		Last Modified: Tue, 30 Mar 2021 23:18:47 GMT  
		Size: 42.1 MB (42120250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b448d9cdc0300784b14c4a254300d86c316aca568d8b068cdc585ff456ccca`  
		Last Modified: Wed, 31 Mar 2021 01:39:43 GMT  
		Size: 9.9 MB (9939722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3845e857248fe8de10609204e4eb4db8efcbb33c6a2f9e10b7d3efe4c3c625be`  
		Last Modified: Wed, 31 Mar 2021 01:39:41 GMT  
		Size: 3.9 MB (3921214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a177cdea9c8b927ab242f3d48404d79f201eae96cb5226a0939a0177356b64`  
		Last Modified: Wed, 31 Mar 2021 22:24:56 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650334722a7c4c89b651c6e30e02a1764fac9c00aa08648f5e350b208ed31e03`  
		Last Modified: Wed, 31 Mar 2021 22:25:43 GMT  
		Size: 61.1 MB (61059979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aeb203c968b1cab8815970da286e4b28fb74667ffadafe52129920f64f5222d`  
		Last Modified: Wed, 31 Mar 2021 22:25:23 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213e81d9e7ad47c4f8dcea7ddd5ea77b295035fa0fbfe05108eb036adb64b29f`  
		Last Modified: Wed, 31 Mar 2021 22:25:22 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f533a698ed54ac7064cfb3c42ac923a6b24fda3265f705d0c7719d18800d1fc6`  
		Last Modified: Wed, 31 Mar 2021 22:25:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:781ea6ca32fdfe2c121b4dc47ce17ebd870ea448e1561976e6742895e560a92c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118109154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650e2561a1c44aae5fe2b89c1a6599bd56822bf333ab9c81000c2c294f525399`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:45 GMT
ADD file:0546f28e5d1be54699d1e0756275203da731735b3212f2ff1a87cd7f8dcc9049 in / 
# Tue, 30 Mar 2021 21:49:50 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 00:22:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 17:12:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 17:12:33 GMT
ENV INFLUXDB_VERSION=1.8.4
# Wed, 31 Mar 2021 17:12:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 31 Mar 2021 17:12:44 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 17:12:45 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 17:12:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 17:12:47 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 31 Mar 2021 17:12:48 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 17:12:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 17:12:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9317dc7ea567b49ade0ea730b5530d1363b065549e8b75a198e0b60bdde1f1d7`  
		Last Modified: Tue, 30 Mar 2021 21:56:46 GMT  
		Size: 43.2 MB (43177588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaf1b7b1bdfdc23af33da7d1fc9670524e63a8408bb04de9aebdf95979c5635`  
		Last Modified: Wed, 31 Mar 2021 00:33:12 GMT  
		Size: 10.2 MB (10201033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4446041554682b465ef9a0e853a5067e7d794fa1c840946d140beab2ddeb51`  
		Last Modified: Wed, 31 Mar 2021 00:33:09 GMT  
		Size: 4.1 MB (4096741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf88a824acc9fb8f6c222255ac308ae4dfd9c222a1ee0f5fcaed4052bffdc2c`  
		Last Modified: Wed, 31 Mar 2021 17:13:54 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effc16879d2db69ffd1eeb7acb404cf305d677bf650263c2fa69959896c199e1`  
		Last Modified: Wed, 31 Mar 2021 17:14:25 GMT  
		Size: 60.6 MB (60629222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcca9a0237fd4dd309bb8f89cd2a77fe9b3a319c976d41348863523f85e3793`  
		Last Modified: Wed, 31 Mar 2021 17:14:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b534230d3f2e93044a487a712c1092ccbf5c29a9615c1d7588316bb67f818e`  
		Last Modified: Wed, 31 Mar 2021 17:14:13 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f1561ad6adcd68374d79b0d000e63539bac0d6a6b46036bbe816a40351e46f`  
		Last Modified: Wed, 31 Mar 2021 17:14:12 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-alpine`

```console
$ docker pull influxdb@sha256:cafe33f7cd2450cb43483623abf12bcc13212af744d33304d7c03128e86dc81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cbdbbda6e5e6e03eb37653283d3888fcc7c2cac18d18863ca3d8d009f5b40295
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68939068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20af4836eea3bc3a24572d6b430a1c5b6414a0447d52d72933b03931290e5889`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:08:44 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 31 Mar 2021 22:09:53 GMT
ENV INFLUXDB_VERSION=1.8.4
# Wed, 31 Mar 2021 22:10:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 31 Mar 2021 22:10:01 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:10:01 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:10:01 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:10:01 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:10:01 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:10:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:10:02 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f9e539bb1e7629825670530d6a7fea3f07e8044425ad739925c87c1c5ea1cc`  
		Last Modified: Wed, 31 Mar 2021 22:12:25 GMT  
		Size: 1.4 MB (1430776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365703c3c3ec6f8c9e476dd6b99601cf6ac5982328158c8175029d2a7c497b88`  
		Last Modified: Wed, 31 Mar 2021 22:14:34 GMT  
		Size: 64.7 MB (64706686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c85993cc8327087ae49547d9f4fe7b90097bef116ae95f61fe513dae7d3e727`  
		Last Modified: Wed, 31 Mar 2021 22:14:25 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9124858c2b28014874cf0715909190e955c2ec3060bdf7c6b59507a8c1bc43`  
		Last Modified: Wed, 31 Mar 2021 22:14:25 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e093d985351a8e16fad3585fda3f1072d938d071c457c96aa5eb4000c4f8563`  
		Last Modified: Wed, 31 Mar 2021 22:14:25 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data`

```console
$ docker pull influxdb@sha256:c47990ad54cbab2c4b7ce6e5e34b87d517d46a6323f9bfc8abda198038602a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:f7e31854dd0ffbfa5ef8ac02df3abcf90ff84e89fff55ae0ceb82c4dc6208d16
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126810142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076db8957be42f4ddbd11be5d3b3ae5c80792bb2f5c5e547779208ccb54e9396`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:08:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:08:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:08:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 22:10:06 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 31 Mar 2021 22:10:12 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 31 Mar 2021 22:10:13 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:10:13 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:10:13 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:10:13 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:10:13 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:10:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:10:14 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61ad49fa9961d6dfe53dc067fd690133f205498e8045e8f7ef6b9da0d42bd2`  
		Last Modified: Tue, 30 Mar 2021 23:17:25 GMT  
		Size: 11.3 MB (11286658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af62e04c0f85ed10801df4314d8cb9ba5e6c391f6a3c1db1080a0a78c8d4ed9d`  
		Last Modified: Tue, 30 Mar 2021 23:17:23 GMT  
		Size: 4.3 MB (4342466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ea2dd79e17761ed8d11e98f7420d9d909dcbc0ca1fe34ad492f5e495302a6`  
		Last Modified: Wed, 31 Mar 2021 22:12:05 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d41b7827948e414f042e1b9178e16f0fe855f9c0a2043a884762561ebcc529c`  
		Last Modified: Wed, 31 Mar 2021 22:14:56 GMT  
		Size: 65.8 MB (65796441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd72595d8d8e4975ceb4c2dc6f49bd4d712750c83b2ea0306138ad9367dc582`  
		Last Modified: Wed, 31 Mar 2021 22:14:47 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd848f72b95e08bf0cad39dc3de90ba4fa88364406a9f418c8ee9dfd2faf08d`  
		Last Modified: Wed, 31 Mar 2021 22:14:47 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1657f716309bf8a123806bff8a8b445f5ed98211006d7fa2e159d9ea6a02b0`  
		Last Modified: Wed, 31 Mar 2021 22:14:47 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data-alpine`

```console
$ docker pull influxdb@sha256:53386503e99f45244c7335689f11135d7eaf40ba27aa3d4f11703e460edc0a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:25f64b07b44114d25994531b533b989a3bbbd11c9a9fde3b9b04d9df71ec7b7e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69773182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1867ac52349985be3abbd7d162bff782c417b699a51657b5b3a5d19bf7f957fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:08:44 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 31 Mar 2021 22:10:18 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 31 Mar 2021 22:10:26 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 31 Mar 2021 22:10:26 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:10:26 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:10:26 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:10:27 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:10:27 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:10:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:10:27 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f9e539bb1e7629825670530d6a7fea3f07e8044425ad739925c87c1c5ea1cc`  
		Last Modified: Wed, 31 Mar 2021 22:12:25 GMT  
		Size: 1.4 MB (1430776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a19954818447d2176905c41c281ada51d631cb2b450436c92e5fd159be05ea`  
		Last Modified: Wed, 31 Mar 2021 22:15:22 GMT  
		Size: 65.5 MB (65540744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c2436e61f7cc05d5259eb9f7dc8f4919f3727c50c673ff6176b39ba7bf45c4`  
		Last Modified: Wed, 31 Mar 2021 22:15:13 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e29dd894fbc5b5e36a12b37840fa84556a70b2a9a3c5c089536c38b81b8790`  
		Last Modified: Wed, 31 Mar 2021 22:15:13 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1873d4c45433d2f9e20a15bbed16c5d4edb18c976c4fe26eb3147a2569ca8e`  
		Last Modified: Wed, 31 Mar 2021 22:15:13 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-meta`

```console
$ docker pull influxdb@sha256:f2f779eec1a6dd4ecebccffa6d9cbfa16637f9f71855e12018326f61e9328bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:07f58b191138c487f7e05e370dae45ff3c77b29a7c353c59f1f5bd56de231d67
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83878780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6321e44de6670b2fa75aab6098396ff070902779c12bf9f1a7ed1edb8960ef8b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:08:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:08:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:08:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 22:10:06 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 31 Mar 2021 22:10:35 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 31 Mar 2021 22:10:35 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 31 Mar 2021 22:10:36 GMT
EXPOSE 8091
# Wed, 31 Mar 2021 22:10:36 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:10:36 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:10:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:10:36 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61ad49fa9961d6dfe53dc067fd690133f205498e8045e8f7ef6b9da0d42bd2`  
		Last Modified: Tue, 30 Mar 2021 23:17:25 GMT  
		Size: 11.3 MB (11286658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af62e04c0f85ed10801df4314d8cb9ba5e6c391f6a3c1db1080a0a78c8d4ed9d`  
		Last Modified: Tue, 30 Mar 2021 23:17:23 GMT  
		Size: 4.3 MB (4342466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ea2dd79e17761ed8d11e98f7420d9d909dcbc0ca1fe34ad492f5e495302a6`  
		Last Modified: Wed, 31 Mar 2021 22:12:05 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33184db9c22eb774767a5e0d59084338e22aa85921c99554dc03e64cd3a3cca3`  
		Last Modified: Wed, 31 Mar 2021 22:15:41 GMT  
		Size: 22.9 MB (22866284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0c565154abc635cf8741449ae2632fd60b8f8c800d91fbf82896af8c6620e0`  
		Last Modified: Wed, 31 Mar 2021 22:15:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cd9818c31165e7bf5db665dd7f1bab0d30fb5132e853a34afd94501ac7f730`  
		Last Modified: Wed, 31 Mar 2021 22:15:39 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-meta-alpine`

```console
$ docker pull influxdb@sha256:39aa359985fb3b4befb240e3c96f7cd364f82491637b981bd476d357c6334609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ed56a3d248256dd6ffded198ba68cb376670d09c36e465be2432ebc0a887005c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26966631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2f205931ae4121f85700a26ded6400cca220cf3cf8c5ffbd659767ee295496`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:08:44 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 31 Mar 2021 22:10:18 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 31 Mar 2021 22:10:44 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 31 Mar 2021 22:10:44 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 31 Mar 2021 22:10:45 GMT
EXPOSE 8091
# Wed, 31 Mar 2021 22:10:45 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:10:45 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:10:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:10:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f9e539bb1e7629825670530d6a7fea3f07e8044425ad739925c87c1c5ea1cc`  
		Last Modified: Wed, 31 Mar 2021 22:12:25 GMT  
		Size: 1.4 MB (1430776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec545b4936bf871f85c7c3c2800ebe59111c875cd2ed5f84a6e414ac5b99116e`  
		Last Modified: Wed, 31 Mar 2021 22:15:57 GMT  
		Size: 22.7 MB (22735394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8667c4944d3ed1b8e3f3ac5c388f8b312f34881190d9ae8c06adeedf575780e2`  
		Last Modified: Wed, 31 Mar 2021 22:15:54 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345ad36b894191aeac6a52143e6f0b96c7847a6cd3e82962022770ea6f63b857`  
		Last Modified: Wed, 31 Mar 2021 22:15:54 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-data`

```console
$ docker pull influxdb@sha256:c47990ad54cbab2c4b7ce6e5e34b87d517d46a6323f9bfc8abda198038602a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-data` - linux; amd64

```console
$ docker pull influxdb@sha256:f7e31854dd0ffbfa5ef8ac02df3abcf90ff84e89fff55ae0ceb82c4dc6208d16
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126810142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076db8957be42f4ddbd11be5d3b3ae5c80792bb2f5c5e547779208ccb54e9396`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:08:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:08:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:08:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 22:10:06 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 31 Mar 2021 22:10:12 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 31 Mar 2021 22:10:13 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:10:13 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:10:13 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:10:13 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:10:13 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:10:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:10:14 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61ad49fa9961d6dfe53dc067fd690133f205498e8045e8f7ef6b9da0d42bd2`  
		Last Modified: Tue, 30 Mar 2021 23:17:25 GMT  
		Size: 11.3 MB (11286658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af62e04c0f85ed10801df4314d8cb9ba5e6c391f6a3c1db1080a0a78c8d4ed9d`  
		Last Modified: Tue, 30 Mar 2021 23:17:23 GMT  
		Size: 4.3 MB (4342466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ea2dd79e17761ed8d11e98f7420d9d909dcbc0ca1fe34ad492f5e495302a6`  
		Last Modified: Wed, 31 Mar 2021 22:12:05 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d41b7827948e414f042e1b9178e16f0fe855f9c0a2043a884762561ebcc529c`  
		Last Modified: Wed, 31 Mar 2021 22:14:56 GMT  
		Size: 65.8 MB (65796441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd72595d8d8e4975ceb4c2dc6f49bd4d712750c83b2ea0306138ad9367dc582`  
		Last Modified: Wed, 31 Mar 2021 22:14:47 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd848f72b95e08bf0cad39dc3de90ba4fa88364406a9f418c8ee9dfd2faf08d`  
		Last Modified: Wed, 31 Mar 2021 22:14:47 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1657f716309bf8a123806bff8a8b445f5ed98211006d7fa2e159d9ea6a02b0`  
		Last Modified: Wed, 31 Mar 2021 22:14:47 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-data-alpine`

```console
$ docker pull influxdb@sha256:53386503e99f45244c7335689f11135d7eaf40ba27aa3d4f11703e460edc0a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:25f64b07b44114d25994531b533b989a3bbbd11c9a9fde3b9b04d9df71ec7b7e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69773182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1867ac52349985be3abbd7d162bff782c417b699a51657b5b3a5d19bf7f957fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:08:44 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 31 Mar 2021 22:10:18 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 31 Mar 2021 22:10:26 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 31 Mar 2021 22:10:26 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:10:26 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:10:26 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:10:27 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:10:27 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:10:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:10:27 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f9e539bb1e7629825670530d6a7fea3f07e8044425ad739925c87c1c5ea1cc`  
		Last Modified: Wed, 31 Mar 2021 22:12:25 GMT  
		Size: 1.4 MB (1430776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a19954818447d2176905c41c281ada51d631cb2b450436c92e5fd159be05ea`  
		Last Modified: Wed, 31 Mar 2021 22:15:22 GMT  
		Size: 65.5 MB (65540744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c2436e61f7cc05d5259eb9f7dc8f4919f3727c50c673ff6176b39ba7bf45c4`  
		Last Modified: Wed, 31 Mar 2021 22:15:13 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e29dd894fbc5b5e36a12b37840fa84556a70b2a9a3c5c089536c38b81b8790`  
		Last Modified: Wed, 31 Mar 2021 22:15:13 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1873d4c45433d2f9e20a15bbed16c5d4edb18c976c4fe26eb3147a2569ca8e`  
		Last Modified: Wed, 31 Mar 2021 22:15:13 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-meta`

```console
$ docker pull influxdb@sha256:f2f779eec1a6dd4ecebccffa6d9cbfa16637f9f71855e12018326f61e9328bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:07f58b191138c487f7e05e370dae45ff3c77b29a7c353c59f1f5bd56de231d67
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83878780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6321e44de6670b2fa75aab6098396ff070902779c12bf9f1a7ed1edb8960ef8b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:08:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:08:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:08:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 22:10:06 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 31 Mar 2021 22:10:35 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 31 Mar 2021 22:10:35 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 31 Mar 2021 22:10:36 GMT
EXPOSE 8091
# Wed, 31 Mar 2021 22:10:36 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:10:36 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:10:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:10:36 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61ad49fa9961d6dfe53dc067fd690133f205498e8045e8f7ef6b9da0d42bd2`  
		Last Modified: Tue, 30 Mar 2021 23:17:25 GMT  
		Size: 11.3 MB (11286658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af62e04c0f85ed10801df4314d8cb9ba5e6c391f6a3c1db1080a0a78c8d4ed9d`  
		Last Modified: Tue, 30 Mar 2021 23:17:23 GMT  
		Size: 4.3 MB (4342466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ea2dd79e17761ed8d11e98f7420d9d909dcbc0ca1fe34ad492f5e495302a6`  
		Last Modified: Wed, 31 Mar 2021 22:12:05 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33184db9c22eb774767a5e0d59084338e22aa85921c99554dc03e64cd3a3cca3`  
		Last Modified: Wed, 31 Mar 2021 22:15:41 GMT  
		Size: 22.9 MB (22866284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0c565154abc635cf8741449ae2632fd60b8f8c800d91fbf82896af8c6620e0`  
		Last Modified: Wed, 31 Mar 2021 22:15:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cd9818c31165e7bf5db665dd7f1bab0d30fb5132e853a34afd94501ac7f730`  
		Last Modified: Wed, 31 Mar 2021 22:15:39 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-meta-alpine`

```console
$ docker pull influxdb@sha256:39aa359985fb3b4befb240e3c96f7cd364f82491637b981bd476d357c6334609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ed56a3d248256dd6ffded198ba68cb376670d09c36e465be2432ebc0a887005c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26966631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2f205931ae4121f85700a26ded6400cca220cf3cf8c5ffbd659767ee295496`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:08:44 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 31 Mar 2021 22:10:18 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 31 Mar 2021 22:10:44 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 31 Mar 2021 22:10:44 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 31 Mar 2021 22:10:45 GMT
EXPOSE 8091
# Wed, 31 Mar 2021 22:10:45 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:10:45 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:10:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:10:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f9e539bb1e7629825670530d6a7fea3f07e8044425ad739925c87c1c5ea1cc`  
		Last Modified: Wed, 31 Mar 2021 22:12:25 GMT  
		Size: 1.4 MB (1430776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec545b4936bf871f85c7c3c2800ebe59111c875cd2ed5f84a6e414ac5b99116e`  
		Last Modified: Wed, 31 Mar 2021 22:15:57 GMT  
		Size: 22.7 MB (22735394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8667c4944d3ed1b8e3f3ac5c388f8b312f34881190d9ae8c06adeedf575780e2`  
		Last Modified: Wed, 31 Mar 2021 22:15:54 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345ad36b894191aeac6a52143e6f0b96c7847a6cd3e82962022770ea6f63b857`  
		Last Modified: Wed, 31 Mar 2021 22:15:54 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.4`

```console
$ docker pull influxdb@sha256:2fad3a39ce1bcfe2653bebab8a364382c91b72ac23ca7c3eb902f8243dc147b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8.4` - linux; amd64

```console
$ docker pull influxdb@sha256:1e56e8397d8a4dfb0976c4e838d13752bad8c6d12c703cbc602d6f62b66d3cbe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125980433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32270dcd881f7082ff2c40edee89c96e4a588745100b56814f1827370be7346d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:08:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:08:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:08:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 22:09:43 GMT
ENV INFLUXDB_VERSION=1.8.4
# Wed, 31 Mar 2021 22:09:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 31 Mar 2021 22:09:48 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:09:49 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:09:49 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:09:49 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:09:49 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:09:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:09:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61ad49fa9961d6dfe53dc067fd690133f205498e8045e8f7ef6b9da0d42bd2`  
		Last Modified: Tue, 30 Mar 2021 23:17:25 GMT  
		Size: 11.3 MB (11286658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af62e04c0f85ed10801df4314d8cb9ba5e6c391f6a3c1db1080a0a78c8d4ed9d`  
		Last Modified: Tue, 30 Mar 2021 23:17:23 GMT  
		Size: 4.3 MB (4342466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ea2dd79e17761ed8d11e98f7420d9d909dcbc0ca1fe34ad492f5e495302a6`  
		Last Modified: Wed, 31 Mar 2021 22:12:05 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9b858efb0b11f8f11c90b664ca3a7908f7eb9bf558303496e14edd293e9185`  
		Last Modified: Wed, 31 Mar 2021 22:14:14 GMT  
		Size: 65.0 MB (64966792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25ac85aa53d757d16652d2d471e78dc9620da1f878ef9847c9f90fb98b6caad`  
		Last Modified: Wed, 31 Mar 2021 22:14:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d214a7ad757b11f3bfdbaa89e9d074c4a7fd5ff316182c6accca8749fe5351`  
		Last Modified: Wed, 31 Mar 2021 22:14:06 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a797563c924c918d19c78efa451650fbfef9533776ce3ca21f8d7815d6f0cd4c`  
		Last Modified: Wed, 31 Mar 2021 22:14:06 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.4` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:4441068a546cda688fedd1f8746b60d2f8da5aa0fb3c161de2ef2859414e8b3e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117045739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366e5c0bc8282c0853c96618002003a4f872a516d1ad403216a291e944df890f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 23:11:31 GMT
ADD file:65b5cf73b0b90f1f459a64d5706f2420deed7cdc5a9e13abacf5bcb05cc3138d in / 
# Tue, 30 Mar 2021 23:11:34 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:29:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 01:29:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:23:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 22:24:20 GMT
ENV INFLUXDB_VERSION=1.8.4
# Wed, 31 Mar 2021 22:24:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 31 Mar 2021 22:24:36 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:24:37 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:24:38 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:24:39 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:24:39 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:24:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:80ad3ae4821828f32ce9b3e0f76c3c8f157a7f111e64ffad3ba40287904dfc63`  
		Last Modified: Tue, 30 Mar 2021 23:18:47 GMT  
		Size: 42.1 MB (42120250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b448d9cdc0300784b14c4a254300d86c316aca568d8b068cdc585ff456ccca`  
		Last Modified: Wed, 31 Mar 2021 01:39:43 GMT  
		Size: 9.9 MB (9939722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3845e857248fe8de10609204e4eb4db8efcbb33c6a2f9e10b7d3efe4c3c625be`  
		Last Modified: Wed, 31 Mar 2021 01:39:41 GMT  
		Size: 3.9 MB (3921214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a177cdea9c8b927ab242f3d48404d79f201eae96cb5226a0939a0177356b64`  
		Last Modified: Wed, 31 Mar 2021 22:24:56 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650334722a7c4c89b651c6e30e02a1764fac9c00aa08648f5e350b208ed31e03`  
		Last Modified: Wed, 31 Mar 2021 22:25:43 GMT  
		Size: 61.1 MB (61059979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aeb203c968b1cab8815970da286e4b28fb74667ffadafe52129920f64f5222d`  
		Last Modified: Wed, 31 Mar 2021 22:25:23 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213e81d9e7ad47c4f8dcea7ddd5ea77b295035fa0fbfe05108eb036adb64b29f`  
		Last Modified: Wed, 31 Mar 2021 22:25:22 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f533a698ed54ac7064cfb3c42ac923a6b24fda3265f705d0c7719d18800d1fc6`  
		Last Modified: Wed, 31 Mar 2021 22:25:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.4` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:781ea6ca32fdfe2c121b4dc47ce17ebd870ea448e1561976e6742895e560a92c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118109154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650e2561a1c44aae5fe2b89c1a6599bd56822bf333ab9c81000c2c294f525399`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:45 GMT
ADD file:0546f28e5d1be54699d1e0756275203da731735b3212f2ff1a87cd7f8dcc9049 in / 
# Tue, 30 Mar 2021 21:49:50 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 00:22:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 17:12:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 17:12:33 GMT
ENV INFLUXDB_VERSION=1.8.4
# Wed, 31 Mar 2021 17:12:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 31 Mar 2021 17:12:44 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 17:12:45 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 17:12:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 17:12:47 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 31 Mar 2021 17:12:48 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 17:12:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 17:12:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9317dc7ea567b49ade0ea730b5530d1363b065549e8b75a198e0b60bdde1f1d7`  
		Last Modified: Tue, 30 Mar 2021 21:56:46 GMT  
		Size: 43.2 MB (43177588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaf1b7b1bdfdc23af33da7d1fc9670524e63a8408bb04de9aebdf95979c5635`  
		Last Modified: Wed, 31 Mar 2021 00:33:12 GMT  
		Size: 10.2 MB (10201033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4446041554682b465ef9a0e853a5067e7d794fa1c840946d140beab2ddeb51`  
		Last Modified: Wed, 31 Mar 2021 00:33:09 GMT  
		Size: 4.1 MB (4096741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf88a824acc9fb8f6c222255ac308ae4dfd9c222a1ee0f5fcaed4052bffdc2c`  
		Last Modified: Wed, 31 Mar 2021 17:13:54 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effc16879d2db69ffd1eeb7acb404cf305d677bf650263c2fa69959896c199e1`  
		Last Modified: Wed, 31 Mar 2021 17:14:25 GMT  
		Size: 60.6 MB (60629222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcca9a0237fd4dd309bb8f89cd2a77fe9b3a319c976d41348863523f85e3793`  
		Last Modified: Wed, 31 Mar 2021 17:14:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b534230d3f2e93044a487a712c1092ccbf5c29a9615c1d7588316bb67f818e`  
		Last Modified: Wed, 31 Mar 2021 17:14:13 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f1561ad6adcd68374d79b0d000e63539bac0d6a6b46036bbe816a40351e46f`  
		Last Modified: Wed, 31 Mar 2021 17:14:12 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.4-alpine`

```console
$ docker pull influxdb@sha256:cafe33f7cd2450cb43483623abf12bcc13212af744d33304d7c03128e86dc81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.4-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cbdbbda6e5e6e03eb37653283d3888fcc7c2cac18d18863ca3d8d009f5b40295
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68939068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20af4836eea3bc3a24572d6b430a1c5b6414a0447d52d72933b03931290e5889`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:08:44 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 31 Mar 2021 22:09:53 GMT
ENV INFLUXDB_VERSION=1.8.4
# Wed, 31 Mar 2021 22:10:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 31 Mar 2021 22:10:01 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:10:01 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:10:01 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:10:01 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:10:01 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:10:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:10:02 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f9e539bb1e7629825670530d6a7fea3f07e8044425ad739925c87c1c5ea1cc`  
		Last Modified: Wed, 31 Mar 2021 22:12:25 GMT  
		Size: 1.4 MB (1430776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365703c3c3ec6f8c9e476dd6b99601cf6ac5982328158c8175029d2a7c497b88`  
		Last Modified: Wed, 31 Mar 2021 22:14:34 GMT  
		Size: 64.7 MB (64706686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c85993cc8327087ae49547d9f4fe7b90097bef116ae95f61fe513dae7d3e727`  
		Last Modified: Wed, 31 Mar 2021 22:14:25 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9124858c2b28014874cf0715909190e955c2ec3060bdf7c6b59507a8c1bc43`  
		Last Modified: Wed, 31 Mar 2021 22:14:25 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e093d985351a8e16fad3585fda3f1072d938d071c457c96aa5eb4000c4f8563`  
		Last Modified: Wed, 31 Mar 2021 22:14:25 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0`

```console
$ docker pull influxdb@sha256:9b7b0bec6fa7ee4cd2824c82a7ced3861250620b7c5d06b5d5dbf4bd8ba3cabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.0` - linux; amd64

```console
$ docker pull influxdb@sha256:8e941d9a9359b97556fdf2da0738077509ca3c1b90c69096f4b4bc791257e288
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116231489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6cdd3eeabf3ebef08ccfc0f16e73955695f3cb42d6f04f74531de2e5002425b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:16 GMT
ADD file:c254898ceb4172f05cd40460f8d0b1ca2d39d5178bdddd4e794c7d3fc5a60a03 in / 
# Tue, 30 Mar 2021 21:49:16 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:03:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:03:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:10:50 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 31 Mar 2021 22:10:50 GMT
ENV GOSU_VER=1.12
# Wed, 31 Mar 2021 22:10:53 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 31 Mar 2021 22:10:53 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 31 Mar 2021 22:11:00 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 31 Mar 2021 22:11:01 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 31 Mar 2021 22:11:01 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 31 Mar 2021 22:11:01 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 31 Mar 2021 22:11:01 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 31 Mar 2021 22:11:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:11:02 GMT
CMD ["influxd"]
# Wed, 31 Mar 2021 22:11:02 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:11:02 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 31 Mar 2021 22:11:02 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:004f1eed87df3f75f5e2a1a649fa7edd7f713d1300532fd0909bb39cd48437d7`  
		Last Modified: Tue, 30 Mar 2021 21:53:41 GMT  
		Size: 50.4 MB (50432842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6f1e8117dbb1c6a57603cb4f321a861a08105a81bcc6b01b0ec2b78c8523a5`  
		Last Modified: Tue, 30 Mar 2021 23:14:05 GMT  
		Size: 7.8 MB (7832608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c2faf66abec3dce9f54d6722ff592fce6dd4fb58a0d0b72282936c6598a3b3`  
		Last Modified: Tue, 30 Mar 2021 23:14:05 GMT  
		Size: 10.0 MB (9997208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0ed0a9c246f1c5f5cb3db3b62ebd6ce3f0deefcc8b70b26140a7a7f91083c0`  
		Last Modified: Wed, 31 Mar 2021 22:16:16 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87978ba7806d2f52b290e4a8c952671a53732a95e5eb6f959b159f175242d612`  
		Last Modified: Wed, 31 Mar 2021 22:16:14 GMT  
		Size: 961.0 KB (960990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7146865b4d1f8adccb956fe61e04596c2a7a8fd08ef691c6e3a8b87efd171b0f`  
		Last Modified: Wed, 31 Mar 2021 22:16:21 GMT  
		Size: 47.0 MB (47001576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e55c4eb7bc6925072d5c5711d8cbff3bfdf99650fd358d4a0c4e80f28d2418`  
		Last Modified: Wed, 31 Mar 2021 22:16:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9252baf2a0e774c623adc4eb05e561daa2a47fa8ae2642958e2869f66904eecc`  
		Last Modified: Wed, 31 Mar 2021 22:16:13 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1919027a118184a24f16179e23ea3e8c19c669b47183ab5da2e44c25ef6412a`  
		Last Modified: Wed, 31 Mar 2021 22:16:14 GMT  
		Size: 3.9 KB (3924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a1ad4c91f785c5192e14fdf09a8bdead94427331a15b89defc5029a0436f02f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112211365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4112fb1b3e6123701042257e654e3eb1faadfb007ba9044f69a6e4cd9f99469e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:46:50 GMT
ADD file:6a5cce92f1039ef2cb7ac6dd999c9f84289a9f6e1c0891d1edf791ea73b7e125 in / 
# Tue, 30 Mar 2021 21:46:53 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:15:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 00:15:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 17:12:59 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 31 Mar 2021 17:13:00 GMT
ENV GOSU_VER=1.12
# Wed, 31 Mar 2021 17:13:04 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 31 Mar 2021 17:13:04 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 31 Mar 2021 17:13:14 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 31 Mar 2021 17:13:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 31 Mar 2021 17:13:19 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 31 Mar 2021 17:13:20 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 31 Mar 2021 17:13:21 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 31 Mar 2021 17:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 17:13:23 GMT
CMD ["influxd"]
# Wed, 31 Mar 2021 17:13:24 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 17:13:25 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 31 Mar 2021 17:13:26 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:ef28e7e77ecbd3b3b426832bc12e8f5e629959683767466e9bac149c3286e126`  
		Last Modified: Tue, 30 Mar 2021 21:54:03 GMT  
		Size: 49.2 MB (49225808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344d2d9a9cf41c137b0dbb41df255f95fb812a23771a10ee2ab5a8a5047c62c4`  
		Last Modified: Wed, 31 Mar 2021 00:29:59 GMT  
		Size: 7.7 MB (7694530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299f3631f6b52be065a7342da0a46978d55cbd0d15c57fae22f4ca24efcc295a`  
		Last Modified: Wed, 31 Mar 2021 00:29:59 GMT  
		Size: 10.0 MB (9984391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a9ab46ceeb0a146647f85ddaf1972e840edb697acbf5239abd74ef0702c64f`  
		Last Modified: Wed, 31 Mar 2021 17:14:34 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335750e6519d2672bc292efbba97df6886170f9ff85556904ec857e218d2eb85`  
		Last Modified: Wed, 31 Mar 2021 17:14:33 GMT  
		Size: 896.4 KB (896382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78780f92b7d6137947ffeb91607bad3e51a884a6113e35ab3fbdf2feefc38ea3`  
		Last Modified: Wed, 31 Mar 2021 17:14:43 GMT  
		Size: 44.4 MB (44403984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aec80c1e56918a8623d485e1e9c5e6843a8a2ad28daea18ae37b0629640ae8b`  
		Last Modified: Wed, 31 Mar 2021 17:14:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc98efdfdd2d92c21d88e19eefa2bffc7bc35d527328605e95e1e4c36d12120f`  
		Last Modified: Wed, 31 Mar 2021 17:14:33 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c3d67602b6db6d61c3b39a478e309af96fd2162ca6ba90424de77488e48165`  
		Last Modified: Wed, 31 Mar 2021 17:14:33 GMT  
		Size: 3.9 KB (3925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0-alpine`

```console
$ docker pull influxdb@sha256:4bf0e5eeef84813c4b75e13ab4c1611cde1db0bf2294679b4a256f8bf9e39c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.0-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:1ba94f26832cb8a64d679b8cab740264d3cddb653933051726c4acb91e1369de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60481004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f908bf5c6ac4d306e69583534cd13126557aa2a13cc621cae6ba173ba792593`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:11:08 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:11:10 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Wed, 31 Mar 2021 22:11:11 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 31 Mar 2021 22:11:11 GMT
ENV GOSU_VER=1.12
# Wed, 31 Mar 2021 22:11:14 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 31 Mar 2021 22:11:14 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 31 Mar 2021 22:11:20 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 31 Mar 2021 22:11:21 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 31 Mar 2021 22:11:21 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 31 Mar 2021 22:11:22 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 31 Mar 2021 22:11:22 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 31 Mar 2021 22:11:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:11:22 GMT
CMD ["influxd"]
# Wed, 31 Mar 2021 22:11:23 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:11:23 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 31 Mar 2021 22:11:23 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b404698368cc8a559b274599da3c930735e7db53f887d8800a66e7288922e813`  
		Last Modified: Wed, 31 Mar 2021 22:16:41 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723a6ae3b2d3fa0df02c005637f8c9aedb651dcda93f3074b52090bc7d2b1d57`  
		Last Modified: Wed, 31 Mar 2021 22:16:42 GMT  
		Size: 9.7 MB (9701003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8204293e7573d524b907c5d670871ca5fa982b5eb307edfa6d1f41517655c9a`  
		Last Modified: Wed, 31 Mar 2021 22:16:40 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc866209a2237fba750e6bc7e06d80a4911de3badb0b87cd99e1efafbacdee6`  
		Last Modified: Wed, 31 Mar 2021 22:16:37 GMT  
		Size: 960.6 KB (960604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f09a26cfae00074791d1bd7ac1f11a5f47b6f94efe0a956e1a8ae3bf4c2d3c`  
		Last Modified: Wed, 31 Mar 2021 22:16:44 GMT  
		Size: 47.0 MB (47001578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd7d0cf2c67b83dfea8677da73003e373428d96e49e0aef01d1ed91759e134c`  
		Last Modified: Wed, 31 Mar 2021 22:16:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d2dd8a4d4c938baad62470454c75f0c3bbca7dd923ddadafb01411e2e281dd`  
		Last Modified: Wed, 31 Mar 2021 22:16:37 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef9269056ae902b8da282ff725dfbb36378382fd876f312105de4a1f7e650db`  
		Last Modified: Wed, 31 Mar 2021 22:16:38 GMT  
		Size: 3.9 KB (3924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.0-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:7928311c9723a1f254433212d7ca2cfb220d7e721e46fdd26dd29f9aab5cdc04
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57559543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456e1e2b23d556b5706a62ccfa1c10b4be02feb03ff083b277ad0090d3eb23f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 25 Mar 2021 22:40:10 GMT
ADD file:8d7431f7e3e42b162a1626e7abf4ef7605146671dccc753d490de6b7fe429261 in / 
# Thu, 25 Mar 2021 22:40:23 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 01:23:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 26 Mar 2021 01:23:06 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Fri, 26 Mar 2021 01:23:09 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Fri, 26 Mar 2021 01:23:10 GMT
ENV GOSU_VER=1.12
# Fri, 26 Mar 2021 01:23:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 26 Mar 2021 01:23:16 GMT
ENV INFLUXDB_VERSION=2.0.4
# Fri, 26 Mar 2021 01:23:28 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Fri, 26 Mar 2021 01:23:32 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Fri, 26 Mar 2021 01:23:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 26 Mar 2021 01:23:34 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Fri, 26 Mar 2021 01:23:35 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Fri, 26 Mar 2021 01:23:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 01:23:37 GMT
CMD ["influxd"]
# Fri, 26 Mar 2021 01:23:38 GMT
EXPOSE 8086
# Fri, 26 Mar 2021 01:23:39 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 26 Mar 2021 01:23:41 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:5ceb5101e3b0d54efb5f18318982508a04b181b4d5ae52b096dd35dea3a006cc`  
		Last Modified: Thu, 25 Mar 2021 22:44:41 GMT  
		Size: 2.7 MB (2711898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c66d69085d55364acf545d06662277eb28e02a15db508ac63bfd310936ea3f`  
		Last Modified: Fri, 26 Mar 2021 01:24:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a95ce2d86e2205748adfcceeb2cdcadbc4249252c7cc922a0a8127bdf794252`  
		Last Modified: Fri, 26 Mar 2021 01:24:13 GMT  
		Size: 9.5 MB (9541704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a5e616b579edbd75019eca934256e78a0e406eca03c11f2739bbbb539edc17`  
		Last Modified: Fri, 26 Mar 2021 01:24:10 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d177e27b48bc295428d040dc34524b55ea25ee2002b8904d97fbd65852cc8df`  
		Last Modified: Fri, 26 Mar 2021 01:24:08 GMT  
		Size: 896.1 KB (896105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f76c521cf1774059c5681e83c614efefa8da20f51e0e5c103a525aaacbd399`  
		Last Modified: Fri, 26 Mar 2021 01:24:19 GMT  
		Size: 44.4 MB (44403961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726a41b76f732152b387beec268a2db057684743fd4153a6584cd57841792f6f`  
		Last Modified: Fri, 26 Mar 2021 01:24:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459db7f28e6a9b7b3b411e1dfb427cfff89b73317ebfeaa96f1f9d57f3090979`  
		Last Modified: Fri, 26 Mar 2021 01:24:08 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bcf97a3b4eadc65f76552446f69698daa18702dac2333106d10665d2f77f4d4`  
		Last Modified: Fri, 26 Mar 2021 01:24:07 GMT  
		Size: 3.9 KB (3925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0.4`

```console
$ docker pull influxdb@sha256:9b7b0bec6fa7ee4cd2824c82a7ced3861250620b7c5d06b5d5dbf4bd8ba3cabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.0.4` - linux; amd64

```console
$ docker pull influxdb@sha256:8e941d9a9359b97556fdf2da0738077509ca3c1b90c69096f4b4bc791257e288
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116231489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6cdd3eeabf3ebef08ccfc0f16e73955695f3cb42d6f04f74531de2e5002425b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:16 GMT
ADD file:c254898ceb4172f05cd40460f8d0b1ca2d39d5178bdddd4e794c7d3fc5a60a03 in / 
# Tue, 30 Mar 2021 21:49:16 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:03:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:03:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:10:50 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 31 Mar 2021 22:10:50 GMT
ENV GOSU_VER=1.12
# Wed, 31 Mar 2021 22:10:53 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 31 Mar 2021 22:10:53 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 31 Mar 2021 22:11:00 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 31 Mar 2021 22:11:01 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 31 Mar 2021 22:11:01 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 31 Mar 2021 22:11:01 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 31 Mar 2021 22:11:01 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 31 Mar 2021 22:11:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:11:02 GMT
CMD ["influxd"]
# Wed, 31 Mar 2021 22:11:02 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:11:02 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 31 Mar 2021 22:11:02 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:004f1eed87df3f75f5e2a1a649fa7edd7f713d1300532fd0909bb39cd48437d7`  
		Last Modified: Tue, 30 Mar 2021 21:53:41 GMT  
		Size: 50.4 MB (50432842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6f1e8117dbb1c6a57603cb4f321a861a08105a81bcc6b01b0ec2b78c8523a5`  
		Last Modified: Tue, 30 Mar 2021 23:14:05 GMT  
		Size: 7.8 MB (7832608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c2faf66abec3dce9f54d6722ff592fce6dd4fb58a0d0b72282936c6598a3b3`  
		Last Modified: Tue, 30 Mar 2021 23:14:05 GMT  
		Size: 10.0 MB (9997208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0ed0a9c246f1c5f5cb3db3b62ebd6ce3f0deefcc8b70b26140a7a7f91083c0`  
		Last Modified: Wed, 31 Mar 2021 22:16:16 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87978ba7806d2f52b290e4a8c952671a53732a95e5eb6f959b159f175242d612`  
		Last Modified: Wed, 31 Mar 2021 22:16:14 GMT  
		Size: 961.0 KB (960990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7146865b4d1f8adccb956fe61e04596c2a7a8fd08ef691c6e3a8b87efd171b0f`  
		Last Modified: Wed, 31 Mar 2021 22:16:21 GMT  
		Size: 47.0 MB (47001576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e55c4eb7bc6925072d5c5711d8cbff3bfdf99650fd358d4a0c4e80f28d2418`  
		Last Modified: Wed, 31 Mar 2021 22:16:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9252baf2a0e774c623adc4eb05e561daa2a47fa8ae2642958e2869f66904eecc`  
		Last Modified: Wed, 31 Mar 2021 22:16:13 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1919027a118184a24f16179e23ea3e8c19c669b47183ab5da2e44c25ef6412a`  
		Last Modified: Wed, 31 Mar 2021 22:16:14 GMT  
		Size: 3.9 KB (3924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.0.4` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a1ad4c91f785c5192e14fdf09a8bdead94427331a15b89defc5029a0436f02f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112211365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4112fb1b3e6123701042257e654e3eb1faadfb007ba9044f69a6e4cd9f99469e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:46:50 GMT
ADD file:6a5cce92f1039ef2cb7ac6dd999c9f84289a9f6e1c0891d1edf791ea73b7e125 in / 
# Tue, 30 Mar 2021 21:46:53 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:15:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 00:15:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 17:12:59 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 31 Mar 2021 17:13:00 GMT
ENV GOSU_VER=1.12
# Wed, 31 Mar 2021 17:13:04 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 31 Mar 2021 17:13:04 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 31 Mar 2021 17:13:14 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 31 Mar 2021 17:13:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 31 Mar 2021 17:13:19 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 31 Mar 2021 17:13:20 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 31 Mar 2021 17:13:21 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 31 Mar 2021 17:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 17:13:23 GMT
CMD ["influxd"]
# Wed, 31 Mar 2021 17:13:24 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 17:13:25 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 31 Mar 2021 17:13:26 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:ef28e7e77ecbd3b3b426832bc12e8f5e629959683767466e9bac149c3286e126`  
		Last Modified: Tue, 30 Mar 2021 21:54:03 GMT  
		Size: 49.2 MB (49225808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344d2d9a9cf41c137b0dbb41df255f95fb812a23771a10ee2ab5a8a5047c62c4`  
		Last Modified: Wed, 31 Mar 2021 00:29:59 GMT  
		Size: 7.7 MB (7694530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299f3631f6b52be065a7342da0a46978d55cbd0d15c57fae22f4ca24efcc295a`  
		Last Modified: Wed, 31 Mar 2021 00:29:59 GMT  
		Size: 10.0 MB (9984391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a9ab46ceeb0a146647f85ddaf1972e840edb697acbf5239abd74ef0702c64f`  
		Last Modified: Wed, 31 Mar 2021 17:14:34 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335750e6519d2672bc292efbba97df6886170f9ff85556904ec857e218d2eb85`  
		Last Modified: Wed, 31 Mar 2021 17:14:33 GMT  
		Size: 896.4 KB (896382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78780f92b7d6137947ffeb91607bad3e51a884a6113e35ab3fbdf2feefc38ea3`  
		Last Modified: Wed, 31 Mar 2021 17:14:43 GMT  
		Size: 44.4 MB (44403984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aec80c1e56918a8623d485e1e9c5e6843a8a2ad28daea18ae37b0629640ae8b`  
		Last Modified: Wed, 31 Mar 2021 17:14:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc98efdfdd2d92c21d88e19eefa2bffc7bc35d527328605e95e1e4c36d12120f`  
		Last Modified: Wed, 31 Mar 2021 17:14:33 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c3d67602b6db6d61c3b39a478e309af96fd2162ca6ba90424de77488e48165`  
		Last Modified: Wed, 31 Mar 2021 17:14:33 GMT  
		Size: 3.9 KB (3925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0.4-alpine`

```console
$ docker pull influxdb@sha256:4bf0e5eeef84813c4b75e13ab4c1611cde1db0bf2294679b4a256f8bf9e39c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.0.4-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:1ba94f26832cb8a64d679b8cab740264d3cddb653933051726c4acb91e1369de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60481004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f908bf5c6ac4d306e69583534cd13126557aa2a13cc621cae6ba173ba792593`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:11:08 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:11:10 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Wed, 31 Mar 2021 22:11:11 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 31 Mar 2021 22:11:11 GMT
ENV GOSU_VER=1.12
# Wed, 31 Mar 2021 22:11:14 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 31 Mar 2021 22:11:14 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 31 Mar 2021 22:11:20 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 31 Mar 2021 22:11:21 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 31 Mar 2021 22:11:21 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 31 Mar 2021 22:11:22 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 31 Mar 2021 22:11:22 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 31 Mar 2021 22:11:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:11:22 GMT
CMD ["influxd"]
# Wed, 31 Mar 2021 22:11:23 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:11:23 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 31 Mar 2021 22:11:23 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b404698368cc8a559b274599da3c930735e7db53f887d8800a66e7288922e813`  
		Last Modified: Wed, 31 Mar 2021 22:16:41 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723a6ae3b2d3fa0df02c005637f8c9aedb651dcda93f3074b52090bc7d2b1d57`  
		Last Modified: Wed, 31 Mar 2021 22:16:42 GMT  
		Size: 9.7 MB (9701003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8204293e7573d524b907c5d670871ca5fa982b5eb307edfa6d1f41517655c9a`  
		Last Modified: Wed, 31 Mar 2021 22:16:40 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc866209a2237fba750e6bc7e06d80a4911de3badb0b87cd99e1efafbacdee6`  
		Last Modified: Wed, 31 Mar 2021 22:16:37 GMT  
		Size: 960.6 KB (960604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f09a26cfae00074791d1bd7ac1f11a5f47b6f94efe0a956e1a8ae3bf4c2d3c`  
		Last Modified: Wed, 31 Mar 2021 22:16:44 GMT  
		Size: 47.0 MB (47001578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd7d0cf2c67b83dfea8677da73003e373428d96e49e0aef01d1ed91759e134c`  
		Last Modified: Wed, 31 Mar 2021 22:16:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d2dd8a4d4c938baad62470454c75f0c3bbca7dd923ddadafb01411e2e281dd`  
		Last Modified: Wed, 31 Mar 2021 22:16:37 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef9269056ae902b8da282ff725dfbb36378382fd876f312105de4a1f7e650db`  
		Last Modified: Wed, 31 Mar 2021 22:16:38 GMT  
		Size: 3.9 KB (3924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.0.4-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:7928311c9723a1f254433212d7ca2cfb220d7e721e46fdd26dd29f9aab5cdc04
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57559543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456e1e2b23d556b5706a62ccfa1c10b4be02feb03ff083b277ad0090d3eb23f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 25 Mar 2021 22:40:10 GMT
ADD file:8d7431f7e3e42b162a1626e7abf4ef7605146671dccc753d490de6b7fe429261 in / 
# Thu, 25 Mar 2021 22:40:23 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 01:23:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 26 Mar 2021 01:23:06 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Fri, 26 Mar 2021 01:23:09 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Fri, 26 Mar 2021 01:23:10 GMT
ENV GOSU_VER=1.12
# Fri, 26 Mar 2021 01:23:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 26 Mar 2021 01:23:16 GMT
ENV INFLUXDB_VERSION=2.0.4
# Fri, 26 Mar 2021 01:23:28 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Fri, 26 Mar 2021 01:23:32 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Fri, 26 Mar 2021 01:23:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 26 Mar 2021 01:23:34 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Fri, 26 Mar 2021 01:23:35 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Fri, 26 Mar 2021 01:23:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 01:23:37 GMT
CMD ["influxd"]
# Fri, 26 Mar 2021 01:23:38 GMT
EXPOSE 8086
# Fri, 26 Mar 2021 01:23:39 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 26 Mar 2021 01:23:41 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:5ceb5101e3b0d54efb5f18318982508a04b181b4d5ae52b096dd35dea3a006cc`  
		Last Modified: Thu, 25 Mar 2021 22:44:41 GMT  
		Size: 2.7 MB (2711898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c66d69085d55364acf545d06662277eb28e02a15db508ac63bfd310936ea3f`  
		Last Modified: Fri, 26 Mar 2021 01:24:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a95ce2d86e2205748adfcceeb2cdcadbc4249252c7cc922a0a8127bdf794252`  
		Last Modified: Fri, 26 Mar 2021 01:24:13 GMT  
		Size: 9.5 MB (9541704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a5e616b579edbd75019eca934256e78a0e406eca03c11f2739bbbb539edc17`  
		Last Modified: Fri, 26 Mar 2021 01:24:10 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d177e27b48bc295428d040dc34524b55ea25ee2002b8904d97fbd65852cc8df`  
		Last Modified: Fri, 26 Mar 2021 01:24:08 GMT  
		Size: 896.1 KB (896105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f76c521cf1774059c5681e83c614efefa8da20f51e0e5c103a525aaacbd399`  
		Last Modified: Fri, 26 Mar 2021 01:24:19 GMT  
		Size: 44.4 MB (44403961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726a41b76f732152b387beec268a2db057684743fd4153a6584cd57841792f6f`  
		Last Modified: Fri, 26 Mar 2021 01:24:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459db7f28e6a9b7b3b411e1dfb427cfff89b73317ebfeaa96f1f9d57f3090979`  
		Last Modified: Fri, 26 Mar 2021 01:24:08 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bcf97a3b4eadc65f76552446f69698daa18702dac2333106d10665d2f77f4d4`  
		Last Modified: Fri, 26 Mar 2021 01:24:07 GMT  
		Size: 3.9 KB (3925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:4bf0e5eeef84813c4b75e13ab4c1611cde1db0bf2294679b4a256f8bf9e39c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:1ba94f26832cb8a64d679b8cab740264d3cddb653933051726c4acb91e1369de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60481004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f908bf5c6ac4d306e69583534cd13126557aa2a13cc621cae6ba173ba792593`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:11:08 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:11:10 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Wed, 31 Mar 2021 22:11:11 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 31 Mar 2021 22:11:11 GMT
ENV GOSU_VER=1.12
# Wed, 31 Mar 2021 22:11:14 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 31 Mar 2021 22:11:14 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 31 Mar 2021 22:11:20 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 31 Mar 2021 22:11:21 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 31 Mar 2021 22:11:21 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 31 Mar 2021 22:11:22 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 31 Mar 2021 22:11:22 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 31 Mar 2021 22:11:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:11:22 GMT
CMD ["influxd"]
# Wed, 31 Mar 2021 22:11:23 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:11:23 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 31 Mar 2021 22:11:23 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b404698368cc8a559b274599da3c930735e7db53f887d8800a66e7288922e813`  
		Last Modified: Wed, 31 Mar 2021 22:16:41 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723a6ae3b2d3fa0df02c005637f8c9aedb651dcda93f3074b52090bc7d2b1d57`  
		Last Modified: Wed, 31 Mar 2021 22:16:42 GMT  
		Size: 9.7 MB (9701003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8204293e7573d524b907c5d670871ca5fa982b5eb307edfa6d1f41517655c9a`  
		Last Modified: Wed, 31 Mar 2021 22:16:40 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc866209a2237fba750e6bc7e06d80a4911de3badb0b87cd99e1efafbacdee6`  
		Last Modified: Wed, 31 Mar 2021 22:16:37 GMT  
		Size: 960.6 KB (960604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f09a26cfae00074791d1bd7ac1f11a5f47b6f94efe0a956e1a8ae3bf4c2d3c`  
		Last Modified: Wed, 31 Mar 2021 22:16:44 GMT  
		Size: 47.0 MB (47001578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd7d0cf2c67b83dfea8677da73003e373428d96e49e0aef01d1ed91759e134c`  
		Last Modified: Wed, 31 Mar 2021 22:16:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d2dd8a4d4c938baad62470454c75f0c3bbca7dd923ddadafb01411e2e281dd`  
		Last Modified: Wed, 31 Mar 2021 22:16:37 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef9269056ae902b8da282ff725dfbb36378382fd876f312105de4a1f7e650db`  
		Last Modified: Wed, 31 Mar 2021 22:16:38 GMT  
		Size: 3.9 KB (3924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:7928311c9723a1f254433212d7ca2cfb220d7e721e46fdd26dd29f9aab5cdc04
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57559543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456e1e2b23d556b5706a62ccfa1c10b4be02feb03ff083b277ad0090d3eb23f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 25 Mar 2021 22:40:10 GMT
ADD file:8d7431f7e3e42b162a1626e7abf4ef7605146671dccc753d490de6b7fe429261 in / 
# Thu, 25 Mar 2021 22:40:23 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 01:23:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 26 Mar 2021 01:23:06 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Fri, 26 Mar 2021 01:23:09 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Fri, 26 Mar 2021 01:23:10 GMT
ENV GOSU_VER=1.12
# Fri, 26 Mar 2021 01:23:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 26 Mar 2021 01:23:16 GMT
ENV INFLUXDB_VERSION=2.0.4
# Fri, 26 Mar 2021 01:23:28 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Fri, 26 Mar 2021 01:23:32 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Fri, 26 Mar 2021 01:23:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 26 Mar 2021 01:23:34 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Fri, 26 Mar 2021 01:23:35 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Fri, 26 Mar 2021 01:23:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 01:23:37 GMT
CMD ["influxd"]
# Fri, 26 Mar 2021 01:23:38 GMT
EXPOSE 8086
# Fri, 26 Mar 2021 01:23:39 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 26 Mar 2021 01:23:41 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:5ceb5101e3b0d54efb5f18318982508a04b181b4d5ae52b096dd35dea3a006cc`  
		Last Modified: Thu, 25 Mar 2021 22:44:41 GMT  
		Size: 2.7 MB (2711898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c66d69085d55364acf545d06662277eb28e02a15db508ac63bfd310936ea3f`  
		Last Modified: Fri, 26 Mar 2021 01:24:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a95ce2d86e2205748adfcceeb2cdcadbc4249252c7cc922a0a8127bdf794252`  
		Last Modified: Fri, 26 Mar 2021 01:24:13 GMT  
		Size: 9.5 MB (9541704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a5e616b579edbd75019eca934256e78a0e406eca03c11f2739bbbb539edc17`  
		Last Modified: Fri, 26 Mar 2021 01:24:10 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d177e27b48bc295428d040dc34524b55ea25ee2002b8904d97fbd65852cc8df`  
		Last Modified: Fri, 26 Mar 2021 01:24:08 GMT  
		Size: 896.1 KB (896105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f76c521cf1774059c5681e83c614efefa8da20f51e0e5c103a525aaacbd399`  
		Last Modified: Fri, 26 Mar 2021 01:24:19 GMT  
		Size: 44.4 MB (44403961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726a41b76f732152b387beec268a2db057684743fd4153a6584cd57841792f6f`  
		Last Modified: Fri, 26 Mar 2021 01:24:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459db7f28e6a9b7b3b411e1dfb427cfff89b73317ebfeaa96f1f9d57f3090979`  
		Last Modified: Fri, 26 Mar 2021 01:24:08 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bcf97a3b4eadc65f76552446f69698daa18702dac2333106d10665d2f77f4d4`  
		Last Modified: Fri, 26 Mar 2021 01:24:07 GMT  
		Size: 3.9 KB (3925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data`

```console
$ docker pull influxdb@sha256:c47990ad54cbab2c4b7ce6e5e34b87d517d46a6323f9bfc8abda198038602a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:f7e31854dd0ffbfa5ef8ac02df3abcf90ff84e89fff55ae0ceb82c4dc6208d16
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126810142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076db8957be42f4ddbd11be5d3b3ae5c80792bb2f5c5e547779208ccb54e9396`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:08:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:08:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:08:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 22:10:06 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 31 Mar 2021 22:10:12 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 31 Mar 2021 22:10:13 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:10:13 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:10:13 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:10:13 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:10:13 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:10:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:10:14 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61ad49fa9961d6dfe53dc067fd690133f205498e8045e8f7ef6b9da0d42bd2`  
		Last Modified: Tue, 30 Mar 2021 23:17:25 GMT  
		Size: 11.3 MB (11286658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af62e04c0f85ed10801df4314d8cb9ba5e6c391f6a3c1db1080a0a78c8d4ed9d`  
		Last Modified: Tue, 30 Mar 2021 23:17:23 GMT  
		Size: 4.3 MB (4342466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ea2dd79e17761ed8d11e98f7420d9d909dcbc0ca1fe34ad492f5e495302a6`  
		Last Modified: Wed, 31 Mar 2021 22:12:05 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d41b7827948e414f042e1b9178e16f0fe855f9c0a2043a884762561ebcc529c`  
		Last Modified: Wed, 31 Mar 2021 22:14:56 GMT  
		Size: 65.8 MB (65796441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd72595d8d8e4975ceb4c2dc6f49bd4d712750c83b2ea0306138ad9367dc582`  
		Last Modified: Wed, 31 Mar 2021 22:14:47 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd848f72b95e08bf0cad39dc3de90ba4fa88364406a9f418c8ee9dfd2faf08d`  
		Last Modified: Wed, 31 Mar 2021 22:14:47 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1657f716309bf8a123806bff8a8b445f5ed98211006d7fa2e159d9ea6a02b0`  
		Last Modified: Wed, 31 Mar 2021 22:14:47 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:53386503e99f45244c7335689f11135d7eaf40ba27aa3d4f11703e460edc0a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:25f64b07b44114d25994531b533b989a3bbbd11c9a9fde3b9b04d9df71ec7b7e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69773182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1867ac52349985be3abbd7d162bff782c417b699a51657b5b3a5d19bf7f957fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:08:44 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 31 Mar 2021 22:10:18 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 31 Mar 2021 22:10:26 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 31 Mar 2021 22:10:26 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:10:26 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:10:26 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:10:27 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:10:27 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:10:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:10:27 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f9e539bb1e7629825670530d6a7fea3f07e8044425ad739925c87c1c5ea1cc`  
		Last Modified: Wed, 31 Mar 2021 22:12:25 GMT  
		Size: 1.4 MB (1430776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a19954818447d2176905c41c281ada51d631cb2b450436c92e5fd159be05ea`  
		Last Modified: Wed, 31 Mar 2021 22:15:22 GMT  
		Size: 65.5 MB (65540744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c2436e61f7cc05d5259eb9f7dc8f4919f3727c50c673ff6176b39ba7bf45c4`  
		Last Modified: Wed, 31 Mar 2021 22:15:13 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e29dd894fbc5b5e36a12b37840fa84556a70b2a9a3c5c089536c38b81b8790`  
		Last Modified: Wed, 31 Mar 2021 22:15:13 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1873d4c45433d2f9e20a15bbed16c5d4edb18c976c4fe26eb3147a2569ca8e`  
		Last Modified: Wed, 31 Mar 2021 22:15:13 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:9b7b0bec6fa7ee4cd2824c82a7ced3861250620b7c5d06b5d5dbf4bd8ba3cabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:8e941d9a9359b97556fdf2da0738077509ca3c1b90c69096f4b4bc791257e288
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116231489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6cdd3eeabf3ebef08ccfc0f16e73955695f3cb42d6f04f74531de2e5002425b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:16 GMT
ADD file:c254898ceb4172f05cd40460f8d0b1ca2d39d5178bdddd4e794c7d3fc5a60a03 in / 
# Tue, 30 Mar 2021 21:49:16 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:03:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:03:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:10:50 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 31 Mar 2021 22:10:50 GMT
ENV GOSU_VER=1.12
# Wed, 31 Mar 2021 22:10:53 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 31 Mar 2021 22:10:53 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 31 Mar 2021 22:11:00 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 31 Mar 2021 22:11:01 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 31 Mar 2021 22:11:01 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 31 Mar 2021 22:11:01 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 31 Mar 2021 22:11:01 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 31 Mar 2021 22:11:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:11:02 GMT
CMD ["influxd"]
# Wed, 31 Mar 2021 22:11:02 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:11:02 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 31 Mar 2021 22:11:02 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:004f1eed87df3f75f5e2a1a649fa7edd7f713d1300532fd0909bb39cd48437d7`  
		Last Modified: Tue, 30 Mar 2021 21:53:41 GMT  
		Size: 50.4 MB (50432842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6f1e8117dbb1c6a57603cb4f321a861a08105a81bcc6b01b0ec2b78c8523a5`  
		Last Modified: Tue, 30 Mar 2021 23:14:05 GMT  
		Size: 7.8 MB (7832608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c2faf66abec3dce9f54d6722ff592fce6dd4fb58a0d0b72282936c6598a3b3`  
		Last Modified: Tue, 30 Mar 2021 23:14:05 GMT  
		Size: 10.0 MB (9997208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0ed0a9c246f1c5f5cb3db3b62ebd6ce3f0deefcc8b70b26140a7a7f91083c0`  
		Last Modified: Wed, 31 Mar 2021 22:16:16 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87978ba7806d2f52b290e4a8c952671a53732a95e5eb6f959b159f175242d612`  
		Last Modified: Wed, 31 Mar 2021 22:16:14 GMT  
		Size: 961.0 KB (960990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7146865b4d1f8adccb956fe61e04596c2a7a8fd08ef691c6e3a8b87efd171b0f`  
		Last Modified: Wed, 31 Mar 2021 22:16:21 GMT  
		Size: 47.0 MB (47001576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e55c4eb7bc6925072d5c5711d8cbff3bfdf99650fd358d4a0c4e80f28d2418`  
		Last Modified: Wed, 31 Mar 2021 22:16:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9252baf2a0e774c623adc4eb05e561daa2a47fa8ae2642958e2869f66904eecc`  
		Last Modified: Wed, 31 Mar 2021 22:16:13 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1919027a118184a24f16179e23ea3e8c19c669b47183ab5da2e44c25ef6412a`  
		Last Modified: Wed, 31 Mar 2021 22:16:14 GMT  
		Size: 3.9 KB (3924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a1ad4c91f785c5192e14fdf09a8bdead94427331a15b89defc5029a0436f02f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112211365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4112fb1b3e6123701042257e654e3eb1faadfb007ba9044f69a6e4cd9f99469e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:46:50 GMT
ADD file:6a5cce92f1039ef2cb7ac6dd999c9f84289a9f6e1c0891d1edf791ea73b7e125 in / 
# Tue, 30 Mar 2021 21:46:53 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:15:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 00:15:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 17:12:59 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 31 Mar 2021 17:13:00 GMT
ENV GOSU_VER=1.12
# Wed, 31 Mar 2021 17:13:04 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 31 Mar 2021 17:13:04 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 31 Mar 2021 17:13:14 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 31 Mar 2021 17:13:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 31 Mar 2021 17:13:19 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 31 Mar 2021 17:13:20 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 31 Mar 2021 17:13:21 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 31 Mar 2021 17:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 17:13:23 GMT
CMD ["influxd"]
# Wed, 31 Mar 2021 17:13:24 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 17:13:25 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 31 Mar 2021 17:13:26 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:ef28e7e77ecbd3b3b426832bc12e8f5e629959683767466e9bac149c3286e126`  
		Last Modified: Tue, 30 Mar 2021 21:54:03 GMT  
		Size: 49.2 MB (49225808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344d2d9a9cf41c137b0dbb41df255f95fb812a23771a10ee2ab5a8a5047c62c4`  
		Last Modified: Wed, 31 Mar 2021 00:29:59 GMT  
		Size: 7.7 MB (7694530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299f3631f6b52be065a7342da0a46978d55cbd0d15c57fae22f4ca24efcc295a`  
		Last Modified: Wed, 31 Mar 2021 00:29:59 GMT  
		Size: 10.0 MB (9984391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a9ab46ceeb0a146647f85ddaf1972e840edb697acbf5239abd74ef0702c64f`  
		Last Modified: Wed, 31 Mar 2021 17:14:34 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335750e6519d2672bc292efbba97df6886170f9ff85556904ec857e218d2eb85`  
		Last Modified: Wed, 31 Mar 2021 17:14:33 GMT  
		Size: 896.4 KB (896382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78780f92b7d6137947ffeb91607bad3e51a884a6113e35ab3fbdf2feefc38ea3`  
		Last Modified: Wed, 31 Mar 2021 17:14:43 GMT  
		Size: 44.4 MB (44403984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aec80c1e56918a8623d485e1e9c5e6843a8a2ad28daea18ae37b0629640ae8b`  
		Last Modified: Wed, 31 Mar 2021 17:14:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc98efdfdd2d92c21d88e19eefa2bffc7bc35d527328605e95e1e4c36d12120f`  
		Last Modified: Wed, 31 Mar 2021 17:14:33 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c3d67602b6db6d61c3b39a478e309af96fd2162ca6ba90424de77488e48165`  
		Last Modified: Wed, 31 Mar 2021 17:14:33 GMT  
		Size: 3.9 KB (3925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:f2f779eec1a6dd4ecebccffa6d9cbfa16637f9f71855e12018326f61e9328bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:07f58b191138c487f7e05e370dae45ff3c77b29a7c353c59f1f5bd56de231d67
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83878780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6321e44de6670b2fa75aab6098396ff070902779c12bf9f1a7ed1edb8960ef8b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:08:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:08:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:08:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 22:10:06 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 31 Mar 2021 22:10:35 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 31 Mar 2021 22:10:35 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 31 Mar 2021 22:10:36 GMT
EXPOSE 8091
# Wed, 31 Mar 2021 22:10:36 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:10:36 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:10:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:10:36 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61ad49fa9961d6dfe53dc067fd690133f205498e8045e8f7ef6b9da0d42bd2`  
		Last Modified: Tue, 30 Mar 2021 23:17:25 GMT  
		Size: 11.3 MB (11286658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af62e04c0f85ed10801df4314d8cb9ba5e6c391f6a3c1db1080a0a78c8d4ed9d`  
		Last Modified: Tue, 30 Mar 2021 23:17:23 GMT  
		Size: 4.3 MB (4342466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ea2dd79e17761ed8d11e98f7420d9d909dcbc0ca1fe34ad492f5e495302a6`  
		Last Modified: Wed, 31 Mar 2021 22:12:05 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33184db9c22eb774767a5e0d59084338e22aa85921c99554dc03e64cd3a3cca3`  
		Last Modified: Wed, 31 Mar 2021 22:15:41 GMT  
		Size: 22.9 MB (22866284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0c565154abc635cf8741449ae2632fd60b8f8c800d91fbf82896af8c6620e0`  
		Last Modified: Wed, 31 Mar 2021 22:15:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cd9818c31165e7bf5db665dd7f1bab0d30fb5132e853a34afd94501ac7f730`  
		Last Modified: Wed, 31 Mar 2021 22:15:39 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta-alpine`

```console
$ docker pull influxdb@sha256:39aa359985fb3b4befb240e3c96f7cd364f82491637b981bd476d357c6334609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ed56a3d248256dd6ffded198ba68cb376670d09c36e465be2432ebc0a887005c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26966631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2f205931ae4121f85700a26ded6400cca220cf3cf8c5ffbd659767ee295496`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:08:44 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 31 Mar 2021 22:10:18 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 31 Mar 2021 22:10:44 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 31 Mar 2021 22:10:44 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 31 Mar 2021 22:10:45 GMT
EXPOSE 8091
# Wed, 31 Mar 2021 22:10:45 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:10:45 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:10:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:10:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f9e539bb1e7629825670530d6a7fea3f07e8044425ad739925c87c1c5ea1cc`  
		Last Modified: Wed, 31 Mar 2021 22:12:25 GMT  
		Size: 1.4 MB (1430776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec545b4936bf871f85c7c3c2800ebe59111c875cd2ed5f84a6e414ac5b99116e`  
		Last Modified: Wed, 31 Mar 2021 22:15:57 GMT  
		Size: 22.7 MB (22735394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8667c4944d3ed1b8e3f3ac5c388f8b312f34881190d9ae8c06adeedf575780e2`  
		Last Modified: Wed, 31 Mar 2021 22:15:54 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345ad36b894191aeac6a52143e6f0b96c7847a6cd3e82962022770ea6f63b857`  
		Last Modified: Wed, 31 Mar 2021 22:15:54 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
