<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spiped`

-	[`spiped:1`](#spiped1)
-	[`spiped:1-alpine`](#spiped1-alpine)
-	[`spiped:1.6`](#spiped16)
-	[`spiped:1.6-alpine`](#spiped16-alpine)
-	[`spiped:1.6.2`](#spiped162)
-	[`spiped:1.6.2-alpine`](#spiped162-alpine)
-	[`spiped:alpine`](#spipedalpine)
-	[`spiped:latest`](#spipedlatest)

## `spiped:1`

```console
$ docker pull spiped@sha256:2725f394d1c055b793a69764c862103d5fbd88a70531a3ed67a000071fd9b698
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1` - linux; amd64

```console
$ docker pull spiped@sha256:0807efe8e57e7a74993be6066b8c4d4917a1f6e3611dd0833309a2f48e69d189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37086272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43af49e196ea5b3803a09fb654b9f3a31809b1d63db50efadc92753d2a5ea1b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb387415fb818a8b4d56b6c4b1981b2212e57ec6addac3a80cfb2b9d9331b50`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228fe3a70b06fc8ca22481663a32d8b20b71b4a1cc2ef6bad63851b3cddc6a02`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 2.4 MB (2401340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bdc698a91b053c8c6c8793884aeb21f069855e2f35ceaf6d354563a622ec60`  
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 6.5 MB (6470976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562950f9b4e1da298d9932319a15c677ac7b1072f4a6218a62318ec083a438bf`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d26d7b3a2a6d5bfa2d8845580756d251c7acbb85868393a8dc4b15857a936c`  
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:4596a995a081e15712ce75ccbd6382c0362bbb99730c9b479c48fb6deb3de184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb27c549da9cd3fd74e3b201a56fe8440fe2368fbba1fa80abc7dac9262ff93`

```dockerfile
```

-	Layers:
	-	`sha256:d833741283a7f0cc036493894e91aa8f599339f065480034207be52408751f12`  
		Last Modified: Tue, 14 Jan 2025 23:04:24 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab16c690e615571a539221290f9c7154ed500a5de18d47dfbe3d130daff486f`  
		Last Modified: Tue, 14 Jan 2025 23:04:24 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:7ac314027d6a9a74b545bac6a566bab81092bc05f703e8e7feb689f1156a5820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32873874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f112ee2db55ec556284a0e51dab6d903a978b3e1a2817a609a226b6b833092`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 20:33:17 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d02c24549d50cc08f67dd0716935f9fa89992a0a0c1150357bba3bd55a0c1e7`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3c5e73b2f407694f10795c56fde8bcb539c9e2933731585f42dca1b1ace55f`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
		Size: 2.0 MB (1997177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a7e5af36cc87bcf1b73581be95f889fec6304edf80fae57e11543596a65d0b`  
		Last Modified: Tue, 14 Jan 2025 06:07:50 GMT  
		Size: 5.1 MB (5138490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecae1535903b4c1e77ac1ed96f21bd16112f406ad7f1531a331a8cd8bfcfa55`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff755cd6a71e19c14b557cb2ed1fe6c253d3a1f3539ecd08e66d6407b67d9ab5`  
		Last Modified: Tue, 14 Jan 2025 06:07:50 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:5550758ca3d10700c01f4a5f7e2dcc5e0a8bc81017e7a77563cc9e9d98b07ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc4f32a396e255a44a51de0250cbf8899e01021fdaf2877d4c981165ff96278`

```dockerfile
```

-	Layers:
	-	`sha256:2dfe195d70effae453580ecf74321962ef95b82e15bb2544354013d50bebb18b`  
		Last Modified: Tue, 14 Jan 2025 23:04:26 GMT  
		Size: 3.5 MB (3486344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d991ae0cd962a40b1a96f846b396fb35fb42d45ca1a7ffa955e1720f73fa9707`  
		Last Modified: Tue, 14 Jan 2025 23:04:28 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:cf5df2fe01fb9d92b1e5cb28bada0fa5ec279ec78e62c0ee49cc27a8baa06bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30652158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542aca3ffd11814f62e05ff8668c4fb3dff51d8dc3c1db06624b08d47f8f1980`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8717c624029ee40d56a1c31652eaf6ccf71a5567d7758a126900c0de1bcfad4`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b317980174023f6d6d78a005ee029285173f59fce3edc99c447ab905dfd179`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 1.9 MB (1855562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c382dfc5377b730c1b9c7edaff5880dda394c11f91a13f8946755dc7d81cf6d`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 4.9 MB (4880456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6267a4e0459f5d1157f3859e3edbabf7657d48de59e6c177fd3d1cf9114f73`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d786240c1a6e6bbdfc3fe94803ef3170f1198c85e7bb159452e0e2e512d162c`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:d9ba01708f3467414bc4781b45309ee70543bcfbd71a0484cedea151e2068d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3500977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f868daab95ccaa02d7e27af7666f2f1a087ae16fae21fbde97f5bd395594bb6`

```dockerfile
```

-	Layers:
	-	`sha256:8ce0204d70a42133258f980adb2349457dbdb8f72be802bed32e6bb1e0e0ddd5`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 3.5 MB (3485835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a0ec541bf556f8901ffbee01629c3a659a0f7db4cc58f578ffad9de316eb6cf`  
		Last Modified: Tue, 14 Jan 2025 23:04:29 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:ca50c1b1c64713d8110875a1f34775fc38040451acc500447a3622392bf2769f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35770669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772b7d61276d94b67963fb9f20b85927c2b84f7a0f63253fa64d274982b1f130`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3d076ceae3499abc00492adc7b101408d72437a499e4a9cea20964e90c3765`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0214df3970acd6fea09000d0df47a3cee908490cd9b760e15bd23ad7aa3cf552`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 2.2 MB (2247012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2354092ea972f14ee9af251fc4714c734d8cd2c30834f655c2ea396610489655`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 5.5 MB (5481085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d572dacd78b347329872172960cc26ce37ee9b7ac42a83ddc7425ad149add9cb`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e699072832a75d28646bc8d1b28f5ee412affda7e0b1e8469893f897fc236810`  
		Last Modified: Tue, 14 Jan 2025 06:38:45 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:d900c3ed70ec4adfcdeddd4771c0e2f9759b1cae7127b1122c5a54e1c910a28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3283792d48abf7c1421ee1439a40dfbe273c495208c163da83ef6da25092911b`

```dockerfile
```

-	Layers:
	-	`sha256:44d25165467985f6f9d9cf10d0306bed5af4e2ad6406371dc516b77fdf3a2ff3`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 3.5 MB (3487042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec8b87f83866e1f34c08767b42d87be6e439e3737291318890b05e17f026397a`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:50dc383a39b7bbf8bc7274000476568ef19f00fa47f5e77a3b945e542d602e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37529245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff3adfb5bcb041fd776f222523c7e5f7d316c3a84275c48f8a469520e3cf670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9757c47c7f65469fabaf649c24c76e71b0ee344186b7378388e73b9ff3584956`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41f696ea1cea6b748d59acb3f0e93feb73a67b208dc03bdd8d489b78b8c4c1c`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 2.4 MB (2398649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241faa93dbe7603d3ddfe8143dbc5f7e9990a80036efae46f8147ce9b8e684d7`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 5.9 MB (5941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac324e1750c72f49ee4d4c3b000ae242266e9e9b1946584a5a221c6d4b01bbe9`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f5c66d701ad1b4e0469df5595f673c4d111557d936709a7c5ab15e2ca0f378`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:78318e0a0bae94e38b3a5d9c7578f6751580c7038fd2e2660d4d7cc768105076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed705c7a2f1d4214425c51ed536dd3d3ab550dfbe9a1b50c38de8bba85e59791`

```dockerfile
```

-	Layers:
	-	`sha256:b0eb158509e496490a1fa281c429ec733f8201538a8ead508644c888a4a09018`  
		Last Modified: Tue, 14 Jan 2025 23:04:35 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e8230d3f815bb664e5eda60129ff633bc7d34854e10e52903d538454410d33`  
		Last Modified: Tue, 14 Jan 2025 23:04:35 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:c01ffa398018e931ac10ce62e16a6625947a0fcc8a2293eade003a3c6b3ab862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36132905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fb4e4e2a5078ea045150d8177a114a04293312c91ebd35e93cb59f1e2259e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 20:36:28 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252230c34678f565279955a422dad63275a16eeef208147f154e13e5647df2ed`  
		Last Modified: Tue, 14 Jan 2025 18:08:24 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f980dd5eb6de9195670967164c2a6d21dfc4bd270afc766fc82f7303fcea879a`  
		Last Modified: Tue, 14 Jan 2025 18:08:25 GMT  
		Size: 1.8 MB (1841121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fde05de7416ebc2e722610c9c2dc2ff46e18c6ef77c23e6e4dd9dcee7c809c4`  
		Last Modified: Tue, 14 Jan 2025 18:08:25 GMT  
		Size: 5.8 MB (5803593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7fe7c8e4867db382a8bf9a5c5bbd8cf77ba59015bd2dae591763292f1a7687`  
		Last Modified: Tue, 14 Jan 2025 18:08:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2345d9838a2e18ef7406ff0df0a5dedb563ffa5c105d7e69074a1599a12e35b8`  
		Last Modified: Tue, 14 Jan 2025 18:08:25 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:ac952f287cc93e8b3d1962734d5e6d7b7fea48269365cd58ff092baa9691aba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8839767e2b373c2b310dd1f060d29a21907bda9cf88c7ee7eb3bfea9d99af4c6`

```dockerfile
```

-	Layers:
	-	`sha256:edffc4065fe5a50cf43009afbdb9c8d5dc04651bc8b0abafa3baa3ed0ff073d3`  
		Last Modified: Tue, 14 Jan 2025 23:04:36 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:e0838362e10a88cedb5ebf5d4c38e86e979cb384e1bf72965f8839333fa63baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41051304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5145bd62627fce56a871970f71c1423bf8e7bd302f8e8c8cfdb7a4c492dce6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048adc09f28a34691cbfb26824234082fe589f23a9fa178a80bd0a97e36157ae`  
		Last Modified: Tue, 14 Jan 2025 05:12:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06163a828f03667776915ff22220e1c76e276331d5b5553d9d91f54f6e1b0be2`  
		Last Modified: Tue, 14 Jan 2025 05:13:00 GMT  
		Size: 2.6 MB (2582093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4e996ae8bb5769e51b9acf136d0daaec2939316030203ad6bfa9ee6e82658b`  
		Last Modified: Tue, 14 Jan 2025 05:13:00 GMT  
		Size: 6.4 MB (6422823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204877fb93a1bb0e23eefae6b5ecafcb745cca605fc4e56d05cf862c4f46ec06`  
		Last Modified: Tue, 14 Jan 2025 05:12:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ff3d47eee1c6ccd068d483c63d368a7a6b63c65285cc05761b023d365b9eb0`  
		Last Modified: Tue, 14 Jan 2025 05:13:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:2ac6faef580387afaac65a40852917553101f4b0bd349432d9fae7c1c34b8b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01442cee26b43c9b5f0e98561c25f1d8a7533dccea7b29f16318d0dbffb52a81`

```dockerfile
```

-	Layers:
	-	`sha256:07a1d36ee150774030a74edfb128021444921e2d3eff9710baf6e3a2539c33a2`  
		Last Modified: Tue, 14 Jan 2025 05:13:00 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e46605f5ae9d418c541c83eef4a80f85ac8f32ef307ca58ccab597614e90e0d5`  
		Last Modified: Tue, 14 Jan 2025 23:04:40 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:9a8b4589f022b01cb7379216c0ed4bcfd689c1534d89e1ba7feaaf8c2c7335b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34314999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bb0a694ef3ab84e988bb522551da84d245aa5de9bff71d4e174d5dee08f88b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de4963ba94159da6a677e9693e16f2aaca6406d4426d738af27c3ecc011e85e`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d01390fd75845fd56420f30cd57336b2c75946123f8fdef738b1ee09427359`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 2.1 MB (2068686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef25b97e48209f7c51f7ab797e7c2c9e939b8a05b5b8ca73c14e1c82838fcb22`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 5.4 MB (5386034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4f625a2f5c5cca8030def5f775ae31a6cc2f0f701ad190da0d260c82eb52cb`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fcd0f24724877817587b4569325c3d96d4f4f24e77572ca3f0ec447e622d0d`  
		Last Modified: Tue, 14 Jan 2025 04:49:48 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:cb0a11a3acd5c8d5fc548066b9664c5a715152b3f4999ee92005b77403c1a49e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b3f9cad8e646fdb0c0e919133c2cc5c6481b885ce2db546e37c5d2ff97e85a`

```dockerfile
```

-	Layers:
	-	`sha256:77bf42cd7e49ab8b25190be2a4044d6e977c9ddd06f1f4c7fcd6acb450e8e53b`  
		Last Modified: Tue, 14 Jan 2025 23:04:41 GMT  
		Size: 3.5 MB (3504000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf76c9e1d84fed3f30cb373ece1c7713dffbb1a40bd4018101999d0b899e9f72`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:3defbc7042c9287d78d336478981bdf2410928e48fd8a9504755509633620376
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:924e7f71ff8a6210c218250cadec128119d344f463da73b7435727f3b79f8b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3860004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002ee6ce7d381016e688df520b2d8e452892442cc9dd7d7fe4f2fd27e10bd9cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4d648a75810ee71e4a811a07ea0f0ac2c721e73e72187e9a1516d4c4c5ee6f`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe07a72f4be9ce0f108da046cf545981624f6b49403d76321af17c0c395f286d`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda92c005435cc07d0f9aeede336b39adeacb3d2b63892bd145844c2ffdee52b`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 224.8 KB (224801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d408faf96bb5ca591f0228176fd9fe8fcadf008b4a1d270852fc8c6e4ba93ef1`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e29defa7a55825f8f61eda130cb04ee394d66bd712f70709ac7053a248548`  
		Last Modified: Wed, 08 Jan 2025 18:12:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:bbb6e45e7eb3500533fd5eb9b6e02cbb71696097c25c94d70ad5011ff89719b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ed9b89a1c4bf4f119be92f17b9244feb5432b0aa95a99a543b91711e64d2ff`

```dockerfile
```

-	Layers:
	-	`sha256:d6dbec5f27c384596dd421778e731d1e085e3759f6d847458fe59a756fb7ac42`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 74.1 KB (74096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb9a321a7ee93632ee08168238d08c393bd8977dc0b90058743b7578fd3ffc57`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3b33305e723d928de0ceb007a192d635fbcead1966adcef42495013c151ab1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3908b8302a74d29d2ba4f9fad53ec5dae4d694c59ef5e425f9d3b4ae6f8e82c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Tue, 14 Jan 2025 20:34:27 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af3f0630555eb148818822fb59b573ef21353f360d8de1a31a9d923807ee4cd`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779a48568101672a32588570e7ceef7c0674397cbfa25ee720cde2859ab94873`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 7.5 KB (7549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a21818ff816934f603fcd2d4cba9f12db282bab07e3069da21d7578259ccec`  
		Last Modified: Wed, 08 Jan 2025 21:50:17 GMT  
		Size: 209.4 KB (209360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908425f61ccde4470882b7fc3250f120af7e457373de37561ca1bc2c428156fb`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d99959ccf8e07e46905c21480b4a1efde735673420d31417427ecef2146095`  
		Last Modified: Wed, 08 Jan 2025 21:50:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b7cb53f249d979d695f81563768605e871ddd1ea8a0819dd8dd81dc4987a573f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755f963c27fded64f7e3f6ff08da27dc1fd056f8030a81de4cb41f27e65d037b`

```dockerfile
```

-	Layers:
	-	`sha256:696c936ae51f846bce7be1a6d2dde5c03aa3b71ffda41e1e6b2cf2a621f6cd97`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 14.2 KB (14189 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ae8dad9afbb0cc8a3d199d4f081244152b6bb25a314d1c1b53d2015cb7a3148c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3307454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4e1533dc661a40478a134b3fe58301335db42d8f87ae18e6918ff38e81ae91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Tue, 14 Jan 2025 20:45:20 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7fdb315d3c34eb6935e1b7deb703093f5317800ff4d8b3936d5f771137cb79`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3360ef971eae752027c0ac2e924cac0c91b7f45b5099026b2a8f4be3279f6b5`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70480e7090e82ed5e217b413501ec1d1ac188d14349be7aa351d6ebc4bfa572b`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 203.0 KB (202981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa024b8e7a4dcd96a95ba7c408a6b6bf086e89742d975c9ce4fdfcfc7cabc1b`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4350bd55dee2c6c0b00a05b33f36a79b911cbfa491acf490c5bdc593d8e3e547`  
		Last Modified: Wed, 08 Jan 2025 21:55:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:374da430416cd603b6845710a7b6b98de8856fb9d596f167daa655438d68910f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfb7685b3853e3be4a1172afeae58a3bd43dbc7f6bf21565a8d6843e6b79559`

```dockerfile
```

-	Layers:
	-	`sha256:d4af9f6a3307489ccc6bd25b80644c322c26bf5739a42dab919b2dc03edff9ab`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 74.1 KB (74132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d585d482698adea511246e8d288a1602e3c63dc4f235cfa0915b12ae4b080f64`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:3565ca7a9021c033aa2f9aa3fa95ec43241003635fa8669990453c55ff55e1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa0a984328f7027e356ee0aa46ff85666d4fdeec5eb2d5343a30a9dbe998445`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f2d3fc3adfdd301f5e24f24c5392b9879a1b61f182e7752a21cb03e6aeb04`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d972687789bff098d9b33d09c024319254bdf8dcd29abb2bf072809733c79f49`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37195bfd737aa3f22ef0dd56d792afbe7e88b9c83db3bf0e69cb557d04d0d152`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 219.5 KB (219522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9420b682506ca5859fc3f4af6d59a5ca6fb329a69a869e8d7d0766374eb87ae7`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f38e672eaca427117d78c3580183cebdd51913b95165f7a4fecbb7219aeb29`  
		Last Modified: Wed, 08 Jan 2025 22:06:49 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c1545d907101296a82932a434f77b80a720493d1f158f28037a360c849c6b869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af58e3c42e72d2f836cf482efb095b5869000f90e0fd8c744622051f65cbeb6`

```dockerfile
```

-	Layers:
	-	`sha256:802dad5a525c4dc8453a7af1d74e5f8e0f8e9db9e0b53075b1abb70ebcbcac58`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 74.2 KB (74152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31d587a383d8f42361fc2623919a7a23e16261c7eb1f51cb4aa140497be4935`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:92342ba21763b953dae5124e2470d7b310cdec0e1aa1c278c715dda9eb6c5a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a710174a0b36bde4dc08b5531a97264b1a956e7b607e3cb81fa4ed42446333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01646177e05c873338d049d0058c8cd923326812215a3897564adbd669ee56f`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf3460ecbeac950e26287d1cf9fdf47918bf993988d851835f852bbd5707856`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69044b34b50595fbdc42e577dc79e206d3962968154ec6fbf18024dfe607c6cd`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 235.4 KB (235383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2fe84ec006ef02b90eb19d8de0f72b59b1f5d3cad78ef6d043f1ea320d121`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8feb2512bb10b2b05cf6ac1f623ac53ae1aaaf4d759aa98618bf0a96439d0c`  
		Last Modified: Wed, 08 Jan 2025 18:07:24 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f82eea4e46a614570a5475a2c2999ebdb44416593095c39bfe597dfb70954205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 KB (88337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c43d43c6b18f013ddf9e79c05395cc1213c96194b62e9231a34602566ed737c`

```dockerfile
```

-	Layers:
	-	`sha256:662bb99fc24ff68d14f1e276dc7da9f11ef9f56131659d2a511578d1c4547a4e`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 74.1 KB (74071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab4679badb23f30ba84ac1e7ab274f8693e730ac87dbfac78c97707c071c360`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:62a8529f4a88431c2c8453c2198b9f19f5027af08967a818ceb2e9f5485a2d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3806729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b6428f7bf466f0e03b157ec2507c547f21126e87e9b2e288213771e8ccfd2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d50e862e95a905933f50b6440c968976a25afd06a9808138b7b662be556076`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca1e9dba23dfea2ee87d2657bcd8e5e57a74b668b777c31cdf12a5a688c9e23`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b2864e003337f2f79f0ebbd5d8f47c821a711805de5ac4aac9a3f02a5d06b3`  
		Last Modified: Wed, 08 Jan 2025 21:29:15 GMT  
		Size: 223.4 KB (223364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b04a1708fbc0147d4ef6fdeb564449a7a41b7b0e5df2aa27a1441946c81598c`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66b8e9453e2d649488c8d053b0d1d4ae5e3740489586c6bb32f7eae7a3ec003`  
		Last Modified: Wed, 08 Jan 2025 21:29:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:641f93fddb6e6a668353356d78a708a17b7271ab06e13c5d2d1645d499c65794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1511f0eb48159856515b99abf8dee3e56263f52094148ce660d713454d210ec3`

```dockerfile
```

-	Layers:
	-	`sha256:55e5c3dc4287df2df2d9e20c08f5cd46d57a5616350e241f492bf844c18956d1`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 72.2 KB (72179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f348d15a848da4a767fe70750751a3015a5b347ab3175554ad77137d71526a`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:79982546d0bed357c3b7f570dab84958af0f189249fe28e89577d41749385d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3596676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84f4d20594fd72e32a00a9feabc004f2a01714cd681f91d6012c8315cb905ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Tue, 14 Jan 2025 20:50:16 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afdd5abd6a9641f814dc31398b1f41f1208ca3c43eafd4a1c8885cb772431cc5`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473a53dcc89c2068574226fb084968b4ffe7be1af4300f024b632369f8a8c233`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113dcefb1595560f60660ee7a991d2b59509bc30e01ceddb44741db3ef240384`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 215.8 KB (215788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659fa19d2020016e65ba76874ea424e5842bf892ef9cbb0fb225538f1e187cf7`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff65919c3bd12f584108c1e36a3685a85470a54c58c385eb56d95175f5ab8c`  
		Last Modified: Fri, 10 Jan 2025 16:34:52 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1fe29fb7531300754b92edf6a17cb43bbf6bdccf3669dda2f135e21ecd7bc35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d832c44e71bd3c5c8e4af761656415c7160b797f2992b90ae6ccd9ad1d3bae`

```dockerfile
```

-	Layers:
	-	`sha256:22ce3c1ef9750e4e84284967ee5eccca34b598a38edbca4cd170feb5ca477190`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 72.2 KB (72175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aff322ae82649ec4042d09e767199a7e60414c2658b767de2a09545e6bc998d`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e65076fea6d36aa50870267c91ec6d95243f1fb11c28be61a1d14cc261f1cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3684480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f24babcb5d8bb3f6840a272a25b4d6bdcfcea3fcb3a940801065c5753d9538`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe78366bb027e03c42216a6e1d382df7a3ee78f1471f4c62ff2d535ec78d8ce`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644fc493adbda1d67b109c8285fbc4e3c1d916ad0fdd4e52b1d30d0c3b5a8b83`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 7.6 KB (7558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b5aca5c5549a3999391bdaf9bfdf23ae037d07dd0278bcc20a847480979e45`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 212.2 KB (212205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176ea9af669d43767bfdf3ce63602addb4cf802565986d5dc091d471acc30fe8`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93146a4a9bfc5584cd3df6a564e1f4ed3da6472cd8f41e6e08d7031d0c8114`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:93f271bcfc043724cd8ed10b5a81e091db12c7c9d2e449003a555df7b3164e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 KB (86446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e388d85c4a8c82382bf1c9f50c1c9b6f983abffb8517c5e88afc7ecb4b51d7af`

```dockerfile
```

-	Layers:
	-	`sha256:2f690c178f9bae18125b1de0d54e1b4493b26e2f974141f5f5fd3c9d3a20c6cb`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 72.1 KB (72145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8043e5e2fb4d14db768fcedf2f5c98e22493faee4d4820a99c0fb644ece380fc`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:2725f394d1c055b793a69764c862103d5fbd88a70531a3ed67a000071fd9b698
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6` - linux; amd64

```console
$ docker pull spiped@sha256:0807efe8e57e7a74993be6066b8c4d4917a1f6e3611dd0833309a2f48e69d189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37086272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43af49e196ea5b3803a09fb654b9f3a31809b1d63db50efadc92753d2a5ea1b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb387415fb818a8b4d56b6c4b1981b2212e57ec6addac3a80cfb2b9d9331b50`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228fe3a70b06fc8ca22481663a32d8b20b71b4a1cc2ef6bad63851b3cddc6a02`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 2.4 MB (2401340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bdc698a91b053c8c6c8793884aeb21f069855e2f35ceaf6d354563a622ec60`  
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 6.5 MB (6470976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562950f9b4e1da298d9932319a15c677ac7b1072f4a6218a62318ec083a438bf`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d26d7b3a2a6d5bfa2d8845580756d251c7acbb85868393a8dc4b15857a936c`  
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:4596a995a081e15712ce75ccbd6382c0362bbb99730c9b479c48fb6deb3de184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb27c549da9cd3fd74e3b201a56fe8440fe2368fbba1fa80abc7dac9262ff93`

```dockerfile
```

-	Layers:
	-	`sha256:d833741283a7f0cc036493894e91aa8f599339f065480034207be52408751f12`  
		Last Modified: Tue, 14 Jan 2025 23:04:24 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab16c690e615571a539221290f9c7154ed500a5de18d47dfbe3d130daff486f`  
		Last Modified: Tue, 14 Jan 2025 23:04:24 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:7ac314027d6a9a74b545bac6a566bab81092bc05f703e8e7feb689f1156a5820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32873874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f112ee2db55ec556284a0e51dab6d903a978b3e1a2817a609a226b6b833092`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 20:33:17 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d02c24549d50cc08f67dd0716935f9fa89992a0a0c1150357bba3bd55a0c1e7`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3c5e73b2f407694f10795c56fde8bcb539c9e2933731585f42dca1b1ace55f`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
		Size: 2.0 MB (1997177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a7e5af36cc87bcf1b73581be95f889fec6304edf80fae57e11543596a65d0b`  
		Last Modified: Tue, 14 Jan 2025 06:07:50 GMT  
		Size: 5.1 MB (5138490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecae1535903b4c1e77ac1ed96f21bd16112f406ad7f1531a331a8cd8bfcfa55`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff755cd6a71e19c14b557cb2ed1fe6c253d3a1f3539ecd08e66d6407b67d9ab5`  
		Last Modified: Tue, 14 Jan 2025 06:07:50 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:5550758ca3d10700c01f4a5f7e2dcc5e0a8bc81017e7a77563cc9e9d98b07ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc4f32a396e255a44a51de0250cbf8899e01021fdaf2877d4c981165ff96278`

```dockerfile
```

-	Layers:
	-	`sha256:2dfe195d70effae453580ecf74321962ef95b82e15bb2544354013d50bebb18b`  
		Last Modified: Tue, 14 Jan 2025 23:04:26 GMT  
		Size: 3.5 MB (3486344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d991ae0cd962a40b1a96f846b396fb35fb42d45ca1a7ffa955e1720f73fa9707`  
		Last Modified: Tue, 14 Jan 2025 23:04:28 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:cf5df2fe01fb9d92b1e5cb28bada0fa5ec279ec78e62c0ee49cc27a8baa06bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30652158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542aca3ffd11814f62e05ff8668c4fb3dff51d8dc3c1db06624b08d47f8f1980`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8717c624029ee40d56a1c31652eaf6ccf71a5567d7758a126900c0de1bcfad4`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b317980174023f6d6d78a005ee029285173f59fce3edc99c447ab905dfd179`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 1.9 MB (1855562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c382dfc5377b730c1b9c7edaff5880dda394c11f91a13f8946755dc7d81cf6d`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 4.9 MB (4880456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6267a4e0459f5d1157f3859e3edbabf7657d48de59e6c177fd3d1cf9114f73`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d786240c1a6e6bbdfc3fe94803ef3170f1198c85e7bb159452e0e2e512d162c`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:d9ba01708f3467414bc4781b45309ee70543bcfbd71a0484cedea151e2068d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3500977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f868daab95ccaa02d7e27af7666f2f1a087ae16fae21fbde97f5bd395594bb6`

```dockerfile
```

-	Layers:
	-	`sha256:8ce0204d70a42133258f980adb2349457dbdb8f72be802bed32e6bb1e0e0ddd5`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 3.5 MB (3485835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a0ec541bf556f8901ffbee01629c3a659a0f7db4cc58f578ffad9de316eb6cf`  
		Last Modified: Tue, 14 Jan 2025 23:04:29 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:ca50c1b1c64713d8110875a1f34775fc38040451acc500447a3622392bf2769f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35770669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772b7d61276d94b67963fb9f20b85927c2b84f7a0f63253fa64d274982b1f130`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3d076ceae3499abc00492adc7b101408d72437a499e4a9cea20964e90c3765`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0214df3970acd6fea09000d0df47a3cee908490cd9b760e15bd23ad7aa3cf552`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 2.2 MB (2247012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2354092ea972f14ee9af251fc4714c734d8cd2c30834f655c2ea396610489655`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 5.5 MB (5481085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d572dacd78b347329872172960cc26ce37ee9b7ac42a83ddc7425ad149add9cb`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e699072832a75d28646bc8d1b28f5ee412affda7e0b1e8469893f897fc236810`  
		Last Modified: Tue, 14 Jan 2025 06:38:45 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:d900c3ed70ec4adfcdeddd4771c0e2f9759b1cae7127b1122c5a54e1c910a28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3283792d48abf7c1421ee1439a40dfbe273c495208c163da83ef6da25092911b`

```dockerfile
```

-	Layers:
	-	`sha256:44d25165467985f6f9d9cf10d0306bed5af4e2ad6406371dc516b77fdf3a2ff3`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 3.5 MB (3487042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec8b87f83866e1f34c08767b42d87be6e439e3737291318890b05e17f026397a`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:50dc383a39b7bbf8bc7274000476568ef19f00fa47f5e77a3b945e542d602e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37529245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff3adfb5bcb041fd776f222523c7e5f7d316c3a84275c48f8a469520e3cf670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9757c47c7f65469fabaf649c24c76e71b0ee344186b7378388e73b9ff3584956`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41f696ea1cea6b748d59acb3f0e93feb73a67b208dc03bdd8d489b78b8c4c1c`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 2.4 MB (2398649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241faa93dbe7603d3ddfe8143dbc5f7e9990a80036efae46f8147ce9b8e684d7`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 5.9 MB (5941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac324e1750c72f49ee4d4c3b000ae242266e9e9b1946584a5a221c6d4b01bbe9`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f5c66d701ad1b4e0469df5595f673c4d111557d936709a7c5ab15e2ca0f378`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:78318e0a0bae94e38b3a5d9c7578f6751580c7038fd2e2660d4d7cc768105076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed705c7a2f1d4214425c51ed536dd3d3ab550dfbe9a1b50c38de8bba85e59791`

```dockerfile
```

-	Layers:
	-	`sha256:b0eb158509e496490a1fa281c429ec733f8201538a8ead508644c888a4a09018`  
		Last Modified: Tue, 14 Jan 2025 23:04:35 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e8230d3f815bb664e5eda60129ff633bc7d34854e10e52903d538454410d33`  
		Last Modified: Tue, 14 Jan 2025 23:04:35 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:c01ffa398018e931ac10ce62e16a6625947a0fcc8a2293eade003a3c6b3ab862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36132905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fb4e4e2a5078ea045150d8177a114a04293312c91ebd35e93cb59f1e2259e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 20:36:28 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252230c34678f565279955a422dad63275a16eeef208147f154e13e5647df2ed`  
		Last Modified: Tue, 14 Jan 2025 18:08:24 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f980dd5eb6de9195670967164c2a6d21dfc4bd270afc766fc82f7303fcea879a`  
		Last Modified: Tue, 14 Jan 2025 18:08:25 GMT  
		Size: 1.8 MB (1841121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fde05de7416ebc2e722610c9c2dc2ff46e18c6ef77c23e6e4dd9dcee7c809c4`  
		Last Modified: Tue, 14 Jan 2025 18:08:25 GMT  
		Size: 5.8 MB (5803593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7fe7c8e4867db382a8bf9a5c5bbd8cf77ba59015bd2dae591763292f1a7687`  
		Last Modified: Tue, 14 Jan 2025 18:08:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2345d9838a2e18ef7406ff0df0a5dedb563ffa5c105d7e69074a1599a12e35b8`  
		Last Modified: Tue, 14 Jan 2025 18:08:25 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:ac952f287cc93e8b3d1962734d5e6d7b7fea48269365cd58ff092baa9691aba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8839767e2b373c2b310dd1f060d29a21907bda9cf88c7ee7eb3bfea9d99af4c6`

```dockerfile
```

-	Layers:
	-	`sha256:edffc4065fe5a50cf43009afbdb9c8d5dc04651bc8b0abafa3baa3ed0ff073d3`  
		Last Modified: Tue, 14 Jan 2025 23:04:36 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:e0838362e10a88cedb5ebf5d4c38e86e979cb384e1bf72965f8839333fa63baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41051304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5145bd62627fce56a871970f71c1423bf8e7bd302f8e8c8cfdb7a4c492dce6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048adc09f28a34691cbfb26824234082fe589f23a9fa178a80bd0a97e36157ae`  
		Last Modified: Tue, 14 Jan 2025 05:12:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06163a828f03667776915ff22220e1c76e276331d5b5553d9d91f54f6e1b0be2`  
		Last Modified: Tue, 14 Jan 2025 05:13:00 GMT  
		Size: 2.6 MB (2582093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4e996ae8bb5769e51b9acf136d0daaec2939316030203ad6bfa9ee6e82658b`  
		Last Modified: Tue, 14 Jan 2025 05:13:00 GMT  
		Size: 6.4 MB (6422823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204877fb93a1bb0e23eefae6b5ecafcb745cca605fc4e56d05cf862c4f46ec06`  
		Last Modified: Tue, 14 Jan 2025 05:12:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ff3d47eee1c6ccd068d483c63d368a7a6b63c65285cc05761b023d365b9eb0`  
		Last Modified: Tue, 14 Jan 2025 05:13:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:2ac6faef580387afaac65a40852917553101f4b0bd349432d9fae7c1c34b8b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01442cee26b43c9b5f0e98561c25f1d8a7533dccea7b29f16318d0dbffb52a81`

```dockerfile
```

-	Layers:
	-	`sha256:07a1d36ee150774030a74edfb128021444921e2d3eff9710baf6e3a2539c33a2`  
		Last Modified: Tue, 14 Jan 2025 05:13:00 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e46605f5ae9d418c541c83eef4a80f85ac8f32ef307ca58ccab597614e90e0d5`  
		Last Modified: Tue, 14 Jan 2025 23:04:40 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:9a8b4589f022b01cb7379216c0ed4bcfd689c1534d89e1ba7feaaf8c2c7335b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34314999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bb0a694ef3ab84e988bb522551da84d245aa5de9bff71d4e174d5dee08f88b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de4963ba94159da6a677e9693e16f2aaca6406d4426d738af27c3ecc011e85e`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d01390fd75845fd56420f30cd57336b2c75946123f8fdef738b1ee09427359`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 2.1 MB (2068686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef25b97e48209f7c51f7ab797e7c2c9e939b8a05b5b8ca73c14e1c82838fcb22`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 5.4 MB (5386034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4f625a2f5c5cca8030def5f775ae31a6cc2f0f701ad190da0d260c82eb52cb`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fcd0f24724877817587b4569325c3d96d4f4f24e77572ca3f0ec447e622d0d`  
		Last Modified: Tue, 14 Jan 2025 04:49:48 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:cb0a11a3acd5c8d5fc548066b9664c5a715152b3f4999ee92005b77403c1a49e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b3f9cad8e646fdb0c0e919133c2cc5c6481b885ce2db546e37c5d2ff97e85a`

```dockerfile
```

-	Layers:
	-	`sha256:77bf42cd7e49ab8b25190be2a4044d6e977c9ddd06f1f4c7fcd6acb450e8e53b`  
		Last Modified: Tue, 14 Jan 2025 23:04:41 GMT  
		Size: 3.5 MB (3504000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf76c9e1d84fed3f30cb373ece1c7713dffbb1a40bd4018101999d0b899e9f72`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:3defbc7042c9287d78d336478981bdf2410928e48fd8a9504755509633620376
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:924e7f71ff8a6210c218250cadec128119d344f463da73b7435727f3b79f8b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3860004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002ee6ce7d381016e688df520b2d8e452892442cc9dd7d7fe4f2fd27e10bd9cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4d648a75810ee71e4a811a07ea0f0ac2c721e73e72187e9a1516d4c4c5ee6f`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe07a72f4be9ce0f108da046cf545981624f6b49403d76321af17c0c395f286d`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda92c005435cc07d0f9aeede336b39adeacb3d2b63892bd145844c2ffdee52b`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 224.8 KB (224801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d408faf96bb5ca591f0228176fd9fe8fcadf008b4a1d270852fc8c6e4ba93ef1`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e29defa7a55825f8f61eda130cb04ee394d66bd712f70709ac7053a248548`  
		Last Modified: Wed, 08 Jan 2025 18:12:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:bbb6e45e7eb3500533fd5eb9b6e02cbb71696097c25c94d70ad5011ff89719b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ed9b89a1c4bf4f119be92f17b9244feb5432b0aa95a99a543b91711e64d2ff`

```dockerfile
```

-	Layers:
	-	`sha256:d6dbec5f27c384596dd421778e731d1e085e3759f6d847458fe59a756fb7ac42`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 74.1 KB (74096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb9a321a7ee93632ee08168238d08c393bd8977dc0b90058743b7578fd3ffc57`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3b33305e723d928de0ceb007a192d635fbcead1966adcef42495013c151ab1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3908b8302a74d29d2ba4f9fad53ec5dae4d694c59ef5e425f9d3b4ae6f8e82c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Tue, 14 Jan 2025 20:34:27 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af3f0630555eb148818822fb59b573ef21353f360d8de1a31a9d923807ee4cd`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779a48568101672a32588570e7ceef7c0674397cbfa25ee720cde2859ab94873`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 7.5 KB (7549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a21818ff816934f603fcd2d4cba9f12db282bab07e3069da21d7578259ccec`  
		Last Modified: Wed, 08 Jan 2025 21:50:17 GMT  
		Size: 209.4 KB (209360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908425f61ccde4470882b7fc3250f120af7e457373de37561ca1bc2c428156fb`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d99959ccf8e07e46905c21480b4a1efde735673420d31417427ecef2146095`  
		Last Modified: Wed, 08 Jan 2025 21:50:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b7cb53f249d979d695f81563768605e871ddd1ea8a0819dd8dd81dc4987a573f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755f963c27fded64f7e3f6ff08da27dc1fd056f8030a81de4cb41f27e65d037b`

```dockerfile
```

-	Layers:
	-	`sha256:696c936ae51f846bce7be1a6d2dde5c03aa3b71ffda41e1e6b2cf2a621f6cd97`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 14.2 KB (14189 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ae8dad9afbb0cc8a3d199d4f081244152b6bb25a314d1c1b53d2015cb7a3148c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3307454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4e1533dc661a40478a134b3fe58301335db42d8f87ae18e6918ff38e81ae91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Tue, 14 Jan 2025 20:45:20 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7fdb315d3c34eb6935e1b7deb703093f5317800ff4d8b3936d5f771137cb79`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3360ef971eae752027c0ac2e924cac0c91b7f45b5099026b2a8f4be3279f6b5`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70480e7090e82ed5e217b413501ec1d1ac188d14349be7aa351d6ebc4bfa572b`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 203.0 KB (202981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa024b8e7a4dcd96a95ba7c408a6b6bf086e89742d975c9ce4fdfcfc7cabc1b`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4350bd55dee2c6c0b00a05b33f36a79b911cbfa491acf490c5bdc593d8e3e547`  
		Last Modified: Wed, 08 Jan 2025 21:55:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:374da430416cd603b6845710a7b6b98de8856fb9d596f167daa655438d68910f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfb7685b3853e3be4a1172afeae58a3bd43dbc7f6bf21565a8d6843e6b79559`

```dockerfile
```

-	Layers:
	-	`sha256:d4af9f6a3307489ccc6bd25b80644c322c26bf5739a42dab919b2dc03edff9ab`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 74.1 KB (74132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d585d482698adea511246e8d288a1602e3c63dc4f235cfa0915b12ae4b080f64`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:3565ca7a9021c033aa2f9aa3fa95ec43241003635fa8669990453c55ff55e1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa0a984328f7027e356ee0aa46ff85666d4fdeec5eb2d5343a30a9dbe998445`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f2d3fc3adfdd301f5e24f24c5392b9879a1b61f182e7752a21cb03e6aeb04`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d972687789bff098d9b33d09c024319254bdf8dcd29abb2bf072809733c79f49`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37195bfd737aa3f22ef0dd56d792afbe7e88b9c83db3bf0e69cb557d04d0d152`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 219.5 KB (219522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9420b682506ca5859fc3f4af6d59a5ca6fb329a69a869e8d7d0766374eb87ae7`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f38e672eaca427117d78c3580183cebdd51913b95165f7a4fecbb7219aeb29`  
		Last Modified: Wed, 08 Jan 2025 22:06:49 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c1545d907101296a82932a434f77b80a720493d1f158f28037a360c849c6b869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af58e3c42e72d2f836cf482efb095b5869000f90e0fd8c744622051f65cbeb6`

```dockerfile
```

-	Layers:
	-	`sha256:802dad5a525c4dc8453a7af1d74e5f8e0f8e9db9e0b53075b1abb70ebcbcac58`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 74.2 KB (74152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31d587a383d8f42361fc2623919a7a23e16261c7eb1f51cb4aa140497be4935`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:92342ba21763b953dae5124e2470d7b310cdec0e1aa1c278c715dda9eb6c5a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a710174a0b36bde4dc08b5531a97264b1a956e7b607e3cb81fa4ed42446333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01646177e05c873338d049d0058c8cd923326812215a3897564adbd669ee56f`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf3460ecbeac950e26287d1cf9fdf47918bf993988d851835f852bbd5707856`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69044b34b50595fbdc42e577dc79e206d3962968154ec6fbf18024dfe607c6cd`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 235.4 KB (235383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2fe84ec006ef02b90eb19d8de0f72b59b1f5d3cad78ef6d043f1ea320d121`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8feb2512bb10b2b05cf6ac1f623ac53ae1aaaf4d759aa98618bf0a96439d0c`  
		Last Modified: Wed, 08 Jan 2025 18:07:24 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f82eea4e46a614570a5475a2c2999ebdb44416593095c39bfe597dfb70954205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 KB (88337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c43d43c6b18f013ddf9e79c05395cc1213c96194b62e9231a34602566ed737c`

```dockerfile
```

-	Layers:
	-	`sha256:662bb99fc24ff68d14f1e276dc7da9f11ef9f56131659d2a511578d1c4547a4e`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 74.1 KB (74071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab4679badb23f30ba84ac1e7ab274f8693e730ac87dbfac78c97707c071c360`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:62a8529f4a88431c2c8453c2198b9f19f5027af08967a818ceb2e9f5485a2d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3806729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b6428f7bf466f0e03b157ec2507c547f21126e87e9b2e288213771e8ccfd2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d50e862e95a905933f50b6440c968976a25afd06a9808138b7b662be556076`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca1e9dba23dfea2ee87d2657bcd8e5e57a74b668b777c31cdf12a5a688c9e23`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b2864e003337f2f79f0ebbd5d8f47c821a711805de5ac4aac9a3f02a5d06b3`  
		Last Modified: Wed, 08 Jan 2025 21:29:15 GMT  
		Size: 223.4 KB (223364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b04a1708fbc0147d4ef6fdeb564449a7a41b7b0e5df2aa27a1441946c81598c`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66b8e9453e2d649488c8d053b0d1d4ae5e3740489586c6bb32f7eae7a3ec003`  
		Last Modified: Wed, 08 Jan 2025 21:29:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:641f93fddb6e6a668353356d78a708a17b7271ab06e13c5d2d1645d499c65794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1511f0eb48159856515b99abf8dee3e56263f52094148ce660d713454d210ec3`

```dockerfile
```

-	Layers:
	-	`sha256:55e5c3dc4287df2df2d9e20c08f5cd46d57a5616350e241f492bf844c18956d1`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 72.2 KB (72179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f348d15a848da4a767fe70750751a3015a5b347ab3175554ad77137d71526a`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:79982546d0bed357c3b7f570dab84958af0f189249fe28e89577d41749385d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3596676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84f4d20594fd72e32a00a9feabc004f2a01714cd681f91d6012c8315cb905ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Tue, 14 Jan 2025 20:50:16 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afdd5abd6a9641f814dc31398b1f41f1208ca3c43eafd4a1c8885cb772431cc5`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473a53dcc89c2068574226fb084968b4ffe7be1af4300f024b632369f8a8c233`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113dcefb1595560f60660ee7a991d2b59509bc30e01ceddb44741db3ef240384`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 215.8 KB (215788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659fa19d2020016e65ba76874ea424e5842bf892ef9cbb0fb225538f1e187cf7`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff65919c3bd12f584108c1e36a3685a85470a54c58c385eb56d95175f5ab8c`  
		Last Modified: Fri, 10 Jan 2025 16:34:52 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1fe29fb7531300754b92edf6a17cb43bbf6bdccf3669dda2f135e21ecd7bc35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d832c44e71bd3c5c8e4af761656415c7160b797f2992b90ae6ccd9ad1d3bae`

```dockerfile
```

-	Layers:
	-	`sha256:22ce3c1ef9750e4e84284967ee5eccca34b598a38edbca4cd170feb5ca477190`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 72.2 KB (72175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aff322ae82649ec4042d09e767199a7e60414c2658b767de2a09545e6bc998d`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e65076fea6d36aa50870267c91ec6d95243f1fb11c28be61a1d14cc261f1cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3684480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f24babcb5d8bb3f6840a272a25b4d6bdcfcea3fcb3a940801065c5753d9538`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe78366bb027e03c42216a6e1d382df7a3ee78f1471f4c62ff2d535ec78d8ce`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644fc493adbda1d67b109c8285fbc4e3c1d916ad0fdd4e52b1d30d0c3b5a8b83`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 7.6 KB (7558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b5aca5c5549a3999391bdaf9bfdf23ae037d07dd0278bcc20a847480979e45`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 212.2 KB (212205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176ea9af669d43767bfdf3ce63602addb4cf802565986d5dc091d471acc30fe8`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93146a4a9bfc5584cd3df6a564e1f4ed3da6472cd8f41e6e08d7031d0c8114`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:93f271bcfc043724cd8ed10b5a81e091db12c7c9d2e449003a555df7b3164e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 KB (86446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e388d85c4a8c82382bf1c9f50c1c9b6f983abffb8517c5e88afc7ecb4b51d7af`

```dockerfile
```

-	Layers:
	-	`sha256:2f690c178f9bae18125b1de0d54e1b4493b26e2f974141f5f5fd3c9d3a20c6cb`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 72.1 KB (72145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8043e5e2fb4d14db768fcedf2f5c98e22493faee4d4820a99c0fb644ece380fc`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.2`

```console
$ docker pull spiped@sha256:2725f394d1c055b793a69764c862103d5fbd88a70531a3ed67a000071fd9b698
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6.2` - linux; amd64

```console
$ docker pull spiped@sha256:0807efe8e57e7a74993be6066b8c4d4917a1f6e3611dd0833309a2f48e69d189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37086272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43af49e196ea5b3803a09fb654b9f3a31809b1d63db50efadc92753d2a5ea1b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb387415fb818a8b4d56b6c4b1981b2212e57ec6addac3a80cfb2b9d9331b50`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228fe3a70b06fc8ca22481663a32d8b20b71b4a1cc2ef6bad63851b3cddc6a02`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 2.4 MB (2401340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bdc698a91b053c8c6c8793884aeb21f069855e2f35ceaf6d354563a622ec60`  
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 6.5 MB (6470976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562950f9b4e1da298d9932319a15c677ac7b1072f4a6218a62318ec083a438bf`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d26d7b3a2a6d5bfa2d8845580756d251c7acbb85868393a8dc4b15857a936c`  
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:4596a995a081e15712ce75ccbd6382c0362bbb99730c9b479c48fb6deb3de184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb27c549da9cd3fd74e3b201a56fe8440fe2368fbba1fa80abc7dac9262ff93`

```dockerfile
```

-	Layers:
	-	`sha256:d833741283a7f0cc036493894e91aa8f599339f065480034207be52408751f12`  
		Last Modified: Tue, 14 Jan 2025 23:04:24 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab16c690e615571a539221290f9c7154ed500a5de18d47dfbe3d130daff486f`  
		Last Modified: Tue, 14 Jan 2025 23:04:24 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; arm variant v5

```console
$ docker pull spiped@sha256:7ac314027d6a9a74b545bac6a566bab81092bc05f703e8e7feb689f1156a5820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32873874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f112ee2db55ec556284a0e51dab6d903a978b3e1a2817a609a226b6b833092`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 20:33:17 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d02c24549d50cc08f67dd0716935f9fa89992a0a0c1150357bba3bd55a0c1e7`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3c5e73b2f407694f10795c56fde8bcb539c9e2933731585f42dca1b1ace55f`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
		Size: 2.0 MB (1997177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a7e5af36cc87bcf1b73581be95f889fec6304edf80fae57e11543596a65d0b`  
		Last Modified: Tue, 14 Jan 2025 06:07:50 GMT  
		Size: 5.1 MB (5138490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecae1535903b4c1e77ac1ed96f21bd16112f406ad7f1531a331a8cd8bfcfa55`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff755cd6a71e19c14b557cb2ed1fe6c253d3a1f3539ecd08e66d6407b67d9ab5`  
		Last Modified: Tue, 14 Jan 2025 06:07:50 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:5550758ca3d10700c01f4a5f7e2dcc5e0a8bc81017e7a77563cc9e9d98b07ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc4f32a396e255a44a51de0250cbf8899e01021fdaf2877d4c981165ff96278`

```dockerfile
```

-	Layers:
	-	`sha256:2dfe195d70effae453580ecf74321962ef95b82e15bb2544354013d50bebb18b`  
		Last Modified: Tue, 14 Jan 2025 23:04:26 GMT  
		Size: 3.5 MB (3486344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d991ae0cd962a40b1a96f846b396fb35fb42d45ca1a7ffa955e1720f73fa9707`  
		Last Modified: Tue, 14 Jan 2025 23:04:28 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; arm variant v7

```console
$ docker pull spiped@sha256:cf5df2fe01fb9d92b1e5cb28bada0fa5ec279ec78e62c0ee49cc27a8baa06bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30652158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542aca3ffd11814f62e05ff8668c4fb3dff51d8dc3c1db06624b08d47f8f1980`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8717c624029ee40d56a1c31652eaf6ccf71a5567d7758a126900c0de1bcfad4`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b317980174023f6d6d78a005ee029285173f59fce3edc99c447ab905dfd179`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 1.9 MB (1855562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c382dfc5377b730c1b9c7edaff5880dda394c11f91a13f8946755dc7d81cf6d`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 4.9 MB (4880456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6267a4e0459f5d1157f3859e3edbabf7657d48de59e6c177fd3d1cf9114f73`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d786240c1a6e6bbdfc3fe94803ef3170f1198c85e7bb159452e0e2e512d162c`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:d9ba01708f3467414bc4781b45309ee70543bcfbd71a0484cedea151e2068d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3500977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f868daab95ccaa02d7e27af7666f2f1a087ae16fae21fbde97f5bd395594bb6`

```dockerfile
```

-	Layers:
	-	`sha256:8ce0204d70a42133258f980adb2349457dbdb8f72be802bed32e6bb1e0e0ddd5`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 3.5 MB (3485835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a0ec541bf556f8901ffbee01629c3a659a0f7db4cc58f578ffad9de316eb6cf`  
		Last Modified: Tue, 14 Jan 2025 23:04:29 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:ca50c1b1c64713d8110875a1f34775fc38040451acc500447a3622392bf2769f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35770669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772b7d61276d94b67963fb9f20b85927c2b84f7a0f63253fa64d274982b1f130`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3d076ceae3499abc00492adc7b101408d72437a499e4a9cea20964e90c3765`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0214df3970acd6fea09000d0df47a3cee908490cd9b760e15bd23ad7aa3cf552`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 2.2 MB (2247012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2354092ea972f14ee9af251fc4714c734d8cd2c30834f655c2ea396610489655`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 5.5 MB (5481085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d572dacd78b347329872172960cc26ce37ee9b7ac42a83ddc7425ad149add9cb`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e699072832a75d28646bc8d1b28f5ee412affda7e0b1e8469893f897fc236810`  
		Last Modified: Tue, 14 Jan 2025 06:38:45 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:d900c3ed70ec4adfcdeddd4771c0e2f9759b1cae7127b1122c5a54e1c910a28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3283792d48abf7c1421ee1439a40dfbe273c495208c163da83ef6da25092911b`

```dockerfile
```

-	Layers:
	-	`sha256:44d25165467985f6f9d9cf10d0306bed5af4e2ad6406371dc516b77fdf3a2ff3`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 3.5 MB (3487042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec8b87f83866e1f34c08767b42d87be6e439e3737291318890b05e17f026397a`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; 386

```console
$ docker pull spiped@sha256:50dc383a39b7bbf8bc7274000476568ef19f00fa47f5e77a3b945e542d602e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37529245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff3adfb5bcb041fd776f222523c7e5f7d316c3a84275c48f8a469520e3cf670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9757c47c7f65469fabaf649c24c76e71b0ee344186b7378388e73b9ff3584956`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41f696ea1cea6b748d59acb3f0e93feb73a67b208dc03bdd8d489b78b8c4c1c`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 2.4 MB (2398649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241faa93dbe7603d3ddfe8143dbc5f7e9990a80036efae46f8147ce9b8e684d7`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 5.9 MB (5941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac324e1750c72f49ee4d4c3b000ae242266e9e9b1946584a5a221c6d4b01bbe9`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f5c66d701ad1b4e0469df5595f673c4d111557d936709a7c5ab15e2ca0f378`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:78318e0a0bae94e38b3a5d9c7578f6751580c7038fd2e2660d4d7cc768105076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed705c7a2f1d4214425c51ed536dd3d3ab550dfbe9a1b50c38de8bba85e59791`

```dockerfile
```

-	Layers:
	-	`sha256:b0eb158509e496490a1fa281c429ec733f8201538a8ead508644c888a4a09018`  
		Last Modified: Tue, 14 Jan 2025 23:04:35 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e8230d3f815bb664e5eda60129ff633bc7d34854e10e52903d538454410d33`  
		Last Modified: Tue, 14 Jan 2025 23:04:35 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; mips64le

```console
$ docker pull spiped@sha256:c01ffa398018e931ac10ce62e16a6625947a0fcc8a2293eade003a3c6b3ab862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36132905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fb4e4e2a5078ea045150d8177a114a04293312c91ebd35e93cb59f1e2259e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 20:36:28 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252230c34678f565279955a422dad63275a16eeef208147f154e13e5647df2ed`  
		Last Modified: Tue, 14 Jan 2025 18:08:24 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f980dd5eb6de9195670967164c2a6d21dfc4bd270afc766fc82f7303fcea879a`  
		Last Modified: Tue, 14 Jan 2025 18:08:25 GMT  
		Size: 1.8 MB (1841121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fde05de7416ebc2e722610c9c2dc2ff46e18c6ef77c23e6e4dd9dcee7c809c4`  
		Last Modified: Tue, 14 Jan 2025 18:08:25 GMT  
		Size: 5.8 MB (5803593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7fe7c8e4867db382a8bf9a5c5bbd8cf77ba59015bd2dae591763292f1a7687`  
		Last Modified: Tue, 14 Jan 2025 18:08:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2345d9838a2e18ef7406ff0df0a5dedb563ffa5c105d7e69074a1599a12e35b8`  
		Last Modified: Tue, 14 Jan 2025 18:08:25 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:ac952f287cc93e8b3d1962734d5e6d7b7fea48269365cd58ff092baa9691aba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8839767e2b373c2b310dd1f060d29a21907bda9cf88c7ee7eb3bfea9d99af4c6`

```dockerfile
```

-	Layers:
	-	`sha256:edffc4065fe5a50cf43009afbdb9c8d5dc04651bc8b0abafa3baa3ed0ff073d3`  
		Last Modified: Tue, 14 Jan 2025 23:04:36 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; ppc64le

```console
$ docker pull spiped@sha256:e0838362e10a88cedb5ebf5d4c38e86e979cb384e1bf72965f8839333fa63baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41051304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5145bd62627fce56a871970f71c1423bf8e7bd302f8e8c8cfdb7a4c492dce6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048adc09f28a34691cbfb26824234082fe589f23a9fa178a80bd0a97e36157ae`  
		Last Modified: Tue, 14 Jan 2025 05:12:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06163a828f03667776915ff22220e1c76e276331d5b5553d9d91f54f6e1b0be2`  
		Last Modified: Tue, 14 Jan 2025 05:13:00 GMT  
		Size: 2.6 MB (2582093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4e996ae8bb5769e51b9acf136d0daaec2939316030203ad6bfa9ee6e82658b`  
		Last Modified: Tue, 14 Jan 2025 05:13:00 GMT  
		Size: 6.4 MB (6422823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204877fb93a1bb0e23eefae6b5ecafcb745cca605fc4e56d05cf862c4f46ec06`  
		Last Modified: Tue, 14 Jan 2025 05:12:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ff3d47eee1c6ccd068d483c63d368a7a6b63c65285cc05761b023d365b9eb0`  
		Last Modified: Tue, 14 Jan 2025 05:13:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:2ac6faef580387afaac65a40852917553101f4b0bd349432d9fae7c1c34b8b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01442cee26b43c9b5f0e98561c25f1d8a7533dccea7b29f16318d0dbffb52a81`

```dockerfile
```

-	Layers:
	-	`sha256:07a1d36ee150774030a74edfb128021444921e2d3eff9710baf6e3a2539c33a2`  
		Last Modified: Tue, 14 Jan 2025 05:13:00 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e46605f5ae9d418c541c83eef4a80f85ac8f32ef307ca58ccab597614e90e0d5`  
		Last Modified: Tue, 14 Jan 2025 23:04:40 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; s390x

```console
$ docker pull spiped@sha256:9a8b4589f022b01cb7379216c0ed4bcfd689c1534d89e1ba7feaaf8c2c7335b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34314999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bb0a694ef3ab84e988bb522551da84d245aa5de9bff71d4e174d5dee08f88b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de4963ba94159da6a677e9693e16f2aaca6406d4426d738af27c3ecc011e85e`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d01390fd75845fd56420f30cd57336b2c75946123f8fdef738b1ee09427359`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 2.1 MB (2068686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef25b97e48209f7c51f7ab797e7c2c9e939b8a05b5b8ca73c14e1c82838fcb22`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 5.4 MB (5386034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4f625a2f5c5cca8030def5f775ae31a6cc2f0f701ad190da0d260c82eb52cb`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fcd0f24724877817587b4569325c3d96d4f4f24e77572ca3f0ec447e622d0d`  
		Last Modified: Tue, 14 Jan 2025 04:49:48 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:cb0a11a3acd5c8d5fc548066b9664c5a715152b3f4999ee92005b77403c1a49e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b3f9cad8e646fdb0c0e919133c2cc5c6481b885ce2db546e37c5d2ff97e85a`

```dockerfile
```

-	Layers:
	-	`sha256:77bf42cd7e49ab8b25190be2a4044d6e977c9ddd06f1f4c7fcd6acb450e8e53b`  
		Last Modified: Tue, 14 Jan 2025 23:04:41 GMT  
		Size: 3.5 MB (3504000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf76c9e1d84fed3f30cb373ece1c7713dffbb1a40bd4018101999d0b899e9f72`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.2-alpine`

```console
$ docker pull spiped@sha256:3defbc7042c9287d78d336478981bdf2410928e48fd8a9504755509633620376
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6.2-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:924e7f71ff8a6210c218250cadec128119d344f463da73b7435727f3b79f8b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3860004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002ee6ce7d381016e688df520b2d8e452892442cc9dd7d7fe4f2fd27e10bd9cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4d648a75810ee71e4a811a07ea0f0ac2c721e73e72187e9a1516d4c4c5ee6f`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe07a72f4be9ce0f108da046cf545981624f6b49403d76321af17c0c395f286d`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda92c005435cc07d0f9aeede336b39adeacb3d2b63892bd145844c2ffdee52b`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 224.8 KB (224801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d408faf96bb5ca591f0228176fd9fe8fcadf008b4a1d270852fc8c6e4ba93ef1`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e29defa7a55825f8f61eda130cb04ee394d66bd712f70709ac7053a248548`  
		Last Modified: Wed, 08 Jan 2025 18:12:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:bbb6e45e7eb3500533fd5eb9b6e02cbb71696097c25c94d70ad5011ff89719b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ed9b89a1c4bf4f119be92f17b9244feb5432b0aa95a99a543b91711e64d2ff`

```dockerfile
```

-	Layers:
	-	`sha256:d6dbec5f27c384596dd421778e731d1e085e3759f6d847458fe59a756fb7ac42`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 74.1 KB (74096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb9a321a7ee93632ee08168238d08c393bd8977dc0b90058743b7578fd3ffc57`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3b33305e723d928de0ceb007a192d635fbcead1966adcef42495013c151ab1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3908b8302a74d29d2ba4f9fad53ec5dae4d694c59ef5e425f9d3b4ae6f8e82c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Tue, 14 Jan 2025 20:34:27 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af3f0630555eb148818822fb59b573ef21353f360d8de1a31a9d923807ee4cd`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779a48568101672a32588570e7ceef7c0674397cbfa25ee720cde2859ab94873`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 7.5 KB (7549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a21818ff816934f603fcd2d4cba9f12db282bab07e3069da21d7578259ccec`  
		Last Modified: Wed, 08 Jan 2025 21:50:17 GMT  
		Size: 209.4 KB (209360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908425f61ccde4470882b7fc3250f120af7e457373de37561ca1bc2c428156fb`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d99959ccf8e07e46905c21480b4a1efde735673420d31417427ecef2146095`  
		Last Modified: Wed, 08 Jan 2025 21:50:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b7cb53f249d979d695f81563768605e871ddd1ea8a0819dd8dd81dc4987a573f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755f963c27fded64f7e3f6ff08da27dc1fd056f8030a81de4cb41f27e65d037b`

```dockerfile
```

-	Layers:
	-	`sha256:696c936ae51f846bce7be1a6d2dde5c03aa3b71ffda41e1e6b2cf2a621f6cd97`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 14.2 KB (14189 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ae8dad9afbb0cc8a3d199d4f081244152b6bb25a314d1c1b53d2015cb7a3148c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3307454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4e1533dc661a40478a134b3fe58301335db42d8f87ae18e6918ff38e81ae91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Tue, 14 Jan 2025 20:45:20 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7fdb315d3c34eb6935e1b7deb703093f5317800ff4d8b3936d5f771137cb79`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3360ef971eae752027c0ac2e924cac0c91b7f45b5099026b2a8f4be3279f6b5`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70480e7090e82ed5e217b413501ec1d1ac188d14349be7aa351d6ebc4bfa572b`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 203.0 KB (202981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa024b8e7a4dcd96a95ba7c408a6b6bf086e89742d975c9ce4fdfcfc7cabc1b`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4350bd55dee2c6c0b00a05b33f36a79b911cbfa491acf490c5bdc593d8e3e547`  
		Last Modified: Wed, 08 Jan 2025 21:55:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:374da430416cd603b6845710a7b6b98de8856fb9d596f167daa655438d68910f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfb7685b3853e3be4a1172afeae58a3bd43dbc7f6bf21565a8d6843e6b79559`

```dockerfile
```

-	Layers:
	-	`sha256:d4af9f6a3307489ccc6bd25b80644c322c26bf5739a42dab919b2dc03edff9ab`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 74.1 KB (74132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d585d482698adea511246e8d288a1602e3c63dc4f235cfa0915b12ae4b080f64`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:3565ca7a9021c033aa2f9aa3fa95ec43241003635fa8669990453c55ff55e1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa0a984328f7027e356ee0aa46ff85666d4fdeec5eb2d5343a30a9dbe998445`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f2d3fc3adfdd301f5e24f24c5392b9879a1b61f182e7752a21cb03e6aeb04`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d972687789bff098d9b33d09c024319254bdf8dcd29abb2bf072809733c79f49`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37195bfd737aa3f22ef0dd56d792afbe7e88b9c83db3bf0e69cb557d04d0d152`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 219.5 KB (219522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9420b682506ca5859fc3f4af6d59a5ca6fb329a69a869e8d7d0766374eb87ae7`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f38e672eaca427117d78c3580183cebdd51913b95165f7a4fecbb7219aeb29`  
		Last Modified: Wed, 08 Jan 2025 22:06:49 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c1545d907101296a82932a434f77b80a720493d1f158f28037a360c849c6b869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af58e3c42e72d2f836cf482efb095b5869000f90e0fd8c744622051f65cbeb6`

```dockerfile
```

-	Layers:
	-	`sha256:802dad5a525c4dc8453a7af1d74e5f8e0f8e9db9e0b53075b1abb70ebcbcac58`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 74.2 KB (74152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31d587a383d8f42361fc2623919a7a23e16261c7eb1f51cb4aa140497be4935`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; 386

```console
$ docker pull spiped@sha256:92342ba21763b953dae5124e2470d7b310cdec0e1aa1c278c715dda9eb6c5a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a710174a0b36bde4dc08b5531a97264b1a956e7b607e3cb81fa4ed42446333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01646177e05c873338d049d0058c8cd923326812215a3897564adbd669ee56f`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf3460ecbeac950e26287d1cf9fdf47918bf993988d851835f852bbd5707856`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69044b34b50595fbdc42e577dc79e206d3962968154ec6fbf18024dfe607c6cd`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 235.4 KB (235383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2fe84ec006ef02b90eb19d8de0f72b59b1f5d3cad78ef6d043f1ea320d121`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8feb2512bb10b2b05cf6ac1f623ac53ae1aaaf4d759aa98618bf0a96439d0c`  
		Last Modified: Wed, 08 Jan 2025 18:07:24 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f82eea4e46a614570a5475a2c2999ebdb44416593095c39bfe597dfb70954205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 KB (88337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c43d43c6b18f013ddf9e79c05395cc1213c96194b62e9231a34602566ed737c`

```dockerfile
```

-	Layers:
	-	`sha256:662bb99fc24ff68d14f1e276dc7da9f11ef9f56131659d2a511578d1c4547a4e`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 74.1 KB (74071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab4679badb23f30ba84ac1e7ab274f8693e730ac87dbfac78c97707c071c360`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:62a8529f4a88431c2c8453c2198b9f19f5027af08967a818ceb2e9f5485a2d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3806729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b6428f7bf466f0e03b157ec2507c547f21126e87e9b2e288213771e8ccfd2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d50e862e95a905933f50b6440c968976a25afd06a9808138b7b662be556076`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca1e9dba23dfea2ee87d2657bcd8e5e57a74b668b777c31cdf12a5a688c9e23`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b2864e003337f2f79f0ebbd5d8f47c821a711805de5ac4aac9a3f02a5d06b3`  
		Last Modified: Wed, 08 Jan 2025 21:29:15 GMT  
		Size: 223.4 KB (223364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b04a1708fbc0147d4ef6fdeb564449a7a41b7b0e5df2aa27a1441946c81598c`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66b8e9453e2d649488c8d053b0d1d4ae5e3740489586c6bb32f7eae7a3ec003`  
		Last Modified: Wed, 08 Jan 2025 21:29:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:641f93fddb6e6a668353356d78a708a17b7271ab06e13c5d2d1645d499c65794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1511f0eb48159856515b99abf8dee3e56263f52094148ce660d713454d210ec3`

```dockerfile
```

-	Layers:
	-	`sha256:55e5c3dc4287df2df2d9e20c08f5cd46d57a5616350e241f492bf844c18956d1`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 72.2 KB (72179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f348d15a848da4a767fe70750751a3015a5b347ab3175554ad77137d71526a`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:79982546d0bed357c3b7f570dab84958af0f189249fe28e89577d41749385d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3596676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84f4d20594fd72e32a00a9feabc004f2a01714cd681f91d6012c8315cb905ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Tue, 14 Jan 2025 20:50:16 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afdd5abd6a9641f814dc31398b1f41f1208ca3c43eafd4a1c8885cb772431cc5`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473a53dcc89c2068574226fb084968b4ffe7be1af4300f024b632369f8a8c233`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113dcefb1595560f60660ee7a991d2b59509bc30e01ceddb44741db3ef240384`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 215.8 KB (215788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659fa19d2020016e65ba76874ea424e5842bf892ef9cbb0fb225538f1e187cf7`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff65919c3bd12f584108c1e36a3685a85470a54c58c385eb56d95175f5ab8c`  
		Last Modified: Fri, 10 Jan 2025 16:34:52 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1fe29fb7531300754b92edf6a17cb43bbf6bdccf3669dda2f135e21ecd7bc35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d832c44e71bd3c5c8e4af761656415c7160b797f2992b90ae6ccd9ad1d3bae`

```dockerfile
```

-	Layers:
	-	`sha256:22ce3c1ef9750e4e84284967ee5eccca34b598a38edbca4cd170feb5ca477190`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 72.2 KB (72175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aff322ae82649ec4042d09e767199a7e60414c2658b767de2a09545e6bc998d`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e65076fea6d36aa50870267c91ec6d95243f1fb11c28be61a1d14cc261f1cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3684480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f24babcb5d8bb3f6840a272a25b4d6bdcfcea3fcb3a940801065c5753d9538`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe78366bb027e03c42216a6e1d382df7a3ee78f1471f4c62ff2d535ec78d8ce`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644fc493adbda1d67b109c8285fbc4e3c1d916ad0fdd4e52b1d30d0c3b5a8b83`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 7.6 KB (7558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b5aca5c5549a3999391bdaf9bfdf23ae037d07dd0278bcc20a847480979e45`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 212.2 KB (212205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176ea9af669d43767bfdf3ce63602addb4cf802565986d5dc091d471acc30fe8`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93146a4a9bfc5584cd3df6a564e1f4ed3da6472cd8f41e6e08d7031d0c8114`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:93f271bcfc043724cd8ed10b5a81e091db12c7c9d2e449003a555df7b3164e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 KB (86446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e388d85c4a8c82382bf1c9f50c1c9b6f983abffb8517c5e88afc7ecb4b51d7af`

```dockerfile
```

-	Layers:
	-	`sha256:2f690c178f9bae18125b1de0d54e1b4493b26e2f974141f5f5fd3c9d3a20c6cb`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 72.1 KB (72145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8043e5e2fb4d14db768fcedf2f5c98e22493faee4d4820a99c0fb644ece380fc`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:3defbc7042c9287d78d336478981bdf2410928e48fd8a9504755509633620376
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:alpine` - linux; amd64

```console
$ docker pull spiped@sha256:924e7f71ff8a6210c218250cadec128119d344f463da73b7435727f3b79f8b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3860004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002ee6ce7d381016e688df520b2d8e452892442cc9dd7d7fe4f2fd27e10bd9cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4d648a75810ee71e4a811a07ea0f0ac2c721e73e72187e9a1516d4c4c5ee6f`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe07a72f4be9ce0f108da046cf545981624f6b49403d76321af17c0c395f286d`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda92c005435cc07d0f9aeede336b39adeacb3d2b63892bd145844c2ffdee52b`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 224.8 KB (224801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d408faf96bb5ca591f0228176fd9fe8fcadf008b4a1d270852fc8c6e4ba93ef1`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e29defa7a55825f8f61eda130cb04ee394d66bd712f70709ac7053a248548`  
		Last Modified: Wed, 08 Jan 2025 18:12:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:bbb6e45e7eb3500533fd5eb9b6e02cbb71696097c25c94d70ad5011ff89719b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ed9b89a1c4bf4f119be92f17b9244feb5432b0aa95a99a543b91711e64d2ff`

```dockerfile
```

-	Layers:
	-	`sha256:d6dbec5f27c384596dd421778e731d1e085e3759f6d847458fe59a756fb7ac42`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 74.1 KB (74096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb9a321a7ee93632ee08168238d08c393bd8977dc0b90058743b7578fd3ffc57`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3b33305e723d928de0ceb007a192d635fbcead1966adcef42495013c151ab1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3908b8302a74d29d2ba4f9fad53ec5dae4d694c59ef5e425f9d3b4ae6f8e82c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Tue, 14 Jan 2025 20:34:27 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af3f0630555eb148818822fb59b573ef21353f360d8de1a31a9d923807ee4cd`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779a48568101672a32588570e7ceef7c0674397cbfa25ee720cde2859ab94873`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 7.5 KB (7549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a21818ff816934f603fcd2d4cba9f12db282bab07e3069da21d7578259ccec`  
		Last Modified: Wed, 08 Jan 2025 21:50:17 GMT  
		Size: 209.4 KB (209360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908425f61ccde4470882b7fc3250f120af7e457373de37561ca1bc2c428156fb`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d99959ccf8e07e46905c21480b4a1efde735673420d31417427ecef2146095`  
		Last Modified: Wed, 08 Jan 2025 21:50:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b7cb53f249d979d695f81563768605e871ddd1ea8a0819dd8dd81dc4987a573f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755f963c27fded64f7e3f6ff08da27dc1fd056f8030a81de4cb41f27e65d037b`

```dockerfile
```

-	Layers:
	-	`sha256:696c936ae51f846bce7be1a6d2dde5c03aa3b71ffda41e1e6b2cf2a621f6cd97`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 14.2 KB (14189 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ae8dad9afbb0cc8a3d199d4f081244152b6bb25a314d1c1b53d2015cb7a3148c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3307454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4e1533dc661a40478a134b3fe58301335db42d8f87ae18e6918ff38e81ae91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Tue, 14 Jan 2025 20:45:20 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7fdb315d3c34eb6935e1b7deb703093f5317800ff4d8b3936d5f771137cb79`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3360ef971eae752027c0ac2e924cac0c91b7f45b5099026b2a8f4be3279f6b5`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70480e7090e82ed5e217b413501ec1d1ac188d14349be7aa351d6ebc4bfa572b`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 203.0 KB (202981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa024b8e7a4dcd96a95ba7c408a6b6bf086e89742d975c9ce4fdfcfc7cabc1b`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4350bd55dee2c6c0b00a05b33f36a79b911cbfa491acf490c5bdc593d8e3e547`  
		Last Modified: Wed, 08 Jan 2025 21:55:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:374da430416cd603b6845710a7b6b98de8856fb9d596f167daa655438d68910f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfb7685b3853e3be4a1172afeae58a3bd43dbc7f6bf21565a8d6843e6b79559`

```dockerfile
```

-	Layers:
	-	`sha256:d4af9f6a3307489ccc6bd25b80644c322c26bf5739a42dab919b2dc03edff9ab`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 74.1 KB (74132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d585d482698adea511246e8d288a1602e3c63dc4f235cfa0915b12ae4b080f64`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:3565ca7a9021c033aa2f9aa3fa95ec43241003635fa8669990453c55ff55e1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa0a984328f7027e356ee0aa46ff85666d4fdeec5eb2d5343a30a9dbe998445`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f2d3fc3adfdd301f5e24f24c5392b9879a1b61f182e7752a21cb03e6aeb04`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d972687789bff098d9b33d09c024319254bdf8dcd29abb2bf072809733c79f49`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37195bfd737aa3f22ef0dd56d792afbe7e88b9c83db3bf0e69cb557d04d0d152`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 219.5 KB (219522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9420b682506ca5859fc3f4af6d59a5ca6fb329a69a869e8d7d0766374eb87ae7`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f38e672eaca427117d78c3580183cebdd51913b95165f7a4fecbb7219aeb29`  
		Last Modified: Wed, 08 Jan 2025 22:06:49 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c1545d907101296a82932a434f77b80a720493d1f158f28037a360c849c6b869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af58e3c42e72d2f836cf482efb095b5869000f90e0fd8c744622051f65cbeb6`

```dockerfile
```

-	Layers:
	-	`sha256:802dad5a525c4dc8453a7af1d74e5f8e0f8e9db9e0b53075b1abb70ebcbcac58`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 74.2 KB (74152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31d587a383d8f42361fc2623919a7a23e16261c7eb1f51cb4aa140497be4935`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:92342ba21763b953dae5124e2470d7b310cdec0e1aa1c278c715dda9eb6c5a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a710174a0b36bde4dc08b5531a97264b1a956e7b607e3cb81fa4ed42446333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01646177e05c873338d049d0058c8cd923326812215a3897564adbd669ee56f`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf3460ecbeac950e26287d1cf9fdf47918bf993988d851835f852bbd5707856`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69044b34b50595fbdc42e577dc79e206d3962968154ec6fbf18024dfe607c6cd`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 235.4 KB (235383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2fe84ec006ef02b90eb19d8de0f72b59b1f5d3cad78ef6d043f1ea320d121`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8feb2512bb10b2b05cf6ac1f623ac53ae1aaaf4d759aa98618bf0a96439d0c`  
		Last Modified: Wed, 08 Jan 2025 18:07:24 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f82eea4e46a614570a5475a2c2999ebdb44416593095c39bfe597dfb70954205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 KB (88337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c43d43c6b18f013ddf9e79c05395cc1213c96194b62e9231a34602566ed737c`

```dockerfile
```

-	Layers:
	-	`sha256:662bb99fc24ff68d14f1e276dc7da9f11ef9f56131659d2a511578d1c4547a4e`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 74.1 KB (74071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab4679badb23f30ba84ac1e7ab274f8693e730ac87dbfac78c97707c071c360`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:62a8529f4a88431c2c8453c2198b9f19f5027af08967a818ceb2e9f5485a2d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3806729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b6428f7bf466f0e03b157ec2507c547f21126e87e9b2e288213771e8ccfd2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d50e862e95a905933f50b6440c968976a25afd06a9808138b7b662be556076`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca1e9dba23dfea2ee87d2657bcd8e5e57a74b668b777c31cdf12a5a688c9e23`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b2864e003337f2f79f0ebbd5d8f47c821a711805de5ac4aac9a3f02a5d06b3`  
		Last Modified: Wed, 08 Jan 2025 21:29:15 GMT  
		Size: 223.4 KB (223364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b04a1708fbc0147d4ef6fdeb564449a7a41b7b0e5df2aa27a1441946c81598c`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66b8e9453e2d649488c8d053b0d1d4ae5e3740489586c6bb32f7eae7a3ec003`  
		Last Modified: Wed, 08 Jan 2025 21:29:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:641f93fddb6e6a668353356d78a708a17b7271ab06e13c5d2d1645d499c65794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1511f0eb48159856515b99abf8dee3e56263f52094148ce660d713454d210ec3`

```dockerfile
```

-	Layers:
	-	`sha256:55e5c3dc4287df2df2d9e20c08f5cd46d57a5616350e241f492bf844c18956d1`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 72.2 KB (72179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f348d15a848da4a767fe70750751a3015a5b347ab3175554ad77137d71526a`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:79982546d0bed357c3b7f570dab84958af0f189249fe28e89577d41749385d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3596676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84f4d20594fd72e32a00a9feabc004f2a01714cd681f91d6012c8315cb905ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Tue, 14 Jan 2025 20:50:16 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afdd5abd6a9641f814dc31398b1f41f1208ca3c43eafd4a1c8885cb772431cc5`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473a53dcc89c2068574226fb084968b4ffe7be1af4300f024b632369f8a8c233`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113dcefb1595560f60660ee7a991d2b59509bc30e01ceddb44741db3ef240384`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 215.8 KB (215788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659fa19d2020016e65ba76874ea424e5842bf892ef9cbb0fb225538f1e187cf7`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff65919c3bd12f584108c1e36a3685a85470a54c58c385eb56d95175f5ab8c`  
		Last Modified: Fri, 10 Jan 2025 16:34:52 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1fe29fb7531300754b92edf6a17cb43bbf6bdccf3669dda2f135e21ecd7bc35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d832c44e71bd3c5c8e4af761656415c7160b797f2992b90ae6ccd9ad1d3bae`

```dockerfile
```

-	Layers:
	-	`sha256:22ce3c1ef9750e4e84284967ee5eccca34b598a38edbca4cd170feb5ca477190`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 72.2 KB (72175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aff322ae82649ec4042d09e767199a7e60414c2658b767de2a09545e6bc998d`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e65076fea6d36aa50870267c91ec6d95243f1fb11c28be61a1d14cc261f1cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3684480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f24babcb5d8bb3f6840a272a25b4d6bdcfcea3fcb3a940801065c5753d9538`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe78366bb027e03c42216a6e1d382df7a3ee78f1471f4c62ff2d535ec78d8ce`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644fc493adbda1d67b109c8285fbc4e3c1d916ad0fdd4e52b1d30d0c3b5a8b83`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 7.6 KB (7558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b5aca5c5549a3999391bdaf9bfdf23ae037d07dd0278bcc20a847480979e45`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 212.2 KB (212205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176ea9af669d43767bfdf3ce63602addb4cf802565986d5dc091d471acc30fe8`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93146a4a9bfc5584cd3df6a564e1f4ed3da6472cd8f41e6e08d7031d0c8114`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:93f271bcfc043724cd8ed10b5a81e091db12c7c9d2e449003a555df7b3164e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 KB (86446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e388d85c4a8c82382bf1c9f50c1c9b6f983abffb8517c5e88afc7ecb4b51d7af`

```dockerfile
```

-	Layers:
	-	`sha256:2f690c178f9bae18125b1de0d54e1b4493b26e2f974141f5f5fd3c9d3a20c6cb`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 72.1 KB (72145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8043e5e2fb4d14db768fcedf2f5c98e22493faee4d4820a99c0fb644ece380fc`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:2725f394d1c055b793a69764c862103d5fbd88a70531a3ed67a000071fd9b698
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:latest` - linux; amd64

```console
$ docker pull spiped@sha256:0807efe8e57e7a74993be6066b8c4d4917a1f6e3611dd0833309a2f48e69d189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37086272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43af49e196ea5b3803a09fb654b9f3a31809b1d63db50efadc92753d2a5ea1b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb387415fb818a8b4d56b6c4b1981b2212e57ec6addac3a80cfb2b9d9331b50`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228fe3a70b06fc8ca22481663a32d8b20b71b4a1cc2ef6bad63851b3cddc6a02`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 2.4 MB (2401340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bdc698a91b053c8c6c8793884aeb21f069855e2f35ceaf6d354563a622ec60`  
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 6.5 MB (6470976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562950f9b4e1da298d9932319a15c677ac7b1072f4a6218a62318ec083a438bf`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d26d7b3a2a6d5bfa2d8845580756d251c7acbb85868393a8dc4b15857a936c`  
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:4596a995a081e15712ce75ccbd6382c0362bbb99730c9b479c48fb6deb3de184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb27c549da9cd3fd74e3b201a56fe8440fe2368fbba1fa80abc7dac9262ff93`

```dockerfile
```

-	Layers:
	-	`sha256:d833741283a7f0cc036493894e91aa8f599339f065480034207be52408751f12`  
		Last Modified: Tue, 14 Jan 2025 23:04:24 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab16c690e615571a539221290f9c7154ed500a5de18d47dfbe3d130daff486f`  
		Last Modified: Tue, 14 Jan 2025 23:04:24 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:7ac314027d6a9a74b545bac6a566bab81092bc05f703e8e7feb689f1156a5820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32873874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f112ee2db55ec556284a0e51dab6d903a978b3e1a2817a609a226b6b833092`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 20:33:17 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d02c24549d50cc08f67dd0716935f9fa89992a0a0c1150357bba3bd55a0c1e7`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3c5e73b2f407694f10795c56fde8bcb539c9e2933731585f42dca1b1ace55f`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
		Size: 2.0 MB (1997177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a7e5af36cc87bcf1b73581be95f889fec6304edf80fae57e11543596a65d0b`  
		Last Modified: Tue, 14 Jan 2025 06:07:50 GMT  
		Size: 5.1 MB (5138490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecae1535903b4c1e77ac1ed96f21bd16112f406ad7f1531a331a8cd8bfcfa55`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff755cd6a71e19c14b557cb2ed1fe6c253d3a1f3539ecd08e66d6407b67d9ab5`  
		Last Modified: Tue, 14 Jan 2025 06:07:50 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:5550758ca3d10700c01f4a5f7e2dcc5e0a8bc81017e7a77563cc9e9d98b07ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc4f32a396e255a44a51de0250cbf8899e01021fdaf2877d4c981165ff96278`

```dockerfile
```

-	Layers:
	-	`sha256:2dfe195d70effae453580ecf74321962ef95b82e15bb2544354013d50bebb18b`  
		Last Modified: Tue, 14 Jan 2025 23:04:26 GMT  
		Size: 3.5 MB (3486344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d991ae0cd962a40b1a96f846b396fb35fb42d45ca1a7ffa955e1720f73fa9707`  
		Last Modified: Tue, 14 Jan 2025 23:04:28 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:cf5df2fe01fb9d92b1e5cb28bada0fa5ec279ec78e62c0ee49cc27a8baa06bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30652158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542aca3ffd11814f62e05ff8668c4fb3dff51d8dc3c1db06624b08d47f8f1980`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8717c624029ee40d56a1c31652eaf6ccf71a5567d7758a126900c0de1bcfad4`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b317980174023f6d6d78a005ee029285173f59fce3edc99c447ab905dfd179`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 1.9 MB (1855562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c382dfc5377b730c1b9c7edaff5880dda394c11f91a13f8946755dc7d81cf6d`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 4.9 MB (4880456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6267a4e0459f5d1157f3859e3edbabf7657d48de59e6c177fd3d1cf9114f73`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d786240c1a6e6bbdfc3fe94803ef3170f1198c85e7bb159452e0e2e512d162c`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:d9ba01708f3467414bc4781b45309ee70543bcfbd71a0484cedea151e2068d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3500977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f868daab95ccaa02d7e27af7666f2f1a087ae16fae21fbde97f5bd395594bb6`

```dockerfile
```

-	Layers:
	-	`sha256:8ce0204d70a42133258f980adb2349457dbdb8f72be802bed32e6bb1e0e0ddd5`  
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
		Size: 3.5 MB (3485835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a0ec541bf556f8901ffbee01629c3a659a0f7db4cc58f578ffad9de316eb6cf`  
		Last Modified: Tue, 14 Jan 2025 23:04:29 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:ca50c1b1c64713d8110875a1f34775fc38040451acc500447a3622392bf2769f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35770669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772b7d61276d94b67963fb9f20b85927c2b84f7a0f63253fa64d274982b1f130`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3d076ceae3499abc00492adc7b101408d72437a499e4a9cea20964e90c3765`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0214df3970acd6fea09000d0df47a3cee908490cd9b760e15bd23ad7aa3cf552`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 2.2 MB (2247012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2354092ea972f14ee9af251fc4714c734d8cd2c30834f655c2ea396610489655`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 5.5 MB (5481085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d572dacd78b347329872172960cc26ce37ee9b7ac42a83ddc7425ad149add9cb`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e699072832a75d28646bc8d1b28f5ee412affda7e0b1e8469893f897fc236810`  
		Last Modified: Tue, 14 Jan 2025 06:38:45 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:d900c3ed70ec4adfcdeddd4771c0e2f9759b1cae7127b1122c5a54e1c910a28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3283792d48abf7c1421ee1439a40dfbe273c495208c163da83ef6da25092911b`

```dockerfile
```

-	Layers:
	-	`sha256:44d25165467985f6f9d9cf10d0306bed5af4e2ad6406371dc516b77fdf3a2ff3`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 3.5 MB (3487042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec8b87f83866e1f34c08767b42d87be6e439e3737291318890b05e17f026397a`  
		Last Modified: Tue, 14 Jan 2025 06:38:44 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:50dc383a39b7bbf8bc7274000476568ef19f00fa47f5e77a3b945e542d602e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37529245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff3adfb5bcb041fd776f222523c7e5f7d316c3a84275c48f8a469520e3cf670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9757c47c7f65469fabaf649c24c76e71b0ee344186b7378388e73b9ff3584956`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41f696ea1cea6b748d59acb3f0e93feb73a67b208dc03bdd8d489b78b8c4c1c`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 2.4 MB (2398649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241faa93dbe7603d3ddfe8143dbc5f7e9990a80036efae46f8147ce9b8e684d7`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 5.9 MB (5941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac324e1750c72f49ee4d4c3b000ae242266e9e9b1946584a5a221c6d4b01bbe9`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f5c66d701ad1b4e0469df5595f673c4d111557d936709a7c5ab15e2ca0f378`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:78318e0a0bae94e38b3a5d9c7578f6751580c7038fd2e2660d4d7cc768105076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed705c7a2f1d4214425c51ed536dd3d3ab550dfbe9a1b50c38de8bba85e59791`

```dockerfile
```

-	Layers:
	-	`sha256:b0eb158509e496490a1fa281c429ec733f8201538a8ead508644c888a4a09018`  
		Last Modified: Tue, 14 Jan 2025 23:04:35 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e8230d3f815bb664e5eda60129ff633bc7d34854e10e52903d538454410d33`  
		Last Modified: Tue, 14 Jan 2025 23:04:35 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:c01ffa398018e931ac10ce62e16a6625947a0fcc8a2293eade003a3c6b3ab862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36132905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fb4e4e2a5078ea045150d8177a114a04293312c91ebd35e93cb59f1e2259e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 20:36:28 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252230c34678f565279955a422dad63275a16eeef208147f154e13e5647df2ed`  
		Last Modified: Tue, 14 Jan 2025 18:08:24 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f980dd5eb6de9195670967164c2a6d21dfc4bd270afc766fc82f7303fcea879a`  
		Last Modified: Tue, 14 Jan 2025 18:08:25 GMT  
		Size: 1.8 MB (1841121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fde05de7416ebc2e722610c9c2dc2ff46e18c6ef77c23e6e4dd9dcee7c809c4`  
		Last Modified: Tue, 14 Jan 2025 18:08:25 GMT  
		Size: 5.8 MB (5803593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7fe7c8e4867db382a8bf9a5c5bbd8cf77ba59015bd2dae591763292f1a7687`  
		Last Modified: Tue, 14 Jan 2025 18:08:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2345d9838a2e18ef7406ff0df0a5dedb563ffa5c105d7e69074a1599a12e35b8`  
		Last Modified: Tue, 14 Jan 2025 18:08:25 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:ac952f287cc93e8b3d1962734d5e6d7b7fea48269365cd58ff092baa9691aba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8839767e2b373c2b310dd1f060d29a21907bda9cf88c7ee7eb3bfea9d99af4c6`

```dockerfile
```

-	Layers:
	-	`sha256:edffc4065fe5a50cf43009afbdb9c8d5dc04651bc8b0abafa3baa3ed0ff073d3`  
		Last Modified: Tue, 14 Jan 2025 23:04:36 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:e0838362e10a88cedb5ebf5d4c38e86e979cb384e1bf72965f8839333fa63baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41051304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5145bd62627fce56a871970f71c1423bf8e7bd302f8e8c8cfdb7a4c492dce6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048adc09f28a34691cbfb26824234082fe589f23a9fa178a80bd0a97e36157ae`  
		Last Modified: Tue, 14 Jan 2025 05:12:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06163a828f03667776915ff22220e1c76e276331d5b5553d9d91f54f6e1b0be2`  
		Last Modified: Tue, 14 Jan 2025 05:13:00 GMT  
		Size: 2.6 MB (2582093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4e996ae8bb5769e51b9acf136d0daaec2939316030203ad6bfa9ee6e82658b`  
		Last Modified: Tue, 14 Jan 2025 05:13:00 GMT  
		Size: 6.4 MB (6422823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204877fb93a1bb0e23eefae6b5ecafcb745cca605fc4e56d05cf862c4f46ec06`  
		Last Modified: Tue, 14 Jan 2025 05:12:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ff3d47eee1c6ccd068d483c63d368a7a6b63c65285cc05761b023d365b9eb0`  
		Last Modified: Tue, 14 Jan 2025 05:13:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:2ac6faef580387afaac65a40852917553101f4b0bd349432d9fae7c1c34b8b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01442cee26b43c9b5f0e98561c25f1d8a7533dccea7b29f16318d0dbffb52a81`

```dockerfile
```

-	Layers:
	-	`sha256:07a1d36ee150774030a74edfb128021444921e2d3eff9710baf6e3a2539c33a2`  
		Last Modified: Tue, 14 Jan 2025 05:13:00 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e46605f5ae9d418c541c83eef4a80f85ac8f32ef307ca58ccab597614e90e0d5`  
		Last Modified: Tue, 14 Jan 2025 23:04:40 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:9a8b4589f022b01cb7379216c0ed4bcfd689c1534d89e1ba7feaaf8c2c7335b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34314999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bb0a694ef3ab84e988bb522551da84d245aa5de9bff71d4e174d5dee08f88b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de4963ba94159da6a677e9693e16f2aaca6406d4426d738af27c3ecc011e85e`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d01390fd75845fd56420f30cd57336b2c75946123f8fdef738b1ee09427359`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 2.1 MB (2068686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef25b97e48209f7c51f7ab797e7c2c9e939b8a05b5b8ca73c14e1c82838fcb22`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 5.4 MB (5386034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4f625a2f5c5cca8030def5f775ae31a6cc2f0f701ad190da0d260c82eb52cb`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fcd0f24724877817587b4569325c3d96d4f4f24e77572ca3f0ec447e622d0d`  
		Last Modified: Tue, 14 Jan 2025 04:49:48 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:cb0a11a3acd5c8d5fc548066b9664c5a715152b3f4999ee92005b77403c1a49e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b3f9cad8e646fdb0c0e919133c2cc5c6481b885ce2db546e37c5d2ff97e85a`

```dockerfile
```

-	Layers:
	-	`sha256:77bf42cd7e49ab8b25190be2a4044d6e977c9ddd06f1f4c7fcd6acb450e8e53b`  
		Last Modified: Tue, 14 Jan 2025 23:04:41 GMT  
		Size: 3.5 MB (3504000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf76c9e1d84fed3f30cb373ece1c7713dffbb1a40bd4018101999d0b899e9f72`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json
