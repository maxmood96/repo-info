## `hylang:0-pypy2.7-jessie`

```console
$ docker pull hylang@sha256:f38919c6b346f883345290cb51a04b273cde8b760bcaad3da1725f944cff333d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386

### `hylang:0-pypy2.7-jessie` - linux; amd64

```console
$ docker pull hylang@sha256:40b2863555272a6c23658ee6a2555779c7850790f5ebb8c5d54a0ba6047440bf
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72470991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444e51753d893162126890fed8c8ecb5701ef6a7894e09c0d9935fe91dffccae`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 22 Nov 2019 14:56:04 GMT
ADD file:41e78f98c436ed4f05c337e67e10439bb860bbea86c78368cc0e80100026cf40 in / 
# Fri, 22 Nov 2019 14:56:04 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:59:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Nov 2019 00:59:21 GMT
ENV LANG=C.UTF-8
# Sat, 23 Nov 2019 01:01:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libexpat1 		libffi6 		libgdbm3 		libsqlite3-0 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Dec 2019 23:08:14 GMT
ENV PYPY_VERSION=7.3.0
# Thu, 26 Dec 2019 23:12:53 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='f4950a54378ac637da2a6defa52d6ffed96af12fcd5d74e1182fb834883c9826' ;; 		arm64) pypyArch='aarch64'; sha256='a3dd8d5e2a656849fa344dce4679d854a19bc4a096a0cf62b46a1be127a5d56c' ;; 		i386) pypyArch='linux32'; sha256='eac1308b7d523003a5f6d20f58406d52ab14611bcec750122ae513a5a35110db' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy2.7-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 	find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 26 Dec 2019 23:12:54 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Thu, 26 Dec 2019 23:12:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Thu, 26 Dec 2019 23:12:54 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Thu, 26 Dec 2019 23:15:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 26 Dec 2019 23:15:27 GMT
CMD ["pypy"]
# Fri, 27 Dec 2019 04:18:27 GMT
ENV HY_VERSION=0.17.0
# Fri, 27 Dec 2019 04:18:34 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 27 Dec 2019 04:18:34 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:02d147d362835efa14b8a83e3b4a7dd20dd53dd0ba1619316a691acb9e614c13`  
		Last Modified: Fri, 22 Nov 2019 15:03:20 GMT  
		Size: 30.2 MB (30159468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739e238c2628b72e5b5fc22a054b55be6c60fdc578b99c2539b5267891464028`  
		Last Modified: Sat, 23 Nov 2019 01:10:40 GMT  
		Size: 2.8 MB (2811806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8339f98ebb2138f89ed84f9088fb4b10a946dfb7442dd61f468e9bac81436f`  
		Last Modified: Thu, 26 Dec 2019 23:19:27 GMT  
		Size: 34.8 MB (34834078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f45eb516ed2408efa87016bc569d1ac3018913e309597c5352fcc6e3519877`  
		Last Modified: Thu, 26 Dec 2019 23:19:16 GMT  
		Size: 2.2 MB (2162153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c90fd3abbe75ab29e2d6914594d62d4af1fe42d9ec1327f001a2430419e4fa`  
		Last Modified: Fri, 27 Dec 2019 04:19:47 GMT  
		Size: 2.5 MB (2503486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy2.7-jessie` - linux; 386

```console
$ docker pull hylang@sha256:28f5b6fd9efb55c9d28fa66df33b23c3431ae18210065509bf5aa316e5c3a965
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74678888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a562611bd234d05027778c6116ffd15772a172c7437871cb21a7fac4dc87fc37`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 28 Dec 2019 04:39:58 GMT
ADD file:02e7c1b9293024ca07d0f82236c5c2c75c8d87a30a7194281c030d008d8dc074 in / 
# Sat, 28 Dec 2019 04:39:59 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 14:42:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 14:42:31 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 14:45:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libexpat1 		libffi6 		libgdbm3 		libsqlite3-0 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 14:45:29 GMT
ENV PYPY_VERSION=7.3.0
# Sat, 28 Dec 2019 14:52:24 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='f4950a54378ac637da2a6defa52d6ffed96af12fcd5d74e1182fb834883c9826' ;; 		arm64) pypyArch='aarch64'; sha256='a3dd8d5e2a656849fa344dce4679d854a19bc4a096a0cf62b46a1be127a5d56c' ;; 		i386) pypyArch='linux32'; sha256='eac1308b7d523003a5f6d20f58406d52ab14611bcec750122ae513a5a35110db' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy2.7-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 	find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Sat, 28 Dec 2019 14:52:25 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 28 Dec 2019 14:52:25 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 28 Dec 2019 14:52:25 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 28 Dec 2019 14:56:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 28 Dec 2019 14:56:22 GMT
CMD ["pypy"]
# Sun, 29 Dec 2019 00:15:36 GMT
ENV HY_VERSION=0.17.0
# Sun, 29 Dec 2019 00:15:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sun, 29 Dec 2019 00:15:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4e362b2cf6b22bfbf170bdeea97d1e7c3cb1f3508a60e8102479f0a51d3cdd7f`  
		Last Modified: Sat, 28 Dec 2019 04:44:56 GMT  
		Size: 30.3 MB (30304704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fba055a94c70a2dbde39451e8c683f67fc2fda782c515e7f798a64834ab5a2`  
		Last Modified: Sat, 28 Dec 2019 15:00:15 GMT  
		Size: 4.9 MB (4920020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443d39cb9df06c0c73b8b879ae48c285227f8af288c726ea586da6be3bc5347c`  
		Last Modified: Sat, 28 Dec 2019 15:00:32 GMT  
		Size: 34.8 MB (34788688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bc43441a42e0ab98f87b74b60708941ae2d96e760c6a4164f52e863636c8ef`  
		Last Modified: Sat, 28 Dec 2019 15:00:13 GMT  
		Size: 2.2 MB (2162059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa586ae3cda8825f9a1290c55634727f61d6195cc1d5e810b8a23ee249bef0b`  
		Last Modified: Sun, 29 Dec 2019 00:18:18 GMT  
		Size: 2.5 MB (2503417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
