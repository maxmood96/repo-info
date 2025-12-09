## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:dd6df81f8ff49ec14c9523b2e27acae81acdff667464cdd1ac944874c4adb065
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6dcafd72a00cd7683c828e6035caa39babfd4fc781cbc1e9ceef3dfd94144c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.8 MB (343824885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:529953b46f42ba003c545317787c68a158c20cfdda99b1387b8af40541b0658c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:45:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:490e982b5e2060f5a5ea7e5f586ff8bb98bb61a953b4473631a9da94fd85fe11`  
		Last Modified: Mon, 08 Dec 2025 22:17:59 GMT  
		Size: 48.8 MB (48817523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff8ebe9a9fefe126b5d099857127577acadfabc1b7d98ce416ca0faff37c513`  
		Last Modified: Mon, 08 Dec 2025 23:07:36 GMT  
		Size: 27.2 MB (27197450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefa9b0831ef76f3b6f478e168c5a2d244535ebb9ede263a69d319a2cdf5e22b`  
		Last Modified: Tue, 09 Dec 2025 00:06:54 GMT  
		Size: 68.4 MB (68427481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7df42d636bcd80dc7d9ab4d2be6574fe99db41a50f60b4b417fe39ea88e6a82`  
		Last Modified: Tue, 09 Dec 2025 00:46:06 GMT  
		Size: 199.4 MB (199382431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c38d4411ecda5b97186b1c43da600bf7084e809e7e530e6e80daad00d554659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16288880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70698cc0b1ea781283bd14fb7759319ede3317d0b36dcdec5830c1790079278b`

```dockerfile
```

-	Layers:
	-	`sha256:2be87dbca03acced547e7f314617d15b73dd94c43c4654efba8c51fa82c35e83`  
		Last Modified: Tue, 09 Dec 2025 02:23:11 GMT  
		Size: 16.3 MB (16278748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82379c4beb786d157b8736f0a32bc4f9e6ed879812a016c10c317db6bebacb2b`  
		Last Modified: Tue, 09 Dec 2025 02:23:12 GMT  
		Size: 10.1 KB (10132 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:282099c7a1592f4f3442499253feadf1ccb36dad8c5aa2aceb69e3b14d4dd161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291667921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66eabbb88992b4df830cc1100003dad470c9f230f152e95fe0c081be17f45095`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1765152000'
# Tue, 09 Dec 2025 00:06:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:33:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:17:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:76f9334b2a3a315cfbd527ebf785350ccdf20f285fafcc4cb59b172a12b89d6f`  
		Last Modified: Mon, 08 Dec 2025 22:17:07 GMT  
		Size: 45.1 MB (45118376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a62720547143dbd3a73491454b89436c575e1d06808adc4a4d023be5d9947a`  
		Last Modified: Tue, 09 Dec 2025 00:07:27 GMT  
		Size: 24.9 MB (24911741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4a91d293a2f08420426d89a5e0b168d8395fa90d22b8105ee6e181bae6303c`  
		Last Modified: Tue, 09 Dec 2025 01:33:43 GMT  
		Size: 63.3 MB (63326674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce71fa8c09793d4727ded7484e3b7768325dc764e387b26dee1ef2c9c86b396`  
		Last Modified: Tue, 09 Dec 2025 02:18:16 GMT  
		Size: 158.3 MB (158311130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d467f8a07b6c2837955173682d131547c5de45c4fac15370cc3f7a391f7f2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16044632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edef20b271340f5274982d56e430a55596428af9a6310e42dc1858861d940890`

```dockerfile
```

-	Layers:
	-	`sha256:823c1c44c4270ba47b272c2104cfc9baa257570b0fffe23ef13347d8b8a4aba2`  
		Last Modified: Tue, 09 Dec 2025 05:22:03 GMT  
		Size: 16.0 MB (16034435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea10deb31a819c317992467214fe0d5dbd38ce7c33ef94acd742bbaf9efba1fd`  
		Last Modified: Tue, 09 Dec 2025 05:22:04 GMT  
		Size: 10.2 KB (10197 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4d42070b765b4394d9cb80a8c1e4108aa04ff7f4e330f3147eb58421abf3274f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332867419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c45381376099b09e44159d6235c61ca0b68bf27b3069f921ea61b0861b580c0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:10:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:16:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2e5b290b66ba04e2259d84d677cc1c79191dcc391b2b9af44fa26a4735123220`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.8 MB (48838607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e861ca4e0892270da154f93f8077287d4c0bd0913eed59fe54c6514a5d7f1c`  
		Last Modified: Mon, 08 Dec 2025 23:11:15 GMT  
		Size: 26.5 MB (26498040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa12addd0a7e2c939e7bcef4cd81464734e92119acd190fd47b096280916d8c`  
		Last Modified: Tue, 09 Dec 2025 00:12:02 GMT  
		Size: 68.2 MB (68154235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd66c1f605140523e5d0940cc2d32587da9a4838b222601345dae8fd72bc73d`  
		Last Modified: Tue, 09 Dec 2025 01:16:40 GMT  
		Size: 189.4 MB (189376537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:781438ad85c21f0f646082b35f3b7d11792eb8ed766689821fde052c1855f432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16363511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb14135cd7f889e9202f4535e5be48bd0991afd23a7e5e9fb0a46fcf32df91e4`

```dockerfile
```

-	Layers:
	-	`sha256:20974a837809900d0e776586a69580638da8adee40f9291429aba5670b98e0ad`  
		Last Modified: Tue, 09 Dec 2025 05:22:17 GMT  
		Size: 16.4 MB (16353298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1b415d72ecf33a67e9581a0766d2677bf2bd0fa090c0e6854f49948672c2aca`  
		Last Modified: Tue, 09 Dec 2025 05:22:18 GMT  
		Size: 10.2 KB (10213 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:170ffba505dcbb85976c5600d4ff4f4d7cac5fc3ccb3aa70f79e31823d15e44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.4 MB (351358066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec76b8ea66f8b054884d9319657d9424780d6f5b93d6d3ae80e18689da96ecd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:14:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:24:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:17:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:67f7fae0ea3bb931c627a66604e60b0a242047b0c8f9186d188cf96e0133593f`  
		Last Modified: Mon, 08 Dec 2025 22:16:33 GMT  
		Size: 49.9 MB (49947966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9e94662795a8f26e5463a4bcfcaabfbdeca01c44b799e3fa96524d3ed5ff0a`  
		Last Modified: Mon, 08 Dec 2025 23:14:49 GMT  
		Size: 28.4 MB (28430929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2dcabacda9674c82129e92594c80d843967d7757a07ee38e58f0c8b9e9e24a`  
		Last Modified: Tue, 09 Dec 2025 00:24:37 GMT  
		Size: 70.4 MB (70406743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421f45c263fc9ae77e5e4099fef799734e68d22ac77fe7db9913198736d4980f`  
		Last Modified: Tue, 09 Dec 2025 03:25:09 GMT  
		Size: 202.6 MB (202572428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:22c92c018089a0fdf8726dbd8421a80b1d49bb0ce322474336d846d42c7fee38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16258608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57968fbf7faaf29036b7c6e4436baa778ebca5db0b5b79bb6eaa062c55ee2a4a`

```dockerfile
```

-	Layers:
	-	`sha256:d276d92e8a72c7e135d4a67ddc104205613b6aea9d3bdb31ad38051bf73f9604`  
		Last Modified: Tue, 09 Dec 2025 02:23:52 GMT  
		Size: 16.2 MB (16248498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43501e64846238fc14bccfca416a118ce821d0f4f8c1c3a70b12db9b84777f7d`  
		Last Modified: Tue, 09 Dec 2025 02:23:53 GMT  
		Size: 10.1 KB (10110 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6f26e4453e1f3cf280d8636105407e8e0f2dee976fa89d1cd58b96ed42b1838b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.3 MB (348290913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16bd8e4883c6c4448654ca0c7d60c16ba82c83326c29a90219afc13645bbb6e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:22:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:10:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 04:31:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:91f19749139bb2193587558635e0a320b0f29835fa1325bcb8c73b48ad8b72df`  
		Last Modified: Mon, 08 Dec 2025 22:50:49 GMT  
		Size: 53.5 MB (53494424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a82bf53318ee9ff50934cd5a455b97b8549b92db55df72cf410249ca6112c7`  
		Last Modified: Mon, 08 Dec 2025 23:23:07 GMT  
		Size: 28.9 MB (28884607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03e0f90ac822b83290c4938a8d44e3bfd579a2891eac5e11b8dec4f3a80cf68`  
		Last Modified: Tue, 09 Dec 2025 02:11:35 GMT  
		Size: 73.9 MB (73921341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5eeaa3713eb2b2168c3281b5659dc1e0be47bbb9fd7a59a257ce2c86ac33053`  
		Last Modified: Tue, 09 Dec 2025 04:32:46 GMT  
		Size: 192.0 MB (191990541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cf1c5b72ce2943b9556f92e3eb46be917dc56eac79ea63cc063b258f445d951c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16261852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad855282ea4285ec2d611793f9c8d51ebbc5a2de1a6028bee1c3fcac3dce3f0c`

```dockerfile
```

-	Layers:
	-	`sha256:2328c630cfbb172e749f794e3d43dbb900617fec570b3dd8e0ec5f1737f6507e`  
		Last Modified: Tue, 09 Dec 2025 05:23:02 GMT  
		Size: 16.3 MB (16251687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b5a9b131b2a9ecd8f2449ca93b8caa06bdfea369a2553bbc8f44c43a66a97a9`  
		Last Modified: Tue, 09 Dec 2025 05:23:03 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:560382490893079040e0ff079cfbd4f17fb94c7d743cbb76e636f2755db32f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.1 MB (452138991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26071e0c7b6ba26393f5e5fa6eae79e0699d8e431cd5fdc51d66f78916b24d6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1763337600'
# Wed, 19 Nov 2025 19:33:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 22:22:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 22 Nov 2025 21:31:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ed67ff00f4a63ed57f98b299833d8c2bd5b7627bfdca1af20fe366dfb5d9d552`  
		Last Modified: Tue, 18 Nov 2025 01:34:50 GMT  
		Size: 46.8 MB (46807232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12faa2c8d5976c2936626416dbd958b979633ec7e97e5fb377956f757414803`  
		Last Modified: Wed, 19 Nov 2025 19:35:09 GMT  
		Size: 26.4 MB (26394813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c856553cdba1b452f2934482676983f9c2dee9a9410ebeeee2db907f70948a`  
		Last Modified: Thu, 20 Nov 2025 22:25:57 GMT  
		Size: 69.6 MB (69597545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bf6d06ff1c105ed6a3cf1531c6c52c5a38a0e4bce47bfec4b65cce8f7da031`  
		Last Modified: Sat, 22 Nov 2025 21:55:08 GMT  
		Size: 309.3 MB (309339401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eeab707c587e210436d5cb35faae401130eb0565134bc00462108a2f98436dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16311848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79bcc184d1b5e0bffab3e5364c548db87ff63867971b3ddcbf2584dd1c2f088`

```dockerfile
```

-	Layers:
	-	`sha256:9524882e97e0c9f78e82eded7c97a04d66c93abb3be29254aae9d06ee47133cc`  
		Last Modified: Sat, 22 Nov 2025 23:21:13 GMT  
		Size: 16.3 MB (16301683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e341bcdb3aaa46b4d3f480a30a2055291cd10a05824e42f4a7084bfabe8d212`  
		Last Modified: Sat, 22 Nov 2025 23:21:14 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4cd562f8c6c5611893813a37b58b6f80dbaa4b07d8c6f2c9e3b6188f2fed6a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311541684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f1221a0848354fc2cfc95c407ebb0fbaf4679230bfe3c87a096b11120098ea`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1765152000'
# Tue, 09 Dec 2025 00:11:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:47:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:57:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9a7cba59687143fa1a3bde49b08caedd4592355c94693db34a36ceebea332a04`  
		Last Modified: Mon, 08 Dec 2025 22:15:38 GMT  
		Size: 48.4 MB (48404077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c41c2bc13ca9c32fc8ea3b0ee8862d2350cf32202664571fd15af30f5ab552`  
		Last Modified: Tue, 09 Dec 2025 00:11:46 GMT  
		Size: 28.3 MB (28311739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5116962aaf70b7ed1f02f2ccd4dc554c6270985ceaf307b1f7833ab499653777`  
		Last Modified: Tue, 09 Dec 2025 01:47:51 GMT  
		Size: 69.2 MB (69160406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cba9f2c5659054a1f1ad1ecf614c54b3a6a9b1d7290e7cd550c4c8628604863`  
		Last Modified: Tue, 09 Dec 2025 03:01:32 GMT  
		Size: 165.7 MB (165665462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d638bdedaebcb71c758fa0aceda268d36b566acc80915cdfd6d8085636686f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16054274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479d53955de0aa6cbe9ea2daf7d3f576a6fcaaa527f028179169e349a872dafc`

```dockerfile
```

-	Layers:
	-	`sha256:352d458c5c7190c49c86cb88a7aa07193eb222fbca6e36d1d400219238665563`  
		Last Modified: Tue, 09 Dec 2025 05:23:21 GMT  
		Size: 16.0 MB (16044141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e64d942de44fb7e6a21fdc1d6e77d57bc8dc9315b8fad5c641d30b1dda45b60`  
		Last Modified: Tue, 09 Dec 2025 05:23:22 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json
