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
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb387415fb818a8b4d56b6c4b1981b2212e57ec6addac3a80cfb2b9d9331b50`  
		Last Modified: Wed, 15 Jan 2025 00:13:43 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228fe3a70b06fc8ca22481663a32d8b20b71b4a1cc2ef6bad63851b3cddc6a02`  
		Last Modified: Wed, 15 Jan 2025 02:57:45 GMT  
		Size: 2.4 MB (2401340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bdc698a91b053c8c6c8793884aeb21f069855e2f35ceaf6d354563a622ec60`  
		Last Modified: Wed, 15 Jan 2025 00:13:43 GMT  
		Size: 6.5 MB (6470976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562950f9b4e1da298d9932319a15c677ac7b1072f4a6218a62318ec083a438bf`  
		Last Modified: Wed, 15 Jan 2025 02:57:43 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d26d7b3a2a6d5bfa2d8845580756d251c7acbb85868393a8dc4b15857a936c`  
		Last Modified: Wed, 15 Jan 2025 01:02:18 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:33:55 GMT  
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
		Last Modified: Tue, 14 Jan 2025 23:04:30 GMT  
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
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3d076ceae3499abc00492adc7b101408d72437a499e4a9cea20964e90c3765`  
		Last Modified: Wed, 15 Jan 2025 15:46:18 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0214df3970acd6fea09000d0df47a3cee908490cd9b760e15bd23ad7aa3cf552`  
		Last Modified: Wed, 15 Jan 2025 02:57:03 GMT  
		Size: 2.2 MB (2247012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2354092ea972f14ee9af251fc4714c734d8cd2c30834f655c2ea396610489655`  
		Last Modified: Wed, 15 Jan 2025 15:46:19 GMT  
		Size: 5.5 MB (5481085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d572dacd78b347329872172960cc26ce37ee9b7ac42a83ddc7425ad149add9cb`  
		Last Modified: Wed, 15 Jan 2025 02:57:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e699072832a75d28646bc8d1b28f5ee412affda7e0b1e8469893f897fc236810`  
		Last Modified: Wed, 15 Jan 2025 02:57:34 GMT  
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
		Last Modified: Tue, 14 Jan 2025 23:04:32 GMT  
		Size: 3.5 MB (3487042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec8b87f83866e1f34c08767b42d87be6e439e3737291318890b05e17f026397a`  
		Last Modified: Tue, 14 Jan 2025 23:04:33 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:35:48 GMT  
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
		Last Modified: Tue, 14 Jan 2025 23:05:01 GMT  
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
		Last Modified: Tue, 14 Jan 2025 23:04:38 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:36:29 GMT  
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
		Last Modified: Tue, 14 Jan 2025 23:04:47 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json
