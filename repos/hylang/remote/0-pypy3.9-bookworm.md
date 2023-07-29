## `hylang:0-pypy3.9-bookworm`

```console
$ docker pull hylang@sha256:e66da96fcebf49af2ee26e1f79d44173111acc7e4e6092fc54aab2fc1989d0e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:0-pypy3.9-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:4b86434b238b05b091e5739149627bd75852158da006caeef1be8b738970956d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76216676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92d1e835d9c7c185429395f1bfb74f82da21293ca2c0f0f0d0b40eace1ffa94`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:44 GMT
ADD file:209589a8bdb5a3788ee42ecdbccbbb561835dab96b0d8286bb5a2229d2f41be7 in / 
# Thu, 27 Jul 2023 23:24:45 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:02:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 14:02:06 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 14:02:06 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 14:02:06 GMT
ENV PYPY_VERSION=7.3.12
# Fri, 28 Jul 2023 14:05:43 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.12-linux64.tar.bz2'; 			sha256='84c89b966fab2b58f451a482ee30ca7fec3350435bd0b9614615c61dc6da2390'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.12-aarch64.tar.bz2'; 			sha256='e9327fb9edaf2ad91935d5b8563ec5ff24193bddb175c1acaaf772c025af1824'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.12-linux32.tar.bz2'; 			sha256='aa04370d38f451683ccc817d76c2b3e0f471dbb879e0bd618d9affbdc9cd37a4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.12-s390x.tar.bz2'; 			sha256='20d84658a6899bdd2ca35b00ead33a2f56cff2c40dce1af630466d27952f6d4f'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Fri, 28 Jul 2023 14:05:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 28 Jul 2023 14:05:43 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 28 Jul 2023 14:05:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 28 Jul 2023 14:05:55 GMT
CMD ["pypy3"]
# Sat, 29 Jul 2023 00:17:57 GMT
ENV HY_VERSION=0.27.0
# Sat, 29 Jul 2023 00:17:58 GMT
ENV HYRULE_VERSION=0.4.0
# Sat, 29 Jul 2023 00:18:25 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Sat, 29 Jul 2023 00:18:25 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:648e0aadf75ac2ef63c5390adc6dc14fde37a5ad88c2870ea604df0a9c0eb4e5`  
		Last Modified: Thu, 27 Jul 2023 23:29:26 GMT  
		Size: 29.1 MB (29124532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd75e07d7aa79c2aa60b0ecf2fb5ad50381780db291be1709b8ca0f0ad294b2`  
		Last Modified: Fri, 28 Jul 2023 14:10:34 GMT  
		Size: 3.5 MB (3485416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033bb6e5493b2e7c7d6496660618052ababe78e9d06f8960dcd343a2a000f48e`  
		Last Modified: Fri, 28 Jul 2023 14:12:39 GMT  
		Size: 36.6 MB (36566805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6811ebda50b0309064ce6fd2176a5925d8d2d84a23e21efe9d71046121a546d`  
		Last Modified: Fri, 28 Jul 2023 14:12:34 GMT  
		Size: 3.1 MB (3123727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3b2a0ec33e63c6d49bed5a9e683ff2cbadf8302c61b8f9e322d23be095f983`  
		Last Modified: Sat, 29 Jul 2023 00:24:19 GMT  
		Size: 3.9 MB (3916196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy3.9-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:9d587e50a57d5beb7eef32004ec293ce6c83daac2b42e1106501a07f0acd0e7d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73375023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf0d527bde95795aeda0fbc252bd488b8976c266d6bae06cf15e1531203d9d5`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:00 GMT
ADD file:1de2ba0dc88aa343332814e19adc6b850d08e62c31589fe902b8eb2cb465934e in / 
# Thu, 27 Jul 2023 23:43:00 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 06:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 06:15:19 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 06:15:19 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 06:15:19 GMT
ENV PYPY_VERSION=7.3.12
# Fri, 28 Jul 2023 06:18:24 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.12-linux64.tar.bz2'; 			sha256='84c89b966fab2b58f451a482ee30ca7fec3350435bd0b9614615c61dc6da2390'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.12-aarch64.tar.bz2'; 			sha256='e9327fb9edaf2ad91935d5b8563ec5ff24193bddb175c1acaaf772c025af1824'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.12-linux32.tar.bz2'; 			sha256='aa04370d38f451683ccc817d76c2b3e0f471dbb879e0bd618d9affbdc9cd37a4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.12-s390x.tar.bz2'; 			sha256='20d84658a6899bdd2ca35b00ead33a2f56cff2c40dce1af630466d27952f6d4f'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Fri, 28 Jul 2023 06:18:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 28 Jul 2023 06:18:24 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 28 Jul 2023 06:18:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 28 Jul 2023 06:18:36 GMT
CMD ["pypy3"]
# Fri, 28 Jul 2023 19:55:35 GMT
ENV HY_VERSION=0.27.0
# Fri, 28 Jul 2023 19:55:35 GMT
ENV HYRULE_VERSION=0.4.0
# Fri, 28 Jul 2023 19:56:03 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Fri, 28 Jul 2023 19:56:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:90524f7dc01b4ce9b387992acc6cbdbcc2a9ee8c6addfd632429ca06ea18751e`  
		Last Modified: Thu, 27 Jul 2023 23:46:17 GMT  
		Size: 29.2 MB (29157226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95f2ea93c5dbab06e76ad2618a7011dfd95380229a8b1f9a182e5cd064c0765`  
		Last Modified: Fri, 28 Jul 2023 06:22:47 GMT  
		Size: 3.3 MB (3311881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3549e3440470ffddf2a079990248a0aabcfe73909aeaca37d41705a2106d5b5`  
		Last Modified: Fri, 28 Jul 2023 06:24:40 GMT  
		Size: 33.9 MB (33866408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c303a43d8f7c8b0d2cd323ae30512b8ce0554eb671952af5b9ea2fc73a9239`  
		Last Modified: Fri, 28 Jul 2023 06:24:36 GMT  
		Size: 3.1 MB (3123689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb19b280eb4494885e93720bab095af75c48bc70a6af0dbc4c7a9bfb2be82623`  
		Last Modified: Fri, 28 Jul 2023 20:01:54 GMT  
		Size: 3.9 MB (3915819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy3.9-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:45f55c7dcc84d883a7428812f3e26ec52f149e94ef728586595448107eb64e86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73197680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d9d138e403a3b5e2b74e0e461aa2797218c1dfbd100f8600d023ce430ee074`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 27 Jul 2023 23:38:56 GMT
ADD file:3d6e6f3e900e480a7e060fcaf57313c0f954bf906967a7fa0317567c387cf5aa in / 
# Thu, 27 Jul 2023 23:38:57 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 12:53:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 12:53:26 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 12:53:26 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 12:53:26 GMT
ENV PYPY_VERSION=7.3.12
# Fri, 28 Jul 2023 12:57:10 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.12-linux64.tar.bz2'; 			sha256='84c89b966fab2b58f451a482ee30ca7fec3350435bd0b9614615c61dc6da2390'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.12-aarch64.tar.bz2'; 			sha256='e9327fb9edaf2ad91935d5b8563ec5ff24193bddb175c1acaaf772c025af1824'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.12-linux32.tar.bz2'; 			sha256='aa04370d38f451683ccc817d76c2b3e0f471dbb879e0bd618d9affbdc9cd37a4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.12-s390x.tar.bz2'; 			sha256='20d84658a6899bdd2ca35b00ead33a2f56cff2c40dce1af630466d27952f6d4f'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Fri, 28 Jul 2023 12:57:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 28 Jul 2023 12:57:10 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 28 Jul 2023 12:57:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 28 Jul 2023 12:57:24 GMT
CMD ["pypy3"]
# Sat, 29 Jul 2023 03:56:20 GMT
ENV HY_VERSION=0.27.0
# Sat, 29 Jul 2023 03:56:20 GMT
ENV HYRULE_VERSION=0.4.0
# Sat, 29 Jul 2023 03:56:52 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Sat, 29 Jul 2023 03:56:52 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3a8b0c4b1a83609d978d576be6174f951ff27084d7c9aef91892b60b223a5104`  
		Last Modified: Thu, 27 Jul 2023 23:43:26 GMT  
		Size: 30.1 MB (30141788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a92dcaa2da9649f9172135441ac99186c7426c5a33dad0f54b5b919c7d4fef`  
		Last Modified: Fri, 28 Jul 2023 13:02:15 GMT  
		Size: 3.5 MB (3492702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e4dcb25bc0ed8815ac21f79c8fa959fc3f7cc0a45f9f99dfaf7bb745dccb7e`  
		Last Modified: Fri, 28 Jul 2023 13:04:27 GMT  
		Size: 32.5 MB (32523619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f320f75dc29dad44d3f476d2cbe691d0bac7533f8510ec7bce177cb27e0f23`  
		Last Modified: Fri, 28 Jul 2023 13:04:20 GMT  
		Size: 3.1 MB (3123505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b37671b1321f85aa2f8687534180d0ad261da9ebdf7119b4702c1fcf37def29`  
		Last Modified: Sat, 29 Jul 2023 04:03:02 GMT  
		Size: 3.9 MB (3916066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
