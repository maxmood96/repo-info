## `hylang:pypy2.7-jessie`

```console
$ docker pull hylang@sha256:c22edf390d12bbbc87293441935273d9bfa26c574fd3e17b8c1cbf5495974ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386

### `hylang:pypy2.7-jessie` - linux; amd64

```console
$ docker pull hylang@sha256:f10e2519ec7aac030eb32c2d33ff8a4101e25c570fcad395ce384dcbd806eccb
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72507324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2701c06def65a431316b348af74507bbdd178597889692e4c10f86fc794111`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:46 GMT
ADD file:bfa07c80ea2ec0396e781ef354835dbb10845a99934a7c7a226c2098b3641b6b in / 
# Sat, 28 Dec 2019 04:21:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 14:09:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 14:09:57 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 14:11:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libexpat1 		libffi6 		libgdbm3 		libsqlite3-0 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 14:11:52 GMT
ENV PYPY_VERSION=7.3.0
# Sat, 28 Dec 2019 14:16:20 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='f4950a54378ac637da2a6defa52d6ffed96af12fcd5d74e1182fb834883c9826' ;; 		arm64) pypyArch='aarch64'; sha256='a3dd8d5e2a656849fa344dce4679d854a19bc4a096a0cf62b46a1be127a5d56c' ;; 		i386) pypyArch='linux32'; sha256='eac1308b7d523003a5f6d20f58406d52ab14611bcec750122ae513a5a35110db' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy2.7-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 	find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Sat, 25 Jan 2020 02:43:48 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Sat, 25 Jan 2020 02:43:49 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/42ad3426cb1ef05863521d7988d5f7fec0c99560/get-pip.py
# Sat, 25 Jan 2020 02:43:49 GMT
ENV PYTHON_GET_PIP_SHA256=da288fc002d0bb2b90f6fbabc91048c1fa18d567ad067ee713c6e331d3a32b45
# Sat, 25 Jan 2020 02:46:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 25 Jan 2020 02:46:08 GMT
CMD ["pypy"]
# Sat, 25 Jan 2020 03:39:39 GMT
ENV HY_VERSION=0.17.0
# Sat, 25 Jan 2020 03:39:46 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 25 Jan 2020 03:39:46 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f79bccfe408cf63380358b522e6727a24da2086df8fc7dc7db005ccff874370d`  
		Last Modified: Sat, 28 Dec 2019 04:26:18 GMT  
		Size: 30.2 MB (30159553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5400236273a78f37138354743eef43ef595293b93315462ada52d66603e56fc`  
		Last Modified: Sat, 28 Dec 2019 14:21:38 GMT  
		Size: 2.8 MB (2811861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee31a0e76743132b5cfe3ef4692be412c478e7882a70a6c1c0b55ef42cc76de9`  
		Last Modified: Sat, 28 Dec 2019 14:21:49 GMT  
		Size: 34.8 MB (34833951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32893915bd3639921699ee9f586e0e25600abba47ab13e511c05629f77e3dfba`  
		Last Modified: Sat, 25 Jan 2020 02:48:04 GMT  
		Size: 2.2 MB (2179322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b4bd74b53ec9877a354df98716afff157698289f947b79ccf7ddf4ee53b433`  
		Last Modified: Sat, 25 Jan 2020 03:42:02 GMT  
		Size: 2.5 MB (2522637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy2.7-jessie` - linux; 386

```console
$ docker pull hylang@sha256:cdf0d5eeb7fe760c780daad40ec72439c4331a6e0d36b6ff9b8ef06de59c2c58
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74724171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0ef7758ea14de268eb627e74d692314175fb18df018346562c30de18a75a05`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 01 Feb 2020 16:39:59 GMT
ADD file:a8397e82c28512af775407c4f2370040b396f90e7de9b2d0eee7115b55903558 in / 
# Sat, 01 Feb 2020 16:39:59 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 04:35:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 04:35:43 GMT
ENV LANG=C.UTF-8
# Sun, 02 Feb 2020 04:38:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libexpat1 		libffi6 		libgdbm3 		libsqlite3-0 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 04:38:41 GMT
ENV PYPY_VERSION=7.3.0
# Sun, 02 Feb 2020 04:45:39 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='f4950a54378ac637da2a6defa52d6ffed96af12fcd5d74e1182fb834883c9826' ;; 		arm64) pypyArch='aarch64'; sha256='a3dd8d5e2a656849fa344dce4679d854a19bc4a096a0cf62b46a1be127a5d56c' ;; 		i386) pypyArch='linux32'; sha256='eac1308b7d523003a5f6d20f58406d52ab14611bcec750122ae513a5a35110db' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy2.7-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 	find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Sun, 02 Feb 2020 04:45:39 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Sun, 02 Feb 2020 04:45:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/42ad3426cb1ef05863521d7988d5f7fec0c99560/get-pip.py
# Sun, 02 Feb 2020 04:45:39 GMT
ENV PYTHON_GET_PIP_SHA256=da288fc002d0bb2b90f6fbabc91048c1fa18d567ad067ee713c6e331d3a32b45
# Sun, 02 Feb 2020 04:49:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sun, 02 Feb 2020 04:49:36 GMT
CMD ["pypy"]
# Sun, 02 Feb 2020 11:17:05 GMT
ENV HY_VERSION=0.17.0
# Sun, 02 Feb 2020 11:17:12 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sun, 02 Feb 2020 11:17:13 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3d294f17d11f8a748c70456b50961ca0b6b088d8a042fc72d556228e232aaa28`  
		Last Modified: Sat, 01 Feb 2020 16:45:04 GMT  
		Size: 30.3 MB (30304698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208a5790dd0801e3be21b4a4bbb450a26e96986fb9e0ef5d67f535538c28ed9c`  
		Last Modified: Sun, 02 Feb 2020 04:53:49 GMT  
		Size: 4.9 MB (4919991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b90b372fead610d33f30084830c7243864c1015a7dc902ee06e11d623d5248`  
		Last Modified: Sun, 02 Feb 2020 04:54:03 GMT  
		Size: 34.8 MB (34788697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4153661e6a27c02511bb4bafdad4defdb7d42ee74414dffef31b301d407f80`  
		Last Modified: Sun, 02 Feb 2020 04:53:48 GMT  
		Size: 2.2 MB (2183515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c9063eee0209c356dd29369bc4ccf9043747e4ceec4b02121bf50deb5a1e03`  
		Last Modified: Sun, 02 Feb 2020 11:18:54 GMT  
		Size: 2.5 MB (2527270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
