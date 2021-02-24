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
-	[`influxdb:1.8.3-data`](#influxdb183-data)
-	[`influxdb:1.8.3-data-alpine`](#influxdb183-data-alpine)
-	[`influxdb:1.8.3-meta`](#influxdb183-meta)
-	[`influxdb:1.8.3-meta-alpine`](#influxdb183-meta-alpine)
-	[`influxdb:1.8.4`](#influxdb184)
-	[`influxdb:1.8.4-alpine`](#influxdb184-alpine)
-	[`influxdb:1.8-alpine`](#influxdb18-alpine)
-	[`influxdb:1.8-data`](#influxdb18-data)
-	[`influxdb:1.8-data-alpine`](#influxdb18-data-alpine)
-	[`influxdb:1.8-meta`](#influxdb18-meta)
-	[`influxdb:1.8-meta-alpine`](#influxdb18-meta-alpine)
-	[`influxdb:2.0`](#influxdb20)
-	[`influxdb:2.0.4`](#influxdb204)
-	[`influxdb:2.0.4-alpine`](#influxdb204-alpine)
-	[`influxdb:2.0-alpine`](#influxdb20-alpine)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:data`](#influxdbdata)
-	[`influxdb:data-alpine`](#influxdbdata-alpine)
-	[`influxdb:latest`](#influxdblatest)
-	[`influxdb:meta`](#influxdbmeta)
-	[`influxdb:meta-alpine`](#influxdbmeta-alpine)

## `influxdb:1.7`

```console
$ docker pull influxdb@sha256:1960ac1003598e0ed7f4025f5da4058b3ee78328df344f32a9722e920ebe5309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7` - linux; amd64

```console
$ docker pull influxdb@sha256:d0bab180fd96f4fdb6540ad7643093d8caf21faa7f530b3e814f7fae0434708a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125092813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5616230bf2a9013175f05c816c89d00097b2cf7eb527d3b3fd9c90d70acf2d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:55:55 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 10 Feb 2021 04:56:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 10 Feb 2021 04:56:03 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 10 Feb 2021 04:56:03 GMT
EXPOSE 8086
# Wed, 10 Feb 2021 04:56:03 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:56:03 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:56:03 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Feb 2021 04:56:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:56:04 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f0c925438df84d4762925974fa9b347adb5dce48715acd5b548b9fec6ccff4`  
		Last Modified: Wed, 10 Feb 2021 04:58:08 GMT  
		Size: 64.1 MB (64097822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3495c03e1256c3827908e7c1e30fe4076e2286b9dc1d88b8b5d5bd90d804463b`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0281ac5a9a9620a1c9b83ccaa9823614869d84d631aafcc5fa1e86e6734d426`  
		Last Modified: Wed, 10 Feb 2021 04:57:59 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0891697c6072b912191fa07c825ea350448ac9d6fbf7c60aae7134cef65104c`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:c2cbe2c150a21e9d9dba26c5fb8bdb78718d9da623d6d47ad83a8170d7d87ee4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116595682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c33eac64bf64e240a37ffe21ad7211efb7d613e3d99c936f1c94409f0e3bbb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 03:04:53 GMT
ADD file:f884b9fc23d1b8ad0bd21aa823afd0ee186bdebb6829ccba72f77caaeffd8d12 in / 
# Tue, 09 Feb 2021 03:04:55 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:32:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:32:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 19:58:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 19:58:06 GMT
ENV INFLUXDB_VERSION=1.7.10
# Tue, 09 Feb 2021 19:58:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 09 Feb 2021 19:58:18 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 09 Feb 2021 19:58:19 GMT
EXPOSE 8086
# Tue, 09 Feb 2021 19:58:20 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Feb 2021 19:58:21 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 09 Feb 2021 19:58:21 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 09 Feb 2021 19:58:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 19:58:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:5275c778c803ce7d82407c77cfad4fb07fd1ec80fc99ba94cef475a92e4d090c`  
		Last Modified: Tue, 09 Feb 2021 03:13:25 GMT  
		Size: 42.1 MB (42119892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae60b5ed65c5d76acc7c0baf6fe0549a03f324c20d1882c25d60b44aaacaeba`  
		Last Modified: Tue, 09 Feb 2021 04:42:37 GMT  
		Size: 9.9 MB (9913736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99de29c3c448a06c87fa2f84824e9e1d0e9a9c7d7aebb93fce0ca22b55b6c9b`  
		Last Modified: Tue, 09 Feb 2021 04:42:35 GMT  
		Size: 3.9 MB (3921069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266519cf240cda7cb2dcf0551d5435701ea108d2186948c68c5731ad4de7ce03`  
		Last Modified: Tue, 09 Feb 2021 19:59:00 GMT  
		Size: 2.9 KB (2857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713f4d235b12069a40b6dfe010c0690d3400c424a72ba0f4e412f28a0df1fbd2`  
		Last Modified: Tue, 09 Feb 2021 19:59:16 GMT  
		Size: 60.6 MB (60636411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c22200cb267a1a0a8db329d30296f2145537248bb8a06f85d26d237b8ab26d`  
		Last Modified: Tue, 09 Feb 2021 19:59:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1682b000556c4ded272e985658b2954b4b8a341c4bb32807b94eb5896a7f8ec0`  
		Last Modified: Tue, 09 Feb 2021 19:59:00 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc938ac2809782d2101f78c39752449ff06127c2a8475321ef53a2bacbfb5c98`  
		Last Modified: Tue, 09 Feb 2021 19:59:00 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:854784de0250b67fc71cf23a5212dab7c0007592163e21618acfd4d327f46944
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117589919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e56c9f5a1a8e3b3fe1f8634603fc8da2c7d613f7611ff412a06b18d73d68da6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:43:17 GMT
ADD file:fb69ff7b2a28f793efbd16e04b74ffb4557d39e1844b3789075b4d3ff97a0eaa in / 
# Tue, 09 Feb 2021 02:43:20 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:50:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 23:17:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 23:17:19 GMT
ENV INFLUXDB_VERSION=1.7.10
# Tue, 09 Feb 2021 23:17:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 09 Feb 2021 23:17:30 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 09 Feb 2021 23:17:31 GMT
EXPOSE 8086
# Tue, 09 Feb 2021 23:17:33 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Feb 2021 23:17:34 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 09 Feb 2021 23:17:35 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 09 Feb 2021 23:17:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 23:17:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:296c9f0bf5f2cf24e87bc5abd674fc486e8df419d4aa2d362453f64d38900504`  
		Last Modified: Tue, 09 Feb 2021 02:49:43 GMT  
		Size: 43.2 MB (43177550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d546321c8e11789c75187b5b592633207519d75f96e8f03e8378d2da4a72a9`  
		Last Modified: Tue, 09 Feb 2021 05:00:16 GMT  
		Size: 10.2 MB (10182589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91c8ffe219846d18819503633eb252121c21cd20dbff74278b85c4029370992`  
		Last Modified: Tue, 09 Feb 2021 05:00:15 GMT  
		Size: 4.1 MB (4096615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc3bb22e13ab89a21825455644f82709870c5ca9d0f5dcc186f2794e987fbb0`  
		Last Modified: Tue, 09 Feb 2021 23:18:20 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f74c201e199200ed778b4bc839bb874980b6dd044f277dfac0e7544ad2d09e`  
		Last Modified: Tue, 09 Feb 2021 23:18:33 GMT  
		Size: 60.1 MB (60128599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4b3d78a1a06b79f022715c04b6f066a63341bbb8b41babf27c98f7c506de14`  
		Last Modified: Tue, 09 Feb 2021 23:18:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71abeabfd74bb5cb8bab83e09926514d62de03aa2150a5e70cc7e87e904cc3f8`  
		Last Modified: Tue, 09 Feb 2021 23:18:20 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dccd6da96f19506f0ed12a64fe6836b845b295695f0abc5761e3d1f1a632899`  
		Last Modified: Tue, 09 Feb 2021 23:18:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10`

```console
$ docker pull influxdb@sha256:1960ac1003598e0ed7f4025f5da4058b3ee78328df344f32a9722e920ebe5309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7.10` - linux; amd64

```console
$ docker pull influxdb@sha256:d0bab180fd96f4fdb6540ad7643093d8caf21faa7f530b3e814f7fae0434708a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125092813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5616230bf2a9013175f05c816c89d00097b2cf7eb527d3b3fd9c90d70acf2d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:55:55 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 10 Feb 2021 04:56:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 10 Feb 2021 04:56:03 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 10 Feb 2021 04:56:03 GMT
EXPOSE 8086
# Wed, 10 Feb 2021 04:56:03 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:56:03 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:56:03 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Feb 2021 04:56:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:56:04 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f0c925438df84d4762925974fa9b347adb5dce48715acd5b548b9fec6ccff4`  
		Last Modified: Wed, 10 Feb 2021 04:58:08 GMT  
		Size: 64.1 MB (64097822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3495c03e1256c3827908e7c1e30fe4076e2286b9dc1d88b8b5d5bd90d804463b`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0281ac5a9a9620a1c9b83ccaa9823614869d84d631aafcc5fa1e86e6734d426`  
		Last Modified: Wed, 10 Feb 2021 04:57:59 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0891697c6072b912191fa07c825ea350448ac9d6fbf7c60aae7134cef65104c`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:c2cbe2c150a21e9d9dba26c5fb8bdb78718d9da623d6d47ad83a8170d7d87ee4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116595682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c33eac64bf64e240a37ffe21ad7211efb7d613e3d99c936f1c94409f0e3bbb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 03:04:53 GMT
ADD file:f884b9fc23d1b8ad0bd21aa823afd0ee186bdebb6829ccba72f77caaeffd8d12 in / 
# Tue, 09 Feb 2021 03:04:55 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:32:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:32:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 19:58:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 19:58:06 GMT
ENV INFLUXDB_VERSION=1.7.10
# Tue, 09 Feb 2021 19:58:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 09 Feb 2021 19:58:18 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 09 Feb 2021 19:58:19 GMT
EXPOSE 8086
# Tue, 09 Feb 2021 19:58:20 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Feb 2021 19:58:21 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 09 Feb 2021 19:58:21 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 09 Feb 2021 19:58:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 19:58:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:5275c778c803ce7d82407c77cfad4fb07fd1ec80fc99ba94cef475a92e4d090c`  
		Last Modified: Tue, 09 Feb 2021 03:13:25 GMT  
		Size: 42.1 MB (42119892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae60b5ed65c5d76acc7c0baf6fe0549a03f324c20d1882c25d60b44aaacaeba`  
		Last Modified: Tue, 09 Feb 2021 04:42:37 GMT  
		Size: 9.9 MB (9913736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99de29c3c448a06c87fa2f84824e9e1d0e9a9c7d7aebb93fce0ca22b55b6c9b`  
		Last Modified: Tue, 09 Feb 2021 04:42:35 GMT  
		Size: 3.9 MB (3921069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266519cf240cda7cb2dcf0551d5435701ea108d2186948c68c5731ad4de7ce03`  
		Last Modified: Tue, 09 Feb 2021 19:59:00 GMT  
		Size: 2.9 KB (2857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713f4d235b12069a40b6dfe010c0690d3400c424a72ba0f4e412f28a0df1fbd2`  
		Last Modified: Tue, 09 Feb 2021 19:59:16 GMT  
		Size: 60.6 MB (60636411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c22200cb267a1a0a8db329d30296f2145537248bb8a06f85d26d237b8ab26d`  
		Last Modified: Tue, 09 Feb 2021 19:59:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1682b000556c4ded272e985658b2954b4b8a341c4bb32807b94eb5896a7f8ec0`  
		Last Modified: Tue, 09 Feb 2021 19:59:00 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc938ac2809782d2101f78c39752449ff06127c2a8475321ef53a2bacbfb5c98`  
		Last Modified: Tue, 09 Feb 2021 19:59:00 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:854784de0250b67fc71cf23a5212dab7c0007592163e21618acfd4d327f46944
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117589919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e56c9f5a1a8e3b3fe1f8634603fc8da2c7d613f7611ff412a06b18d73d68da6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:43:17 GMT
ADD file:fb69ff7b2a28f793efbd16e04b74ffb4557d39e1844b3789075b4d3ff97a0eaa in / 
# Tue, 09 Feb 2021 02:43:20 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:50:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 23:17:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 23:17:19 GMT
ENV INFLUXDB_VERSION=1.7.10
# Tue, 09 Feb 2021 23:17:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 09 Feb 2021 23:17:30 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 09 Feb 2021 23:17:31 GMT
EXPOSE 8086
# Tue, 09 Feb 2021 23:17:33 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Feb 2021 23:17:34 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 09 Feb 2021 23:17:35 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 09 Feb 2021 23:17:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 23:17:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:296c9f0bf5f2cf24e87bc5abd674fc486e8df419d4aa2d362453f64d38900504`  
		Last Modified: Tue, 09 Feb 2021 02:49:43 GMT  
		Size: 43.2 MB (43177550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d546321c8e11789c75187b5b592633207519d75f96e8f03e8378d2da4a72a9`  
		Last Modified: Tue, 09 Feb 2021 05:00:16 GMT  
		Size: 10.2 MB (10182589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91c8ffe219846d18819503633eb252121c21cd20dbff74278b85c4029370992`  
		Last Modified: Tue, 09 Feb 2021 05:00:15 GMT  
		Size: 4.1 MB (4096615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc3bb22e13ab89a21825455644f82709870c5ca9d0f5dcc186f2794e987fbb0`  
		Last Modified: Tue, 09 Feb 2021 23:18:20 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f74c201e199200ed778b4bc839bb874980b6dd044f277dfac0e7544ad2d09e`  
		Last Modified: Tue, 09 Feb 2021 23:18:33 GMT  
		Size: 60.1 MB (60128599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4b3d78a1a06b79f022715c04b6f066a63341bbb8b41babf27c98f7c506de14`  
		Last Modified: Tue, 09 Feb 2021 23:18:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71abeabfd74bb5cb8bab83e09926514d62de03aa2150a5e70cc7e87e904cc3f8`  
		Last Modified: Tue, 09 Feb 2021 23:18:20 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dccd6da96f19506f0ed12a64fe6836b845b295695f0abc5761e3d1f1a632899`  
		Last Modified: Tue, 09 Feb 2021 23:18:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-alpine`

```console
$ docker pull influxdb@sha256:775e645de86f5fa045d5f2395c2ca79ec4816d635edb3a3eb3d48b3b0e78d4ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:d51c6106662f02e811faf97bcef6a2a6913a0ef3d676b776f00e1afbcafc513c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68070188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946ee76bbc80ab07f2bc3dbb5934eb7c4de7f58024d5ac5cdf9e3dca8b888130`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:47:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 17 Dec 2020 13:47:22 GMT
ENV INFLUXDB_VERSION=1.7.10
# Thu, 17 Dec 2020 13:47:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:47:30 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 17 Dec 2020 13:47:31 GMT
EXPOSE 8086
# Thu, 17 Dec 2020 13:47:31 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 13:47:31 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 17 Dec 2020 13:47:31 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 17 Dec 2020 13:47:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:47:32 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1924738bc6407d8319fdb7d3fca610b5972213dee7ad608f4d801b3990f11a21`  
		Last Modified: Thu, 17 Dec 2020 13:49:35 GMT  
		Size: 1.4 MB (1428296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511d29ff60a150f0c897cbabbca1e1db59493a51bb5991ff7e87be68d032a2d9`  
		Last Modified: Thu, 17 Dec 2020 13:49:46 GMT  
		Size: 63.8 MB (63840959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5de96d55cbf03bad33a1be3c6ce83dff929a7ebef24ac93154aabbb30674490`  
		Last Modified: Thu, 17 Dec 2020 13:49:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f599f84c2c5eb886cceb5fb9d190dac3a4bca360f7085bdb97c83dfadbebbc6b`  
		Last Modified: Thu, 17 Dec 2020 13:49:34 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9945b200342d04735e6160898c3882898c4a1570b22b27157d72854b8d566e68`  
		Last Modified: Thu, 17 Dec 2020 13:49:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-data`

```console
$ docker pull influxdb@sha256:4af280a9420a33eccb8fbcc5ebf6c073759b5fe9309f1fada837860bc32a7872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:a58844cf163a4c4f289134a50d4fbf055806d77d8b101962c15904fcef08060e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148908169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb96bda809ce7fad53c4783719ee9d16e4f4055f19a59e0aad401167ccbd57f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:56:12 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 10 Feb 2021 04:56:22 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Feb 2021 04:56:22 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 10 Feb 2021 04:56:22 GMT
EXPOSE 8086
# Wed, 10 Feb 2021 04:56:23 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:56:23 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:56:23 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Feb 2021 04:56:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:56:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7726fa0aee1911fd933abaf235a87e9ffe1b2634ca67cd6816ed91df579ad587`  
		Last Modified: Wed, 10 Feb 2021 04:58:27 GMT  
		Size: 87.9 MB (87913121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4339ee43e029207b966b143a846da54c5c13ff540f26a49a6b33fde7a7f2a`  
		Last Modified: Wed, 10 Feb 2021 04:58:14 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e1aaf6a49d5b0be78daa7e32333521838a3454702e6bbbfacff86075bd911e`  
		Last Modified: Wed, 10 Feb 2021 04:58:14 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3429ae36607fca2ac5eccda45c507332cf32273f7dd66839ef20b3833adf50ed`  
		Last Modified: Wed, 10 Feb 2021 04:58:14 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-data-alpine`

```console
$ docker pull influxdb@sha256:2b8174c4527c4344779a259b65f1e994d610c22e48d0e9ef08159fa1879db538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:1aada19288a09e51e979d64d825416c9c4019a5d54a73d1d86ecd92b5ed4d936
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91833013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e846d9cdf372741355f7ff7a345adc7bf12038650298d2d65eada44bd6b1597`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:47:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 17 Dec 2020 13:47:40 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Thu, 17 Dec 2020 13:47:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:47:50 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 17 Dec 2020 13:47:50 GMT
EXPOSE 8086
# Thu, 17 Dec 2020 13:47:51 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 13:47:51 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 17 Dec 2020 13:47:51 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 17 Dec 2020 13:47:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:47:52 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1924738bc6407d8319fdb7d3fca610b5972213dee7ad608f4d801b3990f11a21`  
		Last Modified: Thu, 17 Dec 2020 13:49:35 GMT  
		Size: 1.4 MB (1428296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65dd6e6ca392bfd9c0443ca825222f9caa722e13a8d0f97181d82b9336666f56`  
		Last Modified: Thu, 17 Dec 2020 13:50:09 GMT  
		Size: 87.6 MB (87603725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd248e147bc17ad4584e1373ca1406b31caca773d6cabe1c3f05ef36410cb66`  
		Last Modified: Thu, 17 Dec 2020 13:49:53 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79190b655b57c228c95a7fa6fdc71fe5db4a4fb3ee6d015ad3e521a7da7d3844`  
		Last Modified: Thu, 17 Dec 2020 13:49:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc067c0916f35d8ae60aa3959d71eb5903c389839000e351a4c184ff39585f2`  
		Last Modified: Thu, 17 Dec 2020 13:49:54 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-meta`

```console
$ docker pull influxdb@sha256:bd2ade536a4d86c0fbb698e8bd82336be74f991d3aa623a1e83959fbff6df71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:0ef3b034d2c4d595316a40f463e392c906705fed078984b245b3aa6dcdb41f40
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84127444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec9dbe621d18f119a21ce994e923cecfd0608928b8cb8da95cdd9d639fdec97`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:56:12 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 10 Feb 2021 04:56:35 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Feb 2021 04:56:36 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 10 Feb 2021 04:56:36 GMT
EXPOSE 8091
# Wed, 10 Feb 2021 04:56:36 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:56:36 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:56:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:56:37 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37485044ae75fc05a5c133877602f1e563f02702daa88e69dbaf6964262eafa7`  
		Last Modified: Wed, 10 Feb 2021 04:58:36 GMT  
		Size: 23.1 MB (23133606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee04e9fe70d35e8397f670bec3673cf5beb018e5952b9b65d9231d4b708462fa`  
		Last Modified: Wed, 10 Feb 2021 04:58:32 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3984387e1cc482d4c47e13155cc6cced0ecd5d4c215de9081209b028d257259a`  
		Last Modified: Wed, 10 Feb 2021 04:58:32 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-meta-alpine`

```console
$ docker pull influxdb@sha256:de16392636e76e08ab574dd858057a6b975c782c8b5c0b416733e029ce25b5e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:156abf7250306d6f8dcbff15092cef2b76844b7c018d606fc6a62116e89f4f34
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27230754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d7485cab53b185859b0e6762551835468f6f52cc194a69b4e734ddebcf905f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:47:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 17 Dec 2020 13:47:40 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Thu, 17 Dec 2020 13:48:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:48:04 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 17 Dec 2020 13:48:04 GMT
EXPOSE 8091
# Thu, 17 Dec 2020 13:48:05 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 13:48:05 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 17 Dec 2020 13:48:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:48:05 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1924738bc6407d8319fdb7d3fca610b5972213dee7ad608f4d801b3990f11a21`  
		Last Modified: Thu, 17 Dec 2020 13:49:35 GMT  
		Size: 1.4 MB (1428296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810893317995e32ec408ab5a96f97680ed29491804e058a06afc02b4f9764fe9`  
		Last Modified: Thu, 17 Dec 2020 13:50:21 GMT  
		Size: 23.0 MB (23002670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a373124bdc8b99e201610f79430294e29f7444345987bb5ca2c4042360d2f539`  
		Last Modified: Thu, 17 Dec 2020 13:50:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fcd2ae59d54ca79585f5a7888535850738abff6ce791ed0b1061ba560ffda83`  
		Last Modified: Thu, 17 Dec 2020 13:50:18 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-alpine`

```console
$ docker pull influxdb@sha256:775e645de86f5fa045d5f2395c2ca79ec4816d635edb3a3eb3d48b3b0e78d4ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:d51c6106662f02e811faf97bcef6a2a6913a0ef3d676b776f00e1afbcafc513c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68070188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946ee76bbc80ab07f2bc3dbb5934eb7c4de7f58024d5ac5cdf9e3dca8b888130`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:47:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 17 Dec 2020 13:47:22 GMT
ENV INFLUXDB_VERSION=1.7.10
# Thu, 17 Dec 2020 13:47:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:47:30 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 17 Dec 2020 13:47:31 GMT
EXPOSE 8086
# Thu, 17 Dec 2020 13:47:31 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 13:47:31 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 17 Dec 2020 13:47:31 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 17 Dec 2020 13:47:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:47:32 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1924738bc6407d8319fdb7d3fca610b5972213dee7ad608f4d801b3990f11a21`  
		Last Modified: Thu, 17 Dec 2020 13:49:35 GMT  
		Size: 1.4 MB (1428296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511d29ff60a150f0c897cbabbca1e1db59493a51bb5991ff7e87be68d032a2d9`  
		Last Modified: Thu, 17 Dec 2020 13:49:46 GMT  
		Size: 63.8 MB (63840959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5de96d55cbf03bad33a1be3c6ce83dff929a7ebef24ac93154aabbb30674490`  
		Last Modified: Thu, 17 Dec 2020 13:49:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f599f84c2c5eb886cceb5fb9d190dac3a4bca360f7085bdb97c83dfadbebbc6b`  
		Last Modified: Thu, 17 Dec 2020 13:49:34 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9945b200342d04735e6160898c3882898c4a1570b22b27157d72854b8d566e68`  
		Last Modified: Thu, 17 Dec 2020 13:49:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-data`

```console
$ docker pull influxdb@sha256:4af280a9420a33eccb8fbcc5ebf6c073759b5fe9309f1fada837860bc32a7872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:a58844cf163a4c4f289134a50d4fbf055806d77d8b101962c15904fcef08060e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148908169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb96bda809ce7fad53c4783719ee9d16e4f4055f19a59e0aad401167ccbd57f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:56:12 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 10 Feb 2021 04:56:22 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Feb 2021 04:56:22 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 10 Feb 2021 04:56:22 GMT
EXPOSE 8086
# Wed, 10 Feb 2021 04:56:23 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:56:23 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:56:23 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Feb 2021 04:56:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:56:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7726fa0aee1911fd933abaf235a87e9ffe1b2634ca67cd6816ed91df579ad587`  
		Last Modified: Wed, 10 Feb 2021 04:58:27 GMT  
		Size: 87.9 MB (87913121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4339ee43e029207b966b143a846da54c5c13ff540f26a49a6b33fde7a7f2a`  
		Last Modified: Wed, 10 Feb 2021 04:58:14 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e1aaf6a49d5b0be78daa7e32333521838a3454702e6bbbfacff86075bd911e`  
		Last Modified: Wed, 10 Feb 2021 04:58:14 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3429ae36607fca2ac5eccda45c507332cf32273f7dd66839ef20b3833adf50ed`  
		Last Modified: Wed, 10 Feb 2021 04:58:14 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-data-alpine`

```console
$ docker pull influxdb@sha256:2b8174c4527c4344779a259b65f1e994d610c22e48d0e9ef08159fa1879db538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:1aada19288a09e51e979d64d825416c9c4019a5d54a73d1d86ecd92b5ed4d936
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91833013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e846d9cdf372741355f7ff7a345adc7bf12038650298d2d65eada44bd6b1597`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:47:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 17 Dec 2020 13:47:40 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Thu, 17 Dec 2020 13:47:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:47:50 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 17 Dec 2020 13:47:50 GMT
EXPOSE 8086
# Thu, 17 Dec 2020 13:47:51 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 13:47:51 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 17 Dec 2020 13:47:51 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 17 Dec 2020 13:47:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:47:52 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1924738bc6407d8319fdb7d3fca610b5972213dee7ad608f4d801b3990f11a21`  
		Last Modified: Thu, 17 Dec 2020 13:49:35 GMT  
		Size: 1.4 MB (1428296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65dd6e6ca392bfd9c0443ca825222f9caa722e13a8d0f97181d82b9336666f56`  
		Last Modified: Thu, 17 Dec 2020 13:50:09 GMT  
		Size: 87.6 MB (87603725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd248e147bc17ad4584e1373ca1406b31caca773d6cabe1c3f05ef36410cb66`  
		Last Modified: Thu, 17 Dec 2020 13:49:53 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79190b655b57c228c95a7fa6fdc71fe5db4a4fb3ee6d015ad3e521a7da7d3844`  
		Last Modified: Thu, 17 Dec 2020 13:49:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc067c0916f35d8ae60aa3959d71eb5903c389839000e351a4c184ff39585f2`  
		Last Modified: Thu, 17 Dec 2020 13:49:54 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-meta`

```console
$ docker pull influxdb@sha256:bd2ade536a4d86c0fbb698e8bd82336be74f991d3aa623a1e83959fbff6df71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:0ef3b034d2c4d595316a40f463e392c906705fed078984b245b3aa6dcdb41f40
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84127444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec9dbe621d18f119a21ce994e923cecfd0608928b8cb8da95cdd9d639fdec97`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:56:12 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 10 Feb 2021 04:56:35 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Feb 2021 04:56:36 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 10 Feb 2021 04:56:36 GMT
EXPOSE 8091
# Wed, 10 Feb 2021 04:56:36 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:56:36 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:56:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:56:37 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37485044ae75fc05a5c133877602f1e563f02702daa88e69dbaf6964262eafa7`  
		Last Modified: Wed, 10 Feb 2021 04:58:36 GMT  
		Size: 23.1 MB (23133606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee04e9fe70d35e8397f670bec3673cf5beb018e5952b9b65d9231d4b708462fa`  
		Last Modified: Wed, 10 Feb 2021 04:58:32 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3984387e1cc482d4c47e13155cc6cced0ecd5d4c215de9081209b028d257259a`  
		Last Modified: Wed, 10 Feb 2021 04:58:32 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-meta-alpine`

```console
$ docker pull influxdb@sha256:de16392636e76e08ab574dd858057a6b975c782c8b5c0b416733e029ce25b5e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:156abf7250306d6f8dcbff15092cef2b76844b7c018d606fc6a62116e89f4f34
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27230754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d7485cab53b185859b0e6762551835468f6f52cc194a69b4e734ddebcf905f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:47:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 17 Dec 2020 13:47:40 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Thu, 17 Dec 2020 13:48:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:48:04 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 17 Dec 2020 13:48:04 GMT
EXPOSE 8091
# Thu, 17 Dec 2020 13:48:05 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 13:48:05 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 17 Dec 2020 13:48:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:48:05 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1924738bc6407d8319fdb7d3fca610b5972213dee7ad608f4d801b3990f11a21`  
		Last Modified: Thu, 17 Dec 2020 13:49:35 GMT  
		Size: 1.4 MB (1428296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810893317995e32ec408ab5a96f97680ed29491804e058a06afc02b4f9764fe9`  
		Last Modified: Thu, 17 Dec 2020 13:50:21 GMT  
		Size: 23.0 MB (23002670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a373124bdc8b99e201610f79430294e29f7444345987bb5ca2c4042360d2f539`  
		Last Modified: Thu, 17 Dec 2020 13:50:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fcd2ae59d54ca79585f5a7888535850738abff6ce791ed0b1061ba560ffda83`  
		Last Modified: Thu, 17 Dec 2020 13:50:18 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8`

```console
$ docker pull influxdb@sha256:a66fa6bd81bee3c70e6c408235af068422ab73d74aa5d6acfc09dc76eba0ebf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8` - linux; amd64

```console
$ docker pull influxdb@sha256:7539edbf76df0498f730904827f859aa4c67e1386cb72601019d72ec3e12ed0c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125961499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7870fcea362222d648815a18c6d949e3faae225b97b8c0ee7cc27b74e9d8c45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:56:44 GMT
ENV INFLUXDB_VERSION=1.8.4
# Wed, 10 Feb 2021 04:56:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 10 Feb 2021 04:56:52 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 10 Feb 2021 04:56:52 GMT
EXPOSE 8086
# Wed, 10 Feb 2021 04:56:52 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:56:52 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:56:52 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Feb 2021 04:56:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:56:53 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0907122426ac6b2c48c0e3da39e10da254ba8f0e10be1600731b210881c4ef`  
		Last Modified: Wed, 10 Feb 2021 04:58:50 GMT  
		Size: 65.0 MB (64966512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d3d7e535c1e62ce9dfa85b05ccb228f0cbf722440cb8958e74580f3de94dd3`  
		Last Modified: Wed, 10 Feb 2021 04:58:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45b611f60bfbba58da3ec97f086ba4c4dfeb487aef823873770166635986f00`  
		Last Modified: Wed, 10 Feb 2021 04:58:40 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7c9bc15cec46afb70a351b3614181ae2cab6e938d478f34bfbfe2cdda2dcd1`  
		Last Modified: Wed, 10 Feb 2021 04:58:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:5860a6f7fce49f8a6d7abb08246752f8f0b000a1b732817e9dc09ad998dfb521
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117019220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b981467ac4ae2e2898af181253117226acacf5235d51bbd0942434847568d9d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 03:04:53 GMT
ADD file:f884b9fc23d1b8ad0bd21aa823afd0ee186bdebb6829ccba72f77caaeffd8d12 in / 
# Tue, 09 Feb 2021 03:04:55 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:32:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:32:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 19:58:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 19:58:30 GMT
ENV INFLUXDB_VERSION=1.8.4
# Tue, 09 Feb 2021 19:58:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 09 Feb 2021 19:58:42 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 09 Feb 2021 19:58:42 GMT
EXPOSE 8086
# Tue, 09 Feb 2021 19:58:43 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Feb 2021 19:58:44 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 09 Feb 2021 19:58:45 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 09 Feb 2021 19:58:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 19:58:47 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:5275c778c803ce7d82407c77cfad4fb07fd1ec80fc99ba94cef475a92e4d090c`  
		Last Modified: Tue, 09 Feb 2021 03:13:25 GMT  
		Size: 42.1 MB (42119892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae60b5ed65c5d76acc7c0baf6fe0549a03f324c20d1882c25d60b44aaacaeba`  
		Last Modified: Tue, 09 Feb 2021 04:42:37 GMT  
		Size: 9.9 MB (9913736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99de29c3c448a06c87fa2f84824e9e1d0e9a9c7d7aebb93fce0ca22b55b6c9b`  
		Last Modified: Tue, 09 Feb 2021 04:42:35 GMT  
		Size: 3.9 MB (3921069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266519cf240cda7cb2dcf0551d5435701ea108d2186948c68c5731ad4de7ce03`  
		Last Modified: Tue, 09 Feb 2021 19:59:00 GMT  
		Size: 2.9 KB (2857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566dbce2ab0602ce6e21d013e2ef27c24203069bc940c37f70bd22415997cc60`  
		Last Modified: Tue, 09 Feb 2021 19:59:40 GMT  
		Size: 61.1 MB (61059949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0ef9b950cdaed2cc4f6dfb3d0928afded1350969752156ea669344206594b7`  
		Last Modified: Tue, 09 Feb 2021 19:59:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b8013e08b555d7e35d41afb6ce6592ca229da53f7907cc90145c4a2f29113f`  
		Last Modified: Tue, 09 Feb 2021 19:59:23 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206c65c8a4e22d8f7f0dcc8a4cb52960651dcd3267a8301efc9a9b1c77766474`  
		Last Modified: Tue, 09 Feb 2021 19:59:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:cecdf09bdae2736f4cfeea2157e2e04baf728ae09a2d087bdd8081dfdc387277
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118090458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9473609f3c55065609f52855ca8def2f9a505f5876b1f1eedc16049206fd35c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:43:17 GMT
ADD file:fb69ff7b2a28f793efbd16e04b74ffb4557d39e1844b3789075b4d3ff97a0eaa in / 
# Tue, 09 Feb 2021 02:43:20 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:50:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 23:17:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 23:17:49 GMT
ENV INFLUXDB_VERSION=1.8.4
# Tue, 09 Feb 2021 23:17:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 09 Feb 2021 23:18:00 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 09 Feb 2021 23:18:00 GMT
EXPOSE 8086
# Tue, 09 Feb 2021 23:18:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Feb 2021 23:18:02 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 09 Feb 2021 23:18:03 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 09 Feb 2021 23:18:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 23:18:04 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:296c9f0bf5f2cf24e87bc5abd674fc486e8df419d4aa2d362453f64d38900504`  
		Last Modified: Tue, 09 Feb 2021 02:49:43 GMT  
		Size: 43.2 MB (43177550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d546321c8e11789c75187b5b592633207519d75f96e8f03e8378d2da4a72a9`  
		Last Modified: Tue, 09 Feb 2021 05:00:16 GMT  
		Size: 10.2 MB (10182589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91c8ffe219846d18819503633eb252121c21cd20dbff74278b85c4029370992`  
		Last Modified: Tue, 09 Feb 2021 05:00:15 GMT  
		Size: 4.1 MB (4096615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc3bb22e13ab89a21825455644f82709870c5ca9d0f5dcc186f2794e987fbb0`  
		Last Modified: Tue, 09 Feb 2021 23:18:20 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b55933c9b8cf91ab120a56ebee961c795c2f781c696d2ce72ce6ffd35190d7`  
		Last Modified: Tue, 09 Feb 2021 23:18:53 GMT  
		Size: 60.6 MB (60629135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739b5dbd7dbd5e775bb785f8311d2446b7da2b091ffcf6388f0649af38d4413e`  
		Last Modified: Tue, 09 Feb 2021 23:18:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0f5eef745245986f16357dd49791608ad6e8b60307d32bfbe1412b22d8c298`  
		Last Modified: Tue, 09 Feb 2021 23:18:41 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556a000a3eaa8c4c8c0043bfc2c731ff16a702b0d1909eb2893f2cd8e26f1033`  
		Last Modified: Tue, 09 Feb 2021 23:18:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-data`

```console
$ docker pull influxdb@sha256:67876cecbc722648d5eaf17c64854ae57beafca233a55416e95fc212de64bd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-data` - linux; amd64

```console
$ docker pull influxdb@sha256:9ad29edf6629eeeed7540d003ace92750e12e733055524dc08bc50c682eb8dec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126791523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1586215b740555a75748269f512871688d91312d26491ad08a114601e96719b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:57:02 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 10 Feb 2021 04:57:10 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Feb 2021 04:57:10 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 10 Feb 2021 04:57:10 GMT
EXPOSE 8086
# Wed, 10 Feb 2021 04:57:10 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:57:11 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:57:11 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Feb 2021 04:57:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:57:11 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d29e7e8838f6b925c171a67948b5f3bf44fca76a2428583987f3a7474f9e50`  
		Last Modified: Wed, 10 Feb 2021 04:59:10 GMT  
		Size: 65.8 MB (65796478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb80241906ed39ac62840cac80202f837585b84e0224d24571b11c957148879`  
		Last Modified: Wed, 10 Feb 2021 04:59:01 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d44b9df77d08197aca251c63136878d862be3c48adb4878bace9022c7761a3f`  
		Last Modified: Wed, 10 Feb 2021 04:59:01 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a88d904c7edfc7e2abba83d7274f2c25ff792d2688362e3f290b40a35b8f6da`  
		Last Modified: Wed, 10 Feb 2021 04:59:01 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-data-alpine`

```console
$ docker pull influxdb@sha256:1f76bcc17b25bea15aa83eba37ae79913bb097973c16510c29426683554ffa78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ca8eb83702c42e6842af42682894c786ed7df4ccad01039da5e44b25987f621e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69770238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c93b32605cb2f94cf639d1f32c08a983526c4557abd14fe6292fc0d2fa3607`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:47:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 17 Dec 2020 13:48:32 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Thu, 17 Dec 2020 13:48:39 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:48:39 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 17 Dec 2020 13:48:39 GMT
EXPOSE 8086
# Thu, 17 Dec 2020 13:48:39 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 13:48:39 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 17 Dec 2020 13:48:40 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 17 Dec 2020 13:48:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:48:40 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1924738bc6407d8319fdb7d3fca610b5972213dee7ad608f4d801b3990f11a21`  
		Last Modified: Thu, 17 Dec 2020 13:49:35 GMT  
		Size: 1.4 MB (1428296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6edf7ef0639b641e2a6c111b20bb8d65c63a939fb49f70007b70b6a18cd225`  
		Last Modified: Thu, 17 Dec 2020 13:51:10 GMT  
		Size: 65.5 MB (65540953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976d9c1bb701d9b9686a9c72d1711cb0e6b27061b3f6950efbadbbab20dad7bf`  
		Last Modified: Thu, 17 Dec 2020 13:50:58 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d3881e28e4b6909bfc1fd929606827018b6dfb44e91a07edf855afb0f7e856`  
		Last Modified: Thu, 17 Dec 2020 13:50:58 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a300eda57a9818ae4a90aaf183c2476f4e828cbc9073271ec5bffdc644b6e7b2`  
		Last Modified: Thu, 17 Dec 2020 13:50:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-meta`

```console
$ docker pull influxdb@sha256:83e2e77f7ef83ceaa7549f44058d12f255301a99fe7ba6cc1a6f4d8a9fe0cb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:ffe8c67e7d6a188fe1378ca1541b43740e07f77497f65aacd47103897defe8ae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83859997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d706e62f1b535daeefd18b8bde7816e8310504c1c995ebc1701323883d94d74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:57:02 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 10 Feb 2021 04:57:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Feb 2021 04:57:24 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 10 Feb 2021 04:57:24 GMT
EXPOSE 8091
# Wed, 10 Feb 2021 04:57:24 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:57:24 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:57:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:57:25 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97ba6effd1841113e069182d033c17f3bdbbd57c3b3e9347abdc2bdecdde2ef`  
		Last Modified: Wed, 10 Feb 2021 04:59:23 GMT  
		Size: 22.9 MB (22866156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b75a883c5a79201ac582bb3980ed32e7f034f2f6ae3ec49667a25f4582463bf`  
		Last Modified: Wed, 10 Feb 2021 04:59:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ebe920089e36547964e057f165cf7102ff2925b478a707d02b94ebd670efe2`  
		Last Modified: Wed, 10 Feb 2021 04:59:17 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-meta-alpine`

```console
$ docker pull influxdb@sha256:4c29eac32909a131cfaff0592d154d70dd7dfe0478cb9540c2901ddf0da5fae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:dca974575db512c53831bde49ddf78ac0dcf4d82dc22079be452c62da4ba5682
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26963560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8881cbf80321dc2a4ebdf2195439034efa5d7c8d21b315de81395c705b9129c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:47:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 17 Dec 2020 13:48:32 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Thu, 17 Dec 2020 13:48:52 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:48:52 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 17 Dec 2020 13:48:53 GMT
EXPOSE 8091
# Thu, 17 Dec 2020 13:48:53 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 13:48:54 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 17 Dec 2020 13:48:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:48:54 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1924738bc6407d8319fdb7d3fca610b5972213dee7ad608f4d801b3990f11a21`  
		Last Modified: Thu, 17 Dec 2020 13:49:35 GMT  
		Size: 1.4 MB (1428296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160bf10769c16bdb7542730ceba295bdfb41ccdcc94aad7899def6ebc89b50f5`  
		Last Modified: Thu, 17 Dec 2020 13:51:26 GMT  
		Size: 22.7 MB (22735478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc8f9cb3bd7cd3e189107cbd62ad4c10e03619dda2334334e9472e68bed697b`  
		Last Modified: Thu, 17 Dec 2020 13:51:20 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74170b5ea5a39ad5a9878ee9a90ab8f39e7d7331d10ead82b0ed7f28cd4f007`  
		Last Modified: Thu, 17 Dec 2020 13:51:22 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.4`

```console
$ docker pull influxdb@sha256:a66fa6bd81bee3c70e6c408235af068422ab73d74aa5d6acfc09dc76eba0ebf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8.4` - linux; amd64

```console
$ docker pull influxdb@sha256:7539edbf76df0498f730904827f859aa4c67e1386cb72601019d72ec3e12ed0c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125961499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7870fcea362222d648815a18c6d949e3faae225b97b8c0ee7cc27b74e9d8c45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:56:44 GMT
ENV INFLUXDB_VERSION=1.8.4
# Wed, 10 Feb 2021 04:56:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 10 Feb 2021 04:56:52 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 10 Feb 2021 04:56:52 GMT
EXPOSE 8086
# Wed, 10 Feb 2021 04:56:52 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:56:52 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:56:52 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Feb 2021 04:56:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:56:53 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0907122426ac6b2c48c0e3da39e10da254ba8f0e10be1600731b210881c4ef`  
		Last Modified: Wed, 10 Feb 2021 04:58:50 GMT  
		Size: 65.0 MB (64966512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d3d7e535c1e62ce9dfa85b05ccb228f0cbf722440cb8958e74580f3de94dd3`  
		Last Modified: Wed, 10 Feb 2021 04:58:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45b611f60bfbba58da3ec97f086ba4c4dfeb487aef823873770166635986f00`  
		Last Modified: Wed, 10 Feb 2021 04:58:40 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7c9bc15cec46afb70a351b3614181ae2cab6e938d478f34bfbfe2cdda2dcd1`  
		Last Modified: Wed, 10 Feb 2021 04:58:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.4` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:5860a6f7fce49f8a6d7abb08246752f8f0b000a1b732817e9dc09ad998dfb521
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117019220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b981467ac4ae2e2898af181253117226acacf5235d51bbd0942434847568d9d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 03:04:53 GMT
ADD file:f884b9fc23d1b8ad0bd21aa823afd0ee186bdebb6829ccba72f77caaeffd8d12 in / 
# Tue, 09 Feb 2021 03:04:55 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:32:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:32:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 19:58:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 19:58:30 GMT
ENV INFLUXDB_VERSION=1.8.4
# Tue, 09 Feb 2021 19:58:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 09 Feb 2021 19:58:42 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 09 Feb 2021 19:58:42 GMT
EXPOSE 8086
# Tue, 09 Feb 2021 19:58:43 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Feb 2021 19:58:44 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 09 Feb 2021 19:58:45 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 09 Feb 2021 19:58:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 19:58:47 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:5275c778c803ce7d82407c77cfad4fb07fd1ec80fc99ba94cef475a92e4d090c`  
		Last Modified: Tue, 09 Feb 2021 03:13:25 GMT  
		Size: 42.1 MB (42119892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae60b5ed65c5d76acc7c0baf6fe0549a03f324c20d1882c25d60b44aaacaeba`  
		Last Modified: Tue, 09 Feb 2021 04:42:37 GMT  
		Size: 9.9 MB (9913736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99de29c3c448a06c87fa2f84824e9e1d0e9a9c7d7aebb93fce0ca22b55b6c9b`  
		Last Modified: Tue, 09 Feb 2021 04:42:35 GMT  
		Size: 3.9 MB (3921069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266519cf240cda7cb2dcf0551d5435701ea108d2186948c68c5731ad4de7ce03`  
		Last Modified: Tue, 09 Feb 2021 19:59:00 GMT  
		Size: 2.9 KB (2857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566dbce2ab0602ce6e21d013e2ef27c24203069bc940c37f70bd22415997cc60`  
		Last Modified: Tue, 09 Feb 2021 19:59:40 GMT  
		Size: 61.1 MB (61059949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0ef9b950cdaed2cc4f6dfb3d0928afded1350969752156ea669344206594b7`  
		Last Modified: Tue, 09 Feb 2021 19:59:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b8013e08b555d7e35d41afb6ce6592ca229da53f7907cc90145c4a2f29113f`  
		Last Modified: Tue, 09 Feb 2021 19:59:23 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206c65c8a4e22d8f7f0dcc8a4cb52960651dcd3267a8301efc9a9b1c77766474`  
		Last Modified: Tue, 09 Feb 2021 19:59:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.4` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:cecdf09bdae2736f4cfeea2157e2e04baf728ae09a2d087bdd8081dfdc387277
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118090458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9473609f3c55065609f52855ca8def2f9a505f5876b1f1eedc16049206fd35c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:43:17 GMT
ADD file:fb69ff7b2a28f793efbd16e04b74ffb4557d39e1844b3789075b4d3ff97a0eaa in / 
# Tue, 09 Feb 2021 02:43:20 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:50:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 23:17:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 23:17:49 GMT
ENV INFLUXDB_VERSION=1.8.4
# Tue, 09 Feb 2021 23:17:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 09 Feb 2021 23:18:00 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 09 Feb 2021 23:18:00 GMT
EXPOSE 8086
# Tue, 09 Feb 2021 23:18:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Feb 2021 23:18:02 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 09 Feb 2021 23:18:03 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 09 Feb 2021 23:18:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 23:18:04 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:296c9f0bf5f2cf24e87bc5abd674fc486e8df419d4aa2d362453f64d38900504`  
		Last Modified: Tue, 09 Feb 2021 02:49:43 GMT  
		Size: 43.2 MB (43177550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d546321c8e11789c75187b5b592633207519d75f96e8f03e8378d2da4a72a9`  
		Last Modified: Tue, 09 Feb 2021 05:00:16 GMT  
		Size: 10.2 MB (10182589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91c8ffe219846d18819503633eb252121c21cd20dbff74278b85c4029370992`  
		Last Modified: Tue, 09 Feb 2021 05:00:15 GMT  
		Size: 4.1 MB (4096615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc3bb22e13ab89a21825455644f82709870c5ca9d0f5dcc186f2794e987fbb0`  
		Last Modified: Tue, 09 Feb 2021 23:18:20 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b55933c9b8cf91ab120a56ebee961c795c2f781c696d2ce72ce6ffd35190d7`  
		Last Modified: Tue, 09 Feb 2021 23:18:53 GMT  
		Size: 60.6 MB (60629135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739b5dbd7dbd5e775bb785f8311d2446b7da2b091ffcf6388f0649af38d4413e`  
		Last Modified: Tue, 09 Feb 2021 23:18:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0f5eef745245986f16357dd49791608ad6e8b60307d32bfbe1412b22d8c298`  
		Last Modified: Tue, 09 Feb 2021 23:18:41 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556a000a3eaa8c4c8c0043bfc2c731ff16a702b0d1909eb2893f2cd8e26f1033`  
		Last Modified: Tue, 09 Feb 2021 23:18:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.4-alpine`

```console
$ docker pull influxdb@sha256:13c7180652607f6972bab9695bb186518837efb3ead92e183f78b080659d8a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.4-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:792d27b09aa77298b599bfa1e958d8a40d1724f60362f7fc88a2647377ee0ddf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68936049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0668c31135a00187a237367bc867cc53e322931d676c7b19480f21232c7d01`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:47:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 02 Feb 2021 22:20:33 GMT
ENV INFLUXDB_VERSION=1.8.4
# Tue, 02 Feb 2021 22:20:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 02 Feb 2021 22:20:41 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 02 Feb 2021 22:20:41 GMT
EXPOSE 8086
# Tue, 02 Feb 2021 22:20:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 02 Feb 2021 22:20:41 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 02 Feb 2021 22:20:42 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 02 Feb 2021 22:20:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Feb 2021 22:20:42 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1924738bc6407d8319fdb7d3fca610b5972213dee7ad608f4d801b3990f11a21`  
		Last Modified: Thu, 17 Dec 2020 13:49:35 GMT  
		Size: 1.4 MB (1428296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d068636b9da705cbc3a193a0e3e2e60e5aaec151bba413c1ee0df5a65ae7055`  
		Last Modified: Tue, 02 Feb 2021 22:22:00 GMT  
		Size: 64.7 MB (64706824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11962d347128e152320627d885cb1751aef15f8cdbb380973d87c6496b6fc04b`  
		Last Modified: Tue, 02 Feb 2021 22:21:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0fc61450eb47b0bffd007572441f8cab2747e92fc0d21a9ba86bc7eb7f0316`  
		Last Modified: Tue, 02 Feb 2021 22:21:50 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fefbbf2719bee48f7dab29ae4cc3eab0e7664b719d219b5ae426bae5fd21d01`  
		Last Modified: Tue, 02 Feb 2021 22:21:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-alpine`

```console
$ docker pull influxdb@sha256:13c7180652607f6972bab9695bb186518837efb3ead92e183f78b080659d8a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:792d27b09aa77298b599bfa1e958d8a40d1724f60362f7fc88a2647377ee0ddf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68936049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0668c31135a00187a237367bc867cc53e322931d676c7b19480f21232c7d01`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:47:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 02 Feb 2021 22:20:33 GMT
ENV INFLUXDB_VERSION=1.8.4
# Tue, 02 Feb 2021 22:20:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 02 Feb 2021 22:20:41 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 02 Feb 2021 22:20:41 GMT
EXPOSE 8086
# Tue, 02 Feb 2021 22:20:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 02 Feb 2021 22:20:41 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 02 Feb 2021 22:20:42 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 02 Feb 2021 22:20:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Feb 2021 22:20:42 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1924738bc6407d8319fdb7d3fca610b5972213dee7ad608f4d801b3990f11a21`  
		Last Modified: Thu, 17 Dec 2020 13:49:35 GMT  
		Size: 1.4 MB (1428296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d068636b9da705cbc3a193a0e3e2e60e5aaec151bba413c1ee0df5a65ae7055`  
		Last Modified: Tue, 02 Feb 2021 22:22:00 GMT  
		Size: 64.7 MB (64706824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11962d347128e152320627d885cb1751aef15f8cdbb380973d87c6496b6fc04b`  
		Last Modified: Tue, 02 Feb 2021 22:21:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0fc61450eb47b0bffd007572441f8cab2747e92fc0d21a9ba86bc7eb7f0316`  
		Last Modified: Tue, 02 Feb 2021 22:21:50 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fefbbf2719bee48f7dab29ae4cc3eab0e7664b719d219b5ae426bae5fd21d01`  
		Last Modified: Tue, 02 Feb 2021 22:21:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data`

```console
$ docker pull influxdb@sha256:67876cecbc722648d5eaf17c64854ae57beafca233a55416e95fc212de64bd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:9ad29edf6629eeeed7540d003ace92750e12e733055524dc08bc50c682eb8dec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126791523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1586215b740555a75748269f512871688d91312d26491ad08a114601e96719b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:57:02 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 10 Feb 2021 04:57:10 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Feb 2021 04:57:10 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 10 Feb 2021 04:57:10 GMT
EXPOSE 8086
# Wed, 10 Feb 2021 04:57:10 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:57:11 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:57:11 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Feb 2021 04:57:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:57:11 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d29e7e8838f6b925c171a67948b5f3bf44fca76a2428583987f3a7474f9e50`  
		Last Modified: Wed, 10 Feb 2021 04:59:10 GMT  
		Size: 65.8 MB (65796478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb80241906ed39ac62840cac80202f837585b84e0224d24571b11c957148879`  
		Last Modified: Wed, 10 Feb 2021 04:59:01 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d44b9df77d08197aca251c63136878d862be3c48adb4878bace9022c7761a3f`  
		Last Modified: Wed, 10 Feb 2021 04:59:01 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a88d904c7edfc7e2abba83d7274f2c25ff792d2688362e3f290b40a35b8f6da`  
		Last Modified: Wed, 10 Feb 2021 04:59:01 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data-alpine`

```console
$ docker pull influxdb@sha256:1f76bcc17b25bea15aa83eba37ae79913bb097973c16510c29426683554ffa78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ca8eb83702c42e6842af42682894c786ed7df4ccad01039da5e44b25987f621e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69770238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c93b32605cb2f94cf639d1f32c08a983526c4557abd14fe6292fc0d2fa3607`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:47:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 17 Dec 2020 13:48:32 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Thu, 17 Dec 2020 13:48:39 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:48:39 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 17 Dec 2020 13:48:39 GMT
EXPOSE 8086
# Thu, 17 Dec 2020 13:48:39 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 13:48:39 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 17 Dec 2020 13:48:40 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 17 Dec 2020 13:48:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:48:40 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1924738bc6407d8319fdb7d3fca610b5972213dee7ad608f4d801b3990f11a21`  
		Last Modified: Thu, 17 Dec 2020 13:49:35 GMT  
		Size: 1.4 MB (1428296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6edf7ef0639b641e2a6c111b20bb8d65c63a939fb49f70007b70b6a18cd225`  
		Last Modified: Thu, 17 Dec 2020 13:51:10 GMT  
		Size: 65.5 MB (65540953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976d9c1bb701d9b9686a9c72d1711cb0e6b27061b3f6950efbadbbab20dad7bf`  
		Last Modified: Thu, 17 Dec 2020 13:50:58 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d3881e28e4b6909bfc1fd929606827018b6dfb44e91a07edf855afb0f7e856`  
		Last Modified: Thu, 17 Dec 2020 13:50:58 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a300eda57a9818ae4a90aaf183c2476f4e828cbc9073271ec5bffdc644b6e7b2`  
		Last Modified: Thu, 17 Dec 2020 13:50:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-meta`

```console
$ docker pull influxdb@sha256:83e2e77f7ef83ceaa7549f44058d12f255301a99fe7ba6cc1a6f4d8a9fe0cb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:ffe8c67e7d6a188fe1378ca1541b43740e07f77497f65aacd47103897defe8ae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83859997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d706e62f1b535daeefd18b8bde7816e8310504c1c995ebc1701323883d94d74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:57:02 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 10 Feb 2021 04:57:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Feb 2021 04:57:24 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 10 Feb 2021 04:57:24 GMT
EXPOSE 8091
# Wed, 10 Feb 2021 04:57:24 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:57:24 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:57:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:57:25 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97ba6effd1841113e069182d033c17f3bdbbd57c3b3e9347abdc2bdecdde2ef`  
		Last Modified: Wed, 10 Feb 2021 04:59:23 GMT  
		Size: 22.9 MB (22866156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b75a883c5a79201ac582bb3980ed32e7f034f2f6ae3ec49667a25f4582463bf`  
		Last Modified: Wed, 10 Feb 2021 04:59:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ebe920089e36547964e057f165cf7102ff2925b478a707d02b94ebd670efe2`  
		Last Modified: Wed, 10 Feb 2021 04:59:17 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-meta-alpine`

```console
$ docker pull influxdb@sha256:4c29eac32909a131cfaff0592d154d70dd7dfe0478cb9540c2901ddf0da5fae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:dca974575db512c53831bde49ddf78ac0dcf4d82dc22079be452c62da4ba5682
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26963560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8881cbf80321dc2a4ebdf2195439034efa5d7c8d21b315de81395c705b9129c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:47:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 17 Dec 2020 13:48:32 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Thu, 17 Dec 2020 13:48:52 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:48:52 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 17 Dec 2020 13:48:53 GMT
EXPOSE 8091
# Thu, 17 Dec 2020 13:48:53 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 13:48:54 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 17 Dec 2020 13:48:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:48:54 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1924738bc6407d8319fdb7d3fca610b5972213dee7ad608f4d801b3990f11a21`  
		Last Modified: Thu, 17 Dec 2020 13:49:35 GMT  
		Size: 1.4 MB (1428296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160bf10769c16bdb7542730ceba295bdfb41ccdcc94aad7899def6ebc89b50f5`  
		Last Modified: Thu, 17 Dec 2020 13:51:26 GMT  
		Size: 22.7 MB (22735478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc8f9cb3bd7cd3e189107cbd62ad4c10e03619dda2334334e9472e68bed697b`  
		Last Modified: Thu, 17 Dec 2020 13:51:20 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74170b5ea5a39ad5a9878ee9a90ab8f39e7d7331d10ead82b0ed7f28cd4f007`  
		Last Modified: Thu, 17 Dec 2020 13:51:22 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0`

**does not exist** (yet?)

## `influxdb:2.0.4`

**does not exist** (yet?)

## `influxdb:2.0.4-alpine`

**does not exist** (yet?)

## `influxdb:2.0-alpine`

**does not exist** (yet?)

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:13c7180652607f6972bab9695bb186518837efb3ead92e183f78b080659d8a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:792d27b09aa77298b599bfa1e958d8a40d1724f60362f7fc88a2647377ee0ddf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68936049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0668c31135a00187a237367bc867cc53e322931d676c7b19480f21232c7d01`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:47:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 02 Feb 2021 22:20:33 GMT
ENV INFLUXDB_VERSION=1.8.4
# Tue, 02 Feb 2021 22:20:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 02 Feb 2021 22:20:41 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 02 Feb 2021 22:20:41 GMT
EXPOSE 8086
# Tue, 02 Feb 2021 22:20:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 02 Feb 2021 22:20:41 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 02 Feb 2021 22:20:42 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 02 Feb 2021 22:20:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Feb 2021 22:20:42 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1924738bc6407d8319fdb7d3fca610b5972213dee7ad608f4d801b3990f11a21`  
		Last Modified: Thu, 17 Dec 2020 13:49:35 GMT  
		Size: 1.4 MB (1428296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d068636b9da705cbc3a193a0e3e2e60e5aaec151bba413c1ee0df5a65ae7055`  
		Last Modified: Tue, 02 Feb 2021 22:22:00 GMT  
		Size: 64.7 MB (64706824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11962d347128e152320627d885cb1751aef15f8cdbb380973d87c6496b6fc04b`  
		Last Modified: Tue, 02 Feb 2021 22:21:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0fc61450eb47b0bffd007572441f8cab2747e92fc0d21a9ba86bc7eb7f0316`  
		Last Modified: Tue, 02 Feb 2021 22:21:50 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fefbbf2719bee48f7dab29ae4cc3eab0e7664b719d219b5ae426bae5fd21d01`  
		Last Modified: Tue, 02 Feb 2021 22:21:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data`

```console
$ docker pull influxdb@sha256:67876cecbc722648d5eaf17c64854ae57beafca233a55416e95fc212de64bd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:9ad29edf6629eeeed7540d003ace92750e12e733055524dc08bc50c682eb8dec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126791523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1586215b740555a75748269f512871688d91312d26491ad08a114601e96719b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:57:02 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 10 Feb 2021 04:57:10 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Feb 2021 04:57:10 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 10 Feb 2021 04:57:10 GMT
EXPOSE 8086
# Wed, 10 Feb 2021 04:57:10 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:57:11 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:57:11 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Feb 2021 04:57:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:57:11 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d29e7e8838f6b925c171a67948b5f3bf44fca76a2428583987f3a7474f9e50`  
		Last Modified: Wed, 10 Feb 2021 04:59:10 GMT  
		Size: 65.8 MB (65796478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb80241906ed39ac62840cac80202f837585b84e0224d24571b11c957148879`  
		Last Modified: Wed, 10 Feb 2021 04:59:01 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d44b9df77d08197aca251c63136878d862be3c48adb4878bace9022c7761a3f`  
		Last Modified: Wed, 10 Feb 2021 04:59:01 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a88d904c7edfc7e2abba83d7274f2c25ff792d2688362e3f290b40a35b8f6da`  
		Last Modified: Wed, 10 Feb 2021 04:59:01 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:1f76bcc17b25bea15aa83eba37ae79913bb097973c16510c29426683554ffa78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ca8eb83702c42e6842af42682894c786ed7df4ccad01039da5e44b25987f621e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69770238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c93b32605cb2f94cf639d1f32c08a983526c4557abd14fe6292fc0d2fa3607`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:47:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 17 Dec 2020 13:48:32 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Thu, 17 Dec 2020 13:48:39 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:48:39 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 17 Dec 2020 13:48:39 GMT
EXPOSE 8086
# Thu, 17 Dec 2020 13:48:39 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 13:48:39 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 17 Dec 2020 13:48:40 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 17 Dec 2020 13:48:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:48:40 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1924738bc6407d8319fdb7d3fca610b5972213dee7ad608f4d801b3990f11a21`  
		Last Modified: Thu, 17 Dec 2020 13:49:35 GMT  
		Size: 1.4 MB (1428296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6edf7ef0639b641e2a6c111b20bb8d65c63a939fb49f70007b70b6a18cd225`  
		Last Modified: Thu, 17 Dec 2020 13:51:10 GMT  
		Size: 65.5 MB (65540953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976d9c1bb701d9b9686a9c72d1711cb0e6b27061b3f6950efbadbbab20dad7bf`  
		Last Modified: Thu, 17 Dec 2020 13:50:58 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d3881e28e4b6909bfc1fd929606827018b6dfb44e91a07edf855afb0f7e856`  
		Last Modified: Thu, 17 Dec 2020 13:50:58 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a300eda57a9818ae4a90aaf183c2476f4e828cbc9073271ec5bffdc644b6e7b2`  
		Last Modified: Thu, 17 Dec 2020 13:50:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:a66fa6bd81bee3c70e6c408235af068422ab73d74aa5d6acfc09dc76eba0ebf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:7539edbf76df0498f730904827f859aa4c67e1386cb72601019d72ec3e12ed0c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125961499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7870fcea362222d648815a18c6d949e3faae225b97b8c0ee7cc27b74e9d8c45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:56:44 GMT
ENV INFLUXDB_VERSION=1.8.4
# Wed, 10 Feb 2021 04:56:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 10 Feb 2021 04:56:52 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 10 Feb 2021 04:56:52 GMT
EXPOSE 8086
# Wed, 10 Feb 2021 04:56:52 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:56:52 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:56:52 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Feb 2021 04:56:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:56:53 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0907122426ac6b2c48c0e3da39e10da254ba8f0e10be1600731b210881c4ef`  
		Last Modified: Wed, 10 Feb 2021 04:58:50 GMT  
		Size: 65.0 MB (64966512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d3d7e535c1e62ce9dfa85b05ccb228f0cbf722440cb8958e74580f3de94dd3`  
		Last Modified: Wed, 10 Feb 2021 04:58:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45b611f60bfbba58da3ec97f086ba4c4dfeb487aef823873770166635986f00`  
		Last Modified: Wed, 10 Feb 2021 04:58:40 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7c9bc15cec46afb70a351b3614181ae2cab6e938d478f34bfbfe2cdda2dcd1`  
		Last Modified: Wed, 10 Feb 2021 04:58:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:5860a6f7fce49f8a6d7abb08246752f8f0b000a1b732817e9dc09ad998dfb521
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117019220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b981467ac4ae2e2898af181253117226acacf5235d51bbd0942434847568d9d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 03:04:53 GMT
ADD file:f884b9fc23d1b8ad0bd21aa823afd0ee186bdebb6829ccba72f77caaeffd8d12 in / 
# Tue, 09 Feb 2021 03:04:55 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:32:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:32:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 19:58:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 19:58:30 GMT
ENV INFLUXDB_VERSION=1.8.4
# Tue, 09 Feb 2021 19:58:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 09 Feb 2021 19:58:42 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 09 Feb 2021 19:58:42 GMT
EXPOSE 8086
# Tue, 09 Feb 2021 19:58:43 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Feb 2021 19:58:44 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 09 Feb 2021 19:58:45 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 09 Feb 2021 19:58:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 19:58:47 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:5275c778c803ce7d82407c77cfad4fb07fd1ec80fc99ba94cef475a92e4d090c`  
		Last Modified: Tue, 09 Feb 2021 03:13:25 GMT  
		Size: 42.1 MB (42119892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae60b5ed65c5d76acc7c0baf6fe0549a03f324c20d1882c25d60b44aaacaeba`  
		Last Modified: Tue, 09 Feb 2021 04:42:37 GMT  
		Size: 9.9 MB (9913736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99de29c3c448a06c87fa2f84824e9e1d0e9a9c7d7aebb93fce0ca22b55b6c9b`  
		Last Modified: Tue, 09 Feb 2021 04:42:35 GMT  
		Size: 3.9 MB (3921069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266519cf240cda7cb2dcf0551d5435701ea108d2186948c68c5731ad4de7ce03`  
		Last Modified: Tue, 09 Feb 2021 19:59:00 GMT  
		Size: 2.9 KB (2857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566dbce2ab0602ce6e21d013e2ef27c24203069bc940c37f70bd22415997cc60`  
		Last Modified: Tue, 09 Feb 2021 19:59:40 GMT  
		Size: 61.1 MB (61059949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0ef9b950cdaed2cc4f6dfb3d0928afded1350969752156ea669344206594b7`  
		Last Modified: Tue, 09 Feb 2021 19:59:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b8013e08b555d7e35d41afb6ce6592ca229da53f7907cc90145c4a2f29113f`  
		Last Modified: Tue, 09 Feb 2021 19:59:23 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206c65c8a4e22d8f7f0dcc8a4cb52960651dcd3267a8301efc9a9b1c77766474`  
		Last Modified: Tue, 09 Feb 2021 19:59:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:cecdf09bdae2736f4cfeea2157e2e04baf728ae09a2d087bdd8081dfdc387277
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118090458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9473609f3c55065609f52855ca8def2f9a505f5876b1f1eedc16049206fd35c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:43:17 GMT
ADD file:fb69ff7b2a28f793efbd16e04b74ffb4557d39e1844b3789075b4d3ff97a0eaa in / 
# Tue, 09 Feb 2021 02:43:20 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:50:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 23:17:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 23:17:49 GMT
ENV INFLUXDB_VERSION=1.8.4
# Tue, 09 Feb 2021 23:17:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 09 Feb 2021 23:18:00 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 09 Feb 2021 23:18:00 GMT
EXPOSE 8086
# Tue, 09 Feb 2021 23:18:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Feb 2021 23:18:02 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 09 Feb 2021 23:18:03 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 09 Feb 2021 23:18:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 23:18:04 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:296c9f0bf5f2cf24e87bc5abd674fc486e8df419d4aa2d362453f64d38900504`  
		Last Modified: Tue, 09 Feb 2021 02:49:43 GMT  
		Size: 43.2 MB (43177550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d546321c8e11789c75187b5b592633207519d75f96e8f03e8378d2da4a72a9`  
		Last Modified: Tue, 09 Feb 2021 05:00:16 GMT  
		Size: 10.2 MB (10182589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91c8ffe219846d18819503633eb252121c21cd20dbff74278b85c4029370992`  
		Last Modified: Tue, 09 Feb 2021 05:00:15 GMT  
		Size: 4.1 MB (4096615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc3bb22e13ab89a21825455644f82709870c5ca9d0f5dcc186f2794e987fbb0`  
		Last Modified: Tue, 09 Feb 2021 23:18:20 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b55933c9b8cf91ab120a56ebee961c795c2f781c696d2ce72ce6ffd35190d7`  
		Last Modified: Tue, 09 Feb 2021 23:18:53 GMT  
		Size: 60.6 MB (60629135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739b5dbd7dbd5e775bb785f8311d2446b7da2b091ffcf6388f0649af38d4413e`  
		Last Modified: Tue, 09 Feb 2021 23:18:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0f5eef745245986f16357dd49791608ad6e8b60307d32bfbe1412b22d8c298`  
		Last Modified: Tue, 09 Feb 2021 23:18:41 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556a000a3eaa8c4c8c0043bfc2c731ff16a702b0d1909eb2893f2cd8e26f1033`  
		Last Modified: Tue, 09 Feb 2021 23:18:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:83e2e77f7ef83ceaa7549f44058d12f255301a99fe7ba6cc1a6f4d8a9fe0cb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:ffe8c67e7d6a188fe1378ca1541b43740e07f77497f65aacd47103897defe8ae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83859997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d706e62f1b535daeefd18b8bde7816e8310504c1c995ebc1701323883d94d74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:57:02 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 10 Feb 2021 04:57:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Feb 2021 04:57:24 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 10 Feb 2021 04:57:24 GMT
EXPOSE 8091
# Wed, 10 Feb 2021 04:57:24 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:57:24 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:57:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:57:25 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97ba6effd1841113e069182d033c17f3bdbbd57c3b3e9347abdc2bdecdde2ef`  
		Last Modified: Wed, 10 Feb 2021 04:59:23 GMT  
		Size: 22.9 MB (22866156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b75a883c5a79201ac582bb3980ed32e7f034f2f6ae3ec49667a25f4582463bf`  
		Last Modified: Wed, 10 Feb 2021 04:59:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ebe920089e36547964e057f165cf7102ff2925b478a707d02b94ebd670efe2`  
		Last Modified: Wed, 10 Feb 2021 04:59:17 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta-alpine`

```console
$ docker pull influxdb@sha256:4c29eac32909a131cfaff0592d154d70dd7dfe0478cb9540c2901ddf0da5fae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:dca974575db512c53831bde49ddf78ac0dcf4d82dc22079be452c62da4ba5682
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26963560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8881cbf80321dc2a4ebdf2195439034efa5d7c8d21b315de81395c705b9129c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:47:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 17 Dec 2020 13:48:32 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Thu, 17 Dec 2020 13:48:52 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:48:52 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 17 Dec 2020 13:48:53 GMT
EXPOSE 8091
# Thu, 17 Dec 2020 13:48:53 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 13:48:54 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 17 Dec 2020 13:48:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:48:54 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1924738bc6407d8319fdb7d3fca610b5972213dee7ad608f4d801b3990f11a21`  
		Last Modified: Thu, 17 Dec 2020 13:49:35 GMT  
		Size: 1.4 MB (1428296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160bf10769c16bdb7542730ceba295bdfb41ccdcc94aad7899def6ebc89b50f5`  
		Last Modified: Thu, 17 Dec 2020 13:51:26 GMT  
		Size: 22.7 MB (22735478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc8f9cb3bd7cd3e189107cbd62ad4c10e03619dda2334334e9472e68bed697b`  
		Last Modified: Thu, 17 Dec 2020 13:51:20 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74170b5ea5a39ad5a9878ee9a90ab8f39e7d7331d10ead82b0ed7f28cd4f007`  
		Last Modified: Thu, 17 Dec 2020 13:51:22 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
