## `hylang:0-pypy3.10-bullseye`

```console
$ docker pull hylang@sha256:d656ee6545b4efa7f4c5d84cfb6013da32456a5a94c30a0735ff8e73a62e396c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:0-pypy3.10-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:fae3df71e337ece5059ab55e94a01bb8e5554233384c0e4493e03510970075b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72670356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfcfe28b2adf16d674632c0dc41e1e110aa48c063b94cef8768d6e4306c30b2`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 24 Apr 2024 04:14:48 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux64.tar.bz2'; 			sha256='404e6180d6caf9258eaab0c02c72018e9aa8eb03ab9094a0ff17ee5e3b265ac1'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-aarch64.tar.bz2'; 			sha256='fc720999bc5050e1d3706b3b6445e695cf42bfc71ebc7c88ed6bb88828b1d385'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux32.tar.bz2'; 			sha256='0df48aa780159e879ac89a805d143e4a6cd1b842f98046f5a3f865814bfaa2a4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-s390x.tar.bz2'; 			sha256='af97efe498a209ba18c7bc7d084164a9907fb3736588b6864955177e19d5216a'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["pypy3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5fa142287b5e2ea1cb3fdcef8dd067eff6342e9a900fe73f28b64968bf7cbc`  
		Last Modified: Tue, 02 Jul 2024 03:24:10 GMT  
		Size: 1.1 MB (1066633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedb707413502406462031e08f4a0f2d2592a5fc306016d38a1180194ee8086d`  
		Last Modified: Tue, 02 Jul 2024 03:24:10 GMT  
		Size: 30.5 MB (30475138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cab1f282c07e83465cb94a73aae106897dfc53147d3c1188632d352da481ec`  
		Last Modified: Tue, 02 Jul 2024 03:24:10 GMT  
		Size: 3.3 MB (3300894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63111520af010ba82467c649d927c01af650d995075d64a9d5b7dcc3b593021c`  
		Last Modified: Tue, 02 Jul 2024 04:13:52 GMT  
		Size: 6.4 MB (6405407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:7c508835ef92e861689d5bd157e3b7ea7cff22bec6a062863d962cc13f2105ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2674363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89131a51f11ec32055eb571987db36cdbb43481a0d6c6df4826888f3b7dd55af`

```dockerfile
```

-	Layers:
	-	`sha256:e8eb339e537f86c33b342c0ff7d3b047f3c0797ebdcda6d3faed4495c8f28ee3`  
		Last Modified: Tue, 02 Jul 2024 04:13:52 GMT  
		Size: 2.7 MB (2665039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33769ad0807e9eccff38df2ccc4438fb127feb13843724eb0008794d8181f6e3`  
		Last Modified: Tue, 02 Jul 2024 04:13:52 GMT  
		Size: 9.3 KB (9324 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy3.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:9515b2fb515408dca60c9a4f26a43ca040182de2f8b5e29a1a237c1915400cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69617758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a6b7347a26d3016bffea13782e33927709ccab9da052726b44e5afcbcc3b10`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 24 Apr 2024 04:14:48 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux64.tar.bz2'; 			sha256='404e6180d6caf9258eaab0c02c72018e9aa8eb03ab9094a0ff17ee5e3b265ac1'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-aarch64.tar.bz2'; 			sha256='fc720999bc5050e1d3706b3b6445e695cf42bfc71ebc7c88ed6bb88828b1d385'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux32.tar.bz2'; 			sha256='0df48aa780159e879ac89a805d143e4a6cd1b842f98046f5a3f865814bfaa2a4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-s390x.tar.bz2'; 			sha256='af97efe498a209ba18c7bc7d084164a9907fb3736588b6864955177e19d5216a'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["pypy3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebd2bd797f61d8a588af0e5d37443f731d568f431e81c8e6108cfeb31b15b4c`  
		Last Modified: Tue, 02 Jul 2024 19:46:43 GMT  
		Size: 1.1 MB (1053908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f45c3a8ec08e0260fdac7aa42155a35ad062619611aa1760e2aa93acddb4271`  
		Last Modified: Tue, 02 Jul 2024 19:46:44 GMT  
		Size: 28.8 MB (28788058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733bbebcb6ec3e1352a3c8795000245b7fdc48ced94862cd4a0718efca5a9900`  
		Last Modified: Tue, 02 Jul 2024 19:46:43 GMT  
		Size: 3.3 MB (3300549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d93b454d61dcc6273c8cdb4eb240de67a25b86049a5e5365371c1bf0d3ce94`  
		Last Modified: Wed, 03 Jul 2024 08:19:21 GMT  
		Size: 6.4 MB (6405628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:35106ee60ed2b8fa16c2f6298a5da5dc06a6edc8db5042dbe7df94bdb28d624e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2675108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1beb85ebe8239b90776ee8968b1720e0c62daf33638be4c97241c48e472fd4d3`

```dockerfile
```

-	Layers:
	-	`sha256:ad31d1b861dc5863f31dfe75c1925a89dc0310de65498e0b546045168f72d4ea`  
		Last Modified: Wed, 03 Jul 2024 08:19:20 GMT  
		Size: 2.7 MB (2665339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ae46b5074823d9730aab93174ea1b4c9a3fca63c74c66cff7ca64e133129c25`  
		Last Modified: Wed, 03 Jul 2024 08:19:20 GMT  
		Size: 9.8 KB (9769 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy3.10-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:97b7d93962128703aec726ea9eeff62a559118d558968843bf804d1dbfb93278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70000966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebc5abccb0d12fde37eb0b218e190d60ac59d39c6ac176f829a0d757de7622d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 24 Apr 2024 04:14:48 GMT
ADD file:82c5579b81dad9a5dff7724fd8e74d225f919e378995a95c9a0a9c17ca55a77a in / 
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux64.tar.bz2'; 			sha256='404e6180d6caf9258eaab0c02c72018e9aa8eb03ab9094a0ff17ee5e3b265ac1'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-aarch64.tar.bz2'; 			sha256='fc720999bc5050e1d3706b3b6445e695cf42bfc71ebc7c88ed6bb88828b1d385'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux32.tar.bz2'; 			sha256='0df48aa780159e879ac89a805d143e4a6cd1b842f98046f5a3f865814bfaa2a4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-s390x.tar.bz2'; 			sha256='af97efe498a209ba18c7bc7d084164a9907fb3736588b6864955177e19d5216a'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["pypy3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1084208571fd0651d255a493f4e05ba8b2b837b52064c5f2f317a2d979e679bc`  
		Last Modified: Tue, 02 Jul 2024 00:43:26 GMT  
		Size: 32.4 MB (32408452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cdc3a8d87b6405d2eeb15dc164ac9712bc28237a6ec806a2dde8c0ce905b87`  
		Last Modified: Tue, 02 Jul 2024 03:24:24 GMT  
		Size: 1.1 MB (1079147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceecb0530282bc5fc3659685ee29c168d86dd73ed79fbc87718b16517b77b5dc`  
		Last Modified: Tue, 02 Jul 2024 03:24:25 GMT  
		Size: 26.8 MB (26807198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc4f4c9106860b0ecbd937f04eafe6c692aa514425b06a7031bfad143ad4e34`  
		Last Modified: Tue, 02 Jul 2024 03:24:24 GMT  
		Size: 3.3 MB (3300514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8657c69f80c0b2595a9f04fda7d65f97cf0357369638975020987386d08336a8`  
		Last Modified: Tue, 02 Jul 2024 04:13:53 GMT  
		Size: 6.4 MB (6405655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:acc6eadbcdf4c4dbf557361d2dc791092c9d2bd876a3d30b324a39eb20fe169f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3af5bd4f43c0a5b6d3050cd34be667139b8026655ae080da7a17962010a3096`

```dockerfile
```

-	Layers:
	-	`sha256:de9e6b6f6bac6b96aaaed7a3cff3afa6b048efd3b94d336763a94a1fb0612c5a`  
		Last Modified: Tue, 02 Jul 2024 04:13:52 GMT  
		Size: 2.7 MB (2662144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b81be43ed7799d7602f1fb8933a50529616f81413bde2b34a82db1d1ad449059`  
		Last Modified: Tue, 02 Jul 2024 04:13:52 GMT  
		Size: 9.3 KB (9272 bytes)  
		MIME: application/vnd.in-toto+json
