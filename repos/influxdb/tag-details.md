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
$ docker pull influxdb@sha256:f35d345ccdea84215232e22ddac3ac500688b6c540f46ddd6209e08a04f26620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7` - linux; amd64

```console
$ docker pull influxdb@sha256:5b8ab9b7cb0aa131e826073d7d17059386ad2c270f5a7d4dd832ddfac1e5d719
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124571300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf2505d0343fbb0cfd248cb135bfc1a1b24581b0826cf867c40a9a6fcb91e31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:10 GMT
ADD file:373a8875589f170b51fa677a3bf736feeb46ea278c553950a3eb3169a2056c12 in / 
# Tue, 17 Nov 2020 20:24:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:43:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:43:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 02:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 19 Nov 2020 02:59:28 GMT
ENV INFLUXDB_VERSION=1.7.10
# Thu, 19 Nov 2020 02:59:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 19 Nov 2020 02:59:39 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 19 Nov 2020 02:59:39 GMT
EXPOSE 8086
# Thu, 19 Nov 2020 02:59:40 GMT
VOLUME [/var/lib/influxdb]
# Thu, 19 Nov 2020 02:59:40 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 19 Nov 2020 02:59:40 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 19 Nov 2020 02:59:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 02:59:40 GMT
CMD ["influxd"]
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
	-	`sha256:104e29a2e6403a35ba184667f594419af565fadd04a8ea0b1299d126d395b111`  
		Last Modified: Thu, 19 Nov 2020 03:01:18 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0386170a195b354070e7fd426d6530c549c960ae5d4f28f275f6300984a3ea8`  
		Last Modified: Thu, 19 Nov 2020 03:01:28 GMT  
		Size: 64.1 MB (64096980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada8ea16738b1d9b2ecc7651c3eacea31721a3741626b814632953e88bf6c338`  
		Last Modified: Thu, 19 Nov 2020 03:01:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8dfbf0096569a6bc6a7a62dbffa0fcfb781774a9839d2c0f84b7940e9777ea`  
		Last Modified: Thu, 19 Nov 2020 03:01:17 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a006d2129e7671d18675054174044717f1b83aefbecbc5c24ecedc4961b6e690`  
		Last Modified: Thu, 19 Nov 2020 03:01:18 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:466a32c5fcaa36303ff1f63f43e747d9180ded9c79d0f9a768556b50623b38a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116121877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940e94973a31c67675c4a4af4f17710f2e688cc670e9898d3eaa9eef1f70c523`
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
# Wed, 18 Nov 2020 19:30:03 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 18 Nov 2020 19:30:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 18 Nov 2020 19:30:14 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 18 Nov 2020 19:30:14 GMT
EXPOSE 8086
# Wed, 18 Nov 2020 19:30:15 GMT
VOLUME [/var/lib/influxdb]
# Wed, 18 Nov 2020 19:30:16 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 18 Nov 2020 19:30:17 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 18 Nov 2020 19:30:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 19:30:18 GMT
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
	-	`sha256:36f4d81a504c60d8daf9a3bffb83ad231cda47a9d38db5891eff058bd4aedf14`  
		Last Modified: Wed, 18 Nov 2020 19:31:12 GMT  
		Size: 60.6 MB (60635563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a52f5631b90b510c8075b491db45bf9ddaa00aa19240b3e161d5c3260c203f`  
		Last Modified: Wed, 18 Nov 2020 19:30:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ee91909a120aa1ff1e814b6875c379d4a28af504afa1daf364e938df8ea1b0`  
		Last Modified: Wed, 18 Nov 2020 19:30:55 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90151c1f615a16d78e6237a355252bbf9c8ab1e020209ca9194c506387510044`  
		Last Modified: Wed, 18 Nov 2020 19:30:55 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:fd68a164fa63fb3f632d2e2786bd39d50811d717b1db9a0a4c8bec56011fe871
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117105848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a80035ada00b28cde9dda78c593bb409d437e88864e3b7a2f7438229d30e46`
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
# Wed, 18 Nov 2020 21:12:47 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 18 Nov 2020 21:12:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 18 Nov 2020 21:12:58 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 18 Nov 2020 21:13:00 GMT
EXPOSE 8086
# Wed, 18 Nov 2020 21:13:01 GMT
VOLUME [/var/lib/influxdb]
# Wed, 18 Nov 2020 21:13:02 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 18 Nov 2020 21:13:03 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 18 Nov 2020 21:13:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 21:13:05 GMT
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
	-	`sha256:747442b5c738bfc135ae0b298da561c90607cb72c9eb71e9b4d14f1eafb55818`  
		Last Modified: Wed, 18 Nov 2020 21:13:52 GMT  
		Size: 60.1 MB (60127759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40588d61328fb059d5c5314f091da5bfce49923a164b0968cdf2caa28df7e18d`  
		Last Modified: Wed, 18 Nov 2020 21:13:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44aab9f1861f0ce828cdfaa625ccd33a21d58644cbd9aa3f8b5c842b8537a471`  
		Last Modified: Wed, 18 Nov 2020 21:13:37 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1707a9c46fcd0986bf0efd0923e09a5a2ea322a3936981a33f636f8d365540`  
		Last Modified: Wed, 18 Nov 2020 21:13:38 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10`

```console
$ docker pull influxdb@sha256:f35d345ccdea84215232e22ddac3ac500688b6c540f46ddd6209e08a04f26620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7.10` - linux; amd64

```console
$ docker pull influxdb@sha256:5b8ab9b7cb0aa131e826073d7d17059386ad2c270f5a7d4dd832ddfac1e5d719
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124571300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf2505d0343fbb0cfd248cb135bfc1a1b24581b0826cf867c40a9a6fcb91e31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:10 GMT
ADD file:373a8875589f170b51fa677a3bf736feeb46ea278c553950a3eb3169a2056c12 in / 
# Tue, 17 Nov 2020 20:24:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:43:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:43:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 02:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 19 Nov 2020 02:59:28 GMT
ENV INFLUXDB_VERSION=1.7.10
# Thu, 19 Nov 2020 02:59:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 19 Nov 2020 02:59:39 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 19 Nov 2020 02:59:39 GMT
EXPOSE 8086
# Thu, 19 Nov 2020 02:59:40 GMT
VOLUME [/var/lib/influxdb]
# Thu, 19 Nov 2020 02:59:40 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 19 Nov 2020 02:59:40 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 19 Nov 2020 02:59:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 02:59:40 GMT
CMD ["influxd"]
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
	-	`sha256:104e29a2e6403a35ba184667f594419af565fadd04a8ea0b1299d126d395b111`  
		Last Modified: Thu, 19 Nov 2020 03:01:18 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0386170a195b354070e7fd426d6530c549c960ae5d4f28f275f6300984a3ea8`  
		Last Modified: Thu, 19 Nov 2020 03:01:28 GMT  
		Size: 64.1 MB (64096980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada8ea16738b1d9b2ecc7651c3eacea31721a3741626b814632953e88bf6c338`  
		Last Modified: Thu, 19 Nov 2020 03:01:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8dfbf0096569a6bc6a7a62dbffa0fcfb781774a9839d2c0f84b7940e9777ea`  
		Last Modified: Thu, 19 Nov 2020 03:01:17 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a006d2129e7671d18675054174044717f1b83aefbecbc5c24ecedc4961b6e690`  
		Last Modified: Thu, 19 Nov 2020 03:01:18 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:466a32c5fcaa36303ff1f63f43e747d9180ded9c79d0f9a768556b50623b38a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116121877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940e94973a31c67675c4a4af4f17710f2e688cc670e9898d3eaa9eef1f70c523`
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
# Wed, 18 Nov 2020 19:30:03 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 18 Nov 2020 19:30:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 18 Nov 2020 19:30:14 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 18 Nov 2020 19:30:14 GMT
EXPOSE 8086
# Wed, 18 Nov 2020 19:30:15 GMT
VOLUME [/var/lib/influxdb]
# Wed, 18 Nov 2020 19:30:16 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 18 Nov 2020 19:30:17 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 18 Nov 2020 19:30:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 19:30:18 GMT
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
	-	`sha256:36f4d81a504c60d8daf9a3bffb83ad231cda47a9d38db5891eff058bd4aedf14`  
		Last Modified: Wed, 18 Nov 2020 19:31:12 GMT  
		Size: 60.6 MB (60635563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a52f5631b90b510c8075b491db45bf9ddaa00aa19240b3e161d5c3260c203f`  
		Last Modified: Wed, 18 Nov 2020 19:30:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ee91909a120aa1ff1e814b6875c379d4a28af504afa1daf364e938df8ea1b0`  
		Last Modified: Wed, 18 Nov 2020 19:30:55 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90151c1f615a16d78e6237a355252bbf9c8ab1e020209ca9194c506387510044`  
		Last Modified: Wed, 18 Nov 2020 19:30:55 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:fd68a164fa63fb3f632d2e2786bd39d50811d717b1db9a0a4c8bec56011fe871
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117105848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a80035ada00b28cde9dda78c593bb409d437e88864e3b7a2f7438229d30e46`
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
# Wed, 18 Nov 2020 21:12:47 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 18 Nov 2020 21:12:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 18 Nov 2020 21:12:58 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 18 Nov 2020 21:13:00 GMT
EXPOSE 8086
# Wed, 18 Nov 2020 21:13:01 GMT
VOLUME [/var/lib/influxdb]
# Wed, 18 Nov 2020 21:13:02 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 18 Nov 2020 21:13:03 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 18 Nov 2020 21:13:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 21:13:05 GMT
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
	-	`sha256:747442b5c738bfc135ae0b298da561c90607cb72c9eb71e9b4d14f1eafb55818`  
		Last Modified: Wed, 18 Nov 2020 21:13:52 GMT  
		Size: 60.1 MB (60127759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40588d61328fb059d5c5314f091da5bfce49923a164b0968cdf2caa28df7e18d`  
		Last Modified: Wed, 18 Nov 2020 21:13:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44aab9f1861f0ce828cdfaa625ccd33a21d58644cbd9aa3f8b5c842b8537a471`  
		Last Modified: Wed, 18 Nov 2020 21:13:37 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1707a9c46fcd0986bf0efd0923e09a5a2ea322a3936981a33f636f8d365540`  
		Last Modified: Wed, 18 Nov 2020 21:13:38 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-alpine`

```console
$ docker pull influxdb@sha256:55fd282870f2328c36879bdd84e3c3acf5439bdb5da692f673b065189cb6812a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:027917368a08f344869aa03a3efa3b72931a6c508fa1b102fec66d5cadb59251
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68068086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd0b0ff56b8047923d4eea96b82884b005dd34e779b29e164adb462cfb2da72`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:57:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 11 Dec 2020 05:57:55 GMT
ENV INFLUXDB_VERSION=1.7.10
# Fri, 11 Dec 2020 05:58:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 05:58:04 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 11 Dec 2020 05:58:04 GMT
EXPOSE 8086
# Fri, 11 Dec 2020 05:58:04 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Dec 2020 05:58:04 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 11 Dec 2020 05:58:05 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 11 Dec 2020 05:58:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 05:58:05 GMT
CMD ["influxd"]
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
	-	`sha256:16278230bdd89f4300bb64c70f52ab02811e9fb441099f76f89267ba46b906cd`  
		Last Modified: Fri, 11 Dec 2020 06:00:06 GMT  
		Size: 1.4 MB (1428310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638b592207e1dca830b35b87ba613acf664e2fbf62e47e19e035481c536edfa1`  
		Last Modified: Fri, 11 Dec 2020 06:00:17 GMT  
		Size: 63.8 MB (63840964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee90a787efdf1302369562e69db0882071fbab5c50db189515fc06d9a07e5be`  
		Last Modified: Fri, 11 Dec 2020 06:00:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7c80cec09dff80fabc858c474147061e9319df08e33bbf64b4ccc08b1d4268`  
		Last Modified: Fri, 11 Dec 2020 06:00:05 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850f3e0ad4af984d6e0ff11d164a6a076c1b7c551811ab15efa31f6c3be7b543`  
		Last Modified: Fri, 11 Dec 2020 06:00:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-data`

```console
$ docker pull influxdb@sha256:0a5743b3137d76328af96c9dee9eae99c469d1a23123d8e09755fbe88829ee99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:9238e40199831fe25dce3279c159c4f94ccd1e213bd2138978efa82f884cdf41
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148386724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9395b9073179eeea4cb24d689c1ef8622186934f02be21cd50e8a05a794e63fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:10 GMT
ADD file:373a8875589f170b51fa677a3bf736feeb46ea278c553950a3eb3169a2056c12 in / 
# Tue, 17 Nov 2020 20:24:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:43:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:43:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 02:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 19 Nov 2020 02:59:50 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Thu, 19 Nov 2020 02:59:56 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Thu, 19 Nov 2020 02:59:57 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 19 Nov 2020 02:59:57 GMT
EXPOSE 8086
# Thu, 19 Nov 2020 02:59:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 19 Nov 2020 02:59:57 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 19 Nov 2020 02:59:58 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 19 Nov 2020 02:59:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 02:59:58 GMT
CMD ["influxd"]
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
	-	`sha256:104e29a2e6403a35ba184667f594419af565fadd04a8ea0b1299d126d395b111`  
		Last Modified: Thu, 19 Nov 2020 03:01:18 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80168f8bff05fa954ee6359e21939edcb441e54d846817fa8978e8aa4564ff7c`  
		Last Modified: Thu, 19 Nov 2020 03:01:48 GMT  
		Size: 87.9 MB (87912342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7a7c4b6a9c05c38450f7539856e5094eb52a36998c41f25945797bb6bc8873`  
		Last Modified: Thu, 19 Nov 2020 03:01:34 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1c2a38ede310fc41026b1a52b3d15a0441bf1ea01212fbc66f6d8a9f18ba6a`  
		Last Modified: Thu, 19 Nov 2020 03:01:34 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97830fd85ffa96d2a831c1861f7b2f47020dda0ecd60fb34b13988040678b8c`  
		Last Modified: Thu, 19 Nov 2020 03:01:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-data-alpine`

```console
$ docker pull influxdb@sha256:b19a2178bf2a877b3a87d2a9fc2fcbbda760bf00bf64201efb53ebe0a3f693ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a87899b74a7728f4d8b0f0287d14206a809bbf5b5cedc6adf319790e26b70c4d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91830922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c44edb6b2bb4e741708fb143b0fa176001d06d51e3f4807cb912aca45674ae4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:57:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 11 Dec 2020 05:58:14 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Fri, 11 Dec 2020 05:58:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 05:58:24 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 11 Dec 2020 05:58:25 GMT
EXPOSE 8086
# Fri, 11 Dec 2020 05:58:25 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Dec 2020 05:58:25 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 11 Dec 2020 05:58:25 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 11 Dec 2020 05:58:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 05:58:26 GMT
CMD ["influxd"]
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
	-	`sha256:16278230bdd89f4300bb64c70f52ab02811e9fb441099f76f89267ba46b906cd`  
		Last Modified: Fri, 11 Dec 2020 06:00:06 GMT  
		Size: 1.4 MB (1428310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c81f43dd2eacd80f852db4525a6bf6d6b07845809a5825f580d4dfaacc4b27`  
		Last Modified: Fri, 11 Dec 2020 06:00:39 GMT  
		Size: 87.6 MB (87603740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e73125d511af8f3e6b5dbfdd148c2516a08c9e951f77e42309da23a0bdaf1d`  
		Last Modified: Fri, 11 Dec 2020 06:00:24 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741c5b19fe32bdbc5b9a6b33a47579726ba51b34d175b6f9b69e5aa478cb641c`  
		Last Modified: Fri, 11 Dec 2020 06:00:23 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5561ee1d0ceea24cda29000d0497652dcf43e1d32d1d7bd3716501ff06eb7d2e`  
		Last Modified: Fri, 11 Dec 2020 06:00:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-meta`

```console
$ docker pull influxdb@sha256:9ef0d8cd8a5bfe3181bbe0191405e9b11b928ea7a856c11e46037db93214dac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:17f9442e0f0dd3ae486f57fc2ac1e480785d0e93f94c50da17a9a488ed2492da
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83605830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03100ce017006d24058f1765a73192a1b0fe4aa09818a9fa67fef8b760ee4b63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:10 GMT
ADD file:373a8875589f170b51fa677a3bf736feeb46ea278c553950a3eb3169a2056c12 in / 
# Tue, 17 Nov 2020 20:24:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:43:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:43:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 02:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 19 Nov 2020 02:59:50 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Thu, 19 Nov 2020 03:00:08 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Thu, 19 Nov 2020 03:00:09 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 19 Nov 2020 03:00:09 GMT
EXPOSE 8091
# Thu, 19 Nov 2020 03:00:10 GMT
VOLUME [/var/lib/influxdb]
# Thu, 19 Nov 2020 03:00:10 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 19 Nov 2020 03:00:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 03:00:10 GMT
CMD ["influxd-meta"]
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
	-	`sha256:104e29a2e6403a35ba184667f594419af565fadd04a8ea0b1299d126d395b111`  
		Last Modified: Thu, 19 Nov 2020 03:01:18 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e2a10a2c2e4731a273507888bdde4e51833d0378567d325f4ea2c6870ac41d`  
		Last Modified: Thu, 19 Nov 2020 03:01:57 GMT  
		Size: 23.1 MB (23132657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37c23b5bc506b4f4c60cb3515e33d0d2761046a0b0a5a81cd963729973a8310`  
		Last Modified: Thu, 19 Nov 2020 03:01:54 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fcbf2c39868dda2591f18de6bcbbd4651dbf1390b9cc9ffb4a1bac5b330416`  
		Last Modified: Thu, 19 Nov 2020 03:01:55 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-meta-alpine`

```console
$ docker pull influxdb@sha256:c34ab2359f3885cbdcf38ce6f9aa267a38e0fc398ef52f8e96e27efe21c4e7cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:01018a749900a1844fae98d2fa068d94a3f7acf0dab6497e08664803adbda191
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27228647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea777a31f123d624a04af085e55264a92d6fca6e4a70a71f4da665a6e07ef02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:57:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 11 Dec 2020 05:58:14 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Fri, 11 Dec 2020 05:58:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 05:58:38 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 11 Dec 2020 05:58:38 GMT
EXPOSE 8091
# Fri, 11 Dec 2020 05:58:38 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Dec 2020 05:58:39 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 11 Dec 2020 05:58:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 05:58:39 GMT
CMD ["influxd-meta"]
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
	-	`sha256:16278230bdd89f4300bb64c70f52ab02811e9fb441099f76f89267ba46b906cd`  
		Last Modified: Fri, 11 Dec 2020 06:00:06 GMT  
		Size: 1.4 MB (1428310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141af7cde8b85696f4b2f41957be2ef9e959f3d4aad385349dba80291fb0140f`  
		Last Modified: Fri, 11 Dec 2020 06:00:59 GMT  
		Size: 23.0 MB (23002671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b0b58dca244f083a1c157aa9a11de5be92562b2ca038760de4538ad3ab6eab`  
		Last Modified: Fri, 11 Dec 2020 06:00:46 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058230df2fc50fdf25dbbdafdde1e0053ca242143afd79cc029bce943e5d3640`  
		Last Modified: Fri, 11 Dec 2020 06:00:46 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-alpine`

```console
$ docker pull influxdb@sha256:55fd282870f2328c36879bdd84e3c3acf5439bdb5da692f673b065189cb6812a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:027917368a08f344869aa03a3efa3b72931a6c508fa1b102fec66d5cadb59251
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68068086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd0b0ff56b8047923d4eea96b82884b005dd34e779b29e164adb462cfb2da72`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:57:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 11 Dec 2020 05:57:55 GMT
ENV INFLUXDB_VERSION=1.7.10
# Fri, 11 Dec 2020 05:58:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 05:58:04 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 11 Dec 2020 05:58:04 GMT
EXPOSE 8086
# Fri, 11 Dec 2020 05:58:04 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Dec 2020 05:58:04 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 11 Dec 2020 05:58:05 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 11 Dec 2020 05:58:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 05:58:05 GMT
CMD ["influxd"]
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
	-	`sha256:16278230bdd89f4300bb64c70f52ab02811e9fb441099f76f89267ba46b906cd`  
		Last Modified: Fri, 11 Dec 2020 06:00:06 GMT  
		Size: 1.4 MB (1428310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638b592207e1dca830b35b87ba613acf664e2fbf62e47e19e035481c536edfa1`  
		Last Modified: Fri, 11 Dec 2020 06:00:17 GMT  
		Size: 63.8 MB (63840964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee90a787efdf1302369562e69db0882071fbab5c50db189515fc06d9a07e5be`  
		Last Modified: Fri, 11 Dec 2020 06:00:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7c80cec09dff80fabc858c474147061e9319df08e33bbf64b4ccc08b1d4268`  
		Last Modified: Fri, 11 Dec 2020 06:00:05 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850f3e0ad4af984d6e0ff11d164a6a076c1b7c551811ab15efa31f6c3be7b543`  
		Last Modified: Fri, 11 Dec 2020 06:00:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-data`

```console
$ docker pull influxdb@sha256:0a5743b3137d76328af96c9dee9eae99c469d1a23123d8e09755fbe88829ee99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:9238e40199831fe25dce3279c159c4f94ccd1e213bd2138978efa82f884cdf41
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148386724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9395b9073179eeea4cb24d689c1ef8622186934f02be21cd50e8a05a794e63fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:10 GMT
ADD file:373a8875589f170b51fa677a3bf736feeb46ea278c553950a3eb3169a2056c12 in / 
# Tue, 17 Nov 2020 20:24:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:43:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:43:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 02:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 19 Nov 2020 02:59:50 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Thu, 19 Nov 2020 02:59:56 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Thu, 19 Nov 2020 02:59:57 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 19 Nov 2020 02:59:57 GMT
EXPOSE 8086
# Thu, 19 Nov 2020 02:59:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 19 Nov 2020 02:59:57 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 19 Nov 2020 02:59:58 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 19 Nov 2020 02:59:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 02:59:58 GMT
CMD ["influxd"]
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
	-	`sha256:104e29a2e6403a35ba184667f594419af565fadd04a8ea0b1299d126d395b111`  
		Last Modified: Thu, 19 Nov 2020 03:01:18 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80168f8bff05fa954ee6359e21939edcb441e54d846817fa8978e8aa4564ff7c`  
		Last Modified: Thu, 19 Nov 2020 03:01:48 GMT  
		Size: 87.9 MB (87912342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7a7c4b6a9c05c38450f7539856e5094eb52a36998c41f25945797bb6bc8873`  
		Last Modified: Thu, 19 Nov 2020 03:01:34 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1c2a38ede310fc41026b1a52b3d15a0441bf1ea01212fbc66f6d8a9f18ba6a`  
		Last Modified: Thu, 19 Nov 2020 03:01:34 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97830fd85ffa96d2a831c1861f7b2f47020dda0ecd60fb34b13988040678b8c`  
		Last Modified: Thu, 19 Nov 2020 03:01:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-data-alpine`

```console
$ docker pull influxdb@sha256:b19a2178bf2a877b3a87d2a9fc2fcbbda760bf00bf64201efb53ebe0a3f693ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a87899b74a7728f4d8b0f0287d14206a809bbf5b5cedc6adf319790e26b70c4d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91830922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c44edb6b2bb4e741708fb143b0fa176001d06d51e3f4807cb912aca45674ae4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:57:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 11 Dec 2020 05:58:14 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Fri, 11 Dec 2020 05:58:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 05:58:24 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 11 Dec 2020 05:58:25 GMT
EXPOSE 8086
# Fri, 11 Dec 2020 05:58:25 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Dec 2020 05:58:25 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 11 Dec 2020 05:58:25 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 11 Dec 2020 05:58:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 05:58:26 GMT
CMD ["influxd"]
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
	-	`sha256:16278230bdd89f4300bb64c70f52ab02811e9fb441099f76f89267ba46b906cd`  
		Last Modified: Fri, 11 Dec 2020 06:00:06 GMT  
		Size: 1.4 MB (1428310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c81f43dd2eacd80f852db4525a6bf6d6b07845809a5825f580d4dfaacc4b27`  
		Last Modified: Fri, 11 Dec 2020 06:00:39 GMT  
		Size: 87.6 MB (87603740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e73125d511af8f3e6b5dbfdd148c2516a08c9e951f77e42309da23a0bdaf1d`  
		Last Modified: Fri, 11 Dec 2020 06:00:24 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741c5b19fe32bdbc5b9a6b33a47579726ba51b34d175b6f9b69e5aa478cb641c`  
		Last Modified: Fri, 11 Dec 2020 06:00:23 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5561ee1d0ceea24cda29000d0497652dcf43e1d32d1d7bd3716501ff06eb7d2e`  
		Last Modified: Fri, 11 Dec 2020 06:00:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-meta`

```console
$ docker pull influxdb@sha256:9ef0d8cd8a5bfe3181bbe0191405e9b11b928ea7a856c11e46037db93214dac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:17f9442e0f0dd3ae486f57fc2ac1e480785d0e93f94c50da17a9a488ed2492da
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83605830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03100ce017006d24058f1765a73192a1b0fe4aa09818a9fa67fef8b760ee4b63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:10 GMT
ADD file:373a8875589f170b51fa677a3bf736feeb46ea278c553950a3eb3169a2056c12 in / 
# Tue, 17 Nov 2020 20:24:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:43:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:43:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 02:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 19 Nov 2020 02:59:50 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Thu, 19 Nov 2020 03:00:08 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Thu, 19 Nov 2020 03:00:09 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 19 Nov 2020 03:00:09 GMT
EXPOSE 8091
# Thu, 19 Nov 2020 03:00:10 GMT
VOLUME [/var/lib/influxdb]
# Thu, 19 Nov 2020 03:00:10 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 19 Nov 2020 03:00:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 03:00:10 GMT
CMD ["influxd-meta"]
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
	-	`sha256:104e29a2e6403a35ba184667f594419af565fadd04a8ea0b1299d126d395b111`  
		Last Modified: Thu, 19 Nov 2020 03:01:18 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e2a10a2c2e4731a273507888bdde4e51833d0378567d325f4ea2c6870ac41d`  
		Last Modified: Thu, 19 Nov 2020 03:01:57 GMT  
		Size: 23.1 MB (23132657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37c23b5bc506b4f4c60cb3515e33d0d2761046a0b0a5a81cd963729973a8310`  
		Last Modified: Thu, 19 Nov 2020 03:01:54 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fcbf2c39868dda2591f18de6bcbbd4651dbf1390b9cc9ffb4a1bac5b330416`  
		Last Modified: Thu, 19 Nov 2020 03:01:55 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-meta-alpine`

```console
$ docker pull influxdb@sha256:c34ab2359f3885cbdcf38ce6f9aa267a38e0fc398ef52f8e96e27efe21c4e7cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:01018a749900a1844fae98d2fa068d94a3f7acf0dab6497e08664803adbda191
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27228647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea777a31f123d624a04af085e55264a92d6fca6e4a70a71f4da665a6e07ef02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:57:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 11 Dec 2020 05:58:14 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Fri, 11 Dec 2020 05:58:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 05:58:38 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 11 Dec 2020 05:58:38 GMT
EXPOSE 8091
# Fri, 11 Dec 2020 05:58:38 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Dec 2020 05:58:39 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 11 Dec 2020 05:58:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 05:58:39 GMT
CMD ["influxd-meta"]
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
	-	`sha256:16278230bdd89f4300bb64c70f52ab02811e9fb441099f76f89267ba46b906cd`  
		Last Modified: Fri, 11 Dec 2020 06:00:06 GMT  
		Size: 1.4 MB (1428310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141af7cde8b85696f4b2f41957be2ef9e959f3d4aad385349dba80291fb0140f`  
		Last Modified: Fri, 11 Dec 2020 06:00:59 GMT  
		Size: 23.0 MB (23002671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b0b58dca244f083a1c157aa9a11de5be92562b2ca038760de4538ad3ab6eab`  
		Last Modified: Fri, 11 Dec 2020 06:00:46 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058230df2fc50fdf25dbbdafdde1e0053ca242143afd79cc029bce943e5d3640`  
		Last Modified: Fri, 11 Dec 2020 06:00:46 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8`

```console
$ docker pull influxdb@sha256:79b696e8a268752e7439a2fb9091aa81ca3d952817c5d6bc34a8f4702da3c8f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8` - linux; amd64

```console
$ docker pull influxdb@sha256:951292a96756693195c5a96e11b8e1c79f14749f2c004f1de9ac9d502624188e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125440219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a5428c2469cef47413b293fc17b1da120d577d50064d10b2b781a88ff9c4eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:10 GMT
ADD file:373a8875589f170b51fa677a3bf736feeb46ea278c553950a3eb3169a2056c12 in / 
# Tue, 17 Nov 2020 20:24:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:43:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:43:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 02:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 19 Nov 2020 03:00:19 GMT
ENV INFLUXDB_VERSION=1.8.3
# Thu, 19 Nov 2020 03:00:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 19 Nov 2020 03:00:26 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 19 Nov 2020 03:00:26 GMT
EXPOSE 8086
# Thu, 19 Nov 2020 03:00:26 GMT
VOLUME [/var/lib/influxdb]
# Thu, 19 Nov 2020 03:00:26 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 19 Nov 2020 03:00:26 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 19 Nov 2020 03:00:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 03:00:27 GMT
CMD ["influxd"]
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
	-	`sha256:104e29a2e6403a35ba184667f594419af565fadd04a8ea0b1299d126d395b111`  
		Last Modified: Thu, 19 Nov 2020 03:01:18 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4b1b122afb2004f76e5168e1ffa51017fba2803ae8ee5b0affd7c01f81fb67`  
		Last Modified: Thu, 19 Nov 2020 03:02:13 GMT  
		Size: 65.0 MB (64965897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bc9004943d25c7fab8a1d5bdbfc23c29f14d59598dbbe170720f4ebb0c8488`  
		Last Modified: Thu, 19 Nov 2020 03:02:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73260672624f4755cce96b694e24e6e4c2fd39bc3b5cf94f73b635872db0074`  
		Last Modified: Thu, 19 Nov 2020 03:02:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a9d5d6c830c823eb15ce49b2ff6646c6d92ee009cbe159a22462d4e9d9c0d4`  
		Last Modified: Thu, 19 Nov 2020 03:02:03 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm variant v7

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

### `influxdb:1.8` - linux; arm64 variant v8

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

## `influxdb:1.8.3`

```console
$ docker pull influxdb@sha256:79b696e8a268752e7439a2fb9091aa81ca3d952817c5d6bc34a8f4702da3c8f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8.3` - linux; amd64

```console
$ docker pull influxdb@sha256:951292a96756693195c5a96e11b8e1c79f14749f2c004f1de9ac9d502624188e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125440219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a5428c2469cef47413b293fc17b1da120d577d50064d10b2b781a88ff9c4eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:10 GMT
ADD file:373a8875589f170b51fa677a3bf736feeb46ea278c553950a3eb3169a2056c12 in / 
# Tue, 17 Nov 2020 20:24:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:43:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:43:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 02:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 19 Nov 2020 03:00:19 GMT
ENV INFLUXDB_VERSION=1.8.3
# Thu, 19 Nov 2020 03:00:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 19 Nov 2020 03:00:26 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 19 Nov 2020 03:00:26 GMT
EXPOSE 8086
# Thu, 19 Nov 2020 03:00:26 GMT
VOLUME [/var/lib/influxdb]
# Thu, 19 Nov 2020 03:00:26 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 19 Nov 2020 03:00:26 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 19 Nov 2020 03:00:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 03:00:27 GMT
CMD ["influxd"]
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
	-	`sha256:104e29a2e6403a35ba184667f594419af565fadd04a8ea0b1299d126d395b111`  
		Last Modified: Thu, 19 Nov 2020 03:01:18 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4b1b122afb2004f76e5168e1ffa51017fba2803ae8ee5b0affd7c01f81fb67`  
		Last Modified: Thu, 19 Nov 2020 03:02:13 GMT  
		Size: 65.0 MB (64965897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bc9004943d25c7fab8a1d5bdbfc23c29f14d59598dbbe170720f4ebb0c8488`  
		Last Modified: Thu, 19 Nov 2020 03:02:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73260672624f4755cce96b694e24e6e4c2fd39bc3b5cf94f73b635872db0074`  
		Last Modified: Thu, 19 Nov 2020 03:02:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a9d5d6c830c823eb15ce49b2ff6646c6d92ee009cbe159a22462d4e9d9c0d4`  
		Last Modified: Thu, 19 Nov 2020 03:02:03 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.3` - linux; arm variant v7

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

### `influxdb:1.8.3` - linux; arm64 variant v8

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

## `influxdb:1.8.3-alpine`

```console
$ docker pull influxdb@sha256:52e471985734dd73933aff6b0daf770e6aebf307a4f0925d6220a211de66595e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a1c38c710abb2ee0be830a5ac57789ba0ceeb0f79d3583f8b47d1fb0cf482e30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68933770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e061095b61d5920d53e808b0d8ce1134624158f043e017ba9e859632e1d594bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:57:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 11 Dec 2020 05:58:48 GMT
ENV INFLUXDB_VERSION=1.8.3
# Fri, 11 Dec 2020 05:58:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 05:58:56 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 11 Dec 2020 05:58:56 GMT
EXPOSE 8086
# Fri, 11 Dec 2020 05:58:56 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Dec 2020 05:58:57 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 11 Dec 2020 05:58:57 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 11 Dec 2020 05:58:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 05:58:59 GMT
CMD ["influxd"]
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
	-	`sha256:16278230bdd89f4300bb64c70f52ab02811e9fb441099f76f89267ba46b906cd`  
		Last Modified: Fri, 11 Dec 2020 06:00:06 GMT  
		Size: 1.4 MB (1428310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056c44bbdc51aa73cd9de60ffaa505b66f7194e5402020a2404e27974fd24601`  
		Last Modified: Fri, 11 Dec 2020 06:01:17 GMT  
		Size: 64.7 MB (64706649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376c7d2a5561044f029818a7222fa08a97d085bfe122714cb654aec53f22db57`  
		Last Modified: Fri, 11 Dec 2020 06:01:06 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8e1099256915eb16a29e17791adadfffaa9b5ae7ff33795cd837dd68331c9f`  
		Last Modified: Fri, 11 Dec 2020 06:01:06 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a7b06848b95420ba60e38aed5172e4228ced9019f7871ccbd4f56408b51164`  
		Last Modified: Fri, 11 Dec 2020 06:01:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-data`

```console
$ docker pull influxdb@sha256:219098efbe625774e528732cc778b43edc1ecaa632ea69da2e746fa41530fcda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-data` - linux; amd64

```console
$ docker pull influxdb@sha256:47bbfc2d214d6f8a23cf9b96e1abc3a7c895b4c1a34240f25211f3ebda84cc5b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126270435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c04806af37866251de2676fdd8390eca3841bbb0aa621b8af8322f94e44a7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:10 GMT
ADD file:373a8875589f170b51fa677a3bf736feeb46ea278c553950a3eb3169a2056c12 in / 
# Tue, 17 Nov 2020 20:24:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:43:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:43:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 02:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 19 Nov 2020 03:00:35 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Thu, 19 Nov 2020 03:00:42 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Thu, 19 Nov 2020 03:00:43 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 19 Nov 2020 03:00:43 GMT
EXPOSE 8086
# Thu, 19 Nov 2020 03:00:43 GMT
VOLUME [/var/lib/influxdb]
# Thu, 19 Nov 2020 03:00:43 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 19 Nov 2020 03:00:43 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 19 Nov 2020 03:00:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 03:00:44 GMT
CMD ["influxd"]
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
	-	`sha256:104e29a2e6403a35ba184667f594419af565fadd04a8ea0b1299d126d395b111`  
		Last Modified: Thu, 19 Nov 2020 03:01:18 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced307a3661f1076066a25b196cbbaf378a251b493c3b22ac174504c0359e178`  
		Last Modified: Thu, 19 Nov 2020 03:02:31 GMT  
		Size: 65.8 MB (65796057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8b8565f6454c36f829cebbef13f46c0910398d38bf3669c20620ada01a3c75`  
		Last Modified: Thu, 19 Nov 2020 03:02:22 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769df3f9cd5f00c29a2467ff893c140ef2e0d0e3b8fa5552857948589cef2e94`  
		Last Modified: Thu, 19 Nov 2020 03:02:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7b13b57cd44dbfef1276456008d767cbc610833d07a5b2bdd15a9a8997e7a0`  
		Last Modified: Thu, 19 Nov 2020 03:02:21 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-data-alpine`

```console
$ docker pull influxdb@sha256:1c87a9977d2fc65671852b1b5c31e70534d217262d7f415fa98b12d94fe4ceee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:3c345f2719cd0e36c1974cd4ac409bac8ac849f06485f45a58b3a8fb73c66608
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69768139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8053ef724bc76312772b2a367cd762f35b7506765322fd97f1c58cd55b5f7ccc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:57:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 11 Dec 2020 05:59:08 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Fri, 11 Dec 2020 05:59:14 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 05:59:15 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 11 Dec 2020 05:59:15 GMT
EXPOSE 8086
# Fri, 11 Dec 2020 05:59:15 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Dec 2020 05:59:15 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 11 Dec 2020 05:59:16 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 11 Dec 2020 05:59:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 05:59:16 GMT
CMD ["influxd"]
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
	-	`sha256:16278230bdd89f4300bb64c70f52ab02811e9fb441099f76f89267ba46b906cd`  
		Last Modified: Fri, 11 Dec 2020 06:00:06 GMT  
		Size: 1.4 MB (1428310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a30a42ee9180ddc3113a2340beaf2640f180f3b931c3f518e8f43e08d41fdc`  
		Last Modified: Fri, 11 Dec 2020 06:01:37 GMT  
		Size: 65.5 MB (65540957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43037875c9114dab7ac19a7706f707243f179b6ce6747d222e3360be4610839d`  
		Last Modified: Fri, 11 Dec 2020 06:01:26 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40d1d20fe9c8f9431342c512b83d826b544f5955642d96e09c6f25de99ff4f1`  
		Last Modified: Fri, 11 Dec 2020 06:01:26 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85e4ac6ecf6b434790c5db134b171788aca3e40ed6abdb98066007274e608d1`  
		Last Modified: Fri, 11 Dec 2020 06:01:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-meta`

```console
$ docker pull influxdb@sha256:08c4e7f02d8308b1dee992735f5c77ad59938cd6d84aef589939a58934c9feee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:55c68eb777f6e8e268648ac1e9ec8869ceb017ecd78ef7ca2121e31650cf1c41
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83338493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6354163cd7e0770dc7dc4d92646406934f89719e674eb978bba9a789ba2d93ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:10 GMT
ADD file:373a8875589f170b51fa677a3bf736feeb46ea278c553950a3eb3169a2056c12 in / 
# Tue, 17 Nov 2020 20:24:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:43:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:43:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 02:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 19 Nov 2020 03:00:35 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Thu, 19 Nov 2020 03:00:55 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Thu, 19 Nov 2020 03:00:55 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 19 Nov 2020 03:00:55 GMT
EXPOSE 8091
# Thu, 19 Nov 2020 03:00:55 GMT
VOLUME [/var/lib/influxdb]
# Thu, 19 Nov 2020 03:00:55 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 19 Nov 2020 03:00:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 03:00:56 GMT
CMD ["influxd-meta"]
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
	-	`sha256:104e29a2e6403a35ba184667f594419af565fadd04a8ea0b1299d126d395b111`  
		Last Modified: Thu, 19 Nov 2020 03:01:18 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87ee02b2d037b396be1f3561c4d48816ad67b2e0136e7fb12c60c2056030aaf`  
		Last Modified: Thu, 19 Nov 2020 03:02:42 GMT  
		Size: 22.9 MB (22865318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0808c56a0750198f301cce739b65b2204ac082e0730df9ff32b83ad8559bb74d`  
		Last Modified: Thu, 19 Nov 2020 03:02:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8253165bde66516e7d004704808ab12e4d0769886ad05b1cd74196d9045288`  
		Last Modified: Thu, 19 Nov 2020 03:02:39 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-meta-alpine`

```console
$ docker pull influxdb@sha256:aba45952ba793deaaa74101d0c0e202937ca2aa1ffdeba836f15f16a4f2132bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:6de36161d71b004db9cd31ad612af158d39191aad0c2a1d0693c2fccac00f46b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26961458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588f43fb7cf000ae30a9a8e8f3ccb602acb3c89a831a047dec2c0b597c972603`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:57:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 11 Dec 2020 05:59:08 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Fri, 11 Dec 2020 05:59:28 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 05:59:28 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 11 Dec 2020 05:59:28 GMT
EXPOSE 8091
# Fri, 11 Dec 2020 05:59:29 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Dec 2020 05:59:29 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 11 Dec 2020 05:59:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 05:59:29 GMT
CMD ["influxd-meta"]
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
	-	`sha256:16278230bdd89f4300bb64c70f52ab02811e9fb441099f76f89267ba46b906cd`  
		Last Modified: Fri, 11 Dec 2020 06:00:06 GMT  
		Size: 1.4 MB (1428310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439e80f23f5fdb224b0e548ff276d0fd87d74ef07d5b9331e70ff1a95114e118`  
		Last Modified: Fri, 11 Dec 2020 06:01:49 GMT  
		Size: 22.7 MB (22735481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f624aaa254c210e8f87b8be506925d54e7ce9dfd01210b97a72b4c1ed11b79`  
		Last Modified: Fri, 11 Dec 2020 06:01:46 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87faa02d0b3f3414f42ecf87842e3d2782294b5ba32a2e001c0495e02988cff4`  
		Last Modified: Fri, 11 Dec 2020 06:01:46 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-alpine`

```console
$ docker pull influxdb@sha256:52e471985734dd73933aff6b0daf770e6aebf307a4f0925d6220a211de66595e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a1c38c710abb2ee0be830a5ac57789ba0ceeb0f79d3583f8b47d1fb0cf482e30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68933770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e061095b61d5920d53e808b0d8ce1134624158f043e017ba9e859632e1d594bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:57:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 11 Dec 2020 05:58:48 GMT
ENV INFLUXDB_VERSION=1.8.3
# Fri, 11 Dec 2020 05:58:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 05:58:56 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 11 Dec 2020 05:58:56 GMT
EXPOSE 8086
# Fri, 11 Dec 2020 05:58:56 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Dec 2020 05:58:57 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 11 Dec 2020 05:58:57 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 11 Dec 2020 05:58:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 05:58:59 GMT
CMD ["influxd"]
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
	-	`sha256:16278230bdd89f4300bb64c70f52ab02811e9fb441099f76f89267ba46b906cd`  
		Last Modified: Fri, 11 Dec 2020 06:00:06 GMT  
		Size: 1.4 MB (1428310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056c44bbdc51aa73cd9de60ffaa505b66f7194e5402020a2404e27974fd24601`  
		Last Modified: Fri, 11 Dec 2020 06:01:17 GMT  
		Size: 64.7 MB (64706649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376c7d2a5561044f029818a7222fa08a97d085bfe122714cb654aec53f22db57`  
		Last Modified: Fri, 11 Dec 2020 06:01:06 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8e1099256915eb16a29e17791adadfffaa9b5ae7ff33795cd837dd68331c9f`  
		Last Modified: Fri, 11 Dec 2020 06:01:06 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a7b06848b95420ba60e38aed5172e4228ced9019f7871ccbd4f56408b51164`  
		Last Modified: Fri, 11 Dec 2020 06:01:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data`

```console
$ docker pull influxdb@sha256:219098efbe625774e528732cc778b43edc1ecaa632ea69da2e746fa41530fcda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:47bbfc2d214d6f8a23cf9b96e1abc3a7c895b4c1a34240f25211f3ebda84cc5b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126270435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c04806af37866251de2676fdd8390eca3841bbb0aa621b8af8322f94e44a7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:10 GMT
ADD file:373a8875589f170b51fa677a3bf736feeb46ea278c553950a3eb3169a2056c12 in / 
# Tue, 17 Nov 2020 20:24:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:43:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:43:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 02:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 19 Nov 2020 03:00:35 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Thu, 19 Nov 2020 03:00:42 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Thu, 19 Nov 2020 03:00:43 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 19 Nov 2020 03:00:43 GMT
EXPOSE 8086
# Thu, 19 Nov 2020 03:00:43 GMT
VOLUME [/var/lib/influxdb]
# Thu, 19 Nov 2020 03:00:43 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 19 Nov 2020 03:00:43 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 19 Nov 2020 03:00:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 03:00:44 GMT
CMD ["influxd"]
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
	-	`sha256:104e29a2e6403a35ba184667f594419af565fadd04a8ea0b1299d126d395b111`  
		Last Modified: Thu, 19 Nov 2020 03:01:18 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced307a3661f1076066a25b196cbbaf378a251b493c3b22ac174504c0359e178`  
		Last Modified: Thu, 19 Nov 2020 03:02:31 GMT  
		Size: 65.8 MB (65796057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8b8565f6454c36f829cebbef13f46c0910398d38bf3669c20620ada01a3c75`  
		Last Modified: Thu, 19 Nov 2020 03:02:22 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769df3f9cd5f00c29a2467ff893c140ef2e0d0e3b8fa5552857948589cef2e94`  
		Last Modified: Thu, 19 Nov 2020 03:02:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7b13b57cd44dbfef1276456008d767cbc610833d07a5b2bdd15a9a8997e7a0`  
		Last Modified: Thu, 19 Nov 2020 03:02:21 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data-alpine`

```console
$ docker pull influxdb@sha256:1c87a9977d2fc65671852b1b5c31e70534d217262d7f415fa98b12d94fe4ceee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:3c345f2719cd0e36c1974cd4ac409bac8ac849f06485f45a58b3a8fb73c66608
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69768139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8053ef724bc76312772b2a367cd762f35b7506765322fd97f1c58cd55b5f7ccc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:57:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 11 Dec 2020 05:59:08 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Fri, 11 Dec 2020 05:59:14 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 05:59:15 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 11 Dec 2020 05:59:15 GMT
EXPOSE 8086
# Fri, 11 Dec 2020 05:59:15 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Dec 2020 05:59:15 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 11 Dec 2020 05:59:16 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 11 Dec 2020 05:59:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 05:59:16 GMT
CMD ["influxd"]
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
	-	`sha256:16278230bdd89f4300bb64c70f52ab02811e9fb441099f76f89267ba46b906cd`  
		Last Modified: Fri, 11 Dec 2020 06:00:06 GMT  
		Size: 1.4 MB (1428310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a30a42ee9180ddc3113a2340beaf2640f180f3b931c3f518e8f43e08d41fdc`  
		Last Modified: Fri, 11 Dec 2020 06:01:37 GMT  
		Size: 65.5 MB (65540957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43037875c9114dab7ac19a7706f707243f179b6ce6747d222e3360be4610839d`  
		Last Modified: Fri, 11 Dec 2020 06:01:26 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40d1d20fe9c8f9431342c512b83d826b544f5955642d96e09c6f25de99ff4f1`  
		Last Modified: Fri, 11 Dec 2020 06:01:26 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85e4ac6ecf6b434790c5db134b171788aca3e40ed6abdb98066007274e608d1`  
		Last Modified: Fri, 11 Dec 2020 06:01:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-meta`

```console
$ docker pull influxdb@sha256:08c4e7f02d8308b1dee992735f5c77ad59938cd6d84aef589939a58934c9feee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:55c68eb777f6e8e268648ac1e9ec8869ceb017ecd78ef7ca2121e31650cf1c41
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83338493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6354163cd7e0770dc7dc4d92646406934f89719e674eb978bba9a789ba2d93ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:10 GMT
ADD file:373a8875589f170b51fa677a3bf736feeb46ea278c553950a3eb3169a2056c12 in / 
# Tue, 17 Nov 2020 20:24:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:43:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:43:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 02:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 19 Nov 2020 03:00:35 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Thu, 19 Nov 2020 03:00:55 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Thu, 19 Nov 2020 03:00:55 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 19 Nov 2020 03:00:55 GMT
EXPOSE 8091
# Thu, 19 Nov 2020 03:00:55 GMT
VOLUME [/var/lib/influxdb]
# Thu, 19 Nov 2020 03:00:55 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 19 Nov 2020 03:00:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 03:00:56 GMT
CMD ["influxd-meta"]
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
	-	`sha256:104e29a2e6403a35ba184667f594419af565fadd04a8ea0b1299d126d395b111`  
		Last Modified: Thu, 19 Nov 2020 03:01:18 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87ee02b2d037b396be1f3561c4d48816ad67b2e0136e7fb12c60c2056030aaf`  
		Last Modified: Thu, 19 Nov 2020 03:02:42 GMT  
		Size: 22.9 MB (22865318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0808c56a0750198f301cce739b65b2204ac082e0730df9ff32b83ad8559bb74d`  
		Last Modified: Thu, 19 Nov 2020 03:02:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8253165bde66516e7d004704808ab12e4d0769886ad05b1cd74196d9045288`  
		Last Modified: Thu, 19 Nov 2020 03:02:39 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-meta-alpine`

```console
$ docker pull influxdb@sha256:aba45952ba793deaaa74101d0c0e202937ca2aa1ffdeba836f15f16a4f2132bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:6de36161d71b004db9cd31ad612af158d39191aad0c2a1d0693c2fccac00f46b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26961458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588f43fb7cf000ae30a9a8e8f3ccb602acb3c89a831a047dec2c0b597c972603`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:57:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 11 Dec 2020 05:59:08 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Fri, 11 Dec 2020 05:59:28 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 05:59:28 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 11 Dec 2020 05:59:28 GMT
EXPOSE 8091
# Fri, 11 Dec 2020 05:59:29 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Dec 2020 05:59:29 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 11 Dec 2020 05:59:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 05:59:29 GMT
CMD ["influxd-meta"]
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
	-	`sha256:16278230bdd89f4300bb64c70f52ab02811e9fb441099f76f89267ba46b906cd`  
		Last Modified: Fri, 11 Dec 2020 06:00:06 GMT  
		Size: 1.4 MB (1428310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439e80f23f5fdb224b0e548ff276d0fd87d74ef07d5b9331e70ff1a95114e118`  
		Last Modified: Fri, 11 Dec 2020 06:01:49 GMT  
		Size: 22.7 MB (22735481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f624aaa254c210e8f87b8be506925d54e7ce9dfd01210b97a72b4c1ed11b79`  
		Last Modified: Fri, 11 Dec 2020 06:01:46 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87faa02d0b3f3414f42ecf87842e3d2782294b5ba32a2e001c0495e02988cff4`  
		Last Modified: Fri, 11 Dec 2020 06:01:46 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:52e471985734dd73933aff6b0daf770e6aebf307a4f0925d6220a211de66595e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a1c38c710abb2ee0be830a5ac57789ba0ceeb0f79d3583f8b47d1fb0cf482e30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68933770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e061095b61d5920d53e808b0d8ce1134624158f043e017ba9e859632e1d594bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:57:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 11 Dec 2020 05:58:48 GMT
ENV INFLUXDB_VERSION=1.8.3
# Fri, 11 Dec 2020 05:58:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 05:58:56 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 11 Dec 2020 05:58:56 GMT
EXPOSE 8086
# Fri, 11 Dec 2020 05:58:56 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Dec 2020 05:58:57 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 11 Dec 2020 05:58:57 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 11 Dec 2020 05:58:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 05:58:59 GMT
CMD ["influxd"]
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
	-	`sha256:16278230bdd89f4300bb64c70f52ab02811e9fb441099f76f89267ba46b906cd`  
		Last Modified: Fri, 11 Dec 2020 06:00:06 GMT  
		Size: 1.4 MB (1428310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056c44bbdc51aa73cd9de60ffaa505b66f7194e5402020a2404e27974fd24601`  
		Last Modified: Fri, 11 Dec 2020 06:01:17 GMT  
		Size: 64.7 MB (64706649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376c7d2a5561044f029818a7222fa08a97d085bfe122714cb654aec53f22db57`  
		Last Modified: Fri, 11 Dec 2020 06:01:06 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8e1099256915eb16a29e17791adadfffaa9b5ae7ff33795cd837dd68331c9f`  
		Last Modified: Fri, 11 Dec 2020 06:01:06 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a7b06848b95420ba60e38aed5172e4228ced9019f7871ccbd4f56408b51164`  
		Last Modified: Fri, 11 Dec 2020 06:01:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data`

```console
$ docker pull influxdb@sha256:219098efbe625774e528732cc778b43edc1ecaa632ea69da2e746fa41530fcda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:47bbfc2d214d6f8a23cf9b96e1abc3a7c895b4c1a34240f25211f3ebda84cc5b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126270435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c04806af37866251de2676fdd8390eca3841bbb0aa621b8af8322f94e44a7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:10 GMT
ADD file:373a8875589f170b51fa677a3bf736feeb46ea278c553950a3eb3169a2056c12 in / 
# Tue, 17 Nov 2020 20:24:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:43:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:43:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 02:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 19 Nov 2020 03:00:35 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Thu, 19 Nov 2020 03:00:42 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Thu, 19 Nov 2020 03:00:43 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 19 Nov 2020 03:00:43 GMT
EXPOSE 8086
# Thu, 19 Nov 2020 03:00:43 GMT
VOLUME [/var/lib/influxdb]
# Thu, 19 Nov 2020 03:00:43 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 19 Nov 2020 03:00:43 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 19 Nov 2020 03:00:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 03:00:44 GMT
CMD ["influxd"]
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
	-	`sha256:104e29a2e6403a35ba184667f594419af565fadd04a8ea0b1299d126d395b111`  
		Last Modified: Thu, 19 Nov 2020 03:01:18 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced307a3661f1076066a25b196cbbaf378a251b493c3b22ac174504c0359e178`  
		Last Modified: Thu, 19 Nov 2020 03:02:31 GMT  
		Size: 65.8 MB (65796057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8b8565f6454c36f829cebbef13f46c0910398d38bf3669c20620ada01a3c75`  
		Last Modified: Thu, 19 Nov 2020 03:02:22 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769df3f9cd5f00c29a2467ff893c140ef2e0d0e3b8fa5552857948589cef2e94`  
		Last Modified: Thu, 19 Nov 2020 03:02:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7b13b57cd44dbfef1276456008d767cbc610833d07a5b2bdd15a9a8997e7a0`  
		Last Modified: Thu, 19 Nov 2020 03:02:21 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:1c87a9977d2fc65671852b1b5c31e70534d217262d7f415fa98b12d94fe4ceee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:3c345f2719cd0e36c1974cd4ac409bac8ac849f06485f45a58b3a8fb73c66608
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69768139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8053ef724bc76312772b2a367cd762f35b7506765322fd97f1c58cd55b5f7ccc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:57:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 11 Dec 2020 05:59:08 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Fri, 11 Dec 2020 05:59:14 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 05:59:15 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 11 Dec 2020 05:59:15 GMT
EXPOSE 8086
# Fri, 11 Dec 2020 05:59:15 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Dec 2020 05:59:15 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 11 Dec 2020 05:59:16 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 11 Dec 2020 05:59:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 05:59:16 GMT
CMD ["influxd"]
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
	-	`sha256:16278230bdd89f4300bb64c70f52ab02811e9fb441099f76f89267ba46b906cd`  
		Last Modified: Fri, 11 Dec 2020 06:00:06 GMT  
		Size: 1.4 MB (1428310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a30a42ee9180ddc3113a2340beaf2640f180f3b931c3f518e8f43e08d41fdc`  
		Last Modified: Fri, 11 Dec 2020 06:01:37 GMT  
		Size: 65.5 MB (65540957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43037875c9114dab7ac19a7706f707243f179b6ce6747d222e3360be4610839d`  
		Last Modified: Fri, 11 Dec 2020 06:01:26 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40d1d20fe9c8f9431342c512b83d826b544f5955642d96e09c6f25de99ff4f1`  
		Last Modified: Fri, 11 Dec 2020 06:01:26 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85e4ac6ecf6b434790c5db134b171788aca3e40ed6abdb98066007274e608d1`  
		Last Modified: Fri, 11 Dec 2020 06:01:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:79b696e8a268752e7439a2fb9091aa81ca3d952817c5d6bc34a8f4702da3c8f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:951292a96756693195c5a96e11b8e1c79f14749f2c004f1de9ac9d502624188e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125440219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a5428c2469cef47413b293fc17b1da120d577d50064d10b2b781a88ff9c4eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:10 GMT
ADD file:373a8875589f170b51fa677a3bf736feeb46ea278c553950a3eb3169a2056c12 in / 
# Tue, 17 Nov 2020 20:24:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:43:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:43:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 02:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 19 Nov 2020 03:00:19 GMT
ENV INFLUXDB_VERSION=1.8.3
# Thu, 19 Nov 2020 03:00:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 19 Nov 2020 03:00:26 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 19 Nov 2020 03:00:26 GMT
EXPOSE 8086
# Thu, 19 Nov 2020 03:00:26 GMT
VOLUME [/var/lib/influxdb]
# Thu, 19 Nov 2020 03:00:26 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 19 Nov 2020 03:00:26 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 19 Nov 2020 03:00:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 03:00:27 GMT
CMD ["influxd"]
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
	-	`sha256:104e29a2e6403a35ba184667f594419af565fadd04a8ea0b1299d126d395b111`  
		Last Modified: Thu, 19 Nov 2020 03:01:18 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4b1b122afb2004f76e5168e1ffa51017fba2803ae8ee5b0affd7c01f81fb67`  
		Last Modified: Thu, 19 Nov 2020 03:02:13 GMT  
		Size: 65.0 MB (64965897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bc9004943d25c7fab8a1d5bdbfc23c29f14d59598dbbe170720f4ebb0c8488`  
		Last Modified: Thu, 19 Nov 2020 03:02:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73260672624f4755cce96b694e24e6e4c2fd39bc3b5cf94f73b635872db0074`  
		Last Modified: Thu, 19 Nov 2020 03:02:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a9d5d6c830c823eb15ce49b2ff6646c6d92ee009cbe159a22462d4e9d9c0d4`  
		Last Modified: Thu, 19 Nov 2020 03:02:03 GMT  
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

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:08c4e7f02d8308b1dee992735f5c77ad59938cd6d84aef589939a58934c9feee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:55c68eb777f6e8e268648ac1e9ec8869ceb017ecd78ef7ca2121e31650cf1c41
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83338493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6354163cd7e0770dc7dc4d92646406934f89719e674eb978bba9a789ba2d93ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:10 GMT
ADD file:373a8875589f170b51fa677a3bf736feeb46ea278c553950a3eb3169a2056c12 in / 
# Tue, 17 Nov 2020 20:24:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:43:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:43:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 02:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 19 Nov 2020 03:00:35 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Thu, 19 Nov 2020 03:00:55 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Thu, 19 Nov 2020 03:00:55 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 19 Nov 2020 03:00:55 GMT
EXPOSE 8091
# Thu, 19 Nov 2020 03:00:55 GMT
VOLUME [/var/lib/influxdb]
# Thu, 19 Nov 2020 03:00:55 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 19 Nov 2020 03:00:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Nov 2020 03:00:56 GMT
CMD ["influxd-meta"]
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
	-	`sha256:104e29a2e6403a35ba184667f594419af565fadd04a8ea0b1299d126d395b111`  
		Last Modified: Thu, 19 Nov 2020 03:01:18 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87ee02b2d037b396be1f3561c4d48816ad67b2e0136e7fb12c60c2056030aaf`  
		Last Modified: Thu, 19 Nov 2020 03:02:42 GMT  
		Size: 22.9 MB (22865318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0808c56a0750198f301cce739b65b2204ac082e0730df9ff32b83ad8559bb74d`  
		Last Modified: Thu, 19 Nov 2020 03:02:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8253165bde66516e7d004704808ab12e4d0769886ad05b1cd74196d9045288`  
		Last Modified: Thu, 19 Nov 2020 03:02:39 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta-alpine`

```console
$ docker pull influxdb@sha256:aba45952ba793deaaa74101d0c0e202937ca2aa1ffdeba836f15f16a4f2132bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:6de36161d71b004db9cd31ad612af158d39191aad0c2a1d0693c2fccac00f46b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26961458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588f43fb7cf000ae30a9a8e8f3ccb602acb3c89a831a047dec2c0b597c972603`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:57:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 11 Dec 2020 05:59:08 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Fri, 11 Dec 2020 05:59:28 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 05:59:28 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 11 Dec 2020 05:59:28 GMT
EXPOSE 8091
# Fri, 11 Dec 2020 05:59:29 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Dec 2020 05:59:29 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 11 Dec 2020 05:59:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 05:59:29 GMT
CMD ["influxd-meta"]
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
	-	`sha256:16278230bdd89f4300bb64c70f52ab02811e9fb441099f76f89267ba46b906cd`  
		Last Modified: Fri, 11 Dec 2020 06:00:06 GMT  
		Size: 1.4 MB (1428310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439e80f23f5fdb224b0e548ff276d0fd87d74ef07d5b9331e70ff1a95114e118`  
		Last Modified: Fri, 11 Dec 2020 06:01:49 GMT  
		Size: 22.7 MB (22735481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f624aaa254c210e8f87b8be506925d54e7ce9dfd01210b97a72b4c1ed11b79`  
		Last Modified: Fri, 11 Dec 2020 06:01:46 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87faa02d0b3f3414f42ecf87842e3d2782294b5ba32a2e001c0495e02988cff4`  
		Last Modified: Fri, 11 Dec 2020 06:01:46 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
