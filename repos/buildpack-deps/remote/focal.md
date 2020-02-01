## `buildpack-deps:focal`

```console
$ docker pull buildpack-deps@sha256:73354a636011d6cf7fd52b354205bb8414d18186c174b7a31f38111b0a879d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:744c8f965ad15054de7625ba44e33c09f5b0c650a3a6633452aedd05286904b1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245615443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c25d4c50b24ccab9932177b660c2ad31e1d9aaf5588a1d6bc8330903350b2f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:23:16 GMT
ADD file:313024b5cf55edbc2a5804a2000516a581cea278d31b4232050889af00db05e4 in / 
# Thu, 19 Dec 2019 04:23:17 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:23:18 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:23:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:23:19 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:32:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:32:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Dec 2019 07:32:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:34:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b6ea110572053dea2a331bd22b1a9892370ea765f1a2e53f0f56870daa39e76b`  
		Last Modified: Mon, 02 Dec 2019 15:36:40 GMT  
		Size: 28.3 MB (28327971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70e5e5e771c2cc6911e116937467415641a3b20961af36f37becfacf6f3db4`  
		Last Modified: Thu, 19 Dec 2019 04:25:29 GMT  
		Size: 30.6 KB (30624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87d55335709377cbe36b97025840286bb6ce3db2690126b17a73779948b318a`  
		Last Modified: Thu, 19 Dec 2019 04:25:29 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac97c047f450d89bde54d10c362609ba5f24706397df1fe983895f26c1a759e`  
		Last Modified: Thu, 19 Dec 2019 04:25:30 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99398a525264c90444695946f7dc89901530fc4cba52dbb051f4381e35ad7297`  
		Last Modified: Thu, 19 Dec 2019 07:42:01 GMT  
		Size: 6.9 MB (6873646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615b325ba2bf22205e7d8c01b2debef6d1d6bbe54ecb735af373028e97a87240`  
		Last Modified: Thu, 19 Dec 2019 07:42:00 GMT  
		Size: 3.6 MB (3550104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327813c2a40da984f91b631e31ea4ad1151154645dd9bcc858fd5ab74bd27586`  
		Last Modified: Thu, 19 Dec 2019 07:42:17 GMT  
		Size: 49.3 MB (49299245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec8a5ee41a98618dab20f35743d588e5275caa3864049210d238f27eda43e0b`  
		Last Modified: Thu, 19 Dec 2019 07:42:54 GMT  
		Size: 157.5 MB (157532847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:90c6afe873ffa6eb293fccd4ef6ba5d65fe50d45058a4332ef7c3b2ca5c1823f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.6 MB (210565432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91a996fb82d78107dcb54342d66a26d1f7d2c5bd70a08213e85f7712d7f442a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:12:01 GMT
ADD file:a83a5ca41e5d338077de0100edb1eeb1270147fb92480334009a6bf60d77ed55 in / 
# Thu, 19 Dec 2019 06:12:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:12:11 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:12:13 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:12:15 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:50:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:51:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Dec 2019 07:51:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:54:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7a0f5ae94065e1ed84123f74da1c43b7615043cd0703476aa5d3964646741ed2`  
		Last Modified: Mon, 02 Dec 2019 15:37:27 GMT  
		Size: 23.8 MB (23805081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce60abded96d3844e8100be41eb0efd81e3dc5095465c20c75a5614516d942f7`  
		Last Modified: Thu, 19 Dec 2019 06:15:26 GMT  
		Size: 30.6 KB (30598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf0ece898bded66a70bbfcc9b3a71f72154f8a7313ac8a8da9245c13421bd3a`  
		Last Modified: Thu, 19 Dec 2019 06:15:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e9bc5f1170de67d9befe861b7c1d697e41059b5df99c390bd006d0a02a597e`  
		Last Modified: Thu, 19 Dec 2019 06:15:27 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5c88cf0a1482c0aee58ef410192eb502ffa415d96fa29624bcc6d5a624f1d4`  
		Last Modified: Thu, 19 Dec 2019 08:03:00 GMT  
		Size: 5.9 MB (5870993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f882220708c48e547e027fa6b985646ca014afa115a16181505a60aaa62e6236`  
		Last Modified: Thu, 19 Dec 2019 08:02:58 GMT  
		Size: 3.0 MB (3035732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e2922328979b9f7899472c65b52d9f1781f50e2ef42aeaf03eec1489a83ffe`  
		Last Modified: Thu, 19 Dec 2019 08:03:23 GMT  
		Size: 44.7 MB (44653595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1030195ab95c7c88eee42a18aada51ba200a6025d045d8835021732843641fc1`  
		Last Modified: Thu, 19 Dec 2019 08:04:08 GMT  
		Size: 133.2 MB (133168399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7b6417c9b3db790f963cc8f7cff4117e319e99454691fcd87b7183114f4d9859
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226278765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a514297801b09ef4b2f4be97a49a2d38efe27bb0bc325eac541bc9d7985bc5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 00:42:08 GMT
ADD file:3f5a5ff4e005ffd96a9a56c4234117276101fd4cd6b87b503fad5d3f02319d92 in / 
# Thu, 16 Jan 2020 00:42:11 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 00:42:13 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 00:42:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 00:42:15 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 03:38:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 03:38:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:23:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:25:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d0804342421c30932eee7f90821efd1e7dac9398a9cac78b662e33b2a3faeeb3`  
		Last Modified: Thu, 16 Jan 2020 00:44:12 GMT  
		Size: 26.9 MB (26946995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d926bd5118332af73957eb2925d9433286ec09620aa22ed01eaca19e89d76a`  
		Last Modified: Thu, 16 Jan 2020 00:44:05 GMT  
		Size: 30.4 KB (30431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3420a5d9e296a9e1a3d258bef98c8dd8f40f3b0767cdb42b424acdee2b47b2b9`  
		Last Modified: Thu, 16 Jan 2020 00:44:05 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86fe98d56e47198b1f7b547c1dfac333460f1aa23177768180ca62714aaa1d2`  
		Last Modified: Thu, 16 Jan 2020 00:44:05 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebffadfd1bd9db1f35ea7942f2457a5475eee02fce466030cf2e2da39dc9948`  
		Last Modified: Thu, 16 Jan 2020 03:47:49 GMT  
		Size: 6.7 MB (6739368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4410fa1780605483266ecbe523da188f5362a00abf527fe01c5d9e4c010435`  
		Last Modified: Thu, 16 Jan 2020 03:47:49 GMT  
		Size: 3.5 MB (3525553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41628ee665893a420f339aaf1f9f351c2689490d55664c39947115fc62e88223`  
		Last Modified: Sat, 01 Feb 2020 17:36:43 GMT  
		Size: 60.2 MB (60177141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e3a90ee84ab1f6a4067fc7c8237b216b07c187ac8e866eeac48e8d6fc8ee2e`  
		Last Modified: Sat, 01 Feb 2020 17:37:25 GMT  
		Size: 128.9 MB (128858241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:74e67467737c8fbad653c9a5a0afe59ab789045636c20fecf14872e00897b7af
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273404183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b67cc9be6f3d7ddab909bd1a4e054e0cd82bd35def020b63cbea6b4cb12c83f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:19:56 GMT
ADD file:437e0dd068bae1687e4e04e19ec96243aa4afebbab660b1b5bdba8eb5e91f050 in / 
# Thu, 19 Dec 2019 04:20:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:20:13 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:20:20 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:20:22 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 09:55:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:56:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Dec 2019 09:58:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:06:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9af97d6b262669f0a51c75da370ddb33c65b7e7ad545f9a4a28b9c69ae3fcd6b`  
		Last Modified: Mon, 02 Dec 2019 15:38:34 GMT  
		Size: 33.0 MB (33020635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb39a6993f6cc585b3a0610af82965873a030d940f186262498c01f583f18cc`  
		Last Modified: Thu, 19 Dec 2019 04:26:04 GMT  
		Size: 30.5 KB (30510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fe3a933635c2b53543e636825818e38c0637805ed3b268d71de4140148b984`  
		Last Modified: Thu, 19 Dec 2019 04:26:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9229b1ca1966e1e3d889dd099e41076b9832b790da0c37314ab2d3a45a8507c0`  
		Last Modified: Thu, 19 Dec 2019 04:26:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ad492b54e0a93c36460b2aa9ca5e2bf1886addad53033a96f7de5c54eb35ae`  
		Last Modified: Thu, 19 Dec 2019 10:35:44 GMT  
		Size: 7.8 MB (7838027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3bc0cc5d842bc061a79c390b56632b108dd0d780bf80ead2022b7571f16f9c7`  
		Last Modified: Thu, 19 Dec 2019 10:35:40 GMT  
		Size: 4.4 MB (4383403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9172fc10778afdb6ced8ba4e3a93707a397e8139b77b549cb70f87e80ac0e1b`  
		Last Modified: Thu, 19 Dec 2019 10:38:01 GMT  
		Size: 57.3 MB (57281163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531b1faac3c585e4ae727c4b6b71bae2a4d20324290e63dc974bb966f58110b5`  
		Last Modified: Thu, 19 Dec 2019 10:42:12 GMT  
		Size: 170.8 MB (170849409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5633c89ac1b2787fc88e32a3fa26d1430570798126a29158ab035b35c434e4cc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227822088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5add6a160f625228a52c8882e1f877f4d40c1874e0e88c3dc510a1f3ffc4ee98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 01:19:25 GMT
ADD file:b9a490c397526d0bca4d55a54206474d9fecee3c2a9549fc1ae070c71d130e02 in / 
# Thu, 19 Dec 2019 01:19:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 01:19:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 01:19:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 01:19:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 01:53:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 01:53:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Dec 2019 01:53:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 01:55:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc2cfd159ad6ddf185132f3f67f5c2bab1bf0ff3f9951198587295ef1c3b4e09`  
		Last Modified: Thu, 19 Dec 2019 01:20:26 GMT  
		Size: 26.8 MB (26833591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18cf21184d9a1ffd948dab718f14cbc2b7d7564d1ff0366e2681b39671787a1`  
		Last Modified: Thu, 19 Dec 2019 01:20:22 GMT  
		Size: 31.1 KB (31125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0abd1a2a2cea23ca1af5898aac37fed96083fb9da955ea9009be01e5a0b35a`  
		Last Modified: Thu, 19 Dec 2019 01:20:23 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9835afd05a92ecd719c24aa21252ae6c496a0dcd02dc5d598d930ef248ee5b24`  
		Last Modified: Thu, 19 Dec 2019 01:20:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2941f0d0ed4234469e99d55d86a30fff269f359eec9ffd6c4b8ad47563a8beaa`  
		Last Modified: Thu, 19 Dec 2019 01:59:44 GMT  
		Size: 6.5 MB (6523219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8665a013e0fd4f2111cc629d399ed58992dba8d0365f5ca7b56a5e5b7a7156cf`  
		Last Modified: Thu, 19 Dec 2019 01:59:44 GMT  
		Size: 3.5 MB (3537207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb41bd5983299b065f3bae3127d1a8fa8e7344e3585dbac58cb76990e4b5e3b6`  
		Last Modified: Thu, 19 Dec 2019 01:59:57 GMT  
		Size: 49.0 MB (49000195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b65dae26abc32ea023e1533649173cf6aceaabc3b8e471809bd08eb89fcece8`  
		Last Modified: Thu, 19 Dec 2019 02:00:19 GMT  
		Size: 141.9 MB (141895747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
