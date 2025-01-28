<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spiped`

-	[`spiped:1`](#spiped1)
-	[`spiped:1-alpine`](#spiped1-alpine)
-	[`spiped:1.6`](#spiped16)
-	[`spiped:1.6-alpine`](#spiped16-alpine)
-	[`spiped:1.6.3`](#spiped163)
-	[`spiped:1.6.3-alpine`](#spiped163-alpine)
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
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
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
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab16c690e615571a539221290f9c7154ed500a5de18d47dfbe3d130daff486f`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
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
		Last Modified: Tue, 14 Jan 2025 01:33:27 GMT  
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
		Last Modified: Tue, 14 Jan 2025 06:07:50 GMT  
		Size: 3.5 MB (3486344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d991ae0cd962a40b1a96f846b396fb35fb42d45ca1a7ffa955e1720f73fa9707`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
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
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
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
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
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
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e8230d3f815bb664e5eda60129ff633bc7d34854e10e52903d538454410d33`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
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
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
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
		Last Modified: Tue, 14 Jan 2025 18:08:24 GMT  
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
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
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
		Last Modified: Tue, 14 Jan 2025 05:12:59 GMT  
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
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 3.5 MB (3504000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf76c9e1d84fed3f30cb373ece1c7713dffbb1a40bd4018101999d0b899e9f72`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:5c7e4d33c567ce2c052935664bdb5c40a55c846af284c06137e47ec234b2c041
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
$ docker pull spiped@sha256:bf4f80de0db396d644d3bd7d284f1a82968f2f5dca2d8cb33ba829c0043fa7e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1739bfd2f7c6bfc0aec39069cb0902b1e56873b04c7099b83047c17e17df1c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be090fd76d1e36f16806f586b6344fa2de641690144682cd6860b988c3c931d`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1155ce8a77b55d5a058c2b75baec72432a1a394f1d53956393a6e547ba0d7f6c`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9276e935161ceb34d567a8fa6cd5945c8199ddaa39aae106a6c0f34b646ff4`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 97.9 KB (97879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d015ce49382dcd762930d16d6a81450d9b389d35fb79ea80527841a68922f56a`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912bdaad70ad3037b03159d81278ab0dad9b2827a758dd7444163a7203f9314c`  
		Last Modified: Tue, 21 Jan 2025 19:28:19 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:379145c25a8027c2a34d73c76346518adda978e2b00e97869e108358e4b33437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28081c4e7942cc3a13ba88170d117e0ff67b48eaa690d6537b01bba98892a90e`

```dockerfile
```

-	Layers:
	-	`sha256:6625a81c2cffef3b41b47962b504e9dc20cff4471d4d6f1e5d96e14770cd2929`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 79.8 KB (79816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9fee5c0b25d256b52106b1fd933f9f04a617e9e2e3a7d2731ba142a1d8ba0fa`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:0c4472e3c5cd36e439567c13f5cd9a379aab66e0a915889d6d42baafbc2500ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3454044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a7cbce52f04ff9256292b0a9817ed2fa7941835bdeebeaa27869591dd7f9eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee72c2b1876a0156b7d396caf2dc29a0f8081b2b7a6733a3ff64d9527f586ea`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1da6fb0facd6416135ae0db69e959ecf3e75cab6ea327aabb4ead163825dfc7`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4bfb2112b9ff1da637fda9a1fabd68afd45961279bab992964a8bd6e31408f`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 80.9 KB (80855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074202ffcdbaa57f35bc530fa794482ecb273ad51046c53fe8043f01096270ba`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc4e41cff4eb7a1ada1c481fe378e5268751d48dcbbae7342d3241561661269`  
		Last Modified: Tue, 21 Jan 2025 19:29:41 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:366e5b0763df779aacdfe5468363ac3687088dd4e125b847daef76b5029a5661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7ede033b2a067297269492b9cc67391a8024877ed9a838acefe18b08c2e7b5`

```dockerfile
```

-	Layers:
	-	`sha256:464626d886af9ffe2ba5aac0067601f31503365fea01536d0142c873f5980371`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:0ae1d2d6cf54b9aa45265044ba111dd99c549b31e466c67d3afc3abec2fe3ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3181455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbc5512e44ca9ebcc11a994bb12f151c14c2878f9ed60b62665f1ef9e2dd061`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae962cfc489c298278551ba32bca1e0ed1f67cd05192848331b7c3ee926a77`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114d274ac423361940bdd6b0c7904acc23cb9903e6f1a2904b32a6b89f331c4`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60770baea6ea5185f492834462f47c3556209ae19718dec68186d538965228ca`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 75.0 KB (75035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0c2868e02a07fed49e900b254ea234eb48f25e37bc10f580198d191565de75`  
		Last Modified: Tue, 21 Jan 2025 19:30:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e555c89d083ded756b21c5bd510ca93d93cdc37921edd4764164ed46228bd95b`  
		Last Modified: Tue, 21 Jan 2025 19:30:38 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2c10a8c0cd22de6c2045282220f18a4879e5e74494a7d1945236baf2eb256760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58cb4a63496728162216d59f92073861eee5255f9c2edae3276a72c8777b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:7436f70191232399d4d7c405219fafb240274bd898d8ccd07f712aa394e7a86d`  
		Last Modified: Tue, 21 Jan 2025 19:30:38 GMT  
		Size: 79.9 KB (79852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce64a4a26bf1cd792d2cbba128afa6e7fb692cbf52d2fa21f5297938c26001ee`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:4f709a7af2244a5ff9f01387d5030ac4aa1c6c573254cd2266bf3100b9a813a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b82cd26698a5299c656bd15e65f1397979b455479ffdd415881455b92d1991`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987e71ee6cc5ab416ed1f0e49bb9a1696b4b5656b4d3fcc1feca517c7bbe5030`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faf545dafdf63442f66bf2d829b8ba0c5dd8fe81240a3298cbf9fee767c891`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2c84ea327537859da16a3a7c4061d3787af0f266934eb7228b7b3a162359f7`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 91.0 KB (91009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c519261ae45d672eb2ce96c696945b567ef14c566a912cdc782f8a6460f3a5`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c072a47e7cf1bb0073652f81348762878a297e164adca16bd19e1fbed0b7c8a`  
		Last Modified: Tue, 21 Jan 2025 19:50:57 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b5c38e6ae8441ca778cdfb5a4550cc780f4ef358f0a43882a3235e7eb9042be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff3d3634cf407a39a6e662cb942c48f9a3cd5a462a148837480d362d0d3b118`

```dockerfile
```

-	Layers:
	-	`sha256:1a07d546f1499b6116c2af470d73941c09865327e1d8c12e0e00d302b098b024`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 79.9 KB (79872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42e95337c10301d3e0c1a1a7dd5266eb9b51919a6979351d6ab21dd694353ae3`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 14.4 KB (14433 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:142927fc09806045217102e1fd61c9120693bb3437a64b4e53d45fff85604a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3580250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5191a7f4b9da1db034fdb1a2a191bfdbbaf0970362273c14cea5a8d67af9c59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66602b26aee70855e62f399265bc3d459bc2e17fe241dc09f542aea66a732d51`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754deefeb72f062211245a56424039263e88066669b4752e5509b96c3fc75976`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8aa827b00c14c831e4f20dad83f6c4f5e3f61faa06bd0d88a0513abd6919cb`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 107.8 KB (107820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4247d4a0214d8ebd8f0fc13a2dda2e237375c545239c856be1deee79b6db804a`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3260d2ef071d2a025027168328bd57243ca2fcb118e4eca7966966689d64c6a9`  
		Last Modified: Tue, 21 Jan 2025 19:28:00 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:4701fe7d0f9e827457a3849fd8edff76707b89ab2830cd1f661c6968daaf01a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191ca3b524a67e610d402501801e70d4ed64c7e0105ec47581b8221b04617eee`

```dockerfile
```

-	Layers:
	-	`sha256:b243e9db2d57fcb036e6456ffb5fa340acb65741007c7bdc9b4583b6a11fa23e`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 79.8 KB (79791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea95049f4e29abe2a4dbbe1d23dc82dc4e3bb876a61c9cb0ddcb0c6c3f53d6c`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:02217b126efda6419d593927c1e7afedbaae32a0dfac48527891fb61e326668c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3678657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336ce0a2b2749719b0875443f6719cc477728f9d9ca03aeb8fdd2eb80a7fd7bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937ae7bb7a53c30739164fd8d6b1af5449b91bdeaacb11c09da360a795e967b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed2b37b3a36511a8f8cde15ac74df12676c707a75cac7400604b533817a57b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 7.9 KB (7918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78388bac15c7f0679a8f61fec0fd44039e2dc31eb14e7adb586632c8938f4558`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 95.7 KB (95740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dca0f484333f1fbdab6b9693779c9f26be5962fe67e46f46ea2db75698a3d0d`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be1274653db549fd50a72850308000f30c9517f1d7b348cb82463adc3c4cc74`  
		Last Modified: Tue, 21 Jan 2025 19:31:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ed3fde57e25bf38537c7f0c1d97fbc836ebf868397090410e8909472f48a710f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db83784de2b8cebf42f5efb3510f46e989e3bb222c1d74a7ada0a21d3b477c3`

```dockerfile
```

-	Layers:
	-	`sha256:d4d5a0de95eb8f06fde7d4e9a71e8f41b6cc30a14ac230b76293cb5186635d37`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 77.9 KB (77899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f61dcb17bca36ef37c1782c7996fd97fc226af6a408695c157aae47d923bb1f1`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:8753a779e5087f28ca4abda0cdb7c4a28fa8732bf94201fc4f1c6749cac05e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3448196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972586fe36ea4a167e8c4e3dd294a605bd9e95559c656558021b297fc6a0e7d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410676c340782e10ad961429d12c4fc7bc22fe42e602f44af8fe4564583fa790`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb03e5e951a5c0dc5098e3f3712ba683716c2830cd781627b8c589f37e35d49e`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 7.9 KB (7900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725fe5f1d54360199e0c323ed9105f4b968c5b4e9ac846c5c3c41c9f67026998`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 88.6 KB (88643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561e0b8832db6b203f73cdc2a06f1f927f05044848e5a4c911efd349960c1299`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53e08b4d3b18487565f895fcc2e5aa406700b2e9589117a057f0d580eda17bb`  
		Last Modified: Tue, 21 Jan 2025 19:47:11 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:433e9af8a8aae1b47091598b315936f3260b19614787199011d74195be92071c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f61d9865b72e236614e5628bcb24f39a6039f498ece96818cdbce448c511329`

```dockerfile
```

-	Layers:
	-	`sha256:79b96efba8cf867f9e9e2cb09b95054474af816599fa19ea5c5fa0ff4b799030`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 77.9 KB (77895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2249ad8997aa1b69cf185889e51eeaa77a5fbe77b0dcf1b762154def0237b80`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:2d7e1c9817e385b181b3bc711b36578549be6951515e90c415628765f463a86f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3561031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854dee3cfd59deb9dfb570b45c1fc1a4289fa0cce595a8c460b4ff4e38de33ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2d0ea9a1061fe840c13a046b93faaeb9dbcf4357f53a37b83747a395c05279`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068b14e90f05cd3c9537d5988b4bbe6abead4cac15a8b25d1959964036cdbb13`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd06766d16512bbe8f937e09b7f90223e29e8e4f0d7306052387f4bdd5243406`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 84.9 KB (84859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdfee3855ba5896fd063d555eea5f8b0895168a4ba8162a475fce6bbb3cd631`  
		Last Modified: Tue, 21 Jan 2025 19:32:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb327b9c33b07ca822f14e1d5eb0e89aa67aa294ba7fc97ceb881ba83258645`  
		Last Modified: Tue, 21 Jan 2025 19:32:38 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:cf5e04de8914015fdfced9fd2350f25ae04499716af67e6870cadcaa694a5944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a90ae2d8e21694ed59a7386bfdd6650236725793931430a24f9d8a8ac24fab`

```dockerfile
```

-	Layers:
	-	`sha256:a3e79339ec578c35ce808cf83d83181d2070408631264fce657e406f892754d9`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 77.9 KB (77865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d28c39be10ea42747404de7a4952b61efc3419f395d546ad85727355d0bdbd5b`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 14.3 KB (14299 bytes)  
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
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
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
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab16c690e615571a539221290f9c7154ed500a5de18d47dfbe3d130daff486f`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
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
		Last Modified: Tue, 14 Jan 2025 01:33:27 GMT  
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
		Last Modified: Tue, 14 Jan 2025 06:07:50 GMT  
		Size: 3.5 MB (3486344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d991ae0cd962a40b1a96f846b396fb35fb42d45ca1a7ffa955e1720f73fa9707`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
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
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
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
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
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
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e8230d3f815bb664e5eda60129ff633bc7d34854e10e52903d538454410d33`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
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
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
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
		Last Modified: Tue, 14 Jan 2025 18:08:24 GMT  
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
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
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
		Last Modified: Tue, 14 Jan 2025 05:12:59 GMT  
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
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 3.5 MB (3504000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf76c9e1d84fed3f30cb373ece1c7713dffbb1a40bd4018101999d0b899e9f72`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:5c7e4d33c567ce2c052935664bdb5c40a55c846af284c06137e47ec234b2c041
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
$ docker pull spiped@sha256:bf4f80de0db396d644d3bd7d284f1a82968f2f5dca2d8cb33ba829c0043fa7e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1739bfd2f7c6bfc0aec39069cb0902b1e56873b04c7099b83047c17e17df1c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be090fd76d1e36f16806f586b6344fa2de641690144682cd6860b988c3c931d`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1155ce8a77b55d5a058c2b75baec72432a1a394f1d53956393a6e547ba0d7f6c`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9276e935161ceb34d567a8fa6cd5945c8199ddaa39aae106a6c0f34b646ff4`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 97.9 KB (97879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d015ce49382dcd762930d16d6a81450d9b389d35fb79ea80527841a68922f56a`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912bdaad70ad3037b03159d81278ab0dad9b2827a758dd7444163a7203f9314c`  
		Last Modified: Tue, 21 Jan 2025 19:28:19 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:379145c25a8027c2a34d73c76346518adda978e2b00e97869e108358e4b33437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28081c4e7942cc3a13ba88170d117e0ff67b48eaa690d6537b01bba98892a90e`

```dockerfile
```

-	Layers:
	-	`sha256:6625a81c2cffef3b41b47962b504e9dc20cff4471d4d6f1e5d96e14770cd2929`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 79.8 KB (79816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9fee5c0b25d256b52106b1fd933f9f04a617e9e2e3a7d2731ba142a1d8ba0fa`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:0c4472e3c5cd36e439567c13f5cd9a379aab66e0a915889d6d42baafbc2500ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3454044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a7cbce52f04ff9256292b0a9817ed2fa7941835bdeebeaa27869591dd7f9eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee72c2b1876a0156b7d396caf2dc29a0f8081b2b7a6733a3ff64d9527f586ea`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1da6fb0facd6416135ae0db69e959ecf3e75cab6ea327aabb4ead163825dfc7`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4bfb2112b9ff1da637fda9a1fabd68afd45961279bab992964a8bd6e31408f`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 80.9 KB (80855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074202ffcdbaa57f35bc530fa794482ecb273ad51046c53fe8043f01096270ba`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc4e41cff4eb7a1ada1c481fe378e5268751d48dcbbae7342d3241561661269`  
		Last Modified: Tue, 21 Jan 2025 19:29:41 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:366e5b0763df779aacdfe5468363ac3687088dd4e125b847daef76b5029a5661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7ede033b2a067297269492b9cc67391a8024877ed9a838acefe18b08c2e7b5`

```dockerfile
```

-	Layers:
	-	`sha256:464626d886af9ffe2ba5aac0067601f31503365fea01536d0142c873f5980371`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:0ae1d2d6cf54b9aa45265044ba111dd99c549b31e466c67d3afc3abec2fe3ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3181455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbc5512e44ca9ebcc11a994bb12f151c14c2878f9ed60b62665f1ef9e2dd061`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae962cfc489c298278551ba32bca1e0ed1f67cd05192848331b7c3ee926a77`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114d274ac423361940bdd6b0c7904acc23cb9903e6f1a2904b32a6b89f331c4`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60770baea6ea5185f492834462f47c3556209ae19718dec68186d538965228ca`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 75.0 KB (75035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0c2868e02a07fed49e900b254ea234eb48f25e37bc10f580198d191565de75`  
		Last Modified: Tue, 21 Jan 2025 19:30:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e555c89d083ded756b21c5bd510ca93d93cdc37921edd4764164ed46228bd95b`  
		Last Modified: Tue, 21 Jan 2025 19:30:38 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2c10a8c0cd22de6c2045282220f18a4879e5e74494a7d1945236baf2eb256760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58cb4a63496728162216d59f92073861eee5255f9c2edae3276a72c8777b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:7436f70191232399d4d7c405219fafb240274bd898d8ccd07f712aa394e7a86d`  
		Last Modified: Tue, 21 Jan 2025 19:30:38 GMT  
		Size: 79.9 KB (79852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce64a4a26bf1cd792d2cbba128afa6e7fb692cbf52d2fa21f5297938c26001ee`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:4f709a7af2244a5ff9f01387d5030ac4aa1c6c573254cd2266bf3100b9a813a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b82cd26698a5299c656bd15e65f1397979b455479ffdd415881455b92d1991`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987e71ee6cc5ab416ed1f0e49bb9a1696b4b5656b4d3fcc1feca517c7bbe5030`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faf545dafdf63442f66bf2d829b8ba0c5dd8fe81240a3298cbf9fee767c891`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2c84ea327537859da16a3a7c4061d3787af0f266934eb7228b7b3a162359f7`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 91.0 KB (91009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c519261ae45d672eb2ce96c696945b567ef14c566a912cdc782f8a6460f3a5`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c072a47e7cf1bb0073652f81348762878a297e164adca16bd19e1fbed0b7c8a`  
		Last Modified: Tue, 21 Jan 2025 19:50:57 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b5c38e6ae8441ca778cdfb5a4550cc780f4ef358f0a43882a3235e7eb9042be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff3d3634cf407a39a6e662cb942c48f9a3cd5a462a148837480d362d0d3b118`

```dockerfile
```

-	Layers:
	-	`sha256:1a07d546f1499b6116c2af470d73941c09865327e1d8c12e0e00d302b098b024`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 79.9 KB (79872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42e95337c10301d3e0c1a1a7dd5266eb9b51919a6979351d6ab21dd694353ae3`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 14.4 KB (14433 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:142927fc09806045217102e1fd61c9120693bb3437a64b4e53d45fff85604a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3580250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5191a7f4b9da1db034fdb1a2a191bfdbbaf0970362273c14cea5a8d67af9c59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66602b26aee70855e62f399265bc3d459bc2e17fe241dc09f542aea66a732d51`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754deefeb72f062211245a56424039263e88066669b4752e5509b96c3fc75976`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8aa827b00c14c831e4f20dad83f6c4f5e3f61faa06bd0d88a0513abd6919cb`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 107.8 KB (107820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4247d4a0214d8ebd8f0fc13a2dda2e237375c545239c856be1deee79b6db804a`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3260d2ef071d2a025027168328bd57243ca2fcb118e4eca7966966689d64c6a9`  
		Last Modified: Tue, 21 Jan 2025 19:28:00 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:4701fe7d0f9e827457a3849fd8edff76707b89ab2830cd1f661c6968daaf01a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191ca3b524a67e610d402501801e70d4ed64c7e0105ec47581b8221b04617eee`

```dockerfile
```

-	Layers:
	-	`sha256:b243e9db2d57fcb036e6456ffb5fa340acb65741007c7bdc9b4583b6a11fa23e`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 79.8 KB (79791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea95049f4e29abe2a4dbbe1d23dc82dc4e3bb876a61c9cb0ddcb0c6c3f53d6c`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:02217b126efda6419d593927c1e7afedbaae32a0dfac48527891fb61e326668c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3678657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336ce0a2b2749719b0875443f6719cc477728f9d9ca03aeb8fdd2eb80a7fd7bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937ae7bb7a53c30739164fd8d6b1af5449b91bdeaacb11c09da360a795e967b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed2b37b3a36511a8f8cde15ac74df12676c707a75cac7400604b533817a57b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 7.9 KB (7918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78388bac15c7f0679a8f61fec0fd44039e2dc31eb14e7adb586632c8938f4558`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 95.7 KB (95740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dca0f484333f1fbdab6b9693779c9f26be5962fe67e46f46ea2db75698a3d0d`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be1274653db549fd50a72850308000f30c9517f1d7b348cb82463adc3c4cc74`  
		Last Modified: Tue, 21 Jan 2025 19:31:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ed3fde57e25bf38537c7f0c1d97fbc836ebf868397090410e8909472f48a710f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db83784de2b8cebf42f5efb3510f46e989e3bb222c1d74a7ada0a21d3b477c3`

```dockerfile
```

-	Layers:
	-	`sha256:d4d5a0de95eb8f06fde7d4e9a71e8f41b6cc30a14ac230b76293cb5186635d37`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 77.9 KB (77899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f61dcb17bca36ef37c1782c7996fd97fc226af6a408695c157aae47d923bb1f1`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:8753a779e5087f28ca4abda0cdb7c4a28fa8732bf94201fc4f1c6749cac05e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3448196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972586fe36ea4a167e8c4e3dd294a605bd9e95559c656558021b297fc6a0e7d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410676c340782e10ad961429d12c4fc7bc22fe42e602f44af8fe4564583fa790`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb03e5e951a5c0dc5098e3f3712ba683716c2830cd781627b8c589f37e35d49e`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 7.9 KB (7900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725fe5f1d54360199e0c323ed9105f4b968c5b4e9ac846c5c3c41c9f67026998`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 88.6 KB (88643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561e0b8832db6b203f73cdc2a06f1f927f05044848e5a4c911efd349960c1299`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53e08b4d3b18487565f895fcc2e5aa406700b2e9589117a057f0d580eda17bb`  
		Last Modified: Tue, 21 Jan 2025 19:47:11 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:433e9af8a8aae1b47091598b315936f3260b19614787199011d74195be92071c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f61d9865b72e236614e5628bcb24f39a6039f498ece96818cdbce448c511329`

```dockerfile
```

-	Layers:
	-	`sha256:79b96efba8cf867f9e9e2cb09b95054474af816599fa19ea5c5fa0ff4b799030`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 77.9 KB (77895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2249ad8997aa1b69cf185889e51eeaa77a5fbe77b0dcf1b762154def0237b80`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:2d7e1c9817e385b181b3bc711b36578549be6951515e90c415628765f463a86f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3561031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854dee3cfd59deb9dfb570b45c1fc1a4289fa0cce595a8c460b4ff4e38de33ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2d0ea9a1061fe840c13a046b93faaeb9dbcf4357f53a37b83747a395c05279`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068b14e90f05cd3c9537d5988b4bbe6abead4cac15a8b25d1959964036cdbb13`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd06766d16512bbe8f937e09b7f90223e29e8e4f0d7306052387f4bdd5243406`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 84.9 KB (84859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdfee3855ba5896fd063d555eea5f8b0895168a4ba8162a475fce6bbb3cd631`  
		Last Modified: Tue, 21 Jan 2025 19:32:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb327b9c33b07ca822f14e1d5eb0e89aa67aa294ba7fc97ceb881ba83258645`  
		Last Modified: Tue, 21 Jan 2025 19:32:38 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:cf5e04de8914015fdfced9fd2350f25ae04499716af67e6870cadcaa694a5944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a90ae2d8e21694ed59a7386bfdd6650236725793931430a24f9d8a8ac24fab`

```dockerfile
```

-	Layers:
	-	`sha256:a3e79339ec578c35ce808cf83d83181d2070408631264fce657e406f892754d9`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 77.9 KB (77865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d28c39be10ea42747404de7a4952b61efc3419f395d546ad85727355d0bdbd5b`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.3`

```console
$ docker pull spiped@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `spiped:1.6.3-alpine`

```console
$ docker pull spiped@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `spiped:alpine`

```console
$ docker pull spiped@sha256:5c7e4d33c567ce2c052935664bdb5c40a55c846af284c06137e47ec234b2c041
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
$ docker pull spiped@sha256:bf4f80de0db396d644d3bd7d284f1a82968f2f5dca2d8cb33ba829c0043fa7e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1739bfd2f7c6bfc0aec39069cb0902b1e56873b04c7099b83047c17e17df1c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be090fd76d1e36f16806f586b6344fa2de641690144682cd6860b988c3c931d`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1155ce8a77b55d5a058c2b75baec72432a1a394f1d53956393a6e547ba0d7f6c`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9276e935161ceb34d567a8fa6cd5945c8199ddaa39aae106a6c0f34b646ff4`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 97.9 KB (97879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d015ce49382dcd762930d16d6a81450d9b389d35fb79ea80527841a68922f56a`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912bdaad70ad3037b03159d81278ab0dad9b2827a758dd7444163a7203f9314c`  
		Last Modified: Tue, 21 Jan 2025 19:28:19 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:379145c25a8027c2a34d73c76346518adda978e2b00e97869e108358e4b33437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28081c4e7942cc3a13ba88170d117e0ff67b48eaa690d6537b01bba98892a90e`

```dockerfile
```

-	Layers:
	-	`sha256:6625a81c2cffef3b41b47962b504e9dc20cff4471d4d6f1e5d96e14770cd2929`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 79.8 KB (79816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9fee5c0b25d256b52106b1fd933f9f04a617e9e2e3a7d2731ba142a1d8ba0fa`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:0c4472e3c5cd36e439567c13f5cd9a379aab66e0a915889d6d42baafbc2500ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3454044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a7cbce52f04ff9256292b0a9817ed2fa7941835bdeebeaa27869591dd7f9eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee72c2b1876a0156b7d396caf2dc29a0f8081b2b7a6733a3ff64d9527f586ea`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1da6fb0facd6416135ae0db69e959ecf3e75cab6ea327aabb4ead163825dfc7`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4bfb2112b9ff1da637fda9a1fabd68afd45961279bab992964a8bd6e31408f`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 80.9 KB (80855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074202ffcdbaa57f35bc530fa794482ecb273ad51046c53fe8043f01096270ba`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc4e41cff4eb7a1ada1c481fe378e5268751d48dcbbae7342d3241561661269`  
		Last Modified: Tue, 21 Jan 2025 19:29:41 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:366e5b0763df779aacdfe5468363ac3687088dd4e125b847daef76b5029a5661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7ede033b2a067297269492b9cc67391a8024877ed9a838acefe18b08c2e7b5`

```dockerfile
```

-	Layers:
	-	`sha256:464626d886af9ffe2ba5aac0067601f31503365fea01536d0142c873f5980371`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:0ae1d2d6cf54b9aa45265044ba111dd99c549b31e466c67d3afc3abec2fe3ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3181455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbc5512e44ca9ebcc11a994bb12f151c14c2878f9ed60b62665f1ef9e2dd061`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae962cfc489c298278551ba32bca1e0ed1f67cd05192848331b7c3ee926a77`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114d274ac423361940bdd6b0c7904acc23cb9903e6f1a2904b32a6b89f331c4`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60770baea6ea5185f492834462f47c3556209ae19718dec68186d538965228ca`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 75.0 KB (75035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0c2868e02a07fed49e900b254ea234eb48f25e37bc10f580198d191565de75`  
		Last Modified: Tue, 21 Jan 2025 19:30:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e555c89d083ded756b21c5bd510ca93d93cdc37921edd4764164ed46228bd95b`  
		Last Modified: Tue, 21 Jan 2025 19:30:38 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2c10a8c0cd22de6c2045282220f18a4879e5e74494a7d1945236baf2eb256760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58cb4a63496728162216d59f92073861eee5255f9c2edae3276a72c8777b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:7436f70191232399d4d7c405219fafb240274bd898d8ccd07f712aa394e7a86d`  
		Last Modified: Tue, 21 Jan 2025 19:30:38 GMT  
		Size: 79.9 KB (79852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce64a4a26bf1cd792d2cbba128afa6e7fb692cbf52d2fa21f5297938c26001ee`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:4f709a7af2244a5ff9f01387d5030ac4aa1c6c573254cd2266bf3100b9a813a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b82cd26698a5299c656bd15e65f1397979b455479ffdd415881455b92d1991`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987e71ee6cc5ab416ed1f0e49bb9a1696b4b5656b4d3fcc1feca517c7bbe5030`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faf545dafdf63442f66bf2d829b8ba0c5dd8fe81240a3298cbf9fee767c891`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2c84ea327537859da16a3a7c4061d3787af0f266934eb7228b7b3a162359f7`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 91.0 KB (91009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c519261ae45d672eb2ce96c696945b567ef14c566a912cdc782f8a6460f3a5`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c072a47e7cf1bb0073652f81348762878a297e164adca16bd19e1fbed0b7c8a`  
		Last Modified: Tue, 21 Jan 2025 19:50:57 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b5c38e6ae8441ca778cdfb5a4550cc780f4ef358f0a43882a3235e7eb9042be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff3d3634cf407a39a6e662cb942c48f9a3cd5a462a148837480d362d0d3b118`

```dockerfile
```

-	Layers:
	-	`sha256:1a07d546f1499b6116c2af470d73941c09865327e1d8c12e0e00d302b098b024`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 79.9 KB (79872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42e95337c10301d3e0c1a1a7dd5266eb9b51919a6979351d6ab21dd694353ae3`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 14.4 KB (14433 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:142927fc09806045217102e1fd61c9120693bb3437a64b4e53d45fff85604a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3580250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5191a7f4b9da1db034fdb1a2a191bfdbbaf0970362273c14cea5a8d67af9c59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66602b26aee70855e62f399265bc3d459bc2e17fe241dc09f542aea66a732d51`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754deefeb72f062211245a56424039263e88066669b4752e5509b96c3fc75976`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8aa827b00c14c831e4f20dad83f6c4f5e3f61faa06bd0d88a0513abd6919cb`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 107.8 KB (107820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4247d4a0214d8ebd8f0fc13a2dda2e237375c545239c856be1deee79b6db804a`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3260d2ef071d2a025027168328bd57243ca2fcb118e4eca7966966689d64c6a9`  
		Last Modified: Tue, 21 Jan 2025 19:28:00 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:4701fe7d0f9e827457a3849fd8edff76707b89ab2830cd1f661c6968daaf01a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191ca3b524a67e610d402501801e70d4ed64c7e0105ec47581b8221b04617eee`

```dockerfile
```

-	Layers:
	-	`sha256:b243e9db2d57fcb036e6456ffb5fa340acb65741007c7bdc9b4583b6a11fa23e`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 79.8 KB (79791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea95049f4e29abe2a4dbbe1d23dc82dc4e3bb876a61c9cb0ddcb0c6c3f53d6c`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:02217b126efda6419d593927c1e7afedbaae32a0dfac48527891fb61e326668c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3678657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336ce0a2b2749719b0875443f6719cc477728f9d9ca03aeb8fdd2eb80a7fd7bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937ae7bb7a53c30739164fd8d6b1af5449b91bdeaacb11c09da360a795e967b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed2b37b3a36511a8f8cde15ac74df12676c707a75cac7400604b533817a57b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 7.9 KB (7918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78388bac15c7f0679a8f61fec0fd44039e2dc31eb14e7adb586632c8938f4558`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 95.7 KB (95740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dca0f484333f1fbdab6b9693779c9f26be5962fe67e46f46ea2db75698a3d0d`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be1274653db549fd50a72850308000f30c9517f1d7b348cb82463adc3c4cc74`  
		Last Modified: Tue, 21 Jan 2025 19:31:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ed3fde57e25bf38537c7f0c1d97fbc836ebf868397090410e8909472f48a710f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db83784de2b8cebf42f5efb3510f46e989e3bb222c1d74a7ada0a21d3b477c3`

```dockerfile
```

-	Layers:
	-	`sha256:d4d5a0de95eb8f06fde7d4e9a71e8f41b6cc30a14ac230b76293cb5186635d37`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 77.9 KB (77899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f61dcb17bca36ef37c1782c7996fd97fc226af6a408695c157aae47d923bb1f1`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:8753a779e5087f28ca4abda0cdb7c4a28fa8732bf94201fc4f1c6749cac05e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3448196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972586fe36ea4a167e8c4e3dd294a605bd9e95559c656558021b297fc6a0e7d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410676c340782e10ad961429d12c4fc7bc22fe42e602f44af8fe4564583fa790`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb03e5e951a5c0dc5098e3f3712ba683716c2830cd781627b8c589f37e35d49e`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 7.9 KB (7900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725fe5f1d54360199e0c323ed9105f4b968c5b4e9ac846c5c3c41c9f67026998`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 88.6 KB (88643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561e0b8832db6b203f73cdc2a06f1f927f05044848e5a4c911efd349960c1299`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53e08b4d3b18487565f895fcc2e5aa406700b2e9589117a057f0d580eda17bb`  
		Last Modified: Tue, 21 Jan 2025 19:47:11 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:433e9af8a8aae1b47091598b315936f3260b19614787199011d74195be92071c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f61d9865b72e236614e5628bcb24f39a6039f498ece96818cdbce448c511329`

```dockerfile
```

-	Layers:
	-	`sha256:79b96efba8cf867f9e9e2cb09b95054474af816599fa19ea5c5fa0ff4b799030`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 77.9 KB (77895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2249ad8997aa1b69cf185889e51eeaa77a5fbe77b0dcf1b762154def0237b80`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:2d7e1c9817e385b181b3bc711b36578549be6951515e90c415628765f463a86f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3561031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854dee3cfd59deb9dfb570b45c1fc1a4289fa0cce595a8c460b4ff4e38de33ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2d0ea9a1061fe840c13a046b93faaeb9dbcf4357f53a37b83747a395c05279`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068b14e90f05cd3c9537d5988b4bbe6abead4cac15a8b25d1959964036cdbb13`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd06766d16512bbe8f937e09b7f90223e29e8e4f0d7306052387f4bdd5243406`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 84.9 KB (84859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdfee3855ba5896fd063d555eea5f8b0895168a4ba8162a475fce6bbb3cd631`  
		Last Modified: Tue, 21 Jan 2025 19:32:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb327b9c33b07ca822f14e1d5eb0e89aa67aa294ba7fc97ceb881ba83258645`  
		Last Modified: Tue, 21 Jan 2025 19:32:38 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:cf5e04de8914015fdfced9fd2350f25ae04499716af67e6870cadcaa694a5944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a90ae2d8e21694ed59a7386bfdd6650236725793931430a24f9d8a8ac24fab`

```dockerfile
```

-	Layers:
	-	`sha256:a3e79339ec578c35ce808cf83d83181d2070408631264fce657e406f892754d9`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 77.9 KB (77865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d28c39be10ea42747404de7a4952b61efc3419f395d546ad85727355d0bdbd5b`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:c2f5e489d10411b4506fbcbf603693d6a246b40d9398706f7c9575569f77f171
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
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
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
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab16c690e615571a539221290f9c7154ed500a5de18d47dfbe3d130daff486f`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
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
		Last Modified: Tue, 14 Jan 2025 01:33:27 GMT  
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
		Last Modified: Tue, 14 Jan 2025 06:07:50 GMT  
		Size: 3.5 MB (3486344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d991ae0cd962a40b1a96f846b396fb35fb42d45ca1a7ffa955e1720f73fa9707`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
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
		Last Modified: Tue, 14 Jan 2025 08:42:36 GMT  
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
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
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
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e8230d3f815bb664e5eda60129ff633bc7d34854e10e52903d538454410d33`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
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
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
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
		Last Modified: Tue, 14 Jan 2025 18:08:24 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:d18399db45255851ae8ddbad4e7b5c900d55f4e43695efd3981135d67341765b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41069257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d445aa64495f4c7fdb2a32b492a68d159b909988abb7b61737e38b5345a0b8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2904017eed57b6a379aba91f659af48ec8d1305525c46625a955313f2f21e7a9`  
		Last Modified: Tue, 28 Jan 2025 01:42:23 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170c8da9f5a98720edaa9345e098b778f3682abcc6a559d512c35d465ed68eb1`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 2.6 MB (2582109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf6e585af2ae045254fc980b05067c3829832933e9228997d7b38860b66ec72`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 6.4 MB (6440760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839630c4aa5ab3314108a0e90bc3ef41c6d874dbf2195903468542b67df10b19`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bd1225ed7d385f9ccd07a3e86a10eecb6f5aceb0d21253d66059f25cc10f76`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:635959fa2681a25dc8179b535939238e6dedf3b4407e4b61c265dcaef89b8b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7a5467d6b5e70429f77b5ecc51c24454e72e2a4bec50c2ce6d2c38b6d6ceda`

```dockerfile
```

-	Layers:
	-	`sha256:058f9b63cb6c662558bc2dc672de21d6e7f0b7686ae208b7d53a9ed320429272`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58bba2fecafbd5b0fec43540d380620c8286e345af289a079b69e2ac6bc4556c`  
		Last Modified: Tue, 28 Jan 2025 01:42:23 GMT  
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
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 3.5 MB (3504000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf76c9e1d84fed3f30cb373ece1c7713dffbb1a40bd4018101999d0b899e9f72`  
		Last Modified: Tue, 14 Jan 2025 04:49:47 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json
