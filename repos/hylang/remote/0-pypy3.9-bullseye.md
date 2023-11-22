## `hylang:0-pypy3.9-bullseye`

```console
$ docker pull hylang@sha256:e22c5e32b8cf10868b8567774b1a08dce7dbb4fd62acde083128a2a6704cfafd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:0-pypy3.9-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:d93e848fdaf21b6b63ea0c2ed8f9a68674b10fd076ae0d21918ddda1b6dd3d94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75495642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c062c822bf4db8e93f2600a58a3dfcbe0d7255880cadfc1a0aa51263914516`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 19:35:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:35:58 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 19:35:58 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:35:58 GMT
ENV PYPY_VERSION=7.3.13
# Tue, 21 Nov 2023 19:38:59 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.13-linux64.tar.bz2'; 			sha256='323b05a9f607e932cda1995cbe77a96e4ea35994631aa6d734c8035e8479b74e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.13-aarch64.tar.bz2'; 			sha256='317d7876c5825a086f854253648b967a432b993ce87695d2895d3ad6ed0d2716'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.13-linux32.tar.bz2'; 			sha256='ac695238b4a3635ac6b482e74e04e2ea78b31acca0decd5de601dfd2f4ebf35a'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.13-s390x.tar.bz2'; 			sha256='213c88f652a99c4dc4e8e00b4b5b58f381c7f7e9ea1a9b65801fc0eb1e50df0a'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 21 Nov 2023 19:38:59 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 21 Nov 2023 19:38:59 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 21 Nov 2023 19:39:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 21 Nov 2023 19:39:10 GMT
CMD ["pypy3"]
# Wed, 22 Nov 2023 04:43:00 GMT
ENV HY_VERSION=0.27.0
# Wed, 22 Nov 2023 04:43:00 GMT
ENV HYRULE_VERSION=0.4.0
# Wed, 22 Nov 2023 04:43:28 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 22 Nov 2023 04:43:28 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0337998fca395da23ee33151d039d33696c12bfde1746ecfa1393fea01eb70`  
		Last Modified: Tue, 21 Nov 2023 19:43:19 GMT  
		Size: 1.1 MB (1068483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d10a47659a1f02d34f9f3cbc07866541510031fa59e08a42330001bbaaae78`  
		Last Modified: Tue, 21 Nov 2023 19:45:40 GMT  
		Size: 36.0 MB (35958945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909d5a48aa23973f35422ccf6221b0e5d8ef8ec2e86a278cdec7db2998bc91d9`  
		Last Modified: Tue, 21 Nov 2023 19:45:34 GMT  
		Size: 3.1 MB (3131968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfaa732b3bd5899c8daa6bffa6e221b52b60defa27125d7cf2a4af4c83f42691`  
		Last Modified: Wed, 22 Nov 2023 04:48:32 GMT  
		Size: 3.9 MB (3918422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy3.9-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:bc40476a6dd6ebd1a66369896e790e8760c8fce938db508da33619be42de0010
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71737680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3678fa058d64ad2bde81a3b77e2a31fda569410c3b470721bbbd9c6a7e0dace`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 20:39:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 20:39:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:39:18 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 20:39:18 GMT
ENV PYPY_VERSION=7.3.13
# Tue, 21 Nov 2023 20:42:02 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.13-linux64.tar.bz2'; 			sha256='323b05a9f607e932cda1995cbe77a96e4ea35994631aa6d734c8035e8479b74e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.13-aarch64.tar.bz2'; 			sha256='317d7876c5825a086f854253648b967a432b993ce87695d2895d3ad6ed0d2716'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.13-linux32.tar.bz2'; 			sha256='ac695238b4a3635ac6b482e74e04e2ea78b31acca0decd5de601dfd2f4ebf35a'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.13-s390x.tar.bz2'; 			sha256='213c88f652a99c4dc4e8e00b4b5b58f381c7f7e9ea1a9b65801fc0eb1e50df0a'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 21 Nov 2023 20:42:03 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 21 Nov 2023 20:42:03 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 21 Nov 2023 20:42:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 21 Nov 2023 20:42:14 GMT
CMD ["pypy3"]
# Wed, 22 Nov 2023 04:31:25 GMT
ENV HY_VERSION=0.27.0
# Wed, 22 Nov 2023 04:31:25 GMT
ENV HYRULE_VERSION=0.4.0
# Wed, 22 Nov 2023 04:31:53 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 22 Nov 2023 04:31:53 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf157973a6a6e0198d38f8dec212a54185af3658f66389af49200fd69990568f`  
		Last Modified: Tue, 21 Nov 2023 20:46:08 GMT  
		Size: 1.1 MB (1055749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aece2152647e71d9801afbc8f1c838e6f66c77834c61d4f1be4fc32b87f2c14`  
		Last Modified: Tue, 21 Nov 2023 20:47:44 GMT  
		Size: 33.6 MB (33567603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fbe3f7823239f3dd62cdd6b94bc775084cb238212d7e62beeae3c3b94edd11f`  
		Last Modified: Tue, 21 Nov 2023 20:47:40 GMT  
		Size: 3.1 MB (3131715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e564bf0a76202e0b5e0282b9a181631f25a099afec809ea049dc5e563c052f5a`  
		Last Modified: Wed, 22 Nov 2023 04:37:01 GMT  
		Size: 3.9 MB (3918490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy3.9-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:4f0e8dd8ec2eb2f7002d998eca5f6569a88ecb9aeee377f81029178e5f8041da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74890824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a1e3df1bf1ab8b48776ff8e7c69468ecc8bfe886d016bed22d9a12275593f9`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Nov 2023 04:40:15 GMT
ADD file:7de881b584405a880c4d02778056aaa81bb5dd5d1af65b3086d66aed9ff0ad4b in / 
# Tue, 21 Nov 2023 04:40:16 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 15:47:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 15:47:05 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 15:47:05 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 15:47:05 GMT
ENV PYPY_VERSION=7.3.13
# Tue, 21 Nov 2023 15:51:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.13-linux64.tar.bz2'; 			sha256='323b05a9f607e932cda1995cbe77a96e4ea35994631aa6d734c8035e8479b74e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.13-aarch64.tar.bz2'; 			sha256='317d7876c5825a086f854253648b967a432b993ce87695d2895d3ad6ed0d2716'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.13-linux32.tar.bz2'; 			sha256='ac695238b4a3635ac6b482e74e04e2ea78b31acca0decd5de601dfd2f4ebf35a'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.13-s390x.tar.bz2'; 			sha256='213c88f652a99c4dc4e8e00b4b5b58f381c7f7e9ea1a9b65801fc0eb1e50df0a'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 21 Nov 2023 15:51:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 21 Nov 2023 15:51:21 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 21 Nov 2023 15:51:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 21 Nov 2023 15:51:36 GMT
CMD ["pypy3"]
# Wed, 22 Nov 2023 08:34:28 GMT
ENV HY_VERSION=0.27.0
# Wed, 22 Nov 2023 08:34:28 GMT
ENV HYRULE_VERSION=0.4.0
# Wed, 22 Nov 2023 08:35:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 22 Nov 2023 08:35:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:75c11612678b54e79a38118fe66e532c61b3d0798afb741007b4cd3209c0ec4e`  
		Last Modified: Tue, 21 Nov 2023 04:45:24 GMT  
		Size: 32.4 MB (32402632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32385ddf578b3e6564c8d27f1b6a283bcfab59455902fafa8fbb24f5a04b55dc`  
		Last Modified: Tue, 21 Nov 2023 15:56:18 GMT  
		Size: 1.1 MB (1080429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4941149d2feb39068eb2ee5904c5770a45527774bdaff9197e3de92f8548ff`  
		Last Modified: Tue, 21 Nov 2023 15:58:14 GMT  
		Size: 34.4 MB (34357512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89735e2e0f068b7c9e0d06634f3cbb352d68392cd0453f7247487492c0acbfa`  
		Last Modified: Tue, 21 Nov 2023 15:58:05 GMT  
		Size: 3.1 MB (3131618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365405a1d4262584c503838c84e22fd54fbe31df97de4ef2517664a8a38b3689`  
		Last Modified: Wed, 22 Nov 2023 08:40:33 GMT  
		Size: 3.9 MB (3918633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
