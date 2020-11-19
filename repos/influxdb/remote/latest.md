## `influxdb:latest`

```console
$ docker pull influxdb@sha256:aa5efc36964e969137b47805de0fb3367d83e865ec945f38db729926d4a032ac
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
$ docker pull influxdb@sha256:25db15f7348152a0ee794919d968b5cecff9e6e2657921be1f8cdd3ab44acfe4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116543722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ec268c9cb24ad1be71f7fd322be8d33b45160ca2a2fcba9cb4096e459a6df5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 17 Nov 2020 20:26:47 GMT
ADD file:58b80132bbfb3cae1eb2a9345e362cce1e39de41055fdcef8e5a8a8a447f69b0 in / 
# Tue, 17 Nov 2020 20:26:50 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:57:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:57:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 19:30:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 18 Nov 2020 19:30:27 GMT
ENV INFLUXDB_VERSION=1.8.3
# Wed, 18 Nov 2020 19:30:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 18 Nov 2020 19:30:39 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 18 Nov 2020 19:30:39 GMT
EXPOSE 8086
# Wed, 18 Nov 2020 19:30:40 GMT
VOLUME [/var/lib/influxdb]
# Wed, 18 Nov 2020 19:30:41 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 18 Nov 2020 19:30:41 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 18 Nov 2020 19:30:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 19:30:43 GMT
CMD ["influxd"]
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
	-	`sha256:b4f5e414393e51355639c15a6f3e41920c8ec8edba69cfe3e88c9c986ddd17a4`  
		Last Modified: Wed, 18 Nov 2020 19:30:55 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb9a9ae2496590eb3d99afa0d6940bcc5c6e16a1d0e1da61d92faaa02e232be`  
		Last Modified: Wed, 18 Nov 2020 19:31:38 GMT  
		Size: 61.1 MB (61057408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f273235f4072dc391720ac2d5466a51c7b4899ebcbfd6dc316d003df7b95299`  
		Last Modified: Wed, 18 Nov 2020 19:31:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abad5bfa45862cee555e75998d656e6811c59401715bc83639bc13047f70a74a`  
		Last Modified: Wed, 18 Nov 2020 19:31:22 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0576d8f08f2939eb2bbc88db9c2552d4c2b32e31c529fba34de4ea28549d5a44`  
		Last Modified: Wed, 18 Nov 2020 19:31:22 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1b79e9e126b04b77248ff3d75864f244f179d4f89aef98735cc5820c9747392a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117604873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35b5ae257740aa1ef90d566a2e18e6e4f8435affbee7a77d2afc6e50c844a5b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 17 Nov 2020 20:27:33 GMT
ADD file:d2e307c3e54ad69dff47f6bdacca7c8ee0957a09346bb21baec02b9de1a657e1 in / 
# Tue, 17 Nov 2020 20:27:37 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:28:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:28:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 21:12:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 18 Nov 2020 21:13:12 GMT
ENV INFLUXDB_VERSION=1.8.3
# Wed, 18 Nov 2020 21:13:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 18 Nov 2020 21:13:22 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 18 Nov 2020 21:13:23 GMT
EXPOSE 8086
# Wed, 18 Nov 2020 21:13:23 GMT
VOLUME [/var/lib/influxdb]
# Wed, 18 Nov 2020 21:13:24 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 18 Nov 2020 21:13:25 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 18 Nov 2020 21:13:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 21:13:27 GMT
CMD ["influxd"]
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
	-	`sha256:6def7eeebead44e667219a52a3592b983ffa390c1b722142f59c7070419c2b01`  
		Last Modified: Wed, 18 Nov 2020 21:13:38 GMT  
		Size: 2.9 KB (2857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4552a0ba56ac8f1ec8c76995cc57036c44f415ccbd855ac50af51c07f5bc20`  
		Last Modified: Wed, 18 Nov 2020 21:14:15 GMT  
		Size: 60.6 MB (60626780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a775c7ae5fece33c2dde603a585380c22429ac8ee3307a36ce0f7ed71486d6b1`  
		Last Modified: Wed, 18 Nov 2020 21:14:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459bfe537307844ae7866ca3238c9fb2e733f74a801841916d22aef7292bf1a6`  
		Last Modified: Wed, 18 Nov 2020 21:14:00 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf588d096b6e9fb70785cc94e4904fe5f0d972a05c9c1af60f559fd0df6d3a80`  
		Last Modified: Wed, 18 Nov 2020 21:14:01 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
