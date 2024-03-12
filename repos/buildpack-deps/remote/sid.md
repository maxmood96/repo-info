## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:f5a8de794d861f8e5d0d5bbf4e627754aa21b66b0e1c6cc99df2f98930287115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8f95f8a59ac3227cb7483799a6836e9c79d5cef491ba672c1958abdf36bf7648
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.4 MB (408449083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6432734199f2b6b7123afa9e0cd230140426c275050bf484f9e96827c4190c64`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:22:38 GMT
ADD file:3a737ad8ab65fe5ad068d6094fbf99ce9ed2b5beff9c86daceee8c2c50182bde in / 
# Tue, 12 Mar 2024 01:22:38 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:58:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 05:58:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 05:59:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:490d250d3b2798e2c88a398b87b4162c8ca53e579e4e79b47fc41c2c2aaca6fb`  
		Last Modified: Tue, 12 Mar 2024 01:28:23 GMT  
		Size: 51.5 MB (51512918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355c7ca394663c3c42de69370984f58c9ec1386fb7bf3892311813e2a6b72eff`  
		Last Modified: Tue, 12 Mar 2024 06:05:25 GMT  
		Size: 25.7 MB (25711626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7869bc1de22dbe818f4e768896046e07c479ab857f8c3b31b21028de11d24a`  
		Last Modified: Tue, 12 Mar 2024 06:05:43 GMT  
		Size: 66.3 MB (66301825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdd3e806c65a3a69449a8e4118deb06ab4121c40ac121c25913e44d2954b33e`  
		Last Modified: Tue, 12 Mar 2024 06:08:03 GMT  
		Size: 264.9 MB (264922714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bcf7327d7f12ffc8a2a41a1f361e1cf6533d82877429896f0da0f01ae3fdc5bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.3 MB (370331989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41519ced967b01b112d200b16c18a1a11bc1f34d907ed1811981430e1eb64146`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:36 GMT
ADD file:624f450cf1c3fdf8774bf8313557baecef902871c3ad8dff4410f14122f8c507 in / 
# Tue, 13 Feb 2024 01:09:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:47:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:50:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:24aea175239943bb2adfa7be646a8e0c040383dec937faf220aee85a3f296298`  
		Last Modified: Tue, 13 Feb 2024 01:15:26 GMT  
		Size: 49.4 MB (49423639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c530646f760ee121e031a3cfc99e5f7b580df8596f51a1f5e30e10af689119c`  
		Last Modified: Tue, 13 Feb 2024 01:56:34 GMT  
		Size: 23.1 MB (23051918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3a1cdabe4cc17ce6f55149b66ca7c16793fb014ff72d99cb1da643581eed76`  
		Last Modified: Tue, 13 Feb 2024 01:56:59 GMT  
		Size: 64.1 MB (64108591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7541155b76422a64edf910ec2131b609a880f2b83ac01ac06abd5cb73d5ee`  
		Last Modified: Tue, 13 Feb 2024 01:57:51 GMT  
		Size: 233.7 MB (233747841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a8a188b1ac61aeeaf35024c340f52f63a0132ba4657889d2e9437aca5527433b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348778060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ad35eb2f1a3a5e5732ca672c9f3ce8c926a53741aa176c8e2fd0870378fe2c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:22:33 GMT
ADD file:fd66e10084783208c7cc3adad23d5c975d8f5be56c462c5a37d7a50fffacb677 in / 
# Tue, 13 Feb 2024 01:22:34 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:20:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:20:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:22:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a9ce49138215d345df26ba8499250bd7c71ec90f1afb15a8ac29dcd7248b188d`  
		Last Modified: Tue, 13 Feb 2024 01:29:59 GMT  
		Size: 46.9 MB (46928854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bed3d75f3913415a967fa0e909adbaf536b4d7ca377cf97730e2135c92b5c0f`  
		Last Modified: Tue, 13 Feb 2024 04:30:48 GMT  
		Size: 22.4 MB (22360614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78cb86ad182c3cf9cfed5742a1bbd6365a9bcb95a5f378a558088dbcfe7364a`  
		Last Modified: Tue, 13 Feb 2024 04:31:10 GMT  
		Size: 61.5 MB (61467747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496516de4f431d258aba363886cad002ce4f57baeffcdf4e252ed7edd24c0f9`  
		Last Modified: Tue, 13 Feb 2024 04:31:58 GMT  
		Size: 218.0 MB (218020845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ef6f4e52aedd829ce0de3122b8bfe1e5183b239ce9800e3afcf4907cf1d197ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.9 MB (396879453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c044fcdcdaf492bfea47c5177557c1bf675e3cd2e85cc79f253d540155bdc1bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:46:41 GMT
ADD file:1202a56d8723ce5bee3f68e3d9488cef88889fe8b2bb138cde766ff787577a7b in / 
# Tue, 12 Mar 2024 00:46:42 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:29:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 01:29:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 01:31:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8e7b106821c007c3c67e9a4d248bd2f87194491ad746f2aa752c5b0ba2fca099`  
		Last Modified: Tue, 12 Mar 2024 00:51:35 GMT  
		Size: 51.4 MB (51353263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa13c84a803d4b150b717babd5d0b89e39ce55a7c4c07cfbc3d34a5e4ce85a3`  
		Last Modified: Tue, 12 Mar 2024 01:37:43 GMT  
		Size: 25.4 MB (25434519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde6d0bb19e702e70dc6d3b44c7538729b197d5c5c229f8df55709b3de11f031`  
		Last Modified: Tue, 12 Mar 2024 01:37:59 GMT  
		Size: 66.5 MB (66509574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723b9d30029b8a3ce50c4cc475df5ca33be0f8c86a353160538d9108af4cbb3e`  
		Last Modified: Tue, 12 Mar 2024 01:38:31 GMT  
		Size: 253.6 MB (253582097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:251fddb93de647e92e5db9520b50e234245592088d0ea64935cc2fc9cc92550f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.6 MB (403617689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8e0fb16df1b72057c3fe1def6cc1a9b8c83fe2c54bd9320847a6a63ffc2d62`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:38 GMT
ADD file:4189b090bbf8678fcabd8dabb56450346892e68ce7343823f5a1de966a7cfba7 in / 
# Tue, 13 Feb 2024 00:40:38 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:26:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:986c70cdc0585f2b2041c18972cf24b00e1384bf0ae25efa4ed418df60c27f39`  
		Last Modified: Tue, 13 Feb 2024 00:47:09 GMT  
		Size: 53.2 MB (53166067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5992ae92ecc708d9f7dbc50c93a7a44033fbb23286817ad552428376a53b6b21`  
		Last Modified: Tue, 13 Feb 2024 01:33:35 GMT  
		Size: 25.3 MB (25291521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b34fbe23d33273890d47ce232e0ea3ecafabe7cd6f1eacdaed0132a34c12c8`  
		Last Modified: Tue, 13 Feb 2024 01:34:03 GMT  
		Size: 68.2 MB (68249193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef40ea4fb0aaa505ca0fc627a4b7f559f54d7f3a06a621779b84c00fb13dc3d`  
		Last Modified: Tue, 13 Feb 2024 01:35:03 GMT  
		Size: 256.9 MB (256910908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c0d2300446edff839cb063ac7a8dc845a74c03c732a3868c7dc4deb9300269bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.4 MB (375422462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed2ca0dee0dbf1557318206200e117f1237811d5a0ac18ae5ad5153914f3719`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:09:20 GMT
ADD file:19ebc3428f26cc4bc4aed9fbd4cf7f5f3ee4b77b9740ca3ad10c77626e14bc82 in / 
# Tue, 12 Mar 2024 01:09:25 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:21:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 02:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 02:30:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:38f59bdee9eac9fb953df0852a9bf0458844eaf90c474ba863879a284671eca6`  
		Last Modified: Tue, 12 Mar 2024 01:21:04 GMT  
		Size: 50.6 MB (50572329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77dad95891fc49c3987711b4646cb679c4a443baceb97ed9b60ab673bd2cbc6`  
		Last Modified: Tue, 12 Mar 2024 02:48:12 GMT  
		Size: 25.8 MB (25808530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f996b43c740b01d384ef1b4622f6eac51f1f4cb47817c970679a8ba8881f17`  
		Last Modified: Tue, 12 Mar 2024 02:49:05 GMT  
		Size: 65.3 MB (65326963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f781607f9c9361dc741ecd526a2bd1bc08dcd231e5a125d5679db5ba19faa25b`  
		Last Modified: Tue, 12 Mar 2024 02:51:43 GMT  
		Size: 233.7 MB (233714640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0211410863f9de298e261695cb8cb0c3da518581ab739c8e52b2a39840084104
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.3 MB (420310647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8233bf961e14eb63c2c122a0de90efc96f1c4ad16ee563632a9b7ddd87ba2a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:32:08 GMT
ADD file:5a26866ec93cd672e68eb3b6408e2d78eb1ceb2804d316ab9e215bb248c396ea in / 
# Tue, 12 Mar 2024 00:32:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:51:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 01:53:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 02:05:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7d54e43a79af3d6c46553326fe893093beb487d05a53a78510db1edf5ad46734`  
		Last Modified: Tue, 12 Mar 2024 00:40:01 GMT  
		Size: 55.3 MB (55261063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b06e7f021e50f240952103e6d889ea6a36f09aeae1132a71b34e28c7e5d70c0`  
		Last Modified: Tue, 12 Mar 2024 02:22:32 GMT  
		Size: 28.0 MB (27970194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f298aba92b6ebc1731fe8f0003d6c289890904a73a002d5cbf70fa000e9f484e`  
		Last Modified: Tue, 12 Mar 2024 02:22:52 GMT  
		Size: 71.9 MB (71886737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6ff6eb1c6259dff919ad3bf85de7e22274002fae2dd6c5d325c51017560d78`  
		Last Modified: Tue, 12 Mar 2024 02:23:42 GMT  
		Size: 265.2 MB (265192653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:6c3d3c28d0798409f79e2c12e7c382fbe02438e2d872122f26d81e0408c6928f
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.7 MB (439705173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c08ee24ef8e58044f17bd2ec9d1260ab56f2bf9a2bd429dc2c0c8b417ed3f9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:08:51 GMT
ADD file:ad62fb7e744226b84b9b87b22c6b1e797cb2a179f4f2c7295e0db14b95dcd84a in / 
# Tue, 12 Mar 2024 01:08:54 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:30:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 01:32:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 01:40:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9c2efbfef38bc6f28418aabddc7ba24be7bed3ebbd2673ebc8db7533e9ae8c47`  
		Last Modified: Tue, 12 Mar 2024 01:11:24 GMT  
		Size: 49.7 MB (49682014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ab338dc4eeec296303efc67a955dedb7028ccf69f05896a788076dbc0a4108`  
		Last Modified: Tue, 12 Mar 2024 01:41:00 GMT  
		Size: 24.7 MB (24700091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ca4553b75aacf6fefe0df7808ade0293c53b5a2b5926e00353a53712d08926`  
		Last Modified: Tue, 12 Mar 2024 01:42:04 GMT  
		Size: 66.6 MB (66645885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b421251d69b0b51ecca7046816c9f4249e4ac2e888c4d98bd3392fac2df2f8`  
		Last Modified: Tue, 12 Mar 2024 01:47:28 GMT  
		Size: 298.7 MB (298677183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0cdfb88b12e4e11b5e9eaf7e76e61c13cecff0c41863acc661470d4a6a3089a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.3 MB (386293511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6865f83ca92b223674a38572aadc38153bddbe8d8d0163625aafecd7e35fb1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:02:33 GMT
ADD file:5d186ec2d875f4307a34d264914243316106515ef9072abb7cf5e80c252da588 in / 
# Tue, 12 Mar 2024 01:02:36 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:21:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 02:23:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 02:25:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ec6259c8a823fea482e8e351d24e5f493bd9f11e76074191518e50ac63335314`  
		Last Modified: Tue, 12 Mar 2024 01:22:34 GMT  
		Size: 50.9 MB (50889351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d95670fd7000d49d11835682e227fc4e48c87caf6a3e9e49895a14def51b2b0`  
		Last Modified: Tue, 12 Mar 2024 02:49:09 GMT  
		Size: 26.5 MB (26533843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87389e1f052bd2d528d17fbca9aa5301a48fb6e559141c54ae9654424026ef2`  
		Last Modified: Tue, 12 Mar 2024 02:49:25 GMT  
		Size: 68.5 MB (68488916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e593eefe1b3836c496580f39c7e36c21677ecc11c1c00d0609c56c0218f2086`  
		Last Modified: Tue, 12 Mar 2024 02:50:01 GMT  
		Size: 240.4 MB (240381401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
