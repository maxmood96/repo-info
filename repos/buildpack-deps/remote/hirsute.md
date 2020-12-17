## `buildpack-deps:hirsute`

```console
$ docker pull buildpack-deps@sha256:09d86155462ed12d3af0b3c7f99773d46a64f53bc428f27888e04fb3ad349d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v7

### `buildpack-deps:hirsute` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9cc483de72d535e26c15d81ab015c5494f7f46356c5aa1bb86bed2d45d50521a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.2 MB (358153168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dccd05e18a5165262cebc55ad87dd5928dc48831c3203fb398d2d82a833a253`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 23:00:24 GMT
ADD file:efa60bd7da49bad0a724434362f77d98c9f3c786170c7fef64ecb57aa808b18e in / 
# Wed, 25 Nov 2020 23:00:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 23:00:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 23:00:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 23:00:31 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 08:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:41:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 08:42:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:44:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf5d8cf40e57262478b56493eaf1bb9d9a8ecde1d37cfc10e81f73798a0a5b7a`  
		Last Modified: Mon, 23 Nov 2020 22:54:17 GMT  
		Size: 26.3 MB (26336795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d0e651346be2ec39fb01f211210fa42a2ec5212300b3a6d73f450dd1dc709d`  
		Last Modified: Wed, 25 Nov 2020 23:02:22 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe721ee3adfabbef45101e3cdd00ff12aa4ea18319502279b4da2389a2c153f`  
		Last Modified: Wed, 25 Nov 2020 23:02:22 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6b39ed7adb6a7a6d999508a6ae30fe04c7a403accfe529f05acf9a5e742833`  
		Last Modified: Thu, 17 Dec 2020 09:01:48 GMT  
		Size: 4.8 MB (4849916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9e63643887e8142d918de418503ee33102967776ae4dcda5389138288430ec`  
		Last Modified: Thu, 17 Dec 2020 09:01:48 GMT  
		Size: 3.1 MB (3126212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eaf6ce3ed47b1a43b079ba4bed46a379c125af9ddec54251aaeeb847f941f2`  
		Last Modified: Thu, 17 Dec 2020 09:02:13 GMT  
		Size: 41.9 MB (41918985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbea81eaef45f66af40acab0fd811d034d6fb9d6a0f0151f6640a093d248038f`  
		Last Modified: Thu, 17 Dec 2020 09:03:42 GMT  
		Size: 281.9 MB (281920220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
