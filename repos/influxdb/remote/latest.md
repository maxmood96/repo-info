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
