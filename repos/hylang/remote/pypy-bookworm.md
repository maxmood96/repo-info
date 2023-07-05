## `hylang:pypy-bookworm`

```console
$ docker pull hylang@sha256:1d421971abf6ed3e371db66de0818c4b2717d3ad428cad1e28e15a91b278b105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:pypy-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:ea9378c1311f57a0d3ad7915ecd718a9230556259440f8a31343f1d12eaf6630
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78698459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bdf6c9819c547a478a20d1542e2ba299ff2daf3747e3f32743e5fcc403fd73`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Jul 2023 01:19:58 GMT
ADD file:bd80a4461150784e5f2f5a1faa720cc347ad3e30ee0969adbfad574c316f5aef in / 
# Tue, 04 Jul 2023 01:19:58 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:24:42 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 04:24:42 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 04:24:42 GMT
ENV PYPY_VERSION=7.3.12
# Tue, 04 Jul 2023 04:25:27 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.12-linux64.tar.bz2'; 			sha256='6c577993160b6f5ee8cab73cd1a807affcefafe2f7441c87bd926c10505e8731'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.12-aarch64.tar.bz2'; 			sha256='26208b5a134d9860a08f74cce60960005758e82dc5f0e3566a48ed863a1f16a1'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.12-linux32.tar.bz2'; 			sha256='811667825ae58ada4b7c3d8bc1b5055b9f9d6a377e51aedfbe0727966603f60e'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.12-s390x.tar.bz2'; 			sha256='043c13a585479428b463ab69575a088db74aadc16798d6e677d97f563585fee3'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 04 Jul 2023 04:25:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 04 Jul 2023 04:25:27 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 04 Jul 2023 04:25:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 04 Jul 2023 04:25:39 GMT
CMD ["pypy3"]
# Wed, 05 Jul 2023 03:37:35 GMT
ENV HY_VERSION=0.26.0
# Wed, 05 Jul 2023 03:37:35 GMT
ENV HYRULE_VERSION=0.3.0
# Wed, 05 Jul 2023 03:38:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 05 Jul 2023 03:38:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:faef57eae888cbe4a5613eca6741b5e48d768b83f6088858aee9a5a2834f8151`  
		Last Modified: Tue, 04 Jul 2023 01:25:03 GMT  
		Size: 29.1 MB (29124829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da7d9e896dfbab632dab33a1318dac0e952378489188ab7d9c937a03234b34a`  
		Last Modified: Tue, 04 Jul 2023 04:33:18 GMT  
		Size: 3.5 MB (3485409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbc9319f590885fe673d88aa000905f05b320fad01f3eab8699fdc624266b65`  
		Last Modified: Tue, 04 Jul 2023 04:33:24 GMT  
		Size: 36.2 MB (36207082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb57f04be5bcf00cdf56b353a09507a8607aaef28b918a5a788ed98f53d621f`  
		Last Modified: Tue, 04 Jul 2023 04:33:18 GMT  
		Size: 3.5 MB (3511291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7c1c6cb0656510d20d8d652e0a5732f9e0d2e14e0bd608d51a48ee0ca0273b`  
		Last Modified: Wed, 05 Jul 2023 03:43:59 GMT  
		Size: 6.4 MB (6369848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:be545bfce5003e9a93960ba5fe9a558cd0525315f766618fd3e95ada4581f9d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75854999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b892751ade7fe24138b84b6944e6d8195d44979a8d75a7a9f80d2c24636c569`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:35 GMT
ADD file:71fd66666294148382f2e6a09ae5e277d4c4e9c74402ab64b693a79387b67a09 in / 
# Tue, 04 Jul 2023 01:57:36 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:22:34 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 04:22:34 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 04:22:34 GMT
ENV PYPY_VERSION=7.3.12
# Tue, 04 Jul 2023 04:23:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.12-linux64.tar.bz2'; 			sha256='6c577993160b6f5ee8cab73cd1a807affcefafe2f7441c87bd926c10505e8731'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.12-aarch64.tar.bz2'; 			sha256='26208b5a134d9860a08f74cce60960005758e82dc5f0e3566a48ed863a1f16a1'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.12-linux32.tar.bz2'; 			sha256='811667825ae58ada4b7c3d8bc1b5055b9f9d6a377e51aedfbe0727966603f60e'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.12-s390x.tar.bz2'; 			sha256='043c13a585479428b463ab69575a088db74aadc16798d6e677d97f563585fee3'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 04 Jul 2023 04:23:05 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 04 Jul 2023 04:23:05 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 04 Jul 2023 04:23:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 04 Jul 2023 04:23:17 GMT
CMD ["pypy3"]
# Tue, 04 Jul 2023 16:44:01 GMT
ENV HY_VERSION=0.26.0
# Tue, 04 Jul 2023 16:44:01 GMT
ENV HYRULE_VERSION=0.3.0
# Tue, 04 Jul 2023 16:44:33 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 04 Jul 2023 16:44:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3ae0c06b4d3aa97d7e0829233dd36cea1666b87074e55fea6bd1ecae066693c7`  
		Last Modified: Tue, 04 Jul 2023 02:01:20 GMT  
		Size: 29.2 MB (29152458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28388fd881163b88ba86783eea094b265057b0690dd16ebdb5e1df7862a38b6d`  
		Last Modified: Tue, 04 Jul 2023 04:27:46 GMT  
		Size: 3.3 MB (3311792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be6a62702af5dd064d71d2fdf990e935dbd547f49ac6c9b9366ad710aaaa332`  
		Last Modified: Tue, 04 Jul 2023 04:27:50 GMT  
		Size: 33.5 MB (33509545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c194b8053dfe34688ff19d4071859efc5622e85c728d80a7aab68b908d6ecf`  
		Last Modified: Tue, 04 Jul 2023 04:27:46 GMT  
		Size: 3.5 MB (3511247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11289bb8352dc342835e7c9f41db3912e8d77ca324ed1ae8bbe59453fedded78`  
		Last Modified: Tue, 04 Jul 2023 16:50:29 GMT  
		Size: 6.4 MB (6369957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:202de4e38823089dcf8839bcfcce0f6637214d19848ae77ae7f9354a067c0a90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75645935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ccff810b75398635b7e0fcd88e1bdec89694657954c61a58632ad6aa6c2ea82`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 12 Jun 2023 23:39:20 GMT
ADD file:c7ecc5e2bed99e2cbca26f9f4247cd9bc399749556f4084e9357a9b00bb80530 in / 
# Mon, 12 Jun 2023 23:39:20 GMT
CMD ["bash"]
# Thu, 15 Jun 2023 01:30:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 15 Jun 2023 01:30:34 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jun 2023 01:30:34 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Jun 2023 00:56:10 GMT
ENV PYPY_VERSION=7.3.12
# Sat, 24 Jun 2023 00:55:07 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.12-linux64.tar.bz2'; 			sha256='6c577993160b6f5ee8cab73cd1a807affcefafe2f7441c87bd926c10505e8731'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.12-aarch64.tar.bz2'; 			sha256='26208b5a134d9860a08f74cce60960005758e82dc5f0e3566a48ed863a1f16a1'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.12-linux32.tar.bz2'; 			sha256='811667825ae58ada4b7c3d8bc1b5055b9f9d6a377e51aedfbe0727966603f60e'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.12-s390x.tar.bz2'; 			sha256='043c13a585479428b463ab69575a088db74aadc16798d6e677d97f563585fee3'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Sat, 24 Jun 2023 00:55:07 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Sat, 24 Jun 2023 00:55:08 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Sat, 24 Jun 2023 00:55:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 24 Jun 2023 00:55:22 GMT
CMD ["pypy3"]
# Tue, 27 Jun 2023 23:40:58 GMT
ENV HY_VERSION=0.26.0
# Tue, 27 Jun 2023 23:40:58 GMT
ENV HYRULE_VERSION=0.3.0
# Tue, 27 Jun 2023 23:41:36 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 27 Jun 2023 23:41:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:82a41d17956dd7c8ebb39c9ce936fd26841bdbec98d0a185e3db8154b352edff`  
		Last Modified: Mon, 12 Jun 2023 23:46:21 GMT  
		Size: 30.1 MB (30140741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb43f3f858bc03cbd60af609f87d15e19c451bfa296f791a956bee0ad15c25f`  
		Last Modified: Thu, 15 Jun 2023 01:39:58 GMT  
		Size: 3.5 MB (3492627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d492efc85bfc5afde75afd1d2bd3bd3b1ad0f9f5ac98c3bd7d6ca4120190e0cb`  
		Last Modified: Sat, 24 Jun 2023 00:58:54 GMT  
		Size: 32.1 MB (32131619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebfe6152b0d9981e53b3fc3a83de2ad9f458c06863be52f13fc58e976394c3e`  
		Last Modified: Sat, 24 Jun 2023 00:58:47 GMT  
		Size: 3.5 MB (3510956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c410ed95c56e2eeaa458dd30bff06323e94a05f218c4a9c4ae4c75ec410d962`  
		Last Modified: Tue, 27 Jun 2023 23:44:33 GMT  
		Size: 6.4 MB (6369992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
