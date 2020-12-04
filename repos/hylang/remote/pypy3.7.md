## `hylang:pypy3.7`

```console
$ docker pull hylang@sha256:b832a47a790301990fa58a23de19c4d9eba709af69c6fb0af94730d941f9f93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x

### `hylang:pypy3.7` - linux; amd64

```console
$ docker pull hylang@sha256:0679c3b37b1127fc7ec94880a292ed47b58957b8cae8ecf7629adc72c6469e75
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73536508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17a979b0bfc75d3a8284059e0abe93b88c85b39262b42ca6c237a583f90c41d`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 16:34:36 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 16:34:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 16:34:43 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Nov 2020 00:56:51 GMT
ENV PYPY_VERSION=7.3.3
# Tue, 24 Nov 2020 01:00:48 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='37e2804c4661c86c857d709d28c7de716b000d31e89766599fdf5a98928b7096' ;; 		arm64) pypyArch='aarch64'; sha256='ee4aa041558b58de6063dd6df93b3def221c4ca4c900d6a9db5b1b52135703a8' ;; 		i386) pypyArch='linux32'; sha256='7d81b8e9fcd07c067cfe2f519ab770ec62928ee8787f952cadf2d2786246efc8' ;; 		s390x) pypyArch='s390x'; sha256='92000d90b9a37f2e9cb7885f2a872adfa9e48e74bf7f84a8b8185c8181f0502d' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://downloads.python.org/pypy/pypy3.7-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -svT '/opt/pypy/bin/pypy3' '/usr/local/bin/pypy3'; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 03 Dec 2020 22:35:01 GMT
ENV PYTHON_PIP_VERSION=20.3.1
# Thu, 03 Dec 2020 22:35:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/91630a4867b1f93ba0a12aa81d0ec4ecc1e7eeb9/get-pip.py
# Thu, 03 Dec 2020 22:35:01 GMT
ENV PYTHON_GET_PIP_SHA256=d48ae68f297cac54db17e4107b800faae0e5210131f9f386c30c0166bf8d81b7
# Thu, 03 Dec 2020 22:35:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 03 Dec 2020 22:35:18 GMT
CMD ["pypy3"]
# Thu, 03 Dec 2020 23:31:31 GMT
ENV HY_VERSION=0.19.0
# Thu, 03 Dec 2020 23:31:42 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 03 Dec 2020 23:31:42 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48c9f9aa2053199d3d79a2090a1125edc4c3e330ac617f47d7689b26ad41103`  
		Last Modified: Wed, 18 Nov 2020 16:40:16 GMT  
		Size: 2.7 MB (2742481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae04fc32379425f2feff94106892956fb1f1baf6fa3d810e15ead4cd56d3a4c`  
		Last Modified: Tue, 24 Nov 2020 01:03:55 GMT  
		Size: 38.1 MB (38052371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb20241d58c0c201ebc27ab27d16b52e8d90717381bb970fd626cd9aa89c58b`  
		Last Modified: Thu, 03 Dec 2020 22:37:14 GMT  
		Size: 2.6 MB (2562306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6783ff3b12a26b291aa86f9833e534e0d3ef33627c38f34d114fb40efcec79`  
		Last Modified: Thu, 03 Dec 2020 23:34:57 GMT  
		Size: 3.1 MB (3073866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.7` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:d255e2d35123a551084595bea92eb32d69bec15e95d6638304091e73b07cdfed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65926882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e10eb56a8c31aa851a299343948e5b4ac7e61a2ad654d52e0722f3339b07ac`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 06:14:12 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 06:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 06:14:24 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Nov 2020 01:02:14 GMT
ENV PYPY_VERSION=7.3.3
# Tue, 24 Nov 2020 01:09:40 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='37e2804c4661c86c857d709d28c7de716b000d31e89766599fdf5a98928b7096' ;; 		arm64) pypyArch='aarch64'; sha256='ee4aa041558b58de6063dd6df93b3def221c4ca4c900d6a9db5b1b52135703a8' ;; 		i386) pypyArch='linux32'; sha256='7d81b8e9fcd07c067cfe2f519ab770ec62928ee8787f952cadf2d2786246efc8' ;; 		s390x) pypyArch='s390x'; sha256='92000d90b9a37f2e9cb7885f2a872adfa9e48e74bf7f84a8b8185c8181f0502d' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://downloads.python.org/pypy/pypy3.7-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -svT '/opt/pypy/bin/pypy3' '/usr/local/bin/pypy3'; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 03 Dec 2020 22:54:52 GMT
ENV PYTHON_PIP_VERSION=20.3.1
# Thu, 03 Dec 2020 22:54:53 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/91630a4867b1f93ba0a12aa81d0ec4ecc1e7eeb9/get-pip.py
# Thu, 03 Dec 2020 22:54:54 GMT
ENV PYTHON_GET_PIP_SHA256=d48ae68f297cac54db17e4107b800faae0e5210131f9f386c30c0166bf8d81b7
# Thu, 03 Dec 2020 22:55:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 03 Dec 2020 22:55:30 GMT
CMD ["pypy3"]
# Thu, 03 Dec 2020 23:28:09 GMT
ENV HY_VERSION=0.19.0
# Thu, 03 Dec 2020 23:28:30 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 03 Dec 2020 23:28:30 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d488c40d6fb7d62c9b295053c74a83901cee290b51460f3461d44ec5a8c39b`  
		Last Modified: Wed, 18 Nov 2020 06:24:05 GMT  
		Size: 2.6 MB (2606475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa9f6caa3da4ef30461e6cebc99cc0010ce38f9415e38e4ff8242a6d2f3b560`  
		Last Modified: Tue, 24 Nov 2020 01:14:45 GMT  
		Size: 31.8 MB (31819778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88333d5fa4d1e65a834646384083fdfeb790540b257835ab15f1ead4fb6c4304`  
		Last Modified: Thu, 03 Dec 2020 22:59:02 GMT  
		Size: 2.6 MB (2563027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3ab1430e3690ddebf5680ba1cec1e36590c28ad9536965979c26885bd1eab9`  
		Last Modified: Thu, 03 Dec 2020 23:32:45 GMT  
		Size: 3.1 MB (3075070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.7` - linux; 386

```console
$ docker pull hylang@sha256:14c787f628d7e070c08eda5eddc740e031a0bb013a5db2ced4b7fb4caf4215f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76508214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f953b965b86379a0e1ff22c482577dc904b32ba9b09edffd7c33c20864df0cf`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:58 GMT
ADD file:b17dfa607fcb298beb9c58bfbb8b9b0743ceb385875776c56269db2506840edf in / 
# Tue, 17 Nov 2020 20:19:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 03:13:00 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 03:13:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 03:13:13 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Nov 2020 00:50:07 GMT
ENV PYPY_VERSION=7.3.3
# Tue, 24 Nov 2020 00:54:50 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='37e2804c4661c86c857d709d28c7de716b000d31e89766599fdf5a98928b7096' ;; 		arm64) pypyArch='aarch64'; sha256='ee4aa041558b58de6063dd6df93b3def221c4ca4c900d6a9db5b1b52135703a8' ;; 		i386) pypyArch='linux32'; sha256='7d81b8e9fcd07c067cfe2f519ab770ec62928ee8787f952cadf2d2786246efc8' ;; 		s390x) pypyArch='s390x'; sha256='92000d90b9a37f2e9cb7885f2a872adfa9e48e74bf7f84a8b8185c8181f0502d' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://downloads.python.org/pypy/pypy3.7-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -svT '/opt/pypy/bin/pypy3' '/usr/local/bin/pypy3'; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 03 Dec 2020 22:48:07 GMT
ENV PYTHON_PIP_VERSION=20.3.1
# Thu, 03 Dec 2020 22:48:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/91630a4867b1f93ba0a12aa81d0ec4ecc1e7eeb9/get-pip.py
# Thu, 03 Dec 2020 22:48:08 GMT
ENV PYTHON_GET_PIP_SHA256=d48ae68f297cac54db17e4107b800faae0e5210131f9f386c30c0166bf8d81b7
# Thu, 03 Dec 2020 22:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 03 Dec 2020 22:48:27 GMT
CMD ["pypy3"]
# Thu, 03 Dec 2020 23:07:58 GMT
ENV HY_VERSION=0.19.0
# Thu, 03 Dec 2020 23:08:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 03 Dec 2020 23:08:09 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e8e82c9fb36b8f3a9b8f18fe1d88e4d425d5c45968e3f2e94cdbb1255feb4878`  
		Last Modified: Tue, 17 Nov 2020 20:26:45 GMT  
		Size: 27.8 MB (27766186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c05892d420f6daa83bbb25bbc544c83d49916a4491a2eac5e112a2b74543774`  
		Last Modified: Wed, 18 Nov 2020 03:21:06 GMT  
		Size: 2.8 MB (2752685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a6fd85801d2a3d93c6b415bfadf47e07687ad4c077efa2b7b84859d061b233`  
		Last Modified: Tue, 24 Nov 2020 00:58:46 GMT  
		Size: 40.4 MB (40353477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8acbb0c8d59169ba444a9e758fd097435815a30af31b374a5c48baa878a2d2`  
		Last Modified: Thu, 03 Dec 2020 22:50:27 GMT  
		Size: 2.6 MB (2562089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5addf07bcb9fc480de09b84e2729c552b7aa1053544231dcada527148f60ae4`  
		Last Modified: Thu, 03 Dec 2020 23:11:18 GMT  
		Size: 3.1 MB (3073777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.7` - linux; s390x

```console
$ docker pull hylang@sha256:8af6869dbf5345222c92af15b7e1fb2747696b2624fd96f2e7b929b27539878c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68830161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137644f98369166515b9b865d0052d4449f90e4862251cad2f89c39c1bcfe5c7`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Nov 2020 20:18:29 GMT
ADD file:4a3215d1c9b4afb58053c4fff8d121547890c2a71bc027992f7f960551c6acb1 in / 
# Tue, 17 Nov 2020 20:18:34 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 08:45:21 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 08:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:45:35 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Nov 2020 02:08:08 GMT
ENV PYPY_VERSION=7.3.3
# Tue, 24 Nov 2020 02:11:27 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='37e2804c4661c86c857d709d28c7de716b000d31e89766599fdf5a98928b7096' ;; 		arm64) pypyArch='aarch64'; sha256='ee4aa041558b58de6063dd6df93b3def221c4ca4c900d6a9db5b1b52135703a8' ;; 		i386) pypyArch='linux32'; sha256='7d81b8e9fcd07c067cfe2f519ab770ec62928ee8787f952cadf2d2786246efc8' ;; 		s390x) pypyArch='s390x'; sha256='92000d90b9a37f2e9cb7885f2a872adfa9e48e74bf7f84a8b8185c8181f0502d' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://downloads.python.org/pypy/pypy3.7-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -svT '/opt/pypy/bin/pypy3' '/usr/local/bin/pypy3'; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 03 Dec 2020 23:03:04 GMT
ENV PYTHON_PIP_VERSION=20.3.1
# Thu, 03 Dec 2020 23:03:05 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/91630a4867b1f93ba0a12aa81d0ec4ecc1e7eeb9/get-pip.py
# Thu, 03 Dec 2020 23:03:06 GMT
ENV PYTHON_GET_PIP_SHA256=d48ae68f297cac54db17e4107b800faae0e5210131f9f386c30c0166bf8d81b7
# Thu, 03 Dec 2020 23:03:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 03 Dec 2020 23:03:42 GMT
CMD ["pypy3"]
# Thu, 03 Dec 2020 23:19:02 GMT
ENV HY_VERSION=0.19.0
# Thu, 03 Dec 2020 23:19:18 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 03 Dec 2020 23:19:20 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c0d5e3cc51c0b20d3f68226f5332c9a9c2b17cce2f362ec742d4ed325ff7b530`  
		Last Modified: Tue, 17 Nov 2020 20:23:43 GMT  
		Size: 25.7 MB (25721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06da4eaae71448d5d56df06e497bf2c86e3c9a4ac05e252edab32b6109df773a`  
		Last Modified: Wed, 18 Nov 2020 08:51:09 GMT  
		Size: 2.4 MB (2432839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94b1b48629d0c97fc736330bf92ddbfffd059193f1ea41b357f6e6e472fa183`  
		Last Modified: Tue, 24 Nov 2020 02:15:12 GMT  
		Size: 35.0 MB (35038695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c3d15c39920fb734fcd2b2cd44de5560551770c47326ec29e909d607c80a93`  
		Last Modified: Thu, 03 Dec 2020 23:06:01 GMT  
		Size: 2.6 MB (2562638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6da3e0d1e2cd0abcd4ad843e1a0fe3ea2702e4ac9d3249c82a13129fa3e5bb`  
		Last Modified: Thu, 03 Dec 2020 23:24:06 GMT  
		Size: 3.1 MB (3074846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
