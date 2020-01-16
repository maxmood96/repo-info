## `buildpack-deps:xenial`

```console
$ docker pull buildpack-deps@sha256:9a7ac207faa63d88c2b2772fb09cf17430b42b7f73ba24f491abed49aa53519e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:xenial` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a48497f0072d5f2d7ce8f00599c6065360bd6dbe3b2dabbfcffbaf598dc6f88b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233499201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f386474e1655582d98873a61a2f19e3e271790fe6dc09f119bedeac04c8cda`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 01:21:30 GMT
ADD file:4b2eb5cd0b37ca0154f3c5ad9212f5bc7244a35806395a9c76a96723d708b83a in / 
# Thu, 16 Jan 2020 01:21:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 01:21:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:21:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:21:32 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 03:14:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 03:14:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Jan 2020 03:14:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 03:16:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0a01a72a686c389637334de1e2d0012da298960366f6d8f358b8e10dc3b5e330`  
		Last Modified: Wed, 15 Jan 2020 14:20:15 GMT  
		Size: 44.1 MB (44149770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc899a5544da1a6cfb970d2484d32c063f8df26a430d92f39c98e72261e226f2`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 525.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19197c55075519928dd2ff059745665a2c9b72f4e8af6f7a1ce662e696d339bd`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716d454e56b61d1343a01f3b1829574333e2e3df20e77d1958d7b0b939ea1b61`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089dda700c10dc4afdeb81752043f7cf902b1587a3e2c94cf87219b111267121`  
		Last Modified: Thu, 16 Jan 2020 03:20:25 GMT  
		Size: 7.3 MB (7324556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465fbe9063b19f9dbd4141bbbf9b0d0f5174b02855442b9452a3e39791e5cea3`  
		Last Modified: Thu, 16 Jan 2020 03:20:39 GMT  
		Size: 41.8 MB (41845175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35780cf6ab8b8115dd29b1e4492ce1b867a6123fb4adc5ddeb34ce1cb5b4489a`  
		Last Modified: Thu, 16 Jan 2020 03:21:20 GMT  
		Size: 140.2 MB (140178163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:46fd111e798226517b6c6b02822ec14adf42da51d05dbe42b686cbd8f67d6ff5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.4 MB (200445342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d609cde20ada7d6439bf6da93df11eaddd502eca4373b0a944f4477d9d37040a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 01:03:19 GMT
ADD file:8ff374873b44e76e7a7762ed03569b1ed53a0b680461b5eab44a553e034c54ed in / 
# Thu, 16 Jan 2020 01:03:28 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 01:03:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:03:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:03:53 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 02:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 02:15:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Jan 2020 02:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 02:20:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e60df59fb5976f9565e2660056a379f90dbe8a58e5ee5451ec92647e519abb26`  
		Last Modified: Thu, 16 Jan 2020 01:05:33 GMT  
		Size: 38.8 MB (38847547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ba0251fafa2d367b89edee66fcb80412d5dfbf17c303256da18cf760c8a1f9`  
		Last Modified: Thu, 16 Jan 2020 01:05:21 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff14f7ed750ba6c66f6be53003361516dcaa6ae4c7d88746ce88a03484db05e`  
		Last Modified: Thu, 16 Jan 2020 01:05:21 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638c86faa0776e2a98a9a3d92814b0f90fb2ef3e3375d013fa61bb8c0c904046`  
		Last Modified: Thu, 16 Jan 2020 01:05:22 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93078258276d0c44f2e53da15041a68e0dc02eab50c482a7680e431fb423c536`  
		Last Modified: Thu, 16 Jan 2020 02:25:55 GMT  
		Size: 6.2 MB (6176075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7d91f3bb55e42c6b6642919c62605bd35504bafd4698e85e992ce2995fa74c`  
		Last Modified: Thu, 16 Jan 2020 02:26:15 GMT  
		Size: 38.1 MB (38116552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d697a618cecbfa1a8fca920e73180dc999f4c7b453335fc840532d7b4686942`  
		Last Modified: Thu, 16 Jan 2020 02:26:56 GMT  
		Size: 117.3 MB (117303637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:22b2cbc3668479e74f1f19652b80b5faf3fc17bdc97cec1e0746312dc1c3e8b8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208311057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b97c1cf00cc56b8b4222ce23e3121db59b61d1a8fa737229362a17d1cc5ce87`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 00:42:43 GMT
ADD file:d374c720bcf7aac426612a43ac539c3bb5b831a9a9e476a3919ed185eb77deca in / 
# Thu, 16 Jan 2020 00:42:53 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 00:42:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 00:43:02 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 00:43:03 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 03:40:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 03:40:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Jan 2020 03:40:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 03:43:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:185661474c6b71ced0eb4cd45f81a17a651d404bfd04903ba0bf3eb815e2cc1d`  
		Last Modified: Thu, 16 Jan 2020 00:44:31 GMT  
		Size: 39.9 MB (39890711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053aaa7a7ba304aae4e3327a0d30a33f5c3fe9fca6e8ef86dd8226b13c29e28d`  
		Last Modified: Thu, 16 Jan 2020 00:44:20 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ccb1337bb94e5b9ea19de7478366666cde129fb3214d092d15ebcfb644d8bb`  
		Last Modified: Thu, 16 Jan 2020 00:44:20 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d1fb143b02bcaaba5f01be18d73c8072c3687fe6e24464871a825e90416f60`  
		Last Modified: Thu, 16 Jan 2020 00:44:20 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5846897ba657eb54e77164a2da9d0a4e36ec593980d4c6cfaf2d1ab45f9adb`  
		Last Modified: Thu, 16 Jan 2020 03:48:01 GMT  
		Size: 6.4 MB (6382755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a286507cb96a5eecffd5557b70f2214ad21c895e5db720c5590aaa917cb930fb`  
		Last Modified: Thu, 16 Jan 2020 03:48:20 GMT  
		Size: 39.8 MB (39761994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f231a4ff63a5df7be384ff19834be76e9139d24a26aa5d9aa19cf569e47846`  
		Last Modified: Thu, 16 Jan 2020 03:48:59 GMT  
		Size: 122.3 MB (122274110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5d5cbbb58c97b6491baa2e2d0e900f5173d4426ec0af20ab8522ab5c61b3e0d4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234408293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033d59467ee0f26e91dc0ea17f58f26940fb422205b28a7bf965f45e9ec74eef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 00:39:41 GMT
ADD file:2f29178e69cd61ca12af8c20e2924c3a9e98afc47d2e5113b70d66212bb29d77 in / 
# Thu, 16 Jan 2020 00:39:42 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 00:39:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 00:39:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 00:39:43 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 01:26:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 01:26:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Jan 2020 01:27:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 01:29:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1ccce479dbb151a5387e4d6af6496351ef2da8868f1f1e2f95c978c0317be1f2`  
		Last Modified: Thu, 16 Jan 2020 00:40:37 GMT  
		Size: 44.1 MB (44126785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc90a128131a2c6b54763efb8cdc86cf1faed0bdee6bd0944a5bb77b9b23ea5`  
		Last Modified: Thu, 16 Jan 2020 00:40:27 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84873dcb4bf2e8774dddd5277cfe393a45561473a174610d9dcec92f5146dfec`  
		Last Modified: Thu, 16 Jan 2020 00:40:27 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3ce55b56e7f5623be9c9d6bf76afed805523855f6fea238cd0920a50b3a34f`  
		Last Modified: Thu, 16 Jan 2020 00:40:27 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fa6ab6980884003d8a1f5385885f67dedb1498af39fe429d3b841063c4fc11`  
		Last Modified: Thu, 16 Jan 2020 01:33:46 GMT  
		Size: 7.5 MB (7470075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed123659f2ad97825f693dfa4750884bcd308a0dc71e18a149ccd014c3b60cf0`  
		Last Modified: Thu, 16 Jan 2020 01:34:02 GMT  
		Size: 42.8 MB (42836033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f42ab7828d652d560f91292174b1428412d7a8444a7d7539fe7fb0d76b216`  
		Last Modified: Thu, 16 Jan 2020 01:34:36 GMT  
		Size: 140.0 MB (139973874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ac6546524c043a1aa0f6cfc38484ec5b1a42e736d3c96cd772d28f6665da82b8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243616613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388ad1d4b2c1a8ce30e0fef520b5129c1ba69ccdb83b7dcfa28a5306f66378b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 01:19:02 GMT
ADD file:ede483a9702bba446a7b0b4900b4ff93ad44a6e4c24f4a053112c3ade45c38c2 in / 
# Thu, 16 Jan 2020 01:19:08 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 01:19:13 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:19:17 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:19:19 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 02:42:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 02:42:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Jan 2020 02:45:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 02:53:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:37c3cf3eb1e042ee89428810f10789391511973eb89b6c62c7a88a3fba6c50ad`  
		Last Modified: Thu, 16 Jan 2020 01:21:23 GMT  
		Size: 46.1 MB (46067235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755466b12e9883b040990cba7f0c5fcb759b35577ccc7b15c7f67ceb1db7b20e`  
		Last Modified: Thu, 16 Jan 2020 01:21:12 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9243bf2bb93ed9a735b12ffbb1f7a9d17784045a9837a9703be3144b10c449e8`  
		Last Modified: Thu, 16 Jan 2020 01:21:12 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fad244c64092c2be0c599308d97f982c18e99750e95be9c4ae3863b0a8e0d2b`  
		Last Modified: Thu, 16 Jan 2020 01:21:12 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c642ccdd592d10a8f6c9e1d9e3513b92c0719c218298cf6fc25e3eb575e42fb2`  
		Last Modified: Thu, 16 Jan 2020 03:00:56 GMT  
		Size: 7.2 MB (7233122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f292d0b16c6358e2cc574a5c472cf296793b3fe3099cb8a63d21f9711e216c`  
		Last Modified: Thu, 16 Jan 2020 03:01:34 GMT  
		Size: 45.1 MB (45109030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e431e261a8407ba2e86454e21cf72a92b3f611f4e24ef0c876653aae12bf076`  
		Last Modified: Thu, 16 Jan 2020 03:02:19 GMT  
		Size: 145.2 MB (145205732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6e94786a7cc6e96c47995058255afc331cf8f6844411ab9629321d5e7616b5e1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.1 MB (219116571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3238d67e2a36c2770c4a599feb46dd85776a46c0b8da8226599153dcfd637c3d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 00:45:57 GMT
ADD file:8dc624cab286db0b39b659270affdb4f0c5c736f7ec355bc43060e36bd43a336 in / 
# Thu, 16 Jan 2020 00:45:58 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 00:45:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 00:45:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 00:45:59 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 01:31:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 01:31:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Jan 2020 01:31:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 01:32:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a8ee0c46f8e3249703df9b4ab84e86af58fa419bdcee72f85d431e2bf11f1049`  
		Last Modified: Thu, 16 Jan 2020 00:47:02 GMT  
		Size: 42.8 MB (42768510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c8d26a93c7ec74ab940513230781ae8f4b5cb2aadcbab0754f0b610e405950`  
		Last Modified: Thu, 16 Jan 2020 00:46:57 GMT  
		Size: 466.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eddcc7e74f0c3101237ce5c777afbfdddec1941fa42cd0d42ab5ffec6eb70ef`  
		Last Modified: Thu, 16 Jan 2020 00:46:57 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0ad0205b1d8e3ea4a5626a6871714211c5c9111bf16afda2369ee02c57cc20`  
		Last Modified: Thu, 16 Jan 2020 00:46:56 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e854883d3dc6ad434b7349eb300f5d801e9752ea846247379c3e37503489a824`  
		Last Modified: Thu, 16 Jan 2020 01:35:16 GMT  
		Size: 7.1 MB (7061347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22387427565fa150140abe6c85ee1829b3adfa8cd05e40c75e57fda5e69c2c03`  
		Last Modified: Thu, 16 Jan 2020 01:35:28 GMT  
		Size: 42.6 MB (42643126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355b3dd550a59a24fb61782051842db39540561a5e262c3d18caadf3389dab84`  
		Last Modified: Thu, 16 Jan 2020 01:35:48 GMT  
		Size: 126.6 MB (126642105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
