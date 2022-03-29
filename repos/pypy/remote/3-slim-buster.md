## `pypy:3-slim-buster`

```console
$ docker pull pypy@sha256:f116cb96e8e5b95ea9bf629929b8ee55799826c4c0177159370e88c6d5acdc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x

### `pypy:3-slim-buster` - linux; amd64

```console
$ docker pull pypy@sha256:8758a2df4e9ecdc35c5722210e2dac3abae08d0af3bd59420debf69c84f53c9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69503051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1762bfc54832394eee276486fc8e56f37948764ed8596f4d95a055da0a90b32f`
-	Default Command: `["pypy3"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 18:15:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 18:15:38 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 18:15:38 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 18:15:38 GMT
ENV PYPY_VERSION=7.3.8
# Tue, 29 Mar 2022 18:19:15 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.8-linux64.tar.bz2'; 			sha256='089f8e3e357d6130815964ddd3507c13bd53e4976ccf0a89b5c36a9a6775a188'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.8-aarch64-portable.tar.bz2'; 			sha256='0210536e9f1841ba283c13b04783394050837bb3e6f4091c9f1bd9c7f2b94b55'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.8-linux32.tar.bz2'; 			sha256='bea4b275decd492af6462157d293dd6fcf08a949859f8aec0959537b40afd032'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.8-s390x.tar.bz2'; 			sha256='ad53d373d6e275a41ca64da7d88afb6a17e48e7bfb2a6fff92daafdc06da6b90'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.8; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 29 Mar 2022 18:19:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 29 Mar 2022 18:19:15 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 29 Mar 2022 18:19:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 29 Mar 2022 18:19:27 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403755530240b815f3bec242ebade359d2edf509c46f7eb0871f6a479be008bc`  
		Last Modified: Tue, 29 Mar 2022 18:27:12 GMT  
		Size: 2.8 MB (2765092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0123ee663d73ecc57c03108738aa542d4b35f6998ed0c82c529f24e45a3e74`  
		Last Modified: Tue, 29 Mar 2022 18:29:42 GMT  
		Size: 37.0 MB (36957649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2968ca86c2ca9de108dc906a29338b479ffe2a449d13fafb28cc86a8af52f659`  
		Last Modified: Tue, 29 Mar 2022 18:29:36 GMT  
		Size: 2.6 MB (2628340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:3-slim-buster` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:add77eec417db0847beeafd1aabc801f093c7db4c66afe1c6fa19a23610d3dd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64832857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7baf3281863494e63c68c195f4c44cc7c1ab2d197c0c4908110cce46bb79a09`
-	Default Command: `["pypy3"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:22 GMT
ADD file:1c7d8cedf5dc79c676acebde5252ecd3005088a9f29e5e6be547f659f41efb1f in / 
# Thu, 17 Mar 2022 03:22:22 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 00:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 00:08:06 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 00:08:07 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Mar 2022 00:08:08 GMT
ENV PYPY_VERSION=7.3.8
# Fri, 18 Mar 2022 00:12:27 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.8-linux64.tar.bz2'; 			sha256='089f8e3e357d6130815964ddd3507c13bd53e4976ccf0a89b5c36a9a6775a188'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.8-aarch64-portable.tar.bz2'; 			sha256='0210536e9f1841ba283c13b04783394050837bb3e6f4091c9f1bd9c7f2b94b55'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.8-linux32.tar.bz2'; 			sha256='bea4b275decd492af6462157d293dd6fcf08a949859f8aec0959537b40afd032'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.8-s390x.tar.bz2'; 			sha256='ad53d373d6e275a41ca64da7d88afb6a17e48e7bfb2a6fff92daafdc06da6b90'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.8; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Fri, 18 Mar 2022 00:12:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 18 Mar 2022 00:12:28 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 18 Mar 2022 00:12:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 18 Mar 2022 00:12:43 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:c9277cac12165646c33f028489f2a5be3f70745382f4385cd9ed12fcc8cec183`  
		Last Modified: Thu, 17 Mar 2022 03:29:27 GMT  
		Size: 25.9 MB (25923233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0cb40d484223565238a3899f6e3d3bba4db27355cd2a2d82b19baa8d90de31`  
		Last Modified: Fri, 18 Mar 2022 00:24:04 GMT  
		Size: 2.6 MB (2626701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476f64af90451fa32c0ab7dd3854513c104271c2586b7e75c6ef5b178fc9320e`  
		Last Modified: Fri, 18 Mar 2022 00:26:52 GMT  
		Size: 33.9 MB (33864711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8b793efd4e06a871601f7f188940abb8e5cedff3bcc2a7384efc46ae4e500d`  
		Last Modified: Fri, 18 Mar 2022 00:26:46 GMT  
		Size: 2.4 MB (2418212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:3-slim-buster` - linux; 386

```console
$ docker pull pypy@sha256:eea32563fae07c1c0d09a1f44372b2ea31946b935e1fc0cd8c7c8c5b05a98ba8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71753818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171915e4802ac51833b3d3c3bd6b2321e0366812f0c23ec0d7cdefd5ae7ed257`
-	Default Command: `["pypy3"]`

```dockerfile
# Tue, 29 Mar 2022 00:42:26 GMT
ADD file:bcf3d504dc285de8b639c7f4017c41a4593a6c2aa6f046c9be79e587d05b5120 in / 
# Tue, 29 Mar 2022 00:42:27 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:28:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:28:01 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:28:02 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:28:03 GMT
ENV PYPY_VERSION=7.3.8
# Tue, 29 Mar 2022 17:32:15 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.8-linux64.tar.bz2'; 			sha256='089f8e3e357d6130815964ddd3507c13bd53e4976ccf0a89b5c36a9a6775a188'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.8-aarch64-portable.tar.bz2'; 			sha256='0210536e9f1841ba283c13b04783394050837bb3e6f4091c9f1bd9c7f2b94b55'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.8-linux32.tar.bz2'; 			sha256='bea4b275decd492af6462157d293dd6fcf08a949859f8aec0959537b40afd032'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.8-s390x.tar.bz2'; 			sha256='ad53d373d6e275a41ca64da7d88afb6a17e48e7bfb2a6fff92daafdc06da6b90'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.8; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 29 Mar 2022 17:32:16 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 29 Mar 2022 17:32:17 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 29 Mar 2022 17:32:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 29 Mar 2022 17:32:31 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:65b92490caa5e2c0588fab60d39315a2a8c09aa8ea0fe208d23f6984a47ecc03`  
		Last Modified: Tue, 29 Mar 2022 00:50:02 GMT  
		Size: 27.8 MB (27801252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233e5959675f3ed65989a324abc0c6349cc5b162d62ab68997dc30e78dcc3684`  
		Last Modified: Tue, 29 Mar 2022 17:44:18 GMT  
		Size: 2.8 MB (2777530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e034e844d621fa4da7f0296aeec1197f1d28bf558fe209827fae4bce60afed7e`  
		Last Modified: Tue, 29 Mar 2022 17:47:14 GMT  
		Size: 38.8 MB (38756835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5137734c14c31e98d162f27a92247cab5052495e81eaa121dfe741c68d516d94`  
		Last Modified: Tue, 29 Mar 2022 17:47:08 GMT  
		Size: 2.4 MB (2418201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:3-slim-buster` - linux; s390x

```console
$ docker pull pypy@sha256:774f6adb1a67da31d41ce257d198555737fcf921f99f32f0a5aaefcf68e38f01
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65678891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14478f7daf4def4e47c6afb94546d121720630eb434e2dfb3a066d4bb8ac9d01`
-	Default Command: `["pypy3"]`

```dockerfile
# Thu, 17 Mar 2022 03:07:30 GMT
ADD file:4342e1d9db757e91953273ac7120c9d6004d38281f9cea830898b4f35ca43517 in / 
# Thu, 17 Mar 2022 03:07:32 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 18:07:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 18:07:36 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 18:07:36 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 18:07:36 GMT
ENV PYPY_VERSION=7.3.8
# Thu, 17 Mar 2022 18:08:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.8-linux64.tar.bz2'; 			sha256='089f8e3e357d6130815964ddd3507c13bd53e4976ccf0a89b5c36a9a6775a188'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.8-aarch64-portable.tar.bz2'; 			sha256='0210536e9f1841ba283c13b04783394050837bb3e6f4091c9f1bd9c7f2b94b55'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.8-linux32.tar.bz2'; 			sha256='bea4b275decd492af6462157d293dd6fcf08a949859f8aec0959537b40afd032'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.8-s390x.tar.bz2'; 			sha256='ad53d373d6e275a41ca64da7d88afb6a17e48e7bfb2a6fff92daafdc06da6b90'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.8; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 17 Mar 2022 18:08:56 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 17 Mar 2022 18:08:56 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 17 Mar 2022 18:09:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 17 Mar 2022 18:09:07 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:6f8a08956872b0f67802da3a67e007322eb963a60e0dadd736077f3ece414e1f`  
		Last Modified: Thu, 17 Mar 2022 03:13:18 GMT  
		Size: 25.8 MB (25769076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d1788693a74d6af4c72d0963a7bcf2f42218c0d5484dcfbe9ba65f63561fcf`  
		Last Modified: Thu, 17 Mar 2022 18:12:35 GMT  
		Size: 2.5 MB (2452785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9051efca115cb7b74d6a79538499e466f326e6c18b605ecab20a5a3c08db52`  
		Last Modified: Thu, 17 Mar 2022 18:13:05 GMT  
		Size: 34.8 MB (34828816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdf8309759d7dd0c567f98d970b7f6cda10597e19708ca8b3c02003115989c1`  
		Last Modified: Thu, 17 Mar 2022 18:12:59 GMT  
		Size: 2.6 MB (2628214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
