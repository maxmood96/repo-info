## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:d44c029ef98bfed18d0783fa45bc93822ac776e62bce784e1caad3df0541b5ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9fab1092dd6c638eae643898d118ea881a65d5775ac30bef0a1d95f31cf99abd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.8 MB (321831838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e72ff1f31a17f6443e72f857e2faab189bb54123c83a091a5262e9a61406cfd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:04 GMT
ADD file:a858c472d72a55a1ed0b7b2fd2751bac78f77e3549a7533c508022aef7204233 in / 
# Fri, 12 Mar 2021 02:20:04 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:47:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:48:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 02:48:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:49:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:da21a291c553cde4f403910fa28fb69cad95f63ce1b378f341eb17738b45a6ac`  
		Last Modified: Fri, 12 Mar 2021 02:24:58 GMT  
		Size: 54.8 MB (54835833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f47dd55341835080544d848892987ce23838db35fe64a0d4338b1494ad6ed1c`  
		Last Modified: Fri, 12 Mar 2021 03:17:40 GMT  
		Size: 5.1 MB (5136253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb0644d825d57df2b92d247999a507695a22522c5fa2bd93de229b003ea515b`  
		Last Modified: Fri, 12 Mar 2021 03:17:40 GMT  
		Size: 10.9 MB (10860722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bb105cb94d3a12e9d1648ac4750f9b7b3f837fc623dff8a5676d1892f8ea7b`  
		Last Modified: Fri, 12 Mar 2021 03:18:07 GMT  
		Size: 54.6 MB (54573567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675c3488479ed98ce102d2010e80208c24e0536cae45d14b1c555b97d2a10269`  
		Last Modified: Fri, 12 Mar 2021 03:18:56 GMT  
		Size: 196.4 MB (196425463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c263f479d38f94e1dc00335b349d309ea1481460fc1bfbb685b3f9c6710d277b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.9 MB (294912138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f53682a61e604eaa55085c85a65580671cd1205ceb7ccaa1fde04bda8d536aa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 07:50:33 GMT
ADD file:1b779b19b47bb1848292d2bf671b599eb9041626b747d8016817e0c7d46ff881 in / 
# Fri, 26 Mar 2021 07:50:38 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 09:04:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:05:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 09:06:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:09:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d8d862331f8860c127d174052922618c93a166777e5b776e8b08e87702af28cd`  
		Last Modified: Fri, 26 Mar 2021 07:59:08 GMT  
		Size: 52.4 MB (52404525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6864d5c0a91a133802b130cddb5c9fb77329c250e4f5d77c05e96188cbcb31`  
		Last Modified: Fri, 26 Mar 2021 09:25:47 GMT  
		Size: 5.1 MB (5060013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a0cf03c5e0e5a428fa3a5789c4793210e762dbfb24e1f688a878754fe9ada6`  
		Last Modified: Fri, 26 Mar 2021 09:25:48 GMT  
		Size: 10.6 MB (10569895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1985045f60a052a5d3b4e89129ae9f03ece21620c4b057aa105c0c78cc5775a4`  
		Last Modified: Fri, 26 Mar 2021 09:26:11 GMT  
		Size: 52.3 MB (52314372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6846d74db7fd55b80f3ec7ee2ac5146b6ab9455ce7043c5022f74119885c0a7`  
		Last Modified: Fri, 26 Mar 2021 09:27:26 GMT  
		Size: 174.6 MB (174563333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f05a1dbc5c33a74d5bb902370e74b5864acdff9632ccf1dbe265b2d66bac009d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282356628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a8169828866600f63899ac1d708ea5bd22d49b806e32ca2b2848a6bb9ebbd8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:58:33 GMT
ADD file:af7fbd0fe0efe7b818f1484ffecc74c401c4d5b949e8e054570ea8cc7a7ed73b in / 
# Fri, 12 Mar 2021 01:58:40 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:27:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:28:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 03:28:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:31:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2e093244fe0614201f8731e47ce0387edd785d9fbbe8924f2c8e435a7afabe60`  
		Last Modified: Fri, 12 Mar 2021 02:09:18 GMT  
		Size: 50.0 MB (50033302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66de6d835f521bb9c85648b5a81b3279e777ef73195f17383766d6b48701c5f`  
		Last Modified: Fri, 12 Mar 2021 03:45:35 GMT  
		Size: 4.9 MB (4905657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e0b8fc9d72ae8c961878dc03047f7edad8e5025511797effcbca240ae292ee`  
		Last Modified: Fri, 12 Mar 2021 03:45:36 GMT  
		Size: 10.2 MB (10210700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39390d25b386b175cc7e224483f06ef668d193a9ace290ce05b76ec680089826`  
		Last Modified: Fri, 12 Mar 2021 03:45:58 GMT  
		Size: 50.3 MB (50333470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30bea69160675debff03497371b8984c3c5c624518fd5416b38532cd5abee602`  
		Last Modified: Fri, 12 Mar 2021 03:46:55 GMT  
		Size: 166.9 MB (166873499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:76ee27761779d194ec609dab05a9164abce4cda75326622c7bd546f9a9fc49f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313447854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5edb6823487cf216272dc601657b98090a8265d50bc201770094919384b61a03`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:52:22 GMT
ADD file:0b6f3c6d396337f2754d539814c02240e0a459436f4c0992dabf1736069b5a51 in / 
# Fri, 12 Mar 2021 01:52:29 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:26:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 02:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:28:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6c214bbe001dfa953738440417693c3487f97b371a108bdd62425a704347faf8`  
		Last Modified: Fri, 12 Mar 2021 02:00:33 GMT  
		Size: 53.5 MB (53521132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1332f0d3a2e68785b75d30a2f0eeb7e0902ecf1068899b78d4a7e90f5201cf7f`  
		Last Modified: Fri, 12 Mar 2021 02:42:02 GMT  
		Size: 5.1 MB (5125702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70aaac2a7c6ebfc86100e530f2607998a0f8d84b4305495031bbfe789e6e1c2d`  
		Last Modified: Fri, 12 Mar 2021 02:42:03 GMT  
		Size: 10.9 MB (10860189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c201b24dcdc8bd225ab1c164d5ff733c78eb97a701f50d2841449244aa6b43`  
		Last Modified: Fri, 12 Mar 2021 02:42:31 GMT  
		Size: 54.7 MB (54675060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e89dfecfc0f3ea79ccc220c0a07813a3ab3915b2451535f378adfca5216aaac`  
		Last Modified: Fri, 12 Mar 2021 02:43:21 GMT  
		Size: 189.3 MB (189265771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:00ec13b8b60399d4708963a121d6c6cd95f2697cf47a5e59e9a0bdc22f51cedf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.6 MB (327593813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff8b4b297cc0aa04ce85209c7ad9bb9dce96f2f504f1be05a108b1bb52c9ce7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:43:42 GMT
ADD file:bed5cd029b8a9960b76ca6cc40996e558168731aa38831163dfabe7bda8182fe in / 
# Fri, 12 Mar 2021 01:43:42 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:14:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 02:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:16:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0a9f57a86f966b0edd22e1658988495d14ac0adce930bd6b34f3b6d87ff6e270`  
		Last Modified: Fri, 12 Mar 2021 01:50:43 GMT  
		Size: 55.8 MB (55847447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c33e90bcc52eaf7fb93fd28bda768ee89e08c8939b9086f76ba8159568845e3`  
		Last Modified: Fri, 12 Mar 2021 02:34:41 GMT  
		Size: 5.3 MB (5265242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e489d2f5630e3afaad47643cb9f061ff6441e8510705f706d05e12959d9d8e3a`  
		Last Modified: Fri, 12 Mar 2021 02:34:43 GMT  
		Size: 11.2 MB (11240881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cd1263d3b296c32cb3ffdf8344c4fdb870ffa7924132de63c902bf7228f500`  
		Last Modified: Fri, 12 Mar 2021 02:35:11 GMT  
		Size: 55.9 MB (55903553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d39ddd1d040f0d09fdc6ba1d3ead6e1a08ade09cd07b7672bb91cd01e959b73`  
		Last Modified: Fri, 12 Mar 2021 02:36:03 GMT  
		Size: 199.3 MB (199336690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:ee72391480913b5a84b6ad85bf17684b69d11d5a8571fb11d3ad4bdabd5503a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.2 MB (301225638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee81b582048578486c7bd508d0709a15612f853461f2169025093057fc0a7cc6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:08:41 GMT
ADD file:1d48f0f2d8c8cb792d2bbc40d674fcf7f9cd253be061964acd9899304360add2 in / 
# Fri, 12 Mar 2021 02:08:42 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:04:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:04:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 03:05:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:08:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8a576eefe77178505a1242265c25ca38b94b29862aa56a6bf88c698de0ddc31d`  
		Last Modified: Fri, 12 Mar 2021 02:15:03 GMT  
		Size: 53.1 MB (53092083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed4895ee6979d25051187e6c8df7cfcd88bbb3c681b7ce775eb8d68b07962bb`  
		Last Modified: Fri, 12 Mar 2021 03:17:11 GMT  
		Size: 5.1 MB (5098054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6dd67088240632fdbd07e5c60a4b7a579388d081a123d8fb5f7522b43d632cc`  
		Last Modified: Fri, 12 Mar 2021 03:17:14 GMT  
		Size: 10.9 MB (10864207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f215da3f5ea6db6eab83dcb3cefed965fd799248492253375df1bd543f463499`  
		Last Modified: Fri, 12 Mar 2021 03:18:05 GMT  
		Size: 53.3 MB (53312230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a8fe48ea59057dbb228d3979a4380cb357d547d6ca8a91864e5f37d3eb899e`  
		Last Modified: Fri, 12 Mar 2021 03:20:16 GMT  
		Size: 178.9 MB (178859064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1a17bfc14f6aaf7571baeeadaa93a0c6e51eaa89d6f10714ecde1454d0098f78
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.3 MB (330325893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5080daf633333f86ed0a13370e05e6d5e642825fbd15384f6725948d818121`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:30:35 GMT
ADD file:73289d3f358472059064c70edf2135f994f4e4a8ab92fcc0434c1fd611d61e36 in / 
# Fri, 12 Mar 2021 02:30:47 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 10:37:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 10:38:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 10:43:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 11:00:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eab69212baf77adfba26ada26d0c2b425ac1dd30c3a5bf296485f437993872a2`  
		Last Modified: Fri, 12 Mar 2021 02:40:30 GMT  
		Size: 58.7 MB (58746419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db317d5fedb325c195599b5ae894eac6653f54840383838d929f8320084888f9`  
		Last Modified: Fri, 12 Mar 2021 11:54:21 GMT  
		Size: 5.4 MB (5386575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363f493170adbe10fa914f328698104fa7a698cd4fb5fa4ffe9b3d2f8901354a`  
		Last Modified: Fri, 12 Mar 2021 11:54:28 GMT  
		Size: 11.6 MB (11613810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10460b46a9541b31258ad3baa7c968f5230d30409d3ed9c0dd073edbec01543c`  
		Last Modified: Fri, 12 Mar 2021 11:55:53 GMT  
		Size: 58.8 MB (58847526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a57bea2b46011a1b36c2ef80cfb3b753a3faba4925b8d8968cc359806d2606`  
		Last Modified: Fri, 12 Mar 2021 11:59:47 GMT  
		Size: 195.7 MB (195731563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1193c80b816602188f0cbb74f373218964e729b3b217b8fb3843e78bd53e34f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295431667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cf74bed10461e9bfad3c263769f0a1b32b015eea7ce99709618bf0c0b93704`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:45:06 GMT
ADD file:cb5b3f6c2f66ddb51311634b097823751f759ee3270d06de8388ce763fe1087b in / 
# Fri, 12 Mar 2021 01:45:09 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:28:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:28:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 02:28:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:31:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a4cdb5376551135d812bdd513cc33a080cf675d45fd21d8c58d993497afb1e87`  
		Last Modified: Fri, 12 Mar 2021 01:49:44 GMT  
		Size: 53.1 MB (53110995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2d00c7fd437d5508e95a96dd508b356303e256508643d5d6fee7c1e90b2aee`  
		Last Modified: Fri, 12 Mar 2021 02:38:37 GMT  
		Size: 5.1 MB (5121380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8325387d172e529e98282cbf5484e36eb26e81012e7894300cc43b35dee4780b`  
		Last Modified: Fri, 12 Mar 2021 02:38:37 GMT  
		Size: 10.8 MB (10752500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7666766b1f3f8d594995f9643256c8ab2c0b0ac550d63828b195d3594493e457`  
		Last Modified: Fri, 12 Mar 2021 02:38:52 GMT  
		Size: 54.0 MB (54045070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456d487b04a9abdb8e2cebf4395eecd3570fd776061a55567b2404c62affda41`  
		Last Modified: Fri, 12 Mar 2021 02:39:24 GMT  
		Size: 172.4 MB (172401722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
