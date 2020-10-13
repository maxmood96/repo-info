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
$ docker pull influxdb@sha256:4040656da0ccdb622bece795fdebcc4748aed79d9f43661c21ea5f3c741afe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7` - linux; amd64

```console
$ docker pull influxdb@sha256:54b9c5c7e35bd211ce972584c231cc726666bd14ba8ff717234cb9607bf51b7d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124559549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1525f07eb39b55a96c5150a76e5dcc71d6008fd3489802d209425f205567218e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:06:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 11 Sep 2020 03:06:11 GMT
ENV INFLUXDB_VERSION=1.7.10
# Fri, 11 Sep 2020 03:06:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Fri, 11 Sep 2020 03:06:17 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 11 Sep 2020 03:06:17 GMT
EXPOSE 8086
# Fri, 11 Sep 2020 03:06:17 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Sep 2020 03:06:17 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 11 Sep 2020 03:06:17 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 11 Sep 2020 03:06:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Sep 2020 03:06:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b77385dee1edee19a023ac1167f1c1dd58640abfdb7cb19750575954d2db3`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ceca1044f188c3821e1a12bdbcfa44ae44f260051f311774274731c47da36e1`  
		Last Modified: Fri, 11 Sep 2020 03:08:01 GMT  
		Size: 64.1 MB (64096968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9e13de72c09d935afc1ff9cc04fe37192d16b923259c01dab5baa0ef150fc7`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e590363d108a7fccff959e775e4bc2ae9fc4228ec13fc63fd2d010cc6f7195f`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f836d6098e0f77b75ce4f3e0aa99ec6099518d59669531f20684ca3321150ff`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 1.3 KB (1281 bytes)  
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
$ docker pull influxdb@sha256:b738e4b118061065289ab15ee0d1b445c64d121186bcccc490b7ecd6fdd79aa7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117100003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643b4185b48ebb6cd7c8ecdddb2125523c1801879084f4e4b70e53f5a84889fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 09 Sep 2020 23:54:23 GMT
ADD file:f74bb8d38ef70a022988428f254630d1f424ed9a3b957687b0cd0f85b9d49e29 in / 
# Wed, 09 Sep 2020 23:54:25 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:35:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 19:48:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 10 Sep 2020 19:48:54 GMT
ENV INFLUXDB_VERSION=1.7.10
# Thu, 10 Sep 2020 19:49:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 10 Sep 2020 19:49:04 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 10 Sep 2020 19:49:05 GMT
EXPOSE 8086
# Thu, 10 Sep 2020 19:49:06 GMT
VOLUME [/var/lib/influxdb]
# Thu, 10 Sep 2020 19:49:07 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 10 Sep 2020 19:49:08 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 10 Sep 2020 19:49:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 19:49:09 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3b396f138ad78ffceac749b105c676dce568fa15a7b9f2273c2ee13ba023cea1`  
		Last Modified: Thu, 10 Sep 2020 00:01:33 GMT  
		Size: 43.2 MB (43171697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5db606bd1ccd8d11ca18492ee5d5122fdae2e7172ceb0df9cd15dc4d9f3c259`  
		Last Modified: Thu, 10 Sep 2020 00:45:55 GMT  
		Size: 9.7 MB (9700841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd3b5402f1859618a8e455e6bf04a916c8460da1c5f115568ba530c96f6ba3`  
		Last Modified: Thu, 10 Sep 2020 00:45:52 GMT  
		Size: 4.1 MB (4095176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b5628caff97d484a7850ebeeca0c0b9bc1f8c2c5844bbf8bb6258cfa6dc76e`  
		Last Modified: Thu, 10 Sep 2020 19:49:56 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d649e4ed243dc3a52f4eda86894457a00b676eda82007b72251207bc6ec098`  
		Last Modified: Thu, 10 Sep 2020 19:50:12 GMT  
		Size: 60.1 MB (60127720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dbbc18441964860ca464d10befb97ca91f56580a2ac639fe8c7bd78f00876c`  
		Last Modified: Thu, 10 Sep 2020 19:49:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89965d7c6ae433c36e3c547dceea469b88d34119cff02e84d8186da4058d1336`  
		Last Modified: Thu, 10 Sep 2020 19:49:56 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84862b618078cc7d2a2857f0208d3b912700e0036f408f3fa23e22851b84332d`  
		Last Modified: Thu, 10 Sep 2020 19:49:56 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10`

```console
$ docker pull influxdb@sha256:4040656da0ccdb622bece795fdebcc4748aed79d9f43661c21ea5f3c741afe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7.10` - linux; amd64

```console
$ docker pull influxdb@sha256:54b9c5c7e35bd211ce972584c231cc726666bd14ba8ff717234cb9607bf51b7d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124559549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1525f07eb39b55a96c5150a76e5dcc71d6008fd3489802d209425f205567218e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:06:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 11 Sep 2020 03:06:11 GMT
ENV INFLUXDB_VERSION=1.7.10
# Fri, 11 Sep 2020 03:06:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Fri, 11 Sep 2020 03:06:17 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 11 Sep 2020 03:06:17 GMT
EXPOSE 8086
# Fri, 11 Sep 2020 03:06:17 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Sep 2020 03:06:17 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 11 Sep 2020 03:06:17 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 11 Sep 2020 03:06:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Sep 2020 03:06:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b77385dee1edee19a023ac1167f1c1dd58640abfdb7cb19750575954d2db3`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ceca1044f188c3821e1a12bdbcfa44ae44f260051f311774274731c47da36e1`  
		Last Modified: Fri, 11 Sep 2020 03:08:01 GMT  
		Size: 64.1 MB (64096968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9e13de72c09d935afc1ff9cc04fe37192d16b923259c01dab5baa0ef150fc7`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e590363d108a7fccff959e775e4bc2ae9fc4228ec13fc63fd2d010cc6f7195f`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f836d6098e0f77b75ce4f3e0aa99ec6099518d59669531f20684ca3321150ff`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 1.3 KB (1281 bytes)  
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
$ docker pull influxdb@sha256:b738e4b118061065289ab15ee0d1b445c64d121186bcccc490b7ecd6fdd79aa7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117100003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643b4185b48ebb6cd7c8ecdddb2125523c1801879084f4e4b70e53f5a84889fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 09 Sep 2020 23:54:23 GMT
ADD file:f74bb8d38ef70a022988428f254630d1f424ed9a3b957687b0cd0f85b9d49e29 in / 
# Wed, 09 Sep 2020 23:54:25 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:35:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 19:48:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 10 Sep 2020 19:48:54 GMT
ENV INFLUXDB_VERSION=1.7.10
# Thu, 10 Sep 2020 19:49:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 10 Sep 2020 19:49:04 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 10 Sep 2020 19:49:05 GMT
EXPOSE 8086
# Thu, 10 Sep 2020 19:49:06 GMT
VOLUME [/var/lib/influxdb]
# Thu, 10 Sep 2020 19:49:07 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 10 Sep 2020 19:49:08 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 10 Sep 2020 19:49:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 19:49:09 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3b396f138ad78ffceac749b105c676dce568fa15a7b9f2273c2ee13ba023cea1`  
		Last Modified: Thu, 10 Sep 2020 00:01:33 GMT  
		Size: 43.2 MB (43171697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5db606bd1ccd8d11ca18492ee5d5122fdae2e7172ceb0df9cd15dc4d9f3c259`  
		Last Modified: Thu, 10 Sep 2020 00:45:55 GMT  
		Size: 9.7 MB (9700841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd3b5402f1859618a8e455e6bf04a916c8460da1c5f115568ba530c96f6ba3`  
		Last Modified: Thu, 10 Sep 2020 00:45:52 GMT  
		Size: 4.1 MB (4095176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b5628caff97d484a7850ebeeca0c0b9bc1f8c2c5844bbf8bb6258cfa6dc76e`  
		Last Modified: Thu, 10 Sep 2020 19:49:56 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d649e4ed243dc3a52f4eda86894457a00b676eda82007b72251207bc6ec098`  
		Last Modified: Thu, 10 Sep 2020 19:50:12 GMT  
		Size: 60.1 MB (60127720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dbbc18441964860ca464d10befb97ca91f56580a2ac639fe8c7bd78f00876c`  
		Last Modified: Thu, 10 Sep 2020 19:49:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89965d7c6ae433c36e3c547dceea469b88d34119cff02e84d8186da4058d1336`  
		Last Modified: Thu, 10 Sep 2020 19:49:56 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84862b618078cc7d2a2857f0208d3b912700e0036f408f3fa23e22851b84332d`  
		Last Modified: Thu, 10 Sep 2020 19:49:56 GMT  
		Size: 1.3 KB (1281 bytes)  
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
$ docker pull influxdb@sha256:604a59df40d7a06ca19ed7285b8b921cc54dbd191b679926fe881d498a757dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:089896fb33f0ddb10c615401c27bf5d7102ce818a50777d1b0ae22e394d8a29b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148374939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b38bb872b446bd4aba91d9e41d14dccedff092bb48367913241cf98046f52c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:06:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 11 Sep 2020 03:06:25 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Fri, 11 Sep 2020 03:06:33 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Fri, 11 Sep 2020 03:06:33 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 11 Sep 2020 03:06:34 GMT
EXPOSE 8086
# Fri, 11 Sep 2020 03:06:34 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Sep 2020 03:06:34 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 11 Sep 2020 03:06:34 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 11 Sep 2020 03:06:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Sep 2020 03:06:35 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b77385dee1edee19a023ac1167f1c1dd58640abfdb7cb19750575954d2db3`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1604c27f6f1dbd73ec662cafdc66277a46d21bae860736ca86ecfa3f8e29a7`  
		Last Modified: Fri, 11 Sep 2020 03:08:19 GMT  
		Size: 87.9 MB (87912299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc53d8c8ceb22333c38f661b08105db638aba6ec8b7eca3ca8545f2a7d9aa73`  
		Last Modified: Fri, 11 Sep 2020 03:08:06 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd464f83e5678487746fb60edf4ec518b1cab90a064520657b1b278d48e3183`  
		Last Modified: Fri, 11 Sep 2020 03:08:06 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29518191130a3771663c99d95439eb655e63d90ba613284aa8ebdd026482b6c`  
		Last Modified: Fri, 11 Sep 2020 03:08:06 GMT  
		Size: 1.3 KB (1281 bytes)  
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
$ docker pull influxdb@sha256:8c226e342cb217ff26c5c0969a2d6914f102dce732e99bba0d45020dbbf372dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:d6653b1822f91bb93561ed02ed767a5fd35e77e027c86ea69331e17906a1a6e3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83594089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ded2c039fd8a101f615dff205fa869b750e2931bb506136a3d27fe64a8955a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:06:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 11 Sep 2020 03:06:25 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Fri, 11 Sep 2020 03:06:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Fri, 11 Sep 2020 03:06:46 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 11 Sep 2020 03:06:46 GMT
EXPOSE 8091
# Fri, 11 Sep 2020 03:06:46 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Sep 2020 03:06:46 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 11 Sep 2020 03:06:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Sep 2020 03:06:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b77385dee1edee19a023ac1167f1c1dd58640abfdb7cb19750575954d2db3`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5285a4ed94ad186b3377b754446dab903fc62943f9c16b77d4af9c121377efa7`  
		Last Modified: Fri, 11 Sep 2020 03:08:27 GMT  
		Size: 23.1 MB (23132657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553f67409206368c5ea61c4cd7422fc66829495ae9f1aca2772ac99495b84c4b`  
		Last Modified: Fri, 11 Sep 2020 03:08:23 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42e5dd1c7e29bc75e9855b7272cd56edc1275a97df8c95aecf73a9acd02bd37`  
		Last Modified: Fri, 11 Sep 2020 03:08:23 GMT  
		Size: 375.0 B  
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
$ docker pull influxdb@sha256:604a59df40d7a06ca19ed7285b8b921cc54dbd191b679926fe881d498a757dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:089896fb33f0ddb10c615401c27bf5d7102ce818a50777d1b0ae22e394d8a29b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148374939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b38bb872b446bd4aba91d9e41d14dccedff092bb48367913241cf98046f52c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:06:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 11 Sep 2020 03:06:25 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Fri, 11 Sep 2020 03:06:33 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Fri, 11 Sep 2020 03:06:33 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 11 Sep 2020 03:06:34 GMT
EXPOSE 8086
# Fri, 11 Sep 2020 03:06:34 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Sep 2020 03:06:34 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 11 Sep 2020 03:06:34 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 11 Sep 2020 03:06:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Sep 2020 03:06:35 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b77385dee1edee19a023ac1167f1c1dd58640abfdb7cb19750575954d2db3`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1604c27f6f1dbd73ec662cafdc66277a46d21bae860736ca86ecfa3f8e29a7`  
		Last Modified: Fri, 11 Sep 2020 03:08:19 GMT  
		Size: 87.9 MB (87912299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc53d8c8ceb22333c38f661b08105db638aba6ec8b7eca3ca8545f2a7d9aa73`  
		Last Modified: Fri, 11 Sep 2020 03:08:06 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd464f83e5678487746fb60edf4ec518b1cab90a064520657b1b278d48e3183`  
		Last Modified: Fri, 11 Sep 2020 03:08:06 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29518191130a3771663c99d95439eb655e63d90ba613284aa8ebdd026482b6c`  
		Last Modified: Fri, 11 Sep 2020 03:08:06 GMT  
		Size: 1.3 KB (1281 bytes)  
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
$ docker pull influxdb@sha256:8c226e342cb217ff26c5c0969a2d6914f102dce732e99bba0d45020dbbf372dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:d6653b1822f91bb93561ed02ed767a5fd35e77e027c86ea69331e17906a1a6e3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83594089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ded2c039fd8a101f615dff205fa869b750e2931bb506136a3d27fe64a8955a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:06:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 11 Sep 2020 03:06:25 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Fri, 11 Sep 2020 03:06:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Fri, 11 Sep 2020 03:06:46 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 11 Sep 2020 03:06:46 GMT
EXPOSE 8091
# Fri, 11 Sep 2020 03:06:46 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Sep 2020 03:06:46 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 11 Sep 2020 03:06:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Sep 2020 03:06:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b77385dee1edee19a023ac1167f1c1dd58640abfdb7cb19750575954d2db3`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5285a4ed94ad186b3377b754446dab903fc62943f9c16b77d4af9c121377efa7`  
		Last Modified: Fri, 11 Sep 2020 03:08:27 GMT  
		Size: 23.1 MB (23132657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553f67409206368c5ea61c4cd7422fc66829495ae9f1aca2772ac99495b84c4b`  
		Last Modified: Fri, 11 Sep 2020 03:08:23 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42e5dd1c7e29bc75e9855b7272cd56edc1275a97df8c95aecf73a9acd02bd37`  
		Last Modified: Fri, 11 Sep 2020 03:08:23 GMT  
		Size: 375.0 B  
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
$ docker pull influxdb@sha256:6c394679f243a0277214bc9006ed1cc0ff514688bfce5c7f2d69995862493eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8` - linux; amd64

```console
$ docker pull influxdb@sha256:4c6ffc21a190bad583f276335abf08d3d4eaf16c16040940252a37e0df731189
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125428508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35de8cc24dfca8ad80fc93bba1bc7125240b3e27b457a1ef529aac5fb6217eef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:06:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 02 Oct 2020 01:34:42 GMT
ENV INFLUXDB_VERSION=1.8.3
# Fri, 02 Oct 2020 01:34:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Fri, 02 Oct 2020 01:34:53 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 02 Oct 2020 01:34:54 GMT
EXPOSE 8086
# Fri, 02 Oct 2020 01:34:54 GMT
VOLUME [/var/lib/influxdb]
# Fri, 02 Oct 2020 01:34:54 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 02 Oct 2020 01:34:55 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 02 Oct 2020 01:34:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:34:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b77385dee1edee19a023ac1167f1c1dd58640abfdb7cb19750575954d2db3`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5e595336ce87e06ffe8bab919e531d9a8f10e165773cb527601b9c4774bb11`  
		Last Modified: Fri, 02 Oct 2020 01:37:04 GMT  
		Size: 65.0 MB (64965928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bd745fdff76484cd933aec033616c6dd4da4ac16cf74e0a439408c5d0935f6`  
		Last Modified: Fri, 02 Oct 2020 01:36:51 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d8bed28c330d03ba01e47415bcf5f9357ad6bc534b358790a40de5d3b7287f`  
		Last Modified: Fri, 02 Oct 2020 01:36:52 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab924157a65ac65356204cbda230618107fe660d09983313d381d59ff536f9e1`  
		Last Modified: Fri, 02 Oct 2020 01:36:51 GMT  
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
$ docker pull influxdb@sha256:3e648bb4a09c7e8da9884ba0ea57a0efa1a04627c6a13003a8792600f82c0199
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117599020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2635e37ea28bfe980a9d7f800925d727fc01b839750d222e4bb983d4c7fa6456`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 09 Sep 2020 23:54:23 GMT
ADD file:f74bb8d38ef70a022988428f254630d1f424ed9a3b957687b0cd0f85b9d49e29 in / 
# Wed, 09 Sep 2020 23:54:25 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:35:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 19:48:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 01 Oct 2020 21:51:34 GMT
ENV INFLUXDB_VERSION=1.8.3
# Thu, 01 Oct 2020 21:51:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 01 Oct 2020 21:51:50 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 01 Oct 2020 21:51:51 GMT
EXPOSE 8086
# Thu, 01 Oct 2020 21:51:52 GMT
VOLUME [/var/lib/influxdb]
# Thu, 01 Oct 2020 21:51:53 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 01 Oct 2020 21:51:54 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 01 Oct 2020 21:51:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Oct 2020 21:51:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3b396f138ad78ffceac749b105c676dce568fa15a7b9f2273c2ee13ba023cea1`  
		Last Modified: Thu, 10 Sep 2020 00:01:33 GMT  
		Size: 43.2 MB (43171697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5db606bd1ccd8d11ca18492ee5d5122fdae2e7172ceb0df9cd15dc4d9f3c259`  
		Last Modified: Thu, 10 Sep 2020 00:45:55 GMT  
		Size: 9.7 MB (9700841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd3b5402f1859618a8e455e6bf04a916c8460da1c5f115568ba530c96f6ba3`  
		Last Modified: Thu, 10 Sep 2020 00:45:52 GMT  
		Size: 4.1 MB (4095176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b5628caff97d484a7850ebeeca0c0b9bc1f8c2c5844bbf8bb6258cfa6dc76e`  
		Last Modified: Thu, 10 Sep 2020 19:49:56 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f24d17df606a2dac7251c69f972d8f97ddfacfa2bec16caad1ab5375385a17`  
		Last Modified: Thu, 01 Oct 2020 21:52:33 GMT  
		Size: 60.6 MB (60626732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80c6c1cd5c4d4d77fbbf807cb5fecedafafe1d0862ee603bd873eeacde19ee3`  
		Last Modified: Thu, 01 Oct 2020 21:52:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ebbc81b1bce09d47f457494db78dc2b05b58cafe77c0d7257a52f75f25b96b`  
		Last Modified: Thu, 01 Oct 2020 21:52:16 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb74e023eeca4f8d1ac717fb246f3fcd38a7556ad03b9a729f227d7ffced7869`  
		Last Modified: Thu, 01 Oct 2020 21:52:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3`

```console
$ docker pull influxdb@sha256:6c394679f243a0277214bc9006ed1cc0ff514688bfce5c7f2d69995862493eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8.3` - linux; amd64

```console
$ docker pull influxdb@sha256:4c6ffc21a190bad583f276335abf08d3d4eaf16c16040940252a37e0df731189
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125428508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35de8cc24dfca8ad80fc93bba1bc7125240b3e27b457a1ef529aac5fb6217eef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:06:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 02 Oct 2020 01:34:42 GMT
ENV INFLUXDB_VERSION=1.8.3
# Fri, 02 Oct 2020 01:34:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Fri, 02 Oct 2020 01:34:53 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 02 Oct 2020 01:34:54 GMT
EXPOSE 8086
# Fri, 02 Oct 2020 01:34:54 GMT
VOLUME [/var/lib/influxdb]
# Fri, 02 Oct 2020 01:34:54 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 02 Oct 2020 01:34:55 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 02 Oct 2020 01:34:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:34:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b77385dee1edee19a023ac1167f1c1dd58640abfdb7cb19750575954d2db3`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5e595336ce87e06ffe8bab919e531d9a8f10e165773cb527601b9c4774bb11`  
		Last Modified: Fri, 02 Oct 2020 01:37:04 GMT  
		Size: 65.0 MB (64965928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bd745fdff76484cd933aec033616c6dd4da4ac16cf74e0a439408c5d0935f6`  
		Last Modified: Fri, 02 Oct 2020 01:36:51 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d8bed28c330d03ba01e47415bcf5f9357ad6bc534b358790a40de5d3b7287f`  
		Last Modified: Fri, 02 Oct 2020 01:36:52 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab924157a65ac65356204cbda230618107fe660d09983313d381d59ff536f9e1`  
		Last Modified: Fri, 02 Oct 2020 01:36:51 GMT  
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
$ docker pull influxdb@sha256:3e648bb4a09c7e8da9884ba0ea57a0efa1a04627c6a13003a8792600f82c0199
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117599020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2635e37ea28bfe980a9d7f800925d727fc01b839750d222e4bb983d4c7fa6456`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 09 Sep 2020 23:54:23 GMT
ADD file:f74bb8d38ef70a022988428f254630d1f424ed9a3b957687b0cd0f85b9d49e29 in / 
# Wed, 09 Sep 2020 23:54:25 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:35:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 19:48:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 01 Oct 2020 21:51:34 GMT
ENV INFLUXDB_VERSION=1.8.3
# Thu, 01 Oct 2020 21:51:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 01 Oct 2020 21:51:50 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 01 Oct 2020 21:51:51 GMT
EXPOSE 8086
# Thu, 01 Oct 2020 21:51:52 GMT
VOLUME [/var/lib/influxdb]
# Thu, 01 Oct 2020 21:51:53 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 01 Oct 2020 21:51:54 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 01 Oct 2020 21:51:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Oct 2020 21:51:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3b396f138ad78ffceac749b105c676dce568fa15a7b9f2273c2ee13ba023cea1`  
		Last Modified: Thu, 10 Sep 2020 00:01:33 GMT  
		Size: 43.2 MB (43171697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5db606bd1ccd8d11ca18492ee5d5122fdae2e7172ceb0df9cd15dc4d9f3c259`  
		Last Modified: Thu, 10 Sep 2020 00:45:55 GMT  
		Size: 9.7 MB (9700841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd3b5402f1859618a8e455e6bf04a916c8460da1c5f115568ba530c96f6ba3`  
		Last Modified: Thu, 10 Sep 2020 00:45:52 GMT  
		Size: 4.1 MB (4095176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b5628caff97d484a7850ebeeca0c0b9bc1f8c2c5844bbf8bb6258cfa6dc76e`  
		Last Modified: Thu, 10 Sep 2020 19:49:56 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f24d17df606a2dac7251c69f972d8f97ddfacfa2bec16caad1ab5375385a17`  
		Last Modified: Thu, 01 Oct 2020 21:52:33 GMT  
		Size: 60.6 MB (60626732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80c6c1cd5c4d4d77fbbf807cb5fecedafafe1d0862ee603bd873eeacde19ee3`  
		Last Modified: Thu, 01 Oct 2020 21:52:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ebbc81b1bce09d47f457494db78dc2b05b58cafe77c0d7257a52f75f25b96b`  
		Last Modified: Thu, 01 Oct 2020 21:52:16 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb74e023eeca4f8d1ac717fb246f3fcd38a7556ad03b9a729f227d7ffced7869`  
		Last Modified: Thu, 01 Oct 2020 21:52:15 GMT  
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
$ docker pull influxdb@sha256:8c721a2509bde46d06f33a7af0cc41caa45f03eb233b23a97cc82b7d23d5dfc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-data` - linux; amd64

```console
$ docker pull influxdb@sha256:a6211a1d8e8e82c5f1205dd131ce81544149866ea3dbdc0bf2bfe9e65531affa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126258602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:161e93bd0218c6d17196a34a5873ab93a6cec73af5f223b3c926c13ec7102027`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:06:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 02 Oct 2020 01:35:22 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Fri, 02 Oct 2020 01:35:32 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Fri, 02 Oct 2020 01:35:32 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 02 Oct 2020 01:35:33 GMT
EXPOSE 8086
# Fri, 02 Oct 2020 01:35:33 GMT
VOLUME [/var/lib/influxdb]
# Fri, 02 Oct 2020 01:35:34 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 02 Oct 2020 01:35:34 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 02 Oct 2020 01:35:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:35:35 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b77385dee1edee19a023ac1167f1c1dd58640abfdb7cb19750575954d2db3`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfa539eca3101378bb4e420b15618767eb8727f0fa5372c0dd88c564aed49fd`  
		Last Modified: Fri, 02 Oct 2020 01:37:38 GMT  
		Size: 65.8 MB (65795964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ee98358a298acfc6f2dcfea4e80136153483aacac6736a860594fa8dea6c21`  
		Last Modified: Fri, 02 Oct 2020 01:37:27 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4712909e9d154c1145d32ac3f4aab0615ea1d1b15109c40a5ef4947038a051`  
		Last Modified: Fri, 02 Oct 2020 01:37:27 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcdc84420da154d1bfe0ebb037e9cdc50ed9d1a5d4efac8229fa2d5385fbbed`  
		Last Modified: Fri, 02 Oct 2020 01:37:27 GMT  
		Size: 1.3 KB (1280 bytes)  
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
$ docker pull influxdb@sha256:e0eb2c997a4d449cfe2c86a77b56b5c9c98ad5d067f929f971a9e6ab9071f4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:75e7cd9cebb7ace280266484332394262f78a92a271d3db04d6c07b674edf816
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83326705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc130274ba5f32f3a5ec1707ef2334245088d00f6cb67f5d35b701cf6c68398`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:06:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 02 Oct 2020 01:35:22 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Fri, 02 Oct 2020 01:36:07 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Fri, 02 Oct 2020 01:36:08 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 02 Oct 2020 01:36:08 GMT
EXPOSE 8091
# Fri, 02 Oct 2020 01:36:08 GMT
VOLUME [/var/lib/influxdb]
# Fri, 02 Oct 2020 01:36:09 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 02 Oct 2020 01:36:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:36:09 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b77385dee1edee19a023ac1167f1c1dd58640abfdb7cb19750575954d2db3`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a198a7b520fa375dd65e381016b5c6e7a886f0b6cfd91130ed658f06277e6497`  
		Last Modified: Fri, 02 Oct 2020 01:38:11 GMT  
		Size: 22.9 MB (22865271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a01adafd539c99a4a49d5f38eba7b460294cfa9ab7c78bd3825f9f2dcdff54b`  
		Last Modified: Fri, 02 Oct 2020 01:38:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5508a8f6d0a7d2482a2f60fc90c1131bd0ab7f9ca5a7ee578b4898053f9f96`  
		Last Modified: Fri, 02 Oct 2020 01:38:08 GMT  
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
$ docker pull influxdb@sha256:8c721a2509bde46d06f33a7af0cc41caa45f03eb233b23a97cc82b7d23d5dfc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:a6211a1d8e8e82c5f1205dd131ce81544149866ea3dbdc0bf2bfe9e65531affa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126258602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:161e93bd0218c6d17196a34a5873ab93a6cec73af5f223b3c926c13ec7102027`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:06:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 02 Oct 2020 01:35:22 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Fri, 02 Oct 2020 01:35:32 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Fri, 02 Oct 2020 01:35:32 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 02 Oct 2020 01:35:33 GMT
EXPOSE 8086
# Fri, 02 Oct 2020 01:35:33 GMT
VOLUME [/var/lib/influxdb]
# Fri, 02 Oct 2020 01:35:34 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 02 Oct 2020 01:35:34 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 02 Oct 2020 01:35:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:35:35 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b77385dee1edee19a023ac1167f1c1dd58640abfdb7cb19750575954d2db3`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfa539eca3101378bb4e420b15618767eb8727f0fa5372c0dd88c564aed49fd`  
		Last Modified: Fri, 02 Oct 2020 01:37:38 GMT  
		Size: 65.8 MB (65795964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ee98358a298acfc6f2dcfea4e80136153483aacac6736a860594fa8dea6c21`  
		Last Modified: Fri, 02 Oct 2020 01:37:27 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4712909e9d154c1145d32ac3f4aab0615ea1d1b15109c40a5ef4947038a051`  
		Last Modified: Fri, 02 Oct 2020 01:37:27 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcdc84420da154d1bfe0ebb037e9cdc50ed9d1a5d4efac8229fa2d5385fbbed`  
		Last Modified: Fri, 02 Oct 2020 01:37:27 GMT  
		Size: 1.3 KB (1280 bytes)  
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
$ docker pull influxdb@sha256:e0eb2c997a4d449cfe2c86a77b56b5c9c98ad5d067f929f971a9e6ab9071f4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:75e7cd9cebb7ace280266484332394262f78a92a271d3db04d6c07b674edf816
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83326705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc130274ba5f32f3a5ec1707ef2334245088d00f6cb67f5d35b701cf6c68398`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:06:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 02 Oct 2020 01:35:22 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Fri, 02 Oct 2020 01:36:07 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Fri, 02 Oct 2020 01:36:08 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 02 Oct 2020 01:36:08 GMT
EXPOSE 8091
# Fri, 02 Oct 2020 01:36:08 GMT
VOLUME [/var/lib/influxdb]
# Fri, 02 Oct 2020 01:36:09 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 02 Oct 2020 01:36:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:36:09 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b77385dee1edee19a023ac1167f1c1dd58640abfdb7cb19750575954d2db3`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a198a7b520fa375dd65e381016b5c6e7a886f0b6cfd91130ed658f06277e6497`  
		Last Modified: Fri, 02 Oct 2020 01:38:11 GMT  
		Size: 22.9 MB (22865271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a01adafd539c99a4a49d5f38eba7b460294cfa9ab7c78bd3825f9f2dcdff54b`  
		Last Modified: Fri, 02 Oct 2020 01:38:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5508a8f6d0a7d2482a2f60fc90c1131bd0ab7f9ca5a7ee578b4898053f9f96`  
		Last Modified: Fri, 02 Oct 2020 01:38:08 GMT  
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
$ docker pull influxdb@sha256:8c721a2509bde46d06f33a7af0cc41caa45f03eb233b23a97cc82b7d23d5dfc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:a6211a1d8e8e82c5f1205dd131ce81544149866ea3dbdc0bf2bfe9e65531affa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126258602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:161e93bd0218c6d17196a34a5873ab93a6cec73af5f223b3c926c13ec7102027`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:06:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 02 Oct 2020 01:35:22 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Fri, 02 Oct 2020 01:35:32 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Fri, 02 Oct 2020 01:35:32 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 02 Oct 2020 01:35:33 GMT
EXPOSE 8086
# Fri, 02 Oct 2020 01:35:33 GMT
VOLUME [/var/lib/influxdb]
# Fri, 02 Oct 2020 01:35:34 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 02 Oct 2020 01:35:34 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 02 Oct 2020 01:35:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:35:35 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b77385dee1edee19a023ac1167f1c1dd58640abfdb7cb19750575954d2db3`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfa539eca3101378bb4e420b15618767eb8727f0fa5372c0dd88c564aed49fd`  
		Last Modified: Fri, 02 Oct 2020 01:37:38 GMT  
		Size: 65.8 MB (65795964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ee98358a298acfc6f2dcfea4e80136153483aacac6736a860594fa8dea6c21`  
		Last Modified: Fri, 02 Oct 2020 01:37:27 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4712909e9d154c1145d32ac3f4aab0615ea1d1b15109c40a5ef4947038a051`  
		Last Modified: Fri, 02 Oct 2020 01:37:27 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcdc84420da154d1bfe0ebb037e9cdc50ed9d1a5d4efac8229fa2d5385fbbed`  
		Last Modified: Fri, 02 Oct 2020 01:37:27 GMT  
		Size: 1.3 KB (1280 bytes)  
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
$ docker pull influxdb@sha256:6c394679f243a0277214bc9006ed1cc0ff514688bfce5c7f2d69995862493eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:4c6ffc21a190bad583f276335abf08d3d4eaf16c16040940252a37e0df731189
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125428508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35de8cc24dfca8ad80fc93bba1bc7125240b3e27b457a1ef529aac5fb6217eef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:06:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 02 Oct 2020 01:34:42 GMT
ENV INFLUXDB_VERSION=1.8.3
# Fri, 02 Oct 2020 01:34:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Fri, 02 Oct 2020 01:34:53 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 02 Oct 2020 01:34:54 GMT
EXPOSE 8086
# Fri, 02 Oct 2020 01:34:54 GMT
VOLUME [/var/lib/influxdb]
# Fri, 02 Oct 2020 01:34:54 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 02 Oct 2020 01:34:55 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 02 Oct 2020 01:34:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:34:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b77385dee1edee19a023ac1167f1c1dd58640abfdb7cb19750575954d2db3`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5e595336ce87e06ffe8bab919e531d9a8f10e165773cb527601b9c4774bb11`  
		Last Modified: Fri, 02 Oct 2020 01:37:04 GMT  
		Size: 65.0 MB (64965928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bd745fdff76484cd933aec033616c6dd4da4ac16cf74e0a439408c5d0935f6`  
		Last Modified: Fri, 02 Oct 2020 01:36:51 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d8bed28c330d03ba01e47415bcf5f9357ad6bc534b358790a40de5d3b7287f`  
		Last Modified: Fri, 02 Oct 2020 01:36:52 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab924157a65ac65356204cbda230618107fe660d09983313d381d59ff536f9e1`  
		Last Modified: Fri, 02 Oct 2020 01:36:51 GMT  
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
$ docker pull influxdb@sha256:3e648bb4a09c7e8da9884ba0ea57a0efa1a04627c6a13003a8792600f82c0199
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117599020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2635e37ea28bfe980a9d7f800925d727fc01b839750d222e4bb983d4c7fa6456`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 09 Sep 2020 23:54:23 GMT
ADD file:f74bb8d38ef70a022988428f254630d1f424ed9a3b957687b0cd0f85b9d49e29 in / 
# Wed, 09 Sep 2020 23:54:25 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:35:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 19:48:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 01 Oct 2020 21:51:34 GMT
ENV INFLUXDB_VERSION=1.8.3
# Thu, 01 Oct 2020 21:51:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 01 Oct 2020 21:51:50 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 01 Oct 2020 21:51:51 GMT
EXPOSE 8086
# Thu, 01 Oct 2020 21:51:52 GMT
VOLUME [/var/lib/influxdb]
# Thu, 01 Oct 2020 21:51:53 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 01 Oct 2020 21:51:54 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 01 Oct 2020 21:51:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Oct 2020 21:51:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3b396f138ad78ffceac749b105c676dce568fa15a7b9f2273c2ee13ba023cea1`  
		Last Modified: Thu, 10 Sep 2020 00:01:33 GMT  
		Size: 43.2 MB (43171697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5db606bd1ccd8d11ca18492ee5d5122fdae2e7172ceb0df9cd15dc4d9f3c259`  
		Last Modified: Thu, 10 Sep 2020 00:45:55 GMT  
		Size: 9.7 MB (9700841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd3b5402f1859618a8e455e6bf04a916c8460da1c5f115568ba530c96f6ba3`  
		Last Modified: Thu, 10 Sep 2020 00:45:52 GMT  
		Size: 4.1 MB (4095176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b5628caff97d484a7850ebeeca0c0b9bc1f8c2c5844bbf8bb6258cfa6dc76e`  
		Last Modified: Thu, 10 Sep 2020 19:49:56 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f24d17df606a2dac7251c69f972d8f97ddfacfa2bec16caad1ab5375385a17`  
		Last Modified: Thu, 01 Oct 2020 21:52:33 GMT  
		Size: 60.6 MB (60626732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80c6c1cd5c4d4d77fbbf807cb5fecedafafe1d0862ee603bd873eeacde19ee3`  
		Last Modified: Thu, 01 Oct 2020 21:52:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ebbc81b1bce09d47f457494db78dc2b05b58cafe77c0d7257a52f75f25b96b`  
		Last Modified: Thu, 01 Oct 2020 21:52:16 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb74e023eeca4f8d1ac717fb246f3fcd38a7556ad03b9a729f227d7ffced7869`  
		Last Modified: Thu, 01 Oct 2020 21:52:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:e0eb2c997a4d449cfe2c86a77b56b5c9c98ad5d067f929f971a9e6ab9071f4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:75e7cd9cebb7ace280266484332394262f78a92a271d3db04d6c07b674edf816
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83326705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc130274ba5f32f3a5ec1707ef2334245088d00f6cb67f5d35b701cf6c68398`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Sep 2020 03:06:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 02 Oct 2020 01:35:22 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Fri, 02 Oct 2020 01:36:07 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Fri, 02 Oct 2020 01:36:08 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 02 Oct 2020 01:36:08 GMT
EXPOSE 8091
# Fri, 02 Oct 2020 01:36:08 GMT
VOLUME [/var/lib/influxdb]
# Fri, 02 Oct 2020 01:36:09 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 02 Oct 2020 01:36:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 01:36:09 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b77385dee1edee19a023ac1167f1c1dd58640abfdb7cb19750575954d2db3`  
		Last Modified: Fri, 11 Sep 2020 03:07:51 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a198a7b520fa375dd65e381016b5c6e7a886f0b6cfd91130ed658f06277e6497`  
		Last Modified: Fri, 02 Oct 2020 01:38:11 GMT  
		Size: 22.9 MB (22865271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a01adafd539c99a4a49d5f38eba7b460294cfa9ab7c78bd3825f9f2dcdff54b`  
		Last Modified: Fri, 02 Oct 2020 01:38:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5508a8f6d0a7d2482a2f60fc90c1131bd0ab7f9ca5a7ee578b4898053f9f96`  
		Last Modified: Fri, 02 Oct 2020 01:38:08 GMT  
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
