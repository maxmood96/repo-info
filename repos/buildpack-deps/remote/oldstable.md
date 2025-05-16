## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:530e8e9c31c4c893d876ca429bd0975ecfbdb6bffa3eeffa60a07d10f108f1b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:oldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:003121ccc25536fc0bd547da1dfe0f871a93729f5866f0f1fc7ceba722285db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.4 MB (321374998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb78df35e096cb5c55f6121b75d1c62e550b12c6a1c51c797e7f417254cd545f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68201ec6e5815a0906ce41187e7e52419a2d2c28d73d199e7612f268f81bbc35`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 54.8 MB (54756006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee2c8b84461fce714721ac74cb275f6aaa0de67c2aeaccb8193af9ea8b4d38`  
		Last Modified: Thu, 08 May 2025 17:04:52 GMT  
		Size: 197.1 MB (197107708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8e1f6d76738ef5be535cd097615159b51e3642e31d7ed737400fd0c8dda1d2ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15083962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775aab04c6911914190cf9861c8890b918f371426fa22cc756a71331f849dfb1`

```dockerfile
```

-	Layers:
	-	`sha256:32c511ed9e9552151526e542c31fb93e45884ae238c4ad70efe610aa76c8f177`  
		Last Modified: Fri, 09 May 2025 08:46:32 GMT  
		Size: 15.1 MB (15073730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c495b9086b26d5b5716e0b69f3e7ba7cf2b1caa887d591da1f624d3b6a6499b`  
		Last Modified: Fri, 09 May 2025 08:46:32 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:02e270a0de32434b8fa5d60f55118eaa99dce5f16637e9eda194c7e95bba75be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282103121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa0ca967f37c366b073a31c75fc3e08bd5309c06a255019b3ad324d96c7c322`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:72fa46f1d669ee2de1ffbc36b654bfe8dd0aad49156f4143a5d9edd3a5c3d559`  
		Last Modified: Thu, 08 May 2025 17:18:11 GMT  
		Size: 49.0 MB (49040048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de64850f276e76efd1e91be51cb4b2577218e49bf52707b1bf6de3be76028cd8`  
		Last Modified: Thu, 08 May 2025 20:08:04 GMT  
		Size: 14.9 MB (14879026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc4cecedb434598f97e33a3320b6af6e1676388e6c13b31f0aab4b7c9372012`  
		Last Modified: Thu, 08 May 2025 20:08:14 GMT  
		Size: 50.6 MB (50625161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce34362265f33a06975f249d19b3ebf3e131e052b1333868e863a53ee816bc45`  
		Last Modified: Thu, 08 May 2025 20:10:03 GMT  
		Size: 167.6 MB (167558886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ebcff6643cd1ad112a344ab9a7922d66e14cf0db6ce70cd2454eac2f7bb6b59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14884787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78a935ac0f258b1431d64f26e91f6f02eff561dfb521edda9d52fbec853b572`

```dockerfile
```

-	Layers:
	-	`sha256:9d024394af90fb08c546db0cf3486c6b71f7e805b0b9be512e630642d03ead86`  
		Last Modified: Fri, 09 May 2025 08:46:34 GMT  
		Size: 14.9 MB (14874495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f3a0221c3adb5e6a06670201a38a9e1607b68a9e4d21db620269a99deea2be9`  
		Last Modified: Fri, 09 May 2025 08:46:35 GMT  
		Size: 10.3 KB (10292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0eae89394efabd51cf47053d0cc746ccf4ba95dfb984fd52fef04d0000612911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.9 MB (312869416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3674ff282d910fdd55e0c61370c37f59946611a8b34f6f023652796bd33205`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Thu, 08 May 2025 17:08:39 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b10bbe754ef0579f7ae8162881d71484a39910114f01fdcee0bc53987fec1`  
		Last Modified: Thu, 08 May 2025 17:09:23 GMT  
		Size: 15.7 MB (15749108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b30b3b7ef57604d52a4f287f3a1202fa7094c2c34ba89e66f13f2ef75a47ae`  
		Last Modified: Thu, 08 May 2025 17:09:26 GMT  
		Size: 54.9 MB (54850001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356545a2ed16b26897f2a271b3f4a7d7e64a9bf9bc0c78fdf4f1386401e37428`  
		Last Modified: Thu, 08 May 2025 17:09:35 GMT  
		Size: 190.0 MB (190024328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4396b4ce4d4f1436172c8148d704250143ca6093d8b9094e4280d28ff117d6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15086276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e758a8b173226712a332819a547debd03ffbdd5111c90be0143d51a0340cff44`

```dockerfile
```

-	Layers:
	-	`sha256:12122eaa9993e469b1d05ea734c8e9c81df77d16d05c62c7ce972da393787d8e`  
		Last Modified: Fri, 09 May 2025 08:46:33 GMT  
		Size: 15.1 MB (15075964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dd32e95cf9243b835298775747643922f0da3aca160a81d2b4167cb96678d37`  
		Last Modified: Fri, 09 May 2025 08:46:33 GMT  
		Size: 10.3 KB (10312 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:30a7f257300d96f7ef93a34f22e96a5b4464273c4d78d95949cc328c2650e832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.0 MB (327009315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06de521895551d0004f26ea47a5de6138c54f0dd43077c706103d4303c0cce1c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4ef50a397f2c0106a3e44d1d1bae16cf52fb5e7e855c588f4098e281321c3e7b`  
		Last Modified: Thu, 08 May 2025 17:55:44 GMT  
		Size: 54.7 MB (54683102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbb48ef4c334135b55fe5dd328911059bfd41eec15edf03ff0ab96ca44fb6a1`  
		Last Modified: Thu, 08 May 2025 20:09:54 GMT  
		Size: 16.3 MB (16267399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229f9ff435d5a831802e386be1d29f22419a5d3951a76711fcdfc9f9bad0e6e3`  
		Last Modified: Thu, 08 May 2025 20:10:01 GMT  
		Size: 56.0 MB (56047280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ef040f15a9c521f9352beaf246f79eec04035acb8b716f343f27a2aea49563`  
		Last Modified: Thu, 08 May 2025 20:10:19 GMT  
		Size: 200.0 MB (200011534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e6aa87cb552f572d92b1144c884eb2061c6d96e23f6507672b1701417db346e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15072280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7515e16aa70b2f04208611d0ccbcb1e07c776fbe3027834b90f0a212cb37f2`

```dockerfile
```

-	Layers:
	-	`sha256:6f143efd378d1b7f4ed3bb70d99d1ac37b6123e236ec115adc1d50b76c8adecc`  
		Last Modified: Fri, 09 May 2025 08:46:28 GMT  
		Size: 15.1 MB (15062070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f54142478b408a619b162bcff994588b8cde22cc564edc00076d9c5ef36d17`  
		Last Modified: Fri, 09 May 2025 08:46:29 GMT  
		Size: 10.2 KB (10210 bytes)  
		MIME: application/vnd.in-toto+json
