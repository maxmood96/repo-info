## `hylang:pypy3.7-buster`

```console
$ docker pull hylang@sha256:e7c7ca3d608e9b907a5d79aa89f28e340a8062792a2148d9e9f834dc59432875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:pypy3.7-buster` - linux; amd64

```console
$ docker pull hylang@sha256:4439585b780ecb460b100b5db3287da189899a90c556137a487a7f22d17ca11c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74140402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb9dfdc360b1e9d65d2e6e53b29cce9a9b535c3f8600e56102ac50c0bfce9c7`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 11:52:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 11:52:43 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 11:52:43 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 11:52:44 GMT
ENV PYPY_VERSION=7.3.9
# Tue, 13 Sep 2022 11:58:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.9-linux64.tar.bz2'; 			sha256='c58195124d807ecc527499ee19bc511ed753f4f2e418203ca51bc7e3b124d5d1'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.9-aarch64.tar.bz2'; 			sha256='dfc62f2c453fb851d10a1879c6e75c31ffebbf2a44d181bb06fcac4750d023fc'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.9-linux32.tar.bz2'; 			sha256='3398cece0167b81baa219c9cd54a549443d8c0a6b553ec8ec13236281e0d86cd'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.9-s390x.tar.bz2'; 			sha256='fcab3b9e110379948217cf592229542f53c33bfe881006f95ce30ac815a6df48'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 13 Sep 2022 11:58:46 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 13 Sep 2022 11:58:46 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 13 Sep 2022 11:58:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 13 Sep 2022 11:58:57 GMT
CMD ["pypy3"]
# Tue, 13 Sep 2022 15:34:13 GMT
ENV HY_VERSION=0.24.0
# Tue, 13 Sep 2022 15:34:13 GMT
ENV HYRULE_VERSION=0.2
# Tue, 13 Sep 2022 15:34:49 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 13 Sep 2022 15:34:49 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d73d09bc7558c6cb2b82390057493bca85484bdb043573c237385ec8cdc96a8`  
		Last Modified: Tue, 13 Sep 2022 12:04:10 GMT  
		Size: 2.8 MB (2765473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32e9c9e34ce284e257d471cac7447b5a6fce4ea02b7b761d4b4e7b499ce1fc9`  
		Last Modified: Tue, 13 Sep 2022 12:08:42 GMT  
		Size: 37.3 MB (37302455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2bfba90cb4b0a5e09633ec8459c8d29c1ff23966412250b46f13ff329141aaf`  
		Last Modified: Tue, 13 Sep 2022 12:08:35 GMT  
		Size: 3.0 MB (2966373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c953a086cd9a81620288eba677e924643f14f3c26abdc005bfd8c3ef7c5aad`  
		Last Modified: Tue, 13 Sep 2022 15:38:59 GMT  
		Size: 4.0 MB (3975549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.7-buster` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:058dc629ca62c0ecb371cfdfd330fc0e70aed72645ed189571d721b3ea0dc61f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69465699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b37ca3f03f128bc9ab01c4de502a9f9aca95842434405ed86034bc3e74335a5`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 13 Sep 2022 02:11:20 GMT
ADD file:18fa3591fcbf0c3e065dbe581a069fc2af6fab9e4446047348404881af960725 in / 
# Tue, 13 Sep 2022 02:11:21 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:22:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:22:12 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 12:22:13 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 12:22:14 GMT
ENV PYPY_VERSION=7.3.9
# Tue, 13 Sep 2022 12:29:52 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.9-linux64.tar.bz2'; 			sha256='c58195124d807ecc527499ee19bc511ed753f4f2e418203ca51bc7e3b124d5d1'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.9-aarch64.tar.bz2'; 			sha256='dfc62f2c453fb851d10a1879c6e75c31ffebbf2a44d181bb06fcac4750d023fc'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.9-linux32.tar.bz2'; 			sha256='3398cece0167b81baa219c9cd54a549443d8c0a6b553ec8ec13236281e0d86cd'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.9-s390x.tar.bz2'; 			sha256='fcab3b9e110379948217cf592229542f53c33bfe881006f95ce30ac815a6df48'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 13 Sep 2022 12:29:53 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 13 Sep 2022 12:29:53 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 13 Sep 2022 12:30:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 13 Sep 2022 12:30:07 GMT
CMD ["pypy3"]
# Tue, 13 Sep 2022 17:14:18 GMT
ENV HY_VERSION=0.24.0
# Tue, 13 Sep 2022 17:14:19 GMT
ENV HYRULE_VERSION=0.2
# Tue, 13 Sep 2022 17:15:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 13 Sep 2022 17:15:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4c3f5cce277263c7aeaf67f83255af76927e03363e775f39d7587bc5036fcf1e`  
		Last Modified: Tue, 13 Sep 2022 02:17:10 GMT  
		Size: 25.9 MB (25904152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f804c7250071a3303165ca11a87f26abd5794a011ad17ab1383282fcbd75af0`  
		Last Modified: Tue, 13 Sep 2022 12:38:12 GMT  
		Size: 2.6 MB (2634767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3287925f0d658cce7e5f269ffec764ba43086a282435f43d1c0e13d397bf5140`  
		Last Modified: Tue, 13 Sep 2022 12:42:53 GMT  
		Size: 34.2 MB (34202675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f13e847d2393c33810009d86c443d593f9d49ce6f69cbb096d2934dbed4462a`  
		Last Modified: Tue, 13 Sep 2022 12:42:47 GMT  
		Size: 2.7 MB (2748486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d998512297fe4fcb5cc92cc206bbcf82dc80d4e2175a7f26f590140384be18`  
		Last Modified: Tue, 13 Sep 2022 17:21:44 GMT  
		Size: 4.0 MB (3975619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.7-buster` - linux; 386

```console
$ docker pull hylang@sha256:b6ceb278000a358dca5b9fdca207c9fd3975dfcd72e0d8d857521aef62544d94
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76388640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc47e40b52cf76bf792c7eb22f228c7873f7bb564650b1d70c022008bc6f9a5`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Oct 2022 23:40:08 GMT
ADD file:b1ef7e7f4c48770bde0d19751bb1624a887b657a5a5ab5d453fd5365b3448618 in / 
# Tue, 04 Oct 2022 23:40:09 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 08:43:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 08:43:22 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 08:43:23 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 08:43:24 GMT
ENV PYPY_VERSION=7.3.9
# Wed, 05 Oct 2022 08:51:08 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.9-linux64.tar.bz2'; 			sha256='c58195124d807ecc527499ee19bc511ed753f4f2e418203ca51bc7e3b124d5d1'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.9-aarch64.tar.bz2'; 			sha256='dfc62f2c453fb851d10a1879c6e75c31ffebbf2a44d181bb06fcac4750d023fc'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.9-linux32.tar.bz2'; 			sha256='3398cece0167b81baa219c9cd54a549443d8c0a6b553ec8ec13236281e0d86cd'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.9-s390x.tar.bz2'; 			sha256='fcab3b9e110379948217cf592229542f53c33bfe881006f95ce30ac815a6df48'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 05 Oct 2022 08:51:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 05 Oct 2022 08:51:09 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 05 Oct 2022 08:51:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 05 Oct 2022 08:51:24 GMT
CMD ["pypy3"]
# Wed, 05 Oct 2022 18:23:40 GMT
ENV HY_VERSION=0.24.0
# Wed, 05 Oct 2022 18:23:41 GMT
ENV HYRULE_VERSION=0.2
# Wed, 05 Oct 2022 18:24:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 05 Oct 2022 18:24:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d1d1dd08a5009b10b72285f23ffd4c1978d3445cc3855d22f4112018b15a9420`  
		Last Modified: Tue, 04 Oct 2022 23:46:26 GMT  
		Size: 27.8 MB (27797501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173aa2dbac2315880d15de506a472178fac3153453d1488a27818acb8139284e`  
		Last Modified: Wed, 05 Oct 2022 08:59:52 GMT  
		Size: 2.8 MB (2777853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b667236d3006d5f9ca103fa22c95b764a8c85dfb8f74d6270cc4e17ad356f72`  
		Last Modified: Wed, 05 Oct 2022 09:04:43 GMT  
		Size: 39.1 MB (39088939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d058e5dfcf3deff46ec6fb798691f0ec24f65be3a8de0ca709820d4b4eac963b`  
		Last Modified: Wed, 05 Oct 2022 09:04:37 GMT  
		Size: 2.7 MB (2748684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f8a15c779df1c846bef494e3c56cfda841a236e5b1648c84bdbb4696f729a6`  
		Last Modified: Wed, 05 Oct 2022 18:34:18 GMT  
		Size: 4.0 MB (3975663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
