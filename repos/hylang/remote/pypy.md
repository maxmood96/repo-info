## `hylang:pypy`

```console
$ docker pull hylang@sha256:b3dd1d012d41388fd77177ce33273d24408f1cdb7d6e3ad16b33cd008e2145c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x
	-	windows version 10.0.17763.1935; amd64

### `hylang:pypy` - linux; amd64

```console
$ docker pull hylang@sha256:3b547ce5cff457e5063f830179f4ae83324f08740c761a97c07fa39f3513e280
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74181177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90360b49a227e6f9ed2d7426ace42f61fba8007abba53d5f8dbcdc29c37fd92`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 14:46:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 14:46:44 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 14:46:44 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 14:46:45 GMT
ENV PYPY_VERSION=7.3.4
# Wed, 12 May 2021 14:47:14 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.4-linux64.tar.bz2'; 			sha256='09d7298b44a38648a87995ec06e1e093761644e50f547c8bb0b2d7f4fe433548'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.4-aarch64.tar.bz2'; 			sha256='a4148fa73b74a091e004e1f378b278c0b8830984cbcb91e10fa31fd915c43efe'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.4-linux32.tar.bz2'; 			sha256='04de1a2e80530f3d74abcf133ec046a0fb12d81956bc043dee8ab4799f3b77eb'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.4-s390x.tar.bz2'; 			sha256='7d6fb180c359a66a158ef6e81eeca88fbabbb62656a1700f425a70db18de2a0f'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 12 May 2021 14:47:15 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Wed, 12 May 2021 14:47:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 12 May 2021 14:47:15 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 12 May 2021 14:47:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 12 May 2021 14:47:34 GMT
CMD ["pypy3"]
# Thu, 13 May 2021 07:57:36 GMT
ENV HY_VERSION=1.0a1
# Thu, 13 May 2021 07:57:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 13 May 2021 07:57:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db5028b68bc95cdca0100f5f0112b94faeafb23674980662f8593d974f1d8a0`  
		Last Modified: Wed, 12 May 2021 14:51:08 GMT  
		Size: 2.8 MB (2757664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140131ab92eee6c4de2147d919e5e95a8bba973529b71106087c00cd92651543`  
		Last Modified: Wed, 12 May 2021 14:51:17 GMT  
		Size: 38.6 MB (38598883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1e5e4e46b270d0a4cfeb9aec13899d721adc852f8f6048dc8d206b688dd14b`  
		Last Modified: Wed, 12 May 2021 14:51:09 GMT  
		Size: 2.6 MB (2566127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190d264b99b2438a1eb14d3433ada44da962654af9476207a95ef4810aebb137`  
		Last Modified: Thu, 13 May 2021 08:00:35 GMT  
		Size: 3.1 MB (3112588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:f5b71d87b0db417641b8fdab347da1f08580b3590f3c6f1f0ee8ba0f0bdd0875
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69580369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f6a7c08c159148ca9672e419a913e6bbf14c640ff3bd4f0097f7881b27509a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 12 May 2021 00:52:19 GMT
ADD file:91ba1791cab3ad29a1469d1e78f21f4c0b5d3d30598683b7104980604c318854 in / 
# Wed, 12 May 2021 00:52:34 GMT
CMD ["bash"]
# Wed, 12 May 2021 13:45:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 13:45:15 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 13:45:16 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 13:45:18 GMT
ENV PYPY_VERSION=7.3.4
# Wed, 12 May 2021 13:46:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.4-linux64.tar.bz2'; 			sha256='09d7298b44a38648a87995ec06e1e093761644e50f547c8bb0b2d7f4fe433548'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.4-aarch64.tar.bz2'; 			sha256='a4148fa73b74a091e004e1f378b278c0b8830984cbcb91e10fa31fd915c43efe'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.4-linux32.tar.bz2'; 			sha256='04de1a2e80530f3d74abcf133ec046a0fb12d81956bc043dee8ab4799f3b77eb'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.4-s390x.tar.bz2'; 			sha256='7d6fb180c359a66a158ef6e81eeca88fbabbb62656a1700f425a70db18de2a0f'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 12 May 2021 13:46:25 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Wed, 12 May 2021 13:46:30 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 12 May 2021 13:46:35 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 12 May 2021 13:47:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 12 May 2021 13:47:23 GMT
CMD ["pypy3"]
# Thu, 13 May 2021 08:02:03 GMT
ENV HY_VERSION=1.0a1
# Thu, 13 May 2021 08:02:38 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 13 May 2021 08:02:42 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fcad0c936ea5c12e1c8c4edb81a97c0cde04ee71e7067ee3b246474cf1854d7a`  
		Last Modified: Wed, 12 May 2021 01:02:02 GMT  
		Size: 25.9 MB (25911250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae606e4b598425ee3f0eae7006e8aae45b5faf7662ede98f48398412254a4f73`  
		Last Modified: Wed, 12 May 2021 13:52:04 GMT  
		Size: 2.6 MB (2626299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57db94c99213b29a78a31e2ede0db03a9dff2d1a90bf23f2d441a770ece30ff7`  
		Last Modified: Wed, 12 May 2021 13:52:15 GMT  
		Size: 35.4 MB (35363762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9a0e2944bd344909f63a0e568701f8ead1f9a8ddba287831060fa7c3a652d6`  
		Last Modified: Wed, 12 May 2021 13:52:04 GMT  
		Size: 2.6 MB (2565948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fa98a5da19a90939a21cc01dd5d495e07fc0c27f6cd4d678eb260b0a1ea9ea`  
		Last Modified: Thu, 13 May 2021 08:05:04 GMT  
		Size: 3.1 MB (3113110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy` - linux; 386

```console
$ docker pull hylang@sha256:441bbf31bc3815cee562244719f5eded806a28f042ed86f64e4bec0f582df7e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76848043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6f9bdf9d3967e5783e9bf84877e66aee75ffeea740877b6e8d238d55df7f5d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 12 May 2021 00:39:52 GMT
ADD file:62173a7456d614031a7b20be741983644d9723c734eee663b099ad6b47af7b35 in / 
# Wed, 12 May 2021 00:39:53 GMT
CMD ["bash"]
# Wed, 12 May 2021 12:38:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 12:38:40 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 12:38:41 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 12:38:41 GMT
ENV PYPY_VERSION=7.3.4
# Wed, 12 May 2021 12:39:10 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.4-linux64.tar.bz2'; 			sha256='09d7298b44a38648a87995ec06e1e093761644e50f547c8bb0b2d7f4fe433548'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.4-aarch64.tar.bz2'; 			sha256='a4148fa73b74a091e004e1f378b278c0b8830984cbcb91e10fa31fd915c43efe'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.4-linux32.tar.bz2'; 			sha256='04de1a2e80530f3d74abcf133ec046a0fb12d81956bc043dee8ab4799f3b77eb'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.4-s390x.tar.bz2'; 			sha256='7d6fb180c359a66a158ef6e81eeca88fbabbb62656a1700f425a70db18de2a0f'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 12 May 2021 12:39:11 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Wed, 12 May 2021 12:39:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 12 May 2021 12:39:11 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 12 May 2021 12:39:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 12 May 2021 12:39:25 GMT
CMD ["pypy3"]
# Wed, 12 May 2021 19:21:07 GMT
ENV HY_VERSION=1.0a1
# Wed, 12 May 2021 19:21:17 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 12 May 2021 19:21:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9b548256784c8e079e5953ec08bd26ce8cbaed0d606a5d350b4bcd12710d2192`  
		Last Modified: Wed, 12 May 2021 00:46:39 GMT  
		Size: 27.8 MB (27795074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb63b37fe34f2cd5f37adaacc9536932e1923c91535448092ffc5ffcc0d19bb`  
		Last Modified: Wed, 12 May 2021 12:44:01 GMT  
		Size: 2.8 MB (2769460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140de4b878d8cf1b24ae54ce98ccf0f9791927177a904b5f66c16b580f4f6559`  
		Last Modified: Wed, 12 May 2021 12:44:16 GMT  
		Size: 40.6 MB (40605139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add89bd2f94ae5e2d48399acafa4c1724f536282ded7bd4c79a46fa098041878`  
		Last Modified: Wed, 12 May 2021 12:44:01 GMT  
		Size: 2.6 MB (2565766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84e413f0e98e790391ee3869973b78b34bf3001f70c2e7732cb91ac90353b0d`  
		Last Modified: Wed, 12 May 2021 19:26:25 GMT  
		Size: 3.1 MB (3112604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy` - linux; s390x

```console
$ docker pull hylang@sha256:5b4ee55ad1d4435e5eedf21db6a023c1423c8af8016cf7c945b470545984b33e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69473409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ff020b4af23350249a8809179ec992a97f9a5544cfa3136babe64da8bb9bdf`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 12 May 2021 00:43:38 GMT
ADD file:77af21d863769b75a5f055b85b2c9d6e878f9d77a4122397ae8dde6b69e945c6 in / 
# Wed, 12 May 2021 00:43:42 GMT
CMD ["bash"]
# Wed, 12 May 2021 06:13:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 06:13:02 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 06:13:02 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 06:13:03 GMT
ENV PYPY_VERSION=7.3.4
# Wed, 12 May 2021 06:13:59 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.4-linux64.tar.bz2'; 			sha256='09d7298b44a38648a87995ec06e1e093761644e50f547c8bb0b2d7f4fe433548'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.4-aarch64.tar.bz2'; 			sha256='a4148fa73b74a091e004e1f378b278c0b8830984cbcb91e10fa31fd915c43efe'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.4-linux32.tar.bz2'; 			sha256='04de1a2e80530f3d74abcf133ec046a0fb12d81956bc043dee8ab4799f3b77eb'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.4-s390x.tar.bz2'; 			sha256='7d6fb180c359a66a158ef6e81eeca88fbabbb62656a1700f425a70db18de2a0f'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 12 May 2021 06:14:04 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Wed, 12 May 2021 06:14:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 12 May 2021 06:14:05 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 12 May 2021 06:14:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 12 May 2021 06:14:31 GMT
CMD ["pypy3"]
# Wed, 12 May 2021 21:57:45 GMT
ENV HY_VERSION=1.0a1
# Wed, 12 May 2021 21:58:00 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 12 May 2021 21:58:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ba4b99e0e723623b64d4ecb8d74102998d32137ea9bcc88b15fd2e4e34b38df9`  
		Last Modified: Wed, 12 May 2021 00:48:03 GMT  
		Size: 25.8 MB (25760171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2edb18f5c9b647c5730f0ed0acea816dc6504113efcc15f2b461b4959b4470bc`  
		Last Modified: Wed, 12 May 2021 06:15:48 GMT  
		Size: 2.5 MB (2452407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4572a6625dfad1d2e1321c81085e284ec00994ea434cfc1f27f78c687c286e`  
		Last Modified: Wed, 12 May 2021 06:15:57 GMT  
		Size: 35.6 MB (35581814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96bc39c4eacd9dae67c1a3cbe3f612c721538fc86504b57de9ba85f6690fa6a4`  
		Last Modified: Wed, 12 May 2021 06:15:48 GMT  
		Size: 2.6 MB (2566210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1970da7e2ff0630d4e83d4b9d4f11d088824c081565def1bcad096913b4e0b2d`  
		Last Modified: Wed, 12 May 2021 22:00:14 GMT  
		Size: 3.1 MB (3112807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy` - windows version 10.0.17763.1935; amd64

```console
$ docker pull hylang@sha256:5dbf893722b4242e006952513b0beb9ce76afdbeaa218c5aa5d8a47df9ec642b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528806629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826956fd48d9755832d7fc336c6ee7778872e3cf6128120988f23af0261ba951`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 08 May 2021 09:21:48 GMT
RUN Install update 1809-amd64
# Wed, 12 May 2021 12:10:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 May 2021 12:11:29 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 12 May 2021 12:12:07 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 12 May 2021 12:12:08 GMT
ENV PYPY_VERSION=7.3.4
# Wed, 12 May 2021 12:13:11 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.7-v7.3.4-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '0ff4e4653f1ff0653f105680eb101c64c857fa8f828a54a61b02f65c94b5d262'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.7-v7.3.4-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy3 --version") ...'; 	pypy3 --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 12 May 2021 12:13:13 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Wed, 12 May 2021 12:13:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 12 May 2021 12:13:15 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 12 May 2021 12:15:02 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing "pip == {0}" ...' -f $env:PYTHON_PIP_VERSION); 	pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 12 May 2021 12:15:03 GMT
CMD ["pypy3"]
# Wed, 12 May 2021 16:29:35 GMT
ENV HY_VERSION=1.0a1
# Wed, 12 May 2021 16:30:41 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 12 May 2021 16:30:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8116de3c91c3f1ef2d6c09b49ef5407c9b4d672896eb3af5182a997c3c5379c9`  
		Size: 756.2 MB (756156286 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5b8861e3624ab787e21ee36b876b374a3b5ec40eed1621cebfe2f81d1c2cda37`  
		Last Modified: Wed, 12 May 2021 12:20:32 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646d0b1f5b2de003e7020ff1d5159bdda97a41947bc8ea1f0462695be1954832`  
		Last Modified: Wed, 12 May 2021 12:20:32 GMT  
		Size: 5.1 MB (5095334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5660485e40f20eb051915b07c98bbea7a0251908408aedb487ec0cc4de228afa`  
		Last Modified: Wed, 12 May 2021 12:20:49 GMT  
		Size: 15.5 MB (15482514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab72861d4181ae7cfc020ba097cb2253a1702478e0d7f5f20982e162ab08e599`  
		Last Modified: Wed, 12 May 2021 12:20:30 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26a24b8dafc4d3221e206b58f54a9a95f408822c886357fdb7d033e4bd516e1`  
		Last Modified: Wed, 12 May 2021 12:20:38 GMT  
		Size: 26.9 MB (26922970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c022078e9fb6e2a17272ebf52e549ec2dd6b315d8160f77a291eb322b884356`  
		Last Modified: Wed, 12 May 2021 12:20:28 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af180e039a0ed206591e2525438f4bd2e6464be796d222c5028b759fb635e0e5`  
		Last Modified: Wed, 12 May 2021 12:20:28 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68aed7ad8327b382722052574fa1526f82a6ffc0aee98241be0de0a354f0fbb`  
		Last Modified: Wed, 12 May 2021 12:20:28 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f6ac9b0a6e60da6c11709657d49a754879426ca855cce315100b937190b862`  
		Last Modified: Wed, 12 May 2021 12:20:29 GMT  
		Size: 2.9 MB (2896217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37ebbff15b8ca8057773d26cce86ab855233caffe8a0440443f99c4110dd3e5`  
		Last Modified: Wed, 12 May 2021 12:20:28 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b57c5b7505a15beafec8127f84fbf393aca9afd4650343eecaa78990870ee56`  
		Last Modified: Wed, 12 May 2021 16:33:41 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23f4eafe5efc7e6f949bbf2b442396071146fd1ad57f826caeb75d2e63a379b`  
		Last Modified: Wed, 12 May 2021 16:33:41 GMT  
		Size: 3.9 MB (3909099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d7b9618b4f136c40e67c0cf7a32f385dfe83fa9d6ffec7744bc7a420a47ee1`  
		Last Modified: Wed, 12 May 2021 16:33:40 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
