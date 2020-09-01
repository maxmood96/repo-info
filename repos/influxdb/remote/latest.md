## `influxdb:latest`

```console
$ docker pull influxdb@sha256:d24c67b18405bb1a2140ce0b1f7580e09e2abad7b5082e32793e704465c65008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:26d02cd507c2212602e1ca413d2bd444d0321229eb949043eea34a1b4fec1451
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124467369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdff4cd48c12f472840e9f1eea87a56368ce316bff4cfef2a2ea9ca801a2049`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:32 GMT
ADD file:a28d8a949b7577768d87fcbac346797fc5f7bad0539625339edcd09a32d6bf77 in / 
# Tue, 04 Aug 2020 15:45:33 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:35:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:36:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 16:33:30 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 01 Sep 2020 00:59:16 GMT
ENV INFLUXDB_VERSION=1.8.2
# Tue, 01 Sep 2020 00:59:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 01 Sep 2020 00:59:26 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 01 Sep 2020 00:59:27 GMT
EXPOSE 8086
# Tue, 01 Sep 2020 00:59:27 GMT
VOLUME [/var/lib/influxdb]
# Tue, 01 Sep 2020 00:59:28 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 01 Sep 2020 00:59:28 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 01 Sep 2020 00:59:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Sep 2020 00:59:29 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:419e7ae5bb1e4875c367f3249b7bb7f8f39dd27dfceb4ee9d6a92191ed1c452f`  
		Last Modified: Tue, 04 Aug 2020 15:52:05 GMT  
		Size: 45.4 MB (45366706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848839e0cd3b3acc96db8a39c4520a40f98dc8f3a2a5f80b575ff4a1c88f1fcf`  
		Last Modified: Tue, 04 Aug 2020 23:42:18 GMT  
		Size: 10.8 MB (10750599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de30e8b35015c7302e071e9c2b449290f270feaf2a419f6466a555b6907e7d72`  
		Last Modified: Tue, 04 Aug 2020 23:42:17 GMT  
		Size: 4.3 MB (4339945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a43b78da5c81aca131b2d8a546d90ced7de3336296ea931086cbafe0a5b68f`  
		Last Modified: Wed, 05 Aug 2020 16:35:07 GMT  
		Size: 2.8 KB (2775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30fe5d6fdfc76c989ca7a23599b0f5b9c9e69891b1d072d1cd7391b4772bad5f`  
		Last Modified: Tue, 01 Sep 2020 01:02:35 GMT  
		Size: 64.0 MB (64005626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97dac6cf5f7a17f1fba0f66705b8e6f1c4038ce30c89273615594310060f21f`  
		Last Modified: Tue, 01 Sep 2020 01:02:21 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7acdd2f10d3633290f720f90c5ebbab643eb19b9cc0f192384f18aebced3e90`  
		Last Modified: Tue, 01 Sep 2020 01:02:22 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c94f5695a157485e86be74d38c10ac9f246d7faab35b35e1fbdf81e388c92`  
		Last Modified: Tue, 01 Sep 2020 01:02:21 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:1157bb2a790ce31f68b5deb6d44691e96136e776f0ef824a4de4dab44fca27a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115669457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca48fe485f8800ea48b91952a2df8be1abc61036733452d23f271fb38c3e87a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:04 GMT
ADD file:0ba6f3203fb10e66124d03088d234e92fc908c572ec7eed268e866623a383a7d in / 
# Tue, 04 Aug 2020 05:01:07 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:16:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:16:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 04:21:30 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 04:21:56 GMT
ENV INFLUXDB_VERSION=1.8.1
# Wed, 05 Aug 2020 04:22:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 05 Aug 2020 04:22:12 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 05 Aug 2020 04:22:13 GMT
EXPOSE 8086
# Wed, 05 Aug 2020 04:22:14 GMT
VOLUME [/var/lib/influxdb]
# Wed, 05 Aug 2020 04:22:16 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 05 Aug 2020 04:22:17 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 05 Aug 2020 04:22:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 04:22:20 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:323178d00ec2c5eb5ffb9cb696a52eaf8683dcf2eb605c742da2953556f06e37`  
		Last Modified: Tue, 04 Aug 2020 05:08:40 GMT  
		Size: 42.1 MB (42111382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b4e15a79453f6ae10815d79c8f4590aef2f1ac2979c192ff7f1ed0fbf04e60`  
		Last Modified: Tue, 04 Aug 2020 08:30:43 GMT  
		Size: 9.4 MB (9443881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf9cb1ef704caf3af8a2ed43dc12884b4f74ac867ce95f60bd8996f51fde770`  
		Last Modified: Tue, 04 Aug 2020 08:30:41 GMT  
		Size: 3.9 MB (3918490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ad1ae0455f086a984fe5ca80430d33819b38c31587c5972ddc6aedd904cbf6`  
		Last Modified: Wed, 05 Aug 2020 04:22:33 GMT  
		Size: 2.8 KB (2806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc479edc9f408861f73f237123015da94c716f59ab416a62078fc7ab0ac3971`  
		Last Modified: Wed, 05 Aug 2020 04:23:13 GMT  
		Size: 60.2 MB (60191181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacd186a6889b8c5e41c0b0208a92d0f55f6401cb522fa7e71e55dc922b234cf`  
		Last Modified: Wed, 05 Aug 2020 04:22:56 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1fdc63038b078c5450481ae63880edfcde3b6a5ea42ca5896bc6e7e37f93e0`  
		Last Modified: Wed, 05 Aug 2020 04:22:57 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d22af3197898ed08422e5d4a2d9fa52b2e82343f2e13168a54d610e949a020`  
		Last Modified: Wed, 05 Aug 2020 04:22:57 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:292af04787cffff028d2d41e5c4ea5b227acbc62eb2bb67c9ffb673e5b177d93
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116751836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad3f87612d7990058390dc9fb5bdc782051f6753ab23be256b977b8623a1744`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 04 Aug 2020 06:59:38 GMT
ADD file:0a7a65de4c9dc6ea7f7ac97362a47b82a02a45ecab668ddc84cfd011dad26d33 in / 
# Tue, 04 Aug 2020 06:59:41 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:16:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:16:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 07:16:40 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 07:17:08 GMT
ENV INFLUXDB_VERSION=1.8.1
# Wed, 05 Aug 2020 07:17:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 05 Aug 2020 07:17:18 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 05 Aug 2020 07:17:18 GMT
EXPOSE 8086
# Wed, 05 Aug 2020 07:17:19 GMT
VOLUME [/var/lib/influxdb]
# Wed, 05 Aug 2020 07:17:20 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 05 Aug 2020 07:17:21 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 05 Aug 2020 07:17:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 07:17:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:708f9b01fc1a5dff70f7d40443ac7dd0ee1d0ae93202b6f305f4e3627cea7d22`  
		Last Modified: Tue, 04 Aug 2020 07:06:12 GMT  
		Size: 43.2 MB (43171643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dc3a0299d558e9f611edd56658d792af018276662c8c30d86476a05c18b00b`  
		Last Modified: Tue, 04 Aug 2020 11:26:22 GMT  
		Size: 9.7 MB (9700890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feaa2634e51f929e9ca86765cd5579cdf0809084c80d6787166627ca2aed6d4`  
		Last Modified: Tue, 04 Aug 2020 11:26:21 GMT  
		Size: 4.1 MB (4094122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691da85e3888bd2ba9b2a633be8705530081b5fde5f1bfe36535d5a56097f227`  
		Last Modified: Wed, 05 Aug 2020 07:17:36 GMT  
		Size: 2.8 KB (2803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7bd8e8c27c2ddfda4ef8731d73cf066d46aa4ff09a84d9595e4630850d8ca6b`  
		Last Modified: Wed, 05 Aug 2020 07:18:19 GMT  
		Size: 59.8 MB (59780661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb50e8c44feda4b5bcf1773af525f934697314bcc69ba061deffe2fc21efab27`  
		Last Modified: Wed, 05 Aug 2020 07:18:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455d8f53b784a5b76145dd669e1620768099f571ce1a57a248eb1e076eccd9e6`  
		Last Modified: Wed, 05 Aug 2020 07:18:04 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9056c827c399a558a1a6ea15ef45a5bcee6046d6bbdb2e5538772e7e04d69126`  
		Last Modified: Wed, 05 Aug 2020 07:18:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
