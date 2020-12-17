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
$ docker pull influxdb@sha256:e0765a3201ae335975c338b219ef6c352f25f5f38646def27e5fbfd8f42038a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7` - linux; amd64

```console
$ docker pull influxdb@sha256:b9e6e84158c55556c0b0f056b037fbc16950730f5d20c22b41e578914b285bad
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124572233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3402197ae0c1486b970a1124ca46cc55cab10935d8686ceb1e61227eb72d903b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 12 Dec 2020 10:44:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 12 Dec 2020 10:44:11 GMT
ENV INFLUXDB_VERSION=1.7.10
# Sat, 12 Dec 2020 10:44:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sat, 12 Dec 2020 10:44:17 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sat, 12 Dec 2020 10:44:18 GMT
EXPOSE 8086
# Sat, 12 Dec 2020 10:44:18 GMT
VOLUME [/var/lib/influxdb]
# Sat, 12 Dec 2020 10:44:18 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sat, 12 Dec 2020 10:44:18 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 12 Dec 2020 10:44:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 10:44:19 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52143fc259e4b73720a33197dc8ad31fc672b69f4c15cab3ce194785db33b6c`  
		Last Modified: Sat, 12 Dec 2020 10:46:08 GMT  
		Size: 2.8 KB (2827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f25dd964e08fa82fd691520ed1517ac5f81304121d542f658390a82589a1a0`  
		Last Modified: Sat, 12 Dec 2020 10:46:18 GMT  
		Size: 64.1 MB (64096974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97f09da6e4bdcf2382650abcbe57f49e91838f5fd07075088d660694eb484a2`  
		Last Modified: Sat, 12 Dec 2020 10:46:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f647df58b26af525d00a77c67f685889a99af2ef133311dc835a5227ead9e163`  
		Last Modified: Sat, 12 Dec 2020 10:46:08 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693f76f1bca538eb7da7cdfea932aaadf1b44068ef4ec5cab0e468a72d2bab97`  
		Last Modified: Sat, 12 Dec 2020 10:46:07 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:d2cf55340ea0432b1cfa2f749161a263989d41b70d2caa53d6680cc57359bbaf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116123222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32971a3813b9d9236aeea3d705d75d54a9a5a5a8b742a9dd60edefcead62967`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:28:06 GMT
ADD file:e74dce76704e3faa6198db5cf4192fd431f5addf55f658277eb5b60d254fee8e in / 
# Fri, 11 Dec 2020 02:28:09 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:24:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:24:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 18:03:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 17 Dec 2020 18:03:05 GMT
ENV INFLUXDB_VERSION=1.7.10
# Thu, 17 Dec 2020 18:03:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 17 Dec 2020 18:03:17 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 17 Dec 2020 18:03:17 GMT
EXPOSE 8086
# Thu, 17 Dec 2020 18:03:18 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 18:03:19 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 17 Dec 2020 18:03:20 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 17 Dec 2020 18:03:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 18:03:21 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:062f5403576d7e3aca1c92115ff0a9ea110b270cb0b61013efa86744515666fb`  
		Last Modified: Fri, 11 Dec 2020 02:36:48 GMT  
		Size: 42.1 MB (42117949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913e3a9a9e04d7e4fdefdcc5847233d712c26520bf9484ed8e890f521f2bbf41`  
		Last Modified: Thu, 17 Dec 2020 08:56:01 GMT  
		Size: 9.4 MB (9445217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d26373a692630f7276d1b4be2fc66079b5d68123d5ddc98490cc9a4d0775a31`  
		Last Modified: Thu, 17 Dec 2020 08:56:00 GMT  
		Size: 3.9 MB (3919961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2157c2b8bba08a376eb228f45f5f5dd7676bffee987d469cb623db2daac20660`  
		Last Modified: Thu, 17 Dec 2020 18:04:06 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4f4900ff9c24c09a848d8eebd9a4b4742d986a4a00396955d224f6573e0c2b`  
		Last Modified: Thu, 17 Dec 2020 18:04:22 GMT  
		Size: 60.6 MB (60635522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e12ed4d3144d0d62c3f8b50a3e385b9a568177df352b5bf06731304b4bdac2`  
		Last Modified: Thu, 17 Dec 2020 18:04:07 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf28aefc43fa2fc1268ba373af2dff96118b60178de0d5811f78c255e5724ea`  
		Last Modified: Thu, 17 Dec 2020 18:04:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c5c7f889b2c3967bc81e400ecca02793494f32c799dff713153e504dd4d30b`  
		Last Modified: Thu, 17 Dec 2020 18:04:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d6d11517e7235585eff40bf4b69b6dcc52fd9ba093f654cadfa32f77eb18f19c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117106672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0282426d0ee6b4914cf033416b66e6bbbb06fdd7b257382df33339d6123683e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:48:16 GMT
ADD file:48e44714f486662ed380343e556f0f7411bd6600d916440063753c55d1f94b45 in / 
# Fri, 11 Dec 2020 02:48:17 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 10:13:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 10:13:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 15:25:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 17 Dec 2020 15:25:55 GMT
ENV INFLUXDB_VERSION=1.7.10
# Thu, 17 Dec 2020 15:26:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 17 Dec 2020 15:26:17 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 17 Dec 2020 15:26:28 GMT
EXPOSE 8086
# Thu, 17 Dec 2020 15:26:36 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 15:26:36 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 17 Dec 2020 15:26:38 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 17 Dec 2020 15:26:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 15:26:43 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ecefb91918e846819df74a1beb8e41f454bef156738373818c20656a3a46d5f7`  
		Last Modified: Fri, 11 Dec 2020 02:55:36 GMT  
		Size: 43.2 MB (43175941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9a63f37e7beb33012f80c0f66755ce6d87a51fde0a283a06dbdf2857ce533`  
		Last Modified: Thu, 17 Dec 2020 10:41:45 GMT  
		Size: 9.7 MB (9702906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0c493446fd68c6abee0df0169e849bcb73aa61a86ba5e30783c9b5298007b7`  
		Last Modified: Thu, 17 Dec 2020 10:41:43 GMT  
		Size: 4.1 MB (4095483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a00a8a57199af4c15740e382214257dc71414c8a40b544ffcd0d9f53ce2404c`  
		Last Modified: Thu, 17 Dec 2020 15:27:23 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d88dd8ced803e32c54afaa6262ab6169811fc45acb4b5e968cbdac3cf0bce9`  
		Last Modified: Thu, 17 Dec 2020 15:27:37 GMT  
		Size: 60.1 MB (60127768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07894f945b444bbf8ee411e2392a8dbe778491d1d778b7441035737d6802675`  
		Last Modified: Thu, 17 Dec 2020 15:27:23 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f51f444571a0f64dba2812230df34a24b62e4233f4a7fae5c9e73d3684d6aa6`  
		Last Modified: Thu, 17 Dec 2020 15:27:24 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da68ae98baa462fb810d05bc890fdadc71895cbdae37fdf8874452d7c1907cb`  
		Last Modified: Thu, 17 Dec 2020 15:27:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10`

```console
$ docker pull influxdb@sha256:e0765a3201ae335975c338b219ef6c352f25f5f38646def27e5fbfd8f42038a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7.10` - linux; amd64

```console
$ docker pull influxdb@sha256:b9e6e84158c55556c0b0f056b037fbc16950730f5d20c22b41e578914b285bad
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124572233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3402197ae0c1486b970a1124ca46cc55cab10935d8686ceb1e61227eb72d903b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 12 Dec 2020 10:44:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 12 Dec 2020 10:44:11 GMT
ENV INFLUXDB_VERSION=1.7.10
# Sat, 12 Dec 2020 10:44:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sat, 12 Dec 2020 10:44:17 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sat, 12 Dec 2020 10:44:18 GMT
EXPOSE 8086
# Sat, 12 Dec 2020 10:44:18 GMT
VOLUME [/var/lib/influxdb]
# Sat, 12 Dec 2020 10:44:18 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sat, 12 Dec 2020 10:44:18 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 12 Dec 2020 10:44:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 10:44:19 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52143fc259e4b73720a33197dc8ad31fc672b69f4c15cab3ce194785db33b6c`  
		Last Modified: Sat, 12 Dec 2020 10:46:08 GMT  
		Size: 2.8 KB (2827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f25dd964e08fa82fd691520ed1517ac5f81304121d542f658390a82589a1a0`  
		Last Modified: Sat, 12 Dec 2020 10:46:18 GMT  
		Size: 64.1 MB (64096974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97f09da6e4bdcf2382650abcbe57f49e91838f5fd07075088d660694eb484a2`  
		Last Modified: Sat, 12 Dec 2020 10:46:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f647df58b26af525d00a77c67f685889a99af2ef133311dc835a5227ead9e163`  
		Last Modified: Sat, 12 Dec 2020 10:46:08 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693f76f1bca538eb7da7cdfea932aaadf1b44068ef4ec5cab0e468a72d2bab97`  
		Last Modified: Sat, 12 Dec 2020 10:46:07 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:d2cf55340ea0432b1cfa2f749161a263989d41b70d2caa53d6680cc57359bbaf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116123222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32971a3813b9d9236aeea3d705d75d54a9a5a5a8b742a9dd60edefcead62967`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:28:06 GMT
ADD file:e74dce76704e3faa6198db5cf4192fd431f5addf55f658277eb5b60d254fee8e in / 
# Fri, 11 Dec 2020 02:28:09 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:24:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:24:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 18:03:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 17 Dec 2020 18:03:05 GMT
ENV INFLUXDB_VERSION=1.7.10
# Thu, 17 Dec 2020 18:03:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 17 Dec 2020 18:03:17 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 17 Dec 2020 18:03:17 GMT
EXPOSE 8086
# Thu, 17 Dec 2020 18:03:18 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 18:03:19 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 17 Dec 2020 18:03:20 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 17 Dec 2020 18:03:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 18:03:21 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:062f5403576d7e3aca1c92115ff0a9ea110b270cb0b61013efa86744515666fb`  
		Last Modified: Fri, 11 Dec 2020 02:36:48 GMT  
		Size: 42.1 MB (42117949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913e3a9a9e04d7e4fdefdcc5847233d712c26520bf9484ed8e890f521f2bbf41`  
		Last Modified: Thu, 17 Dec 2020 08:56:01 GMT  
		Size: 9.4 MB (9445217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d26373a692630f7276d1b4be2fc66079b5d68123d5ddc98490cc9a4d0775a31`  
		Last Modified: Thu, 17 Dec 2020 08:56:00 GMT  
		Size: 3.9 MB (3919961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2157c2b8bba08a376eb228f45f5f5dd7676bffee987d469cb623db2daac20660`  
		Last Modified: Thu, 17 Dec 2020 18:04:06 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4f4900ff9c24c09a848d8eebd9a4b4742d986a4a00396955d224f6573e0c2b`  
		Last Modified: Thu, 17 Dec 2020 18:04:22 GMT  
		Size: 60.6 MB (60635522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e12ed4d3144d0d62c3f8b50a3e385b9a568177df352b5bf06731304b4bdac2`  
		Last Modified: Thu, 17 Dec 2020 18:04:07 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf28aefc43fa2fc1268ba373af2dff96118b60178de0d5811f78c255e5724ea`  
		Last Modified: Thu, 17 Dec 2020 18:04:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c5c7f889b2c3967bc81e400ecca02793494f32c799dff713153e504dd4d30b`  
		Last Modified: Thu, 17 Dec 2020 18:04:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d6d11517e7235585eff40bf4b69b6dcc52fd9ba093f654cadfa32f77eb18f19c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117106672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0282426d0ee6b4914cf033416b66e6bbbb06fdd7b257382df33339d6123683e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:48:16 GMT
ADD file:48e44714f486662ed380343e556f0f7411bd6600d916440063753c55d1f94b45 in / 
# Fri, 11 Dec 2020 02:48:17 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 10:13:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 10:13:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 15:25:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 17 Dec 2020 15:25:55 GMT
ENV INFLUXDB_VERSION=1.7.10
# Thu, 17 Dec 2020 15:26:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 17 Dec 2020 15:26:17 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 17 Dec 2020 15:26:28 GMT
EXPOSE 8086
# Thu, 17 Dec 2020 15:26:36 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 15:26:36 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 17 Dec 2020 15:26:38 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 17 Dec 2020 15:26:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 15:26:43 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ecefb91918e846819df74a1beb8e41f454bef156738373818c20656a3a46d5f7`  
		Last Modified: Fri, 11 Dec 2020 02:55:36 GMT  
		Size: 43.2 MB (43175941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9a63f37e7beb33012f80c0f66755ce6d87a51fde0a283a06dbdf2857ce533`  
		Last Modified: Thu, 17 Dec 2020 10:41:45 GMT  
		Size: 9.7 MB (9702906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0c493446fd68c6abee0df0169e849bcb73aa61a86ba5e30783c9b5298007b7`  
		Last Modified: Thu, 17 Dec 2020 10:41:43 GMT  
		Size: 4.1 MB (4095483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a00a8a57199af4c15740e382214257dc71414c8a40b544ffcd0d9f53ce2404c`  
		Last Modified: Thu, 17 Dec 2020 15:27:23 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d88dd8ced803e32c54afaa6262ab6169811fc45acb4b5e968cbdac3cf0bce9`  
		Last Modified: Thu, 17 Dec 2020 15:27:37 GMT  
		Size: 60.1 MB (60127768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07894f945b444bbf8ee411e2392a8dbe778491d1d778b7441035737d6802675`  
		Last Modified: Thu, 17 Dec 2020 15:27:23 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f51f444571a0f64dba2812230df34a24b62e4233f4a7fae5c9e73d3684d6aa6`  
		Last Modified: Thu, 17 Dec 2020 15:27:24 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da68ae98baa462fb810d05bc890fdadc71895cbdae37fdf8874452d7c1907cb`  
		Last Modified: Thu, 17 Dec 2020 15:27:23 GMT  
		Size: 1.3 KB (1281 bytes)  
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
$ docker pull influxdb@sha256:0c58300ee62bb73e9f0fd533399d3ee439017a8edfb9508c79401be41a13837b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:b47beaf774ed160f9574c29ea28b050c1d3b56b8456eafb117010367b35063b0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148387662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6017f1c475a96177aae3ac7442c390c1fe88633ff21c99fd4b595a060be8136a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 12 Dec 2020 10:44:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 12 Dec 2020 10:44:28 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Sat, 12 Dec 2020 10:44:36 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Sat, 12 Dec 2020 10:44:37 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 12 Dec 2020 10:44:37 GMT
EXPOSE 8086
# Sat, 12 Dec 2020 10:44:37 GMT
VOLUME [/var/lib/influxdb]
# Sat, 12 Dec 2020 10:44:37 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 12 Dec 2020 10:44:37 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 12 Dec 2020 10:44:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 10:44:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52143fc259e4b73720a33197dc8ad31fc672b69f4c15cab3ce194785db33b6c`  
		Last Modified: Sat, 12 Dec 2020 10:46:08 GMT  
		Size: 2.8 KB (2827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9f8fb7358bcd87898bded841d26fe75e8fee16fdf05ecbda42e34f72edbf52`  
		Last Modified: Sat, 12 Dec 2020 10:46:48 GMT  
		Size: 87.9 MB (87912341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e387b334b06a50bd3e21c79457b97be26bd1e921cdf73e652ca70cf1e7cd7ce1`  
		Last Modified: Sat, 12 Dec 2020 10:46:25 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca47a219f28a092960e10bb25306cee8457850535a059aefa746aaa741d87c7e`  
		Last Modified: Sat, 12 Dec 2020 10:46:24 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1e0bde1351e6f18352f7445af4d4543931b263e3cc9a7fcafcd79ff815fa9f`  
		Last Modified: Sat, 12 Dec 2020 10:46:24 GMT  
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
$ docker pull influxdb@sha256:e34df0e12ba970ae8d88f10d00a54489e756e03906623d6496728b1d4cf54906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:3b8261fabefbaec7495a60535d9bc197ee74f37229748cf13a916d8771f5bd8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83606764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4d50a5c3d9c236961fca2b48b21cce6501917cd0795cf70085bc61b160e1c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 12 Dec 2020 10:44:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 12 Dec 2020 10:44:28 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Sat, 12 Dec 2020 10:44:50 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Sat, 12 Dec 2020 10:44:50 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 12 Dec 2020 10:44:50 GMT
EXPOSE 8091
# Sat, 12 Dec 2020 10:44:50 GMT
VOLUME [/var/lib/influxdb]
# Sat, 12 Dec 2020 10:44:51 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 12 Dec 2020 10:44:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 10:44:51 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52143fc259e4b73720a33197dc8ad31fc672b69f4c15cab3ce194785db33b6c`  
		Last Modified: Sat, 12 Dec 2020 10:46:08 GMT  
		Size: 2.8 KB (2827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5ed2b2708b8f0f41b7abf3c936ec078470755fd4760def51da417b9d3b59b4`  
		Last Modified: Sat, 12 Dec 2020 10:46:58 GMT  
		Size: 23.1 MB (23132648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165b07e67464fa03aa05632a1c9d92f886b079f8fbbc89c992db19a1556b0913`  
		Last Modified: Sat, 12 Dec 2020 10:46:54 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2100a7a206c23e87c61c5ae6eb251cae5a83521037b415bb6eb7035a8afbfe9d`  
		Last Modified: Sat, 12 Dec 2020 10:46:54 GMT  
		Size: 375.0 B  
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
$ docker pull influxdb@sha256:0c58300ee62bb73e9f0fd533399d3ee439017a8edfb9508c79401be41a13837b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:b47beaf774ed160f9574c29ea28b050c1d3b56b8456eafb117010367b35063b0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148387662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6017f1c475a96177aae3ac7442c390c1fe88633ff21c99fd4b595a060be8136a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 12 Dec 2020 10:44:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 12 Dec 2020 10:44:28 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Sat, 12 Dec 2020 10:44:36 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Sat, 12 Dec 2020 10:44:37 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 12 Dec 2020 10:44:37 GMT
EXPOSE 8086
# Sat, 12 Dec 2020 10:44:37 GMT
VOLUME [/var/lib/influxdb]
# Sat, 12 Dec 2020 10:44:37 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 12 Dec 2020 10:44:37 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 12 Dec 2020 10:44:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 10:44:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52143fc259e4b73720a33197dc8ad31fc672b69f4c15cab3ce194785db33b6c`  
		Last Modified: Sat, 12 Dec 2020 10:46:08 GMT  
		Size: 2.8 KB (2827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9f8fb7358bcd87898bded841d26fe75e8fee16fdf05ecbda42e34f72edbf52`  
		Last Modified: Sat, 12 Dec 2020 10:46:48 GMT  
		Size: 87.9 MB (87912341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e387b334b06a50bd3e21c79457b97be26bd1e921cdf73e652ca70cf1e7cd7ce1`  
		Last Modified: Sat, 12 Dec 2020 10:46:25 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca47a219f28a092960e10bb25306cee8457850535a059aefa746aaa741d87c7e`  
		Last Modified: Sat, 12 Dec 2020 10:46:24 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1e0bde1351e6f18352f7445af4d4543931b263e3cc9a7fcafcd79ff815fa9f`  
		Last Modified: Sat, 12 Dec 2020 10:46:24 GMT  
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
$ docker pull influxdb@sha256:e34df0e12ba970ae8d88f10d00a54489e756e03906623d6496728b1d4cf54906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:3b8261fabefbaec7495a60535d9bc197ee74f37229748cf13a916d8771f5bd8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83606764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4d50a5c3d9c236961fca2b48b21cce6501917cd0795cf70085bc61b160e1c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 12 Dec 2020 10:44:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 12 Dec 2020 10:44:28 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Sat, 12 Dec 2020 10:44:50 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Sat, 12 Dec 2020 10:44:50 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 12 Dec 2020 10:44:50 GMT
EXPOSE 8091
# Sat, 12 Dec 2020 10:44:50 GMT
VOLUME [/var/lib/influxdb]
# Sat, 12 Dec 2020 10:44:51 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 12 Dec 2020 10:44:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 10:44:51 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52143fc259e4b73720a33197dc8ad31fc672b69f4c15cab3ce194785db33b6c`  
		Last Modified: Sat, 12 Dec 2020 10:46:08 GMT  
		Size: 2.8 KB (2827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5ed2b2708b8f0f41b7abf3c936ec078470755fd4760def51da417b9d3b59b4`  
		Last Modified: Sat, 12 Dec 2020 10:46:58 GMT  
		Size: 23.1 MB (23132648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165b07e67464fa03aa05632a1c9d92f886b079f8fbbc89c992db19a1556b0913`  
		Last Modified: Sat, 12 Dec 2020 10:46:54 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2100a7a206c23e87c61c5ae6eb251cae5a83521037b415bb6eb7035a8afbfe9d`  
		Last Modified: Sat, 12 Dec 2020 10:46:54 GMT  
		Size: 375.0 B  
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
$ docker pull influxdb@sha256:20254c5366edc77d918bcbb52fca3d24bbacf51b051666a0147907ce66f8356b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8` - linux; amd64

```console
$ docker pull influxdb@sha256:30271ac251a457f5ab9cebc67f1b2df22b2edff8c4092ecfccc2ca4383a921aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125441191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29fe242c193ddafb9228f31a6dbde083c5997e9a6ca2038b50600a4fb5baa6a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 12 Dec 2020 10:44:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 12 Dec 2020 10:44:59 GMT
ENV INFLUXDB_VERSION=1.8.3
# Sat, 12 Dec 2020 10:45:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sat, 12 Dec 2020 10:45:05 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sat, 12 Dec 2020 10:45:05 GMT
EXPOSE 8086
# Sat, 12 Dec 2020 10:45:05 GMT
VOLUME [/var/lib/influxdb]
# Sat, 12 Dec 2020 10:45:06 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sat, 12 Dec 2020 10:45:06 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 12 Dec 2020 10:45:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 10:45:06 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52143fc259e4b73720a33197dc8ad31fc672b69f4c15cab3ce194785db33b6c`  
		Last Modified: Sat, 12 Dec 2020 10:46:08 GMT  
		Size: 2.8 KB (2827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e0dbfc9f2cbbb62ab9347244de54c009ab3ad700adf6327c4a615fa152e4f8`  
		Last Modified: Sat, 12 Dec 2020 10:47:15 GMT  
		Size: 65.0 MB (64965927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5980bdfb50a414e3ad5b456940d145430ae25efdfc42fc048a551e238204130`  
		Last Modified: Sat, 12 Dec 2020 10:47:05 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e480e68ce4c588bc2494b8633984da4dc0176167a217d4a67c94620056fdd7`  
		Last Modified: Sat, 12 Dec 2020 10:47:05 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e61efff46e61b9050bcde8133a416fd5d5c904575af9449f1ee215e0389466`  
		Last Modified: Sat, 12 Dec 2020 10:47:05 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:ea2ffb95fa78ddc47361fe394dc541abce72b44fb83093087b3a4f7f816d3759
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116545058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb68637c2e1d038094ba319bbb88ea47b29ba2d847ffd367e5a7067e19c2f23d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:28:06 GMT
ADD file:e74dce76704e3faa6198db5cf4192fd431f5addf55f658277eb5b60d254fee8e in / 
# Fri, 11 Dec 2020 02:28:09 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:24:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:24:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 18:03:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 17 Dec 2020 18:03:31 GMT
ENV INFLUXDB_VERSION=1.8.3
# Thu, 17 Dec 2020 18:03:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 17 Dec 2020 18:03:45 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 17 Dec 2020 18:03:46 GMT
EXPOSE 8086
# Thu, 17 Dec 2020 18:03:47 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 18:03:47 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 17 Dec 2020 18:03:48 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 17 Dec 2020 18:03:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 18:03:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:062f5403576d7e3aca1c92115ff0a9ea110b270cb0b61013efa86744515666fb`  
		Last Modified: Fri, 11 Dec 2020 02:36:48 GMT  
		Size: 42.1 MB (42117949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913e3a9a9e04d7e4fdefdcc5847233d712c26520bf9484ed8e890f521f2bbf41`  
		Last Modified: Thu, 17 Dec 2020 08:56:01 GMT  
		Size: 9.4 MB (9445217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d26373a692630f7276d1b4be2fc66079b5d68123d5ddc98490cc9a4d0775a31`  
		Last Modified: Thu, 17 Dec 2020 08:56:00 GMT  
		Size: 3.9 MB (3919961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2157c2b8bba08a376eb228f45f5f5dd7676bffee987d469cb623db2daac20660`  
		Last Modified: Thu, 17 Dec 2020 18:04:06 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc92a3808658dfd307f131d1e1c78f77a0b26c44f1aa6cf13f4ada71bf58776`  
		Last Modified: Thu, 17 Dec 2020 18:04:47 GMT  
		Size: 61.1 MB (61057360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a021a88132b01df915db6536c894d380e0f51eaae6eceee3b235ed941c8bcb3`  
		Last Modified: Thu, 17 Dec 2020 18:04:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db2cd5b7dcedc4a793c5f9de0107f6d67c51adfdabb6cf3fde7f3cf3b38c6e3`  
		Last Modified: Thu, 17 Dec 2020 18:04:30 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6521e61a052ade242ca9448aff8b1c4a2acc5e9bf99aca83f3b49a9e48e42e4`  
		Last Modified: Thu, 17 Dec 2020 18:04:29 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:116afd3662c995818965acbc3f515851eb8b59b081852ee633b6516d83a343bd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117605732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83e931cfa467a4db3127999749502aa87a922ddb52333257a88cfe89e012dde`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:48:16 GMT
ADD file:48e44714f486662ed380343e556f0f7411bd6600d916440063753c55d1f94b45 in / 
# Fri, 11 Dec 2020 02:48:17 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 10:13:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 10:13:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 15:25:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 17 Dec 2020 15:26:52 GMT
ENV INFLUXDB_VERSION=1.8.3
# Thu, 17 Dec 2020 15:27:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 17 Dec 2020 15:27:02 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 17 Dec 2020 15:27:03 GMT
EXPOSE 8086
# Thu, 17 Dec 2020 15:27:03 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 15:27:04 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 17 Dec 2020 15:27:05 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 17 Dec 2020 15:27:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 15:27:07 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ecefb91918e846819df74a1beb8e41f454bef156738373818c20656a3a46d5f7`  
		Last Modified: Fri, 11 Dec 2020 02:55:36 GMT  
		Size: 43.2 MB (43175941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9a63f37e7beb33012f80c0f66755ce6d87a51fde0a283a06dbdf2857ce533`  
		Last Modified: Thu, 17 Dec 2020 10:41:45 GMT  
		Size: 9.7 MB (9702906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0c493446fd68c6abee0df0169e849bcb73aa61a86ba5e30783c9b5298007b7`  
		Last Modified: Thu, 17 Dec 2020 10:41:43 GMT  
		Size: 4.1 MB (4095483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a00a8a57199af4c15740e382214257dc71414c8a40b544ffcd0d9f53ce2404c`  
		Last Modified: Thu, 17 Dec 2020 15:27:23 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ed1589af262d0f6104eceb471392d09eff5421d4669f06e2c9054545965652`  
		Last Modified: Thu, 17 Dec 2020 15:27:58 GMT  
		Size: 60.6 MB (60626832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4054772c2c83698fb81c7e810b3698c46ad0ee08ad658c2d70ab1481f90ca177`  
		Last Modified: Thu, 17 Dec 2020 15:27:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0f7491941e8bc9638ce33e93b5d9e88ace69570e4a88ca8f0d2a2125969333`  
		Last Modified: Thu, 17 Dec 2020 15:27:45 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db28bc4ec64e21181ce4865c49ef34edec20ff9c09a4166fd920a2fe64950ebc`  
		Last Modified: Thu, 17 Dec 2020 15:27:45 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3`

```console
$ docker pull influxdb@sha256:20254c5366edc77d918bcbb52fca3d24bbacf51b051666a0147907ce66f8356b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8.3` - linux; amd64

```console
$ docker pull influxdb@sha256:30271ac251a457f5ab9cebc67f1b2df22b2edff8c4092ecfccc2ca4383a921aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125441191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29fe242c193ddafb9228f31a6dbde083c5997e9a6ca2038b50600a4fb5baa6a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 12 Dec 2020 10:44:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 12 Dec 2020 10:44:59 GMT
ENV INFLUXDB_VERSION=1.8.3
# Sat, 12 Dec 2020 10:45:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sat, 12 Dec 2020 10:45:05 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sat, 12 Dec 2020 10:45:05 GMT
EXPOSE 8086
# Sat, 12 Dec 2020 10:45:05 GMT
VOLUME [/var/lib/influxdb]
# Sat, 12 Dec 2020 10:45:06 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sat, 12 Dec 2020 10:45:06 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 12 Dec 2020 10:45:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 10:45:06 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52143fc259e4b73720a33197dc8ad31fc672b69f4c15cab3ce194785db33b6c`  
		Last Modified: Sat, 12 Dec 2020 10:46:08 GMT  
		Size: 2.8 KB (2827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e0dbfc9f2cbbb62ab9347244de54c009ab3ad700adf6327c4a615fa152e4f8`  
		Last Modified: Sat, 12 Dec 2020 10:47:15 GMT  
		Size: 65.0 MB (64965927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5980bdfb50a414e3ad5b456940d145430ae25efdfc42fc048a551e238204130`  
		Last Modified: Sat, 12 Dec 2020 10:47:05 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e480e68ce4c588bc2494b8633984da4dc0176167a217d4a67c94620056fdd7`  
		Last Modified: Sat, 12 Dec 2020 10:47:05 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e61efff46e61b9050bcde8133a416fd5d5c904575af9449f1ee215e0389466`  
		Last Modified: Sat, 12 Dec 2020 10:47:05 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.3` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:ea2ffb95fa78ddc47361fe394dc541abce72b44fb83093087b3a4f7f816d3759
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116545058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb68637c2e1d038094ba319bbb88ea47b29ba2d847ffd367e5a7067e19c2f23d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:28:06 GMT
ADD file:e74dce76704e3faa6198db5cf4192fd431f5addf55f658277eb5b60d254fee8e in / 
# Fri, 11 Dec 2020 02:28:09 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:24:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:24:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 18:03:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 17 Dec 2020 18:03:31 GMT
ENV INFLUXDB_VERSION=1.8.3
# Thu, 17 Dec 2020 18:03:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 17 Dec 2020 18:03:45 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 17 Dec 2020 18:03:46 GMT
EXPOSE 8086
# Thu, 17 Dec 2020 18:03:47 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 18:03:47 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 17 Dec 2020 18:03:48 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 17 Dec 2020 18:03:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 18:03:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:062f5403576d7e3aca1c92115ff0a9ea110b270cb0b61013efa86744515666fb`  
		Last Modified: Fri, 11 Dec 2020 02:36:48 GMT  
		Size: 42.1 MB (42117949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913e3a9a9e04d7e4fdefdcc5847233d712c26520bf9484ed8e890f521f2bbf41`  
		Last Modified: Thu, 17 Dec 2020 08:56:01 GMT  
		Size: 9.4 MB (9445217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d26373a692630f7276d1b4be2fc66079b5d68123d5ddc98490cc9a4d0775a31`  
		Last Modified: Thu, 17 Dec 2020 08:56:00 GMT  
		Size: 3.9 MB (3919961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2157c2b8bba08a376eb228f45f5f5dd7676bffee987d469cb623db2daac20660`  
		Last Modified: Thu, 17 Dec 2020 18:04:06 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc92a3808658dfd307f131d1e1c78f77a0b26c44f1aa6cf13f4ada71bf58776`  
		Last Modified: Thu, 17 Dec 2020 18:04:47 GMT  
		Size: 61.1 MB (61057360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a021a88132b01df915db6536c894d380e0f51eaae6eceee3b235ed941c8bcb3`  
		Last Modified: Thu, 17 Dec 2020 18:04:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db2cd5b7dcedc4a793c5f9de0107f6d67c51adfdabb6cf3fde7f3cf3b38c6e3`  
		Last Modified: Thu, 17 Dec 2020 18:04:30 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6521e61a052ade242ca9448aff8b1c4a2acc5e9bf99aca83f3b49a9e48e42e4`  
		Last Modified: Thu, 17 Dec 2020 18:04:29 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.3` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:116afd3662c995818965acbc3f515851eb8b59b081852ee633b6516d83a343bd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117605732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83e931cfa467a4db3127999749502aa87a922ddb52333257a88cfe89e012dde`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:48:16 GMT
ADD file:48e44714f486662ed380343e556f0f7411bd6600d916440063753c55d1f94b45 in / 
# Fri, 11 Dec 2020 02:48:17 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 10:13:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 10:13:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 15:25:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 17 Dec 2020 15:26:52 GMT
ENV INFLUXDB_VERSION=1.8.3
# Thu, 17 Dec 2020 15:27:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 17 Dec 2020 15:27:02 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 17 Dec 2020 15:27:03 GMT
EXPOSE 8086
# Thu, 17 Dec 2020 15:27:03 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 15:27:04 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 17 Dec 2020 15:27:05 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 17 Dec 2020 15:27:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 15:27:07 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ecefb91918e846819df74a1beb8e41f454bef156738373818c20656a3a46d5f7`  
		Last Modified: Fri, 11 Dec 2020 02:55:36 GMT  
		Size: 43.2 MB (43175941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9a63f37e7beb33012f80c0f66755ce6d87a51fde0a283a06dbdf2857ce533`  
		Last Modified: Thu, 17 Dec 2020 10:41:45 GMT  
		Size: 9.7 MB (9702906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0c493446fd68c6abee0df0169e849bcb73aa61a86ba5e30783c9b5298007b7`  
		Last Modified: Thu, 17 Dec 2020 10:41:43 GMT  
		Size: 4.1 MB (4095483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a00a8a57199af4c15740e382214257dc71414c8a40b544ffcd0d9f53ce2404c`  
		Last Modified: Thu, 17 Dec 2020 15:27:23 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ed1589af262d0f6104eceb471392d09eff5421d4669f06e2c9054545965652`  
		Last Modified: Thu, 17 Dec 2020 15:27:58 GMT  
		Size: 60.6 MB (60626832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4054772c2c83698fb81c7e810b3698c46ad0ee08ad658c2d70ab1481f90ca177`  
		Last Modified: Thu, 17 Dec 2020 15:27:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0f7491941e8bc9638ce33e93b5d9e88ace69570e4a88ca8f0d2a2125969333`  
		Last Modified: Thu, 17 Dec 2020 15:27:45 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db28bc4ec64e21181ce4865c49ef34edec20ff9c09a4166fd920a2fe64950ebc`  
		Last Modified: Thu, 17 Dec 2020 15:27:45 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-alpine`

```console
$ docker pull influxdb@sha256:65cb0a80cab9744a2892c9720867fdbd1a61784529c599fd37105893d8a6a6e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2f73472a38b0fadb41399fcd111877b762b9088fe891e4060ae842c9a3c0e4ed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68935837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d626945ed3abd9dc0fefe18c4f2334be0c05873ffc296139c902819fccdb51`
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
# Thu, 17 Dec 2020 13:48:13 GMT
ENV INFLUXDB_VERSION=1.8.3
# Thu, 17 Dec 2020 13:48:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:48:23 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 17 Dec 2020 13:48:23 GMT
EXPOSE 8086
# Thu, 17 Dec 2020 13:48:23 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 13:48:23 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 17 Dec 2020 13:48:23 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 17 Dec 2020 13:48:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:48:24 GMT
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
	-	`sha256:0c12eb60e6cd81240f7cfece2cd78c24800a82105bb0ccc15d8f108a11b392ed`  
		Last Modified: Thu, 17 Dec 2020 13:50:49 GMT  
		Size: 64.7 MB (64706606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f99d25b1ceb07bd2d7e2314d83eff49e3838acc35cc1b8fad1e4e758087d10`  
		Last Modified: Thu, 17 Dec 2020 13:50:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52690e3b2d969a7bc60dc1b366d40383d4f1573e778c8d9f4643ba117afa24f`  
		Last Modified: Thu, 17 Dec 2020 13:50:31 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3383a0f6861a3a14514428c363a8d2acfc4ab75797c887d79458cb7708641d`  
		Last Modified: Thu, 17 Dec 2020 13:50:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-data`

```console
$ docker pull influxdb@sha256:17c152781f79e762c6ff916c50c350314ab629c9fad112f3b9a646b4b867b88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-data` - linux; amd64

```console
$ docker pull influxdb@sha256:0535236ca2503becbca56f95688a94389c06ec60f8aa81d1645412b3e7065ba5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126271301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fe5f00b333e8528dd79522bbdb9d6168a04e894ccb1d2a9ee8e21dcc9f07d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 12 Dec 2020 10:44:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 12 Dec 2020 10:45:15 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Sat, 12 Dec 2020 10:45:21 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Sat, 12 Dec 2020 10:45:21 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 12 Dec 2020 10:45:21 GMT
EXPOSE 8086
# Sat, 12 Dec 2020 10:45:22 GMT
VOLUME [/var/lib/influxdb]
# Sat, 12 Dec 2020 10:45:22 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 12 Dec 2020 10:45:22 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 12 Dec 2020 10:45:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 10:45:22 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52143fc259e4b73720a33197dc8ad31fc672b69f4c15cab3ce194785db33b6c`  
		Last Modified: Sat, 12 Dec 2020 10:46:08 GMT  
		Size: 2.8 KB (2827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4752551edf8f31717a9d36ea2b1a5cbb87a37020d23f4a9b05ceef409f96a8db`  
		Last Modified: Sat, 12 Dec 2020 10:47:33 GMT  
		Size: 65.8 MB (65795981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbac50fd96ae4c96aaf3849abf7baa57b908e506e1c5b880f7431127de5dd0df`  
		Last Modified: Sat, 12 Dec 2020 10:47:23 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973cfe04b02e27c6bcd22f43b07f91faeae3897a94802bd6ebc0aec776f6a095`  
		Last Modified: Sat, 12 Dec 2020 10:47:22 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbc929eec87d2c6bec3fdd7ea1fd0de6f21ce291d7f20bc9079f4a9ee452935`  
		Last Modified: Sat, 12 Dec 2020 10:47:22 GMT  
		Size: 1.3 KB (1281 bytes)  
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
$ docker pull influxdb@sha256:2885d1ccfd9065aaa8ec9b442a4fe51907fc8518e8cd0e51f575bd67186d6ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:ce877705e6ce4b71a1764a66a82c4039927d444967091305054434218d405593
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83339388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00a9a69b9de7864fb916e34a4d7c89f6ece61a691925e6a818da15db05e9e24`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 12 Dec 2020 10:44:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 12 Dec 2020 10:45:15 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Sat, 12 Dec 2020 10:45:34 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Sat, 12 Dec 2020 10:45:34 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 12 Dec 2020 10:45:34 GMT
EXPOSE 8091
# Sat, 12 Dec 2020 10:45:34 GMT
VOLUME [/var/lib/influxdb]
# Sat, 12 Dec 2020 10:45:34 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 12 Dec 2020 10:45:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 10:45:35 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52143fc259e4b73720a33197dc8ad31fc672b69f4c15cab3ce194785db33b6c`  
		Last Modified: Sat, 12 Dec 2020 10:46:08 GMT  
		Size: 2.8 KB (2827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab8a5bbfc61aefc83113c2fb974853bff285b5d106ac4ae620d12cbfb3b4383`  
		Last Modified: Sat, 12 Dec 2020 10:47:44 GMT  
		Size: 22.9 MB (22865274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b63a02f20a5a667ef49fb2ea64a94abac70f554d57661f12f4d4a0f1e9c481c`  
		Last Modified: Sat, 12 Dec 2020 10:47:41 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99836980a2af3a49c33e50d5cdfa5a2180b74fab991c2038c591e9bdfe6f828`  
		Last Modified: Sat, 12 Dec 2020 10:47:41 GMT  
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

## `influxdb:1.8-alpine`

```console
$ docker pull influxdb@sha256:65cb0a80cab9744a2892c9720867fdbd1a61784529c599fd37105893d8a6a6e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2f73472a38b0fadb41399fcd111877b762b9088fe891e4060ae842c9a3c0e4ed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68935837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d626945ed3abd9dc0fefe18c4f2334be0c05873ffc296139c902819fccdb51`
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
# Thu, 17 Dec 2020 13:48:13 GMT
ENV INFLUXDB_VERSION=1.8.3
# Thu, 17 Dec 2020 13:48:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:48:23 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 17 Dec 2020 13:48:23 GMT
EXPOSE 8086
# Thu, 17 Dec 2020 13:48:23 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 13:48:23 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 17 Dec 2020 13:48:23 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 17 Dec 2020 13:48:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:48:24 GMT
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
	-	`sha256:0c12eb60e6cd81240f7cfece2cd78c24800a82105bb0ccc15d8f108a11b392ed`  
		Last Modified: Thu, 17 Dec 2020 13:50:49 GMT  
		Size: 64.7 MB (64706606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f99d25b1ceb07bd2d7e2314d83eff49e3838acc35cc1b8fad1e4e758087d10`  
		Last Modified: Thu, 17 Dec 2020 13:50:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52690e3b2d969a7bc60dc1b366d40383d4f1573e778c8d9f4643ba117afa24f`  
		Last Modified: Thu, 17 Dec 2020 13:50:31 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3383a0f6861a3a14514428c363a8d2acfc4ab75797c887d79458cb7708641d`  
		Last Modified: Thu, 17 Dec 2020 13:50:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data`

```console
$ docker pull influxdb@sha256:17c152781f79e762c6ff916c50c350314ab629c9fad112f3b9a646b4b867b88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:0535236ca2503becbca56f95688a94389c06ec60f8aa81d1645412b3e7065ba5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126271301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fe5f00b333e8528dd79522bbdb9d6168a04e894ccb1d2a9ee8e21dcc9f07d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 12 Dec 2020 10:44:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 12 Dec 2020 10:45:15 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Sat, 12 Dec 2020 10:45:21 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Sat, 12 Dec 2020 10:45:21 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 12 Dec 2020 10:45:21 GMT
EXPOSE 8086
# Sat, 12 Dec 2020 10:45:22 GMT
VOLUME [/var/lib/influxdb]
# Sat, 12 Dec 2020 10:45:22 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 12 Dec 2020 10:45:22 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 12 Dec 2020 10:45:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 10:45:22 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52143fc259e4b73720a33197dc8ad31fc672b69f4c15cab3ce194785db33b6c`  
		Last Modified: Sat, 12 Dec 2020 10:46:08 GMT  
		Size: 2.8 KB (2827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4752551edf8f31717a9d36ea2b1a5cbb87a37020d23f4a9b05ceef409f96a8db`  
		Last Modified: Sat, 12 Dec 2020 10:47:33 GMT  
		Size: 65.8 MB (65795981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbac50fd96ae4c96aaf3849abf7baa57b908e506e1c5b880f7431127de5dd0df`  
		Last Modified: Sat, 12 Dec 2020 10:47:23 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973cfe04b02e27c6bcd22f43b07f91faeae3897a94802bd6ebc0aec776f6a095`  
		Last Modified: Sat, 12 Dec 2020 10:47:22 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbc929eec87d2c6bec3fdd7ea1fd0de6f21ce291d7f20bc9079f4a9ee452935`  
		Last Modified: Sat, 12 Dec 2020 10:47:22 GMT  
		Size: 1.3 KB (1281 bytes)  
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
$ docker pull influxdb@sha256:2885d1ccfd9065aaa8ec9b442a4fe51907fc8518e8cd0e51f575bd67186d6ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:ce877705e6ce4b71a1764a66a82c4039927d444967091305054434218d405593
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83339388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00a9a69b9de7864fb916e34a4d7c89f6ece61a691925e6a818da15db05e9e24`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 12 Dec 2020 10:44:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 12 Dec 2020 10:45:15 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Sat, 12 Dec 2020 10:45:34 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Sat, 12 Dec 2020 10:45:34 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 12 Dec 2020 10:45:34 GMT
EXPOSE 8091
# Sat, 12 Dec 2020 10:45:34 GMT
VOLUME [/var/lib/influxdb]
# Sat, 12 Dec 2020 10:45:34 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 12 Dec 2020 10:45:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 10:45:35 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52143fc259e4b73720a33197dc8ad31fc672b69f4c15cab3ce194785db33b6c`  
		Last Modified: Sat, 12 Dec 2020 10:46:08 GMT  
		Size: 2.8 KB (2827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab8a5bbfc61aefc83113c2fb974853bff285b5d106ac4ae620d12cbfb3b4383`  
		Last Modified: Sat, 12 Dec 2020 10:47:44 GMT  
		Size: 22.9 MB (22865274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b63a02f20a5a667ef49fb2ea64a94abac70f554d57661f12f4d4a0f1e9c481c`  
		Last Modified: Sat, 12 Dec 2020 10:47:41 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99836980a2af3a49c33e50d5cdfa5a2180b74fab991c2038c591e9bdfe6f828`  
		Last Modified: Sat, 12 Dec 2020 10:47:41 GMT  
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

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:65cb0a80cab9744a2892c9720867fdbd1a61784529c599fd37105893d8a6a6e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2f73472a38b0fadb41399fcd111877b762b9088fe891e4060ae842c9a3c0e4ed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68935837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d626945ed3abd9dc0fefe18c4f2334be0c05873ffc296139c902819fccdb51`
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
# Thu, 17 Dec 2020 13:48:13 GMT
ENV INFLUXDB_VERSION=1.8.3
# Thu, 17 Dec 2020 13:48:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:48:23 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 17 Dec 2020 13:48:23 GMT
EXPOSE 8086
# Thu, 17 Dec 2020 13:48:23 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 13:48:23 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 17 Dec 2020 13:48:23 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 17 Dec 2020 13:48:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:48:24 GMT
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
	-	`sha256:0c12eb60e6cd81240f7cfece2cd78c24800a82105bb0ccc15d8f108a11b392ed`  
		Last Modified: Thu, 17 Dec 2020 13:50:49 GMT  
		Size: 64.7 MB (64706606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f99d25b1ceb07bd2d7e2314d83eff49e3838acc35cc1b8fad1e4e758087d10`  
		Last Modified: Thu, 17 Dec 2020 13:50:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52690e3b2d969a7bc60dc1b366d40383d4f1573e778c8d9f4643ba117afa24f`  
		Last Modified: Thu, 17 Dec 2020 13:50:31 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3383a0f6861a3a14514428c363a8d2acfc4ab75797c887d79458cb7708641d`  
		Last Modified: Thu, 17 Dec 2020 13:50:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data`

```console
$ docker pull influxdb@sha256:17c152781f79e762c6ff916c50c350314ab629c9fad112f3b9a646b4b867b88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:0535236ca2503becbca56f95688a94389c06ec60f8aa81d1645412b3e7065ba5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126271301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fe5f00b333e8528dd79522bbdb9d6168a04e894ccb1d2a9ee8e21dcc9f07d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 12 Dec 2020 10:44:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 12 Dec 2020 10:45:15 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Sat, 12 Dec 2020 10:45:21 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Sat, 12 Dec 2020 10:45:21 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 12 Dec 2020 10:45:21 GMT
EXPOSE 8086
# Sat, 12 Dec 2020 10:45:22 GMT
VOLUME [/var/lib/influxdb]
# Sat, 12 Dec 2020 10:45:22 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 12 Dec 2020 10:45:22 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 12 Dec 2020 10:45:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 10:45:22 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52143fc259e4b73720a33197dc8ad31fc672b69f4c15cab3ce194785db33b6c`  
		Last Modified: Sat, 12 Dec 2020 10:46:08 GMT  
		Size: 2.8 KB (2827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4752551edf8f31717a9d36ea2b1a5cbb87a37020d23f4a9b05ceef409f96a8db`  
		Last Modified: Sat, 12 Dec 2020 10:47:33 GMT  
		Size: 65.8 MB (65795981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbac50fd96ae4c96aaf3849abf7baa57b908e506e1c5b880f7431127de5dd0df`  
		Last Modified: Sat, 12 Dec 2020 10:47:23 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973cfe04b02e27c6bcd22f43b07f91faeae3897a94802bd6ebc0aec776f6a095`  
		Last Modified: Sat, 12 Dec 2020 10:47:22 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbc929eec87d2c6bec3fdd7ea1fd0de6f21ce291d7f20bc9079f4a9ee452935`  
		Last Modified: Sat, 12 Dec 2020 10:47:22 GMT  
		Size: 1.3 KB (1281 bytes)  
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
$ docker pull influxdb@sha256:20254c5366edc77d918bcbb52fca3d24bbacf51b051666a0147907ce66f8356b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:30271ac251a457f5ab9cebc67f1b2df22b2edff8c4092ecfccc2ca4383a921aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125441191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29fe242c193ddafb9228f31a6dbde083c5997e9a6ca2038b50600a4fb5baa6a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 12 Dec 2020 10:44:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 12 Dec 2020 10:44:59 GMT
ENV INFLUXDB_VERSION=1.8.3
# Sat, 12 Dec 2020 10:45:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sat, 12 Dec 2020 10:45:05 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sat, 12 Dec 2020 10:45:05 GMT
EXPOSE 8086
# Sat, 12 Dec 2020 10:45:05 GMT
VOLUME [/var/lib/influxdb]
# Sat, 12 Dec 2020 10:45:06 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sat, 12 Dec 2020 10:45:06 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 12 Dec 2020 10:45:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 10:45:06 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52143fc259e4b73720a33197dc8ad31fc672b69f4c15cab3ce194785db33b6c`  
		Last Modified: Sat, 12 Dec 2020 10:46:08 GMT  
		Size: 2.8 KB (2827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e0dbfc9f2cbbb62ab9347244de54c009ab3ad700adf6327c4a615fa152e4f8`  
		Last Modified: Sat, 12 Dec 2020 10:47:15 GMT  
		Size: 65.0 MB (64965927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5980bdfb50a414e3ad5b456940d145430ae25efdfc42fc048a551e238204130`  
		Last Modified: Sat, 12 Dec 2020 10:47:05 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e480e68ce4c588bc2494b8633984da4dc0176167a217d4a67c94620056fdd7`  
		Last Modified: Sat, 12 Dec 2020 10:47:05 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e61efff46e61b9050bcde8133a416fd5d5c904575af9449f1ee215e0389466`  
		Last Modified: Sat, 12 Dec 2020 10:47:05 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:ea2ffb95fa78ddc47361fe394dc541abce72b44fb83093087b3a4f7f816d3759
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116545058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb68637c2e1d038094ba319bbb88ea47b29ba2d847ffd367e5a7067e19c2f23d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:28:06 GMT
ADD file:e74dce76704e3faa6198db5cf4192fd431f5addf55f658277eb5b60d254fee8e in / 
# Fri, 11 Dec 2020 02:28:09 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:24:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:24:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 18:03:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 17 Dec 2020 18:03:31 GMT
ENV INFLUXDB_VERSION=1.8.3
# Thu, 17 Dec 2020 18:03:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 17 Dec 2020 18:03:45 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 17 Dec 2020 18:03:46 GMT
EXPOSE 8086
# Thu, 17 Dec 2020 18:03:47 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 18:03:47 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 17 Dec 2020 18:03:48 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 17 Dec 2020 18:03:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 18:03:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:062f5403576d7e3aca1c92115ff0a9ea110b270cb0b61013efa86744515666fb`  
		Last Modified: Fri, 11 Dec 2020 02:36:48 GMT  
		Size: 42.1 MB (42117949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913e3a9a9e04d7e4fdefdcc5847233d712c26520bf9484ed8e890f521f2bbf41`  
		Last Modified: Thu, 17 Dec 2020 08:56:01 GMT  
		Size: 9.4 MB (9445217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d26373a692630f7276d1b4be2fc66079b5d68123d5ddc98490cc9a4d0775a31`  
		Last Modified: Thu, 17 Dec 2020 08:56:00 GMT  
		Size: 3.9 MB (3919961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2157c2b8bba08a376eb228f45f5f5dd7676bffee987d469cb623db2daac20660`  
		Last Modified: Thu, 17 Dec 2020 18:04:06 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc92a3808658dfd307f131d1e1c78f77a0b26c44f1aa6cf13f4ada71bf58776`  
		Last Modified: Thu, 17 Dec 2020 18:04:47 GMT  
		Size: 61.1 MB (61057360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a021a88132b01df915db6536c894d380e0f51eaae6eceee3b235ed941c8bcb3`  
		Last Modified: Thu, 17 Dec 2020 18:04:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db2cd5b7dcedc4a793c5f9de0107f6d67c51adfdabb6cf3fde7f3cf3b38c6e3`  
		Last Modified: Thu, 17 Dec 2020 18:04:30 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6521e61a052ade242ca9448aff8b1c4a2acc5e9bf99aca83f3b49a9e48e42e4`  
		Last Modified: Thu, 17 Dec 2020 18:04:29 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:116afd3662c995818965acbc3f515851eb8b59b081852ee633b6516d83a343bd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117605732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83e931cfa467a4db3127999749502aa87a922ddb52333257a88cfe89e012dde`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 11 Dec 2020 02:48:16 GMT
ADD file:48e44714f486662ed380343e556f0f7411bd6600d916440063753c55d1f94b45 in / 
# Fri, 11 Dec 2020 02:48:17 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 10:13:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 10:13:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 15:25:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 17 Dec 2020 15:26:52 GMT
ENV INFLUXDB_VERSION=1.8.3
# Thu, 17 Dec 2020 15:27:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 17 Dec 2020 15:27:02 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 17 Dec 2020 15:27:03 GMT
EXPOSE 8086
# Thu, 17 Dec 2020 15:27:03 GMT
VOLUME [/var/lib/influxdb]
# Thu, 17 Dec 2020 15:27:04 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 17 Dec 2020 15:27:05 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 17 Dec 2020 15:27:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 15:27:07 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ecefb91918e846819df74a1beb8e41f454bef156738373818c20656a3a46d5f7`  
		Last Modified: Fri, 11 Dec 2020 02:55:36 GMT  
		Size: 43.2 MB (43175941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9a63f37e7beb33012f80c0f66755ce6d87a51fde0a283a06dbdf2857ce533`  
		Last Modified: Thu, 17 Dec 2020 10:41:45 GMT  
		Size: 9.7 MB (9702906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0c493446fd68c6abee0df0169e849bcb73aa61a86ba5e30783c9b5298007b7`  
		Last Modified: Thu, 17 Dec 2020 10:41:43 GMT  
		Size: 4.1 MB (4095483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a00a8a57199af4c15740e382214257dc71414c8a40b544ffcd0d9f53ce2404c`  
		Last Modified: Thu, 17 Dec 2020 15:27:23 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ed1589af262d0f6104eceb471392d09eff5421d4669f06e2c9054545965652`  
		Last Modified: Thu, 17 Dec 2020 15:27:58 GMT  
		Size: 60.6 MB (60626832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4054772c2c83698fb81c7e810b3698c46ad0ee08ad658c2d70ab1481f90ca177`  
		Last Modified: Thu, 17 Dec 2020 15:27:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0f7491941e8bc9638ce33e93b5d9e88ace69570e4a88ca8f0d2a2125969333`  
		Last Modified: Thu, 17 Dec 2020 15:27:45 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db28bc4ec64e21181ce4865c49ef34edec20ff9c09a4166fd920a2fe64950ebc`  
		Last Modified: Thu, 17 Dec 2020 15:27:45 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:2885d1ccfd9065aaa8ec9b442a4fe51907fc8518e8cd0e51f575bd67186d6ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:ce877705e6ce4b71a1764a66a82c4039927d444967091305054434218d405593
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83339388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00a9a69b9de7864fb916e34a4d7c89f6ece61a691925e6a818da15db05e9e24`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 12 Dec 2020 10:44:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 12 Dec 2020 10:45:15 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Sat, 12 Dec 2020 10:45:34 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Sat, 12 Dec 2020 10:45:34 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 12 Dec 2020 10:45:34 GMT
EXPOSE 8091
# Sat, 12 Dec 2020 10:45:34 GMT
VOLUME [/var/lib/influxdb]
# Sat, 12 Dec 2020 10:45:34 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 12 Dec 2020 10:45:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 10:45:35 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52143fc259e4b73720a33197dc8ad31fc672b69f4c15cab3ce194785db33b6c`  
		Last Modified: Sat, 12 Dec 2020 10:46:08 GMT  
		Size: 2.8 KB (2827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab8a5bbfc61aefc83113c2fb974853bff285b5d106ac4ae620d12cbfb3b4383`  
		Last Modified: Sat, 12 Dec 2020 10:47:44 GMT  
		Size: 22.9 MB (22865274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b63a02f20a5a667ef49fb2ea64a94abac70f554d57661f12f4d4a0f1e9c481c`  
		Last Modified: Sat, 12 Dec 2020 10:47:41 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99836980a2af3a49c33e50d5cdfa5a2180b74fab991c2038c591e9bdfe6f828`  
		Last Modified: Sat, 12 Dec 2020 10:47:41 GMT  
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
