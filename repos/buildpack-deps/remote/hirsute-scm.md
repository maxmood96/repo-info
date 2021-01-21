## `buildpack-deps:hirsute-scm`

```console
$ docker pull buildpack-deps@sha256:f0adaaa7aec67b3f5208702e5c0f5a6c1941455428becd1922e966550bbebf44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:hirsute-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7b64a30442d1a80485e6fe5a89bea0f30db92ec4a9a48568cc1eab8766374940
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86805885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7609ba6582c3e2684a02ed7538b6caffa6eda1e527f55ee81f33c65feb6a4159`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:50 GMT
ADD file:da9cbdfeec02bbcbb0e30d1ca149ee24af676961d884bf6a903ad59d4d4d2c93 in / 
# Wed, 25 Nov 2020 22:25:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:52 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:53 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 17:15:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 17:15:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 17:16:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1afde3c20e440b7119bc6cf3b8b46e4353cfd8aaa8212bce9fcc2fb1ad58dd38`  
		Last Modified: Thu, 19 Nov 2020 23:17:37 GMT  
		Size: 31.4 MB (31388426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507a3e5d452adc0eb8771ea6dd22da580446b5bd8053c60dfb78a1901a0b804c`  
		Last Modified: Wed, 25 Nov 2020 22:27:04 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92410192260292c4dc7cb4c2fa3175f491b370fa6e1d73e5deb9a3195828de73`  
		Last Modified: Wed, 25 Nov 2020 22:27:04 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd03255284c39646d1eb19c98be25878c44943e83fce6eb74a4140c9de244009`  
		Last Modified: Thu, 17 Dec 2020 17:32:26 GMT  
		Size: 5.4 MB (5416351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a619f23e9336fa1524f8590fb183820b619586ac1224dfc7a40c79914855f47`  
		Last Modified: Thu, 17 Dec 2020 17:32:26 GMT  
		Size: 3.7 MB (3653538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b048788cca8ff7debed52f9a21a3fd677c9f3c0061b73b4e6e1d2460f62e5c0`  
		Last Modified: Thu, 17 Dec 2020 17:32:43 GMT  
		Size: 46.3 MB (46346563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9e30accc7d13b2dfd2e39ef1b22a36d52130385f3b16b94f858c225eb773e6a2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74750959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684dc87af4cfa8515ef78a66300abdf20b32badaa875a8d7756004d0975d810a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:16:37 GMT
ADD file:17dded3554995c7f12ad86abacb523730fe17017e48093ae340e779080122701 in / 
# Thu, 21 Jan 2021 03:16:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:16:43 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:16:45 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:16:45 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:04:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:05:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 21 Jan 2021 04:05:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1c1d7645d96367e0e58c2117b33678b731340f21acdc2aba38e49b8e4128fa4`  
		Last Modified: Thu, 21 Jan 2021 03:19:14 GMT  
		Size: 26.7 MB (26731722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cacf450487d500884c8613e1734fc50f9a652684e5e942828fd5d8f68bb5fd`  
		Last Modified: Thu, 21 Jan 2021 03:19:09 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f33cffa01c22ffcbd890307b89197daf2376e0d269232fcad8ff8785900ed10`  
		Last Modified: Thu, 21 Jan 2021 03:19:08 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee69371d3b2588094ab562eeae01bcfef4abbf4a0ad39a4f2dc89ab467a33789`  
		Last Modified: Thu, 21 Jan 2021 04:17:34 GMT  
		Size: 4.8 MB (4844261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a98674e9b1f0b7b242fde8f3e1deca637083fc3591884ef878cabb731230c6`  
		Last Modified: Thu, 21 Jan 2021 04:17:33 GMT  
		Size: 3.3 MB (3336602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d68796583ef93aa272a1fae0f9eb867c46a03fb8b653819d2679ae1657e8c8`  
		Last Modified: Thu, 21 Jan 2021 04:18:00 GMT  
		Size: 39.8 MB (39837339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a436f91924bc8aaef0a435e168524194d1ac5defbefc17f70027b0ed3297d811
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.3 MB (85261072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a921027bf4557955b67cc377f351011fe1972df62063019bfe58c36baa610099`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:43:49 GMT
ADD file:684109072834ffe6e5130fb786fe91fb344b842b0adfdfed022c072948606081 in / 
# Wed, 25 Nov 2020 22:43:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:43:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:43:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:43:57 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 10:27:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 10:27:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 10:28:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4de913dcc000107d6987a8212435904776bb6d08325b00bcf57becd50f5aacde`  
		Last Modified: Mon, 23 Nov 2020 22:53:53 GMT  
		Size: 29.9 MB (29924288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1104249546118ee3a916a469a5b852ee61a921a17589c55aadd35286f864487d`  
		Last Modified: Wed, 25 Nov 2020 22:45:25 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff31b6873067a11ca32a6a935eae861c6cfa61b77f3d57b7e7223bda5e9162ac`  
		Last Modified: Wed, 25 Nov 2020 22:45:25 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b531874dd96010e121cdf89631969afcb00ff3b121dd2aba82b26af641b141`  
		Last Modified: Thu, 17 Dec 2020 10:47:13 GMT  
		Size: 5.4 MB (5390356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce68abf4d50703a9e41c0014aa88574581434e05e9a1128a80de5c8beedd6fbb`  
		Last Modified: Thu, 17 Dec 2020 10:47:13 GMT  
		Size: 3.6 MB (3637680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ffda80240334287fbfd80ba24324f45c5c796de703a186c9e214abf84b17bd`  
		Last Modified: Thu, 17 Dec 2020 10:47:35 GMT  
		Size: 46.3 MB (46307713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4def5e8a0a7facc74a729954db458fab05b5647ac4d30a649a3c5df038150859
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99629668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b30587b30bd65553e8eb2d10dc6b428ea990678a472ef76a31057d1d2ba291`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:24:36 GMT
ADD file:7c6f20c78db8a5e913be3784f42a557420b7e60e43dfe32b28154ce7311a7f3f in / 
# Wed, 25 Nov 2020 22:24:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:24:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:07 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:14 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 12:51:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 12:52:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 12:56:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ed69aeab3e882b1389707f276ef98da7c3a795efbc8328e98149f7a9de3c649d`  
		Last Modified: Mon, 23 Nov 2020 22:54:25 GMT  
		Size: 36.6 MB (36590516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64270d1e4e0240a2588ad3f07aece9b4d644ed596fc43d2738ad1b6c20a5ba8c`  
		Last Modified: Wed, 25 Nov 2020 22:28:20 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a232cf481e695a04573f464da1605895dd2b0dafd65442b0ab75672d7efc50`  
		Last Modified: Wed, 25 Nov 2020 22:28:20 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d5f59ccfe38296fb18c30ffd4bb449b50eb13d4bc1046f014b1ab5266854ba`  
		Last Modified: Thu, 17 Dec 2020 13:59:00 GMT  
		Size: 6.1 MB (6059938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119446ace209daadeafc6866e500cb81f12999cea1ffe6158ec75db20b99dc23`  
		Last Modified: Thu, 17 Dec 2020 13:58:54 GMT  
		Size: 4.5 MB (4520258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4a9085234447260746e9ae607f1755cf64bfde7981eddeac6b2e7a7f99b596`  
		Last Modified: Thu, 17 Dec 2020 14:00:13 GMT  
		Size: 52.5 MB (52457917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6dfe6e52ff7766c5a0437e8c800a2368a8c9985abfb25da4081a21f4265da36a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91506318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57afced181881ecfbde9da40206d91244f5b7138f75747609b277eddb4f8bd5f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:46:04 GMT
ADD file:ab12e008ff291c18206f1e8490e1672e3ea2aaf390bc444f49317287a034af37 in / 
# Wed, 25 Nov 2020 22:46:11 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:46:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:46:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:46:15 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 11:35:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 11:35:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 11:36:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b3e953add5ac1dcec2264f9083ff5d7dee945c64eb63c1f15f7dec6e9e257095`  
		Last Modified: Mon, 23 Nov 2020 22:55:01 GMT  
		Size: 31.7 MB (31703544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b16aa65d410ea610c84dcc79a64a6ab6587c25f53847b375c660cb1d320946d`  
		Last Modified: Wed, 25 Nov 2020 22:47:46 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93420f7924d968c4d93a439a147955351d7e1a8169caa9b28ae2bbb7d0339cf`  
		Last Modified: Wed, 25 Nov 2020 22:47:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6935d839a42a9a1159cba983cd08b88aaf5f8429c1131a8391da35a1216876f`  
		Last Modified: Thu, 17 Dec 2020 11:51:49 GMT  
		Size: 5.6 MB (5644141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7b74d50fc8289baab6caa8d019fdb678050fab25290d215eb451a501ec6ad9`  
		Last Modified: Thu, 17 Dec 2020 11:51:49 GMT  
		Size: 3.7 MB (3674886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce32436fbfd60f98a1fbfc020cdd306bee49367e04c45ceb09e5636110e9569`  
		Last Modified: Thu, 17 Dec 2020 11:52:06 GMT  
		Size: 50.5 MB (50482711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
