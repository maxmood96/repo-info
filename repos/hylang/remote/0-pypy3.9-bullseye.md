## `hylang:0-pypy3.9-bullseye`

```console
$ docker pull hylang@sha256:df196f75e89d3ab7d160dfc374250ce0b79366109aacbdc1b03e0e4039045525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:0-pypy3.9-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:119608439774a7ab7eb2723d2771744100c67b844ba2b7ce5c6a018d1c5862de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75844862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3e122dff94964678cb5474b74741123ca80185e48a0eccebf9899abe1423df`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 12:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:26:04 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 12:26:04 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 12:26:04 GMT
ENV PYPY_VERSION=7.3.10
# Wed, 21 Dec 2022 12:26:35 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-linux64.tar.bz2'; 			sha256='95cf99406179460d63ddbfe1ec870f889d05f7767ce81cef14b88a3a9e127266'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-aarch64.tar.bz2'; 			sha256='657a04fd9a5a992a2f116a9e7e9132ea0c578721f59139c9fb2083775f71e514'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-linux32.tar.bz2'; 			sha256='b6db59613b9a1c0c1ab87bc103f52ee95193423882dc8a848b68850b8ba59cc5'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-s390x.tar.bz2'; 			sha256='ca6525a540cf0c682d1592ae35d3fbc97559a97260e4b789255cc76dde7a14f0'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 21 Dec 2022 12:26:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 21 Dec 2022 12:26:36 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 21 Dec 2022 12:26:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 21 Dec 2022 12:26:48 GMT
CMD ["pypy3"]
# Wed, 21 Dec 2022 15:38:28 GMT
ENV HY_VERSION=0.25.0
# Wed, 21 Dec 2022 15:38:28 GMT
ENV HYRULE_VERSION=0.2.1
# Wed, 21 Dec 2022 15:38:58 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 21 Dec 2022 15:38:58 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129a64cf99a2262d6ead5a9178302b5c4a2f7d55cef3b98130aac66b0493f855`  
		Last Modified: Wed, 21 Dec 2022 12:35:10 GMT  
		Size: 1.1 MB (1066565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd407560542a4dff39a3ce4ade259b3adbed2ba07d71daba0f31bede318a7a4`  
		Last Modified: Wed, 21 Dec 2022 12:35:16 GMT  
		Size: 36.2 MB (36163472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfcb57b9d26c924a5d5ba2e3188b3850993938767d0a136979fb9ef0d1b19f9`  
		Last Modified: Wed, 21 Dec 2022 12:35:11 GMT  
		Size: 3.2 MB (3170571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e78764ecfcdbc6e90eef782a15de2805d721011a72aed498db9a9e9eb2aafd`  
		Last Modified: Wed, 21 Dec 2022 15:46:26 GMT  
		Size: 4.0 MB (4047311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy3.9-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:8bbd3dbd208318db99f0826185235714180dfe68625268785781cf2b8142b175
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72005577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfdfcd4c2a3a75f601800ca8de171673c019ce4648f3a5e11700fb3665dfa5b2`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 06:41:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 06:41:39 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 06:41:39 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Dec 2022 02:13:26 GMT
ENV PYPY_VERSION=7.3.10
# Wed, 07 Dec 2022 02:13:49 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-linux64.tar.bz2'; 			sha256='95cf99406179460d63ddbfe1ec870f889d05f7767ce81cef14b88a3a9e127266'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-aarch64.tar.bz2'; 			sha256='657a04fd9a5a992a2f116a9e7e9132ea0c578721f59139c9fb2083775f71e514'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-linux32.tar.bz2'; 			sha256='b6db59613b9a1c0c1ab87bc103f52ee95193423882dc8a848b68850b8ba59cc5'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-s390x.tar.bz2'; 			sha256='ca6525a540cf0c682d1592ae35d3fbc97559a97260e4b789255cc76dde7a14f0'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 07 Dec 2022 02:13:50 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 07 Dec 2022 02:13:50 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 07 Dec 2022 02:14:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 07 Dec 2022 02:14:01 GMT
CMD ["pypy3"]
# Wed, 07 Dec 2022 03:11:15 GMT
ENV HY_VERSION=0.25.0
# Wed, 07 Dec 2022 03:11:15 GMT
ENV HYRULE_VERSION=0.2.1
# Wed, 07 Dec 2022 03:11:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 07 Dec 2022 03:11:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10899d04f0abe7df84b5d209e23478deeda253b78e63b28797c2c513ee13c8b0`  
		Last Modified: Tue, 06 Dec 2022 06:52:42 GMT  
		Size: 1.1 MB (1055302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f847314086e78be41b0e3266015df22533d5076891c966d47ec7d6d19cbce44`  
		Last Modified: Wed, 07 Dec 2022 02:21:37 GMT  
		Size: 33.7 MB (33671979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d306161193370feaebdb45211becd451eda991cf5bf60dd165302f51c5ac1dd`  
		Last Modified: Wed, 07 Dec 2022 02:21:32 GMT  
		Size: 3.2 MB (3170981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9270f1f4d3348c40d009ef6070e045919418af6e7165d8c474d71be0750252a7`  
		Last Modified: Wed, 07 Dec 2022 03:17:17 GMT  
		Size: 4.0 MB (4046995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy3.9-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:06233cb74ed072fbc3186b40f335c9fe503e11bce41014d6d5d0d57d91ec2bd0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74662751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a3822f0df7bc9b44d581dc4c05b693fb696089ff9d6812f1671ede540a6c2c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:22 GMT
ADD file:5f553fdf893bb3198d173c48f4531e9bfdbab61798c1aa8217fd80e9d686d7ae in / 
# Wed, 21 Dec 2022 01:39:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 06:22:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 06:22:48 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 06:22:49 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 06:22:50 GMT
ENV PYPY_VERSION=7.3.10
# Wed, 21 Dec 2022 06:23:25 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-linux64.tar.bz2'; 			sha256='95cf99406179460d63ddbfe1ec870f889d05f7767ce81cef14b88a3a9e127266'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-aarch64.tar.bz2'; 			sha256='657a04fd9a5a992a2f116a9e7e9132ea0c578721f59139c9fb2083775f71e514'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-linux32.tar.bz2'; 			sha256='b6db59613b9a1c0c1ab87bc103f52ee95193423882dc8a848b68850b8ba59cc5'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-s390x.tar.bz2'; 			sha256='ca6525a540cf0c682d1592ae35d3fbc97559a97260e4b789255cc76dde7a14f0'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 21 Dec 2022 06:23:26 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 21 Dec 2022 06:23:26 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 21 Dec 2022 06:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 21 Dec 2022 06:23:43 GMT
CMD ["pypy3"]
# Wed, 21 Dec 2022 17:52:12 GMT
ENV HY_VERSION=0.25.0
# Wed, 21 Dec 2022 17:52:12 GMT
ENV HYRULE_VERSION=0.2.1
# Wed, 21 Dec 2022 17:52:52 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 21 Dec 2022 17:52:52 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3228cb514e81f042720b7fd118ace0f279d1a4bc422b7e24189514a574dfa546`  
		Last Modified: Wed, 21 Dec 2022 01:44:46 GMT  
		Size: 32.4 MB (32375745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941f456ea08ae7e340ba6a224752f1ded93f0629c538040f1eb604dd321c990a`  
		Last Modified: Wed, 21 Dec 2022 06:32:27 GMT  
		Size: 1.1 MB (1078741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54aca24bcef9308c4fef589eb0acb22898961271a587c282c9c68f1cbaa77dc7`  
		Last Modified: Wed, 21 Dec 2022 06:32:32 GMT  
		Size: 34.2 MB (34209680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564193364bc026ae42d8f7b92ab445b5ed8295cbed6bdd3a676eb8cff7f3d3c0`  
		Last Modified: Wed, 21 Dec 2022 06:32:28 GMT  
		Size: 3.0 MB (2951363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416b53ee90da7a80733ba0901f42d1e3ba62ac4dff9a4a5b988343fb9f64f2eb`  
		Last Modified: Wed, 21 Dec 2022 18:04:49 GMT  
		Size: 4.0 MB (4047222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
