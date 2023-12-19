## `pypy:2-7-bookworm`

```console
$ docker pull pypy@sha256:3a7febc6b9a8136a1d36b945ae2a37047ae6cb7bb12a90bed3d9423a3ccb2767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `pypy:2-7-bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:108800a5a53407620ebab5a8ca8768011b83979a478e0b109b46fcbc94b90093
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.0 MB (385025269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496f4ed368acafc4ef2553a8566741edace6c26d14e94710525a0f6d8561963a`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:15 GMT
ADD file:7d8adf68670e8dc2af6b8603870ea610fc65ecbb08799f2ca6a3134f5d47d289 in / 
# Tue, 19 Dec 2023 01:20:16 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:32:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:32:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:33:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 15:54:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 15:54:05 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 15:54:05 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 15:54:05 GMT
ENV PYPY_VERSION=7.3.13
# Tue, 19 Dec 2023 16:00:19 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-linux64.tar.bz2'; 			sha256='e41ceb5dc6c4d3a9311ed5f88edfeedbf3e8abbd1ed3c4f2e151a90a5cf4e1d7'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-aarch64.tar.bz2'; 			sha256='f1e20f833cc86a097c1f1318069fc17d01c3988678c1438fe27ed567fcb5cfd0'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-linux32.tar.bz2'; 			sha256='b727d2e759a740f45bab1e333029d001c4384b52949bcbb4bd2ad7912eae8dad'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-s390x.tar.bz2'; 			sha256='fbb2f3d92831c02b094f17e9609b95a6202d4bdcddae437e380ab14388d4556e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 19 Dec 2023 16:00:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 19 Dec 2023 16:00:20 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 19 Dec 2023 16:00:26 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 19 Dec 2023 16:00:26 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:bc0734b949dcdcabe5bfdf0c8b9f44491e0fce04cb10c9c6e76282b9f6abdf01`  
		Last Modified: Tue, 19 Dec 2023 01:24:35 GMT  
		Size: 49.6 MB (49561579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5de22c0f5cd2ea2bb6c0524478db95bff5a294c99419ccd4a9d3ccc9873bad9`  
		Last Modified: Tue, 19 Dec 2023 04:41:08 GMT  
		Size: 24.0 MB (24046123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917ee5330e73737d6095a802333d311648959399ff2c067150890162e720f863`  
		Last Modified: Tue, 19 Dec 2023 04:41:27 GMT  
		Size: 64.1 MB (64131542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43bd898d5fbe0e1606380820047fd1e8b421722c9e69ac12757474305bd6702`  
		Last Modified: Tue, 19 Dec 2023 04:42:04 GMT  
		Size: 211.1 MB (211097790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893aae0ef9d051920825efdc3da272d3ba46b78d6849c0a8e02c4d7cb52bb5a1`  
		Last Modified: Tue, 19 Dec 2023 16:02:47 GMT  
		Size: 3.2 MB (3228058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd08ef2dccb2462401aacb84984e271dfad3353cf0c7e77e16c37d34ba5300dc`  
		Last Modified: Tue, 19 Dec 2023 16:06:28 GMT  
		Size: 31.1 MB (31063640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6bf2c41f4b47a97dc2df4637bf83bb6ff728aabad1308bcb0c8c0f17db9031b`  
		Last Modified: Tue, 19 Dec 2023 16:06:23 GMT  
		Size: 1.9 MB (1896537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-7-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:ea0cb4efdd7629ba1d62918d370f29df416e8401cc89adb56e3e51fa7496c3bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.8 MB (373842421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c32079aef1f5583b1809bffe6e7424fdc1d8b6541aebb7c0c5f5858dca2583`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:02 GMT
ADD file:412f80f75ed3e520f767e70b6b27fc81807f62fc5c6e5adf756507e33af9fa6b in / 
# Tue, 19 Dec 2023 01:41:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:34:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:34:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 16:10:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 16:10:37 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 16:10:37 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 16:10:37 GMT
ENV PYPY_VERSION=7.3.13
# Tue, 19 Dec 2023 16:13:00 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-linux64.tar.bz2'; 			sha256='e41ceb5dc6c4d3a9311ed5f88edfeedbf3e8abbd1ed3c4f2e151a90a5cf4e1d7'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-aarch64.tar.bz2'; 			sha256='f1e20f833cc86a097c1f1318069fc17d01c3988678c1438fe27ed567fcb5cfd0'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-linux32.tar.bz2'; 			sha256='b727d2e759a740f45bab1e333029d001c4384b52949bcbb4bd2ad7912eae8dad'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-s390x.tar.bz2'; 			sha256='fbb2f3d92831c02b094f17e9609b95a6202d4bdcddae437e380ab14388d4556e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 19 Dec 2023 16:13:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 19 Dec 2023 16:13:00 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 19 Dec 2023 16:13:05 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 19 Dec 2023 16:13:05 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:b66b4ecd3ecfb67b3b7a2a44b0199cbdfc94965c8bd3fefab75cd2e612799740`  
		Last Modified: Tue, 19 Dec 2023 01:44:14 GMT  
		Size: 49.6 MB (49592259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c641d36985b2db859fc64c43a6dbf7c25cdf73e5d16d107fab1d95a840bb4e1`  
		Last Modified: Tue, 19 Dec 2023 11:42:17 GMT  
		Size: 23.6 MB (23582271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd8544b6e15c7a4096b1f48a67fb5bed2efba509fca597f1c164b582ab01c02`  
		Last Modified: Tue, 19 Dec 2023 11:42:35 GMT  
		Size: 64.0 MB (63988289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae58c7c06d64a1a86430205c774637c7615d1365a575b256801bb23390ad5260`  
		Last Modified: Tue, 19 Dec 2023 11:43:05 GMT  
		Size: 202.5 MB (202484237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eca93a867101f77fbbe83739d7a1425ea04313150507cf116bc04765f36f1ef`  
		Last Modified: Tue, 19 Dec 2023 16:14:22 GMT  
		Size: 3.2 MB (3220625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd3fc095044d876752247546884178054ee4f505471a34ce29fa0ec51709e97`  
		Last Modified: Tue, 19 Dec 2023 16:16:05 GMT  
		Size: 29.1 MB (29078205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e6816fb3385f39b1bed5b017495601d0aa8d4cf1c273b4e167c306262436bc`  
		Last Modified: Tue, 19 Dec 2023 16:16:01 GMT  
		Size: 1.9 MB (1896535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-7-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:7d44958675e3fb0a5418d63fc0aabd4acdbcd1d4b8caa1452858c3119543cd49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.9 MB (383891163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9517dc5450a4be0de33b23f24dfa1a19bbcb4bbafe5a1272af753f3cfa3ceacb`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 21 Nov 2023 04:39:42 GMT
ADD file:abe2e7bdcd180971e7231cdda92141480a16075563efb8f61699f50e06bdb708 in / 
# Tue, 21 Nov 2023 04:39:42 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 15:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 15:23:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 15:24:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 15:43:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 15:43:57 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 15:43:57 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 15:43:57 GMT
ENV PYPY_VERSION=7.3.13
# Tue, 21 Nov 2023 15:52:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-linux64.tar.bz2'; 			sha256='e41ceb5dc6c4d3a9311ed5f88edfeedbf3e8abbd1ed3c4f2e151a90a5cf4e1d7'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-aarch64.tar.bz2'; 			sha256='f1e20f833cc86a097c1f1318069fc17d01c3988678c1438fe27ed567fcb5cfd0'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-linux32.tar.bz2'; 			sha256='b727d2e759a740f45bab1e333029d001c4384b52949bcbb4bd2ad7912eae8dad'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-s390x.tar.bz2'; 			sha256='fbb2f3d92831c02b094f17e9609b95a6202d4bdcddae437e380ab14388d4556e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 21 Nov 2023 15:52:03 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 21 Nov 2023 15:52:03 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 21 Nov 2023 15:52:10 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 21 Nov 2023 15:52:11 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:c7a059bd70ecf2a95d7693944fbc8baa8c198f05211b46ff1be263e6bad07b85`  
		Last Modified: Tue, 21 Nov 2023 04:44:08 GMT  
		Size: 50.6 MB (50600840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f4eeb47ebfe6b0e0c25efe7157749e45dfa129b162bb85f76f5635f327f8b4`  
		Last Modified: Tue, 21 Nov 2023 15:34:15 GMT  
		Size: 24.9 MB (24885542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3649ea58d07edfa2bbfc0951622d823a33155f6287c03863e17930504aa55b99`  
		Last Modified: Tue, 21 Nov 2023 15:34:46 GMT  
		Size: 66.0 MB (65984014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa271d77366b8effecedd447c479d25da2d21e9a8c10417a57907f63c3fde5bb`  
		Last Modified: Tue, 21 Nov 2023 15:35:36 GMT  
		Size: 210.0 MB (209992274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15caeaa608ad64034960e5bb6bc877840c8c5ded5b2af6138b5181a90059f3e9`  
		Last Modified: Tue, 21 Nov 2023 15:54:43 GMT  
		Size: 3.4 MB (3372759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceafe56316292d2499a6824f430c821b400bf17f208b589fa37fc072fecee324`  
		Last Modified: Tue, 21 Nov 2023 15:58:43 GMT  
		Size: 27.2 MB (27159157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f7a4f32382dcc28ce5d5c3992c4d2692354aa7e33feb8d5b85fb1a97641afd`  
		Last Modified: Tue, 21 Nov 2023 15:58:36 GMT  
		Size: 1.9 MB (1896577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
