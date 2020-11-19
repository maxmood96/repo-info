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
$ docker pull influxdb@sha256:995a3d509e4df00cf938ddefb38161d934dfac6c3362dfc43283adde0bdd3cc8
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
$ docker pull influxdb@sha256:995a3d509e4df00cf938ddefb38161d934dfac6c3362dfc43283adde0bdd3cc8
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
$ docker pull influxdb@sha256:8ca9dcb656fda408443afa6e3dfef8e5e08335427101fdec5caaaef10f2d9cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a6bb057ca821b606f238162dab6d1499ca858caea2bc12260392c793af19fa43
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67943085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b3c3bda5307e814906e9db921e6e571afaed1b617fd1449f1fe441060f818c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:28:23 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 22 Oct 2020 04:28:23 GMT
ENV INFLUXDB_VERSION=1.7.10
# Thu, 22 Oct 2020 04:28:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 22 Oct 2020 04:28:35 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 22 Oct 2020 04:28:35 GMT
EXPOSE 8086
# Thu, 22 Oct 2020 04:28:35 GMT
VOLUME [/var/lib/influxdb]
# Thu, 22 Oct 2020 04:28:36 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 22 Oct 2020 04:28:36 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 22 Oct 2020 04:28:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Oct 2020 04:28:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f09710cb1e9d1e2b329758d6e450a28347bc3d5b9279be1c2f97edf904405`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 1.3 MB (1303321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b51ff1a057029f76ca3d93bf4ade3c0d6c59310622853739f7c473d4d71db57`  
		Last Modified: Thu, 22 Oct 2020 04:31:24 GMT  
		Size: 63.8 MB (63841035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d946660a65bf0b75ad63981bf17617d4a954cc2d2c61c76ee13086a7bf35305`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a085fd5908bfe1eba0d441b84470151d95fceec61695a2cd2693f79cca45c9c2`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91653c31786057dd333e02b9e9f9d82d2b9f24f8dccaed4a17153bd5c2422e52`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 1.3 KB (1282 bytes)  
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
$ docker pull influxdb@sha256:d3314edde16d3b4cd43e8bb0b195720cbbf6c624993d28875b68c0f0aaccb13b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cb3a402ac7574b6e5c60c77f40ac589281a363f2520bb9f903410ce7eb74c9ff
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91705876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065135b1f0ea4c520df6c6f3262a9e5d8ebcee47ffe8a5f70b21f50594bf7306`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:28:23 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 22 Oct 2020 04:28:48 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Thu, 22 Oct 2020 04:29:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 22 Oct 2020 04:29:04 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 22 Oct 2020 04:29:04 GMT
EXPOSE 8086
# Thu, 22 Oct 2020 04:29:04 GMT
VOLUME [/var/lib/influxdb]
# Thu, 22 Oct 2020 04:29:05 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 22 Oct 2020 04:29:05 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 22 Oct 2020 04:29:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Oct 2020 04:29:06 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f09710cb1e9d1e2b329758d6e450a28347bc3d5b9279be1c2f97edf904405`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 1.3 MB (1303321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691475a4c0f221f72a446295525ae32fb33405db9917d047eec7b080a630dfb5`  
		Last Modified: Thu, 22 Oct 2020 04:31:45 GMT  
		Size: 87.6 MB (87603774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6601cb3ece9ced640df833746c0e08be380b725f6588a63414873336afb35ea`  
		Last Modified: Thu, 22 Oct 2020 04:31:31 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ee3d49e2b7dcc574158fa61d2b717f3db120472b0547241174ac320f166d11`  
		Last Modified: Thu, 22 Oct 2020 04:31:30 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8892cd38deb028f934862c3e71787c50f3927223b7b185343883227ea6b22101`  
		Last Modified: Thu, 22 Oct 2020 04:31:30 GMT  
		Size: 1.3 KB (1279 bytes)  
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
$ docker pull influxdb@sha256:b962e0b547dfe71507b7eb58d4d90318b6f73e92f5ecb5b9d0ab9cbd32090d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:08abd4dd2be4dabc8853880a9e4cda89cccdc0e7dd3191646197e4f3a4977d06
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27103600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2b886053cbe0cf5e0392ef620d950c0318f276b8deacb1dc4da2604d311a71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:28:23 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 22 Oct 2020 04:28:48 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Thu, 22 Oct 2020 04:29:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 22 Oct 2020 04:29:25 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 22 Oct 2020 04:29:25 GMT
EXPOSE 8091
# Thu, 22 Oct 2020 04:29:25 GMT
VOLUME [/var/lib/influxdb]
# Thu, 22 Oct 2020 04:29:26 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 22 Oct 2020 04:29:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Oct 2020 04:29:27 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f09710cb1e9d1e2b329758d6e450a28347bc3d5b9279be1c2f97edf904405`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 1.3 MB (1303321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fd0067901c10cf3abc23e6be7aca60cce83e716e6085d57f8ae06c9e0a587`  
		Last Modified: Thu, 22 Oct 2020 04:31:55 GMT  
		Size: 23.0 MB (23002697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7a3f0750d6361cb01d5bc3b0a68d1b3041775acf485aaaca6b982d03a7f3ab`  
		Last Modified: Thu, 22 Oct 2020 04:31:51 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca7a8968c2c25210d62ec34dd8d021340922d52240f827997aefc00fbf26b43`  
		Last Modified: Thu, 22 Oct 2020 04:31:51 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-alpine`

```console
$ docker pull influxdb@sha256:8ca9dcb656fda408443afa6e3dfef8e5e08335427101fdec5caaaef10f2d9cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a6bb057ca821b606f238162dab6d1499ca858caea2bc12260392c793af19fa43
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67943085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b3c3bda5307e814906e9db921e6e571afaed1b617fd1449f1fe441060f818c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:28:23 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 22 Oct 2020 04:28:23 GMT
ENV INFLUXDB_VERSION=1.7.10
# Thu, 22 Oct 2020 04:28:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 22 Oct 2020 04:28:35 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 22 Oct 2020 04:28:35 GMT
EXPOSE 8086
# Thu, 22 Oct 2020 04:28:35 GMT
VOLUME [/var/lib/influxdb]
# Thu, 22 Oct 2020 04:28:36 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 22 Oct 2020 04:28:36 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 22 Oct 2020 04:28:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Oct 2020 04:28:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f09710cb1e9d1e2b329758d6e450a28347bc3d5b9279be1c2f97edf904405`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 1.3 MB (1303321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b51ff1a057029f76ca3d93bf4ade3c0d6c59310622853739f7c473d4d71db57`  
		Last Modified: Thu, 22 Oct 2020 04:31:24 GMT  
		Size: 63.8 MB (63841035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d946660a65bf0b75ad63981bf17617d4a954cc2d2c61c76ee13086a7bf35305`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a085fd5908bfe1eba0d441b84470151d95fceec61695a2cd2693f79cca45c9c2`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91653c31786057dd333e02b9e9f9d82d2b9f24f8dccaed4a17153bd5c2422e52`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 1.3 KB (1282 bytes)  
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
$ docker pull influxdb@sha256:d3314edde16d3b4cd43e8bb0b195720cbbf6c624993d28875b68c0f0aaccb13b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cb3a402ac7574b6e5c60c77f40ac589281a363f2520bb9f903410ce7eb74c9ff
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91705876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065135b1f0ea4c520df6c6f3262a9e5d8ebcee47ffe8a5f70b21f50594bf7306`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:28:23 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 22 Oct 2020 04:28:48 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Thu, 22 Oct 2020 04:29:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 22 Oct 2020 04:29:04 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 22 Oct 2020 04:29:04 GMT
EXPOSE 8086
# Thu, 22 Oct 2020 04:29:04 GMT
VOLUME [/var/lib/influxdb]
# Thu, 22 Oct 2020 04:29:05 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 22 Oct 2020 04:29:05 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 22 Oct 2020 04:29:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Oct 2020 04:29:06 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f09710cb1e9d1e2b329758d6e450a28347bc3d5b9279be1c2f97edf904405`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 1.3 MB (1303321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691475a4c0f221f72a446295525ae32fb33405db9917d047eec7b080a630dfb5`  
		Last Modified: Thu, 22 Oct 2020 04:31:45 GMT  
		Size: 87.6 MB (87603774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6601cb3ece9ced640df833746c0e08be380b725f6588a63414873336afb35ea`  
		Last Modified: Thu, 22 Oct 2020 04:31:31 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ee3d49e2b7dcc574158fa61d2b717f3db120472b0547241174ac320f166d11`  
		Last Modified: Thu, 22 Oct 2020 04:31:30 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8892cd38deb028f934862c3e71787c50f3927223b7b185343883227ea6b22101`  
		Last Modified: Thu, 22 Oct 2020 04:31:30 GMT  
		Size: 1.3 KB (1279 bytes)  
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
$ docker pull influxdb@sha256:b962e0b547dfe71507b7eb58d4d90318b6f73e92f5ecb5b9d0ab9cbd32090d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:08abd4dd2be4dabc8853880a9e4cda89cccdc0e7dd3191646197e4f3a4977d06
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27103600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2b886053cbe0cf5e0392ef620d950c0318f276b8deacb1dc4da2604d311a71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:28:23 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 22 Oct 2020 04:28:48 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Thu, 22 Oct 2020 04:29:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 22 Oct 2020 04:29:25 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 22 Oct 2020 04:29:25 GMT
EXPOSE 8091
# Thu, 22 Oct 2020 04:29:25 GMT
VOLUME [/var/lib/influxdb]
# Thu, 22 Oct 2020 04:29:26 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 22 Oct 2020 04:29:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Oct 2020 04:29:27 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f09710cb1e9d1e2b329758d6e450a28347bc3d5b9279be1c2f97edf904405`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 1.3 MB (1303321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fd0067901c10cf3abc23e6be7aca60cce83e716e6085d57f8ae06c9e0a587`  
		Last Modified: Thu, 22 Oct 2020 04:31:55 GMT  
		Size: 23.0 MB (23002697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7a3f0750d6361cb01d5bc3b0a68d1b3041775acf485aaaca6b982d03a7f3ab`  
		Last Modified: Thu, 22 Oct 2020 04:31:51 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca7a8968c2c25210d62ec34dd8d021340922d52240f827997aefc00fbf26b43`  
		Last Modified: Thu, 22 Oct 2020 04:31:51 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8`

```console
$ docker pull influxdb@sha256:aa5efc36964e969137b47805de0fb3367d83e865ec945f38db729926d4a032ac
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
$ docker pull influxdb@sha256:aa5efc36964e969137b47805de0fb3367d83e865ec945f38db729926d4a032ac
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
$ docker pull influxdb@sha256:fa9c29387c8360d444e5c97c333e506614e86fc06f14c0c95e8b2e3a58a3f20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b22e31d531bfa7252dec3a1c25cf632813e5b875d98720ac50213d50feeb0f23
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68808650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8547609c51108d14614f1352838a0d8d72bd96c56fa9bd5ee72012f05c83daf4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:28:23 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 22 Oct 2020 04:29:36 GMT
ENV INFLUXDB_VERSION=1.8.3
# Thu, 22 Oct 2020 04:29:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 22 Oct 2020 04:29:49 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 22 Oct 2020 04:29:49 GMT
EXPOSE 8086
# Thu, 22 Oct 2020 04:29:49 GMT
VOLUME [/var/lib/influxdb]
# Thu, 22 Oct 2020 04:29:50 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 22 Oct 2020 04:29:50 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 22 Oct 2020 04:29:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Oct 2020 04:29:51 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f09710cb1e9d1e2b329758d6e450a28347bc3d5b9279be1c2f97edf904405`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 1.3 MB (1303321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65afcd077387f3004aa678cd1a97c4ab452ef130c1dabb9379fd8a8ea02bf0c1`  
		Last Modified: Thu, 22 Oct 2020 04:32:12 GMT  
		Size: 64.7 MB (64706602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5ed56e1e804b4e14492088d5cdc079f81cce8c2be7a2f2e2a5a9f1fadbb5d2`  
		Last Modified: Thu, 22 Oct 2020 04:32:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff7ff23b8fd0e2f766fea8d90029c074f251d78186f990af67c6c5d8f58d962`  
		Last Modified: Thu, 22 Oct 2020 04:32:02 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff4a837504c80f785d2225635ef420bb90097f8c3f80b9311949691c26c7912`  
		Last Modified: Thu, 22 Oct 2020 04:32:01 GMT  
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
$ docker pull influxdb@sha256:f7d173e15d6fc0c9ac7c35678ee0dad64aee110184d2f6d024df02f0683a17ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4c1c4fc1fcba7030db3a6ecb9f3e1ec71b2c4ea701ee604e88e08c85ffb87977
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69642956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd86d6b75a3b1cbe226e141409b8e3eee099a1cb8579a0d0ba4671e7d5d2f9e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:28:23 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 22 Oct 2020 04:30:02 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Thu, 22 Oct 2020 04:30:14 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 22 Oct 2020 04:30:15 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 22 Oct 2020 04:30:15 GMT
EXPOSE 8086
# Thu, 22 Oct 2020 04:30:15 GMT
VOLUME [/var/lib/influxdb]
# Thu, 22 Oct 2020 04:30:16 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 22 Oct 2020 04:30:16 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 22 Oct 2020 04:30:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Oct 2020 04:30:17 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f09710cb1e9d1e2b329758d6e450a28347bc3d5b9279be1c2f97edf904405`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 1.3 MB (1303321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ab6db73d4a9305b65e1cb79b5f854615fbac1e876c49861f195e55b70c2bed`  
		Last Modified: Thu, 22 Oct 2020 04:32:29 GMT  
		Size: 65.5 MB (65540847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3593bcff93ebc0496719df41b2d6e370288fb04e554496f829675c8e71144fef`  
		Last Modified: Thu, 22 Oct 2020 04:32:19 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bf060f1ee990128c3b7df2445c1747090139579b1542045f169053d42d0879`  
		Last Modified: Thu, 22 Oct 2020 04:32:19 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9309edcbfe2961f008f1a2b1e86ae658ae5a17b2c3a05e56d87b02842b705820`  
		Last Modified: Thu, 22 Oct 2020 04:32:19 GMT  
		Size: 1.3 KB (1281 bytes)  
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
$ docker pull influxdb@sha256:70f1b7c824ff978cd09deb7298a666d08af5cffdabae3a775ae094100c3d328c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:1a0b1f3ee8a905d2a15396c6db7fcca6d6a64628ff2dc724396058b781cba5d8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26836360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d09e706a7d6ea4d3b2519326e3c10f8f7c066de7883ffb247aa43501ef79694`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:28:23 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 22 Oct 2020 04:30:02 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Thu, 22 Oct 2020 04:30:36 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 22 Oct 2020 04:30:36 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 22 Oct 2020 04:30:36 GMT
EXPOSE 8091
# Thu, 22 Oct 2020 04:30:37 GMT
VOLUME [/var/lib/influxdb]
# Thu, 22 Oct 2020 04:30:37 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 22 Oct 2020 04:30:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Oct 2020 04:30:38 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f09710cb1e9d1e2b329758d6e450a28347bc3d5b9279be1c2f97edf904405`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 1.3 MB (1303321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5e0408288a75aaffef5d1ed0ebecbc6de897c805a773b1b408b466aa9d44f8`  
		Last Modified: Thu, 22 Oct 2020 04:32:58 GMT  
		Size: 22.7 MB (22735457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99edc72327260928d9a712a434891d826ebf86b646c823068077ad3527660e2e`  
		Last Modified: Thu, 22 Oct 2020 04:32:53 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9e43ba683d42003bc67956a1151ce9b3f35ca4257b3fcd81b4c88c42219ee3`  
		Last Modified: Thu, 22 Oct 2020 04:32:54 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-alpine`

```console
$ docker pull influxdb@sha256:fa9c29387c8360d444e5c97c333e506614e86fc06f14c0c95e8b2e3a58a3f20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b22e31d531bfa7252dec3a1c25cf632813e5b875d98720ac50213d50feeb0f23
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68808650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8547609c51108d14614f1352838a0d8d72bd96c56fa9bd5ee72012f05c83daf4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:28:23 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 22 Oct 2020 04:29:36 GMT
ENV INFLUXDB_VERSION=1.8.3
# Thu, 22 Oct 2020 04:29:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 22 Oct 2020 04:29:49 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 22 Oct 2020 04:29:49 GMT
EXPOSE 8086
# Thu, 22 Oct 2020 04:29:49 GMT
VOLUME [/var/lib/influxdb]
# Thu, 22 Oct 2020 04:29:50 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 22 Oct 2020 04:29:50 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 22 Oct 2020 04:29:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Oct 2020 04:29:51 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f09710cb1e9d1e2b329758d6e450a28347bc3d5b9279be1c2f97edf904405`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 1.3 MB (1303321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65afcd077387f3004aa678cd1a97c4ab452ef130c1dabb9379fd8a8ea02bf0c1`  
		Last Modified: Thu, 22 Oct 2020 04:32:12 GMT  
		Size: 64.7 MB (64706602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5ed56e1e804b4e14492088d5cdc079f81cce8c2be7a2f2e2a5a9f1fadbb5d2`  
		Last Modified: Thu, 22 Oct 2020 04:32:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff7ff23b8fd0e2f766fea8d90029c074f251d78186f990af67c6c5d8f58d962`  
		Last Modified: Thu, 22 Oct 2020 04:32:02 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff4a837504c80f785d2225635ef420bb90097f8c3f80b9311949691c26c7912`  
		Last Modified: Thu, 22 Oct 2020 04:32:01 GMT  
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
$ docker pull influxdb@sha256:f7d173e15d6fc0c9ac7c35678ee0dad64aee110184d2f6d024df02f0683a17ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4c1c4fc1fcba7030db3a6ecb9f3e1ec71b2c4ea701ee604e88e08c85ffb87977
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69642956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd86d6b75a3b1cbe226e141409b8e3eee099a1cb8579a0d0ba4671e7d5d2f9e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:28:23 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 22 Oct 2020 04:30:02 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Thu, 22 Oct 2020 04:30:14 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 22 Oct 2020 04:30:15 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 22 Oct 2020 04:30:15 GMT
EXPOSE 8086
# Thu, 22 Oct 2020 04:30:15 GMT
VOLUME [/var/lib/influxdb]
# Thu, 22 Oct 2020 04:30:16 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 22 Oct 2020 04:30:16 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 22 Oct 2020 04:30:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Oct 2020 04:30:17 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f09710cb1e9d1e2b329758d6e450a28347bc3d5b9279be1c2f97edf904405`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 1.3 MB (1303321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ab6db73d4a9305b65e1cb79b5f854615fbac1e876c49861f195e55b70c2bed`  
		Last Modified: Thu, 22 Oct 2020 04:32:29 GMT  
		Size: 65.5 MB (65540847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3593bcff93ebc0496719df41b2d6e370288fb04e554496f829675c8e71144fef`  
		Last Modified: Thu, 22 Oct 2020 04:32:19 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bf060f1ee990128c3b7df2445c1747090139579b1542045f169053d42d0879`  
		Last Modified: Thu, 22 Oct 2020 04:32:19 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9309edcbfe2961f008f1a2b1e86ae658ae5a17b2c3a05e56d87b02842b705820`  
		Last Modified: Thu, 22 Oct 2020 04:32:19 GMT  
		Size: 1.3 KB (1281 bytes)  
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
$ docker pull influxdb@sha256:70f1b7c824ff978cd09deb7298a666d08af5cffdabae3a775ae094100c3d328c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:1a0b1f3ee8a905d2a15396c6db7fcca6d6a64628ff2dc724396058b781cba5d8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26836360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d09e706a7d6ea4d3b2519326e3c10f8f7c066de7883ffb247aa43501ef79694`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:28:23 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 22 Oct 2020 04:30:02 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Thu, 22 Oct 2020 04:30:36 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 22 Oct 2020 04:30:36 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 22 Oct 2020 04:30:36 GMT
EXPOSE 8091
# Thu, 22 Oct 2020 04:30:37 GMT
VOLUME [/var/lib/influxdb]
# Thu, 22 Oct 2020 04:30:37 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 22 Oct 2020 04:30:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Oct 2020 04:30:38 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f09710cb1e9d1e2b329758d6e450a28347bc3d5b9279be1c2f97edf904405`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 1.3 MB (1303321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5e0408288a75aaffef5d1ed0ebecbc6de897c805a773b1b408b466aa9d44f8`  
		Last Modified: Thu, 22 Oct 2020 04:32:58 GMT  
		Size: 22.7 MB (22735457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99edc72327260928d9a712a434891d826ebf86b646c823068077ad3527660e2e`  
		Last Modified: Thu, 22 Oct 2020 04:32:53 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9e43ba683d42003bc67956a1151ce9b3f35ca4257b3fcd81b4c88c42219ee3`  
		Last Modified: Thu, 22 Oct 2020 04:32:54 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:fa9c29387c8360d444e5c97c333e506614e86fc06f14c0c95e8b2e3a58a3f20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b22e31d531bfa7252dec3a1c25cf632813e5b875d98720ac50213d50feeb0f23
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68808650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8547609c51108d14614f1352838a0d8d72bd96c56fa9bd5ee72012f05c83daf4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:28:23 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 22 Oct 2020 04:29:36 GMT
ENV INFLUXDB_VERSION=1.8.3
# Thu, 22 Oct 2020 04:29:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 22 Oct 2020 04:29:49 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 22 Oct 2020 04:29:49 GMT
EXPOSE 8086
# Thu, 22 Oct 2020 04:29:49 GMT
VOLUME [/var/lib/influxdb]
# Thu, 22 Oct 2020 04:29:50 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 22 Oct 2020 04:29:50 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 22 Oct 2020 04:29:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Oct 2020 04:29:51 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f09710cb1e9d1e2b329758d6e450a28347bc3d5b9279be1c2f97edf904405`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 1.3 MB (1303321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65afcd077387f3004aa678cd1a97c4ab452ef130c1dabb9379fd8a8ea02bf0c1`  
		Last Modified: Thu, 22 Oct 2020 04:32:12 GMT  
		Size: 64.7 MB (64706602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5ed56e1e804b4e14492088d5cdc079f81cce8c2be7a2f2e2a5a9f1fadbb5d2`  
		Last Modified: Thu, 22 Oct 2020 04:32:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff7ff23b8fd0e2f766fea8d90029c074f251d78186f990af67c6c5d8f58d962`  
		Last Modified: Thu, 22 Oct 2020 04:32:02 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff4a837504c80f785d2225635ef420bb90097f8c3f80b9311949691c26c7912`  
		Last Modified: Thu, 22 Oct 2020 04:32:01 GMT  
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
$ docker pull influxdb@sha256:f7d173e15d6fc0c9ac7c35678ee0dad64aee110184d2f6d024df02f0683a17ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4c1c4fc1fcba7030db3a6ecb9f3e1ec71b2c4ea701ee604e88e08c85ffb87977
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69642956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd86d6b75a3b1cbe226e141409b8e3eee099a1cb8579a0d0ba4671e7d5d2f9e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:28:23 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 22 Oct 2020 04:30:02 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Thu, 22 Oct 2020 04:30:14 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 22 Oct 2020 04:30:15 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 22 Oct 2020 04:30:15 GMT
EXPOSE 8086
# Thu, 22 Oct 2020 04:30:15 GMT
VOLUME [/var/lib/influxdb]
# Thu, 22 Oct 2020 04:30:16 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 22 Oct 2020 04:30:16 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 22 Oct 2020 04:30:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Oct 2020 04:30:17 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f09710cb1e9d1e2b329758d6e450a28347bc3d5b9279be1c2f97edf904405`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 1.3 MB (1303321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ab6db73d4a9305b65e1cb79b5f854615fbac1e876c49861f195e55b70c2bed`  
		Last Modified: Thu, 22 Oct 2020 04:32:29 GMT  
		Size: 65.5 MB (65540847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3593bcff93ebc0496719df41b2d6e370288fb04e554496f829675c8e71144fef`  
		Last Modified: Thu, 22 Oct 2020 04:32:19 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bf060f1ee990128c3b7df2445c1747090139579b1542045f169053d42d0879`  
		Last Modified: Thu, 22 Oct 2020 04:32:19 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9309edcbfe2961f008f1a2b1e86ae658ae5a17b2c3a05e56d87b02842b705820`  
		Last Modified: Thu, 22 Oct 2020 04:32:19 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull influxdb@sha256:70f1b7c824ff978cd09deb7298a666d08af5cffdabae3a775ae094100c3d328c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:1a0b1f3ee8a905d2a15396c6db7fcca6d6a64628ff2dc724396058b781cba5d8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26836360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d09e706a7d6ea4d3b2519326e3c10f8f7c066de7883ffb247aa43501ef79694`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:28:23 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 22 Oct 2020 04:30:02 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Thu, 22 Oct 2020 04:30:36 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 22 Oct 2020 04:30:36 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 22 Oct 2020 04:30:36 GMT
EXPOSE 8091
# Thu, 22 Oct 2020 04:30:37 GMT
VOLUME [/var/lib/influxdb]
# Thu, 22 Oct 2020 04:30:37 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 22 Oct 2020 04:30:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Oct 2020 04:30:38 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f09710cb1e9d1e2b329758d6e450a28347bc3d5b9279be1c2f97edf904405`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 1.3 MB (1303321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5e0408288a75aaffef5d1ed0ebecbc6de897c805a773b1b408b466aa9d44f8`  
		Last Modified: Thu, 22 Oct 2020 04:32:58 GMT  
		Size: 22.7 MB (22735457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99edc72327260928d9a712a434891d826ebf86b646c823068077ad3527660e2e`  
		Last Modified: Thu, 22 Oct 2020 04:32:53 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9e43ba683d42003bc67956a1151ce9b3f35ca4257b3fcd81b4c88c42219ee3`  
		Last Modified: Thu, 22 Oct 2020 04:32:54 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
