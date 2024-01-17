## `hylang:0-pypy3.9`

```console
$ docker pull hylang@sha256:3258f07685af396b6755b00e0279b8eecb6260556ad4bb16f0e421d1fcf15136
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `hylang:0-pypy3.9` - linux; amd64

```console
$ docker pull hylang@sha256:9e07e10b4b31c6c30ef01fed63dae734e653508da37d9ad4dd3e53b62224fd45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77820322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cc1c8fff257faf36df3ae42363ea0291e7d64f68669c5f8ae7d5cf30ccdff3`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYPY_VERSION=7.3.15
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-linux64.tar.bz2'; 			sha256='f062be307200bde434817e1620cebc13f563d6ab25309442c5f4d0f0d68f0912'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-aarch64.tar.bz2'; 			sha256='03e35fcba290454bb0ccf7ee57fb42d1e63108d10d593776a382c0a2fe355de0'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-linux32.tar.bz2'; 			sha256='c6209380977066c9e8b96e8258821c70f996004ce1bc8659ae83d4fd5a89ff5c'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-s390x.tar.bz2'; 			sha256='deeb5e54c36a0fd9cfefd16e63a0d5bed4f4a43e6bbc01c23f0ed8f7f1c0aaf3'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["pypy3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24be3246fb7cea7c247e8a5a742ec32281c4b4e8beb9bc127f037a3da6b229c`  
		Last Modified: Tue, 16 Jan 2024 23:55:54 GMT  
		Size: 3.5 MB (3490952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3684352c1f9463911b70db1c06f5fb2fadfbbc9942a46f40a656853870c23004`  
		Last Modified: Tue, 16 Jan 2024 23:55:55 GMT  
		Size: 37.6 MB (37564834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98355f093416566d18e4a328118cdbd45fcb7e17f9fa2330db6ec87adb8b1364`  
		Last Modified: Tue, 16 Jan 2024 23:55:54 GMT  
		Size: 3.3 MB (3306647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff92ce3748908fec6a2c810ab1c97d251b66f2abc12045de08db1f1ff93b236`  
		Last Modified: Wed, 17 Jan 2024 00:48:21 GMT  
		Size: 4.3 MB (4331968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:794879894c9b36173cf1dba06e50e9a81d28ca073ca3421d4a966b8eeee06224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3157486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75af3660cc8450a18857aca807743478e305aa8806f1c97aef36647c4a486ce1`

```dockerfile
```

-	Layers:
	-	`sha256:26608fd6d9c6a42cd1b1c714069e9448b83421df1804fad836ef5c847f00f7cf`  
		Last Modified: Wed, 17 Jan 2024 00:48:21 GMT  
		Size: 3.1 MB (3147642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70d62752231efc05890ffe8706b3c45e4c8838f7eb8c0b5edd84d11acce9ad4a`  
		Last Modified: Wed, 17 Jan 2024 00:48:20 GMT  
		Size: 9.8 KB (9844 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy3.9` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:ef13fdede6a45d4617f6ea829205df48ce11c3237f5d0013d6dc149c8d38bd6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75016645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753ed5813a89c2f8a2e587366c5226d5f888a8bb9c8ae379d4a39d535f0a7c55`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 25 Dec 2023 11:23:57 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Mon, 25 Dec 2023 11:23:57 GMT
CMD ["bash"]
# Mon, 25 Dec 2023 11:23:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Dec 2023 11:23:57 GMT
ENV LANG=C.UTF-8
# Mon, 25 Dec 2023 11:23:57 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Dec 2023 11:23:57 GMT
ENV PYPY_VERSION=7.3.14
# Mon, 25 Dec 2023 11:23:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-linux64.tar.bz2'; 			sha256='febd770a616641ca8419c381c7fb224e515b892551d0db49a1231397ed38859d'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-aarch64.tar.bz2'; 			sha256='14b842f32f60ce2d9d130971f9bcbdb6875824a0e78fac36806d267e0982179c'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-linux32.tar.bz2'; 			sha256='4ad89a22369a6f2f83a7d8d047e0fc4cf5597f0921fa7afa23499ed05f663503'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-s390x.tar.bz2'; 			sha256='ba2451e9081db5bc724a05530a7f98817231de83ff6fdf15bad21a4e9b6dfeae'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 25 Dec 2023 11:23:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 25 Dec 2023 11:23:57 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 25 Dec 2023 11:23:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 25 Dec 2023 11:23:57 GMT
CMD ["pypy3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa08786caa4d74f3bf11ea2caa37196d90b37f529f9b8c5525bd68019cca438`  
		Last Modified: Fri, 12 Jan 2024 17:16:39 GMT  
		Size: 3.3 MB (3314054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb28d329ed24f5c644d32f32950c04dc1abd4cc49136d3b4d76a103222daea1e`  
		Last Modified: Fri, 12 Jan 2024 17:21:17 GMT  
		Size: 34.9 MB (34906549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a237f02b363f95187f5c690bed7b390db4730ce684956347957ea8d810f7bdb`  
		Last Modified: Fri, 12 Jan 2024 17:21:16 GMT  
		Size: 3.3 MB (3306804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992dad6f8b3f7961ba8ee6726641435fd0811db7b1db5f3befd455a2d2a31a72`  
		Last Modified: Fri, 12 Jan 2024 21:39:49 GMT  
		Size: 4.3 MB (4331903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:9b662ed9abba6abff207936d3e94eb8b555696f6af88e01efcc47fb083f0478c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a345393f66ff7c0e89ab260619511c44ecd2ba4c996ae8a58b8c5c7f25dba2`

```dockerfile
```

-	Layers:
	-	`sha256:17e416127c5eb7b5d1ea3dc29fd7e103fb44e303901ea86d26b4b540790f7256`  
		Last Modified: Fri, 12 Jan 2024 21:39:49 GMT  
		Size: 3.1 MB (3122825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5743032f56aa5ac58254ad98530fd1700cf824502957185f46309320ea7fae37`  
		Last Modified: Fri, 12 Jan 2024 21:39:49 GMT  
		Size: 9.9 KB (9886 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy3.9` - linux; 386

```console
$ docker pull hylang@sha256:e415003eae7aa617c788f431eec8f2f99e29c10f0c2102d0751a88f868cfcab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74687904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7140bb75ff24c32d3c17bb108947008cbd2d74c71aa7bdb98a61696b64bd2c47`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:48689786b7812032adc0d36643501f16ddee15750a8f0f8b614dba58e5037b2b in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYPY_VERSION=7.3.15
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-linux64.tar.bz2'; 			sha256='f062be307200bde434817e1620cebc13f563d6ab25309442c5f4d0f0d68f0912'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-aarch64.tar.bz2'; 			sha256='03e35fcba290454bb0ccf7ee57fb42d1e63108d10d593776a382c0a2fe355de0'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-linux32.tar.bz2'; 			sha256='c6209380977066c9e8b96e8258821c70f996004ce1bc8659ae83d4fd5a89ff5c'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-s390x.tar.bz2'; 			sha256='deeb5e54c36a0fd9cfefd16e63a0d5bed4f4a43e6bbc01c23f0ed8f7f1c0aaf3'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["pypy3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:de2bfe459016bec412fddc313b793adc6d47c8a4540608a6f3e217998027f073`  
		Last Modified: Thu, 11 Jan 2024 02:43:20 GMT  
		Size: 30.1 MB (30143875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3276ecb69b2ee50cdb1d0c7cccd52a734f75e1b44f77bd42373260ee13b805`  
		Last Modified: Tue, 16 Jan 2024 23:55:59 GMT  
		Size: 3.5 MB (3496100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbee07dad871274784de98bdd5510182672ce17ca8bf2d34c8a8afebe358c0a`  
		Last Modified: Tue, 16 Jan 2024 23:55:59 GMT  
		Size: 33.4 MB (33409917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8599b5c3324744831c4fc2294dd54639be79cfb929916e812d5c8d73ec1e61b`  
		Last Modified: Tue, 16 Jan 2024 23:55:59 GMT  
		Size: 3.3 MB (3306267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63eebca1da8e3cd69896285056ab58a1bc5eeec1bb4736e05545c1ff86d9fcfc`  
		Last Modified: Wed, 17 Jan 2024 00:48:11 GMT  
		Size: 4.3 MB (4331745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:be12db0f7a9f8781f1a07bf81dae096b54eb1ece79cf2341f1986760c1e666e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05ce34494234d92b05310498d13a5ef2728b7de446f3e7d6e60379e29b4414d`

```dockerfile
```

-	Layers:
	-	`sha256:29651c965c5d0d927e7158c5a59e86dc4bb83ade81eb46e96c2f8ae54db2da7f`  
		Last Modified: Wed, 17 Jan 2024 00:48:11 GMT  
		Size: 3.1 MB (3141963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1176547f3ee9a34ce623766b389e120e32536b75ce06ae5012311113db0fad6`  
		Last Modified: Wed, 17 Jan 2024 00:48:10 GMT  
		Size: 9.8 KB (9791 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy3.9` - windows version 10.0.20348.2227; amd64

```console
$ docker pull hylang@sha256:f9f028945747aa97c4a54fe4932c6fd72f702be9dd06aa6f0cc9f42ce12b9a46
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1952908783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd18b11e3efdaaa008deda33f1dc68f455298530e759c98f8cab20fdd44ab3d2`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Tue, 16 Jan 2024 23:58:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Jan 2024 23:58:53 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 16 Jan 2024 23:59:02 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 16 Jan 2024 23:59:03 GMT
ENV PYPY_VERSION=7.3.15
# Tue, 16 Jan 2024 23:59:21 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.9-v7.3.15-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a156dad8b58570597eaaabe05663f00f80c60bc11df4a9c46d0953b6c5eb9209'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.9-v7.3.15-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 16 Jan 2024 23:59:22 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 16 Jan 2024 23:59:23 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 16 Jan 2024 23:59:44 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 16 Jan 2024 23:59:45 GMT
CMD ["pypy"]
# Wed, 17 Jan 2024 00:55:15 GMT
ENV HY_VERSION=0.28.0
# Wed, 17 Jan 2024 00:55:16 GMT
ENV HYRULE_VERSION=0.5.0
# Wed, 17 Jan 2024 00:56:14 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 17 Jan 2024 00:56:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00452a1070e759d3ca4a95365e16bb1867c3cdcf57d82a438d5867ee6a847c5`  
		Last Modified: Tue, 16 Jan 2024 23:59:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce886381b02044e8a1d042bbb847c1c5456f13b1f58f091f417b0a3521639d6a`  
		Last Modified: Tue, 16 Jan 2024 23:59:52 GMT  
		Size: 488.1 KB (488058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a62a464dabb74f7529295c33fd2895d91f3719881b048029c4ca340979cd2e4`  
		Last Modified: Tue, 16 Jan 2024 23:59:53 GMT  
		Size: 15.5 MB (15540472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79be8cdb064c3b9b386c999bb6a75b31033dad9ec54609e9bc42a09821f0cc4`  
		Last Modified: Tue, 16 Jan 2024 23:59:52 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235ad6a5eee9f35e68492928da0a4ac2fdd61ce56a3f3cbbda1acbf7a5089bfa`  
		Last Modified: Tue, 16 Jan 2024 23:59:53 GMT  
		Size: 27.6 MB (27581903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8667f2296339db4bf0d6500528ba7d6794b89bc789544981a27b5f98a717a41c`  
		Last Modified: Tue, 16 Jan 2024 23:59:49 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deda35a3ee78c246c968826f259491972c91005322cf1f1f7b1ab00cbe054790`  
		Last Modified: Tue, 16 Jan 2024 23:59:49 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516ebcdae6507a6b5cc2e9d0d57f17e6c23a2c1d61eeb85e971073eba593405c`  
		Last Modified: Tue, 16 Jan 2024 23:59:50 GMT  
		Size: 3.9 MB (3927342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600601f226b87dc441e6b11a6385c92bfac2645d74bb56e1c67957e91025160f`  
		Last Modified: Tue, 16 Jan 2024 23:59:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14442a82a872a78b2d64bb01c21d9ffefbd022b247393209871138124fefa8c1`  
		Last Modified: Wed, 17 Jan 2024 00:56:19 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aed3a9c9d56bbfc476920e5b8b69b9419c7478166c39a09950f4fbe86d54ab6`  
		Last Modified: Wed, 17 Jan 2024 00:56:18 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f673b0108cad70f1dcedacaa687f8ccb9e119efaea9b83e3a09750f0cf7757`  
		Last Modified: Wed, 17 Jan 2024 00:56:20 GMT  
		Size: 5.1 MB (5147824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f3c35c7dc66d540e9442b2d33515158126f41deba9fd1b02414cec22f0cdb4`  
		Last Modified: Wed, 17 Jan 2024 00:56:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy3.9` - windows version 10.0.17763.5329; amd64

```console
$ docker pull hylang@sha256:1c8d36421f2de7c9d1f2def25439dc37457c6929d10b0f6fd70c2b25cbcc31ac
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2122340127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cafa1d85ddbb21efb968f204950eb41f11c4f8c1a4d62517bd0243bf0727652e`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 17 Jan 2024 00:18:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Jan 2024 00:20:29 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 17 Jan 2024 00:21:03 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 17 Jan 2024 00:21:04 GMT
ENV PYPY_VERSION=7.3.15
# Wed, 17 Jan 2024 00:21:44 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.9-v7.3.15-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a156dad8b58570597eaaabe05663f00f80c60bc11df4a9c46d0953b6c5eb9209'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.9-v7.3.15-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 17 Jan 2024 00:21:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 17 Jan 2024 00:21:46 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 17 Jan 2024 00:22:25 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 17 Jan 2024 00:22:26 GMT
CMD ["pypy"]
# Wed, 17 Jan 2024 00:56:21 GMT
ENV HY_VERSION=0.28.0
# Wed, 17 Jan 2024 00:56:23 GMT
ENV HYRULE_VERSION=0.5.0
# Wed, 17 Jan 2024 00:57:58 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 17 Jan 2024 00:57:59 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0392cf644bf5d4e63b9d2d7fd94df9f0a8a49ce69c277eeee3eee89199a3603`  
		Last Modified: Wed, 17 Jan 2024 00:22:31 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72e853e0f55db9c7c0d13571981b2b79197f3884322a3902726da6535967eaf`  
		Last Modified: Wed, 17 Jan 2024 00:22:30 GMT  
		Size: 493.6 KB (493619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4153db4b7b6edbe0e906c46fa6278aa361cbdd1d7871a559025091a2ab9163`  
		Last Modified: Wed, 17 Jan 2024 00:22:31 GMT  
		Size: 15.5 MB (15522902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e393f1bf90954fcc5cf96f4fb93a7cd1043eb72a2bbfc48a207a71146a81c0c`  
		Last Modified: Wed, 17 Jan 2024 00:22:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e197778f307375a523c988848f35d122221e4a6a56a999031831b07e8fcb35`  
		Last Modified: Wed, 17 Jan 2024 00:22:33 GMT  
		Size: 27.6 MB (27576958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc18a5899caf6fbf9bd254b94eb7d22a813accd9dea719cb79d042b9515c2492`  
		Last Modified: Wed, 17 Jan 2024 00:22:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50bc2cd79bc24841db6d3e00645aadc2f3e525c44064ac9e8e08b07929f8b20`  
		Last Modified: Wed, 17 Jan 2024 00:22:29 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1959bdff94d59a0f731cddba8887d5449433a9cdbd14cdb111d71b83521572`  
		Last Modified: Wed, 17 Jan 2024 00:22:30 GMT  
		Size: 3.9 MB (3916896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2425a6940a1592bc6497a101c69be666b495c6ae7966c20b407d703a67bf17`  
		Last Modified: Wed, 17 Jan 2024 00:22:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd611c331385fd4e121ed33022d28ee079155cbf7ee3b654ce2c023346a88419`  
		Last Modified: Wed, 17 Jan 2024 00:58:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9474e91fe787aace25e1dbbb010009300b996b2fd756153e69a9dda9d385dd38`  
		Last Modified: Wed, 17 Jan 2024 00:58:03 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649a5f5a2dfa64abfdc275f26d5e3e1be6248cf20313c94656af0ba44475f873`  
		Last Modified: Wed, 17 Jan 2024 00:58:04 GMT  
		Size: 5.1 MB (5096819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d84ea02a1af2d5bcd107d7a905c0f81a21e282496d7381ad61c7b610df0eb1`  
		Last Modified: Wed, 17 Jan 2024 00:58:03 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
